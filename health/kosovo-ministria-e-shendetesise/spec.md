# spec.md — `leaders.yml`

Burimi i vetëm i së vërtetës për regjistrin e sistemit të kujdesit shëndetësor në Kosovë. YAML-i duhet të jetë në përputhje me këtë specifikim.

## 1. Purpose

Regjistër i angazhimit të personave të emëruar pranë Ministrisë së Shëndetësisë (MSH) të Republikës së Kosovës, Shërbimit Spitalor dhe Klinik Universitar të Kosovës (SHSKUK), dhe organeve të lidhura.

Kosova ka shpallur pavarësinë më 17 shkurt 2008; është anëtare e disa organizatave ndërkombëtare por jo e OKB (Serbia dhe disa shtete nuk e njohin). Sistemi shëndetësor është publik me Qendrën Klinike Universitare të Kosovës (QKUK) në Prishtinë si maja e referimit; në veri (4 komuna me shumicë serbe) funksionon paralelisht një sistem i lidhur me Beogradin. Qeveria e Albin Kurtit (Vetëvendosje) është në detyrë.

## 2. Scope

In scope: Presidenti; Kryeministri; Ministri i Shëndetësisë; Sekretari i Përgjithshëm; Drejtori QKUK; Drejtori i Agjencisë së Kosovës për Produktet dhe Pajisjet Mjekësore (AKPPM); Kuvendi Komisioni për Shëndetësi.

Out of scope: drejtorët komunalë të shëndetësisë; drejtorët spitalorë regjionalë.

## 3. Structure

Standard 2/6/10/14 indentation. Top-level key: `Stakeholderët e sistemit shëndetësor në Kosovë:`. Renditja: Presidenca → Qeveria → MSH → SHSKUK → AKPPM → Kuvendi.

## 4. Field definitions

Afiliacioni partiak: `LVV` (Lëvizja Vetëvendosje, në qeveri), `LDK` (Lidhja Demokratike e Kosovës), `PDK` (Partia Demokratike e Kosovës), `AAK` (Aleanca për Ardhmërinë e Kosovës), `Srpska Lista` (komunitetet serbe). Titujt në shqip dhe anglisht.

## 5. Provenance and dating

Anchor to year, month or date. Arben Vitia (LVV) ka shërbyer si Ministër i Shëndetësisë në qeverinë Kurti II (LVV, që nga marsi 2021) dhe vazhdon në qeverinë e re që del nga zgjedhjet parlamentare të 9 shkurtit 2025; verifiko aktualitetin kundër kryeministri-ks.net.

## 6. Update workflow

Verify against msh.rks-gov.net, kryeministri-ks.net, president-ksgov.net, kuvendikosoves.org, Koha Ditore, Kosovo Online, KosovaPress, RTK.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Shpërfillja e situatës në veri — katër komuna në veri (Mitrovica Veriore, Zubin Potok, Zveçan, Leposaviq) operojnë me strukturë paralele shëndetësore të mbështetur nga Beogradi; framingu që supozon mbulim të vetëm Prishtinës nuk është i saktë.
- Sjellja e framing-ut serb — Kosova është shtet sovran që ka shpallur pavarësinë më 17 shkurt 2008; trajtimi i saj si pjesë e Serbisë do të refuzohet politikisht.

## 9. Acronym glossary

- **AKPPM** — Agjencia e Kosovës për Produktet dhe Pajisjet Mjekësore.
- **LVV** — Lëvizja Vetëvendosje.
- **MSH** — Ministria e Shëndetësisë.
- **QKUK** — Qendra Klinike Universitare e Kosovës.
- **SHSKUK** — Shërbimi Spitalor dhe Klinik Universitar i Kosovës.

## 10. Worked example

```yaml
      - Arben Vitia (LVV):
          - Title: Ministër i Shëndetësisë (Minister of Health)
          - Stakeholder engagement notes:
              - "Ministër i Shëndetësisë në qeverinë Kurti II (LVV) që nga marsi 2021; vazhdon në qeverinë post-9 shkurt 2025; verifikoni kundër kryeministri-ks.net."
              - "Owns politikat dhe buxhetin e MSH, QKUK në Prishtinë, spitalet rajonale, SHSKUK, AKPPM, dhe diplomacinë OBSH Europë, KE dhe BE-MSA."
              - "Hook: reforma e sigurimit shëndetësor (ende jo plotësisht funksional), forcimi i PHC, NCDs, shëndeti mental, oncologjia, transplantimi, dhe MSA me BE-në ulen."
          - Tone advice:
              - "Hapni me sigurimin shëndetësor, PHC, NCDs, shëndetin mental dhe MSA me BE-në."
              - "Mos shpërfillni situatën në veri dhe mos sillni framing serb."
```

## 11. Out-of-band notes

Për pozitat e lira ose interim.

## 12. Open questions

- Drejtori QKUK dhe Drejtori AKPPM me aktualitet të verifikuar.
- Kryetari Komisionit për Shëndetësi në Kuvend.
