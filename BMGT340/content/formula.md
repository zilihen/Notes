# Important Formula

## DuPont Equation

$\text{Return On Equity (ROE)} = \text{PM} * \text{TATO} * \text{EM}$

> [!note]
> Equity = Total Assets + Total Liabilities

$\text{Profit Margin (PM)} = \dfrac{\text{Net Income}}{\text{Sales}}$

$\text{Total Assets Turnover (TATO)} = \dfrac{\text{Sales}}{\text{Assets}}$

$\text{Equity Multiplier (EM)} = \dfrac{\text{Assets}}{\text{Equity}}$

## Time Value Money (TVM)

The worth of your money over time. 

General Formula:

$\text{Future Value (FV)} = \text{Present Value} (PV) * (1+r)^N \iff PV = \dfrac{FV}{(1+r)^N}$, where $N$ is the number payment periods (How many times you are getting paid) and $r$ is the periodic rate (yearly rate, monthly rate, daily rate, etc..).


## PV of uneven cash flows

$PV = \dfrac{C_1}{1+r} + \dfrac{C_2}{(1+r)^2} + ... + \dfrac{C_N}{(1+r)^N}$, where $C_1, C_2, ..., C_N$ are all different cash flows (sometimes called payment)

## Perpetuity:

Payment forever where:

$PV = \dfrac{C}{r}$

### Derivation

Since perpetuity is payment forever, the general formula is defined as:

 $PV = \dfrac{C}{1+r} + \dfrac{C}{(1+r)^2} + \dfrac{C}{(1+r)^3} + ...$

Multiply both sides by $(1+r)$, we get: 

$$(1+r)PV = C + \dfrac{C}{1+r} + \dfrac{C}{(1+r)^2} + ...$$
$$(1+r)PV = C + PV$$
$$(1+r)PV - PV = C$$ 
$$PV((1+r) -1) = C$$
$$PV = \dfrac{C}{((1+r)-1)}$$
$$PV = \dfrac{C}{r}$$

Alternatively, this follow an infinite geometric series

$$PV = \displaystyle \sum_{i = 1}^{\infty} \dfrac{C}{(1+r)^i}$$
$$PV =\dfrac{\dfrac{C}{(1+r)}}{1-\dfrac{1}{(1+r)}}$$
$$PV =\dfrac{\dfrac{C}{(1+r)}}{\dfrac{(1+r)-1}{(1+r)}}$$
$$PV =\dfrac{C}{(1+r)-1}$$
$$PV =\dfrac{C}{r}$$


> [!tip]
> For some payment period $k$ where we want the $PV$ of the cash flow of every $k$ period (can be year, month, day, etc..). Then,
> 
> $$PV = \dfrac{C}{(1+r)^k - 1}$$
>
> Proof
> 
> Suppose we want the cash flow of every $k$ year, starting $k$ year(s) from now. Then,
> 
> $$PV = \dfrac{C}{(1+r)^k} + \dfrac{C}{(1+r)^{2k}} + \dfrac{C}{(1+r)^{3k}} + ...$$ 
> $$(1+r)^kPV = C + \dfrac{C}{(1+r)^{k}} + \dfrac{C}{(1+r)^{2k}} + ...$$ 
> $$(1+r)^kPV = C + PV$$ 
> $$(1+r)^kPV - PV = C$$ 
> $$PV((1+r)^k - 1) = C$$ 
> $$PV = \dfrac{C}{(1+r)^k - 1}$$
> 
> Example
> 
> Suppose we want the cash flow of the even year, starting 2 years from now. Then,
> 
> $$PV = \dfrac{C}{(1+r)^2} + \dfrac{C}{(1+r)^4} + \dfrac{C}{(1+r)^6} + ...$$
> $$(1+r)^2PV = C + \dfrac{C}{(1+r)^4} + \dfrac{C}{(1+r)^6} + ...$$
> $$(1+r)^2PV = C + PV$$
> $$(1+r)^2PV - PV = C$$
> $$PV((1+r)^2 - 1) = C$$
> $$PV = \dfrac{C}{(1+r)^2 - 1}$$

Multiply the $PV$ of the perpetuities by $(1+r)^N$ gives you the $FV$ for $N$ period(s)

## Growing Perpetuity

$PV = \dfrac{C}{r-g}$, where $r$ is the periodic rate, $g$ is the growth rate and $r > g$

Again multiply by $(1+r)^N$ gives you the $FV$ for $N$ period(s)

## Annuity

Payment until $N$ where: 

$PV = \dfrac{C}{r}*\left (1 - \dfrac{1}{(1+r)^N}\right)$

$FV = \dfrac{C}{r}*\left ((1+r)^N - 1 \right)$, derive by multiplying $PV$ by $(1+r)^N$

## Growing Annuity

$PV = \dfrac{C}{r-g}*\left (1 - \left(\dfrac{1+g}{1+r}\right)^N\right)$

$FV = \dfrac{C}{r-g}*\left ((1+r)^N -(1+g)^N \right)$, derive by multiplying $PV$ by $(1+r)^N$

## Annual Percentage Rate (APR) and Effective Annual Rate (EAR)

$APR$ is sometimes called the interest rate, the yearly rate, or the discount rate

$EAR = (1+r)^m - 1$, where $r$ is the periodic rate (or the rate per compounding period), and $m$ is the number of compounding period(s) per year (not payment period(s) which is defined above as $N$). 
- $r = \dfrac{APR}{m}$

Substituting $r$ into the $EAR$ equation you can find the $APR$. 

Also you might have noticed that in the $EAR$ equation the $(1+r)^m$ looks similiar to the TVM of $(1+r)^N$. This is because $EAR$ can be read as the effective annual interest rate you are getting compounded over $m$ period(s).
- Since $m$ is the compounding period(s) per year, $m=1$ if compounded yearly, $m=2$ if compounded semiannually, $m=4$ if compounded quarterly, $m=12$ if compounded monthly, $m=52$ if compounded weekly, $m=365$ if compounded daily (assuming not leap year), etc...
- Note: We can use either the $EAR$ or the $r$ defined above as the $r$ that is found in the TVM formula in which case we need to adjust $N$ depending on which one we use.
  - For example, if $m = 12$ and $APR = 0.06$ then $r = 0.005$ and $EAR = 0.061678$ (this is rounded)
  - You would see that $(1+r)^{12}$ gives you the same answer as $(1+EAR)$, this is because the $EAR$ is already compounded over 12 months where as $r$ is just the simple interest rate for one month.




