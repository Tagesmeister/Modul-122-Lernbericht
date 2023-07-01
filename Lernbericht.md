# Modul 122 Lernbericht
Geschrieben von Pascal Oestrich

Es gibt viele BBB Lernende, die kein geordnetes Dateisystem haben, viele Moodle Dateien liegen im Downloadordner.
Im Modul 122 habe ich ein Powershell-Skript geschireben, dass alle Dateien im Moodle nach Modul und Dateityp ordnet.


## Was habe ich gelernt?

In meinem Projekt habe ich gelernt, wie man eine JSON datei auslesen und für das Skirpt verwenden kann.

## Beschreibung

In meinem Projekt habe ich ein Konfigruartionsdatei verwenden, um die Pfade, wenn gewollt, anpassen zu können.
Die Konfigurationsdatei ist eine `JSON-Datei`.

![image](https://github.com/Tagesmeister/Modul-122-Lernbericht/assets/110892258/85c36268-d0d2-4b34-8dca-b0dd8784afe1)

Um in der `JSON-Datei` etwas einfügen oder überschreiben zu können, muss man das was man überschreiben möchte im `Powershell-Skirpt` erstellen. In meinem Powershell-Skript gibt es die Variabel `sourceDir` und `destinationDir`. Die werden zuvor mit den Dateipfaden deklariert und dannach, mit dem `$config = @` in einem Hastable gespeichert.

Hastables sind Datenstrukturen, die zwei Werte, die zueineander stehen (Schlüsselpaare) zusammen abspeichern. Jeder Wert in einem Hastable, besteht aus einem Schlüssel. Mit dem bestimmten gegebenen Schlüssel, kann man auf die Daten zugreifen und verändern. Es ist wichtig zu wissen, dass jeder Eintrag in den Hastable einen eigenen, einzigartigen Schlüssel hat.

In meinem Beispiel, sind die Variablen `$soureceDir und $destinationDir` die Werte und `"sourceDir", "destinationDir"` die jeweiligen Schlüsseln dazu.

Mit dem `ConverTo-Json` werden die eingegebenen Pfaden in die JSON-Sprache konventiert Und danach mit dem `Set-Content` in die JSON-Datei überschrieben.

``` json
{ 
  "sourceDir": "C:\\Users\\pasca\\Downloads",
  "destinationDir": "C:\\Users\\pasca\\OneDrive - BBBaden\\Dokumente\\Montag IT"
}
```
### Resulatat
Das ist das Resultat von meinem Script

## Verifikation

✍️ Erklären Sie kurz und bündig, inwiefern die von Ihnen verwendeten Medien zeigen, was Sie gelernt haben.

# Reflektion zum Arbeitsprozess

👍 Überlegen Sie sich jeweils etwas, was gut an Ihrer Arbeit lief; 

👎 und etwas, was nicht gut lief.

**VBV**: ✍️ Formulieren Sie davon ausgehend einen *handelbaren* Verbesserungsvorschlag.
