# Label and scoring examples for AI/DNN/HMM English.

Examples are separated into "AmE" (American) and "BrE" (British, Australian, etc) folders for their relative accents.

5 lab files are provided.
<br>These files are meant to opened in [WaveSurfer](https://sourceforge.net/projects/wavesurfer/) with the provided configuration file.

`.wrd` shows the current word for reference purposes.
<br>`.lab` is the conventional way of phonetically labeling english for most open source and commerical software packages.
<br> &emsp; `[br]` is not labeled in these examples, however you can if you prefer and include an accomodating `[br]` note in the score.
<br>`.score` shows how the score should be timed (and lyrics written) with the audio and labels
<br> &emsp; In a real scenerio these would be XML/MIDI/etc to include pitch information.

Along with these files, two more files are included **specifically** to accomodate DiffSinger, as that software package breaks most conventions.
<br>`.DS-lab` shows how the audio should be labeled for DiffSinger. It is nearly the same except labeling breaths is NON-OPTIONAL.
<br>`.DS-score` shows how scoring works if DiffSinger. DiffSinger, being chinese centric, doesn't support placing consonants phonemes in their correct place in the syllable.
<br> &emsp; Rather, the note breaks are based on the attack of the note, so the consonants are almost always at the end of the note regardless of the place in the syllable.

The "DS-lab" examples are based on a workflow that uses [UtaUtaUtau's converter](https://github.com/UtaUtaUtau/nnsvs-db-converter#language-definition). This is to accomodate it's `[pau]` detection to segment audio. (So the converter will convert `[pau]` to `[SP]` and you can manually convert `[br]` to `[AP]`).
<br>If you are using a different workflow you will need to pre-segment your audio to 4-15 second chunks before labeling and label silence as `[SP]` and breaths as `[AP]`.
