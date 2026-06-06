# spec.md — `leaders.yml`

Single source of truth for the Cambodian health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around Cambodia's Ministry of Health, Drug Department, Calmette Hospital, Khmer-Soviet Friendship Hospital, Cambodia-China Friendship Hospitals, and adjacent bodies.

The Cambodian system is tax-funded and donor-supported; MoH runs the public network; donor coordination with WHO, USAID, Global Fund, KOICA, JICA. Significant private and pagoda-based health services.

## 2. Scope

In scope: PM Hun Manet; Minister of Health; Secretaries of State; DG Department of Health; DG Drug Department; CEO Calmette Hospital, Khmer-Soviet Friendship Hospital, Preah Kossamak Hospital, National Maternal and Child Health Center; Heads of 25 Provincial Health Departments; National Assembly Health Committee; Cambodian Medical Council.

## 3. Structure

Standard.

## 4. Field definitions

Party affiliation: `CPP` (Cambodian People's Party — Hun Sen / Hun Manet, dominant). Titles in English / Khmer.

## 5. Provenance and dating

H.E. Prof. Chheang Ra serves as Minister of Health in the Hun Manet CPP government (since 2023); medical professor; engaged with UNDP, WHO, US Embassy bilateral cooperation, China bilateral cooperation including Guang'anmen Hospital and Cambodia-China Friendship Hospital network.

## 6. Update workflow

Verify against moh.gov.kh, pressocm.gov.kh, Khmer Times, Phnom Penh Post, VOA Khmer, Cambodianess.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Importing US framings — Cambodia operates pluralistic donor coordination with significant China engagement.

## 9. Acronym glossary

- **CPP** — Cambodian People's Party.
- **MoH** — Ministry of Health.

## 10. Worked example

```yaml
      - H.E. Prof. Chheang Ra (CPP):
          - Title: Minister of Health, Kingdom of Cambodia
          - Stakeholder engagement notes:
              - "Minister of Health in the Hun Manet CPP government (since the 2023 transition from Hun Sen); medical professor; active 2025-2026 public lines: review of Cambodia-China Friendship Hospital achievements; call for higher medical ethics and service quality at provincial healthcare facility inauguration; integrated care emphasis; welcomed UNDP delegation; visit Guang'anmen Hospital in China; United States-Cambodia bilateral Health MOU signed (US Embassy)."
              - "Owns MoH policy, hospital network coordination, donor and bilateral cooperation balancing US-China-Vietnam-Japan-Korea, Institut Pasteur Cambodge research partnership, mpox / dengue / TB / HIV programmes, and Cambodia's WHO WPRO and ASEAN health diplomacy."
              - "Hook: integrated care, medical ethics and service quality, Cambodia-China Friendship Hospital network, US bilateral health MOU, Institut Pasteur Cambodge research, ASEAN cooperation, and donor coordination balancing land."
          - Tone advice:
              - "Open with integrated care, medical ethics, ASEAN cooperation and donor balancing — these are his sustained authored lines."
              - "Do not pitch with single-partner-aligned framings — Cambodia balances US-China-Japan-Korea-Vietnam-EU partnerships pragmatically; single-aligned framings will be filtered."
```

## 11. Out-of-band notes

For roles unfilled or in transition.

## 12. Open questions

- Named Secretaries of State and DG Drug Department under Chheang Ra.
- Heads of Calmette, Khmer-Soviet Friendship, Preah Kossamak Hospitals with currency verified.
- Heads of 25 Provincial Health Departments with currency verified.
- National Assembly Health Committee Chair with currency verified.
- President Cambodian Medical Council with currency verified.
