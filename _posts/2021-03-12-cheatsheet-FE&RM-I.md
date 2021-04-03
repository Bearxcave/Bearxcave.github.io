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

### Introduction to Basic Fixed Income Securities & Instruments

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

### Introduction to Derivative Securities

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

#### Introduction to Term Structure Lattice Models and the Cash Account

* short-rate

* Rist-neutral pricing for a "coupon" paying security: $ \frac{Z_t}{B_t} = E_t^{\mathbb Q} \left[ \sum_{j=t+1}^{t+s} \frac{C_j}{B_j} + \frac{Z_{t+s}}{B_{t+s}}  \right]$

#### Fixed Income Derivatives

* Pricing a forward on a coupon-bearing bond: $ G_0 = \frac{E_0^{\mathbb Q} [S_n /B_n]}{ E_0^{\mathbb Q} [1 /B_n] } $

* Pricing future contract: $ F_0 = E_0^{\mathbb Q}  [S_n] $

* Caplet and floorlet: The payoff at time *t* are $ (r_{t-1} - c)^+ $ and $ (c- r_{t-1})^+ $ respectively. \
$Rightarrow$ Swaps & swaption.

* Forward equation: My naive understanding is to switch the calculation direction.

### Supplement material

* Conditional expectations and variances \
$E[X] = E[E[X|Y]]$ \
$Var(X) = Var(E[X|Y]) + E(Var(X|Y))$

* Martingale betting strategy \
