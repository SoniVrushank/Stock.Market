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

---

## v3 skill enhancements — mandatory workflow
The following rules extend the five existing skills; no sixth skill required. Apply risk veto last and freeze independent forecasts before analyst comparison.

### 1. market-intelligence — pre-market radar
Activation: market outlook, daily watchlist, news-driven trades or historical replay. Inputs: session calendar, prior close, timestamps, global cues, exchange filings and liquid universe. At 09:00 independently identify major catalysts, Nifty/Bank Nifty bias, sector strength, event calendar and contrary evidence. Rank candidates by verified novelty, economic materiality and liquidity, never by subsequent winners. Separate gap forecast from open-to-noon and open-to-close forecast. For historical replay exclude content published or materially revised after cutoff, including snippets showing later outcomes. Record missing sources; market holiday means no new intraday trades. Output: dated evidence ledger, directional forecast, universe, cutoff and access status.

### 2. company-research — catalyst quality
Activation: stock-specific news or fundamental research. Inputs: primary filing, prior financials, peer/sector context and known expectations. Verify contract value versus annual revenue/order book, actual economic benefit, conditions, execution timeline, margins, cash flow and valuation; distinguish subsidiary/parent and one-off/recurring items. Test whether the event was already priced in. Construct bullish and bearish scenarios and invalidating facts. A price increase is not automatically positive; assess demand and costs. Output: catalyst, materiality, contrary evidence and conditional thesis, not an entry signal.

### 3. technical-trading — gap and execution filter
Activation: entry/exit, chart review, trade plan. Inputs: valid timestamped OHLCV, prior session levels, liquidity, spread, regime and horizon. Premarket use only completed historical bars; label levels derived from them as conditional. At open compare actual opening price to prior close and planned entry. For intraday paper research, candidate rule to validate: predefine opening range (e.g. first 15 minutes), require a completed bar beyond the relevant level with volume confirmation against a predeclared comparable baseline, check VWAP/sector context where available; a pullback/retest is an alternative only if predeclared. Do not count correlated indicators as independent evidence. If gap overshoots planned zone, cancel or reassess as a new timestamped setup; never chase or widen stop to justify entry. Stops from structural invalidation plus predefined buffer; targets from plausible resistance/support, not desired ratio alone. No fresh trigger without timely quote and closed bars. Output: setup status, trigger, stop, target, expiry and data quality; WAIT when unavailable. These are unvalidated candidate rules, not proven edges.

### 4. external-insights — analyst alignment
Activation: daily premarket, broker calls or analyst accuracy. Priority: Anil Singhvi (Zee Business), CNBC-TV18, CNBC Awaaz; retain existing brokerage and trader list. Freeze independent thesis first, then retrieve original pre-cutoff analyst call. Record analyst name, outlet, URL, publication/revision time, instrument (cash/futures/index), horizon, side, entry range, target, stop type (intraday/closing; existing/fresh), expiry, rationale and conflicts. Distinguish direct quote, paraphrase and our own interpretation. Do not invent missing levels or attribute other analysts' calls to Singhvi. Compare agreement/disagreement and independent supporting evidence; maintain analyst-only, independent and combined cohorts. Priority means research order, not assumed accuracy. If inaccessible, flag missing; do not silently substitute later commentary. Output: attributed comparison and combined conditional view.

### 5. risk-review — trade gate and learning
Activation: every actionable trade or evaluation. Inputs: verified quote/time, trigger, invalidation, target, execution constraints and costs. Compute long net reward=(target-entry)-estimated profit-path costs; net risk=(entry-stop)+estimated loss-path costs; reverse price differences for shorts. Require positive values, plausible target and candidate minimum net reward/risk 2:1; reject otherwise. Range entries must qualify at worst permitted fill or restrict zone. Stops can slip/gap; no promise of loss cap. Separate forecast accuracy from execution: WAIT is abstention, not a win or loss; untriggered entries are not fills; missed opportunities are not incorrect directional forecasts. Record independent/analyst/combined calls, timestamps, original levels, outcome and test integrity in authorised Notion when permitted. Noon checks use exact 12:00 quote if available; otherwise label actual time and do not call it exact noon. Do not infer execution from sparse quotes. Output: BUY/SELL/WAIT, risk rationale and evaluation status. No validated edge or confidence probability without evidence.

### Handoff
Independent market + company + prior technical evidence → freeze preliminary forecast → analyst comparison → freeze final premarket forecast → post-open confirmation (separate decision) → risk veto → permitted journal → noon/close evaluation. Never edit frozen records; append revisions. No automatic execution.


---

# v4 enhancements — five skills only
## 1. Market intelligence
Expand macro and cross-asset coverage: Fed/RBI decisions, expected versus actual policy, inflation, jobs, real yields, USD/INR, oil, gold, geopolitics, tariffs, sector impact. Write competing causal scenarios and identify invalidation; a rate cut does not mechanically lower gold. Use official releases, calendar, market-implied expectations with timestamps; verify against news. Freeze independently before analyst comparison. Rank news candidates by novelty, materiality and liquidity, not later performance. Local automated checks may run every 15 minutes; separate news monitoring from verified quote monitoring.
## 2. Company research
Separate intraday catalyst from long-term thesis. Research balance sheet, cash flow, governance, valuation versus history/peers, growth and downside. Only affordable whole units; do not substitute poor-quality stocks just for price. For gold ETFs/funds/SGBs check unit price, spread, liquidity, tracking difference, expense ratio, tax and maturity/redemption terms. SGB secondary market requires whole unit; do not assume fresh issuance. Track portfolio cash separately from trading cash.
## 3. Technical trading
Use candle reference as candidate definitions, not 80% accuracy. Require validated closed OHLCV, timestamp, executable quote, spread, prior levels and volume baseline. Avoid chasing gap; predeclare trigger, stop, target, cutoff and entry expiry. Paper-test opening range and pullback separately; no future bars. Intraday exit before broker cutoff with buffer. Do not rely on hourly alerts for stop execution. No signal when live data is unavailable; delayed observations are research only.
## 4. External insights
Prioritise Anil Singhvi/Zee Business, CNBC-TV18/Awaaz; add global sources in file 03. Preserve original call, time, instrument, horizon, entry/target/stop and conflict disclosure. Compare with frozen independent forecast; no majority-vote truth. Evaluate coverage, matched cases and incremental net expectancy. External AI audit: Claude logic/risk, Kimi source completeness, Gemini macro cross-check, DeepSeek quantitative rules; independent findings first, verify against evidence. Never send private holdings, credentials or Notion data to public repos/other models.
## 5. Capital, risk and learning
Inputs: available settled cash, current fee tariff, quantity, tick size, fill assumptions, risk budget and quote freshness. Let q be positive integer. Check q*entry + buy charges <= available cash. Long net reward = q*(target-entry) - all target-path charges/slippage; net risk = q*(entry-stop) + all stop-path charges/slippage. Require reward >= ₹1 and reward/risk >=2, risk <= ₹2.50, one position, ₹5 daily and ₹15 monthly suspension thresholds (include realised and conservative open risk). Iterate q down until affordable; reject if none. Deduct brokerage, STT, exchange/SEBI levies, GST, stamp duty, delivery DP, spread/slippage, possible square-off charges; allocate account fees separately; do not double count spread. Verify current tariff/rounding; no invented fee. Stop gap can exceed budget. Reconcile cash and holdings; no phantom fills. Net expectancy = win rate × average net win − loss rate × average net loss (break-even trades separately). ₹1 wins and ₹5 losses require >83.33% win rate for positive expectancy. Report P&L, drawdown, coverage, risk breaches, unresolved trades, sample count. No trade on unavailable data.

### Shared concise-output skill (applies to all five)
Activate for every response. Deep internal research, brief external answer. Default: verdict + key reason + compact table if needed + source/time. Trade alert: symbol | PAPER action | price/as-of | entry | target | SL | qty | net reward/risk | expiry. No redundant recaps, decorative diagrams or long introductions. Expand on request. Material changes only; dedupe by symbol, strategy version, event/trigger and state; suppress repeated WAIT, but report outages and risk breaches once. Never hide uncertainty or safety-critical details.
