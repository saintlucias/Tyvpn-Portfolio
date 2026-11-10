# 프로젝트 자료와 코드 참조

[README](../README.md) · [기능 상세](FEATURES.md) · [기술 설계](ARCHITECTURE.md)

## 프로젝트 기준

| 항목 | 기준 |
| --- | --- |
| 원본 저장소 | [saintlucias/TYVPN](https://github.com/saintlucias/TYVPN) |
| 원본 브랜치 | `V3` |
| 기준 커밋 | [`94ed53687e826fc41490a00d769c1f85e635106a`](https://github.com/saintlucias/TYVPN/commit/94ed53687e826fc41490a00d769c1f85e635106a) |
| 커밋 날짜 | 2026-11-09 |
| 공개 포트폴리오 | [saintlucias/Tyvpn-Portfolio](https://github.com/saintlucias/Tyvpn-Portfolio) |
| 화면 출처 | 원본 `public/readme/`의 PNG 19개 |

## 기능별 코드 참조

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

- 원본 이미지: `public/readme/`의 PNG 19개.
- 화면 갤러리: [SCREENS.md](SCREENS.md).
- 이미지 정보: [manifest.json](../assets/screenshots/manifest.json)의 원본 경로·크기·용량·SHA-256 해시.
