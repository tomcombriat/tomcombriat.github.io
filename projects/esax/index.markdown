---
title: TES - E-Sax
toc: true


---

# Electronic saxophone

## Presentation

The E-Sax is an Electronic Wind Instrument (EWI) based on a real saxophone, providing a feeling as close as possible to the acoustic instrument. This allows saxophone players to immediatly feel at ease with this instrument while being able to create breath-expressive electronic sounds.
It outputs MIDI and as such needs to be connected to a synthesizer for instance a [10k synth](/projects/8_10ksynths).



## Features/specs

These are the features of the latest version:

 - MIDI output
 - High resolution breath (12 bits), controlling two MIDI CCs
 - different keyings, classic, EWI style, …
 - screen for checking the settings of the instrument
 - joystick for menu navigation, custom MIDI CC and pitchbend
 - easily changeable presets via custom keyings
 - possibility to generate chords and arpegiators via custom keyings
 - Teensy (soon changed to RP2040) MCU

## Status

### History

Since young age, I was always interested into getting weird sounds out of my sax, starting with shovelling a microphone in the bell and plugging it into guitar pedals. Growing up and moving into flats where the noise level created by an acoustic saxophone can be a concern, another motivation was to be able to play silent, with headphones, allowing practice even in the middle of the night.

I then got an EWI (Electronic Wind Instrument) from [undisclosed brand]. This particular EWI was only acting as an USB-MIDI controller, which was not a bad thing because I was fairly knowledgeable of GNU/Linux suite of free synthesizers. This instrument would be tactile for the pressed keys and have an analog sensor for the breath, the latter outputting as a MIDI-CC signal (it apparently also had a "bite" sensor, but I never managed to understand how that worked, or how to make it react). Having the breath as a MIDI-CC is practical as it allows to control a variety of parameters but unfortunately very few synthesizers would be able to use that data in an expressive way, with the notable exception of [Phasex](https://github.com/williamweston/phasex) (a very powerful and surprisingly fast synthesizer, with maybe a bit too many parameters). That would rule out most simple synths and sampler like QSynth or [AMsynth](https://amsynth.github.io/).

The main problem of this machine was that the keys were tactile (capacity sensor?). Hence, a barely touched key is considered as "closed", and there is no mechanical motion of the keys. This proves to be fairly disturbing when coming from the saxophone where it is common to be at rest on the keys and pressing them down to close them. Even if the keyings are similar, the differences between these two ways of playing calls for an adaptation time when switching from one instrument to the other.

This prompted this project with the motto:

> To feel like a real sax, it has to be a real sax

And to transform a real saxophone into an EWI by keeping all the mechanical parts which give the saxophone its feel and "electrofying" it by adding sensors to it in order create MIDI signals or electronic sounds.

### Current status

This instrument underwent a lot of different versions. After a quick prototypes based on a PVC tube with switches to prove the concept, it soon moved to using real saxophones as a base, slowly increasing reliability and features with time. This process included a huge variety of MCU, from AVR based boards, to RP2040 via STM32F1 and Teensy.

Because of the specificities of these different boards, and of the different saxophones, the code has become increasingly hard to maintain and to port between the different hardware versions, leading to a lot of similar, but not quite the same, software versions.

For this reason, the code is now undergoing a huge refractoring and rethinking. The main change will be to have as much as possible of it as a [library](https://github.com/tomcombriat/TES_eSax-lib) so that the improvements are automatically propagated to the different hardware versions, with the main code containing only the hardware details of the instruments.

While at it, there might be a few improvements for instance:

 - possibility to have chords and arpegiators at the same time
 - MIDI clock input/output
 - ...


## Videos

Small demonstration videos, done with live-looping on an old version of the E-sax, showing the capabilities of the instrument.
{% include video id="zAvgZpWs4oU" provider="youtube" %}
{% include video id="aQSkXTa9qaI" provider="youtube" %}


## Gallery
{% include image-gallery.html folder="/projects/esax/media" %}


