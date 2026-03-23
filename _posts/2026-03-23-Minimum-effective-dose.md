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

Nobody designed this system to be wasteful. Someone, at some point, had a real problem — a coordination gap, a missed dependency, a deployment that went wrong because one team didn't know what the other was doing. And they solved it. With process. And then the problem that originally caused the process faded, or changed, or was already being solved better somewhere else, and the process stayed.
Process is surprisingly hard to kill. It has stakeholders. It has history. It has the implicit defence of well, we haven't had that problem since we started doing this — which is not the same as saying the process is why.

This happens for three reasons, and they're embarrassingly human.
Visibility bias: you get credit for what's seen. A thorough system is seen. A minimal solution that quietly handles the problem is not. So teams build to be visible, not to be sufficient.
The thoroughness alibi: over-engineering is socially safe. If you build more than needed and it works, you were diligent. If you build exactly what's needed and something breaks, you cut corners. The incentives point in the wrong direction.
Process as proof of progress: when teams feel uncertain, they generate process. Meetings, documentation, preparation calls. These feel like momentum. Often, they're just the appearance of it.

The itch I'm describing is an immune response to all three. It's the recognition, before you can fully articulate it, that effort is being spent on the wrong thing.

The most productive teams I've been part of had one habit in common: they asked why this, why now, why us before they asked how. They treated scope as a decision, not a given. And the people who protected that scope most aggressively weren't always engineers — they were the product people who understood that every unnecessary hour of engineering is an hour not spent on the work that actually matters.

#BTW...
We never shipped that ERP. A few weeks before launch, the institution's servers were hacked. Data was stolen. The project got shelved overnight.
Four months of careful, competent engineering — cancelled by a security incident that had nothing to do with anything we built.

I've thought about the lesson in that ending for a long time. And I think it's this: the work wasn't wasted because it got cancelled. It was wasted the moment it started. The hack just made it impossible to pretend otherwise.
The itch was right. It almost always is.

The hardest skill isn't knowing what to build. It's having the conviction to stop where the problem actually ends — and not one line of code beyond it.
