# spec.md — `leaders.yml`

Single source of truth for the Bruneian health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Brunei Darussalam Ministry of Health (MoH) and adjacent bodies.

Brunei is an absolute monarchy under Sultan Hassanal Bolkiah (since 1967); the Sultan is also Prime Minister, Defence Minister, Foreign Affairs Minister and Finance Minister. The health system is publicly funded, free at point of use for Bruneian citizens, with subsidised access for permanent residents and employed expatriates. RIPAS Hospital (Raja Isteri Pengiran Anak Saleha) in Bandar Seri Begawan is the apex facility.

## 2. Scope

In scope: Sultan (Head of State and Head of Government); Minister of Health; Permanent Secretary (Health); Director-General Medical Services; CEO RIPAS Hospital; Legislative Council (Majlis Mesyuarat Negara) Health-related Committee.

Out of scope: district health officers.

## 3. Structure

Standard 2/6/10/14 indentation. Top-level key: `Bruneian health stakeholders:`. Ordering: Sultan and Cabinet → MoH → RIPAS → Legislative Council.

## 4. Field definitions

Brunei is a non-party absolute monarchy; no party affiliation. Titles in English with Malay honorifics: `Yang Berhormat Dato Seri Setia Dr. Haji ...` (the formal style). Use the shortened form `YB Dato Seri Setia` or `Hon.` in operational contexts.

## 5. Provenance and dating

Anchor to year, month or date. YB Dato Seri Setia Dr. Haji Md Isham bin Haji Jaafar has long served as Minister of Health; verify currency against the Prime Minister's Office and the Brunei MoH.

## 6. Update workflow

Verify against moh.gov.bn, pmo.gov.bn, Borneo Bulletin, The Scoop, Radio Television Brunei (RTB), BruDirect.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Importing party-political framings — Brunei operates a non-party absolute monarchy; party framings will be filtered.
- Ignoring the Islamic-policy lens — Brunei applies Syariah law and Islamic policy principles in health (e.g., halal pharmaceuticals, modesty in service delivery, alcohol prohibition); framings that ignore this lens are inaccurate.
- Conflating with Malaysia — Brunei is a sovereign state with its own health-system architecture distinct from neighbouring Malaysia.

## 9. Acronym glossary

- **MoH** — Ministry of Health.
- **RIPAS** — Raja Isteri Pengiran Anak Saleha Hospital.
- **YB** — Yang Berhormat (honourable).

## 10. Worked example

```yaml
      - YB Dato Seri Setia Dr. Haji Md Isham bin Haji Jaafar:
          - Title: Minister of Health
          - Stakeholder engagement notes:
              - "Long-serving Minister of Health under Sultan Hassanal Bolkiah; medical doctor; verify currency against the Prime Minister's Office and MoH."
              - "Owns MoH policy and budget, RIPAS Hospital (Bandar Seri Begawan), Suri Seri Begawan Hospital (Kuala Belait), Pengiran Muda Mahkota Pengiran Muda Haji Al-Muhtadee Billah Hospital (Tutong), Pengiran Anak Puteri Hajah Rashidah Sa'adatul Bolkiah Hospital (Temburong), the primary-care centre network, the Halal Health Excellence agenda, and ASEAN-Health Cluster diplomacy."
              - "Hook: NCDs (high obesity, diabetes, cardiovascular burden), tobacco control, halal pharmaceutical and biomedical agenda, digital health, mental health, and ASEAN cooperation land."
          - Tone advice:
              - "Open with NCDs, tobacco control, halal-health agenda, digital health and ASEAN cooperation — durable MoH lines."
              - "Do not import party-political framings or ignore the Islamic-policy lens — both will be filtered."
```

## 11. Out-of-band notes

For roles unfilled or interim.

## 12. Open questions

- Permanent Secretary (Health) and Director-General Medical Services with currency verified.
- CEO RIPAS with currency verified.
