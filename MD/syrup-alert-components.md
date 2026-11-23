# Syrup Design System — Alert 컴포넌트

| 항목 | 값 |
| --- | --- |
| Figma File | [Syrup_Design-System](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System) |
| Page / Section | `Alert` 페이지 → [Alert 섹션 `8928:30872`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=8928-30872) |
| 섹션 구성 | `Alert` 1440×1285 → `Guidelines` 960×548 → `Usage` 2560×494 (가로 일렬) |
| 기준일 | 2026-11-18 (현재 원본의 말줄임·줄바꿈 및 MD 테스트 확인) |
| 관련 문서 | [syrup-design-tokens.md](syrup-design-tokens.md) · [syrup-dialog-components.md](syrup-dialog-components.md) · [syrup-ad-components.md](syrup-ad-components.md) · [syrup-badge-components.md](syrup-badge-components.md) · [syrup-banner-components.md](syrup-banner-components.md) · [syrup-border-components.md](syrup-border-components.md) · [syrup-bottom-info-components.md](syrup-bottom-info-components.md) · [syrup-bottom-cta-components.md](syrup-bottom-cta-components.md) · [syrup-bottom-sheet-components.md](syrup-bottom-sheet-components.md) · [syrup-bubble-components.md](syrup-bubble-components.md) · [syrup-button-components.md](syrup-button-components.md) · [syrup-checkbox-components.md](syrup-checkbox-components.md) · [syrup-chip-components.md](syrup-chip-components.md) · [syrup-card-components.md](syrup-card-components.md) · [syrup-dim-components.md](syrup-dim-components.md) · [syrup-grid-list-components.md](syrup-grid-list-components.md) · [syrup-grid-scroll-components.md](syrup-grid-scroll-components.md) · [syrup-header-components.md](syrup-header-components.md) · [syrup-icon-button-components.md](syrup-icon-button-components.md) · [syrup-indicator-components.md](syrup-indicator-components.md) · [syrup-keypad-components.md](syrup-keypad-components.md) · [syrup-label-components.md](syrup-label-components.md) · [syrup-list-footer-components.md](syrup-list-footer-components.md) · [syrup-list-header-components.md](syrup-list-header-components.md) · [syrup-list-row-components.md](syrup-list-row-components.md) · [syrup-loader-components.md](syrup-loader-components.md) · [syrup-lottie-components.md](syrup-lottie-components.md) · [syrup-product-grid-components.md](syrup-product-grid-components.md) · [syrup-product-list-components.md](syrup-product-list-components.md) · [syrup-product-scroll-components.md](syrup-product-scroll-components.md) · [syrup-progress-stepper-components.md](syrup-progress-stepper-components.md) · [syrup-result-components.md](syrup-result-components.md) · [syrup-search-field-components.md](syrup-search-field-components.md) · [syrup-stepper-components.md](syrup-stepper-components.md) · [syrup-swipe-components.md](syrup-swipe-components.md) · [syrup-switch-components.md](syrup-switch-components.md) · [syrup-tab-components.md](syrup-tab-components.md) · [syrup-tab-bar-components.md](syrup-tab-bar-components.md) · [syrup-text-button-components.md](syrup-text-button-components.md) · [syrup-text-field-components.md](syrup-text-field-components.md) · [syrup-ticker-components.md](syrup-ticker-components.md) · [syrup-toast-components.md](syrup-toast-components.md) |

> **사용자에게 중요한 정보나 상태를 안내하는 컴포넌트예요.**
> 현재 Figma 원본의 Variant·텍스트 설정을 기준으로 사용해요. 문구와 날짜·금액은 예시이며 운영 정책이 아니에요.

## 구성과 공개 속성

Master Component Set: `8928:34476` · 6 variants. 기존 마스터 인스턴스를 사용하고 내부 구조·스타일·아이콘을 유지해요.

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `Variant` | VARIANT | `Link` | `Link` · `Link2` · `Action` · `Multi-line Action` · `Info` · `Info_Center` |

공개 속성은 `Variant`뿐이에요. 제목·본문·라벨·버튼 문구와 액션 개수는 별도 공개 속성이 아니므로 아래 수정 경로에서 해당 인스턴스의 하위 레이어를 편집해요. 원본 마스터를 편집하거나 인스턴스를 분리하지 않아요.

## 유형 선택과 현재 줄 처리

2026-11-18 현재 원본에서 확인한 값이에요. `textAutoResize=HEIGHT`만 보고 여러 줄을 허용한다고 판단하지 말고 `textTruncation`과 `maxLines`도 함께 확인해요.

| Variant / 원본 노드 | 용도 | 본문 줄 처리 | 우측·하단 요소 |
| --- | --- | --- | --- |
| `Link` / `8928:34475` | 주의 안내와 관련 화면 이동 | **한 줄 말줄임**: `ENDING`, `maxLines=1` | 오른쪽 Arrow |
| `Link2` / `9061:11919` | 새 소식·혜택 안내와 관련 화면 이동 | **한 줄 말줄임**: `ENDING`, `maxLines=1` | 오른쪽 Arrow |
| `Action` / `8928:34477` | 짧은 안내와 한 가지 행동 | **한 줄 말줄임**: `ENDING`, `maxLines=1` | Text Button 1개 |
| `Multi-line Action` / `8928:71183` | 여러 줄 안내와 행동 | **줄바꿈 허용**: `DISABLED`, `maxLines=null` | 본문 아래 Text Button **1~2개**, 세로 배치 |
| `Info` / `8928:71153` | 라벨로 정보 종류·상태 구분 | **한 줄 말줄임**: `ENDING`, `maxLines=1` | 별도 행동 없음 |
| `Info_Center` / `8928:71130` | 행동 없는 가운데 안내 | **줄바꿈 허용**: `DISABLED`, `maxLines=null` | 라벨·아이콘·액션 없음 |

- `Link`·`Link2`의 `Title`은 `HUG`이며 말줄임 제한이 없어요. 본문과는 다른 설정이에요. 제목을 길게 쓰면 본문이 사용할 폭이 줄어들어요.
- **예제 B (`Link2`) 타이틀은 “출석 리워드가 올랐어요”를 기준으로 공백 포함 최대 12자**를 사용해요. 본문에 대한 제한이 아니며, 다른 Variant 전체의 공통 제한으로 확대하지 않아요. 좁은 카드나 더 넓은 글리프를 쓰는 경우에는 12자 이내라도 더 줄여 본문·화살표 공간을 확보해요. 이 12자 기준은 작성 규칙이며 Figma가 자동으로 입력을 제한하는 속성이 아니에요.
- `Info`의 `레이블`도 `ENDING`, `maxLines=1`이지만 라벨·pill 너비는 `HUG`예요. 긴 라벨이 자동으로 좁아질 것이라 가정하지 말고 짧은 상태명·분류명을 사용해요.
- 버튼 라벨은 원본의 `HUG`를 유지하고 짧은 행동 문구를 사용해요. 긴 라벨은 본문 폭을 줄이거나 가용 폭을 넘길 수 있어요.

## 공통 크기와 레이아웃

| 항목 | 현재 기준 |
| --- | --- |
| 폭 | 단독 기본 328px. 카드 안에서는 Alert 루트를 `FILL`로 변경 |
| 높이 | Link·Link2·Action·Info는 본문 한 줄 말줄임으로 40px 유지. Multi-line Action·Info_Center는 내용에 따라 확장. 루트는 HUG이며 기본 마스터에는 최소 높이 40px이 설정돼 있어요 |
| 모서리 | 전 Variant `Corner radius/400` (16) |
| 루트 레이아웃 | HORIZONTAL Auto Layout |
| 세로 정렬 | 기본 CENTER, Multi-line Action만 MIN(상단) |
| Clip | 원본 루트의 `clipsContent=true` 유지 |

328px 카드의 좌우 패딩이 각각 16px이면 Alert의 실사용 폭은 296px이에요. 카드 테두리를 레이아웃 계산에 포함하는지에 따라 실사용 폭이 달라질 수 있으므로 부모의 실제 콘텐츠 폭을 확인해요. 328px을 그대로 고정해 카드 밖으로 밀어내거나, 폭을 맞추기 위해 내부 아이콘·패딩을 축소하지 않아요.

### 높이가 달라지는 경우

- 한 줄 유형은 본문 한 줄 말줄임을 유지해요. 한 줄 문구가 길다는 이유로 줄 수 제한을 해제해 여러 줄 유형처럼 사용하지 않아요.
- Multi-line Action은 본문 줄 수와 표시한 버튼 수에 따라 높이가 늘거나 줄어요. 기본 마스터의 한 줄 본문+버튼 2개가 107px이며, 같은 조건에서 버튼 1개는 81px이에요. 2줄 본문+버튼 1개는 테스트에서 100px으로 확인됐어요. 이 수치는 예시이며 본문·스타일·가용 폭에 따른 실제 Hug 높이를 사용해요.
- Info_Center도 줄바꿈에 따라 높이가 늘어요. 3줄 본문은 테스트에서 74px이었어요. 가운데 정렬과 상하 패딩을 유지하며, 높이를 40px로 고정하지 않아요.

### 패딩과 간격

| Variant | Padding T/R/B/L | 루트 Gap |
| --- | --- | --- |
| Link · Link2 | 10 / 12 / 10 / 16 | `Spacing/250` (10) |
| Action | 10 / 16 / 10 / 16 | `Spacing/250` (10) |
| Multi-line Action | 16 / 20 / 20 / 16 | `Spacing/200` (8) |
| Info | 8 / 20 / 8 / 16 | `Spacing/200` (8) |
| Info_Center | 10 / 16 / 10 / 16 | `Spacing/400` (16) |

## 배경·텍스트·아이콘

| Variant | 배경 | 텍스트·강조 |
| --- | --- | --- |
| Link | `Color/Third_Pastel_Yellow` #FFF9E2 | 제목·본문 직접 색상 **#6E5033** 유지 |
| Link2 | `Color/Third_Pastel_Blue` #F1F6FF | `Color/Gray_200` |
| Action · Multi-line Action | `Color/Third_Pastel_Blue` | 아이콘·본문·버튼 `Color/Secondary_Blue` #3496F4 |
| Info | `Color/Gray_1000` #FAFAFB | 본문 `Color/Gray_100`; pill 배경 `Color/Gray_White`; 라벨 글자와 **1.2px 테두리** `Color/Secondary_Red` #FF3E00 |
| Info_Center | `Color/Gray_1000` | 본문 `Color/Gray_100` |

Link의 #6E5033은 현재 원본의 직접 색상 예외예요. 임의로 Gray_200으로 통일하거나 새 토큰으로 바꾸지 않아요. Info의 빨간 라벨·테두리는 단순 안내에서도 같은 원본 색상을 사용해요. 공개된 색상 변경 속성이 없으므로 의미를 추정해 중립색으로 바꾸지 않아요.

| 영역 | 텍스트 스타일 |
| --- | --- |
| Link · Link2 제목 | `t1060_13_bold` (13 / 18 / Bold / 자간 0) |
| Link · Link2 · Action · Info · Info_Center 본문 | `b500_13_regular` (13 / 18 / Regular / 자간 0) |
| Multi-line Action 본문 | `t1300_15_medium` (15 / 19 / Medium / 자간 -0.5) |
| Info pill 라벨 | `t1050_14_bold` (14 / 18 / Bold / 자간 -0.3) |
| Text Button 라벨 | 원본 `b500_13_regular` 유지 |

기본 글꼴은 Pretendard예요. 이름이 같은 원격 스타일로 바꾸지 않고 현재 로컬 텍스트 스타일을 유지해요. Link의 알람 아이콘, Link2의 확성기 벡터, Action 계열의 안내 아이콘과 오른쪽 Arrow는 원본 인스턴스를 사용해요. Link2 아이콘 내부 숨김 래스터를 다시 노출하지 않아요.

## 인스턴스에서 문구·액션 수정하기

같은 `Text` 이름의 프레임과 텍스트가 있으므로 **TEXT 노드**를 선택했는지 확인해요.

| Variant | 수정 경로 |
| --- | --- |
| Link · Link2 | `Icon+Text` → `Text` 프레임 → `Title` / `Text` 텍스트 |
| Action | `Icon+Text` 아래 `Text` 프레임의 본문 TEXT. 오른쪽 `Text Button` 내부 `text` TEXT |
| Multi-line Action | 루트 `Text` 프레임의 본문 `Text` TEXT, 각 `Text Button` 내부 `text` TEXT |
| Info | `Title` pill의 `레이블` TEXT와 본문 `Text` TEXT |
| Info_Center | 본문 `Text` TEXT |

Multi-line Action의 버튼이 1개면 원본 순서의 첫 번째 Text Button을 사용하고 두 번째 **중첩 버튼 인스턴스**를 숨겨요. 버튼 텍스트를 빈 값으로 지우는 방식은 사용하지 않아요. 버튼을 삭제하거나 분리하지 않고, 숨김 후 본문·첫 버튼 사이 간격 8px과 하단 패딩 20px이 유지되는지 확인해요. 액션 0개가 필요한 경우에는 임의로 모든 버튼을 없애지 말고 행동 없는 유형 중 목적에 맞는 것을 선택해요.

## 여러 줄·좁은 영역 사용 시 주의

1. **유형의 목적부터 확인해요.** Link·Link2는 이동, Action은 짧은 한 가지 행동, Multi-line Action은 여러 줄 본문과 1~2개 행동이에요. 단순히 문구가 길다는 이유로 상호작용이 다른 유형으로 대체하지 않아요.
2. **한 줄 유형의 본문은 말줄임을 유지해요.** Link·Link2는 내부 Text 묶음 높이가 고정이고 루트가 Clip이므로, 여러 줄 허용으로 바꾸면 이전 테스트처럼 내용이 배경 밖으로 나가 잘릴 수 있어요. 현재의 `ENDING / 1`을 해제해 해결하지 않아요. 긴 제목·버튼을 먼저 줄이고 가용 폭을 확인해요.
3. **여러 줄 유형은 본문 FILL + HEIGHT와 상위 Hug를 유지해요.** Multi-line Action과 Info_Center는 `DISABLED / null`을 사용해요. 오래된 인스턴스 오버라이드에 `maxLines=1`이나 고정 높이가 남아 있으면 현재 원본과 대조해 복원해요. 107px·40px을 강제로 고정하거나 폰트·행간을 줄여 끼워 넣지 않아요.
4. **실제 폭에서 확인해요.** 단독 328px과 카드 안 296px을 각각 확인해요. 줄바꿈 시 아이콘 첫 줄 정렬, 버튼 1~2개, 가운데 안내의 가로·세로 배치와 상하 여백을 확인해요. 정보가 반드시 모두 보여야 하면 한 줄 말줄임으로 핵심 내용이 사라지지 않도록 문구와 유형을 재검토해요.
5. **라벨과 버튼은 짧게 써요.** HUG 요소는 가용 본문 폭을 잠식할 수 있어요. 예제 B 타이틀 최대 12자도 모든 폭·글리프에서 공간을 보장하는 수치가 아니에요.

## Usage와 Guidelines

- [Usage `11241:48322`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11241-48322): A Link / B Link2 / C Action / D Multi-line Action / E Info / F Info_Center.
- [Guidelines `11187:22`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11187-22): 카드 안에서는 폭을 Fill로 설정해요.
- Usage 컷의 360px 폭과 주변 Header는 문서 설명용 맥락이에요. Alert 자체의 기본 폭 328px이나 모든 실제 화면의 고정 규격으로 확대하지 않아요.

## 확인 범위

2026-11-18 현재 원본을 읽어 줄 처리 설정을 재확인했어요. 과거 테스트의 Link·Link2 줄 넘침과 Multi-line Action 한 줄 말줄임은 **현재 원본의 규칙이 아니에요**. 수정 전 인스턴스에 남은 오버라이드를 재사용할 때 특히 주의해요. 이번 MD 보완에서는 Figma Master·Usage·Guidelines를 변경하지 않았어요.
