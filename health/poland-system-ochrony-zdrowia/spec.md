# spec.md — `leaders.yml`

Single source of truth for the structure, semantics, and update rules of `leaders.yml` for the Polish system ochrony zdrowia. The YAML must conform to this spec; if they disagree, the spec wins and the YAML is fixed.

## 1. Purpose

`leaders.yml` is an engagement register of named individuals in and around the Polish health system. Each entry helps a reader inside Ministerstwo Zdrowia (MZ), Narodowy Fundusz Zdrowia (NFZ), Agencja Oceny Technologii Medycznych i Taryfikacji (AOTMiT), Główny Inspektorat Sanitarny (GIS), Urząd Rejestracji Produktów Leczniczych (URPL), or an adjacent body decide who to engage, how, and where.

The Polish system is Bismarckian single-payer through NFZ, which contracts hospitals and primary-care providers. MZ sets policy; NFZ is the universal buyer. AOTMiT performs HTA and tariff-setting. GIS handles public health surveillance and sanitary supervision. The 16 voivodeships own a large share of hospitals through marszałek województwa, while university hospitals sit under MZ. Tusk's coalition government has been in office since 13 December 2023 (KO, Trzecia Droga (PSL + Polska 2050), Lewica).

## 2. Scope

**In scope:** Prezes Rady Ministrów; Minister Zdrowia; sekretarze and podsekretarze stanu; Dyrektor Generalny MZ; Prezes NFZ; Prezes AOTMiT; Główny Inspektor Sanitarny; Prezes URPL; Konsultanci krajowi (in major specialties); Rektorzy uniwersytetów medycznych and dyrektorzy uniwersyteckich szpitali klinicznych for the largest centres (WUM Warszawa, GUMed Gdańsk, UM Poznań, UM Łódź, UJ CM Kraków, ŚUM Katowice, UM Wrocław); Przewodniczący Sejmowej Komisji Zdrowia; Przewodniczący Naczelnej Rady Lekarskiej; Przewodnicząca Naczelnej Rady Pielęgniarek i Położnych; Prezes Naczelnej Izby Aptekarskiej.

**Out of scope:** operational staff below dyrektor departamentu; vendors; historical post-holders.

## 3. Structure

```
Polski system ochrony zdrowia — interesariusze:
  - {Organisation}:
      - {Person}:
          - Title: ...
          - Stakeholder engagement notes: [...]
          - Tone advice: [...]
```

Indentation 2/6/10/14 spaces. Ordering: Rząd → MZ → NFZ → AOTMiT → GIS → URPL → uczelnie medyczne i szpitale kliniczne → Sejmowa Komisja Zdrowia → samorządy zawodowe.

## 4. Field definitions

Standard family conventions. Party affiliation using canonical Polish abbreviations: `KO` (Koalicja Obywatelska), `PSL`, `Polska 2050`, `Lewica` (Nowa Lewica), `PiS` (Prawo i Sprawiedliwość), `Konfederacja`, `Razem`. Titles in Polish with English glosses.

## 5. Provenance and dating

Anchor facts to year, month or exact date. The Tusk coalition government (KO + Trzecia Droga + Lewica) was sworn in 13 December 2023. Jolanta Sobierańska-Grenda was confirmed as Minister Zdrowia on 24 July 2025 in a Tusk reshuffle replacing Izabela Leszczyna. Treat any MZ entry pre-dating 24 July 2025 as warranting re-verification.

## 6. Update workflow

1. Identify the change. 2. Verify against premier.gov.pl, gov.pl/web/zdrowie, nfz.gov.pl, aotmit.gov.pl, gis.gov.pl, urpl.gov.pl, sejm.gov.pl, Rzeczpospolita, Gazeta Wyborcza, Puls Medycyny, Medexpress, Termedia, Onet, OKO.press. 3. Apply minimum diff. 4. Confirm structure. 5. Re-validate cross-references.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Importing NHS framings unmodified — Poland is Bismarckian single-payer with strong regional ownership of hospital infrastructure.
- Ignoring voivodeship marszałek dimension — many hospital decisions are political-regional, not central-MZ.

## 9. Acronym glossary

- **AOTMiT** — Agencja Oceny Technologii Medycznych i Taryfikacji (HTA and tariff agency).
- **GIS** — Główny Inspektorat Sanitarny.
- **MZ** — Ministerstwo Zdrowia.
- **NFZ** — Narodowy Fundusz Zdrowia (statutory single payer).
- **URPL** — Urząd Rejestracji Produktów Leczniczych, Wyrobów Medycznych i Produktów Biobójczych (Polish medicines and devices agency).

## 10. Worked example

```yaml
      - Jolanta Sobierańska-Grenda:
          - Title: Minister Zdrowia (Minister of Health) (od 24 lipca 2025)
          - Stakeholder engagement notes:
              - "Minister Zdrowia od 24 lipca 2025 w rządzie Donalda Tuska (koalicja KO + Trzecia Droga + Lewica), po rekonstrukcji rządu w której odeszła Izabela Leszczyna; profil menedżerski."
              - "Od 2017 r. prezes zarządu Szpitali Pomorskich w Gdańsku; doktor nauk społecznych w dyscyplinie ekonomia i finanse; MBA dla kadry medycznej; uznawana za jedną z najbardziej profesjonalnych osób zarządzających w polskim systemie ochrony zdrowia."
              - "Owns kontrakty NFZ ze szpitalami i POZ, planowanie sieci szpitali (sieć szpitali), reformę finansowania ochrony zdrowia, KPO Zdrowie, oraz dialog z samorządami zawodowymi (Naczelna Rada Lekarska, Naczelna Rada Pielęgniarek i Położnych)."
              - "Mandat oparty na 'odpolitycznieniu' resortu i wzmocnieniu menedżerskiego zarządzania — kontrast z politycznie eksponowaną prowadzą Leszczyny."
              - "Hook: sieć szpitali, NFZ kontraktowanie, KPO Zdrowie, deficyty placówek, kadry medyczne, lista refundacyjna, e-zdrowie (eRecepta, IKP) lądują; pitche centralistyczne ignorujące samorząd wojewódzki nie lądują."
          - Tone advice:
              - "Otwierać siecią szpitali, NFZ, KPO Zdrowie i kadrami — to filary mandatu i jej menedżerski język."
              - "Nie pitchować polityki politycznym wymiarze — Sobierańska-Grenda została powołana jako menedżer, nie jako polityk; framingi polityczne będą filtrowane."
```

## 11. Out-of-band notes

For roles unfilled or interim.

## 12. Open questions

- Named sekretarze and podsekretarze stanu in Ministerstwo Zdrowia pod Sobierańską-Grendą with currency verified.
- Prezes NFZ following the 24 lipca 2025 reshuffle.
- Prezes AOTMiT, Główny Inspektor Sanitarny, Prezes URPL with currency verified.
- Przewodniczący Sejmowej Komisji Zdrowia in the current X kadencja Sejmu.
- Przewodniczący Naczelnej Rady Lekarskiej, Naczelnej Rady Pielęgniarek i Położnych, Naczelnej Izby Aptekarskiej with currency verified.
- Rektorzy uniwersytetów medycznych i dyrektorzy uniwersyteckich szpitali klinicznych (WUM, GUMed, UMP, UMŁ, UJ CM, ŚUM, UMW) with currency verified.
- Konsultanci krajowi in major specialties — kardiologia, onkologia, neurologia, psychiatria, anestezjologia, medycyna rodzinna.
