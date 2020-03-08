# Rastra

A music notation rendering engine for Android.

## Overview

Upon redesigning [Vivace](https://github.com/colematthew4/Vivace), I wanted to use a rendering engine that could satisfy a series of goals:

- Exportable to musicxml by default
  - Custom exporter can be configured if desired
- All notation elements must have hooks for user interaction
  - Notes must be selectable individually, multiplicatively, or across different staves
  - Markings, like [accidentals](https://en.wikipedia.org/wiki/Accidental_(music)), <!-- (for special markings, e.g double flats/sharps, naturals quarter tones, etc) -->
      [articulations](https://en.wikipedia.org/wiki/List_of_musical_symbols#Articulation_marks), <!-- (staccato, spiccato, accent, tenuto, marcato, fermata) -->
      [ornaments](https://en.wikipedia.org/wiki/List_of_musical_symbols#Ornaments), <!-- (trill, mordent, turn, apoggiatuea, acciaccatura) -->
      and other instrument-specific notations (pizzicato, harmonics, directional bowing for strings, pedal marks for piano, mallet numbers for percussion, etc)
      can be set upon drawing or be calculated by the renderer
- Allow custom textboxes
- Dynamics, note relationships (ties, tuplets, glissando, etc), and text is anchored to notes

I did research on existing rendering engines that would be compatible with Vivace, and found libraries that only worked in the browser
([Verovio](https://github.com/rism-ch/verovio), [VexFlow](https://github.com/0xfe/vexflow)) or OpenGL-based projects like the
[Guido Project](https://github.com/grame-cncm/guidolib) that limited user interaction with notation elements.

Thus, Rastra was born.

Rastra is currently in early stages of design and development.
