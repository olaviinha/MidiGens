# Midi Turmoil

Midi Turmoil is a collection of jupyter notebooks dedicated to MIDI related experimentation:
- generating MIDI files that are ready to be drag & dropped into a DAW
- generating MIDI from audio
- programmatically modifying MIDI files

All notebooks run in [Google Colaboratory](https://colab.research.google.com) (i.e. your browser), using your [Google Drive](https://drive.google.com/drive/my-drive) as data source and/or storage.

---

## Random Seq

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/olaviinha/MidiGenerators/blob/main/RandomSeq.ipynb)

Random Seq outputs two kinds of DAW-ready randomized midi notations based on given chord, octaves, randomized velocities etc. Preview players are provided inside the notebook.

### Arplike

![Arplike](https://storage.googleapis.com/olaviinha/github/midi-generators/rs_arp1.png)

Arplike cell takes bpm, notes per beat, and length, and generates a randomized arpeggio-like sequence. Technically it's not an arpeggio, but think of a synth arpeggio where the chord notes are randomized instead of directional.

### Bounce

![Arplike](https://storage.googleapis.com/olaviinha/github/midi-generators/rs_bnc1.png)

Bounce cell takes build-up time and fall-down time and generates randomized notation placing it in time based on a bouncing ball simulation.

### Audio Demos
Description | Generated MIDI | DAW render | 
------------ | ------------ | ------------- |
Bounce - A9sus4 and E9sus4 in 2 octaves. Bass loop added in DAW. | [.mid#1](https://storage.googleapis.com/olaviinha/github/midi-generators/rs_bnc_124bpm_A9sus4_oct3-4__afzr.mid), [.mid#2](https://storage.googleapis.com/olaviinha/github/midi-generators/rs_bnc_124bpm_E9sus4_oct3-4__aibl.mid) | [.wav](https://storage.googleapis.com/olaviinha/github/midi-generators/rs_bnc_124bpm_A9sus_e9sus4.wav)
Arplike - A9sus4 in 2 octaves | [.mid](https://storage.googleapis.com/olaviinha/github/midi-generators/ra_170bpm_A9sus4_oct3-4__ruxk.mid) | [.wav](https://storage.googleapis.com/olaviinha/github/midi-generators/ra_170bpm_A9sus4_oct3-4__ruxk.wav)
Arplike - Cmaj in 2 octaves | [.mid](https://storage.googleapis.com/olaviinha/github/midi-generators/ra_170bpm_Cmaj_oct2-3__iimg.mid) | [.wav](https://storage.googleapis.com/olaviinha/github/midi-generators/ra_170bpm_Cmaj_oct2-3__iimg.wav)

---

## Transcriber

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/olaviinha/MidiGenerators/blob/main/Transcriber.ipynb)

Transcriber takes an audio file or a youtube link, separates it into stems using Deezer Spleeter, then transcribes the track or selected stem to MIDI notation using Google Magenta's Onsets and Frames Piano Transcription.

### Audio Demos
Input | Generated MIDI | Clip of original audio | Clip of DAW-rendered MIDI
------------ | ------------ | ------------- | ------------- |
[youtube-link](https://www.youtube.com/watch?v=oUFJJNQGwhk) | [.mid](https://storage.googleapis.com/olaviinha/github/midi-turmoil/The_Cinematic_Orchestra_-_To_Build_A_Home_piano_wvxf.mid) | [.wav](https://storage.googleapis.com/olaviinha/github/midi-turmoil/orkkis.wav) | [.wav](https://storage.googleapis.com/olaviinha/github/midi-turmoil/piano.wav)
