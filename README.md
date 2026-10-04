# corpus-ecfr-title-14

Pinned text mirror of the **Code of Federal Regulations Title 14
(Aeronautics and Space — the Federal Aviation Regulations)**, built for the
[XERJ Corpus Hub](https://hub.xerj.org) as reference-retrieval material for
"what does the regulation actually say" questions — pilots' and mechanics'
daily lookup.

- Source (single bulk XML): https://www.govinfo.gov/bulkdata/ECFR/title-14/ECFR-title14.xml
- Downloaded: 2026-10-04 · amendment date in the source XML: **July 24, 2026** (see PROVENANCE.txt)
- Shape: one plain-text file per CFR section (§) or appendix, grouped per part
  (`parts/part-<N>/sec-<id>.txt`), each with a title/part/subpart breadcrumb —
  the same split as the live `ecfr-title-12/26/29` mirrors, produced by
  `tools/xerj-code/hub/nonit/split_ecfr.py` in the xerj repo.
- 226 parts · 6,363 section files (+28 section-less parts written whole).
- Pin: the commit of this repository IS the snapshot; re-snapshotting is a new
  commit, never a force-push.

## Licence

Works of the U.S. federal government, including CFR text published by GPO, are
in the **public domain** (17 U.S.C. § 105; government edicts are not
copyrightable). GPO imposes no restrictions on bulk-data redistribution.
No attribution is legally required; the source link above is kept for
provenance.

## Regeneration

Re-download the bulk XML and re-run the splitter; commit the result:

    curl -sL -o ECFR-title14.xml https://www.govinfo.gov/bulkdata/ECFR/title-14/ECFR-title14.xml
    python3 tools/xerj-code/hub/nonit/split_ecfr.py ECFR-title14.xml .
