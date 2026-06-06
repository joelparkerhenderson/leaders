# spec.md — `leaders.yml`

Single source of truth for the Iranian health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Iranian Ministry of Health and Medical Education (وزارت بهداشت، درمان و آموزش پزشکی, Vezārat-e Behdāsht, Darmān va Āmuzesh-e Pezeshki), the Iran Food and Drug Administration (IFDA), social-insurance organisations, university hospitals, and adjacent bodies.

The Iranian system combines the public Ministry of Health network (universal access for the uninsured), the Social Security Organisation (SSO) and Iran Health Insurance Organisation (IHIO) for formal-sector workers and others, a large foundation (bonyad) sector, the Imam Khomeini Relief Foundation, military medical services, and a substantial private sector. Medical Universities (Tehran, Shahid Beheshti, Iran University of Medical Sciences, Mashhad, Shiraz, Isfahan, Tabriz) run regional health systems combining academic, hospital and population-health functions.

## 2. Scope

In scope: Supreme Leader's Office (where it intervenes on health); President; First Vice-President; Minister of Health and Medical Education; Deputy Ministers (Health, Treatment, Education, Food and Drug); Head of Iran Food and Drug Administration; Director of Social Security Organisation; Director of Iran Health Insurance Organisation; Chancellors of major Medical Universities; Director Pasteur Institute of Iran; Chair Majles (Parliament) Health and Treatment Commission; President Iran Medical Council; President Iran Nursing Organisation.

## 3. Structure

Standard 2/6/10/14. Ordering: Presidency → Ministry of Health → IFDA → SSO/IHIO → major Medical Universities → Pasteur Institute → Majles Commission → professional councils.

## 4. Field definitions

Party affiliation in Iran is fluid; principal alignments are Reformist / Moderate vs Principalist / Conservative; personalities and factions often more salient than parties. Titles in English with Persian (Farsi) where useful.

## 5. Provenance and dating

Mohammad-Reza Zafarghandi has served as Minister of Health and Medical Education since August 2024 in the Masoud Pezeshkian (Reformist) government formed after the July 2024 presidential election that followed the death of Ebrahim Raisi. Vascular surgeon; previously head of the Iranian Medical Council 2018-2021; full professor at Tehran University of Medical Sciences. Active 2025-2026 statements have been dominated by health-impact of US-Israeli strikes on Iran and on Gaza/Lebanon, including reported damage to fifty hospitals.

## 6. Update workflow

Verify against behdasht.gov.ir, president.ir, ifda.fda.gov.ir, fda.gov.ir, parliament.ir, IRNA, ISNA, Tasnim, Mehr News, PressTV, IranWire, Iran International (in exile).

## 7. Invariants

Standard.

## 8. Anti-patterns

- Ignoring the Supreme Leader's overall directive role on strategic health questions.
- Importing US framings unmodified — Iran has segmented Bismarckian-Beveridge mix with significant foundation and military pillars, plus sanctions-shaped supply chains.

## 9. Acronym glossary

- **IFDA** — Iran Food and Drug Administration.
- **IHIO** — Iran Health Insurance Organisation.
- **Majles** — Islamic Consultative Assembly (parliament).
- **MoHME** — Ministry of Health and Medical Education.
- **Pasteur Institute** — Institut Pasteur d'Iran (vaccine, infectious-disease research).
- **SSO** — Social Security Organisation.

## 10. Worked example

```yaml
      - Mohammad-Reza Zafarghandi (Pezeshkian Reformist coalition):
          - Title: Minister of Health and Medical Education (since August 2024)
          - Stakeholder engagement notes:
              - "Minister of Health and Medical Education since August 2024 in the Pezeshkian government formed after the July 2024 election that followed President Ebrahim Raisi's death; vascular surgery specialist; full professor at Tehran University of Medical Sciences; previously head of the Iranian Medical Council (Sazman Nezam Pezeshki) 2018-2021."
              - "Parliament Health Commission approved his qualification for the ministry; aligned with the Pezeshkian reformist health-and-development agenda."
              - "Active 2025-2026 public lines: called on UN to halt Israeli raids on Gaza medical centres; called US-Israeli bombing of Tehran's Pasteur Institute (April 2026) an 'international disaster'; stated fifty Iranian hospitals damaged during US-Israeli attacks on Iran; appealed to WHO DG via Iran_GOV X account framing attacks as 'war on health'."
              - "Owns Ministry of Health budget, IFDA regulation, MoHME-affiliated medical universities, hospital network reconstruction, sanctions-affected drug-supply files (including biologics), and post-strike Pasteur Institute reconstruction."
              - "Hook: hospital reconstruction post-strikes, Pasteur Institute rebuilding, sanctions-affected drugs and biologics supply, immunisation, NCDs, primary care expansion (the Pezeshkian health reform legacy from his earlier ministerial term under Khatami) land."
          - Tone advice:
              - "Open with hospital reconstruction, sanctions-affected medicine supply, Pasteur Institute rebuilding and humanitarian framing on Gaza-Lebanon — these are his sustained 2026 public lines."
              - "Do not pitch with US-aligned framings — engagement is politically charged given the 2025-2026 strikes; Western-corporate framings will require careful sanctions-compliance and political calibration."
```

## 11. Out-of-band notes

For roles unfilled or in transition.

## 12. Open questions

- Named Deputy Ministers under Zafarghandi (Health, Treatment, Education, Food and Drug) with currency verified.
- Head of IFDA with currency verified.
- Director SSO and Director IHIO with currency verified.
- Chancellors of Tehran University of Medical Sciences (TUMS), Shahid Beheshti University of Medical Sciences (SBMU), Iran University of Medical Sciences (IUMS), Mashhad UMS, Shiraz UMS, Isfahan UMS, Tabriz UMS with currency verified.
- Director Pasteur Institute of Iran post-strike reconstruction.
- Chair Majles Health and Treatment Commission in the current Majles term.
- President Iran Medical Council and Iran Nursing Organisation with currency verified.
