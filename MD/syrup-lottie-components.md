# Syrup Design System — Lottie 컴포넌트

| 항목 | 값 |
| --- | --- |
| Figma File | [Syrup_Design-System](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System) |
| Page / Section | `Lottie` 페이지 → [Lottie 섹션 `9112:17174`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=9112-17174) |
| 섹션 크기 | 1440 × 3505 |
| 컴포넌트 수 | **16개** (Component Set 14 · Component 2) |
| 기준일 | 2026-11-09 (공통 설명·Usage 갱신, 기존 에셋 점검은 2026-10-12 기준) |
| 관련 문서 | [syrup-design-tokens.md](syrup-design-tokens.md) · [syrup-ad-components.md](syrup-ad-components.md) · [syrup-dialog-components.md](syrup-dialog-components.md) · [syrup-alert-components.md](syrup-alert-components.md) · [syrup-badge-components.md](syrup-badge-components.md) · [syrup-banner-components.md](syrup-banner-components.md) · [syrup-border-components.md](syrup-border-components.md) · [syrup-bottom-info-components.md](syrup-bottom-info-components.md) · [syrup-bottom-cta-components.md](syrup-bottom-cta-components.md) · [syrup-bottom-sheet-components.md](syrup-bottom-sheet-components.md) · [syrup-bubble-components.md](syrup-bubble-components.md) · [syrup-button-components.md](syrup-button-components.md) · [syrup-card-components.md](syrup-card-components.md) · [syrup-checkbox-components.md](syrup-checkbox-components.md) · [syrup-chip-components.md](syrup-chip-components.md) · [syrup-dim-components.md](syrup-dim-components.md) · [syrup-grid-list-components.md](syrup-grid-list-components.md) · [syrup-grid-scroll-components.md](syrup-grid-scroll-components.md) · [syrup-header-components.md](syrup-header-components.md) · [syrup-icon-button-components.md](syrup-icon-button-components.md) · [syrup-indicator-components.md](syrup-indicator-components.md) · [syrup-keypad-components.md](syrup-keypad-components.md) · [syrup-label-components.md](syrup-label-components.md) · [syrup-list-footer-components.md](syrup-list-footer-components.md) · [syrup-list-header-components.md](syrup-list-header-components.md) · [syrup-list-row-components.md](syrup-list-row-components.md) · [syrup-loader-components.md](syrup-loader-components.md) · [syrup-product-grid-components.md](syrup-product-grid-components.md) · [syrup-product-list-components.md](syrup-product-list-components.md) · [syrup-product-scroll-components.md](syrup-product-scroll-components.md) · [syrup-progress-stepper-components.md](syrup-progress-stepper-components.md) · [syrup-result-components.md](syrup-result-components.md) · [syrup-search-field-components.md](syrup-search-field-components.md) · [syrup-stepper-components.md](syrup-stepper-components.md) · [syrup-swipe-components.md](syrup-swipe-components.md) · [syrup-switch-components.md](syrup-switch-components.md) · [syrup-tab-components.md](syrup-tab-components.md) · [syrup-tab-bar-components.md](syrup-tab-bar-components.md) · [syrup-text-button-components.md](syrup-text-button-components.md) · [syrup-text-field-components.md](syrup-text-field-components.md) · [syrup-ticker-components.md](syrup-ticker-components.md) · [syrup-toast-components.md](syrup-toast-components.md) |

> 기능과 콘텐츠에 맞는 기존 Lottie 모션을 사용해요.
> 숫자로 구분된 Variant는 모션의 표현 단계이며, 서로 다른 사용 유형이 아니에요.
> 재생 시점과 반복·종료 조건은 에셋별 정의를 따라요. 예제는 화면에 배치된 대표 상태를 보여줘요.

---

## 목차

1. [구성 한눈에 보기](#구성-한눈에-보기)
2. [Master Component 11종](#1-master-component-11종)
3. [Child Items 5종](#2-child-items-5종)
4. [공통 사용 설명](#공통-사용-설명)
5. [Usage — 사용처별 예제](#usage--사용처별-예제)
6. [설계 규칙 요약](#설계-규칙-요약)
7. [점검 필요 사항](#점검-필요-사항)

---

## 구성 한눈에 보기

마스터 섹션 높이는 3,505예요. 기존 노드·인스턴스 집계는 2026-10-12 기준이며, 이후 추가된 Section 1과 Usage는 포함하지 않아요.

이 페이지는 기존 모션 에셋과 표현 단계를 정리하고, Usage에서 실제 사용 맥락을 소개해요. 별도 Guidelines는 두지 않고 공통 설명과 사용처별 예제로 구성해요. Figma에 보이는 대표 상태만으로 실제 재생 조건을 판단하지 않아요.

| 보드 위치 | 섹션 | 내용 |
| --- | --- | --- |
| y 434 | Master Component | 애니메이션 **11종** |
| y 2579 | Child Items | primitive **5종** |
| 별도 섹션 | [Usage](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11623-1613) | 사용처별 예제 A~G **7개** |

### 전체 목록

아래 인스턴스 수는 2026-10-12의 기존 집계이며 현재 사용 여부를 판단하는 기준이 아니에요.

| # | 이름 | 타입 | 프레임 수 | 크기 | 인스턴스(기존 집계) |
| --- | --- | --- | --- | --- | --- |
| 1 | `Lottie / Alarm` | Set | **8** | 18 × 18 | 0 |
| 2 | `Lottie / Checkin` | Set | 3 | 68 × 68 | 0 |
| 3 | `Lottie / Thunderbolt1` | Set | 2 | 96 × 96 | **1** (`Card`) |
| 4 | `Lottie / Thunderbolt2` | Set | 2 | 44 × 44 | **1** (`Card`) |
| 5 | `Lottie / Quiz_Coachmark` | Set | 3 | 328 × 91 | 0 |
| 6 | `Lottie / Quiz` | Set | 3 | 42 × 42 | **1** (`List Row`) |
| 7 | `Lottie / Meal` | **Component** | — | 110 × 110 | 0 |
| 8 | `Lottie / Shopping` | Set | 2 | 20 × 20 | 0 |
| 9 | `Lottie / Dot` | **Component** | — | 24 × 12 | 0 |
| 10 | `Lottie / snack1` | Set | 3 | 340 × 135 | 0 |
| 11 | `Lottie / snack2` | Set | 3 | 246 × 240 | 0 |
| 12 | `.primitive / Lottie / Meal / Loading` | Set | **5** | 110 × 110 | 1 |
| 13 | `.primitive / Lottie / Meal / AI` | Set | 3 | 32 × 32 | **6** |
| 14 | `.primitive / Lottie / Dot1` | Set | 2 | 4 × 12 | 1 |
| 15 | `.primitive / Lottie / Dot2` | Set | 3 | 4 × 12 | 1 |
| 16 | `.primitive / Lottie / Dot3` | Set | 3 | 4 × 12 | 1 |

**14개 컴포넌트셋 전부 `Property 1`에 숫자 프레임 번호**를 담고 있습니다.

---

## 1. Master Component 11종

### 애니메이션 분류

| 용도 | 컴포넌트 | 프레임 | 크기 |
| --- | --- | --- | --- |
| **알림** | `Alarm` | 8 | 18 |
| **출석 체크** | `Checkin` | 3 | 68 |
| **번개 적립** | `Thunderbolt1` · `Thunderbolt2` | 각 2 | 96 · 44 |
| **퀴즈** | `Quiz` · `Quiz_Coachmark` | 각 3 | 42 · 328 × 91 |
| **식사 기록** | `Meal` | 조립형 | 110 |
| **쇼핑** | `Shopping` | 2 | 20 |
| **로딩 점** | `Dot` | 조립형 | 24 × 12 |
| **간식 안내** | `snack1` · `snack2` | 각 3 | 340 × 135 · 246 × 240 |

프레임 수는 **2~8장**이며, `Alarm`이 가장 많습니다.

### 조립형 2종

`Lottie / Meal`과 `Lottie / Dot`만 **variant 없이 primitive를 조합**합니다.

| 컴포넌트 | 크기 | 구성 |
| --- | --- | --- |
| `Lottie / Meal` | 110 × 110 | `.primitive / Lottie / Meal / Loading` (110) + `.primitive / Lottie / Meal / AI` (32) |
| `Lottie / Dot` | 24 × 12 | `.primitive / Lottie / Dot1` · `Dot2` · `Dot3` (각 4 × 12) |

`Lottie / Dot`은 **점 3개를 각각 다른 primitive로** 만들었습니다. 점마다 애니메이션 타이밍이 달라 프레임 수가 2 · 3 · 3으로 다릅니다.

> [Loader](syrup-loader-components.md)의 `.primitive / Loader / Lottie`(점 2개, 20 × 20)와 **역할이 겹칩니다** → [점검 5](#5-loader와-역할이-겹침)

### 실제 사용

| 컴포넌트 | 쓰이는 곳 |
| --- | --- |
| `Lottie / Thunderbolt1` · `Thunderbolt2` | [Card](syrup-card-components.md) ▸ `Card / Thunderbolt` ▸ `Type=Title` |
| `Lottie / Quiz` | [List Row](syrup-list-row-components.md) ▸ `List Row / Quiz` |

위 표는 기존 재사용 컴포넌트의 연결을 정리한 내용이에요. 현재 화면에서 확인한 사용 맥락은 아래 Usage A~G를 기준으로 확인해요.

---

## 2. Child Items 5종

| 컴포넌트 | 크기 | 프레임 | 쓰이는 곳 |
| --- | --- | --- | --- |
| `.primitive / Lottie / Meal / Loading` | 110 × 110 | 5 | `Lottie / Meal` |
| `.primitive / Lottie / Meal / AI` | 32 × 32 | 3 | `Lottie / Meal` 외 (**6건**) |
| `.primitive / Lottie / Dot1` | 4 × 12 | 2 | `Lottie / Dot` |
| `.primitive / Lottie / Dot2` | 4 × 12 | 3 | `Lottie / Dot` |
| `.primitive / Lottie / Dot3` | 4 × 12 | 3 | `Lottie / Dot` |

`Meal / AI`가 6건으로 가장 많이 쓰이며, 전부 `Lottie` 페이지 안입니다.

---

## 공통 사용 설명

- 기능과 콘텐츠에 맞는 기존 Lottie 모션을 사용해요. 사용처별 예제는 독립적인 컴포넌트 유형이나 새로운 Variant를 뜻하지 않아요.
- 숫자로 구분된 `Property 1` 값은 모션의 표현 단계예요. 선택 상태나 업무 진행 단계로 해석하지 않아요.
- 재생 시점과 반복·종료 조건은 에셋별 정의를 따라요. 정지 화면만으로 재생 시간, 반복 횟수, 완료 시 동작을 임의로 지정하지 않아요.
- 예제에는 모션을 이해하는 데 필요한 문구와 보조 요소만 함께 배치해요. 전체 서비스 화면을 복제할 필요는 없어요.
- 에셋 파일명이나 경로가 문서에 없는 경우 이름만으로 파일을 추정하지 않아요. 실제 모션 파일과 재생 정의를 확인해 사용해요.

## Usage — 사용처별 예제

[Usage 섹션](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11623-1613)에 A~G 예제를 구성했어요. 별도 Guidelines는 추가하지 않아요.

| 예제 | 사용 컴포넌트 | 설명 | 함께 배치하는 요소 |
| --- | --- | --- | --- |
| [A. 알림 기능 안내](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11623-1614) | `Lottie / Alarm` | 알림 받기 기능 옆에 Alarm 모션을 배치해요. 기능을 설명하는 문구와 함께 사용해요. | 알림 받기 문구 |
| [B. 출석 영역 강조](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11623-1637) | `Lottie / Checkin` | 출석 날짜에 Checkin 모션을 사용해요. 날짜와 모션이 함께 보이도록 배치해요. | 출석 날짜 |
| [C. 이벤트 콘텐츠 연출](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11623-1660) | `Lottie / Thunderbolt1` · `Thunderbolt2` | 이벤트 카드에 Thunderbolt 모션을 사용해요. 카드의 이미지와 문구를 함께 구성해요. | `Card / Thunderbolt`, 이벤트 이미지·문구 |
| [D. 퀴즈 참여 안내](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11623-1690) | `Lottie / Quiz` | 퀴즈 목록에서 Quiz 모션을 사용해요. 마감 안내와 참여 버튼을 함께 배치해요. | `List Row / Quiz`, 날짜·마감 안내·참여 버튼 |
| [E. AI 분석 중 안내](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11623-1721) | `Lottie / Meal` | AI 분석을 기다리는 동안 Meal 모션을 사용해요. 진행 상태를 설명하는 문구를 함께 표시해요. | AI 분석 중 안내 문구 |
| [F. 콘텐츠 혜택 안내](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11623-1787) | `Lottie / Shopping` | 콘텐츠 혜택을 안내하는 문구 옆에 Shopping 모션을 사용해요. | 콘텐츠 혜택 안내 문구 |
| [G. 페이지 이동 안내](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11626-1736) | `Lottie / Dot` | 외부 페이지로 이동하는 동안 Dot 모션을 사용해요. 이동할 대상을 안내하는 문구와 함께 표시해요. | 쿠팡 로고·이동 안내 문구 |

### 예제 해석

- Quiz_Coachmark의 퀴즈 보상 안내는 Lottie 에셋 재생이 아닌 개발 모션으로 확인되어 2026-11-17 사용 예제에서 제외했어요. 마스터 구조 표의 기존 Figma 명칭은 참고용이며 Lottie 파일이 있다는 뜻은 아니에요.

- E의 “5초 정도 걸릴 수 있어요.”는 해당 화면의 안내 문구이며, 모든 Lottie의 재생 시간이나 대기 시간 기준이 아니에요.
- G의 Dot은 외부 페이지 이동 안내 사례예요. 일반 콘텐츠 로딩에 사용하는 `Loader`의 M/S 선택 기준과 혼동하지 않아요.
- `snack1`·`snack2`는 마스터 목록에 유지해요. 이번에 확인한 사용처 예제에 없다는 이유로 삭제하거나 새 용도를 임의로 부여하지 않아요.

---

## 설계 규칙 요약

| 항목 | 값 |
| --- | --- |
| 프레임 표현 | `Property 1`에 **숫자**(`1` · `2` · `3` …) |
| 프레임 수 | 2 ~ 8장 |
| 크기 | 4 × 12 ~ 340 × 135 (용도별 제각각) |
| 주 색상 | `#FF6315`(Primary Orange 계열) · `#3496F4`(Blue 계열) — **대부분 미바인딩** |
| 배경 | 없음 |

**이 페이지에는 공통 설계 규칙이 거의 없습니다.** 애니메이션마다 크기·프레임 수·색이 전부 다릅니다.

---

## 점검 필요 사항

> 아래는 2026-10-12의 에셋 점검 기록이에요. 이번 갱신은 공통 설명과 Usage 문서화에 한정하며, 과거 건수·전체 파일 통계·미바인딩 상태는 재집계하지 않았어요. 사용 여부는 최신 Usage를 우선하고, 이 기록의 제안을 확정된 사용 규칙으로 해석하지 않아요.

### 1. `Property 1` **14건** — 파일에서 가장 많이 몰린 페이지

파일 전체 잔여 **46건 중 14건**이 이 페이지입니다.

| 컴포넌트 | 값 |
| --- | --- |
| `Alarm` | `1`~`8` |
| `Checkin` · `Quiz` · `Quiz_Coachmark` · `snack1` · `snack2` · `Meal / AI` · `Dot2` · `Dot3` | `1`~`3` |
| `Thunderbolt1` · `Thunderbolt2` · `Shopping` · `Dot1` | `1`~`2` |
| `Meal / Loading` | `1`~`5` |

**모든 값이 애니메이션 키프레임 번호**입니다. `Frame` · `Keyframe` · `Step` 중 하나로 통일하면 의미가 드러납니다.

| 후보 | 장단점 |
| --- | --- |
| **`Frame`** | 애니메이션 용어로 가장 직관적 |
| `Keyframe` | 더 정확하지만 길어짐 |
| `Step` | 다른 페이지에서 단계 의미로 쓰여 혼동 여지 |

[Loader](syrup-loader-components.md)의 `.primitive / Loader / Lottie`도 같은 성격이라, **15건을 한 번에 정리**할 수 있습니다.

> 다만 **실제 구현에서는 Lottie JSON 파일이 애니메이션을 담당**하고 Figma variant는 참고용 정지 프레임입니다. 코드가 이 variant 이름을 참조할 일이 거의 없어, **정리의 실익은 "Figma 안에서 읽기 쉬워지는 것"** 에 한정됩니다.

### 2. `snack1` · `snack2`의 variant 순서가 뒤섞임

두 컴포넌트셋에서 **캔버스 배치 순서와 옵션 순서가 다릅니다.**

| 컴포넌트 | 자식(캔버스) 순서 | `Property 1` 옵션 순서 |
| --- | --- | --- |
| `Lottie / snack1` | `1` · **`3`** · **`2`** | `1` · `2` · `3` |
| `Lottie / snack2` | `1` · **`3`** · **`2`** | `1` · `2` · `3` |

**애니메이션 프레임은 순서가 의미를 갖습니다.** 보드에서 왼쪽부터 `1 → 3 → 2`로 놓여 있어, 움직임을 눈으로 따라가기 어렵습니다.

다른 컴포넌트셋(`Alarm` 8종 · `Meal / Loading` 5종 등)은 **캔버스 순서와 옵션 순서가 일치**합니다.

캔버스에서 `2`와 `3`의 위치를 바꾸면 해소됩니다. 옵션 순서는 이미 정상이라 **동작에는 영향이 없고 보드 가독성 문제**입니다.

### 3. 미바인딩 색상 **다수** — 일러스트 범주

| 색 | 건수 | 성격 |
| --- | --- | --- |
| `#D9D9D9` | 24 | 회색 (일러스트 음영) |
| `#BE820B` · `#D8D8D8` | 각 8 | 금색 · 회색 |
| `#FFFFFF` · `#3496F4` | 각 6 | 흰색 · 파랑 |
| `#FFCE99` | 4 | 살구색 |
| **`#FF6315`** | **3** | **`Color/Primary_Orange`와 같은 값** |
| `#FF5E00` · `#FF6200` | 3 | 오렌지 유사색 |
| 그 외 | 다수 | 일러스트 색 |

**애니메이션 일러스트의 내부 색**이라, 아이콘·일러스트를 토큰화 대상에서 제외해 온 기준([Card](syrup-card-components.md) · [Grid List](syrup-grid-list-components.md) · [List Row](syrup-list-row-components.md))과 같은 범주입니다.

> [List Row](syrup-list-row-components.md)에서 `Lottie / Quiz` 내부의 `#FF6315` 1건을 같은 이유로 **바인딩 대상에서 제외**한 바 있습니다.

눈에 띄는 점은 **오렌지 계열이 세 가지 값**(`#FF6315` · `#FF5E00` · `#FF6200`)으로 쓰인다는 것입니다. 브랜드 오렌지가 애니메이션마다 미세하게 다른 셈입니다. Lottie 원본(JSON) 쪽에서 정리할 사안입니다.

### 4. 마스터 8종 사용 0건

| 구분 | 컴포넌트 | 인스턴스 |
| --- | --- | --- |
| **쓰임** | `Thunderbolt1` · `Thunderbolt2` | 각 1 (`Card`) |
| **쓰임** | `Quiz` | 1 (`List Row`) |
| **0건** | `Alarm` · `Checkin` · `Quiz_Coachmark` · `Meal` · `Shopping` · `Dot` · `snack1` · `snack2` | **0** |

이는 2026-10-12의 집계예요. 현재는 Section 1과 Usage에 Alarm·Checkin·Meal·Shopping·Dot 사용 사례가 추가되어, 0건을 현재 상태로 해석할 수 없어요.

> **이 수치는 이 Figma 파일 기준**입니다. 다른 파일·디태치·코드 사용은 포함되지 않습니다.

애니메이션은 **구현 시 Lottie JSON을 직접 넣는 방식**이라, Figma 컴포넌트는 "이런 애니메이션이 있다"는 **카탈로그 역할**일 가능성이 큽니다. 그렇다면 0건이 문제가 아닙니다.

다만 그 역할이라면 **각 컴포넌트에 Lottie 파일명이나 경로를 Description으로 적어 두는 것**이 유용합니다. 현재 `Lottie / Meal` · `Lottie / Dot`의 Description은 비어 있습니다.

### 5. Loader와 역할이 겹침

| 컴포넌트 | 위치 | 구성 | 크기 |
| --- | --- | --- | --- |
| `.primitive / Loader / Lottie` | [Loader](syrup-loader-components.md) 페이지 | 점 **2개** | 20 × 20 |
| `Lottie / Dot` | **Lottie 페이지** | 점 **3개** (primitive 3종 조합) | 24 × 12 |

**둘 다 "점이 움직이는 로딩 표시"** 인데 페이지도 구성도 다릅니다.

| | Loader | Lottie / Dot |
| --- | --- | --- |
| 점 개수 | 2 | 3 |
| 프레임 | 3 | 점마다 2 · 3 · 3 |
| 사이즈 축 | `Size` S/M 있음 | 없음 |

현재 확인한 사용 맥락은 Loader의 콘텐츠 로딩 표시와 Dot의 외부 페이지 이동 안내로 구분해요. 모양이 비슷하다는 이유로 자동 통합하거나 대체하지 않아요. 명칭·구조 통합 여부는 별도 검토 사항이에요.

### 6. 스타일 미적용 텍스트 21건

보드 표기 4건을 제외한 수치입니다.

| 크기 · 굵기 | 건수 | 위치 |
| --- | --- | --- |
| **17 Medium** | **15** | `snack1` · `snack2` 안내 문구 |
| **17 Bold** | **6** | `snack1` · `snack2` 강조 |

**전부 `snack1` · `snack2`의 코치마크 문구**입니다("사고싶은 **쿠팡 상품**을 검색하고…").

17px에는 대응 토큰이 있습니다.

| 현재 | 후보 토큰 | 스펙 |
| --- | --- | --- |
| 17 Medium | **`t1100_17_medium`** | Medium 17 / 22 / −0.8 |
| 17 Bold | **`t800_17_bold`** | Bold 17 / 22 / 0 |

다만 **애니메이션 프레임 안의 텍스트**라, 실제로는 Lottie가 렌더링합니다. 토큰을 적용해도 구현에 반영되지 않으므로 **Figma 일관성 목적**의 작업입니다.

### 7. 미바인딩 레이아웃 값 — 전부 애니메이션 내부

| 값 | 건수 | 성격 |
| --- | --- | --- |
| radius `30` | **30** | 일러스트 도형 |
| radius `139.52` | 5 | 벡터 스케일 값 |
| padding `2.68` · `2.79` · `10.71` · `9.38` 등 | 60+ | **전부 소수점** — 일러스트 내부 |
| gap `2.68` · `2.79` | 14 | 동일 |

**소수점 값이 대부분**이고 애니메이션 일러스트 내부라 토큰화 대상이 아닙니다. [Grid List](syrup-grid-list-components.md)의 소수점 라운드 63건과 같은 성격입니다.

### 8. 토큰 상태 — 특수 페이지

| 항목 | 결과 |
| --- | --- |
| **원격 텍스트 스타일** | **0건** |
| **제어문자 · U+2028** | **0건** |
| 외부 토큰 | `Spec docs` 4 — 문서 레이아웃 전용 |
| 폰트 | 전부 Pretendard |
| 미바인딩 fill · radius · padding | **다수** — 전부 일러스트 내부 |

**애니메이션 에셋 페이지라 일반적인 토큰 기준을 적용하기 어렵습니다.** 미바인딩 수치가 많지만 대부분 Lottie 원본에서 온 값입니다.

원격 스타일·제어문자가 0건이고 폰트가 통일되어 있다는 점은 양호합니다.

---

## 정리 우선순위

| 순위 | 항목 | 성격 | 비용 |
| --- | --- | --- | --- |
| 1 | `snack1` · `snack2` 캔버스 순서 ([2](#2-snack1--snack2의-variant-순서가-뒤섞임)) | 보드 정리 | 낮음 |
| 2 | `Property 1` **14건** → `Frame` ([1](#1-property-1-14건--파일에서-가장-많이-몰린-페이지)) | 이름만 변경 · **Loader와 함께 15건** | 낮음 |
| 3 | Description에 Lottie 파일 경로 ([4](#4-마스터-8종-사용-0건)) | 문서화 | 낮음 |
| 4 | `Loader` / `Lottie / Dot` 역할 정리 ([5](#5-loader와-역할이-겹침)) | 구조 판단 | 중간 |
| 5 | `snack` 문구 토큰 적용 ([6](#6-스타일-미적용-텍스트-21건)) | 실익 확인 필요 | 중간 |
| 6 | 오렌지 3종 값 통일 ([3](#3-미바인딩-색상-다수--일러스트-범주)) | **Lottie 원본 쪽 작업** | 높음 |

**1 · 2번은 시각적 변화 없이 바로 처리 가능**합니다.
