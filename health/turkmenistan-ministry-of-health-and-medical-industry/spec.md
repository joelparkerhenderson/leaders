# spec.md — `leaders.yml`

Single source of truth for the Turkmen health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Turkmen Ministry of Health and Medical Industry (MoHMI) and adjacent bodies.

Turkmenistan is a closed presidential republic under Serdar Berdimuhamedow (President, since March 2022) with his father Gurbanguly Berdimuhamedow (Chairman of the Halk Maslahaty / People's Council). The DPT (Democratic Party of Turkmenistan) dominates a tightly controlled political space. The country is permanently neutral by UN-recognised status, has limited international media access, and engages externally primarily via WHO Europe and CIS frameworks.

## 2. Scope

In scope: President; Chairman of the People's Council; Minister of Health and Medical Industry; Director Central Hospital; Mejlis Committee on Science, Education, Culture and Youth Policy.

Out of scope: provincial (welayat) health office heads.

## 3. Structure

Standard 2/6/10/14 indentation. Top-level key: `Turkmen health stakeholders:`. Ordering: Presidency → MoHMI → Mejlis.

## 4. Field definitions

Affiliation: `DPT` (Democratic Party of Turkmenistan, ruling). Titles in English.

## 5. Provenance and dating

Anchor to year, month or date. The Minister of Health and Medical Industry under the Serdar Berdimuhamedow government is to be verified against TDH (Turkmen State News Agency) and Watan news programme; external visibility is limited.

## 6. Update workflow

Verify against tdh.gov.tm, mfa.gov.tm, mejlis.gov.tm, Watan, Chronicles of Turkmenistan, Turkmen.news, RFE/RL Azatlyk Radiosy.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Assuming open data access — Turkmenistan operates a highly restricted information environment; published epidemiological data has historically been incomplete or contested (notably during Covid-19 the government did not report cases).
- Importing standard CIS-engagement framings — Turkmenistan has UN-recognised permanent neutrality status (1995) and selective external engagement; standard CIS framings will be partially filtered.

## 9. Acronym glossary

- **DPT** — Democratic Party of Turkmenistan.
- **MoHMI** — Ministry of Health and Medical Industry.
- **TDH** — Turkmen State News Agency.

## 10. Worked example

```yaml
      - Notes on Minister of Health and Medical Industry of Turkmenistan:
          - Status: Verify against TDH and Watan; external visibility is limited.
          - Implication: Engagement requires (i) identification via official Ashgabat channels, (ii) recognition of permanent-neutrality framing, (iii) selective external engagement via WHO Europe.
          - Hook: NCDs, MCH, TB, vector-borne disease control, and Caspian regional cooperation land.
          - Tone: Open with NCDs, MCH and WHO Europe cooperation; do not assume CIS-default engagement.
```

## 11. Out-of-band notes

For substantive identities of office-holders where external visibility is limited.

## 12. Open questions

- Minister of Health and Medical Industry substantive identity with currency verified.
- Director Central Hospital; Mejlis Committee Chair.
