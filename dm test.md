...
Теорема о существовании минимального автомата.

пусть $\Phi(\alpha,q^{i}) = q^{r}$ ($r = \xi(\phi(a, q_{n(S)}))$), тогда по определению
$\Phi$ $q(a,q_{n(S)}) \in Q_{r}$
$\phi(\beta, q_{n(S)})$ и $q_{n(S)}$ - неотличимы

$$
\begin{align}

\phi(a,\phi(\beta,q_{n(S)})) = \phi(&\beta \mathfrak{A}, q_{n(S)}) \\
&\alpha \\
\phi(a, q_{n(S)}) \in \mathbb{Q}_{r}\\

\end{align}
$$
4. Докажем, что $\forall q_{i}\in Q \exists q^{i}\in Q'$
$(f_{j}^{q_{i}} \equiv f_{\mathfrak{T}}^{q^{j}})$
$$
\begin{align}

q_{i}\in Q_{j} \\
f_{\mathfrak{a}}^{q_{i}}\equiv f_{\mathfrak{a}}^{q_{n(S)}} = f_{\mathfrak{T}}^{q^{j}}
\end{align}
$$
Значит, автоматы $\mathfrak{a}$ и $\mathfrak{T}$ - эквивалентны
5. Покажем, что $\mathfrak{T}$ - минимальный
пусть $q^{i},q^{j}\in Q'(i\neq j)$
$f_{g}^{q} \equiv f_{T}^{q}$
$$
\begin{align}
f_{\mathfrak{T}}^{q^{i}} = &f_{\mathfrak{a}}^{f_{n(i)}}\in Q_{i} \\
&\neq \\
f_{\mathfrak{T}}^{q^{j}} = &f_{\mathfrak{a}}^{q_{n(j)}} \in Q_{j} \\
\end{align}
Q_{i} \neq Q_{j}
$$
чтд.

$$
Q_{1}\dots Q_{\alpha}
$$
## Автоматы как акцепторы / Распознавание слов конечными автоматами
$\mathfrak{A} = (A,B,Q,\phi,\xi)$
$f_{0}\in Q$ - начальное состояние
$D \subseteq Q$
### Определение
$U \subseteq A^{*}$ распознаётся автоматом $\mathfrak{A}$ автоматом $q_{0}$ для множества состояний $D$, тогда множество слов распознаётся 
$$
\overset{def}{\iff}
$$
$$
\begin{align}
\forall\alpha \in A^{*}(\alpha \in U\leftrightarrow \phi(\alpha,q_{0})\in D)
\end{align}
$$
### Замечание
Для обозначения автоматов, распознав. множество слов будем использовать следующую запись $\mathfrak{A}=(A,Q,\phi,q_{0},D)$
### Пример
$\mathfrak{A}\quad A=\{S,O\}; \;q_{0}$ - начальное состояние
$\alpha=\alpha'SOS\alpha''$

### Теорема
Пусть $U_{1}$  $$
\begin{cases}
U_{1} \quad \mathfrak{A}_{1}=(A,Q_{1},\phi_{1},q^{1}_{0},D_{1}) \\
U_{2} \quad \mathfrak{A}_{2}=(A,Q_{2},\phi_{2},q^{2}_{0},D_{2})
\end{cases}
$$
---
$$
\mathfrak{A}_{3}=(A,Q_{3},\phi_{3},q^{3}_{0},D_{3})
$$
$$
\begin{align}

U_{1}&\cup U_{2} \\
(U_{1}\cap U_{2}&,U_{1}\backslash U_{2})
\end{align}
$$
### Доказательство
$$
\begin{align}

\mathfrak{A}_{3}=(A,&Q_{3},\phi_{3}, (q^{1}_{0},q^{2}_{0}),) \\
Q_{1}&\times Q_{2} \\
\phi_{3}: A\times Q_{1}&\times Q_{2} \to Q_{1}\times Q_{2} \\
&{Q_{3}} \\

\end{align}
\quad
\phi(a,(q',q'')) = (\phi_{1}(a,q'),\phi_{2}(a,q''))
$$
$$
D_{3}=D_{1}\times Q_{2}\cup Q_{1}\times D_{2}
$$
Покажем, что $U_{3}$ изначального состояния $q_{0}^{1}q_{0}^{2}$ для распознающего множества $D_{3}$ $U_{1}\cup U_{2}$
$$
\begin{align}
&\alpha \in U_{3}\to\alpha \in U_{1}\cup U_{2} \\
&\alpha \in U_{1}\cup U_{2}\to\alpha \in U_{3} \\
&(U_{3}=U_{1}\cup U_{2})
\end{align}
$$
Пусть $\alpha \in U_{3}$
$\alpha \in U_{3} \implies \phi_{3}(\alpha,(q_{0}^{1},q_{0}^{2}))\in D_{3} \implies$
$\implies(\phi_{1}(\alpha,q_{0}^{1}),\phi_{2}(\alpha,q_{0}^{2}))\in D_{3}\implies(q^{1};q^{2})\in D_{1}\times Q_{2}\cup Q_{1}\times D_{2}\implies$
$\implies(q^{1},q^{2})\in D_{1}\times Q_{2}$ или $(q^{1},q^{2})\in Q_{1}\times D_{2}\implies q^{1}\in D_{1}\cup q^{2}D_{2}\implies$
$\implies\alpha \in U_{1}\cup\alpha \in U_{2}$

Если $U_{3} = U_{1}\cap U_{2}$
$D_{3}=D_{1}\times D_{2}$
Если $U_{3}=U_{1}\backslash U_{2}$
$D_{3}=D_{1}\times(Q_{2}\backslash D_{2})$


