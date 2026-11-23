# Syrup Design System — Dialog 컴포넌트

| 항목 | 값 |
| --- | --- |
| Figma File | [Syrup_Design-System](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System) |
| Page / Section | `Dialog` 페이지 → [Dialog 섹션 `8505:12329`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=8505-12329) |
| 섹션 구성 | `Dialog` 1440×5260 → `Guidelines` 960×3236 → `Usage` 4560×874 (가로 일렬) |
| 기준일 | 2026-11-06 (Usage · Guidelines 신설 / 스펙 정리: 2026-09-21) |
| 관련 문서 | [syrup-design-tokens.md](syrup-design-tokens.md) · [syrup-ad-components.md](syrup-ad-components.md) · [syrup-alert-components.md](syrup-alert-components.md) · [syrup-badge-components.md](syrup-badge-components.md) · [syrup-banner-components.md](syrup-banner-components.md) · [syrup-border-components.md](syrup-border-components.md) · [syrup-bottom-info-components.md](syrup-bottom-info-components.md) · [syrup-bottom-cta-components.md](syrup-bottom-cta-components.md) · [syrup-bottom-sheet-components.md](syrup-bottom-sheet-components.md) · [syrup-bubble-components.md](syrup-bubble-components.md) · [syrup-button-components.md](syrup-button-components.md) · [syrup-checkbox-components.md](syrup-checkbox-components.md) · [syrup-chip-components.md](syrup-chip-components.md) · [syrup-card-components.md](syrup-card-components.md) · [syrup-dim-components.md](syrup-dim-components.md) · [syrup-grid-list-components.md](syrup-grid-list-components.md) · [syrup-grid-scroll-components.md](syrup-grid-scroll-components.md) · [syrup-header-components.md](syrup-header-components.md) · [syrup-icon-button-components.md](syrup-icon-button-components.md) · [syrup-indicator-components.md](syrup-indicator-components.md) · [syrup-keypad-components.md](syrup-keypad-components.md) · [syrup-label-components.md](syrup-label-components.md) · [syrup-list-footer-components.md](syrup-list-footer-components.md) · [syrup-list-header-components.md](syrup-list-header-components.md) · [syrup-list-row-components.md](syrup-list-row-components.md) · [syrup-loader-components.md](syrup-loader-components.md) · [syrup-lottie-components.md](syrup-lottie-components.md) · [syrup-product-grid-components.md](syrup-product-grid-components.md) · [syrup-product-list-components.md](syrup-product-list-components.md) · [syrup-product-scroll-components.md](syrup-product-scroll-components.md) · [syrup-progress-stepper-components.md](syrup-progress-stepper-components.md) · [syrup-result-components.md](syrup-result-components.md) · [syrup-search-field-components.md](syrup-search-field-components.md) · [syrup-stepper-components.md](syrup-stepper-components.md) · [syrup-swipe-components.md](syrup-swipe-components.md) · [syrup-switch-components.md](syrup-switch-components.md) · [syrup-tab-components.md](syrup-tab-components.md) · [syrup-tab-bar-components.md](syrup-tab-bar-components.md) · [syrup-text-button-components.md](syrup-text-button-components.md) · [syrup-text-field-components.md](syrup-text-field-components.md) · [syrup-ticker-components.md](syrup-ticker-components.md) · [syrup-toast-components.md](syrup-toast-components.md) |

> **중요한 메시지나 결정을 안내하는 모달 형태의 컴포넌트에요.**
> 사용자의 흐름을 잠시 멈추고 확인, 선택, 취소 등의 행동을 유도할 때 사용해요.

---

## 공개 에셋 이름 정리

2026-11-11 아래 원본의 `.primitive / ` 접두사만 제거했어요. 노드·컴포넌트 키·variant·인스턴스 연결은 유지했으며 게시 작업은 별도로 진행해요. 숨김 유지·검토 대상의 접두사는 유지해요.

| 현재 전체 이름 | 원본 노드 |
| --- | --- |
| `Dialog / Image` | `8582:1284` |
| `Dialog / Share` | `8634:3243` |

## 목차

1. [구성 한눈에 보기](#구성-한눈에-보기)
2. [Dialog — Master Component](#1-dialog--master-component)
3. [Lottie 조합](#2-lottie-조합)
4. [Child Item](#3-child-item) — [Image](#3-1-image) · [Title](#3-2-title) · [Share](#3-3-share) · [Button Area](#3-4-button-area) · [Button](#3-5-button) · [Text Button](#3-6-text-button)
5. [설계 규칙 요약](#설계-규칙-요약)
6. [Usage](#usage)
7. [Guidelines](#guidelines)
8. [점검 필요 사항](#점검-필요-사항)

---

## 구성 한눈에 보기

페이지는 **Master Component → Lottie 조합 → Child Item** 순서로 구성되어 있습니다.

| # | 이름 | 타입 | Variant 축 | 크기 |
| --- | --- | --- | --- | --- |
| 1 | `Dialog` | Component Set | `Image` × `Slot` (2×2) | 288 × 213~355 |
| 2 | `Lottie` 조합 | 예시 (컴포넌트 아님) | — | 288 × 576 |
| 3-1 | `Dialog / Image` | Component Set | `Type` 7종 | 100 × 100 |
| 3-2 | `.primitive / Dialog / Title` | Component Set | `2 Line` × `Gold` (2×2) | 248 × 27~58 |
| 3-3 | `Dialog / Share` | Component Set | `Type` 4종 | 64 × 64 |
| 3-4 | `.primitive / Dialog / Button Area` | Component Set | `2 Buttons` 2종 | 328 × 123 |
| 3-5 | `.primitive / Dialog / Button` | Component | — | 120 × 48 |
| 3-6 | `.primitive / Button / Text Button` | Component | — | 95 × 18 |

---

## 1. Dialog — Master Component

**Node** `8578:2117` · Component Set

### Properties

| Property | Type | Default | Options | 역할 |
| --- | --- | --- | --- | --- |
| `Image` | VARIANT | `True` | `True` · `False` | 상단 이미지 오브젝트 노출 여부 |
| `Slot` | VARIANT | `False` | `True` · `False` | 본문 아래 자유 영역 사용 여부 |
| `Slot Image` | SLOT | — | — | Slot 영역에 삽입할 콘텐츠 |
| `Body Text` | BOOLEAN | `true` | — | 본문 텍스트 노출 여부 |
| `Confetti` | BOOLEAN | `true` | — | 축하 이펙트 배경 노출 여부 |

### Variants

| Variant | 크기 | 구성 |
| --- | --- | --- |
| `Image=True, Slot=False` | 288 × 259 | title + Button Area + Images + Confetti |
| `Image=True, Slot=True` | 288 × 355 | 위 + Slot 영역 |
| `Image=False, Slot=False` | 288 × 213 | title + Button Area |
| `Image=False, Slot=True` | 288 × 309 | 위 + Slot 영역 |

**공통** — 폭 288 고정 · `Corner radius/400` (16) · 배경 `Color/Gray_White` · VERTICAL 오토레이아웃

### 내부 구조 (`Image=True, Slot=True` 기준)

| 영역 | 크기 | Padding (T/R/B/L) | Gap | 비고 |
| --- | --- | --- | --- | --- |
| 루트 | 288 × 355 | 0 | 0 | radius 16, `Color/Gray_White` |
| `popup / title` | 288 × 267 | `Spacing/1100`(44) / `Spacing/500`(20) / 0 / `Spacing/500`(20) | `Spacing/400` (16) | |
| └ `Text` | 248 × 127 | 0 | `Spacing/300` (12) | Title + Body 묶음 |
| &nbsp;&nbsp;&nbsp;└ `Title` | 248 × 58 | 0 | `Spacing/100` (4) | Title 컴포넌트 인스턴스 |
| &nbsp;&nbsp;&nbsp;└ `Body Text` | 248 × 57 | — | — | `b300_15_regular` / `Color/Gray_200` |
| └ `Slot Image` | 248 × 80 | 0 | 0 | **SLOT** — 임의 콘텐츠 삽입 |
| `.primitive / Dialog / Button Area` | 288 × 88 | `Spacing/500`(20) 전방향 | 0 | |
| `Images` | 100 × 100 | — | — | y −64 — 다이얼로그 **위로 걸쳐** 배치 |
| `Confetti` | 360 × 270 | — | — | 배경 이펙트, 다이얼로그 밖으로 확장 |

- 상단 padding **44**는 `Images`(100×100)가 다이얼로그 상단 밖으로 걸쳐 나오는 구조를 위한 여백입니다.
- `Image=False` 변형에는 `Images` · `Confetti` 레이어가 아예 없습니다.

### 본문 가이드 문구 (플레이스홀더)

> Body text는 최대한 간결하게 적용합니다.
> 타이틀에서 버튼과의 연관성이 부족한 경우,

---

## 2. Lottie 조합

**Node** `9167:6560` — 컴포넌트가 아니라 **조합 예시**입니다. 상단에 Lottie 애니메이션을 얹은 형태를 보여줍니다.

| 영역 | 크기 | 비고 |
| --- | --- | --- |
| 컨테이너 | 288 × 576 | itemSpacing **−44** (음수) |
| `Lottie` | 288 × 176 | 애니메이션 영역, 라벨 `t600_21_bold` / `Color/Gray_White` |
| `Dialog` 인스턴스 | 288 × 444 | `Slot=True` 구성, Slot에 ETMS 삽입 |

음수 gap(−44)으로 Lottie가 다이얼로그 상단을 덮습니다. `Images`가 걸쳐 나오는 것과 같은 패턴입니다.

---

## 3. Child Item

### 3-1. Image

**Node** `8582:1284` · Component Set · 전 variant **100 × 100** 고정

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `Type` | VARIANT | `Gold` | `Gold` · `Gold_New` · `Slot` · `Reward` · `Game` · `Up` · `Down` |
| `Slot` | SLOT | — | `Type=Slot`일 때 삽입할 이미지 |

| Variant | 구성 레이어 | 용도 |
| --- | --- | --- |
| `Type=Gold` | `5차-클로버` | 기본 금(클로버) 오브젝트 |
| `Type=Gold_New` | `5차-클로버` + `Frame 3466478` (36×17 pill, `Corner radius/circle`) | 신규 표시 뱃지가 붙은 금 |
| `Type=Slot` | `Slot` | 임의 이미지 삽입용 |
| `Type=Reward` | `5차-클로버` + `image 3191` | 리워드 지급 |
| `Type=Game` | `Frame 3467851` | 게임 그래픽 |
| `Type=Up` | `Union` + `Ellipse 3` + `Vector` | 상승/증가 |
| `Type=Down` | `Union` + `Ellipse 3` + `Vector` | 하락/감소 |

### 3-2. Title

**Node** `8582:2061` · Component Set · 폭 **248** 고정

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `2 Line` | VARIANT | `False` | `False` · `True` |
| `Gold` | VARIANT | `False` | `False` · `True` |

| Variant | 크기 | 레이아웃 | 구성 |
| --- | --- | --- | --- |
| `2 Line=False, Gold=False` | 248 × 27 | VERTICAL | `Title01` 단독 |
| `2 Line=False, Gold=True` | 248 × 27 | HORIZONTAL, gap `Spacing/100`(4) | `Gold` 뱃지 + `Text` |
| `2 Line=True, Gold=False` | 248 × 58 | VERTICAL, gap `Spacing/100`(4) | `Title01` + `Title02`(Text) |
| `2 Line=True, Gold=True` | 248 × 58 | VERTICAL, gap `Spacing/100`(4) | `Title01` + `Title02`(Gold + Text) |

2×2 조합 4종이 모두 존재합니다. `Title02`는 Gold 유무와 관계없이 **HORIZONTAL 프레임 구조를 유지**하므로, `Gold` 값을 바꿔도 본문 텍스트 오버라이드가 보존됩니다.

**타이포 · 색상**

| 요소 | 스타일 | 색상 |
| --- | --- | --- |
| 타이틀 본문 | `t600_21_bold` | `Color/Gray_100` (#222222) |
| 금액 텍스트 (예 "50금") | `t600_21_bold` | `Color/Primary_Orange` (#FF6315) |
| `syrup_gold` 아이콘 | 25 × 14 | — |

- Gold 묶음 내부 gap은 `Spacing/50` (2).
- 타이틀 가이드: **최대 2줄, 30글자**.
- `Gold` 묶음 안의 `syrup_gold` 아이콘(25×14)은 **의도적으로 숨김 처리**되어 있습니다. 다이얼로그가 복잡해 보여 아이콘 없이 금액 텍스트만 노출하도록 정리한 결정입니다. 레이어는 남아 있으므로 필요할 때 다시 켤 수 있습니다.

### 3-3. Share

**Node** `8634:3243` · Component Set · 전 variant **64 × 64** 고정

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `Type` | VARIANT | `Kakao` | `Kakao` · `Link` · `Naver` · `Threads` |

`Link`만 벡터(`Ellipse 5495` + `Vector`)로 그려져 있고 나머지 3종은 이미지(`image 2`)입니다.

### 3-4. Button Area

**Node** `8576:903` · Component Set · **328 × 123** (두 variant 동일)

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `2 Buttons` | VARIANT | `True` | `True` · `False` |
| `Text Button` | BOOLEAN | `true` | 하단 텍스트 버튼 노출 여부 |

**공통** — padding `Spacing/500`(20) 전방향

#### `2 Buttons=True`

| 영역 | 크기 | 배경 | 라벨 스타일 | 라벨 색 |
| --- | --- | --- | --- | --- |
| `popup_btn` (HORIZONTAL, gap `Spacing/200`(8)) | 288 × 48 | — | — | — |
| └ 좌 · 보조 버튼 | 140 × 48 | `Color/Gray_900` (#F2F2F2) | `t800_17_bold` | `Color/Gray_200` |
| └ 우 · 주 버튼 | 140 × 48 | `Color/Primary_Orange` (#FF6315) | `t800_17_bold` | `Color/Gray_White` |
| `popup / text_btn` | 288 × 35 | — | — | — |
| └ Text Button | 95 × 18 | — | `b400_14_regular` | `Color/Gray_500` |

`popup / text_btn`의 padding은 `14 / Spacing/400(16) / 0 / Spacing/400(16)`, gap `Spacing/250`(10).

#### `2 Buttons=False`

단일 주 버튼 **288 × 48**, `Color/Primary_Orange`. 텍스트 버튼 영역은 동일합니다.

#### 버튼 공통 스펙

| 속성 | 값 |
| --- | --- |
| 높이 | 48 |
| Padding | `Spacing/50`(2) / `Spacing/300`(12) |
| Gap | `Spacing/100` (4) |
| Radius | `Corner radius/250` (10) |
| 라벨 | `t800_17_bold` |

### 3-5. Button

**Node** `8570:6508` · Component (단일) · **120 × 48** · description **"2btn"**

| Property | Type | Default | 역할 |
| --- | --- | --- | --- |
| `Bubble` | BOOLEAN | `true` | 버튼 위 말풍선 뱃지 노출 |

구성: `Button` 인스턴스 + `Bubble` 인스턴스 (HORIZONTAL)

### 3-6. Text Button

**Node** `8576:942` · Component (단일) · **95 × 18**

`Label` 텍스트 단독. `b400_14_regular` / `Color/Gray_500`. 취소 · 다시 보지 않기 같은 3차 액션에 사용합니다.

---

## 설계 규칙 요약

| 항목 | 규칙 |
| --- | --- |
| 폭 | **288 고정** (Button Area 단독 전시는 328) |
| 모서리 | `Corner radius/400` (16) |
| 배경 | `Color/Gray_White` |
| 좌우 여백 | `Spacing/500` (20) |
| 상단 여백 | `Spacing/1100` (44) — 이미지가 걸쳐 나오는 구조 |
| 타이틀 | `t600_21_bold` / `Color/Gray_100` / 최대 2줄 30자 |
| 본문 | `b300_15_regular` / `Color/Gray_200` / 간결하게 |
| 주 액션 | `Color/Primary_Orange` 배경 + `Color/Gray_White` 라벨 |
| 보조 액션 | `Color/Gray_900` 배경 + `Color/Gray_200` 라벨 |
| 3차 액션 | 텍스트 버튼 `b400_14_regular` / `Color/Gray_500` |
| 버튼 모서리 | `Corner radius/250` (10) |

**액션 위계가 3단계**입니다 — 주 버튼(오렌지) → 보조 버튼(회색) → 텍스트 버튼. 2버튼 구성에서는 오른쪽이 주 액션입니다.

---

## Usage

| 항목 | 값 |
| --- | --- |
| 섹션 | [`Usage` `11514:2428`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11514-2428) · 4560 × 874 |
| 구성 | 11패턴 · 화면 360 × 540 · Dialog 높이 182~401 |
| 템플릿 | `Usage` 컴포넌트 [`11237:46733`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11237-46733) (`❖System Components` 페이지) |

> **컷은 화면 캡처가 아니라 실제 컴포넌트 인스턴스입니다.**
> 해당 컴포넌트와 **꼭 필요한 맥락 요소만** 남기고 나머지 화면 요소는 모두 지웠습니다. 남은 요소도 잘라낸 그림이 아니라 마스터를 직접 참조하는 인스턴스라, 컴포넌트 디자인이 바뀌면 문서가 함께 바뀝니다 (2026-11-06).

**열한 컷 모두 딤 위에 떠 있는 화면입니다.** Dialog는 흰 배경이라 떼어 놓으면 경계가 보이지 않고, **화면 한가운데**라는 자리도 드러나지 않습니다. 컷마다 360 × 540 화면을 두고 `Dim` 위에 Dialog를 중앙 정렬했습니다.

| 화면 프레임 | 값 |
| --- | --- |
| 크기 | **360 × 540** (전 컷 동일) |
| 배경 | `Color/Gray_White` |
| 딤 | `Dim` [`10285:3541`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=10285-3541) · 검정 75% |
| Dialog 자리 | 좌우 **36** · **가로·세로 중앙** |

좌우 36은 제품 109건이 예외 없이 쓰는 값입니다 (288 + 36 × 2 = 360).

**패턴을 가르는 축은 「무엇을 채우는가」입니다.** Dialog는 `Image` · `Slot` 두 VARIANT가 골격을 정하므로, 열한 패턴을 그 축으로 세 묶음으로 나눴습니다.

| 묶음 | 패턴 | Variant |
| --- | --- | --- |
| **텍스트만으로 안내** | A · B · C · H | `Image=False` · `Slot=False` |
| **본문 Slot 활용** | D · E · F · G · K | `Image=False` · **`Slot=True`** |
| **보상 이미지** | I · J | **`Image=True`** |

### 텍스트만으로 안내 — A · B · C · H

| | 패턴 | 설명 | 버튼 | Dialog 높이 |
| --- | --- | --- | --- | --- |
| **A** | 간단한 안내 | 상태나 처리 완료 여부를 짧게 안내할 때 사용해요. 확인 버튼 하나로 내용을 확인하고 닫을 수 있어요. | 1개 「확인」 | **182** |
| **B** | 행동 확인 | 진행하거나 중단하기 전에 사용자의 의사를 확인해요. 행동으로 달라지는 내용을 설명하고 버튼에는 실행할 행동을 적어요. | 2개 「그만하기」·「계속하기」 | 209 |
| **C** | 설정·업데이트 안내 | 기능 사용에 필요한 설정이나 업데이트를 안내해요. 필요한 이유를 설명하고 해당 화면으로 이동할 수 있는 버튼을 제공해요. | 2개 「취소」·「설정하기」 | 228 |
| **H** | 결과 안내 | 참여 결과를 제목과 설명으로 안내해요. 결과를 나타내는 이미지는 내용과 일치하도록 사용해요. | 1개 「확인」 | 209 |

**A가 가장 작은 Dialog입니다 (182).** 제목 한 줄 + 설명 한 줄 + 버튼 하나로, 이 컴포넌트가 가질 수 있는 최소 구성입니다.

**B와 C는 버튼 문구가 다릅니다.** B는 「그만하기 / 계속하기」로 **되돌림과 진행**을, C는 「취소 / 설정하기」로 **거절과 이동**을 묻습니다. 둘 다 보조 행동이 왼쪽입니다 → [Guidelines 3](#3-필요한-행동에-맞춰-버튼을-구성해요)

### 본문 Slot 활용 — D · E · F · G · K

| | 패턴 | 설명 | Slot에 담은 것 | Dialog 높이 |
| --- | --- | --- | --- | --- |
| **D** | 상세 안내 | 이용 방법이나 유의 사항처럼 여러 항목을 안내할 때 사용해요. 제목과 본문을 구분하고 관련 내용을 묶어 보여줘요. | 유의 사항 4줄 (`Body Text=false`) | 329 |
| **E** | 정보 입력 | 코드 등 필요한 정보를 입력받을 때 본문 Slot에 입력 컴포넌트를 배치해요. 입력 조건과 오류 안내를 함께 제공해요. | 입력 필드 + 조건 + 오류 문구 | 239 |
| **F** | 항목 선택 | 계정 등 선택이 필요한 항목을 본문 Slot에 배치해요. 선택한 항목을 구분하고 확인 버튼으로 선택을 완료해요. | `Checkbox` 3줄 (Npay 아이디) | **373** |
| **G** | 공유 방법 선택 | 공유할 채널이나 링크 복사 등 실행할 방법을 나란히 제공해요. 각 아이콘에 문구를 함께 표시해 방법을 구분해요. | 공유 아이콘 2개 (64 × 64) | 310 |
| **K** | 이미지 구성 | 이미지가 필요한 경우 본문 Slot 안에 이미지와 보조 요소를 자유롭게 구성할 수 있어요. 안내 내용에 맞는 이미지를 사용하고 제목, 설명, 버튼과 구분해 배치해요. | 복권 이미지 묶음 | **401** |

**D만 `Body Text=false`입니다.** 유의 사항 네 줄을 전부 Slot에 넣었기 때문에, 컴포넌트가 가진 본문 텍스트 자리는 비워 두었습니다. 나머지 넷은 **제목 + 본문 + Slot** 세 층을 모두 씁니다.

**K가 가장 큽니다 (401).** 이미지를 상단 `Image` 자리가 아니라 **Slot 안에서 자유롭게 구성**한 경우라, 보상 이미지(I · J)와는 다른 길입니다 → [Guidelines 2](#2-보상을-받는-팝업에는-보상-이미지를-사용해요)

### 보상 이미지 — I · J

| | 패턴 | 설명 | 구성 | Dialog 높이 |
| --- | --- | --- | --- | --- |
| **I** | 보상 수령 | 금이나 쿠폰 등 받는 대상의 이미지를 팝업 상단에 사용해요. 금은 기존 Lottie 영역을 활용하고, 받은 보상과 수량을 명확하게 안내해요. | `Images` `Type=Gold` (100 × 100) | 190 |
| **J** | 보상과 추가 콘텐츠 | 보상 수령 안내 아래에 광고 등 추가 콘텐츠를 함께 보여줄 때 사용해요. 보상 정보와 추가 콘텐츠, 하단 행동을 구분해 배치해요. | `Images` + Slot에 `P_AD` (248 × 177) | **383** |

**`Images`는 Dialog 위로 걸쳐 나옵니다.** 100 × 100 금괴가 상단 바깥으로 올라앉고, 그만큼 `popup / title`의 상단 패딩이 **44**로 잡혀 있습니다.

**J는 세 층을 한 팝업에 담습니다** — 보상(`Images` + 제목) · 추가 콘텐츠(`P_AD` 광고) · 하단 행동(2버튼). 보상만 전하는 I보다 **193이 더 높습니다.**

### 제품 실측 (2026-11-06)

제품 파일 **[Syrup_App](https://www.figma.com/design/LekNzN0LrcSKQYdutQFI1i)** 전체에서 `Dialog` 인스턴스 **111건**을 전수 조사했습니다. 아이데이션은 2건뿐이라, 실제 제품 화면은 **109건**입니다.

| 항목 | 값 | 건수 |
| --- | --- | --- |
| 배치 | **직접 배치** | **109** |
| | 다른 컴포넌트 안에 중첩 | **0** |
| 폭 | **288** | **109** |
| 좌우 여백 | **36 / 36** | **109** |
| 높이 | 159 ~ 460 | — |
| `Image` | `False` | 79 |
| | `True` | **30** |
| `Slot` | `False` | 57 |
| | **`True`** | **52** |
| `Body Text` | `true` | 81 |
| | `false` | 28 |
| `Confetti` | **`true`** | **75** |
| | `false` | 34 |
| `Button Area` | `2 Buttons=True` | **62** |
| | `2 Buttons=False` | 43 |
| | **`Text Button=true`** | **4** |
| 딤 | `Dim` 컴포넌트 | 81 |
| | 직접 그린 사각형 | **21** |
| | 없음 | 7 |

**중첩이 한 건도 없습니다.** Dialog는 언제나 화면 위에 혼자 올라오는 요소라, 다른 컴포넌트 안에 들어가지 않습니다. 폭 288과 좌우 36도 109건이 예외 없이 같습니다 → [Guidelines 1](#1-화면-중앙에-dialog를-배치하고-dim을-함께-사용해요)

**`Slot=True`가 절반에 가깝습니다 (52 / 109).** Dialog는 「제목 + 본문 + 버튼」 틀만 쓰는 컴포넌트가 아니라, **본문 자리에 무엇이든 끼워 쓰는 그릇**으로 쓰입니다. Usage에서 Slot 묶음에 다섯 컷을 둔 이유입니다 → [Guidelines 4](#4-입력이나-선택이-필요하면-본문-slot을-활용해요)

**버튼은 둘이 기본입니다 (62 / 109).** 하나짜리 43건은 결과·완료를 알리고 닫는 자리입니다. `Text Button=true`는 4건뿐입니다.

**`Confetti`는 보상 팝업에서 사실상 항상 켜집니다.**

| `Image` | `Confetti` | 건수 | 실제 효과 |
| --- | --- | --- | --- |
| `True` | **`true`** | **29** | 컨페티 보임 |
| `True` | `false` | 1 | — |
| `False` | `true` | **46** | **레이어가 없어 효과 없음** |
| `False` | `false` | 33 | — |

보상 팝업 30건 중 **29건이 컨페티를 켭니다.** 그런데 Usage · Guidelines의 모든 컷은 `Confetti=false`입니다 → [점검 5](#5-컷에-confetti가-한-번도-켜져-있지-않습니다)

---

## Guidelines

지켜지지 않으면 결과가 깨지는 것만 올렸습니다. 각 항목은 Figma **[`Guidelines` 섹션 `11514:3066`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11514-3066)** (960 × 3236) 에 한 쌍씩 들어 있습니다.

규칙 하나가 `Guidelines` 템플릿 인스턴스 [`11237:44468`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11237-44468) (`❖System Components` 페이지) 하나입니다. 폭 760, `Title`(제목 + 설명) 아래 `Image` 프레임에 슬롯이 좌우로 들어갑니다.

**여덟 컷 모두 Usage와 같은 360 × 540 딤 화면입니다.** 규칙 1의 Don't만 딤이 없는데, 그것이 비교 대상이기 때문입니다.

| 형식 | 규칙 | 슬롯 라벨 | 라벨 색 |
| --- | --- | --- | --- |
| Do / Don't | **1 · 2** | `Do` · `Don’t` (2는 뒤에 설명을 덧붙임) | `#222222` · **`#FF3E00`** |
| 두 경우 비교 | **3 · 4** | 「내용 확인」·「행동 선택」 / 「입력 컴포넌트」·「선택 항목」 | `#222222` · **`#222222`** |

3 · 4는 **둘 다 정상인 선택**이라 Do / Don't로 두지 않았고, [Bottom Sheet 규칙 6](syrup-bottom-sheet-components.md#6-부가-설명은-보조-설명으로-나눌-수-있어요)에서 정한 대로 오른쪽 라벨 색도 검정으로 맞췄습니다.

### 1. 화면 중앙에 Dialog를 배치하고 Dim을 함께 사용해요

화면 배경은 흰색으로 두고, 전체 영역을 덮는 Dim 위에 Dialog를 가로·세로 중앙 정렬해요.
레이어는 화면 → Dim → Dialog 순서로 배치해 뒤 화면과 명확하게 구분해요.

| | 레이어 | 결과 |
| --- | --- | --- |
| **Do** | 화면 → **`Dim`** → Dialog | Dialog가 앞에 떠 보임 |
| **Don't** | 화면 → Dialog | 흰 Dialog가 흰 화면에 묻혀 경계가 사라짐 |

두 컷 모두 같은 보상 팝업(288 × 190)이 같은 자리에 있고, **다른 것은 `Dim` 하나**입니다.

**Don't에서는 Dialog의 테두리가 보이지 않습니다.** Dialog는 그림자가 없고 배경이 `Color/Gray_White`라, 경계를 만드는 것이 전적으로 딤입니다. 금괴 이미지와 버튼만 허공에 떠 있는 것처럼 보입니다.

딤은 `Dim` 컴포넌트를 쓰세요 — 제품 109건 중 21건이 직접 그린 사각형을 씁니다 → [점검 6](#6-딤을-직접-그린-사각형으로-쓴-곳이-21건입니다)

### 2. 보상을 받는 팝업에는 보상 이미지를 사용해요

금이나 쿠폰 등 받는 대상의 이미지를 팝업 상단에 배치해요. 금은 기존 컴포넌트의 Lottie 영역을 사용해요.
현재 예제는 금 수령 사례이며, 쿠폰을 제공하는 경우에는 해당 쿠폰 이미지를 사용해요.

| | `Image` | `Images` | Dialog 높이 |
| --- | --- | --- | --- |
| **Do · 보상 이미지 표시** | **`True`** | `Type=Gold` 100 × 100 | 190 |
| **Don't · 보상 이미지 없음** | `False` | 없음 | 182 |

두 컷 모두 「5금 받았어요! / 식단 기록 완료!」로 **문구가 같습니다.** 다른 것은 상단 이미지의 유무입니다.

**무엇을 받았는지를 글자로만 전하면 약합니다.** 보상 팝업은 순간적으로 지나가는 화면이라, 받은 대상이 그림으로 먼저 보여야 합니다. 제품에서도 `Image=True` 30건이 전부 보상·결과 안내 자리입니다.

**금 외의 보상은 해당 이미지를 씁니다.** 설명의 두 번째 문장이 그 범위를 열어 둡니다 — 쿠폰이면 쿠폰 이미지입니다.

### 3. 필요한 행동에 맞춰 버튼을 구성해요

내용 확인만 필요하면 확인 버튼 하나를 사용해요. 진행 여부를 물을 때는 보조 행동을 왼쪽, 주요 행동을 오른쪽에 둬요.
버튼 문구는 사용자가 실행할 행동을 알 수 있도록 작성해요.

| 라벨 | `2 Buttons` | 버튼 | 폭 |
| --- | --- | --- | --- |
| **내용 확인** | `False` | 「확인」 1개 | 248 |
| **행동 선택** | **`True`** | 「그만하기」(보조) · 「계속하기」(주요) | 120 + 120 |

**버튼 문구에 행동을 적습니다.** 「예 / 아니오」가 아니라 「그만하기 / 계속하기」입니다. 팝업을 덮어 쓴 상태에서도 **무엇이 일어날지**가 버튼만 보고 읽혀야 합니다.

**제품은 둘짜리를 더 많이 씁니다** — `2 Buttons=True` 62건 · `False` 43건. 하나짜리는 결과를 알리고 닫는 자리에 쓰입니다.

### 4. 입력이나 선택이 필요하면 본문 Slot을 활용해요

정보를 입력하거나 항목을 선택해야 할 때는 본문 Slot에 필요한 컴포넌트를 배치해요.
기존 Dialog의 제목·본문·버튼 구조를 유지하고 입력 조건이나 선택 상태가 명확하게 보이도록 구성해요.

| 라벨 | Slot에 담은 것 | `Body Text` | Dialog 높이 |
| --- | --- | --- | --- |
| **입력 컴포넌트** | 입력 필드 + 「영문, 숫자 포함 7자리」 + 오류 문구 | `false` | 239 |
| **선택 항목** | `Checkbox` 3줄 (Npay 아이디) | `true` | **373** |

**Slot은 제목·버튼을 건드리지 않습니다.** 두 컷 모두 위에는 제목이, 아래에는 2버튼이 그대로 있고 **가운데만 바뀝니다.** 설명의 「기존 Dialog의 구조를 유지하고」가 그 뜻입니다.

**조건과 상태를 함께 보여 줍니다.** 입력 쪽은 입력 조건(「영문, 숫자 포함 7자리」)과 오류 문구를, 선택 쪽은 어느 항목이 선택됐는지를 Slot 안에서 보여 줍니다.

---

## 점검 필요 사항

### 1. ✅ 레이어 · 프로퍼티 이름 오타 (2026-09-21 수정 완료)

| 위치 | 변경 전 | 변경 후 | 건수 |
| --- | --- | --- | --- |
| Dialog 컴포넌트셋 프로퍼티 | `Boty Text#8582:0` | `Body Text#8582:0` | 1 |
| Dialog variant 내부 텍스트 레이어 | `Bodt Text` | `Body Text` | 4 |
| Text Button 플레이스홀더 문구 | `Text Botton Line` | `Text Button Line` | 1 |

프로퍼티 이름은 `#8582:0` 식별자가 유지되므로 기존 인스턴스의 프로퍼티 연결은 끊기지 않습니다.

### 2. ✅ Variant 조합 누락 (2026-09-21 추가 완료)

`Title`에 빠져 있던 **`2 Line=True, Gold=False`** (Node `10618:201`)를 추가했습니다. 이제 `2 Line` × `Gold` 2×2 조합 4종이 모두 존재합니다.

| 항목 | 내용 |
| --- | --- |
| 생성 방식 | `2 Line=True, Gold=True`를 복제 후 `Title02` 안의 `Gold` 뱃지 프레임만 제거 |
| 결과 구조 | `Title01` + `Title02`(HORIZONTAL, gap 4) › `Text` |
| 컴포넌트셋 크기 | 288 × 192 → **288 × 270** |
| variant 순서 | (F,F) → (F,T) → **(T,F)** → (T,T) |

`Title02`를 프레임 그대로 유지했기 때문에 `Gold` 값을 전환해도 본문 텍스트 오버라이드가 유지됩니다.

### 3. 토큰 미바인딩 값

2026-09-21 파일 전체 바인딩 정리 이후 Dialog 페이지에 남은 값입니다. (인스턴스 외부 기준)

| 속성 | 남은 값 (건수) | 비고 |
| --- | --- | --- |
| padding | `100` (12) · `5` (2) · `14` (2) · `140` (2) · `2.5` (2) · `80` (1) | `2.5` 소수점 패딩은 정리 대상 |
| itemSpacing | `−44` (1) | Lottie 겹침용 음수 값 — 토큰화 대상 아님 |

> **radius `5`(모서리 20건)는 감사 대상에서 제외합니다.** Dialog 페이지의 컴포넌트셋 5개(`Dialog` · `Image` · `Title` · `Share` · `Button Area`)의 **점선 컨테이너에 Figma가 기본으로 넣는 값**입니다. 파일 전체로는 컴포넌트셋 178개 전부에 동일하게 나타나며, 프로덕션에 렌더링되지 않습니다.

#### ✅ radius 정리 완료 (2026-09-21)

| 대상 | 변경 전 | 변경 후 | 노드 수 |
| --- | --- | --- | --- |
| Share `Type=Kakao` · `Naver` · `Threads` → `image 2` (64×64) | `300` | `Corner radius/circle` | 3 (모서리 12건) |
| Image `Type=Gold_New` → `Frame 3466478` (36×17) | `116.84` | `Corner radius/circle` | 1 (모서리 4건) |

두 건 모두 **렌더링이 바뀌지 않습니다.** Figma는 모서리 반경을 짧은 변의 절반까지만 적용하므로(64×64 → 32, 36×17 → 8.5) `300` · `116.84` · `100` 모두 같은 완전 라운드 형태로 그려집니다. `116.84`는 도형 리사이즈 과정에서 반경이 비례 조정되며 생긴 값으로 보입니다.

### 4. 남은 외부 라이브러리 토큰

| 토큰 | 건수 | 비고 |
| --- | --- | --- |
| `paragraphSpacing/0` · `paragraphIndent/0` @semantic tokens | 24 | 전역 이슈 — 로컬 텍스트 스타일 20개가 참조 중 |
| `Spec docs/margin` · `Spec docs/width` @docs | 15 | 문서 레이아웃 전용, 의도적 유지 |

값이 Syrup 토큰과 일치하는 외부 토큰은 모두 교체 완료되었습니다. 자세한 내용은 [syrup-design-tokens.md](syrup-design-tokens.md)의 "토큰 적용 현황"을 참고하세요.

### 5. 컷에 `Confetti`가 한 번도 켜져 있지 않습니다

Usage 11컷과 Guidelines 8컷, **열아홉 컷 전부 `Confetti=false`** 입니다. 그런데 제품에서는 보상 팝업이 사실상 항상 컨페티를 켭니다.

| | `Image=True` 중 `Confetti=true` |
| --- | --- |
| 제품 | **29 / 30** |
| Usage · Guidelines 컷 | **0 / 4** (Usage I · J · Guidelines 1 Do · 2 Do) |

컨페티는 360 × 270으로 **Dialog 밖까지 퍼지는 배경 이펙트**라, 켜면 컷의 인상이 꽤 달라집니다. 보상 팝업을 다루는 [Usage I · J](#보상-이미지--i--j)와 [Guidelines 2](#2-보상을-받는-팝업에는-보상-이미지를-사용해요)는 **제품과 같은 상태로 켜 두는 편이 실제에 가깝습니다.**

#### 함께 확인할 것 — `Image=False`에서 켜진 46건

`Confetti`는 BOOLEAN이고 기본값이 `true`인데, **`Image=False` variant에는 레이어 자체가 없습니다.**

| `Image` | `Confetti` | 건수 | 실제 효과 |
| --- | --- | --- | --- |
| `False` | **`true`** | **46** | **없음** — 레이어가 없어 아무 일도 하지 않음 |
| `False` | `false` | 33 | — |

프로퍼티 패널에는 계속 노출되므로 **켜 두고도 아무 변화가 없어 혼동**을 줍니다. [Bubble의 `Gold` 레이어](syrup-bubble-components.md)와 같은 구조이고, 그쪽은 의도된 설계로 확인된 건입니다. Dialog도 같은 판단이라면 기록해 두고, 아니라면 기본값을 `false`로 내리는 편이 깔끔합니다.

### 6. 딤을 직접 그린 사각형으로 쓴 곳이 21건입니다

제품 109건 중 **21건**이 `Dim` 컴포넌트가 아니라 직접 그린 사각형을 쓰고 있습니다.

| 딤 | 건수 |
| --- | --- |
| `Dim` 컴포넌트 인스턴스 | 81 |
| 직접 그린 사각형 (`dim` RECTANGLE 등) | **21** |
| 없음 | 7 |

지금은 같은 검정 75%라 보이는 결과가 같지만, **딤 농도가 바뀌면 이 21건만 따라오지 않습니다.** [Bottom Sheet에서도 같은 건이 2건](syrup-bottom-sheet-components.md#10-딤을-직접-그린-사각형으로-쓴-곳이-있습니다) 있었는데, Dialog 쪽이 열 배 많습니다.

딤이 아예 없는 7건은 팝업만 따로 떼어 둔 작업용 프레임으로 보이나, 화면에 올라가는 컷이라면 [Guidelines 1](#1-화면-중앙에-dialog를-배치하고-dim을-함께-사용해요)의 Don't 상태입니다 — 함께 확인이 필요합니다.
