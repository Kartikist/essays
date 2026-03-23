---
layout: post
title: "The Minimum Effective Dose"
date: 2026-03-23
---

There's a concept in medicine called the minimum effective dose: the smallest amount that produces the desired effect. 
Anything above it is just side effects, anything below doesn't work. Engineering has an equivalent. The discipline isn't in knowing the solution. It's in knowing where the solution stops.


There's a particular kind of waste that's invisible because it looks exactly like work.
Four months. Three engineers. A full ERP reimplementation for an educational institution: student records, payment histories, inventory lists, invoices, receipts. The kind of data that, if you're honest about it, lives quite comfortably in a well-organised spreadsheet. Everything we built, the database schemas, migration scripts, custom interfaces, could have been replaced with a structured excel template and a weekend of careful manual entry.
The engineering was sound. It was also, in the most precise sense, unnecessary.
I knew this from roughly week two. I had a feeling I couldn't shake — low-grade, like wearing a shoe on the wrong foot. Not painful enough to stop. Just wrong enough to notice. The feeling had a question inside it: does this need to be this hard?

That same feeling showed up later, in a different job, at a much smaller scale.
Our team had a deployment ritual. Every week, a rotating "captain" owned the deployment, regardless of whether they'd built anything being deployed. The captain had no context on the code. The person who did would guide them through the process on a call: click here, approve this, watch that. A day before, there was a separate call to review what would be deployed. After deployment, another sync to confirm the two teams were aligned.
Three scheduled meetings to ship code that one informed person could have deployed in twenty minutes.
When I asked why, the answer was reasonable: two sister teams needed to stay in sync. Fair. But somewhere between the real problem and this solution, something went wrong. The coordination gap that originally caused this process had either been solved another way, or had quietly stopped existing — and the process stayed, because process is hard to kill. It has stakeholders. It has history. It has the irrefutable defence of, "we haven't had that problem since we started doing this", which isn't the same as saying, "THIS IS WHY".

Nobody designed this system to be wasteful. Someone, at some point, had a real problem: a coordination gap, a missed dependency, a deployment that went wrong because one team didn't know what the other was doing. And they solved it. With process. And then the problem that originally caused the process faded, or changed, or was already being solved better somewhere else, and the process stayed.
Process is surprisingly hard to kill. It has stakeholders. It has history. It has the implicit defence of well, we haven't had that problem since we started doing this — which is not the same as saying the process is why.

Here is what I think is actually going on in situations like these, and it is not strategic or political.

People invent work because stillness is uncomfortable. Not because they are lazy or ambitious in the wrong direction. Because their nervous system reads "nothing urgent right now" as a threat. So they fill it. A meeting. A process. A ticket. A call to prepare for the call. It is not malicious. It is anxiety with a calendar invite.

The engineer who builds a system that did not need to be built is not showing off. He is soothing something. The manager who adds a third sync to a two-step process is not being bureaucratic on purpose. She cannot sit with the uncertainty of fewer touchpoints. The team that spends a sprint on a feature nobody asked for is not wasting time consciously. They just could not tolerate the discomfort of a lighter backlog.

The most productive people I have worked with shared one quality. They could tolerate having nothing unnecessary to do. They did not fill the gap. They trusted that the next real problem would arrive, and they wanted to be rested and sharp when it did.

That is a harder skill than it sounds. Most workplaces implicitly punish it. Being visibly busy reads as committed. Being precisely busy reads as underwhelming. So people perform, and eventually they stop being able to tell the difference between the performance and the real thing.

__BTW...___
We never shipped that ERP. A few weeks before launch, the institution's servers were hacked. Data was stolen. The project was shelved overnight.
Four months of careful, competent engineering, cancelled by a security incident that had nothing to do with anything we built.
The work was not wasted because it got cancelled. It was wasted the moment it started. The hack just made it impossible to pretend otherwise.

The itch was right. It almost always is.

The hardest skill at work is tolerating the discomfort of having nothing unnecessary to do, and resisting the urge to invent it anyway.
The question is not whether you are capable of doing the work. The question is whether the work needs to exist at all. Most of the time, if you ask honestly, it does not. Just because you can do something does not mean it needs to be done. That sounds obvious. It is the hardest thing to practice.
