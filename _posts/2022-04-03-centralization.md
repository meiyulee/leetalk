---
title: 什麼是母體集中趨勢？
description: 母體所有的元素(或稱數字)可產生集中趨勢，那麼什麼叫做集中趨勢呢？集中趨勢的代表數字會受到哪些因素影響？對我們後續做統計分析時又會有什麼影響？且看內文與你分享的觀點。
author: 李玫郁
date: 2022-04-03
categories:
 - 統計觀念
tags: [圖解觀念, 敘述統計]
image: https://raw.githubusercontent.com/meiyulee/pic001/master/stat/T_centralization.jpg
layout: post
---

# 1. 前言

想了解數據的大概可以採用數據歸納方法，即敘述統計中的係數計算，了解母體或一組數據集的粗略狀態。其中的平均數系列可謂是數據的集中趨勢代表。我們因為取得數據會用敘述統計了解數據大概，但同樣地，母體也有集中趨勢，此時我們得將母體內的所有元素都拿出來看，用於知計算母體集中趨勢。

母體集中趨勢的影響在於如果數據來自母體且母體未知時，我們使用統計分析了解母體集中趨勢就須讓樣本保持相同的集中趨勢。

![](https://raw.githubusercontent.com/meiyulee/pic001/master/stat/T_centralization.jpg)

# 2. 什麼是集中趨勢？

所謂集中趨勢是指我們想**用一個數字**代表母體或一個數據集所有數字的現象。如果我們看的是母體，稱為母體集中趨勢；如果我們看的是樣本，稱為樣本集中趨勢。

這個數據還需要和母體或一個數據集的所有數字產生誤差最小。通常使用「最小平方法」計算。這也是點估計量效率特性的表現方式。

讓我們用迴歸方程式或者是你可以想像這是個代號的恆等式來看集中趨勢。令$X$為母體中的元素，$\mu$ 為母體的集中趨勢。我們以 $X= \mu - \varepsilon$ 表示。

## 2.1. 最小平方法

最小平方法是指 $E(\varepsilon^{2})$ 最小。所以令 $\varepsilon =X-k$，設

$$
L(k)=E(\varepsilon^{2})=E \left[ \left(X-k \right)^{2} \right]
$$

經過一次微分後得到

$$ \begin{align*}
L'(k) &=-2E(X-k)=0,  \\
E(X) &=k, \\
L''(k) &=2 
\end{align*}
$$

將 $\mu$ 代入 $k$，代表母體集中趨勢已是和母體的所有數字之誤差最小。

## 2.2. 最小平方法得到母體集中趨勢的意義

誤差平方期望值最小，表示母體集中趨勢的代表性愈高。如果誤差平方期望值愈大表示母體內的所有數字愈不集中於 $\mu$。所以母體集中趨勢的數字代表性須以誤差平方期望值為依據，而此誤差平方期望值為「相信此母體集中趨勢」的風險。

> 誤差平方期望值 $= E(\varepsilon^{2}) = Var(X-\mu)=Var(X)=\sigma^{2}$。

# 3. 數字型態影響對應的母體集中趨勢

一般來說，我們取得的具有累加性的數據就使用母體算數平均數計算即可。例如母體的所有數字為 $X_{1}, X_{2}, \cdots, X_{n}$，並且這些數字具有累加性，也就是等差級數，則母體集中趨勢為

$$
\mu = \frac{X_{1}+X_{2}+ \cdots +X_{n}}{n}
\tag{1}
$$

## 3.1. 等比級數配幾何平均數

如果母體內的數字為等比級數，$k_{0}, k_{0} \times r, k_{0} \times r^{2}, \cdots$，此時我們可以將此等比級數轉換成等差級數為

$$
ln(k_{0}), ln(k_{0})+ ln(r), ln(k_{0}) + 2\times ln(r), \cdots
\tag{2}
$$

此時我們就可使用式(1)計算式(2)，得到

$$ \begin{split}
ln(G) &= \frac{ln(X_{1})+ln(X_{2})+ \cdots +ln(X_{n})}{n} \\
      &= ln \left(X_{1} \times X_{2} \times \cdots \times X_{n} \right)^{\frac{1}{n}}
\tag{3}
\end{split}
$$

兩邊去 $ln$，得到

$$ 
G= \left(X_{1} \times X_{2} \times \cdots \times X_{n} \right)^{\frac{1}{n}}
\tag{4}
$$

## 3.2. 調和級數配調和平均數

對於調和級數來說，相當是等差級數內的數字做倒數。所以同樣套用式(1)，只是所有的 $X$ 都變成倒數，得到調和平均數 $H$ 為

$$
H=\frac{n}{\frac{1}{X_{1}}+\frac{1}{X_{2}}+ \cdots + \frac{1}{X_{n}}}
\tag{5}
$$

式(4)和式(5)的 $X$都要大於$0$。

## 3.3. 類別型數字配眾數

類別型數字不具有加減乘除的意義，我們只是按「性質」區分，是這個性質就算「**1**」，然後計算此性質的相對次數得到機率值。機率值愈大代表出現可能性愈高，因此使用眾數代表。但並非每組數據集都能有眾數。

## 3.4. 順序型數字配中位數

這種數字在統計學中稱為順序統計量(order statistic)，只有一種功能，就是排序用。它不能做加減乘除，而且可能沒有任何規則可言。此時用原數據集內的數字由小排到大，然後重新編號為 $1, 2, \cdots, N$。

我們運用新的編號得到平均數為 $(N+1) / 2$。根據此平均數編號，找到對應的原數字。

還有一種情況是母體機率分配不存在平均數，此時我們得改用中位數代表母體集中趨勢。

# 4. 小結

了解母體集中趨勢有助於取得數據後計算的樣本集中趨勢和母體集中趨勢一致。不至於發生母體集中趨勢為某一數字特性，但樣本集中趨勢都使用算術平均數的窘境。

母體集中趨勢是統計學分析的主軸之一，連迴歸分析也是在找條件期望值的數學式。在學統計學的歸納、比較、分析、決策和預測前，了解母體型態、特徵等是非常重要的。如本文所言，母體集中趨勢的代表數字不同，如果我們在統計學用錯統計量，其代表性不足，遑論繼續分析下去。

# 參考資料

創碼有限公司，2014，「統計學(上)」，創碼有限公司出版，ISBN: 978-986-90519-1-0。