Geiles Projekt. 👍 Und sehr gute Haltung: **Abstraktion vor GUI**, **Originaltreue**, **intellektuelle Reibung**. Das ist genau die Art Projekt, an der man wirklich Informatik lernt.

Ich halte mich an deine Regeln: **keine Lösungen**, **keine fertigen Designs**, **keine Klassendiagramme**, nur **Aufgaben + Denkrahmen**. Hinweise nur, wenn du danach fragst.

---

## Grundprinzip für das ganze Projekt

Behandle Pokémon **nicht als Spiel**, sondern als **formales System mit Regeln**.

Dein Ziel ist nicht „spielbar“, sondern:

> _Alle Spielregeln korrekt modelliert, überprüfbar und erweiterbar._

---

## [[Phase 0]] – Regel-Extraktion (sehr wichtig)

Bevor du **eine einzige Klasse** schreibst:

👉 **Schreibe die Spielregeln auf.**  
Nicht technisch, sondern logisch.

Beispiele (nur Denkimpulse, keine Antworten):

- Wann **existiert** ein Pokémon?
    
- Was macht ein Pokémon **zu einem anderen Pokémon**?
    
- Was ist **fix**, was ist **dynamisch**?
    
- Welche Zustände sind **illegal**, auch wenn sie im Spiel nie vorkommen?
    

💡 Ziel: Du merkst schnell, dass viele Dinge, die „klar wirken“, extrem unscharf sind.

---

## [[Phase 1]] – Domänenkern (ohne Kampf!)

Ignoriere **komplett**:

- Kampf
    
- Attacken
    
- Typen
    
- Schaden
    

### Aufgabe

Modelliere **nur Existenz und Identität** eines Pokémon.

Fragen, die du dir beantworten musst (für dich, nicht mir):

- Ist ein Pokémon:
    
    - ein Objekt?
        
    - ein Zustand?
        
    - eine Entität mit Identität über Zeit?
        
- Hat ein Pokémon:
    
    - Eigenschaften, die sich nie ändern?
        
    - Eigenschaften, die sich nur unter Bedingungen ändern?
        
- Was unterscheidet:
    
    - wildes Pokémon
        
    - Trainer-Pokémon
        
    - Ei
        
    - entwickeltes Pokémon
        

🚨 Wenn du hier „alles in eine Klasse“ stecken willst → du bist zu früh im Code.

---

## [[Phase 2]] – Zustände & Invarianten

Jetzt wird’s spannend.

### Aufgabe

Definiere **Zustände**, die ein Pokémon haben kann, und **Invarianten**, die immer gelten müssen.

Beispiele für Denkfallen:

- Kann ein Pokémon **Level 0** haben?
    
- Kann ein Pokémon existieren **ohne Art**?
    
- Kann ein Pokémon gleichzeitig:
    
    - im Team **und** im PC sein?
        
- Gibt es Zustände, die nur **kurzzeitig** existieren dürfen?
    

🎯 Ziel:

> Du sollst an einen Punkt kommen, wo dein Code **Zustände verbietet**, nicht nur handhabt.

---

## [[Phase 3]] – Entwicklung (Evolution)

ORAS ist hier perfekt, weil:

- Level-Evolution
    
- Item-Evolution
    
- Tausch-Evolution
    
- Spezialfälle
    

### Aufgabe

Modelliere Entwicklung so, dass:

- sie **nicht hardcoded** ist
    
- sie **prüfbar** ist
    
- sie **scheitern kann**, ohne Seiteneffekte
    

💣 Abstraktionsbombe:

> Ist Entwicklung eine **Transformation** oder ein **Zustandswechsel**?

Diese Entscheidung beeinflusst dein gesamtes Design.

---

## [[Phase 4]] – Zeit & Ereignisse

Noch kein Kampf, aber:

### Aufgabe

Definiere, was ein **Ereignis** ist.

Beispiele:

- Level-Up
    
- Entwicklung
    
- Fang
    
- Ablage im PC
    

Fragen:

- Wer **löst** ein Ereignis aus?
    
- Wer **reagiert** darauf?
    
- Kann ein Ereignis:
    
    - rückgängig gemacht werden?
        
    - abgelehnt werden?
        

🧠 Hier trennt sich:

> „Ich programmiere ein Spiel“  
> von  
> „Ich modelliere ein System“

---

## [[Phase 5]] – Bedingungen & Regeln

Jetzt darfst du anfangen, **Bedingungen zu prüfen**.

### Aufgabe

Baue ein System, das:

- Bedingungen **formuliert**
    
- Bedingungen **prüft**
    
- Bedingungen **kombiniert**
    

Ohne `if (x && y && z)`-Monster.

💡 Denk eher in:

- Regeln
    
- Prädikaten
    
- Gültigkeitsbereichen
    

---

## Meta-Regel für dein Projekt

Wenn du dir denkst:

> „Das ist overengineered“

…dann bist du **wahrscheinlich genau richtig** für dein Lernziel.

---

## Wie wir weitermachen können

Du bestimmst den nächsten Schritt:

- 🧠 _„Ich habe Phase 1 durchdacht – überprüf meine Denkfehler“_
    
- 🧩 _„Ich hänge bei Identität vs Zustand“_
    
- ⚙️ _„Ich will anfangen zu coden, aber ohne Designfehler“_
    
- 🔥 _„Gib mir eine richtig fiese Abstraktionsfrage“_
    

Sag einfach, **wo du stehst**, und ich erhöhe gezielt den Schwierigkeitsgrad.