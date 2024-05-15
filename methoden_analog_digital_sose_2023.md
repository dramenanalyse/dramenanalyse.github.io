# Methoden der Dramenanalyse: analog und digital (Sommersemester 2023)

:warning: Das Seminar lief vom April bis Juli 2023. Der **Seminarplan** bleibt für Dokumentationszwecke in dieser Form online, zumal auch die Ergebnisse verlinkt sind.

## Seminarbeschreibung
Im Mittelpunkt dieses Seminars, das gemeinsam von der Freien Universität Berlin und der Universität Potsdam veranstaltet wird, steht die Analyse dramatischer Texte. Dies geschieht sowohl mithilfe tradierter als auch neuartiger Methoden, wie sie im Bereich der Digital Humanities entwickelt werden. Die Veranstaltung zielt so auch auf die Vermittlung grundlegender digitaler Fertigkeiten, die für das gesamte Studium und darüber hinaus vonnutzen sein können. Der inhaltliche Fokus liegt auf dem deutschsprachigen Drama von der Mitte des 17. bis zur Mitte des 20. Jahrhunderts, bezieht aber die Dramenproduktion anderer europäischer Literaturen seit der Antike mit ein. Untersucht werden nicht nur Volltexte, sondern auch die Vernetzung dramatischer Werke mit der digitalen Umgebung (Enzyklopädien, Faktendatenbanken, digitalisierte Aufführungszeugnisse). Dabei wird auch das Verhältnis zwischen den Ergebnissen digitaler Ansätze und denen traditionellerer Interpretationsmodelle kritisch diskutiert. Auf der [DraCor-Plattform](https://dracor.org/), die im Seminar eine zentrale Stellung einnehmen wird, kann man sich bereits vorab mit Möglichkeiten digitaler Analysen vertraut machen.

## Verantwortlich:
- [Prof. Dr. Peer Trilcke](https://www.uni-potsdam.de/de/lit-19-jhd/welcome) (UP)
- [Prof. Dr. Frank Fischer](https://lehkost.github.io/) (FU)

## Organisatorisches
### Universität Potsdam
- [Eintrag im VV der UP](https://puls.uni-potsdam.de/qisserver/rds?state=verpublish&status=init&vmfile=no&publishid=100743&moduleCall=webInfo&publishConfFile=webInfo&publishSubDir=veranstaltung)

### Freie Universität Berlin
- [Eintrag im VV der FU](https://www.fu-berlin.de/vv/de/lv/793092)
- [Link zum Blackboard](https://fu-berlin.blackboard.com/webapps/blackboard/execute/courseMain?course_id=_180984_1)

## Termine
### 1. Sitzung: 20. April (Do), 14–16 Uhr: Einführung
- [Einführungspräsentation](https://lehkost.github.io/slides/2023-04-20-dramenanalyse-intro/index.html)
- Bis nächste Woche Transkription einzelner Seiten (Seitenverteilung wie besprochen): [https://de.wikisource.org/wiki/Index:Kotzebue\_-\_Blind\_geladen.pdf](https://de.wikisource.org/wiki/Index:Kotzebue_-_Blind_geladen.pdf)
- Vorbereitung für die nächste Sitzung:
  - Lesen Sie bitte das Kapitel [»XML«](https://doi.org/10.1007/978-3-476-05446-3_9) im Band »Digital Humanities. Eine Einführung« (2017, S. 128–146), gibt es auch elektronisch über das Bibliotheksportal Primo der FU sowie im Moodle der UP.
  - Sie können auch schon einen Blick auf die [Kodierungsrichtlinien (Guidelines) der Text Encoding Initiative (TEI)](https://tei-c.org/release/doc/tei-p5-doc/de/html/index.html) werfen.

### 2. Sitzung: 27. April (Do), 14–16 Uhr: Dramen als digitale Objekte: Theorie & TEI
- Nachbesprechung der Transkriptionsaufgabe:
  - Welche Schwierigkeiten gab es?
  - historische Orthografie vs. aktuelle Rechtschreibung
  - semantische Textauszeichnung (Überschriften, g e s p e r r t, **Sprecher\*innen**, *Regieanweisungen*)
  - editorische Hilfsmittel (obere Leiste des Bearbeitungsfensters in Wikisource)
- Diskussion des gelesenen »XML«-Kapitels.
- Kurze Einführung in TEI als Markup-Sprache für historische Dokumente (Präsentation).
  - Beispiel: TEI-Markup zu Goethes [»Ur-Faust«](https://dracor.org/api/corpora/ger/play/goethe-faust-in-urspruenglicher-gestalt/tei).
- Vorbereitung für die nächste Sitzung:
  - Installation des **Oxygen XML Editor** (FU: [über das Software-Portal](https://portal.zedat.fu-berlin.de/software/); UP: [Campuslizenz](https://www.uni-potsdam.de/de/zim/angebote-loesungen/software-campuslizenzen/oxygen-xml-editor)).
  - Suchen Sie sich ein kurzes Stück in der [Einakter-Datenbank](https://einakter.dracor.org/), das noch keine Wikidata-ID hat. Vorzugsweise ist das ein deutschsprachiges Originalstück (keine Übersetzung). **Alternativ** können Sie auch jedes andere (längere) Drama zu Ihrem Projekt machen.
    - Teams sollten je nach Umfang des Stücks aus 1–3 Personen bestehen.
    - In der nächsten Sitzung präsentieren wir die Projektideen und finalisieren die Zusammensetzung der Teams.
    - Ziel für den ersten Hackathon: TEI-Kodierung der jeweiligen Dramen und erste Analyseschritte.

### 3. Sitzung: 4. Mai (Do), 14–16 Uhr: Dramen als digitale Objekte: Praxis
- Praktische Übung mit dem Oxygen XML Editor:
  - Download der Datei ["drama-test.xml"](https://raw.githubusercontent.com/dramenanalyse/dramenanalyse.github.io/main/drama-test.xml).
  - TEI-Markup-Übung (zum Copy & Pasten):

```txt
Marthens Garten.

Margarete. Faust.

MARGARETE.
Versprich mir, Heinrich!

FAUST.
Was ich kann!

MARGARETE.
Nun sag, wie hast du's mit der Religion?
Du bist ein herzlich guter Mann,
Allein ich glaub', du hältst nicht viel davon.

FAUST.
Laß das, mein Kind! Du fühlst, ich bin dir gut;
Für meine Lieben ließ' ich Leib und Blut,
Will niemand sein Gefühl und seine Kirche rauben.

MARGARETE.
Das ist nicht recht, man muß dran glauben!

FAUST.
Muß man?
```

- XPath-Übungen (in Oxygen):
  - ```//l```
  - ```//sp```
  - ```//speaker```
  - ```distinct-values(//speaker)```
  - ```//speaker[contains(., 'U')]```
- Teams und Projekte ([Übersicht](https://etherpad.wikimedia.org/p/3xNEx6N2NS8YRZunRO0R)):
  1. (Anonym): [Emilie oder die Philosophisch-Verliebten. Ein Lustspiel von einem Aufzuge](https://dracor.org/id/ger000634) (1770)
  2. Joseph Bernhard Pelzel: [Apolls Gericht, oder das bestrafte Vorurtheil Vindebonens. Ein allegorisches Drama in einem Akte von einem Wiener](https://dracor.org/id/ger000626) (1769)
  3. (Anonym): [Amalie und Charlotte Baronessen von Habenichts: oder die ungleichen Schwestern. Ein deutsches Lustspiel von einer Handlung](https://dracor.org/id/ger000639) (1754)
  4. Moritz Preusse (Übers.): [Herzmutterchen! Lustspiel in einem Act](https://dracor.org/id/ger000623) (1847)
  5. Karl Ferdinand Daniel Grohmann: [Der Physiognomist. Oder: Keine Regel ohn' Ausnahme. Ein Lustspiel in einem Aufzug](https://dracor.org/id/ger000625) (1778)
  6. (Anonym, Übers.): [Das Urtheil des Paris. Ein Musicalisches Schäfer-Spiel in einer Handlung](https://dracor.org/id/ger000624) (1752)
  7. (Anonym, Übers.): [Die Gespenster. Lustspiel in 1 Akt aus dem Französischen des Moissy](https://dracor.org/id/ger000640) (1770)
  8. Lina Reinhardt: [Die Braut des Echo's. Lustspiel in einem Akte](https://dracor.org/id/ger000641) (1835)
  9. Johann Albrecht Huber: [Die Torte. Ein Lustspiel für Kinder in einem Aufzuge](https://dracor.org/id/ger000627) (1786)
  10. Clementine Schrader: [Der Hohlweg. Lustspiel in einem Akt](https://dracor.org/id/ger000621) (1843)
  11. Ludwig Georg Franz Freisleben: [Der Weihnachtstag. Drama in Einem Aufzuge. Bearbeitet nach einer Schreckensscene aus der wirklichen Welt](https://dracor.org/id/ger000638) (1827)
  12. Johann Ludwig Schlosser: [Die Maskerade. Ein Lustspiel in einem Akt](https://dracor.org/id/ger000635) (1767)
  13. (Anonym): [Das Ehrenmaal des Patrioten. Singspiel](https://dracor.org/id/ger000642) (1774)
  14. Achat (Johann Heinrich Gempt jun.): [Ein April-Scherz. Original-Lustspiel in einem Akt](https://dracor.org/id/ger000637) (1842)
  15. August von Kotzebue: [Das unsichtbare Mädchen. Ein Intermezzo in einem Aufzuge](https://dracor.org/id/ger000636) (1811)
- Einführung in [Transkribus](https://transkribus.eu/). Mit diesem Tool kann man Handschriften, aber auch Drucke in 𝔉𝔯𝔞𝔨𝔱𝔲𝔯 digitalisieren.
- Hausaufgabe bis zur Blocksitzung:
  - Digitalisierung des von Ihnen ausgewählten Stücks mit Transkribus.

### 4.–7. Sitzung (Blocksitzung): 26. Mai (Fr), 10–17 Uhr: Editathon & analoge Analysen
- Veranstaltungsort: Universität Potsdam ([Campus Am Neuen Palais 10](https://goo.gl/maps/sZFh5PDypUwQT5ck8)), 14469 Potsdam, Raum: 8.0.58 = Gebäude »8«, Erdgeschoss (»0«), Raum-Nr. »58«).

**10:00–13:00 – Dramen digital edieren**
- Begrüßung (Fischer, Trilcke)
- Gruppenarbeit: Wo stehen wir mit unserem Editionsprojekt? (Selbstevaluation)
- Plenum: Berichte aus den Gruppen: Welches Stück genommen? Wie ist der Stand des Projekts? Welche Probleme gibt es (mit Transkribus?); Was wären die nächsten Schritte geht es weiter
- Vorbereiten für die Transformation mit [ezDrama](https://github.com/dracor-org/ezdrama)
- Input (Trilcke): Transformation von Textdatein nach DraCor TEI (Verwendung von ezDrama mit Colab): [Notebook auf Colab](https://colab.research.google.com/github/dracor-org/ezdrama/blob/main/ezdramaparser.ipynb)
- Gruppenarbeit: Transformation und Arbeit an den TEI-Dateien der eigenen Stücke

**13:00–14:00 – Pause / Mensa**

**14:00–17:00 – Dramen digital analysieren**
- Einführung in [AntConc](https://www.laurenceanthony.net/software/antconc/) (Peer Trilcke)
- Partner\*innenarbeit (Übung mit AntConc)
  - Daten: [GerDraCor_SpokenText](https://github.com/dramenanalyse/dramenanalyse.github.io/raw/main/GerDraCor_SpokenText.zip)
  - Daten: [GerDraCor_StageDirections](https://github.com/dramenanalyse/dramenanalyse.github.io/raw/main/GerDraCor_StageDirections.zip)
  - Metadaten: [GerDraCor_Metadata.csv](https://github.com/dramenanalyse/dramenanalyse.github.io/raw/main/GerDraCor_Metadata.csv)
  - Deutsche Stopword-Liste: [stopword_list_de.txt](https://github.com/dramenanalyse/dramenanalyse.github.io/raw/main/stopword_list_de.txt)
- Durchführung einer kleinen beispielhaften Forschungsarbeit (Frank Fischer)
- Gruppen-/Partner-/Einzelarbeit: Erarbeitung einer kleinen Forschungsfrage; Durchführung der entsprechenden Analyse

### 8.–11. Sitzung (Blocksitzung): 16. Juni (Fr), 10–17 Uhr: Digitale Dramenanalyse
- Veranstaltungsort: [Ada Lovelace Center for Digital Humanities](https://www.ada.fu-berlin.de/) (Co-Working Space 2. OG, Zentralbibliothek der FU, Garystraße 39, 14195 Berlin).

**10:15–11:15 – Digitales Edieren**
- Stand der Projekte
- Transformation in XML: Erfahrungsberichte (und Helpdesk)
- Korrektur der Speaker Identification

**11:30–13:00 – Mixed Methods: Theorie und (eigene) Anwendung**
- gemeinsame Diskussion der Forschungstexte (mit Fokus Mixed Methods):
  - Michael Stubbs: Conrad in the computer: examples of quantitative stylistic methods. In: Language and Literature 14.1 (2005), S. 5–24. ([doi:10.1177/0963947005048873](https://doi.org/10.1177/0963947005048873))
  - Berenike J. Herrmann: In a test bed with Kafka. Introducing a mixed-method approach to digital stylistics. In: Digital Humanities Quarterly 11.4 (2017). ([http://www.digitalhumanities.org/dhq/vol/11/4/000341/000341.html](http://www.digitalhumanities.org/dhq/vol/11/4/000341/000341.html))
  - Thomas Weitin, Thomas Gilli, Nico Kunkel: Auslegen und Ausrechnen. Zum Verhältnis hermeneutischer und quantitativer Verfahren in der Literaturwissenschaft. In: Zeitschrift für Literaturwissenschaft und Linguistik 46 (2016), S. 103–115. ([doi:10.1007/s41244-016-0004-8](https://doi.org/10.1007/s41244-016-0004-8))
- Diskussion über mögliche eigene Forschungsprojekte

**13:00–14:00 – Mittagspause**

**14:00–17:00 – Stylo-Hackathon**
- Vortrag »Einführung in die Stilometrie mit Stylo« (Folien: [bit.ly/dram166](https://bit.ly/dram166))
- Einführung in die Software
  - Arbeitskorpus: ["stylo_dramenanalyse_directories.zip"](https://lehkost.github.io/slides/2023-06-16-dramenanalyse-stylo/files/stylo_dramenanalyse_directories.zip)
- Hackathon in Gruppen

### 12. Sitzung: 29. Juni (Do), 14–16 Uhr: Mixed Methods-Studien I

### 13. Sitzung: 6. Juli (Do), 14–16 Uhr: Mixed Methods-Studien II

### 14. Sitzung: (individuell): Prüfungsvorbereitung
