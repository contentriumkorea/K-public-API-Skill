# Catalog guide / 한국 API 탐색 안내

This small navigation reference is bundled so the skill does not depend on files outside its installation folder. It is not a complete or continuously synchronized API database. Candidate links below are discovery leads, not verified availability or pricing claims.

## Source and provenance

- Distribution fork: https://github.com/contentriumkorea/K-publid-API-Skill
- Original catalog: https://github.com/yybmion/public-apis-4Kr
- Source snapshot used to prepare this guide: `5f0570083484a5b8ce10d71628f16eb811a3295e` (reviewed 2026-09-04).
- Pinned Korean catalog: https://github.com/yybmion/public-apis-4Kr/blob/5f0570083484a5b8ce10d71628f16eb811a3295e/README.md
- Live Korean catalog: https://github.com/contentriumkorea/K-publid-API-Skill/blob/main/README.md
- Machine-readable Korean catalog: https://raw.githubusercontent.com/contentriumkorea/K-publid-API-Skill/main/README.md
- Live global catalog, explained in Korean: https://github.com/contentriumkorea/K-publid-API-Skill/blob/main/GLOBAL_PUBLIC_APIS_KR.md
- Machine-readable global catalog: https://raw.githubusercontent.com/contentriumkorea/K-publid-API-Skill/main/GLOBAL_PUBLIC_APIS_KR.md
- English Korean-services catalog: https://github.com/contentriumkorea/K-publid-API-Skill/blob/main/README_EN.md

Use the live fork for discovery. If it is unavailable or appears stale, consult the original repository and record which revision or page was actually read. Neither repository is the API provider. Final access, field, freshness, price, and reuse claims come from the current provider documentation.

## Topic routing

Search the Korean catalog's exact headings and the adjacent rows. Keywords may occur in more than one category.

| User need | Catalog headings | Helpful search terms |
| --- | --- | --- |
| Public services and local data | 정부 & 공공기관; 지역별 공공데이터 | 공공데이터포털, 서울 열린데이터광장, 지역명 |
| Maps, addresses, places | 지도 & 위치; 네이버; 카카오 | 지도, 좌표, 주소, Geocoding |
| Weather, air quality | 날씨 & 환경; 정부 & 공공기관 | 기상청, 예보, 에어코리아 |
| Charging stations and status | 에너지 & 전력; 날씨 & 환경 | 전기차, 충전소, 충전기, 운영기관 |
| Buses, rail, traffic | 교통; 지역별 공공데이터 | 버스, 열차, 도착, 교통량 |
| Tourism, events, content | 문화 & 관광; 미디어 & 콘텐츠 | TourAPI, 관광, 축제, 영화 |
| Property and business | 부동산; 비즈니스 & 기업; 정부 & 공공기관 | 실거래가, 사업자, 공시 |
| Payments and economic data | 금융 & 결제; 생활경제; 통계 & 지표 | 결제, 환율, 한국은행, 인증 |
| Safety, health, education | 공공안전; 의료 & 보건; 교육 | 재난, 병원, 학교 |
| Other Korean services | Remaining Korean catalog headings | Search the user's domain and needed fields |
| Global alternatives | GLOBAL_PUBLIC_APIS_KR.md headings | 날씨, 지오코딩, 오픈 데이터, 개발, 금융 |

## A few starting links

These links were present in the source snapshot. They deliberately carry no asserted current price, quota, or permission. Without web access, give only candidate names/links and pending checks.

| Candidate | Provider page from the catalog | What to establish before use |
| --- | --- | --- |
| 공공데이터포털 | https://www.data.go.kr/ | Find the exact dataset or API and its owning institution |
| 기상청 단기예보 | https://www.data.go.kr/data/15084084/openapi.do | Current operations, forecast times, coordinates, service key |
| 카카오맵 | https://apis.map.kakao.com/web/guide/ | Distinguish map SDK, place search, and any separate routing service |
| 네이버 지도 | https://www.ncloud.com/product/applicationService/maps | Product/API selection, client restrictions, quota and billing |
| 한국관광공사 TourAPI | https://api.visitkorea.or.kr/ | Current version, language coverage, access terms |
| 전국전기차충전소표준데이터 | https://www.data.go.kr/data/15013115/standard.do | Standard-data/download delivery and freshness; do not assume live status |
| 전기차충전기정보 | https://chargeinfo.ksga.org/front/cs/api/infomation | Provider access procedure, operator coverage, current endpoint |
| 전기차 충전소 정보 | https://www.data.go.kr/data/15076352/openapi.do | Exact fields, status updates, key requirements, reuse terms |

The charging rows intentionally cover both `날씨 & 환경` and `에너지 & 전력`. Do not confuse station location, charger availability, and charging prices: the presence of one does not establish the others.

## Evidence to report

For each shortlisted API, include the official source and a checked-on date. Distinguish:

- **Catalog candidate:** listed in the repository; provider conditions not yet checked.
- **Documentation checked:** specific claims supported by the provider page; not a successful live API call.
- **Live call tested:** an authorized request was actually executed and its outcome inspected.

With offline or blocked access, state the missing evidence and continue with a clearly provisional shortlist. An old link-health report does not establish current API access or commercial permission.
