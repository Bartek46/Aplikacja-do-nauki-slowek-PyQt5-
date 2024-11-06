*README nie zostało jeszcze skończone, jest to zarys konieczny do porpawy.*

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
Celem aplikacji jest nauka słówek wykorzystując mechanizmy gratyfikacji.
Aplikacja jest skierowana do osób chcących nauczyć się lub utrwalić podstawowe słownictwo.

## Status projektu
Aplikacja jest we wstępnej fazie rozwoju.\
W obecnym momencie identyfikowane są błędy, planowane usprawnienia aplikacji oraz weryfikacja każdej funkcjonalności.

## Demo
Wkrótce link do yt.

## Technologie
Interfejs został napisany w `PyQt5`.\
Dane (słówka) przechowywane są w `.json`.\
Za pomocą api `ElevenLabs` tworzone są pliki audio z wymawianymi słówkami po angielsku.\
`pygame` służy do odczytywania plików audio.

## Funckjonalności
Możliwe jest już uczenie sie słówek z języka angielskiego w podziale na poziomy A1-B2.\
Każdy poziom został podzielony na pliki po 100 słówek, razem prawie 6k słów.\
Każde słowo będzie przyporządkowane do jednej z trzech grup:
- `znam` - słowa, które znamy wystarczjąco dobrze i nie musimy się go uczyć
- `uczę się` - słowa, których chcemy się uczyć, otrzymują one zestaw parametrów
- `nauczone` - podczas nauki, gdy parametry danego słowa sukcesywnie się zmniejszają do określonego zakresu możemy ręcznie oznaczyć słowo jako nauczone lub aplikacja sama uzna dane słowo za nauczone.

Aplikacja składa się z kart/okien:
- Statystyki - zbiór statystyk takich jak:
  - liczba osiągniętych dziennych celów
  - wykres liczby przerobionych słów w podziale na dni
  - przedstawienie każdego poziomu w podziale na znajomość słówek
  - szczegółowe przedstawienie staystyk każdego pliku
- Pierwszy raz - przechodzi się po każdym słowie z pliku i decyduje się czy słowo oznaczone będzie jako `znam` lub `uczę się`
- Nauka - przechodzi się po każdym słowie z pliku oznaczonym jako `uczę się` i przepisuje się słowo po angielsku, celem zapoznania się ze słowem, dodatkowo każde słowo jest wymawiane
- Gra 1 - tłumaczenie, po wybraniu pliku do nauki, losowo jest wyświetlane słowo po polsku - celem jest wpisanie tłumaczenia do rubryki, dodatkowo po poprawnym wpisaniu słowo jest wymawiane
- Gra 2 - ćwiczenie słuchu, po wybraniu pliku do nauki, losowo wybierane jest słowo dla któego uruchiamiany jest plik audio - celem jest rozpoznanie słowa po angielsku i wpisanie go do rubryki

## Planowane funkcjonalności
- dodanie własnych plików ze słówkami
- Gra 3 -
- Gra 4 - 
- Gra 5 -
- przeniesienie funkcji tworzenia plików audio, na ten moment tworzone są w odrębnym notebook'u, docelowo będą one tworzone na etapie przyporządkowania słów, gdy trafi do grupy `uczę się` zostanie stworzony plik audio.
- stworzenie kilku plików audio dla każdego słowa
