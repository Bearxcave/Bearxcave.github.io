---
layout:     post
title:      Financial Engineering and Risk Management
date:       2021-03-12
author:     Bearx
header-img: img/post-bg-grand-canyon.jpg
catalog: true
tags:
    - note
    - financial engineering
    - risk management
---
 
### Basic Fixed Income Securities & Instruments

#### Basics of Fixed Income Securities

The no-arbitrage condition bounds the price *p* for this contract:

* Weak No-Arbitrage: $c_k \geq 0$ for all $k \geq 1 \Rightarrow p \geq 0$
* Strong No-Arbitrage: $c_k \geq 0$ for all $k \geq 1$ and $c_l>0$ for some $l \Rightarrow p \geq 0$

An amount *A* invested for *n* periods at a __simple__ interst rate of *r* per period is worth $A(1+n\dot r)$ at maturity.

An amount *A* invested for *n* periods at a __compound__ interst rate of *r* per period is worth $A(1+r)^n$ at maturity.

__Continuous compounding__: an amount *A* invested for *y* years is worth $\lim_{n\to \infty} A(1+r/n)^{yn}=A e^{ry}$ at maturity.

__Present value__: $PV(\mathbf{c}; r) = \sum_{k=0}^N \frac{c_k}{(1+r)^k}$

Can Lend at rate $r_L$ and borrow rate at rate $r_B$: $r_L < r_B$? Bounds on the price $PV(\mathbf{c}; r_B) \geq p \geq PV(\mathbf{c}; r_L)$. Therefore, supply and demand set the price.

__Fixed income securities__:

* Default risk
* Inflation risk
* Market risk

#### Basic Fixed Income Instruments

Linear pricing theorem

Discount rate, spot rate, forward rate

__Forward contract__

### Derivative Securities

#### Swaps & Futures

__Swaps__: contracts that transform one kind of cash flow into another.

__Futures__: 

Pros:
* High leverage: high profit
* Very liquid
* Can be written on a wide variety of underlying assets

Cons:
* High leverage: high risk
* Futures prices are approximately linear function of the underlying - only linear payoffs can be hedged
* May not be flexible enough; back to Forwards!

Minimum variance hedging

#### Options and Options Pricing

The St Petersberg Paradox

Utility function

#### The 1-Period Binomial Model

Derivative security pricing:
* Can use repolicating portfolio argument to find price, $C_0$, of any derivative security with payoff function, $C_1(S_1)$ ($C_u$ for up-move and $C_d$ for down-more), at time *t=1*.
* Set up replicating portfolio as \
$u S_0 x + Ry = C_u$ \
$d S_0 x + Ry = C_d$
* Solve for *x* and *y* as before and then must have $C_0 = x S_0 + y$.

Risk-neutral probabilities & risk-neutral pricing

### Option Pricing in the Multi-Period Binomial Model

#### The Multi-Period Binomial Model

* no arbitrage <=> *d* < *R* < *u*
* anay derivative security with time *T* payoff, $C_T$, can be priced using $C_0 = \frac{1}{R^n} \mathrm{E}^{\mathbb{Q}}_0 [C_T]$

#### Pricing American Options and Replicating Strategies

#### Dividends, Pricing in the Binomial Model, and the Black-Scholes Model

* Risk-neutral pricing of European call with *K*=0: $S_0 = \mathrm{E}^{\mathbb{Q}}_0 [S_n R^{-n}] $
* Including dividend, $D_i$: $S_0 = \mathrm{E}^{\mathbb{Q}}_0 [S_n R^{-n} + \sum_{i=1}^n D_i R^{-i} ] $


### Term Structure Models

#### Term Structure Lattice Models and the Cash Account

* short-rate

* Rist-neutral pricing for a "coupon" paying security: $ \frac{Z_t}{B_t} = E_t^{\mathbb Q} \left[ \sum_{j=t+1}^{t+s} \frac{C_j}{B_j} + \frac{Z_{t+s}}{B_{t+s}}  \right]$

#### Fixed Income Derivatives

* Pricing a forward on a coupon-bearing bond: $ G_0 = \frac{E_0^{\mathbb Q} [S_n /B_n]}{ E_0^{\mathbb Q} [1 /B_n] } $

* Pricing future contract: $ F_0 = E_0^{\mathbb Q}  [S_n] $

* Caplet and floorlet: The payoff at time *t* are $ (r_{t-1} - c)^+ $ and $ (c- r_{t-1})^+ $ respectively. \
$\Rightarrow$ Swaps & swaption.

* Forward equation: My naive understanding is to switch the calculation direction.

#### Model Calibration

* Ho-Lee model: $r_{i,j} = a_i + b_i j$
* Black-Derman-Toy: $r_{i,j} = a_i e^{b_i j}$, where $\log(a_i)$ and $b_i$ are the drift and volatility parameter for $\log(r)$ respectively.

* Calibration problem: $\mathrm{min} = \sum_i \omega_i [P_i(\text{model})-P_i(\text{market})]^2 + \lambda \text{ abs}( \mathbf \theta - \mathbf \theta_{\text{prev}} )^2 $

#### Defaultable Bonds

Characterized by
* Coupon *c*
* Face value *F*
* Recovery value *R* = random fraction of face value recovered on default

ZCB with recovery: $\bar Z^T_{i,j,0} = \frac{1}{1+r_{ij}} [q_u (1-h_{ij}) \bar Z^T_{i+1,j+1,0} + q_d (1-h_{ij}) \bar Z^T_{i+1,j,0} + q_u h_{ij} R + q_d h_{ij} R] $

* State-independent hazard rates: assume that $h_{ij}=h_i$.
* Let $q(t)$ be risk-neutral probability that the bond survives until date *t*, so that $q(t+1) = (1-h_t) q(t) = \prod (1-h_k)$
* Let $I(t)$ be 1 if the bond is not in default at time *t*, and 0 otherwise.
* $\Rightarrow \mathbb E_0^Q [I(t)] = q(t)$

Price of defaultable fixed coupon bond is: $\bar P(0) = \sum c q(t_k) d(0, t_k) + F q(t_n) d(0,t_n) + RF \sum [q(t_{k-1}) - q(t_k)] d(0,t_k)$

#### Credit Default Swipes

* *N*: notional principal amount of credit protectino
* Accrued interest: interest accumulated from last coupon to default
* *S*: coupon or spread
* CDS seller has to compensate the buyer (1-*R*)*N* on default

Assumption: Default event uniformly distributied over the premium interval $\delta$

* Par spread: $S_\text{par} = \frac{(1-R) \sum [q(t_{k-1}) - q(t_k)] d(0,t_k)}{\frac{\delta}{2} \sum [q(t_{k-1}) + q(t_k)] d(0,t_k) }$
* Suppose $q(t_k)\approx (1-h) q(t_{k-1})$: $S_\text{par} = \frac{(1-R)h}{1-h/2}$

### Mortgage Mathematics and Mortgage-Backed Securities

Mortgage-backed secrities (MBSs) are a particular class of asset-backed securities (ABS). The underlying pools of securities can be mortgages, auto-loans, credit-card receivables, student loans etc.
* Securitization: the process by which ABS are created.

Types of mortgages:
* level-payment mortgage
* adjustable-rate mortgage (ARM)
* balloon mortgages

Basics for a standard level-payment mortgage:
* Initial mortgage principal: $M_0 = M$
* Assume equal periodic payments of size *B* dollars
* The coupon rate per period: *c*
* There are a total of repayment periods: *n*
* After the *n* payments, the mortgage is fully __amortizing__
* Mortgage principal remaining after the *k*th period: $M_k=(1+c)M_{k-1}-B$, with $M_n=0$
* $\Rightarrow M_k = M_0 \frac{(1+c)^n-(1+c)^k}{(1+c)^n-1}$

#### Prepayment Risks and Pass-Throughs

#### Principal-Only and Interest Only Mortgage-Backed Securities

#### CMOs and Pricing Mortgage-Backed Securities

### Supplement material

* Conditional expectations and variances \
$E[X] = E[E[X|Y]]$ \
$Var(X) = Var(E[X|Y]) + E(Var(X|Y))$

* Martingale betting strategy
