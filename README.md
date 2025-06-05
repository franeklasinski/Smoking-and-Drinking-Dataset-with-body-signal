
# Analiza danych z ankiet medycznych za pomocą drzew decyzyjnych 

Projekt analizuje dane zdrowotne z ankiet przy użyciu klasyfikatorów drzew decyzyjnych, w celu identyfikacji wzorców związanych ze stylem życia – na przykład spożywaniem alkoholu.

## Cel projektu

Celem było:
- Oczyszczenie i przygotowanie danych ankietowych (m.in. z koreańskiego NHIS)
- Zbudowanie modeli predykcyjnych do klasyfikacji zmiennej `DRK_YN` (czy osoba pije alkohol)
- Zidentyfikowanie kluczowych cech wpływających na zachowanie zdrowotne
- Przetestowanie skuteczności drzew decyzyjnych i ich interpretowalności

## Zbiór danych

- Źródło: Korea National Health Insurance Service (syntetyczny zbiór z zakodowanymi cechami)
- Link: https://www.kaggle.com/datasets/sooyoungher/smoking-drinking-dataset
- Liczba rekordów: ~990 000
- Przykładowe kolumny:
  - `age`, `sex`, `SBP`, `DBP`, `cholesterol`, `gamma_GTP`
  - `SMK_stat_type_cd` – palenie
  - `DRK_YN` – cel klasyfikacji (czy osoba pije alkohol)

## Technologie i biblioteki

- Python 3.10+
- Pandas, NumPy
- scikit-learn
- Matplotlib / Seaborn (do wizualizacji)
- Jupyter Notebook

## Co zostało zrobione?

- Wczytanie danych i analiza wstępna (missing values, typy danych)
- Kodowanie zmiennych kategorycznych (`sex`, `DRK_YN`)
- Przekształcenie danych do formatu float
- Budowa i trenowanie modeli decyzyjnych
- Obliczenie metryk skuteczności (accuracy, confusion matrix, ROC)
- Wizualizacja ważności cech i rozkładów

## Wyniki

- Modele drzew decyzyjnych pozwoliły trafnie klasyfikować `DRK_YN`
- Kluczowe cechy: wiek, ciśnienie, poziom GTP i cholesterol
- Drzewa oferują dobrą równowagę między skutecznością a interpretowalnością

## Pliki

- `Demo DD wyklad.ipynb` – główny notebook z kodem analizy
- `smoking_drinking_dataset.csv` – dane wejściowe (nie dołączone ze względu na rozmiar)
- `Prezentacja.pptx` – slajdy podsumowujące projekt (opcjonalnie)

## Wnioski

Drzewa decyzyjne są skutecznym i przejrzystym narzędziem do analizy danych ankietowych w kontekście zdrowia. Umożliwiają łatwe odkrywanie wzorców, które mogą być użyte w systemach wspierania decyzji medycznych.

## Licencja

Projekt edukacyjny, dane mają charakter syntetyczny. Użycie zgodne z celami dydaktycznymi.
