# 청담 모바일 시안

주황(A) · 블루(B) 두 시안. 화면·데이터·로직은 `CleanApp.dc.html` 하나를 공유하고, 레이아웃은 `dc-import` 속성으로 분기합니다.

- index.html — 시안 선택 화면
- cheongdam-a.html — **A · 주황** (화이트 상단바 · 아이콘 카테고리 · 대형 포토카드)
- cheongdam-b.html — **B · 블루** (컬러 상단바 · 사진 카테고리 · 가로형 리스트)
- CleanApp.dc.html — 실제 화면·데이터·로직
- cheongdam-color-system.md — 컬러 토큰 정의와 용도
- assets/ — 로고 SVG, 배너 사진 / font/ — 로컬 프리텐다드
- support.js — 런타임 (수정 불필요)

## 시안 속성 (html 파일의 dc-import)
- theme: orange / blue
- layout: large(아이콘·대형카드) / 생략(사진·리스트)
- header: white / color

## 실행
파일을 직접 더블클릭하면 브라우저 보안 정책 때문에 CleanApp을 못 불러옵니다.
VS Code 확장 **Live Server** 설치 → `index.html` 우클릭 → "Open with Live Server".

## 수정 위치 (CleanApp.dc.html)
- 색상: `THEMES` (orange / blue) — 토큰 정의와 용도는 `cheongdam-color-system.md`
- 내 주변 청소업체 데이터: `NEAR`
- 시공 카테고리 업체 데이터: `BUILD` (거리는 `DIST0`·`bdist()`로 시·도 기준 자동 계산)
- 카테고리/아이콘: `CATS`, `catIcons`
- 배너 사진: `bannerImg` / 카드 사진: `IMG`

## 타이포 규격
폰트: 로컬 프리텐다드 (`font/pretendard.css`, `.woff` 9종).
자간은 전 단계 `0`, 행간은 기본 `1.4`(공용 `body`), 굵기는 **800 / 700 / 500** 세 개만, 크기는 **13px이 최소**다.

| 단계 | 크기 | 굵기 | 쓰임 |
|---|---|---|---|
| 헤드라인 | 26px | 800 | 홈 로고, 업체 상세명 |
| 제목 | 20px | 800 | 섹션 제목, 배너 카피, 화면·시트 제목 |
| 부제 | 18px | 800 | 업체 카드명, 상세 섹션 제목, 리스트 타이틀 |
| 본문 | 15px | 500 | 설명, 메타 정보, 입력 |
| 캡션 | 13px | 500 | 배지·칩, 지역·거리·별점 표기, 보조 설명 |

- **700은 버튼·배지·칩·탭 등 누르는 요소와 강조 라벨 전용.** 크기는 그 자리의 단계를 따른다.
- 굵기·행간을 쓰지 않은 텍스트는 공용 `body{font-weight:500;line-height:1.4}`가 받는다.
- 두 줄 이상 넘어가는 헤드라인·제목 카피(배너 `전화 한 통으로 / 우리 동네 견적 비교`)는 `1.3`.
- 예외: 상세 평점 숫자 `34px/800`, 전화번호 `28px/800`, 그리고 `▼ ‹ × ♥` 기호 글리프(`line-height:1` 유지).
