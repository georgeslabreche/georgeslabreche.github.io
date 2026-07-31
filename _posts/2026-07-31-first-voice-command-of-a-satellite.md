---
title: "PRETTY DOOMed: The First Voice Command of a Satellite"
excerpt: "A radio amateur spoke to a satellite in orbit and it played DOOM."
text_shadow: rgba(37, 42, 52, 0.9)
header:
  overlay_image: /assets/images/posts/2026-07-31/voice-command-waveform.png
  overlay_filter: 0.4
  caption: "The amplitude envelope of the voice command, as captured onboard OPS-SAT PRETTY."
categories:
  - opssat
tags:
  - opssat
  - research
  - doom
  - radio
---

Hej folks! These past few months I've been working on a project to send a voice command to a spacecraft, and I'm happy to say that it finally worked! On 27 July 2026, a radio amateur in Oslo pointed their antenna to space, spoke into a microphone, and a satellite in orbit heard its instructions to play DOOM! It is the [first time a satellite has been commanded by voice](https://tanagraspace.com/opssat-pretty-doomed/).

Onboard ESA's OPS-SAT PRETTY satellite, the processing pipeline I developed captures the 1296 MHz uplink with a software-defined radio, narrows and demodulates it, transcribes the speech with an onboard speech-to-text AI model, matches the command despite transcription errors, and launches DOOM. A postcard with the gameplay frame, the transcription, and signal diagnostics is then downlinked.

<figure>
  <audio controls preload="metadata" style="width: 100%;" src="/assets/images/posts/2026-07-31/command.mp3">Your browser does not support the audio element. <a href="/assets/images/posts/2026-07-31/command.mp3">Download the recording.</a></audio>
  <figcaption>The command sent from Oslo: <em>"LA4O, PRETTY PRETTY, PLEASE PLAY DOOM DOOM DOOM."</em> This is the recording as captured onboard OPS-SAT PRETTY during the evening pass, dug out of the noise floor 500 km up.</figcaption>
</figure>

<figure>
  <a href="/assets/images/posts/2026-07-31/postcard.png"><img src="/assets/images/posts/2026-07-31/postcard.png" alt="A DOOM-themed postcard composed onboard the satellite: a gameplay frame with logos, the onboard transcription, and signal diagnostics."></a>
  <figcaption>The postcard OPS-SAT PRETTY composed and downlinked, transcription included. That is what the satellite made of the command: imperfect, but enough to match on.</figcaption>
</figure>

This is not a pre-scripted trigger. It is a spoken command sent over amateur radio, detected and acted on autonomously in orbit.

The Oslo Group of the Norwegian Radio Relay League ([LA4O](https://www.qrz.com/db/LA4O)) ran the [July campaign](https://radio.lb6aj.net/doom/): three of six captures triggered DOOM on the morning pass, then a live human voice reproduced it on the evening pass. They followed link tests from Legnica, Poland. Everyone involved is credited in the [acknowledgements](https://github.com/georgeslabreche/opssat-pretty-doomed#acknowledgements), and the experiment does not happen without them.

### Links

- [Project Page.](https://tanagraspace.com/opssat-pretty-doomed/)
- [GitHub Repository.](https://github.com/georgeslabreche/opssat-pretty-doomed)
- [Acknowledgements.](https://github.com/georgeslabreche/opssat-pretty-doomed#acknowledgements)
- [Oslo Campaign Report.](https://radio.lb6aj.net/doom/)
