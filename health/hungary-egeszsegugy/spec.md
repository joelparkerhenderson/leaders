# spec.md — `leaders.yml`

Single source of truth for the structure, semantics, and update rules of `leaders.yml` for Hungarian egészségügy. The YAML must conform to this spec; if they disagree, the spec wins and the YAML is fixed.

## 1. Purpose

`leaders.yml` is an engagement register of named individuals in and around the Hungarian health system. Each entry helps a reader inside Egészségügyi Minisztérium (or its predecessor Belügyminisztérium egészségügyi államtitkársága), NEAK / OEP (statutory insurer), OGYÉI (medicines agency), Nemzeti Népegészségügyi és Gyógyszerészeti Központ (NNGYK), an OKK hospital, or an adjacent body decide who to engage, how, and where.

The Hungarian system has been Bismarckian single-payer through the social insurer (NEAK / OEP, sometimes called Egészségbiztosítási Pénztár) under the Belügyminisztérium since 2018. The 2026 Tisza government has reportedly restored an independent Egészségügyi Minisztérium (Ministry of Health) and is reorganising the National Health Insurance Fund — the institutional landscape is in transition. The 320-some állami fenntartású hospitals (OKK system) sit under central management; the OGYÉI regulates medicines.

## 2. Scope

**In scope:** Miniszterelnök; Egészségügyi miniszter (or, in pre-2026 arrangements, Egészségügyi államtitkár inside Belügyminisztérium); politikai államtitkárok; helyettes államtitkárok; NEAK / Országos Egészségbiztosítási Pénztár főigazgatója; OGYÉI főigazgatója; NNGYK főigazgatója; nagyobb klinikák (Semmelweis Egyetem Klinikák, Debreceni Egyetem Klinikai Központ, Pécsi Tudományegyetem Klinikai Központ, Szegedi Tudományegyetem Szent-Györgyi Albert Klinikai Központ) vezetői; Magyar Orvosi Kamara (MOK) elnöke; Magyar Egészségügyi Szakdolgozói Kamara elnöke; Magyar Gyógyszerészi Kamara elnöke; Országgyűlés Népjóléti bizottsága elnöke.

**Out of scope:** operational staff below főosztályvezető; vendors; historical post-holders.

## 3. Structure

```
Magyar egészségügy érintettek:
  - {Organisation}:
      - {Person}:
          - Title: ...
          - Stakeholder engagement notes: [...]
          - Tone advice: [...]
```

Indentation 2/6/10/14 spaces. Ordering: Kormány → Egészségügyi Minisztérium → NEAK / OEP → OGYÉI → NNGYK → major klinikák → Országgyűlés Népjóléti bizottság → professional bodies.

## 4. Field definitions

Standard family conventions. Party affiliation using canonical Hungarian abbreviations: `Tisza` (Tisza Párt — Magyar Péter), `Fidesz`, `KDNP`, `DK` (Demokratikus Koalíció), `Jobbik-Konzervatívok`, `Momentum`, `MSZP`, `LMP`, `Mi Hazánk Mozgalom`, `Párbeszéd`. Titles in Hungarian with English glosses.

## 5. Provenance and dating

Anchor facts to year, month or exact date. The Tisza Párt (Magyar Péter) victory in the 2026 Országgyűlés election produced a new government in 2026. Zsolt Hegedűs was confirmed by Magyar Péter on 30 October 2025 as future Egészségügyi miniszter and took office with the Tisza government in 2026; the Egészségügyi Minisztérium was restored as an independent ministry, ending the 2018-2026 arrangement in which health was a state secretariat inside Belügyminisztérium under Takács Péter (Fidesz). Treat all Egészségügy entries pre-dating the 2026 Tisza government formation as discontinued.

## 6. Update workflow

1. Identify the change. 2. Verify against kormany.hu, the new ministry website, neak.gov.hu, ogyei.gov.hu, nngyk.gov.hu, parlament.hu, Index, Telex, HVG, Magyar Nemzet, Népszava, Mandiner, Portfolio. 3. Apply minimum diff. 4. Confirm structure. 5. Re-validate cross-references.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Importing Fidesz-era institutional framings — the Tisza government has restored the independent health ministry and is restructuring NEAK / OEP; engagement based on 2018-2026 architecture will be out of date.
- Importing NHS framings unmodified — Hungary is Bismarckian single-payer, not Beveridgean.

## 9. Acronym glossary

- **MOK** — Magyar Orvosi Kamara (Hungarian Medical Chamber).
- **NEAK** — Nemzeti Egészségbiztosítási Alapkezelő (the statutory insurer; in some 2018-2026 organograms titled OEP — Országos Egészségbiztosítási Pénztár).
- **NNGYK** — Nemzeti Népegészségügyi és Gyógyszerészeti Központ (National Centre for Public Health and Pharmacy).
- **OGYÉI** — Országos Gyógyszerészeti és Élelmezés-egészségügyi Intézet (medicines and food-health agency).
- **OKK** — országos kórházi központ (state-hospital management framework).
- **SE** — Semmelweis Egyetem (Budapest), Hungary's largest medical university.

## 10. Worked example

```yaml
      - Zsolt Hegedűs (Tisza):
          - Title: Egészségügyi miniszter (Minister of Health) (a Tisza-kormányban, 2026-tól)
          - Stakeholder engagement notes:
              - "Egészségügyi miniszter a 2026-ban hivatalba lépett Tisza-kormányban (Magyar Péter pártja, ami az Országgyűlési választáson nyerte el a többséget); Magyar Péter 2025. október 30-án jelentette be Hegedűs miniszteri kinevezését."
              - "Ortopéd sebész; 2005-2015 között az Egyesült Királyság NHS-ében dolgozott — Clinical Lead és Head of the Orthopaedic Department, North Manchester General Hospital, majd Lead Surgeon for Day Surgery, Cirencester Treatment Centre — szakmai hivatkozási rendszere brit NHS-orientált."
              - "Hazai szerepei: a '1001 orvos vesztegetés nélkül' mozgalom egyik vezetője; később a Magyar Orvosi Kamara Etikai Bizottságának elnöke — etikai-szakmai legitimációval érkezik a ressortba."
              - "Politikai államtitkára Svéd Tamás (a MOK volt főtitkára); az alapellátásért felelős államtitkár Porpáczy Krisztina (háziorvos, Tisza-egyéni képviselő); külön államtitkár van népegészségügyért és betegségmegelőzésért, járó- és fekvőbeteg-ellátásért, és digitalizációért."
              - "Hook: Tisza-kormány egészségügyi terve, a NEAK / OEP restrukturálása, alapellátás megerősítése, kórházhálózat-konszolidáció, NHS-stílusú szakmai irányítás, európai uniós helyreállítási források landolnak."
          - Tone advice:
              - "Kezdje az alapellátással, a NEAK / OEP reformjával, a brit NHS-stílusú irányítási elemekkel és az európai uniós forrásokkal — ezek Hegedűs intellektuális forrásai és a Tisza programjának keretei."
              - "Ne pitcheljen a 2018-2026-os Fidesz-éra architektúrája alapján — a Belügyminisztérium-egészségügyi-államtitkárság konstrukció megszűnt, és az új minisztérium aktívan restrukturálódik."
```

## 11. Out-of-band notes

For roles unfilled or interim.

## 12. Open questions

- Confirm Zsolt Hegedűs' exact swearing-in date and party-affiliation formalities in the Tisza government.
- Named politikai államtitkárok beyond Svéd Tamás and Porpáczy Krisztina, and helyettes államtitkárok in the new Egészségügyi Minisztérium.
- NEAK / OEP főigazgatója under the new government following its restructuring.
- OGYÉI and NNGYK főigazgatói with currency verified.
- Magyar Orvosi Kamara, Magyar Egészségügyi Szakdolgozói Kamara, Magyar Gyógyszerészi Kamara elnökei with currency verified after Svéd Tamás' move from MOK to government.
- Országgyűlés Népjóléti bizottsága elnöke and party spokespeople in the post-2026-election parliament.
- Major klinikai központok (Semmelweis Egyetem, Debreceni Egyetem, PTE, SZTE) klinikai központi főigazgatói and rektorai with currency verified.
