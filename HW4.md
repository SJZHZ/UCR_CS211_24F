# UCR-CS217-HW4: Performance Analysis

## Prerequisite
- Notation
    - Problem size: $n$
    - Number of processors: $p$
    - Fraction of potentially parallel tasks: $f,s$
    - Inherently sequential computations: $\sigma(n)$
    - Potentially parallel computations: $\phi(n)$
    - Communication operations: $\kappa(n,p)$
    $$$$
- Amdahl's Law
    $$\Psi \leq \frac{1}{(1-f)+\frac{f}{p}}$$
- Gustafson-Barsis' Law
    $$\Psi \leq p+(1-p)s= s+(1-s)p$$
- Karp-Flatt metric
    $$\Psi(n,p) \leq \frac{\sigma(n)+\phi(n)}{\sigma(n)+\frac{\phi(n)}{p}+\kappa(n,p)}$$
- Isoefficiency metric

## Q1
It's obvious that $f=95\%=0.95, p=10$. According to Amdahl's Law, the maximum speed up is
$$\Psi \leq \frac{1}{0.05+0.95/10} = \frac{1}{0.145} \approx 6.9$$

## Q2
Let us assume $\Psi=10$. To get the minimum number of processors, assume that other parts can be parallelized.  
Thus $f=(1-6\%)=0.94$.
$$
    \Psi =10 \leq \frac{1}{(0.06 + \frac{0.94}{p})} 
    \implies 0.06 + \frac{0.94}{p} \leq \frac{1}{10} 
    \implies \frac{0.94}{p} \leq 0.04 
    \implies p \geq \frac{0.94}{0.04} = 23.5
    \implies p = 24
$$ 

## Q3
As stated in the problem, $\Psi = 50$. According to Amdahl's Law,
$$\Psi = 50 \leq \frac{1}{(1-f)+\frac{f}{p}} < \frac{1}{(1-f)}, f \neq 0 
\implies f' = 1-f < \frac{1}{50} = 0.02 $$

## Q4
According to the problem statement, $\Psi=9, p=10$. According to Amdahl's Law,
$$\Psi = 9 \leq \frac{1}{(1-f)+\frac{f}{10}} \implies (1-f)+\frac{f}{10} \leq 1/9 \implies \frac{8}{9} \leq \frac{9}{10}f \implies f \geq \frac{80}{81} \approx 0.988$$

## Q5
According to the problem statement, $p=16, t_{parallel, scaled} = t*p = 233*16 = 3728$.  
According to Gustafson-Barsis' Law, 
$$s = \frac{t_{sequential, scaled}}{t_{total, scaled}} = \frac{}$$
$$\Psi \leq p+(1-p)s= s+(1-s)p$$

## Q6

## Q7

## Q8

## Q9

## Q10
