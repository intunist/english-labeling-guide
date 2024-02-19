# Table of contents
- [Introduction](#Introduction)
- PHoneme sets
  - BrE Phoneme set - Southern/AuE/International
  - BrE Phoneme set - Northern
  - AmE Phoneme set
  - Consonants - general
  - Utility Phonemes
- Q&A

(editing note, QA section may be removed and each phoneme section may have it's own instead)

# Introduction
The system we use for English labeling is called **AMBIbet**.

AMBIbet is a phonetic system based on ARPAbet with alterations made to make it more universally compatible with non-American dialects.
It is extended from our previous work standardizing English for NNSVS!

_Why base it on ARPAbet?_
ARPAbet is a widely known and accepted standard for inputting English phonetics. It has wide availability and compatibility.
We chose it especially to be more readily accessible and inclusive to users without requiring users to learn an entirely new phonetic system or struggle with more complex or incompatible systems such as IPA-derived X-SAMPA!

While we chose to repurpose ARPAbet for the BrE extension of AMBIbet, months of careful considerations were still taken to ensure wide support for international English.

The actual phonetic symbols we decided to use _technically_ did not matter as the __**functionality would be the same**__, however we chose and believe an ARPAbet-derived system was the best way to present our work.

### AMBIbet has been verified to work perfectly for over 20 speakers/unique dialects!

Here we provide three base vowel systems.
The most common, the Southern BrE vowel set, is for nearly all non-American English speakers including Australian. Southern BrE is the primary accent most British-leaning accents aim for and is the best option for most speakers targeting a British dialect.
Separate reference IPA phonetics are provided for AuE (Australian English) speakers to clear any confusion. Generally speaking, AuE and Northern BrE speakers will most often use the same AMBIbet symbols for the same words.

The second option is Northern BrE. Northern speakers have a unique set of dialectal quirks that make it unique enough to need its own special vowel set to accurately portray them!
This includes a lot of vowel dropping and special considerations for small local dialects.

Then the third set, for Americans and what nearly everyone uses in the NNSVS space, is also provided.

Our system is designed for compatibility _and_ interoperability between dialects with minimal effort. American, British, Australian, etc.
Along with this, we are working on 3 pronunciation dictionaries (AmE, N.Bre, S.BrE) that will extend to a **per-dialect selectable G2P system for OpenUTAU**.

# BrE Phoneme set - Southern and International Variant
This is the primary phoneme set, designed for most speakers with a British-leaning accent. It also accomodates Australian English.

| **Phoneme** | **Word**          | **IPA** | **AuE IPA** | **X-SAMPA** | **SynthV** | **Vocaloid (Broken)** |                                                                                                                                                                                                                                                  |
| ----------- | ----------------- | ------- | ----------- | ----------- | ---------- | --------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| ah          | hUt, hUndred      | /ʌ/     | /a/         | V           | ah         | V                     |                                                                                                                                                                                                                                                  |
| aa          | cAlm, cAr         | /ɑ/ /a/ | /a/         | A           | aa         |                       | /a/ is included for reference but uncommon/merged with /ɑ/. If desired it can be added as [au] (a-unrounded). Refer to the [ae] phoneme for concatenative synthesis as BrE uses [aa] and [ae] interchangeably for words like “bath”, “hat”, etc. |
| oh          | plOt, blOnde, nOt | /ɒ/     | /ɔ/         | Q           |            | Q                     |
| ao          | nAUght, cORe, All | /ɔ/ /o/ | /o/         | O           | ao         | O:                    |
| ae          | bAth, bAt, nAsty  | /æ/     | /æ/         | ({) (A)     | ae         | ({) (e@0)             |                                                                                                                                                                                                                                                  |
| ax          | commA             | /ə/     | /ə/         | @           | ax         | @                     |                                                                                                                                                                                                                                                  |
| iy          | bEAt              | /i/     | /i/         | i           | iy         | i:                    |                                                                                                                                                                                                                                                  |
| ih          | sIt               | /ɪ/     | /ɪ/ /ɨ/     | I           | ih         | I                     |                                                                                                                                                                                                                                                  |
| ix          | demOn, Example    | /ɨ/     | /ɨ/         |             |            |                       | Only makes sense for concatenative synths (ie UTAU users)                                                                                                                                                                                        |
| uh          | bOOk              | /ʊ/     | /ʊ/         | U           | uh         | U                     |                                                                                                                                                                                                                                                  |
| uw          | bOOt              | /u/     | /ʉ/         | u           | uw         | u:                    |                                                                                                                                                                                                                                                  |
| eh          | bEt               | /ɛ/     | /e/         | E           | eh         | E                     |                                                                                                                                                                                                                                                  |
| er          | bIRd, sIR         | /ɜ/     | /ɚ/ /ɜ/ /ə/ | (@\`) (3)   | er         | @r                    |                                                                                                                                                                                                                                                  |
| axr         | colOR, mothER     | /ɚ/ /ə/ | /ɚ/         |             |            |                       | concatenative only.                                                                                                                                                                                                                              |


# BrE Phoneme set - Northern Variant
The Northern variant has several adjustments made to accomodate the unique challenges of Northern BrE dialects.

# AmE Phoneme set
This set is the closest to standard Arpabet, _however_ it does have several extras that many find invaluable and have worked their way into common use for both English and Japanese datasets. For cleanliness most of those phonemes now reside in #Utility-Phonemes

# Utility Phonemes
These are phonemes that have special purposes outside simply labeling speech sounds.

# Q&A
> Why doesn't the phoneme set include [ix]?

For reader context, [ix] refers to the i-shaped schwa. The [ix] phoneme was deemed useless after much testing and merging it into [ih] is both standard practice and works flawlessly thanks it to it largely being length contextual.
Unforuntely it's also too difficult for most speakers to accurately identify [ix] so it's best to exclude it as a unique phoneme.

> tr dr nonsense
