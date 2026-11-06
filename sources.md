# 데이터 소스 조사표

작성일: 2026-11-06 · 상태: 1차 후보. "확인" 칸은 실제로 URL을 열어 채운다.

| 구분 | 소스 | URL / 접근 방식 | 갱신 주기 | 약관상 수집 | 확인 | 비고 |
| --- | --- | --- | --- | --- | --- | --- |
| 전국구 | BBC Sport Football | RSS `https://feeds.bbci.co.uk/sport/football/rss.xml` | 수시 | 개인·비상업 가능(확인) | [ ] | 공식 발표 빠름, 티어 1급 |
| 전국구 | The Guardian Football | RSS `https://www.theguardian.com/football/rss` | 수시 | Open Platform API 있음 | [ ] | 구단별: `/football/liverpool/rss` |
| 전국구 | Sky Sports Football | RSS `https://www.skysports.com/rss/12040` | 수시 | 확인 필요 | [ ] | 이적 속보 많음 |
| 전국구 | The Times (폴 조이스) | 유료, RSS 제한 | | 불가 추정 | [ ] | Google News 바이라인 검색으로 우회 |
| 전국구 | The Athletic (온스테인·피어스) | 유료 | | 불가 추정 | [ ] | 동일하게 우회, 제목·리드만 |
| 지역 | Liverpool Echo | RSS `https://www.liverpoolecho.co.uk/sport/football/?service=rss` | 수시 | 확인 필요 | [ ] | 구단 전담 기자 다수 |
| 집계 | Google News RSS | `https://news.google.com/rss/search?q="Paul Joyce" Liverpool&hl=en-GB&gl=GB&ceid=GB:en` | 수시 | 개인 용도 가능(확인) | [ ] | 기자명 검색으로 기자 태깅 가능. 원문은 링크 따라가야 함 |
| 집계 | NewsNow 리버풀 이적 | HTML `https://www.newsnow.co.uk/h/Sport/Football/Premier+League/Liverpool/Transfer+News` | 실시간 | 확인 필요 | [ ] | RSS 없음, 스크래핑 약관 확인 |
| 구단 공식 | Liverpool FC 공식 | `https://www.liverpoolfc.com/news` (RSS 여부 확인) | 수시 | 확인 필요 | [ ] | 티어 0(공식 발표) 역할 |
| 기자 개인 | 로마노 Substack/YouTube | RSS 확인 | | | [ ] | |

## 결정 (ADR-001 근거)

1. 1차 수집은 RSS가 공개된 소스(BBC·Guardian·Sky·Echo)로 시작한다.
2. 유료 매체 소속 기자는 Google News RSS 바이라인 검색으로 제목·요약·링크만 수집하고, 원문 전문은 저장하지 않는다.
3. X 수집은 API 비용과 약관 문제로 MVP에서 제외한다.

## 확인 절차 (1주차)

- [ ] 각 URL을 브라우저에서 열어 응답 여부, 최근 항목 날짜, 본문 포함 여부 기록
- [ ] robots.txt 와 이용약관에서 자동 수집 조항 확인
- [ ] 하루 동안 리버풀 관련 항목 수를 세어 밀도 기록 (목표: 소스 합산 일 20건 이상)
