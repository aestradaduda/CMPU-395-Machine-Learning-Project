1. Title
2. Introduction, general description
3. References
4. IDMT source dataset
5. Generated dataset
   1. Table of pedals
   2. table of settings
   3. Csv files
   4. Folder structure
   5. File names explanation
6. Scripts


# **GUITAR-FX-DIST:** A Dataset of Processed Guitar Recordings for Music Research

GUITAR-FX-DIST is a dataset of electric guitar recordings processed with overdrive, distortion and fuzz audio effects. It was developed for research in guitar effects detection, classification and parameters estimation. The dataset is also useful for research on automatic music trascription, intelligent music production, signal processing or effects modelling. It contains both unprocessed and processed recordings.

## **Authors**
Marco Comunità - [Centre for Digital Music](http://c4dm.eecs.qmul.ac.uk/), Queen Mary University of London

## **Reference**
If you make use of **GUITAR-FX-DIST**, please cite the following publication:

[cite] 

---
## **Dataset Snapshot**
- **Size:** ~550k samples (~305 hours) + 550k mel spectrograms 
- **Audio Format:** WAV - 44.1kHz, 16bit,  mono, -6dBFS
- **Mel-Spectrogram Format:** NPY - 128 frequency bands, sample rate 22050Hz, window length 1024, hop size 512, 
- **Effects:** 14 between overdrive, distortion and fuzz
- **Unprocessed recodings**
  - 624 monophonic notes
  - 420 polyphonic (2, 3 and 4 notes intervals and chords)
  - 2 guitars, with up to 2 pick-up settings and up to 3 plucking styles (finger pluck - hard, finger pluck - soft, pick) 
    - Schecter Diamond C-1 Classic
    - Chester Stratocaster
- **Samples length:** 2 sec

---
## **Unprocessed Recordings**
The original (unprocessed) recordings are from the [IDMT-SMT-Audio-Effects](https://www.idmt.fraunhofer.de/en/business_units/m2d/smt/audio_effects.html) dataset.

For details please refer to the website and the accompaning publication:

*Stein, Michael; Abeßer, Jakob; Dittmar, Christian; Schuller, Gerald: Automatic
Detection of Audio Effects in Guitar and Bass Recordings. Proceedings of the AES 128th
Convention, 2010.*

## **Processed Recordings**
The processed recordings are divided into 4 sub-datasets which are named depending on the unprocessed recordings used (monophonic or polyphonic) and on the settings' values (discrete or continuous).

The sub-datasets are called: Mono Discrete, Poly Discrete, Mono Continuous, Poly Continuous

Mono Discrete and Poly Discrete use a discrete set of combinations selected as the most common and representative settings a person might use (see Table of Settings).

For Mono Continuous and Poly Continuous both unprocessed samples as well as settings’ values
are drawn from a uniform distribution (10000 samples for each effect). Settings values are limited to fall between the extremes shown in the Table of Settings.

Samples:
- Mono Discrete: ~160k
- Poly Discrete: ~110k
- Mono Continuous: 140k
- Poly Continuous: 140k

---
## **Table of Effects**
| Designer | Plugin | Emulation of | Id |
| :--- | :--- | :--- | :---|
| Audified | Multidrive <br> Pedal Pro | Ibanez TS808 <br> Ibanez TS9 <br> Boss BD2 <br> Boss OD1 <br> Boss SD1 <br> Boss DS1 <br> ProCo Rat <br> MXR Distortion+ <br> Boss MT2 <br> Arbiter Fuzz Face <br> Electro-Harmonix Big Muff | 808 <br> TS9 <br> BD2 <br> OD1 <br> SD1 <br> DS1  <br> RAT <br> DPL <br> MT2 <br> FFC <br> BMF |
| Mercuriall | Greed Smasher | Mesa/Boogie Grid Slammer | MGS |
| Analog <br> Obsession | Pig Pie | Electro-Harmonix Russian Big Muff | RBM |
| | Zupaa | Vox Tone Bender | VTB |
|

---
## **Table of Controls**
The original controls names have been uniformed as shows in the following table:

| Id | Level | Gain | Tone/Eq1 | Tone/Eq2 | Tone/Eq3 | Tone/Eq4 |
| :--- | :--- | :--- | :---| :--- | :--- | :--- |
| 808 | Level | Overdrive | Tone |  |  |
| TS9 | Level | Drive | Tone |  |  |
| BD2 | Level | Gain | Tone |  |  |
| OD1 | Level | Gain |  |  |  |
| SD1 | Level | Drive | Tone |  |  |
| DS1 | Level | Dist | Tone |  |  |
| RAT | Volume | Distortion | Filter |  |  |
| DPL | Output | Distortion |  |  |  |
| MT2 | Level | Gain | Bass | Treble | Mid Level | Mid Freq |
| FFC | Volume | Fuzz |  |  |  |
| BMF | Volume | Sustain | Tone |  |  |
| MGS | Level | Drive | Tone |  |  |
| RBM | Volume | Sustain | Tone |  |  |
| VTB | Volume | Filter |  |  |  |
|

---
## **Table of Settings**
| Id | Level | Gain | Tone/Eq1 | Tone/Eq2 | Tone/Eq3 | Tone/Eq4 |
| :--- | :--- | :--- | :---| :--- | :--- | :--- |
| 808 | [1.0] | [0.2, 0.5, 0.8, 1.0] | [0.0, 0.2, 0.5, 0.8, 1.0] |  |  |
| TS9 | [1.0] | [0.2, 0.5, 0.8, 1.0] | [0.0, 0.2, 0.5, 0.8, 1.0] |  |  |
| BD2 | [1.0] | [0.2, 0.5, 0.8, 1.0] | [0.0, 0.2, 0.5, 0.8, 1.0] |  |  |
| OD1 | [1.0] | [0.2, 0.5, 0.8, 1.0] |  |  |  |
| SD1 | [1.0] | [0.2, 0.5, 0.8, 1.0] | [0.0, 0.2, 0.5, 0.8, 1.0] |  |  |
| DS1 | [1.0] | [0.2, 0.5, 0.8, 1.0] | [0.0, 0.2, 0.5, 0.8, 1.0] |  |  |
| RAT | [1.0] | [0.2, 0.5, 0.8, 1.0] | [0.0, 0.2, 0.5, 0.8, 1.0] |  |  |
| DPL | [1.0] | [0.2, 0.5, 0.8, 1.0] |  |  |  |
| MT2 | [1.0] | [0.2, 0.5, 0.8, 1.0] | [0.0, 1.0] | [0.0, 1.0] | [0.0, 1.0] | [0.0, 1.0] |
| FFC | [1.0] | [0.0, 0.2, 0.5, 0.8, 1.0] |  |  |  |
| BMF | [1.0] | [0.2, 0.5, 0.8, 1.0] | [0.0, 0.2, 0.5, 0.8, 1.0] |  |  |
| MGS | [1.0] | [0.2, 0.5, 0.8, 1.0] | [0.0, 0.2, 0.5, 0.8, 1.0] |  |  |
| RBM | [1.0] | [0.2, 0.5, 0.8, 1.0] | [0.0, 0.2, 0.5, 0.8, 1.0] |  |  |
| VTB | [1.0] | [0.0, 0.2, 0.5, 0.8, 1.0] |  |  |  |
|

---
## **Folders Tree**

```
+ DATA
    + _NoFX_mono
        *.wav
    + _NoFX_mono_preprocessed
        *.wav
    + _NoFX_poly
        *.wav
    + _NoFX_poly_preprocessed
        *.wav
    + Mono_Continuous
        + Audio
            + 808
                *.wav
                settings.csv
            + BD2
                *.wav
                settings.csv
            + ...
        + Features
            + 808
                + mel_22050_1024_512
                proc_settings.csv
            + BD2
                + mel_22050_1024_512
                proc_settings.csv
            + ...
    + Mono_Discrete
        + ...
    + Poly_Continuous
         ...
    + Poly_Discrete
        + ...
+ PLUGINS
+ SCRIPTS
```
---
## **CSV Files**
The *settings.csv* files contain the parameters values for every generated sample in their original form.

The *proc_settings.csv* files contain the parameters' values uniformed across the effects and scaled between 0.0 and 1.0.

---
## **File Names**
All the necessary info are encoded in the file names.

### **Unprocessed Monophonic**
see original dataset for complete details

Format: ABC-DDEFF-GHHI-KKKKK.wav

- A (Instrument):
  - G - guitar
- B (Make):
  - 6 - Schecter Diamond C-1 Classic, pickup position 1
  - 7 - Schecter Diamond C-1 Classic, pickup position 2
  - 8 - Chester Stratocaster, pickup position 1
  - 9 - Chester Stratocaster, pickup position 2
- C (Plucking Style):
  - 1 - Finger pluck, soft
  - 2 - Finger pluck, hard
  - 3 - Pick
- DD (Pitch MIDI number) - between 28 and 76
- E (String Number):
  - 1 - E
  - 2 - A
  - 3 - D
  - 4 - G
  - 5 - B
  - 6 - E
- FF (Fret Number): between 00 and 12
- G (Effect Group):
  - 1 - No Effect
- HH (Effect):
  - 1 - No Effect
- I (Settings Combination): 1, 2 or 3
- KKKKK (File Id)

Example: G61-40100-1111-20593.wav

### **Unprocessed Polyphonic**
see original dataset for complete details

Format: ABC-DDEEF-GHHI-KKKKK

- A (Instrument):
  - G - guitar
- B (Make):
  - 6 - Schecter Diamond C-1 Classic, pickup position 1
  - 9 - Chester Stratocaster, pickup position 2
- C (Playing Technique):
  - 4 - two-note interval
  - 5 - 3- or 4-note chord
- DD (Pitch MIDI number) - between 28 and 76
- EE (Polyphony Type):
  - 11 - Minor Third
  - 12 - Major Third
  - 13 - Fouth
  - 14 - Fifth
  - 15 - Minor Seventh
  - 16 - Major Seventh
  - 17 - Octave
  - 21 - Major Triad
  - 22 - Minor Triad
  - 23 - Sus4 Triad
  - 24 - Power Chord
  - 25 - Major Seventh Chord
  - 26 - Minor Seventh Chord
  - 27 - Diminished Seventh Chord
- F (Fret Number n.a.): 0 
- G (Effect Group):
  - 1 - No Effect
- HH (Effect):
  - 1 - No Effect
- I (Settings Combination): 1, 2 or 3
- KKKKK (File Id)


Example: P64-43110-1111-41185

### **Processed Monophonic and Polyphonic**
Format: ABC-DDEEF-GGG-HIHI...-KKKKK

- GGG (Effect ID): see Effects Table
- H (Setting Name):
  - B - Bass
  - D - Drive/Dist/Distortion
  - F - Filter
  - G - Gain
  - MF - Mid Freq
  - ML - Mid Level
  - O - Overdrive
  - S - Sustain
  - T - Treble
- I (Settings Value): between 0 and 10 with one decimal place
- KKKKK (File Id)

Example: G61-40100-808-O2.1T10-20593

Generated from: G61-40100-1111-20593

---
## **Scripts**
The dataset includes the MATLAB scripts used to generate the samples:
- *script_to_generate_continuous_datasets.m* was used to generate the Mono_Continuous and Poly_Continuous datasets
- *script_to_generate_discrete_datasets.m* was used to generate the Mono_Discrete and Poly_Discrete datasets