## Motivation
Bisher haben wir [[Sprache|Sprachen]] mathematisch als Mengen spezifiziert - z.B. durch Charakterisierung der eingeschlossenen [[Wort|Wörter]]. Das kann mitunter recht mühsam und umständlich sein sauber formal zu spezifizieren. Man hätte daher gerne eine relativ einfache  intuitiver Beschreibung einer Sprache.

## Definition
Ein **regulärer Ausdruck** ist eine Beschreibung einer [[Reguläre Sprache|regulären Sprache]].

## Syntax
Wir definieren die ***Syntax* regulärer Ausdrücke** über einem [[Alphabet]] $\Sigma$ induktiv wie folgt:
- Verankerung
	- $\emptyset$ und $\varepsilon$ sind regulüre Ausdrücke
	- $a$ ist ein regulärer Ausdruck für jedes $a \in \Sigma$
- Induktion
	- Sind $\alpha$ und $\beta$ reguläre Ausdrücke, so auch ($\alpha \cdot \beta$) und ($\alpha + \beta$)
	- Ist $\alpha$ ein regulärer Ausdruck, so auch ($\alpha^*$)

## Semantik
Wir definieren die ***Semantik* regulärer Ausdrücke** über einem Alphabet $\Sigma$ induktiv. Jedem regulärem Ausdruck $\alpha$ ist eine Sprache $L(\alpha) \subseteq \Sigma^*$ folgendermaßen zugeordnet:
- Verankerung:
	- $\mathcal{L}(\emptyset) := \mathcal{L}_\emptyset = \emptyset$
	- $\mathcal{L}(\varepsilon):= \mathcal{L}_\varepsilon = \{\varepsilon\}$
	- $\mathcal{L}(a):= \{(a)\}$ für $a \in \Sigma$
- Induktion für reguläre Ausdrücke $\alpha$ und $\beta$
	- $\mathcal{L}((\alpha^*)) := \mathcal{L}(\alpha)^*$
	- $\mathcal{L}((\alpha \cdot \beta)) := \mathcal{L}(\alpha) \circ \mathcal{L}(\beta)$
	- $\mathcal{L}((\alpha + \beta)) := \mathcal{L}(\alpha) \cup \mathcal{L}(\beta)$

## Vereinfachung der Syntax
Wir vereinbaren folgende Vereinfachungen und Operatorpräzedenzen
- Wir lassen das Zeichen $\cdot$ (für die Konkatenation) weg, d.h. wir schreiben ($\alpha \beta$) statt ($\alpha \cdot \beta$)
- $*$ bindet stärker als $\cdot$ und als $+$
- $\cdot$ bindet stärker als $+$
- Hinweis: $\cdot$ und $+$ sind assoziativ, $+$ ist zudem kommutativ (bzgl. der erzeugten Sprachen)
- Wir lassen Klammerung weg, wo dies eindeutig oder überflüssig ist.
## Reguläre Ausdrücke in der Praxis
Reguläre Ausdrücke - englisch "regular expressions" werden in der Praxis fast immer abkürzend als "regex" oder "regexp" bezeichnet.

In der Praxis verwendet man Regexes primär als Suchmuster ("pattern"). Man versucht in einem Text Stellen mit einer gewissen Struktur zu finden die durch die Regex angegeben wird.

Suchtreffer im Text, d.h. Stellen, die dem von der Regex vorgegebenem Pattern entsprechen, nennen wir "match".
Der Vorgang des Suchens nach matches wird als "matching" bezeichnet.