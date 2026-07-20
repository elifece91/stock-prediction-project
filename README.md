# Apple (AAPL) Hisse Senedi Fiyat Tahmin Projesi (PyTorch)

Bu proje, Apple Inc. (AAPL) şirketinin geçmiş hisse senedi kapanış fiyatlarını kullanarak gelecekteki fiyat trendlerini tahmin etmek amacıyla geliştirilmiştir. Proje kapsamında PyTorch kullanılarak modern Derin Öğrenme (LSTM & GRU) modelleri karşılaştırmalı olarak analiz edilmiştir.

---

## 🚀 Kurulum ve Çalıştırma Talimatları

Projeyi yerel bilgisayarınızda çalıştırmak için aşağıdaki adımları takip edebilirsiniz:

1. **Gerekli kütüphaneleri yükleyin:**
   ```bash
   pip install yfinance pandas matplotlib scikit-learn torch torchvision torchaudio seaborn jupyter
   ```

2. **Projeyi başlatın:**
   Jupyter Notebook uygulamasını açın ve `Apple_Stock_Prediction.ipynb` dosyasını çalıştırın (Tüm hücreleri çalıştır / Run All).

---

## 📊 Kullanılan Veri Seti

- **Kaynak:** Yahoo Finance (`yfinance` kütüphanesi)
- **Hisse Senedi:** Apple (AAPL)
- **Zaman Aralığı:** 2021-01-01 - Günümüz (Günlük Kapanış Fiyatları)

---

## 🔍 Model Performans Karşılaştırmaları (Metrics)

Modellerin test veri seti üzerindeki başarı oranları aşağıdaki hata payı kriterlerine (MSE ve RMSE) göre ölçülmüştür. İki model de PyTorch mimarisiyle 60 tur (Epoch) eğitilmiştir:

| Model | Mean Squared Error (MSE) | Root Mean Squared Error (RMSE) |
| --- | --- | --- |
| LSTM | 109.95 | 10.49 |
| GRU (Şampiyon) | 37.95 | 6.16 |

---

## 💡 Proje Bulguları ve Özet Analiz

- **LSTM vs GRU:** Her iki derin öğrenme modeli de zaman serilerindeki geçmiş verileri hafızasında tutma yeteneği sayesinde fiyat hareketlerini takip etmiştir. Ancak GRU modeli çok daha hızlı öğrenmiş ve daha az hata payına sahip olmuştur.
- **Sonuç:** GRU modeli, ani fiyat değişimlerine daha hızlı adapte olan sade mimarisi sayesinde 6.16 RMSE skoru elde ederek projenin en başarılı modeli olmuştur.
