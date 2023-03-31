## Definition
Eine Sprache $L \subseteq \Sigma^*$ nennen wir **reguläre Sprache**, wenn (mindestens) einer der folgenden Punkte für sie gilt:
- Verankerung
	- $L = L_\emptyset$
	- $L = L_\varepsilon$
	- $L = \{(a) \mid a \in \Sigma\}$
- Induktion seien $L_1$ und $L_2$ reguläre Sprachen
	- $L = L_1 \cup L_2$
	- $L = L_1 \circ L_2$
	- $L = L_1^*$