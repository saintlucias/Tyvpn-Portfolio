# 출처와 검증 범위

[README](../README.md) · [기능 상세](FEATURES.md) · [기술 설계](ARCHITECTURE.md)

## 작성 기준

| 항목 | 기준 |
| --- | --- |
| 원본 저장소 | [saintlucias/TYVPN](https://github.com/saintlucias/TYVPN) |
| 원본 브랜치 | `V3` |
| 기준 커밋 | [`94ed53687e826fc41490a00d769c1f85e635106a`](https://github.com/saintlucias/TYVPN/commit/94ed53687e826fc41490a00d769c1f85e635106a) |
| 커밋 날짜 | 2026-11-09 |
| 문서 검토일 | 2026-11-10 |
| 공개 포트폴리오 | [saintlucias/Tyvpn-Portfolio](https://github.com/saintlucias/Tyvpn-Portfolio) |
| 화면 출처 | 원본 `public/readme/`의 PNG 19개 |

문서는 로컬 원본 소스, 기존 README, 화면 캡처를 대조해 작성했습니다. 확인 당시 원본 작업 트리에 수정 사항은 없었습니다. 원본 애플리케이션은 변경하지 않았습니다.

## 기능별 코드 근거

모든 링크는 문서 기준 커밋에 고정했습니다. 원본 저장소가 비공개인 경우 열람 권한이 필요합니다.

| 설명 | 원본 파일 |
| --- | --- |
| 기본 레이아웃·공통 UI | [layout.tsx](https://github.com/saintlucias/TYVPN/blob/94ed53687e826fc41490a00d769c1f85e635106a/src/app/layout.tsx) |
| VPN 메인 구성 | [Main.tsx](https://github.com/saintlucias/TYVPN/blob/94ed53687e826fc41490a00d769c1f85e635106a/src/components/layout/main/Main.tsx) |
| 임대 PC 구성 | [RentalPCMain.tsx](https://github.com/saintlucias/TYVPN/blob/94ed53687e826fc41490a00d769c1f85e635106a/src/components/layout/rental-pc/RentalPCMain.tsx) |
| 상품·FAQ·상담 데이터 | [item.ts](https://github.com/saintlucias/TYVPN/blob/94ed53687e826fc41490a00d769c1f85e635106a/src/contants/item.ts) |
| VPN 요금 카드·상담 열기 | [Price.tsx](https://github.com/saintlucias/TYVPN/blob/94ed53687e826fc41490a00d769c1f85e635106a/src/components/module/price/Price.tsx) |
| PC 요금 카드·품절 상태 전달 | [RentalPrice.tsx](https://github.com/saintlucias/TYVPN/blob/94ed53687e826fc41490a00d769c1f85e635106a/src/components/module/price/RentalPrice.tsx) |
| 내비게이션 조건 | [useScrollHideView.ts](https://github.com/saintlucias/TYVPN/blob/94ed53687e826fc41490a00d769c1f85e635106a/src/hooks/useScrollHideView.ts) |
| 커튼 효과 | [Contact.tsx](https://github.com/saintlucias/TYVPN/blob/94ed53687e826fc41490a00d769c1f85e635106a/src/components/module/contact/Contact.tsx), [useScrollCurtain.ts](https://github.com/saintlucias/TYVPN/blob/94ed53687e826fc41490a00d769c1f85e635106a/src/hooks/useScrollCurtain.ts) |
| Sticky 전환 | [ChangedSticky.tsx](https://github.com/saintlucias/TYVPN/blob/94ed53687e826fc41490a00d769c1f85e635106a/src/components/module/changed-contents/ChangedSticky.tsx), [useScrollChangeContainer.ts](https://github.com/saintlucias/TYVPN/blob/94ed53687e826fc41490a00d769c1f85e635106a/src/hooks/useScrollChangeContainer.ts) |
| 상담 채널·Wechat QR | [ContactModal.tsx](https://github.com/saintlucias/TYVPN/blob/94ed53687e826fc41490a00d769c1f85e635106a/src/components/module/modal/ContactModal.tsx), [Wechat.tsx](https://github.com/saintlucias/TYVPN/blob/94ed53687e826fc41490a00d769c1f85e635106a/src/components/module/modal/Wechat.tsx) |
| 모달 상태·바깥 클릭 | [useOpenContainer.ts](https://github.com/saintlucias/TYVPN/blob/94ed53687e826fc41490a00d769c1f85e635106a/src/hooks/useOpenContainer.ts) |
| FAQ | [QnA.tsx](https://github.com/saintlucias/TYVPN/blob/94ed53687e826fc41490a00d769c1f85e635106a/src/components/module/qna/QnA.tsx), [RentalQnA.tsx](https://github.com/saintlucias/TYVPN/blob/94ed53687e826fc41490a00d769c1f85e635106a/src/components/module/qna/RentalQnA.tsx), [Accordion.tsx](https://github.com/saintlucias/TYVPN/blob/94ed53687e826fc41490a00d769c1f85e635106a/src/components/basic/container/Accordion.tsx) |
| IP 표시·판별 | [TopDisplayIP.tsx](https://github.com/saintlucias/TYVPN/blob/94ed53687e826fc41490a00d769c1f85e635106a/src/app/TopDisplayIP.tsx), [convertIP.ts](https://github.com/saintlucias/TYVPN/blob/94ed53687e826fc41490a00d769c1f85e635106a/src/utils/convertIP.ts) |
| IP 응답 핸들러 | [functions/api/ip.ts](https://github.com/saintlucias/TYVPN/blob/94ed53687e826fc41490a00d769c1f85e635106a/functions/api/ip.ts) |
| 스타일·애니메이션 | [module.module.scss](https://github.com/saintlucias/TYVPN/blob/94ed53687e826fc41490a00d769c1f85e635106a/src/styles/module.module.scss), [_common.scss](https://github.com/saintlucias/TYVPN/blob/94ed53687e826fc41490a00d769c1f85e635106a/src/styles/_common.scss) |
| 메타데이터·JSON-LD | [seo.ts](https://github.com/saintlucias/TYVPN/blob/94ed53687e826fc41490a00d769c1f85e635106a/src/app/seo.ts), [JsonLd.tsx](https://github.com/saintlucias/TYVPN/blob/94ed53687e826fc41490a00d769c1f85e635106a/src/app/JsonLd.tsx) |
| 페이지별 구조화 데이터 | [VPN 메인](https://github.com/saintlucias/TYVPN/blob/94ed53687e826fc41490a00d769c1f85e635106a/src/app/page.tsx), [임대 PC](https://github.com/saintlucias/TYVPN/blob/94ed53687e826fc41490a00d769c1f85e635106a/src/app/Rental-PC/page.tsx), [VPN 요금](https://github.com/saintlucias/TYVPN/blob/94ed53687e826fc41490a00d769c1f85e635106a/src/app/price/vpn/page.tsx), [PC 요금](https://github.com/saintlucias/TYVPN/blob/94ed53687e826fc41490a00d769c1f85e635106a/src/app/price/rental-pc/page.tsx) |
| 검색 엔진 탐색 | [sitemap.ts](https://github.com/saintlucias/TYVPN/blob/94ed53687e826fc41490a00d769c1f85e635106a/src/app/sitemap.ts), [robots.ts](https://github.com/saintlucias/TYVPN/blob/94ed53687e826fc41490a00d769c1f85e635106a/src/app/robots.ts) |
| 정적 출력·이미지 설정 | [next.config.ts](https://github.com/saintlucias/TYVPN/blob/94ed53687e826fc41490a00d769c1f85e635106a/next.config.ts) |
| 기술 버전 | [package-lock.json](https://github.com/saintlucias/TYVPN/blob/94ed53687e826fc41490a00d769c1f85e635106a/package-lock.json) |
| 기존 설명·캡처 | [원본 README](https://github.com/saintlucias/TYVPN/blob/94ed53687e826fc41490a00d769c1f85e635106a/README.md), [public/readme](https://github.com/saintlucias/TYVPN/tree/94ed53687e826fc41490a00d769c1f85e635106a/public/readme) |

## 화면 자료

`assets/screenshots/`는 원본 `public/readme/`의 폴더·파일명을 유지합니다. 이미지 수정이나 신규 촬영은 하지 않았습니다. [manifest.json](../assets/screenshots/manifest.json)에 원본 경로, PNG 크기, 파일 용량, SHA-256 해시를 기록했습니다.

- 일부 장점 캡처의 `WHT` 문구는 기준 소스에서 `WHY`로 수정되어 있습니다.
- 원본 README의 효과 명칭과 현재 사용 훅이 다른 부분은 [인터랙션 문서](INTERACTIONS.md)에 구분했습니다.
- 원본 IP 바의 일부 마스킹을 포함해 이미지에 있던 내용은 그대로 유지했습니다.
- 운영 가격·판매 여부·서비스 문구를 최신 정보로 보증하는 자료는 아닙니다.
- 캡처·브랜드 이미지·폰트의 제3자 재사용 허가는 이 저장소에서 별도로 부여하지 않습니다.

## 수행한 확인

- 4개 실제 페이지 진입점과 그 하위 컴포넌트·훅 연결을 확인했습니다.
- 상품 카드 3종·PC 카드 5종·FAQ 12개/8개의 소스 데이터를 확인했습니다.
- 스크롤·모달·FAQ·IP 응답·SEO 코드와 기존 설명을 대조했습니다.
- 기존 PNG 19개를 열어 화면과 설명을 대조했습니다.
- 문서 내 상대 링크·이미지 경로, 파일 목록·원본 이미지 해시를 검사했습니다.

## 별도 검증하지 않은 내용

운영 사이트의 기능 테스트, Cloudflare 배포 상태, 외부 상담 연결 성공, 신규 빌드·테스트, 모바일 실기기와 접근성 전수 검사, Lighthouse·Core Web Vitals, VPN·원격 PC의 실제 동작·보안·성능은 검증하지 않았습니다.

실측 성과와 개발 기간·팀 구성·개인 기여율을 임의로 작성하지 않았습니다. 기능의 존재는 코드에서 확인한 범위이며 사용자·사업 효과는 기대 효과로 구분했습니다.
