# spec.md — `leaders.yml`

Single source of truth for the Kyrgyz health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Kyrgyz Ministry of Health (MoH) and adjacent bodies.

Kyrgyzstan operates a post-Soviet, Semashko-legacy mixed system under President Sadyr Japarov; reform programme "Den Sooluk" and the State-Guaranteed Benefits Package (SGBP) are central financing instruments. Member of WHO Europe, EAEU, CIS, SCO, OTS (Organisation of Turkic States).

## 2. Scope

In scope: President; Chair of the Cabinet of Ministers (Prime Minister); Minister of Health; Director-General National Hospital; Director Mandatory Health Insurance Fund (MHIF); Jogorku Kenesh (Parliament) Committee on Social Policy.

Out of scope: oblast health department heads.

## 3. Structure

Standard 2/6/10/14 indentation. Top-level key: `Kyrgyz health stakeholders:`. Ordering: Presidency → Cabinet → MoH → MHIF → Jogorku Kenesh.

## 4. Field definitions

Party affiliation: contemporary Kyrgyz politics is fluid; presidential alignment (`Japarov-aligned`) and pro-presidential bloc references. Titles in English.

## 5. Provenance and dating

Anchor to year, month or date. Erkin Checheybaev has served as Minister of Health in the Japarov-Zhaparov government; verify currency against the Cabinet of Ministers and Kabar (Kyrgyz News Agency).

## 6. Update workflow

Verify against med.kg, gov.kg, kenesh.kg, kabar.kg, 24.kg, Azattyk (RFE/RL Kyrgyz Service).

## 7. Invariants

Standard.

## 8. Anti-patterns

- Conflating Kyrgyzstan with Kazakhstan — sovereign states with distinct architecture, financing model and SGBP design despite shared Soviet inheritance.
- Importing Russian framings — Kyrgyzstan is a multi-vector state in the EAEU/SCO/CSTO orbit but with its own policy priorities.

## 9. Acronym glossary

- **EAEU** — Eurasian Economic Union.
- **MHIF** — Mandatory Health Insurance Fund.
- **MoH** — Ministry of Health.
- **OTS** — Organisation of Turkic States.
- **SGBP** — State-Guaranteed Benefits Package.

## 10. Worked example

```yaml
      - Erkin Checheybaev (Japarov-aligned):
          - Title: Minister of Health
          - Stakeholder engagement notes:
              - "Minister of Health in the Japarov government; verify currency against Cabinet of Ministers and Kabar."
              - "Owns MoH policy and budget, National Hospital (Bishkek), oblast and rayon hospital network across the seven oblasts (Batken, Chuy, Issyk-Kul, Jalal-Abad, Naryn, Osh, Talas) plus Bishkek and Osh cities, MHIF, SGBP, Den Sooluk reform programme legacy, and WHO Europe, EAEU and SCO diplomacy."
              - "Hook: NCDs, MCH, MHIF strengthening, primary-care reform legacy, mental health, TB and HIV, and OTS-Turkic cooperation land."
          - Tone advice:
              - "Open with NCDs, MCH, MHIF-SGBP, PHC reform and TB-HIV — durable MoH lines."
              - "Do not conflate with Kazakhstan or import Russian framings."
```

## 11. Out-of-band notes

For roles unfilled or interim.

## 12. Open questions

- Director-General National Hospital and Director MHIF with currency verified.
- Jogorku Kenesh Committee on Social Policy Chair with currency verified.
