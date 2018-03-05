---
title: "Homework6"
author: "Fledging RUCers"
date: "2018/3/1"
output: ioslides_presentation
---



## Analytical Results

\[\begin{aligned}
power&=Pr(Reject H_0|H_1)\\
&=Pr(|t|>c|\mu=\mu_0)\\
&=Pr(\frac{\overline{x}-0}{\sqrt{\frac{1}{n}}}>c|\mu=\mu_0)+Pr(\frac{\overline{x}-0}{\sqrt{\frac{1}{n}}}<-c|\mu=\mu_0)\\
&=Pr(\frac{\overline{x}-\mu_0}{\sqrt{\frac{1}{n}}}>\frac{c\sqrt{\frac{1}{n}}-\mu_0}{\sqrt{\frac{1}{n}}}|\mu=\mu_0)+Pr(\frac{\overline{x}-\mu_0}{\sqrt{\frac{1}{n}}}<\frac{-c\sqrt{\frac{1}{n}}-\mu_0}{\sqrt{\frac{1}{n}}}|\mu=\mu_0)\\
&=1-\Phi(c-\frac{\mu_0}{\sqrt{\frac{1}{n}}})+\Phi(-c-\frac{\mu_0}{\sqrt{\frac{1}{n}}})
\end{aligned}\]



## Question 1

<img src="fledglingrucers_186971_2978152_Homework6-Fledging_RUCers_files/figure-html/unnamed-chunk-1-1.png" width="720" />

##Question 2

<img src="fledglingrucers_186971_2978152_Homework6-Fledging_RUCers_files/figure-html/unnamed-chunk-2-1.png" width="720" />

##Question3

<img src="fledglingrucers_186971_2978152_Homework6-Fledging_RUCers_files/figure-html/unnamed-chunk-3-1.png" width="720" />

##Question5


```
## [1] 1
```

```
## [1] 11
```
