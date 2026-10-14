## What this changes

<!-- One or two sentences. Which words, types or areas. -->

## Issue

<!-- "Closes #123". For a tracking issue use "Refs #123". A typo or a generated file can take the `no-issue` label from a maintainer. -->

Closes #

## Checklist

- [ ] Glossary entries are of the form `{ "phrase": "<ISO English>", "to": "<this language>" }`, and a longer phrase is not shadowed by a shorter one that was already there.
- [ ] ISO type and element names, acronyms (IBAN, BIC, ...) and `|` line breaks are unchanged in `types/`.
- [ ] A term is the same in names and in definitions (the glossary is the source).
- [ ] The text builds: `node ../iso-20022-text/build/build.mjs --spoke . --out <a folder outside this repository>` (there is no automatic check yet).
- [ ] The variety this is for (general, or one region) is stated above.
- [ ] I read the changed text in this language, or it is marked as a machine draft in the description.
