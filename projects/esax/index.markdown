---
title: TES - E-Sax
toc: true


---

# Electronic saxophone

## Presentation



But the problem was not there…



## Features

## Status

### History

Since I was young, I was always interested into getting weird sounds out of my sax, starting with shovelling a microphone in the bell and plugging it into guitar pedals. Growing up and moving into flats where the noise level created by an acoustic saxophone can be a concern, another motivation was to be able to play silent, with headphones, allowing practice even in the middle of the night.

I then got an EWI (Electronic Wind Instrument) from [undisclosed brand]. This particular EWI was only acting as an USB-MIDI controller, which was not a bad thing because I was fairly knowledgeable of GNU/Linux suite of free synthesizers. This instrument would be tactile for the pressed keys and have an analog sensor for the breath, the latter outputting as a MIDI-CC signal (it apparently also had a "bite" sensor, but I never managed to understand how that worked, or how to make it react). Having the breath as a MIDI-CC is practical as it allows to control a variety of parameters but unfortunately very few synthesizers would be able to use that data in an expressive way, with the notable exception of [Phasex](https://github.com/williamweston/phasex) (a very powerful and surprisingly fast synthesizer, with maybe a bit too many parameters). That would rule out most simple synths and sampler like QSynth or [AMsynth](https://amsynth.github.io/).

The main problem of this machine was that the keys were tactile (capacity sensor?). Hence, a barely touched key is considered as "closed", and there is no mechanical motion of the keys. This proves to be fairly disturbing when coming from the saxophone where it is common to be at rest on the keys and pressing them down to close them. Even if the keyings are similar, the differences between these two ways of playing calls for an adaptation time when switching from one instrument to the other.

This prompted this project with the motto:

> To feel like a real sax, it has to be a real sax

And to transform a real saxophone into an EWI by keeping all the mechanical parts which give the saxophone its feel and "electrofying" it by adding sensors to it in order create MIDI signals or electronic sounds.

### Current status


## Videos

Small demonstration videos, done with live-looping on an old version of the E-sax, showing the capabilities of the instrument.
{% include video id="zAvgZpWs4oU" provider="youtube" %}
{% include video id="aQSkXTa9qaI" provider="youtube" %}


## Gallery
{% include image-gallery.html folder="/projects/esax/media" %}


