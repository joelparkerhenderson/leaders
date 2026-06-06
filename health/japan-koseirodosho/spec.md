# spec.md — `leaders.yml`

Single source of truth for the structure, semantics, and update rules of `leaders.yml` for the Japanese health system. The YAML must conform to this spec; if they disagree, the spec wins and the YAML is fixed.

## 1. Purpose

`leaders.yml` is an engagement register of named individuals in and around the Japanese health system. Each entry helps a reader inside the Ministry of Health, Labour and Welfare (Kōsei Rōdō Shō / 厚生労働省), the PMDA (Pharmaceuticals and Medical Devices Agency), Chuikyo (Central Social Insurance Medical Council), the Japan Health Insurance Association (Kyōkai Kenpō), the National Hospital Organisation, or an adjacent body decide who to engage, how, and where.

The Japanese system is Bismarckian universal social-insurance through ~3,000 employer-based and municipal funds operating under uniform benefit and fee schedules. The Ministry of Health, Labour and Welfare (MHLW, often called Kōrōshō) sets policy and the biennial Shinryō Hōshū revision through the Chuikyo (中央社会保険医療協議会) advisory council. PMDA regulates medicines and devices. Hospitals are predominantly private not-for-profit; the National Hospital Organisation runs major public hospitals.

## 2. Scope

**In scope:** Naikaku Sōri Daijin (Prime Minister); Kōsei Rōdō Daijin (Minister of Health, Labour and Welfare); Senior Vice-Minister and Parliamentary Vice-Ministers; Jimu-jikan (Administrative Vice-Minister); Kanbō-chō (Director-General Minister's Secretariat); Iseikyoku-chō (Director-General Health Policy Bureau); Hokenkyoku-chō (Health Insurance Bureau); Yakkyoku-chō (Pharmaceutical Safety Bureau); Riji-chō PMDA; Chair Chuikyo; President National Hospital Organisation; Chair JMA (Nihon Ishikai); Chair JPMA; Chair JNA (Nihon Kango Kyōkai); Chair House of Representatives Committee on Health, Labour and Welfare; Chair House of Councillors Committee on Health, Labour and Welfare.

**Out of scope:** operational staff below kacho level inside Kōrōshō; vendors; historical post-holders.

## 3. Structure

```
日本の医療システム関係者 / Japanese health system stakeholders:
  - {Organisation}:
      - {Person}:
          - Title: ...
          - Stakeholder engagement notes: [...]
          - Tone advice: [...]
```

Indentation 2/6/10/14 spaces. Ordering: Naikaku → Kōrōshō → PMDA → Chuikyo → National Hospital Organisation → JMA / JNA / JPMA → House Committees.

## 4. Field definitions

Standard family conventions. Party affiliation using canonical Japanese abbreviations: `LDP` (自民党, Jimintō), `Komeito` (公明党), `CDP` (立憲民主党, Rikken Minshutō), `Ishin no Kai` (日本維新の会), `Kokumin Minshutō` (国民民主党), `Reiwa Shinsengumi` (れいわ新選組), `JCP` (日本共産党, Nihon Kyōsantō), `Sansei-tō` (参政党). Titles in English with Japanese where useful; person names in family-name-first order following Japanese convention.

## 5. Provenance and dating

Anchor facts to year, month or exact date. Sanae Takaichi (LDP) became Prime Minister in October 2025 following Shigeru Ishiba's resignation; Kenichiro Ueno took office as Minister of Health, Labour and Welfare on 21 October 2025 in the Takaichi Cabinet.

## 6. Update workflow

1. Identify the change. 2. Verify against kantei.go.jp, mhlw.go.jp, pmda.go.jp, sangiin.go.jp, shugiin.go.jp, Nikkei, Asahi, Yomiuri, Mainichi, NHK, Japan Times. 3. Apply minimum diff. 4. Confirm structure. 5. Re-validate cross-references.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating MHLW as a buyer — fees are set by Chuikyo through the Shinryō Hōshū process; insurers and providers operate within those uniform fee schedules.
- Importing NHS framings unmodified — Japan is multi-payer Bismarckian with uniform fees and predominantly private hospital ownership.

## 9. Acronym glossary

- **Chuikyo / 中医協** — Central Social Insurance Medical Council (Chuō Shakai Hoken Iryō Kyōgikai).
- **JMA / 日本医師会** — Japan Medical Association (Nihon Ishikai).
- **JNA / 日本看護協会** — Japan Nursing Association.
- **JPMA / 日本製薬工業協会** — Japan Pharmaceutical Manufacturers Association.
- **Kōrōshō / 厚生労働省** — Ministry of Health, Labour and Welfare (MHLW).
- **Kyōkai Kenpō** — Japan Health Insurance Association (the largest employer-based insurer for SMEs).
- **NHO / 国立病院機構** — National Hospital Organisation.
- **PMDA / 医薬品医療機器総合機構** — Pharmaceuticals and Medical Devices Agency.
- **Shinryō Hōshū / 診療報酬** — the biennial uniform medical fee schedule revision.

## 10. Worked example

```yaml
      - Ueno Kenichirō / 上野 賢一郎 (LDP):
          - Title: Minister of Health, Labour and Welfare (厚生労働大臣 Kōsei Rōdō Daijin) (since 21 October 2025)
          - Stakeholder engagement notes:
              - "Minister of Health, Labour and Welfare in the Takaichi Cabinet from 21 October 2025; LDP; takes office at a time of acute labour-shortage and population-ageing pressures."
              - "Owns the next Shinryō Hōshū (medical fee schedule) revision cycle, MHLW policy on long-term care insurance (Kaigo Hoken), pharmaceutical pricing policy through Chuikyo, vaccine and infectious-disease policy, and workforce-import policy through the technical-trainee and Specified-Skilled-Worker visa frameworks."
              - "Sectoral context: severe shortage of medical and care workforce in the ageing population, hospital consolidation, drug pricing pressure, and the post-Covid recovery of MHLW credibility are recurring policy lines."
              - "Hook: medical fee schedule revision, long-term care insurance reform, workforce import, pharmaceutical pricing, regional medical care planning (chiiki iryō kōsō), and digital health (Online Shihō, My Number Health Insurance Card) land."
          - Tone advice:
              - "Open with Shinryō Hōshū revision, long-term care, workforce, pharmaceutical pricing and digital health — these are the MHLW levers and current Takaichi-cabinet priorities."
              - "Do not pitch as if MHLW were a single buyer or hospital operator — Japan's universal coverage is delivered by ~3,000 insurers contracting with predominantly private not-for-profit hospitals through uniform fees; MHLW sets the rules, not the contracts."
```

## 11. Out-of-band notes

For roles unfilled or interim.

## 12. Open questions

- Named Senior Vice-Minister and Parliamentary Vice-Ministers under Ueno in the Takaichi Cabinet with currency verified.
- Jimu-jikan (Administrative Vice-Minister) and bureau heads (Iseikyoku, Hokenkyoku, Yakkyoku, Roken-kyoku, Roudou-kijun-kyoku) with currency verified.
- Riji-chō PMDA, Chair Chuikyo (rotating among employer-side, provider-side, and impartial seats), President National Hospital Organisation with currency verified.
- Chair Japan Medical Association (JMA), Japan Nursing Association (JNA), Japan Pharmaceutical Association (Nihon Yakuzaishi Kai), Japan Pharmaceutical Manufacturers Association (JPMA) with currency verified.
- Chair House of Representatives Committee on Health, Labour and Welfare and Chair House of Councillors Committee on Health, Labour and Welfare in the current Diet sessions.
