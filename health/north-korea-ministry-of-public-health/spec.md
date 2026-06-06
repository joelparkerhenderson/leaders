# spec.md — `leaders.yml`

Single source of truth for the DPRK health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Democratic People's Republic of Korea (DPRK) Ministry of Public Health (MoPH) and adjacent bodies.

The DPRK operates a centrally planned single-party state under the Workers' Party of Korea (WPK) led by General Secretary Kim Jong Un, with a constitutionally free, universal, public health system whose operational capacity has been heavily affected by sanctions, structural constraints, and the 2020-2023 Covid border closure. Engagement is conducted within UN Security Council sanctions and humanitarian exemption frameworks.

## 2. Scope

In scope: General Secretary WPK / Chairman SAC; Premier of the Cabinet; Minister of Public Health; Director Pyongyang Maternity Hospital; Director Kim Man Yu Hospital; Director Ryugyong Dental Hospital.

Out of scope: provincial and county public-health office heads.

## 3. Structure

Standard 2/6/10/14 indentation. Top-level key: `DPRK health stakeholders:`. Ordering: WPK → Cabinet → MoPH → Hospitals.

## 4. Field definitions

Affiliation: `WPK` (Workers' Party of Korea). Titles in English.

## 5. Provenance and dating

Anchor to year, month or date. Choe Kyong Chol has been reported as Minister of Public Health in the DPRK cabinet; verify currency against KCNA (Korean Central News Agency) and Rodong Sinmun reporting.

## 6. Update workflow

Verify against kcna.kp (when accessible), Rodong Sinmun, NK News (third-party analytical reporting), 38 North, WHO DPRK country office briefings.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Assuming normalised engagement — UN Security Council sanctions and bilateral sanctions impose strict compliance requirements; humanitarian exemptions exist but require specific licensing.
- Ignoring the border-closure legacy — the 2020-2023 Covid border closure had material effects on access, supply chains and the donor architecture; framings that assume continuity from the pre-2020 architecture are inaccurate.
- Conflating with South Korea — sovereign states with radically different political, economic and health systems.

## 9. Acronym glossary

- **DPRK** — Democratic People's Republic of Korea.
- **KCNA** — Korean Central News Agency.
- **MoPH** — Ministry of Public Health.
- **WPK** — Workers' Party of Korea.

## 10. Worked example

```yaml
      - Choe Kyong Chol (WPK):
          - Title: Minister of Public Health
          - Stakeholder engagement notes:
              - "Minister of Public Health reported in DPRK cabinet listings under Premier Kim Tok Hun; verify currency against KCNA and Rodong Sinmun reporting."
              - "Owns MoPH policy and budget within constraints, Pyongyang Maternity Hospital, Kim Man Yu Hospital, Ryugyong Dental Hospital, the provincial people's hospital network across the nine provinces and three city-level administrations, and engagement with WHO DPRK, UNICEF DPRK, IFRC and a small number of permitted bilateral and NGO partners under humanitarian-exception frameworks."
              - "Hook: TB and MDR-TB (a sustained burden recognised by Global Fund and Eugene Bell Foundation), MCH, immunisation, NCDs, mental health, traditional Koryo medicine integration, and humanitarian-exception coordination land."
          - Tone advice:
              - "Open with TB, MCH, immunisation, NCDs and humanitarian-exception coordination."
              - "Do not assume normalised engagement, do not ignore the 2020-2023 border-closure legacy, do not conflate with the Republic of Korea."
```

## 11. Out-of-band notes

For roles where external visibility is limited.

## 12. Open questions

- Substantive identity of Minister of Public Health with currency verified.
- Directors of major hospitals.
