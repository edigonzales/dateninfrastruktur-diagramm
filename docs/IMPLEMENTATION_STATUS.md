# Prüfstand Dateninfrastruktur-Diagramm

## Startdiagramm für das Controller-Gespräch

Stand: 4. Oktober 2026. Zieldatei: `dateninfrastruktur.drawio`. Basisrevision des Zielrepositorys: `e51db7d71184908266c2fec4108c743462b605f9`, ergänzt im Arbeitsbaum.

Umgesetzt: eine native editierbare A3-Querformat-Seite mit zehn funktionalen Bausteinen, elf beschrifteten Verbindungen, Querschnittsaufgaben, vier beispielhaften Leistungen und drei Gesprächsfragen. Sechs sichtbare, editierbare Layer; BI-Beiträge separat schaltbar. Quellenhinweise stehen in den Elementmetadaten. Ausbaustand und offene fachliche Definitionen bzw. Betreuung sind ausdrücklich bezeichnet.

Fachliche Grundlage: zehn bereitgestellte Screenshots; `Dateninfrastruktur_V0_1.pptx` (13 Folien samt Notizen), `SwiftScan 2 Oct 2026 16.09(1).pdf` (Ideenskizze) und `Whitepaper_Business_Intelligence_V0_1(1).docx` (7 Seiten). Diese wurden gelesen bzw. visuell betrachtet. Die lokale `notizen.md` wurde beim Umzug gelesen und unverändert belassen.

Abgleich mit der vollständigen Ziel-`AGENTS.md`: Funktionssicht, native Formen, gerichtete Datenflüsse und gestrichelte Definitionsnutzung, Quellenbezug, offene Rollen und separat schaltbare BI-Beiträge stimmen überein. Blau statt des bevorzugten Rot, A3 und Erhalt der fünf ursprünglichen Layer plus BI-Beiträge folgen dem ausdrücklichen Nutzerplan. Statusangaben sind in der Legende erläutert. Es wird keine bestehende kantonale BI-Dienstleistung oder Organisationsbesetzung zugesichert.

### Tatsächliche Prüfungen

| Befehl / Prüfung | Ergebnis |
| --- | --- |
| `git status --short`, `git rev-parse HEAD` in beiden Repositorys | Exit 0; Ausgangsstände geprüft. Im Ziel war ausschliesslich `notizen.md` ungetrackt. |
| `python3 /tmp/build_dateninfrastruktur.py` | Exit 0; native XML-Struktur erstellt, anschliessend gezielt Layout und Legendentexte angepasst. |
| `python3 -` – XML-/Referenz-/Layoutprüfung mit ElementTree | Exit 0; 103 eindeutige IDs, sechs sichtbare editierbare Layer, zehn Bausteine mit Quellenmetadaten, elf gerichtete Verbindungen (drei gestrichelt), gültige Eltern und Endpunkte, vier konsistente Leistungsnummern; Geometrien innerhalb A3, Whitespace und Dateiende geprüft. |
| `/Applications/draw.io.app/Contents/MacOS/draw.io --export --format png --scale 1.5 --size page --output /tmp/dateninfrastruktur-controller.png --timeout 30 /Users/stefan/sources/dateninfrastruktur-diagramm/dateninfrastruktur.drawio` | Exit 0; vollständige gerenderte Vorschau tatsächlich betrachtet: Texte, Pfeile, Formen, Legende und Seitenränder geprüft. |
| Native Prüfung in draw.io Desktop 31.7.0 | Layerliste geprüft, BI-Beiträge ausgeblendet und wieder eingeblendet. Grundübersicht bleibt ohne Leistungsnummern verständlich. Alle Layer zum Abschluss wieder sichtbar. UI-Prüfung ohne Shell-Exitcode. |

Abschluss des Umzugs: `git diff --check` in beiden Repositorys **Exit 0**. `python3 -` bestätigt **Exit 0**: Ursprungsrepository mit leerem `git status --porcelain=v1`, Statusbericht bytegleich zu HEAD, keine Diagramm- oder Backupdatei zurückgeblieben. Die bereits vorhandene ungetrackte `notizen.md` im Ziel ist per SHA-256 unverändert. Separater Whitespacecheck umfasst auch die neuen ungetrackten Dateien. Die verschobene Hauptdatei wurde erneut in draw.io geöffnet, alle sechs Layer sichtbar.

Diagramm-SHA-256 nach Umzug und abschliessender Legendenanpassung: `98b6b40d63838ff97f40e2ae41b4ec21290412335ea0a9341c767083710e07ef`.

**Nicht ausgeführt:** Anwendungstests, Typecheck, Lint, Engine-/Browser-/Deploymenttests und `npm run verify`; reine Diagramm-/Dokumentationsänderung, keine Dependencies oder Anwendungscode geändert. Keine neue Requirement- oder V1-Abnahme.

**Nächster Schritt:** Mit dem Controller einen konkreten Bericht durchgehen, Eigenleistung und Unterstützung klären sowie Kennzahlendefinitionen, Abnahme und spätere Betreuung festhalten. Technischer Ort der Integration und konkrete Servicezuständigkeiten bleiben offen.

## Historischer Prüfstand der leeren Grundstruktur

Der folgende Nachtrag entstand zunächst im versehentlich gewählten Datenwerkstatt-Repository. Er wurde zusammen mit dem Diagramm hierher verschoben; A4 und leere Inhaltslayer beschreiben ausschliesslich den früheren Zwischenstand.

## Dokumentation — leere draw.io-Grundstruktur

Stand 4. Oktober 2026. **Abgeschlossener Dokumentationsschritt gemäss separatem Nutzerauftrag**, keine neue P0–P8-Implementierungsphase und keine zusätzliche REQ-001–080-/AT-001–072-Abnahme. Prüfbasis: Git-Revision `c1d4bc0ee38eafb182d736e5f606d1650bb8e7f6`; die Diagrammdatei und dieser Statusnachtrag liegen zusätzlich im uncommitteten Arbeitsbaum.

Dateien: [`dateninfrastruktur.drawio`](../dateninfrastruktur.drawio) und dieser Statusbericht. Das native, unkomprimierte XML enthält eine Seite „Dateninfrastruktur“, A4-Querformat (1169 × 827), weissen Hintergrund und 10-Pixel-Raster. Fünf sichtbare, editierbare Layer, von vorne nach hinten: **Legende, Anmerkungen, Datenflüsse, Systeme, Grenzen**. Ausschliesslich der Legendenlayer enthält elf Zeichenelemente mit den allgemeinen Symbolen für System, Datenfluss, Grenze und Anmerkung. Die vier Inhaltslayer sind vollständig leer; keine fachlichen Komponenten oder Beziehungen ergänzt.

Tatsächlich ausgeführte Prüfungen:

| Befehl / Prüfung | Exit / Ergebnis |
|---|---|
| `git status --short`, `git rev-parse HEAD` | **Exit 0**; sauberer Ausgangsbaum, Basisrevision identifiziert. |
| `python3 -` — XML-Prüfung mit `xml.etree.ElementTree`, vor und nach Desktop-Speicherung | Jeweils **Exit 0**; Seitenformat/Raster, fünf Layer und Reihenfolge, Sichtbarkeit/Editierbarkeit, elf Legendenelemente, vier leere Inhaltslayer, eindeutige IDs, gültige Elternreferenzen und Geometrien geprüft. Abschlussprüfung umfasst auch Whitespace und abschliessenden Zeilenumbruch. |
| Native UI-Prüfung in draw.io Desktop **31.7.0** | Datei tatsächlich geöffnet; Legende und Layerliste lesbar. Legende ausgeblendet: Zeichenfläche leer. Wieder eingeblendet: alle Legendenelemente sichtbar, fünf Layer sichtbar und entsperrt; „All changes saved“. Native UI-Prüfung hat keinen Shell-Exitcode. |
| `git diff --no-index --check -- /dev/null dateninfrastruktur.drawio` | **Exit 1**, ohne Whitespacehinweise; `--no-index` meldet den erwarteten Dateiunterschied zur leeren Datei. Separater Python-Whitespacecheck **Exit 0**. |
| `git diff --check` | **Exit 0**. |

Verifizierte Diagrammbytes nach draw.io-Speicherung: SHA-256 `3dc2974f6dff9086c7c60cb84719a48b5782cfc5092e5881a7eb833134448495`. Die ausschliesslich bei dieser UI-Prüfung entstandene lokale draw.io-Backupdatei wurde entfernt; die Diagrammdatei bleibt in draw.io geöffnet.

**Nicht ausgeführt:** Typecheck, Lint, Unit-/Engine-/Browser-/Deploymenttests und `npm run verify`; Anwendungscode, Dependencies und vorhandene Tests wurden nicht geändert. Keine neue V1-Fertigmeldung. **Blocker für diesen Dokumentationsschritt:** keine. **Nächster konkreter Diagrammschritt:** fachliche Inhalte erst nach einem gesonderten Auftrag und anhand belegter Projektquellen ergänzen; die Grundstruktur bleibt bis dahin leer.
