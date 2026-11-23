# Syrup Design System — Keypad 컴포넌트

| 항목 | 값 |
| --- | --- |
| Figma File | [Syrup_Design-System](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System) |
| Page / Section | `Keypad` 페이지 → [Keypad 섹션 `8705:25499`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=8705-25499) |
| 섹션 구성 | Keypad 1440×1780 → Guidelines 960×1415 → Usage 960×870 |
| 컴포넌트 수 | **2개** (Component 1 · Component Set 1) |
| 기준일 | 2026-11-09 (가이드라인 4항목 · 예제 2패턴 반영) |
| 관련 문서 | [syrup-design-tokens.md](syrup-design-tokens.md) · [syrup-ad-components.md](syrup-ad-components.md) · [syrup-dialog-components.md](syrup-dialog-components.md) · [syrup-alert-components.md](syrup-alert-components.md) · [syrup-badge-components.md](syrup-badge-components.md) · [syrup-banner-components.md](syrup-banner-components.md) · [syrup-border-components.md](syrup-border-components.md) · [syrup-bottom-info-components.md](syrup-bottom-info-components.md) · [syrup-bottom-cta-components.md](syrup-bottom-cta-components.md) · [syrup-bottom-sheet-components.md](syrup-bottom-sheet-components.md) · [syrup-bubble-components.md](syrup-bubble-components.md) · [syrup-button-components.md](syrup-button-components.md) · [syrup-card-components.md](syrup-card-components.md) · [syrup-checkbox-components.md](syrup-checkbox-components.md) · [syrup-chip-components.md](syrup-chip-components.md) · [syrup-dim-components.md](syrup-dim-components.md) · [syrup-grid-list-components.md](syrup-grid-list-components.md) · [syrup-grid-scroll-components.md](syrup-grid-scroll-components.md) · [syrup-header-components.md](syrup-header-components.md) · [syrup-icon-button-components.md](syrup-icon-button-components.md) · [syrup-indicator-components.md](syrup-indicator-components.md) · [syrup-label-components.md](syrup-label-components.md) · [syrup-list-footer-components.md](syrup-list-footer-components.md) · [syrup-list-header-components.md](syrup-list-header-components.md) · [syrup-list-row-components.md](syrup-list-row-components.md) · [syrup-loader-components.md](syrup-loader-components.md) · [syrup-lottie-components.md](syrup-lottie-components.md) · [syrup-product-grid-components.md](syrup-product-grid-components.md) · [syrup-product-list-components.md](syrup-product-list-components.md) · [syrup-product-scroll-components.md](syrup-product-scroll-components.md) · [syrup-progress-stepper-components.md](syrup-progress-stepper-components.md) · [syrup-result-components.md](syrup-result-components.md) · [syrup-search-field-components.md](syrup-search-field-components.md) · [syrup-stepper-components.md](syrup-stepper-components.md) · [syrup-swipe-components.md](syrup-swipe-components.md) · [syrup-switch-components.md](syrup-switch-components.md) · [syrup-tab-components.md](syrup-tab-components.md) · [syrup-tab-bar-components.md](syrup-tab-bar-components.md) · [syrup-text-button-components.md](syrup-text-button-components.md) · [syrup-text-field-components.md](syrup-text-field-components.md) · [syrup-ticker-components.md](syrup-ticker-components.md) · [syrup-toast-components.md](syrup-toast-components.md) |

> **금액이나 수량처럼 숫자를 입력하는 화면에 사용하는 키패드 컴포넌트예요.**
> 숫자 키, 빠른 입력, 삭제 기능과 하단 CTA를 함께 구성해요.

---

## 목차

1. [구성 한눈에 보기](#구성-한눈에-보기)
2. [Keypad — Master Component](#1-keypad--master-component)
3. [Child Items — Keypad / Button](#2-child-items--keypad--button)
4. [설계 규칙 요약](#설계-규칙-요약)
5. [Usage](#usage)
6. [Guidelines](#guidelines)
7. [AI 도구 적용 기준](#ai-도구-적용-기준)
8. [현재 확인 사항](#현재-확인-사항)

---

## 구성 한눈에 보기

마스터 섹션은 1440×1780이며, Keypad와 키 버튼 2개 컴포넌트 정의로 구성됩니다. Chip과 Bottom CTA를 재사용하며, 별도 Guidelines 4항목과 Usage 2패턴에서 입력 상태와 동작을 설명합니다.

| 보드 위치 | 섹션 | 내용 |
| --- | --- | --- |
| y 434 | Master Component | `Keypad` 1종 |
| y 1190 | Child Items | `.primitive / Keypad / Button` 6종 |

| # | 이름 | 타입 | Variant / Props | 크기 | 과거 집계 인스턴스 (2026-10-12) |
| --- | --- | --- | --- | --- | --- |
| 1 | `Keypad` | Component | `CTA` BOOLEAN | 360 × 416 | **0** |
| 2 | `.primitive / Keypad / Button` | Set | `States` × `Kind` (**6종**) | 120 × 63 | 12 |

---

## 1. Keypad — Master Component

**Node** `8705:25481` · Component · variant 없음

| Property | Type | Default |
| --- | --- | --- |
| `CTA#8705:0` | BOOLEAN | `true` |

### 레이아웃

| 항목 | 값 |
| --- | --- |
| 크기 | **360 × 416** (화면 전체 폭) |
| 방향 | 세로 오토레이아웃 |
| Padding | 0 |
| Gap | `Spacing/400` (16) |
| 배경 | `Color/Gray_White` |

### 3단 구조

| # | 영역 | 크기 | 내용 |
| --- | --- | --- | --- |
| 1 | `Chip` | 360 × 56 | **[Chip](syrup-chip-components.md)** ▸ `Chip / Action` `Kind=Action3, Wrap=False` |
| 2 | `Column` | 360 × 252 | 숫자 버튼 **4행 × 3열 = 12개** |
| 3 | `Bottom CTA` | 360 × 76 | **[Bottom CTA](syrup-bottom-cta-components.md)** 인스턴스 |

**다른 페이지의 마스터 컴포넌트 2종을 그대로 가져다 씁니다.**

- 상단 칩은 `+1,000금` · `+10,000금` · `모두` 같은 **수량 바로 추가** 버튼입니다
- 하단 CTA는 `CTA` BOOLEAN으로 켜고 끌 수 있습니다

### 버튼 격자

| 항목 | 값 |
| --- | --- |
| `Chip` 영역 Padding | `Spacing/400`(16) / `Spacing/400`(16) / 0 / `Spacing/400`(16) |
| `Chip` 영역 Gap | `Spacing/300` (12) |
| `Column` Padding | 좌우 `Spacing/400` (16) |
| `Column` · `Row` Gap | **0** |
| 버튼 1개 | **109 × 63** (마스터 안에서) |

**행·열 간격이 0**입니다. 버튼이 서로 맞닿아 격자를 이룹니다.

> 현재 Section 1과 Usage A·B에서 Keypad 인스턴스를 사용합니다. 과거 0건 집계를 현재 미사용의 근거로 해석하지 않습니다.

---

## 2. Child Items — Keypad / Button

**Node** `8705:7659` · Component Set · **6 variants** · 120 × 63

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `States` | VARIANT | `Default` | `Default` · `Hover` |
| `Kind` | VARIANT | `Num` | `Icon` · `Text` · `Num` |

2 × 3 = **6조합이 모두 존재하는 완전 매트릭스**입니다.

### States — 평상시 ↔ 누름

| States | Padding | 배경 | 라운드 | 테두리 |
| --- | --- | --- | --- | --- |
| `Default` | 상하 `Spacing/400` (16) | **없음** | **0** | `Color/Gray_850` 1px — **숨김** |
| `Hover` | **0** | **`Color/Gray_900`** | **`Corner radius/400`** (16) | 없음 |

누르면 **회색 라운드 사각형이 나타나는** 방식입니다. 평상시에는 배경 없이 글자만 보입니다.

> `Default`의 `Color/Gray_850` 1px 테두리가 **페인트는 있으나 `visible: false`** 입니다. 현재는 화면에 표시하지 않는 테두리입니다

### Kind — 버튼 내용

| Kind | 내용 | 스타일 | 색 |
| --- | --- | --- | --- |
| `Num` | 숫자 `0`~`9` | **`t500_23_bold`** (23 / 29 / −0.3) | `Color/Gray_100` |
| `Text` | `전체삭제` | **`b200_16_regular`** (16 / 20 / −0.8) | `Color/Gray_100` |
| `Icon` | `syrup_ico_keyboard_back` 26 × 16 | — | — |

정렬은 **가로·세로 모두 중앙**입니다.

**숫자는 23px Bold로 크고 굵게**, 기능 버튼(`전체삭제`)은 16px Regular로 작게 처리해 숫자를 우선 읽히게 합니다.

---

## 설계 규칙 요약

| 항목 | 값 |
| --- | --- |
| 키패드 폭 | **360** (화면 전체) |
| 버튼 크기 | 109 × 63 (마스터 안) · 120 × 63 (컴포넌트셋) |
| 격자 | 4행 × 3열, **간격 0** |
| 좌우 여백 | `Spacing/400` (16) |
| 영역 간격 | `Spacing/400` (16) |
| 누름 배경 | `Color/Gray_900` + `Corner radius/400` (16) |
| 숫자 | `t500_23_bold` + `Color/Gray_100` |
| 기능 라벨 | `b200_16_regular` + `Color/Gray_100` |
| 배경 | `Color/Gray_White` |

---

## Usage

| 항목 | 값 |
| --- | --- |
| 섹션 | [Usage `11577:275`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11577-275) · 960×870 |
| 구성 | 2패턴 · 각 슬롯 360×536 · Keypad 본체 360×416 |
| 템플릿 | Usage `11237:46733` · ❖System Components |

Section 1의 금 판매 수량 입력 화면에서 필요한 입력 영역과 Keypad만 재사용합니다. Header와 금 시세 정보는 제외합니다. 수집된 두 화면은 다른 입력 유형이 아니라 같은 흐름의 입력 전·입력 중 상태입니다.

| 예제 | Node | 설명 | 표시·상태 |
| --- | --- | --- | --- |
| A. 입력 전 | `11577:276` | 입력 전에는 입력할 내용을 안내하고 보유 수량을 함께 보여줘요. 숫자 키나 빠른 입력으로 값을 입력하기 전에는 다음 버튼을 비활성화해요. | 「몇 금을 판매할까요?」 · 1,100금 보유 중 · 다음 비활성 |
| B. 수량 입력 | `11577:356` | 입력한 수량을 단위와 함께 보여줘요. 입력값이 조건을 만족하면 다음 버튼을 활성화해요. 빠른 입력과 삭제를 사용한 뒤에도 표시 값과 버튼 상태를 함께 갱신해요. | 1,000금 입력 · 보유량 1,100금 안내 · 다음 활성 |

두 예제 모두 CTA=true이며, 내부 Button의 Disabled를 각각 True/False로 설정합니다. **CTA의 노출 여부와 버튼 활성 여부는 서로 다른 설정**입니다. 일반 입력 화면에서는 모든 숫자 키를 Default로 두며, 마지막 누른 키의 Hover를 유지하지 않습니다.

### 현재 배치

| 항목 | 값 | 범위 |
| --- | --- | --- |
| 설명 영역–슬롯 | 50 | 문서 템플릿 |
| 예제 슬롯 | 360×536 | 입력 안내 + Keypad를 담은 문서 영역 |
| Keypad | 360×416 | CTA가 보이는 현재 본체 |
| 빠른 입력 | +1,000금 · +10,000금 · 모두 | 해당 화면의 샘플 · 고정 공통값 아님 |
| 정상 입력 예시 | 입력 1,000금 / 보유 1,100금 | 설명용 수량 |

Section 1 원본의 입력 중 사례는 12,000금 입력 / 1,100금 보유인데 다음이 활성화된 상태였습니다. 정상 입력 예제에서는 혼동을 줄이기 위해 입력값을 1,000금으로 정리했습니다. Section 1 원본은 변경하지 않았으며, 해당 원본을 보유량 초과가 허용되는 정책의 근거로 해석하지 않습니다.

---

## Guidelines

[Guidelines `11577:274`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11577-274) · 960×1415 · 4항목

Guidelines 템플릿 `11237:44468`의 좌우 슬롯으로 상태와 동작을 비교합니다. 모두 허용된 상태·기능이며 Do / Don’t 형식이 아닙니다. 설명 영역과 슬롯의 간격은 50입니다.

### 1. 입력값과 다음 버튼의 상태를 함께 맞춰요

**Node** `11577:442`

입력 전에는 안내 문구와 보유 수량을 보여주고 다음 버튼을 비활성화해요.
입력 후에는 수량과 단위를 표시하고, 보유 수량 등 화면의 입력 조건을 만족할 때만 다음 버튼을 활성화해요.

| 왼쪽 | 오른쪽 |
| --- | --- |
| 입력 전 · 다음 비활성 | 유효한 입력 · 다음 활성 |
| Button Disabled=True | Button Disabled=False |

현재 가이드의 슬롯은 높이 76의 Bottom CTA 비교입니다. 입력 안내·수량까지 포함한 전체 조합은 Usage A·B에서 설명합니다. 가이드에 입력 영역 전체가 있다고 가정하지 않습니다.

입력값이 존재하는 것만으로 유효한 입력은 아닙니다. 보유 수량 등 해당 화면에서 정의된 조건을 확인합니다. 최소 수량·상한·단위 같은 상세 정책 수치를 이 문서에서 임의로 새로 정의하지 않습니다.

### 2. 직접 입력과 빠른 입력을 함께 제공해요

**Node** `11577:642`

숫자 키로 수량을 직접 입력하거나 상단 Chip으로 정해진 수량을 빠르게 입력할 수 있어요.
추가 수량과 모두의 기준은 해당 화면의 단위·보유 수량에 맞추고, 입력 후 값과 다음 버튼의 상태를 갱신해요.

| 왼쪽 | 오른쪽 |
| --- | --- |
| 숫자 키 · 직접 입력 | Chip · 빠른 입력 |
| Num 키 대표 사례 | +1,000금 · +10,000금 · 모두 |

Chip은 빠른 입력을 돕는 동작이며 숫자 키 입력과 동일한 값·조건 검증을 따릅니다. 제품에서 단위가 원 등으로 달라지면 Chip 문구와 입력값 단위를 함께 맞춥니다. 초과 시 제한·오류 표현 같은 세부 처리는 해당 화면 정책을 따릅니다.

### 3. 전체 삭제와 한 글자 삭제를 구분해요

**Node** `11577:706`

전체삭제는 입력한 값을 모두 지우고, 삭제 아이콘은 마지막 숫자 한 자리를 지워요.
값을 모두 지우면 입력 전 안내와 다음 버튼의 비활성 상태로 돌아가요.

| 왼쪽 | 오른쪽 |
| --- | --- |
| 전체삭제 · 입력값 초기화 | 삭제 아이콘 · 한 자리 삭제 |
| Kind=Text | Kind=Icon |

삭제 후에는 숫자 표시뿐 아니라 단위·입력 안내·CTA 상태도 현재 값에 맞게 갱신합니다. 서로 다른 두 기능을 같은 동작으로 구현하지 않습니다.

### 4. 키를 누르면 상태 변화를 보여줘요

**Node** `11578:426`

기본 상태는 Default, 키를 누르는 동안은 Hover를 사용해 입력 반응을 보여줘요.
입력 후에는 Default로 돌아가며, 마지막으로 누른 키에 상태를 유지하지 않아요.

| 왼쪽 | 오른쪽 |
| --- | --- |
| Default · 기본 상태 | Hover · 누르는 동안 |
| 같은 숫자 6 · 배경 없음 | 같은 숫자 6 · 회색 라운드 배경 |

두 키 모두 Num이며 대표 크기 120×63으로 비교합니다. **현재 Figma의 실제 속성값은 States=Hover**이지만 이 모바일 가이드에서는 누르는 동안의 피드백을 뜻합니다. 마우스가 올라간 상태나 입력 후 유지하는 선택 상태로 해석하지 않습니다. 구현에서 pressed/active에 대응시키되 Figma 속성명을 임의로 변경하지 않습니다.

Hover는 Num·Icon·Text 모두에 존재합니다. 비교 예제는 숫자 6 한 쌍으로 보여주며, 별도 Usage를 추가하지 않습니다.

---

## AI 도구 적용 기준

1. Keypad 본체와 기존 Chip·Bottom CTA를 재사용합니다. 숫자·삭제 키의 4행×3열 배열과 좌우 여백을 임의로 다시 구성하지 않습니다.
2. 직접 입력·Chip·삭제는 같은 입력값을 변경합니다. 표시 수량·단위·보유량 안내·CTA 상태를 함께 갱신합니다.
3. CTA 노출은 Keypad의 BOOLEAN `CTA#8705:0`, 버튼 활성은 내부 Button의 VARIANT Disabled로 구분합니다. Disabled는 문자열 True/False입니다.
4. 내부 키 버튼은 VARIANT `States`와 `Kind`를 사용합니다. States는 Default/Hover, Kind는 Num/Icon/Text이며 이름을 임의로 Pressed 등으로 바꿔 호출하지 않습니다.
5. Hover는 누르는 동안만 사용합니다. 입력 후 Default로 돌아가고 마지막 키를 선택된 것처럼 남겨 두지 않습니다.
6. 유효성은 해당 화면 정책을 따릅니다. 이 예제의 1,000금·1,100금·빠른 입력 값은 정책의 고정 상수나 새로운 상한·하한이 아닙니다.
7. 컴포넌트셋 키 폭 120과 실제 Keypad 내부 폭 약 109.33을 구분합니다. 실제 폭은 (화면 폭−좌우 16×2)÷3으로 배분하며 대표 크기 120을 세 열에 강제 적용하지 않습니다.
8. 문서 슬롯 높이 536은 입력 안내까지 포함한 설명용 영역입니다. Keypad 본체 높이 416이나 제품 전체 화면 높이와 구분합니다.
9. 이 문서는 금액·수량의 숫자 입력 사례를 설명합니다. 문자 키보드나 비밀번호·인증번호·보안 키패드 동작까지 제공된다고 확대 해석하지 않습니다.
10. MD 업데이트는 Figma 마스터·프로퍼티명·Section 1 원본을 변경하지 않습니다.

---

## 현재 확인 사항

2026-11-09 현재 Guidelines 4항목과 Usage 2패턴을 확인했습니다. 제품 파일 전체를 전수 조사한 통계는 아닙니다.

| 항목 | 확인 결과 |
| --- | --- |
| 컴포넌트 정의 | Keypad Component 1개 · 키 버튼 Component Set 1개 / 6 variants |
| 분류 | 금 판매 수량 입력의 입력 전·입력 중 상태 |
| Usage | A 입력 전 / B 수량 입력 · Keypad CTA=true |
| Guidelines | 입력·CTA 연동 / 직접·빠른 입력 / 삭제 구분 / Default·Hover |
| 정상 수량 | 문서 예제는 1,000금 입력 · 1,100금 보유 안내 |
| 원본 | Section 1은 유지 · 이번 작업에 아노테이션 삭제 요청은 없었음 |
| 이름 | States=Hover 유지 · 모바일 누름 피드백으로 설명 |

이전 2026-10-12 문서의 전체 노드·인스턴스·미바인딩 건수와 정리 우선순위는 최신 문서 추가 이후 현황으로 재검증하지 않아 현황 표에서 제외했습니다. 구성 표의 과거 인스턴스 집계는 별도로 표시했습니다.

Default의 숨겨진 테두리나 기존 효과·토큰을 이 문서 업데이트만으로 정리하지 않습니다. Chip과 Bottom CTA를 재사용하므로 해당 컴포넌트가 변경되면 Keypad의 빠른 입력·CTA도 함께 확인합니다.
