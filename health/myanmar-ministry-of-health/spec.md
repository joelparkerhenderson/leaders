# spec.md — `leaders.yml`

Single source of truth for the Myanmar health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Myanmar Ministry of Health under the new Union Government of Myanmar formed 10 April 2026 by President Min Aung Hlaing following the 11 April 2026 parliamentary installation, and parallel National Unity Government (NUG) Ministry of Health for resistance-controlled territories. Myanmar's health system has experienced massive disruption since the February 2021 military coup; civil war ongoing.

## 2. Scope

In scope: For the SAC-successor / Min Aung Hlaing Union Government — Minister of Health; Deputy Ministers; Director-General Public Health; DG Medical Services; CEO Yangon General Hospital, Mandalay General Hospital; State and Regional Health Departments. For parallel NUG — NUG Minister of Health. WHO Myanmar; UN OCHA Myanmar.

## 3. Structure

Standard. Document both administrations separately.

## 4. Field definitions

SAC-successor government is military-controlled; NUG is pro-democracy parallel government in resistance areas. Titles in English / Burmese.

## 5. Provenance and dating

The State Administration Council (SAC) was dissolved at end of July 2025; Min Aung Hlaing was installed as President of the Republic of the Union of Myanmar on 11 April 2026 by the new parliament; he established the new Union Government 10 April 2026, appointing many individuals from previous ministries. Substantive identity of the Minister of Health in the new Union Government should be verified against moi.gov.mm Union Government List and moh.gov.mm. The civil war and December 2025 elections context shape continued instability.

## 6. Update workflow

Verify against moi.gov.mm, moh.gov.mm, NUG ministry sites, Mizzima, Irrawaddy, Frontier Myanmar, Myanmar Now, Radio Free Asia Burmese.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating Myanmar as one health system — SAC-successor and NUG operate parallel structures.
- Ignoring war and humanitarian context.

## 9. Acronym glossary

- **NUG** — National Unity Government (parallel pro-democracy government).
- **SAC** — State Administration Council (military junta 2021-2025, dissolved July 2025).

## 10. Worked example

```yaml
      - Notes on Minister of Health, Union Government of Myanmar:
          - Status: Min Aung Hlaing was installed as the 11th President of the Republic of the Union of Myanmar on 11 April 2026 by the new parliament after the SAC was dissolved at the end of July 2025; he established the new Union Government on 10 April 2026 appointing many individuals who had served in his previous ministries. The substantive identity of the Minister of Health in the new Union Government for 2026 should be verified against the Union Government List at moi.gov.mm and the Ministry of Health website at moh.gov.mm. The December 2025 / 2025-26 general election context and ongoing civil war continue to shape political instability.
          - Implication: Engagement on Myanmar health requires acknowledging the dual administration (Min Aung Hlaing Union Government in territories under SAC-successor control; NUG parallel Ministry of Health in resistance-controlled territories), the politically isolated status of the post-coup government internationally, and the humanitarian-corridor and access constraints. WHO Myanmar operates under cross-line access negotiations.
```

## 11. Out-of-band notes

For roles unfilled or in transition.

## 12. Open questions

- Confirm Minister of Health in the post-10-April-2026 Min Aung Hlaing Union Government.
- NUG Minister of Health and parallel administration leadership.
- Deputy Ministers, DG Public Health, DG Medical Services with currency verified.
- CEO Yangon General Hospital, Mandalay General Hospital with currency verified.
- State and Regional Health Department directors with currency verified.
- WHO Myanmar Country Representative and UN OCHA Humanitarian Coordinator.
