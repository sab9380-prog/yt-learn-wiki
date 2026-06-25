---
title: "옵시디언 + LLM 이 조합 미쳤습니다 | 옵시디언 + LLM Wiki로 만드는 나만의 AI 업무 시스템"
source_url: https://youtube.com/watch?v=UbxFpDuWt8Q
video_id: UbxFpDuWt8Q
source_type: youtube
lang: ko
analyzed: 2026-05-22
category: 일반학습
status: active
---
# 옵시디언 + LLM 이 조합 미쳤습니다 | 옵시디언 + LLM Wiki로 만드는 나만의 AI 업무 시스템

[[_category-일반학습]]

## 🧠 이해 (Understand)
- **Summary:** AI와 함께 업무 자료를 효율적으로 관리하는 LM 위키 시스템에 대한 설명입니다. 기존 노트앱들은 입력, 검색, 유지 비용이 높아 지식 무덤이 되지만, 옵시디언과 AI를 조합한 LM 위키는 이 문제를 해결합니다. 소스 폴더에 원본 자료를 저장하고, AI가 이를 읽어 위키 폴더에 주제별 문서로 정리하며, 새 자료 추가 시 기존 위키와 자동 연결 업데이트합니다. 사람은 방향 설정과 판단에 집중하고, AI는 반복 정리와 연결을 담당하는 역할 분담이 핵심입니다.
- **Core Message:** AI가 관리하는 개인 업무 위키를 만들어 자료 정리와 업무 결과물 생성을 자동화할 수 있다.
> 앞으로 AI를 잘 쓰는 사람은 단순히 질문을 잘하는 사람이 아니라 AI가 참고할 수 있는 자기만의 지식 시스템을 가진 사람이 될 가능성이 큽니다
> 사람은 판단과 편집에 집중하고 AI는 반복 정리와 연결을 담당하죠
> 대부분의 노트앱은 시간이 지나면 두 번째 뇌가 아니라 지식 무덤이 되었습니다
❗ 테슬라 AI 총괄자였던 안드레 카파시가 LM 위키 방식을 최근 소개했다
❗ 옵시디언은 폴더와 텍스트 파일 기반이라 AI가 직접 파일을 읽고 수정할 수 있다
❗ 기존 노트앱의 실패 원인은 입력비용, 검색비용, 유지비용 3가지다

## 📚 핵심 용어
- **LM 위키:** AI가 자료를 읽어 주제별 위키 문서로 정리하고 업데이트하는 개인 지식 관리 시스템 / 개인 비서가 내 모든 자료를 읽고 주제별 파일철로 정리해서, 필요할 때 언제든 관련 자료를 찾아주는 것과 같다. / 기존 노트앱은 사람이 직접 정리해야 하지만, LM 위키는 AI가 자료를 읽고 연결하며 자동 업데이트한다.
- **옵시디언:** 마크다운 기반의 개인 지식 관리 앱으로 폴더와 텍스트 파일로 구성됨 / 노션이 예쁜 전시장이라면, 옵시디언은 AI가 자유롭게 드나들며 정리할 수 있는 작업실 같다. / 노션은 앱 의존적이지만, 옵시디언은 파일 기반이라 AI가 직접 읽고 수정하기 쉽다.
- **마크다운:** 사람과 AI가 모두 읽고 이해하기 쉬운 구조화된 텍스트 형식 / 복잡한 워드 문서 대신 간단한 기호로 제목, 목록을 표시하는 것. 메모장에도 쓸 수 있어 범용성이 높다. / 워드나 PDF는 형식이 복잡하지만, 마크다운은 순수 텍스트라 AI가 내용을 파악하기 쉽다.

## 🚀 실행 (Execute)
- [ ] 옵시디언 설치하고 새 볼트 생성 후 소스/위키/에이전트MD/아웃풋 4개 폴더 구조 만들기
  - 담당: 나
  - 이유: LM 위키의 기본 틀을 만들어야 AI가 자료를 체계적으로 정리할 수 있음
- [ ] 현재 업무 자료 3-5개를 소스 폴더에 넣고 AI에게 위키 문서 생성 요청하기
  - 담당: 나
  - 이유: 작은 규모로 시작해서 시스템이 실제로 작동하는지 확인하고 감각을 익혀야 함
- 자료: 영상 설명란의 옵시디언 플러그인 설치 방법
- 자료: 기본 폴더 구조와 에이전트 MD 예시 프롬프트
- 자료: 안드레 카파시의 LM 위키 원본 자료 (확인 필요)
- Timeline: 1주차에 환경 구축, 2주차에 실제 자료로 테스트, 3주차부터 본격 업무 적용

## 📝 자막 전문
- [0:01](https://youtube.com/watch?v=UbxFpDuWt8Q&t=1) 업무에 AI를 사용하려고 자신의
- [0:03](https://youtube.com/watch?v=UbxFpDuWt8Q&t=3) 업무, 이번 분기 목표, 지난주에 뭘
- [0:07](https://youtube.com/watch?v=UbxFpDuWt8Q&t=7) 결정했는지 등을 AI한테 매번
- [0:09](https://youtube.com/watch?v=UbxFpDuWt8Q&t=9) 설명하느라 시간을 잡아먹으신 적
- [0:11](https://youtube.com/watch?v=UbxFpDuWt8Q&t=11) 있으신가요?
- [0:13](https://youtube.com/watch?v=UbxFpDuWt8Q&t=13) 시간이 지나고 비슷한 업무를 AI한테
- [0:16](https://youtube.com/watch?v=UbxFpDuWt8Q&t=16) 다시 물어볼 때 온갖 자료를 다시
- [0:18](https://youtube.com/watch?v=UbxFpDuWt8Q&t=18) 던져 줘야 하고 그렇게 나온 답변이
- [0:21](https://youtube.com/watch?v=UbxFpDuWt8Q&t=21) 이전 맥락과 동떨어진 적 있지
- [0:23](https://youtube.com/watch?v=UbxFpDuWt8Q&t=23) 않으신가요?
- [0:25](https://youtube.com/watch?v=UbxFpDuWt8Q&t=25) 또 외부 미팅이나 출장 중에 갑자기
- [0:27](https://youtube.com/watch?v=UbxFpDuWt8Q&t=27) 업무 관련 내용을 업데이트해야 하거나
- [0:30](https://youtube.com/watch?v=UbxFpDuWt8Q&t=30) 팀원과 공유해야 할 때 곤란했던
- [0:32](https://youtube.com/watch?v=UbxFpDuWt8Q&t=32) 적은요.
- [0:34](https://youtube.com/watch?v=UbxFpDuWt8Q&t=34) 오늘은이 문제를 해결하는 시스템 LM
- [0:37](https://youtube.com/watch?v=UbxFpDuWt8Q&t=37) 위키에 대해 알려 드리겠습니다.이
- [0:39](https://youtube.com/watch?v=UbxFpDuWt8Q&t=39) 영상을 끝까지 보시면 내 업무 자료를
- [0:42](https://youtube.com/watch?v=UbxFpDuWt8Q&t=42) 어떻게 AI가 계속 이해하고 활용할
- [0:44](https://youtube.com/watch?v=UbxFpDuWt8Q&t=44) 수 있는 구조로 만들 수 있는지
- [0:47](https://youtube.com/watch?v=UbxFpDuWt8Q&t=47) 머릿속에 그려지실 겁니다.
- [0:50](https://youtube.com/watch?v=UbxFpDuWt8Q&t=50) 사실 사람들은 예전부터 두 번째 내를
- [0:53](https://youtube.com/watch?v=UbxFpDuWt8Q&t=53) 만들고 싶어 했습니다. 업무 자료,
- [0:56](https://youtube.com/watch?v=UbxFpDuWt8Q&t=56) 프로젝트 기록, 의사 결정 과정.
- [0:59](https://youtube.com/watch?v=UbxFpDuWt8Q&t=59) 나중에 써먹을 만한 인사이트들을 한
- [1:02](https://youtube.com/watch?v=UbxFpDuWt8Q&t=62) 곳에 모아두고 싶어 했었죠. 하지만
- [1:05](https://youtube.com/watch?v=UbxFpDuWt8Q&t=65) 대부분의 노트앱은 시간이 지나면 두
- [1:08](https://youtube.com/watch?v=UbxFpDuWt8Q&t=68) 번째 뇌가 아니라 지식 무덤이
- [1:09](https://youtube.com/watch?v=UbxFpDuWt8Q&t=69) 되었습니다. 왜냐하면 세 가지
- [1:12](https://youtube.com/watch?v=UbxFpDuWt8Q&t=72) 때문인데요. 첫 번째로는 입력
- [1:14](https://youtube.com/watch?v=UbxFpDuWt8Q&t=74) 비용입니다. 자료를 일일이 정리해서
- [1:17](https://youtube.com/watch?v=UbxFpDuWt8Q&t=77) 넣어야 했었죠.
- [1:18](https://youtube.com/watch?v=UbxFpDuWt8Q&t=78) 둘째는 검색 비용인데요. 이전에
- [1:21](https://youtube.com/watch?v=UbxFpDuWt8Q&t=81) 저장해 둔 내용인 것 같은데 막상
- [1:23](https://youtube.com/watch?v=UbxFpDuWt8Q&t=83) 필요할 때는 찾기 어려웠었습니다.
- [1:26](https://youtube.com/watch?v=UbxFpDuWt8Q&t=86) 셋째는 유지 비용입니다. 새로운
- [1:28](https://youtube.com/watch?v=UbxFpDuWt8Q&t=88) 자료가 생겼을 때 기존 노트와
- [1:30](https://youtube.com/watch?v=UbxFpDuWt8Q&t=90) 연결하고 오래된 내용을 업데이트하고
- [1:33](https://youtube.com/watch?v=UbxFpDuWt8Q&t=93) 중복 내용을 정리한 데는 많은 노력이
- [1:36](https://youtube.com/watch?v=UbxFpDuWt8Q&t=96) 필요했었죠.이 이 세 가지가 쌓이다
- [1:39](https://youtube.com/watch?v=UbxFpDuWt8Q&t=99) 보면 결국 노트앱은 나중에 읽겠다고
- [1:41](https://youtube.com/watch?v=UbxFpDuWt8Q&t=101) 밀어둔 자료 창고가 됩니다. 문제는
- [1:45](https://youtube.com/watch?v=UbxFpDuWt8Q&t=105) 그 나중에 거의 오지 않는다는
- [1:47](https://youtube.com/watch?v=UbxFpDuWt8Q&t=107) 겁니다. 그런데 AI가 등장하면서이
- [1:50](https://youtube.com/watch?v=UbxFpDuWt8Q&t=110) 구조가 바뀌고 있습니다. 이제 사람이
- [1:53](https://youtube.com/watch?v=UbxFpDuWt8Q&t=113) 모든 자료를 직접 정리하지 않아도
- [1:55](https://youtube.com/watch?v=UbxFpDuWt8Q&t=115) 됩니다. AI가 자료를 읽고 요약하고
- [1:59](https://youtube.com/watch?v=UbxFpDuWt8Q&t=119) 분류하고 기존 노트와 연결하고 필요한
- [2:02](https://youtube.com/watch?v=UbxFpDuWt8Q&t=122) 결과물로 바꿔 줄 수 있기
- [2:03](https://youtube.com/watch?v=UbxFpDuWt8Q&t=123) 때문입니다. 하지만 이때 중요한
- [2:06](https://youtube.com/watch?v=UbxFpDuWt8Q&t=126) 조건이 있습니다. AI가 잘 읽을 수
- [2:09](https://youtube.com/watch?v=UbxFpDuWt8Q&t=129) 있는 형식으로 지식이 저장되어 있어야
- [2:11](https://youtube.com/watch?v=UbxFpDuWt8Q&t=131) 합니다. 그래서 중요한게 바로
- [2:14](https://youtube.com/watch?v=UbxFpDuWt8Q&t=134) 마크다운입니다.
- [2:16](https://youtube.com/watch?v=UbxFpDuWt8Q&t=136) 마크다운은 사람과 AI가 읽고
- [2:19](https://youtube.com/watch?v=UbxFpDuWt8Q&t=139) 이해하기 쉽게 구조한 텍스트
- [2:21](https://youtube.com/watch?v=UbxFpDuWt8Q&t=141) 형식입니다. 여기서 오시디언의 강점이
- [2:24](https://youtube.com/watch?v=UbxFpDuWt8Q&t=144) 나옵니다. 노션이나 에보노트 같은
- [2:27](https://youtube.com/watch?v=UbxFpDuWt8Q&t=147) 일반적인 메모 앱은 화면은 예쁘지만
- [2:30](https://youtube.com/watch?v=UbxFpDuWt8Q&t=150) 내부 구조가 앱에 많이 의존합니다.
- [2:32](https://youtube.com/watch?v=UbxFpDuWt8Q&t=152) 반면 옵시디어는 폴더와 텍스트 파일
- [2:35](https://youtube.com/watch?v=UbxFpDuWt8Q&t=155) 기반의 앱입니다. 그래서 AI
- [2:38](https://youtube.com/watch?v=UbxFpDuWt8Q&t=158) 에이전트나 lm이 폴더를 읽고 파일을
- [2:41](https://youtube.com/watch?v=UbxFpDuWt8Q&t=161) 수정하고 새 문서를 만들고 기존
- [2:44](https://youtube.com/watch?v=UbxFpDuWt8Q&t=164) 문서와 연결하기가 훨씬 쉽습니다.
- [2:48](https://youtube.com/watch?v=UbxFpDuWt8Q&t=168) 기존 노트앱은 사람이 보기 좋은
- [2:50](https://youtube.com/watch?v=UbxFpDuWt8Q&t=170) 정리함에 가까웠다면 옵시디언의 사람도
- [2:55](https://youtube.com/watch?v=UbxFpDuWt8Q&t=175) AI도 읽고 이해할 수 있는 지식
- [2:57](https://youtube.com/watch?v=UbxFpDuWt8Q&t=177) 작업장에 가깝습니다.
- [3:00](https://youtube.com/watch?v=UbxFpDuWt8Q&t=180) 그래서 앞으로 AI와 함께 개인 지식
- [3:03](https://youtube.com/watch?v=UbxFpDuWt8Q&t=183) 관리, 업무 정리, 자료 분석을
- [3:06](https://youtube.com/watch?v=UbxFpDuWt8Q&t=186) 하려면 옵시디언과 같은 마크다운 기반
- [3:09](https://youtube.com/watch?v=UbxFpDuWt8Q&t=189) 시스템이 훨씬 유리합니다.
- [3:13](https://youtube.com/watch?v=UbxFpDuWt8Q&t=193) 오픈 AI 멤버이자 테슬라의
- [3:16](https://youtube.com/watch?v=UbxFpDuWt8Q&t=196) 인공지능 총괄자였던 안드레 카파시가
- [3:19](https://youtube.com/watch?v=UbxFpDuWt8Q&t=199) 최근 LM 위키라는 방식을
- [3:21](https://youtube.com/watch?v=UbxFpDuWt8Q&t=201) 소개했습니다.
- [3:23](https://youtube.com/watch?v=UbxFpDuWt8Q&t=203) LM 위키는 AI가 관리하는 나만의
- [3:26](https://youtube.com/watch?v=UbxFpDuWt8Q&t=206) 업무 위키입니다.
- [3:28](https://youtube.com/watch?v=UbxFpDuWt8Q&t=208) 쉽게 말하면 자료를 한 폴더에
- [3:31](https://youtube.com/watch?v=UbxFpDuWt8Q&t=211) 모아두고 AI에게이 자료들을 읽어서
- [3:34](https://youtube.com/watch?v=UbxFpDuWt8Q&t=214) 주제별 위키 문서로 정리해 달라고
- [3:36](https://youtube.com/watch?v=UbxFpDuWt8Q&t=216) 하는 겁니다. 그다음 새 자료를 넣을
- [3:39](https://youtube.com/watch?v=UbxFpDuWt8Q&t=219) 때마다 AI에게 기존 위키와 연결해서
- [3:42](https://youtube.com/watch?v=UbxFpDuWt8Q&t=222) 요약하고 관련 문서를 업데이트해
- [3:45](https://youtube.com/watch?v=UbxFpDuWt8Q&t=225) 달라고 하면 됩니다. 이게 LM
- [3:47](https://youtube.com/watch?v=UbxFpDuWt8Q&t=227) 위키의 기본 구조입니다.
- [3:51](https://youtube.com/watch?v=UbxFpDuWt8Q&t=231) LLM 위키를 구현하기 위해서 필요한
- [3:54](https://youtube.com/watch?v=UbxFpDuWt8Q&t=234) 도구는 세 가지인데요. 옵시디언,
- [3:56](https://youtube.com/watch?v=UbxFpDuWt8Q&t=236) 옵시디언 플러그인, 그리고 채치T와
- [3:59](https://youtube.com/watch?v=UbxFpDuWt8Q&t=239) 같은 LM입니다.
- [4:02](https://youtube.com/watch?v=UbxFpDuWt8Q&t=242) 옵시디엄 플러그인과 설치 방법은 영상
- [4:04](https://youtube.com/watch?v=UbxFpDuWt8Q&t=244) 설명란에 따로 정리해 두겠습니다.
- [4:07](https://youtube.com/watch?v=UbxFpDuWt8Q&t=247) 그럼 실제로 시작한 순서를 정리해
- [4:10](https://youtube.com/watch?v=UbxFpDuWt8Q&t=250) 보겠습니다. 첫 번째 옵시디언에서 세
- [4:13](https://youtube.com/watch?v=UbxFpDuWt8Q&t=253) 볼트를 만듭니다. 두 번째 폴더를네
- [4:17](https://youtube.com/watch?v=UbxFpDuWt8Q&t=257) 개 만듭니다.
- [4:19](https://youtube.com/watch?v=UbxFpDuWt8Q&t=259) 소스 위키 에이전트 MD
- [4:22](https://youtube.com/watch?v=UbxFpDuWt8Q&t=262) 아웃풋.
- [4:24](https://youtube.com/watch?v=UbxFpDuWt8Q&t=264) 소스는 원본 자료를 모아 놓는
- [4:26](https://youtube.com/watch?v=UbxFpDuWt8Q&t=266) 곳입니다. 회의록 리서치 자료,
- [4:29](https://youtube.com/watch?v=UbxFpDuWt8Q&t=269) 프로젝트 문서, 기획 초안, 기사,
- [4:32](https://youtube.com/watch?v=UbxFpDuWt8Q&t=272) PDF 같은 것들이 있죠.
- [4:35](https://youtube.com/watch?v=UbxFpDuWt8Q&t=275) 여기서 중요한 원칙은 하나인데요.
- [4:38](https://youtube.com/watch?v=UbxFpDuWt8Q&t=278) 소스 폴더의 원본 자료는 절대
- [4:40](https://youtube.com/watch?v=UbxFpDuWt8Q&t=280) 수정하지 않습니다.
- [4:42](https://youtube.com/watch?v=UbxFpDuWt8Q&t=282) 왜냐하면 원본이 바뀌면 나중에 AI가
- [4:45](https://youtube.com/watch?v=UbxFpDuWt8Q&t=285) 어떤 자료를 근거로 정리했는지
- [4:47](https://youtube.com/watch?v=UbxFpDuWt8Q&t=287) 추적하기 어려워지기 때문입니다.
- [4:50](https://youtube.com/watch?v=UbxFpDuWt8Q&t=290) 반대로 위키 폴더는 LM이 정리한
- [4:53](https://youtube.com/watch?v=UbxFpDuWt8Q&t=293) 결과물이 들어가는 곳입니다. 즉
- [4:56](https://youtube.com/watch?v=UbxFpDuWt8Q&t=296) AI가 정리한 지식 백과사전 폴더죠.
- [5:00](https://youtube.com/watch?v=UbxFpDuWt8Q&t=300) 그리고 에이전트 MD 파일에는 AI가
- [5:03](https://youtube.com/watch?v=UbxFpDuWt8Q&t=303) 지켜야 할 규칙을 졌습니다. 정리
- [5:06](https://youtube.com/watch?v=UbxFpDuWt8Q&t=306) 방식, 출처 기록 방식, 업데이트
- [5:09](https://youtube.com/watch?v=UbxFpDuWt8Q&t=309) 방식 등을 적어두면 AI가 훨씬
- [5:12](https://youtube.com/watch?v=UbxFpDuWt8Q&t=312) 일간되게 결과물을 내뱉습니다.
- [5:16](https://youtube.com/watch?v=UbxFpDuWt8Q&t=316) 세 번째 원본 자료를 소스에
- [5:19](https://youtube.com/watch?v=UbxFpDuWt8Q&t=319) 넣었습니다. 처음부터 많은 자료를
- [5:22](https://youtube.com/watch?v=UbxFpDuWt8Q&t=322) 넣지 않아도 됩니다. 회의록 세 개,
- [5:24](https://youtube.com/watch?v=UbxFpDuWt8Q&t=324) 보고서 세 개, 기획 초환 한 개
- [5:27](https://youtube.com/watch?v=UbxFpDuWt8Q&t=327) 정도면 충분합니다.네
- [5:30](https://youtube.com/watch?v=UbxFpDuWt8Q&t=330) 번째 AI에게 이렇게 요청합니다.
- [5:34](https://youtube.com/watch?v=UbxFpDuWt8Q&t=334) 소스 폴더의 자료를 읽고 위키폴더의
- [5:37](https://youtube.com/watch?v=UbxFpDuWt8Q&t=337) 주제별 문서를 만들어 줘. 중복되는
- [5:40](https://youtube.com/watch?v=UbxFpDuWt8Q&t=340) 내용은 합치고 중요한 결정 사항과
- [5:43](https://youtube.com/watch?v=UbxFpDuWt8Q&t=343) 업무 기준은 따로 정리해 줘.
- [5:45](https://youtube.com/watch?v=UbxFpDuWt8Q&t=345) 다섯 번째 새 자료가 생길 때마다
- [5:48](https://youtube.com/watch?v=UbxFpDuWt8Q&t=348) 이렇게 요청합니다. 새로 추가한 소스
- [5:51](https://youtube.com/watch?v=UbxFpDuWt8Q&t=351) 자료를 읽고 기존 위키 문서 중
- [5:54](https://youtube.com/watch?v=UbxFpDuWt8Q&t=354) 업데이트가 필요한 문서를 수정해 줘.
- [5:57](https://youtube.com/watch?v=UbxFpDuWt8Q&t=357) 그리고 새로운 개념이 있으면 새
- [5:59](https://youtube.com/watch?v=UbxFpDuWt8Q&t=359) 문서를 만들고 관련 문서와 링크로
- [6:02](https://youtube.com/watch?v=UbxFpDuWt8Q&t=362) 연결해 줘.
- [6:04](https://youtube.com/watch?v=UbxFpDuWt8Q&t=364) 여섯 번째 필요할 때 아웃풋 폴더의
- [6:08](https://youtube.com/watch?v=UbxFpDuWt8Q&t=368) 결과물을 요청합니다.
- [6:10](https://youtube.com/watch?v=UbxFpDuWt8Q&t=370) 예를 들자면 위키폴더 내용을 바탕으로
- [6:13](https://youtube.com/watch?v=UbxFpDuWt8Q&t=373) 회의 공유용 요약분을 만들어 줘.
- [6:15](https://youtube.com/watch?v=UbxFpDuWt8Q&t=375) 혹은 기획 방향성 문서를 참고해서
- [6:18](https://youtube.com/watch?v=UbxFpDuWt8Q&t=378) 임원 보고 한 페이지 보고서를
- [6:21](https://youtube.com/watch?v=UbxFpDuWt8Q&t=381) 만들어줘. 이렇게 하면 메모가 단순히
- [6:24](https://youtube.com/watch?v=UbxFpDuWt8Q&t=384) 저장되는 것이 아니라 실제 업무
- [6:26](https://youtube.com/watch?v=UbxFpDuWt8Q&t=386) 결과물로 이어집니다.
- [6:29](https://youtube.com/watch?v=UbxFpDuWt8Q&t=389) 그럼 실제 업무에서는 어떻게 쓸 수
- [6:31](https://youtube.com/watch?v=UbxFpDuWt8Q&t=391) 있을까요? 예를 들어 신규 프로젝트
- [6:34](https://youtube.com/watch?v=UbxFpDuWt8Q&t=394) 기획 업무를 한다고 해 보겠습니다.
- [6:37](https://youtube.com/watch?v=UbxFpDuWt8Q&t=397) 소스 폴더에 회의록 리서치 자료,
- [6:40](https://youtube.com/watch?v=UbxFpDuWt8Q&t=400) 시장 조사 자료, 프로젝트 문서,
- [6:42](https://youtube.com/watch?v=UbxFpDuWt8Q&t=402) 기획 초안, 기사 PDF를
- [6:44](https://youtube.com/watch?v=UbxFpDuWt8Q&t=404) 넣었습니다. 그리고 AI에게 이렇게
- [6:47](https://youtube.com/watch?v=UbxFpDuWt8Q&t=407) 요청합니다. 소스 폴더의 자료를 읽고
- [6:51](https://youtube.com/watch?v=UbxFpDuWt8Q&t=411) 위키폴더의 프로젝트 개, 문제 정의,
- [6:53](https://youtube.com/watch?v=UbxFpDuWt8Q&t=413) 경쟁사 비교, 핵심 의사 결정,
- [6:56](https://youtube.com/watch?v=UbxFpDuWt8Q&t=416) 리스크 요인을 정리해 줘.
- [6:58](https://youtube.com/watch?v=UbxFpDuWt8Q&t=418) 이렇게 요청을 하면 AI는 위키폴더의
- [7:02](https://youtube.com/watch?v=UbxFpDuWt8Q&t=422) 프로젝트 개요, 문지정의, 경쟁사
- [7:05](https://youtube.com/watch?v=UbxFpDuWt8Q&t=425) 비교, 리스크 요인, 핵심 의사
- [7:07](https://youtube.com/watch?v=UbxFpDuWt8Q&t=427) 결정, MD 파일을 만들 수
- [7:09](https://youtube.com/watch?v=UbxFpDuWt8Q&t=429) 있습니다. 이제 다음부터는 AI에게
- [7:12](https://youtube.com/watch?v=UbxFpDuWt8Q&t=432) 이렇게 요청할 수도 있습니다.
- [7:14](https://youtube.com/watch?v=UbxFpDuWt8Q&t=434) 위키폴드의 내용을 참고해서 보고서 한
- [7:17](https://youtube.com/watch?v=UbxFpDuWt8Q&t=437) 페이지 기회관 초안을 만들어 줘.
- [7:19](https://youtube.com/watch?v=UbxFpDuWt8Q&t=439) 혹은 경쟁사 비교 분수를 참고해서
- [7:22](https://youtube.com/watch?v=UbxFpDuWt8Q&t=442) 우리 서비스의 차별화 포인트를 다섯
- [7:24](https://youtube.com/watch?v=UbxFpDuWt8Q&t=444) 개로 정리해 줘라고 요청할 수 있죠.
- [7:27](https://youtube.com/watch?v=UbxFpDuWt8Q&t=447) 왜냐하면 AI는 내가 쌓아둔 지식
- [7:29](https://youtube.com/watch?v=UbxFpDuWt8Q&t=449) 구조를 계속 참고할 수 있기
- [7:31](https://youtube.com/watch?v=UbxFpDuWt8Q&t=451) 때문입니다.
- [7:33](https://youtube.com/watch?v=UbxFpDuWt8Q&t=453) 이때 사람은 방향을 정하고 AI가
- [7:36](https://youtube.com/watch?v=UbxFpDuWt8Q&t=456) 정리한 결과를 검토하고 중요한 판단을
- [7:38](https://youtube.com/watch?v=UbxFpDuWt8Q&t=458) 내립니다. 즉 사람은 판단과 편집에
- [7:42](https://youtube.com/watch?v=UbxFpDuWt8Q&t=462) 집중하고 AI는 반복 정리와 연결을
- [7:45](https://youtube.com/watch?v=UbxFpDuWt8Q&t=465) 담당하죠.
- [7:46](https://youtube.com/watch?v=UbxFpDuWt8Q&t=466) 정리하자면 카파시의 LM 위키는
- [7:49](https://youtube.com/watch?v=UbxFpDuWt8Q&t=469) AI가 관리하는 지식 위키입니다. 즉
- [7:52](https://youtube.com/watch?v=UbxFpDuWt8Q&t=472) 자료를 한 곳에 모으고 AI에게
- [7:55](https://youtube.com/watch?v=UbxFpDuWt8Q&t=475) 주제별로 정리하게 한 다음 새 자료가
- [7:57](https://youtube.com/watch?v=UbxFpDuWt8Q&t=477) 들어올 때마다 기존 위키와 연결해
- [8:00](https://youtube.com/watch?v=UbxFpDuWt8Q&t=480) 업데이트하는 시스템입니다.이
- [8:03](https://youtube.com/watch?v=UbxFpDuWt8Q&t=483) 시스템을 만들면 AI에게 매번 내
- [8:05](https://youtube.com/watch?v=UbxFpDuWt8Q&t=485) 업무 여행락을 설명하지 않아도
- [8:07](https://youtube.com/watch?v=UbxFpDuWt8Q&t=487) 됩니다. 옵시디언에 저장한 메모와
- [8:10](https://youtube.com/watch?v=UbxFpDuWt8Q&t=490) 자료가 그냥 기록으로 끝나는 것이
- [8:12](https://youtube.com/watch?v=UbxFpDuWt8Q&t=492) 아니라 AI가 실제 업무 결과물을
- [8:15](https://youtube.com/watch?v=UbxFpDuWt8Q&t=495) 만드는 재료가 됩니다.
- [8:18](https://youtube.com/watch?v=UbxFpDuWt8Q&t=498) 앞으로 AI를 잘 쓰는 사람은 단순히
- [8:21](https://youtube.com/watch?v=UbxFpDuWt8Q&t=501) 질문을 잘하는 사람이 아니라 AI가
- [8:23](https://youtube.com/watch?v=UbxFpDuWt8Q&t=503) 참고할 수 있는 자기만의 지식
- [8:26](https://youtube.com/watch?v=UbxFpDuWt8Q&t=506) 시스템을 가진 사람이 될 가능성이
- [8:27](https://youtube.com/watch?v=UbxFpDuWt8Q&t=507) 큽니다. 그래서 옵시디언을 그냥 메모
- [8:31](https://youtube.com/watch?v=UbxFpDuWt8Q&t=511) 앱으로만 쓰지 말고 LM 위키의
- [8:33](https://youtube.com/watch?v=UbxFpDuWt8Q&t=513) 기반으로 써 보시길 추천드립니다.
- [8:36](https://youtube.com/watch?v=UbxFpDuWt8Q&t=516) 영상 설명란에 기본 폴더 구조와
- [8:39](https://youtube.com/watch?v=UbxFpDuWt8Q&t=519) 에이전트 MD 예시프트를 남겨
- [8:42](https://youtube.com/watch?v=UbxFpDuWt8Q&t=522) 두겠습니다.
