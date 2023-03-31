Ein **deterministicher endlicher Automat (DEA)** (englich **deterministic finite automaton (DFA)**) wird beschrieben durch ein Tupel ($Q, \Sigma, s, F, \sigma$), wobei gilt:
- $Q$ ist eine *endliche*, nicht-leere Menge von Zustände
- $\Sigma$ ist das zugrundeliegende Alphabet (Menge der Eingabezeichen)
- $s \in Q$ ist der Startzustand
- $F \in Q$ ist die Menge der "akzeptierenden" Zustände
- $\sigma: Q \mul \Sigma \arrowr Q$ ist die Übergangsfunktion