# Stravigor

A music notation rendering engine for Android.

Stravigor is currently in early stages of design and development.

## Overview

Upon redesigning [Vivace](https://github.com/colematthew4/Vivace), I wanted to use a rendering engine that could satisfy a series of goals:

- *Easily transposable with musicxml schema*
- Can have multiple staves for different instruments or melodies
- Notes:
  - must be selectable in the following contexts:
    - individually
    - multiplicatively
    - across staves
  - must have the ability to render marking types, like:
    - [accidentials](https://en.wikipedia.org/wiki/Accidental_(music))
        (for special markings, e.g double flats/sharps, naturals quarter tones, etc)
    - [articulations](https://en.wikipedia.org/wiki/List_of_musical_symbols#Articulation_marks)
        (staccato, spiccato, accent, tenuto, marcato, fermata)
    - [ornaments](https://en.wikipedia.org/wiki/List_of_musical_symbols#Ornaments)
        (trill, mordent, turn, apoggiatuea, acciaccatura)
    - other instrument-specific notations (pizzicato, harmonics, directional bowing for strings,
        pedal marks for piano, mallet numbers for percussion, etc)
- Stave, measure, and note metadata is independent of each other
- Allow custom text markers

I did research on existing rendering engines that would be compatable with Vivace, and found libraries that only worked in the browser ([Verovio](https://github.com/rism-ch/verovio), [VexFlow](https://github.com/0xfe/vexflow)) or OpenGL-based projects like the [Guido Project](https://github.com/grame-cncm/guidolib) that limited user interaction with notation elements. This is how I arrived at Stravigor.
