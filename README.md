# Masterarbeit: Interaktive Lernumgebung zu Large Language Models

## Anleitung zur Benutzung

Diese Lernumgebung besteht aus zwei getrennten Jupyter-Notebooks, die aufeinander aufbauen:  
1. **Notebook 1 – Emotionserkennung mit Transformern**  [![Öffnen in Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/fabi981/Transformer-Architektur-unboxed/HEAD?labpath=Notebook%201%20-%20Exploration%20von%20Transformern%20im%20Rahmen%20der%20Emoionserkennung.ipynb)

2. **Notebook 2 – Die Vorverarbeitungskette einer Texteingabe in LLMs**  [![Öffnen in Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/FabianBuchheister/Transformer-Architektur-Unbox/HEAD?labpath=Notebook%202%20-%20Eine%20Erkundung%20der%20Eingabeverarbeitung%20von%20Transformern.ipynb)

Beide Notebooks sind **autonom und explorativ** konzipiert.  
Sie kombinieren instruktive und explorative Phasen, sind multimedial gestaltet und auf Oberstufenschüler:innen (Mathe-LK) sowie Lehramtsstudierende der Informatik ausgerichtet.

## Notebook 1: Emotionserkennung mit Transformern

**Idee der Einleitung und der Umrahmung:**  
Die Lernenden starten mit einem Beispiel aus ihrem Alltag: Emotionserkennung durch die Transformer-Technologie.  
Sie begegnen Modellen, die Gefühle aus Text, Sprache oder Bildern erkennen können, und vergleichen diese mit der menschlichen Wahrnehmung.  
So wird Neugier auf die Architektur geweckt und zugleich eine Brücke zu ethischen Fragen geschlagen.

**Übergreifendes Lernziel dieses Notebooks**  
Lernende verstehen die Anwendungsmöglichkeiten von Transformern im Rahmen der Emotionserkennung und reflektieren deren gesellschaftliche und ethische Implikationen anhand dreier klassischer Ethiken.

--
### **Block 1 – Explorationsaufgaben zur Emotionserkennung**

**Kurzbeschreibung:**  
Lernende erkunden drei Modelle zur Emotionserkennung (Text, Audio, Bild), vergleichen Mensch vs. Maschine und leiten erste Ideen zum Mechanismus der Erkennung ab. Diese bieten Anschluss an eine breite Palette an Themen wie der Eingabeverarbeitung und der Self-Attention eines Transformers.

**Explorierte Modelle:**
https://huggingface.co/spaces/ElenaRyumina/Facial_Expression_Recognition bzw. https://huggingface.co/ElenaRyumina/face_emotion_recognition bzw. https://github.com/ElenaRyumina/EMO-AffectNetModel

Die Deep-Residual-Learning Architektur (https://github.com/ox-vgg/vgg_face2) wurde auf einen Datensatz mit über 3 Millionen Bildern angewendet, um akkurat Emotionen aus Bildern auslesen zu können. Es handelt sich um eine der Vorgänger-Architekturen der Transformers - es bereits Residual Connections verwendet. Diese dienen der Verbindung der Encoder-Schichten eines Transformers und des Ausführens von Linearen Transformationen und Layernormalisierungen im Rahmen der Self-Attention.  

https://huggingface.co/spaces/Dpngtm/Audio-Emotion-Recognition bzw. https://huggingface.co/Dpngtm/wav2vec2-emotion-recognition

Dieses Wav2Vec2-Modell kann bis zu sieben Emotionen in Sprachdateien erkennen.

https://huggingface.co/ChrisLalk/German-Emotions

Es handelt sich um ein FacebookAI-Roberta-base-Modell (also ein von MetaAI optimiertes BERT) und wurde feintrainiert, 27 verschiedene Emotionen aus deutschen Texten im String-Format abzulesen und zu unterscheiden.

Alle drei Modelle basieren auf großen vortrainierten Architekturen (pre-trained) und wurden von ihrer Veröffentlicher:in feintrainiert (finetuned).

**Lernziele:**  
- Modelle zur Emotionserkennung praktisch erproben und die Ergebnisse reflektieren.  
- Erste konzeptionelle Brücke zum zugrunde liegenden Mechanismus schlagen (Vorwissen Richtung Self-Attention).

**Grundvorstellungen:**  
- Emotionserkennung ist modalitätsübergreifend (Text/Audio/Bild) möglich und liefert auswertbare Klassifikationen.  
- Erste, vorläufige Vorstellung: Modellentscheidungen beruhen auf systematischen Merkmalen der Eingabe (Ausblick auf Self-Attention).

**Anschlusskonzepte:**
- Tokenisierung, Worteinbettungen, Self-Attention

---

### **Block 2 – Ethische Betrachtung der Emotionserkennung**

**Kurzbeschreibung:**  
Vier reale oder realitätsnahe Fälle der Anwendung von Transformer-Technologien werden mit mit drei klassischen Ethiken (Utilitarismus, Deontologie, Tugendethik) analysiert. Die Ergebnisse werden in einem Padlet festgehalten.

**Lernziele:**  
Lernende verstehen die Anwendungsmöglichkeiten von Transformern im Rahmen der Emotionserkennung und reflektieren deren gesellschaftliche und ethische Implikationen anhand drei klassischer Ethiken.

**Grundvorstellungen:**  
- Die Bewertung des Einsatzes von KI erfordert normatives Abwägen (Nutzen, Pflichten/Regeln, Tugenden).  
- Technikfolgen sind kontextabhängig (Schule, Bewerbung, Unterricht, Kasse) und müssen argumentativ begründet werden.

---

## Notebook 2: Die Vorverarbeitungskette einer Texteingabe in LLMs

**Idee der Einleitung und Umrahmung:**  
Die Lernenden begleiten eine Texteingabe auf ihrem Weg durch ein Sprachmodell – von Buchstaben über Tokens bis hin zu Vektoren.  
So wird der scheinbar „magische“ Vorgang der Sprachverarbeitung Schritt für Schritt transparent gemacht.

**Übergreifendes Lernziel dieses Notebooks**:

Lernende verstehen die komplette Vorverarbeitungskette einer Texteingabe – von der Tokenisierung bis zur semantischen Ähnlichkeitsmessung – und können diese auf reale LLMs übertragen.

**Reflexion & kognitive Belastung:**  
Am Ende reflektieren die Lernenden, welche Teilprozesse sie am stärksten gefordert haben, und bewerten den eigenen Lernfortschritt.  
Dadurch wird die metakognitive Bewusstheit gestärkt und Überforderung reduziert.

---

### **Block 1 – Exploration der Vokabeltabelle**

**Kurzbeschreibung:**  
Untersuchung des Token-Vokabulars; Subword-Strukturen werden sichtbar gemacht.

**Lernziele:**  
Lernende vollziehen den Prozess der Tokenisierung nach, indem sie:  
- das Konzept des Tokens als kleinste Verarbeitungseinheit und das der Vokabeltabelle eines Transformers explorativ erfahren.

**Grundvorstellungen:**  
- Tokens sind die kleinsten Verarbeitungseinheiten eines LLMs, in die Eingabewörter aufgespalten werden.  
- Sie sind Bestandteil eines Vokabulars.  
- `##`-Tokens sind dabei Stücke eines Wortes, die nicht am Wortanfang stehen.  
- Die Sondertokens `[CLS]`, `[SEP]` und `[PAD]` strukturieren den Eingabesatz.  
- Der `[UNK]`-Token dient als Platzhalter für zu lange Eingabewörter und für unbekannte Symbole.  
- Tokens sind eindeutigen IDs zugeordnet.

---

### **Block 2 – Tokenisierung**

**Kurzbeschreibung:**  
Schrittweises Nachvollziehen der Tokenisierung mit realem deutschen BERT-Modell.

**Konzepte:**
- Token, Tokenisierung, strukturbildende Sondertokens, [UNK]-Token

**Lernziele:**  
Lernende vollziehen den Prozess der Tokenisierung nach, indem sie:  
- die Tokenisierung anhand eines realen deutschen BERT-Modells eigenständig durchführen.

**Grundvorstellungen:**  
- Lernende verstehen, dass die Tokenisierung der erste Schritt der Verarbeitungskette einer Texteingabe in einem LLM ist.  
- Sie wird durch einen Tokenisierer durchgeführt.  
- Es findet ein Abgleich mit einem Token-Vokabular statt.  
- Ist ein Wort nicht vorhanden, wird es so lange iterativ aufgespalten, bis das gesamte Wort gestückelt wurde (oder ein Randfall auftritt).

---

### **Block 2.1 – WordPiece / Greedy-Longest-Match-First**

**Kurzbeschreibung:**  
Vertiefter Einblick in den Algorithmus der WordPiece-Tokenisierung nach Google Inc. (2018).  
Lernende durchlaufen den Original-Code, wenden das Verfahren auf eigene Eingaben an und reflektieren Sonder- und Randfälle.

**Konzepte:**
- Tokenisierung, [UNK]-Token, WordPiece, Greedy-Longest-Match-First

**Lernziele:**  
Lernende vollziehen das Greedy-Longest-Match-First-Verfahren des WordPiece-Modells nach, indem sie:  
- den Original-Code der Google Inc. durchlaufen.  
- das Verfahren auf einen Eingabesatz ihrer Wahl anwenden.  
- Sonder- und Randfälle reflektieren.

**Grundvorstellungen:**  
- Ein häufig verwendeter Algorithmus der Tokenisierung ist Greedy-Longest-Match-First im WordPiece-Modell der Google Inc. (2018).  
- Es handelt sich um ein heuristisches Suchverfahren, das von links nach rechts nach dem längsten, im Vokabular vorhandenen Wortstück des Eingabewortes sucht.  
- Nach dem Finden eines Tokens spaltet es den Rest iterativ erneut auf.  
- Beispiele für Sonder- und Randfälle – für die der `[UNK]`-Token reserviert ist – werden reflektiert.

---

### **Block 3 – Grundlagen der Vektorrechnung**

**Kurzbeschreibung:**  
Wiederholung zentraler Operationen (Betrag, Skalarprodukt, Vektoraddition) als Grundlage für Worteinbettungen.

**Konzepte:**
- (Spalten-)Vektoren, Vektoraddition und -subtraktion, Betrag eines Vektors, Skalarprodukt (geometrisch und algebraisch)

**Lernziele:**  
Lernende beherrschen die Grundlagen der Vektorrechnung. Sie können:  
- Elemente eines Vektors ablesen.  
- Vektoren addieren und subtrahieren.  
- zweidimensionale Vektoren in ein Koordinatensystem einzeichnen.  
- den Betrag eines Vektors ermitteln.  
- das Skalarprodukt zweier Vektoren ermitteln.

**Grundvorstellungen:**  
- Die grundlegende Darstellungsweise von Informationen in Transformern sind Einbettungsvektoren.
- Interne Mechanismen eines Transformers verwenden grundlegende Vektor-Operationen wie die Vektor-Addition und das Skalarprodukt.
- Für das Skalarprodukt existiert eine geometrische und eine algebraische Formel, die für das Verständnis von Worteinbettungen und der semantischen Nähe nützlich sind.

---

### **Block 4 – Worteinbettungen (Embeddings)**

**Kurzbeschreibung:**  
Von Tokens zu Vektoren – Repräsentation im semantischen Raum als Grundlage weiterer Verarbeitung.

**Konzepte:**
- 

**Lernziele:**  
Lernende verstehen das Konzept der Worteinbettungen auf mehreren Ebenen und können es erläutern, indem sie:  
- rezitieren, dass eine Einbettung ein hochdimensionaler Vektor in Zeilenvektor-Schreibweise ist, auf dem Rechenoperationen ausgeführt werden können.  
- erklären, wie aus einer Vokabeltabelle mithilfe der Token-ID eine Einbettung abgelesen wird.  
- reflektieren und beispielhaft erklären, dass Einbettungen als mentale Repräsentationen von Tokens und Wörtern fungieren und semantische wie auch grammatikalische Zusammenhänge kodieren.  
- reale Worteinbettungen im Tensor-Format explorieren.  
- ihr Wissen zu Einbettungen auf den nachfolgenden Lernblock zur Kosinusähnlichkeit übertragen.

**Grundvorstellungen:**  
- (Wort-)Einbettungen sind hochdimensionale Vektoren im Spaltenvektor-Format.  
- Sie speichern semantische und syntaktische Eigenschaften eines Tokens.  
- Jedem Token des Vokabulars ist eine feste, eindeutige Vektorrepräsentation zugeordnet.  
- Zwischen Worteinbettungen bestehen Ähnlichkeitsbeziehungen, die ihre semantische Nähe widerspiegeln.  
- Semantische Nähe kann sich beispielsweise darin ausdrücken, dass sich Wörter taxonomisch, thematisch oder grammatikalisch nahestehen oder häufig im gleichen Kontext vorkommen.

---

### **Block 5 – Kosinus-Ähnlichkeit & semantische Nähe**

**Kurzbeschreibung:**  
Messen semantischer Nähe zwischen Wortvektoren über die Kosinus-Ähnlichkeit.

**Konzepte:**
- Die Kosinus-Ähnlichkeit als anschauliches Maß der semantischen Nähe von Einbettungen

**Lernziele:**  
- Kosinus-Ähnlichkeit berechnen und interpretieren.  
- Semantische Nähe anhand geometrischer und algebraischer Zugänge diskutieren.

**Grundvorstellungen:**  
- Die Kosinusähnlichkeit beschreibt die Ähnlichkeit zweier Einbettungsvektoren ausschließlich über ihren Winkel zueinander – unabhängig von ihrer Länge.  
- Sie stellt ein legitimes und anschauliches Werkzeug dar, um Bedeutungsnähe visuell zu explorieren.

---

### **Angedachter Block 6 – Positional Encoding**

**Kurzbeschreibung:**  
Positionsinformation wird als Zusatzsignal eingebracht, um Reihenfolge zu kodieren.

*Zu diesem Lernblock wurden noch keine Grundvorstellungen formuliert.*  


---

### **Angedachter Block 7 - Worked Examples**

**Kurzbeschreibung:**  
Überprüfen, festigen und übertragen: angeleitetes Beispiel plus eigenständige Anwendung.

*Zu diesem Lernblock wurden noch keine Grundvorstellungen formuliert.* 

---
