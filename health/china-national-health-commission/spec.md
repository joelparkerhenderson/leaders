# spec.md — `leaders.yml`

Single source of truth for the structure, semantics, and update rules of `leaders.yml` for the People's Republic of China health system. The YAML must conform to this spec; if they disagree, the spec wins and the YAML is fixed.

## 1. Purpose

`leaders.yml` is an engagement register of named individuals in and around the PRC health system. Each entry helps a reader inside the National Health Commission (NHC / 国家卫生健康委员会), the National Medical Products Administration (NMPA / 国家药品监督管理局), the National Healthcare Security Administration (NHSA / 国家医疗保障局), the National Disease Control and Prevention Administration (NDCPA / 国家疾病预防控制局), provincial Health Commissions, or an adjacent body decide who to engage, how, and where.

The Chinese health system combines a centrally-steered policy architecture with provincial and city implementation. The NHC sets policy, coordinates with the State Council, and oversees provincial health commissions. The NHSA (created 2018) administers the centralised drug procurement (VBP / Volume-Based Procurement), DRG and DIP payment reforms, and the unified basic medical insurance schemes. NMPA regulates medicines and devices on EMA-equivalent infrastructure. The NDCPA (created 2021 post-Covid) handles disease prevention and control. Hospitals are predominantly public, organised by tier (tertiary, secondary, primary) and increasingly by university-hospital alliances. Hong Kong and Macau SARs have separate systems.

## 2. Scope

**In scope:** Premier (Guowuyuan Zongli); Vice-Premier with health portfolio; Minister of NHC (NHC Zhuren) — concurrently CCP Committee Secretary of NHC; Vice-Ministers; Director of NMPA; Director of NHSA; Director of NDCPA; Director of National Administration of Traditional Chinese Medicine; President Chinese Academy of Medical Sciences; President of major academic hospitals (Peking Union Medical College Hospital, Huashan Hospital Fudan, West China Hospital, Zhongshan Hospital Fudan, Beijing Tiantan Hospital, PLA General Hospital — 301 Hospital); Directors of major provincial Health Commissions (Guangdong, Jiangsu, Shanghai, Beijing, Shandong, Zhejiang, Henan, Sichuan, Hubei, Hunan); SAR Secretaries for Health and Food and Health (Hong Kong, Macau); Chair NPC Education, Science, Culture and Public Health Committee; Chair Chinese Medical Association.

**Out of scope:** operational staff below department head (zhang) level; vendors; historical post-holders.

## 3. Structure

```
中华人民共和国卫生健康利益相关方 / People's Republic of China health stakeholders:
  - {Organisation}:
      - {Person}:
          - Title: ...
          - Stakeholder engagement notes: [...]
          - Tone advice: [...]
```

Indentation 2/6/10/14 spaces. Ordering: State Council (Vice-Premier with health portfolio) → NHC → NHSA → NMPA → NDCPA → National Administration of Traditional Chinese Medicine → Chinese Academy of Medical Sciences → major academic hospitals → major provinces → Hong Kong SAR Secretary for Health → Macau SAR Secretary for Social Affairs and Culture (health subset) → Chinese Medical Association.

## 4. Field definitions

Standard family conventions. Use Hanyu Pinyin transliterations of names with Chinese characters in brackets where useful. Person names in family-name-first order. Communist Party of China (CCP) affiliation is the operational party affiliation but is rarely the only relevant identifier; if a person is on the CCP Central Committee or is a CCP Committee Secretary of a body that fact should be flagged. Titles in English with Chinese (Mandarin / Hanyu Pinyin / Chinese characters) where useful.

## 5. Provenance and dating

Anchor facts to year, month or exact date. Lei Haichao (雷海潮) is Minister of NHC and concurrently CCP Committee Secretary of NHC; he led the Chinese delegation to the 79th World Health Assembly in May 2026, visited the Hong Kong SAR 12-13 January 2026 (including delegation to HKU), and attended a joint meeting with Hong Kong and Macao health officials on 20 January 2026. China publicly aims to raise average life expectancy to around 80 years in five years (October 2025 statement).

## 6. Update workflow

1. Identify the change. 2. Verify against nhc.gov.cn, nmpa.gov.cn, nhsa.gov.cn, ndcpa.gov.cn, gov.cn, npc.gov.cn, Xinhua, People's Daily, China Daily, Caixin, SCMP, Reuters, Bloomberg, Healthcare Asia. 3. Apply minimum diff. 4. Confirm structure. 5. Re-validate cross-references.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Importing US or NHS framings unmodified — China is a centrally-steered system with provincial implementation, distinct procurement and payment reforms (VBP, DRG / DIP), and predominantly public hospital ownership.
- Treating NHC as the only national counterparty — NHSA holds the procurement and reimbursement levers and is functionally as important for pharma engagement.

## 9. Acronym glossary

- **CASS** — Chinese Academy of Sciences (separate from CAMS).
- **CAMS** — Chinese Academy of Medical Sciences.
- **CCP** — Communist Party of China.
- **CMA** — Chinese Medical Association (中华医学会).
- **DIP** — Diagnosis-Intervention Packet (Chinese hospital payment innovation alongside DRG).
- **DRG** — Diagnosis-Related Groups (China is rolling out DRG payment nationally).
- **HKU** — University of Hong Kong (and HKUMed for its medical school).
- **NDCPA** — National Disease Control and Prevention Administration (created 2021).
- **NHC** — National Health Commission (国家卫生健康委员会).
- **NHSA** — National Healthcare Security Administration (国家医疗保障局).
- **NMPA** — National Medical Products Administration (国家药品监督管理局).
- **NRDL** — National Reimbursement Drug List.
- **PUMCH** — Peking Union Medical College Hospital.
- **SAR** — Special Administrative Region (Hong Kong, Macau).
- **VBP** — Volume-Based Procurement (centralised drug procurement).

## 10. Worked example

```yaml
      - Lei Haichao / 雷海潮:
          - Title: Minister of the National Health Commission (国家卫生健康委员会主任 Guojia Weisheng Jiankang Weiyuanhui Zhuren) and CCP Committee Secretary of NHC
          - Stakeholder engagement notes:
              - "Minister of the National Health Commission and concurrently CCP Committee Secretary of NHC — combining administrative and party leadership of the central health portfolio; career within the Chinese health-policy and public-health management system."
              - "Led the Chinese delegation to the 79th World Health Assembly in Geneva (May 2026) — head-of-delegation status; visited Hong Kong SAR 12-13 January 2026 including HKU delegation; attended joint meeting with Hong Kong and Macao health officials 20 January 2026."
              - "Public policy line: 'Healthy China, not just China' — articulated at the WHA, signalling China's interest in global-health rules-and-norms participation; aligns with the State Council target announced October 2025 to raise average life expectancy to around 80 years within five years."
              - "Owns NHC steering of provincial health commissions, the national hospital reform programme, integrated medical-care vision (yiliao-yibao-yiyao 'three-medical-linkage' coordination with NHSA and NMPA), traditional Chinese medicine integration, and primary-care strengthening."
              - "Hook: 'Healthy China 2030', three-medical-linkage reform, hospital-tier reform, primary-care strengthening, HK-Macao-Mainland health coordination, global health multilateral participation, traditional Chinese medicine and innovation-medicine policy land."
          - Tone advice:
              - "Open with 'Healthy China', three-medical-linkage, primary-care strengthening and HK-Macao-Mainland coordination — these are Lei's authored public-policy framings."
              - "Do not pitch through commercial-Western-pharma frames without engaging NHSA on procurement and pricing — VBP and DRG / DIP reforms have changed the commercial logic of the Chinese health market, and pitches that ignore them will be marked as out-of-date."
```

## 11. Out-of-band notes

For roles unfilled or interim.

## 12. Open questions

- Named Vice-Premier with health portfolio in the current State Council with currency verified.
- Named NHC Vice-Ministers under Lei Haichao with currency verified.
- Director of NMPA, Director of NHSA, Director of NDCPA, Director of National Administration of Traditional Chinese Medicine with currency verified.
- President Chinese Academy of Medical Sciences and Presidents of the major academic hospitals (PUMCH, Huashan, West China, Zhongshan Fudan, Beijing Tiantan, 301 PLA General).
- Directors of major provincial Health Commissions (Guangdong, Jiangsu, Shanghai, Beijing, Shandong, Zhejiang, Henan, Sichuan, Hubei, Hunan).
- HK SAR Secretary for Health and Macau SAR Secretary for Social Affairs and Culture (health subset) with currency verified.
- Chair NPC Education, Science, Culture and Public Health Committee with currency verified.
- Chair Chinese Medical Association with currency verified.
