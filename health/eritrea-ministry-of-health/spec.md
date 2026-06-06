# spec.md — `leaders.yml`

Single source of truth for the Eritrean health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Eritrean Ministry of Health (MoH) and adjacent bodies.

Eritrea operates a single-party (PFDJ) state under President Isaias Afwerki and a centrally planned public health system. The country is partially closed to external NGOs, has been under prolonged sanctions episodes, and engages selectively with WHO Africa, IGAD and the African Union.

## 2. Scope

In scope: President; Minister of Health; Director-General of MoH operations; Director-General of MoH regulatory functions; Head of Eritrean Pharmaceutical Corporation (EPHARMECOR).

Out of scope: zoba (regional) health office heads.

## 3. Structure

Standard 2/6/10/14 indentation. Top-level key: `Eritrean health stakeholders:`. Ordering: Presidency → MoH → EPHARMECOR.

## 4. Field definitions

Single-party state: party affiliation is uniformly `PFDJ` (People's Front for Democracy and Justice) for officials, omitted in practice. Titles in English.

## 5. Provenance and dating

Anchor to year, month or date. Amina Nurhussien has long served as Minister of Health in the Afwerki Cabinet; verify currency against MoH and Ministry of Information communications.

## 6. Update workflow

Verify against shabait.com (Ministry of Information), Eritrean MoH announcements, WHO Eritrea country office briefings, IGAD bulletins.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Assuming open NGO access — Eritrea is selective on international NGO operations; framings that assume open access are inaccurate.
- Conflating Eritrea with Ethiopia — the two are distinct sovereign states with separate health architectures and a contested border history.

## 9. Acronym glossary

- **EPHARMECOR** — Eritrean Pharmaceutical and Medical Supplies Corporation.
- **IGAD** — Intergovernmental Authority on Development.
- **MoH** — Ministry of Health.
- **PFDJ** — People's Front for Democracy and Justice.

## 10. Worked example

```yaml
      - Amina Nurhussien:
          - Title: Minister of Health
          - Stakeholder engagement notes:
              - "Long-serving Minister of Health in the President Isaias Afwerki Cabinet; verify currency against shabait.com Ministry of Information communications and WHO Eritrea country office briefings."
              - "Owns MoH policy and budget, Orotta National Referral Hospital, Halibet Hospital, zoba referral hospitals, primary-care clinic network across the six zobas, EPHARMECOR procurement, malaria and TB programmes, and IGAD and WHO Africa diplomacy."
              - "Hook: maternal and child health, malaria, TB, HIV continuity, NCDs, and IGAD regional cooperation land; large reform framings will be filtered through a sovereignty-and-self-reliance lens."
          - Tone advice:
              - "Open with maternal and child health, malaria, TB, NCDs and IGAD cooperation — these are durable MoH priorities."
              - "Do not assume open NGO access or import Ethiopian framings — Eritrea is selective on international NGO operations and distinct from Ethiopia."
```

## 11. Out-of-band notes

For roles unfilled or interim.

## 12. Open questions

- Named Director-General(s) of MoH operations and regulation with currency verified.
- Head of EPHARMECOR with currency verified.
