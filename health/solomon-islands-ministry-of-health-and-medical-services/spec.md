# spec.md — `leaders.yml`

Single source of truth for the Solomon Islands health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Solomon Islands Ministry of Health and Medical Services (MHMS) and adjacent bodies.

Solomon Islands is a Commonwealth realm under King Charles III with an archipelago geography (~900 islands). The Jeremiah Manele (OUR Party — Ownership, Unity and Responsibility) government has been in office since May 2024 following the April 2024 election that succeeded Manasseh Sogavare's government. Member of PIF, MSG, ACP, Commonwealth.

## 2. Scope

In scope: Governor-General; Prime Minister; Minister of Health and Medical Services; Permanent Secretary; National Referral Hospital; National Parliament Committee.

Out of scope: provincial health officers.

## 3. Structure

Standard 2/6/10/14 indentation. Top-level key: `Solomon Islands health stakeholders:`.

## 4. Field definitions

Party affiliation: `OUR Party` (Ownership, Unity and Responsibility, ruling Manele), `DCC` (Democratic Coalition for Change, coalition partner), `KP` (Kadere Party), `PAP` (People's Alliance Party), `UP` (United Party). Titles in English.

## 5. Provenance and dating

Anchor to year, month or date. The Minister of Health under PM Jeremiah Manele (since May 2024) is to be verified against the Office of the Prime Minister.

## 6. Update workflow

Verify against pmc.gov.sb, parliament.gov.sb, Solomon Star, Solomon Times Online, SIBC.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating SI as small SIDS — second-largest Melanesian state by population with continental-scale archipelago challenges.
- Ignoring the China-bilateral shift — Solomon Islands switched recognition from Taiwan to China in 2019 and has signed a security pact with China in 2022; geopolitical context shapes engagement.

## 9. Acronym glossary

- **MHMS** — Ministry of Health and Medical Services.
- **MSG** — Melanesian Spearhead Group.
- **OUR Party** — Ownership, Unity and Responsibility.

## 10. Worked example

```yaml
      - Notes on Minister of Health and Medical Services of Solomon Islands:
          - Status: Verify against pmc.gov.sb.
          - Implication: Engagement requires recognition of Manele coalition dynamics, China-bilateral shift, and archipelago architecture.
          - Hook: malaria (high burden), MCH, NCDs, TB, dengue, climate-and-health, post-2022-riots reconstruction.
          - Tone: Open with malaria, MCH, NCDs, climate-and-health and PIF-MSG cooperation.
```

## 11. Out-of-band notes

For roles unfilled or interim.

## 12. Open questions

- Substantive identity of Minister of Health and Medical Services with currency verified.
