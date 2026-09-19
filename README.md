## Thành Đạt

Quantitative researcher in Hanoi. I build tick-level research infrastructure and
test trading hypotheses against it — mostly to find out that they do not work,
which is the part I write down.

Most of what I publish is a record rather than a product: the hypothesis, the
acceptance criterion fixed before the held-out split was touched, the cost model
the result was charged against, and the verdict. Negative results stay in the
repository next to the positive ones.

### What I'm working on

**[tickbench](https://github.com/datxbt/tickbench)** — a tick-data research
platform built on 696M Exness raw-spread ticks (EURUSD, USDJPY, XAUUSD, USTEC,
2020–2026). Thirty hypotheses — price-action folklore, published papers,
machine-learned signals — implemented and priced with a cost model measured from
the same feed. One survived as a deployable strategy, one more as a forecasting
model. The other twenty-eight are written up with the null they were tested
against.

**[edge-auditor](https://github.com/datxbt/edge-auditor)** — an agentic
robustness auditor for systematic strategies. Given a configuration and the
evidence from the period it was developed on, it predicts what the strategy will
actually do out of sample, evaluated against 258 configurations whose
out-of-sample results were measured months before the project existed. Built for
the micro1 Agentic Workflows Hackathon.

**[xauusd-research-ORB](https://github.com/datxbt/xauusd-research-ORB)** — an
empirical study of intraday session-breakout structure in spot gold on raw tick
data, under a pre-registered testing protocol, with a synthetic tick generator
supplying the null control.

**[NetworkPacketSniffer](https://github.com/datxbt/NetworkPacketSniffer)** — a
Python CLI packet sniffer and traffic analyzer for Windows, with protocol
parsing, multi-format logging, and a lightweight detection engine for scans,
floods, and DNS anomalies.

### How I work

- Splits are fixed before the strategy work starts, and the test split is
  touched once, at the end.
- Every result is charged a spread, commission, and slippage measured from the
  same feed it was found in — a strategy that only works gross does not work.
- A replication is not finished until the control runs too: a synthetic null,
  a coin-flip entry on a random bar, or a reconstruction of the original
  author's numbers.
- Known regime breaks in the data are documented, because a strategy fitted
  across one is fitted to two different markets.

### Tools

Python, pandas/NumPy, Parquet + zstd for tick storage, scikit-learn, MQL5 and
the MT5 strategy tester for deployment checks.

---

Open to quantitative research work. Reach me through the email on this profile.
