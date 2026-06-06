# spec.md — `leaders.yml`

Single source of truth for the structure, semantics, and update rules of `leaders.yml` for the Cypriot health system, dominated by the General Healthcare System (ΓεΣΥ / GeSY). The YAML must conform to this spec; if they disagree, the spec wins and the YAML is fixed.

## 1. Purpose

`leaders.yml` is an engagement register of named individuals in and around the Cypriot health system. Each entry helps a reader inside the Υπουργείο Υγείας (Ministry of Health), the Οργανισμός Ασφάλισης Υγείας (HIO — the GeSY single payer), the State Health Services Organisation (OKYpY), or an adjacent body decide who to engage, how, and where.

The Cypriot system completed a structural transformation between 2019 and 2020 with the introduction of GeSY (Γενικό Σύστημα Υγείας), the country's universal single-payer scheme. HIO (Health Insurance Organisation, Οργανισμός Ασφάλισης Υγείας) administers GeSY. OKYpY (Οργανισμός Κρατικών Υπηρεσιών Υγείας) operates the public hospitals as a state-owned autonomous body, contracted by HIO on equal footing with private providers. The 2024 target was state-health autonomy; this remained a live policy file into 2026.

## 2. Scope

**In scope:** Πρόεδρος της Δημοκρατίας; Υπουργός Υγείας (Minister of Health); Γενικός Διευθυντής Υπουργείου Υγείας; Πρόεδρος Διοικητικού Συμβουλίου and Γενικός Διευθυντής of HIO; Πρόεδρος Διοικητικού Συμβουλίου and Γενικός Διευθυντής of OKYpY; Φαρμακευτικές Υπηρεσίες (Drug pharmaceutical services); Ιατρικές Υπηρεσίες και Υπηρεσίες Δημόσιας Υγείας; Διευθυντής Νοσοκομείου for the largest hospitals (Γενικό Νοσοκομείο Λευκωσίας, Μακάρειο, Λεμεσού, Λάρνακας, Πάφου, Αμμοχώστου); Πρόεδρος Παγκύπριου Ιατρικού Συλλόγου; Πρόεδρος Παγκύπριου Συλλόγου Φαρμακοποιών; Πρόεδρος Παγκύπριου Συλλόγου Νοσηλευτών; Πρόεδρος Βουλής Επιτροπή Υγείας.

**Out of scope:** operational staff below directorate level; vendors; historical post-holders.

## 3. Structure

```
Σύστημα Υγείας Κύπρου — ενδιαφερόμενα μέρη:
  - {Organisation}:
      - {Person}:
          - Title: ...
          - Stakeholder engagement notes: [...]
          - Tone advice: [...]
```

Indentation 2/6/10/14 spaces. Ordering: Πρόεδρος → Υπουργείο Υγείας → HIO (ΟΑΥ) → OKYpY → Φαρμακευτικές Υπηρεσίες → major hospitals → Βουλή Επιτροπή Υγείας → professional bodies.

## 4. Field definitions

Standard family conventions. Party affiliation in parentheses using canonical Cypriot abbreviations: `ΔΗΣΥ`, `ΑΚΕΛ`, `ΔΗΚΟ`, `ΕΛΑΜ`, `ΕΔΕΚ`, `ΟΙΚΟΛΟΓΟΙ`, `ΔΗΠΑ`, `Άλμα` (independent grouping). Greek-letter party abbreviations are the canonical form.

Titles in Greek with English glosses where useful.

## 5. Provenance and dating

Anchor facts to year, month or exact date. President Nikos Christodoulides was elected in February 2023 (independent backed by ΔΗΣΥ et al). His cabinet has had two major reshuffles. As of June 2026, Neophytos Charalambides serves as Minister of Health (Υπουργός Υγείας), having taken over from Michael Damianos on 8 December 2025 when Damianos moved to the Energy, Commerce and Industry portfolio. Treat any Υπουργείο Υγείας entry pre-dating 8 December 2025 as warranting re-verification.

## 6. Update workflow

1. Identify the change. 2. Verify against presidency.gov.cy, moh.gov.cy, gesy.org.cy, gov.cy, Cyprus Mail, Phileleftheros, Politis, Stockwatch, CBN. 3. Apply minimum diff. 4. Confirm structure. 5. Re-validate cross-references.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating GeSY as a Ministry programme — HIO is statutorily autonomous and contracts on equal footing with private providers.
- Importing NHS framings unmodified — GeSY is a single-payer commissioning model with patient choice across public and private providers, not a state-delivered service.

## 9. Acronym glossary

- **GeSY / ΓεΣΥ** — Γενικό Σύστημα Υγείας (General Healthcare System; the universal single-payer scheme).
- **HIO / ΟΑΥ** — Health Insurance Organisation / Οργανισμός Ασφάλισης Υγείας (the GeSY single payer).
- **OKYpY / ΟΚΥπΥ** — Οργανισμός Κρατικών Υπηρεσιών Υγείας (State Health Services Organisation, the autonomous public-hospital operator from 2019).
- **PIS** — Παγκύπριος Ιατρικός Σύλλογος (Pancyprian Medical Association).

## 10. Worked example

```yaml
      - Neophytos Charalambides:
          - Title: Υπουργός Υγείας (Minister of Health) (από 8 Δεκεμβρίου 2025)
          - Stakeholder engagement notes:
              - "Υπουργός Υγείας από 8 Δεκεμβρίου 2025 στην κυβέρνηση του Προέδρου Νίκου Χριστοδουλίδη, διαδεχόμενος τον Michael Damianos που μετακινήθηκε στο Υπουργείο Ενέργειας, Εμπορίου και Βιομηχανίας."
              - "Αναλαμβάνει σε φάση όπου το ΓεΣΥ ωριμάζει: ολοκλήρωση αυτονόμησης ΟΚΥπΥ, διαπραγματεύσεις με ιδιώτες παρόχους, διαχείριση συνταγογράφησης και προϋπολογισμός €1,5 δισ. για 2026."
              - "Hook: ΟΚΥπΥ αυτονομία, ΓεΣΥ διακυβέρνηση, χρόνια νοσήματα, ψυχική υγεία, εξειδικευμένη περίθαλψη και ευρωπαϊκή χρηματοδότηση Recovery and Resilience πιάνουν τόπο."
          - Tone advice:
              - "Εστίαση σε αυτονόμηση ΟΚΥπΥ, διακυβέρνηση ΓεΣΥ και χρόνια νοσήματα — αυτές είναι οι ώριμες πτυχές του μεταρρυθμιστικού κύκλου του ΓεΣΥ."
              - "Μην προωθείτε πλαίσια που υποτιμούν τον δημόσιο τομέα — η αυτονόμηση ΟΚΥπΥ είναι κεντρική προτεραιότητα, και ιδιωτικά-κεντρικά πλαίσια θα απορριφθούν."
```

## 11. Out-of-band notes

For roles unfilled or interim.

## 12. Open questions

- Verify Neophytos Charalambides' exact policy line and biographical details to within six months of source publication.
- Named Γενικός Διευθυντής of the Ministry of Health under Charalambides.
- Named Πρόεδρος ΔΣ and Γενικός Διευθυντής of HIO (ΟΑΥ) with currency verified.
- Named Πρόεδρος ΔΣ and Γενικός Διευθυντής of OKYpY through the continuing state-health autonomy reform.
- Διευθυντές of the major state hospitals (Νοσοκομείο Λευκωσίας, Μακάρειο, Νοσοκομείο Λεμεσού, Λάρνακας, Πάφου).
- Πρόεδρος Βουλής Επιτροπή Υγείας in the current parliamentary term (13η Βουλή).
- Πρόεδρος Παγκύπριου Ιατρικού Συλλόγου, Παγκύπριου Συλλόγου Φαρμακοποιών, and Παγκύπριου Συλλόγου Νοσηλευτών with currency verified.
