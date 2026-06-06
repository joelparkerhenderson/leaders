# spec.md — `leaders.yml`

Single source of truth for the Kuwaiti health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Kuwait Ministry of Health (وزارة الصحة), Kuwait Foundation for the Advancement of Sciences (KFAS), Kuwait Cancer Control Center, KOC and KMC medical services, and adjacent bodies.

The Kuwaiti system delivers universal coverage for citizens free at point of use through MoH-operated public hospitals, primary health centres and Polyclinics. Expatriates pay for treatment under separate insurance arrangements. The 'New Kuwait 2035' Vision frames reform.

## 2. Scope

In scope: Amir; Crown Prince; PM; Minister of Health; Undersecretary; Heads of major public hospitals (Mubarak Al-Kabeer, Al-Adan, Al-Amiri, Farwaniya, Al-Sabah, Al-Razi, Jaber, Jahra, New Maternity); Director-General Kuwait Cancer Control Centre; Director Pharmaceutical and Health Stores; Director Public Health Department; Chair National Assembly Health Committee (when Assembly convened); Kuwait Medical Association.

## 3. Structure

Standard. Ordering: Amir / PM → MoH → major public hospitals → Kuwait Cancer Control Centre → Pharmaceutical Department → National Assembly Committee → Kuwait Medical Association.

## 4. Field definitions

Kuwait does not have formal political parties; major political groupings: `tribal`, `Islamist`, `liberal-merchant`, `Shia`. Titles in English with Arabic transliteration.

## 5. Provenance and dating

Dr. Ahmad Abdulwahab Al-Awadhi has served as Minister of Health; in May 2026 His Highness the Amir received Minister Al-Awadhi at the presentation of newly-appointed Health Ministry Undersecretary Sheikh Dr. Salman Khalifah Al-Sabah; in December 2025 Al-Awadhi issued 11 ministerial decrees to strengthen governance and modernise the health sector across public health, technical, private and pharmaceutical-control sectors.

## 6. Update workflow

Verify against moh.gov.kw, e.gov.kw, Kuwait News Agency (KUNA), Kuwait Times, Arab Times Kuwait, Al-Anbaa, Al-Qabas.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating MoH as the only relevant authority — Kuwait Oil Company and Kuwait Petroleum Corporation health services and military health systems are parallel.
- Importing US framings unmodified — Kuwait is fully tax-funded for citizens with strong sovereign-wealth backing.

## 9. Acronym glossary

- **KFAS** — Kuwait Foundation for the Advancement of Sciences.
- **MoH** — Ministry of Health.
- **New Kuwait 2035** — national vision framework.

## 10. Worked example

```yaml
      - Dr. Ahmad Abdulwahab Al-Awadhi:
          - Title: Minister of Health of the State of Kuwait
          - Stakeholder engagement notes:
              - "Minister of Health of the State of Kuwait; in May 2026 His Highness the Amir received Minister Al-Awadhi, who presented the newly-appointed Health Ministry Undersecretary Sheikh Dr. Salman Khalifah Al-Sabah (KUNA, May 2026) — extension of the senior leadership team."
              - "December 2025 issued 11 ministerial decrees to strengthen governance and modernise the health sector, covering the public health, technical, private and pharmaceutical control sectors (Kuwait Times) — substantive administrative reform agenda."
              - "Owns MoH policy and budget, public hospital network (Mubarak Al-Kabeer, Al-Adan, Al-Amiri, Farwaniya, Al-Sabah, Al-Razi, Jaber, Jahra), Kuwait Cancer Control Centre, Pharmaceutical and Health Stores, Public Health Department, and Kuwait's WHO EMRO, GCC and Arab League positioning."
              - "Hook: governance modernisation (11 December 2025 decrees), public hospital expansion, oncology national programme, pharmaceutical-control modernisation, healthtech and AI, sovereign-wealth-funded health-infrastructure investment land."
          - Tone advice:
              - "Open with governance modernisation, public hospital network, oncology and healthtech — these are the live 2025-2026 priorities and his authored decree-based reforms."
              - "Do not assume rapid political timelines — Kuwait's National Assembly cycles are volatile; major legislative health reforms require Amiri Decree where the Assembly is suspended."
```

## 11. Out-of-band notes

For roles unfilled or interim. Note the recent appointment of Sheikh Dr. Salman Khalifah Al-Sabah as Undersecretary.

## 12. Open questions

- Undersecretary MoH (Sheikh Dr. Salman Khalifah Al-Sabah confirmed per recent KUNA coverage) with currency verified.
- Heads of major public hospitals with currency verified.
- Director-General Kuwait Cancer Control Centre, Director Pharmaceutical and Health Stores, Director Public Health Department with currency verified.
- Chair National Assembly Health Committee when Assembly is convened.
- President Kuwait Medical Association with currency verified.
