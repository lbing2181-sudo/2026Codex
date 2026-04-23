# Evidence Chain

## Objective

Ensure every meaningful asset in `Sable Archive` can be proven, reconstructed, and defended later by another AI or a human operator.

## Rule

No important release should exist without evidence.

## Minimum Evidence Package

For each major published work, store:

1. asset ID
2. prompt text
3. prompt version number
4. reference assets used
5. draft output set
6. final selected file
7. any edit notes
8. publication date
9. publication platform
10. publication URL
11. file hash of the master file
12. file hash of the release file

## Folder Discipline

The evidence chain should eventually map to a predictable local structure such as:

- `assets/master/`
- `assets/release/`
- `assets/proof/`
- `posts/`
- `characters/`

## Hash Rule

Generate hashes for:

- the master file
- the public release file
- key dossier files when they are finalized

This helps prove that the protected file existed in a given form at a given time.

## Release Rule

Public files and master files should be treated as different layers.

- master: untouched source of truth
- release: published version
- proof: supporting evidence package

## Documentation Rule

If a post becomes important, a summary of its identity should be written back into repository memory rather than left only on the platform.

## Handoff Rule

Future AIs must be able to answer:

- what was made
- when it was made
- how it was made
- what version was released
- where it was published

If they cannot answer these questions, the evidence chain is incomplete.
