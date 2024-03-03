NOTE: THIS IS A DRAFT. Please open an issue or contact for questions, concerns, etc

# Intunist Guide to English labeling very rough draft
### For DiffSinger and NNSVS

This is a guide to assist with consistent, easier, and stable labeling.
Inconsistency in labels causes undesirable and unexpected results in trained models, which can be an incredible headache. (ex: a model being unusable to all but who labeled it).
This guide along with it's Github repo will provide examples on best practices for english labels.

All information and methods in this guide has been tested heavily for accuracy and compatibility with synthesis systems.

These label guidelines can be carried over to nearly all speech and singing vocal synthesis software.

Some aspects regarding syllabification may not be specifically relevent for DiffSinger due to it's limited handling of phoneme placement, but are still useful concepts to understand. Notes are provided where applicable.
All other information is validated for DiffSinger.

---
### NOTE FOR UTAU USERS:
please bare in mind concepts learned from the use of the UTAU software DO NOT carry over to ML/AI/DNN/HTS systems AT ALL.
It is best to assume most of what you know may not be suitable for an easier experience.

---
Guide is optimized for BrE as Intunist current production datasets focuses on this dialect.
However this guide is valid for any and all major dialects of english, including notes for particular broad dialects.

Intunist plans on releasing an 8hr singing dataset and models for pretraining.
<br>These models, when available, should help reduce the workload and allow more stable models with less data.

Bear in mind we want to _mostly label_ English **PHONEMICALLY NOT phonetically**. Based on how it sounds in context and not being painfully accurate, to allow for natural reproduction of the singing voice.
<br>Labeling based on the intention and not the exact phoneme used is idea in most cases.
<br>While vowels are generally labeled stylistically/exactly as pronounced (can be personal preference), consonants are labeled based on their phonological grouping.
<br>Most speakers cannot distinguish fine phonetic differences accurately and handling it broadly allows us to rely on the model to handle these differences naturally.
<br>Exceptions are/can be [dx] and [ax] where one may prefer having more control of these sounds.
<br>**HOWEVER, if you, for example, randomly/stylistically pronounce a word like "sleep" as [s l ey p] instead of [s l iy p] then it makes much more sense to label it as [ey]!**
<br> **STYLE OVERRIDES THE "CORRECT" PHONEME!**

<sup>1</sup> Exceptions do occur, as we are inconsistent humans, however if you find you are making exceptions more often than not you should stop making that exception and allow the model to learn it as a default behavior.

[**DiffSinger base phone dict**](https://github.com/intunist/diffsinger-english-support) (remove phonemes you do not use, handled automatically by some training notebooks)
<br>[**NNSVS English HED**](https://github.com/intunist/nnsvs-english-support)

---
## Phonemes: (as separate linked markdown document.)
For compatibility with the most vocal synthesis systems possible, Intunist makes use of a lightly modified Arpabet.
<br>This modified version has careful consideration for most English Dialects

(Notes for public phoneme lists, to remove:)
- Full phone set
- Simple phone set
  Simplified phoneme set which may make labeling and use easier for non-native speakers.
  Note that a simplified phoneme set may have issues with context and sound a tad awkward in some situations.
    - remove ax (may break schwa in long note context)
	- may remove el, em, en as these were always optional
	- may remove [dx] and use [t] instead (with context).


(NEW PHONEME DOCUMENT)[phone.md]
The new phone.md contains all information at once, rather than separate files for various dialects.

----------

## Consonants
Consonants are almost labeled exactly as you think.
<br>However, keep in mind clusters at the START of words like "tree" and "dream".
<br>Users from the UTAU community have a very bad habit of labeling these with [ch r] and [jh r] and this is INCORRECT.
<br>AI handles phonetics contextually and the "t" and "d" in these examples aren't even the same sound as "ch" and "j". They are unique sounds.
<br>Not to mention the average person will default to using [t] and [d] when typing phonetics and all existing pronunciation dictionaries do too.
<br>For compatibility with 100% of the existing tools, models, etc, you should label as [t r] and [d r].
<br>This method also perfectly represents and recreates the original pronunciation of the vocalist without the user having to think about it.
<br>
<br>Given that 100% of NNSVS and nearly all DiffSinger English models do this and work perfectly well, and all existing support is for it, it is HIGHLY ADVISABLE to continue doing the same to avoid complications.
<br>
As a related note, [tr] and [dr] are INVALID phonemes and only exist as an artifact/bodge of SynthV's early development. These were introduced due to poor pronunciation in their Eleanor Forte product and isn't even consistent between other voices for SynthV.
<br>For AI singing synthesis these phonemes are completely useless, serve no function, and introduce the complication of spreading your data thin. Label the phonemes individually. Effectively less than useless.
<br>
<br>NOTE: Some DiffSinger users claim that "[ch r] and [jh r] is more accurate and provides better loss" but no proof has been provided for this. Perhaps only when data is below 15 minutes.
<br>In Intunist's rigorous testing this has not been the case and has no real practical benefit outside of being more comfortable for a small subset of UTAU users.
<br>Given that nothing is compatible with this and no one else (SynthV, Vocaloid, CMU, etc) does this, it is our recommendation to continue using [t r] and [d r]
<br>If there is enough demand, Intunist could provide a version of our G2P model that supports this.
<br>	However bare in mind that there is NO way to properly support it as it causes every user to label their models differently.

# Vowels
You can label vowels in two ways, perceptually or "correct/strict" to the dictionary,
<br>This is up to personal preference and neither will make or break a model. It will remain compatible regardless.
<br>Intunist recommends for new users to label vowels "perceptually".
<br>As in, if the vowel in context of the phrase sounds correct, even if it's stylistically altered, to still label it as that vowel.
<br>Of course, if a vowel is VERY obviously different, then you should change the label.
<br>- For example, if "sleep" is pronounced as "sleyp" with a clear vowel replacement, label it as such.
<br>
<br>If you choose to label "correct/strict", you risk the model being awkward (less data) or unable to sing outside the genres of it's original data (more data, not necessarily bad).
<br>Choose which you feel is more appropriate for your dataset.

## Syllabification:
Words with multiple syllables can look challenging but are often fairly simple.
A syllable is split into 3 sections. Onset, nucleus, coda.
[[IMAGE]]
Think of onset and coda as the regions where consonants reside and the nucleus is the vowel sound.
Most existing methods of syllibification are created around the idea of arbitrary concepts created by linguists.
In general, these methods are based around conceptual units of speech or person-preference of the person who devised it.
<br>Ambi has devised a way of dividing syllables SPECIFICALLY for _singing_ synthesis. Based around actual physical articulation and ease.
In multi-syllable words:
- Most coda consonants become onset consonants for the next syllable in the same word.
	- "except" is [ eh - k s eh p t] NOT [eh k - s eh p t]
    - EXCEPT fluids (m, n, ng, l, r) IF PAIRED with another consonant after.
        - singing is [s ih - ng ih ng] NOT [s ih ng - ih ng]
        - single is [s ih ng - g ax l] NOT [s ih - ng g ax l]
		- lethargic is [l ax - th aa r - jh ih k] NOT [l ax - th aa - r jh ih k]
	- EXCEPT in COMPOUND words.
	    - soundbite is [s ow n d - b ay t] NOT [s ow n - d b ay t]
		- yourself is [y ao r - s eh l f] NOT [y ao - r s eh l f]
	- EXCEPT in suffixes that start with a consonant. Often has micro-pause.
	    - youthful is [y uw th - f ax l] NOT [y uw - th f ax l]
	- FOR THE PREVIOUS it may help to conceptualize these consonant combinations as requiring a "pause" to transition.
	- whisper is [w ih - s p er] NOT [w ih s - p er]
	    - [s p] is a common starting cluster and part of the same root word.
- Rhotics paired with another consonant are NOT transferred to the next syllable. IN A PRIOR VERSION they were carried for "international consistency" but doing so is incredibly broken.
    - clearly is [k l ih r - l iy] NOT [k l ih - r l iy]
- Sometimes an [r] can be pronounced as either a rhotic or a starting r. This changes the syllabification.
	- when an [r] is surrounded by two vowels, even if it is technically a rhotic it is often functionally a starting [r] for the next syllable.
	- Most dictionaries will transcibe "carry" as [k ae r - iy] but most speakers in a singing context (ESPECIALLY NON-AMERICAN) will actually pronounce [k ae - r iy].
	- can often times can be difficult to discern. For non-american dialects it is ALWAYS carried over, otherwise you may use your own discretion but most times it's safer to place the [r] at the start of the next syllable.
		- For an [r] of long length and/or heavily colors the prior vowel you may choose to place [r] at the end of the prior syllable, however even in these cases you can get away with keeping it at the beginning of the next syllable if you prefer.
		- Even the later note about when to treat as a rhotic isn't truly consistent and you can often get away with always carrying the [r] to the next syllable
	- NOTE THAT EVEN IF [r] IS MOVED TO THE NEXT SYLLABLE, THE VOWEL NOTES FOR THE [RHOTICS](#Rhotics) SECTION ARE STILL VALID. This is due to these [r] technically still being rhotic.
### FOR DIFFSINGER:
DiffSinger has a limited syllable system where note start is defined by phoneme placement.
- In the  most general sense place **ALL** consonants at the end of the note/split.
- The [r] within a start cluster (like **cr**ow) will actually go at the **START** of the next split as the [r] in these cases is after the note-start/attack.
- For example, "The crow squawks" would be [ dh | ax k | **r** ow s k w | aa k s ]


## Rhotics:
- [iy r] with a rhotic is an invalid label, always label as [ih r].
(artifact of human labeling with lacking symbols)
(actually i-shape schwa [ix])
(context handles it as long as handled correctly)
Clear:	[k l ih r] NOT [k l iy r]
Ear:	[ih r]
Hero:	[hh ih - r ow]
NON RHOTIC:
Erase:	[**iy** - r ey s] (non-rhotic, r is part of a separate syllable and does not color the prior vowel)
> This is difficult to explain and some dialects will sound as if words like "clear" and "hero" use a distinct "iy" sound.
> In most of these cases this is due to how the brain handles language and speech processing, causing a [iy] to be incorrectly heard.
> Even if your dialect makes a distinct [iy] it is best practice to still label with [ih] for consistency and compatibility. Context will handle the rest.
> <br>**If you have enough data** (>4 hours) you may label _both_ so users can use them interchangeably. But this can reduce quality on smaller datasets as examples are split between phonemes.
- EXCEPTION: [iy r] can be labeled for very VERY intentional stylistic choices for additional singer control. However don't do this for general cases.
- Mistakes in labeling this causes difficulty when using models as users have to guess which vowel was used.
    - Can be easily fixed in bulk using Notepad++ or other tool with text replace.
- [ey r] is an invalid label for smooth monophthonic vowels, always label as [eh r]. This is due to the rhotic changing the shape of the vowel causing confusion.
	- it may seem reasonable to use [ey] if it is pronounced as [eh - iy] but this is often two separate syllables. Of course exceptions do occur. As long as you do not label smooth vowels as [ey] and diphthonic vowels as [eh] it should be ok.
- [uw r] is an invalid label. Label as [uh r].
- LABEL DROPPED RHOTICS. Especially in BrE/AuE dialects. (example: car crash [k aa r - k r ae sh] NOT [k aa - k r ae sh]
    - This gives the model very important context. In BrE these dropped rhotics often exist as a very short schwa. Without this label the model will not produce the correct pronunciation.
    - Many American dialects also feature dropped rhotics.
- DO NOT label linking [r] in ANY dialect. This is a specific dialect trait, let model handle it as part of vowel contextually.
    - "I saw a" [ay - s aa - ah] NOT [ay - s aa r - ah]
- Almost NEVER label an r-r transition UNLESS it involves two word ending and starting with an [r]. For example "here is" should ONLY have one [r] even if the attack is strong.

## Diphthongs:
- Runs with diphthongs should use repeated phonemes.
    - [ay - ay - ay] NOT [aa - aa - ay]
    - DIFFSINGER ONLY: You can label runs with a SINGLE vowel label but split across multiple notes. **NOTE:** this will prevent multiple/split-phoneme cases from working entirely if done exclusively.
	
## Runs and held vowels:
- vowels held over multiple notes carries the vowel along.
	- "steels" across two notes is [s t iy][iy l z]
		- across 3 notes it is [s t iy] [iy] [iy l z]
    - Has same diffsinger notice as [above](#Diphthongs)

## Phonemic quirks/rules:
- [iy ng] doesn't exist, always label as [ih ng]
- [aa l] is invalid, always label as [ao l]
    - fall [f ao l]
	- falling [f ao - l ih ng]
    - alder [ao l - d er] 
    - some dictionaries will label US English with [aa l] and [ao l] sporatically and UK English with [ao l] exclusively. This is an odd arbitrary decision with no real purpose.
    - NOTE: For American (AmE) English it becomes [aa - l] for multi-syllable words. This is due to light/dark [l] differences.
        - abolish is [aa - b **aa** - l ih sh] NOT [aa - b **ao** - l ih sh]
        - biology is [b ay - **aa** - l ax - jh iy] not [b ay - **ao** - l ax - jh iy]
- [iy l] can sometimes sound like [iy ax l], label as [iy l] as this is not a true vowel and more a transition from [iy] to [l]
- Incidental sounds, such as "new" being pronounced as [n y uw] or [n ih uw], the [y]/[ih] should be ignored in most cases.
	- This is because the [ih] is ACTUALLY [ix] (i-shape schwa). Very easy confusion. Same as [ax] in the prior note.
- unstable pronunciations (vowels that drift rapidly) are generally best labeled as a stable vowel.
    - example: My Chemical Romance "sleEeEeEep" sounding as [s l iy ih iy ih iy p] is labeled as simple [s l iy p]
- voiced and devoiced [hh] share the same phoneme. Handled by context in model.
    - dropped [hh] such as "in her" (sounds like [ih - n er]) should still have the [hh] labeled shortly as part of the tap.
- [ey ng] doesn't exist. Should always be labeled as [ae ng]
    - "canker" is [k ae ng - k er] not [k ey ng - ker]
    - NOT to be confused with [eh ng], the difference is vowel frontness ([ae] is more forward and [eh] more central). 
    - I personally hate this but seems to be universally accepted (~heteric)
	- NOT TO BE CONFUSED FOR [eh ng] THAT IS VALID.
		- if it sounds more like [ey] it is [ae]. If it's cleaner and lower then it is [eh] (although [eh ng] is much more rare).
		- "length" is [l eh ng (k) th] but "bank" is [b ae ng k]
- AuE QUIRKS
    - Sometimes [iy] sounds like [ih] or [ax] for brief moments. Continue to label as [iy]
	- There are three variations of the [ae] phoneme. These can all share the same label without problem.

## Devoiced vowels:
Devoiced/whispered vowels do not have their own phoneme. Instead it is best to use variance in DiffSinger or a flag in NNSVS.

## Don't reference the CMU dictionary:
Blasphemy!
The struggle is CMU Dict was never designed for singing synthesis in mind. It has many odd inconsistencies and lacks some important phonemes.
If you know what you are doing it can be a valuable resource, however for a novice many mistakes may be made.
Once you are comfortable and understand the rules here you may be able to use CMU Dict and mentally correct it as you work.

[Intunist provides a REFERENCE-ONLY dictionary to assist with syllabification.](https://github.com/hetteric/english-labeling-guide/blob/main/reference/AmE_guide_dictionary_v0.5.txt)
This dictionary cannot be used for synthesis but should be a useful resource. It contains over 40,000 words and their syllable breaks.
Please bare in mind this dictionary may break rules stated in this resource. Please ignore the dictionary mistakes and follow the rules in this document. Report any inconsistency please.
