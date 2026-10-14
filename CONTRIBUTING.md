# Contributing to the Portuguese text

This repository holds the **Portuguese text** of the ISO 20022 message explorer and library: only what differs from the ISO English. Read the [README](README.md) for what is in it and how it is built. The convention is in the [hub's SPECIFICATION.md](https://github.com/Beneficial-Strategies/iso-20022-text/blob/main/SPECIFICATION.md).

## The quickest ways to help

| You want to | Open |
|---|---|
| Say that a word or phrase should be translated another way | **Glossary entry**. "When ISO 20022 says `Transaction` it should say `Transação`." |
| Fix a definition that is wrong, awkward or still in English | **Wrong, unclear or missing translation** |
| Tell us a term is used only in one country or region | Pick the **Language variety** in either form |
| Offer to review or take over this language or a business area | **Offer to review or maintain** |
| Ask for a text of its own for one variety | **Propose a regional text** |
| Report a host, build or site problem | **Problem with the host, the build or the site** |

If the English itself looks wrong, that is ISO's text in the [hub](https://github.com/Beneficial-Strategies/iso-20022-text/issues/new/choose).

## Varieties (regions)

Portuguese is spoken in many countries, and financial vocabulary differs between them. This repository holds one text of Portuguese. Where a term is **general**, one glossary entry serves everyone. Where a term belongs to **one region**, we record it with its variety rather than lose it or force it on everyone.

Every glossary and translation form asks which **variety** a term belongs to. An answer such as "Brazil (pt-BR)" becomes the label `variety:pt-BR` on its own, so [the issues of one variety](https://github.com/Beneficial-Strategies/iso-20022-text-pt/issues?q=label%3Avariety%3Apt-BR) can be counted and read together. A variety that **keeps coming up** and has **at least one person willing to review it** is a candidate for a text of its own, one level out: a new repository such as `iso-20022-text-pt-BR` that holds only what differs from this one (that is how `en-US` relates to `en`). When that looks near, someone opens **Propose a regional text**.

## Pull requests

* Edit `glossary.json` for a word, `types/<first letter>/<Type>.json` for a definition or an exception. See the README for the shapes.
* Every pull request says which issue it settles (`Closes #123`, or `Refs #123` for a tracking issue). A check fails without one; a maintainer can add the `no-issue` label for a typo.
* Keep ISO's type and element names, acronyms and `|` line breaks as they are.
* Build it before you ask for review: `node ../iso-20022-text/build/build.mjs --spoke . --out <a folder outside this repository>`.
* Say whether you read the text as a speaker of the variety, or whether it is a machine draft. Both are welcome; we only need to know which.

## Labels

`glossary` and `definition` say what the issue is about. `variety:<tag>` is added for you. `needs-triage` means nobody has looked yet. `machine-draft` and `needs-native-review` mark text that a person has not read. `regional-variant` marks proposals for a variety's own repository, `volunteer` offers of help, `maintainer-wanted` the places where help would make the most difference. `good first issue` and `help wanted` are the usual.

## Licence

By contributing you agree that your contribution is under this repository's MIT licence. ISO's own text, which this text translates, stays ISO's.
