---
type: synth
concept: vector-search
---

# 🧭 벡터 검색 — 종합

> 자동 생성 · 4개 노트 종합 (수정 금지)

# 벡터 검색 (Vector Search)

## 핵심 메커니즘

벡터 검색은 **텍스트를 수백~수천 차원의 숫자 좌표(임베딩)로 변환해 저장**하고, 의미가 비슷한 것들끼리 공간상 가까이 배치하는 방식으로 작동한다. '자동차'로 검색해도 '차량'을 찾을 수 있는 것처럼, **글자가 달라도 의미가 같으면 연결**된다. [[2026-05-22-카파시도-못-말한-LLM-Wiki의-진실]] [[2026-05-22-The-7-Levels-of-Claude-Code-RAG]]

## 노트들이 공통으로 강조하는 것

모든 노트가 벡터 검색을 **단독으로 쓰지 않고 '하이브리드 검색'의 한 축**으로 사용한다고 말한다. 키워드 검색(정확성) + 벡터 검색(의미적 유연성)을 결합해야 한쪽의 한계를 보완한다는 것. [[2026-06-15-Build-a-second-brain-with-Gbrain-memory]] [[2026-06-15-Skill-Review-GBrain-인공지능-에이전트가-사용자의]]

## 서로 다른 강조점

| 노트 | 포커스 |
|---|---|
| G-Brain 두 편 | 벡터 검색을 AI 에이전트의 **장기 기억** 인프라로 봄 |
| 7 Levels of RAG | **Vector DB**를 RAG 시스템의 핵심 부품으로 단계적 도입 권장 |
| LLM-Wiki 진실 | 한국어 임베딩 모델 선택, 비용(5천 노트 ≈ 1.2만원), **지속성**이 진짜 문제라고 경고 |

## 실전 주의점

- 벡터 검색 자체보다 **"입력 마찰이 검색 가치보다 크면 시스템은 죽는다"**는 게 핵심 함정. 기술이 작동해도 꾸준히 노트를 넣지 않으면 무용지물 [[2026-05-22-카파시도-못-말한-LLM-Wiki의-진실]]
- 한국어 환경에서는 임베딩 모델 선택(BGE-M3 vs OpenAI)이 검색 정확도를 좌우함 [[2026-05-22-카파시도-못-말한-LLM-Wiki의-진실]]
- 최고 수준의 벡터 DB 시스템이 필요한 사람은 소수. 대부분은 Obsidian 수준으로 충분 [[2026-05-22-The-7-Levels-of-Claude-Code-RAG]]

---

## 한 줄 정의
벡터 검색이란 텍스트를 의미 기반 숫자 좌표로 변환해, 글자가 달라도 뜻이 비슷하면 찾아주는 검색 방식이다.

---
## 📎 참조 노트 (클릭 → 원문)
- [Build a second brain with Gbrain - memory for AI agents](https://github.com/sab9380-prog/yt-learn-wiki/blob/main/notes/2026-06-15-Build-a-second-brain-with-Gbrain-memory.md)
- [[Skill Review] GBrain, 인공지능 에이전트가 사용자의 개인적인 삶과 지식을 깊이 있게 학습할 수 있도록 돕는 Skill](https://github.com/sab9380-prog/yt-learn-wiki/blob/main/notes/2026-06-15-Skill-Review-GBrain-인공지능-에이전트가-사용자의.md)
- [The 7 Levels of Claude Code & RAG](https://github.com/sab9380-prog/yt-learn-wiki/blob/main/notes/2026-05-22-The-7-Levels-of-Claude-Code-RAG.md)
- [카파시도 못 말한 LLM-Wiki의 진실: 개인 지식 베이스가 망하는 이유 | #NEWIT](https://github.com/sab9380-prog/yt-learn-wiki/blob/main/notes/2026-05-22-카파시도-못-말한-LLM-Wiki의-진실.md)

---
- 개념 페이지: [[_concept-vector-search]]
- [[INDEX]]
