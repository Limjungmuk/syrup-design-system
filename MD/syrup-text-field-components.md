# Syrup Design System — Text Field 컴포넌트

| 항목 | 값 |
| --- | --- |
| Figma File | [Syrup_Design-System](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System) |
| Page / Section | `Text Field` 페이지 → [Text Field 섹션 `8795:37747`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=8795-37747) |
| 마스터 섹션 크기 | 최신 Figma 원본 배치 기준 |
| 컴포넌트 수 | 입력 3종 + 보조 Character Progress 1종 |
| Variant 총수 | **31개** (20 · 4 · 2 + 보조 5) |
| 기준일 | 2026-11-23 (자동 높이·하단 표시·Guidelines 8개·Usage A~I) |
| 관련 문서 | [syrup-design-tokens.md](syrup-design-tokens.md) · [syrup-ad-components.md](syrup-ad-components.md) · [syrup-alert-components.md](syrup-alert-components.md) · [syrup-badge-components.md](syrup-badge-components.md) · [syrup-banner-components.md](syrup-banner-components.md) · [syrup-border-components.md](syrup-border-components.md) · [syrup-bottom-cta-components.md](syrup-bottom-cta-components.md) · [syrup-bottom-info-components.md](syrup-bottom-info-components.md) · [syrup-bottom-sheet-components.md](syrup-bottom-sheet-components.md) · [syrup-bubble-components.md](syrup-bubble-components.md) · [syrup-button-components.md](syrup-button-components.md) · [syrup-card-components.md](syrup-card-components.md) · [syrup-checkbox-components.md](syrup-checkbox-components.md) · [syrup-chip-components.md](syrup-chip-components.md) · [syrup-dialog-components.md](syrup-dialog-components.md) · [syrup-dim-components.md](syrup-dim-components.md) · [syrup-grid-list-components.md](syrup-grid-list-components.md) · [syrup-grid-scroll-components.md](syrup-grid-scroll-components.md) · [syrup-header-components.md](syrup-header-components.md) · [syrup-icon-button-components.md](syrup-icon-button-components.md) · [syrup-indicator-components.md](syrup-indicator-components.md) · [syrup-keypad-components.md](syrup-keypad-components.md) · [syrup-label-components.md](syrup-label-components.md) · [syrup-list-footer-components.md](syrup-list-footer-components.md) · [syrup-list-header-components.md](syrup-list-header-components.md) · [syrup-list-row-components.md](syrup-list-row-components.md) · [syrup-loader-components.md](syrup-loader-components.md) · [syrup-lottie-components.md](syrup-lottie-components.md) · [syrup-product-grid-components.md](syrup-product-grid-components.md) · [syrup-product-list-components.md](syrup-product-list-components.md) · [syrup-product-scroll-components.md](syrup-product-scroll-components.md) · [syrup-progress-stepper-components.md](syrup-progress-stepper-components.md) · [syrup-result-components.md](syrup-result-components.md) · [syrup-search-field-components.md](syrup-search-field-components.md) · [syrup-stepper-components.md](syrup-stepper-components.md) · [syrup-swipe-components.md](syrup-swipe-components.md) · [syrup-switch-components.md](syrup-switch-components.md) · [syrup-tab-components.md](syrup-tab-components.md) · [syrup-tab-bar-components.md](syrup-tab-bar-components.md) · [syrup-text-button-components.md](syrup-text-button-components.md) · [syrup-ticker-components.md](syrup-ticker-components.md) · [syrup-toast-components.md](syrup-toast-components.md) |

> **사용자가 텍스트를 입력하거나 수정할 수 있는 입력 컴포넌트에요.**
> 검색, 정보 입력, 의견 작성 등 사용자 입력이 필요한 영역에 사용해요.

---

## 목차

1. [구성 한눈에 보기](#구성-한눈에-보기)
2. [Text Field — Master Component](#1-text-field--master-component)
3. [Text Field / Text Area](#2-text-field--text-area)
4. [Text Field / Task](#3-text-field--task)
5. [가이드라인](#가이드라인)
6. [Usage — 사용 예제](#usage--사용-예제)
7. [문서용 정렬 설정과 실제 사용 규격](#문서용-정렬-설정과-실제-사용-규격)
8. [설계 규칙 요약](#설계-규칙-요약)
9. [점검 필요 사항](#점검-필요-사항)
10. [정리 우선순위](#정리-우선순위)

---

## 구성 한눈에 보기

현재 마스터 섹션의 크기는 최신 Figma 배치를 기준으로 해요. 아래 보드 위치는 과거 점검 기록이에요. 기존 노드 192개·텍스트 64개, 아래 보드 위치·인스턴스 0건은 2026-10-12 점검 기록으로, 현재 페이지 전체 집계가 아니에요.

| 보드 위치 | 섹션 | 내용 |
| --- | --- | --- |
| y 0 | Title Bar | 페이지 제목 |
| y 434 | Section Header | Master Component |
| y 574 | (높이 1,411) | 컴포넌트 3종 |

| # | 이름 | 타입 | Variant 축 | 크기 | 인스턴스 |
| --- | --- | --- | --- | --- | --- |
| 1 | `Text Field` | **Set 20** | `State`(7) × `Type`(4) | 360 × 80 (모든 상태 FIXED) | **0** |
| 2 | `Text Field / Text Area` | Set 4 | `Filled` × `Auto Height` | 폭 312 · 최소 높이 80 | **0** |
| 3 | `Text Field / Task` | Set 2 | `Filled` | 326 × 64 | **0** |

Text Area는 하단 표시용 Character Progress 보조 컴포넌트를 사용해요. 입력 3종의 Variant 26개와 보조 5개를 구분해요.

---

## 1. Text Field — Master Component

**Node** `8795:37778` · Component Set · **20 variants**

| Property | Type | Options |
| --- | --- | --- |
| `State` | VARIANT | `Inactive` · `Focused` · `Typing` · `Error` · `Complete` · **`Complete_Time`** · **`Focused_Time`** |
| `Type` | VARIANT | `Birth` · `Text` · **`Text+Arrow`** · **`Text+Button`** |

7 × 4 = 28 중 **20개만** 존재합니다 → [점검 5](#5-variant-매트릭스-2028)

### 플로팅 라벨 방식

| State | 구조 | 라벨 |
| --- | --- | --- |
| `Inactive` | `field` 하나 | 입력란 자리에 **17 Regular** `Color/Gray_500` |
| `Focused` 이후 | 라벨 + `field` 2단 | **위로 올라가 14 Regular** `Color/Gray_500` |

입력이 시작되면 안내문구가 **작아지며 위로 올라가고**, 입력란에는 17 Medium `Color/Gray_100` 글자가 들어갑니다.

### State별 밑줄 색

| State | 밑줄 | 특징 |
| --- | --- | --- |
| `Inactive` | `Color/Gray_800` ✅ | 라벨이 입력란 자리에 |
| `Focused` | `Color/Gray_100` ✅ | `cursor` 1 × 26 표시 |
| `Typing` | `Color/Gray_100` ✅ | `leading` 묶음 + `cursor` + Close 아이콘 |
| `Complete` | `Color/Gray_800` ✅ | 입력값만 |
| **`Error`** | **`Color/Secondary_Red`** ✅ | 하단 예약 영역에 오류 안내문 표시 (전체 높이 80 유지) |
| `Complete_Time` · `Focused_Time` | `Color/Gray_800` ✅ | `counttime` 「2:51」 `Color/Primary_Orange` |

밑줄은 **`field` 프레임의 하단 테두리**(`strokeBottomWeight` 1)로 그립니다. [Text Button](syrup-text-button-components.md)의 `Underline`과 같은 방식입니다.

### 높이와 실제 사용 패딩 — 2026-11-10

| 항목 | 실제 사용 규격 |
| --- | --- |
| 전체 높이 | **80 고정** · 20개 베리언트 공통 |
| 입력 영역 | 위쪽 **60** · 입력 밑줄 기준선 y=60 |
| 하단 안내 영역 | **20 예약** · 오류가 없어도 유지 |
| 좌우 패딩 | **왼쪽 24 / 오른쪽 24** · `Spacing/600` |
| 오류가 없는 상태 | 하단 Padding 20으로 안내 공간 확보 |
| Error 상태 | 입력 영역 아래 Gap 2 + 오류 문구 한 줄 18 = 20 |
| 상단 패딩 | 0 |

기존 60·63·80이 혼재한 구조를 통일했어요. 일반 상태는 라벨 18 + Gap 2 + field 40 = 60이고, Inactive는 field 60으로 같은 밑줄 위치를 유지해요. 오류 문구가 나타나도 전체 높이와 다음 요소의 위치가 바뀌지 않도록 해요.

오류 문구는 한 줄 기준이에요. 두 줄 이상의 설명을 넣을 때 임의로 높이 80 안에 압축하거나 잘라 넣지 않아요. 이 높이 규칙은 기본 `Text Field`에 적용하며 `Text Area`와 `Task`는 각자 규격을 유지해요.

문서의 왼쪽 패딩 0은 아래 [문서용 정렬 설정](#문서용-정렬-설정과-실제-사용-규격)을 참고해요. 실제 화면에서 왼쪽 패딩을 0으로 쓰는 규칙이 아니에요.

### Type별 구성

| Type | 구성 |
| --- | --- |
| `Text` | `field` ▸ 텍스트 |
| `Birth` | `field` ▸ `1`(생년월일 6자리) + `-` + `2`(주민번호 앞자리 + 마스킹) |
| `Text+Arrow` | `field` ▸ 텍스트 + `Icon / Arrow` 20 × 20 |
| `Text+Button` | `field`(232폭) + [Button](syrup-button-components.md) 64 × 38 |

`Birth`만 **입력란을 둘로 쪼개고** 가운데 `-`를 둡니다.

---

## 2. Text Field / Text Area

**Node** `10002:64297` · Component Set · **4 variants** · 폭 **312**, 최소 높이 **80**

| 속성 | 지원 값과 의미 |
| --- | --- |
| Filled | False / True · 입력 내용 유무이며 완료 검증과 별개 |
| Auto Height | False / True · 지정 높이·내부 스크롤 / 내용에 따른 확장·축소 |
| Character Progress | False / True · 하단 표시 여부, 기본 False |

세로 오토레이아웃, 사방 패딩 16, Text Container와 하단 표시 사이 Gap 16, 라운드 10을 유지해요. 본문은 15 Regular·행간 19, 하단은 높이 20·13 Regular·아이콘/숫자 간격 4예요. Text Container 안의 Placeholder / Text 레이어를 수정해요. 과거 `총 보유 SCON Credit` 레이어명은 현재 규격이 아니에요.

Filled=False는 회색 테두리, True는 주황 테두리예요. False를 Disabled로 해석하지 않아요. 고정형의 260px은 샘플 설정이며 모든 사용처의 필수 높이가 아니에요. Auto Height=True는 최소 80px부터 실제 본문 높이에 맞추고, 삭제와 폭 변경에도 다시 계산해요. 표시를 켜면 본문과 겹치지 않게 하단 20px과 Gap 16px을 확보해요.

### Character Progress

보조 세트 `12368:10793`의 지원 조합은 Progress의 Default / In Progress / Ready / Complete와 Counter의 Default, 총 5개예요. Counter에 다른 상태가 있다고 가정하지 않아요.

- Type=Progress: 좌측 하단의 주황 원형 진행률 + 남은 글자 수. 조건 충족 시 주황 원 안의 흰 체크와 0을 유지해요.
- Type=Counter: 우측 하단 현재/최대 글자 수. 향후 확장용이며 현재 서비스 적용 사례는 없어요.
- 표시 On/Off와 유효성 검증은 별개예요. 금한돈 당첨 후기는 최소 50자·최대 100자예요(2026-11-25 변경). Progress의 완료 기준 50과 최대 입력 제한 100을 구분하며, 이 정책을 다른 사용처의 공통 제한으로 적용하지 않아요.

### 입력·재생 조건
공백과 줄바꿈을 포함한 화면 입력값을 Unicode 코드 포인트 단위(`Array.from(value).length`)로 계산해요. 한글 조합 중에도 화면 글자 수가 기준에 도달해 남은 수가 0이 되는 즉시 완료를 표시해요. 초과 입력의 남은 수는 0으로 유지해요. 입력값이 비어 진행률이 0이면 주황색 진행 선을 완전히 숨겨요. 조건 미만으로 삭제한 뒤 다시 충족하면 완료 모션이 재생돼요.

완료 원은 20×20px을 유지하며 560ms 동안 scale 0.55→1.18→0.92→1.06→1로 나타나요. 흰 체크는 120ms 뒤부터 320ms 동안 드러나요. 모션 줄이기 환경에서는 최종 상태를 즉시 표시해요.

웹 상단은 초기 플레이스홀더 2초 후 후기를 자음·모음 단위로 입력하고 잠시 유지한 뒤 빠르게 지우며 반복해요. 직접 클릭·입력하면 멈추고 값을 유지해요. 모두 지우고 입력 영역을 벗어나면 초기 2초 대기부터 다시 시작해요. 값이 남아 있으면 자동 재생하지 않아요. 하단 표시·유형 선택 설정은 기본 숨김이며 필요할 때만 다시 켤 수 있어요. 일시정지 버튼은 기존 우측 하단 위치를 유지해요.

---

## 3. Text Field / Task

**Node** `10002:64210` · Component Set · **2 variants** · **326 × 64**

| Property | Options |
| --- | --- |
| `Filled` | `False` · `True` |

가로 오토레이아웃 CENTER · Padding `20 / 24 / 20 / 20` (`Spacing/500` · `600` ✅) · 배경 `Color/Gray_White` ✅ · 라운드 16 (`Corner radius/400` ✅)

| Filled | 테두리 | 구성 | Gap |
| --- | --- | --- | --- |
| `False` | `Color/Primary_Orange` ✅ | `Image` + `Text`(「직접 입력하기」) + [Checkbox](syrup-checkbox-components.md) | 8 (`Spacing/200`) |
| `True` | `Color/Primary_Orange` ✅ | `Frame 1171277247` ▸ `Image` + `Frame 1171277247` + Checkbox | 20 (`Spacing/500`) |

**두 상태 모두 테두리가 주황**입니다. `Text Area`가 `Gray_800` → `Primary_Orange`로 바뀌는 것과 다릅니다.

`Filled=True`에서만 **래퍼 프레임이 한 겹 더** 생기고, 그 안에 **같은 이름(`Frame 1171277247`)이 2겹 중첩**돼 있습니다.

`Filled=False`의 `Text`는 **17 Regular 스타일 미적용**입니다 → [점검 3](#3-스타일-미적용-텍스트-1건)

---

## 가이드라인

[Figma Guidelines](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11787-940)

### 1. 입력할 내용에 맞는 컴포넌트를 사용해요

이름처럼 짧은 정보는 Text Field, 할 일 목록에서 직접 입력하는 항목은 Text Field / Task를 사용해요.
의견이나 소감처럼 여러 줄의 내용은 Text Field / Text Area로 구성해요.

- 비교: Text Field · 기본 입력 / Task · 할 일 직접 입력
- [가이드라인 1](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11787-942)

### 2. 입력 상태에 맞게 표시해요

입력 전은 Inactive, 포커스가 있으면 Focused, 입력 중은 Typing, 입력 후에는 Complete를 사용해요.
입력 영역 60과 하단 안내 영역 20을 포함해 모든 상태의 전체 높이를 80으로 유지해요.
하단 안내 영역은 오류가 있을 때 사용해요. Complete는 입력 상태이며 인증 성공을 의미하지 않아요.

- 비교: Inactive → Focused / Typing → Complete
- [가이드라인 2](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11787-995)

### 3. 선택과 실행 기능을 구분해요

목록에서 값을 선택하는 입력에는 Text+Arrow를 사용해요. 입력값과 관련된 요청을 실행할 때는 Text+Button을 사용해요.
선택한 값이나 요청 결과에 맞춰 문구와 상태를 함께 변경해요.

- 비교: Text+Arrow · 값 선택 / Text+Button · 요청 실행
- [가이드라인 3](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11787-1055)

### 4. 인증 정보에 맞는 입력 유형과 상태를 사용해요

생년월일과 추가 식별 정보를 입력할 때는 Birth의 구분과 마스킹을 유지해요.
인증번호 입력에는 시간 표시 상태를 사용하고, 만료 등 오류가 발생하면 Error와 구체적인 안내를 보여줘요.

- 비교: Birth · 구분과 마스킹 / 인증번호 · 시간 표시와 오류
- 만료 오류 예제는 시간 0:00과 「인증번호가 만료되었습니다.」를 함께 표시해요. 기본 마스터의 2:51 샘플값은 오류 예제에서 별도로 수정했어요.
- [가이드라인 4](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11787-1107)

### 5. 여러 줄의 내용은 Text Area로 입력해요

의견이나 당첨 후기처럼 여러 줄의 내용에는 Text Field / Text Area를 사용해요. 비어 있으면 Filled=False, 내용이 있으면 Filled=True로 표시해요. 최소 작성 조건과 최대 입력 제한을 구분해요.

### 6. 화면 목적에 맞게 높이를 고정하거나 자동으로 늘려요

Auto Height=False는 지정한 높이를 유지하고 넘치는 본문은 내부 스크롤해요. True는 최소 높이 80px부터 실제 줄바꿈·입력량·폭에 따라 늘어나고, 삭제하면 줄어들어요. 글자 수로 높이를 계산하지 않아요. 사방 패딩 16px, 본문과 하단 표시 사이 간격 16px, 하단 표시 높이 20px을 유지해요.

### 7. 글자 수 안내가 필요할 때만 하단 표시를 켜요

Character Progress로 하단 표시를 켜거나 꺼요. Type=Progress는 좌측 원형 진행률과 남은 글자 수, Type=Counter는 우측 현재/최대 글자 수예요. 함께 사용하지 않아요. 표시를 꺼도 입력값과 작성 조건 검증은 유지해요.

### 8. 필수 작성 조건과 최대 글자 수를 구분해요

금한돈 당첨 후기 미션은 최소 50자 작성이 필수이고 최대 100자까지 입력해요(2026-11-25 변경). Progress는 50자를 기준으로 입력할수록 채워지고 조건 충족 즉시 체크와 0을 표시해요. 50자를 충족한 뒤에도 최대 100자까지 작성할 수 있어요. 삭제해 조건 미만이면 진행 중으로 돌아가요. 최소 조건은 최대 입력 제한이나 리워드 지급 완료가 아니에요. Counter는 향후 확장용이며 현재 서비스 사용 사례는 없어요. 웹 상단만 30글자 완료 시연이에요.

---

## Usage — 사용 예제

[Figma Usage](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11787-941)

| 예제 | 설명 | 구성 | 링크 |
| --- | --- | --- | --- |
| A. 기본 정보 입력 | 이름처럼 짧은 정보를 입력해요. 입력 영역 60과 안내 영역 20을 포함한 전체 높이 80을 유지해 상태가 바뀌어도 주변 요소가 움직이지 않도록 해요. | Text · Focused / Complete | [A](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11787-1206) |
| B. 목록에서 값 선택 | 통신사처럼 정해진 목록에서 값을 선택해요. Text+Arrow를 사용하고 선택한 값을 입력 영역에 보여줘요. | Text+Arrow · Inactive / Complete | [B](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11787-1229) |
| C. 인증 요청과 번호 입력 | 휴대폰번호 입력 옆에서 인증을 요청하고, 인증번호 입력에는 남은 시간을 함께 보여줘요. 인증번호를 입력한 상태와 인증 성공은 구분해요. | Text+Button · Complete + Text · Complete_Time | [C](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11787-1255) |
| D. 생년월일 입력 | Birth를 사용해 생년월일과 추가 식별 정보를 구분해요. 민감한 정보는 기존 컴포넌트의 마스킹 방식으로 표시해요. | Birth · Complete | [D](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11787-1285) |
| E. 할 일 직접 입력 | 목록에서 원하는 할 일을 직접 입력해요. 내용이 없으면 Filled=False, 입력한 내용이 있으면 Filled=True로 표시해요. | Task · Filled=False / True · 예제 폭 328, 높이 64 | [E](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11787-1310) |
| F. 의견과 소감 작성 | 여러 줄 의견을 입력하고 하단 안내는 필요할 때만 켜요. | Text Area · Filled | [F](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11787-1344) |
| G. 고정 높이와 자동 높이 | 지정 높이·내부 스크롤과 최소 80px부터 내용에 따른 확장·축소를 비교해요. | Text Area | [G](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=12387-705) |
| H. 필수 후기 작성 진행률 | 금한돈 당첨 후기의 최소 50자·최대 100자와 입력 전·진행 중·완료·재입력 조건을 안내해요. | Text Area | [H](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=12387-740) |
| I. 선택형 글자 수 카운터 | 우측 현재/최대 글자 수를 표시하는 확장용 예시예요. | Text Area | [I](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=12387-775) |

## 문서용 정렬 설정과 실제 사용 규격

| 항목 | 실제 화면·마스터 | Guidelines·Usage의 문서용 인스턴스 |
| --- | --- | --- |
| 적용 대상 | 기본 Text Field 20개 베리언트 | 기본 Text Field 인스턴스 17개만 |
| 왼쪽 패딩 | **24** (`Spacing/600`) | **0** (`Spacing/0`) · 문서 제목과 입력 내용의 왼쪽 시작점을 맞추기 위한 오버라이드 |
| 오른쪽 패딩 | **24** | **24 유지** |
| 전체 높이 | **80 고정** | **80 고정** |
| 입력 영역·밑줄 | **60 · y=60** | 동일 |
| 하단 안내 영역 | **20 예약** | 동일 |

문서 인스턴스의 왼쪽 패딩 0을 실제 제품의 기본 패딩으로 복사하지 않아요. 실제 사용은 마스터의 왼쪽·오른쪽 24를 기준으로 해요. 문서용 오버라이드는 마스터나 Section 1에 적용하지 않았어요.

Text Area의 내부 패딩 16, Task의 왼쪽 20·오른쪽 24는 각 컴포넌트 고유 규격으로 유지했어요. 이 두 컴포넌트에 문서용 왼쪽 패딩 0을 일괄 적용한 것이 아니에요.

### 예제 레이아웃과 AI 사용 기준

- Guidelines와 Usage는 최신 Figma 섹션 배치를 기준으로 해요. 기존 섹션의 흰 배경·모서리 24를 사용해요.
- Slot은 폭 360, 패딩 0, 좌측·상단 정렬, 높이 Hug예요. 관련 컴포넌트를 직접 넣고 별도 ‘화면’ 래퍼를 만들지 않았어요.
- 제목·설명 영역 끝과 Slot 사이 간격은 50이에요. Usage 설명 영역 높이를 맞춰 예제 시작점을 정렬했어요.
- Slot 패딩 0과 기본 Text Field의 문서용 왼쪽 패딩 0은 서로 다른 설정이에요. Slot은 문서 배치 컨테이너이고, Text Field 패딩은 컴포넌트 내부 규격이에요.
- 기본 Text Field의 Type·State에는 실제 존재하는 조합만 사용해요. Text+Arrow에 Typing·Error, Birth 등에 시간 표시 상태가 있다고 가정하지 않아요.
- Complete는 값 입력 후의 표시 상태예요. 별도의 검증 없이 인증 성공·요청 성공·제출 완료로 해석하지 않아요.
- Text Area·Task의 Filled는 입력 내용 유무를 나타내요. 기본 Text Field의 State와 같은 속성으로 취급하지 않아요.
- 글자 수 제한은 사용처별 규칙이에요. 50자·200자·500자 샘플을 모든 입력 컴포넌트의 공통 제한으로 사용하지 않아요.
- Auto Height=True는 실제 입력과 줄바꿈에 따라 확장·축소해요. False는 지정 높이와 내부 스크롤을 유지해요.

---

## 설계 규칙 요약

> 아래 토큰·스타일 건수는 과거 마스터 보드 점검 기록이에요. 이번에 확인한 높이·패딩 규격과 사용 문서 외의 전체 토큰 재점검 결과는 아니에요.

### 세 컴포넌트의 입력 영역 표현이 다릅니다

| 컴포넌트 | 입력 영역 | 비활성 | 활성 |
| --- | --- | --- | --- |
| `Text Field` | **하단 밑줄만** | `Gray_800` | `Gray_100` |
| `Text Field / Text Area` | **사각 테두리** (라운드 10) | `Gray_800` | `Primary_Orange` |
| `Text Field / Task` | **사각 테두리** (라운드 16) | `Primary_Orange` | `Primary_Orange` |

한 페이지 안에서 **밑줄형과 박스형이 공존**하고, 활성 색도 `Gray_100` / `Primary_Orange`로 갈립니다. 용도가 다른 입력이라 의도된 구분으로 보이나 **기준을 문서로 남겨둘 필요**가 있습니다.

### 토큰 적용 상태

| 항목 | 상태 |
| --- | --- |
| 밑줄 · 테두리 색 | `Gray_100` · `Gray_800` · `Primary_Orange` · `Secondary_Red` ✅ |
| 텍스트 색 | `Gray_100` · `Gray_200` · `Gray_500` · `Gray_600` · `Gray_700` · `Primary_Orange` · `Secondary_Red` ✅ |
| 배경 | `Color/Gray_White` ✅ |
| Padding · Gap | `Spacing/50`~`600` ✅ |
| 라운드 | `Corner radius/150` · `250` · `400` ✅ — **1 ×8건 미바인딩** |
| 텍스트 스타일 | 6종 적용 ✅ — **미적용 1건** |
| 미바인딩 색상 | **0건** ✅ |
| 원격 텍스트 스타일 | **0건** ✅ |
| **줄 구분자(U+2028/9)** | **1건** (보드 설명문) |

**색은 전부 토큰에 묶여 있습니다.** 남은 것은 `cursor`의 라운드 1과 스타일 1건뿐입니다.

### 타 페이지 의존

| 출처 | 컴포넌트 | 건수 |
| --- | --- | --- |
| [Button](syrup-button-components.md) | `Button` | 5 |
| ❖Components | `Icon / Arrow` 3 · `Icon / Close` 3 | 6 |
| [Checkbox](syrup-checkbox-components.md) | `Checkbox` | 2 |
| ❖System Components | `Title Bar` 1 · `Section Header` 1 | 2 |

외부 라이브러리 인스턴스는 **0건**입니다.

---

## 점검 필요 사항

> 아래 네이밍·토큰·구조 제안은 2026-10-12 기록이에요. 이번 마스터 높이·패딩 및 가이드라인·예제 기준을 우선해요. 과거의 인스턴스 0건을 현재 변경 영향 범위로 해석하지 않아요.

### 1. 레이어명이 내용과 맞지 않음

이 페이지에서 **가장 두드러진 문제**입니다.

#### `아이디` 29건 — 압도적 1위

텍스트 레이어 대부분의 이름이 `아이디`인데, 실제 내용은 제각각입니다.

| 레이어명 | 실제 내용 | 위치 |
| --- | --- | --- |
| `아이디` | 「이름」 | `Type=Text` 라벨 |
| `아이디` | 「김시럽」 | `State=Typing` 입력값 |
| `아이디` | 「통신사」 | `Type=Text+Arrow` |
| `아이디` | 「023451」 | `State=Error` 인증번호 |
| `아이디` | 「인증번호」 | `State=Error` 라벨 |
| `아이디` | 「생년월일 6자리」 | `Type=Birth` |

**한 variant 안에서도 라벨과 입력값이 똑같이 `아이디`**라 레이어 패널에서 구분되지 않습니다.

#### 텍스트 내용이 그대로 레이어명이 된 경우

| 레이어명 | 건수 | 문제 |
| --- | --- | --- |
| `●●●●●●` | 5 | 마스킹 문자가 이름 |
| `주민번호뒷자리 입력` | 5 | 한글 문장 |
| `-` | 5 | 구분 기호 하나 |
| `970303` | 3 | **샘플 데이터 값** |
| `총 보유 SCON Credit` | 2 | **Text Area인데 내용과 무관** — 다른 컴포넌트에서 복제한 흔적 |
| `생년월일 6자리` | 1 | 한글 문장 |

2026-11-23 Text Area는 Text Container 안의 Placeholder / Text로 정리됐어요. 다음은 과거 기록이에요.

**`총 보유 SCON Credit`이 특히 문제**입니다. [Text Area](#2-text-field--text-area)의 본문 레이어인데 내용은 「자유롭게 의견을 작성해…」입니다. 다른 화면에서 복사해 온 흔적이 이름에 남았습니다.

`970303`은 **샘플 생년월일**이 그대로 이름이 된 경우로, 내용을 바꾸면 이름과 어긋납니다.

#### 그 외

| 레이어명 | 건수 | 문제 |
| --- | --- | --- |
| `field` | 22 | 소문자 |
| `2` · `1` · `0` | 9 · 5 · 1 | **숫자만** |
| `cursor` | 8 | 소문자 |
| `counttime` | 3 | 소문자 · 붙여쓰기 |
| `Frame 1171277402` | 3 | 기본 이름 |
| `leading` | 2 | 소문자 |
| **`" "`(공백)** | **2** | **이름이 공백 한 칸** |
| `errornoti` | 1 | 소문자 · 붙여쓰기 |
| `Frame 1171277401` · `Frame 1171277247` | 1 · 2 | 기본 이름 |

**이름이 공백 한 칸인 레이어가 2건** 있습니다. 레이어 패널에서 빈 줄로 보입니다.

`counttime` · `errornoti`는 **띄어쓰기 없이 붙인 소문자**라 `Count Time` · `Error Notice` 등으로 정리할 여지가 있습니다.

### 2. `cursor`의 무효 테두리 8건

| 속성 | 값 |
| --- | --- |
| 테두리 색 | **`#979797`** (미바인딩) |
| 두께 | **0** |
| 표시 | **`visible: false`** |

`cursor` 8개 전부에 **두께 0이고 꺼져 있는 테두리**가 남아 있습니다. 두 겹으로 무효화돼 있어 **화면에 전혀 영향이 없습니다.**

`#979797`은 이 파일에 대응 토큰이 없는 색이라, **지우면 깔끔해집니다.**

> [Search Field](syrup-search-field-components.md)에서 제거한 숨은 채움 `#D8D8D8`과 같은 유형입니다. 다만 그때는 **라운드를 지웠다가 테두리가 사각형이 된 일**이 있었으므로, 이번에는 **두께 0 · visible false 두 조건을 모두 확인**했습니다.

### 3. 스타일 미적용 텍스트 1건

| 위치 | 크기/굵기 | 적용 가능 토큰 |
| --- | --- | --- |
| `Text Field / Task` ▸ `Filled=False` ▸ `Text` | **17 Regular** | **`b100_17_regular`** |

같은 페이지의 `Text Field`가 17 Regular에 `b100_17_regular`를 쓰고 있어 **바로 적용 가능**합니다.

17px는 **시스템이 관리하는 크기**라 10~11px을 제외해 온 기준과 다릅니다.

### 4. 라운드 1 × 8건

`cursor` 1 × 26 사각형의 라운드입니다.

| 값 | 건수 | 대응 토큰 |
| --- | --- | --- |
| 1 | 8 | **없음** (최소 `Corner radius/100` = 4) |

폭이 1px인 커서라 **라운드 1은 사실상 보이지 않습니다.** 토큰도 없어 바인딩 대상이 아닙니다.

### 5. Variant 매트릭스 20/28

`State`(7) × `Type`(4) = 28 중 **20개**만 있습니다.

| State | Text | Text+Arrow | Birth | Text+Button | 소계 |
| --- | --- | --- | --- | --- | --- |
| `Inactive` | ✅ | ✅ | ✅ | ✅ | 4 |
| `Focused` | ✅ | ✅ | ✅ | ✅ | 4 |
| `Typing` | ✅ | **❌** | ✅ | ✅ | 3 |
| `Complete` | ✅ | ✅ | ✅ | ✅ | 4 |
| `Error` | ✅ | **❌** | ✅ | ✅ | 3 |
| `Complete_Time` | ✅ | ❌ | ❌ | ❌ | 1 |
| `Focused_Time` | ✅ | ❌ | ❌ | ❌ | 1 |

빠진 8개는 두 묶음입니다.

| 묶음 | 조합 | 해석 |
| --- | --- | --- |
| `Typing`·`Error` + `Text+Arrow` | 2 | **화살표 필드는 직접 입력이 아니라 선택형**이라 입력 중·오류 상태가 없음 |
| `*_Time` + `Text+Arrow`·`Birth`·`Text+Button` | 6 | **타이머는 인증번호 입력(`Text`) 전용** |

**둘 다 설명이 되는 생략**입니다. Figma는 없는 조합을 고르면 임의의 다른 variant로 대체하므로, 의도적 생략이라면 **축을 나누는 편**이 안전하지만 **variant 20개 재구성 비용**이 큽니다.

### 6. `State`·`Type` 값 표기

| 값 | 문제 | 제안 |
| --- | --- | --- |
| **`Complete_Time`** · **`Focused_Time`** | 언더스코어 — 다른 State는 단어 하나 | `Complete Time` 또는 별도 축 `Timer` |
| **`Text+Arrow`** · **`Text+Button`** | `+` 기호 | `Text Arrow` 또는 별도 축 `Trailing` |

`_Time`은 **타이머 표시 여부**라는 별개 개념이 `State`에 섞여 들어간 결과입니다. `Timer` BOOLEAN으로 빼면 `State` 5개 × `Timer` 2개로 정리되지만, **그 역시 구조 변경**입니다.

`+` 기호는 [Swipe](syrup-swipe-components.md)의 `Icon+Text` 레이어명을 `Content`로 정리한 것과 같은 성격입니다. 다만 이쪽은 **variant 값**이라 인스턴스 영향을 봐야 합니다 — 현재 사용 화면과 가이드라인·예제에 인스턴스가 있으므로 영향 범위를 확인해야 해요.

### 7. 줄 구분자 1건

| 위치 | 내용 |
| --- | --- |
| 보드 ▸ `{ShortDefinition}` | 「…입력 컴포넌트에요.**U+2028**검색, 정보 입력…」 |

**컴포넌트가 아니라 섹션 설명문**입니다. 줄바꿈이 일반 개행(`\n`)이 아닌 **U+2028 줄 구분자**로 들어가 있습니다.

파일 전체에 2건이 있고 **둘 다 `{ShortDefinition}`**입니다.

| 페이지 | 레이어 |
| --- | --- |
| [AD](syrup-ad-components.md) | `{ShortDefinition}` |
| **Text Field** | `{ShortDefinition}` |

같은 템플릿에서 생긴 것으로 보입니다. `\n`으로 바꾸면 **보이는 줄바꿈은 그대로 유지**됩니다.

### 8. 인스턴스 현황 — 과거 기록

| 구분 | 인스턴스 |
| --- | --- |
| `Text Field` · `Text Area` · `Task` | **전부 0** |

입력 필드는 **화면마다 직접 배치하는 요소**라 다른 컴포넌트 보드에 들어갈 일이 적습니다. [Result](syrup-result-components.md) · [Search Field](syrup-search-field-components.md) · [Tab Bar](syrup-tab-bar-components.md)와 같은 상황입니다.

현재 기본 Text Field 인스턴스는 이 페이지에서 43개이며, 그중 가이드라인·Usage의 17개는 문서용 왼쪽 패딩 0을 적용했어요. 43개 모두 높이 80을 확인했어요. Text Area·Task는 이 집계에 포함하지 않아요. 개명·구조 변경의 영향이 없다고 판단하지 않아요.

> **이 수치는 이 Figma 파일 기준**입니다. 다른 파일·디태치·코드 사용은 포함되지 않습니다.

---

## 정리 우선순위

### 이번 업데이트 (2026-11-10)

기본 Text Field 마스터 20개를 높이 80 및 밑줄 y=60으로 통일하고 페이지 내 인스턴스 43개를 확인했어요. 가이드라인 5개·Usage A~F를 추가했으며, 최대 글자 수에 따른 Text Area 높이 기준과 문서용 왼쪽 패딩 0을 실제 사용 패딩 24와 구분했어요. Section 1의 아노테이션 12개를 제거했어요. Text Area·Task 마스터 높이와 기존 State·Type 속성명은 변경하지 않았어요.

### 과거 점검의 후속 제안

| 순위 | 항목 | 성격 | 비용 |
| --- | --- | --- | --- |
| 1 | `Text` → `b100_17_regular` ([3](#3-스타일-미적용-텍스트-1건)) | **스타일 적용** | 낮음 |
| 2 | `cursor` 무효 테두리 8건 제거 ([2](#2-cursor의-무효-테두리-8건)) | **모양 안 바뀜** | 낮음 |
| 3 | 공백 이름 2건 · 기본 이름 6건 ([1](#1-레이어명이-내용과-맞지-않음)) | 모양 안 바뀜 | 낮음 |
| 4 | `총 보유 SCON Credit` 등 내용 불일치 이름 ([1](#1-레이어명이-내용과-맞지-않음)) | 모양 안 바뀜 | 낮음 |
| 5 | `아이디` 29건 ([1](#1-레이어명이-내용과-맞지-않음)) | **역할별 이름 필요 — 판단** | 중간 |
| 6 | 줄 구분자 → `\n` ([7](#7-줄-구분자-1건)) | **AD와 함께 2건** | 낮음 |
| 7 | `State`·`Type` 값 표기 ([6](#6-statetype-값-표기)) | **기존 인스턴스 영향 확인 필요** | 중간 |
| 8 | Variant 매트릭스 ([5](#5-variant-매트릭스-2028)) | 설명되는 생략 — 보류 | 높음 |
| — | 라운드 1 ×8건 ([4](#4-라운드-1--8건)) | 토큰 없음 · 안 보임 — 제외 | — |

**1~4번과 6번은 모양이 바뀌지 않습니다.**

이 페이지의 핵심은 **[점검 1의 레이어명](#1-레이어명이-내용과-맞지-않음)** 입니다. 토큰은 이미 깨끗한데(미바인딩 색 0건 · 원격 스타일 0건) **레이어 이름이 내용과 어긋난 경우가 50건 가까이** 됩니다.

특히 **`아이디` 29건**은 라벨·입력값·안내문을 가리지 않고 붙어 있어, 역할별로 나눠야 합니다. `Label` · `Value` · `Placeholder` 같은 기준을 정하면 한 번에 정리할 수 있습니다.


## 2026-11-23 반영

자동 높이·최소 높이, 하단 Progress/Counter 지원 조합, 최소 작성 조건과 최대 제한, 완료 모션과 자동 시연 복귀를 최신 원본에 맞춰 정리했어요. 가이드라인 8개와 예제 A~I를 제공해요.
