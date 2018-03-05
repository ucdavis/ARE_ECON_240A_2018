---
title: 'Computing Assignment #6'
author: 'Group: redSloth (Tyler Hoppenfield, Daniel Mather, Iwunze Ugo)'
date: "2/28/2018"
output: beamer_presentation
---





## Heat Map
![](redsloth_184984_2977828_redSloth_ps6_files/figure-beamer/heatmap-1.pdf)<!-- --> 

## Power: Analytic solution
Note that $T_\mu \sim N(0,1)$, where $T_\mu \equiv H_0: \mu = \mu$, implies $T_0 = T_\mu + \mu \sqrt{n}$. And so,
\begin{align*}
\pi (\mu, n) &= Pr(T_0 > 1.96 | \mu, n) \\
&= Pr(T_\mu + \mu \sqrt{n} > 1.96 | \mu, n) \\
&= 1 - Pr(T_\mu < 1.96 - \mu \sqrt{n} | \mu, n) + Pr(T_\mu < -1.96 - \mu \sqrt{n} | \mu, n) \\
\pi (\mu, n) &= 1 - \Phi(1.96 - \mu \sqrt{n}) + \Phi(-1.96 - \mu \sqrt{n})
\end{align*}

## Power: Graph with fixed n
![](redsloth_184984_2977828_redSloth_ps6_files/figure-beamer/power.u-1.pdf)<!-- --> 

## Power: Graph with fixed $\mu$
![](redsloth_184984_2977828_redSloth_ps6_files/figure-beamer/power.n-1.pdf)<!-- --> 

##Power: Practical Answers

* Yes, you can expect to reject the null more than 90% of the time
* To Reject 80% of the time, you would need about 9 obserations
