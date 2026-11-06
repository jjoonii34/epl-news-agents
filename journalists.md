# 기자 티어 표 (초안)

작성일: 2026-11-06 · 소속은 2026-11 기준 확인 필요. 이 표가 `scripts/seed.py`의 시드 데이터가 된다.

## 티어 기준

| 티어 | 정의 | 피드 가중치(초안) |
| --- | --- | --- |
| 0 | 구단·리그 공식 발표 | 1.0 |
| 1 | 공식 발표 수준의 정확도. 이적 확정("here we go")·부상 공식 소식을 사실상 최초 보도 | 1.0 |
| 2 | 구단 전담 기자. 내부 사정에 밝으나 확정 전 단계 보도가 많음 | 0.7 |
| 3 | 일반 매체·집계·타블로이드. 추측성 포함 | 0.3 |

## 전국구

| 이름 | 소속(확인 필요) | 티어 | 커버 구단 | 수집 경로 |
| --- | --- | --- | --- | --- |
| Fabrizio Romano | 프리랜서 / CaughtOffside | 1 | 전체 | Google News 바이라인, Substack |
| David Ornstein | The Athletic | 1 | 전체 (아스널·리버풀 강점) | Google News 바이라인 |
| Paul Joyce | The Times | 1 | 리버풀·북서부 | Google News 바이라인 |
| Sami Mokbel | BBC Sport | 2 | 전체 | BBC RSS |
| Rob Dawson | ESPN | 2 | 맨유·맨시티 | Google News 바이라인 |

## 리버풀 전담

| 이름 | 소속(확인 필요) | 티어 | 수집 경로 |
| --- | --- | --- | --- |
| James Pearce | The Athletic | 1 | Google News 바이라인 |
| David Lynch | 프리랜서 (Liverpool.com 등) | 2 | Google News 바이라인 |
| Ian Doyle | Liverpool Echo | 2 | Echo RSS |
| Chris Bascombe | The Telegraph | 2 | Google News 바이라인 |
| Lewis Steele | Daily Mail | 2 | Google News 바이라인 |
| Neil Jones | GOAL / 프리랜서 | 2 | Google News 바이라인 |

## 나머지 빅6 전담 (2주차에 2명씩 채운다)

| 구단 | 기자 1 | 기자 2 |
| --- | --- | --- |
| 아스널 | | |
| 맨시티 | | |
| 첼시 | | |
| 맨유 | | |
| 토트넘 | | |

## 티어 3 (일반)

BBC·Guardian·Sky 바이라인 없는 기사, NewsNow 집계, 타블로이드 전반. 기자 개별 등록 없이 소스 단위로 티어 3 부여.

## ADR-002 근거

자동 신뢰도 추정(예: 과거 보도의 실제 적중률 계산)은 데이터가 쌓인 뒤에나 가능하다. MVP는 수동 배정으로 시작하고, "정확해요/틀렸어요" 반응이 쌓이면 Could 기능으로 재조정한다.
