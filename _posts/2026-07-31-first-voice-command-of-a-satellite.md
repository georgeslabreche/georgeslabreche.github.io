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

I developed the processing pipeline that ran onboard ESA's OPS-SAT PRETTY satellite. It captured the 1296 MHz uplink with a software-defined radio, narrowed and demodulated it, transcribed the speech with an onboard speech-to-text AI model, detected the command despite transcription errors, and launched DOOM. It then downlinked a postcard with the gameplay frame, the transcription, and signal diagnostics.

<figure>
  <audio controls preload="metadata" style="width: 100%;" src="/assets/images/posts/2026-07-31/command.mp3">Your browser does not support the audio element. <a href="/assets/images/posts/2026-07-31/command.mp3">Download the recording.</a></audio>
  <figcaption>The operator spoke into the microphone: <em>"LIMA ALFA FOUR OSCAR, PRETTY PLAY DOOM DOOM DOOM, PRETTY PLAY DOOM DOOM DOOM."</em> The spacecraft captured this recording during the evening pass.</figcaption>
</figure>

<figure>
  <a href="/assets/images/posts/2026-07-31/postcard-evening.png"><img src="/assets/images/posts/2026-07-31/postcard-evening.png" alt="A DOOM-themed postcard composed onboard the satellite on the evening pass: a gameplay frame with logos, the onboard transcription, and signal diagnostics."></a>
  <figcaption>OPS-SAT PRETTY composed this postcard and downlinked it, transcription included. That is what the satellite made of the live human voice: imperfect, but the repeated DOOM trigger word still got through.</figcaption>
</figure>

This was not a pre-scripted trigger. It was a spoken command sent over amateur radio, detected and acted on autonomously in orbit.

The Oslo Group of the Norwegian Radio Relay League ran the [July campaign](https://doom.lb6aj.net) under the club call sign [LA4O](https://www.qrz.com/db/LA4O): the satellite detected the command from a synthesized voice on the morning pass, then from an operator speaking live into a microphone that evening. The campaign followed earlier link tests from Legnica, Poland. Everyone involved is credited in the [acknowledgements](https://github.com/georgeslabreche/opssat-pretty-doomed#acknowledgements), and the experiment would not have happened without them.

### Links

- [Project Page.](https://tanagraspace.com/opssat-pretty-doomed/)
- [GitHub Repository.](https://github.com/georgeslabreche/opssat-pretty-doomed)
- [Acknowledgements.](https://github.com/georgeslabreche/opssat-pretty-doomed#acknowledgements)
- [Oslo Campaign Report.](https://doom.lb6aj.net)
