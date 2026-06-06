# spec.md — `leaders.yml`

Jedinstveni izvor istine za registar zdravstvenog sistema Crne Gore. YAML mora biti u skladu sa ovom specifikacijom.

## 1. Purpose

Registar angažovanja imenovanih lica u Ministarstvu zdravlja Crne Gore, Fondu za zdravstveno osiguranje (FZO), Institutu za javno zdravlje i pridruženim tijelima.

Crna Gora je parlamentarna republika, članica NATO (od 2017) i kandidat za članstvo u EU (najnapredniji u regionu — pregovori u završnoj fazi). Zdravstveni sistem zasnovan na obaveznom zdravstvenom osiguranju preko FZO. Vlada Milojka Spajića (PES — Pokret Evropa Sad!) je u funkciji od oktobra 2023.

## 2. Scope

In scope: Predsjednik; Predsjednik Vlade; Ministar zdravlja; Direktor FZO; Direktor Kliničkog centra Crne Gore; Direktor Instituta za javno zdravlje; Skupština Odbor za zdravstvo, rad i socijalno staranje.

Out of scope: opštinski direktori; direktori regionalnih bolnica.

## 3. Structure

Standard 2/6/10/14 indentation. Top-level key: `Učesnici crnogorskog zdravstvenog sistema:`. Redoslijed: Predsjedništvo → Vlada → Ministarstvo → FZO → IJZ → Skupština.

## 4. Field definitions

Stranačka pripadnost: `PES` (Pokret Evropa Sad!, vladajuća), `DPS` (Demokratska partija socijalista), `Demokrate`, `URA`, `SNP`, `Bošnjačka stranka`. Naslovi na crnogorskom i engleskom.

## 5. Provenance and dating

Anchor to year, month or date. Vojislav Šimun (PES) bio je Ministar zdravlja u Vladi Spajića od oktobra 2023; provjerite tekuće stanje protiv gov.me; izbori za predsjednika 2023. su pobijedili Jakov Milatović (PES) kao Predsjednik.

## 6. Update workflow

Verify against gov.me, predsjednik.gov.me, skupstina.me, MINA (Montenegro Independent News Agency), Vijesti, Pobjeda, Dan.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Mješanje sa Srbijom — Crna Gora je suverena država od 3. juna 2006, sa sopstvenom institucionalnom arhitekturom, i članica je NATO; takvi framingovi neće biti politički prihvatljivi.
- Ignorisanje EU pregovaračke faze — Crna Gora je najnapredniji kandidat u regionu i zdravstveni acquis je u aktivnom usaglašavanju.

## 9. Acronym glossary

- **DPS** — Demokratska partija socijalista.
- **FZO** — Fond za zdravstveno osiguranje.
- **IJZ** — Institut za javno zdravlje.
- **PES** — Pokret Evropa Sad!.

## 10. Worked example

```yaml
      - Vojislav Šimun (PES):
          - Title: Ministar zdravlja (Minister of Health)
          - Stakeholder engagement notes:
              - "Ministar zdravlja u Vladi Milojka Spajića (PES) od oktobra 2023; ljekar; provjerite protiv gov.me."
              - "Owns politiku i budžet Ministarstva, Klinički centar Crne Gore u Podgorici, opšte i specijalne bolnice u Beranama, Cetinju, Nikšiću, Pljevljima, FZO, IJZ, i diplomatiju SZO Europa, EU-pregovori i NATO."
              - "Hook: EU acquis harmonizacija, FZO reforma, NCDs, mentalno zdravlje, onkologija, digitalizacija, i kadrovska politika slijeću."
          - Tone advice:
              - "Otvorite sa EU-acquis, FZO reformom, NCDs, mentalnim zdravljem i kadrovima."
              - "Ne mješajte sa Srbijom i prepoznajte status NATO-EU-pristupanje."
```

## 11. Out-of-band notes

Za vakantne ili privremene pozicije.

## 12. Open questions

- Direktor FZO i Direktor KCCG sa verifikovanom titularnošću.
- Direktor IJZ.
- Predsjednik Odbora za zdravstvo u Skupštini.
