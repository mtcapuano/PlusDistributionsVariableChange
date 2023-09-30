# Changing variables of plus distributions
We present here a Mathematica code to change variables of plus distributions of the form

$$\left(\frac{\log^p(a-x)}{a-x}\right)_+$$

or

$$\left(\frac{\log^p x}{x}\right)_+.$$

The first regularizes integrals logarithmically divergent in the superior extremum $a$, while the second those divergent in the inferior extremum $0$.

We consider the variable change

$$y=f(x)$$

that moves the divergence from $a$ to $b=f(a)$. Since the integral must still be logarithmically divergent in order to be regularized by the plus distribution, we assume that the variable change can always be rewritten as

$$y=b+\mathcal{C}(x)(a-x),$$

where $\mathcal{C}(x)$ is a regular non-zero function in $x$. Rewriting the equation as

$$(b-y)^{-1+\epsilon}=(-\mathcal{C})^{-1+\epsilon}(a-x)^{-1+\epsilon},$$

we can use the distributional identity

$$(a-x)^{-1+\epsilon}=\frac{\delta(a-x)}{\epsilon}+\sum_{k=0}^\infty\frac{\epsilon^k}{k!}\left(\frac{\log^k(a-x)}{a-x}\right)_+$$

on $(b-y)$ and $(a-x)$ and the standard Taylor serie for $\mathcal{C}^\epsilon$. Comparing same-order terms we find plus distributions in $y$ in terms of plus distributions in $x$ with $x$ dependent coefficients.
If we moved the coefficient $\mathcal{C}$ to the LHS we would get plus distributions in $x$ in terms of plus distributions in $y$ with $x$ dependent coefficients. For an example see appendix A of my <a href="https://github.com/mtcapuano/mtcapuano/blob/main/MastersThesis.pdf" class="image fit">Master's thesis</a>.

After download and running the Mathematica notebook, here are the possible commands.

`ChangeVariable[y,b,n,x,a,f]` gives the plus distribution $\left(\frac{\log^n (b-y)}{b-y}\right)_+$ in terms of $x$ distributions, where $f$ is the function $y=f(x)$. Plus distributions are expressed as `plus[y,b,n]`.

`ChangeVariableInv[x,a,n,y,b,f]` gives the plus distribution $\left(\frac{\log^n (a-x)}{a-x}\right)_+$ in terms of $y$ distributions, where $f$ is the function $y=f(x)$.


