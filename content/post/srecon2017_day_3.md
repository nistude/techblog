+++
categories = []
date = "2017-09-02T22:09:46+02:00"
description = ""
featured = ""
featuredalt = ""
featuredpath = ""
linktitle = ""
title = "SREcon Europe 2017 -- Day 3"
type = "post"

+++

With a short delay, the recap of the final day 3 of SRECon Europe 2017. In
the morning I jumped around quite a bit, so I didn't get much of a coherent
experience.

## Statistics for Engineers

This workshop was held by
[Heinrich Hartmann](https://www.usenix.org/conference/srecon17europe/program/presentation/hartman)
from Circonus.

> Statistics is the art of extracting information from data. In this workshop,
> we will visit the statistical methods that are relevant for operating
> modern IT infrastructures. Containerized cloud architectures are incredibly
> difficult monitoring targets. Creating probabilistic models of the
> behaviors of these systems, that can be used for reliable predictions is a
> very difficult task. In fact, it's so difficult that I don't think anyone
> has done that, yet. We will certainly not try to here.
>
> Instead, we will take a different path in this workshop, and talk about
> statistical methods that are known to work and provided value for your daily
> job as a SRE. In this workshop you will learn:
>
> * How to measure the quality of APIs you provide and consume.
> * How to interpret the telemetry data that is emitted from the systems you
> are running.
> * How to aggregate metrics from single nodes to service-level views.
>
> Topics we will cover in depths include: data visualisation, averages,
> percentiles, histograms, regressions, robustness and mergeability. We will
> cover the material from a theoretical and a practical perspective. Bring
> pen and paper as well as your laptop!

I only stayed for the first 25 minutes or so and then left for...

## Distributed Systems, Like It or Not

After yesterdays workshop about distributed systems, finally a crisp talk by
[Theo Schlossnagle](https://www.usenix.org/conference/srecon17europe/program/presentation/schlossnagle-distributed-systems)
from Circonus.

> Over the last twenty years, complex distributed systems have been deployed to
> solve the leading challenges in the systems resiliency and robustness realm.
> At this point in systems architecture design, distributed systems are
> everywhere in everything; even the most simple architectures incorporate
> distributed software and carry with that the failure scenarios they bring.
>
> SREs are put in an even more complicated situation, because of their wide net
> or responsibilities, to manage distributed systems of distributed systems.
> Things can and will go wrong and one of the fundamental skills for SREs going
> forward will be strong distributed systems reasoning skills.
>
> In this talk we discuss the types of failure scenarios that distributed
> systems bring with them (with anecdotes) and develop various reasoning skills
> that can be used to tackle these challenges with increased confidence.

Theo is one of those icons of our times, funny and opinionated. As I hadn't
joined his workshop about distributed systems the previous day, I was very much
looking forward to this crisp presentation. Unfortunately, 30 minutes was just
too little time to get into any meaningful detail. In retrospect, I wish I had
gone to his workshop instead.

## The EU's New Data Protection Law - a Survival Guide

Finally I joined the other long morning session by
[Simon McGarr and John Looney](https://www.usenix.org/conference/srecon17europe/program/presentation/mcgarr)
only to find out that they hadn't moved past slide 1 in over 60 minutes!

> What data do you hold?  Are you processing the data, or controlling it?  Do
> you have the consents to use that data like that?  Do you have a register of
> all that data and every way you use it, and what for?  Can you find every
> piece of data you hold that relates to an individual, copy it and send it to
> them—for free—within 30 days?  What happens when they say they want it
> erased?
>
> The General Data Protection Directive comes into force on the 25th May 2018.
> New powers mean regulators can impose fines for breaches up to 4% of annual
> turnover. This workshop is for anyone trying to make sure that their
> organisation isn't in breach by the implementation date.
>
> GDPR isn't just a compliance project. It's a business culture change project.
> Let's struggle our way through together.

There is a certain kind of lawyer that is funny as hell to listen to, Simon
McGarr is one of them. The reason they hadn't moved past slide 1 was, that
this session was kind of a guided Q&A around Europe's new *General Data
Protection Directive*. Insightful and entertaining, I happily joined for a
2nd dose after the break.

## Panel: AMA for New SREs

After lunch, I struggled again which session to go to and finally decided to
join this panel, hoping to see the recording of Theo Schlossnagle's second
talk of the day later.

Panelists where Gráinne Sheerin, John Looney, Chris Sinjakli, Ola Klapcinska
with
[Murali Suriar](https://www.usenix.org/conference/srecon17europe/program/presentation/suriar-panel)
as moderator.

> If you're new to SRE, or considering becoming an SRE, and you have questions,
> come to this session. You'll get the opportunity to ask a variety of
> experienced SREs for their opinion on topics related to SRE teams and
> culture, hiring, oncall, troubleshooting, performance, release management,
> and more.

This was quite an insightful conversation. Too many points to list here
individually but definately one of the sessions that made the whole conference
a success for me. All my questions where answered even without me asking them
and answers to other questions gave me lots of food for thought. We even
extended the session well into the break before it was time getting back into
the large conference room for the closing plenary session.

## Have You Tried Turning It off and Turning It on Again?

[Tanya Reilly](https://www.usenix.org/conference/srecon17europe/program/presentation/reilly),
SRE at Google, started off the closing plenary session with her talk on
disaster recovery.

> Most of us have a backup strategy, many of us have a restore strategy and
> several of us have a fully tested restore strategy. But backups are not the
> whole story. I'll talk about the parts of disaster recovery we're less
> prepared for, and dependencies that you might not think about until one day
> when you really do turn an entire service, entire site or (perish the
> thought!) an entire company off and on again.
>
> This talk will cover managing complexity, testing your fallback plan and
> avoiding dependency cycles that make it impossible to restart groups of
> systems. Like, where do you store the documentation on how to recover the
> documentation server?

This was a talk about an important topic but I couldn't find enough depth to
make it meaningful to me.

## 100 Teams, 100 Ways to Fail

Next up where
[John Keiser and Ben Broderick Phillips](https://www.usenix.org/conference/srecon17europe/program/presentation/keiser)
from Microsoft with some dramatized experience reports from their SRE work.

> Every SRE organization hits the same problems at some point: How do we
> convince teams to let us help, and own the work and results together? As an
> SRE, you will encounter different kinds of resistance from the teams you work
> with.
>
> Azure has 100+ teams, and Azure SRE has gained experience with every type of
> engagement on the map. If any of these scenarios sound familiar to you:
>
> * Engineers that do not understand your utopian visions (nobody understands
>   me)!
> * Everyone is rational, no one is right
> * “This too shall pass” i.e. the team that knows you will eventually sort out
>   the rough edges in your tooling or find another job, and can safely ignore
>   you until then
>
> Come join Azure SRE as we share stories about teams we’ve worked with, the
> resistance we’ve run into, and sometimes even how we fixed it.

Comedy, sometimes funny, often times not so much. In the end the talk concluded
with 3 points that could have been presented in a lightning talk as well.

When engaging SRE with a new team:
1. live their problems
1. show how you can help, don't tell what the team needs to change
1. be happy when they don't need you anymore

## Persistent SRE Antipatterns

[Jonah Horowitz and Blake Bisset](https://www.usenix.org/conference/srecon17europe/program/presentation/horowitz)
also packaged their messages in comedy, only they had more content and where
more funny.

> What isn’t Site Reliability Engineering? Does your NOC escalate outages to
> your DevOops Engineer, who in turn calls your Packaging and Deployment Team?
> Did your Chef just sprinkle some Salt on your Ansible Red Hat and call it
> SRE? Lots of companies claim to have SRE teams, but some don’t quite
> understand the full value proposition, or what shiny technologies and
> organizational structures will negatively impact your operations, rather than
> empowering your team to accomplish your mission.
>
> You’ll hear stories about anti-patterns in Monitoring, Incident Response,
> Configuration Management, and more that we’ve tripped over in our own
> teams, seen actually proposed as good practice in talks at other
> conferences, and heard as we speak to peers scattered around the industry.
> We'll also discuss how Google and Netflix each view the role of the SRE,
> and how it differs from the traditional Systems Administrator role. The
> talk also explains why freedom and responsibility are key, trust is
> required, and when chaos is your friend.

As there was no overarching topic, content wise, there's no point listing all
their individual points. Suffice to say, they had quite a wealth of experience
and for someone new to SRE, there where a few hidden gems.

## Conclusion

This concludes SRECon Europe 2017 for me. It was quite a nice conference and
I am lucky I got the chance to attend.

As I am still new to the concept of SRE, I got lots of input from this
conference and see myself attending again next year. I only wish for there to
be *less* tracks, as many tracks just increase the chance of conflicts of
interest.
