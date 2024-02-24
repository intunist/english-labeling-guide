# Table of contents
- [Introduction](#Introduction)
- Phoneme sets
  - [BrE Phoneme set - Southern/AuE/International](#bre-phoneme-set---southern-and-international-variant)
  - [BrE Phoneme set - Northern](#bre-phoneme-set---northern-variant)
  - [AmE Phoneme set](#ame-phoneme-set)
  - [Consonants - general](#ame-phoneme-set)
  - [Utility Phonemes](#utility-phonemes)
- [Q&A](#qa)

(editing note, QA section may be removed and each phoneme section may have it's own instead)

# Introduction
The system we use for English labeling is called **AMBIbet**.

AMBIbet is a phonetic system based on ARPAbet with alterations made to make it more universally compatible with non-American dialects.
It is extended from our previous work standardizing English for NNSVS!

_Why base it on ARPAbet?_
ARPAbet is a widely known and accepted standard for inputting English phonetics. It has wide availability and compatibility.
We chose it especially to be more readily accessible and inclusive to users without requiring users to learn an entirely new phonetic system or struggle with more complex or incompatible systems such as IPA-derived X-SAMPA!

While we chose to re-purpose ARPAbet for the BrE extension of AMBIbet, months of careful considerations were still taken to ensure wide support for international English.

The actual phonetic symbols we decided to use _technically_ did not matter as the __**functionality would be the same**__, however we chose and believe an ARPAbet-derived system was the best way to present our work.

### AMBIbet has been verified to work perfectly for over 20 speakers/unique dialects!

Here we provide three base vowel systems.
The most common, the Southern BrE vowel set, is for nearly all non-American English speakers including Australian. Southern BrE is the primary accent most British-leaning accents aim for and is the best option for most speakers targeting a British dialect.
Separate reference IPA phonetics are provided for AuE (Australian English) speakers to clear any confusion. Generally speaking, AuE and Northern BrE speakers will most often use the same AMBIbet symbols for the same words.

The second option is Northern BrE. Northern speakers have their own set of dialectal quirks that make it unique enough to require its own special vowel set to accurately portray them!
This includes a lot of vowel dropping and special considerations for small local dialects.

Then the third set, for Americans and what nearly everyone uses in the NNSVS space, is also provided.

Our system is designed for compatibility _and_ interoperability between dialects with minimal effort. American, British, Australian, etc.
Along with this, we are working on 3 pronunciation dictionaries (AmE, N.Bre, S.BrE) that will extend to a **per-dialect selectable G2P system for OpenUTAU**.

# BrE Phoneme set - Southern and International Variant
This is the primary phoneme set, designed for most speakers with a British-leaning accent. It also accommodates Australian English.

| **Phoneme** | **Common Name**  | **Word**                 | **IPA**     | **AuE IPA** | **X-SAMPA** | **SynthV** | **Vocaloid (Broken)** |                                                                                                               |
| ----------- | ---------------- | ------------------------ | ----------- | ----------- | ----------- | ---------- | --------------------- | ------------------------------------------------------------------------------------------------------------- |
| ah          | short u          | hUt, hUndred             | /ʌ/         | /a/         | V           | ah         | V                     |                                                                                                               |
| aa          | broad/long a     | cAlm, cAr                | /ɑ/ /⁠a/     | /a/         | A           | aa         |                       | /a/ is included for reference but uncommon/merged with /ɑ/. If desired it can be added as [au] (a-unrounded). |
| oh          | short o          | plOt, blOnde, nOt        | /ɒ/         | /ɔ/         | Q           |            | Q                     |
| ao          | long             | nAUght, cORe, All        | /ɔ/ /⁠o/     | /o/         | O           | ao         | O:                    |
| ae          | short a          | bAth, bAt, nAsty         | /æ/ /⁠ɑ/     | /æ/         | ({) (A)     | ae         | ({) (e@0)             | For BrE and AuE /æ/ and /ɑ/ are merged into the [ae] phoneme. (refer to [#Q&A](#qa))                          |
| ax          | short            | commA                    | /ə/         | /ə/         | @           | ax         | @                     | Is merged with [uh] in some forms of APRAbet. While ok for speech,  merging causes issues for singing.        |
| iy          | long e           | bEAt                     | /i/         | /i/         | i           | iy         | i:                    |                                                                                                               |
| ih          | short i          | sIt, demOn, Example      | /ɪ/ /⁠ɨ/     | /ɪ/ /ɨ/     | I           | ih         | I                     | Merged with [ix] with no reprecussions. (refer to [#Q&A](#a))                                                 |
| uh          | short oo         | bOOk                     | /ʊ/         | /ʊ/         | U           | uh         | U                     |                                                                                                               |
| uw          | long oo          | bOOt                     | /u/         | /ʉ/         | u           | uw         | u:                    |                                                                                                               |
| eh          | short e          | bEt                      | /ɛ/         | /e/         | E           | eh         | E                     |                                                                                                               |
| er          | long             | bIRd, sIR, colOR, mothER | /ɜ/ /⁠ɚ/ /⁠ə/ | /ɚ/ /ɜ/ /ə/ | (@\`) (3)   | er         | @r                    | Merged with [axr] with no repercussions. (refer to #Q&A(#Q&A)                                                 |
| ay          | long i           | bIte                     | /aɪ/        | /ɑɪ/        | aI          | ay         | aI                    |                                                                                                               |
| aw          | long             | abOUt                    | /aʊ/        | /æɔ/        | aU          | aw         | aU                    |                                                                                                               |
| ey          | long             | bAIt                     | /eɪ/        | /æɪ/        | eI          | ey         | eI                    |                                                                                                               |
| oy          | long             | bOY                      | /ɔɪ/        | /oɪ/        | OI          | oy         | OI                    |                                                                                                               |
| ow          | long o           | bOAt                     | /əʊ/ /oʊ/   | /əʉ/        | (@U) (oU)   | ow         | @U                    |                                                                                                               |

Note that short/long naming conventions are antiquated and inaccurate. They are only provided for reference and understanding. These are especially inaccurate for singing (and Australian English, which uses it's own short/long vowel designations).
 - [axr] is omitted as it's handled contextually by [er]
 - [ix] is omitted as it's handled contextually by [ih] (refer to [#Q&A](#qa))
 - AuE is fully supported, however note there may be some confusion with multiple symbols covering the same phoneme. This is because many sounds in AuE are realized as "long/short" versions of the same exact phoneme. Such as /a/ for strut and /aː/ for palm. You could potentially merge down these sounds, however at the moment it is suggested to not do this. This is both a "just in case" due to dialect variation and to allow AuE datasets to be compatible with BrE dictionaries and G2P while retaining correct pronunciations.

# BrE Phoneme set - Northern Variant
The Northern variant has several adjustments made to accommodate the unique challenges of Northern BrE dialects.
It should be noted this specifically refers to dialects found in the northern region of _the island of Great Britain_. If the speaker is off-island it is more likely you want the Southern Variant of the phoneme set.
| **Phoneme** | **Common Name**  | **Word**                 | **IPA**    | **X-SAMPA** | **SynthV** | **Vocaloid (Broken)** |                                                                                                    |
| ----------- | ---------------- | ------------------------ | ---------- | ----------- | ---------- | --------------------- | -------------------------------------------------------------------------------------------------- |
| aa          | broad/long a     | cAlm                     | /ɑ/ /⁠a/    | A           | aa         |                       |                                                                                                    |
| oh          | short o          | plOt, blOnde, nOt        | /ɒ/        | Q           |            | Q                     |                                                                                                    |
| ao          | long             | nAUght, cORe, All, yAWn  | /o/ /⁠ɔ/    | o           | ao         | O:                    | Some northern BrE goes from /ɔ/ to strict /o/ for “or”. But symbol assignment is unchanged         |
| ae          | short a          | bAth, bAt, gAs, glAss    | /æ/        | ({) (A)     | ae         | ({) (e@0)             | Northern dialects only have a single “ae” vowel. So the note for Southern dialects can be ignored. |
| ax          | short            | commA                    | /ə/        | @           | ax         | @                     |                                                                                                    |
| iy          | long e           | bEAt                     | /i/        | i           | iy         | i:                    |                                                                                                    |
| ih          | short i          | sIt, demOn, Example      | /ɪ/ /⁠ɨ/    | I           | ih         | I                     | Merged with [ix] with no reprecussions. (refer to [#Q&A](#qa)                                      |
| uh          | short oo         | bOOk, hUt, hUndred       | /ʊ/ /⁠ʌ/    | U           | uh         | U                     | Northern BrE speakers merge /ʊ/ /ʌ/ into one sound. Therefore, [ah] is excluded entirely.          |
| uw          | long oo          | bOOt                     | /u/        | u           | uw         | u:                    |                                                                                                    |
| eh          | short e          | bEt                      | /ɛ/        | E           | eh         | E                     |                                                                                                    |
| er          | long             | bIRd, colOR, mothERship, | /ɜ/ /⁠ɚ/ /⁠ə/| (@\`) (3)   | er         | @r                    | Loose use of er, and ax. Dilution while singing means [er] is often optional for many speakers.    |
| ay          | long i           | bIte                     | /aɪ/       | aI          | ay         | aI                    |                                                                                                    |
| aw          | long             | abOUt                    | /aʊ/       | aU          | aw         | aU                    |                                                                                                    |
| ey          | long             | bAIt                     | /eɪ/       | eI          | ey         | eI                    |                                                                                                    |
| oy          | long             | bOY                      | /ɔɪ/       | OI          | oy         | OI                    |                                                                                                    |
| ow          | long o           | bOAt                     | /əʊ/ /oʊ/  | (@U) (oU)   | ow         | @U                    |                                                                                                    |

Note that short/long naming conventions are antiquated and inaccurate. They are only provided for reference and understanding. These are especially inaccurate for singing.
- The Manchester dialect has an interesting quirk where [aa] (/ɑ/) becomes /ɔ/ when r-colored. And example of this would be the word "car". Thankfully context handles this, so it can be ignored and labeled with [aa] as per usual ([k aa r]).

# AmE Phoneme set
This set is the closest to standard Arpabet, _however_ it does have several extras that many find invaluable and have worked their way into common use for both English and Japanese datasets. For cleanliness most of those phonemes now reside in #Utility-Phonemes
| **Phoneme** | **Common Name**  | **Word**                 | **IPA**     | **X-SAMPA** | **SynthV** | **Vocaloid (Broken)** |                                                                                                                                                                                                                 |
| ----------- | ---------------- | ------------------------ | ----------- | ----------- | ---------- | --------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| ah          | short u          | hUt, hUndred             | /ʌ/         | V           | ah         | V                     |                                                                                                                                                                                                                 |
| aa          | long a          | cAlm, cAr, plOt          | /ɑ/ /⁠ɒ/      | A           | aa         | Q                     | The merging of these two vowels has worked flawlessly in all public and private datasets thus far. There is no reason to change that. Most Americans cannot reliably identify/differentiate these vowels either. |
| ao          | long o           | cORe, All                | /ɔ/         | O           | ao         | O:                    |                                                                                                                                                                                                                 |
| ae          | short a          | bAth, bAt, nAsty         | /æ/          | ({)         | ae         | ({) (e@0)             |                                                                                                                                                                                                                 |
| ax          | short            | commA                    | /ə/         | @           | ax         | @                     |                                                                                                                                                                                                                 |
| iy          | long e           | bEAt                     | /i/         | i           | iy         | i:                    |                                                                                                                                                                                                                 |
| ih          | short i          | sIt, demOn, Example      | /ɪ/         | I           | ih         | I                     |                                                                                                                                                                                                                 |
| uh          | short oo         | bOOk                     | /ʊ/         | U           | uh         | U                     |                                                                                                                                                                                                                 |
| uw          | long oo/u        | bOOt                     | /u/         | u           | uw         | u:                    |                                                                                                                                                                                                                 |
| eh          | short e          | bEt                      | /ɛ/         | E           | eh         | E                     |                                                                                                                                                                                                                 |
| er          | long             | bIRd, sIR, colOR, mothER | /ɜ/ /⁠ɚ/ /⁠ɝ/   | (@\`) (3)   | er         | @r                    |                                                                                                                                                                                                                 |
| ay          | long i           | bIte                     | /aɪ/        | aI          | ay         | aI                    |                                                                                                                                                                                                                 |
| aw          | long             | abOUt                    | /aʊ/        | aU          | aw         | aU                    |                                                                                                                                                                                                                 |
| ey          | long             | bAIt                     | /eɪ/        | eI          | ey         | eI                    |                                                                                                                                                                                                                 |
| oy          | long             | bOY                      | /ɔɪ/        | OI          | oy         | OI                    |                                                                                                                                                                                                                 |
| ow          | long o           | bOAt                     | /əʊ/ /oʊ/   | (@U) (oU)   | ow         | @U                    |                                                                                                                                                                                                                 |

# Consonants - General
| **phoneme** | **Example**                           | **IPA**  | **Description**                                                            |
| ----------- | ------------------------------------- | -------- | -------------------------------------------------------------------------- |
| p           | PoP                                   |          |                                                                            |
| b           | BoB                                   |          |                                                                            |
| t           | TaT, Tree                             |          | Phoneme contex handling.                                                   |
| d           | DaD, Drink                            |          | Phoneme contex handling.                                                   |
| k           | CaKE                                  | /k/ /kʰ/ |                                                                            |
| g           | GaG                                   |          |                                                                            |
| s           | SaS                                   |          |                                                                            |
| z           | ZooS                                  |          |                                                                            |
| ch          | CHurCH                                |          |                                                                            |
| jh          | JuDGE                                 |          | Makes 'dg' sound for end of words. like [d][zh] or /dZ/ in xsampa.         |
| sh          | Ship, puSH                            |          |                                                                            |
| zh          | pleaSure                              |          | The 'judge' example is [j ah d zh], not [j ah zh]. To avoid any confusion. |
| f           | FlooF                                 |          |                                                                            |
| v           | Verge, nerVe                          |          |                                                                            |
| hh          | Herb(BrE), Happy(AmE)                 |          | syllable onset only. Use [exh] for end-of-note exhales.                    |
| th          | THin, myTH                            |          |                                                                            |
| dh          | THis, widTH                           |          |                                                                            |
| n           | NaNNy, paN                            |          |                                                                            |
| m           | MoM, MoMent                           |          |                                                                            |
| ng          | baNG, suNG                            |          |                                                                            |
| w           | Wisp                                  |          | syllable onset only.                                                       |
| y           | Yes                                   |          | syllable onset only.                                                       |
| r           | Road, caR                             |          | rhotic shares same phoneme. It's fine. UK dropped r as well.               |
| l           | List, caLL                            |          | dark L shares same phoneme. It's fine.                                     |
| q           | boTTom(BrE), we-eat(AmE), batten(AmE) |          | glottal stop and vowel separator. NOT vocal fry.                           |
| dx          | shuTup(BrE), buTTer(AmE)              |          | tapped/flapped d/tt. Use in UK English is spotty.                          |
| rr          | peRRo                                 |          | Trilled r (like in spanish)                                                |
| rx          | fuRet, bRechen                        |          | Fricative r (like in german or french)                                     |
| x           | loCH                                  |          | Voiceless velar fricative. Scottish/Welsh specific.                        |

Consonants that have a vowel-like quality in terms of sustain.
These are entirely optional as no G2P will EVER support these due to them being incredibly situational (you CANNOT replace every instance).
| **phoneme** | **Example**    |                                                                     |
| ----------- | -------------- | ------------------------------------------------------------------- |
| el          | peopLE, doubLE | USE [ax l] INSTEAD, vowellike l, where l makes most of the syllable |
| em          | bottOM         | USE [ax m] INSTEAD, vowellike m, where m makes most of the syllable |
| en          | buttON         | USE [ax n] INSTEAD, vowellike n, where n makes most of the syllable |

 - Note that combinations such as [tr] and [dr] do not exist. Some users have referenced an early version of Eleanor Forte for SynthV R1(?) which only had these phonemes due to mispronunciations in this early voice. It is a bodge to fix a quirk, not something that should be replicated. Not even SynthV makes much use of this in it's current state.
   - In addition to this, the difference between the [t] in "take" and "tree" (and [d] in "day" and "drink") are handled contextually. DO NOT supplement these with [ch] and [jh] as that is incorrect and unsupported everywhere. It bares no functional improvement either and [t][r] and [d][r] has been proven time and time again to work without issue. It only serves to make your resulting model incompatible with everything else as it’s non-standard.
 - Differences in aspiration and voicing are handled contextually. No additional symbols are required to handle these cases (such as [k], [t], [d], or [hh]).
 - Phonemes such as [ty], [ky], etc are JAPANESE ONLY and should not be done at all for English labeling. Not even for borrowed words.
   - For example "kyoku" would be [k y ow][k uw] NOT [ky ow][k uw].

# Utility Phonemes
These are phonemes that have special purposes outside simply labeling speech sounds.
Note that [exh], [axh], and [vf] were introduced by Ambision/Intunist and are custom to AMBIbet. You will not find these in any common/normal ARPAbet dataset.
| phoneme | Example          | Description                                                                                            |
|---------|------------------| -------------------------------------------------------------------------------------------------------|
| pau     | silence          | During unsung/silent periods.                                                                          |
| br      | [breath]         | **NOT TO BE USED FOR NNSVS. ALSO NOTE DIFFSINGER HAS IT'S OWN AP/SP SYSTEM**                           |
| exh     | [exhale]         | end breaths, end of phrase exhale. devoiced. Label consonant coda.                                     |
| axh     | [release]        | voiced variation of [exh]. voiced schwa exhale/release. Label as consonant coda.                       |
| vf      | [vocal fry]      | vocal fry. Can be used as a consonant OR on it's own note.                                             |

**THESE ARE NONSTANDARD and have almost no applicable use-case**. They are best avoided wherever possible. They are provided as they are custom additonal phonemes in Ambision's (Intunist's) NNSVS english support.
| phoneme | Example          | Description                                                                                            |
|---------|------------------| -------------------------------------------------------------------------------------------------------|
| ct      | [closure-toggle] | override the default state of a consonant's closure. Entirely optional.                                |
| cl      | [held stop]      | Held stop/plosive consonant. For when the silence is held. Similar to Japanese usage but not syllabic. |

# Q&A
### Why is the Vocaloid reference labeled "broken"?
>Vocaloid's implementation of SAMPA appears to be broken. It is not possible to approximate it to British phonetics due to it's lack of /A/ and incorrect use of /Q/ and /O/. Several phonemes have odd/non-standard mappings that don't function or exist at all outside of Vocaloid.
### Why is [ix] excluded from the phoneme set?
>For context, [ix] refers to the i-shaped schwa. The [ix] phoneme was deemed useless after much testing and merging it into [ih] is both standard practice and works flawlessly thanks it to it largely being length contextual.
Unfortunately it's also too difficult for most speakers to accurately identify [ix] so it's best to exclude it as a unique phoneme.
>
>**Long answer:**
>Some Arpabet-based systems include [ix] to handle the i-shaped schwa. However it's common to use the [ih] symbol instead. the "i-schwa" often replaces [ih] and [eh] in lax syllables, so the word "example" is most often [ih g z ae m p ax l] when short and/or lax and [eh g z ae m p ax l] when the first syllable has more stress applied, it's not necessarily related to length.. [ih] works perfectly well for AI-based singing synthesis and simplifies the labeling process as the vast majority of speakers cannot reliably identify [ix] and will always confuse it for another phoneme.
### Why is [axr] excluded from the phoneme set?
>While some arpabet-derivatives choose to include [axr] as a symbol, the model is fully capable of learning the correct context with the [er] symbol alone. No need to complicate things!
>On top of this, the sound(s) [axr] would represent on it's own are fairly rare or non-existent for **Northern BrE** dialects.
### Why are /æ/ and /ɑ/ merged?
>While incredibly weird looking, it works correctly and is fine.
>
>The only minor quirk is that the model may confuse the correct sound with _tiny_ amounts of data.
>Note that most singers standardize to the southern dialect. Regardless, the model will learn the original dialect in our testing.
>One can still choose to label these phonemes separately by utilizing both [ae] and [aa], however note this will increase user-error when using a model with an unfamiliar dialect. This should be supported in the final phonemizer.
>
>"I personally hate this but it works" - Soup
### What is [tr] and [dr]? (Why you SHOULDN'T do this)
> 𝒫𝓁𝑒𝒶𝓈𝑒 DO NOT use [tr] and [dr] when labeling your dataset.
> SynthV included these as an artifact of **incorrect/broken pronunciation** in the **old Elenaor Forte Standard (non-AI) voice**. Not even SynthV makes much use of this anymore and the current voices handle [t][r] and [d][r] without it.
>
> Some users have claimed that using [tr] and [dr] may provide "lower loss" without any evidence supporting this (and much existing evidence _against it_).
> Even if it did result in a _slightly_ lower loss in _a single_ use-case, that is not how loss metrics should be used as _any_ change can have small effects on the loss value.
> For speech synthesis tasks, human-perception is more important and this would be teeth pulling...
>
> Given that [t][r] and [d][r] is common in ALL existing English datasets and models with absolutely no issue with it, it is STRONGLY RECOMMENDED to not break from this.
### How do I handle linking and intrusive r sounds?
>Sometimes a vowel becomes [er] or adds an [r] for vowel linkages. This is referred to as the "intrusive R". It is recommended to still label these as their original vowel and allow the model to learn the contextual change.
>"Idea of" may sound like "idear of" to split the vowels. But you would never label the [r].
>The same relatively applies to the "linking r" but in reverse. Where a word with an expected r drops the r when another consonant is already in place to split the vowels.
>For example, "four dogs" will not have an audible [r] and instead would have a softer schwa. However, "four otters" would have an audible linking r. In both cases you will want to include an [r] phoneme to provide context to the model.
### How do I handle r-colored vowels?
>There are no symbols for r-colored vowels because the [r] phoneme handles this. When between two vowels the [r] phoneme triggers a rhotic. When the next phoneme is a consonant it will drop the rhotic but make the prior vowel r-colored.
