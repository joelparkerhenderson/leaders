# spec.md — `leaders.yml`

Single source of truth for the structure, semantics, and update rules of `leaders.yml` for the Italian Servizio Sanitario Nazionale (SSN). The YAML must conform to this spec; if they disagree, the spec wins and the YAML is fixed.

## 1. Purpose

`leaders.yml` is an engagement register of named individuals in and around the Italian SSN. Each entry helps a reader inside the Ministero della Salute, AGENAS, AIFA, Istituto Superiore di Sanità (ISS), a Regione, a Direzione Generale Sanità, or an Azienda Sanitaria Locale (ASL) decide who to engage, how, and where.

The SSN was established by Legge 833/1978 as a Beveridgean tax-funded universal system. Italy operates a regionalised governance model: the State sets framework legislation and Livelli Essenziali di Assistenza (LEA); the 20 regions (and 2 autonomous provinces) own delivery through their Assessorati alla Sanità, Aziende Sanitarie Locali (ASL) and Aziende Ospedaliere (AO). The Conferenza Stato-Regioni coordinates. AIFA (Agenzia Italiana del Farmaco) regulates medicines; AGENAS coordinates regional service planning; ISS leads public health and biomedical research.

## 2. Scope

**In scope:** Presidente del Consiglio dei Ministri; Ministro della Salute and Viceministro / Sottosegretari; Capo di Gabinetto del Ministro and Direttori Generali del Ministero della Salute; Direttore Generale AGENAS; Presidente AIFA and Direttore Generale AIFA; Presidente ISS; Direttore Generale Istituto Nazionale per le Malattie Infettive Spallanzani; Assessori alla Sanità delle 21 regioni (Lombardia, Lazio, Campania, Sicilia, Veneto, Emilia-Romagna, Piemonte, Puglia, Toscana, Calabria, Sardegna, Liguria, Marche, Abruzzo, Friuli-Venezia Giulia, Trentino-Alto Adige (Bolzano, Trento), Umbria, Basilicata, Molise, Valle d'Aosta); Presidente Commissione Igiene e Sanità del Senato; Presidente Commissione Affari Sociali della Camera; Presidente Federazione Nazionale degli Ordini dei Medici Chirurghi e degli Odontoiatri (FNOMCeO); Presidente Federazione Nazionale degli Ordini delle Professioni Infermieristiche (FNOPI); Presidente Federazione degli Ordini dei Farmacisti Italiani (FOFI); Presidente FIASO (Federazione Italiana Aziende Sanitarie e Ospedaliere).

**Out of scope:** operational staff below dirigente di seconda fascia; vendors; historical post-holders.

## 3. Structure

```
Servizio Sanitario Nazionale italiano — stakeholder:
  - {Organisation}:
      - {Person}:
          - Title: ...
          - Stakeholder engagement notes: [...]
          - Tone advice: [...]
```

Indentation 2/6/10/14 spaces. Ordering: Governo → Ministero della Salute → AGENAS → AIFA → ISS → 21 Regioni (Assessori alla Sanità) → Camera e Senato Commissioni → professional federations (FNOMCeO, FNOPI, FOFI) → FIASO.

## 4. Field definitions

Standard family conventions. Party affiliation using canonical Italian abbreviations: `FdI` (Fratelli d'Italia), `Lega`, `FI` (Forza Italia), `PD` (Partito Democratico), `M5S` (Movimento 5 Stelle), `Italia Viva`, `Azione`, `+Europa`, `AVS` (Alleanza Verdi-Sinistra), `Noi Moderati`, `Sudtiroler Volkspartei` (SVP). Titles in Italian with English glosses.

## 5. Provenance and dating

Anchor facts to year, month or exact date. The Meloni government (FdI-Lega-FI-Noi Moderati) has been in office since 22 October 2022 with Orazio Schillaci as Ministro della Salute throughout. Treat regional Assessori entries as warranting re-verification after each regionale election cycle.

## 6. Update workflow

1. Identify the change. 2. Verify against governo.it, salute.gov.it, agenas.gov.it, aifa.gov.it, iss.it, senato.it, camera.it, regioni.it, Corriere della Sera, La Repubblica, Il Sole 24 Ore, Quotidiano Sanità, Sanità Informazione. 3. Apply minimum diff. 4. Confirm structure. 5. Re-validate cross-references.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating the SSN as a single national service — the 21 regions own delivery; engagement strategies must include the regional dimension.
- Importing NHS framings without regional adaptation — Italy is constitutionally regionalised in health since 2001.

## 9. Acronym glossary

- **AGENAS** — Agenzia Nazionale per i Servizi Sanitari Regionali.
- **AIFA** — Agenzia Italiana del Farmaco.
- **AO** — Azienda Ospedaliera (independent hospital trust).
- **ASL** — Azienda Sanitaria Locale (local health authority).
- **Conferenza Stato-Regioni** — formal coordination forum between national government and regions.
- **DRG** — Diagnosis-Related Groups (Italian variant for SSN hospital payment).
- **FIASO** — Federazione Italiana Aziende Sanitarie e Ospedaliere.
- **FNOMCeO** — Federazione Nazionale degli Ordini dei Medici Chirurghi e degli Odontoiatri.
- **FNOPI** — Federazione Nazionale degli Ordini delle Professioni Infermieristiche.
- **FOFI** — Federazione degli Ordini dei Farmacisti Italiani.
- **IRCCS** — Istituto di Ricovero e Cura a Carattere Scientifico (research-and-care hospital).
- **ISS** — Istituto Superiore di Sanità.
- **LEA** — Livelli Essenziali di Assistenza (essential levels of care).
- **MMG** — Medico di Medicina Generale (GP).
- **PNRR** — Piano Nazionale di Ripresa e Resilienza (national recovery and resilience plan; large health investment envelope).
- **SSN** — Servizio Sanitario Nazionale.

## 10. Worked example

```yaml
      - Orazio Schillaci:
          - Title: Ministro della Salute (Minister of Health) (dal 22 ottobre 2022)
          - Stakeholder engagement notes:
              - "Ministro della Salute nel governo Meloni dal 22 ottobre 2022 — incarico tecnico-accademico, non parlamentare; Professore ordinario di Medicina Nucleare all'Università di Roma Tor Vergata, di cui è stato Rettore dal 2019 fino alla nomina ministeriale."
              - "Nato il 27 aprile 1966 a Roma con origini calabresi; precedente Direttore Dipartimento di Biomedicina e Prevenzione dell'Università Tor Vergata e Preside della Facoltà di Medicina e Chirurgia."
              - "Owns l'attuazione del PNRR Salute, il rinnovo dei contratti di lavoro del personale sanitario, la riforma della medicina generale e del territorio (Case di Comunità), la coordinazione con la Conferenza Stato-Regioni, e la rappresentanza italiana in sede UE (Consiglio EPSCO, EMA Management Board)."
              - "Pubblicamente posizionato su una 'svolta verso una sanità più predittiva e personalizzata' — linea di mandato che valorizza la medicina di precisione, la genomica e l'intelligenza artificiale clinica."
              - "Hook: PNRR Salute, Case di Comunità, medicina di precisione, peste suina africana e biosicurezza, AIFA reform, formazione e contratti del personale, IRCCS aterrissont; pitch che ignorano il livello regionale non aterrissont."
          - Tone advice:
              - "Aprire con PNRR Salute, Case di Comunità, medicina di precisione e contratti del personale — sono le linee di mandato e l'orizzonte professionale di Schillaci (medico-accademico)."
              - "Non proporre framing che bypassano le Regioni — Schillaci coordina la Conferenza Stato-Regioni e qualsiasi proposta centralizzata sarà rinviata ad Assessori regionali."
```

## 11. Out-of-band notes

For roles unfilled or interim.

## 12. Open questions

- Named Viceministro and Sottosegretari della Salute under Meloni with currency verified.
- Named Capo di Gabinetto and Direttori Generali del Ministero della Salute (Programmazione Sanitaria, Prevenzione, Personale, Digitalizzazione) with currency verified.
- Direttore Generale AGENAS, Presidente AIFA, Direttore Generale AIFA, and Presidente ISS with currency verified.
- Direttore Generale Istituto Nazionale per le Malattie Infettive Spallanzani.
- Assessori alla Sanità di tutte e 21 le regioni e province autonome — particolare priorità a Lombardia (Bertolaso continuation?), Lazio, Campania, Sicilia, Veneto, Emilia-Romagna, Piemonte, Puglia, Toscana, Calabria, Sardegna.
- Presidenti delle Commissioni Igiene e Sanità del Senato e Affari Sociali della Camera nella XIX legislatura.
- Presidenti FNOMCeO, FNOPI, FOFI, FIASO with currency verified.
