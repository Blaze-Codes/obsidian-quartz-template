Weiter zu: [[Phase 1]]

# Die Regel-Extraktion

## Fragen zum Beantworten
### Wann existiert ein Pokémon?
Die Frage erscheint mir etwas fragwürdig. 
Ich würde ein Interface Pokemon schreiben, welches alle Pokémon zwingend implementieren müssen. Somit kann ich auch mit instanceof checken, ob ein Objekt ein Pokémon ist.
### Was macht ein Pokémon zu einem anderen Pokémon?
Auch eine komische Frage. Ich bin mir nicht ganz sicher, was damit gemeint ist.
Ich nehme mal an, inwiefern man ein Pokémon identifizieren kann. Ein Beispiel wäre die Pokédex Nummer, die im Interface definiert sein könnte.

### Was ist fix, was ist dynamisch?
Das wären hier die Attribute für das Interface Pokemon. Hier mal eine kleine Idee:
```java
public Interface Pokemon {
	public final int dex_number; // das sollte nicht geändert werden dürfen!
	public final String name;
	public int hp;
	public int level;
	public int xp;
	public int required_xp; // xp required for level up
	public boolean capped = false; // true, if level == 100 
	private int affection; // how affected the Pokemon is to the trainer
	private boolean fainted = false; // true, if hp <= 0 -> set hp to 0
	public Status status; // current status
	public Type primary;
	public Type secondary;
	public Ability ability;
	public int stat; // stats, like atk, def, spd, sp.atk etc.
	
	enum Status{
		NONE, // default
		PARALYSIS,
		SLEEP,
		POISON,
		CHARME,
		BURN,
		FREEZE
	}
	
	enum Type{
		NONE, // only allowed if there is no secondary Type
		FIRE,
		FIGHTING,
		WATER,
		DARK,
		...
	}
	
	enum Ability{
		...
	}
	
	public int weakTo(Type attack_type) // 0 if immune, 0.5 if not effective...
	public void gainXP(int xp_gained) // calls levelUp if xp cap is completed
	public void levelUp(int leftover_xp) // updates level & do pop up
	public void damage_taken(int damage)
	public boolean hasDainted() // checks if Pokemon has fainted
}
```

### Welche Zustände sind illegal, auch wenn sie im Spiel nie vorkommen?
* 0 >= level || level > 100
* hp <= 0 & fainted == false
* primary type ist NONE oder null
* affection < 0
* keine Fähigkeit

## Ein paar Anmerkungen
Da ich das Programm in Java schreiben werde, verwende ich dementsprechend auch Java Syntax und Funktionen (z.B. der Check mit instanceof).
Außerdem, wenn eine Klasse A ein Interface I implementiert, dann implementieren auf alle Subklassen B von A das Interface. Somit gilt:
```java
B b = new B();
b instanceof I //sollte true sein
```