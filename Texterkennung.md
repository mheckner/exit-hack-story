# Texterkennung
Für diese Aufgabe sollen Sie die Daten auf einem Bild eines Rechners analysieren und die Informationen auf dem Bild in Text umwandeln:

https://github.com/mheckner/exit-hack/blob/master/03_OCR/solution/rechner.png

Ihre Lösung sollen Sie in dem Programm `ocr.py` (OCR = Optical Character Recognition) im Ordner `03_OCR/solution/` entwickeln.

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

Um die Zahlen auf dem Bild zu erkennen, können Sie die Bibliothek `pytesseract` verwenden. Das folgende Beispiel zeigt das Importieren dieser Bibliothek und die Verwendung der Texterkennungsfunktion.

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
Sie wollen den erkannten Text jetzt in einer Datei abspeichern, damit Sie diesen an das Lager senden können. Das folgende Beispiel zeigt den Code, um den Text "hello" in eine Datei zu schreiben.

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
Sie haben es fast geschafft. Im letzten Schritt müssen Sie jetzt die Datei an das Lager übermitteln, um diese dort prüfen zu lassen. Frau Groß hat Ihnen dafür bereits ein Skript geschrieben, das Sie im Ordner `03_SOS/solution` finden.

**Führen Sie dieses Skript wie folgt aus:**
```shell
python3 submit.py numbers.csv
```
Das Programm teilt Ihnen mit, ob Sie erfolgreich waren.


