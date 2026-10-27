# Legal notice

**This is not legal advice.** It explains what this repository contains, what
it deliberately leaves out, and why. If you plan to reuse or redistribute
anything here, get advice from a lawyer in your own jurisdiction.

## Not affiliated

This is an independent university study project. It is **not affiliated with,
endorsed by, or sponsored by** Anysphere, Inc. (Cursor), xAI, SpaceX, or any of
their affiliates. "Grok", "Grok Bot", "Cursor" and related names and logos are
trademarks of their respective owners. They are used here only to identify the
software being studied (nominative use). No logos or brand assets are included.

## What this repository contains

Only original work written for this project:

- `scripts/recover-installed-app.sh`: a script that unpacks and analyses a copy
  of the application **that the person running it has lawfully installed on
  their own Mac**;
- `scripts/ghidra/ExportDecompiled.java`: a Ghidra headless script;
- `docs/`: our own descriptions of how the software is put together and what
  changed between versions, in our own words.

The docs mention short identifiers (package, function, RPC and event names) and
public library names. They are cited only to describe facts about the software.
They are not the software's code.

## What this repository does NOT contain

None of the following is committed, and it must never be committed or shared.
`.gitignore` blocks it:

- the Grok Bot application, installers (`.dmg`/`.exe`) or any part of them;
- extracted, beautified or otherwise reproduced upstream JavaScript, CSS, HTML,
  assets or native binaries;
- Ghidra projects, decompiled C or any other output of `recovered/`;
- source code from other people's unlicensed reconstructions.

Anyone running the script creates that material **locally, for their own
private study**. It is upstream copyrighted material and stays theirs to keep
private.

## Why studying it locally is permitted, and why the output stays private

- The Grok Bot Terms (cursor.com/terms/grok-bot) supplement the Cursor Terms of
  Service. §1.5 of those terms forbids reverse engineering and decompiling
  "except and solely to the extent such a restriction is impermissible under
  applicable law".
- **EU:** Directive 2009/24/EC on the legal protection of computer programs
  allows a lawful user to observe, study and test how a program works (Art.
  5(3)). It allows decompilation for interoperability under strict conditions
  (Art. 6). Contract terms that override these rights are void (Art. 8). Spain
  implements this in the Ley de Propiedad Intelectual, art. 100. Art. 6(2)
  forbids handing the information obtained to others, or using it to build a
  substantially similar program. **That is why decompiled output is never
  published here.**
- **US:** 17 U.S.C. § 1201(f) and case law such as *Sega v. Accolade* (1992)
  recognise reverse engineering for interoperability. The terms' Texas
  governing-law clause may still apply to the contract itself.
- No technical protection measure is circumvented. The app's `app.asar` is an
  unencrypted archive format, and Ghidra only reads the binaries.

## Your responsibility

If you run the tooling, you are responsible for complying with the terms you
accepted and with the law where you live. Do not use it to bypass security or
anti-abuse measures, access accounts or services without authorisation, or
redistribute the vendor's software.

## Takedown / contact

If you are a rights holder and believe something here infringes your rights,
please open an issue on this repository. We will review it promptly and remove
material where appropriate.
