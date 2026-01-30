Zurück zu [[Phase 1]]
Weiter zu [[Phase 3]]

# Zustände und Invarianten

## Fragen zum Beantworten
Es geht hauptsächlich darum, Zustände, die ein Pokémon haben kann, und Invarianten, die immer gelten müssen, zu definieren. Hier ein paar Denkanstöße/-fallen:
* Kann ein Pokémon Level 0 haben? Nein. 1 <= Level <= 100
* Kann ein Pokémon existieren ohne Art? Im Sinne von Typ? Nein.
* Kann ein Pokémon gleichzeitig im Team und PC sein? Nein. Gefahr der Duplikation.
* Gibt es Zustände, die nur kurzzeitig existieren dürfen? Wetter in einem Kampf
* Solange die HP von einem Pokémon > 0 sind, ist es kampffähig.
* Es kann nicht mehr als ein Wetterzustand existieren


Ziel: Code soll bestimmte Zustände verbieten, nicht nur handhaben.

## Ein paar Anmerkungen
Überhaupt nicht einfach! Ich finde kaum etwas, aber das war auch zu erwarten lol