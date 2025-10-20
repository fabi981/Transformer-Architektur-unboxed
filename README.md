# Masterarbeit: Interaktive Lernumgebung zu Large Language Models

## Anleitung zur Benutzung
<!-- (Platzhalter – füllst du selbst aus) -->

---

## Notebook 1: Emotionserkennung mit Transformern

### Einleitung
<!-- (nur Überschrift, kein Inhalt) -->

### Lernblöcke

#### Block 1 – Explorationsaufgaben zur Emotionserkennung
**Kurzbeschreibung:** Lernende erkunden drei Modelle zur Emotionserkennung (Text, Audio, Bild), vergleichen Mensch vs. Maschine und leiten erste Ideen zum Mechanismus der Erkennung ab.   
**Lernziele:**
- Modelle zur Emotionserkennung praktisch erproben und Ergebnisse reflektieren. 
- Erste konzeptionelle Brücke zum zugrunde liegenden Mechanismus schlagen (Vorwissen Richtung Self-Attention). 
**Grundvorstellungen:**
- Emotionserkennung ist modalitätsübergreifend (Text/Audio/Bild) möglich und liefert auswertbare Klassifikationen. 
- Erste, vorläufige Vorstellung: Modellentscheidungen beruhen auf systematischen Merkmalen der Eingabe (Ausblick auf Self-Attention). 

#### Block 2 – Ethische Betrachtung der Emotionserkennung
**Kurzbeschreibung:** Diskussion von vier realitätsnahen Fällen mit drei klassischen Ethiken (Utilitarismus, Deontologie, Tugendethik); Ergebnisse werden festgehalten.   
**Lernziele:**
- Anwendungen und Implikationen der Emotionserkennung entlang der drei Ethiken analysieren. 
- Standpunkte begründet entwickeln und dokumentieren (z. B. Gruppenpuzzle/Debatte). 
**Grundvorstellungen:**
- Bewertung von KI-Einsatz erfordert normatives Abwägen (Nutzen, Pflichten/Regeln, Tugenden). 
- Technikfolgen sind kontextabhängig (Schule, Bewerbung, Unterricht, Kasse) und müssen argumentativ begründet werden. 

**Übergreifendes Notebook-Ziel (für N1):** Anwendungen von Transformern in der Emotionserkennung verstehen und die gesellschaftlich-ethischen Implikationen reflektieren. 

---

## Notebook 2: Die Vorverarbeitungskette einer Texteingabe in LLMs

### Einleitung
<!-- (nur Überschrift, kein Inhalt) -->

> **Hinweis:** Das Notebook bildet die Schritte bis zu maschinenlesbaren Einbettungsvektoren ab; BERT dient als Ankermodell; Ziele in Blöcken 1–2: Tokenisierung offenlegen und nachvollziehen. 

### Lernblöcke

#### Block 1 – Exploration der Vokabeltabelle
**Kurzbeschreibung:** Untersuchung des Token-Vokabulars; Subword-Strukturen werden sichtbar gemacht.   
**Lernziele:**
- Das Konzept „Token“ als kleinste Verarbeitungseinheit und die Rolle der Vokabeltabelle explorativ verstehen. 
**Grundvorstellungen (Tokens):**
- Tokens sind kleinste Verarbeitungseinheiten und Teil eines Vokabulars; Sonderformen: `##`-Subtokens (nicht am Wortanfang), [CLS], [SEP], [PAD], [UNK]; jedem Token ist eine ID zugeordnet. 

#### Block 2 – Tokenisierung & WordPiece (Greedy-Longest-Match-First)
**Kurzbeschreibung:** Schrittweises Nachvollziehen der Tokenisierung mit realem deutschen BERT-Modell; WordPiece-Verfahren wird erklärt.   
**Lernziele:**
- Tokenisierung eigenständig durchführen; WordPiece-Ablauf (Greedy Longest Match) rekonstruieren. 
**Grundvorstellungen (Tokenisierung):**
- Tokenisierung ist der erste Schritt der Verarbeitungskette; erfolgt durch einen Tokenizer via Vokabularabgleich (inkl. Greedy-Verfahren) und Einfügung von Sondertokens zur Sequenzstrukturierung. 

#### Block 3 – Worteinbettungen (Embeddings)
**Kurzbeschreibung:** Von Tokens zu Vektoren: Repräsentation im semantischen Raum als Grundlage weiterer Verarbeitung. (Notebook-Zielsetzung nennt Einbettungen explizit.)   
**Lernziele:**
- Den Übergang von diskreten Tokens zu kontinuierlichen Vektoren erläutern. 
**Grundvorstellungen:**
- Bedeutung wird als numerische Repräsentation in Vektorräumen modelliert (Einbettungsvektoren als „mentale“ Stellvertreter). 

#### Block 4 – Kosinus-Ähnlichkeit & semantische Nähe
**Kurzbeschreibung:** Messen semantischer Nähe zwischen Wortvektoren über die Kosinus-Ähnlichkeit. (Explizit als zentrales Konzept benannt.)   
**Lernziele:**
- Kosinus-Ähnlichkeit berechnen und interpretieren; semantische Nähe diskutieren. 
**Grundvorstellungen:**
- Ähnlichkeit ergibt sich aus dem Winkel zwischen Vektoren (unabhängig von ihrer Länge); semantische Beziehungen sind quantitativ erfassbar. 

#### Block 5 – Positional Encoding
**Kurzbeschreibung:** Positionsinformation wird als Zusatzsignal in die Repräsentation eingebracht, um Reihenfolge zu kodieren. (Als Bestandteil der Vorverarbeitung genannt.)   
**Lernziele:**
- Zweck von Positionskodierungen erklären und deren Rolle für Satzstruktur einordnen. 
**Grundvorstellungen:**
- Bedeutung entsteht auch durch Reihenfolge; Positionsinformationen sind notwendig, um Sequenzstruktur abzubilden. 

#### Block 6 – Quiz, Worked Example & Transferaufgabe
**Kurzbeschreibung:** Überprüfen, festigen und übertragen: angeleitetes Beispiel plus eigenständige Anwendung. (Im Notebook als didaktische Elemente vorgesehen.)   
**Lernziele:**
- Gelerntes anwenden, festigen und auf neue Beispiele übertragen. 
**Grundvorstellungen:**
- Verständnissicherung gelingt über gestufte Aufgabenformate (Instruktion → Exploration → Transfer). 

#### Block 7 – Reflexion & kognitive Belastung
**Kurzbeschreibung:** Selbstreflexion zu Lernfortschritt und Beanspruchung; Passung der Instruktions-/Explorationsanteile. (Kombination aus SEASIDE/MASL/Instruktion als Leitidee.)   
**Lernziele:**
- Eigenen Lernprozess bewerten und Strategien anpassen. 
**Grundvorstellungen:**
- Multimediale, explorative Elemente und klare Instruktionsschritte wirken gemeinsam lernwirksam; Transparenz über Mechanismen erhöht Nachvollziehbarkeit. 


