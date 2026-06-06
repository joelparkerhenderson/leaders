# spec.md — `leaders.yml`

Single source of truth for the Jamaican health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around Jamaica's Ministry of Health and Wellness, the four Regional Health Authorities (SERHA, NERHA, SRHA, WRHA), the National Health Fund (NHF), Pharmaceutical Council of Jamaica, and adjacent bodies.

Jamaica operates a tax-funded public sector with low user fees through the Ministry and four RHAs; the NHF covers chronic-disease medications; private hospitals and private health insurance (Sagicor, Guardian, JN) complement.

## 2. Scope

In scope: PM; Minister of Health and Wellness; Permanent Secretary; CMO; Chief Pharmacist; Regional Directors (SERHA, NERHA, SRHA, WRHA); CEO NHF; Heads of major hospitals (University Hospital of the West Indies UHWI, Kingston Public Hospital, Cornwall Regional, Bustamante Hospital for Children); Chair Joint Select Committee on Health; Medical Association of Jamaica; Jamaica Pharmaceutical Society; Nurses Association of Jamaica.

## 3. Structure

Standard. Ordering: PM → Ministry → CMO → 4 RHAs → NHF → major hospitals → Parliament committee → professional bodies.

## 4. Field definitions

Party affiliation: `JLP` (Jamaica Labour Party), `PNP` (People's National Party). Titles in English.

## 5. Provenance and dating

Dr. the Hon. Christopher Tufton is Minister of Health and Wellness in the Andrew Holness JLP government; long-tenured in the role across multiple Holness cabinet cycles. Active 2026 announcements include calling for 2026 to be 'Year of Mental Wellness'.

## 6. Update workflow

Verify against moh.gov.jm, jis.gov.jm, opm.gov.jm, parliament.gov.jm, Jamaica Gleaner, Jamaica Observer, Loop Jamaica.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating Ministry as the operational owner — RHAs run delivery.
- Importing US framings unmodified — Jamaica is tax-funded universal with low user fees plus NHF chronic-disease subsidy and a substantial private sector.

## 9. Acronym glossary

- **NERHA / NHF / SERHA / SRHA / UHWI / WRHA** — North East / National Health Fund / South East / Southern / University Hospital of the West Indies / Western Regional Health Authority.

## 10. Worked example

```yaml
      - Dr. the Hon. Christopher Tufton (JLP):
          - Title: Minister of Health and Wellness (in the Andrew Holness JLP government)
          - Stakeholder engagement notes:
              - "Minister of Health and Wellness in the Andrew Holness JLP government; long-tenured in the role; PhD in international business and political economy; previously held Industry and Investment portfolio."
              - "Public lines 2025-2026: called for 2026 to be 'Year of Mental Wellness' (Gleaner December 2025); announced $1-billion Health Infrastructure Maintenance Fund (Observer May 2026); developing menopause/andropause policy (Observer May 2026); pushed recruitment agenda; moves to tighten financial operations in public health sector."
              - "Owns Ministry policy, the four RHAs (SERHA, NERHA, SRHA, WRHA), NHF chronic-disease subsidies, public-private balance, primary-care strengthening (Compassionate Care, Health Centres), and Jamaica's CARICOM, PAHO and CARPHA positioning."
              - "Hook: mental wellness, health infrastructure maintenance, NCDs, menopause / andropause policy, NHF subsidies, workforce recruitment and CARICOM cooperation land."
          - Tone advice:
              - "Open with mental wellness, NCDs, NHF and infrastructure — these are Tufton's authored 2026 lines."
              - "Do not pitch as if RHAs were subunits — RHAs operate hospitals with operational autonomy."
```

## 11. Out-of-band notes

For roles unfilled or in transition.

## 12. Open questions

- Named Permanent Secretary, CMO, Chief Pharmacist with currency verified.
- Regional Directors of SERHA, NERHA, SRHA, WRHA with currency verified.
- CEO National Health Fund with currency verified.
- Heads of UHWI, Kingston Public Hospital, Cornwall Regional Hospital, Bustamante Hospital for Children.
- Chair Joint Select Committee on Health in the current Parliament.
- President MAJ, JPS, NAJ with currency verified.
