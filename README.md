# AI Hedge Fund

This is a proof of concept for an AI-powered hedge fund.  The goal of this project is to explore the use of AI to make trading decisions.  This project is for **educational** purposes only and is not intended for real trading or investment.

This system employs several agents working together:

1. Aswath Damodaran Agent - The Dean of Valuation, focuses on story, numbers, and disciplined valuation
2. Ben Graham Agent - The godfather of value investing, only buys hidden gems with a margin of safety
3. Bill Ackman Agent - An activist investor, takes bold positions and pushes for change
4. Cathie Wood Agent - The queen of growth investing, believes in the power of innovation and disruption
5. Charlie Munger Agent - Warren Buffett's partner, only buys wonderful businesses at fair prices
6. Michael Burry Agent - The Big Short contrarian who hunts for deep value
7. Mohnish Pabrai Agent - The Dhandho investor, who looks for doubles at low risk
8. Nassim Taleb Agent - The Black Swan risk analyst, focuses on tail risk, antifragility, and asymmetric payoffs
9. Peter Lynch Agent - Practical investor who seeks "ten-baggers" in everyday businesses
10. Phil Fisher Agent - Meticulous growth investor who uses deep "scuttlebutt" research 
11. Rakesh Jhunjhunwala Agent - The Big Bull of India
12. Stanley Druckenmiller Agent - Macro legend who hunts for asymmetric opportunities with growth potential
13. Warren Buffett Agent - The oracle of Omaha, seeks wonderful companies at a fair price
14. Valuation Agent - Calculates the intrinsic value of a stock and generates trading signals
15. Sentiment Agent - Analyzes market sentiment and generates trading signals
16. Fundamentals Agent - Analyzes fundamental data and generates trading signals
17. Technicals Agent - Analyzes technical indicators and generates trading signals
18. Risk Manager - Calculates risk metrics and sets position limits
19. Portfolio Manager - Makes final trading decisions and generates orders

<img width="1042" alt="Screenshot 2025-03-22 at 6 19 07 PM" src="https://github.com/user-attachments/assets/cbae3dcf-b571-490d-b0ad-3f0f035ac0d4" />

Note: the system does not actually make any trades.

> **Personal note:** I'm using this project to learn how LLM agents can be composed into multi-agent workflows. My main interest is in comparing how different investor personas weight the same financial data differently. I find the Ben Graham and Nassim Taleb agents particularly interesting to compare — one focuses on margin of safety through undervaluation, the other through asymmetric risk exposure.

> **My workflow:** I typically run this against a watchlist of 5–10 tickers at a time and log the per-agent signals to a CSV so I can review disagreements between agents (e.g. when Buffett is bullish but Taleb flags tail risk). That divergence is often the most instructive part.

> **Agents I find most useful for my style:** Ben Graham, Charlie Munger, and Nassim Taleb. I tend to discount the Cathie Wood and Bill Ackman agents for my own use — their high-conviction/high-volatility style doesn't match how I think about risk. Mohnish Pabrai is an underrated one in this lineup; his Dhandho framing (heads I win, tails I don't lose much) overlaps nicely with Taleb's asymmetry focus but is more grounded in business fundamentals.
