---
title: "PRETTY DOOMed: The First Voice Command of a Satellite"
excerpt: "A radio amateur spoke to a satellite in orbit and it played DOOM."
text_shadow: rgba(37, 42, 52, 0.9)
header:
  overlay_image: /assets/images/posts/2026-07-31/postcard.png
  caption: "The postcard composed and downlinked on board OPS-SAT PRETTY. Original DOOM cover art: id Software"
categories:
  - opssat
tags:
  - opssat
  - research
  - doom
  - radio
---

Hej folks! On 27 July 2026, a radio amateur in Oslo pointed their antenna to space, spoke into a microphone, and a satellite in orbit heard its instructions to play DOOM! It is the [first time a satellite has been commanded by voice](https://tanagraspace.com/opssat-pretty-doomed/).

Onboard ESA's OPS-SAT PRETTY satellite, a software-defined radio captures the 1296 MHz uplink, narrows and demodulates it, transcribes the speech with an onboard speech-to-text model, matches the command despite transcription errors, and launches DOOM. A postcard with the gameplay frame, the transcription, and signal diagnostics is then downlinked.

<figure>
  <audio controls preload="metadata" style="width: 100%;" src="/assets/images/posts/2026-07-31/command.mp3">Your browser does not support the audio element. <a href="/assets/images/posts/2026-07-31/command.mp3">Download the recording.</a></audio>
  <figcaption>The voice command as recovered on board during the evening pass, dug out of the noise floor 500 km up. The transcription in the header is what the satellite made of it: imperfect, but enough to match on.</figcaption>
</figure>

This is not a pre-scripted trigger. It is a spoken command sent over amateur radio, detected and acted on autonomously in orbit.

The Oslo Group of the Norwegian Radio Relay League ([LA4O](https://www.qrz.com/db/LA4O)) ran the [July campaign](https://radio.lb6aj.net/doom/): three of six captures triggered DOOM on the morning pass, then a live human voice reproduced it on the evening pass. They followed link tests from Legnica, Poland. Every one of them is named in the [acknowledgements](https://github.com/georgeslabreche/opssat-pretty-doomed#acknowledgements), and the experiment does not happen without them.

### Links

- [Project Page.](https://tanagraspace.com/opssat-pretty-doomed/)
- [GitHub Repository.](https://github.com/georgeslabreche/opssat-pretty-doomed)
- [Acknowledgements.](https://github.com/georgeslabreche/opssat-pretty-doomed#acknowledgements)
- [Oslo Campaign Report.](https://radio.lb6aj.net/doom/)
