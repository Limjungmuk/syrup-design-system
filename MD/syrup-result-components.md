# Syrup Design System — Result 컴포넌트

| 항목 | 값 |
| --- | --- |
| Figma File | [Syrup_Design-System](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System) |
| Page / Section | `Result` 페이지 → [Result 섹션 `8461:11952`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=8461-11952) |
| 섹션 크기 | 1440 × 1683 |
| 컴포넌트 수 | **3개** (Master 1 · Child Item 2) |
| Variant 총수 | **8개** |
| 기준일 | 2026-11-10 (가이드라인·예제 순서·문구 갱신, 기존 점검 기록 유지) |
| 관련 문서 | [syrup-design-tokens.md](syrup-design-tokens.md) · [syrup-ad-components.md](syrup-ad-components.md) · [syrup-alert-components.md](syrup-alert-components.md) · [syrup-badge-components.md](syrup-badge-components.md) · [syrup-banner-components.md](syrup-banner-components.md) · [syrup-border-components.md](syrup-border-components.md) · [syrup-bottom-cta-components.md](syrup-bottom-cta-components.md) · [syrup-bottom-info-components.md](syrup-bottom-info-components.md) · [syrup-bottom-sheet-components.md](syrup-bottom-sheet-components.md) · [syrup-bubble-components.md](syrup-bubble-components.md) · [syrup-button-components.md](syrup-button-components.md) · [syrup-card-components.md](syrup-card-components.md) · [syrup-checkbox-components.md](syrup-checkbox-components.md) · [syrup-chip-components.md](syrup-chip-components.md) · [syrup-dialog-components.md](syrup-dialog-components.md) · [syrup-dim-components.md](syrup-dim-components.md) · [syrup-grid-list-components.md](syrup-grid-list-components.md) · [syrup-grid-scroll-components.md](syrup-grid-scroll-components.md) · [syrup-header-components.md](syrup-header-components.md) · [syrup-icon-button-components.md](syrup-icon-button-components.md) · [syrup-indicator-components.md](syrup-indicator-components.md) · [syrup-keypad-components.md](syrup-keypad-components.md) · [syrup-label-components.md](syrup-label-components.md) · [syrup-list-footer-components.md](syrup-list-footer-components.md) · [syrup-list-header-components.md](syrup-list-header-components.md) · [syrup-list-row-components.md](syrup-list-row-components.md) · [syrup-loader-components.md](syrup-loader-components.md) · [syrup-lottie-components.md](syrup-lottie-components.md) · [syrup-product-grid-components.md](syrup-product-grid-components.md) · [syrup-product-list-components.md](syrup-product-list-components.md) · [syrup-product-scroll-components.md](syrup-product-scroll-components.md) · [syrup-progress-stepper-components.md](syrup-progress-stepper-components.md) · [syrup-search-field-components.md](syrup-search-field-components.md) · [syrup-stepper-components.md](syrup-stepper-components.md) · [syrup-swipe-components.md](syrup-swipe-components.md) · [syrup-switch-components.md](syrup-switch-components.md) · [syrup-tab-components.md](syrup-tab-components.md) · [syrup-tab-bar-components.md](syrup-tab-bar-components.md) · [syrup-text-button-components.md](syrup-text-button-components.md) · [syrup-text-field-components.md](syrup-text-field-components.md) · [syrup-ticker-components.md](syrup-ticker-components.md) · [syrup-toast-components.md](syrup-toast-components.md) |

> 빈 상태, 오류, 완료 등 현재 상태와 다음 행동을 안내하는 컴포넌트예요.
> 아이콘 또는 서비스 이미지, 안내 문구, 버튼을 상황에 맞게 조합해요.

---

## 공개 에셋 이름 정리

2026-11-11 아래 원본의 `.primitive / ` 접두사만 제거했어요. 노드·컴포넌트 키·variant·인스턴스 연결은 유지했으며 게시 작업은 별도로 진행해요. 숨김 유지·검토 대상의 접두사는 유지해요.

| 현재 전체 이름 | 원본 노드 |
| --- | --- |
| `Result / Icon / Image` | `8464:12451` |

## 목차

1. [구성 한눈에 보기](#구성-한눈에-보기)
2. [Result — Master Component](#1-result--master-component)
3. [`.primitive / Result / Icon / Empty`](#2-primitive--result--icon--empty)
4. [`Result / Icon / Image`](#3-primitive--result--icon--image)
5. [가이드라인](#가이드라인)
6. [Usage — 사용 예제](#usage--사용-예제)
7. [예제 레이아웃과 AI 사용 기준](#예제-레이아웃과-ai-사용-기준)
8. [설계 규칙 요약](#설계-규칙-요약)
9. [점검 필요 사항](#점검-필요-사항)
10. [정리 우선순위](#정리-우선순위)

---

## 구성 한눈에 보기

마스터 1종과 시각 요소 2종으로 구성돼요. 별도 섹션에 가이드라인 4개와 Usage A~I를 정리했어요. 기존 노드·인스턴스·토큰 집계는 2026-10-12 기준이며, 추가된 Section 1과 문서 예제까지 포함한 최신 통계는 아니에요.

| 보드 위치 | 섹션 | 내용 |
| --- | --- | --- |
| y 0 | Title Bar | 페이지 제목 |
| y 434 | Section Header | Master Component |
| y 574 | (높이 545) | `Result` 1종 |
| y 1119 | Section Header | Child Items |
| y 1259 | (높이 360) | `.primitive / Result / Icon / *` 2종 |
| 별도 섹션 | [Guidelines](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11672-1792) | 가이드라인 4개 |
| 별도 섹션 | [Usage](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11672-1793) | 상태별 예제 A~I 9개 |

| # | 이름 | 타입 | Variant 축 | 크기 | 인스턴스(기존 집계) |
| --- | --- | --- | --- | --- | --- |
| 1 | `Result` | Set 2 | `Visual` (Icon·Image) + BOOLEAN 3 | 360 × 235 / 360 × 305 | **1** ([Card](syrup-card-components.md)) |
| 2 | `.primitive / Result / Icon / Empty` | Component | — | 50 × 50 | 1 (페이지 내부) |
| 3 | `Result / Icon / Image` | Set 5 | `Service` (서비스 5종) | 120 × 120 | 1 (페이지 내부) |

### 조립 방식

`Result`는 **위에서 아래로 3단**입니다.

```
Result (세로 오토레이아웃 · Padding 50/0/50/0 · Gap 16)
├─ Content (Gap 12)
│  ├─ 아이콘 또는 이미지   ← Icon BOOLEAN
│  └─ Description 「텍스트」 ← Description BOOLEAN
└─ Button                  ← Button BOOLEAN
```

`Visual`이 **1단의 시각 요소 종류**를 고르고, BOOLEAN 3개가 각 요소를 켜고 끕니다.

---

## 1. Result — Master Component

**Node** `8461:12025` · Component Set · **2 variants**

| Property | Type | Default | Options | 연결 레이어 |
| --- | --- | --- | --- | --- |
| `Visual` | VARIANT | `Icon` | `Icon` · `Image` | — |
| `Icon` | BOOLEAN | `true` | — | 아이콘/이미지 인스턴스 |
| `Description` | BOOLEAN | `true` | — | `Description` 레이어 |
| `Button` | BOOLEAN | `true` | — | `Button` 인스턴스 |

> `Visual`은 2026-10-12에 `Property 1`에서 개명했습니다 ✅

| Variant | 크기 | 1단 요소 |
| --- | --- | --- |
| `Visual=Icon` | **360 × 235** | `.primitive / Result / Icon / Empty` 50 × 50 |
| `Visual=Image` | **360 × 305** | `Result / Icon / Image` 120 × 120 |

**공통 레이아웃** — 세로 오토레이아웃 CENTER/CENTER · Padding `50 / 0 / 50 / 0` · Gap 16 (`Spacing/400`) · 배경 `Color/Gray_White`

| 레이어 | 타입 | 크기 | 내용 |
| --- | --- | --- | --- |
| `Content` | Frame | 50 × 81 / 120 × 151 | Gap 12 |
| └ 아이콘 / 이미지 | Instance | 50 × 50 / 120 × 120 | `Icon` BOOLEAN |
| └ `Description` | Text | 38 × 19 | 15 Regular `b300_15_regular` `Color/Gray_200` · `Description` BOOLEAN |
| `Button` | Instance | 64 × 38 | [Button](syrup-button-components.md) 페이지 · `Button` BOOLEAN |

두 variant의 차이는 **1단 인스턴스 하나와 그에 따른 높이뿐**이고, 2·3단은 완전히 동일합니다.

### 기존 재사용 사례

| 페이지 | 경로 | Variant | 인스턴스 크기 |
| --- | --- | --- | --- |
| [Card](syrup-card-components.md) | `Card / Invite / Code` ▸ `Property 1=Empty` ▸ `List` | `Visual=Icon` | **276 × 126** |

마스터 360 × 235가 **276 × 126으로 줄어** 쓰이고 있습니다. 높이가 109 줄었으므로 하위 요소 일부가 꺼졌거나 Padding이 재정의된 상태입니다.

---

## 2. `.primitive / Result / Icon / Empty`

**Node** `8461:12301` · Component · **50 × 50**

| 항목 | 값 |
| --- | --- |
| 레이아웃 | 가로 오토레이아웃 **CENTER / CENTER** |
| Padding | **0** |
| Gap | **0** |
| **테두리** | **`Color/Gray_700` (#D2D2D2) 1px** |
| 라운드 | `Corner radius/circle` (100) |
| 배경 | 없음 |

| 레이어 | 타입 | 크기 | 위치 | 색상 |
| --- | --- | --- | --- | --- |
| `Union` | Boolean Op | 4.23 × 22.34 | y 13.83 | `Color/Gray_700` |
| └ `Bar` | Vector | 4.08 × 16.91 | y 13.83 | `Color/Gray_700` |
| └ `Dot` | Ellipse | 4.23 × 4.23 | y 31.94 | `Color/Gray_700` |

**`Color/Gray_700` 1px 테두리가 그리는 원** 안에, 같은 색 느낌표(!)가 들어 있는 구조입니다. 세로 막대(16.91) 아래 점(4.23)이 떨어져 있습니다.

이름은 `Empty`인데 그려진 기호는 느낌표입니다 → [점검 3](#3-empty라는-이름과-느낌표-아이콘).

라운드는 **이 테두리를 원형으로 만드는 값**이라 반드시 필요합니다 → [점검 4](#4-원형-라운드---정정).

### 정렬 방식 변경 (2026-10-12)

| 항목 | 변경 전 | 변경 후 |
| --- | --- | --- |
| Padding | `14 / 23 / 14 / 23` | **0** |
| Gap | 10 | **0** |
| 정렬 | MIN / CENTER | **CENTER / CENTER** |

Padding 수치로 아이콘 위치를 잡던 방식에서 **오토레이아웃 가운데 정렬**로 바뀌었습니다.

| 축 | `Union` 위치 | 계산 |
| --- | --- | --- |
| 가로 | x 22.89 | (50 − 4.23) ÷ 2 = 22.885 |
| 세로 | y 13.83 | (50 − 22.34) ÷ 2 = 13.83 |

결과는 이전과 **같은 자리**인데, 하드코딩된 14 / 23이 사라져 아이콘 크기가 바뀌어도 가운데가 유지됩니다. 토큰이 없던 Padding 2종도 함께 해소됐습니다 → [점검 6](#6-padding-50-미바인딩).

---

## 3. `Result / Icon / Image`

**Node** `8464:12451` · Component Set · **5 variants** · 모두 **120 × 120**

| Property | Type | Options |
| --- | --- | --- |
| `Service` | VARIANT | `Challenge` · `Live` · `Favorite` · `Now-Empty` · `Now-Gold` |

> `Service`는 2026-10-12에 `Property 1`에서 개명했습니다 ✅

| Variant | 구조 | 크기 | 비고 |
| --- | --- | --- | --- |
| `Challenge` | `Image` | 103.73 × 103.73 | — |
| `Live` | `Image` + `Badge` | 120 × 120, 31.86 × 27.39 | `Badge`가 우상단(x 81.77, y 19.12)에 겹침 |
| `Favorite` | `Image` | 80 × 102 | — |
| `Now-Empty` | `Illustration` ▸ `Image 1`·`Image 2` | 90 × 90 | 배경 `Color/Third_Pastel_Yellow` · 숨겨진 1장 삭제됨 ✅ |
| `Now-Gold` | `Illustration` ▸ `Image` | 90 × 90 | 배경 `Color/Third_Pastel_Yellow` · 이미지 94 × 142가 프레임 밖으로 넘침 (의도) |

서비스·상태별 이미지 5종이에요. 빈 상태뿐 아니라 완료나 다음 동작 안내에도 사용해요. 앞 3개는 이미지를 바로 올렸고, 뒤 2개는 `Color/Third_Pastel_Yellow` 배경 프레임 위에 이미지를 얹은 2단 구조입니다.

레이어명은 전부 정리했습니다 ✅ → [점검 5](#5-레이어명-정리---완료-16건). `Now-Empty`의 숨겨진 레이어도 삭제됐습니다 → [점검 9](#9-숨겨진-레이어와-프레임-넘침--처리-완료).

---

## 가이드라인

### 1. 현재 상태와 필요한 안내를 분명하게 전달해요

내역이나 검색 결과가 없을 때는 무엇이 없는지 안내해요. 불러오기 실패는 빈 결과와 구분해 설명해요. 다음 행동이나 다시 확인할 시점이 있으면 문구에 함께 담아요.

[Figma 가이드라인 1](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11672-1794)

### 2. 안내 목적에 맞는 시각 요소를 사용해요

일반적인 빈 상태나 오류는 Visual=Icon, 서비스 맥락을 함께 보여줄 때는 Visual=Image를 사용해요. 간단한 영역 안내는 Icon=False로 문구만 표시할 수 있어요. 서비스 이미지는 내용에 맞게 선택해요.

`Visual`은 종류를 선택하는 VARIANT, `Icon`은 시각 요소의 표시 여부를 제어하는 BOOLEAN이에요. `Visual=Image`일 때도 `Icon=False`이면 서비스 이미지가 숨겨져요. `Image=False`라는 속성을 임의로 만들지 않아요.

[Figma 가이드라인 2](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11672-1847)

### 3. 바로 실행할 수 있는 동작이 있을 때 버튼을 사용해요

재시도처럼 사용자가 바로 실행할 동작이 있으면 Button=True로 표시해요. 단순 안내만 필요하면 Button=False로 숨기고, 버튼에는 실행할 동작을 구체적으로 적어요.

[Figma 가이드라인 3](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11672-1898)

### 4. 사용하는 영역에 맞춰 크기와 여백을 조정해요

Result의 폭과 높이는 전체 화면이나 목록·카드 등 사용 영역에 맞춰 조정해요. 상하 여백도 영역에 맞게 조정하고, 안내 문구와 버튼이 잘리지 않도록 필요한 높이를 확보해요.

마스터의 폭 360과 상하 패딩 50은 기본 구성이고 모든 사용처의 고정 규격이 아니에요. 안내 요소는 컴포넌트 내부에서 가운데 정렬을 유지하고, 문서 슬롯에 추가 패딩을 넣어 위치를 보정하지 않아요.

[Figma 가이드라인 4](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11672-1951)

---

## Usage — 사용 예제

[Usage 섹션](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11672-1793)은 같은 구성의 문구 차이 → 버튼·시각 요소 차이 → 서비스별 상태 안내 순서로 구성했어요. A·B·C는 같은 컴포넌트 구성을 사용하지만 상태와 다음 행동을 구분하기 위해 별도 예제로 유지해요. 서로 다른 Variant를 뜻하지 않아요.

| 순서 / 예제 | 구성 | 설명 |
| --- | --- | --- |
| [A. 내역이 없는 경우](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11672-2004) | `Visual=Icon`, `Icon=True`, `Button=False` | 표시할 내역이 없을 때 무엇이 없는지 안내해요. 일반적인 빈 상태는 아이콘과 문구로 구성해요. |
| [B. 검색 결과가 없는 경우](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11672-2031) | A와 같은 구성 | 검색 결과가 없음을 알리고 검색어를 다시 확인하도록 안내해요. 불러오기 오류와 구분해 표현해요. |
| [C. 일시적인 오류 안내](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11672-2137) | A와 같은 구성 | 직접 실행할 동작을 제공하지 않는 오류 안내는 Button=False로 사용해요. 잠시 후 다시 확인할 수 있도록 안내해요. |
| [D. 재시도가 필요한 경우](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11672-2085) | `Visual=Icon`, `Button=True` | 불러오기 실패를 안내하고 다시 시도할 수 있는 버튼을 제공해요. Button=True로 설정하고 동작을 구체적으로 적어요. |
| [E. 문구만 사용하는 경우](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11672-2058) | `Icon=False`, `Button=False` | 목록이나 카드 안의 간단한 안내는 Icon=False, Button=False로 문구만 표시할 수 있어요. |
| [F. 서비스 콘텐츠 준비 중](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11672-2112) | `Visual=Image`, `Service=Challenge`, `Button=False` | 서비스에 맞는 이미지와 안내 문구를 함께 사용해요. 챌린지 예제는 Visual=Image와 Service=Challenge를 사용해요. |
| [G. 오늘의 콘텐츠를 모두 확인한 경우](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11672-2164) | `Visual=Image`, `Service=Now-Empty`, 어두운 배경 | 단순한 내역 없음과 구분해 콘텐츠를 모두 확인했음을 알려요. 새로운 콘텐츠를 확인할 시점을 함께 안내해요. 배경색에 맞춰 안내 문구의 색상을 조정해요. |
| [H. 리워드 받기 완료](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11672-2189) | `Visual=Image`, 어두운 배경 | 리워드를 받은 결과를 이미지와 문구로 알려요. 예제의 금액은 실제 지급 결과에 맞춰 표시해요. |
| [I. 광고 재생 전 안내](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11672-2214) | `Visual=Image`, 어두운 배경 | 광고 재생 전에 다음에 일어날 동작을 안내해요. 문구의 대기 시간은 실제 동작에 맞춰 표시해요. |

### 문구와 상태 구분

- A는 데이터가 없는 상태, B는 검색 결과가 없는 상태, C는 조회에 실패한 상태예요. 같은 아이콘·문구 구성을 사용해도 의미를 섞지 않아요.
- C는 직접 실행할 동작이 없는 오류 안내, D는 재시도 동작을 제공하는 안내예요. 모든 오류에 버튼을 일괄 추가하지 않아요.
- G는 아직 내역이 없는 상태와 달리, 오늘의 콘텐츠를 모두 확인했다는 뜻이에요. 다음에 확인할 시점을 함께 안내해요.
- G의 배경별 문구 색상 기준은 H·I에도 적용해요. 같은 설명을 각 예제에 반복하지 않아요.
- H는 지급 완료, I는 광고 재생 전 안내예요. 금액·대기 시간은 실제 상태에 맞게 사용하며 예제의 3금·3초를 공통 규격으로 고정하지 않아요.

### 예제 문구 정리 완료

2026-11-10 H의 내부 Result 문구를 “3금을 받았어요!”로 수정했어요. H는 리워드 수령 완료, I의 “3초 후 금 받는 광고가 재생됩니다”는 광고 재생 전 안내로 구분해요. H의 3금 배지와 안내 금액은 서로 일치하며, 실제 사용 시 지급 결과에 맞춰 함께 변경해요.

## 예제 레이아웃과 AI 사용 기준

- 단독 Result는 불필요한 `화면` 프레임 없이 슬롯에 직접 배치할 수 있어요. 배경이나 별도 보조 요소를 구성해야 하는 경우에만 필요한 프레임을 사용해요.
- 슬롯의 추가 패딩은 제거하고 좌측·상단 정렬로 배치해요. Result 자체의 가운데 정렬과 내부 여백은 별개로 유지해요.
- 가이드라인과 예제의 공통 설명은 아이콘·버튼·서비스 이미지 선택 기준이고, 상태별 예제 A~I는 별도 컴포넌트 유형을 추가하는 규칙이 아니에요.
- 서비스 이미지는 안내 내용을 설명하는 핵심 요소이므로 단순히 예제를 간결하게 만든다는 이유로 숨기지 않아요. 문구만 필요한 경우에는 `Icon=False`로 구성해요.
- 배경색에 맞춰 안내 문구 색상을 조정해요. 어두운 배경에는 읽을 수 있는 밝은 텍스트를 사용하고, 적용 가능한 기존 색상 토큰을 활용해요. 기본 흰 배경·기본 텍스트 색을 모든 사용처에 강제하지 않아요.
- 현재 예제 설명은 3줄에 맞춰 줄바꿈을 조정한 문서 레이아웃이에요. 끝줄 정렬을 위한 빈 줄은 실제 서비스 문구에 포함하는 데이터가 아니에요.
- Result 내부의 안내 문구는 상태에 필요한 내용이 잘리지 않게 구성해요. Description을 켜고, 실행 가능한 동작이 있을 때만 Button을 켜요.
- 마스터 크기와 상하 여백을 화면 전체 규격으로 해석하지 않아요. 사용 영역과 안내 내용에 맞춰 조정하고 원본 인스턴스 연결을 유지해요.

---

## 설계 규칙 요약

### 구조

| 단 | 요소 | 제어 |
| --- | --- | --- |
| 1 | 아이콘 50 × 50 **또는** 이미지 120 × 120 | `Visual` + `Icon` BOOLEAN |
| 2 | 안내 문구 15 Regular | `Description` BOOLEAN |
| 3 | 버튼 64 × 38 | `Button` BOOLEAN |

세 요소를 모두 끄면 **Padding 50 + 50만 남은 빈 프레임**이 됩니다. Figma가 막지 않으므로 사용 측 주의가 필요합니다.

### 토큰 적용 상태

| 항목 | 상태 |
| --- | --- |
| 배경 | `Color/Gray_White` 바인딩 ✅ |
| 아이콘 색 | `Color/Gray_700` 바인딩 ✅ |
| 일러스트 색 | `Color/Third_Pastel_Yellow` 바인딩 ✅ |
| 테두리 | `Color/Gray_700` 바인딩 ✅ |
| 텍스트 색 | `Color/Gray_200` 바인딩 ✅ |
| 텍스트 스타일 | `b300_15_regular` 적용 ✅ · **미적용 0건** |
| Gap | 16(`Spacing/400`) 바인딩 ✅ |
| 라운드 | `Corner radius/circle` 바인딩 ✅ |
| Padding | **50 미바인딩** — 대응 토큰 없음 (14 / 23은 해소 ✅) |
| 원격 텍스트 스타일 | **0건** ✅ |
| 미바인딩 색상 | **0건** ✅ |
| 줄 구분자(U+2028/9) | **0건** ✅ |

**지금까지 문서화한 33개 페이지 중 토큰 적용이 가장 깨끗합니다.** 미바인딩 색상·스타일 미적용 텍스트·원격 스타일이 모두 0건이고, 남은 것은 대응 토큰 자체가 없는 Padding 3종뿐입니다.

---

## 점검 필요 사항

> 아래는 2026-10-12의 점검 기록이에요. 이번 갱신은 최신 가이드라인·예제 순서·문구와 사용 기준 문서화이며, 파일 전체의 토큰·스타일·인스턴스 건수는 재집계하지 않았어요. 과거 검토 제안은 확정된 사용 규칙과 구분해요.

### 1. `Property 1` 2건 — ✅ 완료

| 컴포넌트 | 변경 전 | 변경 후 | 근거 |
| --- | --- | --- | --- |
| `Result` `8461:12025` | `Property 1` | **`Visual`** | 1단 시각 요소의 종류 (`Icon` · `Image`) |
| `Result / Icon / Image` `8464:12451` | `Property 1` | **`Service`** | 서비스 구분 (`Challenge` 등 5종) |

variant 이름도 `Visual=Icon` · `Service=Challenge` 형태로 따라 바뀌었습니다. 파일 전체 `Property 1` 집계에서 2건이 빠집니다.

### 2. `Icon` 이름이 두 가지로 쓰임 — ✅ 해소

```
변경 전   Property 1 = Icon | Image   ← 시각 요소의 종류
          Icon       = BOOLEAN         ← 그 요소의 표시 여부

변경 후   Visual     = Icon | Image
          Icon       = BOOLEAN
```

같은 컴포넌트 안에서 `Icon`이 서로 다른 두 가지를 가리켰습니다. `Visual=Image`일 때 `Icon` BOOLEAN은 아이콘이 아니라 **이미지**를 끄고 켜는데, 속성 패널에 `Icon`이 두 번 보여 혼동을 불렀습니다. [점검 1](#1-property-1-2건---완료)의 개명으로 해소됐습니다.

`Description` BOOLEAN이 제어하는 레이어명도 `Text` → **`Description`**으로 맞췄습니다 ✅

다만 **`Icon` BOOLEAN이라는 이름 자체는 그대로**입니다. `Visual=Image`에서도 `Icon`이 이미지를 제어하므로, 엄밀히는 `Show Visual` 같은 이름이 정확합니다. 영향이 작아 판단에 맡깁니다.

### 3. `Empty`라는 이름과 느낌표 아이콘

`.primitive / Result / Icon / Empty`가 그리는 것은 **느낌표(!)**입니다. 세로 막대 + 점 구조가 그렇습니다.

| 해석 | 적절한 이름 |
| --- | --- |
| 빈 상태를 뜻하는 아이콘 | `Empty` (현행 유지) |
| 경고·안내를 뜻하는 기호 | `Caution` · `Notice` |

느낌표는 통상 **주의**를 뜻하므로, 빈 상태 전용이라면 모양 쪽을 바꾸는 선택지도 있습니다. 어느 쪽이 의도인지 확인이 필요합니다.

또한 `Result / Icon / Image`의 variant에도 **`Now-Empty`**가 있어, 같은 페이지에서 `Empty`가 두 층위로 쓰입니다.

### 4. 원형 라운드 — ⚠️ 정정

**이 항목의 앞선 기록은 틀렸습니다.**

`.primitive / Result / Icon / Empty`의 라운드를 "배경이 없어 화면에 드러나지 않는다"고 판단해 0으로 제거했는데, 실제로는 **모양이 원에서 사각형으로 바뀌었습니다.** 사용자가 `Corner radius/circle`(100)로 되돌렸습니다.

| 속성 | 값 | 실제 역할 |
| --- | --- | --- |
| **테두리** | **`Color/Gray_700` 1px** | **원을 그리는 선** |
| 라운드 | `Corner radius/circle` | **그 선을 원형으로 만듦** |
| Padding | 0 | 가운데 정렬로 대체됨 |
| Gap | 0 | 자식이 1개라 영향 없음 |

> **교훈 — "배경이 없으니 라운드는 무효"는 성립하지 않습니다.**
>
> 라운드는 배경뿐 아니라 **테두리·클리핑·그림자**의 모서리도 결정합니다. 이 컴포넌트는 배경 없이 **테두리만으로** 원을 그리고 있었습니다.
>
> 스캔 결과에 테두리가 드러나지 않았는데, 그 상태로 "보이는 결과가 바뀌지 않는다"고 단정한 것이 문제였습니다. **모양에 영향을 줄 수 있는 값을 지울 때는 fill·stroke·effect·clipsContent를 모두 확인**해야 합니다.
>
> 이 문서의 다른 "무손실" 판단과 [Progress Stepper](syrup-progress-stepper-components.md)의 `라운드 23 → circle` 건도 같은 기준으로 다시 볼 필요가 있습니다. 다만 Progress Stepper 쪽은 **40 × 40 도형의 radius 23 → 100**이라 둘 다 원이 되는 변경이어서 결과가 같습니다.

### 4-1. 인스턴스에 Gap 재정의가 남음

| 노드 | Padding | Gap |
| --- | --- | --- |
| 원본 `.primitive / Result / Icon / Empty` | 0 | **0** |
| `Result` ▸ `Content` 안의 인스턴스 | 0 | **10** |

원본의 Gap을 0으로 바꾸면서 인스턴스에 **10이 재정의로 남았습니다.** Padding과 정렬은 따라왔지만 Gap만 어긋나 있습니다.

자식이 1개라 **화면에는 영향이 없습니다.** 인스턴스에서 Gap을 0으로 맞추거나 재정의를 초기화하면 해소됩니다.

### 5. 레이어명 정리 — ✅ 완료 (16건)

| 변경 전 | 변경 후 | 위치 | 건수 | 근거 |
| --- | --- | --- | --- | --- |
| `Icon+Text` | `Content` | `Result` | 2 | `+` 결합 표기 제거 |
| `Text` | `Description` | `Result` | 2 | `Description` BOOLEAN과 일치 |
| `Component 3` | `Illustration` | `Image` ▸ `Now-*` | 2 | **FRAME인데 이름이 `Component`** |
| `IT_td05200000619 1` | `Image` | `Image` ▸ `Challenge` | 1 | 작업용 에셋 파일명 |
| `image 3` | `Image` | `Image` ▸ `Live` | 1 | 기본 이름 |
| `image 4` | `Badge` | `Image` ▸ `Live` | 1 | 우상단 31.86 × 27.39 겹침 요소 |
| `image 3241` | `Image` | `Image` ▸ `Favorite` | 1 | 기본 이름 |
| `image 3260` | `Image` | `Image` ▸ `Now-Gold` | 1 | 기본 이름 |
| `image 3346·3347·3348` | `Image 1·2·3` | `Image` ▸ `Now-Empty` | 3 | 겹쳐 쌓인 3장 |
| `Rectangle 218` | `Bar` | `Empty` ▸ `Union` | 1 | 느낌표 세로 막대 |
| `Oval 190` | `Dot` | `Empty` ▸ `Union` | 1 | 느낌표 아래 점 |

[Progress Stepper](syrup-progress-stepper-components.md)에서 쓴 기준(공백 구분 · 대문자 시작 · 역할을 드러내는 이름)을 그대로 적용했습니다.

### 6. Padding 50 미바인딩

| 값 | 건수 | 위치 | 대응 토큰 | 상태 |
| --- | --- | --- | --- | --- |
| 50 | 4 | `Result` 두 variant의 상하 | **없음** (최대 `Spacing/900`=36) | 판단 필요 |
| ~~14~~ | ~~2~~ | ~~`Empty` 상하~~ | — | ✅ 가운데 정렬로 대체 |
| ~~23~~ | ~~2~~ | ~~`Empty` 좌우~~ | — | ✅ 가운데 정렬로 대체 |

`Empty`의 14 / 23은 **오토레이아웃 CENTER 정렬로 바뀌며 사라졌습니다.** 수치로 위치를 잡던 것을 정렬로 대체한 방식이라, 토큰 없는 값을 늘리지 않으면서 같은 결과를 얻습니다.

남은 것은 `Result`의 Padding 50 네 건입니다. Spacing 스케일이 `50`(2)부터 `900`(36)까지라 **50px를 담을 토큰이 없습니다.** 빈 상태는 화면 가운데에 여백을 크게 두는 요소라 50이 과한 값은 아닙니다.

| 선택지 | 내용 |
| --- | --- |
| A | 현행 유지 — 빈 상태 전용 여백으로 두고 미바인딩 허용 |
| B | `Spacing` 스케일에 큰 값(40 · 48 · 50) 추가 |
| C | 48 등으로 낮춰 기존 스케일에 흡수 |

### 7. 인스턴스 1건 — 사용처가 매우 좁음

| 구분 | 인스턴스 |
| --- | --- |
| `Result` | **1** ([Card](syrup-card-components.md) ▸ `Card / Invite / Code`) |
| `.primitive / … / Empty` | 1 (Result 페이지 내부) |
| `.primitive / … / Image` | 1 (Result 페이지 내부) |

당시에는 Card 한 곳에서만 집계됐지만, 현재 Section 1과 Usage에는 다양한 빈 상태·오류·완료 안내 사례가 추가됐어요. 과거 1건 집계를 현재 사용 범위로 해석하지 않아요.

| 가능성 | 확인 방법 |
| --- | --- |
| 각 화면이 빈 상태를 직접 그려 씀 | 다른 페이지에서 비슷한 레이아웃 탐색 |
| 제품 화면 파일이 따로 있음 | 이 파일 밖의 사용 현황 확인 |
| 아직 확산 전인 신규 컴포넌트 | 도입 계획 확인 |

서비스 이미지의 과거 사용 건수도 최신 사용 현황이 아니에요. 현재 Usage에서는 Challenge·Now-Empty와 서비스별 결과 이미지를 사용해요.

> **이 수치는 이 Figma 파일 기준**입니다. 다른 파일·디태치·코드 사용은 포함되지 않습니다.

### 8. Card에서 마스터보다 작게 축소됨

| 구분 | 크기 |
| --- | --- |
| 마스터 `Visual=Icon` | 360 × 235 |
| Card의 인스턴스 | **276 × 126** |

높이 **109 차이**는 하위 요소가 꺼졌거나 Padding 50이 재정의된 결과입니다. 폭 276은 Card 내부 폭에 맞춘 것으로 보입니다.

빈 상태를 카드 안에 넣는 용도가 자주 생긴다면 **좁은 폭 전용 variant**를 두는 쪽이 재정의를 줄입니다. 지금은 1건뿐이라 당장 필요하지는 않습니다.

### 9. 숨겨진 레이어와 프레임 넘침 — 처리 완료

레이어명을 정리하며 `Result / Icon / Image` 내부에서 두 가지를 찾았고, 둘 다 정리됐습니다.

| Variant | 레이어 | 내용 | 결과 |
| --- | --- | --- | --- |
| `Now-Empty` | `Image 1` (이전 `image 3346`) 106 × 81 | `visible: false` — 교체 전 버전 잔존 | **삭제 완료** ✅ |
| `Now-Gold` | `Image` (이전 `image 3260`) 94 × 142 | `Illustration` 90 × 90을 넘침 (x −3, y −8) | **의도 — 유지** |

`Now-Empty`는 이제 `Image 1`(106 × 76) · `Image 2`(108 × 74) 두 장만 남았습니다.

### 9-1. `Image 2` · `Image 3` 번호 재정렬 — ✅ 완료

`Image 1`이 삭제되면서 **`Image 2`부터 시작하는 번호**가 됐습니다.

| 변경 전 | 변경 후 |
| --- | --- |
| `Image 2` (106 × 76) | **`Image 1`** |
| `Image 3` (108 × 74) | **`Image 2`** |

`Image 1` 삭제로 2부터 시작하던 번호를 당겨 맞추었습니다.

---

## 정리 우선순위

### ✅ 완료 (2026-10-12)

레이어명·속성명 **20건**을 처리했습니다. 라운드 제거 1건은 모양을 바꿔 되돌렸습니다([점검 4](#4-원형-라운드---정정)).

| # | 항목 | 결과 |
| --- | --- | --- |
| 1 | 레이어명 정리 ([5](#5-레이어명-정리---완료-16건)) | **16건** |
| 1-1 | `Image` 번호 재정렬 ([9-1](#9-1-image-2--image-3-번호-재정렬---완료)) | 2건 |
| 2 | `Property 1` → `Visual` · `Service` ([1](#1-property-1-2건---완료)) | 2건 |
| 3 | `Text` → `Description` ([2](#2-icon-이름이-두-가지로-쓰임---해소)) | 레이어명 2건 (위 16건에 포함) |
| 4 | `Empty` Gap 제거 ([4-1](#4-1-인스턴스에-gap-재정의가-남음)) | 1건 · 인스턴스 재정의 발생 |
| — | ~~`Empty` 라운드 제거~~ | **철회** — 원→사각형 변형 |

정리 후 기본 이름 **0건**, `Property 1` **0건**입니다. 사용자가 `Corner radius/circle` 복원과 `Now-Empty` 숨김 레이어 삭제를 직접 처리했습니다.

### 남은 과제

| 순위 | 항목 | 성격 | 비용 |
| --- | --- | --- | --- |
| 1 | `Empty` 인스턴스 Gap 재정의 ([4-1](#4-1-인스턴스에-gap-재정의가-남음)) | 값 일치 · 화면 영향 없음 | 낮음 |
| 2 | `Empty` 이름 vs 느낌표 모양 ([3](#3-empty라는-이름과-느낌표-아이콘)) | 판단 필요 | 낮음 |
| 3 | `Icon` BOOLEAN 이름 ([2](#2-icon-이름이-두-가지로-쓰임---해소)) | 판단 필요 | 낮음 |
| 4 | Padding 50 토큰화 여부 ([6](#6-padding-50-미바인딩)) | 판단 필요 | 중간 |
| 5 | Image variant 4종의 사용 계획 ([7](#7-인스턴스-1건--사용처가-매우-좁음)) | 확인 필요 | — |
| 6 | 좁은 폭 variant 신설 ([8](#8-card에서-마스터보다-작게-축소됨)) | 구조 추가 | 중간 |

토큰 측면은 이미 깨끗해서, 남은 과제가 전부 **네이밍 판단과 사용 현황 확인**입니다.
