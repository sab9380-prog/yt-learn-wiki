---
type: synth
concept: vector-search
---

# 🧭 벡터 검색 — 종합

> 자동 생성 · 4개 노트 종합 (수정 금지)

# 벡터 검색 (Vector Search)

## 핵심 원리 — 4개 노트가 공통으로 말하는 것

벡터 검색은 **텍스트를 수백~수천 차원의 숫자 좌표(벡터)로 변환**해서 저장하고, 검색할 때 *단어 일치*가 아닌 *의미적 유사성*으로 결과를 찾는 방식이다. '자동차'로 검색해도 '차량'이 나오는 것처럼, 표현이 달라도 뜻이 비슷하면 찾아준다. [[2026-05-22-카파시도-못-말한-LLM-Wiki의-진실]] [[2026-05-22-The-7-Levels-of-Claude-Code-RAG]]

---

## 다른 관점·강조

| 노트 | 강조점 |
|------|--------|
| [[2026-05-22-The-7-Levels-of-Claude-Code-RAG]] | 벡터 DB는 의미 유사성 기반 검색을 가능하게 하는 *인프라*. 일반 DB는 2차원(행·열), 벡터 DB는 수백~수천 차원 |
| [[2026-05-22-카파시도-못-말한-LLM-Wiki의-진실]] | 벡터 임베딩은 *기술적으로 작동*하지만, 지속 가능성은 입력 마찰과 검색 빈도에 달림. 5,000개 노트 초기 비용 약 12,000원 |
| [[2026-06-15-Skill-Review-GBrain-인공지능-에이전트가-사용자의]] [[2026-06-15-Build-a-second-brain-with-Gbrain-memory]] | 벡터 검색은 *단독 사용보다 하이브리드로* 써야 강력. 키워드 정확성 + 벡터 의미 유연성을 동시에 활용 |

---

## 실전 적용

- **하이브리드 검색이 실전 정답**: 벡터만 쓰면 정확한 고유명사를 놓치고, 키워드만 쓰면 표현이 다를 때 실패. 두 방식 + 관계 검색까지 합쳐야 높은 정확도. [[2026-06-15-Build-a-second-brain-with-Gbrain-memory]] [[2026-06-15-Skill-Review-GBrain-인공지능-에이전트가-사용자의]]
- **한국어 환경 주의**: 임베딩 모델에 따라 한국어 검색 품질이 크게 달라짐. BGE-M3 vs OpenAI embedding 비교 테스트 필요. [[2026-05-22-카파시도-못-말한-LLM-Wiki의-진실]]
- **질문 확장 전략**: 질문 하나를 받으면 여러 유사 질문으로 확장해서 더 넓게 검색하면 성능이 올라감. [[2026-06-15-Skill-Review-GBrain-인공지능-에이전트가-사용자의]]

---

## 상충·주의점

- 벡터 검색은 기술 자체보다 **콘텐츠를 지속적으로 쌓는 것**이 병목. 시스템을 구축한 사람의 90% 이상이 3개월 내 포기. [[2026-05-22-카파시도-못-말한-LLM-Wiki의-진실]]
- 벡터 검색 단독으로는 RAG 시스템의 일부일 뿐. 실제 AI 기억 문제를 해결하려면 벡터 검색 + 청킹 전략 + 스킬 플레이북까지 조합 필요. [[2026-06-15-Skill-Review-GBrain-인공지능-에이전트가-사용자의]] [[2026-05-22-The-7-Levels-of-Claude-Code-RAG]]

---

## 한 줄 정의

> **벡터 검색이란, 텍스트의 '의미'를 숫자 좌표로 바꿔 저장하고 단어가 아닌 뜻의 유사성으로 정보를 찾는 기술로, AI가 외부 지식을 정확하게 검색하는 핵심 엔진이다.**

---
## 📎 참조 노트 (클릭 → 원문)
- [Build a second brain with Gbrain - memory for AI agents](https://github.com/sab9380-prog/yt-learn-wiki/blob/main/notes/2026-06-15-Build-a-second-brain-with-Gbrain-memory.md)
- [[Skill Review] GBrain, 인공지능 에이전트가 사용자의 개인적인 삶과 지식을 깊이 있게 학습할 수 있도록 돕는 Skill](https://github.com/sab9380-prog/yt-learn-wiki/blob/main/notes/2026-06-15-Skill-Review-GBrain-인공지능-에이전트가-사용자의.md)
- [The 7 Levels of Claude Code & RAG](https://github.com/sab9380-prog/yt-learn-wiki/blob/main/notes/2026-05-22-The-7-Levels-of-Claude-Code-RAG.md)
- [카파시도 못 말한 LLM-Wiki의 진실: 개인 지식 베이스가 망하는 이유 | #NEWIT](https://github.com/sab9380-prog/yt-learn-wiki/blob/main/notes/2026-05-22-카파시도-못-말한-LLM-Wiki의-진실.md)

---
- 개념 페이지: [[_concept-vector-search]]
- [[INDEX]]
