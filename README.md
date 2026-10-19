# 청담 모바일 시안

- cheongdam-2a.html — 주황 · 아이콘 카테고리 + 1열 대형카드 · 화이트 상단바(풀폭 배너)
- cheongdam-3b.html — 블루 · 사진 카테고리 + 리스트 · 컬러 상단바(사진 배너)
- CleanApp.dc.html — 실제 화면·데이터·로직 (두 시안 공통)
- support.js — 런타임 (수정 불필요)

## 시안 속성 (html 파일의 dc-import)
- theme: orange / blue
- layout: large(아이콘·대형카드) / 생략(사진·리스트)
- header: white / color

## 실행
파일을 직접 더블클릭하면 브라우저 보안 정책 때문에 CleanApp을 못 불러옵니다.
VS Code 확장 **Live Server** 설치 → `cheongdam-2a.html` 우클릭 → "Open with Live Server".

## 수정 위치 (CleanApp.dc.html)
- 색상: `THEMES` (orange / blue)
- 내 주변 청소업체 데이터: `NEAR`
- 시공 카테고리 업체 데이터: `BUILD`
- 카테고리/아이콘: `CATS`, `catIcons`
- 사진: `IMG` (Unsplash 샘플 → 실사진 경로로 교체)
