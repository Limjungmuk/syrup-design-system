# Syrup Design System — Bottom Info 컴포넌트

> 이름 확인 (2026-11-11): `🟧`로 시작하는 컴포넌트·컴포넌트 세트는 없어요. 아래 구 에셋명과 접두사 건수는 과거 점검 기록이며, 일부 그룹·프레임·벡터·인스턴스 레이어에는 해당 이름이 남아 있어요. 하위 레이어명을 현재 라이브러리 컴포넌트 이름으로 사용하지 않아요.


| 항목 | 값 |
| --- | --- |
| Figma File | [Syrup_Design-System](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System) |
| Page / Section | `Bottom Info` 페이지 → [Bottom Info 섹션 `8519:5708`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=8519-5708) |
| 섹션 구성 | `Bottom Info` 1440×1965 → `Guidelines` 960×3970 → `Usage` 3760×736 (가로 일렬) |
| 기준일 | 2026-11-05 (Guidelines 7규칙으로 확장 / Usage · Guidelines 신설: 2026-11-04 / 스펙 정리: 2026-09-21) / 2026-11-11 내부 하단 패딩 적용 위치 보완 |
| 관련 문서 | [syrup-design-tokens.md](syrup-design-tokens.md) · [syrup-dialog-components.md](syrup-dialog-components.md) · [syrup-alert-components.md](syrup-alert-components.md) · [syrup-badge-components.md](syrup-badge-components.md) · [syrup-banner-components.md](syrup-banner-components.md) · [syrup-border-components.md](syrup-border-components.md) · [syrup-ad-components.md](syrup-ad-components.md) · [syrup-bottom-cta-components.md](syrup-bottom-cta-components.md) · [syrup-bottom-sheet-components.md](syrup-bottom-sheet-components.md) · [syrup-bubble-components.md](syrup-bubble-components.md) · [syrup-button-components.md](syrup-button-components.md) · [syrup-checkbox-components.md](syrup-checkbox-components.md) · [syrup-chip-components.md](syrup-chip-components.md) · [syrup-card-components.md](syrup-card-components.md) · [syrup-dim-components.md](syrup-dim-components.md) · [syrup-grid-list-components.md](syrup-grid-list-components.md) · [syrup-grid-scroll-components.md](syrup-grid-scroll-components.md) · [syrup-header-components.md](syrup-header-components.md) · [syrup-icon-button-components.md](syrup-icon-button-components.md) · [syrup-indicator-components.md](syrup-indicator-components.md) · [syrup-keypad-components.md](syrup-keypad-components.md) · [syrup-label-components.md](syrup-label-components.md) · [syrup-list-footer-components.md](syrup-list-footer-components.md) · [syrup-list-header-components.md](syrup-list-header-components.md) · [syrup-list-row-components.md](syrup-list-row-components.md) · [syrup-loader-components.md](syrup-loader-components.md) · [syrup-lottie-components.md](syrup-lottie-components.md) · [syrup-product-grid-components.md](syrup-product-grid-components.md) · [syrup-product-list-components.md](syrup-product-list-components.md) · [syrup-product-scroll-components.md](syrup-product-scroll-components.md) · [syrup-progress-stepper-components.md](syrup-progress-stepper-components.md) · [syrup-result-components.md](syrup-result-components.md) · [syrup-search-field-components.md](syrup-search-field-components.md) · [syrup-stepper-components.md](syrup-stepper-components.md) · [syrup-swipe-components.md](syrup-swipe-components.md) · [syrup-switch-components.md](syrup-switch-components.md) · [syrup-tab-components.md](syrup-tab-components.md) · [syrup-tab-bar-components.md](syrup-tab-bar-components.md) · [syrup-text-button-components.md](syrup-text-button-components.md) · [syrup-text-field-components.md](syrup-text-field-components.md) · [syrup-ticker-components.md](syrup-ticker-components.md) · [syrup-toast-components.md](syrup-toast-components.md) |

> **화면 하단에 안내나 설명을 표시하는 정보 영역이에요.**
> 안내해야 하는 긴 내용을 화면 하단에서 보여줄 때 사용해요.

---

## 공개 에셋 이름 정리

2026-11-11 아래 원본의 `.primitive / ` 접두사만 제거했어요. 노드·컴포넌트 키·variant·인스턴스 연결은 유지했으며 게시 작업은 별도로 진행해요. 숨김 유지·검토 대상의 접두사는 유지해요.

| 현재 전체 이름 | 원본 노드 |
| --- | --- |
| `Bottom Info / List` | `8529:19478` |

## 목차

1. [구성 한눈에 보기](#구성-한눈에-보기)
2. [간격 규칙](#간격-규칙)
3. [Bottom Info — Master Component](#1-bottom-info--master-component)
4. [List Item](#2-list-item)
5. [Dot](#3-dot)
6. [설계 규칙 요약](#설계-규칙-요약)
7. [Usage](#usage)
8. [Guidelines](#guidelines)
9. [점검 필요 사항](#점검-필요-사항)

---

## 구성 한눈에 보기

페이지는 **Master Component → Child Item → List Item** 세 단계로 구성되어 있습니다.

| # | 이름 | 타입 | Variant 축 | 크기 |
| --- | --- | --- | --- | --- |
| 1 | `Bottom Info` | Component Set | `Padding` 2종 | 360 × 314~414 |
| 2 | `Bottom Info / List` | Component Set | `Property 1` 3종 | 312 × 18~22 · 68 × 18 |
| 3 | `.primitive / Bottom Info / Dot` | Component | — | 3 × 11 |

---

## 간격 규칙

보드에 가이드 문구가 직접 적혀 있습니다.

> 제목과 설명은 하나의 정보 그룹으로 간주하며, 그룹 내부 요소 간 간격은 8을 적용합니다.
> 정보 그룹 간 간격은 20을 적용합니다.

| 층위 | 간격 | 토큰 |
| --- | --- | --- |
| 정보 그룹 **내부** (제목 ↔ 설명, Dot ↔ 텍스트) | 8 | `Spacing/200` |
| 정보 그룹 **사이** | 20 | `Spacing/500` |
| 섹션 제목 ↔ 본문 묶음 | 16 | `Spacing/400` |

실제 컴포넌트 구조가 이 규칙과 일치하는 것을 확인했습니다.

---

## 1. Bottom Info — Master Component

**Node** `8547:19164` · Component Set · 2 variants

### Properties

| Property | Type | Default | 역할 |
| --- | --- | --- | --- |
| `Padding` | VARIANT | `True` | 배경·여백 포함 여부 |
| `Title` | BOOLEAN | `true` | 상단 제목 노출 |
| `List` | SLOT | — | `Padding=True`의 본문 슬롯 |
| `List2` | SLOT | — | `Padding=False`의 본문 슬롯 |

### Variants

| Variant | 크기 | Padding (T/R/B/L) | Gap | 배경 |
| --- | --- | --- | --- | --- |
| `Padding=True` | 360 × 414 | `Spacing/600`(24) / `Spacing/600`(24) / **`Spacing/1000`(40)** / `Spacing/600`(24) | `Spacing/400` (16) | `Color/Gray_950` |
| `Padding=False` | 360 × 314 | 0 | `Spacing/400` (16) | 없음 |

- 하단 패딩만 **40**으로 다른 면(24)보다 큽니다. 화면 최하단 안전 영역을 확보하려는 의도로 보입니다.
- `Padding=False`는 배경과 여백 없이 폭 360을 그대로 씁니다. 이미 여백이 있는 컨테이너 안에 넣을 때 쓰는 변형입니다.

### 내부 구조 (`Padding=True` 기준)

| 영역 | 크기 | Padding | Gap | 비고 |
| --- | --- | --- | --- | --- |
| 루트 | 360 × 414 | 24 / 24 / 40 / 24 | `Spacing/400` (16) | VERTICAL · `Color/Gray_950` |
| `List` (Title variant) | 312 × 22 | 0 | `Spacing/200` (8) | 제목 "알려드려요!" |
| `List` **SLOT** | 312 × 312 | 0 | `Spacing/500` (20) | 정보 그룹 컨테이너 |
| └ 정보 그룹 | 312 × n | 0 | `Spacing/200` (8) | Dot + 텍스트 묶음 (HORIZONTAL) |
| &nbsp;&nbsp;&nbsp;└ 텍스트 묶음 | 301 × n | 0 | `Spacing/200` (8) | VERTICAL |

슬롯 안에 `List` 프레임을 중첩해 **정보 그룹 → 줄** 두 단계로 쌓는 구조입니다.

---

## 2. List Item

**Node** `8529:19478` · Component Set · 3 variants

### Properties

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `Property 1` | VARIANT | `Title` | `Title` · `Text` · `Link` |
| `Dot` | BOOLEAN | `true` | 불릿 노출 |

### Variants

| Variant | 크기 | 구성 | 타이포 | 색상 | 텍스트 폭 |
| --- | --- | --- | --- | --- | --- |
| `Property 1=Title` | 312 × 22 | `title` | `t800_17_bold` | `Color/Gray_200` (#464646) | HUG |
| `Property 1=Text` | 312 × 18 | `Dot` + `text` | `b500_13_regular` | `Color/Gray_400` (#777777) | FILL |
| `Property 1=Link` | 68 × 18 | `Text Button` | — | — | — |

- 세 variant 모두 HORIZONTAL · gap `Spacing/200` (8).
- `Link` variant만 **좌측 패딩 11**이 붙어 있습니다. Dot 폭(3) + gap(8) = 11로, 본문 텍스트의 좌측 시작선에 맞추기 위한 값입니다.
- 샘플 문구: 제목 "알려드려요!", 본문 "새로운 미션에 도전하고 싶다면, 미션을 다시 눌…"

---

## 3. Dot

**Node** `8547:19133` · Component · **3 × 11**

| 항목 | 값 |
| --- | --- |
| 불릿 | `Ellipse 33` 3 × 3 · `Color/Gray_400` |
| 상단 패딩 | `Spacing/200` (8) |
| Gap | `Spacing/250` (10) |

높이 11에 3px 원을 상단 패딩 8로 밀어 넣어, 첫 줄 텍스트의 시각 중심에 맞춥니다.

---

## 설계 규칙 요약

| 항목 | 값 |
| --- | --- |
| 폭 | 360 (Padding=True는 내부 콘텐츠 312) |
| 배경 | `Color/Gray_950` (#F6F6F7) — `Padding=True`만 |
| 여백 | 상·좌·우 24 / 하 40 |
| 제목 | `t800_17_bold` / `Color/Gray_200` |
| 본문 | `b500_13_regular` / `Color/Gray_400` |
| 불릿 | 3 × 3 원 / `Color/Gray_400` |
| 그룹 내부 간격 | `Spacing/200` (8) |
| 그룹 간 간격 | `Spacing/500` (20) |
| 제목 ↔ 본문 | `Spacing/400` (16) |

---

## Usage

| 항목 | 값 |
| --- | --- |
| 섹션 | [`Usage` `11343:1337`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11343-1337) · 3760 × 736 |
| 구성 | 9패턴 · 폭 360 · 높이는 내용에 맞춰 306~536 |
| 템플릿 | `Usage` 컴포넌트 [`11237:46733`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11237-46733) (`❖System Components` 페이지) |

> **컷은 화면 캡처가 아니라 실제 컴포넌트 인스턴스입니다.**
> 해당 컴포넌트와 **꼭 필요한 맥락 요소만** 남기고 나머지 화면 요소는 모두 지웠습니다. 남은 요소도 잘라낸 그림이 아니라 마스터를 직접 참조하는 인스턴스라, 컴포넌트 디자인이 바뀌면 문서가 함께 바뀝니다 (2026-11-04).

패턴 하나가 `Usage` 템플릿 인스턴스 하나입니다. 템플릿은 `Title`(제목 + 설명)과 `Component` **슬롯**으로 이루어져 있고, 슬롯 안에 그 패턴을 보여 줄 인스턴스를 넣습니다. 가로 간격은 40입니다.

Bottom Info는 **variant가 `Padding` 하나뿐**이라, 실제로 달라지는 것은 거의 전부 **슬롯 안을 어떻게 쌓느냐**와 **무엇과 함께 놓이느냐**입니다. 아홉 패턴을 세 묶음으로 나눴습니다.

| 묶음 | 패턴 | 무엇이 달라지는가 |
| --- | --- | --- |
| **슬롯 구성** | A · B · C · D · E | 슬롯 안의 층위와 요소 |
| **컴포넌트 변형** | F · G | `Title` · `Padding` 값과 배경색 |
| **함께 놓이는 요소** | H · I | 아래에 떠 있는 요소와 그에 맞춘 하단 여백 |

### 슬롯 구성 — A · B · C · D · E

| | 패턴 | 설명 | 슬롯에 담은 것 | 슬롯 높이 |
| --- | --- | --- | --- | --- |
| **A** | 단순 나열 | 안내할 항목이 같은 수준의 정보일 때 사용해요. 각 항목 앞에 점을 표시하고, 항목 사이는 8 간격을 둬요. | 정보 그룹 3개 · 각 1줄 · 그룹 간 **8** | 190 |
| **B** | 소제목으로 묶기 | 안내할 내용이 여러 주제로 나뉠 때 사용해요. 소제목에는 점을 표시하지 않고, 묶음 사이는 20 간격을 둬요. | 소제목 묶음 2개 · 그룹 간 **20** | 254 |
| **C** | 한 단계 더 들여쓰기 | 묶음 안에서 하위 항목을 구분할 때 사용해요. 한 단계마다 11씩 들여쓰고, 본문 너비도 그만큼 줄여요. | 소제목 묶음 안에 소제목 묶음 (3단) | 224 |
| **D** | 링크 넣기 | 관련 화면으로 이동할 수 있도록 Link를 사용해요. 특정 주제의 링크는 해당 묶음 안에, 안내 전체에 관한 링크는 묶음 밖에 배치해요. | 묶음 안 `Link` 1개 + 슬롯 직계 `Link` 1개 | 210 |
| **E** | 소제목 강조하기 | 소제목과 본문을 더 명확하게 구분할 때 소제목에 Bold를 적용할 수 있어요. 같은 수준의 소제목은 굵기를 통일해요. | 소제목 묶음 5개 · 소제목만 **Bold** | 420 |

**D의 두 자리는 실제로 쓰임이 갈립니다.** 묶음 안의 `Link`는 그 주제에 딸린 바로가기이고, 슬롯에 바로 넣은 `Link`는 안내 전체에 걸립니다. 수집 예제에서도 묶음 안 4건 · 슬롯 직계 1건으로 둘 다 나옵니다.

### 컴포넌트 변형 — F · G

| | 패턴 | 설명 | 슬롯에 담은 것 | 슬롯 높이 |
| --- | --- | --- | --- | --- |
| **F** | 제목과 여백 없이 쓰기 | 이미 여백이 있는 콘텐츠에 이어 붙일 때 사용해요. Title=False로 제목을 숨기고, Padding=False로 여백을 제거해 안내 본문만 배치해요. | `List Header` + `Text Field / Text Area` + `Padding=False` | 256 |
| **G** | 흰 배경으로 쓰기 | 상단 영역에 배경색이 있을 때 사용해요. Bottom Info에 흰 배경을 적용해 상단 콘텐츠와 안내 영역을 명확하게 구분할 수 있어요. | `상단 콘텐츠 (배경색 있음)` 블록(360 × 72) + 흰 배경 `Bottom Info` | 262 |

**F와 G는 맥락이 있어야 이유가 보입니다.** F는 「이미 여백이 있는 콘텐츠」가, G는 「배경색이 있는 상단 영역」이 전제라서, 그것 없이 컴포넌트만 두면 왜 그렇게 쓰는지가 드러나지 않습니다.

- **F** — 소감 입력 화면을 그대로 세웠습니다. `List Header`(「당첨 소감을 들려주세요!」)와 `Text Field / Text Area` 아래에 안내 본문만 이어 붙입니다.
- **G** — 상단 블록은 컴포넌트가 아니라 「배경색이 있는 영역」을 대신하는 프레임이고, 색 `#F1F6FF`는 **`Color/Third_Pastel_Blue`** 에 바인딩되어 있습니다. Bottom Info 쪽 흰 배경은 `Color/Gray_White`입니다.

### 함께 놓이는 요소 — H · I

| | 패턴 | 설명 | 슬롯에 담은 것 | 슬롯 높이 |
| --- | --- | --- | --- | --- |
| **H** | 닫을 수 있는 ETMS와 함께 쓰기 | 닫기 버튼이 있는 ETMS도 안내 본문을 가리지 않도록 하단 여백을 확보해요. 닫은 뒤에는 기본 패딩으로 돌아가거나 여백을 유지할 수 있어요. | `Bottom Info`(하단 여백 **120**) + `ETMS`·`Type=Gold` (142 × 140) | 306 |
| **I** | 복수 플로팅과 함께 쓰기 | 여러 플로팅 요소를 함께 사용할 때는 마지막 글줄과 각 요소의 크기·위치를 고려해 하단 영역을 조정해요. 본문과 플로팅 요소가 가려지거나 서로 겹치지 않도록 배치해요. | `Bottom Info`(하단 여백 **160**) + `ETMS`·`Type=Egg` (108 × 108) + `btn_timer` (194 × 40) | 346 |

예제 H·I의 하단 여백 120·160은 Bottom Info 자체의 `paddingBottom`이에요. 스크롤 콘텐츠 바깥에 빈 영역을 추가한 값이 아니며, 모든 화면의 고정 여백으로 사용하지 않아요.

**플로팅은 종류마다 크기도 자리도 다릅니다.** H의 금괴는 `syrup_ico_40_floating_close_enabled_gray_400`(40 × 40) 닫기 버튼을 달고 오른쪽 아래에 혼자 떠 있고, I는 황금알과 타이머 버튼 두 개가 세로로 쌓입니다. 그래서 하단 여백이 숫자 하나로 정해지지 않습니다 — 같은 안내인데 H는 120, I는 160입니다.

**H의 닫기 버튼이 별도 규칙이 된 이유가 있습니다.** 금괴는 닫을 수 있어서 「닫기 전」과 「닫은 뒤」 두 상태를 갖는데, 닫기 버튼이 본문 위에 올라앉으면 글자와 겹쳐 읽히지 않습니다 → [Guidelines 3](#3-닫기-버튼이-있어도-본문을-가리지-않아요). I는 닫을 수 없는 요소가 둘이라 크기와 자리를 함께 따져야 합니다 → [Guidelines 2](#2-플로팅-요소에-맞춰-하단-영역을-조정할-수-있어요)

### 슬롯은 두 가지 모양으로만 쌓입니다

실측해 보니 슬롯 안의 정보 그룹은 둘 중 하나입니다.

| 모양 | 구조 | 쓰임 |
| --- | --- | --- |
| **평면형** | `List` 세로 프레임(간격 8) → `Text` 줄들 | 같은 수준의 항목을 나열 |
| **소제목형** | `List` 가로 프레임(간격 8) → [`Dot`, `List` 세로 프레임] | 소제목 아래로 항목들을 묶음 |

**소제목은 별도 variant가 아닙니다.** `Property 1=Title`은 맨 위 「알려드려요!」 한 줄에만 쓰이고, 묶음의 소제목은 **`Property 1=Text`에서 `Dot`만 끈 것**입니다. 점은 바깥 묶음의 `Dot` 컴포넌트가 대신 찍습니다. **E의 Bold도 variant가 아니라 그 텍스트의 굵기를 직접 바꾼 것**입니다 → [점검 9](#9--소제목에-텍스트-스타일-적용-2026-11-05-완료)

들여쓰기는 **소제목형을 중첩**해서 만듭니다. 한 단계 들어갈 때마다 `Dot` 너비 3 + 간격 8 = **11**씩 밀립니다.

| 단계 | 왼쪽 들여쓰기 | 본문 너비 |
| --- | --- | --- |
| 1단 | 0 | 312 |
| 2단 | 11 | 301 |
| 3단 | 22 | 290 |

제품 파일에서 **3단까지 확인**됩니다. 4단은 없습니다.

### 수집 예제 실측 (2026-11-04)

Figma `Section 1`(`11332:57601`)에 모아 두었던 **15개 예제**를 전수 조사한 결과입니다. 그 섹션은 문서화를 마친 뒤 2026-11-05에 정리되었고, 여기 남은 수치가 유일한 기록입니다 → [점검 8](#8--수집-예제-정리-2026-11-05-완료)

| 항목 | 값 | 건수 |
| --- | --- | --- |
| `Padding` | `True` | 13 |
| | `False` | **2** |
| 배경 | `Color/Gray_950` | 12 |
| | **흰색** | **1** |
| | 없음 (`Padding=False`) | 2 |
| 슬롯 간격 | `20` | 9 |
| | `8` | **6** |
| 가장 깊은 단계 | 1단 (평면만) | 6 |
| | 2단 (소제목) | 6 |
| | **3단** | **3** |
| `Link` 사용 | 묶음 안 | 4 |
| | 슬롯 직계 | 1 |

**슬롯 간격이 8과 20으로 갈리는 데에는 규칙이 있습니다.** 소제목 묶음이 하나라도 있으면 20, 모든 항목이 같은 수준이면 8입니다. 15건 중 14건이 이 규칙을 따릅니다 — 예외는 소제목 묶음이 있는데 8을 쓴 1건뿐입니다 → [점검 6](#6-슬롯-간격-8과-20이-섞여-있습니다)

보드에 적힌 「정보 그룹 간 간격은 20」은 **소제목으로 묶었을 때의 값**이고, 단순 나열에서는 항목 간격과 같은 8을 씁니다. 지금 보드 문구만 보면 이 구분이 드러나지 않습니다.

---

## Guidelines

지켜지지 않으면 결과가 깨지는 것만 올렸습니다. 각 항목은 Figma **[`Guidelines` 섹션 `11343:1336`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11343-1336)** (960 × 3970) 에 한 쌍씩 들어 있습니다.

규칙 하나가 `Guidelines` 템플릿 인스턴스 [`11237:44468`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11237-44468) (`❖System Components` 페이지) 하나입니다. 폭 760, `Title`(제목 + 설명) 아래 `Image` 프레임에 슬롯이 좌우로 들어갑니다.

**2026-11-05에 여섯에서 일곱으로 늘었습니다.** 「닫기 버튼이 있어도 본문을 가리지 않아요」가 3번으로 들어오면서 뒤 네 항목의 번호가 하나씩 밀렸습니다.

| 번호 | 규칙 | 2026-11-04 기준 |
| --- | --- | --- |
| 1 | 하단 고정 버튼이 있으면 하단 여백을 확보해요 | 1 (제목·설명 수정) |
| 2 | 플로팅 요소에 맞춰 하단 영역을 조정할 수 있어요 | 2 (두 경우 비교 → **Do / Don't**) |
| **3** | **닫기 버튼이 있어도 본문을 가리지 않아요** | **신설** |
| 4 | 콘텐츠에 이어 붙일 때는 제목과 여백을 없애요 | 3 |
| 5 | 상단 영역과 구분할 때는 흰 배경을 사용할 수 있어요 | 4 |
| 6 | 소제목으로 나눈 묶음 사이는 20으로 띄워요 | 5 |
| 7 | 소제목을 강조해 정보 묶음을 구분할 수 있어요 | 6 |

**앞 세 규칙은 모두 「하단에 무엇이 떠 있는가」를 다룹니다.** 떠 있는 것이 고정 버튼인지, 닫을 수 없는 플로팅 요소 여럿인지, 닫기 버튼이 달린 ETMS인지에 따라 확보해야 하는 여백이 달라집니다.

| 규칙 | 아래에 떠 있는 것 | Do의 하단 여백 | Don't |
| --- | --- | --- | --- |
| **1** | `Bottom CTA` (360 × 112) | 120 | 같은 **120**인데 본문이 한 문단 더 김 |
| **2** | `ETMS`·Egg (108 × 108) + `btn_timer` (194 × 40) | **160** | **40** |
| **3** | `ETMS`·Gold (142 × 140, 닫기 버튼 포함) | **120** | **40** |

**여섯은 Do / Don't이고, 마지막 하나만 두 경우를 나란히 비교합니다.**

| 형식 | 규칙 | 슬롯 라벨 |
| --- | --- | --- |
| Do / Don't | 1 · 2 · 3 · 4 · 5 · 6 | `Do` · `Don’t` |
| 두 경우 비교 | **7** | 「기본」 · 「소제목 강조」 |

**규칙 2의 형식이 바뀐 데에는 이유가 있습니다.** 2026-11-04에는 「단일 플로팅」·「복수 플로팅」 두 경우를 비교했는데, 단일 플로팅이 3번으로 독립하면서 2번에 「여백이 모자라 요소가 본문을 가리는」 실패 사례가 생겼습니다. 둘 다 정상인 비교로 남은 것은 7번뿐입니다 — Badge 규칙 1, Banner 규칙 3과 같은 방식입니다.

**규칙 1 · 4 · 5는 Figma 아노테이션에서 왔습니다.** 수집 예제에 직접 달아 두었던 7개 메모를 주제별로 묶은 것으로, 메모 자체는 `Section 1`과 함께 정리되었습니다.

| 아노테이션 | 건수 | → 규칙 |
| --- | --- | --- |
| 「아래에 보톰CTA처럼 요소가 있는 경우 필요한만큼 하단 영역 확보」 외 3건 | 4 | 1 · 2 · 3 |
| 「컨텐츠와 하단에 쓰이는 경우 배경과 여백 없이 사용」 | 2 | 4 |
| 「상단 컨텐츠에서 배경색이 사용된 경우 … 화이트 배경 사용 가능」 | 1 | 5 |

6은 보드에 적힌 간격 규칙과 실측에서, 7은 수집 예제의 Bold 소제목에서 나왔습니다.

### 1. 하단 고정 버튼이 있으면 하단 여백을 확보해요

Bottom CTA처럼 화면 하단에 고정된 버튼이 있으면 본문이 가려지지 않도록 하단 여백을 확보해요.
스크롤을 끝까지 내렸을 때 마지막 글줄까지 읽을 수 있도록 배치해요.

| | 안내 문단 | 본문이 끝나는 높이 | 결과 |
| --- | --- | --- | --- |
| **Do** | 2문단 | 142 | `Bottom CTA`(150~262)와 겹치지 않음 |
| **Don't** | 3문단 | **186** | 마지막 문단이 `Bottom CTA`(152~264) 아래로 들어가 잘림 |

두 컷 모두 하단 여백은 **120으로 같고** `Bottom CTA`(360 × 112, `Top Gradient=true` · `Upper Item=false`)도 같은 자리입니다. 달라진 것은 안내 문단 수 하나입니다 — 같은 여백이라도 본문이 길어지면 모자랄 수 있다는 뜻입니다 → [점검 11](#11-규칙-1의-두-컷은-하단-여백이-같습니다)

### 2. 플로팅 요소에 맞춰 하단 영역을 조정할 수 있어요

플로팅 요소의 크기와 위치, 본문의 마지막 글줄을 고려해 하단 영역의 높이와 여백을 조정할 수 있어요.
여러 요소를 함께 사용할 때는 본문과 각 요소가 서로 가려지지 않도록 배치해요.

하단 고정·플로팅 요소를 피하기 위한 추가 여백은 Bottom Info 내부의 `paddingBottom`으로 확보해요. 바깥 스크롤 콘텐츠의 하단 패딩, 고정 높이 확대, 빈 프레임으로 대체하거나 여백을 중복 적용하지 않아요. Bottom Info의 높이는 내용과 패딩에 맞춰 늘어나고, 배경색이 추가 여백까지 이어지도록 해요. 필요한 여백은 마지막 글줄과 고정·플로팅 요소의 실제 위치를 기준으로 정해요.

| | 하단 여백 | 전체 높이 | 결과 |
| --- | --- | --- | --- |
| **Do** | **160** | 346 | 황금알과 타이머 버튼이 모두 본문 아래에 놓임 |
| **Don't** | **40** | 226 | 두 요소가 본문 위로 올라와 글줄을 가림 |

두 컷 모두 같은 안내에 `ETMS`·`Type=Egg`(108 × 108)와 `btn_timer`(194 × 40)를 같은 조합으로 띄웠고, **다른 것은 `paddingBottom` 하나**입니다.

**요소가 둘이라 「쌓인 높이」로 계산해야 합니다.** 황금알 아래에 타이머 버튼이 이어 붙어 108 + 40 = 148이 되고, 여기에 마지막 글줄과의 간격을 더해 160이 나옵니다.

### 3. 닫기 버튼이 있어도 본문을 가리지 않아요

ETMS가 표시된 상태에서도 안내 내용을 모두 읽을 수 있도록 하단 여백을 확보해요.
닫은 뒤에는 기본 패딩으로 돌아가거나, 화면의 안정적인 배치를 위해 확보한 여백을 유지할 수 있어요.

| | 하단 여백 | 전체 높이 | 결과 |
| --- | --- | --- | --- |
| **Do** | **120** | 306 | 금괴와 닫기 버튼이 본문 아래에 놓임 |
| **Don't** | **40** | 226 | 금괴가 본문 위로 올라오고 닫기 버튼이 글자 위에 겹침 |

두 컷 모두 같은 안내에 `ETMS`·`Type=Gold`(142 × 140)를 띄웠고, **다른 것은 `paddingBottom` 하나**입니다.

**닫기 버튼이 겹치면 두 가지가 한꺼번에 깨집니다.** 글자가 가려져 읽히지 않는 것이 하나고, 글자 위에 탭 영역이 올라앉아 본문을 누르려다 ETMS가 닫히는 것이 둘입니다. `syrup_ico_40_floating_close_enabled_gray_400`은 40 × 40이라 보이는 원(22 × 22)보다 탭 영역이 넓습니다.

**닫은 뒤의 여백은 둘 다 맞습니다.** 기본 패딩 40으로 돌아가도 되고, 화면이 흔들리지 않도록 확보한 120을 유지해도 됩니다. 설명의 두 번째 문장이 이 선택을 열어 둡니다.

### 4. 콘텐츠에 이어 붙일 때는 제목과 여백을 없애요

이미 여백이 있는 콘텐츠에 이어 붙일 때는 Title=False로 제목을 숨기고, Padding=False로 여백을 제거해요.
기존 콘텐츠의 흐름에 맞춰 안내 본문만 배치해요.

| | Variant | 결과 |
| --- | --- | --- |
| **Do** | `Padding=False` · `Title=False` | 본문이 콘텐츠의 좌우 여백에 맞음 (본문 너비 312) |
| **Don't** | `Padding=True` | 여백이 겹쳐 본문이 안쪽으로 밀리고(264), 회색 박스가 따로 떠 보임 |

**제목을 함께 숨기는 것이 규칙에 들어왔습니다.** 이어 붙이는 자리에서는 「알려드려요!」가 콘텐츠의 제목과 중복되기 때문입니다.

**밀리는 폭이 숫자로 보입니다.** 두 컷의 상단은 `List Header`(「당첨 소감을 들려주세요!」)와 `Text Field / Text Area`(312 × 100)로 같고, 둘 다 좌우 여백 24인 화면 안에 들어 있습니다. Do의 본문은 그 312를 그대로 쓰지만, Don't는 `Padding=True`의 좌우 24가 한 번 더 붙어 **264**로 줄어듭니다.

### 5. 상단 영역과 구분할 때는 흰 배경을 사용할 수 있어요

상단 영역에 배경색이 있는 경우 Bottom Info에 흰 배경을 사용할 수 있어요.
상단 영역과 안내 영역이 명확하게 구분되도록 배경색을 선택해요.

| | 배경 | 결과 |
| --- | --- | --- |
| **Do** | **`Color/Gray_White`** | 상단 영역과 경계가 보임 |
| **Don't** | `Color/Gray_950` | 배경색이 이어져 한 덩어리로 보임 |

두 컷 모두 위에 `상단 콘텐츠 (배경색 있음)` 블록(360 × 72 · **`Color/Third_Pastel_Blue`** #F1F6FF)을 두었고, **다른 것은 Bottom Info의 배경색 하나**입니다. 흰 배경은 2026-11-04에 **`Color/Gray_White`에 바인딩**했습니다 → [점검 7](#7--흰-배경-토큰-바인딩-2026-11-04-완료)

### 6. 소제목으로 나눈 묶음 사이는 20으로 띄워요

소제목으로 나눈 정보 묶음 사이에는 20 간격을 둬요.
묶음 안의 항목 간격인 8과 차이를 두어 각 묶음을 구분해요.

| | 슬롯 간격 | 슬롯 높이 | 전체 높이 | 결과 |
| --- | --- | --- | --- | --- |
| **Do** | **20** | 126 | 228 | 묶음의 경계가 보임 |
| **Don't** | **8** | 114 | 216 | 항목 간격과 같아 묶음이 구분되지 않음 |

**단순 나열에는 이 규칙이 적용되지 않습니다.** 모든 항목이 같은 수준이면 8이 맞습니다 (Usage **A**). 20은 **소제목으로 묶었을 때**의 값입니다.

### 7. 소제목을 강조해 정보 묶음을 구분할 수 있어요

소제목과 본문의 구분이 필요할 때는 소제목에 Bold를 적용할 수 있어요.
같은 수준의 소제목에는 동일한 굵기를 적용해요.

| 라벨 | 소제목 | 본문 | 슬롯 높이 |
| --- | --- | --- | --- |
| **기본** | Regular 13 (`b500_13_regular`) | Regular 13 (`b500_13_regular`) | 450 |
| **소제목 강조** | **Bold 13** (`t1060_13_bold`) | Regular 13 (`b500_13_regular`) | 450 |

두 컷 모두 같은 기프티콘 안내(유의 사항 · 사용 장소 · 발행자 · 고객센터 · 환불안내)이고, **다른 것은 소제목의 굵기 하나**입니다. 묶음이 다섯이라 슬롯 높이가 450으로 가장 큽니다.

「같은 수준의 소제목은 굵기를 통일한다」가 핵심입니다. 한 안내 안에서 어떤 소제목만 Bold면 수준이 다른 것처럼 읽힙니다.

양쪽 소제목 모두 2026-11-05에 **텍스트 스타일을 적용**했습니다 → [점검 9](#9--소제목에-텍스트-스타일-적용-2026-11-05-완료)

---

## 점검 필요 사항

### 1. ⚠️ 본문 텍스트의 명암비가 WCAG AA 미달

`Padding=True`의 배경 `Color/Gray_950`(#F6F6F7) 위에 본문 텍스트 `Color/Gray_400`(#777777)이 놓입니다.

| 항목 | 값 |
| --- | --- |
| 명암비 | **약 4.15 : 1** |
| WCAG AA 기준 (일반 텍스트) | 4.5 : 1 |

본문이 13px이라 "큰 텍스트" 예외(18pt / 14pt bold 이상)에도 해당하지 않습니다. `Color/Gray_300`(#666666)으로 한 단계 진하게 하면 약 5.3:1이 되어 기준을 넘습니다.

불릿(`Ellipse 33`)도 같은 `Color/Gray_400`이라 함께 검토가 필요합니다.

### 2. Padding variant마다 슬롯 이름이 다름

| Variant | 슬롯 이름 |
| --- | --- |
| `Padding=True` | `List` |
| `Padding=False` | `List2` |

Figma는 variant를 전환할 때 **레이어 이름으로 콘텐츠를 매칭**합니다. 슬롯 이름이 다르면 `Padding` 값을 바꿨을 때 슬롯에 넣어둔 내용이 승계되지 않을 수 있습니다. 두 슬롯을 같은 이름(`List`)으로 통일하는 편이 안전합니다.

### 3. `Link` variant의 좌측 패딩이 하드코딩

`Property 1=Link`의 `paddingLeft`가 **11**이며 토큰에 바인딩되어 있지 않습니다. Spacing 스케일에 11은 없습니다.

이 값은 `Dot 폭(3) + gap(8)`의 합이라 본문과 좌측을 맞추기 위한 계산값입니다. Dot을 숨긴 채(`Dot=false`) 같은 구조를 유지하면 하드코딩 없이 자동으로 정렬을 맞출 수 있습니다.

파일 내 3곳(컴포넌트 원본 1 + 슬롯에 배치된 인스턴스 2)에서 발견됩니다.

### 4. `Dot` 프로퍼티가 일부 variant에서 무의미

`Dot` BOOLEAN의 기본값이 `true`지만, `Property 1=Title`과 `Link` variant에는 Dot 레이어 자체가 없습니다. 프로퍼티 패널에는 계속 노출되므로 사용자가 혼동할 수 있습니다.

같은 맥락으로 `Dot` 컴포넌트의 `itemSpacing`(`Spacing/250` = 10)도 자식이 `Ellipse` 하나뿐이라 실제로는 아무 효과가 없습니다.

### 5. 토큰 상태

| 항목 | 결과 |
| --- | --- |
| 미바인딩 radius · gap | **0건** |
| 미바인딩 padding | `11` 3건 (위 3번) · `100` 4건 · `460` 2건 |
| 스타일 미적용 / 원격 스타일 텍스트 | **0건** |
| 외부 토큰 | `Spec docs/margin` 4 · `Spec docs/width` 1 · paragraph 계열 3 |

`100`(4건)과 `460`(2건)은 컴포넌트가 아니라 **문서 보드의 섹션 레이아웃 프레임**(`8529:19339`)에 붙은 값이라 정리 대상이 아닙니다.

컴포넌트 자체에서 남은 실제 정리 대상은 **`Link` variant의 패딩 11** 하나입니다.

### 6. 슬롯 간격 8과 20이 섞여 있습니다

보드에는 「정보 그룹 간 간격은 20」이라고만 적혀 있는데, 수집 예제 15건의 슬롯 간격은 **20이 9건, 8이 6건**입니다.

| 슬롯 내용 | 간격 | 건수 |
| --- | --- | --- |
| 소제목 묶음이 있음 | **20** | 9 |
| 모든 줄이 같은 층위 | **8** | 5 |
| 소제목 묶음이 있는데 8 | ⚠️ **8** | **1** |

**14건은 「소제목이 있으면 20, 단순 나열이면 8」로 일관**됩니다. 보드 문구가 이 구분을 담고 있지 않아, 읽는 사람은 단순 나열에도 20을 적용해야 하는 것으로 오해할 수 있습니다.

보드 문구를 「소제목으로 묶은 정보 그룹 사이는 20, 같은 층위의 줄 사이는 8」로 고쳐 두면 예외가 사라집니다. 어긋난 1건은 그에 맞춰 20으로 바꾸면 됩니다.

### 7. ✅ 흰 배경 토큰 바인딩 (2026-11-04 완료)

흰 배경을 쓰는 두 인스턴스(Usage **G** · Guidelines **4**의 Do)가 `#FFFFFF`를 직접 지정하고 있어 **`Color/Gray_White`에 바인딩**했습니다. 값이 같아 무손실이고 렌더링은 그대로입니다.

| 대상 | 전 | 후 |
| --- | --- | --- |
| Usage G의 `Bottom Info` | `#FFFFFF` 직접 지정 | **`Color/Gray_White`** |
| Guidelines 4 Do의 `Bottom Info` | `#FFFFFF` 직접 지정 | **`Color/Gray_White`** |

이제 두 섹션의 `Bottom Info` 인스턴스 **21개가 모두 토큰을 가리킵니다** — `Color/Gray_950` 19개, `Color/Gray_White` 2개, `Padding=False` 2개는 배경 없음.

**다만 배경이 여전히 `Padding` 축에 묶여 있습니다.** 배경만 바꾸려면 인스턴스에서 덮어써야 하고, 그때마다 바인딩을 손으로 걸어야 합니다. 쓰임이 늘면 `Background` 축을 따로 만드는 편이 낫습니다.

### 8. ✅ 수집 예제 정리 (2026-11-05 완료)

Usage · Guidelines를 만드는 데 쓴 원본 예제 15개가 담겨 있던 `Section 1`(`11332:57601` · 9253 × 3637)이 삭제되었습니다. 페이지는 이제 **`Bottom Info` · `Guidelines` · `Usage` 세 섹션**만 남았습니다.

아노테이션 7건도 함께 사라졌습니다. 메모의 내용은 Guidelines 1 · 4 · 5로, 실측 수치는 [수집 예제 실측](#수집-예제-실측-2026-11-04)으로 옮겨 두었으므로 문서에는 남아 있습니다.

### 9. ✅ 소제목에 텍스트 스타일 적용 (2026-11-05 완료)

Usage **E**와 Guidelines **7**의 소제목이 텍스트 스타일 없이 굵기만 지정된 상태였습니다. 값이 똑같은 스타일이 이미 있어 **양쪽 모두 적용**했습니다.

| 대상 | 폰트 | 크기 / 행간 / 자간 | 적용한 스타일 | 곳 |
| --- | --- | --- | --- | --- |
| **Bold 소제목** | Pretendard Bold | 13 / 18 / 0 | **`t1060_13_bold`** ✅ | Usage E 5 · Guidelines 7 「소제목 강조」 5 |
| **Regular 소제목** | Pretendard Regular | 13 / 18 / 0 | **`b500_13_regular`** ✅ | Guidelines 7 「기본」 5 |
| 본문 | Pretendard Regular | 13 / 18 / 0 | `b500_13_regular` (이미 적용) | — |

**15곳에 적용했고 값은 하나도 바뀌지 않았습니다.** 세 값이 모두 일치해 무손실이었고, 렌더링도 그대로입니다. `t1060_13_bold`는 [Badge](syrup-badge-components.md)의 `Size=M` 라벨이 쓰는 것과 같은 스타일입니다.

이제 타입 램프가 바뀌면 소제목도 함께 따라갑니다. 규칙 7의 「같은 수준의 소제목에는 동일한 굵기를 적용해요」를 손으로 지키지 않아도 됩니다.

**두 섹션에 스타일 없는 텍스트는 1건만 남았습니다** — Usage **I**의 `ETMS`·Egg 안에 있는 「황금알 모으기」(Bold 12)이고, Bottom Info가 아니라 그 에셋 쪽 건입니다.

### 10. 플로팅 에셋 안의 임시색

Usage **I**와 Guidelines **2**의 복수 플로팅 컷 안에 있는 `🟧syrup_img_shopping_badge_gold` 인스턴스(18 × 18)에 **`#00D9FF`** 가 fill로 들어 있습니다. **3곳** 모두 `visible=false`인 숨은 fill입니다.

[Badge 점검 7](syrup-badge-components.md#7--숨겨진-작업-흔적-제거-2026-10-08-완료)에서 정리한 것과 **같은 계열의 임시색**입니다. Bottom Info가 아니라 **그 에셋 쪽 건**이라 여기서 고칠 대상은 아니지만, 같은 흔적이 다른 에셋에도 남아 있다는 신호입니다. 해당 에셋을 쓰는 페이지에서 함께 확인하는 편이 좋습니다.

### 11. 규칙 1의 두 컷은 하단 여백이 같습니다

[Guidelines 1](#1-하단-고정-버튼이-있으면-하단-여백을-확보해요)의 Do와 Don't는 **둘 다 `paddingBottom`이 120**입니다. 달라진 것은 안내 문단 수(2 ↔ 3)뿐입니다.

| | 하단 여백 | 문단 | 본문이 끝나는 높이 | `Bottom CTA` 상단 |
| --- | --- | --- | --- | --- |
| **Do** | 120 | 2 | 142 | 150 |
| **Don't** | **120** | 3 | **186** | 152 |

화면에서는 의도대로 보입니다 — Don't의 마지막 문단이 `Bottom CTA` 아래로 들어가 잘립니다. 다만 **규칙 제목이 「여백을 확보해요」인데 두 컷의 여백이 같아서**, 수치로 비교하는 사람에게는 차이가 보이지 않습니다.

다른 규칙 2 · 3은 `paddingBottom` 하나만 다릅니다(160 ↔ 40, 120 ↔ 40). 규칙 1도 Don't의 여백을 기본값 40으로 낮추고 문단 수를 Do와 맞추면 세 규칙이 같은 방식으로 읽힙니다.
