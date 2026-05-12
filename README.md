# Polish Road Sign Recognition

## Environment setup

Install the notebook dependencies in the same Python environment used by the Jupyter kernel:

```powershell
python -m pip install -r requirements.txt
```

From inside `notebooks/Sign-Recognition.ipynb`, you can also run:

```python
%pip install -r ../requirements.txt
```

Projekt dotyczy rozpoznawania polskich znaków drogowych na zdjęciach z wykorzystaniem modeli YOLO11.

## Cel projektu

Celem projektu jest przygotowanie systemu, który na podstawie zdjęcia pojedynczego znaku drogowego rozpozna jego klasę oraz znaczenie, np. `B-20 STOP`, `B-33 ograniczenie prędkości do 50 km/h`, `D-6 przejście dla pieszych` lub `A-7 ustąp pierwszeństwa`.

Projekt skupia się na klasyfikacji obrazów znaków drogowych. Wejściem do modelu będzie zdjęcie pojedynczego znaku, a wyjściem przewidziana klasa znaku.

## Dane

Dane będą pochodziły ze zbioru polskich znaków drogowych podzielonych na klasy. Obrazy zostaną przygotowane do treningu poprzez zmianę rozmiaru, normalizację oraz podział na zbiór treningowy, walidacyjny i testowy.

## Modele

W projekcie zostanie porównanych kilka wariantów modelu YOLO11, np.:

- YOLO11n
- YOLO11s
- YOLO11m

Porównanie ma pokazać, który wariant osiąga najlepszy kompromis między skutecznością rozpoznawania a czasem działania.

## Plan projektu

1. Wczytanie i przygotowanie danych.
2. Analiza danych, w tym liczba zdjęć w każdej klasie i przykładowe obrazy.
3. Podział danych na zbiory treningowy, walidacyjny i testowy.
4. Trening kilku wariantów YOLO11.
5. Porównanie modeli na podstawie accuracy, precision, recall i F1-score.
6. Przygotowanie macierzy pomyłek dla najlepszego modelu.
7. Zapis wytrenowanego modelu.
8. Przygotowanie prostego skryptu do testowania modelu na nowym zdjęciu.
9. Sformułowanie wniosków końcowych.
