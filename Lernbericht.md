# Modul 122 Lernbericht
#### Geschrieben von Pascal Oestrich

Es gibt viele BBB Lernende, die kein geordnetes Dateisystem haben. Viele Moodle Dateien liegen im Downloadordner.
Im Modul 122 habe ich ein Powershell-Skript geschireben, dass alle Dateien im Moodle nach Modul und Dateityp ordnet.


## Was habe ich gelernt?

In meinem Projekt habe ich gelernt, wie man eine JSON-Datei auslesen und für das Skript verwenden kann.

## Beschreibung

In meinem Projekt habe ich eine Konfigurationsdatei verwendet, um die Pfade, wenn gewollt, anpassen zu können.
Die Konfigurationsdatei ist eine `JSON-Datei`.

![image](https://github.com/Tagesmeister/Modul-122-Lernbericht/assets/110892258/85c36268-d0d2-4b34-8dca-b0dd8784afe1)

Um in der `JSON-Datei` etwas einfügen oder überschreiben zu können, muss man das, was man überschreiben möchte, im `Powershell-Skirpt` erstellen. In meinem Powershell-Skript gibt es die Variabel `sourceDir` und `destinationDir`. Die werden zuvor mit den Dateipfaden deklariert und danach mit dem `$config = @` in einem Hastable gespeichert.

Hastables sind Datenstrukturen zweier Werte, die zueinander stehen (Schlüsselpaare) zusammen abspeichern. Jeder Wert in einem Hastable besteht aus einem Schlüssel. Mit dem bestimmten gegebenen Schlüssel kann man auf die Daten zugreifen und verändern. Es ist wichtig zu wissen, dass jeder Eintrag in den Hastable einen eigenen, einzigartigen Schlüssel hat.

In meinem Beispiel sind die Variablen `$soureceDir und $destinationDir` die Werte und `"sourceDir", "destinationDir"` die jeweiligen Schlüssel dazu.

Mit dem `ConverTo-Json` werden die eingegebenen Pfade in die JSON-Sprache konventiert und danach mit dem `Set-Content` in die JSON-Datei überschrieben.

``` json
{ 
  "sourceDir": "C:\\Users\\pasca\\Downloads",
  "destinationDir": "C:\\Users\\pasca\\OneDrive - BBBaden\\Dokumente\\Montag IT"
}
```
## Verifikation

* Der Text beschreibt, wie in dem Script die Configurations-Daten in die `JSON-Datei` überschrieben wird.
* Das Bild zeigt den ganzen `Configurations-Code`
* Der Codeschnipsel zeigt, wie die `JSON-Datei` aussieht.

# Reflexion zum Arbeitsprozess

Ich habe gut und strukturiert gearbeitet. Ich konnte gut mit Problemen umgehen und fand jedes Mal eine Lösung.

Was ich nicht gut hinbekam, war, dass ich meine Datei auf OneDrive hatte und wenn ich auf einem anderen Computer arbeitete, funktionierte OneDrive nicht immer.

**VBV**: Das nächste Mal werde ich meine Arbeit auf OneDrive für ein Backup hochlade und auf einen UBS-Stick laden. Somit kann ich jedes Mal an einem anderen Computer arbeiten.
