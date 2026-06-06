# spec.md — `leaders.yml`

Single source of truth for the Botswana health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Botswana Ministry of Health (MoH), Botswana Medicines Regulatory Authority (BoMRA), National AIDS and Health Promotion Agency (NAHPA), and adjacent bodies.

Botswana operates a predominantly public, primary-care-focused health system funded from general taxation with effectively universal coverage; the country is a recognised HIV/AIDS-response success case (~95-95-95 achieved early). The Ministry serves under the Duma Boko UDC coalition government (since October 2024).

## 2. Scope

In scope: President; Vice President; Minister of Health; Assistant Minister; Permanent Secretary; CEO BoMRA; CEO NAHPA; Director Health Services; Director Public Health; Parliamentary Portfolio Committee on Health; Botswana Medical Association (BMA); Botswana Nurses Union (BONU).

Out of scope: hospital superintendents; district-health-management-team members.

## 3. Structure

Standard 2/6/10/14 indentation. Top-level key: `Botswana health stakeholders:`. Ordering: Presidency → MoH → BoMRA → NAHPA → Parliament → professional associations.

## 4. Field definitions

Party affiliation: `UDC` (Umbrella for Democratic Change, ruling coalition led by BNF), `BNF` (Botswana National Front, lead UDC party), `BDP` (Botswana Democratic Party, principal opposition — in government for 58 years until 2024), `BPF` (Botswana Patriotic Front), `BCP` (Botswana Congress Party). Independent for non-aligned and specially-elected MPs without affiliation. Titles in English.

## 5. Provenance and dating

Anchor to year, month or date. Dr. Stephen Modise was appointed Minister of Health on 16 November 2024 by President Duma Boko, six weeks into the UDC coalition government following the historic 30 October 2024 BDP defeat.

## 6. Update workflow

Verify against moh.gov.bw, gov.bw, parliament.gov.bw, bomra.co.bw, Mmegi, Botswana Daily News, Sunday Standard, Mmegi Monitor, Weekend Post.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating Botswana as low-middle-income default — Botswana is an upper-middle-income country with sophisticated regulatory and clinical capacity (the SADC HIV reference state); framings appropriate to LIC contexts will be filtered.
- Ignoring the 2024 political transition — the BDP lost power for the first time since independence (1966); the UDC government is implementing a different policy stance on procurement, HR and decentralisation; pitches built on the prior administration's programmes risk being out of date.

## 9. Acronym glossary

- **BDP** — Botswana Democratic Party.
- **BMA** — Botswana Medical Association.
- **BNF** — Botswana National Front.
- **BoMRA** — Botswana Medicines Regulatory Authority.
- **MoH** — Ministry of Health.
- **NAHPA** — National AIDS and Health Promotion Agency.
- **UDC** — Umbrella for Democratic Change.

## 10. Worked example

```yaml
      - Dr. Stephen Modise (UDC):
          - Title: Minister of Health (since 16 November 2024)
          - Stakeholder engagement notes:
              - "Appointed Minister of Health on 16 November 2024 by President Duma Boko, six weeks into the UDC coalition government following the historic BDP defeat of 30 October 2024 (the BDP had held power continuously since independence in 1966); Specially Elected MP; 37 years old at appointment — one of the youngest health ministers in Africa; nominated to the World Economic Forum Young Global Leaders Class of 2026."
              - "Owns MoH policy and budget, the national hospital network (Princess Marina, Nyangabgwe, Sir Ketumile Masire Teaching Hospital), the primary-care clinic and health-post network, BoMRA oversight, NAHPA programmes (HIV, NCDs, mental health), and SADC health-diplomacy participation."
              - "Hook: HIV continuity (Botswana is the SADC and global 95-95-95 reference case), NCDs (rising diabetes and hypertension burden), universal access strengthening, mental health, HR retention (specialist emigration to South Africa and Gulf), and Young Global Leader-network engagement on health-system innovation land."
          - Tone advice:
              - "Open with HIV continuity, NCDs, universal access, mental health and health-system innovation — these are Modise's signature lines and the priorities of the UDC government."
              - "Do not anchor to the prior BDP administration's programmes or HR doctrine — the UDC is recalibrating procurement, decentralisation and specialist-retention policy; framings that assume continuity will be politely corrected."
```

## 11. Out-of-band notes

For roles unfilled or interim.

## 12. Open questions

- Named Assistant Minister and Permanent Secretary with currency verified.
- CEO BoMRA and CEO NAHPA with currency verified.
- Parliamentary Portfolio Committee on Health Chair with currency verified.
