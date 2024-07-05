
# $L = \lim_{x \to 0} \frac{\sin x}{x}$
```
clear,clc;
syms x ;
f = sin(x)/x ;
L = limit(f, x, 0) ;
```
 
# $L = \lim_{x \to \infty} x{(1 + \frac{a}{x})}^x \sin \frac{b}{x})$
```
syms x a b ; 
f = x*(1+a/x)^x*sin(b/x) ;
L = limit(f, x, inf) ;
```

# $L = \lim_{x \to 0^+} \frac{e^{x^3} - 1}{1 - \cos \sqrt{x - \sin x}}$
```
syms x ;
f = (exp(x^3) - 1)/(1 - cos(sqrt(x - sin(x)))) ;
L = limit(f, x, 0, 'right') ;
```

# $\lim_{x \to (\frac{\pi}{2})^-} \tan t$ and $\lim_{x \to (\frac{\pi}{2})^+} \tan t$
```
syms t ;
f = tan(t) ;
L1 = limit(f, t, pi/2, 'left') ;
L2 = limit(f, t, pi/2, 'right') ;
```

# $L = \lim_{n \to \infty} \frac{\sqrt[3]{n^2} \sin n!}{n + 1}$
```
syms n positive ; 	# syms n>0
f = (n^(2/3) * sin(factorial(n)))/(n + 1) ;
L = limit(f, n, inf)
```

# $\lim_{x \to 2} [ \lim_{y \to -2} f(x, y) ]$
```
syms x, y ;
f = x^2 + y^2 ;
L1 = limit(limit(f, x, 2), y, -2)
```