# spec.md — `leaders.yml`

Single source of truth for the Albanian health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Ministria e Shëndetësisë dhe Mbrojtjes Sociale (Ministry of Health and Social Protection), Fondi i Sigurimit të Detyrueshëm të Kujdesit Shëndetësor (FSDKSH), Agjencia Kombëtare e Barnave dhe Pajisjeve Mjekësore, Trauma Hospital and major University hospitals, and adjacent bodies.

The Albanian system has compulsory health insurance through FSDKSH; the Ministry sets policy; QSU Nënë Tereza Tirana is the main academic tertiary referral. EU accession negotiations and the Rama government's reform programme shape ongoing change.

## 2. Scope

In scope: President; PM; Minister of Health and Social Protection; Deputy Ministers; Director FSDKSH; Director National Agency of Medicines and Medical Devices; CEO QSU Nënë Tereza; CEO Trauma Hospital; District health authorities; Parliament Health Committee; Albanian Order of Physicians.

## 3. Structure

Standard. Ordering: PM → Ministry → FSDKSH → AKB → QSU Nënë Tereza → Trauma Hospital → district authorities → Parliament → Order of Physicians.

## 4. Field definitions

Party affiliation: `PS` (Socialist Party — Rama), `PD` (Democratic), `PL` (Liberal), `LSI` (Socialist Movement for Integration). Titles in Albanian / English.

## 5. Provenance and dating

Albana Koçiu served as Minister of Health and Social Protection September 2023 to September 2025, when she moved to Minister of Internal Affairs (then leaving March 2026). Identity of current Minister of Health and Social Protection in the Rama government must be verified against kryeministria.al cabinet listing.

## 6. Update workflow

Verify against shendetesia.gov.al, kryeministria.al, parlament.al, RTSH, Top Channel, Vizion+, Reporter.al, Politiko.al.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating Ministry as the only counterparty — FSDKSH is the statutory insurer.
- Importing US framings — Albania is mandatory insurance with state-dominated delivery.

## 9. Acronym glossary

- **AKBPM** — Agjencia Kombëtare e Barnave dhe Pajisjeve Mjekësore.
- **FSDKSH** — Fondi i Sigurimit të Detyrueshëm të Kujdesit Shëndetësor.
- **QSU** — Qendra Spitalore Universitare ('Nënë Tereza' Tirana).

## 10. Worked example

```yaml
      - Notes on Minister of Health and Social Protection:
          - Status: Albana Koçiu (PS) served as Minister of Health and Social Protection from September 2023 to September 2025, when she moved to the Ministry of Internal Affairs portfolio (where she served until March 2026 before leaving the government). The substantive identity of the current Minister of Health and Social Protection in the Edi Rama (PS) government for the 2026 cabinet cycle should be verified against the Council of Ministers listing at kryeministria.al and current Albanian media.
          - Implication: Engagement should be routed through the Permanent Secretariat / Deputy Minister of Health, the Director of FSDKSH, and the CEO of QSU Nënë Tereza Tirana until the substantive Minister identity is confirmed in this register.
```

## 11. Out-of-band notes

For roles unfilled or in transition.

## 12. Open questions

- Confirm identity of current Minister of Health and Social Protection in the Rama government.
- Named Deputy Ministers under the new Minister with currency verified.
- Director FSDKSH and Director AKBPM with currency verified.
- CEO QSU Nënë Tereza Tirana, CEO Trauma Hospital with currency verified.
- District-level health authority leadership with currency verified.
- Parliament Health Committee Chair with currency verified.
- President Albanian Order of Physicians with currency verified.
