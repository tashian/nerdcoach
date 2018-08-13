---
title: "The Hidden Bets of Agile"
date: 2017-09-30
description: "The future is unknown, so we bet on which abstractions will make sense. We codify the bets."
images: ["story/the-hidden-bets-of-agile/pachinko.jpg"]
---

{{< figure src="pachinko.jpg" caption="Photo by Tischbeinahe, CC-BY-SA" class="ma0" >}}

Agile stories don’t tell us what to code; they are only examples. They offer small slices of the bigger abstractions that we’ll usually need.

Stories are tiny windows that we can peer through as we code. The simplicity of a story motivates and concentrates our creative effort. Their value is in boiling down the larger picture of the problem domain and what the customer really wants, in plain language. It’s up to the team to work out the larger abstractions over time.

Much as we would like every story to be perfectly self-contained, many abstractions are covered by several stories. Abstractions bleed into future stories that haven’t been written yet, that won’t be written for months. Embracing change means choosing abstractions using incomplete information.

We’re not supposed to do much up-front design, though. Just enough to cover the next week or two. Yet as the project grows, we begin having to do deeper surgery more frequently. Refactoring. It’s not just about DRYing up code. Its highest purpose is in the development of the abstractions. It helps us bring the code into line with our latest understanding of the bigger picture.

Refactoring addresses the deeper problem that our software is not uniformly flexible. We do not have a perfect view of the future, yet we have to design areas of flexibility into the software today.

Agile seeks a sweet spot between up-front design and refactoring. A hybrid approach, where we sketch the abstractions, accepting that our design will always be incomplete. We sketch just enough to make wise bets, to give us a sense of how we might find the right path through the forest as we code.

Bets. That’s an important word. The future is unknown, so we bet on which abstractions will make sense. We codify the bets.

If we don’t notice and acknowledge the bets we are making, they may not be wise bets. Some of the bets that are quite subtle today will become consequential later. Yet if we try to get too clever about bet making, we risk premature optimization. Cleverness leads to abstractions that are too grand, too florid.

---

Stories don’t tell us about the bets we’re about to make. They disguise bets in examples. But, the process of writing the stories and the associated design work begins to reveal the bets of past, present, and future. That’s why it’s crucial for developers to write their own stories.

Senior engineers make wise bets because they are always holding the context of where the project and business is going, and it informs their decision-making while coding. Junior engineers make blind bets.

But, it’s not only up to the individual developer. Wise bets have to come from a wise organization. If the product organization keeps changing its mind or doesn’t get the team into alignment around the bigger vision, poor bets are inevitable.

Poorly made bets can calcify into technical debt. As the abstraction gap between the software and the product vision (and product backlog) grows, it becomes harder to move.

(This often gives startups a huge competitive advantage. The big company’s codebase will eventually fall out of line with the market, and a startup can start from scratch with more current abstractions. If the startup can paddle hard enough in the new direction, their flexibility will overcome the big company’s rigidity.)

But whenever the product owner changes and brings an entirely new point of view, or the roadmap is redrawn, or the mission or vision of the organization changes, we can immediately expect to have a lot of debt to pay to the software.

This is not technical debt. It’s product debt. It’s bet debt.

Should we track the bets we’re making? If so, how? Agile doesn’t have a concrete mechanism for this.

Do story points help at all? Well, story points feed information about past bets back into the product conversation: Maybe we should do X first (2 points) and defer Y (5 points), even though Y is somewhat more important, because there’s flexibility to do X, but Y will require a bunch of refactoring first.

By this point we’re arguing with the past. It’s too late for the product team to have any say.

Even though Agile prioritizes responsiveness to change, we build rigidity into software. We are constantly anticipating where the changes will occur, either explicitly (with up-front design) or implicitly (through spontaneous, often unstated design choices). So, a team will make better software if it knows more about the customer’s needs and where the flexibility will be needed. The challenge is then to strike a balance between doing up-front design, making wise bets (and timely optimizations), and refactoring.
