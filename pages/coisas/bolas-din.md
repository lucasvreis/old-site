~~~
<meta name="twitter:card" content="summary_large_image"><meta name="twitter:site" content="@lucasvreis"><meta name="twitter:title" content="Bolas dinâmicas"><meta name="twitter:image" content="https://lucasvreis.github.io/pages/coisas/bolas-din/6.png">
~~~

# Bolas dinâmicas

A parte preta nas imagens abaixo é o conjunto dos pontos que ficam a menos de $r$ de distância do ponto vermelho $x$ (ele tá bem pequeno, mas está lá) durante toda a trajetória dos primeiros $n-1$ iterados: a bola dinâmica $B(x,n,r)$. Em outras palavras,

\[B(x,n,r)=\{y : d(f^i(x),f^i(y)) < r, \text{ para todo }\; i\in\{1,\dots,n-1\} \} \]

Usamos essas bolas em uma das formas de definir a entropia topológica de uma dinâmica; se a dinâmica tem entropia topológica positiva, quando o $n$ aumenta precisamos de cada vez mais bolas de raio $r$ para cobrir uma parte do espaço: a dinâmica "gera informação" (a entropia) "evidenciando os detalhes" ao afastar os pontos uns dos outros, e assim as bolas dinâmicas tendem a perder pontos a cada iterado.

![](https://live.staticflickr.com/65535/51155270717_d61e5e62c6_o.png)

![](https://live.staticflickr.com/65535/51157051050_f78fedd2fb_o_d.png)

![](https://live.staticflickr.com/65535/51156179448_1b0d05e762_o_d.png)

![](https://live.staticflickr.com/65535/51155280107_b710f11a06_o_d.png)

Código fonte: [.html](dynamics.jl) / [.jl](notebook.jl)
