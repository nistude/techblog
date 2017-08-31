+++
categories = []
date = "2017-08-30T20:35:23+02:00"
description = "day 1 summary of srecon 2017 in dublin, ireland"
featured = ""
featuredalt = ""
featuredpath = ""
linktitle = ""
title = "SREcon Europe 2017 -- Day 1"
type = "post"

+++

I am currently in Dublin, Ireland, for SRECon Europe/Middle East/Africa 2017.
The day started right off with a surprise at the registration desk, I wasn't
on the list of participants. Luckily the issue could be resolved quickly and
I could enter the conference area.

## Care and Feeding of SRE

The first keynote was delivered by
[Narayan Desai](https://landing.google.com/sre/book.html),
an SRE manager from Google.

> As SRE enters the ops zeitgeist, much of the focus has been placed on
> tactics--techniques that individual operations teams can adopt to improve
> their effectiveness. While there is value in singleton adoption, I'll make
> the case in this talk that organizational support and culture across the
> organization that corresponds with these tactics results in impact far
> greater than the sum of its parts. I'll focus on three SRE goals: maintaining
> SLOs, managing operational load, and maximizing leverage, and discuss failure
> modes without sufficient organizational support. These aren't tactics that
> can be fully implemented by an operations team. SRE is an organizational
> strategy that need to be adopted by the business.

With him being at Google for only a year, he tried to give an outsider's
perspective on SRE and the underlying values at Google. He identified these
as

1. Reliability is paramount
1. Precise promises
1. Assuming best intentions

However, the summary's last sentence is probably the most important aspect of
his talk. Similar to DevOps, which never was about techniques, SRE also is
not about techniques. Instead it is an organizational architecture whose values
enable tactics. Let's see how many organizations keep this in mind when
adopting this approach...

## Diversity and Inclusion in SRE

The second keynote was by
[Niall Murphy](https://www.usenix.org/conference/srecon17europe/program/presentation/murphy-postmortem)
from [SRE book fame](https://landing.google.com/sre/book.html).

> Whether a cause or a consequence of diversity & inclusion problems, members
> of minority groups in SRE experience harassment, bullying, and anti-social
> exclusion far too often. Although primarily an ethical and behavioural issue,
> it also has extremely costly negative effects on team effectiveness,
> arising from loss of psychological safety and even attrition. The data
> supporting these assertions are reasonably clear, but what is perhaps less
> clear is what to do about it.
>
> We therefore analyse the situation in the form of a postmortem, suggesting
> some root causes, presenting a timeline, and analysing factors which
> contributed to (and offset) The Incident, and propose some actions to
> remediate.

The experience of this talk was kind of strange, as I listened only with one
ear, while thinking more about situations at work that felt related.

## SRE 101

As first regular talk, I went with
[Laura Nolan](https://www.usenix.org/conference/srecon17europe/program/presentation/nolan),
a Google SRE.

> The purpose of an SRE team is to keep its services up, reliable, performant
> and efficient. How do effective SRE teams do this?
>
> We'll run through an overview of key SRE competencies: monitoring and
> alerting, incident response, disaster recovery, performance and efficiency,
> change management and capacity planning.
>
> We'll also look at the habits of successful SRE teams and some common
> pitfalls.

This was a quick and unfortunately overloaded, overview of site reliability
engineering with lots and lots of details but hardly any depth. In retrospect
I would have preferred a more high level introduction focusing more on concepts
than technical details. However, I found quite some value in the words she
spoke beyond what was written on the slides, making this talk worth my while.

## Bots Are Fast, Humans Are Smarter

In the afternoon I skipped a few sessions and then joined
[Felix Glaser](https://www.usenix.org/conference/srecon17europe/program/presentation/glaser)
for an exploration of the shoe buying bot community (sic!).

> In a world with ever-growing DDoS attacks, L7 attacks give even the most
> experienced engineers the sweats. Imagine if instead of following easy to
> detect patterns, bots could mimic the behaviour of customers. Well, that’s
> exactly what Shopify sees every day during flash sales.
>
> Come and learn how we block nearly all bot traffic on our load balancers
> without any human intervention. We will share our challenges of
> differentiating between web crawlers and bots, users behind NATs and bots
> rotating user agents, as well as fast humans and browser extensions. When the
> stakes are blocking a customer completing a checkout, misclassification isn’t
> an option.
>
> This is not yet another machine learning talk, but an example of how simple
> statistics, heuristics and some sane limits can give great results with
> minimal complexity. The lessons learned in this talk are applicable to any
> real-world problem with inexact constraints.

This talk was amazing because of the problem he was trying to solve: prevent
bots from buying limited edition sneakers. While the setup created quite a
few laughs, unfortunately he couldn't follow through with details on how he
actually stopped the bots. He could only point to the ideas they implemented
on a high level, like TCP fingerprinting with [p0f](http://lcamtuf.coredump.cx/p0f3/)
and comparing the detected operating system with the User-Agent header. However,
what keeps my mind busy is his final recommendation: once you detect a bot,
don't let them know. Otherwise you find yourself in a full blown arms race with
bot developers.

## Google SDN Peering: An Early Engagement Case Study

My final talk for the day was by
[Murali Suriar](https://www.usenix.org/conference/srecon17europe/program/presentation/suriar-early),
a Google SRE.

> How do you build a new SRE team around a completely novel product? This talk
> will deal with some of the challenges involved in launching Espresso,
> Google's software defined peering architecture.
>
> * How do you build an SRE team for a product which isn't serving real users yet?
> * How do you build a cohesive team and structure out of many disparate teams? (Networking, SRE, software development)
> * How do you build on call discipline in a team which largely hasn't been oncall before?
>
> And as an aside, we'll also get into some of the technical details of
> Espresso, since it's necessary to understand what made it so challenging and
> different.

This talk was quite interesting by explaining how Google got started with SDN,
however, the content didn't quite match the title or abstract. Most of the
talk was about SDN and the history of networking at Google, with only a few
final minutes on team challenges and SRE.

This concludes my first day at SRECon and I am looking forward to a day packed
full of interesting talks tomorrow. The only downer is, that many of them are
scheduled in parallel, whereas other times I expect more leisure time. The
curse of the multi-track conference...
