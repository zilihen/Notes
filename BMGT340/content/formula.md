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

$\text{Future Value (FV)} = \text{Present Value} (PV) * (1+r)^N \iff PV = \dfrac{FV}{(1+r)^N}$, where $N$ is the number payment periods (How many times you are getting paid).


## PV of uneven cash flows

$PV = \dfrac{C_1}{1+r} + \dfrac{C_2}{(1+r)^2} + ... + \dfrac{C_N}{(1+r)^N}$, where $C_1, C_2, ..., C_N$ are all different cash flows (sometimes called payment)

## Perpetuity:

Payment forever where $PV = \dfrac{C}{r}$

### Derivation

Since perpetuity is payment forever, the general formula is defined as $PV = \dfrac{C}{1+r} + \dfrac{C}{(1+r)^2} + \dfrac{C}{(1+r)^3} + ...$

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
> For some payment period $k$, for example we only want the cash flow of even years (so, $k=2$)
> Then the $PV = \dfrac{C}{(1+r)^k - 1}$
>
> > Proof


