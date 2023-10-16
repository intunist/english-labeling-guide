NOTE: THIS IS A DRAFT.

# Intunist Guide to English labeling very rough draft
### For DiffSinger and NNSVS

This is a guide to assist with consistent, easier, and stable labeling.
Inconsistency in labels causes undesirable and unexpected results in trained models, which can be an incredible headache. (ex: a model being unusable to all but who labeled it).
This guide along with it's Github repo will provide examples on best practices for english labels.

These label guidelines can be carried over to nearly all speech and singing vocal synthesis software.
Some aspects may not be relevent for DiffSinger due to time/scoring method but may still be useful to understand. A future update will help distinguish specifics.

---
### NOTE FOR UTAU USERS:
please bare in mind concepts learned from the use of the UTAU software DO NOT carry over to ML/AI/DNN/HTS systems.
It is best to assume most of what you know may not be suitable for an easier experience.

---
Guide is optimized for BrE as Intunist current production datasets focuses on this dialect.
However this guide should be valid for any and all major dialects of english, including notes for particular broad dialects.

((Intunist plans on releasing an 8hr singing dataset and models for pretraining.))
This model, when available, should help reduce the workload and allow more stable models with less data.

Bare in mind we want to label English PHONEMICALLY NOT PHONETICALLY.
(1)We are labeling based on the intention not the exact phoneme used in most cases.
Most speakers cannot distinguish fine phonetic differences accurately and handling it broadly allows us to rely on the model to handle these differences naturally.
Exceptions are/can be [dx] and [ax] where one may prefer having more control of these sounds.
!!1!! Exceptions do occur, as we are inconsistent humans, however if you find you are making exceptions more often than not you should stop making that exception and allow the model to learn it as a default behavior.

DiffSinger base phone dict: [url] (remove phonemes you do not use)
<br>NNSVS English HED: [url]

---
## Phonemes: (as separate linked markdown document.)
For comparability with the most vocal synthesis systems possible, Intunist makes use of a lightly modified Arpabet.
This modified version has careful consideration for most English Dialects
- Full phone set
- Simple phone set
  Simplified phoneme set which may make labeling and use easier for non-native speakers.
  Note that a simplified phoneme set may have issues with context and sound a tad awkward in some situations.
    - remove ax (may break schwa in long note context)
	- may remove el, em, en as these were always optional
	- may remove [dx] and use [t] instead (with context).

(US/AmE PHONETICS LIST)[phone_AmE.md]

(UK/BrE PHONETICS LIST)[phone_AmE.md]


AU/AuE PHONETICS LIST
(refer UK until next update)

----------
## Syllabification:
Words with multiple syllables can look challenging but are often fairly simple.
A syllable is split into 3 sections. Onset, nucleus, coda.
[[IMAGE]]
Think of onset and coda as the regions where consonants reside and the nucleus is the vowel sound.
In multi-syllable words
- Most coda consonants become onset consonants for the next syllable in the same word.
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
- Rhotics are also transferred to the next syllable. For international consistency.
    - sorrow is [s aa - r ow] NOT [s aa r - ow]

## Rhotics:
- [iy r] is an invalid label, always label as [ih r].
(artifact of human labeling with lacking symbols)
(actually i-shape schwa [ix])
(context handles it as long as handled correctly)
Clear:	[k l ih r] NOT [k l iy r]
Ear:	[ih r]
Hero:	[hh ih - r ow]
- This is difficult to explain and some dialects will sound as if words like "clear" and "hero" use a distinct "iy" sound.
- In most of these cases this is due to how the brain handles language and speech processing, causing a [iy] to be incorrectly heard.
- Even if your dialect makes a distinct [iy] it is best practice to still label with [ih] for consistency and compatibility. Context will handle the rest.
- EXCEPTION: [iy r] can be labeled for very VERY intentional sylistic choices for additional singer control. However don't do this for genral cases.
- Mistakes in labeling this causes difficulty when using models as users have to guess which vowel was used.
    - Can be easily fixed in bulk using Notepad++ or other tool with text replace.
- LABEL DROPPED RHOTICS. Especially in BrE dialects.
    - This gives the model very important context. In BrE these dropped rhotics often exist as a very short schwa.
- NO NOT label linking [r]. Let model handle it as part of vowel.
    - "I saw a" [ay - s aa - ah] NOT [ay - s aa r - ah]

## Diphthongs:
- Runs with diphthongs should use repeated phonemes.
    - [ay - ay - ay] NOT [aa - aa - ay]
    - DIFFSINGER ONLY: You can label runs with a SINGLE vowel label but split across multiple notes.
	
## Runs and held vowels:
- vowels held over multiple notes carries the vowel along.
	- "steels" across two notes is [s t iy][iy l z]
		- across 3 notes it is [s t iy] [iy] [iy l z]

## Phonemic quirks/rules:
- [iy ng] doesn't exist, always label as [ih ng]
- [aa l] is invalid, always label as [ao l]
    - fall [f ao l]
	- falling [f ao - l ih ng]
- [iy l] can sometimes sound like [iy ax l], label as [iy l] as this is not a true vowel and more a transition from [iy] to [l]
- Incidental sounds, such as "new" being pronounced as [n y uw], the [ih] should be ignored in most cases.
	- This is because the [ih] is ACTUALLY [ix] (i-shape schwa). Very easy confusion.
- unstable pronunciations (vowels that drift rapidly) are generally best labeled as a stable vowel.
    - example: My Chemical Romance "sleEeEeEep" sounding as [s l iy ih iy ih iy p] is labeled as simple [s l iy p]
- voiced and devoiced [hh] share the same phoneme. Handled by context in model.
    - dropped [hh] such as "in her" (sounds like [ih - n er]) should still have the [hh] labeled shortly as part of the tap.
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

Intunist provides a REFERENCE-ONLY dictionary to assist with syllabification.
This dictionary cannot be used for synthesis but should be a useful resource. It contains over 40,000 words and their syllable breaks.
Please bare in mind this dictionary may break rules stated in this resource. Please ignore the dictionary mistakes and follow the rules in this document. Report any inconsistency please.