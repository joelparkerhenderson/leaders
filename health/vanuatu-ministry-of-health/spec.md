# spec.md — `leaders.yml`

Single source of truth for the ni-Vanuatu health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Vanuatu Ministry of Health and adjacent bodies. Vanuatu is a parliamentary republic with bilingual English-French heritage as a former Anglo-French condominium; PIF, MSG, ACP, Commonwealth, OIF member; political fragmentation has driven frequent government turnover (most recent: PM Jotham Napat from late 2024 / early 2025).

## 2. Scope

In scope: President; Prime Minister; Minister of Health; Director-General Vila Central Hospital; Parliament.

Out of scope: provincial health office heads.

## 3. Structure

Standard 2/6/10/14 indentation.

## 4. Field definitions

Vanuatu has many small parties: `Reunification of Movements for Change (RMC)`, `Leaders Party`, `Union of Moderate Parties`, `Vanua'aku Pati`, `National United Party`. Titles bilingual.

## 5. Provenance and dating

Verify against gov.vu and Vanuatu Daily Post.

## 6. Update workflow

Verify against gov.vu, parliament.gov.vu, Vanuatu Daily Post, Vanuatu Independent, VBTC.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Assuming government stability — Vanuatu has frequent VONCs and cabinet reshuffles.
- Ignoring bilingual heritage.

## 9. Acronym glossary

Standard PIF/MSG.

## 10. Worked example

See leaders.yml.

## 11. Out-of-band notes

For roles in flux.

## 12. Open questions

- Substantive identity of Minister of Health.
