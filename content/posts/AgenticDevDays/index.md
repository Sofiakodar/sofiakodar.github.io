---
title: "Agentic DevDays - my takeaways"
date: 2026-04-29
draft: false
tags: ["vibecoding", "cursor", "conference"]
cover:
  image: "devdays.png"
  alt: "Agentic DevDays"
  relative: true
---

Yesterday I attended the Agentic DevDays conference here in Stockholm. I enjoyed it a lot and there were some great talks. This is just a quick post about my favorite talks and learnings. 

Usually conferences have several tracks, but here all talks were at the main stage, with only a few workshops in another room. This was actually refreshing: no decision paralysis, no running between rooms, and no realizing halfway through that you’d picked the wrong talk and wished you'd gone to the other one. The venue, Nalen, was great and everything worked very smoothly. 

{{< figure src="metr.png" 
caption="The METR graph was shown at least twice https://metr.org/time-horizons/" 
alt="The METR graph" >}}

### What vibe engineering thought me about Rust - a practical example of building and agentic LLM gateway / router ### 
Marcus Elwin did a great and entertaining talk about the difference between vibe coding and vibe engineering. I’m definitely going to use that distinction in the future. He has written a blog post about taste in software engineering that can be found here: https://www.umai-tech.com/blog/taste-still-matters-in-ai-software-engineering-


{{< figure src="vibe-engineering.jpg" 
caption="Vibe coding vs vibe engineering (love that the engineering one has a bunker as well)" 
alt="vibe engineering" >}}

He talked about his experience learning Rust through vibe engineering and how important it is with the right principles. For example: Plan before you prompt. Bite-sized PRs. Draw the system. Keep it simple. Know your language. Mix your tools. 

### Bug Hunting with Rival AIs: How Cross-Model Debate Found Bugs Self-Review Missed ###
Magnus Gille talked about how to let agents criticize each other’s work. “One grumpy senior engineer is good, one with a fresh perspective is sharper”. (Fresh context, different model and different harness.) Make the second agent adversarial, truth-seeking and grumpy. 

### Every Guardrail Everywhere All at Once: Designing and Testing Guardrails for LLM Applications ###
Donato Capitella talked about guardrails and how to design systems: Defence-in-depth for LLM applications. He talked about testing different inputs and outputs and guardrails in different stages in the workflow. He showed some scary examples of injections through e-mails and calendar invites. 

### Your next error message won't be read by a human: lessons from Chrome DevTools MCP ###
Michael Hablich talked about Chrome DevTools and the mistakes they made. He talked about Tokens per successful outcome - TPSO. He talked about how agent experience is just as important as user experience. He also mentioned the lethal trifecta: Access to private data + exposure to untrusted content + ability to communicate. He encouraged everyone to read “The lethal trifecta for AI Agents” https://simonwillison.net/2025/Jun/16/the-lethal-trifecta/

### A TDD Engineering Process for Augmented Coding ###
Emily Bache talked about how TDD and agentic coding makes the perfect match for code quality. 

### MIMER and open source coding agents ###
Martin Körling talked about how to use open source coding tools, harness architecture and some examples and tips. Perfect timing now that I’m trying out different local LLMs for my projects. 

{{< figure src="harness.jpg" 
caption="AI harness" 
alt="AI Harness" >}}

### Defensive Architectures for Agentic Systems ###
Miki Habryn held a very interesting and entertaining talk about how agent’s can misbehave (Summer’s OpenClaw mailbox fail was mentioned for example). Lots of interesting points about replayability and how you always should count on having trojans installed on your computer, through some compromised dependency somewhere. Put everything in boxes, lots of different boxes. And never give an agent your google credentials…

{{< figure src="Summer_OpenClaw.jpg" 
caption="The famous post" 
alt="The famous post" >}}

{{< figure src="miki.png" 
caption="An example" 
alt="An example" >}}

### "Continuous learning" aka Letting the agent vent (Unsure of the name of the talk) ###
In an impromptu talk (the planned speaker couldn’t make it) Benjamin from Lovable talked about how they set up so their agents could complain about environmental issues that made it impossible for them to fulfill users prompts and how that created a great feedback loop that made it possible for them to find issues they didn’t know about. Great idea and solution. 

### My takeaways: ###
We already know AI is moving at breakneck speed, what we talked about yesterday will likely be outdated by next summer. There were some solid warnings on security risks when agents run wild or make mistakes, but no easy solutions yet. I think the hard truths will emerge over coming years, and maybe there’ll be off-the-shelf guardrails down the line so not everyone has to reinvent containers or build their own agent lock-down systems from scratch.
But if you look at how messy real-world DevOps environments still are, after all those years of progress, maybe I’m being too optimistic.

I’ve already been planning building a better agents-vs-agents workflow: having one agent write code while another reviews it and the architecture. Now I’m even more excited to build it out. The talks gave me some great tips for adding trust and robustness – specifically around safety, edge cases, and assumption drift. My first step is testing a minimal setup where the reviewer catches those three things. I’ll let you know how well it works later. 

See the whole schedule and more about each talk here https://agenticdevdays.org/schedule


*Note to speakers:*
Dark mode might look good on your computer, but it’s very difficult to photograph or read slides at a distance. Tiny blue text on a black background is not easy to read at the back of the room. 
Don’t make the text tiny, use the whole slide – you’re presenting for 350 people. 
