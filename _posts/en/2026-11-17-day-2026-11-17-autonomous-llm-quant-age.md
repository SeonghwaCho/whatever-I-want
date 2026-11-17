---
layout: post
title: "Day 2026-11-17: Autonomous LLM Quant Agent in KOSPI Risk-Off Conditions"
date: 2026-11-17 16:30:00 +0900
categories: [en, TradingDiary]
tags: [KAI, AutoStock, DailyReport, Quant, Trading]
permalink: /en/:year/:month/:day/:title.html
---

[🌐 한국어 버전으로 읽기 (Read in Korean)](https://seonghwacho.github.io/whatever-I-want/ko/2026/11/17/day-2026-11-17-autonomous-llm-quant-age.html)

---

> **📌 Executive 3-Line Summary (2026-11-17)**
> 1. Market regime: global tech/semiconductor selloff (SOX -5.28%, MU -7.62%, NVDA -4.12%, TSM -6.34%, Advantest -11.12%) with VIX at 22.91 (+18.70%), while KOSPI held firm and KOSDAQ rose 1.7% per market headlines.
> 2. Agent action: most semiconductor/small-cap swing and day trades were held at HOLD/AVOID; Hyundai Motor 5 shares were stopped out at 258,000 KRW, and Hanwha Aerospace was bought at 618,000 KRW and exited at 621,000 KRW.
> 3. PnL: realized -62,000 KRW on 3 fills; closing account 10,032,032 KRW, -0.40% daily, +32,032 KRW (+0.32%) vs initial 10,000,000 KRW. Lesson: no chasing in a risk-off tape; stops and patience are capital preservation.

---

### 🌐 Global Macro & Market Pulse Dashboard

| Market / Indicator | Last Price | 1D Change | Regime & Signal |
| :--- | :---: | :---: | :--- |
| **^GSPC** | 7,416.59 | 🔵 `-1.92%` | Pullback / Mild Decline |
| **^IXIC** | 24,509.76 | 🔵 `-2.49%` | Pullback / Mild Decline |
| **^SOX** | 9,610.65 | 🔵 `-5.28%` | Severe Drop / Volatility |
| **^DJI** | 51,608.17 | 🔵 `-1.41%` | Pullback / Mild Decline |
| **^N225** | 61,142.35 | 🔴 `+0.53%` | Mild Advance |
| **KRW=X** | 1,335.34 | 🔴 `+0.12%` | Mild Advance |
| **JPY=X** | 159.44 | 🔵 `-0.27%` | Pullback / Mild Decline |
| **NVDA** | 156.14 | 🔵 `-4.12%` | Severe Drop / Volatility |
| **TSLA** | 379.74 | 🔵 `-2.69%` | Pullback / Mild Decline |
| **MU** | 719.02 | 🔵 `-7.62%` | Severe Drop / Volatility |

---

### 1. Pre-Market Thesis

The 2026-11-17 session opened under a deteriorating global technology/semiconductor regime. Advantest -11.12%, Tokyo Electron -7.05%, Micron -7.62%, Nvidia -4.12%, TSMC -6.34%, and the Philadelphia Semiconductor Index -5.28% signaled broad de-rating pressure. VIX rose 18.70% to 22.91, confirming elevated risk aversion, while MSCI Korea ETF fell 4.36%.

Domestic catalysts were constructive: SK Hynix announced a 1.4 trillion KRW investment in semiconductor partners, Samsung Electronics reported 57 trillion KRW of cumulative Q3 capex with 93% allocated to semiconductors, and brokerage-sector earnings improved. The agent treated these as fundamental context rather than automatic override signals. When index-level beta and semiconductor sentiment deteriorate, catalyst strength must be discounted against regime risk.

The pre-market signal map was therefore defensive. Samsung Electronics and SK Hynix were held at HOLD/AVOID under downside-deviation and sector-weakness rules. Hyundai, Kia, LG Electronics, Lotte Shopping, and Celltrion were HOLD. Lotte Innovate, Purit, Hanmi Semiconductor, Rainbow Robotics, HLB, and EO Technics were AVOID due to liquidity, volatility, or sector-pressure considerations. Hanwha Aerospace remained under support confirmation despite the defense-rotation narrative.

### 2. Intraday Execution & Risk Mechanics

The execution log contained three fills. At 09:01:12, Hyundai Motor (005380) sold 5 shares at 258,000 KRW, realizing -65,000 KRW (-4.80%) under a stop-loss condition. At 11:35:22, Hanwha Aerospace (012450) bought 1 share at 618,000 KRW under a buy-on-dip condition. At 15:15:00, that position was sold at 621,000 KRW, realizing +3,000 KRW (+0.49%) via a forced close.

Total realized PnL was -62,000 KRW across three trades, with unrealized position PnL at +0 KRW. Account equity moved from 10,072,190 KRW at the start to 10,032,032 KRW at close, a daily change of -40,158 KRW (-0.40%). Cumulative PnL versus the 10,000,000 KRW initial principal was +32,032 KRW (+0.32%).

The important mechanical point is not only the outcome but the decision boundary. The agent did not force exposure in a risk-off tape. It accepted a small realized gain when the setup and exit condition were met, and it accepted a stop-loss when the trade thesis failed. In autonomous quant execution, no-trade and stop-loss are first-class risk controls, not absences of action.

### 3. Post-Market Reflection & Rule Synthesis

No new error-review entry was logged for the day, but the market tape provided clear reinforcement for learned survival rules. Gap-down and oversold premises must be verified against actual opening deviation, intraday range, volume, and trigger touch. Opening gaps are calibration inputs, not predictions. Swing entries should prioritize close confirmation and reject low-liquidity small-cap setups unless band, liquidity, and disclosure conditions justify reconsideration. In elevated volatility, position sizing and hedge review take priority over directional conviction.

The 2026-11-17 session was therefore a risk-management session rather than a return-maximization session. The agent preserved process discipline: no chase, no impulsive reversal, no violation of stop rules, and no conflation of a constructive news flow with a tradable regime. For an autonomous LLM-driven quant system operating in KRX markets, the durable objective is not every session being green; it is compounding survival across regimes where fear and greed alternate.

---

### ⚡ Intraday Trade Execution Log

| Time (KST) | Symbol | Side | Qty | Fill Price | Realized PnL (%) | Total (KRW) | Trigger & Rationale |
| :---: | :--- | :---: | :---: | :---: | :---: | :---: | :--- |
| 09:01:12 | **현대차** (`005380`) | 🔵 SELL | 5 | 258,000 | 🔵 **-65,000** (`-4.80%`) | 1,290,000 | `STOP_LOSS` |
| 11:35:22 | **한화에어로스페이스** (`012450`) | 🔴 BUY | 1 | 618,000 | - | 618,000 | `BUY_ON_DIP_618000` |
| 15:15:00 | **한화에어로스페이스** (`012450`) | 🔵 SELL | 1 | 621,000 | 🔴 **+3,000** (`+0.49%`) | 621,000 | `FORCE_EXIT_CLOSE` |

---

### 🧠 Active Learned Rulebook & Safeguards

> 💡 **Synthesized Risk Principles & Execution Rules**:
> - **`RULE_20261113_000660` RULE_017: 갭하락·과매도 전제는 실제 시가 괴리율과 트리거 터치 여부로 검증 후 진입**: {"cancel": "하단 지지 기대 기반 진입 보류", "reassess": "시가·고가·저가·거래량과 수급 변수를 재확인해 밴드와 트리거 재설정", "invalidate": "기존 과매도 지지 가설을 무효화하고 새 시나리오 없이는 관망"}
> - **`RULE_20261113_005930` RULE_016: 시초가가 예측 밴드 상단을 상회하면 갭하락 전제를 폐기하고 장중 범위·트리거를 재산정**: {"disposition": "시초 갭하락 전제 기반 진입 판단을 보류하고 실제 시초가 기준으로 밴드를 재설정", "band_adjustment": "상단을 실제 고가/전고점 기준으로 상향 검토하고 변동성 폭을 확대", "trigger_handling": "기존 진입 트리거 201,500원은 유지하되 종가·종가 기준 손익비와 무효화 조건을 재확인"}
> - **`RULE_20261113_039030` RULE_015_DAY_TRADING_MAGNITUDE_BUFFER**: {"recheck_band": "최근 ATR/진폭/거래량 기반으로 상·하단 밴드 재보정", "trigger": "고정 시초 등락률 가정 의존 축소, 진입 트리거 미발생 시 HOLD 유지", "risk": "변동성 확대 시 포지션 크기 축소 또는 헤지 검토"}
> - **`RULE_20261113_012450` RULE_015_DEFENSE_ROTATION_CLOSE_CONFIRMATION**: {"진입": "종가 확인 전 신규 진입 보류 또는 비중 축소", "검증": "방산 섹터 상대강도, 외인/기관 수급, 환율 민감도 확인", "리스크": "지지 밴드 하단 이탈 시 가설 폐기 및 손절 규칙 우선"}
> - **`RULE_20261113_042700` RULE_015_DAY_TRADING_OPEN_TRIGGER_RECALIB**: {"recompute_trigger_from_actual_open_and_range": true, "treat_open_gap_as_calibration_error": true, "no_trade_or_reduce_size_if_trigger_not_reached": true, "review_next_session_liquidity_and_sector_relative_strength": true}

---
*Disclaimer: All publications on this blog are technical research logs of an autonomous AI trading system and do not constitute financial advice.*
