# Syrup Design System — AD (광고) 컴포넌트

| 항목 | 값 |
| --- | --- |
| Figma File | [Syrup_Design-System](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System) |
| Page / Section | `AD` 페이지 → [AD 섹션 `10403:6794`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=10403-6794) |
| 섹션 구성 | `AD` 1440×5719 → `Guidelines` 960×904 → `Usage` 3360×816 (가로 일렬) |
| 기준일 | 2026-11-18 (기본 인스턴스 기반 MD 테스트 · 원본 디자인 변경 없음) |
| 관련 문서 | [syrup-design-tokens.md](syrup-design-tokens.md) — 디자인 토큰<br>[syrup-dialog-components.md](syrup-dialog-components.md) — Dialog 컴포넌트<br>[syrup-alert-components.md](syrup-alert-components.md) — Alert 컴포넌트<br>[syrup-badge-components.md](syrup-badge-components.md) — Badge 컴포넌트<br>[syrup-banner-components.md](syrup-banner-components.md) — Banner 컴포넌트<br>[syrup-border-components.md](syrup-border-components.md) — Border 컴포넌트<br>[syrup-bottom-info-components.md](syrup-bottom-info-components.md) — Bottom Info 컴포넌트<br>[syrup-bottom-cta-components.md](syrup-bottom-cta-components.md) — Bottom CTA 컴포넌트<br>[syrup-bottom-sheet-components.md](syrup-bottom-sheet-components.md) — Bottom Sheet 컴포넌트<br>[syrup-bubble-components.md](syrup-bubble-components.md) — Bubble 컴포넌트<br>[syrup-button-components.md](syrup-button-components.md) — Button 컴포넌트<br>[syrup-checkbox-components.md](syrup-checkbox-components.md) — Checkbox 컴포넌트<br>[syrup-chip-components.md](syrup-chip-components.md) — Chip 컴포넌트<br>[syrup-card-components.md](syrup-card-components.md) — Card 컴포넌트<br>[syrup-dim-components.md](syrup-dim-components.md) — Dim 컴포넌트<br>[syrup-grid-list-components.md](syrup-grid-list-components.md) — Grid List 컴포넌트<br>[syrup-grid-scroll-components.md](syrup-grid-scroll-components.md) — Grid Scroll 컴포넌트<br>[syrup-header-components.md](syrup-header-components.md) — Header 컴포넌트<br>[syrup-icon-button-components.md](syrup-icon-button-components.md) — Icon Button 컴포넌트<br>[syrup-indicator-components.md](syrup-indicator-components.md) — Indicator 컴포넌트<br>[syrup-keypad-components.md](syrup-keypad-components.md) — Keypad 컴포넌트<br>[syrup-label-components.md](syrup-label-components.md) — Label 컴포넌트<br>[syrup-list-footer-components.md](syrup-list-footer-components.md) — List Footer 컴포넌트<br>[syrup-list-header-components.md](syrup-list-header-components.md) — List Header 컴포넌트<br>[syrup-list-row-components.md](syrup-list-row-components.md) — List Row 컴포넌트<br>[syrup-loader-components.md](syrup-loader-components.md) — Loader 컴포넌트<br>[syrup-lottie-components.md](syrup-lottie-components.md) — Lottie 컴포넌트<br>[syrup-product-grid-components.md](syrup-product-grid-components.md) — Product Grid 컴포넌트<br>[syrup-product-list-components.md](syrup-product-list-components.md) — Product List 컴포넌트<br>[syrup-product-scroll-components.md](syrup-product-scroll-components.md) — Product Scroll 컴포넌트<br>[syrup-progress-stepper-components.md](syrup-progress-stepper-components.md) — Progress Stepper 컴포넌트<br>[syrup-result-components.md](syrup-result-components.md) — Result 컴포넌트<br>[syrup-search-field-components.md](syrup-search-field-components.md) — Search Field 컴포넌트<br>[syrup-stepper-components.md](syrup-stepper-components.md) — Stepper 컴포넌트<br>[syrup-swipe-components.md](syrup-swipe-components.md) — Swipe 컴포넌트<br>[syrup-switch-components.md](syrup-switch-components.md) — Switch 컴포넌트<br>[syrup-tab-components.md](syrup-tab-components.md) — Tab 컴포넌트<br>[syrup-tab-bar-components.md](syrup-tab-bar-components.md) — Tab Bar 컴포넌트<br>[syrup-text-button-components.md](syrup-text-button-components.md) — Text Button 컴포넌트<br>[syrup-text-field-components.md](syrup-text-field-components.md) — Text Field 컴포넌트<br>[syrup-ticker-components.md](syrup-ticker-components.md) — Ticker 컴포넌트<br>[syrup-toast-components.md](syrup-toast-components.md) — Toast 컴포넌트 |

> **광고 정보를 노출하는 영역이에요.**
> 사용자에게 광고, 프로모션, 이벤트 콘텐츠를 전달할 때 사용해요.

---

## 목차

1. [컴포넌트 한눈에 보기](#컴포넌트-한눈에-보기)
2. [DA](#1-da)
3. [ETMS](#2-etms)
4. [P.AD](#3-pad)
5. [P.AD NW](#4-pad-nw)
6. [Naver 피드](#5-naver-피드)
7. [Naver DA](#6-naver-da)
8. [금주머니](#7-금주머니)
9. [공통 요소](#공통-요소)
10. [Usage](#usage)
11. [Guidelines](#guidelines)
12. [반응형에서 별도로 설정할 부분](#반응형에서-별도로-설정할-부분)
13. [2026-11-18 검토 결과](#2026-11-18-검토-결과)
14. [과거 점검 이력](#과거-점검-이력)

---

## 컴포넌트 한눈에 보기

| # | 이름 | 타입 | Variant 축 | 크기 | 특징 |
| --- | --- | --- | --- | --- | --- |
| 1 | `DA` | Component Set | `Type` 4종 | 360×210 / 187 / 100 / 80 | 인피드 디스플레이 배너 |
| 2 | `ETMS` | Component Set | `Type` 5종 | 300×330 / 320×67 / 142×140 / 108×108 | 팝업 + 뉴스형 + 플로팅 |
| 3 | `P_AD` | Component Set | `Type` 2종 | 320×234 / 256×181 | 카드형 광고 |
| 4 | `P.ad NW` | Component | — (슬롯) | 360×254 | 타이틀·CTA 포함 풀 배너 |
| 5 | `Naver_AD` | Component Set | `Corner` 2종 | 360×338 | 네이버 피드 광고 |
| 6 | `Naver DA` | Component | — | 360×256 | 네이버 DA + CTA |
| 7 | `pocket` | Component Set | `Active` 2종 | 88×85 | 금주머니 플로팅 |

섹션 헤더 명칭은 각각 **DA · ETMS · P.AD · P.AD NW · Naver 피드 · Naver DA · 금주머니** 입니다.

---

## 1. DA

인피드 디스플레이 배너. 높이 스펙별로 variant가 나뉩니다.

**Node** `8591:4265` · Component Set

### Properties

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `Type` | VARIANT | `Top` | `Top` · `H185` · `H100` · `H80` |
| `Image` | BOOLEAN | `false` | — |
| `Description` | BOOLEAN | `true` | — |

### Variants

| Variant | 크기 | 구성 | 이미지 리사이즈 규칙 |
| --- | --- | --- | --- |
| `Type=Top` | 360×210 | Image, **Badge**, **Indicator** | 1.71:1 비율로 리사이즈 |
| `Type=H185` | 360×187 | Image | H185 리사이즈 |
| `Type=H100` | 360×100 | Image | H100 리사이즈 |
| `Type=H80` | 360×80 | Image | H80 리사이즈 |

- 레이아웃은 전부 **VERTICAL 오토레이아웃**, corner radius `0`.
- **Badge와 Indicator는 `Type=Top`에만 존재합니다.** 나머지 3종은 이미지 영역 단독 구성입니다.
- `Type=Top`의 이미지 영역만 `FRAME`이고, H185 / H100 / H80은 `RECTANGLE`입니다.

---

## 2. ETMS

팝업·뉴스형 광고와 플로팅 오브젝트(금·두더지·알)를 묶은 5종 세트입니다.

**Node** `8590:9391` · Component Set

### Properties

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `Type` | VARIANT | `Popup` | `Popup` · `News` · `Gold` · `Mole` · `Egg` |
| `Title` | BOOLEAN | `true` | — |

### Variants

| Variant | 크기 | Radius | 구성 |
| --- | --- | --- | --- |
| `Type=Popup` | 300×330 | `Corner radius/400` (16) | 이미지 영역 + Title 영역 |
| `Type=News` | 320×67 | 원본 유지 | 이미지 + 광고 안내·타이틀 + 뱃지 |
| `Type=Gold` | 142×140 | 0 | 오브젝트 + 닫기 버튼 |
| `Type=Mole` | 142×140 | 0 | 오브젝트 + 닫기 버튼 |
| `Type=Egg` | 108×108 | 0 | 오브젝트 (`syrup_img_egg`) |

### `Type=Popup` 상세

| 영역 | 크기 | 배경 | Padding | Gap |
| --- | --- | --- | --- | --- |
| 루트 | 300×330 | `Color/Gray_White` | 0 | 0 |
| `image(1200x627)` | 300×250 | `Color/Gray_950` | — | — |
| `Title` | 300×80 | `Color/Gray_White` | `Spacing/400` (16) 전방향 | `Spacing/250` (10) |

- 이미지 자리표시자 문구: **"300X250 비율 리사이즈"** (`b200_16_regular` / `Color/Gray_400`)
- Title 영역 우측에 정보 아이콘 `syrup_img_ad_etms_info` 16×16
- `Gold` · `Mole`은 닫기 아이콘 `syrup_ico_40_floating_close_enabled_gray_400`을 공유합니다.

---

## 3. P.AD

카드형 광고. 이미지 + 텍스트 2단 구성입니다.

**Node** `8590:3536` · Component Set

### Properties

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `Type` | VARIANT | `Default` | `Default` · `Popup` |
| `Text` | BOOLEAN | `true` | — |

### Variants

| Variant | 크기 | Radius | 구성 |
| --- | --- | --- | --- |
| `Type=Default` | 320×234 | `radius/radius_300` ⚠️ | `image(1200x627)` + `Text` |
| `Type=Popup` | 256×181 | 12 | `image(1200x627)` + `Text` |

### `Type=Default` 상세

| 영역 | 크기 | 배경 | Padding (T/R/B/L) | Gap |
| --- | --- | --- | --- | --- |
| 루트 | 320×234 | `Color/Gray_White` | 0 | 0 |
| `image(1200x627)` | 320×166 | `Color/Gray_900` | — | — |
| `Text` | 320×68 | `Color/Gray_White` | 14 / `Spacing/1500`(60) / 14 / `Spacing/400`(16) | `Spacing/500` (20) |

- 이미지 자리표시자 문구: **"이미지 원본 비율 리사이즈"** (`b200_16_regular` / `Color/Gray_400`)
- ⚠️ `Text` 영역의 **top·bottom 패딩 14는 토큰에 바인딩되지 않은 임의 값**입니다. Spacing 스케일에 14가 없습니다. (우측 60은 `Spacing/1500`으로 바인딩 완료)

---

## 4. P.AD NW

타이틀·설명·CTA를 모두 갖춘 풀 배너입니다.

**Node** `9725:33458` · Component (단일)

### Properties

| Property | Type | 비고 |
| --- | --- | --- |
| `Image` | SLOT | 이미지 영역을 슬롯으로 교체 |

### 컴포넌트 설명 (Figma description)

> 해상도 대응: 미디어는 w 400 까지 비율유지 축소/확대
> w 400 초과 시 높이값 고정, 미디어 영역 좌우로 여백 추가

### 구조

| 영역 | 크기 | 배경 | Padding (T/R/B/L) | Gap |
| --- | --- | --- | --- | --- |
| 루트 | 360×254 | `color/black/black800` ⚠️ | 0 | 0 |
| `Image` (슬롯) | 360×188 | `Color/Gray_950` | — | — |
| `Title` | 360×30 | `color/white` ⚠️ | `Spacing/300`(12) / `Spacing/400`(16) / 0 / `Spacing/400`(16) | `Spacing/100` (4) |
| `pad_Atype_cta` | 360×36 | `Color/Gray_White` | 0 / `Spacing/400`(16) / `Spacing/200`(8) / `Spacing/400`(16) | 2 |

### 텍스트 슬롯

| 레이어 | 제한 | 스타일 | 색상 | 샘플 |
| --- | --- | --- | --- | --- |
| `Title(16자 이내)` | 16자 | `b500_13_regular` | `Color/Gray_400` | "desc 20자 한" |
| `Description(50자 이내)` | 50자 | `t1350_14_medium` | `Color/Gray_100` | "추천 광고" |
| CTA `Title(10자 이내)` | 10자 | `b500_13_regular` | `Color/Gray_200` | "다른 광고 보러 가기" |

- ✅ `Description`은 스타일 미적용 Pretendard Medium 14 / line-height **20** 이었습니다. 2026-09-21에 신설된 **`t1350_14_medium`**(14 / 18 / −0.5)을 적용해 **line-height가 20 → 18, letter-spacing이 0 → −0.5로 조정**되었습니다.
- ✅ `Badge`의 `3금` 텍스트도 스타일 미적용 Pretendard Bold 13이었습니다. 신설된 **`t1060_13_bold`**(13 / 18 / 0)를 적용했고 값이 동일해 변화는 없습니다. Alert의 `Title` 레이어와 같은 조합입니다.

- 이미지 영역 자리표시자: **"P.AD NW 광고 / 1.91:1 비율 리사이즈 / 1200X627"**
- 이미지 위에 `Badge` 64×30, `Indicator` 120×37, `pagination / dot / solid` 40×8이 얹힙니다.
- CTA 끝에 `Icon / Arrow` 12×12.

---

## 5. Naver 피드

**Node** `8595:15613` · Component Set

### Properties

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `Corner` | VARIANT | `False` | `False` · `True` |

### Variants

| Variant | 크기 | Radius |
| --- | --- | --- |
| `Corner=False` | 360×338 | 0 |
| `Corner=True` | 360×338 | 16 |

- 두 variant 모두 내부는 자리표시자 텍스트 하나뿐입니다: **"네이버 피드 광고 / 약 1.065:1 비율 유지 / (원본 이미지 360×338)"**
- 실제 소재는 네이버에서 내려오므로 컴포넌트는 영역·모서리 처리만 정의합니다.
- 현재 속성명은 **`Corner`**입니다. 과거 `Coner` 표기는 사용하지 않습니다.

---

## 6. Naver DA

**Node** `9734:46882` · Component (단일)

### 컴포넌트 설명 (Figma description)

> 해상도 대응: 미디어는 w 400 까지 비율유지 축소/확대
> w 400 초과 시 높이값 고정, 미디어 영역 좌우로 여백 추가

### 구조

| 영역 | 크기 | 배경 | Padding (T/R/B/L) | Gap |
| --- | --- | --- | --- | --- |
| 루트 | 360×256 | `color/black/black800` ⚠️ | 0 | 0 |
| `media` | 360×210 | `Color/Gray_950` | — | — |
| `pad_Atype_cta` | 360×46 | `Color/Gray_White` | 0 / `Spacing/400`(16) / 0 / `Spacing/400`(16) | `Spacing/50` (2) |

- 미디어 자리표시자: **"네이버 DA 광고 / 약 1.71:1 비율 / 기준 영역 360×210"** (`b200_16_regular` / `Color/Gray_400`)
- CTA 문구 **"더보기"** (`b500_13_regular` / `Color/Gray_200`) + Arrow 아이콘 12×12
- P.AD NW와 CTA 영역(`pad_Atype_cta`)을 공유하지만 **높이가 다릅니다** (46 vs 36).

---

## 7. 금주머니

적립 유도용 플로팅 오브젝트입니다.

**Node** `8914:66527` · Component Set

### Properties

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `Active` | VARIANT | `On` | `On` · `Off` |
| `Bubble` | BOOLEAN | `true` | — |

### 구조 (`Active=On`)

| 영역 | 크기 | 배경 | Radius | Padding (T/R/B/L) |
| --- | --- | --- | --- | --- |
| 루트 | 88×85 | — | — | `Spacing/200`(8) / `Spacing/400`(16) / `Spacing/200`(8) / `Spacing/400`(16) |
| 주머니 오브젝트 | 56×56 | — | `Corner radius/circle` | — |
| `timer` | 42×20 | `Color/Primary_Orange` | — | 2 / 6 / 2 / 6 |
| `Bubble` → `Text` | 74×28 | `Color/Gray_200` | `Corner radius/250` (10) | 6 / 10 / 6 / 10 |

- 오브젝트 안에 잔여 횟수 텍스트 (예: "5금"), `timer` 안에 **"받기"** 라벨.
- `Bubble`에는 말풍선 꼬리 `Tail` 6×3이 붙습니다.
- `Active=Off`는 `Bubble`이 제거된 구성입니다.
- ⚠️ 루트의 `itemSpacing`이 **`-7`(음수)** 입니다. 주머니와 timer를 겹치기 위한 의도로 보이나 토큰화할 수 없는 값입니다.

---

## 공통 요소

여러 광고 컴포넌트가 공유하는 하위 요소입니다.

### Badge

`DA(Top)` · `ETMS(Popup)` · `P.AD` · `P.AD NW`에서 동일 스펙으로 사용됩니다.

| 속성 | 값 |
| --- | --- |
| 크기 | 64×30 |
| 배경 | `Color/Primary_Orange` (#FF6315) |
| Radius | `Corner radius/500` (20) |
| Padding | `2` / `Spacing/250`(10) / `2` / `Spacing/250`(10) |
| Gap | `Spacing/100` (4) |
| 텍스트 색 | `Color/Gray_White` |
| 샘플 | "3금" |
| 구성 | `Badge / Icon` 20×20 + 텍스트 |

### pagination / dot / solid

| 속성 | 값 |
| --- | --- |
| 크기 | 40×8 (gap 4) |
| active dot | 16×4 |
| inactive dot | 4×4 |
| Radius | `radius/radiusmax` ⚠️ |

### pad_Atype_cta

하단 CTA 행. `P.AD NW`(36px)와 `Naver DA`(46px)가 공유합니다.

| 구성 | 값 |
| --- | --- |
| 배경 | `Color/Gray_White` |
| 좌우 Padding | `Spacing/400` (16) |
| 텍스트 | `b500_13_regular` / `Color/Gray_200` / 10자 이내 |
| 아이콘 | `Icon / Arrow` 12×12 |

### 이미지 자리표시자 규칙

모든 광고 컴포넌트의 이미지 영역은 동일한 패턴을 따릅니다.

| 속성 | 값 |
| --- | --- |
| 배경 | `Color/Gray_950` (#F6F6F7) 또는 `Color/Gray_900` (#F2F2F2) |
| 안내 문구 스타일 | `b200_16_regular` |
| 안내 문구 색 | `Color/Gray_400` (#777777) |
| 문구 형식 | `{광고명} / {비율} 비율 리사이즈 / {원본 해상도}` |

**소재 규격 정리**

| 컴포넌트 | 비율 | 원본 해상도 |
| --- | --- | --- |
| DA (Top) | 1.71 : 1 | — |
| ETMS (Popup) | — | 300 × 250 |
| P.AD | 원본 비율 유지 | 1200 × 627 |
| P.AD NW | 1.91 : 1 | 1200 × 627 |
| Naver 피드 | 360:338 (약 1.065:1) | 360 × 338 |
| Naver DA | 360:210 (약 1.71:1) | 360 × 210 |

---

## 반응형에서 별도로 설정할 부분

**컴포넌트 설명은 사용 의도이며, 폭만 바꾸면 모든 조건이 자동으로 적용된다는 뜻은 아닙니다.** 아래 설정은 사용하는 인스턴스와 지면 래퍼에서 처리하며 원본 마스터를 수정하거나 인스턴스를 분리하지 않습니다.

### H80과 네이버 피드

- H80: 가용 폭을 w라 할 때 루트 폭 w, 높이 w/4.5를 함께 지정합니다. 320폭에서는 71.11px입니다. 폭만 줄여 높이80을 유지하지 않습니다. 이미지 표시 시 소재의 CROP·제약 조건도 확인합니다.
- Naver_AD: Corner=True/False를 먼저 선택하고 폭 w, 높이 w×338/360을 함께 지정합니다. 라운드형의360폭 화면은 좌우20이므로 가용 폭320·높이300.44입니다. 원본의16px 라운드와 텍스트·뱃지 크기는 유지하며 전체를 비례 확대하는 Scale 도구로 대체하지 않습니다.

### P.ad NW · Naver DA의 폭400 상한

현재 기본 인스턴스는 폭을 넓히면 미디어도 비례 확대됩니다. NW는400폭에서Image208.89·전체274.89, 440폭에서는Image229.78·전체295.78입니다. Naver DA는440폭에서media256.67·전체302.67입니다. **400초과 높이 고정과 좌우 여백은 자동 적용되지 않습니다.**

설명의 ‘400까지 비례 확대, 이후 높이 고정’을 적용하려면 아래처럼 별도 설정합니다. 수치는400폭에서 확장을 멈추는 기준으로 계산한 적용식이며, 현재 원본의 자동 동작으로 간주하지 않습니다.

1. 지면 폭 w에 루트 가로를 맞추고 세로는 Hug로 둡니다. 하위 Title·CTA의 자체 높이·패딩·타이포는 유지합니다.
2. NW의Image 슬롯 또는 Naver DA의media 프레임은 가로 Fill을 유지하고, 세로를 Fixed로 지정합니다. 높이는 각각 min(w,400)×188/360 또는 min(w,400)×210/360입니다. 비율 연결로440폭의 높이가 다시 계산되지 않도록 해제·재확인합니다.
3. 내부 실제 소재는 폭 min(w,400)로 가운데 정렬합니다. w가400을 넘으면 좌우 여백은 각각(w−400)/2입니다. 미디어 바깥 프레임은 지면 폭을 채우되 실제 소재를 전체 폭으로 늘리지 않습니다. 슬롯은 허용된 콘텐츠로 교체하고, media 내부는 사용 가능한 인스턴스 오버라이드나 지면 래퍼로 구성합니다. 내부 제어가 불가능하면 부모 폭만 변경한 상태를 완료로 처리하지 않습니다.
4. 예: 지면440에서는 실제 소재 폭400·좌우20. NW 미디어 높이208.89, Title30+CTA36을 포함한 전체274.89. Naver DA 미디어233.33+CTA46으로 전체279.33입니다. 제품 코드에서도 같은 상한·가운데 정렬을 따로 구현해야 합니다.
5. 안내용 자리표시자·텍스트·뱃지·CTA를 미디어와 함께 확대하지 않습니다. 수치 지정 후 슬롯·소재·클립·돌출 뱃지와 실제 소재의 광고 규격을 확인합니다. NW의1200×627 소재와 Naver DA의360×210 기준 영역은 서로 다른 비율이므로 혼용하지 않습니다.

### 지면 위치와 플로팅

- 화면 하단 고정은 지면 래퍼의 하단 제약 또는 제품 코드에서 설정합니다. Usage A의 위55 빈칸은 문서 표현용이며 실제 화면의 고정 상단 여백이 아닙니다.
- Header55 바로 아래 H80을 놓습니다. ETMS는 루트 하단과 배너 상단 사이20, pocket은 루트 하단과 배너 상단 사이0으로 맞춥니다. pocket 내부 패딩과 버블 돌출은 별개이며 시각 오브젝트 사이 여백을 임의로0으로 만들지 않습니다.
- ETMS에 배너가 없으면 화면 하단에서20을 둡니다. 지면 폭·배너 높이가 바뀌면 좌표를 다시 계산하고 화면·스크롤 래퍼의Clip이 버블을 자르지 않는지 확인합니다. 현재 고정·하단 고정 설정은 마스터가 자동으로 결정하지 않습니다.

---

## Usage

| 항목 | 값 |
| --- | --- |
| 섹션 | [`Usage` `11261:2202`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11261-2202) · 3360 × 816 |
| 구성 | 8패턴 · 폭 360 · 높이는 내용에 맞춰 251~600 |
| 템플릿 | `Usage` 컴포넌트 [`11237:46733`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11237-46733) (`❖System Components` 페이지) |

> **컷은 화면 캡처가 아니라 실제 컴포넌트 인스턴스입니다.**
> 해당 컴포넌트와 **꼭 필요한 맥락 요소만** 남기고 나머지 화면 요소는 모두 지웠습니다. 남은 요소도 잘라낸 그림이 아니라 마스터를 직접 참조하는 인스턴스라, 컴포넌트 디자인이 바뀌면 문서가 함께 바뀝니다 (2026-11-03).

패턴 하나가 `Usage` 템플릿 인스턴스 하나입니다. 템플릿은 `Title`(제목 + 설명)과 `Component` **슬롯**으로 이루어져 있고, 슬롯 안에 그 패턴을 보여 줄 인스턴스를 넣습니다. 세로 간격은 50입니다.

| | 패턴 | 설명 | 슬롯에 담은 것 | 슬롯 높이 |
| --- | --- | --- | --- | --- |
| **A** | 하단 고정 배너 | 화면 하단에 고정해 스크롤 중에도 광고를 보여줘요. H80 배너는 가용 폭에 맞춰 4.5:1 비율을 유지해요. | `DA / Type=H80` (위 **55** 비움) | 135 |
| **B** | 상단 배너 | 헤더 바로 아래에 배치해요. 화면 진입 시 먼저 보여줄 광고에 사용하며, 배너의 규격과 비율을 유지해요. | `Header` + `DA / Type=H80` | 135 |
| **C** | 인피드 배너 | 목록 흐름 중간에 배치해요. H185는 소재 높이 185에 상하 여백 1씩을 더해 전체 높이 187로 사용해요. | `DA / Type=H185` | 187 |
| **D** | 플로팅 오브젝트 | 화면 오른쪽 아래에 배치해요. 하단 배너가 없으면 화면 하단에서 20, 배너가 있으면 배너 상단에서 20 간격을 둬요. | `ETMS / Type=Gold` + `DA / Type=H80` | 240 |
| **E** | 금주머니 플로팅 | 적립을 유도하는 전용 플로팅이에요. 화면 오른쪽 아래에 고정하고, 하단 배너가 있으면 배너 바로 위에 배치해요. | `pocket / Active=On` + `DA / Type=H80` | 165 |
| **F** | 네이버 피드 · 라운드 | 좌우 여백은 20, 모서리는 라운드형을 사용해요. 원본 360×338 비율을 유지해 폭 320일 때 높이는 약 300.4로 맞춰요. | `Naver_AD / Corner=True` · **320 × 300.4** | 300.4 |
| **G** | 네이버 피드 · 전체 폭 | 좌우 여백 없이 화면 폭을 채워요. 모서리는 직각으로 두고 원본 360×338 비율을 유지해요. | `Naver_AD / Corner=False` · **360 × 338** | 338 |
| **H** | 카드형 광고 | 목록 안에 카드 형태로 배치해요. 주변 카드와 간격·모서리 규칙을 맞추고 광고 카드 컴포넌트를 사용해요. | `P_AD / Type=Default` × 2 · 320폭 · 간격 **16** | 484 |

### 맥락 요소를 함께 넣은 패턴

| | 함께 넣은 것 | 이유 |
| --- | --- | --- |
| **A** | 위쪽 **55** 빈 공간 | `DA / Type=H80`은 B와 같은 variant입니다. 위를 비워 **화면 하단에 붙는다**는 걸 보여 줍니다 |
| **B** | `Header` | 같은 이유로, 헤더를 둬 **헤더 바로 아래**라는 위치를 보여 줍니다 |
| **D · E** | `DA / Type=H80` | 설명 자체가 배너와의 **간격**입니다. 배너가 없으면 패턴이 성립하지 않아요 |
| **H** | `P_AD` 두 장 | 카드 **사이 간격 16**이 규칙이라 한 장으로는 보이지 않아요 |

나머지 셋(C · F · G)은 variant가 서로 달라 컴포넌트 하나로 구분됩니다.

**A · D · E의 슬롯에는 레이아웃용 빈 프레임이 하나 더 있습니다.** 빈 공간을 두거나 플로팅을 오른쪽 끝에 절대 좌표로 놓으려면 필요해서, 칠도 선도 없는 투명 프레임입니다.

---

## Guidelines

지켜지지 않으면 결과가 깨지는 것만 올렸습니다. 각 항목은 Figma **[`Guidelines` 섹션 `11169:22`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11169-22)** (960 × 904) 에 Do / Don't 한 쌍으로 들어 있습니다.

규칙 하나가 `Guidelines` 템플릿 인스턴스 [`11237:44468`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11237-44468) (`❖System Components` 페이지) 하나입니다. 폭 760, `Title`(제목 + 설명) 아래 `Image` 프레임에 `Do` · `Don't` **슬롯**이 좌우로 들어갑니다. Do / Don't 표시는 슬롯 이름이 대신합니다.

### 1. H80 배너는 가로세로 비율을 유지해요

H80 배너의 기준 크기는 `360 × 80`이에요. 가용 폭이 달라지면 `4.5 : 1` 비율로 높이도 함께 조정해요. 다른 광고 유형은 각 컴포넌트의 규격을 따라요.

| | 내용 |
| --- | --- |
| **Do** | `DA / Type=H80` 을 `360 × 80` 그대로 |
| **Don't** | 높이만 `120` 으로 늘려 안쪽 여백이 벌어짐 |

높이를 늘려도 이미지는 `CROP`이라 찌그러지지 않습니다. 대신 **배너 안쪽 여백만 벌어져** 비율 기준이 조용히 깨집니다.

### 2. 플로팅은 하단 배너와 겹치지 않게 배치해요

하단 배너가 있으면 배너 상단을 기준으로 플로팅을 배치해요. 플로팅 오브젝트는 배너와 **20** 간격을 두고, 금주머니는 배너 바로 위에 배치해요.

| | 배치 | 결과 |
| --- | --- | --- |
| **Do** | `ETMS` 아래에 **20** 띄우고 `DA / Type=H80` | 둘 다 온전히 보임 |
| **Don't** | `ETMS` 를 배너 위치까지 내림 | 배너가 플로팅을 **80** 가림 |

간격 기준이 둘로 갈립니다. **`ETMS`는 20**, **`pocket`은 0**(배너에 붙임)입니다. Usage **D · E**의 컷이 각각 그 간격 그대로입니다.

---

## 2026-11-18 검토 결과

- [AD MD 테스트 섹션](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=12215-257)에서 Usage 복사 없이 기본 인스턴스로 배치와 폭 변경을 검사했습니다. 원본 AD·Guidelines·Usage는 수정하지 않았습니다.
- 현재 참조 섹션은10403:6794입니다. Naver_AD의Corner와 ETMS News320×67을 반영했습니다.
- P_AD Default는320×234(이미지166+Text68), Popup은256×181.34입니다. P.ad NW는360×254(Image188+Title30+CTA36)입니다. H의카드2개+간격16=484는 현재 치수와 일치합니다. 이는 현재 기본 콘텐츠의 측정값이며 다른 문구·옵션에도 무조건 고정하는 지시가 아닙니다.
- P_AD Default의 현재 설명·타이틀은 각각 한 줄 말줄임(ENDING/maxLines=1)입니다. 긴 문구를 임의로 여러 줄로 늘려 카드 높이를 변경하지 않습니다.
- pocket Off는 원본에Sandoll Gyeokdonggulim Regular가 지정되어 있습니다. 실행 환경에 이 폰트가 없어 인스턴스 생성·시각 검증은 보류했고 원본 구조만 확인했습니다. 임의 폰트로 대체하거나 미검증 상태를 시각 검증 완료로 표기하지 않습니다.
- 아래 토큰 정리 건수·경고·해결 이력은 기재된 과거 날짜의 기록이며, 이번 점검에서 파일 전체를 재집계한 결과가 아닙니다. 현재 사용은 위 규격·속성·반응형 지침을 우선합니다.

---

## 과거 점검 이력


### 1. 타 라이브러리 토큰 혼용

AD 컴포넌트를 포함해 파일 전반에 Syrup `global`이 아닌 **다른 라이브러리의 토큰**이 섞여 있습니다. 이 파일의 로컬 베리어블 컬렉션은 `global` **하나뿐**입니다.

#### ✅ 해결 완료 (2026-09-21, 파일 전체 48개 페이지 기준 · 총 2,112건)

**1차 — radius max / black 계열 (532건)**

| 변경 전 | 실제 값 | 변경 후 | 건수 |
| --- | --- | --- | --- |
| `radius/radius_max` @base tokens | 100 | `Corner radius/circle` | 468 |
| `radius/radiusmax` @tokens | 100 | `Corner radius/circle` | 32 |
| `radius/radius_max` @Foundation | 100 | `Corner radius/circle` | 4 |
| `color/black/black800` @tokens | #F4F4F4 | `Color/Gray_900` (#F2F2F2) | 16 |
| `color/black/black500` @tokens | #C7C7C7 | `Color/Gray_700` (#D2D2D2) | 6 |
| `color/black/black300` @tokens | #868686 | `Color/Gray_400` (#777777) | 4 |
| `color/black/black200` @tokens | #626262 | `Color/Gray_300` (#666666) | 2 |

> ⚠️ **`color/black/black*`는 이름과 달리 블랙이 아니었습니다.** 타 디자인시스템의 회색 계조에 "black" 이름이 붙어 있던 것으로, Syrup Gray 스케일에 정확히 일치하는 값이 없어 **RGB 거리 기준 최근접 토큰**으로 매핑했습니다. 색이 최대 15/255(약 6%) 달라집니다.
>
> radius는 세 이름 변형 모두 값이 `100`으로 `Corner radius/circle`과 동일해 **시각적 변화가 없습니다.**

**2차 — 값이 정확히 일치하는 외부 토큰 전량 (1,580건)**

| 교체 후 Syrup 토큰 | 건수 | 교체된 외부 토큰 |
| --- | --- | --- |
| `Spacing/*` | 621 | `spacing/spacing_*` @base tokens |
| `Corner radius/*` | 455 | `radius/radius_100`~`_400` @base tokens · `radius250` · `radius050` @tokens · `Round/Medium` @(국내) Component |
| `Font family/pretendard` | 113 | `fontFamilies/pretendard` @semantic tokens |
| `Color/*` | 91 | `color/gray_*` · `primary_orange` · `secondary_red` · `third_pastel_coral` @base tokens |
| `Font weight/*` | 88 | `fontWeights/fontweight-400` · `-500` · `-700` @semantic tokens |
| `Letter spacing/*` | 76 | `letterSpacing/*` @semantic tokens |
| `Font size/*` | 69 | `fontSize/*` @semantic tokens |
| `Line height/*` | 67 | `lineHeights/*` @semantic tokens |

값이 동일한 건만 교체했으므로 **시각적 변화가 없습니다.** 인스턴스 내부 노드는 제외했습니다 — 원본 컴포넌트가 정리되었으므로 자동으로 상속됩니다.

> 💡 텍스트 노드의 타이포 바인딩은 **범위별 배열**로 저장됩니다. 단일 참조만 처리하면 조용히 누락되므로, 스크립트에서 `Array.isArray(boundVariables[field])` 분기가 필요합니다.

#### 남은 외부 참조 (인스턴스 외부 기준 2,365건)

| 항목 | 건수 | 필요한 조치 |
| --- | --- | --- |
| `paragraphSpacing/0` · `paragraphIndent/0` @semantic tokens | 1,900 | **Syrup `global`에 대응 토큰이 없음.** 로컬 텍스트 스타일 20개 전부가 참조 중. 값 `0`짜리 토큰 2개를 신규 생성해 스타일을 재연결하면 일괄 해소 (시각 변화 없음) |
| `Spec docs/margin` (236) · `Spec docs/width` (27) @docs | 263 | 문서 레이아웃 전용 토큰. 제품 UI 토큰과 분리해 두는 편이 맞다고 보고 **의도적으로 제외** |
| 원격 텍스트 스타일 사용 노드 37개 | ~140 | 변수가 아니라 **스타일** 문제. 대부분 해소되어 **현재 4건** 잔존 → **ℹ️ 의도된 예외** ([아래](#원격-텍스트-스타일--ℹ-의도된-예외-2026-10-08)) |
| 일치값 없는 색상 | ~11 | 아래 표 |

**일치값이 없어 자동 교체에서 제외된 색상**

| 외부 토큰 | 실제 값 | 건수 | 비고 |
| --- | --- | --- | --- |
| `border/thumbnail_border` @Brand and theme colors | #000000 **5%** | 4 | Syrup Opacity 스케일은 4%(`Opacity_Black_500`)와 8%(`Opacity_Black_450`)뿐 — 5%는 없음 |
| `Base/Grey/Grey 700` @Color | #4E5968 | 2 | 청록빛 회색 — Syrup Gray에 대응 없음 |
| `styles/scrim20` @OLB.DSL | #000000 20% | 2 | Syrup Opacity 스케일에 20% 없음 |
| `Semantic/Text/Subtle` @Color | #8B95A1 | 1 | 대응 없음 |
| `(구)color/blueblack/700` @(구)Foundation | #E8E8EA | 1 | 구버전 라이브러리. 이름과 달리 연회색. 최근접은 `Color/Gray_800` (#E4E4E4) |
| `typeset_lg_medium/*` @typeset | Medium 16 / 24 / 0 | 10 | 원격 텍스트 스타일 `typeset_lg_medium`(노드 2개)이 끌고 오는 5개 속성. Syrup에 대응 스타일 없음 |

이 밖에 `textRangeFills`(문자 범위 단위 색상)로 지정된 몇 건은 노드 단위 교체 대상이 아니어서 남아 있습니다.

#### 원격 텍스트 스타일 — ℹ️ 의도된 예외 (2026-10-08)

파일 전체의 원격 텍스트 스타일을 정리하는 과정에서, **AD 페이지의 4건은 교체하지 않고 예외로 두기로** 했습니다.

| 스타일 | 스펙 | 건수 | Node | 위치 |
| --- | --- | --- | --- | --- |
| `typeset_lg_medium` | Pretendard Medium 16 / LH 24 / LS 0 | 2 | `8590:9311` · `8590:3509` | `ETMS` › `48` · `P_AD` › "1.91:1 비율로 리사이즈" |
| `syrup_typo/c200` | Pretendard Regular 11 / LH 16 / LS 0 | 2 | `8590:3513` · `8590:3514` | `P_AD` › "쿠팡 골드박스" · "오전 7시부터 공개되는 한정 상품" |

**AD는 사내 다른 시스템의 규격을 따르는 영역이 있어, 해당 라이브러리 스타일을 그대로 유지합니다.** Syrup 토큰으로 수렴시킬 대상이 아닙니다.

참고로 로컬에 값이 가까운 스타일은 있습니다. 나중에 판단이 바뀔 경우를 위해 기록해 둡니다.

| 원격 | 로컬 최근접 | 차이 |
| --- | --- | --- |
| `typeset_lg_medium` | `t1200_16_medium` | LH 24 → 20 · LS 0 → −0.8 |
| `syrup_typo/c200` | `c200_11_regular` | **LS 0 → −0.3** (이름·크기·LH 동일) |

### 2. ✅ 프로퍼티명 오타 — 해소 (2026-10-12 확인)

`Naver_AD` `8595:15613`의 variant 축 이름이 **`Coner`** 였습니다. `Corner`가 맞습니다.

| 항목 | 2026-09-21 | 2026-10-12 |
| --- | --- | --- |
| 프로퍼티명 | **`Coner`** | **`Corner`** ✅ |
| 옵션 | `False` · `True` | 변경 없음 |

**재확인 결과 이미 수정되어 있습니다.** 파일 전체를 `coner` 패턴으로 스캔해도 **0건**입니다.

> 파일 전체의 프로퍼티명 오타는 [List Footer](syrup-list-footer-components.md)의 `Viariant`, [List Row](syrup-list-row-components.md)의 `Cancle`, [Product Grid](syrup-product-grid-components.md)의 `Phatner`와 함께 **모두 해소**되었습니다.

### 3. 토큰 미바인딩 값

2026-09-21 파일 전체 바인딩 정리로 **값이 토큰과 일치하는 건은 모두 바인딩**되었습니다. AD 페이지에 남은 값은 전부 스케일에 없는 임의 값입니다. (인스턴스 외부 기준)

| 속성 | 남은 값 (건수) |
| --- | --- |
| padding | `100` (14) · `5` (12) · `14` (7) · `1` (6) · `7` (5) · `11` (1) |
| itemSpacing | `−7` (2) · `5` (1) · `7` (1) · `143` (1) |

> corner radius `5`(20건)는 목록에서 제외했습니다. **Figma가 컴포넌트셋 점선 컨테이너에 기본으로 넣는 값**이며, 파일 전체 컴포넌트셋 178개에 동일하게 나타납니다. 프로덕션에 렌더링되지 않으므로 토큰화 대상이 아닙니다.

- `Spacing` 스케일은 0 · 2 · 4 · 6 · 8 · 10 · 12 · 16 · 20 … 으로 구성되어 **1 · 5 · 7 · 11 · 14** 같은 값은 대응 토큰이 없습니다. 디자인을 스케일에 맞출지, 토큰을 추가할지 판단이 필요합니다.
- 금주머니 `Active=On`의 itemSpacing **−7**은 주머니와 timer를 겹치기 위한 음수 값이라 토큰화 대상이 아닙니다.
- `Badge`의 상하 padding `2`와 금주머니 `timer`의 padding `2 / 6`은 각각 `Spacing/50` · `Spacing/150`으로 **바인딩 완료**되었습니다.

### 4. ✅ 명칭과 실제 치수 불일치 (2026-11-03 해소)

`DA`의 `Type=H185` variant는 이름상 높이 185이지만 **실제 프레임 높이는 187**이었습니다.

**소재 높이가 185이고 위아래 여백이 1씩** 붙어 187이 되는 구조였습니다. 자리표시자 문구를 「H185 리사이즈」에서 **「H185 · 소재 185 / 전체 187」** 로 바꿔 컴포넌트 안에 기준을 남겼고, Usage **C**의 설명에도 같은 내용을 적었습니다.

### 5. 텍스트에 U+2028 포함

Title Bar 등 일부 텍스트에 **U+2028 (LINE SEPARATOR)** 문자가 줄바꿈으로 들어 있습니다. Figma에서는 정상 표시되지만, JSON으로 내보내거나 API로 읽을 때 파서를 깨뜨릴 수 있습니다. 일반 개행(`\n`)으로 교체하는 편이 안전합니다.

### 6. 배너 계열 컷이 회색 자리표시자로 보입니다

`DA` · `Naver_AD` 마스터 컴포넌트는 **실제 광고 소재가 아니라 규격만 적힌 회색 자리표시자**입니다. 컷을 인스턴스로 바꾸면서 Usage의 **A · B · C · F · G**가 회색 박스로 보입니다.

2026-11-03에 자리표시자 문구를 **규격을 읽을 수 있게** 고쳤습니다.

| 컴포넌트 | 자리표시자 문구 |
| --- | --- |
| `DA / Type=H80` | 「H80 리사이즈」 |
| `DA / Type=H185` | 「H185 · 소재 185 / 전체 187」 |
| `Naver_AD` | 「네이버 피드 광고 약 1.065:1 비율 유지(원본 이미지 360×338)」 |

소재가 들어 있는 D·E·H와 달리 일부 배너는 규격 안내용 자리표시자입니다. 실제 사용 소재는 허용된 슬롯·인스턴스 오버라이드로 적용하며, 이 문서를 사용한다는 이유로 원본 마스터를 수정하지 않습니다.

### 7. 정리 대기 노드

| 노드 | 내용 |
| --- | --- |
| [`원본 컷 (정리 전)` `11146:10`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11146-10) | 교체 전 `360 × 780` 화면 컷 12개 (Usage 8 · Guidelines 4). 확인 후 지우면 됩니다 |
| `네이버 피드` `11141:15965` | `G` 컷에서 쓰던 로컬 컴포넌트. `Naver_AD` 세트에 속하지 않는 별도 컴포넌트라 교체 때 `Naver_AD / Corner=False`로 바꿨습니다 |
