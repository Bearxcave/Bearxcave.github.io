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



