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

### Introduction to No-arbitrage

Consider the following contract

* Pay price *p* at time *t*=0
* Receive $c_k$ at time *t*=*k*, *k*=1, $\cdots$, *T*

The no-arbitrage condition bounds the price *p* for this contract:

* Weak No-Arbitrage: $c_k \geq 0$ for all $k \geq 1 \Rightarrow p \geq 0$
* Strong No-Arbitrage: $c_k \geq 0$ for all $k \geq 1$ and $c_l>0$ for some $l \Rightarrow p \geq 0$

An amount *A* invested for *n* periods at a __simple__ interst rate of *r* per period is worth $A(1+n\dot r)$ at maturity.

An amount *A* invested for *n* periods at a __compound__ interst rate of *r* per period is worth $A(1+r)^n$ at maturity.

__Continuous compounding__: an amount *A* invested for *y* years is woth $\lim_{n\to \infty} A(1+r/n)^{yn}=A e^{ry}$ at maturity.
