# spec.md — `leaders.yml`

Single source of truth for the structure, semantics, and update rules of `leaders.yml` for the Belgian gezondheidszorg / soins de santé. The YAML must conform to this spec; if they disagree, the spec wins and the YAML is fixed.

## 1. Purpose

`leaders.yml` is an engagement register of named individuals in and around the Belgian health system. Each entry helps a reader inside the federal FOD Volksgezondheid / SPF Santé publique, the RIZIV / INAMI, the FAGG / AFMPS, Sciensano, the Gemeenschappen / Communautés health competences, a hospital network, or an adjacent body decide:

1. Who to engage for a given topic.
2. How to engage them — the angle that lands and the angle that fails.
3. Where to engage them — which public channels they use.

Belgium has one of the most institutionally complex health systems in Europe. Federal competence covers health insurance (RIZIV/INAMI), medicines (FAGG/AFMPS), the hospital legal framework, and public health surveillance (Sciensano). Health policy is partly devolved to the Vlaamse Gemeenschap, the Fédération Wallonie-Bruxelles, the Région wallonne (AVIQ), the Cocof / Cocom in Brussels, and the Deutschsprachige Gemeinschaft — covering prevention, ambulatory health, elder care, mental health and primary care. The 2014 Sixth State Reform shifted significant health-policy competence to the Gemeenschappen / Communautés.

## 2. Scope

**In scope:** Federal level — Premier; Minister van Sociale Zaken en Volksgezondheid / Ministre des Affaires sociales et de la Santé publique; Voorzitter / Président des Comités van Beheer/de Gestion of RIZIV/INAMI and FAGG/AFMPS; Sciensano (Directeur-Generaal); FOD Volksgezondheid (Voorzitter Directiecomité). Gemeenschappen / Communautés — Vlaams Minister van Welzijn, Volksgezondheid en Gezin; Ministre wallonne de la Santé and AVIQ Administrateur général; Ministre bruxelloise de la Santé and Iriscare; Deutschsprachige Gemeinschaft Minister für Gesundheit. Federal Parliament: Voorzitter Kamercommissie Volksgezondheid. Professional bodies: Orde der Artsen / Ordre des Médecins; Belgische Vereniging van Artsensyndicaten (BVAS/ABSyM); BeNe Allmed; Domus Medica; SSMG; Algemene Pharmaceutische Bond (APB).

**Out of scope:** operational staff below directieniveau; vendors; historical post-holders.

## 3. Structure

```
Belgisch gezondheidssysteem stakeholders / Stakeholders du système de santé belge:
  - {Organisation}:
      - {Person}:
          - Title: ...
          - {optional contact fields}
          - Stakeholder engagement notes: [...]
          - Tone advice: [...]
```

Indentation 2/6/10/14 spaces. Ordering: Federale regering → FOD Volksgezondheid → RIZIV/INAMI → FAGG/AFMPS → Sciensano → Vlaamse Regering → Fédération Wallonie-Bruxelles + Région wallonne (AVIQ) → Région de Bruxelles (Iriscare) → Deutschsprachige Gemeinschaft → Parlement → professional bodies.

## 4. Field definitions

**Organisation name** — official Dutch and/or French name with English in parentheses where useful (e.g. `Federale Overheidsdienst Volksgezondheid / Service public fédéral Santé publique (FOD VG / SPF Santé)`).

**Person name** — academic titles `Dr.`, `Prof.`, `Pr` where used publicly. Party affiliation in parentheses using canonical Belgian abbreviations: Flemish-side `N-VA`, `Vooruit`, `CD&V`, `Open Vld`, `Groen`, `Vlaams Belang`; Francophone `MR`, `PS`, `Les Engagés`, `Ecolo`, `PTB-PVDA`, `DéFI`.

**Title** — Dutch or French (or both for federal officials), with English gloss where not obvious. Status flags: `ad interim`, `(sinds {datum})`, `(actualité à vérifier)`.

**Contact fields** (optional): `LinkedIn`, `X`, `Bluesky`, `Mastodon`, `Website`, `GitHub`, `Email`.

**Stakeholder engagement notes** — 3-7 bullets. **Tone advice** — exactly 2.

## 5. Provenance and dating

Anchor facts to year, month or exact date. The De Wever federal coalition was sworn in 3 February 2025 (N-VA, MR, CD&V, Vooruit, Les Engagés — the Arizona coalition) after the June 2024 election. Frank Vandenbroucke (Vooruit) is Vice-Prime Minister and Minister of Social Affairs and Public Health. Treat any federal-government entry pre-dating 3 February 2025 as warranting re-verification.

## 6. Update workflow

1. Identify the change. 2. Verify against premier.be, vandenbroucke.belgium.be, health.belgium.be, riziv.fgov.be, fagg-afmps.be, sciensano.be, Vlaamse Regering, gouvernement-wallonie.be, parlament.brussels, De Standaard, Le Soir, De Tijd, L'Echo. 3. Apply minimum diff. 4. Confirm structure. 5. Re-validate cross-references.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating Belgium as a unitary system — health competence is split between federal and Gemeenschappen/Communautés since 2014.
- Importing NHS or French framings unmodified — Belgium has Bismarckian insurance with strong professional self-administration (mutualiteiten / mutualités) and devolved prevention/ambulatory care.

## 9. Acronym glossary

- **AFMPS** — Agence fédérale des médicaments et des produits de santé (French name of FAGG).
- **APB** — Algemene Pharmaceutische Bond (federal pharmacists' association).
- **AVIQ** — Agence pour une Vie de Qualité (Walloon health and disability agency).
- **BVAS / ABSyM** — Belgische Vereniging van Artsensyndicaten / Association Belge des Syndicats Médicaux.
- **Cocof / Cocom / GGC** — French Community / Common Community Commission (Brussels-region competences).
- **FAGG** — Federaal Agentschap voor Geneesmiddelen en Gezondheidsproducten (Belgian medicines agency).
- **FOD VG** — Federale Overheidsdienst Volksgezondheid, Veiligheid van de Voedselketen en Leefmilieu (federal health ministry).
- **Iriscare** — Brussels-bicommunal social-protection agency (covers elder care, disability, family allowances, certain ambulatory health).
- **KCE** — Federaal Kenniscentrum voor de Gezondheidszorg / Centre fédéral d'expertise (Belgian HTA body).
- **NIC / INAMI** — Nationaal Intermutualistisch College / Institut national d'assurance maladie-invalidité (statutory health insurer; common abbreviation RIZIV/INAMI).
- **Mutualiteiten / Mutualités** — sickness funds; seven nationally — CM/MC, MLOZ/UNMS, Bond Moyson/Solidaris, Liberale, Neutrale, etc.
- **RIZIV** — Rijksinstituut voor Ziekte- en Invaliditeitsverzekering (Dutch name of INAMI).
- **Sciensano** — Belgian public-health and biomedical research institute (created 2018 by merging WIV-ISP and CODA-CERVA).
- **Sixth State Reform** — 2014 constitutional reform devolving major health competences to Gemeenschappen / Communautés.
- **VAZG** — Vlaams Agentschap Zorg en Gezondheid; now integrated as Departement Zorg under the Vlaamse Regering.

## 10. Worked example

```yaml
      - Frank Vandenbroucke (Vooruit):
          - Title: Vice-eersteminister en Minister van Sociale Zaken en Volksgezondheid, belast met Armoedebestrijding (Vice-PM and Minister of Social Affairs and Public Health, in charge of Poverty Reduction) (sinds 3 februari 2025)
          - Stakeholder engagement notes:
              - "Vice-eersteminister en Minister van Sociale Zaken en Volksgezondheid in de regering-De Wever (N-VA, MR, CD&V, Vooruit, Les Engagés — Arizona-coalitie) sinds 3 februari 2025; Vooruit; aanhoudende federale aanwezigheid op het ressort na de Vivaldi-periode 2020-2024."
              - "Owns het federale gezondheidsbudget (€41,3 mld voor 2026, met €1,57 mld nieuwe middelen), de RIZIV-/INAMI-conventies met artsen en ziekenfondsen, de FAGG-koers en de federale beleidsnota Volksgezondheid 2026 als instrument."
              - "Per 1 januari 2026: alle opnamedagen in een psychiatrisch ziekenhuis tellen volledig mee voor de maximumfactuur — concreet voorbeeld van zijn distributieve agenda inzake mentale gezondheid en armoedebestrijding."
              - "Hook: ziekenhuishervorming, conventies en honoraria, geestelijke gezondheidszorg, federaal-deelstatelijke coördinatie, medicijnenbeleid landen; pitches die de devolutie sinds 2014 negeren landen niet."
          - Tone advice:
              - "Open met geestelijke gezondheidszorg, ziekenhuishervorming, conventies en armoedebestrijding — dit zijn zijn Vooruit-lijnen en zijn institutionele voorkeur voor distributie en hervorming."
              - "Pitch niet als ware er één Belgische zorgcontactpersoon — Gemeenschappen/Communautés bezitten preventie, ambulant en ouderenzorg sinds 2014; centraliserende framings worden teruggespeeld."
```

## 11. Out-of-band notes

For roles unfilled or interim.

## 12. Open questions

- Named Voorzitter Directiecomité of FOD Volksgezondheid, Administrateur-Generaal RIZIV/INAMI, and Administrateur-Generaal FAGG/AFMPS with currency verified.
- Named Directeur-Generaal Sciensano with currency verified.
- Vlaams Minister van Welzijn, Volksgezondheid en Gezin in the Diependaele Vlaamse Regering and Departementshoofd Departement Zorg.
- Ministre wallonne de la Santé under the Adrien Dolimont MR-Les Engagés regional government and Administrateur général AVIQ.
- Ministres bruxellois de la Santé (Cocom and Cocof) and Iriscare leadership.
- Minister für Gesundheit der Deutschsprachigen Gemeinschaft.
- Voorzitter Kamercommissie Volksgezondheid in the 56e legislatuur and party spokespeople.
- Voorzitter Orde der Artsen / Président Ordre des Médecins, BVAS/ABSyM, Domus Medica, SSMG, APB with currency verified.
