# A3 BKM8: Index Models

Z. Bodie, A. Kane, A. Marcus

## Cliff's Summary

[**Single Factor Model**](#single-factor)

$r_i = \operatorname{E}[r_i] + \beta_i m + e_i$

* Assumptions and source of uncertainty

Variance and covariance

* $\sigma^2_i = \beta^2_i \sigma^2_m + \sigma^2(e_i)$

* $\operatorname{Cov}(r_i, r_j) = \operatorname{Cov}(\beta_i m + e_i, \beta_j m + e_j) = \beta_i \beta_j \sigma^2_m$

**Single Index Model**

Return Premium with market index $M$:

* $R_i(t) = \alpha_i + \beta_i R_M(t) + e_i(t)$

Expected Return Premium:

* $\operatorname{E}[R_i] = \overbrace{\underbrace{\alpha_i}_{\text{Non-mkt premium}} + \underbrace{\beta_i \operatorname{E}[R_M]}_{\text{Systematic risk premium}}}^{\text{Components of risk premium}}$

[Pros and cons](#single-index-pros-cons) of single index model

[Portfolio variance](#firm-spec-risk) as number of stock change

* $\sigma^2_p = \underbrace{\beta^2_p \sigma^2_m}_{\text{System}} + \underbrace{\sigma^2(e_p)}_{\text{Firm}}$

* $\sigma^2(e_p) = \dfrac{\bar{\sigma}^2(e)}{n}$

Security characteristic line

* And other things to do with parameters $\alpha$ and $\beta$

[Alpha transport](#alpha)

[Portfolio construction](#ptf-construct)

1. Get the weight between active portfolio based on $\dfrac{\alpha_i}{\sigma^2(e_i)}$ then scale it to 1

2. Get the weighted parameters ($\alpha, \sigma^2(e_i), \beta_i$)

3. Use the 2 part formula to get the weight of the active portfolio within the total risky portfolio

    * $w^*_A = \dfrac{w^0_A}{1 + (1-\beta_A)w^0_A}$

    * $w^0_A = \dfrac{ \alpha_A / \sigma^2(e_A)}{\operatorname{E}[R_M] / \sigma^2_m}$

4. Get the weight of the market and weight of the individual stocks withint the total risky portfolio (simple math)

5. Risk premium and variance of the risky portfolio

    * $\operatorname{E}[R_p] = (w^*_M + w^*_A \beta_A) \operatorname{E}[R_M] + w^*_A \alpha_A$

    * $\sigma^2_p = (w^*_M + w^*_A \beta_A)^2 \sigma^2_M + \underbrace{(w^*_A)^2\sigma^2(e_A)}_{\text{firm risk}}$

### Types of Exam Questions

<span style="color:red">Haven't done TIA practice questions</span>

**Covariance/ Systematic Risk**

* $\star$ 2003, Q12: $\sigma$ and Cov with single index model
    * Same cov formula as the one in single index model
* $\star$ [2004, Q8](#2004-8): systematic and non systemmatic
* $\star$ [2015, Q3](#2015-3): Covariance, systematic and firm risk

**Risky portfolio construction**

* $\star$ [2013, Q3](#2013-3): optimal risky portfolio portions

**Concepts**

* 2014, Q4: Markowitz vs single index (number of estimate and internal consistency)

## Single Factor Model

Problem with Markowitz Model from BKM 7

* As # of securities $\uparrow$, # of variables that need to be estimate $\Uparrow$

    * $n$ expected return, $n$ variance, and $\dfrac{n^2 - n}{2}$ covariance
    
* Increase likelihood of estimation error and may produce nonsensical results

<a name="single-factor"></a> **Single Factor Model**

$r_i = \operatorname{E}[r_i] + \beta_i m + e_i$

* $m \sim$ mean = 0, $\sigma_m$

* $e_i \sim$ mean = 0, $\sigma_i$

**Assumptions** for single factor model

Return of a security:

* $r_i = \operatorname{E}[r_i] + e_i$

* $e_i \sim$ mean = 0, $\sigma_i$

Joint normally distributed based on factor $m$

**2 sources of uncertainty**:

1) Uncertainty about $m$ (systematic)

    * Influences all securities as it generates correlation for all securities
    
    * Assume that the sensitivity of a stock to $m$ is $\beta_i$ (some firms are more sensitive to changes in the economy)
    
2) Firm specific uncertainty $e_i$

$m$ and $e_i$ are uncorrelated

* $e_i$ is independent to shocks that impact the entire economy

**Variance and Covariance**

$\sigma^2_i = \beta^2_i \sigma^2_m + \sigma^2(e_i)$

$\operatorname{Cov}(r_i, r_j) = \operatorname{Cov}(\beta_i m + e_i, \beta_j m + e_j) = \beta_i \beta_j \sigma^2_m$

* Beware of what's given in a question, $\sigma^2_i$ or $\sigma^2(e_i)$

## Single Index Model

A version of the single factor model with return on an index used as proxy for the common factor $m$

* Lots of data available on a broad index like S&P 500 to estimate the parameters

**Return Premium** with market index $M$:

* $R_i(t) = \alpha_i + \beta_i R_M(t) + e_i(t)$

* $\alpha_i$: expected XS return of security when market XS return $R_M(t)$ = 0

* $\alpha_i$ $\uparrow$ if stock is underpriced

**Expected Return Premium**:

* $\operatorname{E}[R_i] = \overbrace{\underbrace{\alpha_i}_{\text{Non-mkt premium}} + \underbrace{\beta_i \operatorname{E}[R_M]}_{\text{Systematic risk premium}}}^{\text{Components of risk premium}}$

* Compare $\alpha_i$ for stock picks

***

<a name="single-index-pros-cons"></a> **Advantages**

Only requires $3n+2$ variables

* $\alpha_i, \beta_i, \sigma_i$ for each stock and $R_M$ and $\sigma^2_m$

Allows for specialization of effort in security analysis

* No need for anyone to estimate the covariance between stocks from 2 different industries

* With significantly less estimates, mutually inconsistent results are far less likely

**Disadvantages**

Oversimplifies the true uncertainty

* Splits into micro vs macro risk

* Ignores correlation between security returns

* Ignores industry events (factors that impact many firms within an industry but without materially impacting the overall economy)

Might be more appropriate to use multi index model if there are correlations not account for by $M$

***

<a name="firm-spec-risk"></a>

Firm specific risk $\downarrow$ as stock in portfolio $\uparrow$

Portfolio variance with equally weighted securities:

* $\sigma^2_p = \underbrace{\beta^2_p \sigma^2_m}_{\text{System}} + \underbrace{\sigma^2(e_p)}_{\text{Firm}}$

* $\sigma^2(e_p) = \dfrac{\bar{\sigma}^2(e)}{n}$

    * $\lim \limits_{n \rightarrow \infty} \sigma^2(e_p) = 0$
    
### Estimating the Single Index Model

**Security Characteristic Line** (SCL)

* Resulting equation from regressions to estimate the parameters of the Single Index Model

#### Significance of alpha and beta

Hypothesis test: $\alpha = 0$

To reject $H_0: \alpha = 0$

1) Magnitude of $\alpha$ need to be large enough to be deemed *economically* significant

2) $\alpha$ also need to be *statistically significant* (e.g. t > 2, p-value = 0.05)

Even if $\alpha$ passes the 2 criteria above, it is no appropriate to rely on it to forecast a future period as $\alpha$ do not persist over time

***

Similar can test $\beta =0$ or $\beta > 1$ (market wide $\beta$)

Also can test the correlation between stock and S&P (R^2^) $\Rightarrow$ Indicates the portion of the variation in the stock that can be explained by the variance of the S&P

#### Predicting Beta

Need to forecast $\beta$'s as it changes over time

**Option 1**: Regression based on past $\beta$

$\beta_t = a + b \times \beta_{t-1}$

**Option 2**: Regression with other financial variables that may impact $\beta$

$\beta_t = a + b_1 \times \beta_{t-1} + b_2 \times \text{Firm Size} + b_3 \times \text{Debt Ratio}$

* Other potential variables: variance in earnings or cash flow, EPS growth, market capitalization, dividend yield, debt:asset ratio

#### Alpha Transport

<a name="alpha"></a> **Alpha Transport**

Earn return independent from the market return, not exposed to risk of market

Separate the alpha from the choice of market exposure by purchasing the security and short selling the tracking portfolio

**Tracking Portfolio**

* Matches the systematic component of the risky security's return

* Has the same beta as the risky security

***

Example

* $R_p = 0.04 + 1.4 R_{S\&P} + e_p$

* tracking portfolio = 1.4 S&P - 0.4 t-bills

* $\alpha = 0$ since only S&P and t-bills

* Alpha transport: $R_c = R_p - R_T = 0.04 + e_p$

## Portfolio Construction

### Alpha & Security Analysis

1) Estimate risk premium and risk of the market index\
    * Macro econ analysis
2) Calculate $\beta$ and $\sigma^2(e_i)$ of each security
    * Statistical analysis
3) Calculate $\operatorname{E}[r_i]$ based only on market return             * Excluding $\alpha$
4) Calculate $\alpha$ using security analysis
    * Return based on security analysis - results from step 3

### Optimal Risky Portfolio

Based on Single Index Model

**Inputs**:

* $R_M$: risk premium of S&P
* $\sigma_m$: s.d. of S&P
* $\alpha_i, \beta_i, \sigma^2(e_i)$ $\forall n$ stocks

**Risky Portfolio**:

${\color{blue}{\alpha_p}} = \sum w_i \alpha_i$

${\color{orange}{\beta_p}} = \sum w_i \beta_i$

${\color{green}{\sigma^2(e_p)}} = \sum w^2_i \sigma^2(e_i)$

* <span style="color:red">Assume independent?</span>

Select weights that maximize Sharpe ratio $\dfrac{\operatorname{E}[R_p]}{\sigma_p}$

$\operatorname{E}[R_p] = {\color{blue}{\alpha_p}} + \operatorname{E}[R_M] {\color{orange}{\beta_p}}$

$\sigma_p = \sqrt{\sigma^2_m {\color{orange}{\beta^2_p}} + {\color{green}{\sigma^2(e_p)}}}$

Optimal weight of active portfolio (vs market portfolio):

$w^*_A = \dfrac{w^0_A}{1 + (1-\beta_A)w^0_A}$

* $w^0_A = \dfrac{\alpha_A / \sigma^2(e_A)}{\operatorname{E}[R_M] / \sigma^2_m}$

If objective is to diversify, should just invest in the market portfolio

* Procedure above is to produce the optimal risky portfolio, which is a mix of the market portfolio and the selected securities from security analysis

*Advantages*:  
Identify non-zero $\alpha$s and over/under weight relative to the market to increase return

*Disadvantage*:  
Introduce firm specific risk (since it's not as diversify as the market portfolio)

### Information Ratio

**Sharpe Ratio**:

$S^2_p = S^2_M + \left[ \overbrace{\dfrac{\alpha_A}{\sigma(e_A)}}^{\text{info ratio}}\right]^2$

**Information Ratio** represents the contribution of the active portfolio when held at optimal weight, to the Sharpe ratio

* Based on the additional return from security analysis, relative to the additional firm specific risk
    
To maximize the Sharpe ratio, we need to maximize the information ratio

* Investment in each security needs to be $\propto \dfrac{\alpha_i}{\sigma^2(e_i)}$ while keeping total investment in the active portfolio $= w^*_A$

* $w^*_i = w^*_A \dfrac{\alpha_i / \sigma^2(e_i)}{\sum \alpha_i / \sigma^2(e_i)}$

If short positions are prohibited, we need to take out securities with negative weight and give them 0 weight

### Summary of Procedure

<a name="ptf-construct"></a>

1. Calculate the ratio of each security of the active portfolio

    * $w^0_i = \dfrac{\alpha_i}{\sigma^2(e_i)}$

2. Scale the above to = 1

    * $w_i = \dfrac{w^0_i}{\sum w^0_i}$

3. Calculate the alpha, beta and residual variance of the active portfolio

    * ${\color{blue}{\alpha_A}} = \sum \limits_{i \in A} w_i \alpha_i$

    * ${\color{orange}{\beta_A}} = \sum \limits_{i \in A} w_i \beta_i$

    * ${\color{green}{\sigma^2(e_A)}} = \sum \limits_{i \in A} w^2_i \sigma^2(e_i)$

4. Calculate the weight of active portfolio $W^*_A$

    * $w^*_A = \dfrac{w^0_A}{1 + (1-{\color{orange}{\beta_A}})w^0_A}$

        * $w^0_A = \dfrac{ {\color{blue}{\alpha_A}} / {\color{green}{\sigma^2(e_A)}}}{\operatorname{E}[R_M] / \sigma^2_m}$

5. Calculate the weights of the market and each security in the optimal risky portfolio

    * $w^*_M = 1 - w^*_A$ Weight of market

    * $w^*_i = w^*_A \cdot w_i$ Weight of each security 

6. Calculate the risk premium and variance of the optimal risky portfolio

    * $\operatorname{E}[R_p] = (w^*_M + w^*_A {\color{orange}{\beta_A}}) \operatorname{E}[R_M] + w^*_A {\color{blue}{\alpha_A}}$

    * $\sigma^2_p = (w^*_M + w^*_A {\color{orange}{\beta_A}})^2 \sigma^2_M + \underbrace{(w^*_A)^2{\color{green}{\sigma^2(e_A)}}}_{\text{firm risk}}$
    
## Past Exam Questions

<a name="2004-8"></a> 2004, Q8
![alt text](Section A/questions/2004-8Q.png)
![alt text](Section A/questions/2004-8A.png)

<a name="2013-3"></a> 2013, Q3
![alt text](Section A/questions/2013-3Q.png)
![alt text](Section A/questions/2013-3A.png)

<a name="2015-3"></a> 2015, Q3
![alt text](Section A/questions/2015-3Q.png)
![alt text](Section A/questions/2015-3A.png)
