# Masterarbeit: Interaktive Lernumgebung zu Large Language Models

## Anleitung zur Benutzung

Diese Lernumgebung besteht aus zwei getrennten Jupyter-Notebooks, die aufeinander aufbauen:  
1. **Notebook 1 – Emotionserkennung mit Transformern**  
2. **Notebook 2 – Die Vorverarbeitungskette einer Texteingabe in LLMs**

Beide Notebooks sind **autonom und explorativ** konzipiert. Sie kombinieren instruktive und explorative Phasen, sind multimedial gestaltet und auf Oberstufenschüler:innen (Mathe-LK) sowie Lehramtsstudierende der Informatik ausgerichtet.

---

## Notebook 1: Emotionserkennung mit Transformern

### Einleitung
Das Notebook führt in die Anwendung von Transformer-Modellen im Bereich der Emotionserkennung ein.  
Lernende explorieren reale Modelle, vergleichen maschinelle und menschliche Erkennungsergebnisse und reflektieren ethische Implikationen.

---

### **Block 1 – Explorationsaufgaben zur Emotionserkennung**

**Kurzbeschreibung:**  
Lernende erkunden drei Modelle zur Emotionserkennung (Text, Audio, Bild), vergleichen Mensch vs. Maschine und leiten erste Ideen zum Mechanismus der Erkennung ab.

**Lernziele:**
- Modelle zur Emotionserkennung praktisch erproben und Ergebnisse reflektieren.  
- Erste konzeptionelle Brücke zum zugrunde liegenden Mechanismus schlagen (Vorwissen Richtung Self-Attention).

**Grundvorstellungen:**
- Emotionserkennung ist modalitätsübergreifend (Text/Audio/Bild) möglich und liefert auswertbare Klassifikationen.  
- Erste, vorläufige Vorstellung: Modellentscheidungen beruhen auf systematischen Merkmalen der Eingabe (Ausblick auf Self-Attention).

---

### **Block 2 – Ethische Betrachtung der Emotionserkennung**

**Kurzbeschreibung:**  
Diskussion von vier realitätsnahen Fällen mit drei klassischen Ethiken (Utilitarismus, Deontologie, Tugendethik); Ergebnisse werden festgehalten.

**Lernziele:**
- Anwendungen und Implikationen der Emotionserkennung entlang der drei Ethiken analysieren.  
- Standpunkte begründet entwickeln und dokumentieren (z. B. Gruppenpuzzle/Debatte).

**Grundvorstellungen:**
- Bewertung von KI-Einsatz erfordert normatives Abwägen (Nutzen, Pflichten/Regeln, Tugenden).  
- Technikfolgen sind kontextabhängig (Schule, Bewerbung, Unterricht, Kasse) und müssen argumentativ begründet werden.

---

### **Übergreifendes Notebook-Ziel (für N1)**  
Lernende verstehen die Anwendungsmöglichkeiten von Transformern im Rahmen der Emotionserkennung und reflektieren deren gesellschaftliche und ethische Implikationen anhand dreier klassischer Ethiken.

---

## Notebook 2: Die Vorverarbeitungskette einer Texteingabe in LLMs

### Einleitung
Dieses Notebook bildet den Weg einer Texteingabe bis zu maschinenlesbaren Einbettungsvektoren ab.  
Das **BERT-Modell** dient als Ankermodell; in den **Blöcken 1–2** wird der Prozess der **Tokenisierung** offengelegt.

---

### **Block 1 – Exploration der Vokabeltabelle**

**Kurzbeschreibung:**  
Untersuchung des Token-Vokabulars; Subword-Strukturen werden sichtbar gemacht.

**Lernziele:**
- Das Konzept „Token“ als kleinste Verarbeitungseinheit und die Rolle der Vokabeltabelle explorativ verstehen.

**Grundvorstellungen (Tokens):**
- Tokens sind die kleinsten Verarbeitungseinheiten eines LLMs, in die Eingabewörter aufgespalten werden.  
- Sie sind Bestandteil eines Vokabulars.  
- `##`-Tokens sind Stücke eines Wortes, die nicht am Wortanfang stehen.  
- Die Sondertokens `[CLS]`, `[SEP]` und `[PAD]` strukturieren den Eingabesatz.  
- Der `[UNK]`-Token dient als Platzhalter für zu lange Eingabewörter und unbekannte Symbole.  
- Tokens sind eindeutigen IDs zugeordnet.

---

### **Block 2 – Tokenisierung & WordPiece (Greedy-Longest-Match-First)**

**Kurzbeschreibung:**  
Schrittweises Nachvollziehen der Tokenisierung mit realem deutschen BERT-Modell; WordPiece-Verfahren wird erklärt.

**Lernziele:**
- Tokenisierung eigenständig durchführen.  
- WordPiece-Ablauf (Greedy Longest Match) rekonstruieren.

**Grundvorstellungen (Tokenisierung):**
- Lernende verstehen, dass die Tokenisierung der erste Schritt der Verarbeitungskette einer Texteingabe in einem LLM ist.  
- Sie wird durch einen Tokenisierer durchgeführt.  
- Es findet ein Abgleich mit einem Token-Vokabular statt.  
- Ist ein Wort nicht vorhanden, wird es so lange iterativ aufgespalten, bis das gesamte Wort gestückelt wurde.

---

### **Block 3 – Grundlagen der Vektorrechnung**

**Kurzbeschreibung:**  
Wiederholung zentraler Operationen (Betrag, Skalarprodukt, Vektoraddition) als Grundlage für Worteinbettungen.

**Lernziele:**
- Elemente eines Vektors ablesen.  
- Vektoren addieren und subtrahieren.  
- Zweidimensionale Vektoren in ein Koordinatensystem einzeichnen.  
- Den Betrag eines Vektors ermitteln.  
- Das Skalarprodukt zweier Vektoren bestimmen.

*Hinweis: Zu diesem Lernblock wurden noch keine expliziten Grundvorstellungen formuliert. Ergänzung folgt.*  
_Potentielle Herleitung: Lernende begreifen Vektoren als abstrakte Repräsentationen, auf die algebraische und geometrische Operationen angewendet werden können._

---

### **Block 4 – Worteinbettungen (Embeddings)**

**Kurzbeschreibung:**  
Von Tokens zu Vektoren – Repräsentation im semantischen Raum als Grundlage weiterer Verarbeitung.

**Lernziele:**
- Lernende verstehen das Konzept der Worteinbettungen auf mehreren Ebenen und können es erläutern, indem sie:  
  - rezitieren, dass eine Einbettung ein hochdimensionaler Vektor in Zeilenvektor-Schreibweise ist, auf dem Rechenoperationen ausgeführt werden können.  
  - erklären, wie aus einer Vokabeltabelle mithilfe der Token-ID eine Einbettung abgelesen wird.  
  - reflektieren und beispielhaft erklären, dass Einbettungen als mentale Repräsentationen von Tokens und Wörtern fungieren und semantische wie auch grammatikalische Zusammenhänge kodieren.  
  - reale Worteinbettungen im Tensor-Format explorieren.  
  - ihr Wissen zu Einbettungen auf den nachfolgenden Lernblock zur Kosinusähnlichkeit übertragen.

**Grundvorstellungen (Worteinbettungen):**
- (Wort-)Einbettungen sind hochdimensionale Vektoren im Spaltenvektor-Format.  
- Sie speichern semantische und syntaktische Eigenschaften eines Tokens.  
- Jedem Token des Vokabulars ist eine feste, eindeutige Vektorrepräsentation zugeordnet.  
- Zwischen Worteinbettungen bestehen Ähnlichkeitsbeziehungen, die ihre semantische Nähe widerspiegeln.

---

### **Block 5 – Kosinus-Ähnlichkeit & semantische Nähe**

**Kurzbeschreibung:**  
Messen semantischer Nähe zwischen Wortvektoren über die Kosinus-Ähnlichkeit.

**Lernziele:**
- Kosinus-Ähnlichkeit berechnen und interpretieren.  
- Semantische Nähe anhand geometrischer und algebraischer Zugänge diskutieren.

**Grundvorstellungen (Kosinus-Ähnlichkeit):**
- Die Kosinusähnlichkeit beschreibt die Ähnlichkeit zweier Einbettungsvektoren ausschließlich über ihren Winkel zueinander – unabhängig von ihrer Länge.  
- Sie stellt ein legitimes und anschauliches Werkzeug dar, um Bedeutungsnähe visuell zu explorieren.

---

### **Block 6 – Positional Encoding**

**Kurzbeschreibung:**  
Positionsinformation wird als Zusatzsignal eingebracht, um Reihenfolge zu kodieren.

*Hinweis: Zu diesem Lernblock wurden noch keine Grundvorstellungen formuliert. Ergänzung folgt.*  
_Potentielle Herleitung: Lernende verstehen, dass Bedeutung auch durch Reihenfolge entsteht und Positionsinformationen notwendig sind, um Satzstruktur abzubilden._

---

### **Block 7 – Quiz, Worked Example & Transferaufgabe**

**Kurzbeschreibung:**  
Überprüfen, festigen und übertragen: angeleitetes Beispiel plus eigenständige Anwendung.

*Hinweis: Lernziele und Grundvorstellungen wurden im Ergebnisteil nicht konkret formuliert. Ergänzung empfohlen.*  
_Potentielle Herleitung: Lernende wenden Konzepte der Tokenisierung und Einbettung eigenständig auf neue Sätze an, um die Transferfähigkeit zu sichern._

---

### **Block 8 – Reflexion & kognitive Belastung**

**Kurzbeschreibung:**  
Selbstreflexion zu Lernfortschritt und Beanspruchung; Passung der Instruktions-/Explorationsanteile.

**Lernziele:**
- Eigenen Lernprozess bewerten und Strategien anpassen.

**Grundvorstellungen:**
- Multimediale, explorative Elemente und klare Instruktionsschritte wirken gemeinsam lernwirksam.  
- Transparenz über Mechanismen erhöht Nachvollziehbarkeit und reduziert kognitive Belastung.

---

## Übergreifendes Ziel (für N2)
Lernende verstehen die komplette Vorverarbeitungskette einer Texteingabe – von der Tokenisierung bis zur semantischen Ähnlichkeitsmessung – und können diese auf reale LLMs übertragen.
