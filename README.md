# Quarto-Vorlage

Moin,

mit dieser Vorlage kannst du deine Hausarbeit, Bachelor-, Masterarbeit oder was auch immer ganz einfach mit Quarto erstellen. Dieses Repo ist als Template formatiert, das heißt, du kannst es als Template benutzen, wenn du ein neues Repo erstellst. [Hier](https://docs.github.com/de/repositories/creating-and-managing-repositories/creating-a-repository-from-a-template) findest du eine Anleitung dazu.

Diese Vorlage habe ich anhand der [hier](https://r.ikmz.uzh.ch/Wissen_macht_R!/09-Quarto.html) zu findenden Vorlage von Benjamin Fretwurst von der Uni Zürich erstellt und minimalisiert sowie auf die Uni Marburg zugeschnitten. Vielen Dank an Herrn Fretwurst für die Veröffentlichungserlaubnis.

Im Folgenden gebe ich eine Übersicht über die Ordner und Dateien und wofür diese da sind.

-   `_common.R` Hier werden generelle Einstellungen gespeichert, die jeweils in die einzelnen Teile inkludiert werden. Unter anderem wird der generelle Umgang mit Code-Chunks geregelt (siehe dazu auch [hier](https://quarto.org/docs/reference/cells/cells-knitr.html#code-output) und [hier](https://quarto.org/docs/computations/r.html#chunk-options)), das Standardlayout für Grafiken (in der Vorlage mit `dplyr`) sowie eine einheitliche und stimmige Farbpalette. Mehr geht natürlich immer.

-   `_quarto.yml` Hier befinden sich alle Metadaten zum Buch, aber auch Einträge für die Frontpage und die Struktur des Dokuments sowie nicht zuletzt die Layout-Informationen. Vergleiche dazu auch: [hier](https://quarto.org/docs/books/#config-file) und [hier](https://quarto.org/docs/books/book-structure.html).

-   `.gitignore` In dieser Datei wird gesammelt, was Git nicht berücksichtigen soll. Wenn du Git nicht nutzt, kannst du die Datei einfach ignorieren.

-   `01-Theorieteil.qmd` Alle Dokumente, die mit einer Zahl beginnen, sind der eigentliche Inhalt der Arbeit. Sie müssen in der `_quarto.yml` eingefügt werden, um berücksichtigt zu werden. Wichtig zu beachten ist, dass jeder Teil für sich renderbar sein sollte und nicht von anderen Teilen abhängen sollte, sonst kann man die einzelnen Quarto Dokumente nicht rendern. Du kannst natürlich jede Menge weiterer Teile anfügen und auch die Namen ändern.

-   `02-Methode.qmd` s.o.

-   `03-Ergebnisse.qmd` s.o.

-   `07-Schluss.qmd` s.o.

-   `08-Anhang.qmd` Hier kommen alle Anhänge rein. Wie du ein Literaturverzeichnis an der Stelle deiner Wahl erzeugst, wird [hier](https://quarto.org/docs/authoring/footnotes-and-citations.html#bibliography-generation) erklärt.

-   `Datenaufbereitungsvorlage.qmd` In diesem Dokument bereitest du alle Daten, die du nutzt, so vor, dass du sie nicht mehr manipulieren musst (also nicht mehr rekodieren, umbenennen etc.). Die Idee dahinter ist, dass du am Ende von der Datenaufbereitung einen (oder mehrere) Datensätze hast, die fertig sind und du die Datenaufbereitung nicht immer neu machen musst. Das ist fehleranfälliger.

-   `files` In diesem Ordner befinden sich wichtige inhaltliche Sachen.

    -   `LaTeX` Deine Quarto-Dateien werden erst in Markdown und dann anhand von Pandoc in LaTeX umgewandelt. LaTeX ist ein Drucksatzprogramm, mit der hochwertige PDFs erstellt werden können. Die Einstellungen, die in LaTeX vorgenommen werden, damit es am Ende so aussieht, wie es aussieht, befinden sich in diesem Ordner. Du kannst dich gerne ausprobieren, was Dinge bewirken, aber bedenke, dass jede Änderung auch dazu führen kann, dass nichts mehr funktioniert.
        -   `macros.tex` Hier werden die genutzten Makros geladen.
        -   `quarto_template.tex` Hier befinden sich Anpassungen für LaTeX. Unter anderem können hier auch Einträge auf der Frontpage verändert werden (über Variablen, die in der `_quarto.yml` definiert werden).
    -   `Methodensteckbrief.xlsx` Wenn du den Methodensteckbrief nutzen möchtest, bearbeitest du diesen inhaltlich in dieser Datei. Die Idee ist, eine Übersichtstabelle zu haben, wo alle Methodeninfos gebündelt und übersichtlich stehen. Du kannst den Steckbrief natürlich anpassen, ggf. musst du dann auch den Wertebereich, der importiert wird, anpassen. Aktuell wird der Steckbrief in `02-Methode.qmd` importiert.
    -   `pandoc-quotes.lua` In dieser Datei befinden sich verschiedene Layouts für die Nutzung von Anführungszeichen und Co. (im Deutschen `„` und `“`). Hier musst/solltest du nichts verändern.
    -   `references.bib` Das ist deine Bib-Datei, in der die Literatureinträge aus Zotero importiert werden. Die Referenzierung darauf (also die Einstellung, welche Bib-Datei man benutzt) erfolgt in der `_quarto.cml`.
    -   `Silbentrennung.tex` Hier solltest du auch nichts ändern.

-   `Forschungsbericht` In diesem Ordner landet am Ende deine Arbeit.

-   `images` Hier kannst du Bilder speichern, die du verwenden möchtest.

    -   `pum_logo_sw.pdf` Das ist das Logo der Philipps-Universität Marburg.
    -   `pum_logo_sw.svg` Das ist das Logo in einem anderen Format.

-   `index.qmd` In diese Datei kommt die Einleitung rein.

-   `name.Rproj` Das ist die R-Projektdatei. Die kannst du umbenennen wie du willst. Du solltest dein Projekt immer mit deiner Projektdatei öffnen, sonst funktionieren ggf. Dinge nicht.

-   `README.md` Das ist diese Markdown-Datei, die du gerade liest. Sie ist für deine Arbeit irrelevant und soll dir nur helfen, diese Vorlage besser zu verstehen.
