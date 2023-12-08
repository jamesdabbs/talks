# [fit] Community,

# [fit] Building

_Reflections on trying to get humans together to build and use software_

### AIM _**|**_ James Dabbs _**|**_ Dec 2023

---

# Background – Procore

- ~4K people
- 14M lines of code
- 500M requests / day
- ~20PB of data
- deploy every ~30m

^ Unsurprisingly, this scale implies interesting problems
^ The ones that have hooked me aren't the ones I expected

---

> _Any sufficiently complex system is going to always exist in a certain degree of degradation._
> -- [Cindy Sridharan](https://copyconstruct.medium.com/testing-in-production-the-safe-way-18ca102d0ef1)

^ Some server needs to be restarted. A shark is chewing through a cable somewhere.
^ This means you
^ - engineer for resiliency
^ - tolerate-to-promote redundancy

---

# Complex Systems

- Shared human sociotechnical endeavors **are** complex distributed systems
- It is **very** often the human parts that are degraded

^ If the only tool you have is a hammer, everything looks like a nail
^ If you're a tool builder, question the assumption that issues are tool gaps

---

# [fit] Productivity Engineering

Building sociotechnical systems where the humans in the loops are engaged, joyful, and doing their **best work**.

^ "Best work" is a term of art here, though we're not gonna get too deep on measurement or engagement frameworks
^ This nascent community is grappling with identity, but I think / hope this resonates

---

# Outline

- Key concepts & terms
- Guiding prinicples
- Story time
- Reflections
- Q&A

---

# [fit] Key Concepts

---

# Cognitive load

- Human brain cycles are **far** more scarce than cpu cycles
  - Be a good steward of those resources
- Provide support for managing essential complexity
- Remove incidental complexity

^ The hardest part here is deciding what's essential. It's contextual and changes. Something that _seems_ essential today may be irrelevant in 5 years. It is different for different people with different goals.
^ Knowls are a very effective tool for managing cognitive load

---

# Personas

We're building tools for humans. You need to know who those humans are.

I think a lot about:

- Kira: the seasoned on-call operator who just got paged at 3AM and needs to make a multi-million-dollar decision **now**
- Brendan: the new intern that wants to do their best, but has no idea what they don't know yet

^ Tools for Kira would slice Brendans fingers off, but someday Brendan wants to be Kira
^ Persona: my department chair gave me these macros, I just want to publish my PDF

---

# Feedback Loops

Many of the best things we can do look like getting informative, actionable feedback to folks, in context, as early and often as possible.

---

# Feedback Loops

Fast inner feedback loops that let folks stay in-flow

- Test / compiler / error messages
- Syntax highlighting
- Guides with "you'll know you're on the right track if you see ..."
- Ex. – run arxiv validation locally

---

# Feedback Loops

Effective, predictable outer loops

- Test suites that detect errors and enforce standards **without shame**
- Asking for help is intrisically scary; work to make it less so
- Set clear expectations about where and how to get support

---

# Measurement Frameworks

Is it working?

- ⚠️ Incentives are hard, but critical
  - DON'T promote for lines of code written or tickets closed (activity)
  - DO survey for satisfaction; count and minimize handoffs (outcomes)
- DORA, SPACE, MAP
- Talk to your users

^ You can make sure people get paid or promoted for writing code, and they will write code. This may create more problems than it solves.

---

# [fit] Principles

---

# Lead with Principles

Good examples

- LMFDB
- Arxiv

^ So friction and wasted energy stems from the various actors making different, implicit assumptions about the social contract. Being explicit avoids so much of this.
^ "Pricipals-led" and "survived leadership changes" go hand-in-hand

---

# Center the Humans

- What problem are you helping your user solve? How would **they** understand and describe it?
- What sorts of activities would enrich your ecosystem? What would motivate someone to do those things?

^ Spoiler: "I wish I had to learn a brand new tool and bevy of concepts" is **vanishingly** few people's motivation.

---

# Think Global, Act Local

- ⭐️ North star
- Current state
- Next target state

^ Also called "observe, orient, act"

---

![inline fit](https://images.squarespace-cdn.com/content/v1/5f258da0d2666a6d4fe4cb92/1608478877910-G048EKXRZGAATIVFG7LL/Success+diagram.jpg)

---

# Marathons, not Sprints

- The work is whatever gets in the way of the work.
- It is never done; it evolves.
  - Things that can't make incremental progress often make no progress
  - Think about the evolutionary pressures and selection mechanisms

^ "Done is dead". Improvements stop when it stops becoming worthwhile to improve.

---

# [fit] Story

# [fit] Time

---

# [fit] The Tragedy of the

# [fit] Monolith

![Monolith](https://static.wikia.nocookie.net/2001/images/4/41/A_itmes.jpg/revision/latest?cb=20111116211153)

---

# The Tragedy of the Monolith

- A tiny fraction (but large number) of user requests trigger errors
- We have a tool that records those errors and sends an alert to Slack
- We've had a few high-profile outages recently that could have been avoided if anyone noticed the alert and did something about it

So ... why didn't they?

---

# The Tragedy of the Monolith

- Many of these are "expected" / retry / don't impact customers.
- These alerts go into a giant Slack channel that everyone is in and no one pays attention to.

---

# Background Efforts

- A passionate guild organizes files into "domains", but the data has quality issues. It's ~80% there.
- A similar guild succeeded in mapping team owners 2 years ago, but the teams have changed since then.
- 4 years we had a "zero errors" push and drove the error rate down to zero. It started creeping back up when our focus changed.

---

# ⭐️ North Star

- Stable system with no serious customer-impacting issues
- Everyone knows how to find an owner for a thing
- Owners understand the things they own

^ No one doesn't want this

---

# [fit] **Why are we stuck?**

# [fit] **What would you change?**

# [fit] **(Why are we talking about this?)**

---

# [fit] Personas

---

# Developers

- are motivated (incentivized) to build and release new features for users
- **do** want to know about and fix errors in their code
- **do not** want to deal with systemic issues or other peoples' code
- outnumber all other personas significantly
- are the ones that actually make the changes

---

# Operators

- want to make sure the system is up and stable
- are **not** incentivized by the fast flow of changes
- know and care deeply about systemic issues – fixing bugs, applying security patches safely
- can make **some** changes, but not at the scale required to acheive those outcomes directly

---

# Shepherds

- are intrinsically motivated by e.g.
  - a strong "ownership" value
  - a desire to organize and classify and impose order
- have no structural authority

---

# Directors

- want to avoid any more outages - **especially** ones we should have seen coming
- are nervous about slowing the flow of features
- cannot make **any** changes directly
- control promotions and firings of the other actors

---

# What we

# [fit] Did

^ Interlude: worth talking more about what we did that failed?
^ I'm a big believer that failure is a great teacher, and we should aim to fail
^ more often, more quickly, and less expensively.

---

# We Built

- _Data_ - an initial comprehensive-but-innacurate mapping between errors and components and team owners
- _Tools_ - that make it easy to update the map (but impossible to unmap ownership)
- _Process_ - for mediating disagreements
- _Documentation_ - explaining the what and the why and the how to get help

---

# We Did

- Updated the Slack alerts to go to the mapped team owners
- Pointed folks at the documentation and mediation process
- Listened and answered questions
- Waited

---

# We Saw

When teams got an error notification, either

- it was theirs => easiest thing was to fix it
- it wasn't theirs => easiest thing was to fix its ownership

---

# We (Later) Saw

- Notifications converged towards teams with expertise
- Teams decided for themselves whether and when to improve their notifications
- We noticed errors before our customers did signficantly more often
- The domain and ownership mapping data improved without direct central effort

^ We made it valuable enough for people to update the component maps that they
^ started doing it. We never asked them to. But now we _use_ those component and
^ ownership maps as inputs to a host of other organizational work.

---

# We _**Could**_ Do

Some teams are farther along that others. We could force the issue by:

- reporting up on "open error notifications past <n>-days"
- set up paging alerts on frequent errors

But we haven't needed to

^ The key here is that we moved the cost (noise) back to the folks who were
^ empowered to make decisions about whether it's worth the cost. They've made
^ decisions that are right for them.

---

# [fit] Takeaways

---

# Takeaways

Dynamical systems give good metaphors for change over time

- Asymptotic trends
- Attractors
- Phase changes

---

# Takeaways

Humans are discontinuous

- was your change or question clear enough that someone could grok it in the 10 minutes they hand between meetings?
- was your error the **first** or the **tenth** someone saw today?
- is there someone they know and trust enough to be vulnerable and ask for help?

---

# Takeaways

Making socialtechnical change takes

- aligning tools, knowledge, and incentives
- intentional strategy
- empathy

---

# Further reading

- [Recoding America](https://www.recodingamerica.us/)

> When systems or organizations don’t work the way you think they should, it is generally not because the people in them are stupid or evil. It is because they are operating according to structures and incentives that aren’t obvious from the outside

^ “government is the name we give to the things we choose to do together”

^ Similar story of how COVID helped the Post Office fix data quality issues, through test kit mailing

---

# [fit] Community,

# [fit] Building

_Reflections on trying to get humans together to build and use software_

### AIM _**|**_ James Dabbs _**|**_ Dec 2023

---

---

# [fit] ✂️ Cut Topics

---

# ✂️ Cut Topics

On strategy

> _... a deployable decision-making framework, enabling action ..._
> -- Stephen Bungay

- Strategies need to help people make real tradeoffs between not-obviously-bad options
- They need to help you decide what you _won't_ do and where you _should_ focus

---

# ✂️ Cut Topics

Insist on simplicity

- Complexity is an equity issue. Complexity favors folks with experience and disposable time, and excludes folks that don't.
- Our most durable tools are simple, focused, intuitive, composable.

---

# ✂️ Cut Topics

Layer on complexity

> _complex systems that work evolved from simple systems that worked; systems that start complex don’t work_
> -- Gall

- Define clear boundaries with clear interfaces
- Facilitate "popping up" or "peeling back" a layer
- Help outsiders find a good starting layer

^ Knowls are great for that sort of peeling back

---

# ✂️ Cut Topics

- Papercuts matter (`linear_combination`)
- Effectively sharing solutions is often harder than solving them

---

# ✂️ Cut Topics

- Misconceptions I had about working in industry
  - There _is_ some central power, but it will _rarely_ be wielded to force technical unificiation or push "low-level" initiatives
  - There is status and recognition, but rarely for folks doing the boring work that lets everyone clock out and sleep soundly
  - Ownership, maintenance, resourcing are still real challenges
