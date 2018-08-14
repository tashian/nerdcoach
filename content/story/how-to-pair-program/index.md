---
title: "How to Pair Program"
description: "Drop the rockstar ego. Pairing is a duet, and you are an accompanist."
date: 2016-06-23
resources:
- name: cover
  src: pairing-station.jpg
  title: Illustration by Siobhán K Cronin
---

Programming, like any art practice, is a performance. Our code reflects the physical and virtual environment it was created in, the culture of the team, the social weather of the room, the constraints of the toolchain and the target architecture, and the mood and facility of the performer at moment of strike.

We often imagine a solo act. It’s 2am and our hero works at a laptop at a small desk in a dark bedroom. To their left is an empty can of energy drink. Their level of concentration is so deep that you could stomp through with a marching band and they might not notice.

Or it’s 3pm and our hero is at their desk in a glassy, green-walled open-planned office. They’re listening to EDM, and everyone knows not to fuck with them when the earbuds are in. Distraction is so expensive these days.

Pair programming doesn’t fit these archetypes. Pairing is a graceful duet. It allows two programmers to combine their strengths and build something more thoughtful and cohesive than a single person can build. I believe it’s the fastest way to become a better programmer. And it can be a delightful experience.

## Why pair?

Pair programming results in:

* **code with fewer defects.** With two sets of eyes on everything being written, fewer bugs make their way through the cracks.
* **cleaner code that's easier to understand.** Just because a solo programmer can comprehend their own code, that doesn’t mean it’s clean. But two people can really raise the quality level together.
* **a closer team.** We develop empathy and connection with our teammates through pairing. It also reinforces a shared vocabulary.
* **faster learning or a faster pace**, no matter your skill level. You can trade these things off depending on who you pair with. Sometimes you will learn fast but move slower than when working solo. Sometimes you can get more than two people’s worth of efficiency as a pair.
* **consistency of code style across a project.** Pairing raises questions of code style and forces developers to agree on good — or at least consistent — answers.
* **a diffuse comprehension of the code across the team.** Pairing breaks down code silos that tend to form when bigger projects are being built.
* **less time dealing with git branches and pull requests.** You are reviewing the code as you write the code.

## Who should you pair with?

### In short: anyone.

Some options include:

* Two experienced developers. This is the most efficient pairing setup.
* A beginner and a seasoned developer. This is the best learning environment for both parties. Beginners often ask amazing and thought-provoking questions!
* Beginners pairing together will learn faster than working alone, and will challenge each other.

----

## Preparing to pair
Start by removing as many external distractions as you can. Put your mobile devices into airplane mode. Close Gmail. Turn on Do Not Disturb mode on your laptop. The best programming environment may be a separate account on the laptop that’s dedicated to focused work.

Get a clean glass and fill it with water. Drink the entire thing. Now, refill the glass and bring it with you to the pairing station.

Determine your roles. One person will drive, having control of the keyboard and mouse, and the other will navigate. (You can switch anytime you like.)

Product decisions will emerge as you code. Who will have the final say on these? Is that person within reach?

Everything happens on one monitor (or two mirrored monitors). The navigator should avoid doing side work on a mobile phone or laptop of their own during the session.

The navigator is responsible for deflecting any potential interruptions by other team members.

The navigator is responsible for monitoring any obstacles to development and noting opportunities for improvement of the toolchain. If a common step requires too much energy in the form of mouse work, commands, or keystrokes, make a note of it.

Agree on the development software and key mappings you’ll use. A tried-and-true development environment that is well understood by both of you is much better than a fancy new and shiny one. Efficient pairing depends on alignment around the development environment and key bindings. Role switches during the session should feel super fluid and not require any additional switchover time within the environment.

Clean your workspace, including the monitor.

### You will need:

* One machine, two mice, and two keyboards
* A place to take notes

Now you can begin the pairing session.

{{< figure src="pair-weaving.jpg" caption="WPA-era pair weaving" >}}

### During the session:

* Empathy is key. You should both feel open, relaxed, safe, and aware of the emotional vibe of the session. Psychological safety is paramount! Stress, anxiety, and anger lead to bad code and burnout.
* Sometimes what seems like an offhand remark can be an emotional trigger. If this comes up, it’s time to take a break.
* Don’t allow the more senior person to drive for the entire session, even though it can be faster. The person with less experience will get more out of it if they type, even if they are being told what to type!
* You can switch roles as often as you like during the session.
* Psychological safety allows either person to speak up when they don’t understand something. “I don’t know” will be said often in a good pairing session, no matter your seniority. Typing should not proceed until both parties understand what is being written.
* Don’t code for too long without talking.
* What if you encounter a problem that neither person knows how to solve? Step away from the keyboard, and whiteboard and do some research for a minute. Go outside. Shut the door.
* Monitor your energy level. A pairing session is not time-bound, it is energy-bound. The pairing session ends when either party’s energy level begins to wane.
* Take notes along the way of anything you discover about the codebase that is out of scope of the session: areas of code in need of refactoring, unanswered programming questions, defects discovered, and ideas for improving the toolchain.

### Optional practices

* A common pattern combines pairing with TDD. One person writes a test and the other writes the code to make it pass. This has worked really well for me in the past.
* As the navigator, you may find it easier to focus if you have something to do with your hands. In Waldorf schools, the students knit while they learn. Why not knit while you code?

{{< figure src="pair-knitting.jpg" caption="Traditional Shaker pair knitting" >}}

Programming requires creativity, discipline, and patience. Pairing is a great way to develop all three. It is a performance practice and a skill in its own right. And it’s fun!

_Thanks to Siobhán K Cronin, Patrick Ewing, and Erik Hanson._

