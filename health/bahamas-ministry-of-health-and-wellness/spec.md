# spec.md — `leaders.yml`

Single source of truth for the Bahamian health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Bahamas Ministry of Health and Wellness (MoHW), Public Hospitals Authority (PHA), National Health Insurance Authority (NHIA) and adjacent bodies.

The Bahamas is a CARICOM constitutional parliamentary democracy under King Charles III as Head of State (represented by the Governor-General). The Davis (PLP) government has been in office since September 2021. Geography is an archipelago of ~700 islands and cays, with health-system concentration in New Providence (Nassau) and Grand Bahama (Freeport).

## 2. Scope

In scope: Governor-General; Prime Minister; Minister of Health and Wellness; Permanent Secretary; CEO Public Hospitals Authority; Director NHIA; House of Assembly Standing Committee on Health.

Out of scope: Family Island administrators; hospital clinical service heads.

## 3. Structure

Standard 2/6/10/14 indentation. Top-level key: `Bahamian health stakeholders:`. Ordering: Governor-General → Prime Minister → MoHW → PHA → NHIA → Parliament.

## 4. Field definitions

Party affiliation: `PLP` (Progressive Liberal Party, ruling), `FNM` (Free National Movement, principal opposition), `DNA` (Democratic National Alliance). Titles in English; `Hon.` standard for ministers.

## 5. Provenance and dating

Anchor to year, month or date. Dr. Michael Darville has served as Minister of Health and Wellness in the Davis PLP government since September 2021; medical doctor.

## 6. Update workflow

Verify against bahamas.gov.bs, mohw.gov.bs, parliament.bs, Tribune242, Nassau Guardian, ZNS Bahamas, Bahamas Information Services.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating the Bahamas as a Caribbean SIDS with only one island — the archipelago dimension is structural for health-system design (inter-island referral, air-medical evacuation).
- Conflating with Jamaica or Trinidad — distinct sovereign CARICOM member.
- Ignoring NHI rollout — the National Health Insurance is in phased rollout and is a sustained political priority.

## 9. Acronym glossary

- **CARICOM** — Caribbean Community.
- **MoHW** — Ministry of Health and Wellness.
- **NHIA** — National Health Insurance Authority.
- **PHA** — Public Hospitals Authority.
- **PLP** — Progressive Liberal Party.

## 10. Worked example

```yaml
      - Hon. Dr. Michael Darville (PLP):
          - Title: Minister of Health and Wellness (since September 2021)
          - Stakeholder engagement notes:
              - "Minister of Health and Wellness in the Davis PLP government since September 2021; medical doctor; long-serving PLP parliamentarian."
              - "Owns MoHW policy and budget, Princess Margaret Hospital (Nassau), Rand Memorial Hospital (Freeport), Sandilands Rehabilitation Centre, the Family Island clinic network (across the 16 inhabited Family Islands), PHA operations, NHIA rollout, and CARICOM-CARPHA and PAHO diplomacy."
              - "Hook: NHI rollout and primary-care strengthening, NCDs (high obesity, diabetes, cardiovascular burden), mental health, hurricane preparedness (post-Dorian 2019 reconstruction), and CARPHA cooperation land."
          - Tone advice:
              - "Open with NHI, NCDs, mental health, hurricane preparedness and CARPHA cooperation."
              - "Do not treat as single-island or conflate with other CARICOM states."
```

## 11. Out-of-band notes

For roles unfilled or interim.

## 12. Open questions

- Permanent Secretary and CEO PHA with currency verified.
- Director NHIA with currency verified.
- House Standing Committee on Health Chair.
