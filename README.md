# Bool Kombajn 🚜

**Interaktywny symulator logiki boolowskiej i algebry Boole'a** – kompletne narzędzie edukacyjne do techniki cyfrowej.

**Zaprojektował i zbudował: Paweł K** 🛠️

## 🎯 O Projekcie

Bool Kombajn to nowoczesna aplikacja webowa (PWA) do nauki i eksperymentowania z:
- **Wyrażeniami boolowskimi** – parsowanie i ewaluacja
- **Minimalizacją funkcji** – algorytm Quine-McCluskey
- **Mapami Karnaugh** – wizualizacja i zaznaczanie grup
- **Schematami bramkowymi** – reprezentacja sprzętowa (AND/OR, NAND/NOR)
- **Testowaniem logiki** – weryfikacja wartości wyjściowych

## ✨ Główne Funkcje

### 1. Parser Wyrażeń Boolowskich
Wprowadź wyrażenia logiczne w naturalnej notacji:
- **OR** (suma): `+`
- **AND** (iloczyn): `*`, `·`
- **NOT** (negacja): `!`, `~`, `'`, `` ` ``
- **Nawiasy**: `(`, `)`

Przykład: `(A+B)·C' + A·B·C`

### 2. Algorytm Quine-McCluskey
Automatyczna minimalizacja funkcji logicznych:
- Wczytanie mintermów i don't-care
- Iteracyjne łączenie terminów
- Wyszukiwanie pokrycia minimalne
- Wizualizacja wszystkich kroków

### 3. Mapy Karnaugh
Interaktywne mapy dla 2–6 zmiennych:
- Kolorowe zaznaczanie grup pierwotnych (prime implicants)
- Klik na komórkę → ustawienie wartości (0, 1, X)
- Automatyczne wyliczanie wyniku na mapie
- Obsługa don't-care

### 4. Schematy Bramkowe
Wygenerowane diagramy logiczne:
- **Implementacja SOP** (Sum of Products) – AND + OR
- **Implementacja POS** (Product of Sums) – OR + AND
- **NAND-NAND** – uniwersalne NAND
- **NOR-NOR** – uniwersalne NOR
- Automatyczne rozmieszczanie bramek i inwerterów

### 5. Testowanie & Weryfikacja
- Tablica prawdy (truth table)
- Ewaluacja wyrażeń dla dowolnych kombinacji wejść
- Wskaźnik zgodności minimalizacji
- Porównanie oryginalnych i zminimalizowanych funkcji

## 📱 Cechy PWA

✅ **Offline-first** – działa bez internetu  
✅ **Instalowalne** – dodaj do ekranu głównego  
✅ **Responsywne** – telefon, tablet, desktop  
✅ **Szybkie** – React + preoptymalizowany kod  
✅ **Bez zależności** – brak npm, jeden plik  

## 🚀 Szybki Start

### Online
Otwórz w przeglądarce: https://caprianopl.github.io/BooleanPWA/

### Offline
1. Otwórz aplikację online
2. Przycisk menu (⋮) → "Zainstaluj"
3. Aplikacja dostępna offline!

## 💻 Technologia

- **React 18** – interfejs użytkownika
- **Vanilla JS** – parser, QMC, algorytmy
- **SVG** – diagramy bramek
- **PWA** – manifest + service worker

## 📚 Jak Używać?

### Przykład 1: Minimalizacja Funkcji
```
Wejście: A·B + A·B·C' + A·C
Mintemy: 3, 4, 5, 7
Rezultat: A + B·C (zminimalizowane)
```

### Przykład 2: Tablica Prawdy
```
f = A + B'·C

  A B C | f
  ------+---
  0 0 0 | 0
  0 0 1 | 1
  0 1 0 | 0
  0 1 1 | 0
  1 0 0 | 1
  1 0 1 | 1
  1 1 0 | 1
  1 1 1 | 1
```

### Przykład 3: Mapa Karnaugh 3-zmiennych
```
Wpisz mintery → mapa się generuje → zaznacz grupy
Algorytm zaproponuje optymalne pokrycie
```

## 🎓 Dla Nauczycieli

Idealne do:
- 📖 Lekcji o algebrze Boole'a
- 🔧 Laboratorium techniki cyfrowej
- 📝 Prac domowych i testów
- 💡 Dyskusji nad optymalnym schematem

**Bez instalacji, bez konfiguracji – otwórz i ucz!**

## 🐛 Znane Ograniczenia

- Maksymalnie **6 zmiennych** (limit mapy Karnaugh)
- Parser: notacja infikowa (nie RPN)
- Don't-care (X) – tylko do 4 zmiennych w pełnej optymalizacji

## 🔧 Rozwój

Aby rozwijać:
```bash
# Klonuj
git clone https://github.com/caprianopl/BooleanPWA.git

# Edytuj index.html – wszystko w jednym pliku
# Testuj w przeglądarce (F5)
# Commituj i push
```

### Struktura Kodu
```
index.html
├── React + ReactDOM (CDN)
├── Parser wyrażeń boolowskich (lex + BParser)
├── Quine-McCluskey (QMC algorithm)
├── Mapy Karnaugh (kCells, piCoverage)
├── Generowanie schematów (Gates component)
└── UI (React components)
```

## 📄 Licencja

MIT – używaj, modyfikuj, rozpowszechniaj

## 🙋 Wsparcie

Znalazłeś błąd? Masz pomysł?  
→ [Otwórz issue](https://github.com/caprianopl/BooleanPWA/issues)

---

**Bool Kombajn** – najmądrzejsza maszyna do logiki boolowskiej 🚜✨

*Zaprojektowała i zbudowała: **Paweł K*** 🛠️
