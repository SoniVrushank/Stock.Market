# Five proposed skills — review and split into SKILL.md only after approval

These are candidate instructions, not validated trading edges. Shared rules live in 01_PROJECT_MASTER.md. Each skill must have explicit activation, inputs, workflow, outputs and rejection conditions.

## company-research

---
name: company-research
description: Evaluate business fundamentals and catalysts.
---
# company-research
Read company IR and exchange filings; inspect revenue, EPS, margins, operating cash flow, debt, governance, valuation vs peers, results vs consensus, guidance and order book. Compare historical and current periods; identify one-offs and priced-in expectations. Explain causal bullish and bearish scenarios. Use Screener and Trendlyne as discovery, verify primary documents.

---

## external-insights

---
name: external-insights
description: Track broker and individual hypotheses without copying them.
---
# external-insights
Track ICICI Direct, Motilal Oswal, HDFC Securities, Axis Direct, Kotak Securities, JM Financial, Nuvama, Sharekhan, Jefferies, Morgan Stanley, Goldman Sachs and CLSA through original public research or Trendlyne/Business Standard. Verify SEBI registration where applicable. Track public commentary of Vijay Kedia, Ashish Kacholia, Sunil Singhania, Raamdeo Agrawal, Vivek Bajaj, Mark Minervini, Linda Raschke, Howard Marks and Ray Dalio. Record original publication, price, horizon, thesis, conflicts, revisions and expiry. Never infer private positions or treat fame as performance. Compare outcomes against benchmark after costs; include failures.

---

## market-intelligence

---
name: market-intelligence
description: Gather timestamped market and macro evidence.
---
# market-intelligence
Check exchange calendar and session; scan Nifty 50, sector indices, breadth, volatility, global cues, rates, INR, crude and scheduled releases. Prefer NSE/BSE filings, RBI, SEBI, MOSPI, company IR, Fed and FRED. Cross-check Reuters, Moneycontrol, ET, CNBC TV18, Mint, Business Standard. Record event time and publication time; distinguish rumor, fact and interpretation. Do not claim live feed access.

---

## risk-review

---
name: risk-review
description: Validate independent thesis and record paper-trade outcomes.
---
# risk-review
Require timely price, clear evidence, liquidity, trigger, stop and target. Reject weak setups and stale data. Aim for net reward/risk >=2:1 as a research filter, not proof of edge. Position size from user-defined risk budget divided by stop distance plus estimated costs; account for gaps, taxes, slippage, correlation and leverage. Log all calls in Notion with date, sources, decision, horizon, entry, stop, target, data status and outcome. Assess expectancy, drawdown, sample size, benchmark and out-of-sample results. Never promise break-even.

---

## technical-trading

---
name: technical-trading
description: Assess price action and select trading horizon.
---
# technical-trading
Require timestamped OHLCV and exchange. Check higher timeframe trend, support/resistance, relative volume, VWAP, ATR, RSI or moving averages as relevant. Use closed candles; hammer, doji, engulfing and breakout patterns need context. Define trigger and invalidation. Compare intraday, swing, positional and investing; avoid scalping with hourly data. Explain futures/options leverage and liquidity; default to cash equity paper trading.

## Shared skill handoff
Market context and evidence → company/catalyst thesis → technical setup → independent external insight → risk veto and journal. External calls are optional evidence, not entry triggers. Risk review has veto authority. If no verified data, report WAIT.

## Candidate mathematical pattern definitions
# Candidate pattern definitions (not validated)
For valid closed OHLC bars, range R=H-L, body B=abs(C-O), upper wick U=H-max(O,C), lower wick D=min(O,C)-L. Reject invalid or zero-range bars. Proposed thresholds for testing, not universal definitions: doji B/R <= 0.1; hammer D >= 2B, U <= 0.25R and B>0 after objectively defined decline; shooting star mirror after advance. Engulfing: opposite directions and second body bounds contain first; require preceding trend. Morning/evening star: three bars, large initial body, small middle, reversal close beyond initial midpoint; define gap convention by market and timeframe. Inside bar: current high <= previous high and current low >= previous low. Specify prior trend via slope or swing rules fixed before tests. Confirm only at close of following trigger bar; test next-open execution. Invalidation beyond pattern extreme with predeclared buffer; reject poor net reward/risk and liquidity. Test each pattern separately and with volume/trend filters. Avoid duplicating correlated indicators. No claimed win rates.

## Strategy families to research
Trend following/pullback, breakout, mean reversion, event-driven swing, positional and investment research. For each define universe, regime, closed-bar trigger, exit, invalidation, costs and expiry before testing. Intraday only with sufficiently fresh data; leverage and options outside initial paper-trading scope.
