# Syrup Design System — Bottom Sheet 컴포넌트

| 항목 | 값 |
| --- | --- |
| Figma File | [Syrup_Design-System](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System) |
| Page / Section | `Bottom Sheet` 페이지 → [Bottom Sheet 섹션 `8680:16343`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=8680-16343) |
| 섹션 구성 | `Bottom Sheet` 1440×5059 → `Guidelines` 960×4020 → `Usage` 3360×914 (가로 일렬) |
| 기준일 | 2026-11-05 (Usage · Guidelines 신설 / 스펙 정리: 2026-10-01) / 2026-11-11 Selection 전체 이름·선택 표시 기준 보완 |
| 관련 문서 | [syrup-design-tokens.md](syrup-design-tokens.md) · [syrup-dialog-components.md](syrup-dialog-components.md) · [syrup-alert-components.md](syrup-alert-components.md) · [syrup-badge-components.md](syrup-badge-components.md) · [syrup-banner-components.md](syrup-banner-components.md) · [syrup-border-components.md](syrup-border-components.md) · [syrup-bottom-info-components.md](syrup-bottom-info-components.md) · [syrup-bottom-cta-components.md](syrup-bottom-cta-components.md) · [syrup-ad-components.md](syrup-ad-components.md) · [syrup-bubble-components.md](syrup-bubble-components.md) · [syrup-button-components.md](syrup-button-components.md) · [syrup-checkbox-components.md](syrup-checkbox-components.md) · [syrup-chip-components.md](syrup-chip-components.md) · [syrup-card-components.md](syrup-card-components.md) · [syrup-dim-components.md](syrup-dim-components.md) · [syrup-grid-list-components.md](syrup-grid-list-components.md) · [syrup-grid-scroll-components.md](syrup-grid-scroll-components.md) · [syrup-header-components.md](syrup-header-components.md) · [syrup-icon-button-components.md](syrup-icon-button-components.md) · [syrup-indicator-components.md](syrup-indicator-components.md) · [syrup-keypad-components.md](syrup-keypad-components.md) · [syrup-label-components.md](syrup-label-components.md) · [syrup-list-footer-components.md](syrup-list-footer-components.md) · [syrup-list-header-components.md](syrup-list-header-components.md) · [syrup-list-row-components.md](syrup-list-row-components.md) · [syrup-loader-components.md](syrup-loader-components.md) · [syrup-lottie-components.md](syrup-lottie-components.md) · [syrup-product-grid-components.md](syrup-product-grid-components.md) · [syrup-product-list-components.md](syrup-product-list-components.md) · [syrup-product-scroll-components.md](syrup-product-scroll-components.md) · [syrup-progress-stepper-components.md](syrup-progress-stepper-components.md) · [syrup-result-components.md](syrup-result-components.md) · [syrup-search-field-components.md](syrup-search-field-components.md) · [syrup-stepper-components.md](syrup-stepper-components.md) · [syrup-swipe-components.md](syrup-swipe-components.md) · [syrup-switch-components.md](syrup-switch-components.md) · [syrup-tab-components.md](syrup-tab-components.md) · [syrup-tab-bar-components.md](syrup-tab-bar-components.md) · [syrup-text-button-components.md](syrup-text-button-components.md) · [syrup-text-field-components.md](syrup-text-field-components.md) · [syrup-ticker-components.md](syrup-ticker-components.md) · [syrup-toast-components.md](syrup-toast-components.md) |

> **화면 하단에서 위로 등장하여 추가 정보나 행동을 제공하는 모달 요소에요.**
> 사용자가 현재 맥락을 유지하면서 보조적인 정보를 확인하거나 액션을 해야할 때 사용해요.

---

## 공개 에셋 이름 정리

2026-11-11 아래 원본의 `.primitive / ` 접두사만 제거했어요. 노드·컴포넌트 키·variant·인스턴스 연결은 유지했으며 게시 작업은 별도로 진행해요. 숨김 유지·검토 대상의 접두사는 유지해요.

| 현재 전체 이름 | 원본 노드 |
| --- | --- |
| `Bottom Sheet / Body / List` | `8687:8524` |
| `Bottom Sheet / Body / List / List Item` | `8687:6643` |
| `Bottom Sheet / Body / Selection` | `8689:5852` |
| `Bottom Sheet / Body / Selector / Select Item` | `8689:5842` |
| `Bottom Sheet / Body / Stepper` | `8687:9149` |
| `Bottom Sheet / Body / Page` | `8689:5598` |
| `Bottom Sheet / Body / Slot` | `8689:5886` |
| `Bottom Sheet / Image / Logo` | `8689:5183` |

## 목차

1. [구성 한눈에 보기](#구성-한눈에-보기)
2. [Bottom Sheet — Master Component](#1-bottom-sheet--master-component)
3. [Title · Sub title](#2-title--sub-title)
4. [Button Area](#3-button-area)
5. [Body 컴포넌트](#4-body-컴포넌트)
6. [Image / Logo](#5-image--logo)
7. [설계 규칙 요약](#설계-규칙-요약)
8. [Usage](#usage)
9. [Guidelines](#guidelines)
10. [점검 필요 사항](#점검-필요-사항)

---

## 구성 한눈에 보기

**컴포넌트 12개**로 지금까지 문서화한 것 중 가장 큽니다. 페이지는 `Master Component` → `Child Item`(Body · Upper Item · Title & Sub Title & Description · Image) 순서입니다.

| # | 이름 | 타입 | Variant / Props | 크기 |
| --- | --- | --- | --- | --- |
| 1 | `Bottom Sheet` | Component Set | `Button` 2종 | 340 × 285~377 |
| 2 | `Body / List` | Component | `Logo` BOOLEAN | 340 × 170 |
| 3 | `Body / List / List Item` | Component | `Option` · `Checkbox` BOOLEAN | 340 × 40 |
| 4 | `Body / Selection` | Component | — | 340 × 254 |
| 5 | `Body / Selector / Select Item` | Component Set | `Checked` 2종 | 340 × 40 |
| 6 | `Body / Stepper` | Component | — | 340 × 411 |
| 7 | `Body / Page` | Component | `Slot` SLOT | 340 × 248 |
| 8 | `Body / Slot` | Component | `Selection` SLOT | 340 × 152 |
| 9 | `Button Area` | Component Set | `Buttons` 3종 × `Weak Button` | 340 × 108 · 172 |
| 10 | `Title` | Component | `Arrow` BOOLEAN | 340 × 60 |
| 11 | `Sub title` | Component | — | 340 × 39 |
| 12 | `Image / Logo` | Component Set | `Type` 2종 | 116 × 116 |

`.primitive /` 접두사는 표에서 생략했습니다.

---

## 1. Bottom Sheet — Master Component

**Node** `8687:8773` · Component Set · 2 variants

### Properties

| Property | Type | Default | 역할 |
| --- | --- | --- | --- |
| `Button` | VARIANT | `True` | 하단 버튼 영역 포함 여부 |
| `Sub title` | BOOLEAN | `true` | 보조 설명 노출 |
| `Body` | **INSTANCE_SWAP** | `Body / List` | 본문 영역을 Body 6종 중 하나로 교체 |

**`Body`가 INSTANCE_SWAP**이라는 점이 이 컴포넌트의 핵심입니다. 시트의 틀(Title · Sub title · Button Area)은 고정하고 본문만 갈아 끼우는 구조입니다.

### Variants

| Variant | 크기 |
| --- | --- |
| `Button=True` | 340 × 377 |
| `Button=False` | 340 × 285 |

### 내부 구조 (`Button=True` 기준)

| 영역 | 크기 | Padding (T/R/B/L) | Gap | 비고 |
| --- | --- | --- | --- | --- |
| 루트 | 340 × 377 | 0 | 0 | VERTICAL · `Color/Gray_White` · `Corner radius/600` (24) |
| `Title` | 340 × 60 | `Spacing/600`(24) / `Spacing/400`(16) / 0 / `Spacing/600`(24) | `Spacing/400` (16) | |
| `Sub title` | 340 × 39 | `Spacing/200`(8) / `Spacing/600`(24) / `Spacing/300`(12) / `Spacing/600`(24) | `Spacing/200` (8) | |
| `Body` (swap) | 340 × 170 | `Spacing/250`(10) / 0 / 0 / 0 | 0 | 기본값은 `Body / List` |
| `Button Area` | 340 × 108 | `Spacing/800`(32) / `Spacing/500`(20) / `Spacing/500`(20) / `Spacing/500`(20) | 0 | |

모서리 `Corner radius/600`(24)은 **네 모서리 전체**에 적용되어 있습니다. 화면 하단에 붙는 시트라면 보통 상단 두 모서리만 둥글게 처리하는데, 이 컴포넌트는 전체가 둥근 형태입니다.

---

## 2. Title · Sub title

### Title

**Node** `8686:11157` · Component · **340 × 60**

| 항목 | 값 |
| --- | --- |
| Padding | `Spacing/600`(24) / `Spacing/400`(16) / 0 / `Spacing/600`(24) |
| Gap | `Spacing/400` (16) |
| 타이틀 텍스트 | `t600_21_bold` / `Color/Gray_100` |
| 우측 아이콘 | `Header / Icon` 36 × 36 (내부 `Union` 16 × 16 / `Color/Gray_100`) |

| Property | Type | Default | 역할 |
| --- | --- | --- | --- |
| `Arrow` | BOOLEAN | `true` | 타이틀 옆 40 × 20 프레임 토글 |

### Sub title

**Node** `8686:11159` · Component · **340 × 39**

| 항목 | 값 |
| --- | --- |
| Padding | `Spacing/200`(8) / `Spacing/600`(24) / `Spacing/300`(12) / `Spacing/600`(24) |
| Gap | `Spacing/200` (8) |
| 텍스트 | `b300_15_regular` / `Color/Gray_400` |
| 샘플 | "보조 설명을 작성해주세요." |

---

## 3. Button Area

**Node** `8686:11122` · Component Set · 3 variants

### Properties

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `Buttons` | VARIANT | `1 Button` | `1 Button` · `2 Buttons (Vertical)` · `2 Buttons` |
| `Weak Button` | VARIANT | `Gray_900` | `Gray_900` ⚠️ (값 1개) |

### Variants

공통 Padding `Spacing/800`(32) / `Spacing/500`(20) 나머지 3면.

| Variant | 크기 | Gap | 버튼 구성 |
| --- | --- | --- | --- |
| `1 Button` | 340 × 108 | 0 | Primary 300 × 56 |
| `2 Buttons (Vertical)` | 340 × 172 | `Spacing/200` (8) | 위 Secondary · 아래 **Primary** |
| `2 Buttons` | 340 × 108 | `Spacing/200` (8) | 좌 Secondary 146 · 우 **Primary** 146 |

### 버튼 스펙

**Bottom CTA의 버튼과 완전히 동일한 스펙**입니다.

| 항목 | 값 |
| --- | --- |
| 높이 | 56 |
| Padding | `Spacing/50`(2) / `Spacing/700`(28) |
| Gap | `Spacing/100` (4) |
| Radius | `Corner radius/250` (10) |
| 라벨 | `t800_17_bold` |
| Primary | `Color/Primary_Orange` + `Color/Gray_White` |
| Secondary | `Color/Gray_900` + `Color/Gray_200` |

주 액션 위치도 같습니다 — **세로형은 아래, 가로형은 오른쪽**.

---

## 4. Body 컴포넌트

본문 컴포넌트는 전부 폭 **340** 고정입니다. `Body` INSTANCE_SWAP에 **직접 끼울 수 있는 것은 5종**이고, 나머지 2종은 그 안에서 한 줄을 이루는 하위 컴포넌트입니다.

| 컴포넌트 | 크기 | Props | 내용 | swap |
| --- | --- | --- | --- | --- |
| `Body / List` | 340 × 170 | `Logo` BOOLEAN(`false`) | List Item 반복 + 상단 Logo 프레임 | ✅ |
| `Body / Selection` | 340 × 254 | — | Select Item 반복 | ✅ |
| `Body / Stepper` | 340 × 411 | — | `Stepper` 프레임 | ✅ |
| `Body / Page` | 340 × 248 | `Slot` SLOT | 슬롯 + 페이지네이션 | ✅ |
| `Body / Slot` | 340 × 152 | `Selection` SLOT | 자유 영역 | ✅ |
| `Body / List / List Item` | 340 × 40 | `Option` · `Checkbox` BOOLEAN(둘 다 `true`) | 체크박스 + 텍스트 + Arrow | — |
| `Body / Selector / Select Item` | 340 × 40 | `Checked` VARIANT(`True`/`False`) | 선택 옵션 행 | — |

다섯 가지를 각각 어떤 자리에 쓰는지는 [Usage A~E](#본문-채우기--a--b--c--d--e)에 컷으로 정리했습니다.

### List Item 상세

| 항목 | 값 |
| --- | --- |
| Padding | `Spacing/250`(10) / `Spacing/600`(24) |
| Gap | `Spacing/400` (16) |
| 구성 | `Checkbox` 20 × 20 + 텍스트 묶음(gap `Spacing/200`=8) + `Icon / Arrow` 16 × 16 |

이 컴포넌트는 **Bottom CTA의 `Upper Item > List` variant에서도 재사용**됩니다.

### Page 상세

| 영역 | 크기 | Padding / Gap | 비고 |
| --- | --- | --- | --- |
| 루트 | 340 × 248 | pad `Spacing/250`(10) / `Spacing/600`(24) / 0 / `Spacing/600`(24), gap `Spacing/600`(24) | `Color/Gray_White` |
| `List` | 292 × 208 | gap `Spacing/500` (20) | |
| └ `Slot` | 292 × 142 | gap `Spacing/250`(10), `Corner radius/400`(16) | **SLOT** |
| └ `Text` | 292 × 46 | gap `Spacing/150` (6) | |
| `syrup_pagination` | 30 × 6 | gap `Spacing/150` (6) | 6 × 6 원 3개 |

페이지네이션은 현재 위치 `Color/Gray_500`, 나머지 `Color/Gray_750`입니다.

### Select Item 상세

정렬·옵션을 고르는 목록의 **한 줄**입니다. `Body / Selection`이 이 컴포넌트를 여러 개 쌓아 목록을 만듭니다.

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `Checked` | VARIANT | `True` | `True` · `False` |

| Variant | Node | 크기 | 텍스트 색 | 체크 표시 |
| --- | --- | --- | --- | --- |
| `Checked=True` | `8689:5840` | 340 × 40 | `Color/Primary_Orange` | `Checkbox` · `Variant=Line` · `Size=M` · `Checked=True` · 24 × 24 (원형 배경 없는 선형 체크) |
| `Checked=False` | `8689:5841` | 340 × 40 | `Color/Gray_100` | 없음 |

| 항목 | `Checked=True` | `Checked=False` |
| --- | --- | --- |
| 상하 Padding | `Spacing/200` (8) | `Spacing/250` (10) |
| 좌우 Padding | `Spacing/600` (24) | `Spacing/600` (24) |
| Gap | `Spacing/500` (20) | `Spacing/500` (20) |
| 텍스트 | `b200_16_regular` | `b200_16_regular` |

**두 variant의 높이가 40으로 같습니다.** 콘텐츠 높이가 다르므로(체크 쪽은 24px 아이콘, 미체크 쪽은 20px 텍스트) 상하 패딩을 8 / 10으로 달리해 맞춘 구조입니다.

---

## 5. Image / Logo

**Node** `8689:5183` · Component Set · 전 variant **116 × 116**

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `Type` | VARIANT | `Naver` | `Naver` · `OCB` |

| Variant | 구성 |
| --- | --- |
| `Type=Naver` | `Naver` 래스터 |
| `Type=OCB` | `P` 래스터 + `OCB` 그룹 (벡터) |

---

## 설계 규칙 요약

| 항목 | 값 |
| --- | --- |
| 폭 | **340 고정** |
| 모서리 | `Corner radius/600` (24) — 네 모서리 전체 |
| 배경 | `Color/Gray_White` |
| 좌우 여백 | `Spacing/600` (24) · 버튼 영역만 `Spacing/500` (20) |
| 타이틀 | `t600_21_bold` / `Color/Gray_100` |
| 보조 설명 | `b300_15_regular` / `Color/Gray_400` |
| 본문 목록 | `b200_16_regular` |
| 버튼 | 높이 56 · `Corner radius/250`(10) · `t800_17_bold` |
| 주 액션 | `Color/Primary_Orange` + `Color/Gray_White` |
| 보조 액션 | `Color/Gray_900` + `Color/Gray_200` |

---

## Usage

| 항목 | 값 |
| --- | --- |
| 섹션 | [`Usage` `11392:545`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11392-545) · 3360 × 914 |
| 구성 | 8패턴 · 화면 360 × 580 · 시트 높이 285~472 |
| 템플릿 | `Usage` 컴포넌트 [`11237:46733`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11237-46733) (`❖System Components` 페이지) |

> **컷은 화면 캡처가 아니라 실제 컴포넌트 인스턴스입니다.**
> 해당 컴포넌트와 **꼭 필요한 맥락 요소만** 남기고 나머지 화면 요소는 모두 지웠습니다. 남은 요소도 잘라낸 그림이 아니라 마스터를 직접 참조하는 인스턴스라, 컴포넌트 디자인이 바뀌면 문서가 함께 바뀝니다 (2026-11-05).

패턴 하나가 `Usage` 템플릿 인스턴스 하나입니다. 템플릿은 `Title`(제목 + 설명)과 `Component` **슬롯**으로 이루어져 있고, 슬롯 안에 그 패턴을 보여 줄 인스턴스를 넣습니다. 가로 간격은 40입니다.

**모든 컷이 딤 위에 떠 있는 화면입니다.** 시트만 떼어 놓으면 **흰 배경에 흰 시트**라 경계가 보이지 않고, 좌우 10 · 하단 32라는 자리도 드러나지 않습니다. 그래서 컷마다 화면 프레임을 두고 `Dim` 인스턴스 위에 시트를 올렸습니다.

| 화면 프레임 | 값 |
| --- | --- |
| 크기 | **360 × 580** (전 컷 동일) |
| 배경 | `Color/Gray_White` |
| 딤 | `Dim` [`10285:3541`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=10285-3541) · 검정 75% |
| 시트 자리 | 좌우 **10** · 하단 **32** |

**시트 바닥이 여덟 컷 모두 548(580 − 32)에 맞춰져 있습니다.** 시트 높이가 285에서 472까지 달라도 아래 선은 흔들리지 않고, 위로 보이는 딤의 높이만 달라집니다.

Bottom Sheet는 **틀을 고정하고 본문만 갈아 끼우는 구조**입니다. 그래서 달라지는 것은 거의 전부 **`Body`에 무엇을 끼우느냐**와 **머리말·버튼을 어떻게 두느냐**입니다. 여덟 패턴을 세 묶음으로 나눴습니다.

| 묶음 | 패턴 | 무엇이 달라지는가 |
| --- | --- | --- |
| **본문 채우기** | A · B · C · D · E | `Body` INSTANCE_SWAP에 끼우는 컴포넌트 |
| **머리말 구성** | F · G | `Logo` · `Sub title` |
| **버튼 구성** | H | `Button Area`의 `Buttons` |

### 본문 채우기 — A · B · C · D · E

`Body`에 끼울 수 있는 컴포넌트는 **다섯 가지**이고, 다섯 패턴이 각각 하나씩 맡습니다.

| | 패턴 | 설명 | `Body` | 시트 높이 |
| --- | --- | --- | --- | --- |
| **A** | 약관 목록 보여주기 | 동의가 필요한 약관을 한 줄씩 나열할 때 사용해요. 각 줄 끝에 화살표를 두어 전문을 따로 열어볼 수 있게 해요. | `Body / List` · 3줄 | 314 |
| **B** | 항목 하나 고르기 | 정렬이나 필터처럼 여러 항목 중 하나만 고를 때 사용해요. 고른 항목만 주황색 글씨와 체크 표시로 나타내요. | `Body / Selection` · 6줄 | 326 |
| **C** | 순서대로 안내하기 | 여러 단계를 거쳐야 하는 이용 방법을 설명할 때 사용해요. 번호와 썸네일을 함께 두어 순서를 따라가게 해요. | `Body / Stepper` · 2단계 | **472** |
| **D** | 여러 장으로 넘겨 보기 | 이미지와 설명을 여러 장으로 나누어 보여줄 때 사용해요. 아래 인디케이터로 전체 장수와 현재 위치를 알려줘요. | `Body / Page` | 416 |
| **E** | 전용 콘텐츠 구성하기 | 내용에 맞는 Body 컴포넌트를 선택하고, 제공된 형태로 담기 어려운 달력 등은 Body / Slot으로 자유롭게 구성해요. 시트의 기본 구조와 좌우 여백 24는 유지해요. | `Body / Slot` | 335 |

**C와 E는 제품 화면을 그대로 세웠습니다.** C의 썸네일은 실제 쇼핑몰 카드와 「금 모으는 쇼핑」 탭이고(화면 프레임 이름도 `SG01-1`), E는 「금 받는 식단 기록」의 달력입니다. 단계 수도 제품에 맞춰 **2단계**로 줄였습니다.

**E가 `Arrow`를 쓰는 유일한 컷입니다.** 달력의 「2025년 7월」 옆에 붙은 **‹ ›** 가 `Title`의 `Arrow` BOOLEAN입니다 — 월을 앞뒤로 넘기는 표시입니다 → [점검 7](#7--title의-arrow가-무엇인지-확인됨-2026-11-05)

**E는 「무엇이든 들어갈 수 있는 자리」입니다.** `Body / Slot`은 292 폭의 빈 슬롯 하나뿐이라, 다른 네 가지로 담기지 않는 화면은 전부 여기로 옵니다. 제품에서 가장 많이 쓰이는 `Body`도 이것입니다 (18건 중 7건).

### 머리말 구성 — F · G

| | 패턴 | 설명 | 켜는 것 | 시트 높이 |
| --- | --- | --- | --- | --- |
| **F** | 제휴 로고 보여주기 | 다른 서비스와 연결되는 동의를 받을 때 사용해요. Logo를 켜서 어느 서비스와 연결되는지 먼저 보여줘요. | `Body / List`의 **`Logo=true`** (116 × 116) | 412 |
| **G** | 보조 설명 더하기 | 제목과 별도로 조건이나 부가 정보를 안내할 때 Sub title을 사용해요. 제목은 주요 내용을, 보조 설명은 관련 조건을 전달해요. | **`Sub title=true`** (39) | 285 |

**F의 `Option`도 함께 켰습니다.** 목록 각 줄에 「(SK플래닛(주) 귀중)」처럼 **괄호 보조 문구**가 붙는 것이 `List Item`의 `Option` BOOLEAN입니다. 제휴 동의처럼 받는 쪽을 밝혀야 하는 자리에서 쓰입니다.

**G는 제품에 아직 없는 조합입니다.** 통신사 선택 시트(`Body / Selection` 4줄)에 보조 설명을 얹었습니다. `Sub title`은 18건 중 3건에서만 켜져 있고 그 3건이 전부 아이데이션 페이지입니다 → [점검 8](#8-sub-title이-제품에서-쓰이지-않습니다)

### 버튼 구성 — H

| | 패턴 | 설명 | `Buttons` | 시트 높이 |
| --- | --- | --- | --- | --- |
| **H** | 되돌리는 행동과 함께 두기 | 이전 단계로 돌아가는 행동과 진행하는 행동을 함께 제공할 때 사용해요. 보조 행동은 왼쪽, 주요 행동은 오른쪽에 둬요. | `2 Buttons` (146 + 146) | 470 |

**버튼이 둘인 경우는 이 하나뿐입니다.** 제품 18건의 `Button Area`도 `1 Button` 9건 · `2 Buttons` 2건이고, 나머지 7건은 버튼 영역 자체가 없습니다. 남은 `2 Buttons (Vertical)`은 제품에도 문서에도 쓰인 곳이 없습니다 → [점검 9](#9-2-buttons-vertical이-쓰인-적이-없습니다)

### 제품 실측 (2026-11-05)

제품 파일 **[Syrup_App](https://www.figma.com/design/LekNzN0LrcSKQYdutQFI1i)** 전체에서 `Bottom Sheet` 인스턴스 **18건**을 전수 조사했습니다. 이 중 3건은 아이데이션 페이지의 것이라, 실제 제품 화면은 **15건**입니다.

| 항목 | 값 | 건수 |
| --- | --- | --- |
| 배치 | **직접 배치** | **18** |
| | 다른 컴포넌트 안에 중첩 | **0** |
| 화면에서의 자리 | 좌우 10 · 하단 **32** | 15 |
| | 좌우 10 · 하단 14 | 1 (아이데이션) |
| `Body` | `Slot` | **7** |
| | `List` | 4 |
| | `Page` | 3 |
| | `Selection` | 2 |
| | `Stepper` | 2 |
| `Button` | `True` | 11 |
| | `False` | 7 |
| `Buttons` | `1 Button` | 9 |
| | `2 Buttons` | 2 |
| | **`2 Buttons (Vertical)`** | **0** |
| `Sub title` | `false` | 15 |
| | `true` | **3** (전부 아이데이션) |
| `Arrow` (Title) | `false` | 17 |
| | **`true`** | **1** (달력 시트) |
| 타이틀 높이 | 60 (1줄) | 13 |
| | 82 (2줄) | 4 |
| | **109 (3줄)** | **1** |
| 딤 | `Dim` 컴포넌트 | 13 |
| | 직접 그린 사각형 | **2** |
| | 없음 | 3 (아이데이션) |
| 시트 높이 | 218 ~ 624 | — |

**중첩이 한 건도 없습니다.** Bottom Sheet는 언제나 화면 위에 혼자 올라오는 요소라, 다른 컴포넌트 안에 들어가지 않습니다. Badge(328건 중 280건 중첩)와 정반대입니다.

**자리가 15건 모두 같습니다.** 좌우 10, 아래 32. 이 수치가 [점검 4](#4--시트-모서리가-네-방향-모두-둥근-이유가-확인됨-2026-11-05)의 「네 모서리가 모두 둥근 이유」를 설명합니다.

> **`Arrow` 수치를 2026-11-05에 고쳤습니다.** 앞서 「18건 전부 `false`」라고 적었던 것은 수집 예제 7컷만 보고 전체로 넓힌 것이었습니다. 제품 전수를 다시 세어 보니 **달력 시트(`AC01_캘린더`) 1건이 `Arrow=true`** 를 쓰고 있습니다 → [점검 7](#7--title의-arrow가-무엇인지-확인됨-2026-11-05)

---

## Guidelines

지켜지지 않으면 결과가 깨지는 것만 올렸습니다. 각 항목은 Figma **[`Guidelines` 섹션 `11392:544`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11392-544)** (960 × 4020) 에 한 쌍씩 들어 있습니다.

규칙 하나가 `Guidelines` 템플릿 인스턴스 [`11237:44468`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11237-44468) (`❖System Components` 페이지) 하나입니다. 폭 760, `Title`(제목 + 설명) 아래 `Image` 프레임에 슬롯이 좌우로 들어갑니다.

**좌우 두 컷 모두 딤 화면에 올렸습니다.** 한쪽만 화면에 올리면 **딤의 유무가 Do의 조건처럼 읽히기** 때문입니다. 두 예외는 딤과 자리 자체가 비교 대상인 규칙입니다 — 규칙 1의 Don't는 화면에 붙여 배치했고, 규칙 2의 Don't에는 딤이 없습니다.

**화면 높이는 규칙마다 다릅니다.** Usage는 여덟 컷을 360 × 580으로 통일했지만, Guidelines는 비교에 필요한 만큼만 잡았습니다. 시트 바닥에서 하단 32를 띄우는 것은 모두 같습니다.

| 규칙 | 화면 높이 |
| --- | --- |
| 1 · 2 | 360 × **380** |
| 3 · 4 | 360 × **360** |
| 5 | 360 × **580** |
| 6 | 360 × **420** |

**여섯 규칙은 세 가지 층위에서 나왔습니다.**

| 층위 | 규칙 | 근거 |
| --- | --- | --- |
| 화면 위에 놓이는 방식 | 1 · 2 | 제품 15건이 모두 같은 자리·같은 딤 |
| 컴포넌트를 고르는 방식 | 3 · 4 | `Button=False`의 하단 여백 16 · `Body` 선택 |
| 안에 담는 내용 | 5 · 6 | 버튼 순서 · 제목과 보조 설명의 분담 |

**다섯은 Do / Don't이고, 마지막 하나만 두 경우를 나란히 비교합니다.**

| 형식 | 규칙 | 슬롯 라벨 | 라벨 색 |
| --- | --- | --- | --- |
| Do / Don't | 1 · 2 · 3 · 4 · 5 | `Do` · `Don’t` | `#222222` · **`#FF3E00`** |
| 두 경우 비교 | **6** | 「보조 설명 활용」 · 「제목으로 안내」 | `#222222` · **`#222222`** |

6은 **둘 다 정상인 선택**이라 Do / Don't로 두지 않았습니다. Badge 규칙 1, Banner 규칙 3, [Bottom Info 규칙 7](syrup-bottom-info-components.md#7-소제목을-강조해-정보-묶음을-구분할-수-있어요)과 같은 방식입니다.

**두 경우 비교에서는 오른쪽 라벨 색도 검정으로 바꿉니다 (2026-11-05).** 앞선 페이지들은 라벨 글자만 바꾸고 `Don’t`의 주황(`#FF3E00`)은 그대로 두었는데, 둘 다 정상인 항목에서 한쪽만 주황이면 **금지로 읽힙니다.** 여기서부터는 색까지 `#222222`로 맞춥니다.

### 1. 화면 아래에서 띄워 배치해요

시트는 화면에 붙이지 않고 좌우 10, 아래 32를 띄워 배치해요.
네 모서리가 모두 둥근 형태라 띄워야 모서리가 온전히 보여요.

| 라벨 | 폭 | 좌우 · 하단 | 결과 |
| --- | --- | --- | --- |
| **Do · 좌우 10 / 하단 32** | 340 | 10 · **32** | 네 모서리가 모두 보임 |
| **Don't · 좌우·하단 여백 없음** | **360** | 0 · **0** | 아래 두 모서리가 화면 밖으로 잘림 |

**이 규칙만 슬롯 라벨에 수치를 붙였습니다.** 두 컷의 차이가 여백이라 라벨에서 바로 읽히는 편이 낫습니다.

두 컷 모두 360 × 380 화면 안에 같은 안내 시트(340 × 276)를 띄운 것이고, **다른 것은 시트의 폭과 자리**입니다. 제품 15건이 예외 없이 좌우 10 · 하단 32를 씁니다.

### 2. 딤을 함께 사용해 뒤 화면과 구분해요

시트를 띄울 때는 Dim으로 뒤 화면을 어둡게 해요.
현재 조작하는 시트를 강조하고 뒤 화면과 구분해요.

| | 딤 | 결과 |
| --- | --- | --- |
| **Do** | `Dim` 컴포넌트 (검정 75%) | 시트가 앞에 떠 보임 |
| **Don't** | 없음 | 시트와 뒤 화면이 한 장으로 보임 |

Don't 컷을 보면 시트의 테두리가 사라져 **어디까지가 시트인지 알 수 없습니다.** Bottom Sheet는 그림자가 없고 배경이 `Color/Gray_White`라, 경계를 만드는 것이 전적으로 딤입니다.

딤은 `Dim` 컴포넌트([`10285:3541`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=10285-3541))를 쓰세요. 제품 15건 중 2건이 직접 그린 사각형을 쓰고 있습니다 → [점검 10](#10-딤을-직접-그린-사각형으로-쓴-곳이-있습니다)

### 3. 버튼이 없으면 시트 내부 하단 여백 16을 유지해요

버튼 없이 본문으로 끝나는 시트는 마지막 항목 아래에 내부 여백 16을 둬요.
항목이 둥근 모서리에 닿지 않도록 시트 안쪽 여백을 유지해요.

| | `paddingBottom` | 시트 높이 | 결과 |
| --- | --- | --- | --- |
| **Do** | **16** | 246 | 마지막 항목과 모서리 사이가 비어 있음 |
| **Don't** | **0** | 230 | 마지막 항목이 모서리에 닿음 |

**「시트 내부」를 제목에 넣은 이유가 있습니다.** Bottom Sheet에는 여백이 두 군데 있습니다 — 화면과 시트 사이의 **하단 32**(규칙 1)와, 시트 안 마지막 항목 아래의 **16**입니다. 둘을 구분하지 않으면 어느 쪽을 말하는지 헷갈립니다.

**이 16은 variant가 이미 가지고 있는 값입니다.** `Button=False` variant에 `paddingBottom=16`이 들어 있어, 손대지 않으면 저절로 지켜집니다. 제품의 `Button=False` 7건이 모두 16입니다.

`Button=True`일 때는 0입니다 — `Button Area`가 자기 몫으로 하단 패딩 20을 갖고 있기 때문입니다.

### 4. 하나만 고르는 목록은 Selection으로 만들어요

정렬이나 필터처럼 하나만 고르는 목록에는 `Bottom Sheet / Body / Selection`을 사용해요.
각 행은 `Bottom Sheet / Body / Selector / Select Item`으로 구성하고, 선택한 항목만 `Checked=True`, 나머지는 `Checked=False`로 설정해요.
선택 표시는 행 내부의 `Checkbox` (`Variant=Line`, `Size=M`, `Checked=True`, `Disabled=False`, 24×24)를 그대로 사용해요. 선택된 문구는 주황색으로 강조하고 오른쪽에 선형 체크를 표시해요. 원형 체크박스나 완료용 Badge를 별도로 덧붙이지 않아요.

선택형 컴포넌트 참조:
- Body 전체 이름: `Bottom Sheet / Body / Selection` · 노드 `8689:5852` · 컴포넌트 키 `07ecdabfe99197e7decb0f49910360520f3cfadf`
- 행 전체 이름: `Bottom Sheet / Body / Selector / Select Item` · 세트 `8689:5842` · 선택 `8689:5840` / 미선택 `8689:5841`
- `Body / Selection`은 위 전체 이름의 약칭이에요. `Selection`과 행 경로의 `Selector`는 실제 이름이 다르므로 같은 이름으로 정규화하지 않아요.
- Body의 행 개수와 문구는 내용에 맞춰 구성해요. ‘추천순·최신순·적립금 높은순·가격 낮은순’ 예제에서는 추천순만 선택해요.
- 찾지 못했을 때 `Body / List`와 별도 Badge로 대체하지 말고, 전체 이름·노드·키를 기준으로 원본을 다시 확인해요.


| | `Body` | 선택 표시 | 결과 |
| --- | --- | --- | --- |
| **Do** | `Body / Selection` | 주황색 글씨 + 오른쪽 체크 | 하나만 고르는 목록으로 읽힘 |
| **Don't** | `Body / List` (`Checkbox=true`) | 왼쪽 빈 원 네 개 | 여러 개를 고를 수 있어 보임 |

**체크 표시의 자리가 다릅니다.** `Select Item`은 고른 줄의 **오른쪽 끝**에만 체크를 두고 글씨를 주황으로 바꿉니다. `List Item`의 체크박스는 **왼쪽**에 빈 원으로 먼저 나타나, 모두 고를 수 있는 것처럼 보입니다.

### 5. 버튼을 가로로 두 개 배치할 때는 주요 행동을 오른쪽에 둬요

버튼을 가로로 두 개 배치할 때는 되돌리는 행동을 왼쪽에, 진행하는 주요 행동을 오른쪽에 둬요.
주요 행동에는 채워진 버튼을 사용해 두 행동의 우선순위를 명확하게 구분해요.

| | 왼쪽 | 오른쪽 |
| --- | --- | --- |
| **Do** | 「이전」 `Variant=Weak` | **「변경하기」 `Variant=Fill`** |
| **Don't** | **「변경하기」 `Variant=Fill`** | 「이전」 `Variant=Weak` |

두 컷 모두 같은 안내에 같은 두 버튼이고, **다른 것은 좌우 순서**입니다. 자리만 바꾼 것이 아니라 `Variant`도 함께 따라가, Don't에서는 **채워진 버튼이 왼쪽에** 옵니다.

**세로형도 같은 원칙입니다.** `2 Buttons (Vertical)`은 위가 `Weak`, 아래가 `Fill`입니다 — 가로의 「오른쪽」이 세로에서는 「아래」가 됩니다. [Bottom CTA](syrup-bottom-cta-components.md)의 버튼 배치와 같습니다.

### 6. 부가 설명은 보조 설명으로 나눌 수 있어요

제목은 내용에 따라 여러 줄로 사용할 수 있어요.
부가 설명을 별도로 안내하고 싶을 때는 제목 아래 보조 설명을 활용해요.

| 라벨 | 제목 | 보조 설명 | `Title` 높이 |
| --- | --- | --- | --- |
| **보조 설명 활용** | 「내 주변 맛집 정보를 보여드릴까요?」 (2줄) | 「네이버가 제공하며 위치 동의가 필요해요.」 | 82 |
| **제목으로 안내** | 「내 주변 맛집 정보는 네이버가 제공하고, 위치 동의가 필요해요!」 (3줄) | 없음 | **109** |

**세 줄 제목은 금지가 아닙니다.** 제품의 실제 화면이고, 제목만으로 다 전달하겠다는 선택입니다. 묻는 말과 조건을 나누고 싶을 때 **보조 설명이라는 다른 방법이 있다**는 것이 이 규칙입니다.

제목은 `t600_21_bold`, 보조 설명은 `b300_15_regular` + `Color/Gray_400`입니다. 조건을 보조 설명으로 옮기면 **묻는 말과 조건이 굵기와 색으로 갈라져** 읽는 순서가 분명해집니다.

---

## 점검 필요 사항

### 1. ✅ `Select Item` 컴포넌트셋 오류 (2026-10-01 수정 완료)

`Bottom Sheet / Body / Selector / Select Item`(`8689:5842`)의 **두 variant 이름이 완전히 동일**해 Figma가 **"Component set has existing errors"** 로 표시하던 문제가 있었습니다. 프로퍼티 조회 자체가 실패했고, 인스턴스에서 선택/미선택을 전환할 수 없었습니다.

| 항목 | 변경 전 | 변경 후 |
| --- | --- | --- |
| 프로퍼티 축 | `Property 1` + `Property 2` (2개) | **`Checked`** (1개) |
| 1번째 variant | `Property 1=select option, Property 2=check` | **`Checked=True`** |
| 2번째 variant | `Property 1=select option, Property 2=check` (동일) | **`Checked=False`** |
| 높이 | 44 / 40 (4px 차이) | **40 / 40 (동일)** |

**검증 결과**

- 컴포넌트셋 오류 해소 — `componentPropertyDefinitions`가 `Checked: VARIANT ["False", "True"]`로 정상 조회됩니다.
- 인스턴스 6개가 모두 **구분된 variant를 가리킵니다** — `Checked=True` 1개, `Checked=False` 5개. 이전에는 전부 같은 이름으로 보여 구분이 불가능했습니다.
- 인스턴스 6개의 높이가 모두 40으로 통일되어, 항목을 선택해도 행 높이가 변하지 않습니다.

> 높이 차이는 체크 아이콘(24px)과 텍스트(20px)의 크기 차이에서 왔습니다. 상하 패딩을 8 / 10으로 달리해 맞췄으므로, 텍스트 크기나 아이콘 크기가 바뀌면 다시 어긋날 수 있습니다.

### 2. ⚠️ 같은 종류의 오류가 Grid List에 남아 있음

파일 전체를 조사했을 때 오류 상태인 컴포넌트셋은 2개였고, 위 1번을 해결한 지금은 **Grid List 1개만 남았습니다.**

| 페이지 | Node | 문제 | 상태 |
| --- | --- | --- | --- |
| Bottom Sheet | `8689:5842` | variant 이름 **중복** | ✅ 해결 (위 1번) |
| Grid List | `9711:5068` | variant 간 **프로퍼티 구성 불일치** | ⚠️ 남음 |

`Grid List / Todo / List Item`의 두 variant는 다음과 같습니다.

```
Last=False
Last=True, Property 2=Grid List, Property 3=Todo, Property 4=List Item, Property 5=True
```

한쪽은 프로퍼티가 1개인데 다른 쪽은 5개입니다. 컴포넌트 이름(`Grid List / Todo / List Item`)이 실수로 프로퍼티 값에 들어간 것으로 보입니다. Grid List 문서를 작성할 때 함께 다루겠습니다.

### 3. `Weak Button` variant 축에 값이 하나뿐

`Button Area`의 `Weak Button` 축은 선택지가 **`Gray_900` 하나**뿐입니다. 고를 것이 없는 축이 프로퍼티 패널에 노출되고, 모든 variant 이름에 `, Weak Button=Gray_900`이 붙어 이름이 길어집니다.

보조 버튼 색을 더 둘 계획이 없다면 축을 제거하는 편이 깔끔합니다. (이 축 제거는 variant 이름이 모두 바뀌므로 인스턴스 영향 확인이 필요합니다.)

### 4. ✅ 시트 모서리가 네 방향 모두 둥근 이유가 확인됨 (2026-11-05)

2026-10-01에 「화면 하단에 붙는 시트는 보통 상단 두 모서리만 둥글게 처리한다」며 의도 확인이 필요하다고 적어 두었던 항목입니다. 제품 실측으로 **의도가 확인되었습니다.**

| | 값 | 건수 |
| --- | --- | --- |
| 좌우 여백 | **10** | 15 / 15 |
| 하단 여백 | **32** | 15 / 15 |

**이 시트는 화면에 붙지 않습니다.** 좌우 10, 아래 32를 띄운 **플로팅 형태**라서 네 모서리가 모두 화면 안에 들어옵니다. `Corner radius/600`(24)을 네 모서리에 모두 건 것이 맞습니다.

이 자리를 [Guidelines 1](#1-화면-아래에서-띄워-배치해요)로 올려 두었습니다. 컴포넌트 설명에 따로 적어 둘 필요 없이, 붙여 쓰면 모서리가 잘린다는 것을 컷으로 보여 줍니다.

### 5. Bottom CTA와 컴포넌트 공유

`Body / List / List Item`이 **Bottom CTA의 `Upper Item > List` variant에서 재사용**됩니다. 이름이 `Bottom Sheet` 계열이라 Bottom CTA 쪽에서 추적하기 어렵습니다.

두 컴포넌트가 함께 쓰는 요소이므로 공용 List Item으로 승격하거나, 최소한 양쪽 문서에 의존 관계를 남겨 두는 편이 안전합니다. (Bottom CTA 문서에도 동일하게 기록해 두었습니다.)

### 6. 토큰 상태

| 항목 | 결과 |
| --- | --- |
| 미바인딩 radius · gap | **0건** |
| 미바인딩 padding | `100` 10건 — 문서 보드 레이아웃 프레임 |
| 미바인딩 fill | `#FE0955` 1건 — `Image / Logo`의 `Type=OCB` 내부 `Oval`(41 × 42), **OCB 로고 에셋 색**이라 토큰화 대상 아님 |
| 스타일 미적용 텍스트 | **0건** |
| 원격 텍스트 스타일 | **0건** |
| 외부 토큰 | `Spec docs` 11 · paragraph 계열 8 — 둘 다 전역 이슈 |

**컴포넌트 자체의 spacing · radius · 색상 · 타이포가 전부 Syrup 토큰과 로컬 스타일로 정리되어 있습니다.** 1번(Select Item 오류)은 2026-10-01에, 4번(모서리 처리)은 2026-11-05에 해결했습니다. 2번은 Grid List 페이지 소관입니다.

### 7. ✅ `Title`의 `Arrow`가 무엇인지 확인됨 (2026-11-05)

처음에는 「기본값이 `true`인데 제품 18건이 전부 `false`이고, 무엇을 뜻하는 표시인지 알 수 없다」고 적었습니다. **두 가지가 틀렸습니다.**

| | 처음 기록 | 확인된 사실 |
| --- | --- | --- |
| 제품 사용 | 0 / 18 | **1 / 18** — `AC01_캘린더` (금 받는 식단 기록) |
| 쓰임 | 알 수 없음 | **달력의 월 이동 화살표** |

켜면 타이틀 글씨 바로 뒤에 `Arrow` 프레임(40 × 20)이 붙고, 그 안에 `Variant=Left` · `Variant=Right` 아이콘(20 × 20)이 한 쌍 들어갑니다. 달력 시트의 「2025년 7월」 옆 **‹ ›** 가 바로 이것입니다 → [Usage E](#본문-채우기--a--b--c--d--e)

**0건이라고 적은 것은 제 오류입니다.** 수집 예제 7컷에 모두 `Arrow=false`인 것을 보고 제품 전체로 넓혔는데, 제품 전수를 다시 세어 보니 1건이 쓰고 있었습니다.

**남은 과제는 기본값뿐입니다.** 18건 중 17건이 끄고 쓰는데 기본값이 `true`라, 달력이 아닌 시트를 만들 때마다 꺼야 합니다. 기본값을 `false`로 내리는 편이 맞습니다.

### 8. `Sub title`이 제품에서 쓰이지 않습니다

`Sub title` BOOLEAN도 기본값이 `true`인데, 켜진 것은 **18건 중 3건**이고 그 **3건이 모두 아이데이션 페이지**(`🐷 모으기 아이데이션`)의 것입니다. 실제 제품 화면 15건에서는 **0건**입니다.

| 페이지 | `Sub title` | 건수 |
| --- | --- | --- |
| 제품 화면 | `false` | **15** |
| 아이데이션 | `true` | 3 |

쓸 자리가 없어서가 아닙니다. 제목만으로 조건까지 담다 보니 **제목이 세 줄까지 늘어난 화면**이 있는데, 이 경우 보조 설명으로 나누는 선택지가 있습니다. [Usage G](#머리말-구성--f--g)와 [Guidelines 6](#6-부가-설명은-보조-설명으로-나눌-수-있어요)에 쓰는 법을 올려 두었습니다.

다만 **세 줄 제목이 틀렸다는 뜻은 아닙니다.** 규칙 6은 둘 다 정상인 두 경우를 나란히 보여 주는 항목입니다.

### 9. `2 Buttons (Vertical)`이 쓰인 적이 없습니다

`Button Area`의 세 variant 중 **세로형만 제품 사용이 0건**입니다.

| `Buttons` | 제품 사용 | Usage 컷 |
| --- | --- | --- |
| `1 Button` | 9 | A · C · D · F |
| `2 Buttons` | 2 | H |
| **`2 Buttons (Vertical)`** | **0** | **없음** |

쓸 자리가 없는 것은 아닙니다 — 가로형 버튼은 글자가 쓸 수 있는 자리가 **90**(146 − 좌우 패딩 28 × 2)뿐이라, 라벨이 그보다 길면 세로형이 필요합니다. 다만 제품에 쓰인 예가 없어 **Usage에서는 다루지 않습니다.** 쓸 자리가 정해지면 그때 컷을 더하면 됩니다.

### 10. 딤을 직접 그린 사각형으로 쓴 곳이 있습니다

제품 15건 중 **2건**이 `Dim` 컴포넌트가 아니라 직접 그린 사각형을 쓰고 있습니다.

| 화면 | 딤 | 종류 |
| --- | --- | --- |
| `GT04-2-A` (금한돈 타이머) | `dim` | RECTANGLE |
| `SP03-modal` (본인인증) | `dimed` | RECTANGLE |
| 나머지 13건 | `Dim` | **INSTANCE** |

지금은 같은 검정 75%라 보이는 결과가 같지만, **딤 농도가 바뀌면 이 둘만 따라오지 않습니다.** `Dim` 컴포넌트([`10285:3541`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=10285-3541))의 인스턴스로 바꾸면 됩니다 → [Guidelines 2](#2-딤을-함께-사용해-뒤-화면과-구분해요)

### 11. 체크박스 유무와 버튼 라벨이 어긋납니다

목록에 체크박스가 있는 화면과 없는 화면이 **같은 버튼 라벨**을 씁니다.

| 화면 | `Checkbox` | 버튼 라벨 |
| --- | --- | --- |
| `PLP01` (PLACE SA) | **`true`** | 모두 동의하고 시작하기 |
| `RCM01` (미션 참여적립) | `false` | 모두 동의하고 시작하기 |
| `GP10` (내 금) | `false` | 모두 동의하기 |

체크박스가 있으면 **항목마다 고르라는 뜻**이고, 「모두 동의하고 시작하기」는 **한 번에 다 받겠다는 뜻**입니다. 둘이 한 화면에 함께 있으면 체크박스를 눌러야 하는지 버튼만 눌러도 되는지가 모호합니다.

어느 쪽으로 정리할지는 동의 항목에 **선택 동의가 섞여 있는지**에 달려 있어, 약관 정책과 함께 확인이 필요합니다. 근거가 정해지기 전에는 규칙으로 올릴 수 없어 **Guidelines에서는 빼 두었습니다.**

### 12. Usage에 복제한 제품 블록의 토큰 상태

[Usage C · D · E · H](#usage)와 [Guidelines 5](#5-버튼을-가로로-두-개-배치할-때는-주요-행동을-오른쪽에-둬요)의 본문 슬롯에는 제품 화면에서 복제한 블록이 들어 있습니다. 시스템 컴포넌트가 아니라 **제품에서 직접 그린 블록**이라, 그 안에 정리되지 않은 값이 남아 있습니다.

| 항목 | 건수 | 위치 |
| --- | --- | --- |
| 미바인딩 fill `#000000` | 3 | `chip_enabled` (H의 할 일 카드) |
| 스타일 없는 TEXT | **59** | **E의 달력 55** · D의 쿠팡 썸네일 4 |

달력 55건은 요일 7개와 날짜 숫자 48개이고, 글자 크기가 **10.1 · 11.02**처럼 소수점까지 들어간 값입니다. 타입 스케일 밖에 있는 수치라 달력 블록을 시스템 컴포넌트로 올릴 때 함께 정리해야 합니다.

**Bottom Sheet 컴포넌트 자체의 문제는 아닙니다.** 두 섹션의 화면 프레임 **20개 전부** 배경이 `Color/Gray_White`에 바인딩되어 있고, 남은 것은 모두 복제해 온 블록 안입니다.

| 두 섹션 구성 요소 | 개수 |
| --- | --- |
| 화면 프레임 (전부 토큰 바인딩) | **20** |
| `Dim` 인스턴스 | **19** (규칙 2의 Don't 1컷만 없음) |
| `Bottom Sheet` 인스턴스 | **20** (Usage 8 · Guidelines 12) |

Guidelines는 미바인딩 fill도 스타일 없는 텍스트도 **0건**입니다.
