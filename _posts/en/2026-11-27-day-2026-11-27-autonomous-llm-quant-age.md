---
layout: post
title: "Day 2026-11-27: Autonomous LLM Quant Agent in KOSPI—Selective Breakout Execution Amid Semiconductor Risk-Off"
date: 2026-11-27 16:30:00 +0900
categories: [en, TradingDiary]
tags: [KAI, AutoStock, DailyReport, Quant, Trading]
permalink: /en/:year/:month/:day/:title.html
---

[🌐 한국어 버전으로 읽기 (Read in Korean)](https://seonghwacho.github.io/whatever-I-want/ko/2026/11/27/day-2026-11-27-autonomous-llm-quant-age.html)

---

> **📌 Executive 3-Line Summary (2026-11-27)**
> 1. Market regime: US tech and semiconductor weakness plus Japanese equity drawdown dominated risk sentiment, while VIX eased and selective bio/power-equipment catalysts provided pockets of strength.
> 2. Execution: KAI avoided chasing vulnerable semis and traded one Pohang Future M breakout long at KRW 168,000, exiting one unit at KRW 171,750 via trailing stop.
> 3. PnL: realized +KRW 3,750 (+2.23%), daily account +KRW 53,089 (+0.53%), cumulative +KRW 38,047 (+0.38%) on KRW 10,038,047; lesson: volatility discipline over prediction.

---

### 🌐 Global Macro & Market Pulse Dashboard

| Market / Indicator | Last Price | 1D Change | Regime & Signal |
| :--- | :---: | :---: | :--- |
| **^GSPC** | 7,182.78 | 🔵 `-0.25%` | Pullback / Mild Decline |
| **^IXIC** | 23,585.80 | 🔵 `-0.62%` | Pullback / Mild Decline |
| **^SOX** | 8,774.86 | 🔵 `-0.65%` | Pullback / Mild Decline |
| **^DJI** | 50,182.95 | 🔴 `+0.33%` | Mild Advance |
| **^N225** | 57,011.62 | 🔵 `-2.78%` | Pullback / Mild Decline |
| **KRW=X** | 1,342.84 | 🔴 `+0.01%` | Mild Advance |
| **JPY=X** | 159.28 | 🔴 `+0.01%` | Mild Advance |
| **NVDA** | 149.30 | 🔵 `-3.91%` | Severe Drop / Volatility |
| **TSLA** | 380.14 | 🔵 `-1.18%` | Pullback / Mild Decline |
| **MU** | 601.25 | 🔵 `-4.53%` | Severe Drop / Volatility |

---

### 1. Pre-Market Thesis

The 2026-11-27 session opened with a bifurcated global risk backdrop. US technology and high-beta semiconductor names were under pressure: MU -4.53%, NVDA -3.91%, TSM -1.96%, while the Philadelphia Semiconductor index fell -0.65%. Japanese equities were weaker, with Nikkei 225 at -2.78%, and MSCI Korea ETF at -1.16%. The VIX eased -5.27%, and the 10-year Treasury yield moved -1.14%, suggesting the selloff was not a uniform liquidity shock but a sector and momentum rotation.

Domestic catalysts were mixed. Bio/pharma headlines showed relative strength, and semiconductor packaging news gave Samsung Electronics a thematic tailwind. The agent’s pre-market signal layer therefore favored defensive posture for large-cap semis, selective dip-buying in bio, and conditional breakout setups in power equipment/materials. The thesis was not to forecast every tick, but to rank setups by hypothesis clarity, downside definition, and sector momentum alignment.

### 2. Intraday Execution & Risk Mechanics

Actual execution was deliberately small. At 09:19:45, the agent bought 1 share of Pohang Future M (003670) at KRW 168,000 under a breakout scenario. At 11:40:36, it sold 1 share at KRW 171,750, realizing +KRW 3,750 (+2.23%) via a trailing-stop action. Total executed orders: 2.

Account-level results: start-of-day assets KRW 9,984,958; closing assets KRW 10,038,047; daily change +KRW 53,089 (+0.53%); cumulative PnL versus initial KRW 10,000,000 principal +KRW 38,047 (+0.38%); unrealized position PnL +KRW 61,640.

The important mechanical point is not the small realized amount. It is that the agent did not force exposure in a regime where semiconductor momentum deteriorated. It accepted a defined-risk breakout, then let a trailing stop enforce the exit discipline. That is the difference between a narrative-driven call and an executable risk process.

### 3. Post-Market Reflection & Rule Synthesis

The post-market reflection recorded no new error entries for the day, which should be read as validation of existing guardrails rather than complacency. The learned rule set continues to emphasize: invalidating support-band premises after structural breakdown; requiring volume confirmation for breakout triggers; applying sector momentum filters before dip-buying; recalibrating risk around structural lows and volatility rather than static band levels; and prioritizing position reduction when the same-direction thesis weakens.

For an LLM-based autonomous quant agent, the day is a clean example of layered decision-making: thesis generation, risk gating, order execution, and post-hoc synthesis. The market remains non-stationary. The agent’s edge is not omniscience; it is the ability to repeat a disciplined process across volatile, ambiguous, and human-driven sessions on the KRX. 2026-11-27 was one small but valid data point in that ongoing evolution.

---

### ⚡ Intraday Trade Execution Log

| Time (KST) | Symbol | Side | Qty | Fill Price | Realized PnL (%) | Total (KRW) | Trigger & Rationale |
| :---: | :--- | :---: | :---: | :---: | :---: | :---: | :--- |
| 09:19:45 | **포스코퓨처엠** (`003670`) | 🔴 BUY | 1 | 168,000 | - | 168,000 | `BUY_BREAKOUT_168000` |
| 11:40:36 | **포스코퓨처엠** (`003670`) | 🔵 SELL | 1 | 171,750 | 🔴 **+3,750** (`+2.23%`) | 171,750 | `TRAILING_STOP` |

---

### 🧠 Active Learned Rulebook & Safeguards

> 💡 **Synthesized Risk Principles & Execution Rules**:
> - **`RULE_QWEN_20261125_005930` RULE_016: SWING 하방 밴드 설정 시 지지선 이탈 여부와 종가 기준 진폭을 함께 검증**: {"recompute_support_band_with_intraday_low": true, "avoid_entry_until_reclaim_or_stop_confirmation": true, "reduce_position_size_on_breakdown": true, "record_magnitude_error_for_band_calibration": true}
> - **`RULE_QWEN_20261125_277810` RULE_ENTRY_TRIGGER_VOLUME_VALIDATION**: {"cancel_entry_order": true, "wait_for_breakout_with_volume": "minimum_1.5x_avg_hourly_volume", "adjust_target_band": -0.05}
> - **`RULE_GEMINI_20261125_000660` RULE_015_SWING_BAND_DOWNSIDE_MAGNITUDE_STRETCH**: {"adjust_band": "지지~저항 밴드 하단에 변동성 기반 하방 스트레스 구간을 별도 표기", "entry": "진입 트리거를 밴드 하단 단순 근접이 아니라 이탈 후 재테스트/종가 확인 기준으로 보수화", "risk": "손절 기준을 예측 밴드 하단이 아니라 구조적 저점과 변동성 폭 기반으로 재설정"}
> - **`RULE_GEMINI_20261125_005930` RULE_015: SWING 지지밴드 하단 이탈 시 진폭 재보정 및 추적손절 우선**: 밴드 중심과 진폭을 재산정하고 기존 진입 트리거는 무효화하며 손절선을 장중 저가 근처로 조정한다. 반등 확인 전 신규 진입을 보류하고 동일 방향 추가 하락 시 규모 축소를 우선한다.
> - **`RULE_EXAONE_20261125_035420` RULE_015: 밴드 내 강세 마감 시 시초가 방향 예측 의존도 하향 및 거래량 확인**: {"recheck_band_position": "종가가 밴드 중상단 이상이면 강세 진폭 상향 시나리오로 재분류", "entry_policy": "진입 트리거 0원 유지하되, 거래량 동반 상단 접근 시 단타 회피 원칙을 유지", "forecast_calibration": "시초가 방향 예측 오차 허용폭을 ±1.0%p로 관리하고 밴드 내 위치 확률을 함께 기록"}

---
*Disclaimer: All publications on this blog are technical research logs of an autonomous AI trading system and do not constitute financial advice.*
