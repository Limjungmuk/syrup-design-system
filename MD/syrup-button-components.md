# Syrup Design System — Button 컴포넌트

| 항목 | 값 |
| --- | --- |
| Figma File | [Syrup_Design-System](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System) |
| Page / Section | `Button` 페이지 → [Button 섹션 `8506:6315`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=8506-6315) |
| 마스터 섹션 크기 | 1440 × 3107 |
| 기준일 | 2026-11-11 (가이드라인 6개·Usage A~K·컬러 조정 기준 반영) |
| 관련 문서 | [syrup-design-tokens.md](syrup-design-tokens.md) · [syrup-dialog-components.md](syrup-dialog-components.md) · [syrup-alert-components.md](syrup-alert-components.md) · [syrup-badge-components.md](syrup-badge-components.md) · [syrup-banner-components.md](syrup-banner-components.md) · [syrup-border-components.md](syrup-border-components.md) · [syrup-bottom-info-components.md](syrup-bottom-info-components.md) · [syrup-bottom-cta-components.md](syrup-bottom-cta-components.md) · [syrup-bottom-sheet-components.md](syrup-bottom-sheet-components.md) · [syrup-bubble-components.md](syrup-bubble-components.md) · [syrup-ad-components.md](syrup-ad-components.md) · [syrup-checkbox-components.md](syrup-checkbox-components.md) · [syrup-chip-components.md](syrup-chip-components.md) · [syrup-card-components.md](syrup-card-components.md) · [syrup-dim-components.md](syrup-dim-components.md) · [syrup-grid-list-components.md](syrup-grid-list-components.md) · [syrup-grid-scroll-components.md](syrup-grid-scroll-components.md) · [syrup-header-components.md](syrup-header-components.md) · [syrup-icon-button-components.md](syrup-icon-button-components.md) · [syrup-indicator-components.md](syrup-indicator-components.md) · [syrup-keypad-components.md](syrup-keypad-components.md) · [syrup-label-components.md](syrup-label-components.md) · [syrup-list-footer-components.md](syrup-list-footer-components.md) · [syrup-list-header-components.md](syrup-list-header-components.md) · [syrup-list-row-components.md](syrup-list-row-components.md) · [syrup-loader-components.md](syrup-loader-components.md) · [syrup-lottie-components.md](syrup-lottie-components.md) · [syrup-product-grid-components.md](syrup-product-grid-components.md) · [syrup-product-list-components.md](syrup-product-list-components.md) · [syrup-product-scroll-components.md](syrup-product-scroll-components.md) · [syrup-progress-stepper-components.md](syrup-progress-stepper-components.md) · [syrup-result-components.md](syrup-result-components.md) · [syrup-search-field-components.md](syrup-search-field-components.md) · [syrup-stepper-components.md](syrup-stepper-components.md) · [syrup-swipe-components.md](syrup-swipe-components.md) · [syrup-switch-components.md](syrup-switch-components.md) · [syrup-tab-components.md](syrup-tab-components.md) · [syrup-tab-bar-components.md](syrup-tab-bar-components.md) · [syrup-text-button-components.md](syrup-text-button-components.md) · [syrup-text-field-components.md](syrup-text-field-components.md) · [syrup-ticker-components.md](syrup-ticker-components.md) · [syrup-toast-components.md](syrup-toast-components.md) |

> **화면에서 가장 중요한 행동을 강조하는 기본 버튼이에요.**
> 사용자가 다음 단계로 이동하거나 주요 작업을 완료할 때 사용해요.

---

## 공개 에셋 이름 정리

2026-11-11 아래 원본의 `.primitive / ` 접두사만 제거했어요. 노드·컴포넌트 키·variant·인스턴스 연결은 유지했으며 게시 작업은 별도로 진행해요. 숨김 유지·검토 대상의 접두사는 유지해요.

| 현재 전체 이름 | 원본 노드 |
| --- | --- |
| `Button / Icon` | `8680:42699` |

## 목차

1. [구성 한눈에 보기](#구성-한눈에-보기)
2. [Button — Master Component](#1-button--master-component)
3. [파생 버튼 4종](#2-파생-버튼-4종)
4. [Child Item](#3-child-item)
5. [가이드라인](#가이드라인)
6. [Usage — 사용 예제](#usage--사용-예제)
7. [컬러 조정 허용 범위](#컬러-조정-허용-범위)
8. [예제 레이아웃과 AI 사용 기준](#예제-레이아웃과-ai-사용-기준)
9. [설계 규칙 요약](#설계-규칙-요약)
10. [점검 필요 사항](#점검-필요-사항)

---

## 구성 한눈에 보기

현재 페이지는 마스터 섹션과 Guidelines·Usage, 유형별 참고 섹션으로 구성해요. 기존 규격·정리 이력은 2026-10-01 기록이며 현재 사용 기준은 아래 가이드라인·Usage를 따라요.

페이지는 `Master Component` → `Child Item`(Icons · Lower Item) 구조이며, 컴포넌트는 **9개**입니다. (2026-10-01 `Quiz / Up`·`Quiz / Down` 병합으로 10개 → 9개)

| # | 이름 | 타입 | Variant / Props | 크기 |
| --- | --- | --- | --- | --- |
| 1 | `Button` | Component Set | `Size` × `Variant` × `Disabled` × `Checked` (**40종**) | 높이 26~56 |
| 2 | `Button / Description` | Component | `Lower Item` BOOLEAN | 360 × 84 |
| 3 | `Button / News` | Component Set | `State` 4종 | 78 × 40 |
| 4 | `Button / Alert` | Component Set | `Alert` 2종 | 65 × 18 / 77 × 18 |
| 5 | `Button / Quiz` | Component Set | `Direction` × `Progress` (**4종**) | 160 × 120 |
| 6 | `Button / Icon` | Component Set | `Type` 3종 | 20 × 20 |
| 7 | `.primitive / Button / Alert` | Component Set | `Check` 2종 | 16 × 16 |
| 8 | `.primitive / Button / Gold` | Component | — | 24 × 24 |
| 9 | `.primitive / Button / Lower Item` | Component Set | `Type` × `Highlight` 3종 | 360 × 28~35 |

---

## 1. Button — Master Component

**Node** `8662:27880` · Component Set · **40 variants**

### Properties

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `Size` | VARIANT | `XS` | `XS` · `S` · `M` · `L` · `XL` |
| `Variant` | VARIANT | `Fill` | `Fill` · `Weak` · `Outline` · `Outline_Secondary` · `Outline_Primary` |
| `Disabled` | VARIANT | `False` | `False` · `True` |
| `Checked` | VARIANT | `False` | `False` · `True` |
| `Icon` | BOOLEAN | `false` | — |

### Variant 구성 — 사이즈마다 정확히 8개

5개 사이즈 × 8개 = 40. 사이즈별 8개의 내역은 다음과 같습니다.

| # | Variant 조합 | 성격 | 배경 | 테두리 | 라벨 색 |
| --- | --- | --- | --- | --- | --- |
| 1 | `Fill` | 기본 (주 액션) | `Color/Primary_Orange` | — | `Color/Gray_White` |
| 2 | `Fill` + `Disabled` | 비활성 | `Color/Gray_600` | — | `Color/Gray_White` |
| 3 | `Fill` + `Checked` | 리워드 처리 후 표시 | `Color/Gray_White` | — | `Color/Primary_Orange` |
| 4 | `Weak` | 보조 | `Color/Gray_900` | — | `Color/Gray_200` |
| 5 | `Weak` + `Disabled` | 보조 비활성 | `Color/Gray_900` | — | `Color/Gray_600` |
| 6 | `Outline_Primary` | 외곽선 · 강조 | `Color/Gray_White` | `Color/Primary_Orange` | `Color/Primary_Orange` |
| 7 | `Outline_Secondary` | 외곽선 · 중립 | `Color/Gray_White` | `Color/Gray_800` | `Color/Gray_Black` |
| 8 | `Outline` + `Disabled` | 외곽선 비활성 | `Color/Gray_White` | `Color/Gray_800` | `Color/Gray_600` |

> ⚠️ **`Variant=Outline`은 `Disabled=True` 조합으로만 존재합니다.** 활성 외곽선 버튼은 `Outline_Primary` · `Outline_Secondary`입니다. 아래 점검 1번 참고.

### Size 램프

| Size | 높이 | 좌우 Padding | Gap | Radius | 라벨 스타일 |
| --- | --- | --- | --- | --- | --- |
| `XS` | 26 | `Spacing/200` (8) | `Spacing/50` (2) | `Corner radius/150` (6) | `t1050_14_bold` |
| `S` | 30 | `Spacing/250` (10) | `Spacing/50` (2) | `Corner radius/150` (6) | `t1050_14_bold` |
| `M` | 38 | `Spacing/300` (12) | `Spacing/50` (2) | `Corner radius/150` (6) | `t1000_15_bold` |
| `L` | 48 | `Spacing/300` (12) | `Spacing/100` (4) | `Corner radius/250` (10) | `t800_17_bold` |
| `XL` | 56 | `Spacing/700` (28) | `Spacing/100` (4) | `Corner radius/250` (10) | `t800_17_bold` |

- 상하 Padding은 전 사이즈 `Spacing/50`(2)로 동일합니다. 높이는 padding이 아니라 고정값으로 결정됩니다.
- **`M`과 `L`의 좌우 Padding이 12로 같습니다.** 높이는 38 → 48로 벌어지는데 여백만 동일합니다.
- 테두리 두께는 전 variant `1`입니다.

---

## 2. 파생 버튼 4종

메인 세트와 별개로 특정 맥락 전용 버튼이 있습니다.

### Button / Description

**Node** `8758:15797` · Component · 360 × 84

| Property | Type | Default |
| --- | --- | --- |
| `Lower Item` | BOOLEAN | `true` |

`Button` 인스턴스 + `.primitive / Button / Lower Item` 조합입니다. 버튼 아래에 설명이나 링크를 덧붙이는 구조로, Bottom CTA의 `Upper Item`과 역할이 유사합니다.

### Button / News

**Node** `10030:136607` · Component Set · 4 variants · 78 × 40

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `State` | VARIANT | `Default` | `Default` · `Progress` · `Available` · `Completed` |

뉴스를 읽고 금(포인트)을 받는 흐름의 **단계별 상태**를 나타냅니다. (2026-10-01 `Property 1` / `Variant2~4` → `State` 정리)

| State | 배경 | 라벨 색 | 부가 레이어 | 의미 |
| --- | --- | --- | --- | --- |
| `Default` | `Color/Gray_White` | `Color/Secondary_Brown_Gray` | `Bubble` 툴팁 | 시작 전 — "스크롤해서 읽고, 버튼 눌러요!" 안내 |
| `Progress` | `Color/Gray_White` | `Color/Secondary_Brown_Gray` | `stroke_active` 진행 호 | 읽는 중 |
| `Available` | `Color/Primary_Orange` | `Color/Gray_White` | — | 받을 수 있음 |
| `Completed` | `Color/Third_Pastel_Coral` | `Color/Primary_Orange` | — | 받기 완료 |

**`Default` → `Progress` → `Available` → `Completed`** 순서가 그대로 사용자 동선입니다. 앞의 두 단계는 흰 배경으로 비활성에 가깝게, 뒤의 두 단계는 오렌지 계열로 행동을 유도하거나 완료를 알립니다.

공통 — Padding `11 / Spacing/300(12)`, Gap `Spacing/250`(10), Radius `Corner radius/circle`, 라벨 `t1050_14_bold`, 샘플 "10금 받기"

### Button / Alert

**Node** `10035:149159` · Component Set · 2 variants

| Variant | 크기 | 라벨 | 라벨 색 |
| --- | --- | --- | --- |
| `Alert=True` | 77 × 18 | "알림받는중" | `Color/Primary_Orange` |
| `Alert=False` | 65 × 18 | "알림받기" | `Color/Gray_400` |

`.primitive / Button / Alert` 아이콘 + 텍스트, Gap `Spacing/50`(2), 라벨 `b400_14_regular`.

### Button / Quiz

**Node** `10027:134176` · Component Set · **4 variants** · 160 × 120

시세가 오를지 내릴지를 고르는 퀴즈 버튼입니다. 2026-10-01에 `Button / Quiz / Up`·`Button / Quiz / Down` **두 컴포넌트셋이 하나로 병합**됐습니다 → [점검 2](#2--기본-생성-이름-property-1--variant2-정리-2026-10-01-완료)

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `Direction` | VARIANT | `Up` | `Up` · `Down` |
| `Progress` | VARIANT | `Empty` | `Empty` · `Filled` |

2 × 2 = **4조합이 모두 존재하는 완전 매트릭스**입니다.

#### Direction — 방향

| Direction | 배경 | 오버레이 색 | 아이콘 | 라벨 |
| --- | --- | --- | --- | --- |
| `Up` | **#F3564F** (빨강) | **#D71900** | `syrup_img_24_goldquiz_arrowup` | "오른다" |
| `Down` | **#3D8BF7** (파랑) | **#0055CB** | `syrup_img_24_goldquiz_arrowdown` | "내린다" |

#### Progress — 참여 비율

| Progress | 오버레이 (`Rectangle`) | 퍼센트 텍스트 |
| --- | --- | --- |
| `Empty` | 숨김 | `0%` |
| `Filled` | 표시 | `Up` 34% · `Down` 66% |

하단에서 차오르는 **진한 색 막대로 투표 비율을 표시**하고, 그 값을 퍼센트 텍스트로 함께 보여줍니다. `Empty`는 아직 아무도 고르지 않은 0% 상태입니다.

> 오버레이 높이는 `Up` 36 · `Down` 73으로 샘플 값이며, 퍼센트와 정확히 비례하지는 않습니다. 실제 구현에서는 비율에 따라 높이가 계산됩니다.

공통 — Radius `Corner radius/400`(16), Gap `Spacing/200`(8), 라벨 `t600_21_bold` / 퍼센트 `t1300_15_medium`, 둘 다 `Color/Gray_White`

---

## 3. Child Item

### Icons

| 컴포넌트 | Variant | 크기 | 내용 |
| --- | --- | --- | --- |
| `Button / Icon` | `Kakao` · `Instagram` · `Number` | 20 × 20 | 소셜 로그인 아이콘 + 숫자 배지 |
| `.primitive / Button / Alert` | `Check=False` · `Check=True` | 16 × 16 | 알림 아이콘 |
| `.primitive / Button / Gold` | — | 24 × 24 | `syrup_img_dialog_btn_gold` |

- `Icon / Number`는 `t1060_13_bold` / `Color/Primary_Orange`로 숫자를 표시합니다.
- `Button / Alert`의 두 variant는 **레이어 구조가 완전히 같고 `Combined Shape`의 색만 다릅니다** — `Check=False` #777777, `Check=True` #FF6315.

### Lower Item

**Node** `8758:14928` · Component Set · 3 variants · 폭 360

| Variant | 크기 | Padding | 타이포 | 색상 |
| --- | --- | --- | --- | --- |
| `Description, Highlight=True` | 360 × 28 | `Spacing/250`(10) / `Spacing/400`(16) / 0 / `Spacing/400`(16) | `b400_14_regular` | `Color/Primary_Orange` |
| `Description, Highlight=False` | 360 × 28 | 〃 | `b400_14_regular` | `Color/Gray_400` |
| `Link Button, Highlight=False` | 360 × 35 | `Spacing/400`(16) / `Spacing/400`(16) / 0 / `Spacing/400`(16) | `b300_15_regular` | `Color/Gray_400` |

`Type` 2종(`Description` · `Link Button`) × `Highlight` 2종 = 4조합 중 **3개만 존재**합니다. `Highlight=True`는 `Description`에만 있습니다. (Bottom CTA의 Upper Item과 같은 패턴)

---

## 가이드라인

[Figma Guidelines](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11830-7493)

### 1. 행동의 중요도에 맞게 버튼을 구분해요

사용자가 우선 실행할 행동은 Fill로 강조하고, 함께 제공하는 보조 행동은 Weak나 Outline 계열로 구분해요.
버튼 문구는 실행할 행동을 구체적으로 표현하고 같은 영역에서 우선순위가 드러나도록 구성해요.

[Figma 가이드라인](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11830-7495)

### 2. 콘텐츠에 맞춰 버튼 컬러를 조정할 수 있어요

이미지나 콘텐츠의 배경에 맞춰 버튼의 배경색과 텍스트 컬러를 변경할 수 있어요. 필요한 경우 문구 일부에 강조색을 사용할 수 있어요.
버튼이 배경과 명확히 구분되고 문구가 잘 읽히도록 조합하며, 크기와 상태별 표현은 기존 컴포넌트 기준을 유지해요.
대응하는 컬러 토큰이 있으면 해당 토큰을 사용해요.

[Figma 가이드라인](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11833-3564)

### 3. 배치 영역에 맞는 크기를 사용해요

목록 안의 짧은 보상 버튼은 XS·S, 콘텐츠 안의 행동은 M·L, 넓은 주요 행동은 XL처럼 배치 영역에 맞춰 선택해요.
각 Size의 높이는 유지하고, 버튼 폭은 문구와 부모 영역에 맞게 조정해요.

[Figma 가이드라인](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11830-7551)

### 4. 실행 가능 여부와 처리 상태를 구분해요

현재 실행할 수 없는 행동은 Disabled=True로 표시하고, 보상 처리 후의 표현에는 Checked=True를 사용해요.
두 속성의 의미를 구분하고, 문구와 컬러가 실제 상태에 맞도록 사용해요.

[Figma 가이드라인](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11830-7593)

### 5. 필요한 보조 정보는 버튼 아래에 배치해요

행동의 조건이나 처리 안내가 필요하면 Button / Description의 하단 설명을 사용해요.
별도의 보조 행동은 하단 링크로 구분하고, 설명이 필요하지 않으면 Lower Item을 꺼서 버튼만 사용해요.

[Figma 가이드라인](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11830-7635)

### 6. 전용 버튼의 진행 상태를 맞춰 사용해요

뉴스 보상 버튼은 읽기 진행·받기 가능·수령 완료를 구분해요. 조건을 충족한 상태를 수령 완료로 표시하지 않아요.
알림 버튼은 설정 여부, 퀴즈 버튼은 선택 방향과 참여 진행에 맞는 전용 속성을 사용해요.

[Figma 가이드라인](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11830-7687)

---

## Usage — 사용 예제

[Figma Usage](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11830-7494)

| 예제 | 설명 | 링크 |
| --- | --- | --- |
| A. 주요 행동 | 사용자가 실행할 행동을 Fill 버튼으로 강조해요. 문구는 ‘할 일 추가하기’처럼 실행 결과를 예상할 수 있도록 작성해요. | [A](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11830-7725) |
| B. 두 행동의 우선순위 | 함께 제공하는 두 행동은 Weak와 Fill로 중요도를 구분해요. 보조 행동과 주요 행동의 배치를 일관되게 유지해요. | [B](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11830-7742) |
| C. 리워드 받기 | 리워드를 받을 수 있을 때 사용해요. 버튼에 받을 수 있는 금액을 표시해요. | [C](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11830-7771) |
| D. 테두리형 보조 행동 | 다시 시도하기처럼 콘텐츠와 관련된 행동을 테두리형 버튼으로 제공해요. 문구 길이에 맞는 폭을 사용해요. | [D](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11830-7786) |
| E. 비활성 상태 | 현재 실행할 수 없는 버튼은 Disabled=True로 표시해요. 표시 문구도 현재 상태에 맞춰 사용해요. | [E](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11830-7803) |
| F. 처리 후 표시 | 보상 처리 후에는 Checked=True로 표시해요. 문구와 컬러를 바꿔 처리 전 버튼과 구분해요. | [F](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11830-7820) |
| G. 처리 안내와 함께 사용 | 버튼 아래에 처리 시간 등 행동과 관련된 설명을 함께 보여줘요. 버튼 문구와 보조 설명의 역할을 구분해요. | [G](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11830-7835) |
| H. 보조 링크와 함께 사용 | 주요 행동은 버튼으로, 관련된 추가 행동은 하단 링크로 제공해요. 두 행동이 같은 동작처럼 보이지 않도록 구분해요. | [H](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11830-7855) |
| I. 두 방향 선택 | 오른다·내린다처럼 두 방향을 선택하는 구성을 사용해요. 방향과 참여 진행에 맞춰 문구·화살표·비율 표시를 함께 맞춰요. | [I](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11830-7877) |
| J. 읽기 진행과 보상 수령 | 안내·읽기 진행·받기 가능·수령 완료를 순서대로 보여줘요. 진행 표시와 버튼 컬러가 각 상태에 맞도록 사용해요. | [J](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11830-7906) |
| K. 알림 설정 상태 | 알림을 받을 수 있는 상태와 알림을 받는 중인 상태를 구분해요. 알림 아이콘과 문구를 설정 여부에 맞춰 함께 표시해요. | [K](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11830-7939) |

## 컬러 조정 허용 범위

- 이미지 위나 콘텐츠·제휴 화면처럼 기본 컬러 조합을 조정할 필요가 있으면 기존 Button 인스턴스의 배경색과 텍스트 컬러를 변경할 수 있어요.
- 필요한 경우 문구 일부에만 강조색을 적용할 수 있어요. 가이드라인 2번은 검정 배경·흰 문구의 ‘혜택 받기’와 검정 배경에서 ‘할 일 추가하기’ 부분을 주황색으로 강조한 예제를 비교해요.
- 배경과 버튼, 버튼과 문구가 명확히 구분되도록 조합해요. 대응하는 컬러 토큰이 있으면 해당 토큰을 사용해요.
- 컬러별로 새 베리언트를 추가하거나 같은 구조의 마스터를 복제할 필요는 없어요. 현재 마스터에 Black 같은 새 Variant 값이 추가된 것은 아니에요.
- Size의 높이·패딩·라운드·타이포와 상태별 의미는 기존 컴포넌트 기준을 유지해요. 배경을 바꿨다는 이유로 Disabled·Checked 상태를 같은 모양으로 표시하지 않아요.
- 혼합 색상 문구는 글자 구간별 색상을 유지해요. 전체 텍스트에 단일 컬러를 다시 적용해 강조 구간을 없애지 않아요.
- 이 기준은 버튼 컬러 조정을 허용하는 범위예요. 모든 버튼을 검정으로 바꾸라는 규칙이나 임의의 크기·구조 변경을 허용하는 기준이 아니에요.

## 예제 레이아웃과 AI 사용 기준

- Guidelines는 **960 × 1949**, Usage는 **4560 × 524**예요. 기존 섹션과 동일한 흰 배경·모서리 24를 사용해요.
- Usage A~K 11개를 **가로 한 줄**로 배치해요. 예제 폭 360, 예제 간격 40, 섹션 상하좌우 여백 100을 유지해요.
- 가장 긴 설명 영역 높이에 맞춰 예제 시작점을 정렬해요. 설명 영역 끝과 Slot 사이는 50이에요.
- Slot은 패딩 0, 좌측·상단 정렬, 높이 Hug예요. 단일 컴포넌트는 직접 배치하고 두 버튼처럼 간격이 필요한 경우에만 Auto Layout 묶음을 사용해요.
- 문서 Slot의 패딩 0과 Button 자체의 패딩은 서로 다른 값이에요. 문서 정렬을 이유로 기본 버튼의 내부 여백을 일괄 제거하지 않아요.
- 단일 Button의 Size 높이는 XS 26 · S 30 · M 38 · L 48 · XL 56을 유지해요. 넓은 버튼의 폭은 문구와 부모 영역에 맞춰 조정해요.
- Disabled와 Checked는 VARIANT 속성으로 True / False를 사용해요. Icon은 BOOLEAN이며 실제 키는 `Icon#8680:0`이에요.
- Checked=True는 현재 기본 버튼에서 리워드 처리 후의 배경·문구 컬러 변화로 표현해요. 이름만 보고 별도의 체크 아이콘을 추가하거나 Disabled와 같은 상태로 해석하지 않아요.
- Button / Description은 Lower Item BOOLEAN으로 하단 표시 여부를 제어해요. 하위 Lower Item의 Type=Description / Link Button과 Highlight를 실제 존재하는 조합 안에서 사용해요.
- 활성 테두리형에는 Outline_Primary 또는 Outline_Secondary를 사용해요. Variant=Outline은 현재 Disabled=True 조합에만 존재해요.
- Quiz 예제는 현재 통합 마스터 Button / Quiz의 Direction=Down / Up, Progress=Filled를 사용해요. 참고 화면의 구형 Down 컴포넌트를 새 예제에 복제하지 않았어요. Progress는 단순 선택 여부가 아니라 참여 비율 표시 구성이에요.
- News 예제는 Default → Progress → Available → Completed를 순서대로 보여줘요. 받을 수 있는 상태와 수령 완료 상태를 구분해요. 샘플 리워드 금액은 상태별 비교가 가능하도록 3금으로 맞췄어요.
- Alert 예제는 Alert=False / True를 나란히 보여줘요. 알림받기와 알림받는 중의 문구·아이콘 컬러를 설정 여부에 맞춰 사용해요.
- 예제의 리워드 금액·비율·처리 시간 문구는 교체 가능한 샘플이에요. 이를 공통 서비스 조건으로 확대하지 않아요.
- 참고용 5개 섹션(Button, Button / Description, Quiz, News, Alert)의 아노테이션 81개를 제거하고 잔여 0개를 확인했어요. 참고 섹션이나 기존 마스터를 삭제한 것은 아니에요.

## 이번 업데이트 — 2026-11-11

가이드라인 6개와 Usage A~K, Figma 링크, 역할·크기·상태·보조 설명·전용 상태 및 컬러 조정 기준을 반영했어요. 예제 C는 ‘리워드 받기’로, F는 ‘처리 후 표시’로 최신 문구를 사용해요. 컬러 조정 가이드라인을 2번에 추가해 기존 2~5번은 3~6번으로 변경했어요. 기존 마스터의 베리언트 수나 속성명은 이번 작업에서 변경하지 않았어요.

---

## 설계 규칙 요약

| 항목 | 값 |
| --- | --- |
| 높이 | XS 26 · S 30 · M 38 · L 48 · XL 56 |
| 상하 Padding | `Spacing/50` (2) — 전 사이즈 공통 |
| 모서리 | XS·S·M `Corner radius/150`(6) · L·XL `Corner radius/250`(10) |
| 테두리 | 1 |
| 주 액션 | `Color/Primary_Orange` + `Color/Gray_White` |
| 보조 액션 | `Color/Gray_900` + `Color/Gray_200` |
| 비활성 (Fill) | `Color/Gray_600` 배경 |
| 비활성 (Weak · Outline) | 배경 유지 + 라벨 `Color/Gray_600` |
| Checked=True · 처리 후 | `Color/Gray_White` 배경 + `Color/Primary_Orange` 라벨 |
| 라벨 | XS·S `t1050_14_bold` · M `t1000_15_bold` · L·XL `t800_17_bold` |

---

## 점검 필요 사항

> 아래 구조·토큰·네이밍 점검과 건수는 기존 정리 기록이에요. 이번에는 사용 문서와 컬러 조정 기준을 추가했으며 마스터 전체를 재설계하거나 파일 전체 토큰을 재점검하지 않았어요. 과거 파일 전체 집계는 현재 수치로 해석하지 않아요.

### 1. ⚠️ `Variant=Outline`이 비활성 전용 — 이름과 역할이 어긋남

`Outline`이라는 값은 **`Disabled=True` 조합으로만 존재**하며, 활성 상태가 없습니다.

| Variant 값 | 활성 | 비활성 |
| --- | --- | --- |
| `Fill` | ✅ | ✅ |
| `Weak` | ✅ | ✅ |
| `Outline_Primary` | ✅ | ❌ |
| `Outline_Secondary` | ✅ | ❌ |
| `Outline` | ❌ | ✅ |

이름만 보면 `Outline`이 외곽선 버튼의 기본형처럼 읽히지만 실제로는 **외곽선 버튼의 비활성 전용 값**입니다. 외곽선 버튼을 쓰려는 사람이 `Outline`을 먼저 고르면 비활성 버튼이 나옵니다.

**정리 방향** — `Outline_Primary` · `Outline_Secondary`에 각각 `Disabled=True`를 추가하고 `Outline` 값을 없애면, 다른 variant와 같은 규칙(활성/비활성 쌍)이 됩니다. 다만 variant 수가 40 → 45로 늘고 기존 인스턴스의 참조가 바뀝니다.

### 2. ✅ 기본 생성 이름 `Property 1` · `Variant2` 정리 (2026-10-01 완료)

Figma가 자동으로 붙인 이름이 남아 있어 **무엇을 고르는 축인지 알 수 없는** 상태였습니다. 의미를 드러내는 이름으로 바꾸고, Quiz는 구조까지 함께 정리했습니다.

#### Button / News — 축 이름 + 값 전부 교체

| 변경 전 | 변경 후 | 의미 |
| --- | --- | --- |
| `Property 1=Default` | `State=Default` | 시작 전 (툴팁) |
| `Property 1=Variant2` | **`State=Progress`** | 읽는 중 |
| `Property 1=Variant3` | **`State=Available`** | 받을 수 있음 |
| `Property 1=Variant4` | **`State=Completed`** | 받기 완료 |

값 4개가 **사용자 동선 순서 그대로** 읽히게 됐습니다.

#### Button / Quiz — 두 컴포넌트셋을 하나로 병합

`Button / Quiz / Up`과 `Button / Quiz / Down`이 **각각 2 variant짜리 별도 컴포넌트셋**이었습니다. 방향이 컴포넌트 이름에, 상태가 `Property 1`에 들어가 축이 둘로 쪼개져 있었습니다.

| 항목 | 변경 전 | 변경 후 |
| --- | --- | --- |
| 컴포넌트셋 | `Quiz / Up` + `Quiz / Down` **2개** | **`Button / Quiz` 1개** (`10027:134176`) |
| 방향 | 컴포넌트 이름으로 구분 | **`Direction`** = `Up` · `Down` |
| 상태 | `Property 1` = `Default` · `Variant2` | **`Progress`** = `Empty` · `Filled` |
| variant | 2 + 2 | **4 (2 × 2 완전 매트릭스)** |

`Progress`라는 이름이 붙으면서, 이 축이 **단순 선택 상태가 아니라 투표 비율 막대의 유무**라는 점이 드러났습니다. 기존 문서에서 `Variant2`를 "선택/눌림 상태"로 추정했던 것은 **잘못된 해석**이었습니다.

#### 결과

당시 마스터 정리 범위에서 기본 생성 속성명을 해소한 기록이에요. 이후 추가된 참고 섹션까지 포함한 현재 페이지 전체의 기본 이름이 0건이라는 뜻은 아니에요. 같은 날 Chip 페이지의 `Chip / Filter`도 `Property 1` → `Type`으로 정리됐습니다 → [syrup-chip-components.md 점검 2](syrup-chip-components.md#2--chip--filter-프로퍼티명-정리-2026-10-01-완료)

다만 **파일 전체로는 61개 컴포넌트셋에 `Property 1`이 남아 있습니다.**

| 페이지 | 건수 | 페이지 | 건수 |
| --- | --- | --- | --- |
| `Lottie` | 14 | `Card 🔴` | 6 |
| `❖Components` | 8 | `Progress Stepper` | 6 |
| `List Row` | 9 | `Grid List` | 3 |
| 그 외 10개 페이지 | 각 1~2 | | |

값까지 기본 이름인 곳은 `Swipe` `10011:127023`(`Variant2~4`)와 `Ticker / Marquee / Inline` `10664:5850`(`Variant2`) **2건**입니다.

> `Grid List`의 `Grid List / Todo / List Item` `9711:5068`은 여전히 **컴포넌트셋 오류 상태**라 프로퍼티를 읽을 수 없습니다. variant 이름 불일치부터 해결해야 합니다.

### 3. Quiz 버튼 색상이 팔레트 밖

| 색상 | 건수 | 위치 |
| --- | --- | --- |
| `#F3564F` | 2 | `Direction=Up` 배경 |
| `#D71900` | 2 | `Direction=Up` 오버레이 |
| `#3D8BF7` | 2 | `Direction=Down` 배경 |
| `#0055CB` | 2 | `Direction=Down` 오버레이 |

Syrup 팔레트에 없는 값이며 베리어블에 바인딩되어 있지 않습니다. 금퀴즈 전용 색이라면 토큰으로 승격할지, 게임 전용 예외로 둘지 결정이 필요합니다.

병합 후에도 **건수는 동일한 8건**입니다. 배경·오버레이가 `Direction` 축 하나로 묶여, 토큰으로 승격한다면 `Up`/`Down` 쌍으로 4개(배경 2 + 오버레이 2)만 정의하면 됩니다.

참고로 `Color/Secondary_Red`(#FF3E00) · `Color/Secondary_Blue`(#3496F4)가 이미 있어 역할이 겹칩니다.

### 4. ✅ 미바인딩 흰색 4건 (2026-10-01 바인딩 완료)

Quiz 버튼의 라벨 텍스트 4개가 `#FFFFFF`를 직접 지정하고 있었습니다. `Color/Gray_White`와 값이 같아 **무손실로 바인딩**했습니다.

| Node | 위치 (현재 이름 기준) |
| --- | --- |
| `10027:134182` | `Direction=Up, Progress=Empty` › text |
| `10027:134188` | `Direction=Up, Progress=Filled` › text |
| `10027:134195` | `Direction=Down, Progress=Empty` › text |
| `10027:134201` | `Direction=Down, Progress=Filled` › text |

2026-09-21 파일 전체 바인딩 정리 이후에 만들어진 컴포넌트라 당시 대상에서 빠져 있었습니다.

### 5. ✅ `Button / Alert` 라벨 텍스트 스타일 (2026-10-01 적용 완료)

"알림받는중" · "알림받기" 두 텍스트가 스타일 없이 지정되어 있어 **`b400_14_regular`** 를 적용했습니다.

| 항목 | 변경 전 | 변경 후 |
| --- | --- | --- |
| 스타일 | 없음 | `b400_14_regular` |
| 크기 · 두께 | 14 Regular | 14 Regular (유지) |
| line-height | **21** | **18** |
| letter-spacing | **−0.3** | **−0.5** |

**variant 크기가 바뀌었습니다.**

| Variant | 변경 전 | 변경 후 |
| --- | --- | --- |
| `Alert=True` | 78 × 21 | **77 × 18** |
| `Alert=False` | 66 × 21 | **65 × 18** |

line-height 21 → 18로 높이가 3px 줄고, letter-spacing이 좁아지며 폭도 1px 줄었습니다. 렌더링은 스크린샷으로 확인했으며 잘림이나 겹침은 없습니다.

### 6. 토큰 상태

| 항목 | 결과 |
| --- | --- |
| 미바인딩 radius | **0건** |
| 미바인딩 padding | `11` 8건 (News 상하) · `100` 6건 (문서 보드) |
| 미바인딩 gap | `1` 4건 |
| 미바인딩 fill | **8건** — Quiz 색상만 (위 3번). 흰색 4건은 2026-10-01 바인딩 완료 |
| 스타일 미적용 텍스트 | **0건** — 2026-10-01 적용 완료 |
| 원격 텍스트 스타일 | **0건** |
| 외부 토큰 | `Spec docs/margin` 6 · paragraph 계열 54 — 전역 이슈 |

**메인 `Button` 세트 40개 variant는 spacing · radius · 색상 · 타이포가 전부 Syrup 토큰과 로컬 스타일로 정리되어 있습니다.**

2 · 4 · 5번은 2026-10-01에 처리했고, 이 페이지에 남은 과제는 **`Variant=Outline` 구조(1번)와 Quiz 색상 토큰화(3번)** 입니다.
