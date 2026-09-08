---
title: "MCP vs API: Why traditional APIs are failing AI agents"
source_url: https://youtube.com/watch?v=185XGEMefgc
video_id: 185XGEMefgc
source_type: youtube
lang: en
analyzed: 2026-09-08
category: 일반학습
tags: ["주제/MCP", "개념/MCP/mcp", "개념/자기서술", "개념/에이전트-네이티브-아키텍처", "개념/컨텍스트-기반-도구-탐색", "개념/API-vs-MCP-레이어-구분"]
key_concepts: ["MCP (Model Context Protocol)", "자기서술(self-describing) 인터페이스", "MCP 서버", "에이전트 네이티브 아키텍처", "컨텍스트 기반 도구 탐색", "API vs MCP 레이어 구분"]
status: active
---
# MCP vs API: Why traditional APIs are failing AI agents

## 🧠 이해 (Understand)
- **Summary:** MCP(Model Context Protocol)는 AI 모델이 외부 도구·데이터에 자율적으로 접근할 수 있도록 설계된 새로운 표준 프로토콜이다. 기존 API는 '프로그램 대 프로그램' 통신에 최적화되어 있어, 모델이 사용하려면 개발자가 매번 엔드포인트·파라미터를 하드코딩해야 했다. MCP는 각 서비스가 자신의 기능을 JSON 스키마로 자기서술(self-describing)하게 하여, 모델이 어떤 도구가 있는지 자동 탐색하고 스스로 판단해 호출할 수 있게 한다. API를 대체하는 것이 아니라 API 위에 올라타는 미들웨어 레이어로, HTTP가 인터넷을 통일했듯 MCP는 AI 에이전트 생태계를 상호운용 가능하게 만드는 것을 목표로 한다. 현재는 생태계 표준화, 보안 권한 제어, 개발자 사고방식 전환이라는 세 가지 과제를 안고 있다.
- **Core Message:** MCP는 API를 대체하는 것이 아니라 그 위에서 작동하는 레이어로, AI 모델이 외부 도구를 하드코딩 없이 자율적으로 발견하고 사용할 수 있게 해주는 새로운 표준이다.
> API is a locked cabinet. You need to know exactly what drawer to open and what shape the key is.
> MCP is trying to make AI environments interoperable — the same way HTTP made websites interoperable.
> MCP sits one layer above APIs, turning them from static routes into living interfaces that models can actually reason about.
❗ MCP를 사용하면 100개의 개별 커스텀 통합 대신 MCP 인터페이스 하나만 만들어도 모든 호환 모델이 즉시 사용할 수 있다.
❗ MCP는 API를 없애는 것이 아니라, 모델과 API 사이의 미들웨어 레이어를 대체하는 구조다.
❗ MCP 스펙은 이미 capabilities, scopes, authentication 등 보안 요소를 정의하고 있으며, 보안 제어가 프로토콜 레이어 안에 내장된다.

## 📚 핵심 용어
- **MCP (Model Context Protocol):** AI 모델이 외부 도구·서비스를 자율적으로 탐색하고 호출할 수 있도록 정의된 표준 통신 규약. / 매장 직원(모델)에게 각 코너가 무엇을 파는지 적힌 안내판(MCP 서버)을 주는 것. 일일이 알려주지 않아도 직원이 스스로 필요한 코너로 간다. / API는 개발자가 '어느 서랍, 어떤 열쇠'를 직접 지정해줘야 하는 반면, MCP는 모델이 스스로 서랍 목록을 읽고 판단한다.
- **MCP 서버:** 서비스가 자신의 기능과 입출력 형식을 JSON 스키마로 공개하는 경량 프로세스. / 식당 메뉴판과 같다. 요리사(모델)가 어떤 재료로 무슨 요리를 만들 수 있는지 메뉴판만 보면 바로 파악할 수 있다. / REST API 문서는 개발자가 읽고 코드로 변환해야 하지만, MCP 서버는 모델이 직접 기계 판독해 즉시 호출할 수 있다.
- **자기서술(Self-describing) 인터페이스:** 도구 스스로 자신의 기능·입력·출력을 기계가 읽을 수 있는 형식으로 명시하는 설계 방식. / IKEA 가구 박스에 부품 목록과 그림 설명서가 이미 들어 있는 것처럼, 별도 안내 없이도 무엇을 어떻게 쓰는지 알 수 있다. / 일반 API는 외부 문서를 사람이 읽어야 하지만, 자기서술 인터페이스는 모델이 런타임에 직접 스키마를 읽어 파악한다.
- **에이전트 네이티브 아키텍처:** 모델이 도구·데이터·추론을 직접 오케스트레이션할 수 있도록 설계된 소프트웨어 구조. / 사람을 위해 설계된 키보드·마우스 UI 대신, 로봇 팔(모델)이 직접 잡을 수 있는 손잡이 구조로 공장을 재설계하는 것. / 전통 아키텍처는 사람이나 코드가 클라이언트지만, 에이전트 네이티브 아키텍처에서는 모델 자체가 1등 시민 클라이언트다.

## 🚀 실행 (Execute)
- [ ] MCP 공식 스펙 문서(modelcontextprotocol.io)를 읽고, 실제 MCP 서버 예제 하나를 로컬에서 실행해보기 — ⏰ 이번 주 · ⚡ 2~3시간
  - 담당: 나 (개발자 또는 기술 기획자)
  - 이유: 개념 이해를 넘어 MCP 서버의 JSON 스키마 구조와 연결 방식을 직접 체험해야 실무 적용 판단이 가능하다.
- [ ] 현재 운영 중인 서비스(또는 PICKS 이커머스 도구)의 API 중 AI 에이전트가 반복 호출하는 것을 목록화하고, MCP 서버로 전환 시 이점을 검토 — ⏰ 2주 내 · ⚡ 2시간
  - 담당: 나 또는 팀 개발자
  - 이유: MCP의 실질적 가치는 반복적인 통합 코드를 줄이는 데 있으므로, 가장 자주 쓰는 API부터 전환 후보를 식별하면 ROI가 명확해진다.
- 자료: modelcontextprotocol.io — MCP 공식 스펙 및 SDK 문서 (실제 존재 확인 필요)
- 자료: Anthropic MCP 발표 블로그 포스트 (anthropic.com, 검색 필요)
- 자료: 영상 내 안내된 '심화 MCP 영상' (같은 채널의 다음 영상)
- Timeline: 1주차: MCP 공식 문서 열람 + 예제 서버 실행 → 2주차: 현재 API 목록화 및 MCP 전환 후보 선정 → 1개월 내: 파일럿 MCP 서버 구성 및 에이전트 연동 테스트

## 🔗 연결
- 카테고리: [[_category-일반학습]]
- 주제: [[_topic-MCP]]
- 핵심 개념: [[_concept-mcp|MCP]] · [[_concept-자기서술|자기서술]] · [[_concept-에이전트-네이티브-아키텍처|에이전트 네이티브 아키텍처]] · [[_concept-컨텍스트-기반-도구-탐색|컨텍스트 기반 도구 탐색]] · [[_concept-API-vs-MCP-레이어-구분|API vs MCP 레이어 구분]]

## 📝 자막 전문
- [0:04](https://youtube.com/watch?v=185XGEMefgc&t=4) If you've ever built an app
that talks to an AI model,
- [0:09](https://youtube.com/watch?v=185XGEMefgc&t=9) MCP changes everything.
- [0:11](https://youtube.com/watch?v=185XGEMefgc&t=11) Because the way AI connects
to your tools, data,
- [0:14](https://youtube.com/watch?v=185XGEMefgc&t=14) and systems is being
completely rewritten.
- [0:17](https://youtube.com/watch?v=185XGEMefgc&t=17) For years, APIs used to be
the glue that held everything
- [0:21](https://youtube.com/watch?v=185XGEMefgc&t=21) together.
- [0:22](https://youtube.com/watch?v=185XGEMefgc&t=22) But now there's a new
standard rising fast,
- [0:25](https://youtube.com/watch?v=185XGEMefgc&t=25) and that something is called the
model context protocol, or MCP.
- [0:30](https://youtube.com/watch?v=185XGEMefgc&t=30) And it might just be the biggest
shift since APIs themselves.
- [0:35](https://youtube.com/watch?v=185XGEMefgc&t=35) So what exactly is
MCP, and why are people
- [0:39](https://youtube.com/watch?v=185XGEMefgc&t=39) saying it could replace
the way we integrate AI
- [0:43](https://youtube.com/watch?v=185XGEMefgc&t=43) with everything around it.
- [0:45](https://youtube.com/watch?v=185XGEMefgc&t=45) Let's break it down clearly so
that by the end of this video,
- [0:49](https://youtube.com/watch?v=185XGEMefgc&t=49) you'll understand how
MCP actually works
- [0:52](https://youtube.com/watch?v=185XGEMefgc&t=52) and how it's
different from APIs,
- [0:54](https://youtube.com/watch?v=185XGEMefgc&t=54) and why it's reshaping how we
build agents and applications
- [0:59](https://youtube.com/watch?v=185XGEMefgc&t=59) that use large language models.
- [1:01](https://youtube.com/watch?v=185XGEMefgc&t=61) For decades, API were
the universal handshake
- [1:05](https://youtube.com/watch?v=185XGEMefgc&t=65) between systems.
- [1:07](https://youtube.com/watch?v=185XGEMefgc&t=67) You define an endpoint,
you send a request
- [1:10](https://youtube.com/watch?v=185XGEMefgc&t=70) and you got a response back.
- [1:12](https://youtube.com/watch?v=185XGEMefgc&t=72) It's clean and predictable,
and for traditional software,
- [1:15](https://youtube.com/watch?v=185XGEMefgc&t=75) that is perfect.
- [1:17](https://youtube.com/watch?v=185XGEMefgc&t=77) But when large language
models enter the picture,
- [1:20](https://youtube.com/watch?v=185XGEMefgc&t=80) everything changed.
- [1:21](https://youtube.com/watch?v=185XGEMefgc&t=81) Models don't just
call one endpoint,
- [1:24](https://youtube.com/watch?v=185XGEMefgc&t=84) they might talk to 10 endpoints.
- [1:26](https://youtube.com/watch?v=185XGEMefgc&t=86) They want to chain them
together or even interpret
- [1:30](https://youtube.com/watch?v=185XGEMefgc&t=90) unstructured data and also
ask follow up questions.
- [1:34](https://youtube.com/watch?v=185XGEMefgc&t=94) And that means they don't
just need access to a tool,
- [1:37](https://youtube.com/watch?v=185XGEMefgc&t=97) they also need context.
- [1:39](https://youtube.com/watch?v=185XGEMefgc&t=99) But here's the problem
APIs are built for programs
- [1:44](https://youtube.com/watch?v=185XGEMefgc&t=104) talking to programs.
- [1:45](https://youtube.com/watch?v=185XGEMefgc&t=105) They are not built for models.
- [1:47](https://youtube.com/watch?v=185XGEMefgc&t=107) Reasoning over messy
real world data and API
- [1:51](https://youtube.com/watch?v=185XGEMefgc&t=111) is like a locked cabinet.
- [1:54](https://youtube.com/watch?v=185XGEMefgc&t=114) You need to know exactly
what drawer to open
- [1:58](https://youtube.com/watch?v=185XGEMefgc&t=118) and what shape the key is.
- [1:59](https://youtube.com/watch?v=185XGEMefgc&t=119) But a model is
trying to understand
- [2:01](https://youtube.com/watch?v=185XGEMefgc&t=121) what's inside the cabinet
without clear labels
- [2:05](https://youtube.com/watch?v=185XGEMefgc&t=125) so it doesn't know
which function to call
- [2:08](https://youtube.com/watch?v=185XGEMefgc&t=128) or which parameters to
pass until you tell it.
- [2:11](https://youtube.com/watch?v=185XGEMefgc&t=131) And you have to
hardcode it sometimes.
- [2:13](https://youtube.com/watch?v=185XGEMefgc&t=133) And oftentimes have to keep
explaining over and over again.
- [2:17](https://youtube.com/watch?v=185XGEMefgc&t=137) That's where MCP comes in.
- [2:19](https://youtube.com/watch?v=185XGEMefgc&t=139) It was designed to make models
autonomously discover and use
- [2:24](https://youtube.com/watch?v=185XGEMefgc&t=144) tools without the
constant hand-holding
- [2:27](https://youtube.com/watch?v=185XGEMefgc&t=147) that we've been doing
in prompt engineering.
- [2:30](https://youtube.com/watch?v=185XGEMefgc&t=150) So before we dive deeper,
let's define both sides.
- [2:34](https://youtube.com/watch?v=185XGEMefgc&t=154) Clearly, APIs are the
traditional way software
- [2:38](https://youtube.com/watch?v=185XGEMefgc&t=158) communicates.
- [2:39](https://youtube.com/watch?v=185XGEMefgc&t=159) They expose specific endpoints.
- [2:41](https://youtube.com/watch?v=185XGEMefgc&t=161) They accept requests in
structured formats like JSON,
- [2:46](https://youtube.com/watch?v=185XGEMefgc&t=166) and they return
predictable outputs.
- [2:48](https://youtube.com/watch?v=185XGEMefgc&t=168) Developers document them,
secure them, and version them.
- [2:52](https://youtube.com/watch?v=185XGEMefgc&t=172) But they assume one
thing that both sides
- [2:55](https://youtube.com/watch?v=185XGEMefgc&t=175) knows exactly what to expect.
- [2:57](https://youtube.com/watch?v=185XGEMefgc&t=177) MCP flips that assumption.
- [2:59](https://youtube.com/watch?v=185XGEMefgc&t=179) Instead of the model needing
to be manually thought
- [3:02](https://youtube.com/watch?v=185XGEMefgc&t=182) about each endpoint, MCP gives
the model a standardized way
- [3:07](https://youtube.com/watch?v=185XGEMefgc&t=187) to discover what a tool can do.
- [3:09](https://youtube.com/watch?v=185XGEMefgc&t=189) What kind of inputs it expects,
and what kind of outputs
- [3:13](https://youtube.com/watch?v=185XGEMefgc&t=193) it returns all through context.
- [3:16](https://youtube.com/watch?v=185XGEMefgc&t=196) Think of it like giving a
model a live, machine readable
- [3:20](https://youtube.com/watch?v=185XGEMefgc&t=200) map of your API instead of
a static instruction manual.
- [3:25](https://youtube.com/watch?v=185XGEMefgc&t=205) Now that sounds abstract,
so let's make it real.
- [3:28](https://youtube.com/watch?v=185XGEMefgc&t=208) Imagine you're building
an AI agent that
- [3:30](https://youtube.com/watch?v=185XGEMefgc&t=210) manages support tickets.
- [3:32](https://youtube.com/watch?v=185XGEMefgc&t=212) You give it access to
Gmail, notion, and Jira.
- [3:36](https://youtube.com/watch?v=185XGEMefgc&t=216) With APIs.
- [3:37](https://youtube.com/watch?v=185XGEMefgc&t=217) You'd write custom code
for each integration,
- [3:40](https://youtube.com/watch?v=185XGEMefgc&t=220) handle issues like pagination,
auth tokens, error cases,
- [3:46](https://youtube.com/watch?v=185XGEMefgc&t=226) rate limits, and also teach
the model through long prompts
- [3:51](https://youtube.com/watch?v=185XGEMefgc&t=231) like when you want to
create a Jira ticket.
- [3:54](https://youtube.com/watch?v=185XGEMefgc&t=234) Call this endpoint
with these fields when
- [3:57](https://youtube.com/watch?v=185XGEMefgc&t=237) you want to reply to an email,
call Gmail with this payload,
- [4:01](https://youtube.com/watch?v=185XGEMefgc&t=241) but with MCP you don't
need to do any of that.
- [4:04](https://youtube.com/watch?v=185XGEMefgc&t=244) Each service like Gmail,
notion, Jira exposes and MCP
- [4:10](https://youtube.com/watch?v=185XGEMefgc&t=250) compatible interface.
- [4:12](https://youtube.com/watch?v=185XGEMefgc&t=252) The model discovers
these tools automatically
- [4:15](https://youtube.com/watch?v=185XGEMefgc&t=255) and understands their functions
as part of its environment.
- [4:19](https://youtube.com/watch?v=185XGEMefgc&t=259) You don't tell it how to
do it, you give the context
- [4:22](https://youtube.com/watch?v=185XGEMefgc&t=262) and it figures it
out dynamically.
- [4:24](https://youtube.com/watch?v=185XGEMefgc&t=264) That's the core
difference between APIs,
- [4:27](https://youtube.com/watch?v=185XGEMefgc&t=267) which are code level contracts
between two applications,
- [4:31](https://youtube.com/watch?v=185XGEMefgc&t=271) and MCP, which is a semantic
protocol between a model
- [4:36](https://youtube.com/watch?v=185XGEMefgc&t=276) and its environment.
- [4:37](https://youtube.com/watch?v=185XGEMefgc&t=277) So you're no longer teaching
the model which endpoint to hit,
- [4:40](https://youtube.com/watch?v=185XGEMefgc&t=280) but you're giving it a
structured description of what's
- [4:43](https://youtube.com/watch?v=185XGEMefgc&t=283) available and letting it
reason about which tool to use
- [4:47](https://youtube.com/watch?v=185XGEMefgc&t=287) and when.
- [4:48](https://youtube.com/watch?v=185XGEMefgc&t=288) It's like giving the
model a toolbox instead
- [4:50](https://youtube.com/watch?v=185XGEMefgc&t=290) of forcing it to memorize
how each tool works.
- [4:54](https://youtube.com/watch?v=185XGEMefgc&t=294) This shift might sound
small, but it's actually
- [4:56](https://youtube.com/watch?v=185XGEMefgc&t=296) massive for developers building
agentic systems with APIs.
- [5:01](https://youtube.com/watch?v=185XGEMefgc&t=301) The logic of what to
call and when to call it
- [5:04](https://youtube.com/watch?v=185XGEMefgc&t=304) lived in your app code.
- [5:06](https://youtube.com/watch?v=185XGEMefgc&t=306) With MCP, that
logic can actually
- [5:08](https://youtube.com/watch?v=185XGEMefgc&t=308) move into the model's
reasoning layer itself.
- [5:11](https://youtube.com/watch?v=185XGEMefgc&t=311) You can now build a
general purpose agent
- [5:14](https://youtube.com/watch?v=185XGEMefgc&t=314) that can plug into any tool
that supports the protocol,
- [5:18](https://youtube.com/watch?v=185XGEMefgc&t=318) without having to rewrite
code for each integration.
- [5:21](https://youtube.com/watch?v=185XGEMefgc&t=321) That's the magic here, and it's
standardization the same way
- [5:26](https://youtube.com/watch?v=185XGEMefgc&t=326) HTTP made websites
interoperable,
- [5:30](https://youtube.com/watch?v=185XGEMefgc&t=330) allowing them to
share and use data
- [5:32](https://youtube.com/watch?v=185XGEMefgc&t=332) with each and other systems,
and letting them work together
- [5:36](https://youtube.com/watch?v=185XGEMefgc&t=336) to perform tasks with
minimal human intervention.
- [5:39](https://youtube.com/watch?v=185XGEMefgc&t=339) MCP is trying to make AI
environments interoperable.
- [5:44](https://youtube.com/watch?v=185XGEMefgc&t=344) But let's talk about
what's actually
- [5:46](https://youtube.com/watch?v=185XGEMefgc&t=346) happening under the hood.
- [5:47](https://youtube.com/watch?v=185XGEMefgc&t=347) And MCP server is a lightweight
process that sits next
- [5:51](https://youtube.com/watch?v=185XGEMefgc&t=351) to your service or data source.
- [5:53](https://youtube.com/watch?v=185XGEMefgc&t=353) It describes what it can do
and what functions it exposes,
- [5:57](https://youtube.com/watch?v=185XGEMefgc&t=357) all using JSON schemas.
- [6:00](https://youtube.com/watch?v=185XGEMefgc&t=360) The model connects
to this server
- [6:01](https://youtube.com/watch?v=185XGEMefgc&t=361) through a standardized interface
like WebSocket or HTTP,
- [6:06](https://youtube.com/watch?v=185XGEMefgc&t=366) and receives metadata about
the available resources.
- [6:11](https://youtube.com/watch?v=185XGEMefgc&t=371) Once connected, the model can
call these functions directly,
- [6:15](https://youtube.com/watch?v=185XGEMefgc&t=375) not by guessing, but
by using the metadata.
- [6:19](https://youtube.com/watch?v=185XGEMefgc&t=379) It knows what
inputs are required
- [6:21](https://youtube.com/watch?v=185XGEMefgc&t=381) and what each field means and
what type of output to expect.
- [6:25](https://youtube.com/watch?v=185XGEMefgc&t=385) The beauty is that everything
is self-describing.
- [6:28](https://youtube.com/watch?v=185XGEMefgc&t=388) You don't have to prompt
engineer the schema or reformat
- [6:33](https://youtube.com/watch?v=185XGEMefgc&t=393) responses.
- [6:34](https://youtube.com/watch?v=185XGEMefgc&t=394) It's all standardized.
- [6:35](https://youtube.com/watch?v=185XGEMefgc&t=395) Compare that to an API where
every single integration
- [6:40](https://youtube.com/watch?v=185XGEMefgc&t=400) is bespoke.
- [6:42](https://youtube.com/watch?v=185XGEMefgc&t=402) You need a developer to read
the docs, map the payloads,
- [6:45](https://youtube.com/watch?v=185XGEMefgc&t=405) and manually wrap the endpoints
so MCP abstracts that away.
- [6:50](https://youtube.com/watch?v=185XGEMefgc&t=410) This means instead of building
100 custom integrations,
- [6:53](https://youtube.com/watch?v=185XGEMefgc&t=413) you build one MCP interface
and every compatible model
- [6:57](https://youtube.com/watch?v=185XGEMefgc&t=417) can use it instantly.
- [6:59](https://youtube.com/watch?v=185XGEMefgc&t=419) That's why people are
calling MCP the plug and play
- [7:02](https://youtube.com/watch?v=185XGEMefgc&t=422) layer for AI systems.
- [7:04](https://youtube.com/watch?v=185XGEMefgc&t=424) Now, this doesn't mean
APIs are going away.
- [7:07](https://youtube.com/watch?v=185XGEMefgc&t=427) APIs are still the foundation.
- [7:09](https://youtube.com/watch?v=185XGEMefgc&t=429) They're how your systems
actually function.
- [7:12](https://youtube.com/watch?v=185XGEMefgc&t=432) But MCP changes how
models access those APIs.
- [7:16](https://youtube.com/watch?v=185XGEMefgc&t=436) Think of it like this.
- [7:18](https://youtube.com/watch?v=185XGEMefgc&t=438) MCP doesn't replace
your backend.
- [7:20](https://youtube.com/watch?v=185XGEMefgc&t=440) It replaces the middleware
between the model and the API.
- [7:25](https://youtube.com/watch?v=185XGEMefgc&t=445) The MCP server acts
like a translator,
- [7:28](https://youtube.com/watch?v=185XGEMefgc&t=448) converting your existing
APIs into a format
- [7:31](https://youtube.com/watch?v=185XGEMefgc&t=451) that models can
understand automatically.
- [7:34](https://youtube.com/watch?v=185XGEMefgc&t=454) So instead of saying MCP
versus API, it's more like MCP
- [7:40](https://youtube.com/watch?v=185XGEMefgc&t=460) on top of APIs.
- [7:41](https://youtube.com/watch?v=185XGEMefgc&t=461) This distinction is key.
- [7:44](https://youtube.com/watch?v=185XGEMefgc&t=464) MCP doesn't compete with APIs.
- [7:47](https://youtube.com/watch?v=185XGEMefgc&t=467) It actually leverages
them, but it changes
- [7:50](https://youtube.com/watch?v=185XGEMefgc&t=470) who the client is with API.
- [7:52](https://youtube.com/watch?v=185XGEMefgc&t=472) The client is another
program or user with MCP,
- [7:57](https://youtube.com/watch?v=185XGEMefgc&t=477) the client is the model itself.
- [7:59](https://youtube.com/watch?v=185XGEMefgc&t=479) And that subtle
difference changes
- [8:01](https://youtube.com/watch?v=185XGEMefgc&t=481) everything about how
we design integrations.
- [8:05](https://youtube.com/watch?v=185XGEMefgc&t=485) Let's Zoom out for a bit.
- [8:06](https://youtube.com/watch?v=185XGEMefgc&t=486) The rise of MCP is
part of a bigger
- [8:09](https://youtube.com/watch?v=185XGEMefgc&t=489) movement towards model
native software architecture.
- [8:13](https://youtube.com/watch?v=185XGEMefgc&t=493) For decades, we've built
systems for humans and for code.
- [8:17](https://youtube.com/watch?v=185XGEMefgc&t=497) Now we're building systems
for models and models
- [8:20](https://youtube.com/watch?v=185XGEMefgc&t=500) don't consume REST
endpoints the way code does.
- [8:24](https://youtube.com/watch?v=185XGEMefgc&t=504) They consume context,
which includes
- [8:26](https://youtube.com/watch?v=185XGEMefgc&t=506) structured descriptions,
schemas, and examples.
- [8:30](https://youtube.com/watch?v=185XGEMefgc&t=510) They do this so that they
can reason, plan and act.
- [8:33](https://youtube.com/watch?v=185XGEMefgc&t=513) So MCP gives them that
in a standardized way.
- [8:37](https://youtube.com/watch?v=185XGEMefgc&t=517) That's why developers
building agent frameworks
- [8:39](https://youtube.com/watch?v=185XGEMefgc&t=519) are moving in this direction.
- [8:41](https://youtube.com/watch?v=185XGEMefgc&t=521) They're realizing
that connecting
- [8:43](https://youtube.com/watch?v=185XGEMefgc&t=523) a model to a world of tools
isn't about a bigger context
- [8:46](https://youtube.com/watch?v=185XGEMefgc&t=526) window.
- [8:47](https://youtube.com/watch?v=185XGEMefgc&t=527) It's about cleaner protocols.
- [8:49](https://youtube.com/watch?v=185XGEMefgc&t=529) And let's be honest,
it's not all magic.
- [8:52](https://youtube.com/watch?v=185XGEMefgc&t=532) MCP is still pretty new.
- [8:54](https://youtube.com/watch?v=185XGEMefgc&t=534) The biggest challenge
right now is adoption.
- [8:56](https://youtube.com/watch?v=185XGEMefgc&t=536) For MCP to truly
work, the ecosystem
- [8:59](https://youtube.com/watch?v=185XGEMefgc&t=539) needs servers,
clients, and tools
- [9:02](https://youtube.com/watch?v=185XGEMefgc&t=542) to agree on the same standard.
- [9:04](https://youtube.com/watch?v=185XGEMefgc&t=544) Another huge challenge
is security and control.
- [9:08](https://youtube.com/watch?v=185XGEMefgc&t=548) When models can directly call
tools through a protocol,
- [9:12](https://youtube.com/watch?v=185XGEMefgc&t=552) you need clear
permission layers.
- [9:14](https://youtube.com/watch?v=185XGEMefgc&t=554) You don't want a model
accidentally sending an email,
- [9:17](https://youtube.com/watch?v=185XGEMefgc&t=557) deleting a file or making
a huge database change
- [9:20](https://youtube.com/watch?v=185XGEMefgc&t=560) that it wasn't supposed to.
- [9:22](https://youtube.com/watch?v=185XGEMefgc&t=562) APIs handle that through
authentication keys and rate
- [9:26](https://youtube.com/watch?v=185XGEMefgc&t=566) limits.
- [9:27](https://youtube.com/watch?v=185XGEMefgc&t=567) MCP needs to bring
those guardrails
- [9:30](https://youtube.com/watch?v=185XGEMefgc&t=570) into its protocol layer,
which is already happening.
- [9:33](https://youtube.com/watch?v=185XGEMefgc&t=573) The spec defines capabilities,
scopes, and authentication
- [9:37](https://youtube.com/watch?v=185XGEMefgc&t=577) methods that keep things safe.
- [9:40](https://youtube.com/watch?v=185XGEMefgc&t=580) But it's still early days,
and the final challenge
- [9:44](https://youtube.com/watch?v=185XGEMefgc&t=584) is the developer mindset.
- [9:45](https://youtube.com/watch?v=185XGEMefgc&t=585) Most of us grew up
in an API world.
- [9:48](https://youtube.com/watch?v=185XGEMefgc&t=588) We think in terms of
endpoints and routes.
- [9:51](https://youtube.com/watch?v=185XGEMefgc&t=591) MCP asks us to think in terms
of capabilities and context
- [9:56](https://youtube.com/watch?v=185XGEMefgc&t=596) to design systems that
describe what they can do,
- [9:59](https://youtube.com/watch?v=185XGEMefgc&t=599) not just how to do it.
- [10:01](https://youtube.com/watch?v=185XGEMefgc&t=601) That's a huge paradigm shift,
but it's worth learning early.
- [10:05](https://youtube.com/watch?v=185XGEMefgc&t=605) Here's where it
all comes together.
- [10:07](https://youtube.com/watch?v=185XGEMefgc&t=607) Think about the moment when
HTTP unified the internet.
- [10:11](https://youtube.com/watch?v=185XGEMefgc&t=611) Before that, every service
had its own protocol
- [10:15](https://youtube.com/watch?v=185XGEMefgc&t=615) from FTP, Gopher, Telnet, which
are all different internet
- [10:19](https://youtube.com/watch?v=185XGEMefgc&t=619) protocols.
- [10:20](https://youtube.com/watch?v=185XGEMefgc&t=620) Once the web standardized
on HTTP, suddenly
- [10:24](https://youtube.com/watch?v=185XGEMefgc&t=624) everything became interoperable.
- [10:26](https://youtube.com/watch?v=185XGEMefgc&t=626) MCP is doing the same
thing for AI agents.
- [10:30](https://youtube.com/watch?v=185XGEMefgc&t=630) Instead of each company
inventing its own plugin format
- [10:33](https://youtube.com/watch?v=185XGEMefgc&t=633) or integration layer, MCP
provides a single open protocol
- [10:38](https://youtube.com/watch?v=185XGEMefgc&t=638) that any model can understand.
- [10:40](https://youtube.com/watch?v=185XGEMefgc&t=640) You build your connector
once and any compliant model
- [10:43](https://youtube.com/watch?v=185XGEMefgc&t=643) can use it.
- [10:44](https://youtube.com/watch?v=185XGEMefgc&t=644) That means the
future of AI tools
- [10:46](https://youtube.com/watch?v=185XGEMefgc&t=646) will look less like
custom integrations
- [10:49](https://youtube.com/watch?v=185XGEMefgc&t=649) and more like a
shared ecosystem.
- [10:51](https://youtube.com/watch?v=185XGEMefgc&t=651) You will have an MCP server
for your product and any AI
- [10:56](https://youtube.com/watch?v=185XGEMefgc&t=656) like Gemini Claude GPT
can use it instantly.
- [11:01](https://youtube.com/watch?v=185XGEMefgc&t=661) That's the world
we're heading towards,
- [11:02](https://youtube.com/watch?v=185XGEMefgc&t=662) one where models, not
just humans, become
- [11:05](https://youtube.com/watch?v=185XGEMefgc&t=665) first class users of software.
- [11:08](https://youtube.com/watch?v=185XGEMefgc&t=668) So to sum it all up
APIs are not dead.
- [11:11](https://youtube.com/watch?v=185XGEMefgc&t=671) They are just evolving.
- [11:13](https://youtube.com/watch?v=185XGEMefgc&t=673) APIs were made for
deterministic systems.
- [11:16](https://youtube.com/watch?v=185XGEMefgc&t=676) One program asking
another for data,
- [11:18](https://youtube.com/watch?v=185XGEMefgc&t=678) and MCP is made for
probabilistic realistic systems,
- [11:22](https://youtube.com/watch?v=185XGEMefgc&t=682) a model reasoning
about what it can do.
- [11:25](https://youtube.com/watch?v=185XGEMefgc&t=685) So the next time someone says
MCP versus API, just remember
- [11:30](https://youtube.com/watch?v=185XGEMefgc&t=690) it's not a direct comparison.
- [11:32](https://youtube.com/watch?v=185XGEMefgc&t=692) It's a foundation being rebuilt.
MCP sits one layer above APIs
- [11:37](https://youtube.com/watch?v=185XGEMefgc&t=697) and turning them from static
routes into living interfaces
- [11:42](https://youtube.com/watch?v=185XGEMefgc&t=702) that models can
actually reason about.
- [11:44](https://youtube.com/watch?v=185XGEMefgc&t=704) And as more frameworks
adopt it, you'll
- [11:47](https://youtube.com/watch?v=185XGEMefgc&t=707) start seeing a new
pattern emerge.
- [11:49](https://youtube.com/watch?v=185XGEMefgc&t=709) Instead of hard
coded integrations,
- [11:51](https://youtube.com/watch?v=185XGEMefgc&t=711) we'll build model
aware systems where
- [11:53](https://youtube.com/watch?v=185XGEMefgc&t=713) context, tools, and reasoning
can all live in harmony.
- [11:58](https://youtube.com/watch?v=185XGEMefgc&t=718) I hope this video was helpful
in explaining the differences
- [12:00](https://youtube.com/watch?v=185XGEMefgc&t=720) between MYC and APIs.
- [12:03](https://youtube.com/watch?v=185XGEMefgc&t=723) To learn more about
the model context
- [12:05](https://youtube.com/watch?v=185XGEMefgc&t=725) protocol at a deeper level,
check out this next video.
