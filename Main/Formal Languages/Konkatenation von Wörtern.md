## Definition
Seien $u = (a_1,a_2,\dots,a_n)$ und $v=(b_1,b_2,\dots,b_m)$ Wörter über $\Sigma$.  Die Verknüpfung
$u \circ v = (a_1,a_2,\dots,a_n,b_1,b_2,\dots,b_m)$ heißt *Konkatenation* oder Hintereinandereiung von $u$ und $v$.

Wir schreiben auch für $u \circ v$ verkürzend $uv$.

## Eigenschaften der Konkatenation
Die Menge $\Sigma^*$ ist mit der Verknüpfung $\circ$ (Konkatenation) ein *Monoid* mit
dem neutralen Element $\varepsilon$.
Das heißt es gelten folgende Eigenschaften bezüglich $\circ$:
- Assoziativität: $(u \circ v) \circ w = u \circ (c \circ w) \; \forall u,v,w \in \Sigma^*$
- neutrales Element $\varepsilon$: $\varepsilon \circ w = w = w \circ \varepsilon \; \forall w \in \Sigma^*$
