---
layout: post
title: "2026-11-25 Autonomous LLM Quant Agent Log: KRX Risk-Off, Stop-Loss Execution, and Rule-Governed Position Management"
date: 2026-11-25 16:30:00 +0900
categories: [en, TradingDiary]
tags: [KAI, AutoStock, DailyReport, Quant, Trading]
permalink: /en/:year/:month/:day/:title.html
---

[🌐 한국어 버전으로 읽기 (Read in Korean)](https://seonghwacho.github.io/whatever-I-want/ko/2026/11/25/2026-11-25-autonomous-llm-quant-agent-lo.html)

---

> **📌 Executive 3-Line Summary (2026-11-25)**
> 1. Risk-off regime: Nikkei -5.06%, SOX -7.88%, Micron -11.01%, NVDA -5.86%, MSCI Korea ETF -3.70%; VIX 26.36.
> 2. Execution: 13 fills; Samsung and POSCO Future M stopped out, KB Financial exited 3 shares at KRW 148,050 for +KRW 750 each, while Celltrion 2 and Purit 68 were added.
> 3. Daily PnL: realized -KRW 31,050; total assets KRW 9,971,958, daily -0.31%, cumulative -KRW 28,042 (-0.28%) vs KRW 10,000,000; lesson: confirm price/volume/liquidity before narrative-driven entries.

---

### 🌐 Global Macro & Market Pulse Dashboard

| Market / Indicator | Last Price | 1D Change | Regime & Signal |
| :--- | :---: | :---: | :--- |
| **^GSPC** | 7,201.09 | 🔵 `-0.50%` | Pullback / Mild Decline |
| **^IXIC** | 23,733.54 | 🔵 `-1.48%` | Pullback / Mild Decline |
| **^SOX** | 8,832.50 | 🔵 `-7.88%` | Severe Drop / Volatility |
| **^DJI** | 50,018.70 | 🔴 `+0.85%` | Mild Advance |
| **^N225** | 56,436.65 | 🔵 `-5.06%` | Severe Drop / Volatility |
| **KRW=X** | 1,340.46 | 🔵 `-0.29%` | Pullback / Mild Decline |
| **JPY=X** | 159.24 | 🔴 `+0.20%` | Mild Advance |
| **NVDA** | 155.38 | 🔵 `-5.86%` | Severe Drop / Volatility |
| **TSLA** | 384.68 | 🔵 `-0.20%` | Pullback / Mild Decline |
| **MU** | 629.79 | 🔵 `-11.01%` | Severe Drop / Volatility |

---

# 2026-11-25 Autonomous LLM Quant Agent DevLog: KRX Risk-Off, Stop Execution, and Rule-Governed Position Management

## 1. Pre-Market Thesis

The 2026-11-25 session formed a conflicted risk-off regime. Positive or stable prints included Dow Jones +0.85%, WTI +1.82%, and VIX at 26.36 (-0.98%). However, technology and semiconductor risk was dominant: Nikkei 225 -5.06%, Philadelphia Semiconductor Index -7.88%, Micron -11.01%, NVIDIA -5.86%, TSMC -3.96%, and MSCI Korea ETF -3.70%. USD/KRW was 1,340.46 (-0.29%), while JPY/USD was 159.24 (+0.20%).

News catalysts were mixed: finalized corporate value-up guidelines with disclosure starting on the 27th, K-bio technology-export expectations from big-pharma patent cliffs, humanoid robot component localization, and HBM4 competition narratives. The agent's pre-market signal layer contained conditional BUY_ON_DIP, HOLD, and AVOID signals across large-cap semis, autos, financials, battery materials, bio, and day-trading names. The dominant risk-control posture was confirmation-first: band-edge support, price and volume validation, foreign and institutional flow, FX, and sector relative strength.

## 2. Intraday Execution and Risk Mechanics

The order log recorded 13 fills. Initial buys included Celltrion 2 shares at KRW 212,000 and POSCO Future M 1 share at KRW 165,200. Samsung Electronics was sold 1 share at KRW 178,500 for a realized loss of KRW 14,700 (-7.61%) under stop-loss logic, then 2 shares were bought at KRW 178,500. Those 2 shares were later sold at KRW 170,900 for KRW 15,200 (-4.26%) realized loss. POSCO Future M was stopped out at KRW 161,800 for KRW 3,400 (-2.06%).

KB Financial was purchased in three tranches at KRW 148,500, KRW 147,300, and KRW 146,100, then fully exited at KRW 148,050 via forced close, with each reported exit at +KRW 750 (+0.51%). Total realized PnL was -KRW 31,050. Closing account value was KRW 9,971,958 versus KRW 10,003,008 at the open, a daily change of -KRW 31,050 (-0.31%). Cumulative PnL versus the KRW 10,000,000 initial principal was -KRW 28,042 (-0.28%). Current unrealized position PnL was recorded as +KRW 0.

## 3. Post-Market Reflection and Rule Synthesis

No new error label was logged for the session, but the rule layer remains central to the agent design. The learned survival rules emphasize: do not infer opening direction from a single touch inside a band; require close, gap position, and volume confirmation; do not promote systematic-risk gap-down forecasts into entry triggers before price and volume evidence; and do not trust narrative-driven oversold entries before checking liquidity, FX, sector momentum, and flow. The session's stop-loss and forced-exit events illustrate the difference between narrative conviction and executable risk control. For an autonomous LLM-assisted quant workflow, the key lesson is that conviction must be conditional, falsifiable, and bounded by pre-defined loss limits.

---

### ⚡ Intraday Trade Execution Log

| Time (KST) | Symbol | Side | Qty | Fill Price | Realized PnL (%) | Total (KRW) | Trigger & Rationale |
| :---: | :--- | :---: | :---: | :---: | :---: | :---: | :--- |
| 09:00:11 | **셀트리온** (`068270`) | 🔴 BUY | 2 | 212,000 | - | 424,000 | `BUY_BREAKOUT_212000` |
| 09:00:14 | **포스코퓨처엠** (`003670`) | 🔴 BUY | 1 | 165,200 | - | 165,200 | `BUY_ON_DIP_165200` |
| 09:00:21 | **삼성전자** (`005930`) | 🔵 SELL | 1 | 178,500 | 🔵 **-14,700** (`-7.61%`) | 178,500 | `STOP_LOSS` |
| 09:00:23 | **삼성전자** (`005930`) | 🔴 BUY | 2 | 178,500 | - | 357,000 | `BUY_ON_DIP_178500` |
| 09:22:31 | **퓨릿** (`445180`) | 🔴 BUY | 68 | 6,720 | - | 456,960 | `BUY_ON_DIP_6720` |
| 10:14:14 | **KB금융** (`105560`) | 🔴 BUY | 1 | 148,500 | - | 148,500 | `BUY_ON_DIP_148500` |
| 10:44:32 | **KB금융** (`105560`) | 🔴 BUY | 1 | 147,300 | - | 147,300 | `BUY_ON_DIP_147300` |
| 11:04:50 | **KB금융** (`105560`) | 🔴 BUY | 1 | 146,100 | - | 146,100 | `BUY_ON_DIP_146100` |
| 12:03:06 | **삼성전자** (`005930`) | 🔵 SELL | 2 | 170,900 | 🔵 **-15,200** (`-4.26%`) | 341,800 | `STOP_LOSS` |
| 14:49:34 | **포스코퓨처엠** (`003670`) | 🔵 SELL | 1 | 161,800 | 🔵 **-3,400** (`-2.06%`) | 161,800 | `STOP_LOSS` |
| 15:15:00 | **KB금융** (`105560`) | 🔵 SELL | 1 | 148,050 | 🔴 **+750** (`+0.51%`) | 148,050 | `FORCE_EXIT_CLOSE` |
| 15:15:02 | **KB금융** (`105560`) | 🔵 SELL | 1 | 148,050 | 🔴 **+750** (`+0.51%`) | 148,050 | `FORCE_EXIT_CLOSE` |
| 15:15:03 | **KB금융** (`105560`) | 🔵 SELL | 1 | 148,050 | 🔴 **+750** (`+0.51%`) | 148,050 | `FORCE_EXIT_CLOSE` |

---

### 🧠 Active Learned Rulebook & Safeguards

> 💡 **Synthesized Risk Principles & Execution Rules**:
> - **`RULE_QWEN_20261123_034020` RULE_015: DAY_TRADING 시초가 약세 예상은 밴드 내 보합~약강세 개장 시 노이즈로 간주하되 트리거 터치 후 종가 확인**: {"error_label": "NOISE", "review_entry_trigger": "38,600원 터치만으로 방향 확정하지 말고 종가와 수급 확인", "adjust_forecast": "시초가 등락률 단일 추정보다 밴드 내 보합 개장 시나리오를 병행", "next_day_check": "원전/SMR 수주 관련 공시·뉴스 플로우와 외인/기관 수급 확인"}
> - **`RULE_QWEN_20261123_000660` RULE_015: 방향성 전제는 밴드 내 종가만으로 채택하지 말고 시초 갭·종가 위치·거래량 확인 필수**: 해당 방향성 가설을 당일 트레이딩 신호에서 제외하고 관망
> - **`RULE_QWEN_20261123_005930` RULE_016: 시스템틱 리스크 기반 갭하락 예측은 가격·거래량 확인 전 진입 근거로 사용 금지**: ['실제 시초 갭이 예측의 50% 미만이면 해당 예측은 무효 처리하고 진입 트리거 사용을 보류한다', '지지~저항 밴드 이탈 여부와 거래량을 확인할 때까지 신규 진입 비중을 축소한다', '시스템틱 리스크 가설은 가격 붕괴와 거래량 급증이 동반될 때만 유효 가설로 승격한다']
> - **`RULE_GEMINI_20261123_034020` RULE_017: 가격 밴드·트리거 스케일 정합성 및 방향 전제 검증**: 해당 예측을 PREMISE_BROKEN으로 폐기하고 직전종가·호가·ATR 기준으로 밴드와 트리거를 재검증하며, 입력 오류면 수정 후 재계산한다
> - **`RULE_GEMINI_20261123_000660` RULE_016: 서사 기반 낙폭 과대 진입 전 수급·매크로 확인**: 예측 밴드와 트리거를 그대로 신뢰하지 말고 진입 보류 또는 비중 축소

---
*Disclaimer: All publications on this blog are technical research logs of an autonomous AI trading system and do not constitute financial advice.*
