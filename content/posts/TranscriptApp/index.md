---
title: "Building a privacy-focused transcription app in 24 Hours"
date: 2026-10-23
draft: false
tags: ["ai", "apps", "vibecoding", "cursor"]
cover:
  image: "transcript_app.png"
  alt: "Hush"
  relative: true
---

Many of my colleagues have been using Granola or similar apps to transcribe and get highlights and summaries of all meetings. In meetings where people don't need to look at their laptops, everyone is still always keeping their laptops a tiny bit open, either for some agent working or for recording/transcribing. 

Apps like these record invisibly, no AI notekeeper is joining the actual Google Meet/Zoom/Teams meeting so you have no idea that this is going on. There is of course some privacy issues with this - people should ask permission or at least inform their colleagues that they are recording/transcribing the meeting! It can be uncomfortable not knowing if everything you said is being recorded without you knowing. 

In the case of most apps like Granola, they are also sending the whole conversation to an US company as the transcription happens in the cloud and you have no idea what they do with that data (and company secrets). 

I would never use an app that sends the whole conversation to an outside company. I can still see the benefit of sometimes getting transcripts and summaries from specific meetings. (I'll write more on the value of actually writing your own meeting notes soon in another blog post.) 

(Side note: I was conducting an interview with an engineer last week and he asked me if he could get the transcript from our interview, as most digital interviews nowadays are recorded and summarized, and that also made me think that for fairness, the candidate should either be allowed to record the interview as well, or get the transcription.)

{{< figure src="recording.png" alt="recording" >}}

What I wanted: 
- A privacy-centered app where everything happens locally on device. 
- An app that works with both Swedish and English. 
- No recordings, just transcripts (and summaries).
- Compatible with Obsidian, so I can keep all transcripts and summaries together with my other notes in an Obsidian vault. 

I started searching and investigating, ChatGPT gave me a bunch of options and we evaluated a few before I decided to test <a href="https://github.com/drcursor/HushScribe">HushScribe</a>. 
HushScribe had what I was looking for: open source, everything happening on device with local models, transcripts as markdown files.  
The default model, Parakeet, was **really** bad at Swedish. WhisperLarge was much better, but the app's setting made it translate everything I said into English. I didn't want my Swedish meetings translated to English, but transcribed as they were. 

It was open source and I still had Cursor tokens left, so the only natural next step was of course to make my own fork and my own version - **HushSwedish**. 

Within 24 hours I had a <a href="https://github.com/Sofiakodar/HushSwedish">new working app</a>, that handles both Swedish and English meetings and a few new features and tweaks to things that annoyed me in the original app. The app pre-loads the model as soon as you open the app, to more quickly be ready to transcribe. It clearly shows when it's ready (as the original app often missed the first few sentences). I also added the option of setting some standard meeting names (for example "standup" for meetings every morning at 9, or "Product sync" every Wednesday at 10.) I also made it possible to add colleagues' names more quickly. 

{{< figure src="Hush_stats.png" alt="Stats" >}}

One thing I'm considering for a later version is to use a model more specialized in Swedish: <a href="huggingface.co/KBLab/kb-whisper-large">KB-Whisper Large</a> , made by Kungliga biblioteket. Getting it working properly needs a bit of extra work though.

You can of course check it out here <a href="https://github.com/Sofiakodar/HushSwedish">HushSwedish</a> and try building and running it (on MacOS). Just remember to let your colleagues know you're transcribing the meeting. 

Everything was done in 24 hours, so there's still room to improve the app, the page, and the screenshots. But I have something that I can already use and that fulfills my requirements and then some. 


*As always, this blog post is written by me, not an AI, so all errors are my own.*