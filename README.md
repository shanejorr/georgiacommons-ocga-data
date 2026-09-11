# Georgia Commons OCGA corpus

Machine-readable release bundles of the **Official Code of Georgia Annotated
(OCGA)** and the Georgia and United States constitutions, extracted from the
State of Georgia's own published PDF volumes.

This repository holds only the published data. The extractor and the
application that read it live in a separate repository.

## Not affiliated with the State of Georgia

Georgia Commons is an independent project. It is not operated, sponsored,
endorsed, or reviewed by the State of Georgia, the Georgia General Assembly,
the Georgia Code Revision Commission, the Office of Legislative Counsel, or any
Georgia court or agency.

**This is not legal advice, and it is not the state's official publication.**
For any purpose where the exact text matters, read the official volumes linked
below.

## What is in the bundle

Each release carries five files:

| File | What it is |
| --- | --- |
| `ocga-code.jsonl.gz` | Every general Code section, one JSON object per line. |
| `ocga-constitution-ga.jsonl.gz` | The Constitution of the State of Georgia. |
| `ocga-constitution-us.jsonl.gz` | The Constitution of the United States. |
| `manifest.json` | Provenance: source volumes, editions, page ranges, per-volume validation results, record counts. |
| `SHA256SUMS` | Checksums over the other four files. Verify before use. |

## Coverage

> The Official Code of Georgia Annotated, current through the 2025 Regular
> Session of the General Assembly.

| | Records |
| --- | --- |
| Code sections (`ocga`) | 29,682 across Titles 1 to 53 |
| Georgia constitution (`ga-constitution`) | 290 |
| United States constitution (`us-constitution`) | 52 |

Section status: 28,538 active, 538 reserved, 534 repealed, 70 redesignated,
1 superseded, 1 note only. Of the 52 United States constitution provisions,
51 are active and one (Amendment XVIII, Prohibition) is repealed, as the
volume's own editor's note says; its text is kept.

The current release is `ocga-2025-supplement-v2` (corpus version
`2025-supplement-35f294dc21c9`). Each release's notes list what changed
from the one before; a published release's assets are never rewritten.

### Qualifications on that coverage

State these with the coverage sentence; do not drop them.

1. The volumes reissued in 2025 (Titles 20 in part, 31, 35, 36, and 46) state
   their currency in their own words as the 2025 Session of the General
   Assembly.
2. Sections with delayed effective dates appear as versions dated 2026 and
   later, as printed.
3. Tables and forms inside statute text are shown as their lines, not as
   tables.
4. Eleven of the 100 source files carry variances printed in the state's own
   pages; they are recorded, not corrected.
5. The Title 9, Chapters 12 to 16 volume comes from the Internet Archive's copy
   of the set the Office of Legislative Counsel produced in 2024, not from the
   state's page.
6. Georgia's constitution is current through the same 2025 supplement; the
   United States constitution volume is the 2025 edition; the appendices of
   local constitutional amendments are not included.
7. Annotations (case notes) are not included for the Code sections. The two
   constitution volumes' notes, as extracted, include the case notes printed
   under each provision.

Every record carries its own provenance: volume id, edition year, source
filename, page range, and the currency statement printed on that volume's title
page or supplement cover.

## Official sources

The text was extracted from PDF volumes the state publishes itself:

- Georgia General Assembly, published Code volumes and supplements:
  <https://www.legis.ga.gov/joint-office/code-of-georgia>
- The state's free public lookup portal:
  <https://law.georgia.gov/law/official-code-georgia-annotated>

One exception is recorded in the manifest: the Volume 7A bound volume (Title 9,
Chapters 12 to 16, 2015 edition) is absent from the state's page and comes from
the Internet Archive's copy of the set the Office of Legislative Counsel
produced to Public.Resource.Org in 2024, with its checksum pinned.

## Verify before you use it

    curl -LO https://github.com/shanejorr/georgiacommons-ocga-data/releases/download/<tag>/SHA256SUMS
    curl -LO https://github.com/shanejorr/georgiacommons-ocga-data/releases/download/<tag>/ocga-code.jsonl.gz
    sha256sum -c SHA256SUMS

## License: CC0 1.0 Universal

To the extent the extraction and arrangement of these files could carry any
rights, they are released under [CC0 1.0](LICENSE): no rights reserved.

The underlying material is uncopyrightable public law. In *Georgia v.
Public.Resource.Org, Inc.*, 590 U.S. 255 (2020), the Supreme Court held that the
annotations in the Official Code of Georgia Annotated are not copyrightable
under the government edicts doctrine. The extraction is mechanical and adds no
authorship.
