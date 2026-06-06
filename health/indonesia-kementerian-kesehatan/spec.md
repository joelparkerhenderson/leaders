# spec.md — `leaders.yml`

Single source of truth for the Indonesian health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around Kementerian Kesehatan Republik Indonesia (Kemenkes), BPJS Kesehatan (the single-payer health insurer), BPOM (food and drug authority), Badan Kebijakan Pembangunan Kesehatan, provincial Dinas Kesehatan, and adjacent bodies.

Indonesia operates universal coverage through Jaminan Kesehatan Nasional (JKN) administered by BPJS Kesehatan since 2014, contracting both public and private providers. Kemenkes sets policy; BPOM regulates medicines and devices; 38 provincial Dinas Kesehatan implement; the network includes Pusat Kesehatan Masyarakat (Puskesmas) primary-care centres and tiered hospitals (RS Tipe A, B, C, D).

## 2. Scope

In scope: Presiden; Menteri Kesehatan; Wakil Menteri Kesehatan; Sekretaris Jenderal Kemenkes; Direktur Jenderal Pelayanan Kesehatan, Kesehatan Masyarakat, P2P (Pencegahan dan Pengendalian Penyakit), Tenaga Kesehatan, Farmalkes; Direktur Utama BPJS Kesehatan; Kepala BPOM; Kepala Badan Kebijakan Pembangunan Kesehatan; Direktur RSCM (Cipto Mangunkusumo) and major academic hospitals; Kepala Dinas Kesehatan of large provinces (Jakarta, Jawa Barat, Jawa Tengah, Jawa Timur, Sumatera Utara); Ketua Komisi IX DPR; IDI (Ikatan Dokter Indonesia); PPNI (Persatuan Perawat Nasional Indonesia); IAI (Ikatan Apoteker Indonesia).

## 3. Structure

Standard 2/6/10/14. Ordering: Kepresidenan → Kemenkes → BPJS Kesehatan → BPOM → Badan Kebijakan → major hospitals → Dinas Kesehatan provinces → DPR Komisi IX → professional bodies.

## 4. Field definitions

Party affiliation using canonical Indonesian abbreviations: `Gerindra` (Gerakan Indonesia Raya — Prabowo), `Golkar`, `PDI-P` (Partai Demokrasi Indonesia Perjuangan), `NasDem`, `PKS` (Partai Keadilan Sejahtera), `PKB`, `PAN`, `Demokrat`, `PSI`. Titles in Bahasa Indonesia with English glosses.

## 5. Provenance and dating

Budi Gunadi Sadikin has served as Menteri Kesehatan since 23 December 2020 in the Jokowi II government; reappointed by President Prabowo Subianto on 21 October 2024 in the Kabinet Merah Putih for the 2024-2029 term. Only the second Indonesian Health Minister without a medical degree (engineering physics background from ITB).

## 6. Update workflow

Verify against kemkes.go.id, presidenri.go.id, bpjs-kesehatan.go.id, pom.go.id, dpr.go.id, Kompas, Tempo, Detik, CNN Indonesia, KumparanNEWS, Antara.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating Kemenkes as the only operational entity — BPJS Kesehatan administers the single-payer insurance covering >270 million enrolled members.
- Importing US framings unmodified — Indonesia has universal coverage through JKN with mixed public-private delivery.

## 9. Acronym glossary

- **BPJS Kesehatan** — Badan Penyelenggara Jaminan Sosial Kesehatan (single-payer health insurer).
- **BPOM** — Badan Pengawas Obat dan Makanan (food and drug authority).
- **IDI** — Ikatan Dokter Indonesia (Indonesian Medical Association).
- **JKN** — Jaminan Kesehatan Nasional (national health insurance scheme).
- **Kemenkes** — Kementerian Kesehatan.
- **Puskesmas** — Pusat Kesehatan Masyarakat (community health centre).
- **RSCM** — Rumah Sakit Cipto Mangunkusumo (national referral hospital, Jakarta).

## 10. Worked example

```yaml
      - Budi Gunadi Sadikin:
          - Title: Menteri Kesehatan Republik Indonesia (Minister of Health) (Kabinet Merah Putih, sejak 21 Oktober 2024)
          - Stakeholder engagement notes:
              - "Menteri Kesehatan since 23 December 2020 in the Jokowi II government; reappointed by President Prabowo Subianto on 21 October 2024 in the Kabinet Merah Putih for the 2024-2029 term — rare continuity across two presidencies."
              - "Born 6 May 1964; Bachelor of Engineering Physics from Bandung Institute of Technology (ITB, 1988) — only the second Indonesian Health Minister without a medical degree (the other was Bambang Sulistomo); career background in IT (IBM Asia-Pacific Tokyo) and banking (Bank Bali, ABN AMRO, Bank Danamon, Mandiri)."
              - "Owns Kemenkes policy, the JKN system through coordination with BPJS Kesehatan (>270 million enrolees), BPOM oversight, the Transformasi Sistem Kesehatan reform (six pillars: primary care, secondary-tertiary care, resilience, financing, workforce, digital), Covid-19 vaccine legacy, post-pandemic preparedness."
              - "2026 public lines: 5 strategies to improve maternal-and-child health services; continued emphasis on TB elimination, stunting reduction, and the rollout of cancer-screening programmes."
              - "Hook: Transformasi Sistem Kesehatan, BPJS Kesehatan reform, digital health (SatuSehat), TB elimination, stunting reduction, maternal-and-child, and BRICS+ / G20 health cooperation land."
          - Tone advice:
              - "Open with Transformasi Sistem Kesehatan, primary care, digital health (SatuSehat), TB, and stunting — these are the Six-Pillars reform frame and Sadikin's sustained public lines."
              - "Do not pitch as if BPJS Kesehatan were a passive payer — BPJS is statutorily autonomous and operationally massive; engagement on financing and provider contracts must include BPJS Kesehatan directly."
```

## 11. Out-of-band notes

For roles unfilled or in transition.

## 12. Open questions

- Named Wakil Menteri Kesehatan (Dante Saksono Harbuwono confirmed continuing per the search), Sekretaris Jenderal, and Direktur Jenderals under Sadikin in the Kabinet Merah Putih.
- Direktur Utama BPJS Kesehatan with currency verified.
- Kepala BPOM with currency verified.
- Direktur RSCM, RSUD Sutomo, RSUP Hasan Sadikin, RSUP Sardjito, RSUP Adam Malik with currency verified.
- Kepala Dinas Kesehatan of large provinces (Jakarta, Jawa Barat, Jawa Tengah, Jawa Timur, Sumatera Utara).
- Ketua Komisi IX DPR in the current parliamentary term.
- Ketua Umum IDI, PPNI, IAI with currency verified.
