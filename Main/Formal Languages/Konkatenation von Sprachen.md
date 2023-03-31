## Definition
Seien $L_1$ und $L_2$ Sprachen. 
Dann nennen wir die Verknüpfung $L_1 \circ L_2 := \{w_1 \circ w_2 \mid w_1 \in L_1, w_2 \in L_2 \}$ die *(Sprachen-) Konkatenation*  von $L_1$ und $L_2$.

Wir schreiben auch für $L_1 \circ  L_2$ verkürzend $L_1L_2$.

## Eigenschaften
Die Menge der nicht-leeren Sprachen über einem Alpabet \Sigma (d.h. $\{L \mid L \Sigma^*,L \neq \emptyset*\}$)
ist mit der Verknüpfung $\circ$ ein *Monoid* mit dem neutralen Element $L_\varepsilon$.
Das heißt es gelten folgende Eigenschaften bezüglich $\circ$:
- Assoziativität
- neutrales Element
Ferner ist $L_\emptyset$ ein auslöschendes Element, denn es gilt $L_\emptyset \circ L = L \circ L_\emptyset = L_\emptyset = \emptyset$