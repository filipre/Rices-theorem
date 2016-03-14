# Rice Theorem

## Todo:

- [ ] Definition Turing Machine
- [ ] Definition Gödelnummer
- [ ] Definition Funktion total rekursiv/berechenbar
- [ ] Definition Sprache rekursiv/entscheidbar
- [ ] Satz D ist nicht rekursiv
- [ ] Korollar \overline{D} ist nicht rekursiv
- [ ] Definition Halteproblem H
- [ ] Satz H ist nicht rekursiv
- [ ] Definition Universelle Sprache U
- [ ] Satz U ist nicht rekursiv
- [ ] *(Satz U ist rekursiv aufzählbar)*
- [ ] Definition spezielles Halteproblem H_eps
- [ ] H_eps ist nicht rekursiv
- [ ] **Satz von Rice**

## Ziel und Strategie

Idee: "Many to one" Reduktion ohne Berücksichtigung von Resourcen (Zeit, Speicherplatz).

## Satz von Rice

Sei $\mathcal{R}$ die Menge der von Turingmaschinen berechenbaren Funktionen und S eine Teilmenge von $S$  mit $S \ne \emptyset$ und $S \ne \mathcal{R}$, das heißt $S$ ist eine nicht triviale Teilmenge aller berechenbaren Funktionen. Dann ist die Sprache

/[
L(S) \stackrel{\mathrm{def}}= \{\langle M \rangle | M \text{ berechnet eine Funktion aus } S\}
]/

nicht rekursiv.

### Erläuterung

| exakt | wort-wörtlich / verständlich |
|-------|---------------|
| $\mathcal{R}$: Menge der von Turingmaschinen berechenbaren Funktionen | Menge aller Funktionen, die sich in mit einer Programmiersprache programmieren lassen |
| $S$ ist eine nicht triviale Teilmenge von $R$ | $S$ ist weder leer noch gleich $R$ |
|Gödelnummer $\langle M \rangle$ | Programmcode für eine Computerprogram $M$ |
|Sprache $L(S)$ | Menge aller Programmcodes, die eine bestimmte Funktion aus $S$ berechnen |
|Sprache $L(S)$ ist nicht rekursiv| Es existiert kein (allgemeines) Computerprogramm, dass für **jeden** Programmcode <br>a) anhält ODER <br>b) sagen kann, dass der Programmcode wirklich eine Funktion aus $S$ berechnen kann.


### Warum ist $S$ eine Teilmenge von $\mathcal{R}$ und nicht ein Element (also irgendeine Funktion)?

Wir könnten $S$ so wählen, dass es nur eine Funktion beinhaltet (also die Frage: "Berechnet mein Programmcode wirklich die Funktion f?") aber der Beweis ist allgemeiner: Es ist nicht nur unentscheidbar, ob der Programmcode *genau* eine bestimmte Funktion berechnet sondern es ist *auch* unentscheidbar, selbst wenn wir weitere Funktionen hinzufügen und am Ende nicht wissen, für welche Funktion der Programmcode jetzt wirklich entscheidbar ist.

### Warum darf S nicht leer sein?

dann kann unser Checker auch für keine Funktion sich entscheiden (da ja keine Funktionen zur Auswahl stehen).

### Warum darf $S$ nicht gleich $\mathcal{R}$ sein?

Wäre $S$ gleich $\mathcal{R}$, dann gäbe es zwar ein Computerprogramm, dass uns sagt, ob $L(S)$ rekursiv (also entscheidbar) ist, aber uns nur sagt, dass unser Computerprogramm wirklich irgendeine Funktion von allen möglichen Funktionen berechnet (also die Menge nicht wirklich einschränkt).

####

## Konsequenzen

- Es ist für Programme nicht entscheidbar, ob diese eine konstante Funktion, die Nullfunktion, usw. berechnen
- Es ist für Programme nicht entscheidbar, ob sie durch die definierte Sprache endlich, leer, unendlich oder ganz \Sigma^* ist.

Es ist nur entscheidbar, dass die Sprache durch ein berechnete Funktion *berechenbar* ist

## Was dennoch geht
