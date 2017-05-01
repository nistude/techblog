+++
categories = ["lessons learned"]
date = "2017-04-30T16:00:41+02:00"
description = "how to properly push metrics to prometheus pushgateway"
featured = ""
featuredalt = ""
featuredpath = ""
linktitle = ""
title = "Losing metrics with the prometheus pushgateway"
type = "post"

+++

At work, we use [Prometheus](https://prometheus.io/) together with its
[pushgateway](https://github.com/prometheus/pushgateway) to monitor and alert
on backup job execution.

The other day we noticed a failing backup job that did not trigger an alert.
Debugging quickly revealed that the pushgateway was losing metrics. Our
metrics look like this:

```
backup_last_success_unixtime{instance_name="some_hostname", job="backup_job"}
```

We have several jobs with the same `job` label, running on different hosts,
thus I thought these would be recorded as different timeseries. But I
oversaw a small detail in pushgateway's documentation: metric grouping.

When pushing metrics to the pushgateway, you can add metric labels in two
ways:

1. add the label to the URL you are pushing to (`job` label in the example
   below)
2. add the label to the metric name in the body of the POST request
   (`instance_name` label in the example below)

```sh
cat <<EOF | curl --data-binary @- http://my.pushgateway:9091/metrics/job/backup_job
# TYPE some_metric counter
some_metric{instance_name="hostname1"} 42
EOF
```

My understanding was that it doesn't matter which way you record the labels.
Labels on metrics are all equal, right? What I missed was, that labels
mentioned in the URL are used to group metrics together. So if, in the example
above, two jobs `backup_job` push metrics, one with `instance_name="hostname1"`
and one with `instance_name="hostname2"`, pushgateway will only present one
metric to prometheus with alternating values for `instance_name`.

## Lesson learned

The pushgateway distinguishes metrics based on their URL.
