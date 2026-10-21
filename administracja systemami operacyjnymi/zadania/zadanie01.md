# Projekt praktyczny: Rozbudowa struktury zasobów systemowych firmy TechCorp

**Temat:** Praktyczne operacje na katalogach, ścieżki względne/bezwzględne i weryfikacja zasobów

---

## Scenariusz branżowy

Zostałeś zatrudniony jako młodszy administrator w dynamicznie rozwijającej się firmie **TechCorp**. Zarząd podjął decyzję o uporządkowaniu struktury katalogów na serwerze głównym oraz o przygotowaniu szablonów dokumentów dla nowych działów i projektów. Twoim zadaniem jest stworzenie pełnej struktury folderów, przygotowanie wstępnych plików oraz ich bezpieczna archiwizacja i weryfikacja.

---

## Wymagania projektowe (Do wykonania krok po kroku)

### Etap 1: Inicjalizacja i sprawdzenie środowiska

1. Upewnij się, że znajdujesz się w swoim katalogu domowym (`~`). Sprawdź i potwierdź swoją bieżącą ścieżkę poleceniem systemowym.
2. Utwórz główny katalog roboczy o nazwie `TechCorp_Project`.

---

### Etap 2: Tworzenie wielopoziomowej struktury drzewiastej

Za pomocą **jednego zoptymalizowanego polecenia** `mkdir` z odpowiednimi opcjami i nawiasami klamrowymi `{}` utwórz wewnątrz `TechCorp_Project` następującą strukturę katalogów:

```text
TechCorp_Project/
├── Dzialy/
│   ├── IT/
│   │   ├── Serwery
│   │   └── Bazy_Danych
│   ├── HR/
│   │   └── Rekrutacja
│   └── Finanse/
│       └── Raporty
├── Projekty/
│   ├── 2026/
│   │   ├── Serwer_Linux
│   │   └── Chmura
│   └── Archiwum
└── Szablony

```

---

### Etap 3: Generowanie i porządkowanie plików wzorcowych

Wykonaj poniższe operacje, używając łączonych poleceń CLI oraz ścieżek bezwzględnych lub względnych:

1. W katalogu `Szablony` utwórz dwa puste pliki: `notatka_wzor.txt` oraz `raport_wzor.txt`.
2. Skopiuj plik `notatka_wzor.txt` z katalogu `Szablony` do katalogu `TechCorp_Project/Dzialy/IT/Serwery/` i zmień jego nazwę przy kopiowaniu na `notatka_serwer.txt`.
3. Skopiuj plik `raport_wzor.txt` do katalogu `TechCorp_Project/Dzialy/Finanse/Raporty/` pod nazwą `raport_q1.txt`.
4. Utwórz w katalogu `TechCorp_Project/Projekty/2026/Serwer_Linux/` plik `opisy.txt`, zawierający wiersz tekstu z nazwą Twojego konta użytkownika.

---

### Etap 4: Reorganizacja i czyszczenie zasobów

1. Zarząd podjął decyzję o rezygnacji z podkatalogu `Chmura` w projektach 2026. Usuń ten katalog z systemu.
2. Przenieś katalog `Bazy_Danych` z `Dzialy/IT/` do katalogu `Projekty/2026/`.

---


### Etap 5: Audyt i weryfikacja końcowa (2 min)

1. Wyświetl pełną, rekurencyjną listę wszystkich utworzonych katalogów oraz plików w katalogu `TechCorp_Project` z uwzględnieniem praw dostępu i rozmiarów (`ls -lR`).
2. Przekieruj wynik tego podsumowania do pliku `struktura_podsumowanie.txt` znajdującego się bezpośrednio w katalogu `TechCorp_Project`.

---


## Tabela weryfikacji efektów (Klucz dla nauczyciela / ucznia)

| Krok | Weryfikowane umiejętności | Oczekiwane polecenie (przykładowe) |
| --- | --- | --- |
| **Etap 1** | Nawigacja i `pwd` | `cd ~ && pwd` |
| **Etap 2** | Tworzenie rozbudowanych drzew katalogów | `mkdir -p TechCorp_Project/{Dzialy/{IT/{Serwery,Bazy_Danych},HR/Rekrutacja,Finanse/Raporty},Projekty/{2026/{Serwer_Linux,Chmura},Archiwum},Szablony}` |
| **Etap 3** | Operacje `touch` i `cp` ze zmianą nazwy | `touch TechCorp_Project/Szablony/{notatka_wzor.txt,raport_wzor.txt}` oraz `cp TechCorp_Project/Szablony/notatka_wzor.txt TechCorp_Project/Dzialy/IT/Serwery/notatka_serwer.txt` |
| **Etap 4** | Przenoszenie (`mv`) i usuwanie (`rmdir`) | `rmdir TechCorp_Project/Projekty/2026/Chmura` oraz `mv TechCorp_Project/Dzialy/IT/Bazy_Danych TechCorp_Project/Projekty/2026/` |
| **Etap 5** | Rekurencja i przekierowanie strumienia (`>`) | `ls -lR TechCorp_Project > TechCorp_Project/struktura_podsumowanie.txt` |

