**Przedmiot:** Uczenie głębokie w systemach rozpoznawania obiektów
**Zajęcia nr / temat:** 01 
**Autor / grupa:** Adrian Zygmutn GL 5.04
**Data:** 15.10.2026

## 1. Cel ćwiczenia

Zbudowanie i wytrenowanie sieci neuronowej do rozpoznawania 
kategorii ubrań na podstawie zdjęć, z wykorzystaniem zbioru FashionMNIST

## 2. Metoda i implementacja

- Wykorzystane narzędzia i modele.
Python, biblioteki PyTorch, torchvision oraz matplotlib
- Najważniejsze fragmenty kodu (lub link do repozytorium/notatnika).
https://github.com/AdrianZygmunt/Uczenie-g-bokie-do-rozpoznawania-obiekt-w/tree/main/L1
- Konfiguracja (parametry, dane).
Przetestowano trzy warianty architektury z różną liczbą warstw ukrytych:   (128,)(256, 128)(512, 256, 128)
## 3. Wyniki

Wariant 1: Jedna warstwa ukryta (128 neuronów), co daje 101 770 parametrów. Dokładność na zbiorze testowym wynosi około 87.5%.   Wariant 2: Dwie warstwy ukryte (256 i 128 neuronów), co przekłada się na 235 146 parametrów. Dokładność wynosi około 88.8%.   Wariant 3: Trzy warstwy ukryte (512, 256 i 128 neuronów) oraz 567 434 parametry. Ten model osiąga najwyższą dokładność na poziomie około 89.4%

## 4. Analiza i interpretacja

Zwiększanie liczby warstw i neuronów poprawiło dokładność modelu z 87.5% do niemal 89.4%. W największym modelu (Wariant 3) zaobserwowano zjawisko przeuczenia. Błędy najczęściej pojawiały się w przypadku wizualnie podobnych ubrań (np. koszula a T-shirt lub płaszcz a sweter)

## 5. Wnioski

Zwykłe sieci neuronowe (MLP) całkiem dobrze radzą sobie z rozpoznawaniem prostych, czarno-białych obrazków ubrań.   Rozbudowa sieci (dodanie większej liczby warstw) poprawiła wyniki, ale sprawiła też problem: największy model zaczął uczyć się danych treningowych "na pamięć" zamiast wyłapywać ogólne cechy.
