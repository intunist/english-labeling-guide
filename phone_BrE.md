Phonemes for British English

BROKEN AS OF 1/11/23. [ae]  MERGE BREAKS WORDS LIKE "father" WHICH ALSO USE THE /ɑ/ SOUND.
<br>FIXING.
<br> 2/11/23 investigating the feasability of merging the two phonetics into one symbol.

Note that many BrE dialects use a reduced phoneme set.
<br>The phoneme set provided is the full set to support southern dialects and Australian engish.
<br>If you have a reduced-set dialect you can choose to either
1. label with the full set, as if the speaker did not have fewer phonemes (recommended for dict/G2P compatibility).
2. label with a reduced set, choosing the closest provided phoneme. (ex: some northern speakers pronounce "hut" as [hh uh t] 

### Vowels - monophthongs:
| Phoneme        | Word               | IPA       | X-SAMPA   | SynthV | Vocaloid (Modified Sampa) |
| -------------- | ------------------ | --------- | --------- | ------ | ------------------------- |
| ah             | hUt                | /ʌ/       | V         | ah     | V                         |
| aa             | ~~fAther~~, plOt   | /ɒ/       | Q         | aa     | Q                         |
| ao             | nAUght, cORe       | /ɔ/       | O         | ao     | O:                        |
| ae<sup>1</sup> | bAth, bAt          | /æ/ /ɑ/   | ({) (A)   | ae     | ({) (e@0)                 |
| ax             | commA              | ə         | @         | ax     | @                         |
| iy             | bEAt               | i         | i         | iy     | i:                        |
| ih             | sIt                | ɪ         | I         | ih     | I                         |
| uh             | bOOk               | ʊ         | U         | uh     | U                         |
| uw             | bOOt               | u         | u         | uw     | u:                        |
| eh             | bEt                | ɛ         | E         | eh     | E                         |
| er<sup>2</sup> | bIRd, pURse, colOR | /ɚ/ /ɜ/   | (@\`) (3) | er     | @r                        |

<sup>1</sup> For BrE and AuE /æ/ and /ɑ/ are merged into the [ae] phoneme.
> While incredibly weird looking, it works correctly and is fine.
> <br>The only minor quirk is that the model may swap northern and southern dialects with _tiny_ amounts of data.
> <br>Note that most singers standardize to the southern dialect. Regardless the model will learn the original dialect.
> <br>"I personally hate this but it works" - Heteric

<sup>2</sup> Some phonetic systems will also include [axr] as a label. This is entirely unnecessary and the [er] phoneme works flawlessly.

### Vowels - diphthongs:
| Phoneme        | Word               | IPA       | X-SAMPA   | SynthV | Vocaloid (Modified Sampa) |
| -------------- | ------------------ | --------- | --------- | ------ | ------------------------- |
| ay             | bIte               | /aɪ/      | aI        | ay     | aI                        |
| aw             | abOUt              | /aʊ/      | aU        | aw     | aU                        |
| ey             | bAIt               | /eɪ/      | eI        | ey     | eI                        |
| oy             | bOY                | /ɔɪ/      | OI        | oy     | OI                        |
| ow             | bOAt               | /əʊ/ /oʊ/ | (@U) (oU) | ow     | @U                        |

### Consonants:
Voice and unvoiced equivalents are paired (ex: k/g, t/d)
| Phoneme        | Word               | IPA       | X-SAMPA   | SynthV | Vocaloid (Modified Sampa) |
| -------------- | ------------------ | --------- | --------- | ------ | ------------------------- |
|                |                    |           |           |        |                           |
|                |                    |           |           |        |                           |
| [t] [r]        |                    |           |           | tr     | dh r                      |
| [d] [r]        |                    |           |           | dr     |                           |

### Syllabic vowel-like-consonants:
Acknowledged but completely optional phonetics for particular cases.
<br>Can be handled with the phonetics above without issue.
<br>Not supported by any dicitonary or G2P
| Phoneme        | Word               | IPA       | X-SAMPA   | SynthV | Vocaloid (Modified Sampa) |
| -------------- | ------------------ | --------- | --------- | ------ | ------------------------- |
| el             |                    |           |           |        |                           |
| em             |                    |           |           |        |                           |
| en             |                    |           |           |        |                           |

### Utility phonemes:
OPTIONAL phonemes that aren't strictly vocal sounds but are useful in one way of another
| phoneme | Example          | Description                                                                                                                          |
|---------|------------------| -------------------------------------------------------------------------------------------------------------------------------------|
| pau     | silence          | During unsung/silent periods.                                                                                                        |
| br      | [breath]         |                                                                                                                                      |
| exh     | [exhale]         | end breaths, end of phrase exhale. devoiced. Label as consonant coda.                                                                |
| axh     | [release]        | voiced variation of [exh]. voiced schwa exhale/release. Label as consonant coda.                                                     |
| cl      | [held stop]      | __**Almost completely useless.**__ Held stop/plosive consonant. For when held and unreleased. Handled contextually and best ignored. |
| vf      | [vocal fry]      | vocal fry. Can be used as a consonant OR on it's own note.                                                                           |