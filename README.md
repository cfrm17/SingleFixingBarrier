# Single Fixing Barrier Fade Option Valuation

A Single Fixing Single Barrier Fade In Option gives a European payoff at expiry if a contractually fixed single barrier has been knocked on a specified single fixing (observation) date and gives nothing if otherwise. The “Out” version gives nothing if the barrier is knocked and a European payoff otherwise. 

Currently, the Fade Option is priced under standard Black-Scholes assumptions with at-the-money (ATM) volatility term structure. Volatility skew is not accounted for and, consequently, these theoretical prices may be different from market ones. Moreover, In/Out parity can induce internal arbitrage (Fade In plus Fade Out add up to a Vanilla that is not on volatility smile as it should).

When the fixing date coincides to expiry date the Fade option payoff (also called European Barrier Option payoff) can be exactly replicated with European Vanilla and European Digital Options. As both Vanilla and European Digital Options can be consistently priced with volatility smile, a Fade Option with fixing at expiry can consequently be priced with smile. 

Let t S be the spot FX rate of a currency pair FOREIGN/DOMESTIC (FOR/DOM, f/d) at time t. In the FOR/DOM notation scheme, when one considers, for example, the EUR/USD-spot trading, say, at 1.26 USD per 1 EUR, the currency USD is used to measure 1 EUR, therefore we say that EUR is the underlying (the asset, the foreign currency) and USD is the numeraire (the domestic currency) used to value the asset 1 EUR. Another example: consider USD/JPY-spot trading, say, at 116 JPY per 1 USD; the currency JPY is used to measure 1 USD, so USD is the underlying (the asset, the foreign currency), and JPY is the numeraire (the domestic currency).

Let T be the time (in years) from current date (valuation date) to expiry date, shortly called time to expiry. Let be the deterministic instantaneous domestic risk-free interest rate at time t, and the deterministic foreign risk-free interest rate (see https://finpricing.com/lib/FiBondCoupon.html ) at time t. Let r (t) dr (t) f σ (t) be the deterministic instantaneous volatility parameter.

The following continuous geometric Brownian process models the spot FX rate (here is the standard Brownian motion), under risk neutral measure:

 

(forward and spot FX rate relation given by interest rate parity relation) and

 

(forward volatility). These quantities come directly from quoted term structures or via standard
interpolation.

 

Where

 

Note that definitions can overlap: Up and Out Call Fade payoff is the same as Down and In Call
Fade payoff. The notional is assumed to be one unit of foreign currency (when the notional is one
unit of domestic currency the usual division by strike should be applied).

From (1) we have:

 

And

 

By standard pricing theory, under domestic risk-neutral measure, the fair current value of payoff
(2) is:

 
