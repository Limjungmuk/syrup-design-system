# Syrup Figma Agent Guidelines
컴포넌트·토큰·라이팅 경량 가이드.
## 공통 기준
- 절별 기준·속성·상태와 기존 마스터 중첩·패딩을 유지. 유형별 규격을 따르며 예제 크기·간격을 앱 공통값으로 확대하지 않아요.
- 현재 토큰·텍스트·효과 스타일을 써요. 다른 역할의 토큰으로 교체 금지. Toast 직접 색상 등 예외는 유지.
- 샘플 금액·날짜·횟수·문구는 운영 정책이 아니에요. 선택·이용 불가·조건 달성·수령 완료를 구분.
- 점검 이력·제안·건수는 규칙이 아니에요. 누락 속성은 추정하지 말고 원본 MD·Figma를 확인.
- 문서 예제: 한 줄·간격40·여백100·설명–Slot50. Slot 패딩0·좌측/상단·Hug. 불필요한 화면 래퍼 없이 컴포넌트 자체 여백을 유지.
- Pretendard 기본. 기존 일러스트·로고·Lottie 재작성·폰트 대체 금지.
속성: 소유자—속성:타입/기본값/선택값. 기본값 없으면 선택값만, 보조 일부 생략.
### Writing 순서와 호칭
순서: 1 익숙한 말, 2 사용자 관점, 3 한 문장 한 내용, 4 해요체, 5 호칭, 6 용어, 7 띄어쓰기, 8 숫자·단위, 9 날짜, 10 문장부호, 11 느낌표, 12 버튼, 13 가능한 행동, 14 진행·수령 구분, 15 상황 배려, 16 일상·혜택. 상세: ../syrup-writing.md.
호칭 구분은 시럽 자체 기준이며 당근·토스의 공통 규칙이 아니에요. 일반 안내는 호칭 생략·혼용 금지.
- 고객: 상담·거래 관계를 구분할 때만. 고객님을 기본 호칭으로 반복하지 않아요.
- 회원: 가입·계정·탈퇴·참여 자격. 시럽/OK캐쉬백/Npay/멤버십 등 서비스명을 명시하고 자격 차이는 생략하지 않아요.
- 사용자: OS·기기 환경 구분. 가입 자격과 구분. 당첨자: 당첨 후 정보 제출·연락·수령 대상만.
- 일반 안내의 유저는 생략하거나 문맥에 맞게 변경. 본인 인증·명의, 고객센터·고객식별자와 승인된 고지 용어는 임의 변경 금지.
- 개인화된 인사·경험 질문은 이름·닉네임+님을 선택적으로 사용: ‘시럽이님, 이번 미션은 어땠나요?’ 반복 금지. 이름이 없으면 임의 생성·빈 이름+님 대신 호칭 없는 문장.
- 작성 예시: ‘고객님의 개인정보는 남기지 말아주세요’ → ‘개인정보는 남기지 말아 주세요.’ 입력 안내: ‘후기를 입력해 주세요.’
### 날짜·시간
최근 기록: 오늘 `14:30`, 어제 `어제`(필요 시 `어제 14:30`), 이전 올해 `11월 21일`, 다른 해 `2025년 12월 31일`. 시간 병기는 목록별 통일·공백 연결. 헤더만 M.D/YYYY.M.D(11.21/2025.11.30), 앞0·점 사이 공백·끝점 생략.
시간은24시간제 HH:mm(09:05), 갱신도 절대 시각. 방금·n분 전은 쓰지 않아요. 날짜만 있으면 오늘/어제/날짜, 가짜00:00 금지. 그룹 제목도 오늘/어제/날짜예요.
Asia/Seoul 달력 날짜로 판정(24/48시간 경과 아님), 자정·화면 복귀 시 갱신. 다른 시간대도 통일·연초 전날도 어제.
마감·예약·지급예정·유효기간·증빙·정산·문서 이력은 전체 날짜. 미래는 별도 기준·오류 보정 금지. 상세: ../syrup-writing.md. 시럽 기준, 당근은 형식만 참고.
## 참조
피그마: https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System
각 절의 G는 Guidelines, U는 Usage 노드예요. 위 URL 뒤에 ?node-id=번호를 붙여 열어요.
상세 원본은 상위 MD 폴더의 컴포넌트별 원본에서 확인. 이 문서는 점검 이력을 제외한 피그마 등록용 통합본이에요.
## 공개 에셋 이름
2026-11-11 공개 대상 59개의 `.primitive / ` 접두사를 제거했어요. 아래 참조는 변경된 이름을 사용. 원본 노드·키·variant는 유지했으며 라이브러리 게시는 별도로 필요해요. 아래 Item은 개별 항목, Icon·Image는 교체용 에셋 세트예요.
상위 묶음의 이름은 유지하고, 하위 에셋은 역할별 이름으로 구분했어요:
- Chip / Action / Item: 개별 Chip `8782:22028` / 상위 묶음 `8784:13432`.
- Chip / Filter / Item: 개별 Chip `9970:27294` / 상위 묶음 `9970:27417`.
- Grid Scroll / Icon / Image: 아이콘 세트 `8958:77489` / 상위 묶음 `8958:77378`.
- List Row / Now / Icon: 아이콘 세트 `9595:12728` / 상위 묶음 `9354:14876`.
- List Row / Every Day / Icon: 아이콘 세트 `9354:10147` / 상위 묶음 `9661:6149`.
- Product Grid / Naver / Item: 상품 항목 `9002:10142` / 상위 묶음 `9110:27033`.
- Product Grid / Stamp / Item: 상품 항목 `9110:26923` / 상위 묶음 `9110:27055`.
## 디자인 토큰
global 컬렉션. Gray는 숫자가 작을수록 어둡고, Opacity Black은 숫자가 클수록 옅어요. 토큰 이름과 값을 그대로 사용하고 근사 색으로 대체하지 않아요.
### 1. Color
#### 1-1. Primary
Token|HEX
`Color/Primary_Orange`|`#FF6315`
#### 1-2. Secondary
Token|HEX
`Color/Secondary_Yellow`|`#FFBE3B`
`Color/Secondary_Coral`|`#FF9550`
`Color/Secondary_Red`|`#FF3E00`
`Color/Secondary_Blue`|`#3496F4`
`Color/Secondary_Brown_Gray`|`#5E5854`
#### 1-3. Third (Pastel)
Token|HEX
`Color/Third_Pastel_Yellow`|`#FFF9E2`
`Color/Third_Pastel_Coral`|`#FFEADE`
`Color/Third_Pastel_Blue`|`#F1F6FF`
#### 1-4. Gray Scale
Token|HEX|비고
`Color/Gray_Black`|`#000000`
`Color/Gray_100`|`#222222`|본문 기본 텍스트
`Color/Gray_200`|`#464646`
`Color/Gray_250`|`#555555`
`Color/Gray_300`|`#666666`|보조 텍스트
`Color/Gray_400`|`#777777`
`Color/Gray_500`|`#999999`|placeholder
`Color/Gray_600`|`#BBBBBB`
`Color/Gray_700`|`#D2D2D2`
`Color/Gray_750`|`#DDDDDD`
`Color/Gray_800`|`#E4E4E4`
`Color/Gray_850`|`#EDEDED`|구분선 / 보더
`Color/Gray_900`|`#F2F2F2`
`Color/Gray_950`|`#F6F6F7`|섹션 배경
`Color/Gray_1000`|`#FAFAFB`
`Color/Gray_White`|`#FFFFFF`
#### 1-5. Opacity Black
Token|HEX8|Alpha|rgba()
`Color/Opacity_Black_100`|`#000000BF`|75%|`rgba(0, 0, 0, 0.75)`
`Color/Opacity_Black_200`|`#00000080`|50%|`rgba(0, 0, 0, 0.5)`
`Color/Opacity_Black_300`|`#00000040`|25%|`rgba(0, 0, 0, 0.25)`
`Color/Opacity_Black_400`|`#0000001F`|12%|`rgba(0, 0, 0, 0.12)`
`Color/Opacity_Black_450`|`#00000014`|8%|`rgba(0, 0, 0, 0.08)`
`Color/Opacity_Black_500`|`#0000000A`|4%|`rgba(0, 0, 0, 0.04)`
### 2. Typography
#### 2-0. Primitive
Token|Value
`Font family/pretendard`|`Pretendard`
Token|Value
`Font weight/300`|Light|`300`
`Font weight/400`|Regular|`400`
`Font weight/500`|Medium|`500`
`Font weight/600`|SemiBold|`600`
`Font weight/700`|Bold|`700`
`Font weight/800`|ExtraBold|`800`
`Font weight/900`|Black|`900`
Token|Value
`Font size/0`|11
`Font size/1`|12
`Font size/2`|13
`Font size/3`|14
`Font size/4`|15
`Font size/5`|16
`Font size/6`|17
`Font size/7`|19
`Font size/8`|20
`Font size/9`|21
`Font size/10`|23
`Font size/11`|24
`Font size/12`|25
`Font size/13`|27
`Font size/14`|28
Token|Value
`Line height/0`|35
`Line height/1`|33
`Line height/2`|31
`Line height/3`|30
`Line height/4`|29
`Line height/5`|27
`Line height/11`|26
`Line height/12`|25
`Line height/13`|24
`Line height/14`|23
`Line height/15`|22
`Line height/16`|21
`Line height/17`|20
`Line height/18`|19
`Line height/19`|18
`Line height/20`|17
`Line height/21`|16
Token|Value
`Letter spacing/0`|-1
`Letter spacing/1`|-0.5
`Letter spacing/2`|-0.3
`Letter spacing/3`|0
`Letter spacing/4`|-0.8
`Letter spacing/5`|-0.9
Token|Value
`paragraphSpacing/0`|0
`paragraphIndent/0`|0
#### 2-1. Text Style — Title (`t`)
Token|Size|Line Height|Weight|Letter Spacing
`t100_28_bold`|28|35|Bold (700)|-1
`t300_25_bold`|25|31|Bold (700)|-0.5
`t500_23_bold`|23|29|Bold (700)|-0.3
`t600_21_bold`|21|27|Bold (700)|-0.3
`t700_19_bold`|19|24|Bold (700)|-0.3
`t800_17_bold`|17|22|Bold (700)|0
`t900_16_bold`|16|20|Bold (700)|-0.3
`t1000_15_bold`|15|19|Bold (700)|0
`t1050_14_bold`|14|18|Bold (700)|-0.3
`t1060_13_bold` 🆕|13|18|Bold (700)|0
`t1100_17_medium`|17|22|Medium (500)|-0.8
`t1200_16_medium`|16|20|Medium (500)|-0.8
`t1300_15_medium`|15|19|Medium (500)|-0.5
`t1350_14_medium` 🆕|14|18|Medium (500)|-0.5
`t1360_13_medium` 🆕|13|18|Medium (500)|0
`t1400_20_regular`|20|24|Regular (400)|-0.8
적용 전|건수|변화
lh 18 / ls 0|15|없음
lh 18 / ls −0.3|7|letter-spacing → 0
lh AUTO / ls 0|3|line-height 18로 고정
lh 13 / ls −0.3|2|line-height 13 → 18, letter-spacing → 0
lh 18 / ls −0.5|1|letter-spacing → 0
적용 전|건수|변화
lh 19 / ls −0.5|2|line-height → 18
lh AUTO / ls −0.5|2|line-height 18로 고정
lh 20 / ls 0|1|line-height → 18, letter-spacing → −0.5
lh 21 / ls −0.3|1|line-height → 18, letter-spacing → −0.5
조합|파일 전체 사용|상태
13 Bold|28곳|`t1060_13_bold` 신설
14 Medium|6곳|`t1350_14_medium` 신설
11 Bold|21곳|❎ 예외 — 등록하지 않음
11 Medium|15곳|❎ 예외 — 등록하지 않음
13 Medium|37곳|`t1360_13_medium` 신설 (2026-10-01)
항목|값
스펙|13 / line-height 18 / letter-spacing 0
번호 근거|Bold 블록 `t1050`(14) → `t1060`(13) 선례를 따라 Medium 블록 `t1350`(14) → `t1360`(13)
값 근거|기존 13px 스타일 `b500_13_regular` · `t1060_13_bold`와 동일한 램프(13 → 18)
베리어블 바인딩|`Font family` · `Font weight` · `Font size` · `Line height` · `Letter spacing` 5개 전부
페이지|건수|적용 전|변화
Bubble|12|lh AUTO / ls 0|line-height 18로 고정
Foundation|12|lh 16 / ls −0.2|lh → 18, ls → 0 (폰트 변환 후 적용)
Progress Stepper|9|lh 16 / ls −0.3|lh → 18, ls → 0
Card · Grid List · Grid Scroll · Tab|각 1|lh 18 / ls 0|변화 없음
변환 전|→|건수|위치
`SUIT Medium`|Pretendard Medium|12|Foundation 컬러칩 라벨
`SF Pro Regular`|Pretendard Regular|6|❖System Components (문서 템플릿)
`Noto Sans KR Regular`|Pretendard Regular|5|Card · Tab Bar
`Noto Sans CJK KR Medium`|Pretendard Medium|1|Foundation weight 샘플
`Noto Sans CJK KR Black`|Pretendard Black|1|〃
`SF Pro Bold`|Pretendard Bold|1|❖System Components
`Roboto Regular`|Pretendard Regular|1|List Row 런처 아이콘 플레이스홀더
폰트|건수|용도
`Sandoll Gyeokdonggulim Regular`|12|AD 금주머니 "10분에1금" · Grid List 캠페인 라벨
`Sandoll GyeokdongGothic Regular`|1|❖Components "핫딜쇼핑" 30px 헤드라인
#### 2-2. Text Style — Body (`b`)
Token|Size|Line Height|Weight|Letter Spacing
`b100_17_regular`|17|22|Regular (400)|-0.9
`b200_16_regular`|16|20|Regular (400)|-0.8
`b300_15_regular`|15|19|Regular (400)|-0.5
`b400_14_regular`|14|18|Regular (400)|-0.5
`b500_13_regular`|13|18|Regular (400)|0
#### 2-3. Text Style — Caption (`c`)
Token|Size|Line Height|Weight|Letter Spacing
`c100_12_regular`|12|17|Regular (400)|-0.5
`c200_11_regular`|11|16|Regular (400)|-0.3
#### 2-4. 네이밍 규칙
### 3. Layout — Spacing
Token|px
`Spacing/0`|0
`Spacing/50`|2
`Spacing/100`|4
`Spacing/150`|6
`Spacing/200`|8
`Spacing/250`|10
`Spacing/300`|12
`Spacing/400`|16
`Spacing/500`|20
`Spacing/600`|24
`Spacing/700`|28
`Spacing/750`|30
`Spacing/800`|32
`Spacing/900`|36
`Spacing/1000`|40
`Spacing/1100`|44
`Spacing/1200`|48
`Spacing/1300`|52
`Spacing/1400`|56
`Spacing/1500`|60
`Spacing/1600`|64
### 4. Layout — Corner Radius
Token|px
`Corner radius/100`|4
`Corner radius/150`|6
`Corner radius/200`|8
`Corner radius/250`|10
`Corner radius/300`|12
`Corner radius/400`|16
`Corner radius/500`|20
`Corner radius/600`|24
`Corner radius/700`|28
`Corner radius/800`|32
`Corner radius/900`|36
`Corner radius/circle`|100
### 5. Effect — Shadow
Token|Color|Offset (x, y)|Blur|CSS `box-shadow`
`light_100`|`Color/Opacity_Black_450` `#00000014`|0, 1|5|`0 1px 5px 0 rgba(0,0,0,0.08)`
`gray_100`|`Color/Opacity_Black_500` `#0000000A`|0, 0|4|`0 0 4px 0 rgba(0,0,0,0.04)`
`color_100`|`Color/Opacity_Black_500` `#0000000A`|0, 0|2|`0 0 2px 0 rgba(0,0,0,0.04)`
## AD (광고)
Figma M:10403-6794,G:11169-22,U:11261-2202.
### 사용 기준
1. H80 배너는 가로세로 비율을 유지해요
360×80(4.5:1). 폭w에 높이w/4.5를 별도 지정(320→71.11).
2. 플로팅은 하단 배너와 겹치지 않게 배치해요
ETMS 하단→배너 상단20,pocket 루트 하단→배너 상단0. 배너 없을 때 ETMS→화면 하단20.
### 적용 시 주의
- DA 기본 Image=false/Description=true,ETMS Title=true,P_AD Text=true,pocket Bubble=true.
- NW·Naver DA의400초과 높이 고정은 자동 아님. 폭440에서 미디어 높이가 각각229.78·256.67로 증가함.
- 상한400 적용 시 별도 설정: 루트 폭w/Hug,Image(NW)·media(Naver DA)는Fill폭/Fixed높이. 미디어 높이=min(w,400)×188/360 또는×210/360. 내부 소재 폭=min(w,400),가운데 정렬,좌우 여백=max(w−400,0)/2. 글자·뱃지·CTA는 확대하지 않음. 440폭이면 소재400/좌우20,미디어208.89·233.33.
- pocket Off는Sandoll Gyeokdonggulim 폰트 미제공으로 시각검증 보류.
### 예제 유형
- A 하단H80(위55는 문서용)
- B Header55+H80
- C H185(소재185+상하1=187)
- D Gold+배너20
- E pocket+배너0
- F Corner=True,좌우20,320×300.44
- G Corner=False,360×338
- H P_AD Default234×2+간격16=484.
### 규격과 속성
DA Type=Top/H185/H100/H80(360폭,높이210/187/100/80).
ETMS Type=Popup/News/Gold/Mole/Egg(300×330/320×67/142×140/142×140/108×108).
P_AD Type=Default/Popup(320×234/256×181.34),Default Text영역68.
P.ad NW Image=SLOT,360×254(Image188+Title30+CTA36).
Naver_AD Corner=False/True,360×338;폭w의높이w×338/360를 별도 지정. Coner 사용 금지.
Naver DA=360×256(media210+CTA46),미디어 약1.71:1(360:210);1.91:1 아님.
pocket Active=On/Off,88×85.
## Alert
Figma M:8928-34476, G:11187-22, U:11241-48322. 2026-11-18 확인.
### 사용 기준
1. 카드 안에서는 폭을 채워요
단독328; 카드 안 Alert=FILL(328 카드·좌우16→296). 내부 패딩·radius16 유지.
### 적용 시 주의
- Link·Link2·Action·Info 본문: 한 줄 말줄임(ENDING/maxLines=1), 높이40 유지. Link류 내부 높이 고정·루트Clip이므로 제한을 해제해 여러 줄로 바꾸지 않아요.
- B(Link2) 타이틀: “출석 리워드가 올랐어요” 기준 공백 포함 최대12자(본문은 별도). 제목HUG·말줄임 없음; 좁으면 더 짧게. 자동 입력 제한은 아니에요.
- Multi-line Action: 본문FILL+HEIGHT·DISABLED/maxLines=null·상단 정렬·15 Medium. 아래 버튼1~2개 세로 배치. 1개면 두 번째 중첩 Text Button을 숨기고 간격8·하단20 유지(빈 문구/삭제/분리 금지).
- Info_Center: 본문FILL+HEIGHT·DISABLED/null·가운데 정렬, 줄 수에 따라 높이 확장. Info 라벨은 HUG·1줄(ENDING/1); 짧게 써요.
- 공개 속성은 Variant만. 하위 TEXT 편집: Link류 Title/Text, Info 레이블/Text, 나머지 본문 Text; 버튼 내부 text. Text 프레임과 구분. 제목·버튼HUG가 본문 폭을 줄여요.
- Link 직접색#6E5033, Info pill 흰 배경·글자/1.2px 테두리 Secondary_Red, 원본 스타일·아이콘 유지. 여러 줄 유형의 오래된 1줄/고정높이 오버라이드는 현재 원본과 대조해 복원해요.
### 예제 유형
A Link / B Link2 / C Action / D Multi-line Action / E Info / F Info_Center.
### 규격과 속성
Variant=위6종. 폭328·radius16·루트HUG/minHeight40. Multi 기본107은 고정값이 아니며 줄·버튼 수에 따라 달라요.
## Badge
Figma G:11224-35, U:11224-22
### 사용 기준
1. 리워드가 있는 항목에 금 배지를 사용해요
리워드 금액은 ‘20금’, 적립 행동 유도는 ‘더 모으기’로 안내.
2. 좁은 영역에서는 작은 배지를 사용해요
좁은 2열 카드에는 Size=S로 이미지 가림을 줄여요.
3. 쇼핑몰에 맞는 리워드 배지를 사용해요
쇼핑은 Rounded, 쿠팡 Stamp·그 외 Gold예요. 외부 Product Grid와 내부 List Item의 Variant를 모두 Shopping으로 설정해요.
Gold는 `Color/Primary_Orange`, Stamp는 원본 보라색이에요. Stamp 전환 시 주황 배경 오버라이드를 해제해요. 비활성 글자색은 아래 확정 기준을 따라요.
4. 지금 탭의 콘텐츠 카드에는 Flag 배지를 사용해요
지금 탭 Card / Now는 Flag, 다른 영역은 해당 배지 기준을 따라요.
### 적용 시 주의
상위 기본 인스턴스 내부의 Badge를 변경하고 별도로 겹쳐 추가하지 않아요. 뉴스 M·Pill은 카드 상단·우측8px, 쇼핑 S·Rounded는 썸네일 왼쪽·위10px, 지금 탭 S·Flag는 썸네일(0,0)이에요. 문구·완료 전환에도 높이와 앵커 여백을 유지하고 너비만 HUG로 바뀌어요.
### 지원 조합·완료 범위
- 13종만 지원. M·Gold·Pill: 기본/비활성/체크 3종. S·Gold·Pill: 기본/체크 2종(비활성 없음). S·Rounded와 S·Flag: 각각 Gold/Stamp × 활성/비활성 4종.
- 체크 완료는 Gold·Pill·활성의 M/S만 지원. 금액 대신 체크 원형이 되며 M 30×30/S 20×20이에요. 높이만 유지하고 폭은 줄어요. Stamp·Rounded·Flag·체크+비활성 조합을 임의 생성하지 않아요. 상위 컴포넌트의 완료 규칙이 없으면 확인.
- 과거 직접 배치 0건은 금지 규칙이 아니에요.
### 예제 유형
- A 기본 · 완료：`Card / News` × 2 (360 × 291.3 · 간격 16)
- B 비활성：`Product Grid`·`Shopping` — 내부 `Grid List Item`·`Live` 2칸
- C 작은 크기：`img_contents` × 2 (156 × 127 · 간격 8)
- D 쇼핑 리스트：`Product Grid`·`Shopping` 4칸 (158 × 248 · 가로 12 · 세로 24)
- E 지금 탭 콘텐츠 카드：`Card / Now`·`Type=Action` (328 × 156)
### 규격과 속성
- 높이 / M = 30, S = 20 (폭은 라벨 길이에 따라 HUG)
- 활성 배경 / Gold: `Color/Primary_Orange` · Stamp: 원본 보라색. 배경 오버라이드 없이 variant 원본을 따라요.
- 기본 텍스트 / `Color/Gray_White`
- 비활성 배경 / M `Color/Gray_500` · S `Color/Opacity_Black_200`
- 비활성 텍스트 / M `Color/Gray_White`, S `Color/Gray_800`. M 배경 Gray_500·흰 글자는 의도된 원본이며 보정하지 않아요.
- 아이콘 / M 20×20 · S 15×15 (원본 포함), 라벨 좌측
- 모서리 / Pill = 알약형 (M 20 · S 원형) · Rounded = 라운드 사각형 (4) · Flag 우하단만 6 · Check 원형
- 패딩 (M) / 상하 5 / 좌우 10 (비활성 4 / 8)
- 패딩 (S) / 상하 1 / 좌우 5 (Stamp 좌 `Spacing/50` 2 · `Pill` 좌우 `Spacing/150` 6)
- 간격 / M 4 · S 1 (Stamp 0)
## Banner
Figma G:11204-31, U:11204-22
### 사용 기준
1. 배너에는 화살표를 켜 둬요
배너는 눌러서 다른 화면으로 이동하는 컴포넌트예요.
이동할 수 있음을 알 수 있도록 화살표를 항상 표시.
2. 인디케이터는 캐러셀에 두 장 이상 있을 때만 켜요
여러 장을 넘겨 보는 캐러셀에서 현재 위치와 전체 장수를 표시.
한 장뿐이거나 세로로 나열한 배너에는 인디케이터를 표시하지 않아요.
3. 강조가 필요한 배너는 색상을 변경할 수 있어요
프로모션이나 이벤트의 주목도를 높일 때는 배경색과 텍스트 색상을 변경할 수 있어요.
텍스트와 화살표가 배경에서 명확히 보이도록 색상을 함께 조정.
### 예제 유형
- A 단독：`Banner` × 1 · `Indicator=false`
- B 세로 나열：`Banner` × 2 · 슬롯 간격 12
- C 캐러셀：`Banner` × 1 · `Indicator=true` 「1 / 2」
- D 색상 강조형：`Banner` × 1 · 배경 `#ABC436` · 흰 텍스트
### 규격과 속성
- 크기 / 328 × 86 고정
- 모서리 / `Corner radius/400` (16)
- 배경 / `Color/Gray_White`
- 패딩 / 8 / 12 / 8 / 16
- 이미지 영역 / 70 × 70 (SLOT)
- 이미지–텍스트 간격 / `Spacing/100` (4)
- 타이틀 / `t900_16_bold` / `Color/Gray_100`
- 본문 / `b500_13_regular` / `Color/Gray_250`
- 1. Banner — Master Component — `Image`: SLOT / 좌측 70 × 70 이미지 영역
- 1. Banner — Master Component — `Arrow`: BOOLEAN / `true` / 우측 이동 화살표 노출
## Border
Figma G:11194-29, U:11194-22
### 사용 기준
1. 컨테이너의 전체 폭을 채워요
높이는 10으로 유지하고, 너비는 컨테이너에 맞춰요.
좌우 여백 없이 배치해 영역 사이의 경계가 명확하게 보이도록 해요.
2. 서로 다른 콘텐츠 묶음 사이에 사용해요
같은 묶음에 속한 항목 사이에는 Border를 넣지 않아요.
하나의 묶음이 서로 다른 영역으로 나뉘어 보일 수 있어요.
### 적용 시 주의
Thick은 높이10의 영역 구분, Thin은1px 구분선이에요. 항목 사이 구분은 Border 컴포넌트나 컴포넌트 자체 하단 Stroke로 구현할 수 있어요. 둘을 중복 적용하지 않아요.
### 예제 유형
- A 새 영역의 시작：`Border` + 묶음 1개
- B 묶음 사이：묶음 + `Border` + 묶음
### 규격과 속성
- 1. Border — Master Component — `Height`: VARIANT / `Thick` / `Thin` · `Thick`
## Bottom CTA
Figma G:11135-24, U:11105-9486
### 사용 기준
1. Upper Item을 켰으면 내용을 채우세요
버튼 위에 추가 안내나 보조 행동이 필요한 경우 Upper Item을 사용. 사용하지 않을 때는 Upper Item을 숨겨주세요.
2. 2버튼은 왼쪽이 보조, 오른쪽이 주 행동
버튼을 가로로 두 개 배치할 때는 왼쪽 보조 행동에 `Weak`, 오른쪽 주요 행동에 `Fill`을 사용.
3. 비활성은 Weak + Disabled로 만드세요
비활성 버튼은 색상을 직접 변경하지 않고, `Variant=Weak`와 `Disabled=True`를 적용.
4. 행동의 관계에 따라 버튼 배치를 구분해요
이전/다음처럼 서로 연결된 단계 이동은 가로로, 이용 조건에 따라 선택하는 서로 다른 행동은 세로로 배치.
### 예제 유형
- A 단일 버튼：`Bottom CTA`
- B 설명 + 강조：`Bottom CTA`
- C 2 버튼 (가로)：`Bottom CTA`
- D 2 버튼 (세로)：`Bottom CTA`
- E 설명 + 강조 없음：`Bottom CTA`
- F 텍스트 버튼 + 주요 행동：`Bottom CTA`
- G 그라디언트 없음：`Bottom CTA` + `Keypad`
### 규격과 속성
- 폭 / 360 고정
- 기본 높이 / 154 (Upper Item + 버튼 1개 기준)
- 배경 / `Color/Gray_White`
- 상단 페이드 / 36px 흰색 그라데이션
- 하단 여백 / `Spacing/500` (20)
- 버튼 영역 좌우 여백 / `Spacing/400` (16)
- Upper Item 여백 / `Spacing/600` (24)
- 버튼 높이 · 모서리 / 56 · `Corner radius/250` (10)
- 버튼 라벨 / `t800_17_bold`
- 주 액션 / `Color/Primary_Orange` + `Color/Gray_White`
## Bottom Info
Figma G:11343-1336, U:11343-1337
### 사용 기준
1. 하단 고정 버튼이 있으면 하단 여백을 확보해요
Bottom CTA처럼 화면 하단에 고정된 버튼이 있으면 본문이 가려지지 않도록 하단 여백을 확보.
스크롤을 끝까지 내렸을 때 마지막 글줄까지 읽을 수 있도록 배치.
2. 플로팅 요소에 맞춰 하단 영역을 조정할 수 있어요
플로팅 요소의 크기와 위치, 본문의 마지막 글줄을 고려해 하단 영역의 높이와 여백을 조정할 수 있어요.
여러 요소를 함께 사용할 때는 본문과 각 요소가 서로 가려지지 않도록 배치.
하단 고정·플로팅 요소를 피하기 위한 추가 여백은 Bottom Info 내부의 `paddingBottom`으로 확보. 바깥 스크롤 콘텐츠의 하단 패딩, 고정 높이 확대, 빈 프레임으로 대체하거나 여백을 중복 적용하지 않아요. Bottom Info의 높이는 내용과 패딩에 맞춰 늘어나고, 배경색이 추가 여백까지 이어지도록 해요. 필요한 여백은 마지막 글줄과 고정·플로팅 요소의 실제 위치를 기준으로 정해요.
3. 닫기 버튼이 있어도 본문을 가리지 않아요
ETMS가 표시된 상태에서도 안내 내용을 모두 읽을 수 있도록 하단 여백을 확보.
닫은 뒤에는 기본 패딩으로 돌아가거나, 화면의 안정적인 배치를 위해 확보한 여백을 유지할 수 있어요.
4. 콘텐츠에 이어 붙일 때는 제목과 여백을 없애요
이미 여백이 있는 콘텐츠에 이어 붙일 때는 Title=False로 제목을 숨기고, Padding=False로 여백을 제거해요.
기존 콘텐츠의 흐름에 맞춰 안내 본문만 배치.
5. 상단 영역과 구분할 때는 흰 배경을 사용할 수 있어요
상단 영역에 배경색이 있는 경우 Bottom Info에 흰 배경을 사용할 수 있어요.
상단 영역과 안내 영역이 명확하게 구분되도록 배경색을 선택.
6. 소제목으로 나눈 묶음 사이는 20으로 띄워요
소제목으로 나눈 정보 묶음 사이에는 20 간격을 둬요.
묶음 안의 항목 간격인 8과 차이를 두어 각 묶음을 구분.
7. 소제목을 강조해 정보 묶음을 구분할 수 있어요
소제목과 본문의 구분이 필요할 때는 소제목에 Bold를 적용할 수 있어요.
같은 수준의 소제목에는 동일한 굵기를 적용.
### 예제 유형
- A 단순 나열
- B 소제목으로 묶기
- C 한 단계 더 들여쓰기
- D 링크 넣기：묶음 안 `Link` 1개 + 슬롯 직계 `Link` 1개
- E 소제목 강조하기
- F 제목과 여백 없이 쓰기：`List Header` + `Text Field / Text Area` + `Padding=False`
- G 흰 배경으로 쓰기：`상단 콘텐츠 (배경색 있음)` 블록(360 × 72) + 흰 배경 `Bottom Info`
- H 닫을 수 있는 ETMS와 함께 쓰기：`Bottom Info`(하단 여백 120) + `ETMS`·`Type=Gold` (142 × 140)
- I 복수 플로팅과 함께 쓰기：`Bottom Info`(하단 여백 160) + `ETMS`·`Type=Egg` (108 × 108) + `btn_timer` (194 × 40)
### 규격과 속성
- 폭 / 360 (Padding=True는 내부 콘텐츠 312)
- 배경 / `Color/Gray_950` (#F6F6F7) — `Padding=True`만
- 여백 / 상·좌·우 24 / 하 40
- 제목 / `t800_17_bold` / `Color/Gray_200`
- 본문 / `b500_13_regular` / `Color/Gray_400`
- 불릿 / 3 × 3 원 / `Color/Gray_400`
- 그룹 내부 간격 / `Spacing/200` (8)
- 그룹 간 간격 / `Spacing/500` (20)
- 제목 ↔ 본문 / `Spacing/400` (16)
- 1. Bottom Info — Master Component — `Padding`: VARIANT / `True` / 배경·여백 포함 여부
## Bottom Sheet
Figma G:11392-544, U:11392-545
### 사용 기준
1. 화면 아래에서 띄워 배치해요
시트는 화면에 붙이지 않고 좌우 10, 아래 32를 띄워 배치.
네 모서리가 모두 둥근 형태라 띄워야 모서리가 온전히 보여요.
2. 딤을 함께 사용해 뒤 화면과 구분해요
시트를 띄울 때는 Dim으로 뒤 화면을 어둡게 해요.
현재 조작하는 시트를 강조하고 뒤 화면과 구분.
3. 버튼이 없으면 시트 내부 하단 여백 16을 유지해요
버튼 없이 본문으로 끝나는 시트는 마지막 항목 아래에 내부 여백 16을 둬요.
항목이 둥근 모서리에 닿지 않도록 시트 안쪽 여백을 유지.
4. 하나만 고르는 목록은 Selection으로 만들어요
정렬이나 필터처럼 하나만 고르는 목록에는 `Bottom Sheet / Body / Selection`을 사용.
각 행은 `Bottom Sheet / Body / Selector / Select Item`으로 구성하고, 선택한 항목만 `Checked=True`, 나머지는 `Checked=False`로 설정해요.
선택 표시는 행 내부의 `Checkbox` (`Variant=Line`, `Size=M`, `Checked=True`, `Disabled=False`, 24×24)를 그대로 사용. 선택된 문구는 주황색으로 강조하고 오른쪽에 선형 체크를 표시. 원형 체크박스나 완료용 Badge를 별도로 덧붙이지 않아요.
선택형 컴포넌트 참조:
- Body 전체 이름: `Bottom Sheet / Body / Selection` · 노드 `8689:5852` · 컴포넌트 키 `07ecdabfe99197e7decb0f49910360520f3cfadf`
- 행 전체 이름: `Bottom Sheet / Body / Selector / Select Item` · 세트 `8689:5842` · 선택 `8689:5840` / 미선택 `8689:5841`
- `Body / Selection`은 위 전체 이름의 약칭이에요. `Selection`과 행 경로의 `Selector`는 실제 이름이 다르므로 같은 이름으로 정규화하지 않아요.
- Body의 행 개수와 문구는 내용에 맞춰 구성. ‘추천순·최신순·적립금 높은순·가격 낮은순’ 예제에서는 추천순만 선택.
- 찾지 못했을 때 `Body / List`와 별도 Badge로 대체하지 말고, 전체 이름·노드·키를 기준으로 원본을 다시 확인.
5. 버튼을 가로로 두 개 배치할 때는 주요 행동을 오른쪽에 둬요
버튼을 가로로 두 개 배치할 때는 되돌리는 행동을 왼쪽에, 진행하는 주요 행동을 오른쪽에 둬요.
주요 행동에는 채워진 버튼을 사용해 두 행동의 우선순위를 명확하게 구분.
6. 부가 설명은 보조 설명으로 나눌 수 있어요
제목은 내용에 따라 여러 줄로 사용할 수 있어요.
부가 설명을 별도로 안내하고 싶을 때는 제목 아래 보조 설명을 활용해요.
### 적용 시 주의
상황에 맞는 Body를 선택하고 제공된 구성으로 담기 어려운 내용은 Body / Slot에 자유롭게 구성. 시트 구조와 본문 좌우24를 유지. 문서 화면360×580, Dim은 전체 영역에 절대 배치.
### 예제 유형
- A 약관 목록 보여주기：`Body / List` · 3줄
- B 항목 하나 고르기：`Bottom Sheet / Body / Selection` · 행 수는 내용에 맞춤
- C 순서대로 안내하기：`Body / Stepper` · 2단계
- D 여러 장으로 넘겨 보기：`Body / Page`
- E 전용 콘텐츠 구성하기：`Body / Slot`
- F 제휴 로고 보여주기：`Body / List`의 `Logo=true` (116 × 116)
- G 보조 설명 더하기：`Sub title=true` (39)
- H 되돌리는 행동과 함께 두기：`2 Buttons` (146 + 146)
### 규격과 속성
- 폭 / 340 고정
- 모서리 / `Corner radius/600` (24) — 네 모서리 전체
- 배경 / `Color/Gray_White`
- 좌우 여백 / `Spacing/600` (24) · 버튼 영역만 `Spacing/500` (20)
- 타이틀 / `t600_21_bold` / `Color/Gray_100`
- 보조 설명 / `b300_15_regular` / `Color/Gray_400`
- 본문 목록 / `b200_16_regular`
- 버튼 / 높이 56 · `Corner radius/250`(10) · `t800_17_bold`
- 주 액션 / `Color/Primary_Orange` + `Color/Gray_White`
- 보조 액션 / `Color/Gray_900` + `Color/Gray_200`
## Bubble
Figma G:11438-3695, U:11438-3694
### 사용 기준
1. 꼬리가 안내 대상을 가리키도록 배치해요
대상의 위치에 맞춰 Placement와 Align을 선택.
Top은 꼬리가 위쪽, Bottom은 아래쪽에 있으며, Align은 꼬리의 가로 위치를 정해요.
2. 대상의 문구와 주요 정보를 가리지 않아요
버튼 문구나 본문의 주요 정보를 가리지 않도록 배치.
가장자리에 일부 겹치더라도 내용을 읽거나 조작하는 데 방해되지 않도록 해요.
3. 주변 요소와 여백에 맞춰 크기를 선택해요
주변 요소가 많거나 배치 공간이 좁은 경우 Size=S를 사용.
안내 문구가 잘 읽히고 주변 요소를 가리지 않도록 크기를 선택.
### 적용 시 주의
금 받기 전에는 Gold=True·Checkbox=False, 수령 완료 후에는 Gold=False·Checkbox=True로 바꿔요.
### 예제 유형
- A 행동 유도：`Switch` · `Check=On`
- B 실행 전 조건 안내：`Button` (`Icon=true` 「2배 받기」)
- C 리워드 안내 · 적립 완료：`Button` 296 (「시럽 쿠팡가기」) 2단
- D 상태와 횟수 안내：`Button` (`Variant=Weak` · `Disabled=True` 「정답」)
- E 변화 안내：금 시세 수치 묶음 (`3.223원 (+0.2%)`)
### 규격과 속성
- 폭 / 라벨 길이에 따라 HUG
- 높이 / S 31(1줄) · 41(2줄) / M 38(1줄) · 56(2줄)
- 배경 · 꼬리 / `Color/Gray_200` (#464646)
- 텍스트 / `Color/Gray_White`
- 모서리 / S `Corner radius/250`(10) · M `Corner radius/300`(12)
- 여백 / S 6 / 10 · M 8 / 12
- 꼬리 들여쓰기 / `Spacing/400` (16) — 전 variant 공통
- 1. Bubble — Master Component — `Placement`: VARIANT / `Top` / `Top` · `Bottom` / 꼬리가 위/아래 중 어디에 붙는지
- 1. Bubble — Master Component — `Align`: VARIANT / `Left` / `Left` · `Center` · `Right` / 꼬리의 수평 위치
## Button
Figma G:11830-7493, U:11830-7494
### 사용 기준
1. 행동의 중요도에 맞게 버튼을 구분해요
사용자가 우선 실행할 행동은 Fill로 강조하고, 함께 제공하는 보조 행동은 Weak나 Outline 계열로 구분.
버튼 문구는 실행할 행동을 구체적으로 표현하고 같은 영역에서 우선순위가 드러나도록 구성.
2. 콘텐츠에 맞춰 버튼 컬러를 조정할 수 있어요
이미지나 콘텐츠의 배경에 맞춰 버튼의 배경색과 텍스트 컬러를 변경할 수 있어요. 필요한 경우 문구 일부에 강조색을 사용할 수 있어요.
버튼이 배경과 명확히 구분되고 문구가 잘 읽히도록 조합하며, 크기와 상태별 표현은 기존 컴포넌트 기준을 유지.
대응하는 컬러 토큰이 있으면 해당 토큰을 사용.
3. 배치 영역에 맞는 크기를 사용해요
목록 안의 짧은 보상 버튼은 XS·S, 콘텐츠 안의 행동은 M·L, 넓은 주요 행동은 XL처럼 배치 영역에 맞춰 선택.
각 Size의 높이는 유지하고, 버튼 폭은 문구와 부모 영역에 맞게 조정.
4. 실행 가능 여부와 처리 상태를 구분해요
현재 실행할 수 없는 행동은 Disabled=True로 표시하고, 보상 처리 후의 표현에는 Checked=True를 사용.
두 속성의 의미를 구분하고, 문구와 컬러가 실제 상태에 맞도록 사용.
5. 필요한 보조 정보는 버튼 아래에 배치해요
행동의 조건이나 처리 안내가 필요하면 Button / Description의 하단 설명을 사용.
별도의 보조 행동은 하단 링크로 구분하고, 설명이 필요하지 않으면 Lower Item을 꺼서 버튼만 사용.
6. 전용 버튼의 진행 상태를 맞춰 사용해요
뉴스 보상 버튼은 읽기 진행·받기 가능·수령 완료를 구분. 조건을 충족한 상태를 수령 완료로 표시하지 않아요.
알림 버튼은 설정 여부, 퀴즈 버튼은 선택 방향과 참여 진행에 맞는 전용 속성을 사용.
### 예제 유형
- A. 주요 행동
- B. 두 행동의 우선순위
- C. 리워드 받기
- D. 테두리형 보조 행동
- E. 비활성 상태
- F. 처리 후 표시
- G. 처리 안내와 함께 사용
- H. 보조 링크와 함께 사용
- I. 두 방향 선택
- J. 읽기 진행과 보상 수령
- K. 알림 설정 상태
### 규격과 속성
- 높이 / XS 26 · S 30 · M 38 · L 48 · XL 56
- 상하 Padding / `Spacing/50` (2) — 전 사이즈 공통
- 모서리 / XS·S·M `Corner radius/150`(6) · L·XL `Corner radius/250`(10)
- 테두리 / 1
- 주 액션 / `Color/Primary_Orange` + `Color/Gray_White`
- 보조 액션 / `Color/Gray_900` + `Color/Gray_200`
- 비활성 (Fill) / `Color/Gray_600` 배경
- 비활성 (Weak · Outline) / 배경 유지 + 라벨 `Color/Gray_600`
- Checked=True · 처리 후 / `Color/Gray_White` 배경 + `Color/Primary_Orange` 라벨
## Card
Figma G:11849-7548, U:11849-7549
### 사용 기준
1. 정보의 목적에 맞는 카드를 사용해요
콘텐츠를 소개하고 행동으로 연결하는 카드와 수치·현황을 요약하는 카드를 구분해 사용.
각 카드가 제공하는 제목·본문·수치·버튼의 역할을 유지하고, 필요한 정보 구조에 맞는 유형을 선택.
2. 필요한 정보만 선택해서 보여줘요
제목·단계 안내·버튼·인디케이터 등 선택 옵션이 있는 요소는 화면에 필요한 정보에 맞춰 표시.
안내가 필요할 때는 단계를 함께 보여주고, 진행 현황만 필요할 때는 해당 정보만 남겨 간결하게 구성.
3. 이미지 영역은 필수로 사용해요
이미지가 포함된 카드는 이미지 영역을 유지하고, 콘텐츠에 맞는 이미지를 함께 사용.
Image=False는 배경색 등을 확인하기 위한 옵션으로, 실제 화면에서 이미지를 생략하는 용도로 사용하지 않아요.
4. 선택 상태와 사용할 수 없는 상태를 구분해요
선택형 카드는 현재 선택한 항목과 선택하지 않은 항목을 구분. 선택할 수 없는 경우에는 Disabled 유형을 사용.
선택 표시·문구·보조 링크가 실제 상태에 맞도록 구성하고, 사용할 수 없는 이유가 있으면 함께 안내.
5. 수치의 의미와 단위를 함께 보여줘요
금액·개수·순위 등 수치가 무엇을 뜻하는지 제목과 단위를 함께 표시.
적립 예정과 완료, 만료 예정처럼 구분이 필요한 정보는 항목명과 기한을 유지해 혼동하지 않도록 해요.
### 적용 시 주의
Summary SG02=적립 예정·완료 요약, OPS03_01=만료 예정. My의 State BOOLEAN은 Disabled의 추가 안내용이며 선택 상태가 아니에요.
### 예제 유형
- A. 콘텐츠와 리워드 안내：`Card / News`
- B. 순위가 있는 콘텐츠：`Card / Now · Ranking`
- C. 단계별 참여 안내：`Card / Todo / Step`
- D. 수치 요약：`Card / Summary · SG02`
- E. 만료 예정 안내：`Card / Summary · OPS03_01`
- F. 순위와 추가 행동：`Card / Invite / Ranking`
- G. 초대 코드와 내역：`Card / Invite / Code · Default`
- H. 정보 입력과 완료 상태：`Card / Tax`
- I. 결과와 참여 방법：`Card / Thunderbolt · Default / Step`
- J. 금과 스탬프 현황：`Card / Shopping · Gold / Stamp`
- K. 두 상품 비교：`Card / Stamp · Grid`
- L. 여러 상품 비교：`Card / Stamp · Compare`
- M. 혜택 조건과 받기：`Card / Shopping / Naver`
- N. 차트로 수치 비교：`Card / Chart`
- O. 표로 수치 비교：`Card / Table`
- P. 선택과 이용 조건：`Card / My · Selected / Default / Disabled`
### 규격과 속성
- 카드 폭 / 326 / 328이 표준 · 312(Invite·Tax) · 320(News·AD·Naver) · 360(SA)
- 라운드 / `Corner radius/400`(16) 가 기본 · `r300`(12) · `r250`(10) · `r200`(8)
- 테두리 / `Color/Gray_850` 1px이 기본 · `Gray_900` · `Gray_800` · 선택 시 `Primary_Orange`
- 배경 / `Color/Gray_White` · 비활성 `Color/Gray_950`
- 패딩 / `Spacing/500`(20) 또는 `Spacing/600`(24)이 가장 흔함 · 좌우 `Spacing/400`(16)도 사용
- 간격 / `Spacing/500`(20) · `Spacing/400`(16) · `Spacing/300`(12)
- 레이아웃 / 대부분 세로 오토레이아웃, 요약형은 가로
- `b400_14_regular` / 본문 (가장 많음)
- `t1000_15_bold` · `t800_17_bold` / 카드 제목
## Checkbox
Figma G:11452-3525, U:11452-3240
### 사용 기준
1. 선택 상태는 관련 항목과 함께 표시해요
어떤 항목을 선택했는지 알 수 있도록 체크박스를 문구 가까이에 배치.
카드형 항목은 체크 표시와 테두리의 선택 상태를 일치시켜요.
2. 완료와 비활성 상태를 구분해요
완료한 항목은 Checked=True로, 선택하거나 실행할 수 없는 항목은 Disabled=True로 표시.
Checked는 사용 맥락에 따라 선택 또는 완료를 뜻해요.
### 적용 시 주의
Circle과 Line을 제공해요. Line은 미선택에도 흐린 체크가 남아요. 라벨·동의 문구는 주변 구성과 함께 사용.
### 예제 유형
- A 항목 선택：`List Row / Todo / Selection` × 2
- B 약관 동의：`Bottom Sheet / Body / List / List Item` × 2
- C 카드형 선택：`Card / My` × 2 (`Selected` ↔ `Default`)
- D 간결한 선택 목록：`Bottom Sheet / Body / Selector / Select Item` × 2
- E 할 일 상태：`List Row / Todo / Task` × 3
- F 완료 표시：`Badge` · `Check=True` / `Bubble` · `Checkbox=true`
### 규격과 속성
- 크기 / XS 16 · S 20 · M 24 · L 30 (정사각)
- 테두리 두께 / 1 (전 사이즈 고정, `Circle`+미선택만)
- 선택 / `Color/Primary_Orange`
- 미선택 / `Color/Gray_700`
- 비활성 / `Color/Gray_850` (`Line`+`Checked=True`만 opacity 30%, 의도된 예외)
- 체크마크 (Circle) / `Color/Gray_White`
- 레이아웃 / 오토레이아웃 없음, 고정 크기
- 1. Checkbox — Master Component — `Variant`: VARIANT / `Circle` / `Line` · `Circle`
- 1. Checkbox — Master Component — `Size`: VARIANT / `XS` / `XS` · `S` · `M` · `L`
## Chip
Figma G:11499-2170, U:11499-1889
### 사용 기준
1. 용도에 맞는 Chip 컴포넌트를 사용해요
콘텐츠 탐색이나 검색·입력 실행에는 Chip / Action을 사용. 목록의 카테고리·조건·요일을 간결하게 선택할 때는 Chip / Filter를 사용.
기존 화면에서는 해당 영역에 적용된 컴포넌트를 따라요.
2. 선택형과 실행형을 구분해요
분류나 조건을 선택하는 칩은 Selected로 현재 선택 상태를 표시.
검색어나 빠른 값 입력처럼 누르면 행동이 실행되는 칩과 구분해 사용.
3. 배치 방식에 맞춰 Wrap을 선택해요
여러 줄로 보여줄 때는 Wrap=True, 한 줄로 배치할 때는 Wrap=False를 사용.
한 줄에 담기지 않는 항목은 가로 스크롤 등으로 접근할 수 있도록 구성.
4. 배경과 구분되는 표현을 선택해요
칩의 문구와 경계가 주변 배경에서 명확하게 보이도록 표현을 선택.
같은 역할의 칩은 선택·미선택 상태를 일관되게 적용.
5. 별도 페이지로 이동할 때는 아이콘을 표시해요
현재 탭 안의 콘텐츠를 바꾸는 경우에는 이동 아이콘을 표시하지 않아요.
별도 페이지로 이동하는 칩에는 Icon=True를 적용해 이동 방식을 구분.
### 예제 유형
- A 콘텐츠 분류 선택：`Chip / Action` `Kind=Select` · `Wrap=False`
- B 추천 검색어 실행：`Chip / Action` `Kind=Action` · `Wrap=True`
- C 배경 위의 추천 검색어：`Chip / Action` `Kind=Action2` · `Wrap=True`
- D 카테고리·조건 선택：`Chip / Filter` `Type=Category` 2행
- E 요일 선택：`Chip / Filter` `Type=Day`
- F 빠른 값 입력：`Chip / Action` `Kind=Action3` · `Wrap=False`
### 규격과 속성
- 칩 높이 / 40 (`minHeight`) / 32 (`minHeight` + FIXED)
- 좌우 패딩 / `Spacing/300` (12) / `Spacing/300` (12)
- 상하 패딩 / `Spacing/50` (2) / `Spacing/50` (2)
- 아이콘 간격 / `Spacing/50` (2) / —
- 칩 사이 간격 / `Spacing/200` (8) / `Spacing/100` (4)
- 라운드 / `Corner radius/circle` (100) / `Corner radius/circle` (100)
- 레이블 (선택) / `t1060_13_bold` 13px / `t1050_14_bold` 14px
- 레이블 (미선택) / `b500_13_regular` 13px / `b400_14_regular` 14px
- 선택 표현 / 배경 채우기 / 테두리 + 글자색
## Dialog
Figma G:11514-3066, U:11514-2428
### 사용 기준
1. 화면 중앙에 Dialog를 배치하고 Dim을 함께 사용해요
화면 배경은 흰색으로 두고, 전체 영역을 덮는 Dim 위에 Dialog를 가로·세로 중앙 정렬해요.
레이어는 화면 → Dim → Dialog 순서로 배치해 뒤 화면과 명확하게 구분.
2. 보상을 받는 팝업에는 보상 이미지를 사용해요
금이나 쿠폰 등 받는 대상의 이미지를 팝업 상단에 배치. 금은 기존 컴포넌트의 Lottie 영역을 사용.
현재 예제는 금 수령 사례이며, 쿠폰을 제공하는 경우에는 해당 쿠폰 이미지를 사용.
3. 필요한 행동에 맞춰 버튼을 구성해요
내용 확인만 필요하면 확인 버튼 하나를 사용. 진행 여부를 물을 때는 보조 행동을 왼쪽, 주요 행동을 오른쪽에 둬요.
버튼 문구는 사용자가 실행할 행동을 알 수 있도록 작성해요.
4. 입력이나 선택이 필요하면 본문 Slot을 활용해요
정보를 입력하거나 항목을 선택해야 할 때는 본문 Slot에 필요한 컴포넌트를 배치.
기존 Dialog의 제목·본문·버튼 구조를 유지하고 입력 조건이나 선택 상태가 명확하게 보이도록 구성.
### 적용 시 주의
이미지도 본문 Slot 안에 자유롭게 구성할 수 있어요. 문서 화면360×540은 예시 크기이며 Dialog 자체 높이가 아니에요. 실제 화면 중앙 배치와 전체 Dim을 유지.
### 예제 유형
- A 간단한 안내
- B 행동 확인
- C 설정·업데이트 안내
- D 상세 안내：유의 사항 4줄 · `Body Text=false`
- E 정보 입력
- F 항목 선택：`Checkbox` 3줄 (Npay 아이디)
- G 공유 방법 선택
- H 결과 안내
- I 보상 수령：`Images` `Type=Gold` (100 × 100)
- J 보상과 추가 콘텐츠：`Images` + Slot에 `P_AD` (248 × 177)
- K 이미지 구성
### 규격과 속성
- 폭 / 288 고정 (Button Area 단독 전시는 328)
- 모서리 / `Corner radius/400` (16)
- 배경 / `Color/Gray_White`
- 좌우 여백 / `Spacing/500` (20)
- 상단 여백 / `Spacing/1100` (44) — 이미지가 걸쳐 나오는 구조
- 타이틀 / `t600_21_bold` / `Color/Gray_100` / 최대 2줄 30자
- 본문 / `b300_15_regular` / `Color/Gray_200` / 간결하게
- 주 액션 / `Color/Primary_Orange` 배경 + `Color/Gray_White` 라벨
- 보조 액션 / `Color/Gray_900` 배경 + `Color/Gray_200` 라벨
## Dim
Figma G:11530-302, U:11530-303
### 사용 기준
1. 화면 전체를 덮도록 사용해요
Dim은 뒤 화면 전체를 덮도록 배치. 헤더나 하단 영역이 일부 남지 않도록 해요.
2. 팝업 아래에 한 번만 배치해요
화면 → Dim → Dialog 또는 Bottom Sheet 순서로 배치. Dim이 중복되어 배경이 지나치게 어두워지지 않도록 해요.
### 예제 유형
- A Dialog：`Dialog` 288 × 182
- B Bottom Sheet：`Bottom Sheet` 340 × 326
### 규격과 속성
- 색 / `#000000`
- 투명도 / 75% (`Color/Opacity_Black_100`)
- 라운드 / 0
- 효과 / 없음 (블러 없음)
- 적용 범위 / 화면 전체 (구현 시 확장)
## Grid List
Figma G:11857-5530, U:11857-5531
### 사용 기준
1. 정보량에 맞는 유형을 사용해요
아이콘과 이름만으로 구분할 수 있는 항목은 아이콘형을 사용. 설명이나 혜택을 함께 안내해야 하면 카드형을 사용.
리워드를 받는 행동이 필요한 경우에는 버튼이 있는 카드형을 선택.
2. 같은 목록의 열과 정렬을 유지해요
같은 목록에서는 항목의 폭과 간격을 일정하게 유지하고, 아이콘과 텍스트의 시작 위치를 맞춰요.
2열 카드형과 3열 목록형은 각 컴포넌트의 구성을 유지하고, 문구가 길어져도 같은 행의 높이가 맞도록 사용.
3. 배지와 리워드를 구분해서 보여줘요
새 항목이나 보유 개수는 아이콘 옆 배지로 표시. 배지의 종류와 숫자는 실제 정보에 맞게 사용.
받을 수 있는 리워드는 버튼에 금액을 표시하고, 메뉴의 보유 개수와 혼동되지 않도록 구분.
4. 3열 목록의 마지막 항목은 오른쪽 구분선을 숨겨요
구분선이 있는 3열 목록은 각 행의 마지막 항목에 Last=True를 사용.
할 일과 금융기관 목록 모두 오른쪽 외곽에 세로 구분선이 남지 않도록 구성.
### 적용 시 주의
가이드1 아이콘형과 예제A는 Variant=Top(8945:10808), 예제B는My예요. Last=True는 각 행 마지막 열의 오른쪽 구분선만 숨기며 선택·완료 상태가 아니에요.
### 예제 유형
- A. 주요 메뉴：`Grid List · Variant=Top`
- B. 보유 내역 메뉴：`Grid List · Variant=My`
- C. 여러 혜택 메뉴：`Grid List · Variant=혜택모음`
- D. 설명이 있는 카드：`Grid List · Variant=더많이모으기`
- E. 리워드 받기 카드：`Grid List · Variant=참여하고모으기`
- F. 할 일과 기록 횟수：`Grid List / Todo`
- G. 금융기관 선택：`Grid List / Bank`
### 규격과 속성
- 묶음 폭 / 328 (본문 영역) · 360 (화면 전체 폭)
- 카드 라운드 / `Corner radius/400` (16)
- 카드 테두리 / `Color/Gray_850` 1px
- 카드 배경 / `Color/Gray_White`
- 아이콘 간격 / `Spacing/200` (8)
- 아이콘–라벨 간격 / `Spacing/150` (6)
- 좌우 여백 / `Spacing/600` (24) — 360 폭 기준
- 배지 / 20 × 20 원형 (`Primary_Orange` / `Secondary_Red`)
- `t1360_13_medium` / 메뉴 라벨
- `t1000_15_bold` / 카드 제목
## Grid Scroll
Figma G:11540-1870, U:11540-1871
### 사용 기준
1. 콘텐츠에 맞는 유형을 사용해요
이동할 메뉴는 Icon, 시간대별 참여는 Live를 사용. 현재 금한돈 당첨 후기는 Ticker / Marquee / Card에서 후기 아이템 Size=M을 사용하며 Grid Scroll / Winner 묶음은 사용하지 않아요.
화면 폭을 넘는 항목은 가로로 탐색하고, 아이템 크기와 간격은 각 컴포넌트의 기본 구성을 유지.
2. 참여 상태에 맞춰 Live를 사용해요
참여 가능은 Available, 참여 완료는 Completed, 시작 전은 Upcoming, 종료 후는 Ended를 사용.
시간과 참여 여부에 맞는 상태를 선택하고, 참여할 수 없는 상태를 참여 가능한 버튼으로 표시하지 않아요.
### 적용 시 주의
후기 아이템 세트12450:4229(현재 원본 이름 Grid Scroll)에 Size=S/M을 제공. S는142×110·본문폭118·최대4줄/64, M은194×142고정·본문폭170·최대7줄/112. 공통13 Regular/행간16·패딩12·Gap4·라운드8, textTruncation=ENDING·textAutoResize=HEIGHT. 닉네임·날짜와 본문 제한을 구분해요. 금한돈 당첨 후기는 최소50자·최대100자이며 현재 Ticker에서 M을 사용. 줄바꿈으로7줄을 넘으면 말줄임될 수 있고 글자 수 제한과 표시 줄 수는 별개예요.
### 예제 유형
- A 쇼핑 메뉴 탐색：`Grid Scroll / Icon` · `Variant=Shopping`
- B 시간대별 참여：`Grid Scroll / Live`
- C 기존 당첨 후기 구조 참고：`Grid Scroll / Winner` · 현재 미사용, 신규 서비스 적용은 Ticker의 M 기준
### 규격과 속성
- 마스터 폭 / 598~664 (화면 밖으로 넘치는 스크롤 영역)
- 마스터 높이 / 110~116
- 아이콘 / 56 × 56
- 아이콘–라벨 간격 / `Spacing/150` (6)
- 아이템 간격 / `Spacing/500`(20) · `Spacing/250`(10) · `Spacing/200`(8)
- 카드 Radius / `Corner radius/400`(16) · `Corner radius/300`(12) · `Corner radius/200`(8)
- 선택 강조 / `Color/Primary_Orange` 1px 테두리
- 비활성 / `Color/Gray_900` 배경 + `Color/Gray_600` 글자
- `t1360_13_medium` / 아이콘 라벨
## Header
Figma G:11546-689, U:11546-690
### 사용 기준
1. 뒤로가기 옆 타이틀은 기본으로 표시하지 않아요
신규 화면에서는 Title=False로 설정해 뒤로가기 버튼 옆에 페이지 타이틀을 표시하지 않아요.
타이틀이 있는 기존 화면은 레거시 사례로 구분. 할 일의 영역명과 알림·타이머의 안내 문구에는 이 기준을 적용하지 않아요.
2. 이동과 종료에 맞는 버튼을 사용해요
이전 화면으로 돌아갈 때는 Back, 현재 화면이나 흐름을 닫을 때는 Close를 사용.
아이콘 모양만 바꾸지 않고 실제 동작에 맞는 유형을 선택.
3. 부가 기능은 실제 상태에 맞게 표시해요
알림은 설정 여부에 따라 표시하고, 타이머는 진행 중과 완료 후의 상태를 구분.
페이지 타이틀을 숨겨도 기능에 필요한 안내 문구와 상태 정보는 유지.
### 적용 시 주의
신규 Back은 페이지 타이틀을 숨기지만 Todo 영역명과 알림·타이머 기능 안내까지 숨기지 않아요. 필요한 상태와 기능 문구는 유지.
### 예제 유형
- A. 뒤로가기
- B. 닫기
- C. 알림 설정
- D. 적립 문의
- E. 시간·적립 상태
- F. 할 일
- G. 타이틀 표시 · 레거시
### 규격과 속성
- 헤더 높이 / 55 (`Todo`만 57)
- 헤더 폭 / 360 (화면 전체)
- 상하 패딩 / 9.5 (토큰 밖)
- 좌 패딩 / `Back` 8 · `Close` · `Todo` 16
- 우 패딩 / `Back` 16~20 · `Close` 12 · `Todo` 16
- 배경 / `Color/Gray_White` (`Theme=Dark`는 없음)
- 제목 / `t1400_20_regular` (20 / 24 / −0.8)
- 아이콘 / 36 × 36 (`Plus` 32), 획 1.8
- 아이콘 색 / `Light` `Color/Gray_100` · `Dark` `Color/Gray_White`
## Icon Button
Figma G:11556-4584, U:11556-4585
### 사용 기준
1. 실행과 설명에 맞는 버튼을 사용해요
정보를 갱신할 때는 Refresh, 추가 설명을 확인할 때는 Info를 사용.
화면에 고정하는 새로고침·맨 위로 이동에는 Floating을 사용하고, 콘텐츠 안의 작은 버튼과 구분.
2. Floating은 화면 하단 오른쪽을 기준으로 배치해요
화면 오른쪽에서 24, 하단에서 20을 띄워요. 하단 고정 ETMS 광고가 있으면 광고 상단부터 20을 띄워요.
버튼이 두 개면 세로 간격 10을 유지하고, 콘텐츠와 하단 고정 요소를 가리지 않도록 여유 공간을 확보.
3. 역할에 맞게 쉐도우형과 스트로크형을 사용해요
버튼 자체를 주변 정보와 구분해야 할 때는 쉐도우형(Shadow=True)을 사용.
갱신 시각이나 목록의 보조 동작처럼 주변 정보와 함께 표시할 때는 스트로크형(Shadow=False)을 사용. 아이콘·텍스트 유무와는 별도로 선택.
4. 필요한 경우 Refresh에 문구를 함께 표시해요
주변 정보로 새로고침 기능을 알 수 있으면 아이콘만 사용. 동작이나 갱신 시각을 알려야 하면 Text=True로 설정해요.
문구는 실제 동작에 맞게 작성하고, 쉐도우·스트로크형은 버튼의 역할에 따라 별도로 선택.
5. 주변 요소에 맞는 크기를 선택해요
Info는 S(16)·M(20)·L(24), Refresh는 S(20)·M(24)를 제공해요.
주변 텍스트와 기존 영역의 크기에 맞는 variant를 사용하고, 화면 위 고정 버튼은 Floating(40)을 사용.
### 예제 유형
- A. 값 새로고침
- B. 문구와 함께 새로고침
- C. 추가 정보 안내
- D. 화면 위 플로팅
- E. 하단 광고 위 플로팅
### 규격과 속성
- 크기 / Info 16·20·24 · Refresh 20·24 · Floating 40
- 라운드 / `Corner radius/circle` (Info만 0)
- 배경 / `Color/Gray_White` (3종 공통)
- 테두리 / Refresh `Color/Gray_800` 1px · Floating `Color/Gray_700` 1px
- 그림자 / `#000000` 14% · blur 5 · offset(0, 2) — Refresh `Shadow=True`만
- 텍스트 / `c200_11_regular` + `Color/Gray_400`
- 좌우 패딩 / `Spacing/200` (8) — Refresh `Text=True`만
- 1. Icon Button / Refresh — `Size`: VARIANT / `S` / `S` · `M`
- 1. Icon Button / Refresh — `Text`: VARIANT / `False` / `False` · `True`
## Indicator
Figma G:11569-4259, U:11569-4260
### 사용 기준
1. 안내할 정보에 맞는 유형을 사용해요
콘텐츠의 현재 위치는 Dot이나 숫자형으로 표시. 현재 순서와 전체 개수를 숫자로 명시할 때는 숫자형을 사용.
참여·시청 횟수도 숫자형으로 표시하고, 무엇을 나타내는 값인지 알 수 있도록 관련 문구와 함께 배치.
2. Dot은 배경에서 구분되는 색을 사용해요
밝은 배경에서는 기본 Dot을, 어두운 이미지나 컬러 위에서는 White=True를 사용.
현재 위치의 활성 점과 나머지 점이 배경에서 구분되는지 확인.
3. 숫자 배경은 배치되는 영역에 맞춰 선택해요
이미지 위에서 숫자를 구분해야 할 때는 Fill, 밝은 영역에서 정보를 묶어 보여줄 때는 Weak를 활용해요.
배경 없이 읽히는 영역에서는 Number를 사용하고, Size와 Padding은 기존 영역의 구성에 맞춰 선택.
4. 숫자의 의미가 드러나도록 표시해요
현재 순서·횟수와 전체 기준을 실제 데이터에 맞게 표시. 의미가 모호하면 주변 문구나 Text, 단위를 함께 사용.
콘텐츠가 바뀌거나 참여가 완료되면 현재 값과 활성 상태도 함께 갱신해요.
### 예제 유형
- A. Dot으로 위치 안내
- B. 숫자로 위치 안내
- C. 이미지 위 위치 안내
- D. 참여 횟수 안내
- E. 문구와 함께 수량 안내
### 규격과 속성
- 점 크기 · 간격 / 6 × 6 · `Spacing/150` (6)
- 현재 위치 강조 / `Color/Gray_Black` (밝은 배경) · `Color/Gray_White` (어두운 배경)
- 비활성 / `Color/Gray_500` · `Color/Gray_750`
- 배경 (어두움) / `Color/Opacity_Black_300` (25%)
- 배경 (밝음) / `Color/Gray_950`
- 패딩 / `Spacing/200` (8) — `Padding=True`만
- 타이포 (M) / `b300_15_regular` · `t1000_15_bold`
- 1. Indicator — Master Component — `Type`: VARIANT / `Dot` / `Dot` · `Number` · `Number_Background`
- .primitive / Indicator / Dot — `White`: VARIANT / `False` / `False` · `True`
## Keypad
Figma G:11577-274, U:11577-275
### 사용 기준
1. 입력값과 다음 버튼의 상태를 함께 맞춰요
입력 전에는 안내 문구와 보유 수량을 보여주고 다음 버튼을 비활성화해요.
입력 후에는 수량과 단위를 표시하고, 보유 수량 등 화면의 입력 조건을 만족할 때만 다음 버튼을 활성화해요.
2. 직접 입력과 빠른 입력을 함께 제공해요
숫자 키로 수량을 직접 입력하거나 상단 Chip으로 정해진 수량을 빠르게 입력할 수 있어요.
추가 수량과 모두의 기준은 해당 화면의 단위·보유 수량에 맞추고, 입력 후 값과 다음 버튼의 상태를 갱신해요.
3. 전체 삭제와 한 글자 삭제를 구분해요
전체삭제는 입력한 값을 모두 지우고, 삭제 아이콘은 마지막 숫자 한 자리를 지워요.
값을 모두 지우면 입력 전 안내와 다음 버튼의 비활성 상태로 돌아가요.
4. 키를 누르면 상태 변화를 보여줘요
기본 상태는 Default, 키를 누르는 동안은 Hover를 사용해 입력 반응을 보여줘요.
입력 후에는 Default로 돌아가며, 마지막으로 누른 키에 상태를 유지하지 않아요.
### 예제 유형
- A. 입력 전
- B. 수량 입력
### 규격과 속성
- 키패드 폭 / 360 (화면 전체)
- 버튼 크기 / 109 × 63 (마스터 안) · 120 × 63 (컴포넌트셋)
- 격자 / 4행 × 3열, 간격 0
- 좌우 여백 / `Spacing/400` (16)
- 영역 간격 / `Spacing/400` (16)
- 누름 배경 / `Color/Gray_900` + `Corner radius/400` (16)
- 숫자 / `t500_23_bold` + `Color/Gray_100`
- 기능 라벨 / `b200_16_regular` + `Color/Gray_100`
- 배경 / `Color/Gray_White`
## Label
Figma G:11582-523, U:11582-524
### 사용 기준
1. 정보의 성격에 맞는 Label을 사용해요
재료명과 수량처럼 개별 정보를 묶어 보여줄 때는 Tag, 영양 항목과 수치에는 Metric을 사용.
Label은 읽기 전용 정보예요. 선택·필터·실행이 필요한 요소와 구분하고 선택 상태나 버튼 동작을 부여하지 않아요.
2. 목록과 상세에 맞는 크기를 사용해요
좁은 목록에서는 S로 정보를 요약하고, 상세처럼 여유 있는 영역에서는 M을 사용.
Metric은 S의 축약 표기와 M의 전체 항목명을 구분하고, 같은 정보 묶음에서는 크기와 단위를 일관되게 맞춰요.
3. Tag가 많으면 영역 안에서 줄바꿈해요
재료가 많아 한 줄에 들어가지 않으면 Wrap=True로 설정해 영역 안에서 줄바꿈해요.
줄바꿈할 영역의 폭을 정하고, 내용이 늘어나면 높이가 함께 늘어나도록 구성.
4. 요약 정보는 항목명과 수치를 나누어 보여줘요
영양 정보를 한 줄로 요약할 때는 Stacked=False, 항목별 수치를 위아래로 구분할 때는 Stacked=True를 사용.
각 항목의 순서와 표시 색상을 유지하고, 수치는 해당 항목의 단위와 함께 표시.
### 예제 유형
- A. 목록의 식단 정보
- B. 상세의 식단 정보
- C. 일일 영양 요약
### 규격과 속성
- 태그 배경 / `Color/Gray_950` (#F6F6F7)
- 태그 라운드 / `Corner radius/150` (6)
- 태그 패딩 / 상하 `Spacing/100`(4) · 좌우 `Spacing/150`(6)
- 태그 간격 / `Spacing/100` (4)
- Metric 점 / 5 × 5 원형, 항목별 색 구분
- Metric 간격 / 가로 `Spacing/250`(10) · 세로 `Spacing/150`(6)
- 본문 색 / `Color/Gray_100`
- 보조 색 / `Color/Gray_400`
- `c100_12_regular` / 태그 `S` · Metric 라벨(Stacked)
## List Footer
Figma G:11589-5306, U:11589-5307
### 사용 기준
1. 관련 목록의 마지막에 배치해요
List Footer는 추가로 확인할 목록의 마지막 항목 아래에 배치.
목록과 같은 폭으로 맞추고, 목록과 함께 스크롤되도록 구성.
2. 동작과 확인할 범위를 문구로 알려줘요
추가 항목은 더보기, 전체 범위는 전체 보기, 이전 기록은 이전 보기처럼 실제 동작에 맞게 작성해요.
여러 목록이 이어지거나 범위 안내가 필요하면 대상명·개수·순위를 함께 표시.
3. 동작에 맞는 화살표 방향을 사용해요
같은 화면에서 목록 아래로 항목을 더 불러올 때는 아래쪽 화살표(Down)를 사용.
전체 목록이나 다른 페이지로 이동할 때는 오른쪽 화살표(Right)를 사용.
### 예제 유형
- A. 목록 더보기
- B. 범위를 표시한 전체 보기
- C. 상품 목록 더보기
- D. 이전 내역 보기
### 규격과 속성
- 크기 / 기준 360×64 · 관련 목록 폭에 맞춤 · 높이 HUG
- 상하 패딩 / 22.5
- 배경 / `Color/Gray_White`
- 경계 / `Color/Gray_900` 상단 1px만
- 라벨 / `t1300_15_medium` + `Color/Gray_200`
- 화살표 / `Icon / Arrow` · S(16) · 추가 로딩 Down / 페이지 이동 Right
- 정렬 / 가로·세로 중앙
- 1. List Footer — Master Component — `Text#8457:30`: TEXT / `더보기`
- 1. List Footer — Master Component — `Arrow#9796:1`: BOOLEAN / `true`
## List Header
Figma G:11594-6661, U:11594-6662
### 사용 기준
1. 제목과 보조 설명의 역할을 나눠요
주제는 제목, 조건·갱신 주기는 Sub Text=True로 나누고 중복하지 않아요.
2. 중요한 정보는 컬러로 강조할 수 있어요
필요한 단어·수치만 기존 컬러 토큰으로 강조해요. 검색 결과 굵기 규칙과 별개예요.
3. 새로운 내용은 제목 옆 N 뱃지로 안내해요
Title Acc=True → Type=Badge → Badge Type=New. N은 새로운 내용이며 수량·완료가 아니에요. 간격4·뱃지20×20을 유지하고 불필요하면 Title Acc를 꺼요.
4. 부가 정보와 기능은 목적에 맞게 선택해요
제목 옆 안내와 오른쪽 기준시각·광고·갱신 기능을 구분. 날짜는 공통 Writing을 따라요.
5. 부모 영역과 제목의 좌우 여백을 맞춰요
부모 여백이 있으면 Padding=0, 더 필요하면8/24. 아래 콘텐츠 시작선과 맞추며 중복하지 않아요.
6. 긴 제목은 줄바꿈에 맞춰 높이를 늘려요
제목 높이를 내용에 맞추고 Sub Text로 대체하지 않아요. 아래 목록·오른쪽 요소와 겹치지 않게 해요.
### 적용 시 주의
검색 결과만 키워드 Bold·나머지 Regular. 예제 I는 사용자 수정 Padding=0이에요. 가이드3(12412:434)·J(12412:463)는 Guidelines·Usage 템플릿 인스턴스를 유지하며 J 슬롯에는 List Header만 넣어요. 웹은 I·J와 가이드3~6 최신 이미지를 사용.
### 예제 유형
- A. 기본 섹션 제목
- B. 보조 설명 포함
- C. 광고·추가 안내
- D. 갱신 시각과 새로고침
- E. 기준 시각 안내
- F. 날짜·알림 기능
- G. 여러 줄 제목
- H. 텍스트 버튼
- I. 검색 결과 제목 · Padding=0
- J. 새로운 내용 안내 · N
### 규격과 속성
- 폭 / 기준 360 · 부모 영역과 콘텐츠 폭에 맞춤
- 높이 / 기본 샘플 24 / 47 · 여러 줄 제목은 내용에 맞춰 증가
- 좌우 패딩 / `0` · `Spacing/200`(8) · `Spacing/600`(24) 중 선택
- 상하 패딩 / 0
- 제목–보조설명 간격 / `Spacing/100` (4)
- 제목–Acc 간격 / `Spacing/100` (4)
- 배경 / 없음 (`Sub Text` primitive만 `Gray_White`)
- 제목 / `S` `t800_17_bold` · `M` `t700_19_bold` + `Color/Gray_100`
- 보조설명 / `S` `b500_13_regular` · `M` `b300_15_regular` + `Color/Gray_400`
## List Row
Figma G:11867-6849, U:11867-6850
### 사용 기준
1. 정보와 행동에 맞는 유형을 사용해요
콘텐츠나 리워드를 안내하는 행과, 이름·값을 보여주는 행을 구분해 사용.
버튼·화살표·체크 표시 등 오른쪽 요소는 각 컴포넌트의 역할에 맞게 유지.
2. 참여 상태에 맞춰 문구와 버튼을 변경해요
참여 전·진행 중·결과 확인·완료 상태는 해당 컴포넌트의 상태 옵션으로 구분.
버튼 문구와 체크 표시, 안내 문구가 실제 상태와 일치하도록 구성하고, 이용 불가 상태를 완료 상태와 혼동하지 않도록 해요.
3. 선택과 화면 이동을 구분해요
목록에서 항목을 고를 때는 Default와 Selected 상태를 사용.
다음 화면에서 내용을 입력하거나 선택하는 항목은 Navigation 유형을 사용하고, 선택 표시와 이동 화살표를 구분.
4. 문구와 보조 정보에 맞는 구성을 선택해요
미션 문구가 두 줄로 필요한 경우에는 2 Line=True를 사용.
분류·시간·설명 등 선택 옵션이 있는 정보는 필요한 경우에 표시하고, 같은 목록에서는 텍스트와 오른쪽 요소의 정렬을 유지.
5. 수치의 의미와 단위를 함께 보여줘요
순위·횟수·금액은 무엇을 뜻하는지 알 수 있도록 이름과 단위를 함께 표시.
같은 목록의 수치는 같은 위치에 정렬하고, 내역의 항목명과 날짜 등 수치를 이해하는 데 필요한 정보를 유지.
### 적용 시 주의
Task는 Completed=True/False, Todo / Task는 State=Default/Completed/Disabled, Todo / Selection은 State=Default/Selected/Navigation이에요. History N=OPS03_1, O=RC01. 예제 간격16을 실제 목록 공통값으로 확대하지 않아요.
### 예제 유형
- A. 현재 할 일 안내：`List Row / Now`
- B. 리워드와 바로가기：`List Row / Every Day · Type=Default / Link`
- C. 미션 참여：`List Row / Mission · 2 Line=False / True`
- D. 퀴즈 참여와 결과：`List Row / Quiz · Open / Pending / Result / Correct / Incorrect / Upcoming`
- E. 참여 완료 표시：`List Row / Task · Check-In / Personality Test / Golden Time`
- F. 할 일의 실행 상태：`List Row / Todo / Task · Default / Completed / Disabled`
- G. 할 일 선택과 이동：`List Row / Todo / Selection · Default / Selected / Navigation`
- H. 등록한 할 일 관리：`List Row / Todo / Management`
- I. 순위와 리워드：`List Row / Ranking · Rank=1 / 2 / 3 / 4 · Me`
- J. 실적 순위：`List Row / Report / Ranking`
- K. 발표와 당첨 상태：`List Row / Status · Upcoming / Winner / Not Winner / Not Entered`
- L. 쇼핑 적립 안내：`List Row / Shopping / Gold`
- M. 이름과 값：`List Row / Value`
- N. 상세 내역：`List Row / History · Type=OPS03_1`
- O. 참여 내역：`List Row / History · Type=RC01`
- P. 프로모션 안내：`List Row / Coupon / Promotion`
### 규격과 속성
- 행 폭 / 328이 표준 · 312 · 326 · 360
- 행 높이 / 43~68 (History는 19~136)
- 좌우 패딩 / `Spacing/500`(20) · `Spacing/600`(24) · `Spacing/400`(16)
- 간격 / `Spacing/250`(10) · `Spacing/400`(16) · `Spacing/500`(20)
- 라운드 / `Corner radius/400`(16) · `Corner radius/300`(12)
- 구분선 / 하단 1px — `Color/Gray_850` 또는 `Color/Gray_900`
- 강조 테두리 / `Color/Primary_Orange` 1px
- 기본 테두리 / `Color/Gray_850` 1px
- 배경 / `Color/Gray_White` 또는 없음
## Loader
Figma G:11601-444, U:11601-445
### 사용 기준
1. 배치 위치에 맞는 크기를 사용해요
화면 중앙에 배치할 때는 M(20), 상단 메뉴나 제목 아래에 배치할 때는 S(16)을 사용.
상단에 배치하는 Loader는 유지되는 영역의 하단에서 16 떨어뜨리고, 가로 중앙에 맞춰요.
### 적용 시 주의
화면 중앙은 M(20), 유지되는 상단 영역 아래는 S(16)를 가로 중앙에 배치. 상단과의 간격16을 유지하고 로딩 완료 후 숨겨요.
### 예제 유형
- A. 화면 전환 로딩
- B. 상단 메뉴 아래 로딩
- C. 제목 아래 로딩
### 규격과 속성
- 크기 / `S` 16 × 16 · `M` 20 × 20
- 색 / `Color/Primary_Orange` (점 2개)
- 배경 · 테두리 · 라운드 / 없음
- 효과 / 없음 (그림자·블러 없음)
- 애니메이션 / 키프레임 3장 (점 크기 7 → 20 → 7)
- 1. Loader — Master Component — `Size`: VARIANT / `S` / `S` · `M`
- 2. Child Item — Loader / Lottie — `Property 1`: VARIANT / `1` / `1` · `2` · `3`
## Lottie
Figma U:11623-1613
### 공통 사용 기준
- 기능과 콘텐츠에 맞는 기존 Lottie 모션을 사용. 사용처별 예제는 독립적인 컴포넌트 유형이나 새로운 Variant를 뜻하지 않아요.
- 숫자로 구분된 `Property 1` 값은 모션의 표현 단계예요. 선택 상태나 업무 진행 단계로 해석하지 않아요.
- 재생 시점과 반복·종료 조건은 에셋별 정의를 따라요. 정지 화면만으로 재생 시간, 반복 횟수, 완료 시 동작을 임의로 지정하지 않아요.
- 예제에는 모션을 이해하는 데 필요한 문구와 보조 요소만 함께 배치. 전체 서비스 화면을 복제할 필요는 없어요.
- 에셋 파일명이나 경로가 문서에 없는 경우 이름만으로 파일을 추정하지 않아요. 실제 모션 파일과 재생 정의를 확인해 사용.
### 적용 시 주의
Dot은 외부 페이지 이동 안내, Loader는 콘텐츠 로딩이에요. 비슷한 모양이라는 이유로 대체하지 않아요. Quiz_Coachmark 퀴즈 보상 안내는 개발 모션이므로 Lottie 예제에 포함하지 않아요.
### 예제 유형
- A. 알림 기능 안내：`Lottie / Alarm`
- B. 출석 영역 강조：`Lottie / Checkin`
- C. 이벤트 콘텐츠 연출：`Lottie / Thunderbolt1` · `Thunderbolt2`
- D. 퀴즈 참여 안내：`Lottie / Quiz`
- E. AI 분석 중 안내：`Lottie / Meal`
- F. 콘텐츠 혜택 안내：`Lottie / Shopping`
- G. 페이지 이동 안내：`Lottie / Dot`
### 웹 실동작 예제 (2026-11-17)
- B~G는 정적 이미지 대신 실제 Lottie JSON을 반복 재생해요. 파일은 웹의 `/assets/lottie/`에 있어요.
- B Checkin: `checkIn.json` (68×68).
- C Thunderbolt: `thunderbolt_sub01.json` (96×96), `thunderbolt_sub02.json` (44×44). 카드·캐릭터·금 이미지는 유지하고 두 번개만 실제 재생해요. 돌출 영역은 자르지 않아요.
- D Quiz: `quiz.json` (42×42). 날짜·마감 안내·참여 버튼 배치를 유지.
- E Meal: `mealplan.json` (110×110), `mealplan_ai.json` (32×32). 분석 안내 문구를 함께 표시.
- F Shopping: `motion_scroll_down.json` (20×20). 콘텐츠 혜택 안내 문구 옆에 표시.
- G Dot: `loading_dot.json` (24×12). 쿠팡 로고·이동 안내 문구와 함께 표시.
- 예제마다 우측 하단에 일시정지·재생을 제공해요. C·E는 두 플레이어를 함께 제어해요. 화면 밖·숨겨진 탭에서는 멈추고 모션 줄이기는 첫 프레임을 표시.
- E~G는 좌측의 360px 슬롯 안에서 가운데 정렬해요. 재생 버튼은 슬롯이 아닌 전체 예제 영역 우측 끝선에 맞춰요.
- H 퀴즈 보상 안내는 개발 모션으로 확인되어 Figma·웹 Lottie 예제에서 제외했어요. 현재 예제는 A~G이며 원본 마스터는 보존해요.
### 규격과 속성
- 프레임 표현 / `Property 1`에 숫자(`1` · `2` · `3` …)
- 프레임 수 / 2 ~ 8장
- 크기 / 4 × 12 ~ 340 × 135 (용도별 제각각)
- 배경 / 없음
## Product Grid
Figma G:11636-3839, U:11636-3838
### 사용 기준
1. 콘텐츠에 맞는 상품 아이템을 사용해요
일반 쇼핑 상품은 Shopping, 라이브 상품은 Live 아이템을 사용. 추천 상품과 네이버 제휴 상품, 스탬프 상품은 각각의 전용 구성을 사용.
2. 바깥 여백을 중복해서 넣지 않아요
화면 전체 폭에 배치할 때는 그리드의 좌우 여백을 사용. 부모 영역에 이미 여백이 있으면 그리드의 여백을 빼요. 같은 목록에서는 상품 폭과 열·행 간격을 일정하게 유지.
3. 상품에 필요한 정보만 표시해요
할인율·제휴처·찜하기는 해당 정보나 기능이 있을 때 표시. 리워드가 있는 상품에 배지를 사용하고, 라이브 표시와 시간은 방송 상태에 맞춰 구성.
4. 스탬프 상품은 제공 방식에 맞게 구성해요
두 상품 중 하나를 제공하는 구성에서는 or를 표시. 여러 상품 중 랜덤으로 제공할 때는 or를 숨기고 조건을 안내. 여러 행을 쌓을 때는 중간 행과 마지막 행을 구분하고, 추가 안내가 필요할 때만 Bubble을 표시.
### 예제 유형
- A. 쇼핑 상품
- B. 라이브 상품
- C. 추천 상품
- D. 네이버 제휴 상품
- E. 스탬프 상품 두 개
- F. 스탬프 상품 여러 개
### 규격과 속성
- 그리드 폭 / 312 · 328 · 360
- 상품 카드 폭 / 96 · 104 · 148 · 158 (그리드에 맞춤)
- 카드 간격 / `Spacing/200`(8) · `Spacing/300`(12) · `Spacing/400`(16)
- 이미지–내용 간격 / `Spacing/250` (10)
- 좌우 패딩 / `Spacing/400`(16) · `Spacing/600`(24)
- 구분선 / `Color/Gray_850` 1px (Stamp 계열)
- 배치 / Product Grid·Naver는 가로 WRAP, Stamp는 2개씩 한 행을 구성
- Shopping 열 / 행 간격 / 12 / 24
- Recommend 열 / 행 간격 / 16 / 20
## Product List
Figma G:11641-1302, U:11641-1301
### 사용 기준
1. 상품 정보와 동작에 맞는 유형을 사용해요
브랜드·상품명·가격을 보여줄 때는 Product를 사용. 받기처럼 행 안에서 실행할 동작이 있으면 Action을 사용하고, 버튼 문구로 동작을 분명하게 안내.
2. 콘텐츠의 설명 수준에 맞춰 구성해요
이미지와 짧은 제목으로 보여줄 때는 Media, 제목과 부가 설명을 함께 보여줄 때는 Content를 사용.
3. 쿠폰 날짜는 필요한 경우에 표시해요
상품 구성만 안내할 때는 Date=False, 사용 기한을 알려줄 때는 Date=True로 사용. 남은 일수도 함께 안내할 때는 Dday=True로 표시. D-day는 Date 영역이 켜져 있을 때 함께 보여요.
4. 사용할 수 없는 쿠폰은 상태를 구분해요
사용할 수 있는 쿠폰은 Default, 사용 완료·기간 만료·사용 불가 쿠폰은 Expired 구성을 사용. 이미지 위에 실제 상태를 문구로 표시하고, 사용할 수 없는 쿠폰의 D-day는 숨겨요.
### 적용 시 주의
항목 간격은 예제 기준 Action16, Media12, Product/Content0, Coupon12예요. 같은 목록 안에서는 같은 간격을 유지.
### 예제 유형
- A. 받기 버튼이 있는 상품
- B. 미디어 목록
- C. 가격 중심 상품 목록
- D. 설명이 있는 콘텐츠
- E. 기한이 있는 쿠폰
- F. 상품 안내용 쿠폰
- G. 사용할 수 없는 쿠폰
### 규격과 속성
- 폭 / 360 (전체 폭) · 332(`Media`) · 328(`Coupon`)
- 높이 / 60 ~ 128
- 이미지 / 80 × 80 (`Coupon`)
- 배치 / 가로 — 이미지 좌 · 텍스트 우
- 패딩 / `Spacing/600`(24) · `Spacing/500`(20) · `Spacing/400`(16) · `Spacing/300`(12)
- 내부 간격 / `Spacing/500`(20) · `Spacing/400`(16), Product의 기존 값 14
- 예제 항목 간격 / Action 16 · Media 12 · Product/Content 0 · Coupon 12
- 카드 테두리 / `Color/Gray_850` 1px (`Coupon`)
- 구분선 / `Color/Gray_900` 하단 1px (`Product`)
## Product Scroll
Figma G:11653-1096, U:11653-1095
### 사용 기준
1. 콘텐츠에 맞는 유형을 사용해요
심리테스트처럼 이미지와 짧은 제목을 보여줄 때는 Personality Test를 사용. 출석 화면의 제휴 상품처럼 상품명과 가격을 함께 보여줄 때는 Check-in을 사용.
2. 항목을 한 줄로 배치해 가로로 탐색해요
스크롤 영역 안에 항목을 한 줄로 배치하고, 영역을 넘는 부분은 가로로 탐색하도록 구성. 전체 항목을 넣기 위해 아이템 폭을 줄이거나 여러 줄로 바꾸지 않아요.
### 예제 유형
- A. 심리테스트 목록
- B. 출석 화면의 제휴 상품
### 규격과 속성
- 마스터 콘텐츠 폭 / 648 · 728 (전체 항목을 펼친 샘플 폭)
- 스크롤 표시 영역 / 부모 영역에 맞는 폭 · 가이드라인 2는 328, Usage는 360
- 아이템 폭 / 84 (`Personality Test`) · 120 (`Check-in`)
- 아이템 간격 / `Spacing/200`(8) · `Spacing/300`(12)
- 이미지–텍스트 간격 / `Spacing/250`(10) · `Spacing/300`(12)
- 이미지 배경 / `Color/Gray_950` (플레이스홀더)
- 이미지 라운드 / `Corner radius/150`(6) · `Corner radius/250`(10)
- 텍스트 / `b500_13_regular` · `t1300_15_medium` · `t900_16_bold`
- 1. Product Scroll — Master Component — `Variant`: VARIANT / `Personality Test` / `Personality Test` · `Check-in`
## Progress Stepper
Figma G:11808-6699, U:11808-6700
### 사용 기준
1. 서비스의 진행 방식에 맞는 유형을 사용해요
누적 금액·참여 횟수·완료한 미션 등 각 서비스의 진행 방식에 맞는 Progress Stepper를 사용.
목표 조건과 보상, 단계 구성을 함께 유지하고 다른 서비스의 형태를 임의로 섞지 않아요.
2. 조건 달성과 보상 수령 완료를 구분해요
보상을 직접 받는 단계는 조건을 달성하면 Available, 보상 수령이 끝나면 Completed로 표시.
아직 조건을 충족하지 못한 단계는 Disabled로 두고, 받을 수 있는 단계가 완료로 보이지 않도록 해요.
3. 현재 진행값과 목표 조건을 함께 보여줘요
현재 횟수나 누적값을 각 단계의 목표 조건과 함께 보여줘요.
선의 진행 위치와 활성 단계는 실제 진행값에 맞추고, 보상 수령 여부는 단계별 상태로 구분.
4. 단계 수에 맞는 구성을 사용해요
검색형은 5개와 10개 구성 중 해당 미션의 단계 수에 맞는 유형을 사용.
각 구성의 아이템 크기와 배열을 유지하고, 한 구성을 임의로 축소하거나 단계를 추가해 맞추지 않아요.
### 적용 시 주의
조건 미달 Disabled → 조건 달성 Available → 수령 완료 Completed. 체크인 수령 전 ‘5금 받기’, 수령 후 ‘5금 적립’과 체크 표시를 함께 바꿔요.
### 예제 유형
- A. 누적 금액 보상：`Collect`
- B. 반복 참여 횟수：`Pig`
- C. 연속 참여 보상：`Quiz`
- D. 누적 시청 보상：`News · Scroll=False`
- E. 완료 개수별 보상：`Personality-Test`
- F. 체크인 미션 보상：`Check-In`
- G. 반복 참여 완료 표시：`Movie`
- H. 순서별 미션 완료：`Mission`
- I. 복권 지급 조건：`Lottery`
- J. 검색 미션 5개：`Progress Stepper · Property 1=5 · Item Size=L`
- K. 검색 미션 10개：`Progress Stepper · Property 1=10 · Item Size=S`
- L. 경로형 도전：`Express · Color=Blue`
### 규격과 속성
- 방식 / 사용처
- SLOT `Line` / Collect · Pig · Check-In · Lottery
- Frame `Line` / Personality-Test · Quiz
- LINE 노드 / News
- Vector / Express
- 라인 없음 / Movie · Mission · Progress Stepper(Search)
- Master / Line (트랙) / Gauge (채움)
- Collect / `Color/Gray_850` / `Color/Secondary_Yellow`
- Pig / `Color/Third_Pastel_Coral` / `Color/Primary_Orange`
### 웹 상단 시연 모션 (2026-11-18)
- 웹 시연용이며 서비스 전체의 공통 재생 규칙으로 확대하지 않아요. 기존 5초 일정 속도 시연을 대체해요.
- 초기 500ms 대기 후 1회까지 600ms, 5·10·15회까지 각각 700ms 이동해요. cubic ease-out(1−(1−t)^3)으로 감속하며 목표를 넘지 않아요.
- 1·5·10회에서 각각 500ms 정지해요. 횟수·보상 판정은 원 중심 34·116·198·280px 기준이에요.
- 15회 말풍선은 50금 원 중심(280px)에 멈춰요. 선 게이지만 180ms 동안 끝(314px)까지 채워요. 최종 대기는 도착부터 1200ms이며 이 180ms를 포함해요.
- 도착한 원은 320ms 동안 최대 1.08배로 한 번 강조해요. 주황 배경·흰 글자 전환은 도착과 동시에 시작해 50ms ease-out으로 완료해요. 이전 220ms·120ms 전환은 대체해요.
- 복귀는 900ms quart ease-out으로 빠르게 시작해 서서히 멈춰요. 말풍선·게이지가 함께 돌아오고 게이지 선단은 314→−12px로 이동해요. 둥근 끝과 음수 시작을 유지해 갑자기 나타나거나 사라지지 않아요.
- 일시정지·재생, 화면 밖·숨겨진 탭 정지를 지원. 모션 줄이기에서는 0회 정지 상태로 표시하고 원 확대도 하지 않아요.
## Result
Figma G:11672-1794, U:11672-1793
### 사용 기준
1. 현재 상태와 필요한 안내를 분명하게 전달해요
내역이나 검색 결과가 없을 때는 무엇이 없는지 안내. 불러오기 실패는 빈 결과와 구분해 설명해요. 다음 행동이나 다시 확인할 시점이 있으면 문구에 함께 담아요.
2. 안내 목적에 맞는 시각 요소를 사용해요
일반적인 빈 상태나 오류는 Visual=Icon, 서비스 맥락을 함께 보여줄 때는 Visual=Image를 사용. 간단한 영역 안내는 Icon=False로 문구만 표시할 수 있어요. 서비스 이미지는 내용에 맞게 선택.
3. 바로 실행할 수 있는 동작이 있을 때 버튼을 사용해요
재시도처럼 사용자가 바로 실행할 동작이 있으면 Button=True로 표시. 단순 안내만 필요하면 Button=False로 숨기고, 버튼에는 실행할 동작을 구체적으로 적어요.
4. 사용하는 영역에 맞춰 크기와 여백을 조정해요
Result의 폭과 높이는 전체 화면이나 목록·카드 등 사용 영역에 맞춰 조정. 상하 여백도 영역에 맞게 조정하고, 안내 문구와 버튼이 잘리지 않도록 필요한 높이를 확보.
### 예제 유형
- A. 내역이 없는 경우
- B. 검색 결과가 없는 경우
- C. 일시적인 오류 안내
- D. 재시도가 필요한 경우
- E. 문구만 사용하는 경우
- F. 서비스 콘텐츠 준비 중
- G. 오늘의 콘텐츠를 모두 확인한 경우
- H. 리워드 받기 완료
- I. 광고 재생 전 안내
### 규격과 속성
- 1 / 아이콘 50 × 50 또는 이미지 120 × 120 / `Visual` + `Icon` BOOLEAN
- 2 / 안내 문구 15 Regular / `Description` BOOLEAN
- 3 / 버튼 64 × 38 / `Button` BOOLEAN
- 배경 / `Color/Gray_White` 바인딩
- 아이콘 색 / `Color/Gray_700` 바인딩
- 일러스트 색 / `Color/Third_Pastel_Yellow` 바인딩
- 테두리 / `Color/Gray_700` 바인딩
- 텍스트 색 / `Color/Gray_200` 바인딩
- Gap / 16(`Spacing/400`) 바인딩
## Search Field
Figma G:11698-2545, U:11698-2544
### 사용 기준
1. 입력 상태에 맞는 State를 사용해요
입력 전에는 Placeholder로 검색할 대상이나 혜택을 안내하고, 검색어를 입력한 상태는 Typing으로 표시. 입력값 지우기 버튼이 필요한 상태는 Typed를 사용. 세 상태의 주황 테두리는 동일하게 유지.
2. 찜하기 미션이 완료되지 않았을 때 Dot을 표시해요
쇼핑적립 탭에서 검색 후 찜하기 미션이 완료되지 않았으면 Dot=True로 표시. 미션을 완료하고 금을 받은 후에는 안내 문구를 바꾸고 Dot=False로 숨겨요. Dot은 Placeholder 상태에서만 표시.
3. 검색 보조 요소는 필드 밖에 배치해요
최근·추천 검색어는 Search Field 아래에 별도로 배치해 검색을 도와요. 찜처럼 검색과 다른 기능은 필드 밖에 두고, 함께 배치하는 요소를 고려해 검색창 폭을 조정.
### 적용 시 주의
미션 전 문구는 ‘상품 찜하고 매일 3금 받으세요’+Dot, 수령 후는 ‘금 받는 상품을 검색해보세요’·Dot=False예요.
### 예제 유형
- A. 입력 전 검색 안내
- B. 검색어 입력 상태
- C. 입력값 지우기
- D. 추천 검색어와 함께 사용
- E. 찜 기능과 함께 사용
### 규격과 속성
- `Placeholder` (입력 전) / 주황 / `Gray_400` (흐림) / 쇼핑적립 찜하기 미션 미완료 시 Dot
- `Typing` (입력 중) / 주황 / `Gray_100` (진함) / —
- `Typed` (입력값 지우기 제공) / 주황 / `Gray_100` / Close 버튼
- 배경 / `Color/Gray_White`
- 테두리 / `Color/Primary_Orange`
- 라운드 / `Corner radius/250`
- Padding / `Spacing/400`
- Gap / `Spacing/250`
- 텍스트 색 / `Color/Gray_400` · `Color/Gray_100`
## Stepper
Figma G:11719-1469, U:11719-1468
### 사용 기준
1. 안내할 정보에 맞게 설명을 구성해요
순서대로 할 일을 짧게 안내할 때는 Number Icon을 사용. 단계별 조건이나 주의 사항을 덧붙일 때는 Number Icon Description으로 제목과 보조 설명을 나눠요.
2. 시각 자료가 필요한 단계에는 Thumbnail을 사용해요
버튼이나 배너의 위치를 설명해야 할 때는 Thumbnail 구성에 필요한 UI 요소를 함께 넣어요. 문구만으로 설명할 수 있으면 Thumbnail=False로 숨겨요. 추가 설명은 필요한 행에만 표시.
3. 주변 구성에 맞는 번호 크기를 사용해요
번호 아이콘은 S(16), M(20), L(24) 중 주변 문구와 배치 공간에 맞게 선택. 같은 안내 묶음에서는 번호 크기를 일관되게 사용하고, 문구가 길면 줄 수에 맞는 행 구성을 선택.
4. 번호 순서를 맞추고 마지막 행을 구분해요
번호는 안내 순서대로 연속해서 표시. 중간 행은 Last Item=False, 마지막 행은 Last Item=True로 사용. 행 사이 간격은 컴포넌트의 아래 여백을 활용하고, 추가 간격을 중복해서 넣지 않아요.
### 예제 유형
- A. 짧은 참여 절차
- B. 여러 줄의 사용 안내
- C. 카드 안의 간결한 안내
- D. 조건과 보조 설명
- E. UI 요소를 함께 보여주는 절차
- F. 이미지 없이 제목을 강조한 안내
### 규격과 속성
- `… / Thumbnail` / 8 / `Spacing/200`
- `… / NumberIcon` / 20 / `Spacing/500`
- 배경 / `Color/Primary_Orange` · `Color/Gray_White`
- 텍스트 색 / `Gray_100` · `Gray_300` · `Gray_500` · `Gray_White`
- 연결선 색 / `Color/Gray_800`
- 텍스트 스타일 / `t1300_15_medium` · `b400_14_regular` · `b500_13_regular` · `t1050_14_bold`
- 라운드 / `Corner radius/circle`
- 1. Stepper — Master Component — `Left`: VARIANT / `Thumbnail` · `Number Icon Description` · `Number Icon`
- 2. `StepperRow / NumberIcon / Thumbnail` — `Title Bold`: VARIANT / `False` / `False` · `True`
## Swipe
Figma G:11724-225, U:11724-226
### 사용 기준
1. 밀기 동작으로 할 일 완료를 실행해요
할 일 알림에서 사용자가 직접 밀어 완료할 때 Swipe를 사용.
대기 상태는 Default, 핸들을 움직이는 중에는 Dragging으로 표시해 동작의 진행을 보여줘요.
2. 처리 중·완료·시간 만료를 구분해요
밀기 동작 후 금 지급을 처리하는 동안에는 Near Complete로 표시. 지급이 끝난 완료 상태로 사용하지 않아요. 완료되면 Complete로 표시하고 손잡이를 숨겨요.
완료 가능한 시간이 지나면 Expired로 전환해 더 이상 완료할 수 없음을 안내.
3. 완료 후에도 리워드 결과를 보여줘요
Complete는 #E7550C 배경과 “완료” 문구로 표시. 손잡이는 숨기고 Bubble=True이면 금액 뒤에 체크 표시가 있는 뱃지를 유지.
처리 중인 Near Complete와 실제 완료인 Complete를 구분하고, 완료 상태에서 다시 밀기 동작을 요구하지 않아요.
4. 리워드 안내가 필요할 때 Bubble을 표시해요
완료로 받을 리워드를 안내할 때는 Bubble=True로 표시. 금액은 실제 지급 조건에 맞춰 사용.
추가 안내가 필요하지 않으면 Bubble=False로 숨겨요. 위로 돌출되는 말풍선이 다른 요소와 겹치지 않도록 배치.
### 예제 유형
- A. 할 일 완료 대기：`Default`
- B. 밀기 진행 중：`Dragging`
- C. 금 지급 처리 중：`Near Complete`
- D. 할 일 완료：`Complete` · 완료 문구와 금액·체크 뱃지
- E. 완료 가능한 시간 만료：`Expired`
### 규격과 속성
- 기본 바 배경 / #FF6315 / `Color/Primary_Orange`
- 진행 바 · 처리 중 · 완료 배경 / #E7550C / 없음
- 만료 배경 · 비활성 핸들 / #FFEADE / `Color/Third_Pastel_Coral`
- 만료 문구 / #FFC59F / 없음
- 핸들 원 · 문구 / #FFFFFF / `Color/Gray_White`
- Padding / `Spacing/250` · `Spacing/900`
- 라운드 / `Corner radius/circle`
- 배경 · 아이콘 색 / 대부분 토큰
- State / Default · Dragging · Near Complete · Complete · Expired
- Bubble / `Bubble` / 완료에도 금액·체크 표시 유지
## Switch
Figma G:11739-612, U:11739-613
### 사용 기준
1. 현재 설정을 On과 Off로 구분해요
기능이나 옵션을 켜고 끌 때 Switch를 사용. 켜진 상태는 Check=On, 꺼진 상태는 Check=Off로 표시.
항목 이름과 함께 배치해 어떤 설정을 변경하는지 알 수 있도록 해요.
2. 어떤 설정을 변경하는지 알 수 있도록 배치해요
설정 이름과 Switch를 함께 배치해 조작 대상을 명확히 해요.
여러 항목을 나열할 때는 Switch의 위치를 맞춰 각 설정의 상태를 쉽게 비교할 수 있도록 해요.
3. 변경할 수 없을 때는 Disabled로 표시해요
권한이나 선행 조건 때문에 설정을 변경할 수 없으면 Disabled=True로 표시. 기존 On·Off 값은 유지.
조건을 충족할 수 있도록 비활성 이유나 필요한 설정을 주변 설명으로 안내.
### 적용 시 주의
마스터42×24, 손잡이20×20. 설정 이름·보조 설명은 Switch 밖의 맥락 요소이며 마스터 내부 속성이 아니에요.
### 예제 유형
- A. 단일 옵션 설정
- B. 기능의 동작 설정
- C. 수신 및 정보 이용 동의
- D. 권한과 선행 조건에 따른 비활성
### 규격과 속성
- 배경 / `Primary_Orange` · `Gray_700` · `Gray_850`
- 손잡이 / `Color/Gray_White`
- Padding · Gap / `Spacing/50`
- 라운드 / `Corner radius/circle`
- 1. Switch — Master Component — `Check`: VARIANT / `On` / `Off` · `On`
- 1. Switch — Master Component — `Disabled`: VARIANT / `False` / `True` · `False`
## Tab Bar
Figma G:11771-656, U:11771-657
### 사용 기준
1. 주요 메뉴와 현재 위치를 일관되게 보여줘요
모으기·지금·쇼핑적립·MY·전체의 순서와 아이콘을 유지해 앱의 주요 메뉴를 탐색해요.
현재 화면에 해당하는 항목만 Selected=True로 표시하고, 나머지는 Selected=False로 구분.
2. Red Dot은 선택 여부와 별도로 표시해요
Red Dot은 각 탭의 서비스 조건에 따라 표시. 선택 상태를 나타내는 Selected와 별도로 관리해요.
탭을 선택했다는 이유만으로 Dot을 켜거나 끄지 않고, 해당 안내의 표시 조건을 따라요.
3. 하단 환경에 맞게 홈 인디케이터를 사용해요
홈 인디케이터 영역이 필요하면 Home Indicator=True, 필요하지 않으면 False를 사용.
Tab Bar는 화면 하단에 배치하고, 하단 광고를 함께 사용하는 경우에는 광고를 Tab Bar 위에 두어요.
### 예제 유형
- A. 기본 메뉴 탐색
- B. 선택 상태와 Red Dot
- C. 하단 광고와 함께 배치
### 규격과 속성
- 아이콘 / `Color/Gray_100` / `Color/Gray_500`
- 라벨 / `Color/Gray_100` / `Color/Gray_400`
- 배경 · 아이콘 · 라벨 색 / `Gray_White` · `Gray_100` · `Gray_400` · `Gray_500` · `Primary_Orange` · `Secondary_Red`
- Gap / `Spacing/100` · `600`
- 1. Tab Bar — Master Component — `Home Indicator`: VARIANT / `True` · `False`
- 2. `.primitive / Tab Bar / Tab Item` — `Selected`: VARIANT / `True` / `True` · `False`
- 2. `.primitive / Tab Bar / Tab Item` — `Red Dot`: VARIANT / `False` / `False` · `True`
- 2. `.primitive / Tab Bar / Tab Item` — `Show Tooltip`: BOOLEAN / `false`
- 3. `.primitive / Tab Bar / Icons` — `Resource`: VARIANT / `05all` · `01pig` · `04wallet` · `02alarm` · `03shopping`
## Tab
Figma G:11765-3726, U:11765-3727
### 사용 기준
1. 탐색할 정보에 맞는 유형을 사용해요
상위 콘텐츠를 구분할 때는 Underline을 사용. 쇼핑몰 이미지와 이름으로 탐색할 때는 Circle을 사용.
같은 탐색 묶음에서는 하나의 유형을 유지해 항목의 역할을 일관되게 보여줘요.
2. 현재 선택한 항목을 명확히 표시해요
한 탐색 묶음에서 현재 선택한 항목은 Selected=True, 나머지는 Selected=False로 표시.
선택 상태는 기존 Tab Item의 선·색상·글자 굵기로 구분하고, 표시되는 콘텐츠와 일치시켜요.
### 예제 유형
- A. 콘텐츠 구분
- B. 쇼핑몰별 탐색
### 규격과 속성
- `Underline` / 하단선 `Gray_850` → `Gray_100` / Regular → Bold
- `Rounded` / 배경 `Gray_900` → 없음 / Regular → Bold · `Gray_400` → `Gray_Black`
- `Circle` / 주황 링 숨김 → 보임 / Regular → Medium · `Gray_400` → `Primary_Orange`
- Padding / `Spacing/50` · `100` · `250` · `400` · `500` — 비정수 4.8 / 3.6 제외
- Gap / `Spacing/0` · `100` · `150` · `250` · `300`
- 라운드 / `Corner radius/400` · `circle`
- 텍스트 색 / `Gray_100` · `Gray_400` · `Gray_500` · `Gray_Black` · `Primary_Orange`
- 선 색 / `Gray_100` · `Gray_850` · `Gray_950` · `Primary_Orange`
- 1. Tab — Master Component — `Type`: VARIANT / `Underline` · `Rounded` · `Circle`
## Text Button
Figma G:11801-5945, U:11801-5946
### 사용 기준
1. 동작을 알 수 있는 문구를 사용해요
연결할 내용이나 실행할 동작이 드러나는 문구를 사용.
참여 방법 보기·수정·삭제처럼 사용자가 누른 뒤의 결과를 예상할 수 있도록 표현해요.
2. 밑줄과 화살표로 클릭할 수 있음을 알려줘요
문장이나 안내 주변에서 링크를 구분할 때는 Underline=True를 사용.
화살표를 함께 표시하려면 Underline=False에서 Arrow=True를 사용. 밑줄형에는 화살표를 함께 표시하지 않아요.
3. 주변 정보에 맞는 크기와 굵기를 사용해요
안내 영역 안의 작은 링크는 XS, 일반적인 보조 동작은 S처럼 주변 텍스트에 맞는 크기를 사용.
금액·개수를 크게 보여주며 상세 내용으로 연결할 때는 XL과 Bold=True를 함께 사용할 수 있어요.
4. 사용 맥락에 맞는 컬러를 사용해요
보관함 이동을 강조할 때는 Primary_Orange, 설정 안내에는 Secondary_Blue 등 사용처에 맞는 컬러를 선택.
수정·삭제나 의견 남기기 같은 보조 동작에는 회색 계열을 사용할 수 있어요. 회색을 비활성 상태로 해석하지 않아요.
### 적용 시 주의
XS·S·M·XL을 제공하며 Underline=True에는 Arrow를 함께 쓰지 않아요. 회색 문구를 비활성으로 단정하지 않아요.
### 예제 유형
- A. 추가 내용 확인
- B. 보관함 이동
- C. 안내에서 설정 연결
- D. 항목 수정과 삭제
- E. 금액 상세 보기
- F. 의견 남기기
### 규격과 속성
- Color 값 / 대응 토큰
- `Primary_Orange` / `Color/Primary_Orange`
- `Secondary_Blue` / `Color/Secondary_Blue`
- `Gray_100` · `Gray_400` · `Gray_600` / `Color/Gray_*`
- 텍스트 색 / `Primary_Orange` · `Secondary_Blue` · `Gray_100` · `Gray_400` · `Gray_600`
- 밑줄 색 / 위와 동일 토큰
- Padding · Gap / 전부 0 — 바인딩 불필요
- 1. Text Button — Master Component — `Color`: VARIANT / `Gray_100` / `Primary_Orange` · `Secondary_Blue` · `Gray_100` · `Gray_400` · `Gray_600`
- 1. Text Button — Master Component — `Size`: VARIANT / `XS` / `XS` · `S` · `M` · `XL`
## Text Field
Figma G:11787-940, U:11787-941
### 사용 기준
1. 입력할 내용에 맞는 컴포넌트를 사용해요
짧은 정보는 Text Field, 할 일은 Task, 여러 줄은 Text Area예요.
2. 입력 상태에 맞게 표시해요
기본 높이80(입력60+안내20), 실제 좌우패딩24. 문서용 왼쪽0은 예외예요. Complete는 인증 성공이 아니에요.
3. 선택과 실행 기능을 구분해요
Text+Arrow는 선택, Text+Button은 요청이에요. 존재하는 Type·State 조합만 사용.
4. 인증 정보에 맞는 입력 유형과 상태를 사용해요
Birth 구분·마스킹을 유지하고 만료는 시간0:00과 오류 안내를 표시.
5. 여러 줄의 내용은 Text Area로 입력해요
Filled는 입력 유무이며 완료 검증과 별개예요.
6. 화면 목적에 맞게 높이를 고정하거나 자동으로 늘려요
Auto Height=False는 지정 높이·내부 스크롤, True는 최소80부터 실제 내용·줄바꿈·폭에 따라 확장·축소해요. 샘플260은 필수값이 아니에요.
7. 글자 수 안내가 필요할 때만 하단 표시를 켜요
Character Progress 기본False. Progress는 좌측 원형+남은 수, Counter는 우측 현재/최대예요. 표시를 꺼도 값·검증은 유지.
8. 필수 작성 조건과 최대 글자 수를 구분해요
금한돈 당첨 후기는 최소50자·최대100자예요. Progress는50에서 완료, 100은 최대 입력 제한이며 지급 완료와 달라요. 다른 사용처의 공통 제한으로 적용하지 않아요. Counter는 확장용이며 현재 사용 사례는 없어요.
### 적용 시 주의
Text Area 폭312·최소높이80·패딩16·본문/하단Gap16·하단높이20. 본문15 Regular/행간19, 하단13 Regular/아이콘Gap4. Text Container의 Placeholder/Text를 수정해요. Filled×Auto Height 4조합, 보조 Progress의 Default/In Progress/Ready/Complete와 Counter의 Default만 지원. Task 패딩 왼쪽20·오른쪽24예요.
공백·줄바꿈 포함 Array.from(value).length로 세고 한글 조합 중에도 기준 도달 즉시 체크와0을 표시. 미만 삭제 시 진행 중, 재충족 시 모션 재생이에요. 완료 원20은560ms scale .55→1.18→.92→1.06→1, 체크는120ms 뒤320ms. 모션 줄이기는 즉시 최종 상태예요.
웹 상단만30글자 시연: 초기2초 후 자음·모음 입력·삭제 반복, 직접 편집하면 정지해요. 모두 지우고blur하면 초기부터 재시작하며 값이 남으면 유지. 설정은 기본 숨김、일시정지는 우측 하단이에요. 진행률0은 주황 선을 숨겨요.
### 예제 유형
- A. 기본 정보 입력
- B. 목록에서 값 선택
- C. 인증 요청과 번호 입력
- D. 생년월일 입력
- E. 할 일 직접 입력
- F. 의견과 소감 작성
- G. 고정 높이와 자동 높이
- H. 필수 후기 작성 진행률
- I. 선택형 글자 수 카운터
### 규격과 속성
색·테두리·라운드 토큰은 개별 MD 원본을 따라요.
## Ticker
Figma G:11784-2005, U:11784-2006
### 사용 기준
1. 정보의 양과 보여주는 방식에 맞는 유형을 사용해요
한 항목씩 간결하게 보여줄 때는 Flip, 한 줄 내용을 가로로 이어 보여줄 때는 Marquee / Inline을 사용.
닉네임·당첨 정보·후기를 함께 구성해 어떤 내용인지 알 수 있도록 해요.
2. 표시 영역 안에서 내용이 이어지도록 구성해요
후기를 여러 줄로 보여줄 때는 Marquee / Card를 사용. 카드의 닉네임·당첨일·본문 구성을 유지.
한 줄 유형은 줄바꿈으로 높이를 늘리지 않고, 가로로 이어지는 내용은 표시 영역 밖으로 넘치지 않도록 처리해요.
### 적용 시 주의
Flip360×36, Inline360×50. Card는후기 Size=M194×142고정 네개·간격10·전체806×142. 현재100자 테스트문구는각6줄이어도 카드높이142를 유지해요. 최신 M 원본142·FIXED를 확인했으며 자동 높이로 구현하지 않아요. 표시창은 화면폭에 맞춰 Clip하되 높이142를 확보해요. 과거312×110의110높이를 M에 적용하지 않아요. Inline의 두 Row는 가로 반복용이며 두 줄 본문이 아니에요.
### 예제 유형
- A. 당첨 소식 요약：`Ticker / Flip` · 360 × 36
- B. 한 줄 후기 흐름：`Ticker / Marquee / Inline` · Default · 360 × 50
- C. 카드형 후기 흐름：`Ticker / Marquee / Card` · 금한돈 당첨 후기·Size=M·높이142고정
### 규격과 속성
- 후기 아이템 / 원본 세트 `Grid Scroll`12450:4229 / Size=M / 4개 (기존 문서명 Grid Scroll / Scroll Item / Review)
## Toast
Figma G:11776-502, U:11776-503
### 사용 기준
1. 문구 길이에 맞는 줄 수를 사용해요
짧은 안내나 완료 메시지는 한 줄로 표시하고, 조건 설명이 길면 두 줄로 나누어 보여줘요.
문구가 잘리거나 읽기 어렵게 줄어들지 않도록 2 Line 유형을 선택.
2. 안내 목적에 맞는 아이콘을 사용해요
한 줄로 리워드 참여를 안내할 때는 Gold, 적립 완료를 알릴 때는 Firecracker 아이콘을 사용.
두 줄로 조건을 설명하는 경우에는 아이콘 없이 문구만으로 안내.
3. 안내할 대상 아래에 배치해요
광고나 콘텐츠에 대한 안내는 대상 요소 아래에 16 간격을 두고 배치.
Toast의 폭은 대상 영역에 맞추고, 서로 겹치지 않도록 배치.
### 적용 시 주의
배경은 #222222 Fill opacity80%, 레이어 opacity100%. Opacity_Black_100(#000000·75%)으로 대체하지 않아요. 한 줄 높이44·두 줄62, 라운드16. 대상 아래16은 화면 하단 고정 오프셋이 아니에요.
### 예제 유형
- A. 리워드 참여 안내：`2 Line=False` · Gold · 「페이지 방문하고 금 받기!」
- B. 적립 조건 안내：`2 Line=True` · 아이콘 없음 · 「광고 누르고, 광고 페이지에서 / 5초 이상 머무르면 금이 적립돼요!」
- C. 적립 완료：`2 Line=False` · Firecracker · 「3금을 적립 받았어요!」
### 규격과 속성
- 문구 색 / `Color/Gray_White`
- 라운드 / `Corner radius/400`
- Padding · Gap / `Spacing/100` · `300` · `500`
- 배경 / `#222222` · 80% 직접 값 · `Opacity_Black_100`으로 대체하지 않아요
- 1. Toast — Master Component — `2 Line`: VARIANT / `True` · `False`
- 2. `Toast / Icon / Image` — `Icon`: VARIANT / `Firecracker` · `Gold`
