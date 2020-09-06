---
layout: article
title: CFA Fixed Income
tags: CFA2 Fixed_Income
key: 20200802
aside:
  toc: true
---

Preparing for CFA Level 2 Exam in 2020.12

<!--more-->

# General | 杂
## Bond: factors influencing YTM
  - Currency: rate of inflation
  - Credit risk: rating
  - Liquidity
  - Tax status: interest income taxable or could be exempt from taxation
  - Periodicity: payment frequency

### Maturity Structure
  - should be analyzed for bonds that have same properties
    - Factors above
    - Same coupon rate -> same coupon reinvestment risk

# Reading 32
Term Structure and Interest Rates Dynamics

## Benchmark Curve
### Spot rate vs. YTM

  - **Coupon-paying bond**:\\
    YTM is the weighted average of spot rates (eg: $s_1, s_2$), and is closer to $s_2$, if the spot curve is upward sloping.
    > $s_1 < YTM < s_2$

  - **Zero-coupon bond:**
    $YTM = s$

### Forward Rate * :star:

#### 1. Discount Factor
  $P(T) = \frac{1}{[1 + r(T)]^T}$

#### 2. Forward Rate Model
- A **forward rate** is an interest rate that is determined today for a loan that will be initiated in a future time period.

- Discount Factor

  $F(T^\*,T) = \frac{1}{[1 + f(T^\*,T)]^T}$

  > $f(T^\*,T)$ is the forward rate of a loan initiated T* years from today with tenor of T years.\\
  > $F(T^\*,T)$ is the forward price at time T* from today for a zero-coupon bond with unit principal maturing at time T+T*

- **Forward rate model**: The relationship between spot rate and forward rate.
  - (1) 计算

     $[1 + r(T^\*+T)]^{(T^\*+T)} = [1 + r(T^\*)]^{T^\*}[1 + f(T^\*,T)]^T$

    > eg: $(1+s_3)^3 = (1+s_1)*(1+f(1,2))^2$
  
  - (2) 结论

    When spot curve is upward sloping:
    - **s & f**: $s_1 < f(1,2) < s_3$
    - **f & f**: $f(2,1) < f(3,1)$

#### 3. Forward Pricing Model

  > :notebook: Calculate the forward price one year from now for a ${$1}$ par, zero-coupon, two-year bond given the following spot rates.\\
  > $~~~~~~$ s1 = 7%, s3 = 9%
  
  > Ans:<br/>
  > $(1 + s_1)(1 + f(1,2))^2 = (1 + s_3)^3$ <br/>
  > $$F(1,2)=\frac{1}{(1 + f(1,2))^2}=\frac{1 + s_1}{(1 + s_3)^3}=\frac{1+7\%}{(1+9\%)^3}$$<br/>
  >$$
  >\begin{eqnarray*}
  >F(1,2)&=&\frac{1}{(1 + f(1,2))^2} \\
  >      &=&\frac{1 + s_1}{(1 + s_3)^3} \\
  >      &=&\frac{1+7\%}{(1+9\%)^3}
  >\end{eqnarray*}
  >$$    
 
#### 4. Active Bond Portfolio Management
- Forward contract price: s' vs. f
  - s' = f => P-<br/>
  - s' < f => P↑<br/>
  > If future spot rates are lower than what is predicted by current forward rates, forward contract price will increase.\\
  > -> Long the forward contract
  - s' > f => P↓<br/>
  > If future spot rates are higher than what is predicted by current forward rates, forward contract price will decrease.\\
  > -> Short the forward contract

- Riding the yield curve/rolling down the curve strategy
  - Assumption:<br/>
    - A yield curve slopes upward. / The forward cureve is always above the current spot curve.<br/>
    - Yield curve won't change its level and shape over an investment horizon.
  - Strategy:<br/>
    - Buy bonds with a maturity longer than the investment horizon.
    > eg: Buy a 30-year bond, hold for 5 year and sell at a 25-year bond price.

### Par Rate
1. 定义\\
  **Par Rate** is the **YTM** on **par bond**.\\
  **Par Curve**: YTM on par bonds, over a range of maturities.\\
  **Par Bond**: coupon-paying government bonds, priced at par.
  > Price = Par Value\\
  > YTM = Par Rate = Coupon Rate :star:

2. 计算\\
   par rate $\Leftrightarrow$ spot rate $\Leftrightarrow$ forward rate\\
   - par rate $\Rightarrow$ spot rate\\
     - 1 yr: $P = Par = \frac{c+Par}{1+s_1}\Rightarrow \frac{c_1}{Par} = CR_1$
     - 2 yr: $P = Par = \frac{c}{1+s_1} + \frac{c+Par}{(1+s_2)^2} \Rightarrow \frac{c_2}{Par} = CR_2$
     - ... 
     - $PR_t = YTM_t = CR_t$
   - spot rate $\Leftarrow$ par rate\\
     - 1 yr: $P = Par = \frac{c+Par}{1+s_1} = \frac{Par\times CR_1+Par}{1+s_1} \Rightarrow s_1 = CR_1 = PR_1$
     - 2 yr: $P = Par = \frac{c}{1+s_1} + \frac{c+Par}{(1+s_2)^2}$
     > $c = Par\times CR_2 = Par\times PR_2$\\
     > $s_1 = PR_1$\\
     > 仅 $s_2$ 未知，可求

### YTM & Spot Rate
  - **Coupon-paying bond**:
    YTM is the weighted average of spot rates (eg: $s_1, s_2, s_3$), and is closest to $s_3$.
  - **Zero-coupon bond:**
    $YTM = s$
  
### Swap Rate
1. 计算\\
  **Swap rate**: the interest rate for the fixed-rate leg of an interest rate swap.\\
  **Swap curve** is a type of **par curve**.\\
  $V_{swap} = V_{fixed} - V_{floating} = 0$

    > 关键假设：floating leg的 coupon rate = spot rate $\Rightarrow$ Par bond
    
    $V_{fixed} = V_{floating} = Par$

    $\Rightarrow$ swap rate(SR) = fixed rate = Coupon rate(CR)
    > Note: 计算swap rate转化为计算fixed-rate leg的coupon rate.\\
    > :notebook: 例题见slides P35.

2. 优点 (3个)\\
  Why swap rate is prefered over government bond as benchmark rate:
  - Higher liquidity
  > 国债只有11个固定期限，而swap期限更灵活，OTC可以定制各种期限（different maturities）
  - Default risk / Credit risk 与公司债券更相似
  > swap rate通常是大型金融机构使用，有较低的credit risk；而国债被认为没有credit risk
  - 管制角度
  > swap：OTC全球交易，unregulated，使用方便；国债受管制较严

## Yield Spread (P39-49)
> 1. 公式(5种Benchmark)\\
>   Yield Spread $= Y_i - Y_B$\\
>   $Y_i = Y_B + $ Yield Spread
>   Note: $Y_i$ and $Y_B$ have the same maturity.期限相同！
> 2. What risk does the spread compensate for?

### Swap Spread
- ${Swap~spread}_t = {swap~rate}_t - {Treasury~yield}_t$
- Swaps have higher **default risk** and higher **market liquidity** than US treasury bonds.

### I-Spread
**I-spreads**: bond rates net of the swap rates of the same maturities.
- ${I-spread} = {bond~rate} - {swap~rate}$
- Compensate for **credit and liquidity** risks.

### Z-Spread
- $Z-spread = S_C - S_T$

  Z-spread is a more **accurate** measure of risk premium (credit & liquiduty) of **corporate bonds**. 
  > Z-spread is the constant basis point spread between 公司债券spot rate and 国债spot rate.

  > eg: Consider a 5% annual coupon bond with a maturity of 2 years and a par value of US\$100. \\
  > The spot yield curve is r(1)=3%, r(2)=4%. The bond price is US\$101.55. Calculate the Z-spread.

  > **Ans**: $101.55 = \frac{5}{1+0.03+ZS}+\frac{105}{(1+0.04+ZS)^2}$\\
  > 试错法找ZS，先试中间值，再根据算出的价格高低调整ZS\\
  > Z-spread = 20bps

### TED spread
- TED = LIBOR - T-bill rate
> TED: T-bill + Eurodollar境外美元（标的资产利率用LIBOR）
- **TED spread** is an indicator od perceived credit risk in the general economy.
- **TED spread** is also a measure of **counterparty risk**.
> TED spread more accurately reflects **risk in the banking system**, whereas swap spread is more often a reflection of differing supply and demand conditions.

### L-OIS
- Libor-OIS spread = Libor - OIS(overnight indexed swap rate)
> **OIS** is an interest rate swap in which the periodic floating rate of the swap is equal to the geometric average of an overnight rate(or overnight index rate) over everyday of the payment period.\\
> **The index rate** is typically the rate for overnight unsecured lending between banks.
- Libor-OIS spread is considered an indicator of the **risk and liquidity of money market securities**.

## Term Structure Theory
> （1）掌握理论描述（定性）; （2）用理论解释收益率曲线Shape

### Pure (Unbiased) Expectations Theory | 纯预期理论
- **Description**: 
  - The forward rate is an unbiased predictor of the future spot rate.
  - The predictions of the unbiased expectations theory are consistent with the assumption of risk neutrality.
    > The assumption is conflict with the large body of evidence that shows that investors are risk aversion. $\Rightarrow$ Local Expectation Theory[Add Link]

- **Implications for the shape**:
  - If the yield curve is **upward sloping**, short-term rates are expected to rise.
  - If the yield curve is **downward sloping**, short-term rates are expected to fall.
  - A **flat yield curve** implites that the market expects short-term rates to remain constant.
  <br/>
- **Local Expectation Theory**
  - **Description**: \\
    Rather than asserting that every maturity strategy has the same expected return over a given investment horizon, this theory instead contends that the expected return for every bond **over short periods** is the risk-free rate.
    > 相对纯预期理论加了"短期"的限制：\\
    > Short term bond: no risk\\
    > Long term bond: not risk-free! + premium!  
  
### Liquidity Preference Theory | 流动性偏好
- **Description**:
  - Liquidity premium exist to compensate investors for the added interest rate risk they face when lending long term and these premium increase with maturity.
  - The forward rate provides an estimate of the expected spot rate that is **biased** upward by the amount of the liquidity premium.

- Shape:\\
    $f = r^e + LRP$\\
    $R_2 = \frac{r_1+r^e_2}{2}+{Liquidity~Risk~Premium}$\\
    **A positive-sloping yield curve** may indicates that:
    - The market expects future interest rates to rise, or
    - rates are expected to remain constant/fall, but the addition of the liquidity premium results in positive slope.

### Segmented Market Theory | 分割理论
- **Description**:
  - Allows lender and borrower preferences to influence the shape of the yield curve.
  - Yields are solely determined by the **supply and demand** for the funds of a **particular maturity**
  - Each maturity sector can be thought of as a segmented market in which yield is determined **independently** from the yields that prevail in other maturity segments.
  > 长期和短期市场是分割且相互独立的\\
  > The theory is consistent with a world where there are asset/liability management(ALM) constraints(eg: IPS, Mandates)\\
  > It assumes market participants are either unwillingly or unable to invest in anything other than securities of their preferred maturities.\\
  > 由于限制/自愿， 只对指定的期限进行投资，则只对指定市场产生影响 $\Rightarrow$ 市场分割

### Preferred Habitat Theory | 习惯性偏好
- **Description**:
  - Many borrowers and lenders have strong preferences for particular maturities but not assert that yields at different maturities are determined independently of each other.
    > 与Segmented market theory对比：\\
    > **相同**: 都分长短期市场\\
    > **区别**: Preffered habitat theory中，长短期市场不完全独立，长短期投资可转换，只要premium足够高;<br/> 
    > $~~~~~~~~$ Segmented market theory不涉及长短期转换，强调**match** investment horizon
  - If the expected additional returns to be gained become large enough, institutions will be willing to deviate from their preferred maturities or habitats.

- **Shape**:
  - Prefer short term investment $\Rightarrow r_短 < r_长 \Rightarrow$ upward sloping yield curve
  - Prefer long term investment $\Rightarrow r_短 > r_长 \Rightarrow$ downward sloping yield curve

## Modern Term Structure Model (定量)

$\Delta r = \underbrace{m(t)\Delta t}_{drift~term} + \underbrace{n(t)\Delta z} _{stochastic~term}$

### Cox-Ingersoll-Ross Model
> Equilibrium Term Structure Model

$dr=\underbrace{a(b-r)}_{m(t)}dt +\underbrace{\sigma\sqrt{r}} _{n(t)}dz$

> dr: change in the short-term interest rate\\
> a: speed of mean aversion parameter\\
> b: long-run value of short-term interest rate\\
> r: the short-term interest rate\\
> dt: small increase in time\\
> $\sigma$ : volatility
> dz: a small random walk movement

:boom: 结论(3个)
- The model has two parts: deterministic part (drift term) & stochastic(random) part;
- The deterministic part ensures **mean aversion** of the interest rate toward a long-run value b, with the speed of adjustment governed by the strictly positive parameter a;
- Volatility increase with the level of interest rates.

### V-Model
> Equlibrium Term Structure Model

$dr=\underbrace{a(b-r)}_{m(t)}dt +\underbrace{\sigma} _{n(constant)}dz$

:boom: 结论(3个)
> 前两个与CIR Model相同

- Volatility remains constant over the period of analysis. It does not increase with the level of interest rates.

### H-L Model
> Arbitrage-free Model\\
> Advantage over equilibrium model: the ability ro calibrate arbitrage-free models to **match current market prices**.

$dr_t=\theta_t dt + \underbrace{\sigma}_{constant} dz_t$

:boom: 结论
- The model can be calibrated to market data by inferring the form of the time-dependent drift term $\theta_t$ from the market prices $\rightarrow$ the model can precisely generate the current term structure.

## Yield Curve Risk
### Factors | 影响因素
- **Level** movement: an upward or downward shift in the yield curve
- **Steapness** movement: non-parallel shift in the yield curve when either short-term rates change more than long-term rates or vise versa
- **Curvature** movement: the short-term and long-term segments rise while the middle-term segment falls or vise versa

### KRD
1. 定义\\
**Key rate duration** is a measure of bond's sensitivity to a change in the benchmark yield curve at a specific maturity segment. (for **non-parallel shifts**)
> KRD allows identification and management of "shaping risk" (yield curve risk), while duration measures bond price risk only for small **paralleled shifts** in the yield curve.(The yields of all maturities change by the same amount.各期限债券的收益率变化相同，只有level movement)

2. 计算|公式\\
  $KRD_i = w_i \times D_i$
  $D_p = - \sum KRD_i$\\
  $\%\Delta P_p = \sum KRD_i\\ \times \Delta y_i$

### Duration分解
> Decompose the risk into sensitivity to three categories of yield curve movement: level, steepness, and curvature.

> $D = -\frac{\Delta P/P}{\Delta y}\Rightarrow \frac{\Delta P}{P} = -D*\Delta y$

$\frac{\Delta P}{P} = - D_L\Delta x_L - D_S\Delta x_S - D_C\Delta x_C$

> $\Delta x_L = 1$: one standard deviation in the level factor (1% change in the yields of all terms).\\
$D_L$: the negative of the proportional change in price per unit change in the level movement.\\
> 要会根据具体定义，用D定义，或KRD计算分解的Duration

### Yield Curve Volatility 
- Quantifying volatility $\sigma_r$ is important:
  - For fixed-income instruments and derivatives with embedded options: $\sigma_r \uparrow  \Rightarrow V_{option} \uparrow$
   - Interest rate management is important, including controlling the impact of interest rate volatilities on the instrument's prive volatility.

- $\sigma_短 > \sigma_长$
> Monetary policy $\Rightarrow$ short-term rates (volatility)\\
> Real economy and inflation $\Rightarrow$ long-term rates (volatility)
- 年月volatility转换\\
  $\sigma_{year} = \sigma_{month} \times \sqrt{12}$

# Reading 33 
The Arbitrage-Free Valuation Framework

## Binominal Interest Rate Tree
- $i_{1,H} = i_{1,L} \times e^{2\sigma}$

- $\sigma$ 的估计：
  - historical $\rightarrow$ recent
  - implied

- $\sigma \uparrow$ : spread out (分散)

- $(1+s_2)^2/(1+s_1) = f_{1,1} = i_M$
  > 用spot rate求出的forward rate是middle rate,再用同期各状态间利率关系求利率二叉树其他利率。\\
  > $(1+s_3)^3 = (1+s_2)^2*(1+f_{2,1}$ \\
  > $f_{2,1} = i_{2,LH} = i_{2,HL}$\\
  > :notebook: 例题见讲义102-103

## Arbitrage-free Valuation

![arbi-free valuation](https://github.com/Lisa-X/Lisa-X.github.io/raw/master/pics/fixed_income_pic/arbitrage_valuation_binominal_tree.png)




  