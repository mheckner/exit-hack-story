# Texterkennung
Für diese Aufgabe sollen Sie die Daten auf einem Bild analysieren. Gehen Sie wie folgt vor.

## Hello World in Python ausführen
Im Ordner "03_SOS/examples" finden Sie die Datei "hello_world.py"
Führen Sie zuerst dieses Programm auf der Kommandozeile aus, bevor Sie weiter fortfahren.

## Bilderkennung
Für diese Aufgabe sollen Sie die Zahlen auf einem Bild erkennen. Dazu müssen Sie das Bild erst öffnen. Dies können Sie mit der Bibliothek Image erledigen. Das folgende Codebeispiel zeigt das Öffnen eines Bilds:

```python
from PIL import Image

def main():
    image = Image.open("mein_bild.png")
    
if __name__ == "__main__":
    main()
```

Um die Zahlen auf dem Bild zu erkennen, können Sie die Bibliothek pytesseract verwenden. Das folgende Beispiel zeigt das Importieren dieser Datei und die Verwendung der Texterkennungsfunktion.

```python
import pytesseract

def main():
    text_in_image = pytesseract.image_to_string(image)
    
if __name__ == "__main__":
    main()
```
text_in_image enthält den Text, den die Funktion image_to_string in dem als Parameter übergebenen Bild gefunden hat. Geben Sie jetzt den Text auf der Kommandozeile aus.

## Text in einer Datei abspeichern


## Datei übermitteln und überprüfen


