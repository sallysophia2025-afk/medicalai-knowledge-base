---

source_id: "SRC-acad3171b5691e32371c"
title: "JPAIS-MED-REF Verification Matrix"
status: "IN_PROGRESS"
last_reviewed: "2026-09-24"
---

# JPAIS-MED-REF Verification Matrix

## 1. Purpose

This verification matrix records the independent verification status of claims extracted from:

`SRC-acad3171b5691e32371c`

The matrix distinguishes source-reported claims from independently verified claims.

---

## 2. Verification Status

| Status              | Meaning                                                                                              |
| ------------------- | ---------------------------------------------------------------------------------------------------- |
| VERIFIED            | Supported by an authoritative external source                                                        |
| PARTIALLY_VERIFIED  | Core reference is confirmed, but the source claim contains additional details requiring verification |
| NOT_VERIFIED        | No authoritative confirmation has yet been established                                               |
| CORRECTION_REQUIRED | External evidence contradicts or materially differs from the source claim                            |
| PROPOSED            | Framework proposal rather than an existing legal or technical requirement                            |
| UNKNOWN             | Not established in the primary source                                                                |

---

## 3. Indonesian Regulatory References

| Claim ID     | Subject                                                                                                                            | Verification Status | Evidence                                                                | Action                                        |
| ------------ | ---------------------------------------------------------------------------------------------------------------------------------- | ------------------- | ----------------------------------------------------------------------- | --------------------------------------------- |
| CLM-ACAD-030 | Permenkes No. 24 Tahun 2022 is part of the regulatory baseline                                                                     | VERIFIED            | JDIH BPK / Permenkes 24/2022                                            | Retain with citation                          |
| CLM-ACAD-031 | KMK No. HK.01.07/Menkes/1423/2022 is a relevant RME variable and metadata reference                                                | VERIFIED            | JDIH Kementerian Kesehatan                                              | Retain with citation                          |
| CLM-ACAD-032 | UU No. 27 Tahun 2022 is the Indonesian Personal Data Protection Law                                                                | VERIFIED            | Authoritative Indonesian legal source required for article-level claims | Verify specific provisions before publication |
| CLM-ACAD-033 | SE Menkominfo No. 9 Tahun 2023 is an AI ethics reference                                                                           | VERIFIED            | JDIH Kemkomdigi                                                         | Retain with citation                          |
| CLM-ACAD-034 | UU No. 17 Tahun 2023 is the current Health Law reference                                                                           | VERIFIED            | JDIH BPK                                                                | Retain with citation                          |
| CLM-ACAD-035 | Specific article-level claims concerning RME infrastructure, ownership, signatures, retention, encryption, and breach notification | PARTIALLY_VERIFIED  | Individual statutory articles must be checked separately                | Do not publish as one bundled claim           |

---

## 4. Permenkes No. 24 Tahun 2022 — Article-Level Verification

| Claim                                                        | Status                        | Finding                                                               |
| ------------------------------------------------------------ | ----------------------------- | --------------------------------------------------------------------- |
| Article 25 concerns ownership of the medical-record document | VERIFIED                      | Document belongs to the healthcare facility                           |
| Article 26 concerns ownership of medical-record contents     | VERIFIED                      | Content belongs to the patient                                        |
| Article 31 concerns electronic signatures                    | VERIFIED                      | Electronic signatures may be used for verification/authentication     |
| Article 39 establishes minimum electronic-record retention   | CORRECTION_REQUIRED           | Minimum period is 25 years from the patient's last visit, not 5 years |
| Article 29 concerns security principles                      | REQUIRES ARTICLE-LEVEL REVIEW | Verify exact wording before publication                               |

### Critical Correction

The supplied JPAIS-MED-REF source states a:

`5-year retention floor`

for Article 39.

This should be corrected in downstream knowledge representations to:

`25-year minimum retention period from the patient's last visit`

unless a later applicable regulation changes the rule.

The authoritative text of Article 39 states the 25-year minimum.

---

## 5. SE Menkominfo No. 9 Tahun 2023

| Claim                                                                                            | Status        | Finding                                                          |
| ------------------------------------------------------------------------------------------------ | ------------- | ---------------------------------------------------------------- |
| SE No. 9/2023 concerns AI ethics                                                                 | VERIFIED      | Official JDIH document confirms title and scope                  |
| AI should consider humanity, safety, transparency, accountability and personal-data protection   | VERIFIED      | These principles appear in the guidance                          |
| AI should not be organized as a policy determinant and/or decision-maker concerning humanity     | VERIFIED      | Appears in the responsibility section                            |
| SE No. 9/2023 is a statute equivalent to an Act                                                  | NOT_SUPPORTED | Treat as a ministerial circular / ethical guidance instrument    |
| SE No. 9/2023 independently creates a medical-AI prohibition applicable to every clinical system | NOT_VERIFIED  | Do not make this broader claim without additional legal analysis |

---

## 6. KMK No. HK.01.07/Menkes/1423/2022

| Claim                                                                  | Status                        | Finding                                               |
| ---------------------------------------------------------------------- | ----------------------------- | ----------------------------------------------------- |
| The decree exists                                                      | VERIFIED                      | Confirmed by JDIH Kementerian Kesehatan               |
| It concerns variables and metadata for electronic medical records      | VERIFIED                      | Confirmed by official title                           |
| It establishes every specific coding relationship listed in the source | REQUIRES ARTICLE/ANNEX REVIEW | Verify against the complete decree before publication |

---

## 7. UU No. 17 Tahun 2023

| Claim                                                                           | Status        | Finding                                      |
| ------------------------------------------------------------------------------- | ------------- | -------------------------------------------- |
| UU 17/2023 concerns Health                                                      | VERIFIED      | Confirmed by JDIH BPK                        |
| UU 17/2023 includes health technology and health information systems            | VERIFIED      | Confirmed in the regulation's subject matter |
| All specific clinical-liability claims attributed to particular articles        | NOT_VERIFIED  | Require article-level verification           |
| UU 17/2023 should be treated as the sole legal basis for clinical AI governance | NOT_SUPPORTED | Additional regulatory sources are required   |

---

## 8. Technical Thresholds

The following claims originate from the JPAIS-MED-REF source but have not yet been independently validated.

| Claim ID     | Subject                             | Status       |
| ------------ | ----------------------------------- | ------------ |
| CLM-ACAD-025 | 99th-percentile OOD threshold       | NOT_VERIFIED |
| CLM-ACAD-026 | PSI threshold for model fallback    | NOT_VERIFIED |
| CLM-ACAD-027 | Clinician Override Rate threshold   | NOT_VERIFIED |
| CLM-ACAD-028 | 3–5 second cognitive-friction delay | NOT_VERIFIED |
| CLM-ACAD-029 | 60–90 day shadow-mode period        | NOT_VERIFIED |

These should remain source-attributed recommendations rather than universal clinical standards.

---

## 9. Proposed Governance Mechanisms

The following should remain `PROPOSED`:

* JPAIS-MED-REF six-dimensional governance sequence
* three autonomy tiers
* structured clinical overrides
* cognitive friction controls
* HMAC-SHA256 audit-chain architecture
* hardware-backed key storage
* PSI-based circuit breakers
* Clinician Override Rate monitoring
* deterministic HL7 CQL fallback
* prospective shadow-mode deployment

These are framework mechanisms and are not automatically current Indonesian legal requirements.

---

## 10. Explicitly Unknown Scope

The following remain UNKNOWN unless independently researched:

* UU ITE provisions requested for digital-forensics analysis
* KUHP Nasional
* KUHAP
* NIST SP 800-86
* NIST SP 800-61 Rev. 3
* SWGDE
* ISO/IEC 27037
* specific GIS / AccessMod 5 coordinates

---

## 11. Publication Decision Rules

A claim may be promoted to `VERIFIED` only when:

1. The authoritative source is identified.
2. The relevant provision or technical specification is located.
3. The source claim accurately matches the external source.
4. Any interpretation is clearly separated from the underlying text.
5. Current status or amendments have been checked.

If an external source contradicts the source record, the contradiction must be preserved in the provenance history rather than silently overwritten.

---

## 12. Current Verification Summary

Current verified baseline:

* Permenkes 24/2022 — reference confirmed
* Article 25 — confirmed
* Article 26 — confirmed
* Article 31 — confirmed
* Article 39 — confirmed, but source's 5-year statement requires correction to 25 years
* KMK HK.01.07/Menkes/1423/2022 — reference confirmed
* SE Menkominfo 9/2023 — reference and AI responsibility language confirmed
* UU 17/2023 — reference confirmed

Remaining verification:

* UU PDP article-level claims
* specific legal interpretations
* technical thresholds
* international standards
* clinical liability implications
* forensic standards
