---
title: "AI가 까먹는 진짜 이유 | Anthropic 컨텍스트 엔지니어링 완벽 가이드"
source_url: https://youtube.com/watch?v=aa-zYgWV00g
video_id: aa-zYgWV00g
source_type: youtube
lang: ko
analyzed: 2026-06-24
category: 일반학습
status: active
---
# AI가 까먹는 진짜 이유 | Anthropic 컨텍스트 엔지니어링 완벽 가이드

## 🧠 이해 (Understand)
- **Summary:** Anthropic이 공개한 '컨텍스트 엔지니어링' 가이드를 정리한 영상입니다. 프롬프트 엔지니어링이 일회성 작업에 국한된다면, 컨텍스트 엔지니어링은 AI에게 어떤 정보를 언제 얼마나 줄지를 전략적으로 설계하는 반복 프로세스입니다. AI는 '주의력 예산'이 한정되어 있어 정보를 과도하게 주면 컨텍스트 포이즈닝·디스트랙션·컨퓨전·클래시 4가지 문제가 발생합니다. 이를 해결하는 핵심 전략은 '저스트 인 타임 컨텍스트'로, 처음부터 모든 정보를 넣지 않고 필요한 순간에만 제공하는 방식입니다. 긴 작업에서는 '과역 패턴'과 '조기 완료 패턴'이라는 두 가지 실패 유형이 발견되었고, 이를 막기 위해 초기화 에이전트와 실행 에이전트를 분리하는 '하네스 패턴'을 제안합니다. 상태 기록은 마크다운보다 JSON이 AI의 임의 수정을 줄인다는 실험적 발견도 포함됩니다. 긴 작업 관리의 세 전략은 압축(새 세션 시작), 구조화된 메모(외부 파일 노트), 서브 에이전트(역할 분산)입니다.
- **Core Message:** AI 실력은 모델이 아니라 컨텍스트 설계에서 갈린다 — 무엇을 언제 얼마나 줄지를 전략적으로 관리하라.
> AI의 실력은 모델이 아니라 컨텍스트에서 갈립니다.
> 프롬프트 엔지니어링은 일회성 작업에 대한 것이고 컨텍스트 엔지니어링은 반복적인 프로세스다.
> AI가 JSON을 코드로 인식해서 함부로 건드리지 않는 거예요.
❗ 상태 기록을 마크다운 대신 JSON으로 했을 때 AI가 임의로 수정하는 경우가 훨씬 줄었다 — AI가 JSON을 '코드'로 인식해 수정을 자제하기 때문.
❗ Anthropic이 AI로 포켓몬 게임을 플레이시켰을 때, AI가 스스로 노트를 작성해 1,000스텝이 넘는 진행을 정확히 추적했다.
❗ Anthropic은 긴 대화의 '압축'보다 아예 새 세션으로 시작하는 것을 더 권장한다.

## 📚 핵심 용어
- **컨텍스트 엔지니어링:** AI에게 어떤 정보를 언제 얼마나 줄지를 전략적으로 설계하는 반복 프로세스. / 요리사가 재료를 한꺼번에 쏟지 않고, 단계마다 필요한 재료만 꺼내 놓는 것과 같다. / 프롬프트 엔지니어링은 질문 하나를 잘 쓰는 것, 컨텍스트 엔지니어링은 대화 전체 흐름을 설계하는 것이다.
- **컨텍스트 러트 (Context Rot):** 정보를 너무 많이 넣으면 AI가 오히려 중요한 것을 놓치게 되는 현상. / 신입사원 첫날에 회사 매뉴얼 전권을 주면 오늘 할 일조차 기억 못 하는 것과 같다. / 단순 토큰 초과(길이 문제)와 달리, 러트는 양이 적어도 무관한 정보가 섞이면 발생하는 질(質)의 문제다.
- **저스트 인 타임 컨텍스트:** 처음부터 모든 정보를 제공하지 않고, 필요한 순간에만 필요한 정보를 전달하는 전략. / 창고에 모든 물건을 쌓아두지 않고, 주문이 들어올 때만 꺼내 배송하는 JIT 재고 방식과 같다. / 사전 로딩(미리 다 넣기)은 메모리를 한번에 소진하고, JIT는 주의력 예산을 아끼며 정확도를 유지한다.
- **하네스 패턴:** 긴 작업을 초기화 에이전트와 실행 에이전트로 분리해 세션별로 역할을 나누는 구조. / 팀장이 프로젝트 계획서를 만들고, 팀원이 항목 하나씩 처리한 뒤 체크리스트에 기록하는 방식이다. / 단일 에이전트가 모든 걸 처리하면 컨텍스트가 바닥나지만, 하네스는 역할 분리로 각 세션을 가볍게 유지한다.

## 🚀 실행 (Execute)
- [ ] 현재 반복적으로 쓰는 AI 작업 하나를 골라 '저스트 인 타임 컨텍스트' 방식으로 재설계하기
  - 담당: 나
  - 이유: 정보를 한꺼번에 넣는 기존 방식이 컨텍스트 러트의 주원인이며, 이 하나만 바꿔도 긴 작업의 정확도가 즉시 올라간다.
- [ ] 긴 AI 작업 시 '하네스 패턴' 템플릿 만들기
  - 담당: 나
  - 이유: 과역 패턴·조기 완료 패턴을 예방하는 구조적 장치이며, 한번 만들어두면 모든 프로젝트에 재사용 가능하다.
- 자료: Anthropic 공식 블로그 — 'Context Engineering' 원문 가이드 (anthropic.com 검색 권장, 직접 URL은 확인 필요)
- 자료: Claude Code 공식 문서 — CLAUDE.md 설정 및 하이브리드 컨텍스트 전략 설명 (docs.anthropic.com, 확인 필요)
- Timeline: 1주차: 기존 작업 1개에 저스트 인 타임 방식 적용 및 효과 비교 → 2주차: 하네스 패턴 JSON 템플릿 제작 및 첫 실전 적용 → 이후: 서브 에이전트 분리 실험으로 확장

## 🔗 연결
- 카테고리: [[_category-일반학습]]

## 📝 자막 전문
- [0:00](https://youtube.com/watch?v=aa-zYgWV00g&t=0) 은 AI한테 한시간 넘게 작업을
- [0:01](https://youtube.com/watch?v=aa-zYgWV00g&t=1) 시켰는데 갑자기 처음에 합의한 내용을
- [0:03](https://youtube.com/watch?v=aa-zYgWV00g&t=3) 까먹어 버립니다. 분명히 똑똑한
- [0:04](https://youtube.com/watch?v=aa-zYgWV00g&t=4) 모델인데 왜 긴 작업만 하면 이렇게
- [0:07](https://youtube.com/watch?v=aa-zYgWV00g&t=7) 되는 걸까요? 엔스로픽이이 문제의
- [0:08](https://youtube.com/watch?v=aa-zYgWV00g&t=8) 근본 원인과 해결법을 공개했습니다.
- [0:10](https://youtube.com/watch?v=aa-zYgWV00g&t=10) 안녕하세요. 클로디컬입니다. 오늘은
- [0:12](https://youtube.com/watch?v=aa-zYgWV00g&t=12) 엔스로픽이 공개한 컨텍스트 엔지니어링
- [0:14](https://youtube.com/watch?v=aa-zYgWV00g&t=14) 완벽 가이드를 정리해 드릴 건데요.
- [0:15](https://youtube.com/watch?v=aa-zYgWV00g&t=15) 프롬프트만 잘 쓰면 된다는 시대는
- [0:17](https://youtube.com/watch?v=aa-zYgWV00g&t=17) 끝났고 AI를 진짜 잘 다루려면이
- [0:19](https://youtube.com/watch?v=aa-zYgWV00g&t=19) 개념을 꼭 알아야 합니다. 지금까지
- [0:21](https://youtube.com/watch?v=aa-zYgWV00g&t=21) AI 잘 쓰는 법이라고 하면
- [0:22](https://youtube.com/watch?v=aa-zYgWV00g&t=22) 프롬프트를 잘 쓰는 거라고 생각하셨을
- [0:24](https://youtube.com/watch?v=aa-zYgWV00g&t=24) 거예요. 역할을 정해 줘라. 단계별로
- [0:26](https://youtube.com/watch?v=aa-zYgWV00g&t=26) 생각하게 해라. 이런 팁들 많이
- [0:28](https://youtube.com/watch?v=aa-zYgWV00g&t=28) 보셨잖아요. 근데 엔스로픽이 이번에
- [0:30](https://youtube.com/watch?v=aa-zYgWV00g&t=30) 아주 명확하게 선언합니다. 프롬프트
- [0:31](https://youtube.com/watch?v=aa-zYgWV00g&t=31) 엔지니어링은 일회성 작업에 대한
- [0:33](https://youtube.com/watch?v=aa-zYgWV00g&t=33) 것이고 컨텍스트 엔지니어링은 반복적인
- [0:36](https://youtube.com/watch?v=aa-zYgWV00g&t=36) 프로세스다. 컨텍스트 엔지니어링이
- [0:38](https://youtube.com/watch?v=aa-zYgWV00g&t=38) 뭐냐면요. AI에게 어떤 정보를 주고
- [0:40](https://youtube.com/watch?v=aa-zYgWV00g&t=40) 어떤 정보를 빼고 언제 어떤 정보를
- [0:42](https://youtube.com/watch?v=aa-zYgWV00g&t=42) 전달할지를 설계하는 거예요. 시스템
- [0:44](https://youtube.com/watch?v=aa-zYgWV00g&t=44) 프롬프트뿐만 아니라 도구 정의, 외부
- [0:46](https://youtube.com/watch?v=aa-zYgWV00g&t=46) 데이터, 대화 히스토리까지 모든
- [0:48](https://youtube.com/watch?v=aa-zYgWV00g&t=48) 토큰을 전략적으로 관리하는 겁니다.
- [0:49](https://youtube.com/watch?v=aa-zYgWV00g&t=49) 여기서 핵심 개념이 나오는데요.
- [0:51](https://youtube.com/watch?v=aa-zYgWV00g&t=51) 컨텍스트 러트라는 겁니다. 정보를
- [0:53](https://youtube.com/watch?v=aa-zYgWV00g&t=53) 많이 줄수록 오히려 AI가 중요한 걸
- [0:55](https://youtube.com/watch?v=aa-zYgWV00g&t=55) 놓치게 되는 현상이에요. 비율를 해
- [0:56](https://youtube.com/watch?v=aa-zYgWV00g&t=56) 볼게요. 신입 사원 첫날에 회사
- [0:58](https://youtube.com/watch?v=aa-zYgWV00g&t=58) 매뉴얼 정권을 던져 주면 어떻게
- [1:00](https://youtube.com/watch?v=aa-zYgWV00g&t=60) 될까요? 오늘 당장 해야 할 일은
- [1:01](https://youtube.com/watch?v=aa-zYgWV00g&t=61) 기억도 못 하잖아요. AI도
- [1:03](https://youtube.com/watch?v=aa-zYgWV00g&t=63) 똑같습니다. 엔스로픽은 이걸 주의력
- [1:05](https://youtube.com/watch?v=aa-zYgWV00g&t=65) 예산이라고 표현하거든요. AI한테도
- [1:07](https://youtube.com/watch?v=aa-zYgWV00g&t=67) 한 번에 집중할 수 있는 양이 정해져
- [1:08](https://youtube.com/watch?v=aa-zYgWV00g&t=68) 있다는 뜻이에요. 그리고이 예산을
- [1:10](https://youtube.com/watch?v=aa-zYgWV00g&t=70) 초과하면네 가지 문제가 생깁니다.
- [1:11](https://youtube.com/watch?v=aa-zYgWV00g&t=71) 잘못된 정보가 추론을 오염시키는
- [1:13](https://youtube.com/watch?v=aa-zYgWV00g&t=73) 컨텍스트 포이닝. 무관한 정보가
- [1:15](https://youtube.com/watch?v=aa-zYgWV00g&t=75) 핵심에서 관심을 분산시키는 컨텍스트
- [1:17](https://youtube.com/watch?v=aa-zYgWV00g&t=77) dist스트션. 비슷한 정보가 섞여서
- [1:19](https://youtube.com/watch?v=aa-zYgWV00g&t=79) 구분이 안 되는 컨텍스트 컴퓨로
- [1:21](https://youtube.com/watch?v=aa-zYgWV00g&t=81) 모순되는 정보가 들어가는 컨텍스트
- [1:23](https://youtube.com/watch?v=aa-zYgWV00g&t=83) 클래시.이네 이네 가지가 바로 AI가
- [1:25](https://youtube.com/watch?v=aa-zYgWV00g&t=85) 긴 작업에서 실수하는 근본
- [1:27](https://youtube.com/watch?v=aa-zYgWV00g&t=87) 원인입니다. 그러면 어떻게 해야
- [1:28](https://youtube.com/watch?v=aa-zYgWV00g&t=88) 할까요? 엔스로픽이 제한하는 핵심
- [1:30](https://youtube.com/watch?v=aa-zYgWV00g&t=90) 전략이 저스트 인타임 컨텍스트예요.
- [1:32](https://youtube.com/watch?v=aa-zYgWV00g&t=92) 처음부터 모든 정보를 다 넣지 말고
- [1:33](https://youtube.com/watch?v=aa-zYgWV00g&t=93) 가벼운 단서만 제공해서 AI가 필요할
- [1:36](https://youtube.com/watch?v=aa-zYgWV00g&t=96) 때 직접 찾아보게 하는 겁니다. 예를
- [1:37](https://youtube.com/watch?v=aa-zYgWV00g&t=97) 들어 클로드 코드는 이렇게 작동해요.
- [1:39](https://youtube.com/watch?v=aa-zYgWV00g&t=99) 코드베이스 전체를 다 읽지 않고 파일
- [1:41](https://youtube.com/watch?v=aa-zYgWV00g&t=101) 이름이나 경로만 기억해 뒀다가 필요한
- [1:43](https://youtube.com/watch?v=aa-zYgWV00g&t=103) 파일만 그때그때 열어 보거든요.
- [1:45](https://youtube.com/watch?v=aa-zYgWV00g&t=105) 그리고 클로드 잼 앤디 같은 핵심
- [1:47](https://youtube.com/watch?v=aa-zYgWV00g&t=107) 설정 파일만 미리 로드하고 나머지는
- [1:49](https://youtube.com/watch?v=aa-zYgWV00g&t=109) 검색 도구로 찾는 하이브리드 전략을
- [1:51](https://youtube.com/watch?v=aa-zYgWV00g&t=111) 씁니다.이 방식의 장점이 뭐냐면요.
- [1:52](https://youtube.com/watch?v=aa-zYgWV00g&t=112) AI의 주의력 예산을 아끼면서도
- [1:54](https://youtube.com/watch?v=aa-zYgWV00g&t=114) 필요한 정보는 정확하게 확보할 수
- [1:56](https://youtube.com/watch?v=aa-zYgWV00g&t=116) 있다는 거예요. 자, 여기서 더
- [1:58](https://youtube.com/watch?v=aa-zYgWV00g&t=118) 중요한게 있어요. 실제로 AI
- [1:59](https://youtube.com/watch?v=aa-zYgWV00g&t=119) 에이전트가 몇 시간짜리 큰 작업을 할
- [2:01](https://youtube.com/watch?v=aa-zYgWV00g&t=121) 때 문제인데요. 엔스로픽이 실험에서
- [2:03](https://youtube.com/watch?v=aa-zYgWV00g&t=123) 발견한 실패 패턴이 두 가지
- [2:05](https://youtube.com/watch?v=aa-zYgWV00g&t=125) 있습니다. 첫째, 한 번에 너무 많이
- [2:06](https://youtube.com/watch?v=aa-zYgWV00g&t=126) 하려다가 컨텍스트가 바닥나는 과역
- [2:08](https://youtube.com/watch?v=aa-zYgWV00g&t=128) 패턴. 둘째, 앞선 작업을 보고 다
- [2:10](https://youtube.com/watch?v=aa-zYgWV00g&t=130) 끝난 줄 알고 멈춰 버리는 조기 완료
- [2:12](https://youtube.com/watch?v=aa-zYgWV00g&t=132) 패턴.이 이 문제를 해결하기 위해
- [2:14](https://youtube.com/watch?v=aa-zYgWV00g&t=134) 엔스로픽이 도입한게 하네스
- [2:15](https://youtube.com/watch?v=aa-zYgWV00g&t=135) 패턴이에요. 핵심은 두 종류의
- [2:17](https://youtube.com/watch?v=aa-zYgWV00g&t=137) 에이전트를 나누는 겁니다. 첫 번째
- [2:18](https://youtube.com/watch?v=aa-zYgWV00g&t=138) 세션에서는 초기와 에이전트가 작업
- [2:20](https://youtube.com/watch?v=aa-zYgWV00g&t=140) 환경을 세팅하고 할 일 목록을
- [2:22](https://youtube.com/watch?v=aa-zYgWV00g&t=142) 제이손으로 만들어요. 그다음
- [2:24](https://youtube.com/watch?v=aa-zYgWV00g&t=144) 세션부터는 코딩 에이전트가 할 일을
- [2:26](https://youtube.com/watch?v=aa-zYgWV00g&t=146) 하나씩 처리하면서 진행 상황을
- [2:27](https://youtube.com/watch?v=aa-zYgWV00g&t=147) 기록합니다. 여기서 아주 재미있는
- [2:29](https://youtube.com/watch?v=aa-zYgWV00g&t=149) 발견이 하나 있는데요. 상태 기록을
- [2:30](https://youtube.com/watch?v=aa-zYgWV00g&t=150) 마크다운으로 했을 때보다 제이손으로
- [2:32](https://youtube.com/watch?v=aa-zYgWV00g&t=152) 했을 때 AI가 임의로 수정하는
- [2:34](https://youtube.com/watch?v=aa-zYgWV00g&t=154) 경우가 훨씬 적었다. AI가 제이손을
- [2:36](https://youtube.com/watch?v=aa-zYgWV00g&t=156) 코드로 인식해서 함부로 건드리지 않는
- [2:38](https://youtube.com/watch?v=aa-zYgWV00g&t=158) 거예요. 그리고 매세션 시작 때마다
- [2:40](https://youtube.com/watch?v=aa-zYgWV00g&t=160) 정해진 루틴을 따르게 합니다. 현재
- [2:41](https://youtube.com/watch?v=aa-zYgWV00g&t=161) 디렉토리 확인하고 깃 로그 읽고 할
- [2:43](https://youtube.com/watch?v=aa-zYgWV00g&t=163) 일 목록 확인하고 개발 서버 띄우고
- [2:46](https://youtube.com/watch?v=aa-zYgWV00g&t=166) 테스트 돌리고 그다음에 작업 시작이
- [2:48](https://youtube.com/watch?v=aa-zYgWV00g&t=168) 구조화된 시작 루틴이 세션마다 토큰을
- [2:50](https://youtube.com/watch?v=aa-zYgWV00g&t=170) 절약해 주거든요. 자 이제 종합해서
- [2:52](https://youtube.com/watch?v=aa-zYgWV00g&t=172) 긴 작업을 잘 관리하는 세 가지
- [2:53](https://youtube.com/watch?v=aa-zYgWV00g&t=173) 전략을 정리해 드리 첫 번째
- [2:55](https://youtube.com/watch?v=aa-zYgWV00g&t=175) 압축이에요. 대화가 너무 길어지면
- [2:57](https://youtube.com/watch?v=aa-zYgWV00g&t=177) 핵심만 요약해서 새로 시작하는
- [2:58](https://youtube.com/watch?v=aa-zYgWV00g&t=178) 건데요. 여기서 중요한 인사이트가
- [3:00](https://youtube.com/watch?v=aa-zYgWV00g&t=180) 하나 있어요. 엔스로픽은 압축보다는
- [3:02](https://youtube.com/watch?v=aa-zYgWV00g&t=182) 아예 처음부터 새로 시작하는 걸 더
- [3:04](https://youtube.com/watch?v=aa-zYgWV00g&t=184) 권장합니다. 대신 매번 작업 끝에 기
- [3:06](https://youtube.com/watch?v=aa-zYgWV00g&t=186) 커밋과 진행 문서를 남겨서 다음
- [3:08](https://youtube.com/watch?v=aa-zYgWV00g&t=188) 세션이 빠르게 맥락을 파악하게 하는
- [3:10](https://youtube.com/watch?v=aa-zYgWV00g&t=190) 거예요. 두 번째 구조화된 메모예요.
- [3:12](https://youtube.com/watch?v=aa-zYgWV00g&t=192) AI가 외브 파일에 노트를 남기게
- [3:13](https://youtube.com/watch?v=aa-zYgWV00g&t=193) 하는 건데요. 앤스로픽이 AI로
- [3:15](https://youtube.com/watch?v=aa-zYgWV00g&t=195) 포켓몬 게임을 플레이하게 했을 때이
- [3:17](https://youtube.com/watch?v=aa-zYgWV00g&t=197) AI가 스스로 노트를 작성하면서
- [3:19](https://youtube.com/watch?v=aa-zYgWV00g&t=199) 1천스텝이 넘는 기록을 정확하게
- [3:21](https://youtube.com/watch?v=aa-zYgWV00g&t=201) 추적했어요. 대화가 초기화된 뒤에도
- [3:23](https://youtube.com/watch?v=aa-zYgWV00g&t=203) 자기 노트를 읽고 전략을
- [3:25](https://youtube.com/watch?v=aa-zYgWV00g&t=205) 이어갔거든요. 세 번째 서브
- [3:26](https://youtube.com/watch?v=aa-zYgWV00g&t=206) 에이전트예요. 복잡한 작업을 혼자
- [3:28](https://youtube.com/watch?v=aa-zYgWV00g&t=208) 다하지 말고 전문화된 하위
- [3:29](https://youtube.com/watch?v=aa-zYgWV00g&t=209) 에이전트에게 나눠 주는 겁니다.
- [3:31](https://youtube.com/watch?v=aa-zYgWV00g&t=211) 팀장이 팀원한테 조사를 맡기고 요약만
- [3:33](https://youtube.com/watch?v=aa-zYgWV00g&t=213) 받듯이 서브 에이전트가 1에서
- [3:34](https://youtube.com/watch?v=aa-zYgWV00g&t=214) 2,000 토큰 요약만 돌려주면 메인
- [3:36](https://youtube.com/watch?v=aa-zYgWV00g&t=216) 에이전트는 깨끗한 컨텍스트에서 좋은
- [3:39](https://youtube.com/watch?v=aa-zYgWV00g&t=219) 판단을 내릴 수 있어요. 자, 오늘
- [3:40](https://youtube.com/watch?v=aa-zYgWV00g&t=220) 내용을 정리해 보면요. 첫째, AI의
- [3:42](https://youtube.com/watch?v=aa-zYgWV00g&t=222) 실력은 모델이 아니라 컨텍스트에서
- [3:44](https://youtube.com/watch?v=aa-zYgWV00g&t=224) 갈립니다. 프롬프트를 넘어서 어떤
- [3:46](https://youtube.com/watch?v=aa-zYgWV00g&t=226) 정보를 언제 얼마나 줄지를
- [3:47](https://youtube.com/watch?v=aa-zYgWV00g&t=227) 설계하세요. 둘째, 정보를 한꺼번에
- [3:49](https://youtube.com/watch?v=aa-zYgWV00g&t=229) 때려넣지 마세요. 저스트 인타임
- [3:51](https://youtube.com/watch?v=aa-zYgWV00g&t=231) 전략으로 필요한 순간에 필요한 것만
- [3:53](https://youtube.com/watch?v=aa-zYgWV00g&t=233) 주면 됩니다. 셋째, 긴 작업은
- [3:55](https://youtube.com/watch?v=aa-zYgWV00g&t=235) 하네스 패턴으로 관리하세요. 제이슨
- [3:56](https://youtube.com/watch?v=aa-zYgWV00g&t=236) 상태 추적, 세션 시작 루틴, 깃
- [3:58](https://youtube.com/watch?v=aa-zYgWV00g&t=238) 커미스로 맥락을 이어가면 됩니다.
- [4:00](https://youtube.com/watch?v=aa-zYgWV00g&t=240) 오늘 영상이 도움이 되셨다면 좋아요와
- [4:02](https://youtube.com/watch?v=aa-zYgWV00g&t=242) 구독 부탁드리고요. 여러분은 AI한테
- [4:04](https://youtube.com/watch?v=aa-zYgWV00g&t=244) 긴 작업을 시킬 때 어떤 방법으로
- [4:06](https://youtube.com/watch?v=aa-zYgWV00g&t=246) 맥락을 관리하고 계신가요? 댓글로
- [4:08](https://youtube.com/watch?v=aa-zYgWV00g&t=248) 공유해 주세요. 다음 영상에서도 AI
- [4:10](https://youtube.com/watch?v=aa-zYgWV00g&t=250) 에이전트 활용의 실전 팁을이어서
- [4:12](https://youtube.com/watch?v=aa-zYgWV00g&t=252) 다뤄볼 예정이니 기대해 주세요. e
