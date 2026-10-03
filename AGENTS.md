# AGENTS.md – Dateninfrastruktur-Übersicht mit draw.io

## 1. Auftrag und Zielgruppe

Erstelle und bearbeite eine allgemeinverständliche, funktionale Übersicht der
Dateninfrastruktur. Die Darstellung dient als Gesprächsgrundlage mit Fachstellen,
Controlling und weiteren möglichen Service-Kunden. Sie soll erklären, **was ein
Baustein ermöglicht**, nicht primär, welches Produkt oder welcher Server dahintersteht.

BI ist eine mögliche Nutzung der Dateninfrastruktur. Die Infrastrukturübersicht ist
weder mit dem BI-Service gleichzusetzen noch bereits ein zugesichertes Leistungsangebot.
Anforderungen, BI-Beiträge und organisatorische Zuständigkeiten werden schrittweise
geklärt und ergänzt.

Diese Datei definiert Zeichen- und Bearbeitungsregeln, **keine fertige Architektur**.
Erzeuge oder erweitere ein Diagramm erst aufgrund eines entsprechenden Arbeitsauftrags.

## 2. Fachliche Grundlage und Arbeitsumfang

- Verwende die aktuellen Nutzeranweisungen und die ausdrücklich bezeichneten
  Projektunterlagen als fachliche Grundlage. Lies relevante Dateien, bevor du ihre
  Inhalte darstellst. Behaupte nicht, nicht zugängliche Unterlagen gelesen zu haben.
- Übernimm Begriffe und Aussagen der Quellen. Löse Widersprüche zwischen Entwürfen
  nicht stillschweigend auf. Benenne fachlich relevante Unklarheiten.
- Ergänze keine Komponenten, Produkte, Datenflüsse, Anforderungen, Zuständigkeiten oder
  Betriebszusagen allein deshalb, weil sie in einer typischen BI-Architektur vorkommen.
  Gewünschte eigene Vorschläge müssen als Vorschläge erkennbar sein.
- Ein funktionaler Baustein muss nicht genau einem Softwareprodukt entsprechen.
  Vermische die funktionale Übersicht nicht ungefragt mit einer Deployment-,
  Netzwerk-, Prozess- oder detaillierten Datenmodellansicht.
- Unterscheide technische Möglichkeiten von tatsächlich angebotenen Dienstleistungen.
  Zeichne fachliche und organisatorische Arbeit nicht so, als würde Software sie
  automatisch vollständig erledigen.
- Beginne bei einer neuen Übersicht grundsätzlich mit der Grundübersicht. Ergänze
  BI-Verweise und Rollen erst, wenn sie beauftragt und inhaltlich ausreichend geklärt sind.
- Behandle fachliche Beschreibung und Darstellungsregeln getrennt. Nutze vorhandene
  Beschreibungsdateien; mache diese AGENTS.md nicht zum Komponenten- oder Leistungskatalog.
- Stelle Rückfragen bei inhaltlich folgenreichen Lücken. Triff kleine, reversible
  Layoutentscheidungen selbst, statt jede Position bestätigen zu lassen.

## 3. Zeichensprache

Die folgende Zuordnung ist unsere Projektkonvention, keine vollständige UML-,
ArchiMate- oder C4-Notation. Verwende möglichst wenige unterschiedliche Formen.

| Element | Bedeutung | Abgrenzung |
| --- | --- | --- |
| Leicht abgerundetes Rechteck | Funktionaler Baustein: erledigt eine Aufgabe oder ermöglicht eine Nutzung. | Standardform. Nicht automatisch ein einzelnes Produkt, ein Server oder ein Prozessschritt. |
| Zylinder / Datenbanksymbol | Gespeicherter Datenbestand oder Datenablage. | Nicht auf relationale Datenbanken beschränkt. Berechnen, Suchen oder Visualisieren ist allein noch kein Grund für einen Zylinder. |
| Dokument mit umgeknickter Ecke | Konkrete Datei oder Informationsartefakt, etwa eine Lieferung, ein Modell oder ein Bericht. | Nur zeigen, wenn dieses Artefakt für das Verständnis wichtig ist. Die Funktion zur Berichtserstellung bleibt ein Rechteck. |
| Grosser, dezenter rechteckiger Rahmen | Funktionale Gruppierung oder ausdrücklich bezeichnete Systemgrenze. | Hintergrundelement, nicht automatisch eine weitere Komponente. Titel muss den Gruppierungsgrund bzw. die Grenze erklären. |
| Einfaches Personensymbol mit Beschriftung | Nutzende oder Nutzergruppe. | Nicht als Ersatz für eine unklare Verantwortungszuordnung verwenden. |
| Kleiner Kreis mit Nummer | Verweis auf eine erläuterte BI-Aufgabe oder Leistung. | Kein automatischer Hinweis auf Reihenfolge, Priorität oder Ausbaustufe. |

Weitere Regeln:

- Verwende native, einzeln bearbeitbare draw.io-Formen, Texte und Verbinder.
- Nutze Rechtecke als Standard; verwende Sonderformen nur bei einer tatsächlichen
  zusätzlichen Aussage. Keine dekorativen Server-, Cloud- oder Produktbilder.
- Zeige interne Speicher einer Komponente nicht zusätzlich, wenn sie für die gewählte
  funktionale Sicht keine eigenständige Aussage beitragen.
- Platziere Gruppierungsrahmen hinter ihren Inhalten und beschrifte sie oben links.
  Verbinde Pfeile grundsätzlich mit den enthaltenen Komponenten, nicht mit dem Rahmen.
- Vermeide unnötige Verschachtelung. Eine Gruppierungsfläche und eine Zeichenebene
  haben unterschiedliche Zwecke; verwechsle sie nicht.
- Querschnittsaufgaben dürfen in einem separaten Bereich mit dem Hinweis
  «Gilt übergreifend» stehen. Zeichne nicht allein deshalb Pfeile zu jedem Baustein.
- Halte eine kleine Legende vor. Erkläre die tatsächlich verwendeten Symbole,
  Linienarten, Nummern und Statusangaben. Führe keine ungenutzten Zeichentypen auf.

## 4. Beziehungen und Pfeile

### 4.1 Durchgezogener Pfeil: Datenfluss

- Bedeutung: Daten oder Informationen werden in Pfeilrichtung weitergegeben bzw.
  bereitgestellt. Richtung immer **von der Quelle zum Empfänger**.
- Beschrifte damit, was fliesst, beispielsweise «Rohdaten», «geprüfte Daten» oder
  «Auswertungsergebnisse». Beispiele sind keine vorgegebenen Projektinhalte.
- Ein lesender Zugriff wird in dieser Sicht durch die Richtung der gelieferten Daten
  erklärt, nicht durch die entgegengesetzte technische Anfrage.
- Ein Datenflusspfeil bedeutet nicht automatisch eine neue dauerhafte Datenkopie,
  einen bestimmten Übertragungsweg oder eine bestimmte Aktualisierungshäufigkeit.
  Halte diese Abstraktion in der Legende fest.

### 4.2 Gestrichelter Pfeil: Nutzung einer unterstützenden Funktion oder Definition

- Führe diese zweite Linienart nur ein, wenn die Unterscheidung benötigt wird.
- Bedeutung: Der Ausgangsbaustein verwendet den Zielbaustein bzw. dessen Definitionen.
  Richtung **vom nutzenden zum genutzten Baustein**.
- Beschrifte mit einer konkreten Beziehung, beispielsweise
  «verwendet Kennzahlendefinitionen». «Ist verbunden mit» genügt nicht.
- Erkläre die andere Semantik gegenüber dem Datenfluss in der Legende.
- Verwende dieselbe Linienart nicht gleichzeitig für «geplant», «optional» oder
  «organisatorisch zuständig».

### 4.3 Darstellung und Linienführung

- Verwende echte, an den Formen angeschlossene Verbinder, keine freistehenden
  Blockpfeile und keine bloss gezeichneten Linien ohne Bezug zu ihren Endpunkten.
- Bevorzuge rechtwinklige Verbinder, dünne Linien und kleine Pfeilspitzen am Ziel.
- Beschrifte Beziehungen eindeutig und passend zu ihrer Richtung.
- Vermeide Doppelpfeile. Zeige zwei Richtungen nur, wenn beide eine relevante und
  beschreibbare Bedeutung haben; verwende dann vorzugsweise zwei beschriftete Verbinder.
- Führe Linien nicht durch Texte oder unbeteiligte Komponenten. Reduziere Kreuzungen
  und unnötige Knicke. Platziere Beschriftungen mit Abstand zu Pfeilspitzen und Knoten.
- Ergänze keine Pfeile nur, um eine vermeintlich vollständige Architektur zu erhalten.
  Keine dritte Pfeilsemantik ohne sachlichen Bedarf und entsprechende Legende.

## 5. Beschriftung und Gestaltung

### Inhalt der Bausteine

- Verwende verständliche deutsche Funktionsnamen als Titel.
- Ergänze eine kurze Beschreibung: Welche Aufgabe erfüllt der Baustein oder welchen
  Nutzen ermöglicht er? Ziel sind ein bis zwei gut lesbare Zeilen.
- Produktnamen sind optional und visuell nachgeordnet. Das Verständnis darf nicht
  von Produktkenntnissen abhängen.
- Verwende Schweizer Rechtschreibung mit «ss» statt «ß» und normale Umlaute.
- Verzichte auf unnötige Abkürzungen, Marketingformulierungen, zusätzliche
  Mini-Überschriften und wiederholte Erklärungen.
- Erhalte fachliche Bedeutung bei Textkürzungen. Verschiebe ausführliche Erläuterungen
  gegebenenfalls in die begleitende Beschreibung, statt sie unlesbar zu verkleinern.

### Visueller Stil

- Seriös, ruhig und übersichtlich: weisser Hintergrund, dunkle Schrift, dezente
  Grautöne, wenige visuelle Akzente.
- Reserviere eine einzige Akzentfarbe für die BI-Nummern; bevorzugt ein gut lesbares
  Rot. Farben sind keine zusätzliche, unbeschriftete Fachsemantik.
- Keine Schatten, Verläufe, 3D-Effekte oder ungefragten Produktlogos.
- Verwende keine nachgezeichneten oder erfundenen Kantonslogos. Nutze ein Logo nur,
  wenn es ausdrücklich gewünscht und als passende Originaldatei verfügbar ist.
- Nutze eine einheitliche, lokal verfügbare serifenlose Schrift. Vorhandene freigegebene
  Projektgestaltung hat Vorrang; sonst ist Arial ein einfacher Ausgangspunkt.
- Richte vergleichbare Bausteine aus und verwende wiederkehrende Breiten, Innenabstände
  und Zwischenräume. Textlängen dürfen unterschiedliche Höhen erfordern.
- Nutze die Fläche für die relevanten Inhalte. Vermeide sowohl gedrängte Kästchen als
  auch grosse dekorative Leerflächen. Keine dominante Titel- oder Hero-Fläche.

Orientierungswerte für eine **neue** Zeichnung ohne bestehende Gestaltung:

- Bausteintitel etwa 16–18, Beschreibungen und Pfeiltexte etwa 12–14 draw.io-Schrifteinheiten.
- Etwa 12–16 Einheiten Innenabstand; etwa 30–50 Einheiten zwischen Bausteinen.
- Etwa 24–28 Einheiten Durchmesser für Nummernkreise; bei mehreren Ziffern anpassen.
- Bevorzuge eine am Bildschirm gut erfassbare Querformat-Anordnung. Kein festes
  Seitenverhältnis erzwingen und nichts abschneiden, nur um auf eine Seite zu passen.

Diese Werte sind Startwerte, keine Vorgabe zum ungefragten Umformatieren bestehender
Zeichnungen. Lesbarkeit geht vor einheitlichen Kästchenmassen oder möglichst kleiner Fläche.

## 6. BI-Verweise, Rollen und Ausbaustand

### BI-Verweise

- Eine Nummer steht für eine fachlich beschriebene BI-Aufgabe oder Leistung.
- Dieselbe Nummer darf an mehreren Komponenten erscheinen. Eine Komponente darf
  mehrere Nummern tragen. Keine künstliche Eins-zu-eins-Zuordnung erzwingen.
- Nummern sind stabile Verweise zwischen Diagramm und Erläuterungen. Nicht ungefragt
  neu nummerieren; keine Nummer ohne zugehörige Erklärung vergeben.
- Platziere Kreise einheitlich an einer Ecke mit genügend Abstand zum Inhalt.
- Aktualisiere bei beauftragten Änderungen alle betroffenen Verweise konsistent,
  einschliesslich einer vorhandenen begleitenden Beschreibung.

### Rollen und Organisationen

- Beschreibe zuerst, welche Verantwortung gemeint ist; ergänze danach eine belegte
  oder ausdrücklich vorgeschlagene Organisation.
- Schreibe nicht einfach «AGI» oder «AIO» neben ein Kästchen. Eine Beschriftung braucht
  die Rolle, beispielsweise «Technischer Betrieb: [Organisation]».
- Kennzeichne nicht beschlossene Besetzungen ausdrücklich mit «Besetzungsvorschlag».
  Leite keine Zustimmung aus dem blossen Auftauchen einer Organisation in Unterlagen ab.
- Setze technischen Betrieb, fachliche Verantwortung und Gesamtverantwortung für
  einen Service nicht gleich. Letztere ergibt sich nicht allein aus Komponentenlabels.
- Halte detaillierte Aufgaben, Entscheidungsrechte und Abgrenzungen in einer eigenen
  Rollenbeschreibung fest, sofern beauftragt; überlade die Grafik damit nicht.

### Ausbaustand

- Unterscheide mit Textkennzeichnungen: «bestehend», «Ausbauvorschlag» und «offen».
- Verwende diese Kennzeichnungen nur entsprechend der fachlichen Grundlage.
  «Offen» bedeutet nicht «beschlossen, aber noch nicht umgesetzt».
- Nutze nicht allein Farben oder gestrichelte Umrandungen zur Statusdarstellung.
- Erhalte Hinweise auf den Entwurfscharakter. Stelle Vorschläge nicht als bereits
  bestellte, finanzierte oder verfügbare Leistungen dar.

## 7. Zeichenebenen

Verwende bei neuen Zeichnungen folgende Struktur, soweit die Inhalte benötigt werden:

| Ebene | Inhalt | Verwendung |
| --- | --- | --- |
| Grundübersicht | Bausteine, Datenbestände, Gruppierungen, Nutzende, Beziehungen und Basislegende. | Muss allein verständlich sein. |
| BI-Beiträge | Nummernkreise, zugehörige Hinweise und gegebenenfalls ergänzende Legende. | Separat zuschaltbar; erst bei entsprechendem Auftrag inhaltlich füllen. |
| Rollen | Rollenbezogene Organisationsangaben und Kennzeichnung der Besetzungsvorschläge. | Separat zuschaltbar; keine ungeklärten Zuordnungen erfinden. |

- Nutze echte draw.io-Zeichenebenen, nicht bloss ähnlich benannte Gruppen.
- Vorhandene Ebenen und ihre Sichtbarkeit erhalten, soweit der Auftrag nichts anderes
  verlangt. Keine ungefragte Umstrukturierung oder Umbenennung bestehender Dateien.
- Für eine erste Infrastrukturübersicht soll die Grundübersicht sichtbar sein;
  optionale Ergänzungen können leer bleiben oder ausgeblendet sein.
- Erhalte die Zuordnung von BI-Markierungen und Rollenlabels zu ihren Bausteinen auch
  über Ebenengrenzen hinweg. Prüfe bei einer Verschiebung die betroffenen Überlagerungen.
- Kopiere nicht die gesamte Grundzeichnung auf jede Ebene. Beim Ausblenden optionaler
  Ebenen dürfen keine notwendigen Basisbeschriftungen oder Datenflüsse verschwinden.

## 8. Dateien und technische Bearbeitung

- Arbeite im ausdrücklich ausgewählten lokalen Projektordner an der bezeichneten
  `.drawio`-Datei. Verwende nicht unbemerkt eine Kopie oder einen anderen Worktree.
- Ist keine Zieldatei benannt, prüfe die vorhandenen Diagramme. Bei mehreren möglichen
  Zielen kläre die Auswahl. Nur bei beauftragter Neuanlage ohne Dateinamensvorgabe
  verwende `dateninfrastruktur.drawio`.
- Die `.drawio`-Datei ist die editierbare Hauptdatei. Bilder sind abgeleitete Vorschauen,
  kein Ersatz für die Zeichnung.
- Verwende native draw.io-XML-Elemente. Keine vollständige Grafik als einzelnes
  eingebettetes PNG/SVG und keine Umstellung auf Mermaid oder andere Quellformate.
- Bevorzuge bei neuen Dateien unkomprimiertes XML in UTF-8. Unterstütze bei bestehenden
  Dateien deren Format korrekt; konvertiere oder formatiere nicht ungefragt alles neu.
- Erhalte Seiten, Ebenen, Element-IDs, eigene Eigenschaften, Links und nicht betroffene
  Metadaten. Vorhandene Elemente bearbeiten statt löschen und identisch neu anlegen.
- Erhalte manuelle Positionen, Grössen, Stile und Linienwege ausserhalb des Änderungsumfangs.
  Kleine Änderungen rechtfertigen weder vollständige Neuerzeugung noch globales Auto-Layout.
- Nutze Auto-Layout höchstens für eine neue, noch nicht abgestimmte Teilansicht oder
  auf ausdrücklichen Wunsch. Beschränke es auf den vereinbarten Bereich.
- Berücksichtige beim Verschieben echte Gruppen und relative Koordinaten. Erhalte
  Verbinderanschlüsse und verschiebe abhängige Labels nur soweit notwendig.
- Behandle XML- und gegebenenfalls HTML-Escaping korrekt, insbesondere bei Umlauten,
  Anführungszeichen, `&`, `<`, `>` und mehrzeiligen Beschriftungen.
- Installiere keine Plugins, Programme oder Abhängigkeiten und ändere keine globalen
  draw.io-/Codex-Einstellungen ohne Auftrag. Prüfe vorhandene lokale Werkzeuge zuerst.
- Lade Projektdateien nicht ungefragt in Webeditoren, externe Renderer oder andere
  zusätzliche Dienste hoch. Die Diagrammbearbeitung und der Export sollen lokal erfolgen.
- Ändere diese AGENTS.md nicht bloss, um eine unbequeme Regel zu umgehen.

## 9. Sicherer Änderungsablauf

1. **Bestand lesen:** Zieldatei, relevante Beschreibung, vorhandene Ebenen, IDs und
   Layout prüfen. Bei Git-Projekten bestehende Änderungen berücksichtigen.
2. **Umfang festlegen:** Nur die angeforderte Änderung und unmittelbar notwendige
   Folgeanpassungen planen. Bei grösseren Eingriffen den Umfang kurz mitteilen.
3. **Ausgangsstand sichern:** Den gelesenen Dateistand inklusive Prüfsumme festhalten.
   Falls keine anderweitige Sicherung besteht, vor dem Überschreiben eine lokale,
   eindeutig benannte Sicherung anlegen.
4. **Gezielt bearbeiten:** Änderungen möglichst an bestehenden IDs vornehmen. Einen
   Kandidaten getrennt von der geöffneten Hauptdatei erzeugen und strukturell prüfen.
5. **Paralleländerungen prüfen:** Unmittelbar vor dem Schreiben den aktuellen
   Dateistand mit dem Ausgangsstand vergleichen. Bei Änderungen durch draw.io oder
   den Nutzer neu einlesen und die gezielten Änderungen auf dieser Basis anwenden.
   Bei Konflikten nicht blind überschreiben, sondern anhalten und klären.
6. **Sicher speichern:** Eine vollständig geschriebene und geprüfte temporäre Datei
   verwenden und die Zieldatei möglichst atomar ersetzen. Dateirechte erhalten.
   Das reduziert unvollständige Zwischenstände, ersetzt aber keine Konfliktprüfung.
7. **Ergebnis prüfen:** Gespeicherte Datei erneut lesen, Struktur prüfen und die
   betroffene Darstellung gemäss Abschnitt 10 kontrollieren.
8. **Kurz berichten:** Geänderte Datei, wesentliche Änderungen, tatsächlich erfolgte
   Prüfungen und verbleibende offene Punkte nennen.

Zusätzlich:

- Verlasse dich nicht darauf, dass die Desktop-App gleichzeitig entstandene Änderungen
  verlustfrei zusammenführt. Bei erkennbarer paralleler Bearbeitung um eine kurze
  Bearbeitungspause bitten; nicht bei jedem kleinen Auftrag vorsorglich blockieren.
- Lösche oder überschreibe keine fremden Änderungen. Keine automatischen Commits,
  Pushes, Resets oder Branchwechsel ohne Auftrag.
- Halte den Projektordner übersichtlich. Vorschauen gehören in einen vorhandenen
  Exportordner oder ersatzweise nach `previews/`. Keine Serie von
  `final_v2_neu_neu.drawio`-Kopien statt Bearbeitung der Hauptdatei.

## 10. Qualitätsprüfung

### Struktur – nach jedem Speichern

- XML lässt sich lesen; Seiten und Diagrammmodelle sind vorhanden und intakt.
- Element-IDs sind innerhalb des jeweiligen Diagrammmodells eindeutig.
- Elternbeziehungen sowie vorhandene Quellen- und Zielreferenzen sind gültig.
- Formen, Verbinder und Labels bleiben einzeln editierbar.
- Keine unbeabsichtigten Löschungen, Ebenenwechsel oder Änderungen ausserhalb des Auftrags.
- Geänderte Nummern, Texte und Verweise stimmen mit ihren Erläuterungen überein.

### Visuelle Prüfung

- Erzeuge nach Neuanlage sowie nach Änderungen an Layout, Text, Formen oder
  Verbindungen möglichst eine lokale PNG-Vorschau mit einem tatsächlich verfügbaren
  draw.io-Exportwerkzeug. Nutze vorhandene Skills oder Hilfsskripte, soweit passend.
- Betrachte die gerenderte Vorschau wirklich. Eine erfolgreiche XML-Prüfung oder ein
  erfolgreich gestarteter Export ist noch keine visuelle Prüfung.
- Prüfe insbesondere Textumbruch, abgeschnittene Inhalte, Überlagerungen, Linienführung,
  Pfeilrichtungen, Kontrast, Schriftgrösse und die Lesbarkeit der Gesamtübersicht.
- Prüfe nach Änderungen an Ebenen oder Überlagerungen die Grundübersicht allein und
  die jeweils betroffene Kombination mit BI-Beiträgen bzw. Rollen.
- Exportiere alternative Ebenensichten nötigenfalls aus temporären Kopien, damit die
  Sichtbarkeitseinstellungen der Hauptdatei nicht unbeabsichtigt verändert werden.
- Korrigiere Darstellungsfehler innerhalb des Auftrags. Keine fachliche Umgestaltung
  unter dem Vorwand einer Layoutverbesserung.
- Ist kein lokaler Renderer oder keine Bildinspektion verfügbar, führe die möglichen
  Strukturprüfungen aus und benenne die fehlende Sichtkontrolle ausdrücklich.
  Behaupte keine erfolgte Öffnung, Synchronisierung oder visuelle Prüfung.

## 11. Ergebnis und Kommunikation

Liefere die bearbeitete lokale Datei, nicht nur XML im Chat oder eine Beschreibung
möglicher Änderungen. Antworte auf Deutsch und halte die Abschlussmeldung knapp:

- Welche Datei bzw. Seite wurde geändert und was wurde angepasst?
- Welche Prüfungen wurden tatsächlich durchgeführt?
- Welche fachlichen Fragen, Konflikte oder Prüfungen bleiben gegebenenfalls offen?

Eine reine Analyse- oder Beratungsfrage ist kein Auftrag, Dateien zu verändern.
Bei einem konkreten Änderungsauftrag dagegen die Änderung ausführen, statt sie nur
anzubieten. Erhalte das Diagramm als gemeinsame, schrittweise weiterentwickelte
Gesprächsgrundlage.
