# spec.md — `leaders.yml`

Single source of truth for the Israeli health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Israeli Ministry of Health (משרד הבריאות), the four Kupot Holim (HMOs / sick funds), the Israel Medical Association, and adjacent bodies.

Israel operates universal Bismarckian-style coverage through the National Health Insurance Law (1995): every resident is enrolled in one of four Kupot Holim — Clalit, Maccabi, Meuhedet, Leumit — financed through the National Insurance Institute and supplementary insurance. The Ministry of Health (משרד הבריאות) sets policy and the annual Public Health Basket revision; the Kupot Holim contract providers and operate some hospitals; the Ministry also directly operates ~15 government hospitals.

## 2. Scope

In scope: Prime Minister; Minister of Health; Deputy Minister; Director-General Ministry of Health; CEO Clalit, Maccabi, Meuhedet, Leumit; Director Public Health Services; Director Medical Administration; Director Israel Drug Administration; Director Israel Center for Disease Control; Directors of major government hospitals (Sheba, Hadassah, Rambam, Ichilov / Sourasky); Chair Knesset Health Committee; President Israel Medical Association (IMA / HaHistadrut HaRefuit); President Israel Nurses Association.

## 3. Structure

Standard 2/6/10/14. Ordering: PM → Ministry of Health → Kupot Holim → Israel Drug Administration → ICDC → government hospitals → Knesset Health Committee → professional bodies.

## 4. Field definitions

Party affiliation using canonical Israeli abbreviations: `Likud`, `Yesh Atid`, `National Unity`, `Shas`, `UTJ` (United Torah Judaism), `Religious Zionism`, `Otzma Yehudit`, `Israeli Labor`, `Meretz`, `Ra'am`, `Hadash-Ta'al`, `Yisrael Beiteinu`, `Noam`. Titles in English (with Hebrew where used officially).

## 5. Provenance and dating

Haim Katz (Likud) was confirmed Minister of Health by the Knesset on 24 November 2025 — one of five ministries Katz absorbed when ultra-Orthodox parties withdrew from the Netanyahu coalition; he simultaneously serves as Minister of Tourism, Minister of Construction and Housing, and Minister of Welfare. The 2026 Public Health Basket revision led on cancer treatment and mental-health drugs (announced February 2026).

## 6. Update workflow

Verify against health.gov.il, gov.il, knesset.gov.il, Times of Israel, Jerusalem Post, Haaretz, Ynet, Calcalist, Israel Hayom, i24News, Israel Democracy Institute, Israel National News.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating the Ministry of Health as the only relevant counterparty — the four Kupot Holim are the largest operational decision-makers in Israeli health.
- Importing US framings unmodified — Israel is universal coverage with managed-competition between sick funds and a small but politically salient supplementary market.

## 9. Acronym glossary

- **Clalit, Maccabi, Meuhedet, Leumit** — the four Kupot Holim (sick funds / HMOs).
- **Hadassah** — Hadassah Medical Center, Jerusalem (Hebrew University-affiliated).
- **HaHistadrut HaRefuit** — Israel Medical Association (IMA).
- **Ichilov / Sourasky** — Tel Aviv Sourasky Medical Center.
- **IMA** — Israel Medical Association.
- **MoH** — Ministry of Health.
- **Sheba** — Sheba Medical Center, Tel HaShomer (largest Israeli hospital).

## 10. Worked example

```yaml
      - Haim Katz (Likud):
          - Title: Minister of Health (and concurrently Minister of Tourism, Minister of Construction and Housing, Minister of Welfare) (since 24 November 2025 confirmation)
          - Stakeholder engagement notes:
              - "Minister of Health, confirmed by the Knesset on 24 November 2025 along with multiple other portfolios; Likud; took the Health, Welfare, Tourism and Construction-and-Housing portfolios after ultra-Orthodox parties (UTJ, Shas) withdrew from the Netanyahu coalition over the draft-law crisis; serves four ministries simultaneously."
              - "Long-time Likud political figure with focus on labour, welfare and pensions; not a clinician; the appointment to Health was administrative-political rather than substantive-clinical."
              - "Israel Democracy Institute described the situation prior to confirmation as 'a ministry with no minister'; Public Health Services Committee for the 2026 Health Basket was appointed after weeks-long delay due to the leadership vacuum."
              - "Owns the 2026 Public Health Basket revision (cancer treatments lead the 2026 basket; new mental-health drugs added per Haaretz Feb 2026), Kupot Holim contracts, government-hospital operations, and the post-Oct-2023 health-system reconstruction in southern and northern border communities."
              - "Hook: Health Basket revision, Kupot Holim financing, hospital workforce, mental health, post-conflict trauma care, Sheba and Soroka recovery aterrissent."
          - Tone advice:
              - "Open with Health Basket revision, Kupot Holim financing, post-conflict trauma and southern/northern recovery — these are the live political files of the coalition."
              - "Do not assume a full-time clinical focus — Katz oversees four ministries; engagement on substantive clinical policy will route through the Director-General of the Ministry and the Public Health Services."
```

## 11. Out-of-band notes

For roles unfilled or interim. Note Katz's multi-ministry arrangement reflects the coalition crisis, not normal Israeli governance.

## 12. Open questions

- Named Deputy Minister of Health under Katz with currency verified.
- Director-General of the Ministry of Health under Katz with currency verified.
- CEOs Clalit, Maccabi, Meuhedet, Leumit with currency verified.
- Director Public Health Services and Director Medical Administration with currency verified.
- Director Israel Drug Administration and Director Israel Center for Disease Control with currency verified.
- Directors of Sheba, Hadassah, Rambam, Ichilov (Sourasky), Soroka with currency verified.
- Chair Knesset Health Committee in the current Knesset.
- President Israel Medical Association with currency verified.
