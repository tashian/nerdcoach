---
title: "Managing Technical Debt"
description: "Many linear feet of books have been written about the complexity of software development, estimation, cost control, QA, and so on."
date: 2017-03-17
resources:
- name: cover
  src: blocks.jpg
  title: Illustration by Siobhán K Cronin
---

Many linear feet of books have been written about the complexity of software development, estimation, cost control, QA, and so on.

Complexity is complex.

I want to share with you a handful of tried-and-true practices that have really helped me as an engineering manager when keeping technical debt under control in a growing project.

### Keep points of flexibility in the right places
Design your software as you would design a building. You have slow moving parts and fast moving parts. Some components, like furniture or wall paint, are loosely coupled to the building. It’s far harder to change the angles at which the walls meet. You have to pick your battles.

Knowing what needs to be flexible isn’t only about the current requirements, it’s about future requirements too. This is what makes software design so difficult. You aren’t simply mapping your software to the world as it is in this moment, you are trying to predict an uncertain future. Now, this is folly to begin with, because the future is murky and there is a huge risk of premature optimization. But you must make choices between what is foundational and what is paint.

The word _software_ is a misnomer, because it implies uniform flexibility. Uniform flexibility might seem like an ideal to aim for, but the ground truth is that a more rigid, tightly coupled system is usually a lot simpler to build at first. For example, it may be argued that a monolithic app is more tightly coupled than a set of microservices — but the monolithic app has the advantage of simplicity. Before even one line of code is written, the microservice-based app has a giant list of requirements relating to communication, coordination, and availability.

And it’s not as though microservices solve the coupling problem. They shift coupling to the network, which can have several really wonderful advantages and can allow for clean, crisp domain boundaries, but the coupling itself is unavoidable.

So, flexibility is expensive. And the sad thing is, I can’t even count the number of times I’ve built something with some subtle beliefs in mind about how the requirements would change later, only to eventually find out that the rigid parts needed changing, and the flexible parts were unnecessarily flexible. At first I thought it was just bad luck, but now I know better.

Software atrophies differently from buildings. If the requirements are pretty stable, the foundation won’t permanently shift or erode like it would in a building. Software doesn’t “wear out.” However, increased scale and new requirements will often impact the foundations. This is really difficult for startups to get right or to plan for, and it’s a problem that cloud services try to solve by encouraging design around scalability at the foundation from the beginning. But optimizing to manage cost and speed as you grow will still require a lot of foundational work, even with modern cloud services, microservice orchestration, and so on.

### Refactor for velocity
Refactoring is one of the best ways to increase your overall velocity. A lot has been said about this already. On a codebase of any decent size, there is always refactoring that can be done. The key is to refactor in the right places — the places where you think you will need simplicity and flexibility in the future. In order for this not to be a guessing game, sometimes it’s nice to refactor ahead of a specific new feature.

Agree to throw away code before writing it
A simple way to reduce technical debt is to agree that some projects are throw-away experiments. For example, you might choose to branch your code and, as quickly and sloppily as possible, get a prototype together that you can validate. Even if the feature is a great success, you will throw away the code you wrote and rewrite it from scratch, properly. Prototyping in this way is risky and unorthodox because it requires that some people on your team lower their standards, but it can be very time-efficient.

### Build with tests and code reviews
Testing is a lifestyle. It is a devotional practice. Even for small projects, I’ve found that tests usually save more time than they waste. Often immediately. And if not immediately, they save time later.

A strong code review culture is critical. No matter how many tests you write, no matter how good you are at refactoring, other people will see problems you missed. Assumptions you made that are confusing. Edge cases. Bugs. Typos. All kinds of stuff. Many companies demand three sets of eyes on every line of code, and I think that can be a good rule of thumb.

The intensity of testing and code review should be commensurate with potential for damage caused by a failure. Foundational code needs more testing than front-end code. All of the software in an insulin pump needs heavier testing than pretty much any app. (Can you imagine the insulin pump team saying “Move fast and break things”?)

### Kill your poorly-performing features
As fellow engineering manager Noah Thorp once told me, “We pay rent on every line of code, every day.”

If you have less code, you’ll pay less rent. So, when I’m working on a project, I care about how each feature is performing, and will regularly bring the team together to decide to remove or improve the features that aren’t carrying their weight. This means occasionally admitting to yourself that a feature that you conceptually love simply isn’t working.

If you can figure out that a feature isn’t right before you write any code, that’s ideal. Paper prototyping and other lo-fidelity user tests should be your first line of defense. There is always pressure, though. There is a constant din of people using the product and asking for terrible features that should never be built. Or features that should be built, but not yet. This is where product management meets engineering management, because even if building the feature is trivial, you still have to pay rent on it.

### Keep dependencies to a bare minimum

You pay rent on dependencies, too.

There are internal and external dependencies. The internal dependencies are the libraries and frameworks that your software depends on. The external dependencies are all of the services your software connects to. You are doubly dependent on the services because they usually have a library associated with them.

When you add a library to your project, you are paying rent on that entire library and your use of it. So, you need to make a good case for every library, every plugin. Even the tiny ones. They add up fast. And if you take the ultralight, disciplined approach, you will be amazed at how quickly you can move.

### Reenforce it in the culture
All of these practices become easier when you have a culture and an environment that supports them. Support good code reviews with GitHub pull requests. Support strong testing with a good CI setup. Support killing features with a monthly meeting. Keep physical books around, like [Refactoring](https://www.amazon.com/Refactoring-Improving-Design-Existing-Code/dp/0201485672), that support good practices (and read them!).

Get clear about what you’re building. Are you building a seaside hideout, a McMansion, or a glassy art museum? Your team has to agree on the answer to this question. Which is why the management of technical debt is not just the engineering manager’s job or the developer’s job. It’s everyone’s job, because it bleeds into every step of the process of making a product, from planning all the way through.
