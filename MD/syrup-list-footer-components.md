# Syrup Design System — List Footer 컴포넌트

| 항목 | 값 |
| --- | --- |
| Figma File | [Syrup_Design-System](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System) |
| Page / Section | `List Footer` 페이지 → [List Footer 섹션 `8444:6159`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=8444-6159) |
| 섹션 구성 | List Footer 1440×902 → Guidelines 960×1251 → Usage 1760×607 |
| 컴포넌트 수 | **1개** (Component) |
| 기준일 | 2026-11-09 (가이드라인 3항목 · 예제 4패턴 · 화살표 방향 기준 반영) |
| 관련 문서 | [syrup-design-tokens.md](syrup-design-tokens.md) · [syrup-ad-components.md](syrup-ad-components.md) · [syrup-dialog-components.md](syrup-dialog-components.md) · [syrup-alert-components.md](syrup-alert-components.md) · [syrup-badge-components.md](syrup-badge-components.md) · [syrup-banner-components.md](syrup-banner-components.md) · [syrup-border-components.md](syrup-border-components.md) · [syrup-bottom-info-components.md](syrup-bottom-info-components.md) · [syrup-bottom-cta-components.md](syrup-bottom-cta-components.md) · [syrup-bottom-sheet-components.md](syrup-bottom-sheet-components.md) · [syrup-bubble-components.md](syrup-bubble-components.md) · [syrup-button-components.md](syrup-button-components.md) · [syrup-card-components.md](syrup-card-components.md) · [syrup-checkbox-components.md](syrup-checkbox-components.md) · [syrup-chip-components.md](syrup-chip-components.md) · [syrup-dim-components.md](syrup-dim-components.md) · [syrup-grid-list-components.md](syrup-grid-list-components.md) · [syrup-grid-scroll-components.md](syrup-grid-scroll-components.md) · [syrup-header-components.md](syrup-header-components.md) · [syrup-icon-button-components.md](syrup-icon-button-components.md) · [syrup-indicator-components.md](syrup-indicator-components.md) · [syrup-keypad-components.md](syrup-keypad-components.md) · [syrup-label-components.md](syrup-label-components.md) · [syrup-list-header-components.md](syrup-list-header-components.md) · [syrup-list-row-components.md](syrup-list-row-components.md) · [syrup-loader-components.md](syrup-loader-components.md) · [syrup-lottie-components.md](syrup-lottie-components.md) · [syrup-product-grid-components.md](syrup-product-grid-components.md) · [syrup-product-list-components.md](syrup-product-list-components.md) · [syrup-product-scroll-components.md](syrup-product-scroll-components.md) · [syrup-progress-stepper-components.md](syrup-progress-stepper-components.md) · [syrup-result-components.md](syrup-result-components.md) · [syrup-search-field-components.md](syrup-search-field-components.md) · [syrup-stepper-components.md](syrup-stepper-components.md) · [syrup-swipe-components.md](syrup-swipe-components.md) · [syrup-switch-components.md](syrup-switch-components.md) · [syrup-tab-components.md](syrup-tab-components.md) · [syrup-tab-bar-components.md](syrup-tab-bar-components.md) · [syrup-text-button-components.md](syrup-text-button-components.md) · [syrup-text-field-components.md](syrup-text-field-components.md) · [syrup-ticker-components.md](syrup-ticker-components.md) · [syrup-toast-components.md](syrup-toast-components.md) |

> **목록의 끝에서 추가 항목이나 전체 목록, 이전 내역을 확인하는 버튼 컴포넌트예요.**
> 관련 목록의 마지막에 배치하고, 실제 동작과 확인할 대상을 문구로 알려줘요.

---

## 목차

1. [구성 한눈에 보기](#구성-한눈에-보기)
2. [List Footer — Master Component](#1-list-footer--master-component)
3. [설계 규칙 요약](#설계-규칙-요약)
4. [Usage](#usage)
5. [Guidelines](#guidelines)
6. [AI 도구 적용 기준](#ai-도구-적용-기준)
7. [현재 확인 사항](#현재-확인-사항)

---

## 구성 한눈에 보기

마스터는 Component 1개이며 variant는 없습니다. 별도 Guidelines 3항목과 Usage 4패턴으로 동작·배치·문구 기준을 설명합니다.

| 보드 위치 | 섹션 | 내용 |
| --- | --- | --- |
| y 434 | Master Component | `List Footer` 1종 |

`Child Item` · `Icon` 섹션이 없습니다.

| # | 이름 | 타입 | Props | 크기 | 과거 집계 인스턴스 (2026-10-12) |
| --- | --- | --- | --- | --- | --- |
| 1 | `List Footer` | Component | `Text` · `Arrow` | 360 × 64 | 3 |

(2026-10-12 `ListFooter` → `List Footer` 이름 정리)

---

## 1. List Footer — Master Component

**Node** `8454:10706` · Component · variant 없음

### Properties

| Property | Type | Default |
| --- | --- | --- |
| `Text#8457:30` | TEXT | `더보기` |
| `Arrow#9796:1` | BOOLEAN | `true` |

상위 컴포넌트는 텍스트 교체와 화살표 표시 여부를 제공합니다. **방향은 하위 `Icon / Arrow`의 Variant를 Down/Right로 선택**합니다. 상위 Arrow는 BOOLEAN이므로 방향 값으로 대체하지 않습니다.

### 레이아웃

| 항목 | 값 |
| --- | --- |
| 크기 | **360 × 64** (마스터 기준 · 인스턴스는 관련 목록의 폭에 맞춤) |
| 방향 | 가로 오토레이아웃 |
| 리사이징 | 가로 FIXED · 세로 HUG |
| 정렬 | 가로·세로 **중앙** |
| Padding | 상하 **22.5** · 좌우 0 |
| Gap | **0** |
| 배경 | `Color/Gray_White` |
| 테두리 | **`Color/Gray_900` — 상단 1px만** (`1/0/0/0`) |
| 라운드 | 0 |

**상단에 1px 선 하나만** 그어 리스트와 경계를 만듭니다. [Card](syrup-card-components.md)의 `Card / SA`(하단 1px만)와 반대 방향입니다.

높이 64는 **패딩에서 계산된 값**입니다.

```
22.5 + 19(텍스트 line-height) + 22.5 = 64
```

세로가 HUG라 패딩이 그대로 높이에 반영됩니다

### 구성 요소

| 레이어 | 타입 | 스펙 |
| --- | --- | --- |
| `더보기` | TEXT | `t1300_15_medium` (15 / 19 / −0.5) + `Color/Gray_200` |
| `Icon / Arrow` | INSTANCE | 16 × 16 · `Variant=Right, Size=S` |

Gap이 0인데도 텍스트와 화살표 사이가 떨어져 보이는 것은 **아이콘 에셋 자체의 여백** 때문입니다.

---

## 설계 규칙 요약

| 항목 | 값 |
| --- | --- |
| 크기 | 기준 360×64 · 관련 목록 폭에 맞춤 · 높이 HUG |
| 상하 패딩 | 22.5 |
| 배경 | `Color/Gray_White` |
| 경계 | `Color/Gray_900` **상단 1px만** |
| 라벨 | `t1300_15_medium` + `Color/Gray_200` |
| 화살표 | `Icon / Arrow` · S(16) · 추가 로딩 Down / 페이지 이동 Right |
| 정렬 | 가로·세로 중앙 |

---

## Usage

| 항목 | 값 |
| --- | --- |
| 섹션 | [Usage `11589:5307`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11589-5307) · 1760×607 |
| 구성 | A~D 4패턴 · 슬롯 폭 360 · Footer 328×64 |
| 템플릿 | Usage `11237:46733` · ❖System Components |

Section 1의 실제 목록·Footer 인스턴스를 재사용하고, 설명에 필요한 최소 목록만 남깁니다. 전체 제품 화면은 복제하지 않습니다. 설명 영역–슬롯 간격은 50입니다.

| 예제 | Node | 설명 | 현재 Footer |
| --- | --- | --- | --- |
| A. 목록 더보기 | `11589:5308` | 목록 아래에서 추가 항목을 확인할 때 사용해요. 관련 목록의 마지막에 배치하고, 목록과 같은 폭으로 맞춰요. | 「더보기」 · Arrow=false |
| B. 범위를 표시한 전체 보기 | `11589:5430` | 전체 목록의 범위나 개수를 알려줄 때 함께 표시해요. 순위·인원 등 실제로 확인할 대상과 범위에 맞게 문구를 작성해요. | 「1~100위 전체 보기」 · Arrow=true · Right |
| C. 상품 목록 더보기 | `11589:5516` | 여러 상품 목록이 이어지면 쇼핑몰이나 콘텐츠명을 함께 표시해요. 어떤 목록의 상품을 더 보는지 구분할 수 있도록 해요. | 「G마켓 상품 더보기」 · Arrow=true · Right |
| D. 이전 내역 보기 | `11589:5628` | 현재 목록보다 이전의 기록을 확인할 때 사용해요. 더보기와 구분해 이전 내역을 확인하는 동작임을 문구로 알려줘요. | 「이전 보기」 · Arrow=true · Right |

A는 일반 목록 항목 2개, B는 순위 항목 2개, C는 2열 상품 목록, D는 이전 당첨 내역 항목 2개 아래에 Footer를 둡니다. 대상 목록과 Footer의 폭은 모두 328입니다.

**현재 A는 화살표가 없는 기존 구성입니다.** 이를 추가 로딩의 신규 방향 기준으로 해석하지 않습니다. 같은 화면 아래에 항목을 불러오는 동작의 신규 구성은 Guidelines 3에 따라 Down을 사용합니다. 이 MD 업데이트는 Figma A의 화살표 상태를 변경하지 않습니다.

D의 현재 표시는 Right입니다. 「이전 보기」라는 문구만으로 방향을 정하는 것이 아니라 실제 동작을 확인합니다. 같은 화면에 이전 항목을 추가하면 Down, 다른 페이지로 이동하면 Right를 적용합니다.

---

## Guidelines

[Guidelines `11589:5306`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11589-5306) · 960×1251 · 3항목

Guidelines 템플릿 `11237:44468`의 좌우 슬롯으로 허용된 배치·문구·동작을 비교합니다. Do / Don’t 형식은 아닙니다. 설명 영역–슬롯 간격은 50입니다.

### 1. 관련 목록의 마지막에 배치해요

**Node** `11589:5708`

List Footer는 추가로 확인할 목록의 마지막 항목 아래에 배치해요.
목록과 같은 폭으로 맞추고, 목록과 함께 스크롤되도록 구성해요.

| 왼쪽 | 오른쪽 |
| --- | --- |
| 일반 목록 · 마지막에 배치 | 상품 목록 · 마지막에 배치 |
| 일반 목록 아래 「더보기」 | 상품 목록 아래 「G마켓 상품 더보기」 |

화면 가장자리의 고정 좌표가 아니라 관련 목록의 흐름 안에 배치합니다. 현재 예제는 폭 328, 원본 수집 사례는 276·312·328·360 등 목록에 따라 폭이 다릅니다. 마스터 폭 360을 모든 목록에 강제하지 않습니다.

### 2. 동작과 확인할 범위를 문구로 알려줘요

**Node** `11589:5886`

추가 항목은 더보기, 전체 범위는 전체 보기, 이전 기록은 이전 보기처럼 실제 동작에 맞게 작성해요.
여러 목록이 이어지거나 범위 안내가 필요하면 대상명·개수·순위를 함께 표시해요.

| 왼쪽 | 오른쪽 |
| --- | --- |
| 범위 · 전체 보기 | 대상 · 상품 더보기 |
| 「1~100위 전체 보기」 | 「G마켓 상품 더보기」 |

실제 범위와 대상에 맞게 문구를 변경합니다. Section 1의 「84명 전체 보기」처럼 인원 수를 포함할 수 있습니다. 100위·84명은 고정 정책이나 항상 표시해야 할 숫자가 아닙니다.

### 3. 동작에 맞는 화살표 방향을 사용해요

**Node** `11589:5948`

같은 화면에서 목록 아래로 항목을 더 불러올 때는 아래쪽 화살표(Down)를 사용해요.
전체 목록이나 다른 페이지로 이동할 때는 오른쪽 화살표(Right)를 사용해요.

| 왼쪽 | 오른쪽 |
| --- | --- |
| Down · 아래 항목 더 불러오기 | Right · 다른 페이지로 이동 |
| Arrow=true · 내부 Variant=Down | Arrow=true · 내부 Variant=Right |
| 문구 「더보기」 | 문구 「더보기」 |

두 예제 모두 같은 문구를 사용하고 방향만 달리해 동작의 차이를 보여줍니다. 「더보기」라는 문구나 화살표 표시 여부만으로 동작을 판단하지 않습니다. 신규 적용 기준은 실제 추가 로딩/페이지 이동에 맞춰 방향을 선택하는 것입니다.

상위 `Arrow#9796:1`은 표시 여부이며 방향을 선택하는 속성이 아닙니다. 방향은 하위 Arrow 인스턴스의 `Variant`에서 지정하며 `Size=S`를 유지합니다. 이미지나 선을 따로 그려 방향을 바꾸지 않습니다.

---

## AI 도구 적용 기준

1. 기존 List Footer 인스턴스를 관련 목록의 마지막 아래에 배치하고 목록과 함께 스크롤되도록 구성합니다. 문서의 좌표를 제품 고정 위치로 복제하지 않습니다.
2. Footer 폭은 목록의 가용 폭에 맞춥니다. 기준 높이 64와 기존 중앙 정렬을 유지하며 마스터 폭 360을 좁은 목록에 강제하지 않습니다.
3. 같은 화면에서 아래 항목을 추가로 불러오면 Down, 전체 목록이나 다른 페이지로 이동하면 Right를 사용합니다. 과거 Arrow=false·Right 사례를 신규 추가 로딩 기준으로 복제하지 않습니다.
4. 실제 Figma 속성 키는 `Text#8457:30`(TEXT), `Arrow#9796:1`(BOOLEAN)입니다. 방향은 하위 `Icon / Arrow`의 VARIANT `Variant=Down/Right`로 지정합니다.
5. 문구는 동작·대상·범위와 일치시킵니다. 상품명·쇼핑몰·인원 수·순위 범위는 실제 데이터와 목적에 맞게 바꿉니다.
6. 「이전 보기」도 실제 동작으로 방향을 결정합니다. 과거 기록을 확인한다는 이유만으로 Left나 Up을 자동 적용하지 않습니다.
7. 기본 패딩 22.5는 현재 높이 64를 구성하는 값입니다. MD 업데이트를 이유로 반올림하거나 토큰 근사값으로 바꾸지 않습니다.
8. 문서 예제는 디자인 기준을 설명하는 정적 인스턴스입니다. Figma의 화살표·문구만으로 로딩·탐색 동작이 구현됐다고 가정하지 않습니다.
9. 이번 업데이트는 MD 문서에 한정합니다. Figma의 기존 예제·마스터·프로퍼티명·토큰은 수정하지 않습니다.

---

## 현재 확인 사항

2026-11-09 현재 가이드라인 3개와 예제 4개를 대조했습니다. 제품 파일 전체 사용량을 조사한 통계는 아닙니다.

| 항목 | 확인 내용 |
| --- | --- |
| 마스터 | List Footer `8454:10706` · Component 1개 · 상위 variant 없음 |
| 배치 기준 | 목록 마지막에 같은 폭으로 배치 · 목록과 함께 스크롤 |
| 방향 기준 | 같은 화면 아래 추가 로딩 Down / 다른 페이지 이동 Right |
| 현재 예제 차이 | Usage A와 가이드 1의 일반 목록은 Arrow=false인 기존 사례 · 신규 방향 규칙은 가이드 3 참조 |
| 원본 자료 | Section 1의 아노테이션 49개 제거 완료 |
| 기존 이름 정리 | 2026-10-12 ListFooter → List Footer, Viariant → Variant, UP → Up 완료 |

이전 문서의 전체 노드·인스턴스·미바인딩 건수와 정리 우선순위는 문서 추가 이후 현황으로 재검증하지 않아 최신 현황에서 제외했습니다. 구성 표의 과거 인스턴스 집계에는 기준일을 표시했습니다.

현재 상단 구분선 색과 상하 패딩은 기존 마스터 규격으로 유지합니다. 문서 업데이트를 이유로 다른 Border 색으로 통일하거나 레이아웃을 바꾸지 않습니다. 과거 프로퍼티 오기 Viariant·UP 대신 현재 Variant·Up을 사용합니다.
