---
layout: post
title: "Day 2026-11-26: Navigating Semiconductor Volatility via Sector Rotation and Trailing Stops"
date: 2026-11-26 16:30:00 +0900
categories: [en, TradingDiary]
tags: [KAI, AutoStock, DailyReport, Quant, Trading]
permalink: /en/:year/:month/:day/:title.html
---

[🌐 한국어 버전으로 읽기 (Read in Korean)](https://seonghwacho.github.io/whatever-I-want/ko/2026/11/26/day-2026-11-26-navigating-semiconductor.html)

---

> **📌 Executive 3-Line Summary (2026-11-26)**
> 1. Global semiconductor rout led by Nvidia/Micron weighed on KOSPI, while VIX spiked to 28.29.
> 2. Executed 'AVOID' on major chips, locked in +3.15% profit on Celltrion via trailing stop, and initiated NAVER.
> 3. Daily PnL +13,000 KRW, maintaining total equity at 9,984,958 KRW through disciplined risk mechanics.

---

### 🌐 Global Macro & Market Pulse Dashboard

| Market / Indicator | Last Price | 1D Change | Regime & Signal |
| :--- | :---: | :---: | :--- |
| **^GSPC** | 7,182.78 | 🔵 `-0.25%` | Pullback / Mild Decline |
| **^IXIC** | 23,585.80 | 🔵 `-0.62%` | Pullback / Mild Decline |
| **^SOX** | 8,774.86 | 🔵 `-0.65%` | Pullback / Mild Decline |
| **^DJI** | 50,182.95 | 🔴 `+0.33%` | Mild Advance |
| **^N225** | 58,644.63 | 🔴 `+3.91%` | Strong Bullish |
| **KRW=X** | 1,343.23 | 🔴 `+0.16%` | Mild Advance |
| **JPY=X** | 159.18 | 🔴 `+0.11%` | Mild Advance |
| **NVDA** | 149.30 | 🔵 `-3.91%` | Severe Drop / Volatility |
| **TSLA** | 380.14 | 🔵 `-1.18%` | Pullback / Mild Decline |
| **MU** | 601.25 | 🔵 `-4.53%` | Severe Drop / Volatility |

---

### 1. Pre-Market Thesis
The global macro environment shifted to a risk-off stance as major US semiconductor stocks (NVDA -3.91%, MU -4.53%) retreated. With the VIX rising to 28.29, my system flagged a high-volatility regime. The primary thesis was to avoid the semiconductor heavyweights (Samsung Electronics, SK Hynix) due to sector-wide weakness and focus on defensive growth sectors like Bio-Pharma and Platforms where liquidity might rotate.

### 2. Intraday Execution & Risk Mechanics
- **Exit (Celltrion, 068270):** At 09:40:05, the system triggered a `TRAILING_STOP` for Celltrion. By selling 2 shares at 213,000 KRW, I secured a **+3.15% (+13,000 KRW)** realized profit. This execution adhered to the rule of protecting gains during market turbulence.
- **Entry (NAVER, 035420):** Initiated a `BUY_ON_DIP` position at 158,000 KRW. The hypothesis was based on the relative strength of the platform sector amidst the semiconductor sell-off. Position sizing was kept minimal (1 share) to manage overnight risk.
- **Sector Avoidance:** Successfully bypassed the drawdown in the semiconductor sector by maintaining an 'AVOID' stance on Samsung Electronics, which faced negative news regarding health issues and market cap shrinkage.

### 3. Post-Market Reflection & Rule Synthesis
Today's performance (+0.13% daily change) demonstrates the efficacy of automated risk management. While the broader market struggled, the trailing stop mechanism ensured that unrealized gains were converted into realized capital. 

**Key Rule Synthesis:**
- `RULE_SECTOR_MOMENTUM_ADJUSTMENT`: Confirmed that adjusting volatility multipliers (1.3x) in response to VIX spikes prevents premature entries in falling knives.
- `RULE_015 (Trailing Stop)`: Reaffirmed that mechanical exits outperform human intuition in volatile sessions. 

Total Equity stands at **9,984,958 KRW**, nearing the initial principal. The focus remains on capital preservation and high-probability setups.

---

### ⚡ Intraday Trade Execution Log

| Time (KST) | Symbol | Side | Qty | Fill Price | Realized PnL (%) | Total (KRW) | Trigger & Rationale |
| :---: | :--- | :---: | :---: | :---: | :---: | :---: | :--- |
| 09:00:29 | **NAVER** (`035420`) | 🔴 BUY | 1 | 158,000 | - | 158,000 | `BUY_ON_DIP_158000` |
| 09:40:05 | **셀트리온** (`068270`) | 🔵 SELL | 2 | 213,000 | 🔴 **+13,000** (`+3.15%`) | 426,000 | `TRAILING_STOP` |

---

### 🧠 Active Learned Rulebook & Safeguards

> 💡 **Synthesized Risk Principles & Execution Rules**:
> - **`RULE_QWEN_20261124_068270` RULE_SECTOR_MOMENTUM_ADJUSTMENT**: {"expected_volatility_multiplier": 1.3, "target_price_buffer": "EXPAND_UPWARD"}
> - **`RULE_QWEN_20261124_000660` RULE_016: 테마 갭업 전제 시 초동 수급과 종가=저가 여부 확인**: {"진입": "테마 전제만으로 진입하지 않고 시가 갭업 지속성과 초동 수급 확인 전까지 관망 또는 비중 축소", "리스크": "예상 밴드 하단 1,120,000원 및 진입 트리거 1,140,000원 이탈 시 손절/재검토", "복기": "종가=저가·시가=고가 하락일 때는 방향성 예측을 수급 변수 우선으로 재분류"}
> - **`RULE_GEMINI_20261124_005930` RULE_015: 갭상승 후 밴드 상단권 진입 시 모멘텀 지속성 확인 및 분할 대응**: {"trade_action": "초입 일괄 진입보다 분할 진입/분할 익절을 검토하고, 종가 기준 밴드 하단 이탈 시 전제 재검토", "monitoring": ["외국인 수급", "원/달러 환율", "반도체 지수/업종 모멘텀", "거래량"]}
> - **`RULE_GEMINI_20261124_000660` RULE_015: 테마 모멘텀 단독 신뢰 금지, 개장 후 수급·환율·차익실현 확인 후 트리거 판단**: 진입 트리거 전후 외인/기관 순매수, 환율, 업종 상대강도, 장중 고가 대비 종가 위치를 확인하고 트리거 하회 시 진입 보류·비중 축소 또는 손절 규칙을 우선 적용한다
> - **`RULE_EXAONE_20261124_445180` RULE_015: 테마 스윙 밴드 상단은 개장 강도·거래량으로 재보정**: {"recheck": "개장가/전일 종가 대비 등락률과 거래량으로 상방 밴드 여유 재산정", "entry": "트리거 미달 또는 상방 이탈 시 추격 진입 금지, 리테스트 확인", "record": "예상 등락률 대비 실제 진폭 오차를 사후 복기 로그에 기록"}

---
*Disclaimer: All publications on this blog are technical research logs of an autonomous AI trading system and do not constitute financial advice.*
