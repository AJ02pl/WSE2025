# WSE2025
Kalkulator mandatów poselskich według głosów metodą D'Hondta

Krok 1: Wprowadzenie danych

Wybierz tryb wprowadzania:

🗳️ Liczba głosów - wprowadź konkretną liczbę głosów
📊 Procenty - wprowadź procent głosów (aplikacja automatycznie przelicza)


Dodaj partie:

Kliknij "➕ Dodaj kolejną partię" aby dodać nową partię
Wybierz kolor partii (kliknij kolorowy kółko)
Wpisz nazwę partii/komitetu wyborczego
Wprowadź liczbę głosów lub procent (zależnie od trybu)


Zarządzaj partiami:

Usuń niepotrzebne partie przyciskiem "×"
Dodaj tyle partii ile potrzebujesz
Aplikacja automatycznie ładuje przykładowe dane z wyborów 2023# 🏛️ Kalkulator Mandatów Poselskich do Sejmu



📋 Dane autora

Autor: A.J Truskolawski

Przedmiot: Pracownia Programowania
Data: Lipiec 2025

📝 Opis projektu
Kalkulator Mandatów Poselskich to aplikacja webowa służąca do obliczania podziału mandatów w Sejmie RP na podstawie wyników wyborów parlamentarnych. Aplikacja wykorzystuje metodę D'Hondta, która jest oficjalnie stosowana w polskim systemie wyborczym.
🎯 Funkcjonalności

Obliczanie mandatów - automatyczny podział 460 mandatów między partie
Metoda D'Hondta - oficjalna metoda stosowana w polskim systemie wyborczym
Progi wyborcze - uwzględnienie 5% progu dla partii i 8% dla koalicji
Dynamiczne dodawanie partii - dodaj dowolną liczbę partii z własnymi nazwami
Dwa tryby wprowadzania - liczba głosów lub procenty
Kolory partii - możliwość wyboru koloru dla każdej partii
Wizualizacja Sejmu - graficzna reprezentacja 460 miejsc w układzie półkolistym
Interfejs użytkownika - nowoczesny, responsywny design
Wizualizacja wyników - przejrzyste karty z wynikami dla każdej partii
Podsumowanie - szczegółowe statystyki podziału mandatów

🔧 Technologie

HTML5 - struktura aplikacji
CSS3 - stylizacja z wykorzystaniem gradientów i animacji
JavaScript - logika obliczeniowa i interakcja z użytkownikiem
Responsive Design - aplikacja działa na wszystkich urządzeniach

🚀 Instrukcja uruchomienia
Wymagania systemowe

Przeglądarka internetowa (Chrome, Firefox, Safari, Edge)
Brak dodatkowych zależności - aplikacja działa offline

Sposób uruchomienia

Pobierz pliki
bashgit clone [URL-do-twojego-repozytorium]
cd kalkulator-mandatow

Uruchom aplikację

Otwórz plik index.html w przeglądarce internetowej
Lub kliknij dwukrotnie na plik index.html


Alternatywnie - serwer lokalny
bash# Python 3
python -m http.server 8000

# Python 2
python -m SimpleHTTPServer 8000

# Node.js (jeśli zainstalowane)
npx http-server
Następnie otwórz http://localhost:8000 w przeglądarce

📖 Instrukcja użytkowania
Krok 1: Wprowadzenie danych

Wpisz nazwy partii/komitetów wyborczych w odpowiednich polach
Wprowadź liczbę głosów dla każdej partii
Aplikacja automatycznie ładuje przykładowe dane z wyborów 2023

Krok 2: Obliczenie wyników

Kliknij przycisk "Przelicz Mandaty"
Aplikacja automatycznie:

Sprawdzi próg wyborczy (5% dla partii)
Wykluczy partie poniżej progu
Obliczy podział mandatów metodą D'Hondta



Krok 3: Analiza wyników

Karty wyników - każda partia ma swoją kartę z:

Nazwą partii
Liczbą głosów
Liczbą mandatów
Procentem głosów


Podsumowanie - statystyki ogólne podziału

🧮 Algorytm - Metoda D'Hondta
Aplikacja implementuje oficjalną metodę D'Hondta używaną w wyborach do Sejmu:

Sprawdzenie progu wyborczego

Partie: minimum 5% głosów
Koalicje: minimum 8% głosów


Obliczenie ilorazów

Dla każdej partii: głosy ÷ (mandaty + 1)
Najwyższy iloraz otrzymuje kolejny mandat


Iteracja

Proces powtarzany 460 razy (liczba mandatów w Sejmie)



Przykład obliczeń:
Partia A: 1000 głosów
Partia B: 600 głosów

Runda 1: A=1000/1=1000, B=600/1=600 → mandat dla A
Runda 2: A=1000/2=500, B=600/1=600 → mandat dla B
Runda 3: A=1000/2=500, B=600/2=300 → mandat dla A
📁 Struktura projektu
kalkulator-mandatow/
├── index.html          # Główna aplikacja
├── README.md           # Dokumentacja projektu
└── screenshots/        # Zrzuty ekranu (opcjonalnie)
    ├── interface.png
    └── results.png
🎨 Funkcje interfejsu
Design

Gradient tło - nowoczesny wygląd z kolorami niebiesko-fioletowymi
Glassmorphism - efekt przezroczystego szkła
Animacje hover - interaktywne elementy reagujące na najechanie
Responsive design - automatyczne dostosowanie do rozmiaru ekranu

Użyteczność

Autouzupełnianie - przykładowe dane z prawdziwych wyborów
Walidacja - sprawdzanie poprawności wprowadzonych danych
Smooth scrolling - płynne przewijanie do wyników
Tooltips - informacje o progach wyborczych

🧪 Przykładowe dane
Aplikacja zawiera predefiniowane dane z wyborów parlamentarnych 2023:

Prawo i Sprawiedliwość: 8,051,935 głosów
Koalicja Obywatelska: 5,060,355 głosów
Trzecia Droga: 2,547,394 głosów
Lewica: 1,223,266 głosów

🔍 Testowanie
Scenariusze testowe:

Test podstawowy - wprowadzenie 4 partii z różną liczbą głosów
Test progu wyborczego - partie poniżej 5%
Test walidacji - puste pola, nieprawidłowe dane
Test responsywności - różne rozmiary ekranów

Weryfikacja wyników:

Suma mandatów = 460
Tylko partie powyżej progu otrzymują mandaty
Partia z największą liczbą głosów otrzymuje najwięcej mandatów

📊 Statystyki techniczne

Rozmiar pliku: ~15KB (HTML + CSS + JavaScript)
Czas ładowania: < 1 sekunda
Kompatybilność: wszystkie nowoczesne przeglądarki
Responsywność: telefony, tablety, komputery

🤝 Rozszerzenia
Potencjalne funkcjonalności do dodania:

Import danych z pliku CSV/Excel
Eksport wyników do PDF
Wizualizacja wykresów (diagramy kołowe, słupkowe)
Porównanie z poprzednimi wyborami
Kalkulator dla wyborów samorządowych
Symulacja różnych scenariuszy wyborczych

📜 Licencja
Projekt stworzony na potrzeby zaliczenia pracowni programowania.
Autor: [Twoje dane]
🆘 Rozwiązywanie problemów
Częste problemy:

Aplikacja się nie ładuje

Sprawdź czy plik index.html jest w głównym folderze
Upewnij się, że używasz nowoczesnej przeglądarki


Błędne wyniki

Sprawdź czy wprowadzone dane są liczbami
Upewnij się, że co najmniej jedna partia przekracza 5%


Problemy z wyświetlaniem

Odśwież stronę (F5)
Sprawdź czy masz włączony JavaScript
