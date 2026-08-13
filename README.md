Manchester United plc (NYSE: MANU)

A discounted cash flow valuation from the filings up. Twelve tabs, one question. Independent research, not investment advice.
The question
I've supported Manchester United my whole life, which means I've spent the last few years watching the club get picked apart, on the pitch and in the accounts. Somewhere in the middle of all that I noticed the share price just sitting there around $22, and nobody, not the fan channels, not the finance press, could actually tell me what was holding it up. So I built this to find out for myself. One question, stripped of all the emotion I normally watch this club with: if you ignore the badge and the history and just value the cash United generates, what is it actually worth?
What that gap actually means

The market says $22.23. My model says $4.34. The first instinct is that the model is wrong somewhere, so I spent most of my time trying to break it. Trading comps, operating comps, a sensitivity grid, a thousand Monte Carlo paths. The number held.

What I concluded is that the gap is not an error, it is a list of things a five year cash flow forecast is structurally incapable of pricing:

a 100,000 seat stadium still in development
a fanbase of roughly 1.1 billion people
a squad that is simultaneously a cost centre and a tradeable asset portfolio
the standing possibility that somebody buys the club outright at a control premium

None of those show up in free cash flow. All of them are real. A DCF is the wrong instrument for measuring them, and I think it is more honest to say that than to torture the assumptions until the model agrees with the market.

The thing I did not expect

Manchester United's equity is far more fragile than a $22 share price suggests.

Every May, one binary outcome resets the entire valuation: Champions League qualification. Miss it and three things happen at once. Broadcast revenue drops. Sponsorship contracts trigger step-down clauses that were negotiated years earlier. And the wage bill does not move at all, because player contracts are fixed regardless of which competition the club is playing in.

Revenue is variable. Costs are not. That asymmetry sits on top of £691.7m of net debt, and in my bear case it takes the equity below zero. Roughly a third of my Monte Carlo paths end in the same place.

I did not set out to find that. It fell out of modelling qualification as a probability weighted driver with a feedback loop into commercial revenue, rather than assuming a European place in perpetuity the way most published models seem to.

On the beta

I did not want to lift a beta off a website.

So I pulled two years of weekly closing prices for MANU and the S&P 500, built the return series, and ran the regression myself. Raw slope: 0.65.

That number is too low to use as is. MANU trades around 350,000 shares a day, and thin trading mechanically suppresses measured beta. I applied the standard Vasicek adjustment toward the market mean and used 0.77 instead. Every figure in the WACC build follows from that one decision, which is exactly why I wanted to make it myself rather than inherit it.

Final WACC: 9.63%.

Where the numbers land
	
DCF value	$4.34 per share
Market price	$22.23 (17 July 2026)
WACC	9.63%
Beta	0.65 regressed, 0.77 Vasicek adjusted
Bear / Base / Bull	-$1.26 / $4.34 / $6.78
Monte Carlo	1,000 runs, ~33% end in equity wipeout
How to read the model

Start at Assumptions. It is the control panel, and every blue cell is an input you can change. Move one and the whole thing recalculates.

From there the chain runs: WACC Build turns the regressed beta into the discount rate → Revenue Build projects five years with the Champions League uplift probability weighted → P&L to FCF converts revenue to cash and applies the wage feedback loop → DCF discounts it and bridges through net debt to a per share figure.

Then four tabs exist purely to attack that figure from different angles: Validation, Trading Comps, Operating Comps, Sensitivity, and Monte Carlo.

Colour convention throughout: blue is an input, black is a formula, green is pulled from another tab, yellow flags a key assumption, and a green fill means the figure is a reported actual straight from the filings.

Data and vintage

Built on Q1 through Q3 FY2026 results, the most recent being Q3 released 27 May 2026, plus full year guidance of £655m to £665m and the confirmed third place finish. Share price, exchange rate, and net debt are current as of 17 July 2026.

Audited full year accounts land around September 2026. When they do, the Quarterly Actuals tab is where the reconciliation goes, and I will update the model rather than leave a stale number in a public repository.

