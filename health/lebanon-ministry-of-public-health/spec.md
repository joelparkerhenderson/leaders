# spec.md — `leaders.yml`

Single source of truth for the Lebanese health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Lebanese Ministry of Public Health (وزارة الصحة العامة), National Social Security Fund (NSSF), military and Internal Security Forces health schemes, and adjacent bodies.

The Lebanese system relies heavily on a substantial private and not-for-profit hospital sector (over 80% of beds private), with the Ministry of Public Health funding care for the uninsured. NSSF covers formal-sector workers (limited). The 2019 financial crisis and 2023-2025 conflict with Israel have severely damaged the system. The new Aoun-Salam government (2025) and the post-conflict reconstruction context shape engagement.

## 2. Scope

In scope: President; Prime Minister; Minister of Public Health; Director-General Ministry; CEO NSSF; Director Pharmacy Department; Heads of Rafik Hariri University Hospital and major private hospitals (AUBMC, Hôtel-Dieu, LAUMC Rizk, Hammoud, Bahman); Heads of South Lebanon hospitals (Marjeyoun, Bint Jbeil, Nabatieh) per the recent conflict context; Parliamentary Health Committee Chair; Lebanese Order of Physicians (Beirut, North, BeqaaTripoli); Lebanese Order of Pharmacists; WHO Lebanon Office head.

## 3. Structure

Standard. Ordering: Presidency → MoPH → NSSF → major hospitals → South Lebanon hospitals → Parliament → Lebanese Order of Physicians → WHO Lebanon.

## 4. Field definitions

Confessional and political alignments. Major parties: `Free Patriotic Movement` (FPM, Maronite, Aounist), `Lebanese Forces` (LF, Maronite), `Future Movement` (Sunni), `PSP` (Druze, Jumblatt), `Hezbollah` (Shia), `Amal Movement` (Shia), `Kataeb`, `Marada`, `Tashnaq` (Armenian). Independents are growing. Titles in English with Arabic where useful.

## 5. Provenance and dating

Dr. Rakan Nassereddine has served as Minister of Public Health in the Nawaf Salam government formed after Joseph Aoun's election as President in January 2025; doctor with PhD in infectious diseases; arterial / vascular surgeon at American University of Beirut Medical Center (AUBMC). Active 2026 on health-sector reconstruction discussions with the World Bank, on mental-health-services expansion (St Charles Rihaniyyeh psychiatric department September 2025), and reporting on Israeli airstrike casualties (March 2026: 394 deaths since 2 March 2026 including 83 children).

## 6. Update workflow

Verify against moph.gov.lb, lp.gov.lb, presidency.gov.lb, the961.com, NowLebanon, L'Orient-Le Jour, The Daily Star Lebanon, Reuters Beirut.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating MoPH as the operational hospital owner — the substantial private hospital sector and AUBMC, Hôtel-Dieu and other major private centres are core.
- Importing US framings unmodified — Lebanon is confessionally distributed, with multiple insurance schemes and a strong private sector.

## 9. Acronym glossary

- **AUBMC** — American University of Beirut Medical Center.
- **HDF** — Hôtel-Dieu de France hospital, Beirut.
- **LAUMC** — Lebanese American University Medical Center.
- **MoPH** — Ministry of Public Health.
- **NSSF** — National Social Security Fund.
- **RHUH** — Rafik Hariri University Hospital (Beirut public hospital).

## 10. Worked example

```yaml
      - Dr. Rakan Nassereddine:
          - Title: Minister of Public Health of Lebanon (in the Nawaf Salam government, since 2025)
          - Stakeholder engagement notes:
              - "Minister of Public Health in the Nawaf Salam government formed after Joseph Aoun's election as President in January 2025; Lebanese doctor; PhD in infectious diseases; arterial / vascular surgeon at the American University of Beirut Medical Center (AUBMC) — clinical-academic background brings substantial credibility to the portfolio."
              - "Active 2026: discussed health-sector reconstruction and hospital development with the World Bank; inaugurated the psychiatric department at St Charles Hospital in Rihaniyyeh (September 2025), emphasising its significance in advancing mental-health services in Lebanon; visited hospitals of Bint Jbeil and other South Lebanon facilities; reported in March 2026 that Israeli airstrikes in Lebanon had killed 394 people since 2 March 2026, including 83 children and 42 women, with 1,130 wounded (CGTN, TRT World)."
              - "Owns MoPH policy, NSSF coordination, oversight of public hospitals (Rafik Hariri University Hospital is the main public tertiary facility), contracts with private hospitals (AUBMC, Hôtel-Dieu, LAUMC, Hammoud, Bahman), pharmaceutical supply, vaccination, mental health, reconstruction of South Lebanon health facilities, and WHO EMRO and Arab League positioning."
              - "Hook: post-conflict reconstruction of South Lebanon hospitals, mental health expansion, pharmaceutical supply, hospital sector financing reform, MoPH-private-hospital contracts, climate-and-health, and WHO / World Bank donor coordination land."
          - Tone advice:
              - "Open with post-conflict reconstruction, mental-health expansion, hospital sector financing and donor coordination — these are his sustained 2025-2026 lines and align with the Aoun-Salam reform government."
              - "Do not assume political stability — Lebanon's confessional politics, continued Israeli strikes, Hezbollah-state tensions and economic crisis make every health-policy decision politically charged."
```

## 11. Out-of-band notes

For roles unfilled or in transition.

## 12. Open questions

- Named Director-General Ministry of Public Health under Nassereddine with currency verified.
- CEO NSSF with currency verified.
- Director Pharmacy Department with currency verified.
- Heads of RHUH, AUBMC, Hôtel-Dieu, LAUMC Rizk, Hammoud, Bahman with currency verified.
- Heads of South Lebanon hospitals (Marjeyoun, Bint Jbeil, Nabatieh) and reconstruction status.
- Parliamentary Health Committee Chair with currency verified.
- Presidents Lebanese Order of Physicians (Beirut), North, Tripoli orders; Lebanese Order of Pharmacists with currency verified.
