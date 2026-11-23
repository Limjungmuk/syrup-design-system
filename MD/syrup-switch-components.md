# Syrup Design System — Switch 컴포넌트

> 이름 확인 (2026-11-11): `🟧`로 시작하는 컴포넌트·컴포넌트 세트는 없어요. 아래 구 에셋명과 접두사 건수는 과거 점검 기록이며, 일부 그룹·프레임·벡터·인스턴스 레이어에는 해당 이름이 남아 있어요. 하위 레이어명을 현재 라이브러리 컴포넌트 이름으로 사용하지 않아요.


| 항목 | 값 |
| --- | --- |
| Figma File | [Syrup_Design-System](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System) |
| Page / Section | `Switch` 페이지 → [Switch 섹션 `8444:9239`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=8444-9239) |
| 섹션 크기 | 1440 × 946 |
| 컴포넌트 수 | **1개** |
| Variant 총수 | **4개** |
| 기준일 | 2026-11-10 (가이드라인·Usage 및 통일된 예제 디자인 반영) |
| 관련 문서 | [syrup-design-tokens.md](syrup-design-tokens.md) · [syrup-ad-components.md](syrup-ad-components.md) · [syrup-alert-components.md](syrup-alert-components.md) · [syrup-badge-components.md](syrup-badge-components.md) · [syrup-banner-components.md](syrup-banner-components.md) · [syrup-border-components.md](syrup-border-components.md) · [syrup-bottom-cta-components.md](syrup-bottom-cta-components.md) · [syrup-bottom-info-components.md](syrup-bottom-info-components.md) · [syrup-bottom-sheet-components.md](syrup-bottom-sheet-components.md) · [syrup-bubble-components.md](syrup-bubble-components.md) · [syrup-button-components.md](syrup-button-components.md) · [syrup-card-components.md](syrup-card-components.md) · [syrup-checkbox-components.md](syrup-checkbox-components.md) · [syrup-chip-components.md](syrup-chip-components.md) · [syrup-dialog-components.md](syrup-dialog-components.md) · [syrup-dim-components.md](syrup-dim-components.md) · [syrup-grid-list-components.md](syrup-grid-list-components.md) · [syrup-grid-scroll-components.md](syrup-grid-scroll-components.md) · [syrup-header-components.md](syrup-header-components.md) · [syrup-icon-button-components.md](syrup-icon-button-components.md) · [syrup-indicator-components.md](syrup-indicator-components.md) · [syrup-keypad-components.md](syrup-keypad-components.md) · [syrup-label-components.md](syrup-label-components.md) · [syrup-list-footer-components.md](syrup-list-footer-components.md) · [syrup-list-header-components.md](syrup-list-header-components.md) · [syrup-list-row-components.md](syrup-list-row-components.md) · [syrup-loader-components.md](syrup-loader-components.md) · [syrup-lottie-components.md](syrup-lottie-components.md) · [syrup-product-grid-components.md](syrup-product-grid-components.md) · [syrup-product-list-components.md](syrup-product-list-components.md) · [syrup-product-scroll-components.md](syrup-product-scroll-components.md) · [syrup-progress-stepper-components.md](syrup-progress-stepper-components.md) · [syrup-result-components.md](syrup-result-components.md) · [syrup-search-field-components.md](syrup-search-field-components.md) · [syrup-stepper-components.md](syrup-stepper-components.md) · [syrup-swipe-components.md](syrup-swipe-components.md) · [syrup-tab-components.md](syrup-tab-components.md) · [syrup-tab-bar-components.md](syrup-tab-bar-components.md) · [syrup-text-button-components.md](syrup-text-button-components.md) · [syrup-text-field-components.md](syrup-text-field-components.md) · [syrup-ticker-components.md](syrup-ticker-components.md) · [syrup-toast-components.md](syrup-toast-components.md) |

> **켜짐/꺼짐 상태를 전환할 수 있는 토글형 컴포넌트예요.**
> 설정이나 옵션의 활성화 여부를 단순하게 제어할 때 사용해요.

---

## 목차

1. [구성 한눈에 보기](#구성-한눈에-보기)
2. [Switch — Master Component](#1-switch--master-component)
3. [가이드라인](#가이드라인)
4. [Usage — 사용 예제](#usage--사용-예제)
5. [예제 디자인과 AI 사용 기준](#예제-디자인과-ai-사용-기준)
6. [설계 규칙 요약](#설계-규칙-요약)
7. [점검 필요 사항](#점검-필요-사항)
8. [정리 우선순위](#정리-우선순위)

---

## 구성 한눈에 보기

마스터 1종의 상태 4개와 별도 가이드라인 3개, Usage A~D로 구성해요.

기존 마스터 섹션 집계는 높이 946 · 노드 **23개** · 텍스트 **3개**예요. 이 문서의 기존 노드·인스턴스·파일 전체 집계는 2026-10-12 점검 기록이며, 이후 추가된 사용 화면과 문서 예제를 포함하지 않아요.

| 보드 위치 | 섹션 | 내용 |
| --- | --- | --- |
| y 0 | Title Bar | 페이지 제목 |
| y 434 | Section Header | Master Component |
| y 574 | (높이 308) | `Switch` 1종 |

| # | 이름 | 타입 | Variant 축 | 크기 | 인스턴스 |
| --- | --- | --- | --- | --- | --- |
| 1 | `Switch` | Set 4 | `Check` × `Disabled` | 42 × 24 | **0** |

**Child Item이 없는 단일 컴포넌트**입니다. 토글 바 하나와 손잡이 원 하나가 전부입니다.

컴포넌트명이 소문자 `switch`로 페이지명과 어긋나 있었고, `Switch`로 바로잡았습니다 ✅ → [점검 1](#1-컴포넌트명-switch-소문자---완료)

---

## 1. Switch — Master Component

**Node** `8444:9249` · Component Set · **4 variants** = `Check`(2) × `Disabled`(2) **완전 매트릭스** ✅

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `Check` | VARIANT | `On` | `Off` · `On` |
| `Disabled` | VARIANT | `False` | `True` · `False` |

### 공통 레이아웃

| 항목 | 값 | 토큰 |
| --- | --- | --- |
| 크기 | **42 × 24** | — |
| 레이아웃 | 가로 오토레이아웃 | — |
| Padding | `2 / 2 / 2 / 2` | `Spacing/50` ✅ |
| Gap | 2 | `Spacing/50` ✅ |
| 라운드 | 100 | `Corner radius/circle` ✅ |
| 손잡이 `Oval` | 20 × 20 | `Color/Gray_White` ✅ |

### 손잡이 위치를 오토레이아웃 정렬로 처리

| Check | 주축 정렬 | `Oval` x | 결과 |
| --- | --- | --- | --- |
| `On` | **MAX** | 20 | 오른쪽 |
| `Off` | **MIN** | 2 | 왼쪽 |

좌표를 직접 찍지 않고 **정렬 값만 바꿔** 손잡이를 좌우로 옮깁니다. 크기가 바뀌어도 양끝 여백 2가 유지되는 구조입니다.

[Swipe](syrup-swipe-components.md)가 핸들을 절대 배치로 뺀 것과 대조적이지만, **Swipe는 중간 위치(x 24)가 필요**하고 Switch는 양끝만 쓰므로 각자 맞는 방식입니다.

### variant별 색과 투명도

| Check | Disabled | 배경 | 투명도 | 크기 |
| --- | --- | --- | --- | --- |
| `On` | `False` | `Color/Primary_Orange` ✅ | 1 | 42 × 24 |
| `Off` | `False` | `Color/Gray_700` ✅ | 1 | 42 × 24 |
| `On` | `True` | `Color/Primary_Orange` ✅ | **0.3** | 42 × 24 ✅ |
| `Off` | `True` | `Color/Gray_850` ✅ | 1 | 42 × 24 |

두 가지가 걸립니다.

- **비활성 표현이 두 방식으로 갈립니다** — `On`은 투명도, `Off`는 색 교체 → [점검 2](#2-비활성-표현이-두-방식)
- `On, Disabled=True`만 폭이 42.48이었고 42로 맞추었습니다 ✅ → [점검 3](#3-폭-4248-1건---완료)

---

## 가이드라인

[Figma Guidelines](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11739-612) · 2026-11-10 기준

### 1. 현재 설정을 On과 Off로 구분해요

기능이나 옵션을 켜고 끌 때 Switch를 사용해요. 켜진 상태는 Check=On, 꺼진 상태는 Check=Off로 표시해요.
항목 이름과 함께 배치해 어떤 설정을 변경하는지 알 수 있도록 해요.

- 비교: 켜짐 · Check=On / 꺼짐 · Check=Off
- [Figma 가이드라인 1](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11739-614)

### 2. 어떤 설정을 변경하는지 알 수 있도록 배치해요

설정 이름과 Switch를 함께 배치해 조작 대상을 명확히 해요.
여러 항목을 나열할 때는 Switch의 위치를 맞춰 각 설정의 상태를 쉽게 비교할 수 있도록 해요.

- 예시: 간단한 옵션 / 보조 설명이 필요한 설정
- 보조 설명과 상세보기의 구성 자체를 Switch의 필수 속성으로 규정하는 항목이 아니에요.
- [Figma 가이드라인 2](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11739-668)

### 3. 변경할 수 없을 때는 Disabled로 표시해요

권한이나 선행 조건 때문에 설정을 변경할 수 없으면 Disabled=True로 표시해요. 기존 On·Off 값은 유지해요.
조건을 충족할 수 있도록 비활성 이유나 필요한 설정을 주변 설명으로 안내해요.

- 비교: 켜진 상태 · Disabled=True / 꺼진 상태 · Disabled=True
- Disabled는 조작 가능 여부이고 Check는 현재 설정 값이에요. 비활성이라고 반드시 Off로 바꾸지 않아요.
- [Figma 가이드라인 3](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11739-725)

---

## Usage — 사용 예제

[Figma Usage](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11739-613) · A~D 순서

| 예제 | 설명 | 예제의 상태 | Figma |
| --- | --- | --- | --- |
| A. 단일 옵션 설정 | 공휴일 제외처럼 하나의 옵션을 켜거나 끌 때 사용해요. 설정 이름과 Switch를 한 줄로 간결하게 배치해요. | Check=On · Disabled=False | [A](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11739-780) |
| B. 기능의 동작 설정 | 동영상 광고 자동 재생 여부를 Switch로 설정해요. 보조 설명은 적용 환경과 해제 시 동작을 이해하도록 돕는 주변 요소예요. | Check=On · Disabled=False | [B](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11739-807) |
| C. 수신 및 정보 이용 동의 | 혜택 알림 수신 등 동의 여부를 Switch로 설정해요. 동의 목적을 안내하는 설명과 내용을 확인하는 상세보기는 별도 요소로 함께 배치해요. | Check=Off · Disabled=False | [C](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11739-838) |
| D. 권한과 선행 조건에 따른 비활성 | 알림 권한이나 상위 설정이 필요하면 Disabled로 표시해요. 야간알림처럼 다른 설정에 영향을 받는 항목은 조건을 함께 안내해요. | 2개 모두 Check=Off · Disabled=True | [D](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11739-875) |

D는 ‘지금 할 일 알림’과 ‘지금 할 일 야간알림’을 함께 보여줘요. 야간알림은 지금 할 일 알림이 켜져 있어야 받을 수 있다는 조건을 주변 설명으로 안내해요. 이 조건은 해당 서비스의 사용 사례이며 모든 Switch에 공통으로 적용하는 조건은 아니에요.

---

## 예제 디자인과 AI 사용 기준

### 통일된 시각 표현

2026-11-10에 사용자가 정리한 최신 Figma 구성을 기준으로 해요. 마스터 Switch와 주변 설정 행은 서로 다른 범위예요.

| 항목 | 최신 문서 예제의 표현 |
| --- | --- |
| Switch | 모든 사례에서 **42 × 24** 유지, 기존 Switch 인스턴스 사용 |
| 설정 이름 | **Pretendard 17 Medium** · `t1100_17_medium` |
| 보조 설명 | **Pretendard 14 Regular** · B·C는 `b400_14_regular`, D는 동일 서체·크기의 개별 토큰 연결 |
| 설명 행간 | B·C는 **18**, D는 **20**으로 현재 적용돼 있어요. 행간까지 모두 동일하다고 가정하지 않아요. |
| A의 행 | 폭 **328**, 좌우 패딩 0, 설정 이름과 Switch를 **Space between**으로 배치 |
| B·C의 행 | 폭 **320**, 텍스트 영역 **262** + 간격 **16** + Switch **42**, 상단 기준 배치 |
| 텍스트와 Switch 사이 | B·C·D의 설정 행에서 **16** · `Spacing/400` |
| 이름과 보조 설명 사이 | B·C에서 **8** · `Spacing/200` |
| C의 상세보기 | 설정 행 아래 **12** · `Spacing/300`, 별도 Text Button 사용 |
| D의 구성 | 폭 **320**의 세로 묶음, 설정 행과 보조 설명을 순서대로 배치, 요소 사이 **8** · `Spacing/200` |
| Slot | 좌측·상단 정렬, 패딩 **0**. A~C의 Slot 간격은 8, D는 0이며 각 Slot에는 ‘화면’ 프레임 1개가 있어요. |
| 문서 섹션 | 원본 컴포넌트 섹션과 동일하게 흰 배경, 모서리 **24**, 테두리 없음. 색상·모서리 토큰 연결 유지 |

A의 `itemSpacing=169`는 Space between 행에 저장된 값이에요. 요소 사이의 고정 간격 규칙으로 사용하지 않아요. B·C의 320, A의 328, 텍스트 폭 262 역시 현재 문서 배치 수치이며 모든 제품 화면의 고정 폭을 뜻하지 않아요.

### 구성과 상태 선택

- `Check`와 `Disabled`는 실제 VARIANT 속성이에요. 값은 각각 `On` / `Off`, `False` / `True`이며 임의로 `State`, `Checked` 같은 속성명으로 바꾸지 않아요.
- 현재 마스터의 기본값은 Check=On · Disabled=False예요. 새 화면의 초기값은 서비스 조건과 실제 설정 값으로 정하고, 마스터 기본값을 그대로 사용자 설정 값으로 해석하지 않아요.
- 기존 Switch 인스턴스를 재사용하고, 별도 도형으로 손잡이나 배경을 다시 그리지 않아요. 현재 비활성 색·투명도 표현도 마스터를 따라요.
- 설정 이름, 보조 설명, 상세보기는 Switch 내부 속성이나 슬롯이 아니에요. 상황에 필요한 주변 요소로 따로 배치해요. 상세보기는 내용을 확인하는 동작이고 Switch는 설정 값을 변경하는 동작이에요.
- 가이드라인의 비교는 모두 유효한 상태·구성 사례예요. 템플릿에 남아 있는 Do / Don’t 레이어 이름만 보고 오른쪽 사례를 금지 사례로 해석하지 않아요.
- 예제의 ‘화면’ 프레임은 설정 이름·설명·Switch 등 관련 요소를 함께 정렬하기 위한 보조 컨테이너예요. 실제 제품 화면 전체를 복제한 것이 아니며, Slot에 불필요한 추가 패딩을 넣지 않아요.
- 문서 설명 끝과 Slot 사이 간격은 **50**을 유지해요. 예제끼리 시각 요소의 시작 높이를 맞추는 것은 문서 레이아웃 기준이에요.
- 기존 값과 같은 현재 시럽 토큰을 사용해요. 이전 `spacing/spacing_400`, `spacing/spacing_200` 등을 신규 예제에 다시 연결하지 않아요. 숫자가 회색으로 보이는 것만으로 미바인딩이라고 판단하지 않고 실제 연결 토큰을 확인해요.
- 아래 기존 점검 기록의 네이밍·비활성 표현 개선 제안은 확정된 사용 규칙이 아니에요. 이번 작업은 사용 가이드와 예제 문서화이며 마스터의 상태 속성이나 비활성 방식을 변경하지 않았어요.

---

## 설계 규칙 요약

### 상태 4종

```
          Disabled=False        Disabled=True
Check=On  주황 · 손잡이 오른쪽   주황 @30% · 손잡이 오른쪽
Check=Off 회색700 · 손잡이 왼쪽  회색850 · 손잡이 왼쪽
```

손잡이는 항상 **흰색 20 × 20 원**으로 네 상태 모두 같습니다. 바뀌는 것은 **배경색과 손잡이 위치**뿐입니다.

### 토큰 적용 상태

| 항목 | 상태 |
| --- | --- |
| 배경 | `Primary_Orange` · `Gray_700` · `Gray_850` ✅ |
| 손잡이 | `Color/Gray_White` ✅ |
| Padding · Gap | `Spacing/50` ✅ |
| 라운드 | `Corner radius/circle` ✅ |
| 미바인딩 색상 | **0건** ✅ |
| 미바인딩 수치 | **0건** ✅ (보드 영역 제외) |
| 원격 텍스트 스타일 | **0건** ✅ |
| 스타일 미적용 텍스트 | **0건** ✅ |
| 줄 구분자(U+2028/9) | **0건** ✅ |

**컴포넌트 내부에 미바인딩이 하나도 없습니다.** [Result](syrup-result-components.md) · [Search Field](syrup-search-field-components.md)와 함께 토큰 적용이 가장 깨끗한 축입니다.

### 타 페이지 의존

| 출처 | 컴포넌트 | 건수 |
| --- | --- | --- |
| ❖System Components | `Title Bar` 1 · `Section Header` 1 | 2 |

컴포넌트 내부 참조와 외부 라이브러리 인스턴스가 모두 **0건**입니다.

---

## 점검 필요 사항

> 아래는 2026-10-12에 기록한 구조 점검과 개선 제안이에요. 2026-11-10에는 가이드라인·Usage, 최신 예제 디자인과 토큰 연결을 반영했어요. 파일 전체 집계나 인스턴스 0건은 현재 수치가 아니에요.

### 1. 컴포넌트명 `switch` 소문자 — ✅ 완료

| 항목 | 값 |
| --- | --- |
| 페이지명 | `Switch` |
| 컴포넌트명 | ~~`switch`~~ → **`Switch`** ✅ |

파일 전체 **컴포넌트 247개**(Set 178 · Component 69) 중 소문자로 시작하는 것은 **8개**뿐이었습니다.

| 페이지 | 이름 | 성격 |
| --- | --- | --- |
| Foundation | `table / column / header` · `table / row / header` ×3 · `value` · `syrup_app_icon` | **문서용 표 · 에셋** |
| [AD](syrup-ad-components.md) | `pocket` | UI 컴포넌트 |
| ~~Switch~~ | ~~`switch`~~ | **해소** ✅ |

Foundation의 6개는 스펙 문서를 그리는 요소라 성격이 다릅니다. 이제 **실제 UI 컴포넌트 중 소문자는 [AD](syrup-ad-components.md)의 `pocket` 하나만** 남았습니다.

2026-10-12 당시 집계에서는 인스턴스가 **0건**이었어요. 현재 사용량을 뜻하지 않아요.

[Search Field](syrup-search-field-components.md)의 `SearchField` → `Search Field` 개명과 같은 성격입니다.

### 2. 비활성 표현이 두 방식

| Check | Disabled=False | Disabled=True | 방식 |
| --- | --- | --- | --- |
| `On` | `Primary_Orange` · 투명도 1 | `Primary_Orange` · **투명도 0.3** | **투명도** |
| `Off` | `Gray_700` | **`Gray_850`** · 투명도 1 | **색 교체** |

같은 `Disabled=True`인데 **한쪽은 투명도를 낮추고 한쪽은 색을 바꿉니다.**

#### 두 방식의 차이

| 방식 | 결과 | 배경 영향 |
| --- | --- | --- |
| 투명도 0.3 | 뒤 배경이 비쳐 보임 | **배경색에 따라 달라 보임** |
| 색 교체 (`Gray_850`) | 항상 같은 색 | 일정 |

투명도 방식은 **흰 배경과 회색 배경에서 다르게 보입니다.** 손잡이(흰 원)도 함께 흐려져 대비가 떨어집니다.

| 선택지 | 내용 |
| --- | --- |
| A | `On, Disabled=True`도 **색 교체**로 — 주황의 흐린 버전 토큰 필요 |
| B | `Off, Disabled=True`도 **투명도**로 — `Gray_700` @30% |
| C | 현행 유지 — 의도된 차이 |

A는 토큰이 없어 신설이 필요하고, B는 `Gray_850`을 쓰지 않게 됩니다. **디자인 의도 확인이 필요합니다.**

[Checkbox](syrup-checkbox-components.md)의 비활성 처리 방식과 맞추는 것도 기준이 됩니다.

### 3. 폭 42.48 1건 — ✅ 완료

| Variant | 수정 전 | 수정 후 | 손잡이 x |
| --- | --- | --- | --- |
| `Check=On, Disabled=False` | 42 | 42 | 20 |
| `Check=Off, Disabled=False` | 42 | 42 | 2 |
| **`Check=On, Disabled=True`** | **42.48** | **42** ✅ | 20.48 → **20** ✅ |
| `Check=Off, Disabled=True` | 42 | 42 | 2 |

혼자만 0.48 넓었고, MAX 정렬이라 손잡이 x도 20.48로 밀려 있었습니다.

화면에서 0.48px는 보이지 않지만, **네 variant가 같은 크기여야 할 토글에서 하나만 다른 것**은 수치를 만지다 남은 흔적이었습니다.

**폭만 42로 고치니 오토레이아웃이 손잡이 위치를 다시 계산해 x가 20으로 따라왔습니다.** 네 variant가 모두 42 × 24로 맞았습니다.

### 4. `Disabled` 옵션 순서

| 속성 | 옵션 순서 | 기본값 |
| --- | --- | --- |
| `Check` | `Off` · `On` | **`On`** |
| `Disabled` | **`True` · `False`** | **`False`** |

`Disabled`의 옵션 순서가 `True` 먼저인데 **기본값은 `False`**입니다. 드롭다운 첫 항목과 실제 기본값이 다릅니다.

[Stepper](syrup-stepper-components.md)에서 확인한 대로 **레이어 재정렬로는 드롭다운 표시 순서가 바뀌지 않고, 값을 개명해야만 다시 계산**됩니다. 기본값은 이미 `False`로 맞으므로 **표시 순서만 남은 문제**입니다.

`Check`도 옵션은 `Off` 먼저인데 기본값은 `On`입니다. 두 속성 모두 같은 상태라 **일관되게 어긋나 있습니다.**

현행 유지가 무난합니다.

### 5. `Check` 속성명

| 현재 | 값 | 제안 |
| --- | --- | --- |
| `Check` | `Off` · `On` | `State` 또는 `Checked` |

`Check`는 동사로 읽히는데 값은 상태(`Off`/`On`)입니다. 「체크하라」인지 「체크됨」인지 이름만으로는 모호합니다.

| 이름 | 어울리는 값 |
| --- | --- |
| `Check` | — |
| **`State`** | `Off` · `On` ✅ |
| **`Checked`** | `False` · `True` |

값을 `Off`/`On` 그대로 둘 것이므로 **`State`가 자연스럽습니다.** [Search Field](syrup-search-field-components.md) · [Swipe](syrup-swipe-components.md)도 같은 개념에 `State`를 씁니다.

다만 [Checkbox](syrup-checkbox-components.md)가 쓰는 속성명과 맞추는 편이 더 나을 수 있어 **함께 확인이 필요합니다.**

### 6. 인스턴스 0건 — 2026-10-12 기록

| 구분 | 인스턴스 |
| --- | --- |
| `Switch` | **0** |

당시에는 이 파일에서 사용 인스턴스가 집계되지 않았어요. 현재는 가이드라인·Usage에 설정 이름, 보조 설명, Text Button과 조합한 사용 예제가 있으므로 과거 0건을 근거로 변경 영향이 없다고 판단하지 않아요.

제품 화면 파일의 사용량은 별도로 확인해야 해요. 이 문서는 파일 전체 인스턴스 수를 다시 집계한 문서가 아니에요.

### 7. 레이어명 — 정리 대상 아님

`Oval`(손잡이)은 Figma 기본 이름처럼 보이지만 **파일 전체에서 237건** 쓰입니다.

| 이름 | 파일 전체 |
| --- | --- |
| `Ellipse` | 238 |
| **`Oval`** | **237** |

두 이름이 거의 같은 비중으로 쓰여 **`Oval`을 기본 이름으로 보고 고치면 237건과 어긋납니다.** 정리 대상에서 제외합니다.

> [Progress Stepper](syrup-progress-stepper-components.md)에서 `🟧` 이모지를 정리 대상으로 잘못 짚었던 것과 같은 유형입니다. **기본 이름처럼 보이는 것도 파일 전체 분포를 먼저 확인**해야 합니다.

---

## 정리 우선순위

### 문서 업데이트 완료 (2026-11-10)

가이드라인 3개와 Usage A~D, 가이드라인 2번 및 예제 B·C의 최신 문구, 사용자가 통일한 설정 이름·보조 설명·간격·프레임 구성을 반영했어요. 이전 토큰 대신 같은 값의 현재 시럽 토큰을 사용하는 기준과 문서 섹션의 통일된 스타일도 정리했어요.

### ✅ 완료 (2026-10-12)

모양이 바뀌지 않는 작업 **2건**을 처리했습니다.

| # | 항목 | 결과 |
| --- | --- | --- |
| 1 | `switch` → `Switch` ([1](#1-컴포넌트명-switch-소문자---완료)) | 인스턴스 0건 |
| 2 | 폭 42.48 → 42 ([3](#3-폭-4248-1건---완료)) | 손잡이 x도 20.48 → 20 자동 반영 |

네 variant가 모두 **42 × 24**로 맞았고, 파일의 소문자 UI 컴포넌트는 [AD](syrup-ad-components.md)의 `pocket` 하나만 남았습니다.

### 남은 과제

| 순위 | 항목 | 성격 | 비용 |
| --- | --- | --- | --- |
| 1 | `Check` → `State` ([5](#5-check-속성명)) | **Checkbox와 함께 판단** | 낮음 |
| 2 | 비활성 표현 통일 ([2](#2-비활성-표현이-두-방식)) | **디자인 의도 확인** | 중간 |
| 3 | `Disabled` 옵션 표시 순서 ([4](#4-disabled-옵션-순서)) | 현행 유지 권장 | — |

기존 23개 노드 집계는 마스터 섹션의 과거 기록이에요. 현재 문서 예제까지 포함한 페이지 전체 노드 수나 모든 값의 토큰 적용 상태로 확대 해석하지 않아요. 위 과제는 마스터의 기존 개선 제안이에요.

가장 생각해 볼 지점은 **[점검 2의 비활성 표현](#2-비활성-표현이-두-방식)** 입니다. `On`은 투명도 0.3, `Off`는 색 교체로 처리해 **배경색에 따라 `On` 비활성만 다르게 보입니다.** [Checkbox](syrup-checkbox-components.md)의 처리 방식과 맞춰 결정하는 편이 좋습니다.
