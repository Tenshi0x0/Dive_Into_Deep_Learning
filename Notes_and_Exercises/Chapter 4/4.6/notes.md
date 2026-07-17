# 4.6 Generalization in Classification

Test error is a mean of Bernoullis, so it estimates population error at rate $O(1/\sqrt n)$; Hoeffding gives the hard bound $n = \ln(1/\delta)/2t^2$ — precision $t$ is quadratically expensive, confidence $\delta$ nearly free (log).

Evaluating $k$ pre-registered models costs only $\log k$ (union bound), but *adaptive* reuse (look → tweak → look) silently voids the guarantee.

For infinite classes, VC dimension $d$ (largest shatterable point set) collapses the effective class size to $n^d$ (Sauer–Shelah), giving $\text{gap} \le c\sqrt{(d - \log\delta)/n}$ — tight for linear models ($\mathrm{VC}=d+1$), vacuous for DNNs (VC $\gg n$ yet they generalize; open problem).
