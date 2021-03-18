# Texterkennung
Zur Wohnungseröffnung erhält jeder Mieter getrennt von seinem Mietvertrag eine persönliche Identifikationsnummer. Der Hausmeister benötigt diese Nummer, um die Türe zu öffnen.

Herr Lambert schreibt sich alle seine Passwörter und Identifikationsnummern in seinen Notizblock. Leider weiß er nicht mehr, welche dieser Nummern die Identifikationsnummer ist.

Es existiert ein Bild dieser Notiz. Diese finden Sie in replit wie folgt:
`03_Texterkennung/solution/notiz.png`
**Sehen Sie sich zuerst diese Notiz in replit an, bevor Sie weiterlesen.**

Da Herr Lambert sich so viele Nummern aufgeschrieben hat, kann er diese nicht einzeln abtippen. Die Zeit drängt!

Für diese Aufgabe sollen Sie alle Zeichenfolgen auf dem Bild der Notiz erkennen und als Textdatei an den Hausmeister übermitteln. Dieser kann dann feststellen, ob die Identifikationsnummer unter diesen Zahlen ist.

Ihre Lösung sollen Sie in dem Programm `ocr.py` (OCR = Optical Character Recognition) im Ordner `03_Texterkennung/solution/` entwickeln.

Gehen Sie wie folgt vor.

## Bilderkennung
Für diese Aufgabe sollen Sie die Zahlen auf einem Bild erkennen. Dazu müssen Sie das Bild erst öffnen. Dies können Sie mit der Bibliothek `Image` erledigen. Das folgende Codebeispiel zeigt das Öffnen eines Bilds:

```python
from PIL import Image

def main():
    image = Image.open("mein_bild.png")
    
if __name__ == "__main__":
    main()
```

Um die Zahlenfolgen auf dem Bild zu erkennen, können Sie die Bibliothek `pytesseract` verwenden. Das folgende Beispiel zeigt das Importieren dieser Bibliothek und die Verwendung der Texterkennungsfunktion.

```python
import pytesseract

def main():
    text_in_image = pytesseract.image_to_string(image)
    
if __name__ == "__main__":
    main()
```
`text_in_image` enthält den Text, den die Funktion `image_to_string` in dem als Parameter übergebenen Bild gefunden hat.

**Erkennen Sie den Text mit `pytesseract`und geben Sie jetzt den Text auf der Kommandozeile aus.**

## Text in einer Datei abspeichern
Sie wollen den erkannten Text jetzt in einer Datei abspeichern, damit Sie diesen versenden können. Das folgende Beispiel zeigt den Code, um den Text "hello" in eine Datei zu schreiben.

```python
def main():
    my_file = open("myfile.txt", "w+")
    my_file.write("hello")
    my_file.close()

if __name__ == "__main__":
    main()
```

**Speichern Sie jetzt den aus dem Bild erkannten Text in der Datei `numbers.csv`.**

## Datei übermitteln und überprüfen
Sie haben es fast geschafft. Im letzten Schritt müssen Sie jetzt die Datei an Herrn Mayer übermitteln, um diese dort prüfen zu lassen. Die Hausverwaltung hat Ihnen dafür bereits ein Skript (`submit.py`) geschrieben, das Sie im Ordner `03_Texterkennung/solution` finden.

**Führen Sie dieses Skript wie folgt aus:**
```shell
python3 submit.py numbers.csv
```
Das Programm teilt Ihnen mit, ob Sie erfolgreich waren.


