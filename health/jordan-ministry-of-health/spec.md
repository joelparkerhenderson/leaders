# spec.md — `leaders.yml`

Single source of truth for the Jordanian health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Jordanian Ministry of Health (وزارة الصحة), Royal Medical Services (RMS), Jordan University Hospital, King Hussein Cancer Centre, and adjacent bodies.

The Jordanian system has four sub-sectors: MoH (public hospitals and primary care, serving the uninsured and Civil Insurance Programme); RMS (military and police); university hospitals; and the private sector. Health insurance covers ~85% of citizens through various schemes. Royal Hashemite Court health programmes (free care for poor families, refugees, etc.) supplement.

## 2. Scope

In scope: King; Prime Minister; Minister of Health; Secretary-General; Director-General Royal Medical Services; CEO Health Insurance Administration; Director-General Jordan Food and Drug Administration (JFDA); Director Jordan University Hospital, King Abdullah University Hospital, King Hussein Cancer Centre; CMO Comprehensive Health Centres; Lower House Health Committee Chair; Senate Health Committee Chair; Jordan Medical Association; Jordan Nurses and Midwives Council; Jordan Pharmacists Association.

## 3. Structure

Standard. Ordering: Royal Court → PM → MoH → RMS → JFDA → Health Insurance Administration → academic hospitals → KHCC → Parliament committees → professional associations.

## 4. Field definitions

Party affiliation is fluid; major political directions: `Islamic Action Front`, `National Charter Party`, `Eradah`. Most ministers are independent / technocratic. Titles in English with Arabic where useful.

## 5. Provenance and dating

Dr. Ibrahim Al-Budour was appointed Minister of Health in the August 2025 reshuffle by Royal Decree under Prime Minister Jaafar Hassan, succeeding Dr. Firas Hawari who had served since 29 March 2021.

## 6. Update workflow

Verify against moh.gov.jo, pm.gov.jo, rhc.jo, parliament.jo, Jordan News Agency (Petra), Jordan Times, Ammon News, Roya News English, Al Rai.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating MoH as the only health authority — RMS, university hospitals and private sector are substantial parallel systems.
- Importing US framings unmodified — Jordan combines public, military, academic and private subsystems under royal patronage.

## 9. Acronym glossary

- **CHC** — Comprehensive Health Centre.
- **JFDA** — Jordan Food and Drug Administration.
- **KHCC** — King Hussein Cancer Center.
- **MoH** — Ministry of Health.
- **RMS** — Royal Medical Services.

## 10. Worked example

```yaml
      - Dr. Ibrahim Al-Budour:
          - Title: Minister of Health (since August 2025, in the Jaafar Hassan government)
          - Stakeholder engagement notes:
              - "Minister of Health appointed in a government reshuffle by Royal Decree under PM Jaafar Hassan in August 2025; succeeded Dr. Firas Hawari, who had served since 29 March 2021 across multiple governments and during the Covid-19 response."
              - "Owns Ministry policy, Comprehensive Health Centre (CHC) programme rollout (a Hawari-era initiative that Al-Budour inherited), Civil Insurance Programme, JFDA regulation, KHCC and KAUH royal-patronage-linked centres of excellence, and Jordan's WHO EMRO, WHO Special Envoy for Polio Eradication and refugee-host-country humanitarian-health portfolio."
              - "Operates in a region of complex political-humanitarian dynamics — Jordan hosts large Syrian and Palestinian refugee populations; UNRWA Health programme coordination is structural to the brief."
              - "Hook: Comprehensive Health Centres rollout, Civil Insurance Programme reform, JFDA regulation, KHCC partnerships, refugee health (UNRWA, UNHCR), oncology national strategy, and WHO EMRO cooperation land."
          - Tone advice:
              - "Open with CHC rollout, Civil Insurance Programme, KHCC and refugee-health framing — these are the institutional priorities of the Jordanian Ministry."
              - "Do not pitch as if MoH could direct RMS or KHCC — RMS and KHCC operate under royal patronage with substantial autonomy; engagement on those programmes must include their leadership."
```

## 11. Out-of-band notes

For roles unfilled or in transition.

## 12. Open questions

- Confirm Dr. Ibrahim Al-Budour's full biographical detail and date of swearing-in.
- Named Secretary-General and Directors of major departments under Al-Budour with currency verified.
- Director-General RMS and DG Jordan Food and Drug Administration with currency verified.
- Director KHCC, Director Jordan University Hospital, Director King Abdullah University Hospital with currency verified.
- Chairs of Lower House and Senate Health Committees in the current parliamentary cycle.
- President Jordan Medical Association, Jordan Nurses and Midwives Council, Jordan Pharmacists Association with currency verified.
