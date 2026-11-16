<div align="center">

# TYVPN 3.0

### 서비스 소개부터 요금제 비교와 상담 연결까지

**Next.js · React · TypeScript · SCSS Modules · Cloudflare Pages Functions**

[서비스 웹사이트](https://tyvpn.kr/) · [원본 소스](https://github.com/saintlucias/TYVPN) · [화면 갤러리](docs/SCREENS.md) · [기능 상세](docs/FEATURES.md) · [인터랙션 효과](docs/INTERACTIONS.md)

</div>

![TYVPN VPN 메인 — 전용 IP 서비스 소개와 요금제 진입](assets/screenshots/main/main_tyvpn_1.png)

VPN과 원격 임대 PC의 소개·가격 화면을 각각 제공하며, 긴 랜딩 페이지에 스크롤 인터랙션과 고정 콘텐츠를 배치함. 상품 카드, FAQ, 상담 모달은 공통 컴포넌트로 구성하고, 검색·공유를 위한 페이지별 메타데이터와 구조화 데이터를 작성함.

## 주요 구현 기능

| 구분 | 구현 내용 |
| --- | --- |
| 서비스 소개 | VPN·전용 IP 랜딩, 원격 임대 PC 랜딩, 서비스별 배너와 CTA |
| 요금·상품 비교 | VPN 요금 카드 3종, 임대 PC 사양·가격 카드 5종, 추천·품절 표시 |
| 상담 연결 | Kakao·Telegram 외부 링크, Wechat QR 모달, 모달 바깥 클릭 닫기 |
| FAQ | VPN 12개·임대 PC 8개 문항, 질문별 독립적인 열기·닫기 |
| 탐색 | 공통 내비게이션, QNA 앵커, 요금 페이지 이동, 부드러운 맨 위 이동 |
| 스크롤 효과 | 좌우 커튼 개방, Sticky 요약, 3단계 콘텐츠 전환, 내비게이션 표시·숨김 |
| CSS 애니메이션 | 소개 영역의 파동·점멸 효과, 버튼·카드 전환 스타일 |
| IP 표시 | 메인에서 `/api/ip` 조회, Cloudflare 요청 헤더 기반 IP 응답 |
| 반응형 스타일 | 1279px·839px 기준 레이아웃·글자·이미지 크기 조정 |
| SEO | 페이지별 Metadata, Open Graph·Twitter 카드, JSON-LD, sitemap·robots |

## 웹페이지 구성

| 화면 | 경로 | 주요 구성 |
| --- | --- | --- |
| VPN 메인 | `/` | IP 바, 히어로, 소개 애니메이션, 요금 CTA, 장점 카드, 스크롤 전환, FAQ |
| 원격 임대 PC | `/Rental-PC` | 히어로, 이미지·텍스트 교차 배치, PC 사양 카드, FAQ |
| VPN 요금 | `/price/vpn` | 상품·가격·제공 항목 비교, 상담 모달 |
| 원격 임대 PC 요금 | `/price/rental-pc` | 월 요금·CPU·GPU·RAM·SSD 비교, 품절 표시, 상담 모달 |

```mermaid
flowchart LR
    A[VPN 메인] --> B[VPN 요금]
    C[원격 임대 PC 소개] --> D[원격 임대 PC 요금]
    A <--> C
    B --> E[상담 채널 선택]
    D --> E
    E --> F[Kakao / Telegram 외부 이동]
    E --> G[Wechat QR 확인]
```

### 서비스 소개

![VPN 장점 — 카드 목록과 Sticky 요약 영역](assets/screenshots/main/main_tyvpn_4_2.png)

![VPN 스크롤 콘텐츠 — 배경 이미지와 설명, 요금 페이지 이동 버튼](assets/screenshots/main/main_tyvpn_5_3.png)

### 원격 임대 PC 소개

VPN과 다른 배너·소개 구성을 사용하면서 공통 탐색과 버튼 스타일을 유지함. PC의 사양과 월 이용료를 카드로 나열하고 요금 페이지로 연결함.

![원격 임대 PC 메인 — 서비스 배너와 요금제 CTA](assets/screenshots/rental-pc/rentalpc_tyvpn_1.png)

### 요금제 비교

VPN 상품은 가격과 제공 항목을, 임대 PC는 하드웨어 사양과 월 요금을 비교할 수 있음. 구매 버튼은 상담 채널 선택 화면을 오픈함.

![VPN 요금 — 상품 카드와 추천 상품 강조](assets/screenshots/vpn-price/vpnprice_tyvpn_1.png)

## 기술 구성과 설계

| 영역 | 기술·구성 | 적용 내용 |
| --- | --- | --- |
| 프레임워크 | Next.js 16.2.9, App Router | 4개 페이지, 공통 레이아웃, Metadata |
| UI | React 19.2.1, TypeScript 5.9.3 | 컴포넌트·상품 타입, 모달·FAQ 상태 관리 |
| 스타일 | Sass 1.94.2, SCSS Modules | 컴포넌트 스타일 분리, 공통 색상·반응형 기준 |
| 인터랙션 | 커스텀 훅, CSS animation·transition | 스크롤 이벤트, 진행률 계산, Sticky·파동 효과 |
| 배포 구성 | `output: "export"` | HTML·CSS·JS 정적 출력 |
| 요청 처리 | Cloudflare Pages Functions | 요청 헤더에서 IP를 읽는 별도 `/api/ip` 핸들러 |
| 검색·공유 | Metadata, JSON-LD, sitemap, robots | 문서·서비스·FAQ 정보 제공 |

- **서비스별 화면 분리:** 소개와 요금을 별도 경로로 나누면서 공통 헤더·푸터를 재사용함.
- **데이터와 표현 분리:** 상품·사양·FAQ·상담 채널을 타입이 있는 배열로 정의하고 공통 UI에 전달함.
- **스크롤 동작 분리:** 커튼·현재 콘텐츠 인덱스·내비게이션 상태를 커스텀 훅에서 계산함. 커튼·콘텐츠 전환 훅은 `requestAnimationFrame`으로 이벤트 갱신을 조절함.
- **검색 정보의 공통화:** `createPageMetadata`로 페이지별 제목·설명·URL·공유 이미지를 구성하고 FAQ 데이터로 구조화 데이터를 생성함.

[기술 설계](docs/ARCHITECTURE.md) · [인터랙션 구현 상세](docs/INTERACTIONS.md)


---

[기능 상세](docs/FEATURES.md) · [화면 갤러리](docs/SCREENS.md) · [인터랙션 효과](docs/INTERACTIONS.md) · [기술 설계](docs/ARCHITECTURE.md) · [코드 참조](docs/SOURCE.md)
