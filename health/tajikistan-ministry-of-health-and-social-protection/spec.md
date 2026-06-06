# spec.md — `leaders.yml`

Single source of truth for the Tajik health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Tajik Ministry of Health and Social Protection of the Population (MoHSPP) and adjacent bodies.

Tajikistan is a presidential republic under Emomali Rahmon (in power since 1992 — one of the longest-serving heads of state in Eurasia), with a Persian-cultural identity, post-Soviet health infrastructure, and a position bordering Afghanistan that shapes security-and-health framing.

## 2. Scope

In scope: President; Prime Minister; Minister of Health and Social Protection; Director-General National Medical Centre Shifobakhsh; Majlisi Namoyandagon (Assembly of Representatives) Committee on Health.

Out of scope: oblast and rayon health office heads.

## 3. Structure

Standard 2/6/10/14 indentation. Top-level key: `Tajik health stakeholders:`. Ordering: Presidency → Cabinet → MoHSPP → Hospitals → Parliament.

## 4. Field definitions

Affiliation: `PDPT` (People's Democratic Party of Tajikistan, ruling — Rahmon-led, dominant). Titles in English.

## 5. Provenance and dating

Anchor to year, month or date. Jamoliddin Abdullozoda has served as Minister of Health and Social Protection of the Population in the Rahmon government; verify currency against the Presidency and Khovar (National Information Agency).

## 6. Update workflow

Verify against moh.tj, president.tj, khovar.tj, Asia-Plus, Radio Ozodi (RFE/RL Tajik Service).

## 7. Invariants

Standard.

## 8. Anti-patterns

- Conflating with Uzbekistan or Kyrgyzstan — sovereign state with Persian-cultural identity (Tajik is a Persian language) and distinct architecture.
- Importing Afghan-driven framings as primary — the Afghan border affects security and migration but Tajikistan operates its own MoHSPP agenda which is broader than border issues.

## 9. Acronym glossary

- **MoHSPP** — Ministry of Health and Social Protection of the Population.
- **PDPT** — People's Democratic Party of Tajikistan.

## 10. Worked example

```yaml
      - Jamoliddin Abdullozoda (PDPT):
          - Title: Minister of Health and Social Protection of the Population
          - Stakeholder engagement notes:
              - "Minister of MoHSPP in the Rahmon government; medical doctor; verify currency against president.tj and Khovar."
              - "Owns MoHSPP policy and budget, the National Medical Centre Shifobakhsh, oblast hospitals across Sughd, Khatlon, GBAO and DRS, primary-care network, social-protection programmes, and WHO Europe, CIS, SCO, ECO and Persian-cultural diplomacy."
              - "Hook: TB and MDR-TB (Tajikistan has high MDR-TB burden), HIV, MCH, NCDs, migration health (large Tajik labour migration to Russia), nutrition, polio surveillance and Afghan-border health-security land."
          - Tone advice:
              - "Open with TB-MDR, MCH, NCDs, migration health, nutrition and polio surveillance."
              - "Do not conflate with neighbouring CA states or reduce to Afghan-border framings."
```

## 11. Out-of-band notes

For roles unfilled or interim.

## 12. Open questions

- Director-General National Medical Centre with currency verified.
- Majlisi Namoyandagon Committee on Health Chair with currency verified.
