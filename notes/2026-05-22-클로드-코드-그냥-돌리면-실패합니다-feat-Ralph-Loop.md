---
title: "클로드 코드, 그냥 돌리면 실패합니다 (feat. Ralph Loop)"
source_url: https://youtube.com/watch?v=mgPTpP-62rw
video_id: mgPTpP-62rw
source_type: youtube
lang: ko
analyzed: 2026-05-22
category: 일반학습
status: active
---
# 클로드 코드, 그냥 돌리면 실패합니다 (feat. Ralph Loop)

## 🧠 이해 (Understand)
- **Summary:** Ralph Loop은 Claude Code의 플러그인으로, AI가 코드를 작성하고 테스트하며 오류를 수정하는 과정을 자동으로 반복한다. 하지만 대부분 실패하는 이유는 프롬프트에 모든 정보를 다 넣거나 세부사항이 빠진 계획서만 넣기 때문이다. 성공하려면 4개의 파일 구조(PROMPT.md, specs 폴더, 실행계획, AGENTS.md)를 미리 만들어두고, 목표와 완료 조건을 명확히 정의한 프롬프트를 작성해야 한다. 이 방법으로 실제 앱을 만들어본 결과 80% 완성도의 결과물을 얻을 수 있었다.
- **Core Message:** Ralph Loop을 성공시키는 핵심은 AI가 필요할 때만 참조할 수 있도록 파일을 분리하고, 명확한 완료 조건이 담긴 프롬프트를 작성하는 것이다.
> AI한테 일 시키고 편하게 잠들고 싶다는 생각, 한 번쯤 해보셨죠
> 우리가 할 일은 코딩이 아닙니다. AI가 잘 일할 수 있는 환경을 만드는 거예요
> 작업 계획을 잘 잡아뒀더니 같은 플러그인인데 결과가 완전히 달랐어요
❗ Ralph Loop으로 실제 앱을 만든 결과 약 80% 완성도를 달성했다
❗ 프롬프트 하나의 구성에 따라 같은 플러그인도 완전히 다른 결과가 나온다
❗ AI가 빈 AGENTS.md 파일에 빌드 명령어와 테스트 방법까지 알아서 채워넣었다

## 📚 핵심 용어
- **Ralph Loop:** AI가 코드 작성, 테스트, 오류 수정을 자동으로 반복하는 Claude Code 플러그인 / 야간 경비원과 같다. 밤새 건물을 돌며 문제를 찾고 고치고, 아침에 보고서를 남긴다. / 일반 코딩 도구는 명령 한 번에 결과 하나지만, Ralph Loop은 목표 달성까지 스스로 반복한다.
- **파일 구조 분리:** 프롬프트, 요구사항, 실행계획, 운영정보를 별도 파일로 나누는 방법 / 요리책처럼 레시피별로 페이지를 나눈다. 파스타 만들 때는 파스타 페이지만 펴면 된다. / 통째 프롬프트는 매번 모든 내용을 읽어야 하지만, 분리하면 필요한 부분만 참조한다.
- **완료 조건:** AI가 스스로 작업 완료 여부를 판단할 수 있는 객관적 기준 / 시험 답안지의 정답표와 같다. 내가 쓴 답이 맞는지 스스로 채점할 수 있다. / 목표는 방향(무엇을)이지만, 완료 조건은 측정(언제 끝)이다.

## 🚀 실행 (Execute)
- [ ] Ralph Loop 플러그인을 Claude Code에 설치하고 4개 파일 구조(PROMPT.md, specs폴더, 실행계획, AGENTS.md) 템플릿 생성
  - 담당: 나
  - 이유: 실제 자동화 개발을 시작하기 위한 기본 환경 구축
- [ ] 소규모 사이드 프로젝트 하나를 선정하여 Ralph Loop으로 프로토타입 개발 실험
  - 담당: 나
  - 이유: 실전 경험을 통해 프롬프트 작성과 파일 구조 최적화 노하우 습득
- 자료: Claude Code 플러그인 스토어에서 Ralph Loop 확인 필요
- 자료: 영상 제작자가 제공하는 PDF 가이드 (프롬프트 템플릿 포함)
- 자료: 프롬프트 엔지니어링 관련 자료
- Timeline: 1일차: 환경 구축 → 2~7일차: 실험 프로젝트 진행 → 이후: 실제 프로젝트 적용 검토

## 🔗 연결
- 카테고리: [[_category-일반학습]]

## 📝 자막 전문
- [0:00](https://youtube.com/watch?v=mgPTpP-62rw&t=0) AI한테 일 시키고
- [0:01](https://youtube.com/watch?v=mgPTpP-62rw&t=1) 편하게 잠들고 싶다는 생각, 한 번쯤 해보셨죠.
- [0:05](https://youtube.com/watch?v=mgPTpP-62rw&t=5) 아침에 눈 떠서 확인했더니
- [0:07](https://youtube.com/watch?v=mgPTpP-62rw&t=7) 코드가 완성되어 있는 거예요.
- [0:09](https://youtube.com/watch?v=mgPTpP-62rw&t=9) 이거 진짜 됩니다.
- [0:11](https://youtube.com/watch?v=mgPTpP-62rw&t=11) Ralph Loop이라는 플러그인이 있거든요.
- [0:14](https://youtube.com/watch?v=mgPTpP-62rw&t=14) Claude Code에서 켜기만 하면 되고, 방법도 쉬워요.
- [0:17](https://youtube.com/watch?v=mgPTpP-62rw&t=17) 근데 그냥 돌리면 십중팔구 실패합니다.
- [0:20](https://youtube.com/watch?v=mgPTpP-62rw&t=20) 오늘 왜 실패하는지, 그리고 어떻게 하면 성공하는지
- [0:23](https://youtube.com/watch?v=mgPTpP-62rw&t=23) 직접 돌려본 결과까지 알려드릴게요.
- [0:29](https://youtube.com/watch?v=mgPTpP-62rw&t=29) Ralph Loop이 뭐냐면요.
- [0:29](https://youtube.com/watch?v=mgPTpP-62rw&t=29) AI가 코드를 짜고, 테스트하고, 틀리면 스스로 고치고, 다시 테스트하고.
- [0:34](https://youtube.com/watch?v=mgPTpP-62rw&t=34) 이걸 자동으로 반복하는 플러그인이에요.
- [0:38](https://youtube.com/watch?v=mgPTpP-62rw&t=38) Claude Code에서 플러그인 켜고
- [0:40](https://youtube.com/watch?v=mgPTpP-62rw&t=40) 명령어 하나만 치면 됩니다.
- [0:42](https://youtube.com/watch?v=mgPTpP-62rw&t=42) 할 일을 적어주고, 최대 몇 바퀴 돌릴지 정하고, 끝나면 뭐라고 말하라고 알려주는 거예요.
- [0:49](https://youtube.com/watch?v=mgPTpP-62rw&t=49) AI가 알아서 반복하면서 완성해가고
- [0:52](https://youtube.com/watch?v=mgPTpP-62rw&t=52) 끝나면 COMPLETE라고 출력합니다.
- [0:52](https://youtube.com/watch?v=mgPTpP-62rw&t=52) 이게 전부예요.
- [0:55](https://youtube.com/watch?v=mgPTpP-62rw&t=55) 이렇게 쉬운데 왜 막상 잘 안되냐면요.
- [0:58](https://youtube.com/watch?v=mgPTpP-62rw&t=58) 이 플러그인은 프롬프트를 하나만 받아요.
- [1:01](https://youtube.com/watch?v=mgPTpP-62rw&t=61) 그리고 그 프롬프트를 매번 똑같이 반복합니다.
- [1:05](https://youtube.com/watch?v=mgPTpP-62rw&t=65) 그래서 이 프롬프트 하나에
- [1:07](https://youtube.com/watch?v=mgPTpP-62rw&t=67) 뭘 넣느냐가 전부예요.
- [1:09](https://youtube.com/watch?v=mgPTpP-62rw&t=69) 대부분 여기에 세부사항이 빠진 계획서만 넣고 돌립니다.
- [1:13](https://youtube.com/watch?v=mgPTpP-62rw&t=73) 그러면 AI가 뭘 만들지 대충 추측하고, 결과도 대충 나와요.
- [1:19](https://youtube.com/watch?v=mgPTpP-62rw&t=79) 저도 처음에 그렇게 했거든요.
- [1:21](https://youtube.com/watch?v=mgPTpP-62rw&t=81) 결과가 엉망이었어요.
- [1:22](https://youtube.com/watch?v=mgPTpP-62rw&t=82) 여기서 핵심이 나옵니다.
- [1:24](https://youtube.com/watch?v=mgPTpP-62rw&t=84) 프롬프트에 모든 걸 다 넣으면
- [1:26](https://youtube.com/watch?v=mgPTpP-62rw&t=86) 매번 루프가 돌 때마다
- [1:28](https://youtube.com/watch?v=mgPTpP-62rw&t=88) 같은 내용을 AI가 처음부터 다 읽어야 해요.
- [1:31](https://youtube.com/watch?v=mgPTpP-62rw&t=91) 토큰도 낭비되고, 지금 할 일에 집중도 안 됩니다.
- [1:35](https://youtube.com/watch?v=mgPTpP-62rw&t=95) 대신 파일을 단계별로 분리해두면
- [1:36](https://youtube.com/watch?v=mgPTpP-62rw&t=96) AI가 필요할 때만 읽을 수 있어요.
- [1:39](https://youtube.com/watch?v=mgPTpP-62rw&t=99) 프롬프트는 짧게 유지하면서
- [1:41](https://youtube.com/watch?v=mgPTpP-62rw&t=101) 상세한 내용은 파일에 두는 거예요.
- [1:44](https://youtube.com/watch?v=mgPTpP-62rw&t=104) 필요한 파일은 네 개입니다.
- [1:46](https://youtube.com/watch?v=mgPTpP-62rw&t=106) 첫 번째, PROMPT.md.
- [1:50](https://youtube.com/watch?v=mgPTpP-62rw&t=110) Ralph Loop에 넣을 메인 프롬프트를
- [1:51](https://youtube.com/watch?v=mgPTpP-62rw&t=111) 파일로 저장해두는 거예요.
- [1:53](https://youtube.com/watch?v=mgPTpP-62rw&t=113) 여기에 작업 목표, 완료 조건, 제약 사항, 그리고 작업 규칙까지 넣어둡니다.
- [2:00](https://youtube.com/watch?v=mgPTpP-62rw&t=120) 매번 타이핑할 필요 없이
- [2:01](https://youtube.com/watch?v=mgPTpP-62rw&t=121) 이 파일 내용을 복사해서 쓰면 됩니다.
- [2:05](https://youtube.com/watch?v=mgPTpP-62rw&t=125) 두 번째, specs 폴더.
- [2:06](https://youtube.com/watch?v=mgPTpP-62rw&t=126) 요구사항을 정리해둔 파일들이에요.
- [2:09](https://youtube.com/watch?v=mgPTpP-62rw&t=129) 프롬프트에 전부 넣지 않고
- [2:11](https://youtube.com/watch?v=mgPTpP-62rw&t=131) 파일로 분리하는 이유가 있습니다.
- [2:14](https://youtube.com/watch?v=mgPTpP-62rw&t=134) AI가 지금 작업하는 요구사항에만 집중할 수 있거든요.
- [2:18](https://youtube.com/watch?v=mgPTpP-62rw&t=138) 인증 기능을 만들 때는 인증 요구사항만 읽으면 되니까요.
- [2:23](https://youtube.com/watch?v=mgPTpP-62rw&t=143) 세 번째, 실행계획이에요.
- [2:25](https://youtube.com/watch?v=mgPTpP-62rw&t=145) 쉽게 말해 AI가 관리하는 할 일 목록이에요.
- [2:29](https://youtube.com/watch?v=mgPTpP-62rw&t=149) 요구사항이 "뭘 만들어야 하는지"라면, 이건 "지금 뭘 해야 하는지"예요.
- [2:35](https://youtube.com/watch?v=mgPTpP-62rw&t=155) AI가 요구사항을 읽고 할 일을 정리하고, 끝난 건 체크 표시하고, 새로 발견한 이슈도 추가합니다.
- [2:42](https://youtube.com/watch?v=mgPTpP-62rw&t=162) 네 번째, AGENTS.md.
- [2:45](https://youtube.com/watch?v=mgPTpP-62rw&t=165) 빌드 명령어, 테스트 방법 같은
- [2:47](https://youtube.com/watch?v=mgPTpP-62rw&t=167) 운영 정보를 적어둔 파일이에요.
- [2:50](https://youtube.com/watch?v=mgPTpP-62rw&t=170) 이건 빈 파일로 시작해도 됩니다.
- [2:52](https://youtube.com/watch?v=mgPTpP-62rw&t=172) AI가 작업하면서 알게 된 걸 여기에 기록하게 하세요.
- [2:56](https://youtube.com/watch?v=mgPTpP-62rw&t=176) 정리하면 이런 구조예요.
- [2:58](https://youtube.com/watch?v=mgPTpP-62rw&t=178) 전부 텍스트 파일이에요.
- [2:59](https://youtube.com/watch?v=mgPTpP-62rw&t=179) 어렵지 않습니다.
- [3:01](https://youtube.com/watch?v=mgPTpP-62rw&t=181) 파일 구조를 잡아뒀다면
- [3:02](https://youtube.com/watch?v=mgPTpP-62rw&t=182) 이제 PROMPT.md에 프롬프트를 쓸 차례예요.
- [3:06](https://youtube.com/watch?v=mgPTpP-62rw&t=186) 좋은 프롬프트에는 네 가지가 들어갑니다.
- [3:09](https://youtube.com/watch?v=mgPTpP-62rw&t=189) 목표, 완료 조건, 제약 사항, 그리고 작업 규칙.
- [3:14](https://youtube.com/watch?v=mgPTpP-62rw&t=194) 예를 들어 습관 추적 앱의
- [3:16](https://youtube.com/watch?v=mgPTpP-62rw&t=196) 인증 기능을 만든다면 이렇게 씁니다.
- [3:19](https://youtube.com/watch?v=mgPTpP-62rw&t=199) 핵심은 두 가지예요.
- [3:20](https://youtube.com/watch?v=mgPTpP-62rw&t=200) 하나는 AI가 스스로
- [3:22](https://youtube.com/watch?v=mgPTpP-62rw&t=202) "됐다" "안 됐다"를 판단할 수 있는
- [3:25](https://youtube.com/watch?v=mgPTpP-62rw&t=205) 객관적인 완료 조건.
- [3:27](https://youtube.com/watch?v=mgPTpP-62rw&t=207) 다른 하나는 작업 규칙이에요.
- [3:29](https://youtube.com/watch?v=mgPTpP-62rw&t=209) 이걸 안 넣으면 AI가
- [3:31](https://youtube.com/watch?v=mgPTpP-62rw&t=211) 파일을 깔아뒀는지도 모릅니다.
- [3:33](https://youtube.com/watch?v=mgPTpP-62rw&t=213) specs 폴더를 읽으라고, 실행계획을 관리하라고
- [3:36](https://youtube.com/watch?v=mgPTpP-62rw&t=216) 프롬프트에 써줘야 해요.
- [3:38](https://youtube.com/watch?v=mgPTpP-62rw&t=218) 그리고 작업이 크면
- [3:40](https://youtube.com/watch?v=mgPTpP-62rw&t=220) 단계별로 나눠서 실행하세요.
- [3:43](https://youtube.com/watch?v=mgPTpP-62rw&t=223) 1단계 인증, 2단계 투두 CRUD, 이런 식으로 Phase를 나눠서
- [3:46](https://youtube.com/watch?v=mgPTpP-62rw&t=226) 하나씩 돌리는 게 안전합니다.
- [3:48](https://youtube.com/watch?v=mgPTpP-62rw&t=228) 이 프롬프트를 복사해서
- [3:51](https://youtube.com/watch?v=mgPTpP-62rw&t=231) Ralph Loop에 이렇게 넣으면 됩니다.
- [3:53](https://youtube.com/watch?v=mgPTpP-62rw&t=233) 이 구조로 실제로 앱을 만들어봤어요.
- [3:55](https://youtube.com/watch?v=mgPTpP-62rw&t=235) 요구사항 파일에
- [3:57](https://youtube.com/watch?v=mgPTpP-62rw&t=237) 인증이랑 투두 기능을 정리해두고
- [3:59](https://youtube.com/watch?v=mgPTpP-62rw&t=239) ralph를 돌렸습니다.
- [4:01](https://youtube.com/watch?v=mgPTpP-62rw&t=241) AI가 요구사항을 읽고
- [4:02](https://youtube.com/watch?v=mgPTpP-62rw&t=242) 할 일 목록을 알아서 만들더라고요.
- [4:05](https://youtube.com/watch?v=mgPTpP-62rw&t=245) 우선순위를 매겨서 정리하고
- [4:07](https://youtube.com/watch?v=mgPTpP-62rw&t=247) 순서대로 구현하고 테스트까지 만들었어요.
- [4:12](https://youtube.com/watch?v=mgPTpP-62rw&t=252) AGENTS.md도 처음에 비어있었는데
- [4:13](https://youtube.com/watch?v=mgPTpP-62rw&t=253) 빌드 명령어, 테스트 방법, 프로젝트 구조까지
- [4:17](https://youtube.com/watch?v=mgPTpP-62rw&t=257) AI가 알아서 채워넣었어요.
- [4:20](https://youtube.com/watch?v=mgPTpP-62rw&t=260) 완벽하진 않았지만
- [4:20](https://youtube.com/watch?v=mgPTpP-62rw&t=260) 약 80퍼센트 완성된 앱이 나왔습니다.
- [4:23](https://youtube.com/watch?v=mgPTpP-62rw&t=263) 작업 계획을 잘 잡아뒀더니
- [4:25](https://youtube.com/watch?v=mgPTpP-62rw&t=265) 같은 플러그인인데 결과가 완전히 달랐어요.
- [4:29](https://youtube.com/watch?v=mgPTpP-62rw&t=269) 직접 돌려보면서 알게 된 팁을 알려드릴게요.
- [4:32](https://youtube.com/watch?v=mgPTpP-62rw&t=272) src 폴더 구조를 먼저 잡아주세요.
- [4:34](https://youtube.com/watch?v=mgPTpP-62rw&t=274) routes middleware tests처럼
- [4:37](https://youtube.com/watch?v=mgPTpP-62rw&t=277) 이름만 봐도 뭐가 들어있는지 알 수 있게요.
- [4:40](https://youtube.com/watch?v=mgPTpP-62rw&t=280) 이렇게 하면 AI가 파일을 찾는 속도가 빨라지고, 나중에 고도화할 때도 좋습니다.
- [4:46](https://youtube.com/watch?v=mgPTpP-62rw&t=286) 그리고 ralph를 사용할 때
- [4:48](https://youtube.com/watch?v=mgPTpP-62rw&t=288) 우리가 할 일은 코딩이 아닙니다.
- [4:51](https://youtube.com/watch?v=mgPTpP-62rw&t=291) AI가 잘 일할 수 있는 환경을 만드는 거예요.
- [4:54](https://youtube.com/watch?v=mgPTpP-62rw&t=294) 요구사항을 잘 쓰고, 필요한 파일을 깔아두고, 프롬프트에 목표와 완료 조건을 섬세하게 정리하는 것.
- [5:02](https://youtube.com/watch?v=mgPTpP-62rw&t=302) 그게 우리 역할입니다.
- [5:04](https://youtube.com/watch?v=mgPTpP-62rw&t=304) 한 가지 주의할 점이 있어요.
- [5:06](https://youtube.com/watch?v=mgPTpP-62rw&t=306) Ralph Loop은 여러 사람이 같이 쓰는
- [5:08](https://youtube.com/watch?v=mgPTpP-62rw&t=308) 코드베이스에서는 쓰지 마세요.
- [5:10](https://youtube.com/watch?v=mgPTpP-62rw&t=310) AI가 밤새 코드를 바꿔놓으면
- [5:12](https://youtube.com/watch?v=mgPTpP-62rw&t=312) 다음 날 팀원들이 혼란스럽겠죠.
- [5:15](https://youtube.com/watch?v=mgPTpP-62rw&t=315) 혼자서 처음부터 만들 때 써보세요.
- [5:17](https://youtube.com/watch?v=mgPTpP-62rw&t=317) 사이드 프로젝트나 새 앱을
- [5:19](https://youtube.com/watch?v=mgPTpP-62rw&t=319) 바닥부터 시작할 때 딱 맞습니다.
- [5:22](https://youtube.com/watch?v=mgPTpP-62rw&t=322) 정리할게요.
- [5:24](https://youtube.com/watch?v=mgPTpP-62rw&t=324) Ralph Loop 플러그인은 켜기만 하면 됩니다.
- [5:26](https://youtube.com/watch?v=mgPTpP-62rw&t=326) 근데 그냥 돌리면 실패해요.
- [5:28](https://youtube.com/watch?v=mgPTpP-62rw&t=328) 파일 네 개를 미리 깔아두세요.
- [5:31](https://youtube.com/watch?v=mgPTpP-62rw&t=331) 메인 프롬프트, 요구사항 폴더, 실행계획, 그리고 운영 가이드.
- [5:35](https://youtube.com/watch?v=mgPTpP-62rw&t=335) 프롬프트에는 목표, 완료 조건, 제약 사항, 그리고 파일을 어떻게 쓰라는 작업 규칙을 넣고
- [5:41](https://youtube.com/watch?v=mgPTpP-62rw&t=341) 작업이 크면 단계별로 나눠서 실행하세요.
- [5:46](https://youtube.com/watch?v=mgPTpP-62rw&t=346) 직접 돌려봤더니
- [5:47](https://youtube.com/watch?v=mgPTpP-62rw&t=347) 같은 플러그인인데 결과가 달랐습니다.
- [5:50](https://youtube.com/watch?v=mgPTpP-62rw&t=350) 오늘 알려드린 팁을 PDF로 정리해뒀습니다.
- [5:54](https://youtube.com/watch?v=mgPTpP-62rw&t=354) 파일 구조, 프롬프트 템플릿, 설정 방법까지 전부요.
- [5:57](https://youtube.com/watch?v=mgPTpP-62rw&t=357) 구독, 좋아요, 알림 설정 하신 다음에
- [6:00](https://youtube.com/watch?v=mgPTpP-62rw&t=360) 댓글로 "PDF" 남겨주시면
- [6:03](https://youtube.com/watch?v=mgPTpP-62rw&t=363) 받을 수 있는 링크 보내드릴게요.
- [6:05](https://youtube.com/watch?v=mgPTpP-62rw&t=365) 다음 영상도 바이브코딩 실전 팁입니다.
- [6:09](https://youtube.com/watch?v=mgPTpP-62rw&t=369) 놓치지 마세요.
