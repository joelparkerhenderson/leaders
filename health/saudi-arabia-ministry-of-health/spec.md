# spec.md — `leaders.yml`

Single source of truth for the Saudi health system register. The YAML must conform to this spec.

## 1. Purpose

Engagement register of named individuals in and around the Saudi Ministry of Health (MoH), the Saudi Health Council, the Saudi Food and Drug Authority (SFDA), Saudi Commission for Health Specialties (SCFHS), the Council of Health Insurance, regional health clusters, and adjacent bodies.

The Saudi system is undergoing transformation under Vision 2030: from a fully Ministry-of-Health-run public service (with Ministry of National Guard Health Affairs, Ministry of Defense Health Services and other parallel networks) to a payer-provider-separated model with 21 regional Health Clusters and a planned single payer. SFDA regulates medicines and food. SCFHS handles professional licensing. Hajj health-services delivery is a recurring annual flagship.

## 2. Scope

In scope: King; Crown Prince and Prime Minister; Minister of Health (concurrently Chairman Saudi Health Council, Chairman SFDA Board, Chairman SCFHS); Deputy Ministers; Director-General of each of the 21 Health Clusters; CEO Council of Health Insurance; CEO Saudi Center for Disease Prevention and Control; President KFSHRC (King Faisal Specialist Hospital and Research Centre); President NGHA (National Guard Health Affairs); Shoura Council Health Committee Chair; Saudi Society professional bodies.

## 3. Structure

Standard 2/6/10/14. Ordering: Royal Court → Ministry of Health → SFDA → SCFHS → Council of Health Insurance → Saudi CDC → 21 Health Clusters → KFSHRC / NGHA / military health → Shoura Health Committee → professional societies.

## 4. Field definitions

Names with Arabic transliteration; titles use 'His Excellency' (H.E.) where official.

## 5. Provenance and dating

Fahad bin Abdulrahman Al-Jalajel has served as Minister of Health since 15 October 2021; concurrently Chairman of the Saudi Health Council, Chairman of the Saudi Commission for Health Specialties Board of Trustees, and Chairman of the SFDA Board of Directors; member of the Council of Economic and Development Affairs (CEDA) and Chair of the Transformation Program Committee in the health sector.

## 6. Update workflow

Verify against moh.gov.sa, my.gov.sa, sfda.gov.sa, scfhs.org.sa, chi.gov.sa, kfshrc.edu.sa, shura.gov.sa, Saudi Press Agency (SPA), Saudi Gazette, Arab News, Asharq Al-Awsat.

## 7. Invariants

Standard.

## 8. Anti-patterns

- Treating the Ministry of Health as the only public sector — NGHA, MoD Health, KFSHRC and Aramco Medical Services are parallel public providers.
- Importing US framings unmodified — Saudi Arabia is undergoing structured Vision-2030 transformation with deliberate sequencing.

## 9. Acronym glossary

- **CEDA** — Council of Economic and Development Affairs.
- **CHI** — Council of Health Insurance.
- **KFSHRC** — King Faisal Specialist Hospital and Research Centre (Riyadh, Jeddah).
- **MoH** — Ministry of Health.
- **NGHA** — National Guard Health Affairs.
- **SCFHS** — Saudi Commission for Health Specialties.
- **SCDC** — Saudi Center for Disease Prevention and Control.
- **SFDA** — Saudi Food and Drug Authority.
- **SHC** — Saudi Health Council.
- **Vision 2030** — Saudi long-term reform programme.

## 10. Worked example

```yaml
      - H.E. Fahad bin Abdulrahman Al-Jalajel:
          - Title: Minister of Health (since 15 October 2021); Chairman Saudi Health Council; Chairman SFDA Board; Chairman SCFHS Board of Trustees
          - Stakeholder engagement notes:
              - "Minister of Health since 15 October 2021; concurrently Chairman of the Saudi Health Council, Chairman of the Saudi Commission for Health Specialties Board of Trustees, and Chairman of the SFDA Board of Directors; member of CEDA and Chair of the Transformation Program Committee in the health sector — unusually broad institutional portfolio."
              - "Public lines 2026: announced advanced healthcare readiness for the 2026 Hajj with bed-capacity surpassing 20,000 (Saudi Gazette); highlighted 40% reduction in chronic-disease mortality and 60% decrease in road-traffic fatalities (Arab News May 2026); inaugurated 37 health projects costing SR 1.6 billion in Hail region."
              - "Owns the Vision 2030 Health Sector Transformation Program: 21 Health Clusters payer-provider separation, single-payer Council of Health Insurance design, e-health (Sehhaty, Tawakkalna-Health) infrastructure, SFDA regulation, SCFHS licensing, and Saudi G20 / GHI multilateral positioning."
              - "Hook: Health Sector Transformation Program, Health Clusters payer-provider separation, single-payer CHI design, Hajj health-services, AI in clinical workflows, SFDA fast-track approvals, biomanufacturing localisation under Vision 2030 land."
          - Tone advice:
              - "Open with Vision 2030 Transformation Program, Health Clusters, Hajj services, SFDA fast-track and AI — these are Al-Jalajel's authored, sustained public lines."
              - "Do not pitch as if the MoH were a single payer — the CHI single-payer design is under construction; current arrangements still vary by cluster and parallel system."
```

## 11. Out-of-band notes

For roles unfilled or in transition.

## 12. Open questions

- Named Deputy Ministers under Al-Jalajel with currency verified.
- Director-Generals of the 21 Health Clusters with currency verified.
- CEO Council of Health Insurance with currency verified.
- CEO Saudi Center for Disease Prevention and Control with currency verified.
- President KFSHRC and President NGHA with currency verified.
- Shoura Council Health Committee Chair with currency verified.
- Presidents of the Saudi Medical Association, Saudi Nursing Society and Saudi Pharmaceutical Society with currency verified.
