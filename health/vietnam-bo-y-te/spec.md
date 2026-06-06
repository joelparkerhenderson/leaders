# spec.md — `leaders.yml`

Single source of truth for the Vietnamese health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around Bộ Y tế (Ministry of Health) of the Socialist Republic of Vietnam, Vietnam Social Security (BHXH) Health Insurance Division, Drug Administration of Vietnam (DAV), National Institute of Hygiene and Epidemiology (NIHE), Bach Mai and other central hospitals, and adjacent bodies.

Vietnam operates universal Social Health Insurance (Bảo hiểm y tế / BHYT) administered by VSS (Vietnam Social Security), covering ~92% of the population by 2025. Bộ Y tế sets policy through medium-term plans; provincial Sở Y tế implement. The system has both central hospitals (e.g., Bạch Mai, Việt Đức, Chợ Rẫy) and provincial-municipal hospitals, with primary care through commune health stations.

## 2. Scope

In scope: Tổng Bí thư and President (combined since 2024); Thủ tướng (Prime Minister); Bộ trưởng Bộ Y tế; Thứ trưởng (Deputy Ministers); Director General VSS Health Insurance Division; Director DAV; Director NIHE; Director Pasteur Institute Ho Chi Minh City; Directors of central hospitals (Bạch Mai, Việt Đức, Chợ Rẫy, Huế Central, K Hospital); Giám đốc Sở Y tế of major provinces / cities (Hà Nội, TP. Hồ Chí Minh, Hải Phòng, Đà Nẵng, Cần Thơ); National Assembly Committee on Social Affairs (Ủy ban Văn hóa và Xã hội after 2026 reorganisation) Chair; Vietnam Medical Association; Vietnam Nurses Association.

## 3. Structure

Standard 2/6/10/14. Ordering: Party-State leadership → Bộ Y tế → BHXH Health Insurance Division → DAV → NIHE → Pasteur Institutes → central hospitals → provincial Sở Y tế → National Assembly Committee → professional bodies.

## 4. Field definitions

CPV (Đảng Cộng sản Việt Nam) party membership is presumed for senior officials. Titles in Vietnamese with English glosses. Person names in family-name-first order following Vietnamese convention; use Vietnamese diacritics.

## 5. Provenance and dating

Đào Hồng Lan has served as Bộ trưởng Bộ Y tế since 2022 (acting from July 2022, confirmed by National Assembly for 2021-2026 term in October 2022); reappointed on 8 April 2026 at the first session of the 16th National Assembly for the 2026-2031 term. She is the third female Health Minister in Vietnamese history and the first Health Minister without a medical background (economics and industrial management).

## 6. Update workflow

Verify against moh.gov.vn, chinhphu.vn, baohiemxahoi.gov.vn, dav.gov.vn, quochoi.vn, Vietnam News Agency, Tuổi Trẻ, Thanh Niên, VnExpress, Lao Động, Sức khỏe & Đời sống, Vietnam Plus.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating Bộ Y tế as the only counterparty — BHXH (Vietnam Social Security) administers BHYT and is the financial counterparty for hospital and pharmacy contracting.
- Importing NHS framings unmodified — Vietnam is universal SHI with mixed public delivery and emerging private hospital sector.

## 9. Acronym glossary

- **Bạch Mai, Việt Đức, Chợ Rẫy** — three of the largest central hospitals (Hanoi, Hanoi, HCMC respectively).
- **BHYT** — Bảo hiểm y tế (compulsory health insurance).
- **BHXH** — Bảo hiểm xã hội Việt Nam (Vietnam Social Security).
- **Bộ Y tế** — Ministry of Health.
- **CPV** — Communist Party of Vietnam (Đảng Cộng sản Việt Nam).
- **DAV** — Drug Administration of Vietnam.
- **NIHE** — National Institute of Hygiene and Epidemiology.
- **Sở Y tế** — provincial / municipal Department of Health.

## 10. Worked example

```yaml
      - Đào Hồng Lan:
          - Title: Bộ trưởng Bộ Y tế (Minister of Health) (nhiệm kỳ 2026-2031, được Quốc hội phê chuẩn 8 tháng 4 năm 2026; tiếp tục từ nhiệm kỳ 2021-2026)
          - Stakeholder engagement notes:
              - "Bộ trưởng Bộ Y tế từ năm 2022 (Quyền Bộ trưởng từ tháng 7/2022, Quốc hội phê chuẩn cho nhiệm kỳ 2021-2026 vào tháng 10/2022); tái bổ nhiệm cho nhiệm kỳ 2026-2031 vào ngày 8 tháng 4 năm 2026 tại kỳ họp đầu Quốc hội khóa XVI."
              - "55 tuổi; quê Hải Phòng; Thạc sĩ Kinh tế và Cử nhân Quản lý Sản xuất Công nghiệp — Bộ trưởng Y tế thứ ba là nữ trong lịch sử Việt Nam (sau Trần Thị Trung Chiến và Nguyễn Thị Kim Tiến) và Bộ trưởng Y tế đầu tiên không có nền tảng chuyên môn y khoa."
              - "Ủy viên Ban Chấp hành Trung ương Đảng khóa XIV, Ủy viên Ban Cán sự Đảng Chính phủ, Bí thư Đảng ủy Bộ Y tế, đại biểu Quốc hội khóa XVI nhiệm kỳ 2026-2031."
              - "Owns chính sách Bộ Y tế, phối hợp với BHXH về BHYT (~92% dân số được bao phủ), DAV về thuốc, NIHE về dịch tễ; chương trình 'Vì một Việt Nam khỏe mạnh hơn 2026' (khám bệnh miễn phí cộng đồng ở Hải Phòng); cải cách hệ thống bệnh viện công lập; vai trò Việt Nam trong WHO Tây Thái Bình Dương và ASEAN."
              - "Hook: BHYT mở rộng, cải cách bệnh viện công lập, y tế cơ sở, dược phẩm, kiểm soát thuốc lá và rượu, chuyển đổi số y tế, hợp tác ASEAN và BRICS+ landings."
          - Tone advice:
              - "Mở đầu với BHYT, y tế cơ sở, cải cách bệnh viện, chuyển đổi số và hợp tác khu vực — đây là khung diễn ngôn nhất quán của Bộ Y tế dưới sự lãnh đạo của Bộ trưởng Lan."
              - "Đừng pitch như thể Bộ Y tế là người mua duy nhất — BHXH thực hiện BHYT một cách độc lập về mặt thể chế; mọi đàm phán về thanh toán và hợp đồng nhà cung cấp phải bao gồm BHXH."
```

## 11. Out-of-band notes

For roles unfilled or in transition.

## 12. Open questions

- Named Thứ trưởng (Deputy Ministers) under Lan in the 2026-2031 term with currency verified.
- Director General BHXH Health Insurance Division with currency verified.
- Director DAV, Director NIHE, Director Pasteur Institute HCMC with currency verified.
- Directors of Bạch Mai, Việt Đức, Chợ Rẫy, Huế Central, K Hospital with currency verified.
- Giám đốc Sở Y tế of Hà Nội, TP. HCM, Hải Phòng, Đà Nẵng, Cần Thơ.
- National Assembly Committee on Social Affairs / Văn hóa và Xã hội Chair in the 16th National Assembly.
- President Vietnam Medical Association and Vietnam Nurses Association with currency verified.
