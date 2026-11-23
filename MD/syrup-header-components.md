# Syrup Design System — Header 컴포넌트

| 항목 | 값 |
| --- | --- |
| Figma File | [Syrup_Design-System](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System) |
| Page / Section | `Header` 페이지 → [Header 섹션 `8533:26889`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=8533-26889) |
| 섹션 구성 | Header 1440×2301 → Guidelines 960×1084 → Usage 2960×458 |
| 컴포넌트 수 | **4개** (전부 Component Set) |
| 기준일 | 2026-11-06 (Header 페이지 규격 · Guidelines · Usage 확인) |
| 관련 문서 | [syrup-design-tokens.md](syrup-design-tokens.md) · [syrup-ad-components.md](syrup-ad-components.md) · [syrup-dialog-components.md](syrup-dialog-components.md) · [syrup-alert-components.md](syrup-alert-components.md) · [syrup-badge-components.md](syrup-badge-components.md) · [syrup-banner-components.md](syrup-banner-components.md) · [syrup-border-components.md](syrup-border-components.md) · [syrup-bottom-info-components.md](syrup-bottom-info-components.md) · [syrup-bottom-cta-components.md](syrup-bottom-cta-components.md) · [syrup-bottom-sheet-components.md](syrup-bottom-sheet-components.md) · [syrup-bubble-components.md](syrup-bubble-components.md) · [syrup-button-components.md](syrup-button-components.md) · [syrup-card-components.md](syrup-card-components.md) · [syrup-checkbox-components.md](syrup-checkbox-components.md) · [syrup-chip-components.md](syrup-chip-components.md) · [syrup-dim-components.md](syrup-dim-components.md) · [syrup-grid-list-components.md](syrup-grid-list-components.md) · [syrup-grid-scroll-components.md](syrup-grid-scroll-components.md) · [syrup-icon-button-components.md](syrup-icon-button-components.md) · [syrup-indicator-components.md](syrup-indicator-components.md) · [syrup-keypad-components.md](syrup-keypad-components.md) · [syrup-label-components.md](syrup-label-components.md) · [syrup-list-footer-components.md](syrup-list-footer-components.md) · [syrup-list-header-components.md](syrup-list-header-components.md) · [syrup-list-row-components.md](syrup-list-row-components.md) · [syrup-loader-components.md](syrup-loader-components.md) · [syrup-lottie-components.md](syrup-lottie-components.md) · [syrup-product-grid-components.md](syrup-product-grid-components.md) · [syrup-product-list-components.md](syrup-product-list-components.md) · [syrup-product-scroll-components.md](syrup-product-scroll-components.md) · [syrup-progress-stepper-components.md](syrup-progress-stepper-components.md) · [syrup-result-components.md](syrup-result-components.md) · [syrup-search-field-components.md](syrup-search-field-components.md) · [syrup-stepper-components.md](syrup-stepper-components.md) · [syrup-swipe-components.md](syrup-swipe-components.md) · [syrup-switch-components.md](syrup-switch-components.md) · [syrup-tab-components.md](syrup-tab-components.md) · [syrup-tab-bar-components.md](syrup-tab-bar-components.md) · [syrup-text-button-components.md](syrup-text-button-components.md) · [syrup-text-field-components.md](syrup-text-field-components.md) · [syrup-ticker-components.md](syrup-ticker-components.md) · [syrup-toast-components.md](syrup-toast-components.md) |

> **화면 상단에서 뒤로가기, 닫기와 화면별 부가 기능을 제공하는 컴포넌트예요.**
> 신규 화면에서는 뒤로가기 버튼 옆 타이틀을 숨기고, 필요한 기능과 상태를 표시해요.

---

## 공개 에셋 이름 정리

2026-11-11 아래 원본의 `.primitive / ` 접두사만 제거했어요. 노드·컴포넌트 키·variant·인스턴스 연결은 유지했으며 게시 작업은 별도로 진행해요. 숨김 유지·검토 대상의 접두사는 유지해요.

| 현재 전체 이름 | 원본 노드 |
| --- | --- |
| `Header / Icon` | `8533:27224` |

## 목차

1. [구성 한눈에 보기](#구성-한눈에-보기)
2. [Header — Master Component](#1-header--master-component)
3. [Child Items — Right Area](#2-child-items--right-area)
4. [Icon](#3-icon)
5. [설계 규칙 요약](#설계-규칙-요약)
6. [Usage](#usage)
7. [Guidelines](#guidelines)
8. [AI 도구 적용 기준](#ai-도구-적용-기준)
9. [현재 확인 사항](#현재-확인-사항)

---

## 구성 한눈에 보기

마스터 섹션은 1440×2301이며, 최상위 컴포넌트 정의는 Component Set 4개입니다. 마스터와 별도로 Guidelines 3항목, Usage 7패턴을 구성했습니다. 전체 노드·인스턴스 수는 문서 추가 이전의 집계와 구분합니다.

| 보드 위치 | 섹션 | 내용 |
| --- | --- | --- |
| y 434 | Master Component | `Header` 7종 |
| y 1321 → 1461 | Child Items → Right Area | `Tailing Acc` · `Timer` |
| y 1831 | Icon | `Header / Icon` 5종 |

| # | 이름 | 타입 | Variant / Props | 크기 | 이전 집계 인스턴스 (2026-10-12) |
| --- | --- | --- | --- | --- | --- |
| 1 | `Header` | Set | `Type` × `Theme` × `Alarm` × `Timer` × `Inquiry` (**7종**) | 360 × 55 / 57 | **0** |
| 2 | `.primitive / Header / Tailing Acc` | Set | `Alert` 2종 + `Bubble` | 65~77 × 18 | 1 |
| 3 | `.primitive / Header / Timer` | Set | `Complete` 2종 | 32 × 32 | 1 |
| 4 | `Header / Icon` | Set | `Property 1` × `Theme` (**5종**) | 32~36 정사각 | 10 |

---

## 1. Header — Master Component

**Node** `8533:26685` · Component Set · **7 variants**

### Properties

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `Type` | VARIANT | `Back` | `Close` · `Back` · `Todo` |
| `Theme` | VARIANT | `Light` | `Light` · `Dark` |
| `Alarm` | VARIANT | `False` | `False` · `True` |
| `Timer` | VARIANT | `False` | `False` · `True` |
| `Inquiry` | VARIANT | `False` | `False` · `True` |
| `Title` | BOOLEAN | `true` | — |
| `NumberIcon` | BOOLEAN | `false` | — |

**지원 조합은 아래 7개입니다.** Alarm·Timer·Inquiry는 Back에만 제공되며 동시에 사용하지 않습니다. Close는 Light/Dark, Todo는 Light만 지원합니다. 이론적 48조합을 모두 지원한다고 해석하지 않습니다.

**Title 마스터 기본값은 true지만 신규 Back 화면의 권장값은 false입니다.** `Title#8533:0=false`를 명시합니다. Todo 영역명과 타이머·알림 안내 문구는 페이지 타이틀과 구분해 유지합니다.

### Variant별 스펙

| Variant | 크기 | Padding (T/R/B/L) | Gap | 배경 |
| --- | --- | --- | --- | --- |
| `Back` 기본 | 360 × 55 | **9.5** / 16 / **9.5** / 8 | `Spacing/50` (2) | `Color/Gray_White` |
| `Back` + `Alarm` | 360 × 55 | **9.5** / 16 / **9.5** / 8 | `Spacing/500` (20) | `Color/Gray_White` |
| `Back` + `Inquiry` | 360 × 55 | **9.5** / 16 / **9.5** / 8 | `Spacing/500` (20) | `Color/Gray_White` |
| `Back` + `Timer` | 360 × 55 | **9.5** / 20 / **9.5** / 8 | `Spacing/250` (10) | `Color/Gray_White` |
| `Close` · `Light` | 360 × 55 | **9.5** / 12 / **9.5** / 16 | `Spacing/200` (8) | `Color/Gray_White` |
| `Close` · `Dark` | 360 × 55 | **9.5** / 12 / **9.5** / 16 | `Spacing/200` (8) | **없음** |
| `Todo` | 360 × **57** | **0** / 16 / **0** / 16 | 0 | `Color/Gray_White` |

현재 규격을 유지합니다.

### 높이와 Auto Layout

- 일반 Header는 **55**, Todo는 **57**입니다. 가로는 화면 폭에 맞춰 Fill을 사용할 수 있지만 **세로 Fill로 남은 화면 높이를 채우지 않습니다.**
- 현재 마스터의 Back 기본·Alarm·Inquiry는 세로 Fixed, Back Timer·Close Light/Dark·Todo는 Hug입니다. 문서 예제의 일부 인스턴스도 Hug로 정리되어 있습니다. 정상적인 Fixed를 모두 Hug로 바꿔야 한다는 의미는 아닙니다.
- Hug 적용 후 내부 요소의 세로 Fill 때문에 높이가 늘지 않는지 확인하고 최종 높이 55/57로 검증합니다.
- Bubble은 Header 밖으로 표시될 수 있습니다. 말풍선 높이를 Header 본체 높이에 합산하지 않고, 잘림과 겹침을 확인합니다.

규격 보충:

- **상하 패딩이 `9.5`**이며 현재 높이 55를 구성하는 값입니다. 별도 디자인 결정 없이 반올림하거나 높이를 바꾸지 않습니다.
- **좌우 패딩이 variant마다 다릅니다** — `Back` 계열은 좌 8 / 우 16~20, `Close`는 좌 16 / 우 12. 버튼 위치에 따라 조정한 값으로 보입니다.
- **`Todo`만 높이 57**이고 상하 패딩이 0입니다. 다른 여섯은 55입니다.

### Theme

`Theme=Dark`는 **`Close` 조합 하나**에만 있습니다. 차이는 **배경 유무**입니다.

| Theme | 배경 |
| --- | --- |
| `Light` | `Color/Gray_White` |
| `Dark` | **없음** (뒤 콘텐츠가 비침) |

사진·영상 위에 올리는 투명 헤더용입니다. 아이콘 색은 `Header / Icon`의 `Theme`가 담당합니다.

### 제목

제목 텍스트는 **7개 variant 모두 `t1400_20_regular`** 로 통일되어 있습니다.

> 2026-10-08까지 6개 variant가 외부 라이브러리의 `syrup_typo/syrup_typo_t1400`(line-height 22)을 쓰고 있었고, 로컬 `t1400_20_regular`(line-height 24)로 교체했습니다. 자세한 내역은 [syrup-design-tokens.md](syrup-design-tokens.md)를 참고하세요.

---

## 2. Child Items — Right Area

헤더 오른쪽에 붙는 부가 요소입니다.

### .primitive / Header / Tailing Acc

**Node** `8537:37273` · Component Set · **2 variants**

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `Alert` | VARIANT | `True` | `False` · `True` |
| `Bubble` | BOOLEAN | `true` | — |

| Variant | 크기 | 구성 |
| --- | --- | --- |
| `Alert=True` | 77 × 18 | `Button / Alert` ▸ `Alert=True` |
| `Alert=False` | 65 × 18 | **`Bubble`** + `Button / Alert` ▸ `Alert=False` |

[Button 페이지](syrup-button-components.md)의 `Button / Alert`를 그대로 감싼 래퍼입니다. "알림받는중"(77px) / "알림받기"(65px) 두 상태입니다.

> **`Alert=False`에만 `Bubble`이 들어 있습니다.** 알림 설정 전 참여를 유도하는 안내입니다. Header의 Alarm은 기능 노출, 하위 Alert는 설정 여부이므로 구분합니다. Alert=True에는 Bubble 레이어가 없어 Bubble을 켜도 표시되지 않습니다.

### .primitive / Header / Timer

**Node** `8535:33341` · Component Set · **2 variants** · 32 × 32

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `Complete` | VARIANT | **`False`** | `True` · `False` |

| Variant | 배경 | 텍스트 | 부가 |
| --- | --- | --- | --- |
| `Complete=False` | 없음 | `10` | `Bubble` |
| `Complete=True` | **`Color/Third_Pastel_Coral`** | `10금` | — |

원형(라운드 100)이며, 스크롤 적립 타이머를 표시합니다. 진행 중에는 남은 초를, 완료되면 받을 금액을 보여줍니다.

텍스트는 둘 다 **12px Bold로 스타일 미적용**입니다 (2026-11-06 재확인). 숫자·금액은 예시이며 실제 조건에 맞게 수정합니다. Usage E의 완료 금액은 5금입니다.

---

## 3. Icon

### Header / Icon

**Node** `8533:27224` · Component Set · **5 variants**

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `Property 1` | VARIANT | `Back` | `Back` · `Close` · `Plus` |
| `Theme` | VARIANT | `Light` | `Light` · `Dark` |

실제 프로퍼티명은 아직 `Property 1`입니다. 자동화에서 `Type`으로 호출하지 않습니다.

3 × 2 = 6조합 중 **5개**만 존재합니다. `Plus`는 `Light`만 있습니다.

| Variant | 크기 | 배경 | 아이콘 | 획 두께 |
| --- | --- | --- | --- | --- |
| `Back` · `Light` | 36 × 36 | 없음 (흰 fill 숨김) | `<` 화살표 — stroke **`Color/Gray_100`** | 1.8 |
| `Back` · `Dark` | 36 × 36 | 없음 (흰 fill 숨김) | `<` 화살표 — stroke **`Color/Gray_White`** | 1.8 |
| `Close` · `Light` | 36 × 36 | 없음 | `×` — fill `Color/Gray_100` | 1.8 |
| `Close` · `Dark` | 36 × 36 | 없음 | `×` — fill `Color/Gray_White` | 1.8 |
| `Plus` · `Light` | 32 × 32 | `Color/Gray_White` + `Color/Gray_850` 1px 테두리 | `+` — `Color/Primary_Orange` | 0.67 |

아이콘은 **획 1.8px**로 그려집니다(`Plus`만 0.67).

> 2026-11-06 확인 결과 Back 두 variant의 흰 fill은 모두 `visible=false`입니다. 이전 문서의 흰 사각형 배경 문제는 현재 상태와 달라 제거했습니다.

`Plus`는 다른 둘과 성격이 다릅니다 — 원형 테두리가 있는 버튼형이고 크기도 32입니다. `Todo` 헤더의 "+" 버튼용입니다.

---

## 설계 규칙 요약

| 항목 | 값 |
| --- | --- |
| 헤더 높이 | **55** (`Todo`만 57) |
| 헤더 폭 | 360 (화면 전체) |
| 상하 패딩 | **9.5** (토큰 밖) |
| 좌 패딩 | `Back` 8 · `Close` · `Todo` 16 |
| 우 패딩 | `Back` 16~20 · `Close` 12 · `Todo` 16 |
| 배경 | `Color/Gray_White` (`Theme=Dark`는 없음) |
| 제목 | `t1400_20_regular` (20 / 24 / −0.8) |
| 아이콘 | 36 × 36 (`Plus` 32), 획 1.8 |
| 아이콘 색 | `Light` `Color/Gray_100` · `Dark` `Color/Gray_White` |

---

## Usage

| 항목 | 값 |
| --- | --- |
| 섹션 | [Usage `11546:690`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11546-690) · 2960×458 |
| 구성 | 7패턴 · Header 인스턴스 9개 · 폭 360 |
| 템플릿 | Usage `11237:46733` · ❖System Components |

전체 화면 캡처가 아니라 실제 Header 인스턴스를 사용합니다. Header와 설명에 필요한 Bubble만 남겼습니다. 설명 영역과 슬롯 간격은 50이며, 설명 영역은 가장 긴 글줄 기준으로 정렬합니다.

| 예제 | Node | 설명 | 주요 설정 | 높이 |
| --- | --- | --- | --- | --- |
| A. 뒤로가기 | `11546:691` | 이전 화면으로 돌아갈 때 사용해요. 신규 화면에서는 뒤로가기 버튼 옆에 페이지 타이틀을 표시하지 않아요. | Back · Title=false | 55 |
| B. 닫기 | `11546:767` | 현재 화면이나 흐름을 닫을 때 사용해요. 이전 화면으로 돌아가는 동작과 구분해 닫기 버튼을 사용해요. | Close · Light · Title=false | 55 |
| C. 알림 설정 | `11546:845` | 업데이트나 적립 소식을 받을 수 있는 화면에 사용해요. 알림 설정 상태에 맞춰 문구와 아이콘을 표시해요. | Back · Alarm=True · Title=false · Alert 전/후 | 각각 55 |
| D. 적립 문의 | `11546:958` | 적립 관련 문의가 필요한 화면에서 사용해요. 뒤로가기 버튼과 오른쪽 적립문의 동작을 함께 제공해요. | Back · Inquiry=True · Title=false | 55 |
| E. 시간·적립 상태 | `11546:1035` | 정해진 시간 동안 콘텐츠를 확인하는 화면에 사용해요. 진행 중에는 남은 시간을, 완료 후에는 적립 결과를 보여줘요. | Back · Timer=True · Complete 전/후 | 각각 55 |
| F. 할 일 | `11546:1124` | 할 일 영역의 진입과 추가 동작에 사용해요. 영역명과 펼침 상태를 보여주고 오른쪽에 추가 버튼을 배치해요. | Todo · Title=true | 57 |
| G. 타이틀 표시 · 레거시 | `11546:1212` | 기존 화면에는 뒤로가기 버튼 옆에 타이틀이 남아 있어요. 레거시 사례이며, 신규 화면에는 타이틀 없는 구성을 사용해요. | Back · Title=true | 55 |

E는 Title=true이지만 페이지 타이틀 대신 Timer를 사용한 구성입니다. 신규 Back의 타이틀 숨김 기준을 기계적으로 적용해 기능 안내까지 제거하지 않습니다. C는 알림 기능 자체의 노출과 알림 설정 상태를 별도로 지정합니다.

---

## Guidelines

[Guidelines `11546:689`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11546-689) · 960×1084 · 3항목

각 항목은 Guidelines 템플릿 `11237:44468`의 좌우 슬롯으로 구성합니다. 모두 기본/레거시, 동작, 상태를 비교하는 사례이며 Do / Don’t 형식은 아닙니다.

### 1. 뒤로가기 옆 타이틀은 기본으로 표시하지 않아요

**Node** `11546:1299`

신규 화면에서는 Title=False로 설정해 뒤로가기 버튼 옆에 페이지 타이틀을 표시하지 않아요.
타이틀이 있는 기존 화면은 레거시 사례로 구분해요. 할 일의 영역명과 알림·타이머의 안내 문구에는 이 기준을 적용하지 않아요.

| 왼쪽 | 오른쪽 |
| --- | --- |
| 기본 · 타이틀 없음 | 레거시 · 타이틀 표시 |
| Back · Title=false | Back · Title=true |

레거시가 현재 존재한다는 설명이며 신규 화면에서 두 방식을 동등하게 선택하라는 의미는 아닙니다.

### 2. 이동과 종료에 맞는 버튼을 사용해요

**Node** `11546:1412`

이전 화면으로 돌아갈 때는 Back, 현재 화면이나 흐름을 닫을 때는 Close를 사용해요.
아이콘 모양만 바꾸지 않고 실제 동작에 맞는 유형을 선택해요.

| 왼쪽 | 오른쪽 |
| --- | --- |
| Back · 이전 화면 | Close · 화면 닫기 |

### 3. 부가 기능은 실제 상태에 맞게 표시해요

**Node** `11546:1527`

알림은 설정 여부에 따라 표시하고, 타이머는 진행 중과 완료 후의 상태를 구분해요.
페이지 타이틀을 숨겨도 기능에 필요한 안내 문구와 상태 정보는 유지해요.

| 왼쪽 | 오른쪽 |
| --- | --- |
| 알림 · 설정 전과 후 | 타이머 · 진행과 완료 |
| Tailing Acc · Alert=False / True | Timer · Complete=False / True |

---

## AI 도구 적용 기준

1. 기존 Header 인스턴스와 지원 variant를 재사용합니다. 아이콘과 텍스트를 따로 그려 Header를 재구성하지 않습니다.
2. 신규 Back 화면은 `Title#8533:0=false`를 명시합니다. 마스터 기본값 true나 레거시 G를 신규 기본값으로 해석하지 않습니다.
3. Todo 영역명과 기능 안내는 페이지 타이틀과 구분해 유지합니다. 타이머 숫자·금액·Bubble 문구는 실제 조건에 맞게 변경합니다.
4. Alarm·Timer·Inquiry는 서로 배타적이며 Back에서만 지원됩니다. Back · Dark 등 없는 조합을 임의로 생성하지 않습니다.
5. 높이는 일반 Header 55, Todo 57로 검증합니다. 세로 Fill로 늘리지 않고 현재 Fixed/Hug와 내부 요소 설정을 유지합니다. 가로 Fill은 화면 폭을 따르는 설정으로 세로 Fill과 구분합니다.
6. Alarm은 기능 노출, Alert는 알림 설정 상태입니다. Timer는 기능 노출, Complete는 진행·완료 상태입니다. 각각 하위 상태까지 설정합니다.
7. 실제 속성 키를 사용합니다: `Title#8533:0`, `NumberIcon#8541:19`, `Bubble#8537:16`. Header Icon의 속성명은 아직 `Property 1`입니다.
8. VARIANT의 True/False는 문자열이며 BOOLEAN의 true/false와 구분합니다. 기본값만으로 신규 화면의 의도된 상태가 완성된다고 가정하지 않습니다.
9. 이 문서의 최신 확인 범위는 디자인 시스템 Header 페이지입니다. 제품 파일 전체를 조사한 사용 건수나 동작 명세로 해석하지 않습니다.

---

## 현재 확인 사항

2026-11-06 Figma 페이지와 문서 예제를 확인했습니다. 이 업데이트는 MD 문서에 한정하며 Figma 마스터·토큰·속성명을 변경하지 않았습니다.

| 항목 | 확인 결과 |
| --- | --- |
| 높이 | 마스터 7종과 문서 Header 인스턴스 17개 모두 일반 55 / Todo 57 |
| 세로 설정 | 마스터 Back 기본·Alarm·Inquiry는 Fixed, Timer·Close·Todo는 Hug. 문서 일부 인스턴스도 Hug로 정리됨 |
| Title | 마스터 기본값 true · 신규 Back 권장 false |
| Timer | Complete 기본값 False (이전 문서의 True 수정) |
| Back 아이콘 배경 | Light/Dark 모두 흰 fill의 visible=false (이전 배경 문제 설명 제거) |
| Icon 속성명 | Property 1 유지 · 이름 변경 전에는 이 키로 호출 |
| 타이머 텍스트 | 마스터 숫자·금액 2개는 12px Bold이며 textStyleId 없음 |
| 숨겨진 Plus 도형 | 8541:45997 · visible=false · 이번 작업에서 삭제하지 않음 |

이전 2026-10-12 문서의 전체 노드 수, 미바인딩 토큰 건수, 제품 사용 추정과 정리 우선순위는 현재 현황으로 재검증되지 않아 제외했습니다. 구성 표의 과거 인스턴스 집계는 집계일을 따로 표시했습니다.

7개만 제공하는 variant 구조는 현재 지원 범위이며, 이론적 조합이 비어 있다는 이유만으로 추가 생성하지 않습니다. 패딩 9.5는 현재 높이 55를 만드는 규격이므로 별도 디자인 결정 없이 자동 보정하지 않습니다.
