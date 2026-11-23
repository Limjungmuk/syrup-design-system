# Syrup Design System — Loader 컴포넌트

| 항목 | 값 |
| --- | --- |
| Figma File | [Syrup_Design-System](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System) |
| Page / Section | `Loader` 페이지 → [Loader 섹션 `8968:11001`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=8968-11001) |
| 섹션 구성 | Loader 1440×1298 → Guidelines 960×704 → Usage 1360×676 |
| 컴포넌트 수 | **2개** (전부 Component Set) |
| 기준일 | 2026-11-09 (가이드라인 통합 · 실제 요소를 사용한 예제 반영) |
| 관련 문서 | [syrup-design-tokens.md](syrup-design-tokens.md) · [syrup-ad-components.md](syrup-ad-components.md) · [syrup-dialog-components.md](syrup-dialog-components.md) · [syrup-alert-components.md](syrup-alert-components.md) · [syrup-badge-components.md](syrup-badge-components.md) · [syrup-banner-components.md](syrup-banner-components.md) · [syrup-border-components.md](syrup-border-components.md) · [syrup-bottom-info-components.md](syrup-bottom-info-components.md) · [syrup-bottom-cta-components.md](syrup-bottom-cta-components.md) · [syrup-bottom-sheet-components.md](syrup-bottom-sheet-components.md) · [syrup-bubble-components.md](syrup-bubble-components.md) · [syrup-button-components.md](syrup-button-components.md) · [syrup-card-components.md](syrup-card-components.md) · [syrup-checkbox-components.md](syrup-checkbox-components.md) · [syrup-chip-components.md](syrup-chip-components.md) · [syrup-dim-components.md](syrup-dim-components.md) · [syrup-grid-list-components.md](syrup-grid-list-components.md) · [syrup-grid-scroll-components.md](syrup-grid-scroll-components.md) · [syrup-header-components.md](syrup-header-components.md) · [syrup-icon-button-components.md](syrup-icon-button-components.md) · [syrup-indicator-components.md](syrup-indicator-components.md) · [syrup-keypad-components.md](syrup-keypad-components.md) · [syrup-label-components.md](syrup-label-components.md) · [syrup-list-footer-components.md](syrup-list-footer-components.md) · [syrup-list-header-components.md](syrup-list-header-components.md) · [syrup-list-row-components.md](syrup-list-row-components.md) · [syrup-lottie-components.md](syrup-lottie-components.md) · [syrup-product-grid-components.md](syrup-product-grid-components.md) · [syrup-product-list-components.md](syrup-product-list-components.md) · [syrup-product-scroll-components.md](syrup-product-scroll-components.md) · [syrup-progress-stepper-components.md](syrup-progress-stepper-components.md) · [syrup-result-components.md](syrup-result-components.md) · [syrup-search-field-components.md](syrup-search-field-components.md) · [syrup-stepper-components.md](syrup-stepper-components.md) · [syrup-swipe-components.md](syrup-swipe-components.md) · [syrup-switch-components.md](syrup-switch-components.md) · [syrup-tab-components.md](syrup-tab-components.md) · [syrup-tab-bar-components.md](syrup-tab-bar-components.md) · [syrup-text-button-components.md](syrup-text-button-components.md) · [syrup-text-field-components.md](syrup-text-field-components.md) · [syrup-ticker-components.md](syrup-ticker-components.md) · [syrup-toast-components.md](syrup-toast-components.md) |

> **데이터를 불러오는 동안 대기 상태를 보여주는 컴포넌트예요.**
> 로딩 범위에 맞는 크기와 위치를 선택하고, 완료되면 해당 콘텐츠로 바꿔 보여줘요.

---

## 목차

1. [구성 한눈에 보기](#구성-한눈에-보기)
2. [Loader — Master Component](#1-loader--master-component)
3. [Child Item — Loader / Lottie](#2-child-item--loader--lottie)
4. [설계 규칙 요약](#설계-규칙-요약)
5. [Usage](#usage)
6. [Guidelines](#guidelines)
7. [AI 도구 적용 기준](#ai-도구-적용-기준)
8. [현재 확인 사항](#현재-확인-사항)

---

## 구성 한눈에 보기

마스터 섹션은 1440×1298이며, Loader와 안쪽 Lottie primitive의 Component Set 2개로 구성됩니다. 별도 Guidelines 1항목과 Usage 3패턴에서 크기·배치 기준을 설명합니다.

| 보드 위치 | 섹션 | 내용 |
| --- | --- | --- |
| y 434 | Master Component | `Loader` 2종 |
| y 834 | Child Item | `.primitive / Loader / Lottie` 3종 |

| # | 이름 | 타입 | Variant 축 | 크기 | 과거 집계 인스턴스 (2026-10-12) |
| --- | --- | --- | --- | --- | --- |
| 1 | `Loader` | Set | `Size` 2종 | 16 / 20 정사각 | **0** |
| 2 | `.primitive / Loader / Lottie` | Set | `Property 1` 3종 | 20 × 20 | 2 |

로딩 점의 시각적 단계를 primitive의 3개 variant로 표현합니다. 정적 Figma 사례만으로 실제 애니메이션 파일·재생 동작이 연결됐다고 간주하지 않습니다.

---

## 1. Loader — Master Component

**Node** `8972:14002` · Component Set · **2 variants**

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `Size` | VARIANT | `S` | `S` · `M` |

| Size | 크기 | 내용 |
| --- | --- | --- |
| `S` | **16 × 16** | `Loader Item` 인스턴스 |
| `M` | **20 × 20** | `Loader Item` 인스턴스 |

공통 — Padding 0, Gap 0, 배경 없음, 라운드 0, 세로 오토레이아웃

두 variant 모두 **`.primitive / Loader / Lottie` 인스턴스 하나만** 담은 래퍼입니다.

> `Size=S`는 20 × 20 primitive를 **16으로 축소**해 씁니다. 원본이 20 하나뿐이라 사이즈별 에셋이 따로 없습니다.

---

## 2. Child Item — Loader / Lottie

**Node** `8968:11025` · Component Set · **3 variants** · 20 × 20

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `Property 1` | VARIANT | `1` | `1` · `2` · `3` |

프로퍼티명이 Figma 기본값이고, 값도 숫자입니다

### 구조

세 variant 모두 **점 2개**(`Ellipse 5772` · `Ellipse 5773`)를 `Color/Primary_Orange`로 그립니다. 차이는 **점 크기**입니다.

| Variant | 점 크기 | 담는 프레임 | 해석 |
| --- | --- | --- | --- |
| `1` | **7 × 7** | 15 × 7 | 작은 점 |
| `2` | **20 × 20** | 20 × 9 | 커진 점 |
| `3` | **7 × 7** | 15 × 7 | 다시 작은 점 |

점 크기가 달라지는 **참고용 정지 단계 3종**입니다. 실제 애니메이션 파일과 반복·재생 시간은 이 문서 업데이트에서 확인하거나 변경하지 않았습니다.

`1`과 `3`은 **크기가 동일**합니다

### 중첩 구조

```
Property 1=1 [20×20]
└ Frame 1171277119 [20×9]
  └ Frame 1171277119 [20×9]     ← 같은 이름 중첩
    └ Frame 1171277120 [15×7]
      ├ Ellipse 5772 [7×7]  Primary_Orange
      └ Ellipse 5773 [7×7]  Primary_Orange
```

프레임이 **3겹**으로 감싸고 있고, 그중 둘은 이름이 같습니다

---

## 설계 규칙 요약

| 항목 | 값 |
| --- | --- |
| 크기 | `S` 16 × 16 · `M` 20 × 20 |
| 색 | **`Color/Primary_Orange`** (점 2개) |
| 배경 · 테두리 · 라운드 | 없음 |
| 효과 | **없음** (그림자·블러 없음) |
| 애니메이션 | 키프레임 3장 (점 크기 7 → 20 → 7) |

기본 색상과 도형은 기존 Loader 인스턴스를 재사용합니다. 크기와 위치는 아래 가이드라인을 따릅니다.

---

## Usage

| 항목 | 값 |
| --- | --- |
| 섹션 | [Usage `11601:445`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11601-445) · 1360×676 |
| 구성 | A~C 3패턴 · 현재 화면 프레임 360×360 |
| 템플릿 | Usage `11237:46733` · ❖System Components |

Section 1의 화면 중앙 로딩과 상단 영역 아래 로딩을 분류했습니다. 전체 제품 화면 대신 실제 Header·Grid List와 Loader 등 이해에 필요한 요소만 사용합니다. 설명 영역–슬롯 간격은 50입니다.

| 예제 | Node | 설명 | 현재 상단 요소·Loader |
| --- | --- | --- | --- |
| A. 화면 전환 로딩 | `11601:446` | 화면 진입이나 메뉴 전환으로 화면의 주요 콘텐츠를 불러올 때 사용해요. M 크기의 Loader를 화면 가로·세로 중앙에 배치해요. | 실제 Header · M 20×20 · x=170, y=170 |
| B. 상단 메뉴 아래 로딩 | `11601:515` | 상단 메뉴를 유지하고 아래 콘텐츠를 불러올 때 사용해요. 메뉴 아래 16 간격으로 S 크기의 Loader를 가로 중앙에 배치해요. | 실제 Grid List 360×108 · S 16×16 · x=172, y=124 |
| C. 제목 아래 로딩 | `11601:592` | 상단 제목과 기능을 유지하고 아래 콘텐츠를 불러올 때 사용해요. 제목 영역 아래 16 간격으로 S 크기의 Loader를 가로 중앙에 배치해요. | 실제 「내 금」 제목·알림·새로고침 영역 360×58 · S 16×16 · x=172, y=75 |

B는 현재 실제 Grid List 인스턴스 `I11601:515;11239:22;11573:25329`로 교체된 상태입니다. 이전 설명용 메뉴 영역이나 글꼴 로딩 실패 상태를 최신 구성으로 기록하지 않습니다. C는 Section 1의 제목 영역을 재사용한 Frame이며, 원래부터 단일 Header 컴포넌트 인스턴스가 아닌 프레임 구성입니다.

### 배치값의 해석

- 현재 예제 화면은 모두 **360×360**입니다. 초기 작업에서 사용했던 360×540은 현재 기준이 아닙니다. 360×360도 문서용 축약 화면이며 제품 화면의 고정 높이 규격이 아닙니다.
- A의 M은 전체 화면 프레임 기준 가로·세로 중앙입니다. Header 아래 남은 영역의 중앙으로 다시 계산하지 않습니다.
- B는 상단 영역 y=0, 높이 108에서 16 아래인 y=124에 S를 배치합니다.
- C는 상단 영역 y=1, 높이 58에서 16 아래인 y=75에 S를 배치합니다. 간격은 화면 맨 위가 아니라 **상단 요소의 하단 외곽**부터 계산합니다.
- 프레임이 달라지면 중앙 좌표도 다시 계산합니다. x=170/172, y=170/124/75를 모든 화면의 절대 좌표로 고정하지 않습니다.

---

## Guidelines

[Guidelines `11601:444`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11601-444) · 960×704 · 1항목

중복된 상단 여백 규칙을 1번에 통합하고 기존 2번은 제거했습니다. 메뉴 아래·제목 아래의 차이는 Usage B·C에서 보여줍니다. Guidelines 템플릿 `11237:44468`의 좌우 슬롯은 모두 허용된 배치 비교이며 Do / Don’t 형식은 아닙니다.

### 1. 배치 위치에 맞는 크기를 사용해요

**Node** `11601:659`

화면 중앙에 배치할 때는 M(20), 상단 메뉴나 제목 아래에 배치할 때는 S(16)을 사용해요.
상단에 배치하는 Loader는 유지되는 영역의 하단에서 16 떨어뜨리고, 가로 중앙에 맞춰요.

| 왼쪽 | 오른쪽 |
| --- | --- |
| M · 화면 중앙 | S · 유지된 영역 아래 |
| 20×20 | 16×16 |
| 360×360의 x=170, y=170 | 상단 Header 높이 55·y=1 아래 16인 y=72, x=172 |

사이즈를 단순히 남은 공간이나 임의의 선호로 고르지 않고 **배치 위치와 유지되는 영역**에 맞춰 선택합니다. 상단 아래 배치는 Loader 외곽의 윗변과 상단 영역의 아랫변 사이를 16으로 유지합니다.

현재 양쪽 예제 모두 실제 Header를 상단에 유지하며, Loader는 각각 M 중앙 / S 상단 아래에 배치합니다. Loader를 Header 위에 겹쳐 놓거나, Header·메뉴가 이미 보이는 상태에서 상단 Loader를 전체 화면 중앙으로 옮기지 않습니다.

---

## AI 도구 적용 기준

1. 기존 Loader 인스턴스를 재사용합니다. 상위 VARIANT `Size`는 문자열 S/M이며 화면 중앙은 M(20), 상단 메뉴·제목 아래는 S(16)입니다.
2. 중앙 배치는 해당 화면 프레임의 가로·세로 중앙으로 계산합니다. 예제의 고정 좌표나 문서 화면 높이를 제품 전체에 복제하지 않습니다.
3. 상단 배치는 유지되는 영역의 하단에서 16 떨어진 가로 중앙입니다. 영역 종류나 높이가 달라져도 해당 하단 외곽 기준을 유지합니다.
4. 로딩이 끝나면 Loader를 숨기고 해당 콘텐츠를 표시합니다. Loader의 점 모양을 완료·실패 상태나 정량 진행률로 해석하지 않습니다.
5. 상단 메뉴·제목·기능은 해당 패턴에서 유지되는 요소입니다. 문서 맥락을 위해 전체 제품 화면이나 불필요한 콘텐츠를 추가하지 않습니다.
6. 안쪽 primitive의 실제 속성명은 `Property 1`, 값은 문자열 1/2/3입니다. 현재 파일에 Frame·State 등 다른 이름의 속성이 있다고 가정하지 않습니다.
7. primitive의 3개 시각 단계를 서로 다른 로딩 종류로 사용하지 않습니다. 정지 예제만으로 Lottie 파일·타이밍·반복 애니메이션이 구현됐다고 가정하지 않습니다.
8. Loader 크기는 본체 외곽 16×16 / 20×20입니다. 안쪽 점의 순간 크기를 기준으로 정렬하거나 여백을 계산하지 않습니다.
9. 새로운 Dim·모달 차단·탭 비활성 정책은 이 문서의 범위가 아닙니다. Loader가 있다는 이유만으로 화면 전체 차단 동작을 추가하지 않습니다.
10. 이번 업데이트는 MD 문서만 수정합니다. Figma의 사용자 수정 화면·간격·실제 컴포넌트와 Section 1을 변경하지 않습니다.

---

## 현재 확인 사항

2026-11-09 현재 Loader 가이드라인과 예제를 대조했습니다. 제품 파일 전체 사용량 통계가 아닙니다.

| 항목 | 확인 결과 |
| --- | --- |
| 컴포넌트 정의 | Loader Component Set 1개 / S·M · Lottie primitive Component Set 1개 / 단계 1·2·3 |
| 가이드라인 | 1항목으로 통합 · 배치 위치별 크기와 상단 간격 16 명시 |
| Usage | 3패턴 · 실제 Header / Grid List / 내 금 제목 영역 사용 |
| 최신 화면 크기 | 360×360 · 초기 540 높이에서 사용자 수정됨 |
| B 교체 상태 | 실제 Grid List 인스턴스로 교체 확인 · 이전 작업 중 글꼴 오류는 현재 미완료 상태가 아님 |
| 원본 자료 | Section 1 유지 · 아노테이션 제거 요청은 없었음 |
| 애니메이션 | 기존 시각 단계 재사용 · 실제 파일과 재생 동작은 이번 업데이트에서 검증하지 않음 |

이전 2026-10-12 문서의 전체 노드·인스턴스·토큰 미바인딩 건수와 정리 우선순위는 문서 추가 이후 현황으로 재검증하지 않아 최신 현황에서 제외했습니다. 구성 표의 과거 인스턴스 집계에는 기준일을 표시했습니다. 마스터 0건이라는 과거 수치는 현재 Section 1과 Guidelines·Usage의 사용 여부를 설명하지 않습니다.

현재 Size=S 축소 방식과 primitive의 단계·중첩 프레임은 유지합니다. MD 업데이트를 이유로 중첩을 해제하거나 단계 3을 삭제하거나 속성명을 변경하지 않습니다.
