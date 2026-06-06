# spec.md — `leaders.yml`

Single source of truth for the Zimbabwean health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Zimbabwean Ministry of Health and Child Care (MoHCC), Medicines Control Authority of Zimbabwe (MCAZ), National AIDS Council (NAC), the Health Service Commission, and adjacent bodies.

Zimbabwe operates a four-tier public system (Central Hospitals — Parirenyatwa, Sally Mugabe, Mpilo, United Bulawayo; Provincial Hospitals; District Hospitals; Rural Health Centres), supplemented by mission hospitals, private medical-aid societies and private providers. The Ministry serves under the ZANU-PF government of President Emmerson Mnangagwa.

## 2. Scope

In scope: President; Minister of Health and Child Care; Deputy Minister; Permanent Secretary; Chief Medical Officer; CEO MCAZ; CEO NAC; Health Service Commission Chair; Portfolio Committee on Health and Child Care (Parliament); Senate Thematic Committee on HIV/AIDS; Zimbabwe Medical Association (ZiMA); Zimbabwe Nurses Association (ZINA); Zimbabwe Hospital Doctors Association (ZHDA).

Out of scope: hospital CEOs (unless nationally visible); provincial medical directors; private medical aid society executives.

## 3. Structure

Standard 2/6/10/14 indentation. Top-level key: `Zimbabwean health stakeholders:`. Ordering: Presidency → MoHCC → MCAZ → NAC → Health Service Commission → Parliament → professional associations.

## 4. Field definitions

Party affiliation in parentheses after name: `ZANU-PF` (Zimbabwe African National Union — Patriotic Front, ruling), `CCC` (Citizens Coalition for Change, principal opposition), `MDC-T` (Movement for Democratic Change — Tsvangirai legacy). Independent for non-aligned. Titles in English.

## 5. Provenance and dating

Anchor to year, month or date. Dr. Douglas Mombeshora is Minister of Health and Child Care in the Mnangagwa Second Republic cabinet; chaired the SADC Ministerial Committee on Health; led the Zimbabwe delegation to the 78th World Health Assembly (May 2025) and 79th WHA (May 2026).

## 6. Update workflow

Verify against mohcc.gov.zw, opc.gov.zw (Office of the President), parlzim.gov.zw, mcaz.co.zw, nac.org.zw, The Herald, NewsDay, Bulawayo24, Zimbabwe Independent, Newzimbabwe.com.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Conflating MoHCC budget with actual disbursements — Treasury allocations and disbursements diverge under fiscal stress; budget headline is not a delivered figure.
- Ignoring the mission-hospital sub-system — Catholic, Methodist, Salvation Army and other mission hospitals provide a substantial share of rural care under MoU with MoHCC and cannot be excluded from engagement framings.
- Assuming sanctions-aligned framings — Zimbabwe is under selective US and EU sanctions on individuals and entities, not blanket country sanctions; pitches that assume blanket prohibition are inaccurate and will be rejected.

## 9. Acronym glossary

- **CCC** — Citizens Coalition for Change.
- **MCAZ** — Medicines Control Authority of Zimbabwe.
- **MoHCC** — Ministry of Health and Child Care.
- **NAC** — National AIDS Council.
- **ZANU-PF** — Zimbabwe African National Union — Patriotic Front.
- **ZiMA** — Zimbabwe Medical Association.

## 10. Worked example

```yaml
      - Dr. Douglas Mombeshora (ZANU-PF):
          - Title: Minister of Health and Child Care (since September 2023)
          - Stakeholder engagement notes:
              - "Minister of Health and Child Care in the Mnangagwa Second Republic cabinet; medical doctor; long-serving ZANU-PF politician with previous portfolios; led Zimbabwe delegation to 78th and 79th WHA; chairs SADC Ministerial Committee on Health."
              - "Owns MoHCC policy and budget, Central Hospitals (Parirenyatwa, Sally Mugabe, Mpilo, United Bulawayo), provincial and district hospital network, MCAZ oversight, NAC AIDS levy and programmes, mission-hospital MoUs, and SADC and African Union health diplomacy."
              - "Hook: HIV/AIDS programme continuity (Zimbabwe is a PEPFAR partner and an AIDS Levy success case), cervical cancer (a sustained presidential priority), maternal and child health, NCDs, primary health care strengthening, SADC One Health, mission-hospital partnership land."
          - Tone advice:
              - "Open with HIV continuity, cervical cancer, maternal and child health, primary care and SADC One Health — these are sustained MoHCC priorities and Mombeshora's signature lines."
              - "Do not assume blanket sanctions — Zimbabwe is under selective individual and entity sanctions, not country-wide prohibition; framings that assume blanket prohibition are inaccurate and will be rejected."
```

## 11. Out-of-band notes

For roles unfilled or interim.

## 12. Open questions

- Named Deputy Minister and Permanent Secretary with currency verified.
- CEO MCAZ and CEO NAC with currency verified.
- Portfolio Committee on Health and Child Care Chair with currency verified.
