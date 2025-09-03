# 🌱 Rozpoznawanie chorób roślin / Plant Disease Recognition

## Autorzy  
- Weronika Poniedziałek
- Patrycja Mazur

## Opis projektu
Projekt zrealizowany w ramach przedmiotu **"Automatyczna analiza obrazu”** na Politechnice Lubelskiej.  
Celem było opracowanie i porównanie modeli głębokiego uczenia do **rozpoznawania chorób roślin na podstawie zdjęć liści**. W ramach projektu przygotowano sieć konwolucyjną (Custom CNN) oraz zastosowano technikę Transfer Learning z wykorzystaniem EfficientNet-B0.  

## Zbiór danych
W projekcie wykorzystano zbiór danych:  
[New Plant Diseases Dataset (Kaggle)](https://www.kaggle.com/datasets/vipoooool/new-plant-diseases-dataset)  

Charakterystyka zbioru:  
- 38 klas chorób roślin,  
- ~76 000 zdjęć w zbiorze treningowym,  
- łącznie ~87 000 obrazów,  
- format zdjęć: kolorowe obrazy liści w różnych warunkach.  

## Cel projektu
- Identyfikacja i klasyfikacja chorób roślin na podstawie obrazu.  
- Porównanie skuteczności sieci CNN z modelem bazującym na Transfer Learning.  
- Analiza metryk jakości (accuracy, precision, recall, F1-score) oraz czasu trenowania.  

## Wykorzystane technologie
- **Język programowania**: Python 
- **Biblioteki**: PyTorch, torchvision, numpy, matplotlib, scikit-learn  
- **Techniki uczenia maszynowego**:  
  - klasyczna sieć konwolucyjna (Custom CNN),  
  - Transfer Learning (EfficientNet-B0, ResNet-50).  

## Struktura projektu
1. **Przygotowanie danych**: wczytanie, zmiana rozmiaru do 224x224 pikseli, normalizacja, preprocessing, augmentacja (odbicia, obroty, przesunięcia, zmiany jasności).  
2. **Modelowanie**:  
   - Custom CNN trenowana od podstaw,  
   - Transfer Learning z EfficientNet-B0 (ImageNet) – trenowanie głowy klasyfikacyjnej + fine-tuning wybranych warstw.  
3. **Ewaluacja**: obliczenie accuracy, precision, recall, F1-score.  
4. **Porównanie modeli**: zestawienie wyników jakościowych i czasów trenowania.  

## Wyniki i wnioski
- **Custom CNN** osiągnęła bardzo dobre wyniki:  
  - Accuracy: 0.91, Precision: 1.00, Recall: 0.91, F1-score: 0.95  
- **EfficientNet-B0 (Transfer Learning)** wypadła znacznie słabiej:  
  - Accuracy: 0.15, Precision: 0.64, Recall: 0.15, F1-score: 0.24  
- Czas trenowania:  
  - Custom CNN: ~1h 20 min  
  - EfficientNet-B0: ~30 min  
- Wnioski:  
  - CNN sprawdził się lepiej w tym zadaniu niż Transfer Learning,  
  - Dobór architektury ma kluczowe znaczenie przy dużych zbiorach danych.  

## Bibliografia
- [PyTorch CNN Tutorial (Datacamp)](https://www.datacamp.com/tutorial/pytorch-cnn-tutorial)  
- [Transfer Learning w PyTorch](https://www.learnpytorch.io/06_pytorch_transfer_learning/)  
