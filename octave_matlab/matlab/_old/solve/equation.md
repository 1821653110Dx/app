# $f(x) = x^3 + 2x=0 \\ x =?$
```
clear, clc ;
syms x ;
f(x) = x^3 +2*x ;
solve(f(x)==0,x) ;
```

# $\zeta=0.707, K=4, \omega_n=2 \\ \beta=\frac{2\zeta \omega_n}{K}=?$
```txt
syms zeta omega_n K

beta = 2 * zeta * omega_n / K

zeta = 0.707 ; K = 4 ; omega_n = 2

eval(beta)
```

# $(1 + \frac{K \beta}{s}) - \frac{1}{s} G_n(s) = 0 \\ G_n(s) = ?$
```txt
syms s K beta G_n(s) ; 

F = (1 + k*beta/s) - (1/s)*G_n(s) == 0

solve(F, G_n(s))
```
# $\begin{matrix}x^2+xy+y-3=0 \\ x^2-4x-2y+3=0 \end{matrix},x,y=?$
```txt
syms x y;
f1 = x^2 + x*y + y -3 ;
f2 = x^2-4*x-2*y+3 ;
[x,y] = solve(f1,f2);
pretty([x,y])
```