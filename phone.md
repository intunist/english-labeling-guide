# Table of contents
- [Introduction](#Introduction)
- Phoneme sets
  - [BrE Phoneme set - Southern/AuE/International](#bre-phoneme-set---southern-and-international-variant)
  - [BrE Phoneme set - Northern](#bre-phoneme-set---northern-variant)
  - [SSE Phoneme set](sse-phoneme-set---scottish-english)
  - [AmE Phoneme set](#ame-phoneme-set)
  - [CanE Phoneme set](#cane-phoneme-set)
  - [Consonants - general](#consonants---general)
  - [Utility Phonemes](#utility-phonemes)
- [Q&A](#qa)

# Introduction
The system we use for English labeling is called **AMBIbet**.

AMBIbet is a ~~phonetic~~ phonemic system based on ARPAbet with alterations made to make it more universally compatible with non-American dialects.
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

Then a third set, for Americans and what nearly everyone uses in the NNSVS space, is also provided.
Canadian English is provided as well but due to phonetic similarities to American English it's mostly notes and reference material rather than a unique phoneme set.

Our system is designed for compatibility _and_ interoperability between dialects with minimal effort. American, British, Australian, etc.
Along with this, we are working on 3 pronunciation dictionaries (AmE, N.Bre, S.BrE) that will extend to a **per-dialect selectable G2P system for OpenUTAU**.

ALONG WITH THIS PHONEME DOC, PLEASE REFER TO [GUIDE.MD](GUIDE.md)

# BrE Phoneme set - Southern and International Variant
This is the primary phoneme set, designed for most speakers with a British-leaning accent. It also accommodates Australian English.
<br>**You cannot label British, Australian, or related dialects with the American English set. It will NOT function.** It won't even Americanize the voice, it'll simply have broken pronuncation with no control to adjust it.

| **Phoneme** | **Common Name**  | **Word**                 | **IPA**     | **AuE IPA** | **X-SAMPA** | **SynthV** | **Vocaloid (Broken)** |                                                                                                               |
| ----------- | ---------------- | ------------------------ | ----------- | ----------- | ----------- | ---------- | --------------------- | ------------------------------------------------------------------------------------------------------------- |
| ah          | short u          | hUt, hUndred             | /ʌ/         | /a/         | V           | ah         | V                     |                                                                                                               |
| aa          | broad/long a     | cAlm, cAr                | /ɑ/ /⁠a/     | /a/         | A           | aa         |                       | /a/ is included for reference but uncommon/merged with /ɑ/. If desired it can be added as [au] (a-unrounded). |
| oh          | short o          | plOt, blOnde, nOt        | /ɒ/         | /ɔ/         | Q           |            | Q                     |
| ao          | long             | nAUght, cORe, All        | /ɔ/ /⁠o/     | /o/         | O           | ao         | O:                    |
| ae          | short a          | bAth, bAt, nAsty         | /æ/ /⁠ɑ/     | /æ/         | ({) (A)     | ae         | ({) (e@0)             | For BrE and AuE /æ/ and /ɑ/ are merged into the [ae] phoneme. (refer to [#Q&A](#qa))                          |
| ax          | short            | commA                    | /ə/         | /ə/         | @           | ax         | @                     | Is merged with [uh] in some forms of APRAbet. While ok for speech,  merging causes issues for singing.        |
| iy          | long e           | bEAt                     | /i/         | /i/         | i           | iy         | i:                    |                                                                                                               |
| ih          | short i          | sIt, demOn, Example      | /ɪ/ /⁠ɨ/     | /ɪ/ /ɨ/     | I           | ih         | I                     | Merged with [ix] with no reprecussions. (refer to [#Q&A](#qa))                                                 |
| uh          | short oo         | bOOk                     | /ʊ/         | /ʊ/         | U           | uh         | U                     |                                                                                                               |
| uw          | long oo          | bOOt                     | /u/         | /ʉ/         | u           | uw         | u:                    |                                                                                                               |
| eh          | short e          | bEt                      | /ɛ/         | /e/         | E           | eh         | E                     |                                                                                                               |
| er          | long             | bIRd, sIR, colOR, mothER | /ɜ/ /⁠ɚ/ /⁠ə/ | /ɚ/ /ɜ/ /ə/ | (@\`) (3)   | er         | @r                    | Merged with [axr] with no repercussions. (refer to #Q&A(#qa)                                                 |
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
| er          | long             | bIRd, colOR, mothERship  | /ɜ/ /⁠ɚ/ /⁠ə/| (@\`) (3)   | er         | @r                    | Loose use of er, and ax. Dilution while singing means [er] is often optional for many speakers.    |
| ay          | long i           | bIte                     | /aɪ/       | aI          | ay         | aI                    |                                                                                                    |
| aw          | long             | abOUt                    | /aʊ/       | aU          | aw         | aU                    |                                                                                                    |
| ey          | long             | bAIt                     | /eɪ/       | eI          | ey         | eI                    |                                                                                                    |
| oy          | long             | bOY                      | /ɔɪ/       | OI          | oy         | OI                    |                                                                                                    |
| ow          | long o           | bOAt                     | /əʊ/ /oʊ/  | (@U) (oU)   | ow         | @U                    |                                                                                                    |

Note that short/long naming conventions are antiquated and inaccurate. They are only provided for reference and understanding. These are especially inaccurate for singing.
- The Manchester dialect has an interesting quirk where [aa] (/ɑ/) becomes /ɔ/ when r-colored. And example of this would be the word "car". Thankfully context handles this, so it can be ignored and labeled with [aa] as per usual ([k aa r]).

# SSE Phoneme set - Scottish English
This is the phoneme set for Scottish English. It's not vastly different from the other variants but helps to explain some dialect changes.
Scottish english has heavy influence from Scots, so many of the phonemes are vastly different from what one would expect.
Technically one can reference the sBre or nBrE symbols and infer the changes but this will help with consistency.

| **Phoneme** | **Word**                  | **IPA**     | **X-SAMPA** |                                                                                                               |
| ----------- | ------------------------- | ----------- | ----------- | ------------------------------------------------------------------------------------------------------------- |
| ah          | hUt, hUndred, strUt       | /ʌ/ /ɐ/     | V           |                                                                                                               |
| aa          | cAlm, cAr, trAp, bAth     | /ɑ/ /⁠a/      | A           |                                                                                                               |
| ao          | nAUght, cORe, All, plOt   | /ɔ/         | O           | note: "a" before coda [l] is standardized to [ao] for all dialects.                                           |
| ax          | commA                     | /ə/         | @           | Is merged with [uh] in some forms of APRAbet. While ok for speech,  merging causes issues for singing.        |
| iy          | bEAt                      | /i/         | i           |                                                                                                               |
| ih          | sIt, demOn, Example, citY | /ɪ/ /⁠ɨ/       | I           | Merged with [ix] with no repercussions. (refer to [#Q&A](#qa))                                                |
| uh          | bOOk, bOOT, gOOse, cUre   | /ʉ/         | }           |                                                                                                               |
| uw          | hOUse                     | /u/         | u           |                                                                                                               |
| eh          | bEt                       | /ɛ/         | E           |                                                                                                               |
| <s>er</s>   | mothER (**REFER BELOW**)  | /ər/ /⁠ɚ/ /⁠ə/  | @\`         | SSE lacks the fern–fir–fur merger. Use below examples for non-"er" cases. Still exists as a reduced form.     |
| [ah r]      | fUR, tURn                 | /ʌ r/       | V\`         |                                                                                                               |
| [eh r]      | fERn, pERson              | /ɛ r/       | E\`         |                                                                                                               |
| [ih r]      | fIR, fIRst                | /ɪ r/       | I\`         |                                                                                                               |
| ay          | bIte, nIce                | /əɪ/ /aɪ/   | @I          | [ay] is more centralized in SSE. But the label is the same.                                                   |
| aw          | abOUt, hOW, mOUth         | /əʉ/ /aʉ/   | @}          | [aw] is more centralized in SSE. But the label is the same.                                                   |
| ey          | bAIt, wAit                | /e/ /eɪ/    | eI          |                                                                                                               |
| oy          | bOY                       | /ɔɪ/ /ɔe/   | (OI) (Oe)   |                                                                                                               |
| ow          | bOAt, fOUr, mOre          | /o/         | o           |                                                                                                               |

- SSE has no [ae] sound, it is merged into [aa]. If the speaker has a dialect that _does_ introduce it then feel free to add [ae] back.
- [ow] in SSE lost it's glide. So it is /o/ rather than /oʊ/.
- [ey] in SSE lost it's glide. So it is /e/ rather than /eɪ/.
- [aw] in SSE doesn't exist in many common words. Rather it is replaced with [uw].
- SSE lacks the foot-goose ([uw] [uh]) split. Use the [uh] sound for this.
- SSE has the horse–hoarse/North-force split.
  - Instead of "or" always using [ao r], as with most other dialects, it is sometimes [ow r]. 
  - "more" is [m ow r] and for is [f ow r]
- SSE has a _very_ strict cot–caught/lot-thought merger. So SSE only needs the [ao] sound, similar to AmE.

- SSE **does not** merge [er] (the fern–fir–fur merger), these situations will need to be handled with two phonemes.
  - Can identify lexically. Words with "i" often use [ih], "er" [eh r], "ur" [ah r]. (ex: "turn" is [t ah r n]
  - If lazy, you can still use [er] and bare the inaccuracies.
- Annoyingly, SSE does still have [er] in the form of a reduced schwa. Such as with "mother" and "runner".
  - Similar to BrE, there is no [axr] and it is handled by [er].

- [ih] may sound like an e-shaped schwa for some. Still use [ih].

- SSE often uses a "tap" consonant for rhotics. Given it's commonality one should still label these as [r] and not [dx]. 
- SSE is most often rhoticised. However some non-rhotic dialects do exist. Similar to BrE you would still label the missing [r] for context (heart: [h aa r t] not [h aa t]).
- Some SSE dialects include [x] for words like "loch" [l ao x].
- "-y" suffix in some dialects use [ih] instead of [iy] for some cases.
  - Similar to BrE we still label it as [iy] as it seems to be handled well enough contextually.
- SSE doesn't drop [h] in words like "where". Use [hw] ([hw eh r]).

# AmE Phoneme set
This set is the closest to standard Arpabet, _however_ it does have several extras that many find invaluable and have worked their way into common use for both English and Japanese datasets. For cleanliness most of those phonemes now reside in [#Utility-Phonemes](#utility-phonemes)
| **Phoneme** | **Common Name**  | **Word**                 | **IPA**     | **X-SAMPA** | **SynthV** | **Vocaloid (Broken)** |                                                                                                                                                                                                                 |
| ----------- | ---------------- | ------------------------ | ----------- | ----------- | ---------- | --------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| ah          | short u          | hUt, hUndred             | /ʌ/         | V           | ah         | V                     |                                                                                                                                                                                                                 |
| aa          | long a           | cAlm, cAr, plOt          | /ɑ/ /⁠ɒ/     | A           | aa         | Q                     | The merging of these two vowels has worked flawlessly in all public and private datasets thus far. There is no reason to change that. Most Americans cannot reliably identify/differentiate these vowels either.|
| ao          | long o           | cORe, All                | /ɔ/         | O           | ao         | O:                    |                                                                                                                                                                                                                 |
| ae          | short a          | bAth, bAt, nAsty         | /æ/         | ({)         | ae         | ({) (e@0)             |                                                                                                                                                                                                                 |
| ax          | short            | commA                    | /ə/         | @           | ax         | @                     |                                                                                                                                                                                                                 |
| iy          | long e           | bEAt                     | /i/         | i           | iy         | i:                    |                                                                                                                                                                                                                 |
| ih          | short i          | sIt, demOn, Example      | /ɪ/         | I           | ih         | I                     |                                                                                                                                                                                                                 |
| uh          | short oo         | bOOk                     | /ʊ/         | U           | uh         | U                     |                                                                                                                                                                                                                 |
| uw          | long oo/u        | bOOt                     | /u/         | u           | uw         | u:                    |                                                                                                                                                                                                                 |
| eh          | short e          | bEt                      | /ɛ/         | E           | eh         | E                     |                                                                                                                                                                                                                 |
| er          | long             | bIRd, sIR, colOR, mothER | /ɜ/ /⁠ɚ/ /⁠ɝ/ | (@\`) (3)   | er         | @r                    |                                                                                                                                                                                                                 |
| ay          | long i           | bIte                     | /aɪ/ /ʌɪ/   | aI          | ay         | aI                    |                                                                                                                                                                                                                 |
| aw          | long             | abOUt                    | /aʊ/ /ʌʊ/   | aU          | aw         | aU                    |                                                                                                                                                                                                                 |
| ey          | long             | bAIt                     | /eɪ/        | eI          | ey         | eI                    |                                                                                                                                                                                                                 |
| oy          | long             | bOY                      | /ɔɪ/        | OI          | oy         | OI                    |                                                                                                                                                                                                                 |
| ow          | long o           | bOAt                     | /əʊ/ /oʊ/   | (@U) (oU)   | ow         | @U                    |                                                                                                                                                                                                                 |

# CanE Phoneme Set
This set is incredibly close to AmE.
As Canadian English has many similarities to American English phonetically, most of the differences come down to which phones you use with which words.
| **Phoneme** | **Common Name**  | **Word**                 | **IPA**      | **SynthV** |                                                                                                                                                              |
| ----------- | ---------------- | ------------------------ | -----------  | ---------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| ah          | short u          | hUt, hUndred             | /ʌ/          | ah         |                                                                                                                                                              |
| aa          | long a           | cAlm, cAr, plOt          | /ɑ/ /⁠ɒ/      | aa         | CanE merges these even moreso than AmE.                                                                                                                      |
| ao          | long o           | cORe, All, sOrry, bOrrow | /ɔ/          | ao         | In some dialects "sorry" and other words use [aa] instead of [ao]. Similar to AmE. "All" is always [ao l] because AMBIbet standardizes to it (read GUIDE.md) |
| ae          | short a          | bAth, bAt, nAsty         | /æ/          | ae         | CanE tends to use /ɛ/ ([eh]) for words like "bag", HOWEVER because it is strictly contextual with the following consonant it should still be labeled as [ae] |
| ax          | short            | commA                    | /ə/          | ax         |                                                                                                                                                              |
| iy          | long e           | bEAt                     | /i/          | iy         |                                                                                                                                                              |
| ih          | short i          | sIt, demOn, Example      | /ɪ/          | ih         |                                                                                                                                                              |
| uh          | short oo         | bOOk                     | /ʊ/          | uh         |                                                                                                                                                              |
| uw          | long oo/u        | bOOt                     | /u/          | uw         | The placement of the /u/ in CanE is more frontal than in other dialects. The French has invaded.                                                             |
| eh          | short e          | bEt                      | /ɛ/          | eh         |                                                                                                                                                              |
| er          | long             | bIRd, sIR, colOR, mothER | /ɜ/ /⁠ɚ/ /⁠ɝ/  | er         |                                                                                                                                                              |
| ay          | long i           | bIte                     | /aɪ/ /⁠ʌɪ/    | ay         |                                                                                                                                                              |
| aw          | long             | abOUt                    | /aʊ⁠/ /⁠ʌʊ/    | aw         |                                                                                                                                                              |
| ey          | long             | bAIt                     | /eɪ⁠/ /⁠e/     | ey         | Many rural/western CanE dialects treat the dipthong /eɪ/ to a monophthong /e/. Still label as [ey].                                                          |
| oy          | long             | bOY                      | /ɔɪ/         | oy         |                                                                                                                                                              |
| ow          | long o           | bOAt                     | /o/ /⁠oʊ/     | ow         | Most rural/western CanE dialects treat the diphthong /oʊ/ as monophthong  /o/. Still label as [ow].                                                          |

 - While Canadian English is phonetically similar to American English (at least in quantity, exact phonemes tends to vary. This would need to be handled as part of the dictionary.
 - CanE doesn't have any additional vowels compared to AmE, however it has changes that can be confusing.
   - An easier example is "about". Depending on the dialect this can be [ax - b aw t], [ax - b ow t], or [ax - b uw t].
   - Because of the vowel positions change in CanE, many confuse some of these vowel sounds for unique/additional ones but they thankfully are not.
- Some CanE dialects pronounce "can", and similar, with a VERY diluted [ae] sound that sounds more like a raised [eh], but is still a unique sound. While we suggest continuing to label this as [ae], as it has worked in prior cases, you are welcome to experiment with labeling is [ee]\(?) and converting to [ae] to compare. We will look into this once more community testing (ideally over 1hr) is available.
  - If you always pronounce this more diluted sound (it is your norm) then always label with [ae]. This is intended for occasional words and/or contexts where the pronuncation changes.

# Consonants - General
| **phoneme** | **Example**                           | **IPA**      | **Description**                                                            |
| ----------- | ------------------------------------- | ------------ | -------------------------------------------------------------------------- |
| p           | PoP                                   | /p/ [pʰ]     |                                                                            |
| b           | BoB                                   |              |                                                                            |
| t           | TaT, Tree                             | /t/ [tʰ]     | Phoneme context handling of "tr".                                          |
| d           | DaD, Drink, batheD                    |              | Phoneme context handling or "dr". Also handles "tapping" at end of words   |
| k           | CaKE                                  | /k/ [kʰ]     |                                                                            |
| g           | GaG                                   |              |                                                                            |
| s           | SaS                                   |              |                                                                            |
| z           | ZooS                                  |              |                                                                            |
| ch          | CHurCH                                | /t͡ʃ/ [t͡ʃʰ]   |                                                                            |
| jh          | JuDGE                                 |              | Makes 'dg' sound for end of words. like [d][zh] or /dZ/ in xsampa.         |
| sh          | Ship, puSH                            |              |                                                                            |
| zh          | pleaSure                              |              | The 'judge' example is [j ah d zh], not [j ah zh]. To avoid any confusion. |
| f           | FlooF                                 |              |                                                                            |
| v           | Verge, nerVe                          |              |                                                                            |
| hh          | Herb(BrE), Happy(AmE)                 |              | syllable onset only. Use [exh] for end-of-note exhales.                    |
| th          | THin, myTH                            |              |                                                                            |
| dh          | THis, widTH                           |              |                                                                            |
| n           | NaNNy, paN                            |              |                                                                            |
| m           | MoM, MoMent                           |              |                                                                            |
| ng          | baNG, suNG                            |              |                                                                            |
| w           | Wisp                                  |              | syllable onset only.                                                       |
| y           | Yes                                   |              | syllable onset only.                                                       |
| r           | Road, caR                             | /ɹ/ /ɻ/ /⁠ʁ/  | rhotic shares same phoneme. It's fine. UK dropped r as well.               |
| l           | List, caLL                            |              | dark L shares same phoneme. It's fine.                                     |
| q           | boTTom(BrE), we-eat(AmE), batten(AmE) |              | glottal stop and vowel separator. NOT vocal fry.                           |
| dx          | shuTup(BrE), buTTer(AmE)              |              | tapped/flapped d/tt. Use in UK English is spotty.                          |
| rr          | peRRo                                 | /r/          | Trilled r (like in spanish)                                                |
| rx          | fuRet, bRechen                        | /ʁ/          | Fricative r (like in german or french)                                     |
| x           | loCH                                  |              | Voiceless velar fricative. Scottish/Welsh specific.                        |

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
| exh     | [exhale]         | end breaths, end of phrase exhale. devoiced. Label consonant coda. Can be between notes.               |
| axh     | [release]        | voiced variation of [exh]. voiced schwa exhale/release. Can be between notes.                          |
| vf      | [vocal fry]      | vocal fry. Can be used as a consonant OR on it's own note.                                             |

**THESE ARE NONSTANDARD and have almost no applicable use-case**. They are best avoided wherever possible. They are provided as they are custom additonal phonemes in Ambision's (Intunist's) NNSVS english support.
| phoneme | Example          | Description                                                                                                                           |
|---------|------------------| --------------------------------------------------------------------------------------------------------------------------------------|
| ct      | [closure-toggle] | override the default state of a consonant's closure. Completely defunct and useless.                                                  |
| cl      | [held stop]      | Held stop/plosive consonant. **For when the silence is held before a consonant release**. Similar to Japanese usage but not syllabic. |
| cr      | [vocal break]    | Optional label for when the singer experiences a vocal break/crack. Labeled as a consonant.                                           |

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
### Why are /æ/ and /ɑ/ merged? (BrE/AuE specific)
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
> Even if it did result in a _slightly_ lower loss in _a single_ use-case, that is not how loss metrics should be used as _any_ change can have small, random, effects on the loss value (in both directions).
> For speech synthesis tasks, human-perception is more important and this would be teeth pulling...
>
> Given that [t][r] and [d][r] is common in ALL existing English datasets and models with absolutely no issue, AND all existing software (open, commerical, or otherwise) also doing the same, it is STRONGLY RECOMMENDED to not break from this.
### How do I handle linking and intrusive r sounds?
>Sometimes a vowel becomes [er] or adds an [r] for vowel linkages. This is referred to as the "intrusive R". It is recommended to still label these as their original vowel and allow the model to learn the contextual change.
>"Idea of" may sound like "idear of" to split the vowels. But you would never label the [r].
>The same relatively applies to the "linking r" but in reverse. Where a word with an expected r drops the r when another consonant is already in place to split the vowels.
>For example, "four dogs" will not have an audible [r] and instead would have a softer schwa. However, "four otters" would have an audible linking r. In both cases you will want to include an [r] phoneme to provide context to the model.
### How do I handle r-colored vowels?
>There are no symbols for r-colored vowels because the [r] phoneme handles this. When between two vowels the [r] phoneme triggers a rhotic. When the next phoneme is a consonant it will drop the rhotic but make the prior vowel r-colored.
