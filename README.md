# Tech Stack:
![image](https://img.shields.io/badge/Python-FFD43B?style=for-the-badge&logo=python&logoColor=blue)
![image](https://img.shields.io/badge/Visual%20Studio%20Code-0078d7.svg?style=for-the-badge&logo=visual-studio-code&logoColor=white)\
![elevenlabs](https://img.shields.io/badge/elevenlabs-%23ffffff.svg?style=for-the-badge&logo=data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABAAAAAQCAQAAAC1+jfqAAAATUlEQVR42mL8//8/AzWAiSTlf3zLx5kMzybBSK1FlAEIhJvYCZPAUpId4GWQEJ4gBJqGh4O6O0L2dChFsJQsGY6IoIlM0gHVSdMKEGAC1JgsVNfc2XAAAAABJRU5ErkJggg==&logoColor=black)
![PyQt5](https://img.shields.io/badge/PyQt5-%23ffffff.svg?style=for-the-badge&logo=Qt&logoColor=black)
![pygame](https://img.shields.io/badge/pygame-%23190F00.svg?style=for-the-badge&logo=python&logoColor=white)
![image](https://img.shields.io/badge/Numpy-777BB4?style=for-the-badge&logo=numpy&logoColor=white)
![image](https://img.shields.io/badge/Pandas-2C2D72?style=for-the-badge&logo=pandas&logoColor=white)
![image](https://img.shields.io/badge/Matplotlib-%23ffffff.svg?style=for-the-badge&logo=Matplotlib&logoColor=black)
![requests](https://img.shields.io/badge/requests-%23ffffff.svg?style=for-the-badge&logo=python&logoColor=3776AB)
![BeautifulSoup](https://img.shields.io/badge/BeautifulSoup-%23ffffff.svg?style=for-the-badge&logo=python&logoColor=3776AB)

# Aplikacja do nauki słówek z języka angielskiego
Aplikacja umożliwia naukę słówek języka angielskiego, wykorzystując mechanizmy gratyfikacji.\
Głównym celem aplikacji jest efektywne przyswajanie słówek, a nie ich kojarzenie.\
Skierowana jest do osób, które chcą nauczyć się lub utrwalić podstawowe słownictwo.


## Status projektu
Aplikacja jest we wstępnej fazie rozwoju.\
Obecnie identyfikowane są błędy, planowane usprawnienia oraz przeprowadzana jest weryfikacja poszczególnych funkcji.

## Demo
Widok karty "Gra 2" — ćwiczenie słuchu.
![image](https://github.com/user-attachments/assets/98973e33-e76c-425d-b43b-9823201486ac)

## Technologie
- **Interfejs:** `PyQt5`
- **Baza danych:** `JSON` (przechowywanie słówek i ich metadanych)
- **Audio:** `ElevenLabs` (generowanie plików dźwiękowych dla wymowy słówek w języku angielskim)
- **Odtwarzanie audio:** `pygame`

## Funckjonalności
Aplikacja umożliwia naukę słówek na poziomach A1-B2, podzielonych na pliki po 100 słów.\
Łącznie baza zawiera prawie 6000 słówek. Każde słowo może być przypisane do jednej z trzech kategorii:
- `znam` - słowa, które użytkownik zna i nie musi się ich uczyć
- `uczę się` - słowa, których chcemy się uczyć, otrzymują one zestaw parametrów
- `nauczone` - podczas nauki, gdy parametry danego słowa sukcesywnie się zmniejszają do określonego zakresu możemy ręcznie oznaczyć słowo jako nauczone lub aplikacja sama uzna dane słowo za nauczone

Aplikacja zawiera następujące moduły:
- `Statystyki` - wyświetla statystyki, takie jak:
  - liczba osiągniętych dziennych celów
  - wykres liczby przerobionych słów w podziale na dni
  - poziom znajomości słówek dla każdego poziomu zaawansowania
  - szczegółowe staystyki każdego pliku
- `Pierwszy raz` - przegląd słówek z wybranego pliku; użytkownik decyduje, czy słowo zostanie oznaczone jako `znam` lub `uczę się`
- `Nauka` - przegląd słówek oznaczonych jako  `uczę się`; użytkownik przepisuje słowo po angielsku, zapoznając się z jego pisownią i wymową, którą można odsłuchać
- `Gra 1` - ćwiczenie tłumaczenia; losowe słowa z wybrenego pliku wyświetlają się po polsku, a użytkownik wpisuje ich tłumaczenie po angielsku. Po poprawnym wpisaniu słowo jest również wymawiane
- `Gra 2` - ćwiczenie słuchu; losowe słowa z wybrenego pliku odtwarzane są po angielsku, a użytkownik wpisuje jego odpowiednik w rubryce

## Planowane funkcjonalności
- opracowanie systemu punktacji
- możliwość dodania własnych plików ze słówkami
- `Gra 3` - zjeżdżające kafelki z kilkoma trybami do wybory:
  - kafelki po polsku a słowo jest czytane po angielsku
  - kafelki po polsku a słowo jest wyświetlane po angielsku
  - kafelki po angielsku a słowo jest wyświetlane po polsku
- `Gra 4` - łączenie par np. z 12 kafelków
- `Gra 5` - generowanie zdań w języku angielskim przez LLM (np. Mistral) względem wybranej tematyki lub słownictwa, jedno ze słów jest usuwane a my musimy je uzupełnić
- znalezienie słów podobnych, zarówno w pisowni (odległość Levenshteina) jak i fonetycznie (są dostępne biblioteki do tego), słowa podobne będą ze sobą zestawiane np. w grze 3
- przeniesienie funkcji tworzenia plików audio, na ten moment tworzone są ręcznie w odrębnym notebook'u, docelowo będą one tworzone na etapie przyporządkowania słów, gdy trafi do grupy `uczę się` zostanie stworzony plik audio
- stworzenie kilku plików audio dla każdego słowa, żeby nie przyzwyczajać się do konkretnej wymowy 
