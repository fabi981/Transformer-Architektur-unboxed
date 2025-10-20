# Masterarbeit: Interaktive Lernumgebung zu Large Language Models

## Anleitung zur Benutzung

Diese Lernumgebung besteht aus zwei getrennten Jupyter-Notebooks, die aufeinander aufbauen:  
1. **Notebook 1 – Emotionserkennung mit Transformern**   ## 📘 Notebook 1: Emotionserkennung mit Transformern  
[![Öffnen in Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/FabianBuchheister/Transformer-Architektur-Unbox/HEAD?labpath=Notebook1.ipynb)

2. **Notebook 2 – Die Vorverarbeitungskette einer Texteingabe in LLMs**  ## 📗 Notebook 2: Die Vorverarbeitungskette einer Texteingabe in LLMs  
[![Öffnen in Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/FabianBuchheister/Transformer-Architektur-Unbox/HEAD?labpath=Notebook2.ipynb)


Beide Notebooks sind **autonom und explorativ** konzipiert.  
Sie kombinieren instruktive und explorative Phasen, sind multimedial gestaltet und auf Oberstufenschüler:innen (Mathe-LK) sowie Lehramtsstudierende der Informatik ausgerichtet.

---

## Notebook 1: Emotionserkennung mit Transformern

### Didaktische Umrahmung

**Einleitungsgeschichte:**  
Die Lernenden starten mit einem Beispiel aus ihrem Alltag: Emotionserkennung durch Maschinen.  
Sie begegnen Modellen, die Gefühle aus Text, Sprache oder Bildern erkennen können, und vergleichen diese mit der menschlichen Wahrnehmung.  
So wird Neugier geweckt und zugleich eine Brücke zu ethischen Fragen geschlagen.

**Reflexion & kognitive Belastung:**  
Am Ende des Notebooks reflektieren die Lernenden ihren Erkenntnisprozess.  
Sie analysieren, welche Darstellungsformen das Verständnis unterstützt haben und wie sich Explorations- und Instruktionsphasen auf ihre kognitive Beanspruchung ausgewirkt haben.

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

**Lernziele (1:1 aus Masterarbeit):**  
Lernende verstehen die Anwendungsmöglichkeiten von Transformern im Rahmen der Emotionserkennung und reflektieren deren gesellschaftliche und ethische Implikationen anhand drei klassischer Ethiken.

**Grundvorstellungen:**  
- Bewertung von KI-Einsatz erfordert normatives Abwägen (Nutzen, Pflichten/Regeln, Tugenden).  
- Technikfolgen sind kontextabhängig (Schule, Bewerbung, Unterricht, Kasse) und müssen argumentativ begründet werden.

---

### **Übergreifendes Notebook-Ziel (für N1)**  
Lernende verstehen die Anwendungsmöglichkeiten von Transformern im Rahmen der Emotionserkennung und reflektieren deren gesellschaftliche und ethische Implikationen anhand dreier klassischer Ethiken.

---

## Notebook 2: Die Vorverarbeitungskette einer Texteingabe in LLMs

### Didaktische Umrahmung

**Einleitungsgeschichte:**  
Die Lernenden begleiten eine Texteingabe auf ihrem Weg durch ein Sprachmodell – von Buchstaben über Tokens bis hin zu Vektoren.  
So wird der scheinbar „magische“ Vorgang der Sprachverarbeitung Schritt für Schritt transparent gemacht.

**Reflexion & kognitive Belastung:**  
Am Ende reflektieren die Lernenden, welche Teilprozesse sie am stärksten gefordert haben, und bewerten den eigenen Lernfortschritt.  
Dadurch wird die metakognitive Bewusstheit gestärkt und Überforderung reduziert.

---

### **Block 1 – Exploration der Vokabeltabelle**

**Kurzbeschreibung:**  
Untersuchung des Token-Vokabulars; Subword-Strukturen werden sichtbar gemacht.

**Lernziele (1:1 aus Masterarbeit):**  
Lernende vollziehen den Prozess der Tokenisierung nach, indem sie:  
- das Konzept des Tokens als kleinste Verarbeitungseinheit und das der Vokabeltabelle eines Transformers explorativ erfahren.

**Grundvorstellungen (1:1 aus Masterarbeit – Tokens):**  
- Tokens sind die kleinsten Verarbeitungseinheiten eines LLMs, in die Eingabewörter aufgespalten werden.  
- Sie sind Bestandteil eines Vokabulars.  
- `##`-Tokens sind dabei Stücke eines Wortes, die nicht am Wortanfang stehen.  
- Die Sondertokens `[CLS]`, `[SEP]` und `[PAD]` strukturieren den Eingabesatz.  
- Der `[UNK]`-Token dient als Platzhalter für zu lange Eingabewörter und für unbekannte Symbole.  
- Tokens sind eindeutigen IDs zugeordnet.

---

### **Block 2 – Allgemeine Tokenisierung**

**Kurzbeschreibung:**  
Schrittweises Nachvollziehen der Tokenisierung mit realem deutschen BERT-Modell.

**Lernziele (1:1 aus Masterarbeit):**  
Lernende vollziehen den Prozess der Tokenisierung nach, indem sie:  
- die Tokenisierung anhand eines realen deutschen BERT-Modells eigenständig durchführen.

**Grundvorstellungen (1:1 aus Masterarbeit – Tokenisierung):**  
- Lernende verstehen, dass die Tokenisierung der erste Schritt der Verarbeitungskette einer Texteingabe in einem LLM ist.  
- Sie wird durch einen Tokenisierer durchgeführt.  
- Es findet ein Abgleich mit einem Token-Vokabular statt.  
- Ist ein Wort nicht vorhanden, wird es so lange iterativ aufgespalten, bis das gesamte Wort gestückelt wurde.

---

### **Block 2.1 – WordPiece / Greedy-Longest-Match-First**

**Kurzbeschreibung:**  
Vertiefter Einblick in den Algorithmus der WordPiece-Tokenisierung nach Google Inc. (2018).  
Lernende durchlaufen den Original-Code, wenden das Verfahren auf eigene Eingaben an und reflektieren Sonder- und Randfälle.

**Lernziele (1:1 aus Masterarbeit):**  
Lernende vollziehen das Greedy-Longest-Match-First-Verfahren des WordPiece-Modells nach, indem sie:  
- den Original-Code der Google Inc. durchlaufen.  
- das Verfahren auf einen Eingabesatz ihrer Wahl anwenden.  
- Sonder- und Randfälle reflektieren.

**Grundvorstellungen (1:1 aus Masterarbeit):**  
- Ein häufig verwendeter Algorithmus der Tokenisierung ist Greedy-Longest-Match-First im WordPiece-Modell der Google Inc. (2018).  
- Es handelt sich um ein heuristisches Suchverfahren, das von links nach rechts nach dem längsten, im Vokabular vorhandenen Wortstück des Eingabewortes sucht.  
- Nach dem Finden eines Tokens spaltet es den Rest iterativ erneut auf.  
- Beispiele für Sonder- und Randfälle – für die der `[UNK]`-Token reserviert ist – werden reflektiert.

---

### **Block 3 – Grundlagen der Vektorrechnung**

**Kurzbeschreibung:**  
Wiederholung zentraler Operationen (Betrag, Skalarprodukt, Vektoraddition) als Grundlage für Worteinbettungen.

**Lernziele (1:1 aus Masterarbeit):**  
Lernende beherrschen die Grundlagen der Vektorrechnung. Sie können:  
- Elemente eines Vektors ablesen.  
- Vektoren addieren und subtrahieren.  
- zweidimensionale Vektoren in ein Koordinatensystem einzeichnen.  
- den Betrag eines Vektors ermitteln.  
- das Skalarprodukt zweier Vektoren ermitteln.

*Hinweis:* _Zu diesem Lernblock wurden noch keine expliziten Grundvorstellungen formuliert._  
_Potentielle Herleitung:_ Lernende begreifen Vektoren als abstrakte Repräsentationen, auf die algebraische und geometrische Operationen angewendet werden können.

---

### **Block 4 – Worteinbettungen (Embeddings)**

**Kurzbeschreibung:**  
Von Tokens zu Vektoren – Repräsentation im semantischen Raum als Grundlage weiterer Verarbeitung.

**Lernziele (1:1 aus Masterarbeit):**  
Lernende verstehen das Konzept der Worteinbettungen auf mehreren Ebenen und können es erläutern, indem sie:  
- rezitieren, dass eine Einbettung ein hochdimensionaler Vektor in Zeilenvektor-Schreibweise ist, auf dem Rechenoperationen ausgeführt werden können.  
- erklären, wie aus einer Vokabeltabelle mithilfe der Token-ID eine Einbettung abgelesen wird.  
- reflektieren und beispielhaft erklären, dass Einbettungen als mentale Repräsentationen von Tokens und Wörtern fungieren und semantische wie auch grammatikalische Zusammenhänge kodieren.  
- reale Worteinbettungen im Tensor-Format explorieren.  
- ihr Wissen zu Einbettungen auf den nachfolgenden Lernblock zur Kosinusähnlichkeit übertragen.

**Grundvorstellungen (1:1 aus Masterarbeit):**  
- (Wort-)Einbettungen sind hochdimensionale Vektoren im Spaltenvektor-Format.  
- Sie speichern semantische und syntaktische Eigenschaften eines Tokens.  
- Jedem Token des Vokabulars ist eine feste, eindeutige Vektorrepräsentation zugeordnet.  
- Zwischen Worteinbettungen bestehen Ähnlichkeitsbeziehungen, die ihre semantische Nähe widerspiegeln.  
- Semantische Nähe kann sich beispielsweise darin ausdrücken, dass sich Wörter taxonomisch, thematisch oder grammatikalisch nahestehen oder häufig im gleichen Kontext vorkommen.

---

### **Block 5 – Kosinus-Ähnlichkeit & semantische Nähe**

**Kurzbeschreibung:**  
Messen semantischer Nähe zwischen Wortvektoren über die Kosinus-Ähnlichkeit.

**Lernziele (1:1 aus Masterarbeit):**  
- Kosinus-Ähnlichkeit berechnen und interpretieren.  
- Semantische Nähe anhand geometrischer und algebraischer Zugänge diskutieren.

**Grundvorstellungen (1:1 aus Masterarbeit):**  
- Die Kosinusähnlichkeit beschreibt die Ähnlichkeit zweier Einbettungsvektoren ausschließlich über ihren Winkel zueinander – unabhängig von ihrer Länge.  
- Sie stellt ein legitimes und anschauliches Werkzeug dar, um Bedeutungsnähe visuell zu explorieren.

---

### **Block 6 – Positional Encoding**

**Kurzbeschreibung:**  
Positionsinformation wird als Zusatzsignal eingebracht, um Reihenfolge zu kodieren.

*Hinweis:* _Zu diesem Lernblock wurden noch keine Grundvorstellungen formuliert._  
_Potentielle Herleitung:_ Lernende verstehen, dass Bedeutung auch durch Reihenfolge entsteht und Positionsinformationen notwendig sind, um Satzstruktur abzubilden.

---

### **Block 7 – Quiz, Worked Example & Transferaufgabe**

**Kurzbeschreibung:**  
Überprüfen, festigen und übertragen: angeleitetes Beispiel plus eigenständige Anwendung.

*Hinweis:* _Lernziele und Grundvorstellungen wurden im Ergebnisteil nicht konkret formuliert._  
_Potentielle Herleitung:_ Lernende wenden Konzepte der Tokenisierung und Einbettung eigenständig auf neue Sätze an, um Transferfähigkeit zu sichern.

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
