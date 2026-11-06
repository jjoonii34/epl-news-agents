# Notes

작업하면서 적는 메모. 위가 최신.

## 결정

- 2026-11-06 — 처음엔 벤치마크 도구를 먼저 만들려 했는데, 측정할 대상(서비스)이 먼저 있어야 해서 순서 바꿈. 평가 모듈은 v2에서 분리.
- 2026-11-06 — 기자 티어는 수동. 자동 적중률 계산은 데이터 몇 달치 쌓인 뒤에.
- 2026-11-06 — X 수집 안 함. API 비용, 약관 애매.
- 2026-11-06 — 소셜은 요약 반응 버튼만. 채점 데이터로 쓸 수 있어서. 댓글·팔로우는 v2 이후.
- 2026-11-06 — 프론트 Next.js. HTMX로 가볍게 할까 했는데 프론트도 제대로 만들어두기로.
- 2026-11-06 — 범위 빅6부터. 소스 밀도 생각하면 리버풀 하나로도 충분할 수 있음.

## 뉴스 소스

아직 하나도 실제로 안 열어봄. 열어보고 체크.

RSS 있는 곳
- BBC 축구 https://feeds.bbci.co.uk/sport/football/rss.xml — 구단별 피드도 있다고 함
- Guardian 축구 https://www.theguardian.com/football/rss — 페이지 주소 뒤에 /rss 붙이면 됨
  - 리버풀 /football/liverpool/rss
  - 이적창 /football/transfer-window/rss
- Sky Sports 뉴스 https://www.skysports.com/rss/0,20514,11095,00.xml — 축구 전용 주소 확인 필요
- Liverpool Echo https://www.liverpoolecho.co.uk/sport/football/?service=rss — 주소 확인 필요
- Football365 리버풀 https://www.football365.com/liverpool/rss2 (티어 3)

RSS 없거나 유료
- The Times (Paul Joyce), The Athletic (Ornstein, Pearce) — 본문 못 긁음
  → 구글 뉴스 RSS로 기자명 검색, 제목+링크만
  https://news.google.com/rss/search?q=%22Paul+Joyce%22+Liverpool&hl=en-GB&gl=GB&ceid=GB:en
- NewsNow — 집계 사이트, RSS 없음, 약관 확인
- liverpoolfc.com — RSS 있는지 모름

경기 데이터
- football-data.org — 무료, 5대 리그 결과·순위·득점. 분당 10회
- API-Football — 상세 스탯 있음. 무료 하루 100회, 유료 월 2~3만원. v2에서
- TheSportsDB — 백업

확인할 것
- [ ] 위 주소 전부 열어보기, 최근 글 날짜
- [ ] robots.txt
- [ ] 하루 리버풀 관련 글 수. 20개 안 되면 소스 추가
- [ ] 구글 뉴스 RSS가 기자명으로 걸러지는지

## 기자 티어

소속은 기억으로 쓴 거. 시드 넣기 전에 확인.

- 0: 구단/리그 공식
- 1: 사실상 공식급. 이적 확정, 부상 공식을 거의 처음 내는 사람
- 2: 구단 전담. 확정 전 단계 기사 많음
- 3: 나머지

피드 가중치 1.0 / 1.0 / 0.7 / 0.3. 근거 없음, 돌려보고 조정.

티어 1
- Fabrizio Romano — 프리랜서
- David Ornstein — The Athletic
- Paul Joyce — The Times
- James Pearce — The Athletic, 리버풀

티어 2 (리버풀)
- Ian Doyle — Liverpool Echo
- David Lynch — 프리랜서?
- Chris Bascombe — Telegraph
- Lewis Steele — Daily Mail
- Neil Jones — GOAL?

티어 2 (전국)
- Sami Mokbel — BBC
- Rob Dawson — ESPN

나머지 빅6 전담은 아직. 구단당 2명.

## 품질 지표 (목표)

- 할루시네이션률 10% 이하
- 핵심 사실 누락률 15% 이하
- 판정자-사람 κ 0.7 이상
- 피드 상위 5개 중 티어 1~2 비율 80% 이상
- 수집 성공률 95% 이상, 요약 30초 안

## 모르는 것

- Athletic 기사는 제목+리드만으로 요약에 쓸 만한가
- issue 묶기: 임베딩 + 48시간 창으로 되나, 선수 이름 매칭 필요한가
- 요약 한국어만 할지 영어도 둘지
- 경기 결과를 피드에 섞을지 탭을 따로 둘지
