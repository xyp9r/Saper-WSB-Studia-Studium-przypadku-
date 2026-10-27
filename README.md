# Gra Saper (Minesweeper) w C#

    Konsolowa implementacja klasycznej gry logicznej **Saper** napisana w języku C#.
    
    ---
    
    ## 📌 Opis działania
    
    Gra działa w trybie turowym w konsoli:
    - **Rozmiar planszy:** 10 × 10 pól (współrzędne od `0` do `9`).
    - **Liczba min:** 15 bomb rozmieszczanych losowo na początku rozgrywki.
    - **Zasady gry:**
      - Gracz podaje współrzędne pola `x y` do odkrycia.
      - Trafienie na minę (`*`) oznacza natychmiastową przegraną (*"Boom! Koniec gry."*).
      - Odkrycie bezpiecznego pola wyświetla liczbę bomb znajdujących się w jego
      bezpośrednim sąsiedztwie (od `0` do `8`).
      - Jeśli pole ma wartość `0`, gra automatycznie (rekurencyjnie) odkrywa sąsiadujące
      puste pola.
      - **Warunek wygranej:** odkrycie wszystkich pól niezawierających min (czyli 85
      pól).
    
    ---
    
    ## ⚙️ Wymagania
    
    - [.NET SDK](https://dotnet.microsoft.com/download) (np. .NET 6 / 7 / 8 lub nowszy)
    albo kompilator `csc` / `mono`.
    
    ---

    ## 🚀 Jak uruchomić

    ### Sposób 1: .NET CLI (Zalecany)

    1. W katalogu projektu utwórz plik konfiguracyjny (jeśli jeszcze nie istnieje):
       ```bash
       dotnet new console --force

2. Uruchom grę:
   dotnet run


### Sposób 2: Bezpośrednia kompilacja

Windows (csc):

    csc saper.cs
    saper.exe

macOS / Linux (mono):

    mcs saper.cs
    mono saper.exe
──────
## 🎮 Instrukcja rozgrywki

1. Po uruchomieniu na ekranie wyświetli się plansza z indeksami kolumn (x) i wierszy
   (y) w zakresie 0–9.
2. Wprowadź współrzędne pola oddzielone spacją:
   Podaj współrzędne (x, y) do odkrycia (np. 2 3):
   2 3
   (gdzie 2 to kolumna x, a 3 to wiersz y).
3. Odkryj całą planszę omijając miny, aby wygrać!