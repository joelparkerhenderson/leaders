# spec.md — `leaders.yml`

Single source of truth for the Turkish health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around T.C. Sağlık Bakanlığı (Ministry of Health), Sosyal Güvenlik Kurumu (SGK), TİTCK (Turkish Medicines and Medical Devices Agency), Halk Sağlığı Genel Müdürlüğü (Public Health Directorate), city hospitals (Şehir Hastaneleri), and adjacent bodies.

The Turkish system has been transformed by the Health Transformation Programme (Sağlıkta Dönüşüm Programı) since 2003 — universal coverage through Genel Sağlık Sigortası administered by SGK; centralised Sağlık Bakanlığı governance; the large Şehir Hastaneleri PPP network as tertiary backbone; primary care through Aile Hekimliği (family-medicine) practitioners.

## 2. Scope

In scope: Cumhurbaşkanı; Sağlık Bakanı; Bakan Yardımcıları (Deputy Ministers); SGK Başkanı; TİTCK Başkanı; Halk Sağlığı Genel Müdürü; Hudut ve Sahiller Sağlık Genel Müdürü; major Şehir Hastaneleri başhekimleri; major üniversite hastaneleri (Hacettepe, Cerrahpaşa, Ege, Dokuz Eylül, Çukurova, Akdeniz); TBMM Sağlık, Aile, Çalışma ve Sosyal İşler Komisyonu Başkanı; Türk Tabipleri Birliği (TTB) Merkez Konseyi Başkanı; Türk Eczacıları Birliği (TEB) Genel Başkanı; Türk Hemşireler Derneği Başkanı.

## 3. Structure

Standard 2/6/10/14. Ordering: Cumhurbaşkanlığı → Sağlık Bakanlığı → TİTCK → SGK → Halk Sağlığı Genel Müdürlüğü → Şehir Hastaneleri ve Üniversite Hastaneleri → TBMM → Meslek Birlikleri.

## 4. Field definitions

Party affiliation using canonical Turkish abbreviations: `AKP` (Adalet ve Kalkınma Partisi), `MHP` (Milliyetçi Hareket Partisi), `CHP` (Cumhuriyet Halk Partisi), `İYİ` (İYİ Parti), `HDP` (closed) / `DEM Parti`, `Saadet`, `Gelecek`, `DEVA`, `Yeniden Refah`, `Zafer`, `TİP`. Titles in Turkish with English glosses.

## 5. Provenance and dating

Prof. Dr. Kemal Memişoğlu was appointed Sağlık Bakanı in the 67th Government by President Erdoğan on 2 July 2024, replacing Fahrettin Koca. Memişoğlu was previously Provincial Health Director of Istanbul 2016-2024.

## 6. Update workflow

Verify against saglik.gov.tr, tccb.gov.tr, sgk.gov.tr, titck.gov.tr, hsgm.saglik.gov.tr, tbmm.gov.tr, Anadolu Ajansı (AA), Hürriyet, Sabah, Sözcü, Cumhuriyet, BirGün, Diken, Medimagazin.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating the system as fragmented — Turkey has centralised under SDP since 2003 with strong vertical integration.
- Importing NHS framings unmodified — Turkey is centralised, Bismarckian-financed, with significant PPP infrastructure (Şehir Hastaneleri).

## 9. Acronym glossary

- **Aile Hekimliği** — family-medicine primary-care programme (since 2010).
- **HSGM** — Halk Sağlığı Genel Müdürlüğü (Public Health Directorate).
- **SGK** — Sosyal Güvenlik Kurumu (Social Security Institution; runs Genel Sağlık Sigortası).
- **SDP** — Sağlıkta Dönüşüm Programı (Health Transformation Programme, 2003-onwards).
- **Şehir Hastanesi** — City Hospital (PPP-built tertiary hospital).
- **TBMM** — Türkiye Büyük Millet Meclisi (Grand National Assembly).
- **TEB** — Türk Eczacıları Birliği.
- **TİTCK** — Türkiye İlaç ve Tıbbi Cihaz Kurumu (medicines and devices regulator).
- **TTB** — Türk Tabipleri Birliği (Turkish Medical Association).

## 10. Worked example

```yaml
      - Prof. Dr. Kemal Memişoğlu (AKP):
          - Title: Sağlık Bakanı (Minister of Health) (since 2 July 2024)
          - Stakeholder engagement notes:
              - "Sağlık Bakanı appointed by President Recep Tayyip Erdoğan on 2 July 2024 in the 67th Government, replacing Fahrettin Koca; born 1966; Hacettepe University Faculty of Medicine graduate (1990); general-surgery specialty at Okmeydanı (1995); Associate Professor 2008, Professor 2016; AKP."
              - "Previously Provincial Health Director of Istanbul 2016-2024 — long executive experience managing the largest provincial health system in Turkey, including the post-2018 city-hospitals expansion in Istanbul."
              - "Public lines 2026: 26,673 personnel hires after the 2026 KPSS; smoke-free Turkey ('Dumansız Türkiye') campaign; 12 city hospitals under construction; addressed TBMM Genel Kurulu on 2026 budget."
              - "Owns Şehir Hastaneleri PPP network, Aile Hekimliği reform, SGK coordination, TİTCK regulatory file, post-2023-earthquake health-infrastructure rebuilding, the Sağlıkta Dönüşüm Programı continuation, and Turkey's WHO Europe and OIC health diplomacy."
              - "Hook: city hospitals, family medicine reform, health workforce, tobacco control, earthquake health reconstruction, R&D and biotechnology (TÜSEB), and digital health (e-Nabız) land."
          - Tone advice:
              - "Open with Şehir Hastaneleri, family medicine, workforce hiring, smoke-free Turkey, and earthquake health reconstruction — these are Memişoğlu's authored 2026 public lines."
              - "Do not pitch as if regional or provincial structures had autonomy — Turkey's system is centralised under Sağlık Bakanlığı with strong vertical control; provincial-autonomy framings will be redirected."
```

## 11. Out-of-band notes

For roles unfilled or in transition.

## 12. Open questions

- Named Bakan Yardımcıları (Deputy Ministers) under Memişoğlu with currency verified.
- Başkan SGK, TİTCK, Halk Sağlığı Genel Müdürü with currency verified.
- Başhekimler of largest Şehir Hastaneleri (Ankara, Mersin, Adana, Eskişehir, Kayseri, İzmir-Bayraklı, İstanbul-Başakşehir Çam ve Sakura).
- Rektörler / Başhekimler of Hacettepe, Cerrahpaşa, Ege, Dokuz Eylül, Çukurova, Akdeniz Tıp Fakülteleri.
- TBMM Sağlık, Aile, Çalışma ve Sosyal İşler Komisyonu Başkanı with currency verified.
- TTB Merkez Konseyi Başkanı, TEB Genel Başkanı, Türk Hemşireler Derneği Başkanı with currency verified.
