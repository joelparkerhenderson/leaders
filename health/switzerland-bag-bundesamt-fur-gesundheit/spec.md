# spec.md — `leaders.yml`

Single source of truth for the Swiss health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Swiss Federal Department of Home Affairs (FDHA / EDI), the Federal Office of Public Health (BAG / FOPH), Swissmedic (medicines authority), cantonal health directors via GDK / CDS, and adjacent bodies.

The Swiss system is mandatory-insurance-financed (LAMal 1996): every resident purchases statutory insurance from one of ~50 competing insurers. The 26 cantons own delivery, hospital planning and licensing; the federal level (Federal Council, EDI, BAG, Swissmedic) sets the framework and lists. GDK / CDS coordinates the cantonal Gesundheitsdirektor:innen.

## 2. Scope

In scope: Federal Council; Vorsteherin EDI (Federal Department of Home Affairs); Director BAG / FOPH; CEO Swissmedic; CEO Health Promotion Switzerland; Director Federal Office of Statistics (health); Director Federal Statistical Office; CEO GDK / CDS (Conference of Cantonal Health Directors); cantonal Gesundheitsdirektor:innen for major cantons (Zurich, Bern, Vaud, Geneva, St Gallen, Basel-Stadt, Aargau); Chair National Council Health Committee; Chair Council of States Health Committee; President FMH (Swiss Medical Association); President pharmaSuisse; President SBK / ASI (nurses).

## 3. Structure

Standard 2/6/10/14. Ordering: Federal Council → EDI → BAG → Swissmedic → GDK / CDS → 26 cantons → Federal Assembly committees → professional associations.

## 4. Field definitions

Party affiliation using canonical Swiss abbreviations: `SP / PS` (Sozialdemokratische / Socialiste), `FDP / PLR` (Freisinnig-Demokratische / Libéral-Radical), `Die Mitte` (Centre, formerly CVP+BDP), `SVP / UDC` (Schweizerische Volkspartei), `Grüne / Verts`, `glp / pvl` (Grünliberale / Vert'libéral), `EVP / PEV`. Titles in German / French / Italian with English glosses.

## 5. Provenance and dating

Elisabeth Baume-Schneider (SP, Jura) has been Federal Councillor since 1 January 2023; she heads the Federal Department of Home Affairs (EDI / FDHA, which includes BAG / Health) since 1 January 2024 — switched from FDJP/DFJP. She succeeded Alain Berset (SP) who had headed EDI 2012-2023. The federal Health Council holds direct portfolio responsibility; cantonal Gesundheitsdirektor:innen handle delivery.

## 6. Update workflow

Verify against admin.ch, bag.admin.ch, edi.admin.ch, swissmedic.ch, gdk-cds.ch, parlament.ch, NZZ, Tages-Anzeiger, Le Temps, RTS, SRF, Le Matin Dimanche.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating BAG as a single national buyer — cantons are the operational owners and statutory insurers are the purchasers.
- Importing NHS framings unmodified — Switzerland is highly competitive insurance market with strong cantonal autonomy and federalist policy-making.

## 9. Acronym glossary

- **BAG / FOPH / UFSP** — Bundesamt für Gesundheit / Federal Office of Public Health / Office fédéral de la santé publique.
- **EDI / FDHA / DFI** — Eidgenössisches Departement des Innern / Federal Department of Home Affairs / Département fédéral de l'intérieur.
- **FMH** — Verbindung der Schweizer Ärztinnen und Ärzte (Federation of Swiss Physicians).
- **GDK / CDS** — Schweizerische Konferenz der kantonalen Gesundheitsdirektorinnen und -direktoren / Conférence suisse des directrices et directeurs cantonaux de la santé.
- **LAMal / KVG** — Loi sur l'assurance-maladie / Krankenversicherungsgesetz (1996 mandatory insurance law).
- **SBK / ASI** — Schweizer Berufsverband der Pflegefachfrauen und Pflegefachmänner / Association suisse des infirmières et infirmiers.
- **Swissmedic** — Swiss Agency for Therapeutic Products.

## 10. Worked example

```yaml
      - Elisabeth Baume-Schneider (SP, Jura):
          - Title: Bundesrätin / Conseillère fédérale, Vorsteherin EDI / Cheffe DFI (Federal Councillor, head of the Federal Department of Home Affairs) (since 1 January 2024; Federal Councillor since 1 January 2023)
          - Stakeholder engagement notes:
              - "Federal Councillor since 1 January 2023; head of EDI / DFI (Federal Department of Home Affairs — including BAG / FOPH for Health) since 1 January 2024, succeeding Alain Berset (SP); previously headed FDJP / DFJP (Justice and Police) 2023; SP / PS; from canton Jura."
              - "First Romand woman to chair EDI / DFI in recent decades; previously Conseillère d'État du Jura with social-welfare and education portfolios; teacher and social worker background."
              - "Reported in blue News to have been against the Federal Council's health-insurance-premium increase decision but had to remain publicly silent due to collegiality — illustrative of Swiss collegial governance constraints on the Health portfolio."
              - "Owns federal Health policy via BAG, KVG / LAMal premium framework, Swissmedic regulation, vaccine policy, EU bilateral health-cooperation, and the federal-cantonal coordination via GDK / CDS."
              - "Hook: KVG premium reform, hospital planning federal-cantonal coordination, mental health, eHealth (DEP / EPD electronic patient record), gender-equality-in-health, climate-and-health, and EU health-bilateral agreements aterrissent."
          - Tone advice:
              - "Open with KVG premium reform, eHealth (DEP / EPD), federal-cantonal coordination and mental health — these are the federal levers and Baume-Schneider's social-democratic frame."
              - "Do not pitch as if Switzerland were federally led — the cantons are constitutionally and operationally sovereign on hospital and primary-care delivery; framings must respect federalism."
```

## 11. Out-of-band notes

For roles unfilled or in transition.

## 12. Open questions

- Named Director BAG / FOPH under Baume-Schneider with currency verified.
- CEO Swissmedic, CEO Health Promotion Switzerland with currency verified.
- CEO GDK / CDS and Gesundheitsdirektor:innen for the major cantons (ZH, BE, VD, GE, SG, BS, AG).
- Chairs of National Council and Council of States Health (and Social Security) Committees in the current 53rd-Legislatur Parliament.
- President FMH, pharmaSuisse and SBK / ASI with currency verified.
