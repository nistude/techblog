+++
categories = []
date = "2017-08-31T22:21:56+02:00"
description = ""
featured = ""
featuredalt = ""
featuredpath = ""
linktitle = ""
title = "SREcon Europe 2017 -- Day 2"
type = "post"

+++

Another day of inspiring talks and discussions is coming to an end. I spend
most of my time in Track 1 on *Setting up SRE teams and engagements*.

## Setting Up SRE in a Global Financial Organization

My first talk of the day was by
[Janna Brummel and Robin van Zijll](https://www.usenix.org/conference/srecon17europe/program/presentation/brummel)
of ING.

> By now, most of us have read the O’Reilly book about Google SRE or have heard
> of other tech companies’ SRE teams. Our story is about doing SRE in a more
> traditional and more regulated environment: in the largest bank in the
> Netherlands.
>
> This talk will address the history, present and future of SRE within a
> financial institution with a BizDevOps way of working. In doing so, we will
> talk about how our journey started at SREcon in Dublin last year, why we
> wanted and need to do SRE within ING, how our SREs started, the distributed
> way of working of SRE within ING, what technologies we actually work with and
> why, and our plans for the future.
>
> Lastly, we will share our SRE dos-and-donts after a year of experience. We
> hope our talk inspires engineers or tech leads to start doing SRE within
> their (possibly more traditional) company and that those who already
> implemented SRE can learn from our journey.

This was the first in a series of experience reports from companies other
than Google on their journey towards SRE.

One notable difference between their take and Google's was that SREs at Google
own the production service, whereas SREs at ING see themselves rather as
enabler and supporter of development teams. They follow the *you build it, you
run it* paradigm.

Also interesting was a pointer to
[Dickerson's hierarchy of service reliability](https://www.david-merrick.com/2017/06/26/dickerson-s-hierarchy-of-service-reliability/).

## From Firefighting to Proactive Work

Next up was
[Alex Gerlic](https://www.usenix.org/conference/srecon17europe/program/presentation/gerlic)
from Intercom.

> Due to an incident on our main datastore, we react and spent an entire week
> trying to keep Intercom up, with the help of 20 engineers from other teams.
> During this tough week, we had obliged to drop any other projects and focus
> on building a firefighting organization.
>
> After the urgency period, it became evident to us that we need to focus on
> reactive work to prevent the incident from happening again. It was the
> launch-pad for the conception of a brand-new organization for our team,
> focusing on ownership and high impact work.
>
> Few months after, results ruled in favour of our hard work: we’ve reduced
> system interruptions by more than 80% ! But good news and radical changes
> also come with consequences: we need to deal with multiple implications and
> drastically change our way to work as a team
>
> During this talk we will cover:
>
> * our journey from a firefighting to a proactive work organization
> * good and bad organizational decisions we made
> * impacts on the morale of the team

The interesting insight here was to keep an eye on the team when evaluating
your current situation. After they mitigated their immediate technical problems,
they couldn't just move on and build great infrastructure, because the team
was still depleted from missing direction and regular pages. Only after they
approached these topics and morale increased, could they start working really
proactively.

## Building a Culture of Reliability

Pagerduty's Director of Engineering
[Arup Chakrabarti](https://www.usenix.org/conference/srecon17europe/program/presentation/chakrabarti)
started the second session of the day.

> Getting customers to care about Reliability is hard. Getting stakeholders to
> care about Reliability is harder. Getting the entire company to care about
> Reliability is even harder.
>
> In this talk, I will cover what steps that every leader in any organization
> can take to get more people to care about Reliability. Because Reliability is
> one of those things that people only notice when it goes in the wrong
> direction, it can be hard to show the value of it and why it is so important.
>
> We will walk through cultural and management changes, metrics to watch and
> obsess over, and some tooling that can help along the way.

Quite a few interesting points in this talk.

When you talk about reliability, you better have convincing metrics. Depending
on whom you are talking to and your business model, this can be easier or
more complicated. In a transactional business, like we have at my current
employer HolidayCheck, *money per time* is quite convincing for business
people. If you have a subscription model, this can be much harder, as
degradations slowly erode user trust which you can't measure in real-time.

I particularly liked their concept of *Failure Friday* where their *Chaos Cat*
would randomly reboot or degrade some service and all engineers would sit
together and fix any upcomming issues.

They also open-sourced their
[incident response documentation](https://response.pagerduty.com/)
which is cerainly a worthy read.

## Building an SRE Capability Inside a Large Organization

[Sriram Gollapalli](https://www.usenix.org/conference/srecon17europe/program/presentation/gollapalli)
talked about the challenges he faces in a more classical organization that
still largely depends on shipping CDs(!) to customers.

> Agilent Technologies, while traditionally known as a hardware company, has
> started to deliver several Software-as-a Service offerings through
> acquisitions and in-house product development. This talk will discuss how to
> transform the thinking across a decentralized, large corporate organization
> to approach software delivery differently. Traditionally, we are used to
> delivering software by burning and shipping CDs/DVDs with annual release
> cycles. Fast-forward to today with SaaS products using CI/CD approaches, etc
> and releasing as frequently as twice a week, this requires a completely
> different operating model and doesn’t fit in the traditional organizational
> framework/processes.

I didn't quite get the point of this talk. It would certainly be interesting
to see in 1-2 years how this company fared with their SRE introduction, given
that they still ship CDs to customers and have release cycles measured in
months. But just talking about their intentions and plans for the near future
isn't really enlightening.

## The Why, What, and How of Starting an SRE Engagement

[Richard Clawson and Josh Gilliland](https://www.usenix.org/conference/srecon17europe/program/presentation/clawson)
from Microsoft Azure told us some stories about one of their engagements.

> One of the hardest things to do is trust an outside voice. What are the
> boundaries between live site features and service features? How much
> expertise is required to be on-call? Who decides what’s in the best interests
> of the service? How is this not another Ops team or a staff augment? Who’s
> "in charge" and who makes prioritization calls? How do you build mutual
> trust? These are just some of the challenges in building a successful
> partnership between a product group and SRE.
>
> In this talk we will present what we learned about the technical,
> organizational, and political systems that were needed to provide SRE to
> the Azure Internet-of-Things product group and how this can be used as a
> template for your services. We will discuss how to start an engagement,
> build partnerships and trust across organizations, provide ROI, keep a
> distinct identity and the frameworks that were developed to maintain tight
> organizational alignment including a new take on error budgets.

The stories told had a recurring theme of SREs patronizing the development
team they engaged with and how they overcame this arrogance. The main
take away for me was to overcome this patronizing attitude and instead
assume best intentions on the side of the team. Instead approach the situation
with a learner's mind, be curious, and ask questions to *really* understand
what's going on before jumping to conclusions.

## The Never-Ending Story of Site Reliability

Linkedin's
[Kurt Andersen](https://www.usenix.org/conference/srecon17europe/conference-program/presentation/andersen)
finally pulled me out of track 1.

> I strongly believe that the commonly proposed bogey-man of "automating
> ourselves out of a job" betrays a simplistic and highly incomplete
> understanding of the SRE field. SRE teams can always grow and develop.
>
> The Dreyfus model is a model of professional expertise that plots an
> individual's progression through a series of five levels: novice, advanced
> beginner, competent, proficient, and expert. The idea in this talk is to take
> aspects of SRE practice (such as monitoring, measurement against SLOs,
> incident management and postmortems, etc) and provide indications of what
> these look like at the different Dreyfus levels - not so much at an
> individual level as at an organizational one.
>
> Often, companies and teams will show uneven levels of proficiency -
> frequently due to pressures to develop some areas more than others. The
> intent of this talk is to provide a framework within which attendees can
> gauge their own company's progress and anticipate/plan for growing weak
> areas.
>
> The concepts for this talk have emerged through exposure to companies at
> different skill/experience levels. It is not by any means definitive, but I
> hope to provide a useful rubric for discussion.

This was another talk I didn't quite get. On the one hand he wanted to talk
about *automating ourselves out of a job*, on the other hand he gave examples
of some core SRE practices and how they would look on different levels of the
[Dreifus model of skill acquisition](https://en.wikipedia.org/wiki/Dreyfus_model_of_skill_acquisition).
I really don't understand what one has to do with the other.

## Hiring SREs May Be Literally Impossible

The last talk of the day was by
[Chris Sinjakli](https://www.usenix.org/conference/srecon17europe/program/presentation/sinjakli),
an SRE from GoCardless.

> If we're gonna do this SRE thing, we need to find the right people to do it.
>
> After a few recent discussions, it became clear just how much everyone—at
> large companies and small—is struggling to find those people.
>
> You can barely get enough applicants in the door, and by the time you've run
> your interview process you're left making a handful of offers.
>
> Hiring SREs from the outside world is a competitive, expensive game to play.
> So why focus so much on people outside your company? You've got potential
> SREs sat all around you!
>
> In this talk, we'll set the scene with a little look at the realities of
> hiring SREs. We won't stay there for too long though, because that's not
> what's going to save us!
>
> The bulk of the talk will be spent looking at ways to discover budding SREs
> in your organisation, how to nurture their interest, and how to coach them in
> a role that's new to them.

He pointed out the extraordinary requirements for SRE candidates: both, broad
*and* deep technical knowledge. [T-shaped skills](https://en.wikipedia.org/wiki/T-shaped_skills)
don't cut it anymore. At GoCardless, they hired less than 2% of their SRE
candidates. As an alternative, he suggested hiring interested people internally
and how to onboard them successfully.

This concludes my second day at SRECon Europe 2017. From the program, it looks
like tomorrow is the day with most interesting talks, unfortunately all taking
place in parallel...
