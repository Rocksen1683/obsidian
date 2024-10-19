Say we have an input 
$$u(t) = U\sin(\omega t)$$
Which means we can get the output $y(t)$ by 
$$y(t) = \mathcal{L}^{-1}\{Y(s)\} = \mathcal{L}^{-1}\{G(s)U(s\}$$
$$= \mathcal{L}^{-1}\{G(s)\mathcal{L}\{{u(t)}\}\}$$
$$= \mathcal{L}^{-1}(G(s)\frac{U\omega}{s^{2} + \omega^{2}} )$$
Assume $G(s)$ has *real* and *distinct* poles $p_{i} = 1, ..., u$
$$y(t) = \mathcal{L}^{-1}(\sum\limits_{i=1}^{n}\frac{A_{i}}{s-p_{i}} + \frac{Q}{s-j\omega} + \frac{\bar{Q}}{s+ j\omega})$$
$\frac{A_{i}}{s-p_{i}}$ tends to $0$
$$y_{ss}(t) = \mathcal{L}^{-1}(\frac{Q}{s-j\omega} + \frac{\bar{Q}}{s+ j\omega})$$
$$Q = (s- j\omega)|Y(s)|$$
at $s = j\omega$
$$ = (s-j\omega)(G(s)\frac{U\omega}{s^{2}+ \omega^{2}})$$
$$ = (s-j\omega)(G(s)\frac{U\omega}{(s-j\omega)(s+j\omega)})$$

$$ = (G(s)\frac{U\omega}{(s+j\omega)})$$
plugging in $s = j\omega$
$$ = G(s)\frac{U}{2j}$$
This gives us 
$$\bar{Q} = G(-j\omega)\frac{U}{-2j}$$
$$ = G(j\omega)\frac{U}{-2j}$$
This gives us 
$$y_{ss}(t) = \mathcal{L}^{-1}(\frac{G(j\omega)U}{2j}\frac{1}{s- j\omega} - \frac{\bar{G(j\omega)}U}{2j}\frac{1}{s+j\omega})$$
$$ = \frac{G(j\omega)Ue^{j\omega t}}{2j} - $$
