# spec.md — `leaders.yml`

Single source of truth for the Libyan health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Libyan Ministry of Health. Libya has two parallel governments: the Government of National Unity (GNU, Tripoli, PM Dbeibah, UN-recognised) and the Government of National Stability (GNS, eastern, Bashagha-aligned / HoR-aligned). Each has separate Health Ministers and parallel administrations.

## 2. Scope

In scope: For both governments — Head of Government; Minister of Health; National Center for Disease Control (NCDC); Medical Supply Authority; National Authority for Pharmaceuticals and Medical Equipment; Hospital directors; House of Representatives Health Committee; Presidential Council; UN Support Mission (UNSMIL) health coordination.

## 3. Structure

Standard. Document both governments separately.

## 4. Field definitions

GNU is Tripoli-based PM Abdul Hamid Dbeibah; GNS is eastern HoR-aligned. Titles in English / Arabic.

## 5. Provenance and dating

Othman Abduljalil serves as Minister of Health in the Government of National Stability (eastern HoR-aligned government); Wikipedia confirmed as of February 2026. GNU Health Minister to verify separately.

## 6. Update workflow

Verify against gov.ly, mohgov.ly, prc.ly, libyareview.com, Libya Observer, Libya Update, AP Libya.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating Libya as unitary — two parallel governments operate.
- Ignoring post-Derna-2023 reconstruction context.

## 9. Acronym glossary

- **GNS** — Government of National Stability (eastern).
- **GNU** — Government of National Unity (Tripoli).
- **HoR** — House of Representatives (Tobruk-based).
- **NCDC** — National Center for Disease Control.
- **UNSMIL** — UN Support Mission in Libya.

## 10. Worked example

```yaml
      - Dr. Othman Abduljalil:
          - Title: Minister of Health, Government of National Stability (eastern HoR-aligned government)
          - Stakeholder engagement notes:
              - "Minister of Health in the Government of National Stability (eastern HoR-aligned government); current as of February 2026 (Wikipedia); previously appointed by Bashagha (Libya Review)."
              - "Active 2025-2026: pledged new health facilities in southern Libya; inaugurated new medical facility in Al-Kufra; led post-Derna 2023 floods reconstruction (six hospitals in Derna resumed service per Prokerala 2023 legacy)."
              - "Owns GNS Ministry policy and budget, eastern Libya hospital reconstruction, southern Libya health-access expansion, and coordination with WHO, Egypt, UAE, Russia in the divided-government context."
              - "Hook: post-Derna reconstruction, southern Libya health access (Al-Kufra, Murzuq, Sebha), Egypt-Libya cooperation, cross-government coordination on shared infectious-disease and pharmaceutical supply land."
          - Tone advice:
              - "Open with eastern-Libya hospital reconstruction, southern access, Egypt cooperation — these are GNS priorities."
              - "Do not assume single Libyan counterpart — engagement requires bridging GNU and GNS or accepting partial coverage."
```

## 11. Out-of-band notes

GNU Health Minister identity to verify separately; the parallel government structure is a structural feature.

## 12. Open questions

- GNU Minister of Health (Tripoli) identity and currency verified.
- GNS Deputy Minister of Health, NCDC Director, Medical Supply Authority Director with currency verified.
- Hospital directors for major facilities (Tripoli Medical Center, Benghazi Medical Center).
- HoR Health Committee Chair (Tobruk-based).
- UNSMIL Health Cluster Coordinator.
