# ISO 20022 text: pt

The pt text of the ISO 20022 message explorer and library. This repository holds the **translation** of the ISO English text. Anything not written here shows the ISO English text. Entries may be machine drafts that no person has reviewed.

## What to edit

The English text this repository translates is in the [hub](https://github.com/Beneficial-Strategies/iso-20022-text), exactly as ISO has it. This repository
holds only what differs from it: two things.

* **`glossary.json`** says how the **names** are translated: the names of types, elements and codes, which are also the values of a dropdown. Each entry is
  a phrase of the hub's names and its Portuguese (`Post Code` -> `Código postal`). The build applies the glossary to every name, longest phrase first, in one
  pass, so one entry fixes a name everywhere. Numbers in a name are left as they are. The first step of a language is to make every word of the names
  an entry: `node build/glossary.mjs missing --spoke <this repository>` in the hub lists the words that are not covered yet.
* **`types/<first letter>/<Type>.json`** holds the **definitions**, and any name that the glossary cannot express (for example one that needs a different word
  order), as explicit entries: only what is translated, under `isoElements`, `isoCodes` and `isoRules`. For example
  `{ "isoType": "AdviceType1Code", "isoCodes": { "ADWD": { "name": "Aviso com detalhes", "definition": "..." } } }`. An entry here wins over the glossary.
  Keep `isoType`, the keys, element names, acronyms (IBAN, BIC, ...) and `|` (a line break) as they are in the hub. Translate with the glossary in hand,
  so that a word is the same in a name and in a definition.

Anything not written here shows the hub's English. A `format` (the text that says what a value must look like) is not translated yet.
Who changed what and when is the repository's history.

## Building what the host serves

```sh
node ../iso-20022-text/build/build.mjs --spoke . --out /path/to/output
```

The output is the complete text of every type, in the shape of the [convention](https://github.com/Beneficial-Strategies/iso-20022-text/blob/main/SPECIFICATION.md).
It is never edited by hand and not committed. There is no automatic check on pull requests yet.

## Status, license and warranty

This text is provided **free of charge and as is**, under the MIT license (see `LICENSE`), without warranty of any kind. We make our best-faith
effort toward an accurate text, but it is not verified by a professional translator, and entries may be machine drafts that no person has reviewed.
**Do not rely on it for legal, financial or compliance decisions**: the authoritative text is ISO's English.

**The controls here are lax at present**: there is no formal review process, release gating or ownership policy beyond what you can see in this
repository. We intend to improve them over time (named maintainers per area, required reviews, release checks) should the libraries gain adoption
and sponsorship. Taking over the care of a language, or of an area of one, is welcome.

The English text this repository translates or adapts is ISO's, and ISO's own terms apply to it. The license above covers what is written
in this repository, not ISO's text. This is not legal advice.