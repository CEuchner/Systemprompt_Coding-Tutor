# KI als Coding-Tutor
Im Rahmen eines Uni-Projekts entstand ein System-Prompt für ein LLM, der das Modell zum Coding-Tutor macht.
Auf Basis von ein paar Angaben, die der Bot zu Beginn abfragt, erstellt er einen Kurs, durch den er anschließend schrittweise durchleitet.
Im Prompt ist das didaktische Modell der *Kognitiven Meisterlehre (Cognitive Apprenticeship)* implementiert, wobei das Modell die Prinzipien nicht immer vollständig konsequent umsetzt.
Am Ende eines Kurses gibt der Bot eine Zusammenfassung in Form eines Cheatsheets und ein einfaches Übergabeprotokoll für einen Folgekurs aus.

## Zielgruppe
Das Modell ist primär für Anfänger gedacht, kann aber auch für Fortgeschrittene verwendet werden.
Die Kurs-Qualität hängt vom verwendeten Sprachmodell ab.

## Konfiguration

### Open WebUI
Die Uni Freiburg bietet mit [Open WebUI](https://openwebui.uni-freiburg.de/) eine Benutzeroberfläche für selbstgehostete KI-Modelle.

Ein KI-Modell lässt sich in der linken Menüleiste über *Arbeitsbereich > Modelle* konfigurieren.
Zuerst oben rechts auf *+ Neues Modell* klicken, einen Namen und ein Modell wählen, und anschließend den Prompt als Systemprompt setzen.
Abschließend *Speichern & Erstellen*.

### ILIAS
In ILIAS lassen sich *Assistenten* anlegen.
Dazu den Prompt in den *Instruktionen* eintragen.

Empfohlener Text für die Einleitung:
```
Beginne mit einer einfachen Begrüßung, damit ich mit dir durchstarten kann.

Ich habe dir einen Hinweis hinterlegt:
- verfügbar nach der Begrüßung
- zu finden neben der Chateingabe
- er enthält ein paar Tipps und Regeln für den Chat, die uns die Kommunikation erleichtern
```

Empfohlener Text für den Hinweis:
```
1. Einen Zeilenumbruch erreichst du mit `Shift` + `Enter`.
2. Wenn du Code oder Text aus der Ausgabe in den Chat kopierst, beginne bitte immer mit "Code:" oder "Ausgabe:".
```

**ACHTUNG**: In ILIAS werden die Markdown-Codeblocks des Nutzers nicht gerendert.
Kleine Tests zeigten keinen Nachteil gegenüber Modellen in Open WebUI, jedoch kann dieser nicht ausgeschlossen werden.

### Empfohlene KI-Modelle
Als Grundlage für den Coding-Tutor wird ein Coding-Modell empfohlen.
Coding-Modelle lassen sich in Open WebUI über die Modellauswahl oben links im Chatfenster identifizieren.
Die Empfehlung beruht lediglich auf allgemeinen Kenntnissen zu LLMs, es wurden keine Tests durchgeführt.

**WICHTIG**: Das Rechenzentrum bittet darum lokale Modelle zu nutzen, da die Uni für die Modelle von OpenAI und MistralAI pro Token zahlt.
Die lokalen Modelle sind durch ein vorangestelltes *UFR* in Open WebUI und ein vorangestelltes *RZ* in ILIAS gekennzeichnet.

### Kachelbilder
Mit ChatGPT wurde ein Kachelbild erstellt, das in den Seitenverhältnissen 1:1 und 3:2 vorliegt.

> [Bild 1:1](/img_CodingTutor_1x1.png)
> 
> [Bild 3:2](/img_CodingTutor_3x2.png)

## Prompt 
Der Prompt kann als [Markdown-Datei](/Prompt.md) heruntergeladen werden.
