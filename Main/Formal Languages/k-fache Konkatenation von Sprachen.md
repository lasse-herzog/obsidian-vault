## Definition
Ist $L$ eine Sprache und $k \in \mathbb{N}$, so nennen wir $L^k := \{w_1 \circ w_2 \circ w_3 \circ \dots \circ w_k \mid w_1,w_2,\dots,w_k \in L\}$ die k-fache Konkatenation von $L$ mit sich selbst, also $L^k$
Formal, induktive Definition: $L^0 := L_\varepsilon$ und $L^i = L\circ L^{i-1}$ für $i \geq 1$.