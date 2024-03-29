+++
date = Date(2021,5,1)
+++

# Alguns contraexemplos de grupos

Esse semestre estou fazendo a disciplina de grupos e representações. Como quase
sempre, alguns dos teoremas levantam a óbvia pergunta "e se eu não supor isso
aqui?", e a resposta costuma ser encontrar um contraexemplo. Estarei compilando
uma lista com com os contraexemplos que consegui resolver. Vamos lá:

@@teorema

Seja $G$ um grupo. Se $N$ for normal em $H$ e $H$ for subgrupo característico de
$G$, então $N \triangleleft G$.

@@

E se trocamos os papéis supondo que $N$ é característico em $H$ e $H$ é normal
em $G$?

<!-- Um contraexemplo em que $N \not\trianglelefteq G$ é em $D_8$, onde o subgrupo da -->
<!-- reflexão vertical $(\cong \Z_2)$ é característico no subgrupo normal {reflexão -->
<!-- horizontal, reflexão vertical} $(\cong \Z_2\oplus\Z_2)$ mas não é normal em -->
<!-- $D_8$. -->

\

\

Outro teorema:

@@teorema

Se $G$ é grupo abeliano, então todo epimorfismo $\varphi \colon G \to \Z^n$
cinde e vale $G \cong \ker\varphi \oplus \Z^n$.

@@

Vamos ver como o teorema falha se $G$ não é abeliano:

O primeiro contraexemplo que pensei foi em relação a $G$ não ser produto direto.
A ideia era "bagunçar" um grupo abeliano e ainda ter um epimorfismo dele em
$\Z$, e pensei no grupo de simetrias de um plano $\Z^2$ em que é permitido
trocar os dois eixos (mas preservando a direção deles). Concretamente, isso é um
produto semidireto $S_2\rtimes_{\phi}\Z^2$, onde
$\phi : S_2 \to \text{Aut}(\Z^2)$ é dada por $\phi(s)(z) = s(z)$, onde
interpretamos a permutação $s$ como uma função que pode trocar as coordenadas da
dupla $z$.

Definimos a $\varphi : G \to \Z$ como $\varphi((s,(a,b))) = a + b$.

Esse grupo quase não funcionou como contraexemplo (pelo menos da primeira forma
que eu pensei), mas com ajuda de [@franchico](https://twitter.com/chico_melllo)
vimos que ele não pode mesmo ser um produto direto.

O segundo, contraexemplo para a conclusão toda, veio da observação que
$\varphi : G \to \Z^n$ sempre cinde se $n=1$. Então a ideia é modificar $\Z^2$ de forma que ele não seja mais comutativo.

Fixe três coisas $a, b$ e $s$. Podemos escrever $\Z^2$ como o grupo abeliano
livre gerado por $a$ e $b$, i.e. $\langle a, b \mid ab=ba \rangle$. Com isso,
vamos tornar o grupo "anticomutativo" com o "sinal" sendo o elemento $s$, assim:
\[ G = \langle a,b,s \mid ab = sba, \; as=sa, \; bs=sb, \; s^2 = 1 \rangle \]

Como sabemos reordenar as letras e cancelar pares de $s$, todo elemento do grupo
é da forma $s^ia^jb^k$ com $i \in \Z_2$ e $j,k \in \Z$. Então podemos associar
$G = \Z_2 \times \Z \times \Z$, de forma que a multiplicação é

\[(i_1,j_1,k_1)(i_2,j_2,k_2) = (i_1 + i_2 + k_1j_2,\; j_1 + j_2,\; k_1 + k_2).\]

Note que o termo $k_1j_2$ aparece porque simplificando a multiplicação
$s^{i_1}a^{j_1}b^{k_1}s^{i_2}a^{j_2}b^{k_2}$, podemos andar com o $s$ para obter
$s^{i_1 + i_2}a^{j_1}b^{k_1}a^{j_2}b^{k_2}$, e então precisamos trocar $b^{k_1}$
por $a^{j_2}$, o que envolve $k_1j_2$ trocas de $a$ e $b$.

Definindo $\varphi(i,j,k) = (j,k) \in \Z^2$, ela é claramente um epimorfismo.
Mas $\varphi$ não cinde, pois se cindisse com $\mu$, então valeria

$$\mu(1,0)\in\{(0,1,0), (1,1,0)\}, \quad \mu(0,1)\in\{(0,0,1), (1,0,1)\}$$

e é simples ver que em qualquer escolha eles não comutam (precisam comutar para
ser homomorfismo).

\

\

Mais um, sugerido por [@franchico](https://twitter.com/chico_melllo):

@@teorema
Suponha que $H \cong G$ são grupos isomorfos, $N \triangleleft G$, $M
\triangleleft H$ e $N \cong M$. É verdade que $G/N \cong H/M$?
@@


<!-- \begin{details}{Resposta} -->

Não é difícil ver que a preposição é equivalente ao caso particular "$M, N
\triangleleft G$ e $M \cong N$ implica $G/N \cong G/M$?".

Um contraexemplo: no grupo $S_3 \times \Z_6$, os subgrupos $\{1\}\times\Z_3$ e
$A_3\times\{1\}$ são normais e isomorfos entre si, já que $A_3\cong\Z_3$. Mas:

$$(S_3\times\Z_6) / (\{1\}\times\Z_3) \cong S_3\times\Z_2,$$
$$(S_3\times\Z_6) / (A_3\times\{1\}) \cong \Z_2\times\Z_6,$$

segundo é abeliano, mas o primeiro não! Então os dois quocientes não são
isomorfos. c.n.q.d.

<!-- \end{details} -->

\

\figenv{(a parte pintada se extende infinitamente, preenchendo o
universo.)}{../cnqd.svg}{width:15em; padding-right: 3em}

\

Mais um:

@@teorema
Suponha que $H \leq G$ e $[G : H]$ é finito. O número de conjugados de $H$ é finito?
@@



