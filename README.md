# 청담 모바일 시안

- cheongdam-2a.html — 주황 시안 (2a)
- cheongdam-3b.html — 블루 1열 대형카드 시안 (3b)
- CleanApp.dc.html — 실제 화면·데이터·로직 (두 시안 공통, `theme` / `layout` 속성으로 분기)
- support.js — 런타임 (수정 불필요)

## 실행
파일을 직접 더블클릭하면 브라우저 보안 정책 때문에 CleanApp을 못 불러옵니다.
VS Code 확장 **Live Server** 설치 → `cheongdam-2a.html` 우클릭 → "Open with Live Server".

## 수정 위치 (CleanApp.dc.html)
- 색상: `THEMES` (orange / blue)
- 내 주변 청소업체 데이터: `NEAR`
- 시공 카테고리 업체 데이터: `BUILD`
- 카테고리/아이콘: `CATS`, `catIcons`
- 사진: `IMG` (Unsplash 샘플 → 실사진 경로로 교체)
