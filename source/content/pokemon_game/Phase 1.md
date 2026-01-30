Zurück zu [[Phase 0]]
Weiter zu [[Phase 2]]

# Domänenkern

## Fragen zum Beantworten
### Ist ein Pokémon...
* ein Zustand?
* ein Objekt?
* eine Entität mit Identität über Zeit?

Ich würde sagen ein Objekt, welchen das Interface Pokemon implementiert.

### Hat ein Pokémon...
* Eigenschaften, die sich nie ändern?
	* Dex Nummer, Fähigkeiten, Typen
* Eigenschaften, die sich nur unter Bedingungen ändern?
	* Attacken (erlernen durch Item/Level up)
	* Stats (Level Up)
	* Stärke eines Angriffs durch das Wetter

### Was unterscheidet...
* wildes Pokémon
* Trainer-Pokémon
* Ei
* entwickeltes Pokémon


Man könnte einen boolean catchable machen. Falls true, dann wird es als wildes Pokemon gewertet, sonst als Trainer-Pokémon (als Trainer Pokémon zählen sowohl die Eigenen, als auch die vom gegnerischen Trainer. Man könnte das Interface für ein Ei einfach nicht verwenden. Um Eier würde ich mich sowieso erst später kümmern.
Man könnte auch einen speziellen Konstruktor für eine Entwicklung erschaffen, sodass das "alte" Pokémon übergeben wird und man alles wichtige übernimmt.


## Ein paar Anmerkungen
Auch wenn ich viel zum Thema Kampf implementiert habe, kommt dieser erst gegen Ende.
Noch weiß ich nicht genau, wie ich das mit den Klassen mache. Auch das Speichern wird schwer. Wie speichere ich, welchem Pokémon welche Dex Nummer gehört? Wie speichere ich das jetzige Team? - den Inhalt vom PC? Wie finde ich heraus, zu welchem Pokémon es bei einer Entwicklung wird? (Beispiel: Dunsparce kann auch zu Dedunsparce werden, aber Dedunsparce kommt viel später im Pokédex).