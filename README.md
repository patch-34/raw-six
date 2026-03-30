# Patch34: Raw Six
Six-voice JSFX signal generator for REAPER

## Overview
Raw Six is a lightweight six-voice signal generator built as a JSFX plugin for REAPER.

It is designed for:
- procedural sound design
- texture and drone generation
- tonal noise layers
- experimental synthesis

The instrument is fully self-contained and can be recorded directly to audio inside REAPER.

## Features
- 6 independent voices
- Waveforms: Sine, Triangle, Square, Saw, Noise
- Frequency range: 20–7000 Hz (log-scaled)
- Optional semitone quantization
- Smooth pitch automation
- Smoothed volume changes (no clicks)
- Automatic normalization by number of active voices
- Output fade-in on unmute
- Stereo output (mono source)
- Low CPU usage

## Signal Flow
Waveform  
(optional noise shaping)  
volume smoothing  
sum of voices  
auto-normalize  
master  
fade gate  
output

## Controls

### Global
- Output — On / Muted
- Master — Global volume (0–127)
- Quantize — Off / Semitone (12-TET)

### Per Voice (01–06)
- Waveform — Sine / Tri / Square / Saw / Noise
- Freq — Base frequency (20–7000 Hz, log-scaled)
- Vol — Voice volume (0–127, smoothed)

## Recording Setup
By default, REAPER tracks record Input, not FX output.

### Manual
1. Arm the track.
2. Right-click the Record button.
3. Choose "Record: output".
4. Select stereo or mono.

### Track Template
Use the included track template.  
It already has Record: output enabled.

## Installation
Copy `Patch34_Raw_Six.jsfx` to:

macOS  
~/Library/Application Support/REAPER/Effects/

Windows  
%APPDATA%\REAPER\Effects\

Linux  
~/.config/REAPER/Effects/

Then rescan JSFX in:
Options → Preferences → Plug-ins → ReaScript / JS → Re-scan

The plugin will appear as:
JS: Raw Six

## Workflow
1. Insert the generator.
2. Set Record: output.
3. Arm the track.
4. Record audio.
5. Adjust and repeat.

## License
MIT
