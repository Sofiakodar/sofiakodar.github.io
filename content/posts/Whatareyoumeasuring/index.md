---
title: "What are you really measuring?"
date: 2026-05-15
draft: false
tags: ["leadership", "product", "engineering"]
cover:
  image: "big_dashboard.png"
  alt: "dashboards"
  relative: true
---


We need to talk about feedback loops. Short feedback loops are the heartbeat of Agile. Once, cutting development cycles to two weeks was a massive achievement (and for many, it still is). But the core principle, learning quickly from what we build, seems to have been lost, even though the tools to do it are better than ever.

Continuous delivery, continuous discovery, and releasing features to users early and often are now standard for many web-based products. Some ship dozens of times a day, others test with users early and often. Even for teams dealing with hardware or complex deployment cycles, the potential for rapid feedback exists. 

### Lofty goals and no follow-up ###
I see the same pattern over and over again: teams set ambitious goals and craft business cases for new features. *"This will boost retention," "This will drive X revenue," "This will decrease churn."* But once the code ships, the conversation stops. The actual results are rarely measured, discussed, or used to inform the next decision.

Teams make bets based on estimates: *"If this takes Y time and delivers X value, it's worth it."* But weeks turn into months. The feature takes twice as long as predicted, yet the work plods on. Or, it launches, and the team immediately moves on to the next item, without asking: Did we hit the target? Was it the right bet? Did we succeed?

At a previous company, we set clear business goals for large cross-team projects. Teams planned eagerly and executed. But when the cycle ended, new goals were set without a word about the old ones. The cross-team projects were quietly dropped, one by one. The teams were left guessing: Did we succeed and fulfill the goals? Did we fail? Was it a strategic pivot, or just a quiet surrender? The teams asked, but the silence was deafening. There was no feedback loop, no closure or learning, only confusion and silence.

{{< figure src="closeup_dashboard.png" 
alt="Team" >}}

### What is success? ###
In an earlier blog post I wrote about <a href="/posts/senseofurgency/">the urgency gap between engineering and product</a>. I think an important part of this is this missing feedback loop. 
If you work hard on a new feature with lofty goals, only to hear nothing about the outcome, or worse, receive only negative feedback, your motivation will inevitably wane. Was all that work worth it? Did we succeed? You have no idea.

It’s like trying to master darts by throwing them out a window without ever seeing the board. You might throw with perfect form, but without seeing where they land, you can’t improve. You’re just guessing.

Most teams have a vague, rudimentary view of how their work actually drives revenue. Companies often lack a feedback loop between Revenue, Customer Success, and Development. Development teams don’t know what actually delighted users, drove upgrades, or solved real problems. They only know what broke. (We are also really lousy at celebrating releases and wins, let's do better!)

Similarly, many teams have a limited understanding of who is using their features and why. While user interviews are invaluable, they cannot replace the scale and objectivity of hard data. Today, getting that data is easier than ever, yet many teams still fly blind.

Another common failure is that data exists, but no one trusts it. Teams waste hours debating which dashboard to use, or worse, discover that there are three different definitions of an "active user" or an "enterprise customer" across the company. This ambiguity kills decision-making. Every company needs a single source of truth: clear, written definitions that everyone agrees on. 

### A true story about customer feedback ### 
Many years ago, my team spent months rebuilding a web interface from the ground up. We poured energy into user research, UX, and a complete architectural overhaul. When we finally released, the only feedback we received came from internal departments: a few bug reports and minor improvement suggestions. Everything was solid and we tried to take some pride in having delivered such a stable new version, but we wondered what the customers thought of the new version.

A few weeks after the release, I walked past the Customer service team on an upper floor and noticed printed out e-mails taped to the wall and a big bouquet of flowers on their desks. Curious, I went to check it out and discovered they were e-mails from happy customers about the new release. One customer was so happy that he had sent actual flowers to customer service! 
I immediately talked to them and they started forwarding all the encouraging and positive e-mails to my team, who sat on the bottom floor completely unaware of the delighted customers. 

{{< figure src="flowers.png" 
alt="Team" >}}

### Let's do better ###
I think we have a lot to gain from taking this more seriously. For example: 
- Make at least a rudimentary analysis before committing to large features. What are we hoping to gain? What is the cost of implementation? This doesn't need to be a weeks-long process, but create a baseline hypothesis to validate and follow up on later.
- Conduct follow-up reviews for both individual teams and larger initiatives after every cycle, month, or quarter. Have honest discussions about what worked and what didn't to make smarter decisions for the next round. Celebrate wins! Take a moment to actually feel proud about features shipped as well. 
- Stop and reevaluate when scope creeps. If the estimated time is exhausted and the feature isn't finished, stop. Re-evaluate. Is it still worth it? Don't just continue on autopilot if it was estimated to only be worth three weeks and you're on week six. Have a deliberate discussion and decide whether to make a new bet or pivot. (Related to this, I can recommend <a href="https://www.viktorcessan.com/the-economics-of-software-teams/">Viktor Cessans post about how much an extra week actually costs</a>.)
- Check on features released three months, six months, or even years ago. Is anyone using them? Did we hit our goals? If you aimed for 10% adoption but are stuck at 1%, do you need better marketing, or was this simply the wrong bet? Remember, every feature means maintenance costs and complexity. Sometimes, the best move is to remove features entirely.
- Create (and maintain!) good feedback loops between departements, specifically between Revenue, Customer Success, Product, and Development. These loops shouldn't just focus on what makes customers unhappy, but also  what drives sign-ups, upgrades, and delight. Understanding the positive drivers is just as critical as fixing the negatives. 
- Establish a single source of truth. Set up dashboards that are accessible and intuitive for everyone. Define consistent metrics across the entire company – what exactly counts as an "active user" for example? Imagine having a unified view of the whole business and every product area, shared widely so anyone can find and understand the data instantly. What would change if transparency was the default?
- Ensure every team owns telemetry and data for their specific features. They need to know: What is being used? Who is using it? What works? Couple this with guardrail metrics and automated alerts. This way, teams immediately detect issues like latency spiking too high or conversion dropping.
- Make sure that the teams have the skills they need. If they lack expertise in implementing telemetry or data engineering, facilitate knowledge transfer from other departments. You might even need to hire dedicated data engineers and analysts to help teams set up their instrumentation correctly and interpret the results effectively.
- When celebrating new deals and revenue, don't give the revenue team all the credit, tie it back to the features and teams that made it possible. 
- Let developers and teams meet customers or internal users, regurarly and discuss their features and see how they are used in the day-to-day work. Nothing is more motivating than actually seeing how you work has impact and helps someone. 

This is not rocket science, we just need to prioritize getting those feedback loops up and running and start looking at the data and discussing it as part of our daily work. What's stopping us? 

<br>* *As always, this blog post is written by me, without any AI, so all errors are completely my own.*