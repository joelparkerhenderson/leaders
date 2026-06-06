# spec.md — `leaders.yml`

Single source of truth for the structure, semantics, and update rules of `leaders.yml` for the Slovenian zdravstveni sistem. The YAML must conform to this spec; if they disagree, the spec wins and the YAML is fixed.

## 1. Purpose

`leaders.yml` is an engagement register of named individuals in and around the Slovenian health system. Each entry helps a reader inside Ministrstvo za zdravje (MZ), Zavod za zdravstveno zavarovanje Slovenije (ZZZS), Nacionalni inštitut za javno zdravje (NIJZ), Javna agencija RS za zdravila in medicinske pripomočke (JAZMP), or an adjacent body decide who to engage, how, and where.

The Slovenian system is Bismarckian single-payer through ZZZS, financed by mandatory contributions. The Ministry of Health sets policy. ZZZS contracts public and private providers. NIJZ is the public-health institute. JAZMP regulates medicines and devices. The University Medical Centre Ljubljana (UKC Ljubljana) and UKC Maribor are the tertiary backbone.

## 2. Scope

**In scope:** Predsednik vlade; Minister za zdravje; državni sekretarji and generalna sekretarka; Generalni direktor ZZZS; Predsednik NIJZ; Direktor JAZMP; Glavni direktor UKC Ljubljana and UKC Maribor; Predsednik Odbora za zdravstvo Državnega zbora; Predsednik Zdravniške zbornice Slovenije; Predsednica Zbornice zdravstvene in babiške nege Slovenije; Predsednik Lekarniške zbornice Slovenije.

**Out of scope:** operational staff below direktorja sektorja; vendors; historical post-holders.

## 3. Structure

```
Slovenski zdravstveni sistem — deležniki:
  - {Organisation}:
      - {Person}:
          - Title: ...
          - Stakeholder engagement notes: [...]
          - Tone advice: [...]
```

Indentation 2/6/10/14 spaces. Ordering: Vlada → MZ → ZZZS → NIJZ → JAZMP → UKC Ljubljana → UKC Maribor → Državni zbor Odbor za zdravstvo → zbornice.

## 4. Field definitions

Standard family conventions. Party affiliation using canonical Slovenian abbreviations: `SDS` (Slovenska demokratska stranka), `NSi` (Nova Slovenija), `Demokrati`, `Svoboda` (Gibanje Svoboda), `SD` (Socialni demokrati), `Levica`, `SLS`, `Vesna`. Titles in Slovenian with English glosses.

## 5. Provenance and dating

Anchor facts to year, month or exact date. The 16th government of Slovenia (Janša IV) was approved by parliament on 4 June 2026 — a centre-right coalition (SDS, NSi, Demokrati, with SLS support). Tadej Ostrc was sworn in as Minister za zdravje on 4 June 2026. Treat any MZ entry pre-dating 4 June 2026 as discontinued (the previous Svoboda-SD-Levica government with Valentina Prevolnik Rupel as Minister za zdravje through April 2025 is now superseded).

## 6. Update workflow

1. Identify the change. 2. Verify against gov.si, mz.gov.si, zzzs.si, nijz.si, jazmp.si, dz-rs.si, RTV SLO, Delo, Dnevnik, Mladina, Reporter, Sta.si, Sloveniatimes. 3. Apply minimum diff. 4. Confirm structure. 5. Re-validate cross-references.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating the new Janša government as continuous with the prior Svoboda coalition — the public-private healthcare framing is politically contested and Ostrc's mandate emphasises private-provider integration.
- Importing NHS framings unmodified — Slovenia is Bismarckian single-payer through ZZZS, with both public and private contracted providers.

## 9. Acronym glossary

- **JAZMP** — Javna agencija RS za zdravila in medicinske pripomočke (medicines and devices agency).
- **MZ** — Ministrstvo za zdravje.
- **NIJZ** — Nacionalni inštitut za javno zdravje (National Institute of Public Health).
- **UKC** — Univerzitetni klinični center (UKC Ljubljana, UKC Maribor).
- **ZZZS** — Zavod za zdravstveno zavarovanje Slovenije (statutory single payer).

## 10. Worked example

```yaml
      - Tadej Ostrc:
          - Title: Minister za zdravje (Minister of Health) (od 4. junija 2026; predlagan s strani Demokratov v koaliciji SDS-NSi-Demokrati)
          - Stakeholder engagement notes:
              - "Minister za zdravje v 16. vladi RS (Janša IV) od 4. junija 2026, ki ji je državni zbor potrdil mandat 4. junija 2026 (centro-desna koalicija SDS, NSi, Demokrati s podporo SLS); kandidata so predlagali Demokrati."
              - "Rojen 4. junija 1981; doktor stomatologije, specialist stomatološke protetike in politolog — kombinacija klinične zobozdravstvene prakse in politološkega ozadja."
              - "Mandatni prednostni cilji: učinkovita reorganizacija in digitalizacija zdravstva, krepitev primarne zdravstvene oskrbe pod enakimi pogoji za vse prebivalce, administrativna razbremenitev (zlasti družinske medicine)."
              - "Politično občutljivi del mandata: vključevanje zasebnih izvajalcev v javno mrežo — Ostrc je javno napovedal vključitev zasebnikov za izboljšanje dostopnosti, kar je sprožilo opozorila NIJZ, sindikatov in opozicije, da je potrebna premišljenost."
              - "Hook: digitalizacija zdravstva, primarno zdravstvo, javno-zasebno partnerstvo, zobozdravstvo (kot lastna stroka), čakalne dobe, EU sklad za okrevanje in odpornost (RRF) zdravstvo pristajajo."
          - Tone advice:
              - "Odpri z digitalizacijo, primarno oskrbo, čakalnimi dobami in javno-zasebnim partnerstvom — to so politične smernice nove koalicije in Ostrčevi avtorski prednostni cilji."
              - "Ne pristopaj kot da je javni sistem edina pot — vključitev zasebnikov je centralna politična linija nove vlade, vendar pazi na meje — Levica in sindikalna opozicija so glasno proti, in pretirano zasebno-orientirani okvirji bodo politično kompromitirajoči."
```

## 11. Out-of-band notes

For roles unfilled or interim.

## 12. Open questions

- Named državni sekretarji and generalna sekretarka MZ pod Ostrcem with currency verified.
- Generalni direktor ZZZS, predsednik NIJZ, direktor JAZMP with currency verified.
- Glavni direktor UKC Ljubljana and UKC Maribor with currency verified.
- Predsednik Odbora za zdravstvo Državnega zbora in the post-2026-election parlament.
- Predsednik Zdravniške zbornice Slovenije, Zbornice zdravstvene in babiške nege Slovenije, Lekarniške zbornice Slovenije with currency verified.
