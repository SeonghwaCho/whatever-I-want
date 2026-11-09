---
layout: page
title: About
permalink: /about/
---

## KAI (AutoStock) 프로젝트 소개

**KAI**는 금융 시장의 비효율성을 포착하고, 감정을 배제한 기계적 원칙 매매를 자율적으로 수행하는 차세대 인공지능 퀀트 에이전트입니다.

### 핵심 철학 (Core Philosophy)
1. **Safety First**: 수익률보다 자본 보존이 최우선입니다. 절대 100% 현금만 사용하며, 신용/미수/공매도는 시스템 레벨에서 원천 차단됩니다.
2. **Mathematical Risk Control**: LLM(대형 언어 모델)은 포지션 크기나 손절가를 임의로 결정할 수 없습니다. 모든 주문은 하드코딩된 리스크 관리 수학 공식(`RiskManager`)을 반드시 거쳐야 합니다.
3. **Continuous Reflection & Learning**: 실패한 매매는 사라지지 않고 즉시 AI 사후 복기 엔진(`ReflectionEngine`)을 통해 분석되어, 미래의 동일 실수를 방지하는 규칙(`Learned Rules`)으로 자가 발전합니다.

### 시스템 스펙
- **Target Market**: 한국거래소 (KOSPI & KOSDAQ)
- **Execution Broker**: 한국투자증권 KIS Open API (REST & Real-time WebSocket)
- **AI Brain**: Google Gemini 3 Flash Preview (`gemini-3-flash-preview`) & `gemini-embedding-001` MRL Vector Store
- **Infrastructure**: Apple Silicon Mac mini, Python 3.12, SQLite & sqlite-vec, macOS launchd
