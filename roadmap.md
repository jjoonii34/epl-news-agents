# Roadmap

## v1 

리버풀 중심. 뉴스 요약 + 품질 측정 + 경기 결과.

- [ ] 기획: 소스 확인, 기자 티어, 테스트셋 50건
- [ ] DB 스키마, Docker Compose
- [ ] 수집 (LangGraph): RSS → 중복 제거 → 기자 태깅
- [ ] issue 묶기 (pgvector) + 요약 v1
- [ ] 평가: LLM 판정자, 직접 채점 30건, κ
- [ ] 반복 측정, 요약 v2, 모델 비교
- [ ] 피드 API, 반응 버튼
- [ ] Next.js 화면, 관리자 대시보드
- [ ] 경기 결과 (football-data.org)
- [ ] 배포 (Supabase, Fly, Vercel), cron, 비용 상한
- [ ] README에 수치

안 하는 것: X 수집, 라이브 스코어, 선수 상세 스탯, 푸시, 소셜.

## v2 

- 5대 리그 결과·순위·득점/도움 랭킹, 선수 페이지
- 상세 스탯은 무료 API에 없음. 유료(API-Football) 전환 여부 이때 결정
- 평가 모듈을 별도 패키지로 분리 (llm-rec-bench, llm-sweep)
- k8s 매니페스트 + kind/k3s 배포 (실서비스는 Fly 유지)

## v3

- 한국인 선수 출전·스탯 알림
- 경기 후 한국어 리뷰 자동 생성 (v1 평가 파이프라인 재사용)
- 한국 시간 기준 일정
- 푸시
