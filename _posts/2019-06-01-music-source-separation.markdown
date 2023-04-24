---
layout: post
title:  "Music Source Separation"
date:   2019-06-01 15:00:44 -0800
tags: NLP
---

An exercise in audio processing for the course Computers, Sound, and Music. This project explores the strengths and weaknesses of current music source separation models, and how effectively they can be applied to audio source separation.

In this machine learning research project I have reproduced the work of Kong et al in their paper “[Decoupling Magnitude and phase estimation with deep ResUNet for music source separation](https://arxiv.org/abs/2109.05418)” (2021). Music source separation involves the separation of a music track into its constituent instruments, including audio. This topic interests me because I am pursuing Natural Language Processing. Music separation lends itself to audio separation, which can be applied in areas such as speech enhancement, and audio clarification. In particular I was interested in determining how effective a model trained on picking vocals out of songs would be at picking audio out from background noise. 

While the results are astounding in general, I found that bytesep did very poorly on classical jazz, and to a lesser degree, ska. Both of these styles include a lot of instrumental sounds in addition to the vocals and rhythm section the model was trained on. If a horn section was present, particularly if they carried the melody in a section, the model could interpret them as vocals. Additionally pure-noise or fricative-style sounds like cymbals were hard for the model to interpret, and would frequently be classified with the vocals. Fricatives have traditionally been hard for voice transcribers to interpret, so this makes sense that a sound separator would have trouble as well. Likely the model performed poorly on horn sections because it had not been trained on this data. 

In terms of vocal separation - separating a speaker from a noisy background, or from another speaker - the model did quite poorly. This makes sense since this was not strictly an audio separator model, but rather a music separator. Therefore it was classifying all audio in the vocals track, whether it be multiple speakers, background vocals, or a cheering audience. While the field of audio separation and music source separation are closely related, this project demonstrates that they are not interchangeable. Still, this project was good for introducing me to both fields and how they get applied in practice.


[Check out the code on github](https://github.com/coding-gen/cs510-comp-sound-music/tree/main/project-music-source-separation)
