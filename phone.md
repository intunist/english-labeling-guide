# Table of contents
- [Introduction](#Introduction)
- Phoneme sets
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

| **Phoneme** | **Word**                 | **IPA**     | **AuE IPA** | **X-SAMPA** | **SynthV** | **Vocaloid (Broken)** |                                                                                                               |
| ----------- | ------------------------ | ----------- | ----------- | ----------- | ---------- | --------------------- | ------------------------------------------------------------------------------------------------------------- |
| ah          | hUt, hUndred             | /ʌ/         | /a/         | V           | ah         | V                     |                                                                                                               |
| aa          | cAlm, cAr                | /ɑ/ /⁠a/     | /a/         | A           | aa         |                       | /a/ is included for reference but uncommon/merged with /ɑ/. If desired it can be added as [au] (a-unrounded). |
| oh          | plOt, blOnde, nOt        | /ɒ/         | /ɔ/         | Q           |            | Q                     |
| ao          | nAUght, cORe, All        | /ɔ/ /⁠o/     | /o/         | O           | ao         | O:                    |
| ae          | bAth, bAt, nAsty         | /æ/ /⁠ɑ/     | /æ/         | ({) (A)     | ae         | ({) (e@0)             | For BrE and AuE /æ/ and /ɑ/ are merged into the [ae] phoneme. (refer to [#Q&A](#Q&A)                          |
| ax          | commA                    | /ə/         | /ə/         | @           | ax         | @                     | Is merged with [uh] in some forms of APRAbet. While ok for speech,  merging causes issues for singing.        |
| iy          | bEAt                     | /i/         | /i/         | i           | iy         | i:                    |                                                                                                               |
| ih          | sIt, demOn, Example      | /ɪ/ /⁠ɨ/     | /ɪ/ /ɨ/     | I           | ih         | I                     | Merged with [ix] with no reprecussions. (refer to [#Q&A](#Q&A)                                                  |
| uh          | bOOk                     | /ʊ/         | /ʊ/         | U           | uh         | U                     |                                                                                                               |
| uw          | bOOt                     | /u/         | /ʉ/         | u           | uw         | u:                    |                                                                                                               |
| eh          | bEt                      | /ɛ/         | /e/         | E           | eh         | E                     |                                                                                                               |
| er          | bIRd, sIR, colOR, mothER | /ɜ/ /⁠ɚ/ /⁠ə/ | /ɚ/ /ɜ/ /ə/ | (@\`) (3)   | er         | @r                    | Merged with [axr] with no reprecussions. (refer to #Q&A(#Q&A)                                                 |

 - [axr] is ommitted as it's handled contextually by [er]
 - [ix] is ommitted as it's handled contextuall by [ih] (refer to [#Q&A](#Q&A))

# BrE Phoneme set - Northern Variant
The Northern variant has several adjustments made to accomodate the unique challenges of Northern BrE dialects.
It should be noted this specifically refers to dialects found in the northern region of _the island of Great Britain_. If the speaker is off-island it is more likely you want the Southern Variant of the phoneme set.
| **Phoneme** | **Word**                 | **IPA**    | **X-SAMPA** | **SynthV** | **Vocaloid (Broken)** |                                                                                                    |
| ----------- | ------------------------ | ---------- | ----------- | ---------- | --------------------- | -------------------------------------------------------------------------------------------------- |
| aa          | cAlm                     | /ɑ/ /⁠a/    | A           | aa         |                       |                                                                                                    |
| oh          | plOt, blOnde, nOt        | /ɒ/        | Q           |            | Q                     |                                                                                                    |
| ao          | nAUght, cORe, All, yAWn  | /o/ /⁠ɔ/    | o           | ao         | O:                    | Some northern BrE goes from /ɔ/ to strict /o/ for “or”. But symbol assignment is unchanged         |
| ae          | bAth, bAt, gAs, glAss    | /æ/        | ({) (A)     | ae         | ({) (e@0)             | Northern dialects only have a single “ae” vowel. So the note for Southern dialects can be ignored. |
| ax          | commA                    | /ə/        | @           | ax         | @                     |                                                                                                    |
| iy          | bEAt                     | /i/        | i           | iy         | i:                    |                                                                                                    |
| ih          | sIt, demOn, Example      | /ɪ/ /⁠ɨ/    | I           | ih         | I                     | Merged with [ix] with no reprecussions. (refer to [#Q&A](#Q&A)                                     |
| uh          | bOOk, hUt, hUndred       | /ʊ/ /⁠ʌ/    | U           | uh         | U                     | Northern BrE speakers merge /ʊ/ /ʌ/ into one sound. Therefore, [ah] is excluded entirely.          |
| uw          | bOOt                     | /u/        | u           | uw         | u:                    |                                                                                                    |
| eh          | bEt                      | /ɛ/        | E           | eh         | E                     |                                                                                                    |
| er          | bIRd, colOR, mothERship, | /ɜ/ /⁠ɚ/ /⁠ə/| (@\`) (3)   | er         | @r                    | Loose use of er, and ax. Dilution while singing means [er] is often optional for many speakers.    |

- The Manchester dialect has an interesting quirk where [aa]⁠(/ɑ/) becomes /ɔ/ when r-colored. And example of this would be the word "car". Thankfully context handles this, so it can be ignored and labeled with [aa] as per usual ([k aa r]).


# AmE Phoneme set
This set is the closest to standard Arpabet, _however_ it does have several extras that many find invaluable and have worked their way into common use for both English and Japanese datasets. For cleanliness most of those phonemes now reside in #Utility-Phonemes

# Utility Phonemes
These are phonemes that have special purposes outside simply labeling speech sounds.

# Q&A
### Why doesn't the phoneme set include [ix]?
>For context, [ix] refers to the i-shaped schwa. The [ix] phoneme was deemed useless after much testing and merging it into [ih] is both standard practice and works flawlessly thanks it to it largely being length contextual.
Unforuntely it's also too difficult for most speakers to accurately identify [ix] so it's best to exclude it as a unique phoneme.
>
>**Long answer:**
>Some Arpabet-based systems include [ix] to handle the i-shaped schwa. However it's common to use the [ih] symbol instead. the "i-schwa" often replaces [ih] and [eh] in lax syllables, so the word "example" is most often [ih g z ae m p ax l] when short and/or lax and [eh g z ae m p ax l] when the first syllable has more stress applied, it's not necessarily related to length.. [ih] works perfectly well for AI-based singing synthesis and simplifies the labeling process as the vast majority of speakers cannot reliably identify [ix] and will always confuse it for another phoneme.
### Why is [axr] excluded from the phoneme set?
>While some arpabet-derivatives choose to include [axr] as a symbol, the model is fully capable of learning the correct context with the [er] symbol alone. No need to copmlicate things!
>On top of this, the sound(s) [axr] would represent on it's own are fairly rare or non-existant for **Northern BrE** dialects.
### Why are /æ/ and /ɑ/ merged?
While incredibly weird looking, it works correctly and is fine.
>The only minor quirk is that the model may confuse northern and southern dialects with _tiny_ amounts of data.
>Note that most singers standardize to the southern dialect. Regardless, the model will learn the original dialect in our testing.
>One can still choose to label these phonemes separetely by utilizing both [ae] and [aa], however note this will increase user-error when using a model with an unfamiliar dialect. This should be supported in the final phonemizer.
>"I personally hate this but it works" - Soup
### tr dr nonsense
>(to add) Please don't use [tr] and [dr] phonemes. Something artifact of old Elenor version for SynthV with broken pronuncation.
### How do I handle linking and intrusive r sounds?
>Sometimes a vowel becomes [er] or adds an [r] for vowel linkages. This is referred to as the "intrusive R". It is recommended to still label these as their original vowel and allow the model to learn the contextual change.
>"Idea of" may sound like "idear of" to split the vowels. But you would never label the [r].
>The same relatively applies to the "linking r" but in reverse. Where a word with an expected r drops the r when another consonant is already in place to split the vowels.
>For example, "four dogs" will not have an audible [r] and instead would have a softer schwa. However, "four otters" would have an audible linking r. In both cases you will want to include an [r] phoneme to provide context to the model.
### How do I handle r-colored vowels?
>There are no symbols for r-colored vowels because the [r] phoneme handles this. When between two vowels the [r] phoneme triggers a rhotic. When the next phoneme is a consonant it will drop the rhotic but make the prior vowel r-colored.
