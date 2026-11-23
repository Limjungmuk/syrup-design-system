# Syrup Design System — Swipe 컴포넌트

| 항목 | 값 |
| --- | --- |
| Figma File | [Syrup_Design-System](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System) |
| Page / Section | `Swipe` 페이지 → [Swipe 섹션 `10011:126743`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=10011-126743) |
| 섹션 크기 | 1440 × 1552 |
| 컴포넌트 수 | **2개** (Master 1 · Child Item 1) |
| Variant 총수 | **7개** (5 · 2) |
| 기준일 | 2026-11-17 (Complete 추가, 가이드라인·예제 갱신) |
| 관련 문서 | [syrup-design-tokens.md](syrup-design-tokens.md) · [syrup-ad-components.md](syrup-ad-components.md) · [syrup-alert-components.md](syrup-alert-components.md) · [syrup-badge-components.md](syrup-badge-components.md) · [syrup-banner-components.md](syrup-banner-components.md) · [syrup-border-components.md](syrup-border-components.md) · [syrup-bottom-cta-components.md](syrup-bottom-cta-components.md) · [syrup-bottom-info-components.md](syrup-bottom-info-components.md) · [syrup-bottom-sheet-components.md](syrup-bottom-sheet-components.md) · [syrup-bubble-components.md](syrup-bubble-components.md) · [syrup-button-components.md](syrup-button-components.md) · [syrup-card-components.md](syrup-card-components.md) · [syrup-checkbox-components.md](syrup-checkbox-components.md) · [syrup-chip-components.md](syrup-chip-components.md) · [syrup-dialog-components.md](syrup-dialog-components.md) · [syrup-dim-components.md](syrup-dim-components.md) · [syrup-grid-list-components.md](syrup-grid-list-components.md) · [syrup-grid-scroll-components.md](syrup-grid-scroll-components.md) · [syrup-header-components.md](syrup-header-components.md) · [syrup-icon-button-components.md](syrup-icon-button-components.md) · [syrup-indicator-components.md](syrup-indicator-components.md) · [syrup-keypad-components.md](syrup-keypad-components.md) · [syrup-label-components.md](syrup-label-components.md) · [syrup-list-footer-components.md](syrup-list-footer-components.md) · [syrup-list-header-components.md](syrup-list-header-components.md) · [syrup-list-row-components.md](syrup-list-row-components.md) · [syrup-loader-components.md](syrup-loader-components.md) · [syrup-lottie-components.md](syrup-lottie-components.md) · [syrup-product-grid-components.md](syrup-product-grid-components.md) · [syrup-product-list-components.md](syrup-product-list-components.md) · [syrup-product-scroll-components.md](syrup-product-scroll-components.md) · [syrup-progress-stepper-components.md](syrup-progress-stepper-components.md) · [syrup-result-components.md](syrup-result-components.md) · [syrup-search-field-components.md](syrup-search-field-components.md) · [syrup-stepper-components.md](syrup-stepper-components.md) · [syrup-switch-components.md](syrup-switch-components.md) · [syrup-tab-components.md](syrup-tab-components.md) · [syrup-tab-bar-components.md](syrup-tab-bar-components.md) · [syrup-text-button-components.md](syrup-text-button-components.md) · [syrup-text-field-components.md](syrup-text-field-components.md) · [syrup-ticker-components.md](syrup-ticker-components.md) · [syrup-toast-components.md](syrup-toast-components.md) |

> **할 일 알림에서 사용자가 밀기 동작으로 할 일을 완료하는 컴포넌트예요.**
> 대기, 밀기 진행, 금 지급 처리 중, 완료, 시간 만료를 구분하고 필요한 경우 받을 리워드를 Bubble로 안내해요.

---

## 목차

1. [구성 한눈에 보기](#구성-한눈에-보기)
2. [Swipe — Master Component](#1-swipe--master-component)
3. [`.primitive / Swipe / Handle`](#2-primitive--swipe--handle)
4. [가이드라인](#가이드라인)
5. [Usage — 사용 예제](#usage--사용-예제)
6. [예제 레이아웃과 AI 사용 기준](#예제-레이아웃과-ai-사용-기준)
7. [설계 규칙 요약](#설계-규칙-요약)
8. [점검 필요 사항](#점검-필요-사항)
9. [정리 우선순위](#정리-우선순위)

---

## 구성 한눈에 보기

마스터 1종과 하위 Handle 1종으로 이뤄져요. 별도 섹션에 가이드라인 4개와 예제 A~E를 정리했어요.

기존 마스터 섹션 집계: 높이 1,552 · 노드 **85개** · 텍스트 **12개**. 노드·인스턴스·토큰 및 파일 전체 집계는 2026-10-12 점검 기록이며, 이후 추가된 Section 1과 문서 예제는 포함하지 않아요.

| 보드 위치 | 섹션 | 내용 |
| --- | --- | --- |
| y 0 | Title Bar | 페이지 제목 |
| y 434 | Section Header | Master Component |
| y 574 | (높이 494) | `Swipe` 1종 |
| y 1068 | Section Header | Child Items |
| y 1208 | (높이 280) | `.primitive / Swipe / Handle` 1종 |

| # | 이름 | 타입 | Variant 축 | 크기 | 인스턴스 |
| --- | --- | --- | --- | --- | --- |
| 1 | `Swipe` | Set 5 | `State` + `Bubble` BOOLEAN | 298 × 48 | **0** |
| 2 | `.primitive / Swipe / Handle` | Set 2 | `Enabled` | 40 × 40 | 4 (페이지 내부) |

### 핸들 위치가 상태를 만듭니다

Default → Dragging → Near Complete → Complete는 밀기 동작과 금 지급 처리 흐름을 보여줘요. Expired는 완료 가능한 시간이 지난 경우의 별도 분기예요. 핸들 좌표는 각 variant의 대표 표현이며, 실제 드래그 임계값이나 동작 시간의 규정은 아니에요.

| State | 핸들 x | 배경 | 문구 | 상태 |
| --- | --- | --- | --- | --- |
| `Default` | **4** | `Color/Primary_Orange` | 「밀어서 완료」 | 대기 |
| `Dragging` | **24** | `Primary_Orange` + 진행 바 68 | 「밀어서 완료」 | 미는 중 |
| `Near Complete` | **234** | `#E7550C` (전체) | 「금 나오는 중」 | **처리 중** |
| `Complete` | **숨김** | `#E7550C` (전체) | 「완료」 | 완료 · 금액 뒤 체크 뱃지 유지 |
| `Expired` | **4** | `Color/Third_Pastel_Coral` | 「완료 가능한 시간이 지났어요!」 | 만료 |

핸들이 4 → 24 → 234로 이동하고, 끝에 닿으면 배경 전체가 진한 주황으로 바뀝니다.

**`Near Complete`는 처리 중**, **`Complete`는 완료**예요. Complete에서는 손잡이를 숨기고 「완료」 문구와 금액 뒤 체크 표시가 있는 Bubble을 유지해요. 배경은 `#E7550C`예요.

> variant 이름은 원래 `Default` · `Variant2` · `Variant3` · `Variant4`로 **Figma 자동 생성명 그대로**였고, 2026-10-12에 의미 있는 이름으로 바꿨습니다 ✅

---

## 1. Swipe — Master Component

**Node** `10011:127023` · Component Set · **5 variants** · 모두 **298 × 48**

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `State` | VARIANT | `Default` | `Default` · `Dragging` · `Near Complete` · `Complete` · `Expired` |
| `Bubble` | BOOLEAN | `true` | — |

### 공통 레이아웃 — 다섯 variant가 동일

| 항목 | 값 | 토큰 |
| --- | --- | --- |
| 크기 | 298 × 48 | — |
| 레이아웃 | 가로 오토레이아웃 CENTER / CENTER | — |
| Padding | `10 / 36 / 10 / 36` | `Spacing/250` · `Spacing/900` ✅ |
| Gap | 0 | — |
| 라운드 | 100 | `Corner radius/circle` ✅ |

### 배치 방식 — 문구만 오토레이아웃

| 레이어 | 배치 | 위치 |
| --- | --- | --- |
| 문구 | **AUTO** | 오토레이아웃으로 가운데 정렬 |
| `.primitive / Swipe / Handle` | **ABSOLUTE** | x = 4 / 24 / 234 |
| `Bubble` | **ABSOLUTE** | x 210, **y −26.25** (바 위로 올라감) |
| 진행 바 (`Dragging`) | **ABSOLUTE** | x 0, 68 × 48 |

핸들과 말풍선을 **절대 배치로 빼고 문구만 오토레이아웃에 남긴** 구조입니다. 핸들이 좌우로 움직여도 문구는 가운데를 유지합니다.

`Bubble`은 y −26.25로 **바 바깥 위쪽**에 뜹니다 → [Bubble](syrup-bubble-components.md) 페이지 인스턴스.

### variant별 구성

| State | 레이어 순서 |
| --- | --- |
| `Default` | 문구 → `Handle` → `Bubble` |
| `Dragging` | **`Progress`** → 문구 → `Handle` → `Bubble` |
| `Near Complete` | `Handle` → `Bubble` → **`Label`**(아이콘 + 텍스트) |
| `Complete` | **완료 문구 → Bubble** · Handle 숨김 |
| `Expired` | `Handle` → `Bubble` → 문구 |

**기존 네 variant의 레이어 순서가 제각각**이며 Complete는 손잡이를 숨깁니다 → [점검 4](#4-variant-간-레이어-순서가-다름)

| Variant | 문구 | 색 |
| --- | --- | --- |
| `Default` · `Dragging` | 「밀어서 완료」 16 Bold `t900_16_bold` | `Color/Gray_White` ✅ |
| `Near Complete` | 「금 나오는 중」 + `gold_test4 3` 아이콘 22 × 20 | `Color/Gray_White` ✅ |
| `Complete` | 「완료」 · 금액 뒤 체크 표시 Bubble | `Color/Gray_White` ✅ |
| `Expired` | 「완료 가능한 시간이 지났어요!」 | **`#FFC59F` 미바인딩** |

---

## 2. `.primitive / Swipe / Handle`

**Node** `10011:126869` · Component Set · **2 variants** · 40 × 40 · 오토레이아웃 없음

| Property | Type | Options |
| --- | --- | --- |
| `Enabled` | VARIANT | `True` · `False` |

| 레이어 | 타입 | 크기 | `Enabled=True` | `Enabled=False` |
| --- | --- | --- | --- | --- |
| `Circle` | Ellipse | 40 × 40 | `Color/Gray_White` ✅ | `Color/Gray_White` ✅ |
| `Arrow` | Boolean Op | 15.85 × 14.79 | `Color/Primary_Orange` ✅ | `Color/Third_Pastel_Coral` ✅ |
| └ `Arrow 1` · `Arrow 2` | Vector | 8.85 × 14.79 | 같음 | 같음 |

흰 원 위에 **겹화살표(»)** 를 올린 구조입니다. 두 벡터가 같은 크기로 나란히 놓여 화살표 두 개를 만듭니다.

`Enabled=False`의 `Color/Third_Pastel_Coral`은 **`Expired`의 배경색과 같은 토큰**이라, 만료 상태에서 핸들이 배경에 묻히는 연출입니다.

`Enabled` 옵션 순서가 **`True` → `False`**로, 파일 관례(`False` → `True`)와 반대입니다 → [점검 5](#5-enabled-옵션-순서)

---

## 가이드라인

[Figma Guidelines](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11724-225) · 2026-11-10 반영

### 1. 밀기 동작으로 할 일 완료를 실행해요

할 일 알림에서 사용자가 직접 밀어 완료할 때 Swipe를 사용해요.
대기 상태는 Default, 핸들을 움직이는 중에는 Dragging으로 표시해 동작의 진행을 보여줘요.

- 비교: 대기 · Default / 밀기 진행 · Dragging
- [Figma 가이드라인 1](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11724-227)

### 2. 처리 중·완료·시간 만료를 구분해요

밀기 동작 후 금 지급을 처리하는 동안에는 Near Complete로 표시해요. 지급이 끝난 완료 상태로 사용하지 않아요. 완료 결과는 Complete로 표시해요.
완료 가능한 시간이 지나면 Expired로 전환해 더 이상 완료할 수 없음을 안내해요.

- 비교: 금 지급 처리 중 · Near Complete / 완료 시간 만료 · Expired
- [Figma 가이드라인 2](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11724-281)

### 3. 완료 후에도 리워드 결과를 보여줘요

처리 중인 Near Complete와 완료인 Complete를 구분해요. 완료되면 손잡이를 숨기고 완료 문구를 표시해요.
Bubble=True이면 금액 뒤 체크 표시가 있는 뱃지를 유지해 결과를 알려요.

- 비교: 금 지급 처리 중 · Near Complete / 할 일 완료 · Complete
- [Figma 가이드라인 3](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=12069-241)

### 4. 리워드 안내가 필요할 때 Bubble을 표시해요

완료로 받을 리워드를 안내할 때는 Bubble=True로 표시해요. 금액은 실제 지급 조건에 맞춰 사용해요.
추가 안내가 필요하지 않으면 Bubble=False로 숨겨요. 위로 돌출되는 말풍선이 다른 요소와 겹치지 않도록 배치해요.

- 비교: 리워드 안내 · Bubble=True / 안내 생략 · Bubble=False
- [Figma 가이드라인 4](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11724-330)


---

## Usage — 사용 예제

[Figma Usage](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11724-226) · A~E 순서 (대기 → 드래그 → 처리 중 → 완료 → 시간 만료)

| 예제 | 설명 | State | Figma |
| --- | --- | --- | --- |
| A. 할 일 완료 대기 | 알림을 받은 할 일을 밀어서 완료하도록 안내해요. Default 상태에서 받을 리워드를 Bubble로 함께 보여줄 수 있어요. | `Default` | [A](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11724-389) |
| B. 밀기 진행 중 | 사용자가 핸들을 미는 동안 Dragging으로 표시해요. 핸들의 이동과 진행 영역으로 밀기 동작을 보여줘요. | `Dragging` | [B](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11724-419) |
| C. 금 지급 처리 중 | 밀기 동작 후 금 지급을 처리하는 동안 Near Complete를 사용해요. “금 나오는 중”은 지급 완료가 아닌 처리 중 안내예요. | `Near Complete` | [C](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11724-444) |
| D. 할 일 완료 | 완료되면 손잡이를 숨기고 완료 문구를 표시해요. 금액 뒤 체크 표시가 있는 뱃지를 유지해요. | `Complete` | [D](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=12069-312) |
| E. 완료 가능한 시간 만료 | 완료할 수 있는 시간이 지나면 Expired를 사용해요. 비활성 표현과 문구로 더 이상 완료할 수 없음을 알려요. | `Expired` | [E](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11724-470) |

---

## 예제 레이아웃과 AI 사용 기준

- 기존 `Swipe` 인스턴스의 `State`와 `Bubble` 속성을 사용해요. `Bubble`은 BOOLEAN 속성(`Bubble#10011:21`)이며 기본값은 true예요.
- `Near Complete`는 처리 중으로 사용하고 완료는 기존 `Complete` variant로 표시해요. Complete의 Bubble은 금 이미지 대신 금액 뒤 체크 표시로 결과를 보여줘요.
- `Expired`는 Near Complete 다음에 반드시 이어지는 단계가 아니라, 완료 가능한 시간이 지난 경우의 별도 상태예요.
- 예제의 “5금”은 표시 사례예요. 실제 리워드 금액은 서비스 지급 조건에 맞춰요.
- 핸들 위치와 진행 바는 상태별 대표 화면이에요. 정적 예제만으로 드래그 거리, 완료 임계값, 애니메이션 시간이나 지급 처리 시간을 추정하지 않아요.
- 마스터 기준 크기는 298 × 48이고 Default 예제는 300 × 48을 사용해요. 예제의 300을 모든 화면의 고정 폭으로 적용하지 않아요. 높이 48과 내부 구성을 유지하며 배치할 영역을 확인해요.
- Bubble은 절대 배치로 바 위쪽에 돌출돼요. 상위 영역의 클리핑이나 인접 요소 때문에 가려지지 않도록 확인해요. 문구는 가운데 정렬을 유지해요.
- 문서 예제는 Slot 안에 Swipe 인스턴스를 직접 배치해요. 불필요한 ‘화면’ 래퍼와 Slot 패딩을 두지 않고 좌측·상단 정렬로 구성해요. 설명 끝과 Slot 사이는 50으로 맞춰요. 이 값은 문서 레이아웃 기준이에요.
- Section 1의 아노테이션은 제거했어요. 전체 알림 화면이나 광고·동의 배너를 복제하지 않고 Swipe 상태와 Bubble 사용을 중심으로 설명해요.
- 아래의 기존 점검 기록과 토큰 개선 제안은 과거 점검 내용이에요. 확정된 사용 규칙이나 신규 토큰 생성 지시로 해석하지 않아요.

---

## 설계 규칙 요약

### 상태 전개

```
Default         핸들 x=4     주황 바        「밀어서 완료」
   ↓ 밀기
Dragging        핸들 x=24    + 진행 바 68   「밀어서 완료」
   ↓ 끝까지
Near Complete   핸들 x=234   진한 주황 전체 「금 나오는 중」  ← 처리 중
   ↓ 완료 결과
Complete        핸들 숨김    진한 주황 전체 「완료」 · 금액+체크 Bubble 유지

Expired         핸들 x=4     코랄 (비활성)  「완료 가능한 시간이 지났어요!」
```

`Expired`는 흐름의 일부가 아니라 **별도 분기**(시간 만료)입니다.

### 색 구성

| 용도 | 색 | 토큰 |
| --- | --- | --- |
| 기본 바 배경 | #FF6315 | `Color/Primary_Orange` ✅ |
| **진행 바 · 처리 중 배경** | **#E7550C** | **없음** |
| 만료 배경 · 비활성 핸들 | #FFEADE | `Color/Third_Pastel_Coral` ✅ |
| **만료 문구** | **#FFC59F** | **없음** |
| 핸들 원 · 문구 | #FFFFFF | `Color/Gray_White` ✅ |

**주황 계열 3단**(#FF6315 → #E7550C → #FFEADE) 중 **가운데만 토큰이 없습니다** → [점검 2](#2-미바인딩-색상-3건)

### 토큰 적용 상태

| 항목 | 상태 |
| --- | --- |
| Padding | `Spacing/250` · `Spacing/900` ✅ |
| 라운드 | `Corner radius/circle` ✅ |
| 텍스트 스타일 | `t900_16_bold` ✅ · **미적용 0건** |
| 배경 · 아이콘 색 | 대부분 토큰 ✅ |
| **미바인딩 색상** | **3건** (#E7550C ×2 · #FFC59F ×1) |
| 미바인딩 수치 | **0건** ✅ (보드 영역 제외) |
| 원격 텍스트 스타일 | **0건** ✅ |
| 줄 구분자(U+2028/9) | **0건** ✅ |

컴포넌트 내부 수치는 **전부 토큰에 묶여 있고**, 남은 것은 색 3건뿐입니다.

### 타 페이지 의존

| 출처 | 컴포넌트 | 건수 |
| --- | --- | --- |
| [Bubble](syrup-bubble-components.md) | `Bubble` | 4 |
| ❖System Components | `Section Header` 2 · `Title Bar` 1 | 3 |

외부 라이브러리 인스턴스는 **0건**입니다.

---

## 점검 필요 사항

> 아래는 2026-10-12 점검 당시 기록이에요. 2026-11-17 추가된 Complete의 현재 기준은 위 상태 표·가이드라인·예제 D를 따라요.

> 아래는 2026-10-12의 구조·토큰 점검 기록이에요. 2026-11-10에는 가이드라인과 예제를 추가했으며, 마스터 구조와 토큰 개선 제안은 이번 작업에서 변경하지 않았어요.

### 1. `Property 1`과 `Variant2`~`4` 자동 생성명 — ✅ 완료

```
변경 전   Property 1 = Default | Variant2 | Variant3 | Variant4
변경 후   State      = Default | Dragging | Near Complete | Expired
```

**속성명과 값 4개 모두 Figma가 자동으로 붙인 이름 그대로**였습니다. 지금까지 문서화한 36개 페이지 중 **값까지 자동 생성명인 유일한 컴포넌트**였습니다.

| 변경 전 | 변경 후 | 상태 |
| --- | --- | --- |
| `Property 1` | **`State`** | 스와이프 진행 상태 |
| `Default` | `Default` | 대기 — 핸들 왼쪽 끝 |
| `Variant2` | **`Dragging`** | 미는 중 — 진행 바 표시 |
| `Variant3` | **`Near Complete`** | **처리 중** — 핸들은 끝에 닿았으나 작업 미완 |
| `Variant4` | **`Expired`** | 시간 만료 — 비활성 |

#### `Near Complete`로 정한 이유

처음에는 `Variant3`을 완료 상태로 읽었으나, **「금 나오는 중」은 처리 중을 뜻하고 완료까지 간 것이 아닙니다.**

| 단계 | 이 컴포넌트에 있는가 |
| --- | --- |
| 제스처 진행 | ✅ `Dragging` |
| 제스처 완료 · 작업 처리 중 | ✅ **`Near Complete`** |
| 작업 완료 | **없음** |

완료 화면은 다른 컴포넌트가 담당하는 것으로 보입니다. `Done`이 아니라 `Near Complete`를 쓴 것은 **"거의 다 왔지만 아직 끝나지 않았다"**는 뜻을 이름에 담기 위해서입니다.

2026-10-12 당시 집계에서는 인스턴스가 **0건**이었어요. 현재 사용량을 뜻하지 않아요.

> **부수 효과** — 값을 개명하자 옵션 순서가 레이어 순서대로 재계산돼 `Default` · `Dragging` · `Near Complete` · `Expired`가 됐습니다. [Stepper](syrup-stepper-components.md)에서 확인한 동작과 같습니다.

### 2. 미바인딩 색상 3건

| 색 | 건수 | 위치 |
| --- | --- | --- |
| **#E7550C** | 2 | `Dragging` 진행 바 · `Near Complete` 배경 |
| **#FFC59F** | 1 | `Expired` 문구 |

둘 다 **파일 전체에서 이 페이지에만** 쓰입니다(#E7550C 2건 · #FFC59F 1건).

#### #E7550C — 주황 3단의 가운데

| 단계 | 색 | 토큰 |
| --- | --- | --- |
| 기본 | #FF6315 | `Color/Primary_Orange` |
| **눌림 · 처리 중** | **#E7550C** | **없음** |
| 연한 배경 | #FFEADE | `Color/Third_Pastel_Coral` |

#FF6315보다 어두운 주황으로, **눌림(pressed) 상태 색**의 성격입니다. 같은 역할의 색이 다른 컴포넌트에도 있다면 **`Color/Primary_Orange_Pressed` 같은 토큰**으로 묶을 만합니다.

| 선택지 | 내용 |
| --- | --- |
| A | 토큰 신설 — 눌림 상태 색을 시스템에 들임 |
| B | 현행 유지 — Swipe 전용 색으로 두고 미바인딩 허용 |

**다른 컴포넌트의 눌림 상태 처리 방식을 먼저 확인**해야 판단할 수 있습니다.

#### #FFC59F — 만료 문구

`Color/Third_Pastel_Coral`(#FFEADE) 배경 위의 문구 색입니다. 배경보다 진하고 `Primary_Orange`보다 연한 중간 톤입니다.

단독 1건이라 **도메인 색으로 두는 쪽**이 무난합니다. [Progress Stepper](syrup-progress-stepper-components.md)의 Express 계열 21건, [Label](syrup-label-components.md)의 Metric 색과 같은 처리입니다.

### 3. 문구가 variant에 박혀 있음

`Swipe`에는 **TEXT 속성이나 SLOT이 없습니다.** 문구 세 가지가 각 variant에 직접 들어 있습니다.

| Variant | 문구 |
| --- | --- |
| `Default` · `Dragging` | 「밀어서 완료」 |
| `Near Complete` | 「금 나오는 중」 |
| `Expired` | 「완료 가능한 시간이 지났어요!」 |

문구를 바꾸려면 인스턴스에서 **직접 덮어써야** 하는데, [점검 4](#4-variant-간-레이어-순서가-다름)처럼 variant마다 레이어 구성이 달라 **상태를 바꾸면 덮어쓴 문구가 유지되지 않을 수 있습니다.**

「밀어서 완료」는 범용 문구지만 **「금 나오는 중」은 특정 서비스 전용**이라, 다른 맥락에서 쓰려면 매번 고쳐야 합니다. `Near Complete`라는 이름 자체는 범용이나, 담긴 문구는 그렇지 않습니다.

| 선택지 | 내용 |
| --- | --- |
| A | TEXT 속성 추가 — 문구를 속성으로 노출 |
| B | 현행 유지 — 인스턴스에서 덮어쓰기 |

A가 바람직하지만 **variant 간 레이어 구조를 먼저 맞춰야** 합니다.

### 4. variant 간 레이어 순서가 다름

| State | 순서 |
| --- | --- |
| `Default` | 문구 → `Handle` → `Bubble` |
| `Dragging` | `Progress` → 문구 → `Handle` → `Bubble` |
| `Near Complete` | **`Handle` → `Bubble` → `Label`** |
| `Expired` | **`Handle` → `Bubble` → 문구** |

앞의 둘은 문구가 먼저, 뒤의 둘은 핸들이 먼저입니다.

Figma는 variant를 바꿀 때 **같은 위치·같은 이름의 레이어끼리 오버라이드를 이어받습니다.** 순서와 이름이 어긋나면 덮어쓴 값이 끊길 수 있습니다.

실제로 문구 레이어 이름도 전부 다릅니다.

| State | 문구 레이어명 |
| --- | --- |
| `Default` · `Dragging` | `밀어서 완료` |
| `Near Complete` | **`Label`** ✅ (안에 텍스트) |
| `Expired` | `완료 가능한 시간이 지났어요!` |

**텍스트 내용이 그대로 레이어명**이 돼 있어, 문구를 바꾸면 레이어명과 내용이 어긋납니다.

| 제안 | 내용 |
| --- | --- |
| 문구 레이어를 모두 `Label`로 통일 | 이름 일치 |
| 레이어 순서를 네 variant 동일하게 | 오버라이드 연결 |

[점검 3](#3-문구가-variant에-박혀-있음)과 함께 처리해야 효과가 있습니다.

### 5. `Enabled` 옵션 순서

| 컴포넌트 | 순서 |
| --- | --- |
| `.primitive / Swipe / Handle` | **`True` → `False`** |
| 파일 관례 | `False` → `True` |

Figma는 첫 옵션을 기본값으로 쓰므로 인스턴스를 새로 놓으면 `True`로 시작합니다. 활성이 기본인 것은 자연스러우나, [Progress Stepper](syrup-progress-stepper-components.md)의 `Pig` · `Movie` · `Lottery` · `Search` · `Express`가 모두 `False` → `True`인 것과 다릅니다.

[Stepper](syrup-stepper-components.md)에서 확인한 대로, **레이어 재정렬만으로는 드롭다운 표시 순서가 바뀌지 않습니다.** 기본값만 바꾸려면 재정렬로 충분하지만, 이 경우 기본값이 `False`가 되어 **오히려 어색해집니다.**

현행 유지가 무난합니다.

### 6. 레이어명 정리 — ✅ 완료 (10건)

| 변경 전 | 변경 후 | 위치 | 건수 | 근거 |
| --- | --- | --- | --- | --- |
| `Vector 34 (Stroke)` | **`Arrow 1` · `Arrow 2`** | `Handle` ▸ `Arrow` | 4 | 기본 이름 · **같은 이름 2개가 겹침** |
| `Ellipse 5536` | **`Circle`** | `Handle` | 2 | 흰 원 배경 |
| `Union` | **`Arrow`** | `Handle` | 2 | 겹화살표 불리언 |
| `Rectangle 34624751` | **`Progress`** | `Dragging` | 1 | 68 × 48 진행 바 |
| `Frame 3467725` | **`Label`** | `Near Complete` | 1 | 아이콘 + 문구 묶음 |

`Handle`은 variant가 2개(`Enabled=True` · `False`)라 각 레이어가 **두 번씩** 잡혔습니다.

`Vector 34 (Stroke)`는 **두 벡터가 같은 이름**이라 레이어 패널에서 구분되지 않았습니다. 부모 안 순서대로 `Arrow 1` · `Arrow 2`를 붙였습니다.

정리 후 **기본 이름 0건**입니다.

[Search Field](syrup-search-field-components.md)의 `Ellipse 2` → `Circle`, `Line` → `Handle`과 같은 기준입니다.

### 7. `gold_test4 3` — 파일 전체 56건

`Near Complete`의 금 아이콘(22 × 20) 레이어명이 **`gold_test4 3`**입니다. `test4`는 작업용 이름입니다.

| 페이지 | 건수 |
| --- | --- |
| [Badge](syrup-badge-components.md) | 9 |
| [Card](syrup-card-components.md) | 8 |
| [AD](syrup-ad-components.md) · ❖Components | 각 6 |
| [List Row](syrup-list-row-components.md) · [Product Grid](syrup-product-grid-components.md) · [Progress Stepper](syrup-progress-stepper-components.md) | 각 5 |
| [Tab](syrup-design-tokens.md) | 4 |
| [Dialog](syrup-dialog-components.md) · [Grid List](syrup-grid-list-components.md) | 각 3 |
| [Banner](syrup-banner-components.md) · **Swipe** | 각 1 |
| **합계** | **56건 / 12개 페이지** |

> **앞선 기록 정정** — [Progress Stepper](syrup-progress-stepper-components.md) 문서에 `gold_test4`를 **17건**으로 적었는데, 그것은 `gold_test4 1` 하나의 이름만 센 수치였습니다. `gold_test4 2` · `3` 등을 포함한 **실제 합계는 56건**입니다.

Swipe만 고치면 나머지 55건과 어긋나므로 **파일 전체를 한 번에 맞추는 편**이 낫습니다. [Product Grid](syrup-product-grid-components.md) 등이 쓰는 `img_gold`가 같은 역할입니다.

### 8. 인스턴스 0건 — 2026-10-12 기록

| 구분 | 인스턴스 |
| --- | --- |
| `Swipe` | **0** |
| `.primitive / Swipe / Handle` | 4 (Swipe 페이지 내부) |

당시 집계에서는 Swipe 인스턴스가 없었어요. 현재는 Section 1의 사용 화면과 가이드라인·Usage에 인스턴스가 있으므로, 이 수치를 현재 사용량이나 구조 변경 영향 범위로 해석하지 않아요. 화면 하단 고정 여부도 이번 가이드라인에서 공통 사용 규칙으로 정하지 않았어요.

> **이 수치는 이 Figma 파일 기준**입니다. 다른 파일·디태치·코드 사용은 포함되지 않습니다.

---

## 정리 우선순위

### 문서 업데이트 완료 (2026-11-10)

가이드라인 3개와 Usage A~D를 반영했어요. Near Complete의 처리 중 의미, Expired의 별도 분기, Bubble 사용 기준을 명시하고 Section 1의 아노테이션을 제거했어요.

아래 구조 개선 과제는 기존 점검 제안이며, 이번 문서 업데이트에서 마스터를 수정한 항목은 아니에요.

### ✅ 완료 (2026-10-12)

모양이 바뀌지 않는 작업 **14건**을 처리했습니다.

| # | 항목 | 결과 |
| --- | --- | --- |
| 1 | 레이어명 정리 ([6](#6-레이어명-정리---완료-10건)) | **10건** |
| 2 | `Property 1` → `State` ([1](#1-property-1과-variant24-자동-생성명---완료)) | 1건 |
| 3 | `Variant2`~`4` → `Dragging` · `Near Complete` · `Expired` ([1](#1-property-1과-variant24-자동-생성명---완료)) | 3건 |

정리 후 **기본 이름 0건 · `Property 1` 0건 · 자동 생성 variant명 0건**입니다.

이 페이지의 핵심이던 **자동 생성명 문제가 해소**됐습니다. 이제 속성 패널만 보고도 `Near Complete`와 `Expired`를 구분할 수 있습니다.

### 판단 완료

| 항목 | 결론 |
| --- | --- |
| `Variant3`이 완료인가 처리 중인가 | **처리 중** — 「금 나오는 중」은 작업이 진행 중인 상태이고 완료까지 가지 않았습니다. `Done`이 아니라 **`Near Complete`**로 정했습니다 |
| `Enabled` 옵션 순서 ([5](#5-enabled-옵션-순서)) | **현행 유지** — 활성이 기본인 편이 자연스럽고, 재정렬하면 기본값이 `False`가 되어 오히려 어색합니다 |

### 남은 과제

| 순위 | 항목 | 성격 | 비용 |
| --- | --- | --- | --- |
| 1 | variant 레이어 순서·문구 레이어명 통일 ([4](#4-variant-간-레이어-순서가-다름)) | 구조 정리 | 중간 |
| 2 | TEXT 속성 추가 ([3](#3-문구가-variant에-박혀-있음)) | 구조 추가 | 중간 |
| 3 | #E7550C 토큰화 여부 ([2](#2-미바인딩-색상-3건)) | **다른 컴포넌트 확인 필요** | 중간 |
| 4 | `gold_test4` 파일 전체 56건 ([7](#7-gold_test4-3--파일-전체-56건)) | **파일 전체 작업** | 중간 |

1·2번은 함께 처리해야 효과가 있습니다. 레이어 순서와 이름을 맞춰야 TEXT 속성을 넣어도 variant 전환에서 문구가 유지됩니다.

3번은 **#E7550C가 Swipe 전용 색인지, 파일 전체의 눌림 상태 색인지**에 따라 갈립니다. 다른 컴포넌트의 눌림 처리 방식을 확인해야 판단할 수 있습니다.

4번은 이 페이지만의 문제가 아니라 **12개 페이지에 걸친 56건**이라, 파일 전체를 한 번에 다루는 편이 낫습니다.
