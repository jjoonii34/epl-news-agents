# 뉴스 소스

어디서 긁어올지 정리. 아직 하나도 실제로 안 열어봄. 열어보고 되는 거 / 안 되는 거 체크 예정.

## RSS 있는 곳 (여기부터 시작)

- BBC Sport Football — https://feeds.bbci.co.uk/sport/football/rss.xml
  공식 발표 제일 빠른 편. 리버풀만 거르려면 제목/본문에 Liverpool 포함 여부로.
- Guardian Football — https://www.theguardian.com/football/rss
  구단별 피드가 따로 있음: https://www.theguardian.com/football/liverpool/rss
  Open Platform API도 있는데 일단 RSS로.
- Sky Sports Football — https://www.skysports.com/rss/12040
  이적 속보 많음. 추측 기사도 많아서 티어 3 취급.
- Liverpool Echo — https://www.liverpoolecho.co.uk/sport/football/?service=rss
  Ian Doyle 등 전담 기자. RSS 주소 맞는지 확인 필요.

## RSS 없거나 유료

- The Times (Paul Joyce) — 유료. 본문 못 긁음.
- The Athletic (Ornstein, Pearce) — 유료. 마찬가지.
  → 둘 다 구글 뉴스 RSS로 기자 이름 검색해서 제목+링크만 가져오는 걸로.
  https://news.google.com/rss/search?q=%22Paul+Joyce%22+Liverpool&hl=en-GB&gl=GB&ceid=GB:en
  (James Pearce, David Ornstein 도 같은 식)
- NewsNow 리버풀 이적 — https://www.newsnow.co.uk/h/Sport/Football/Premier+League/Liverpool/Transfer+News
  RSS 없음. 집계 사이트라 스크래핑 약관 봐야 함. 급하진 않음.
- liverpoolfc.com 공식 뉴스 — RSS 있는지 모름. 있으면 티어 0으로.
- 로마노 — Substack이나 유튜브 RSS 있을 듯. 확인.

## 결정한 것

1. 처음엔 RSS 열린 네 곳(BBC, Guardian, Sky, Echo)만.
2. 유료 매체 기자는 구글 뉴스 RSS로 제목/리드/링크만 저장. 본문은 안 긁음.
3. X 수집은 안 함.

## 할 일

- [ ] 위 URL 전부 브라우저에서 열어보기. 열리면 최근 글 날짜 적기
- [ ] 각 사이트 robots.txt 확인
- [ ] 하루 동안 리버풀 관련 글 몇 개 나오는지 세기. 합쳐서 20개 안 나오면 소스 더 찾아야 함
- [ ] 구글 뉴스 RSS가 기자 이름으로 진짜 걸러지는지 확인
