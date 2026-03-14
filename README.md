# 🌦️ World War II Weather Prediction - Linear Regression

## 📋 Proje Özeti
Bu proje, 2. Dünya Savaşı sırasında toplanan tarihsel verileri kullanarak günlük **Maksimum Sıcaklık (MaxTemp)** tahminlemesi yapmayı amaçlamaktadır.

## 🛠️ Kullanılan Teknolojiler
* **Python** (Pandas, NumPy)
* **Matplotlib & Seaborn**
* **Scikit-Learn**

## 🧹 Veri Temizleme
* %50'den fazlası boş olan sütunlar elendi.
* "T" (Trace) değerleri sayısal verilere dönüştürüldü.
* Gereksiz tarih sütunları temizlendi.

## 📊 Model Performansı

| Model | MAE | MSE | R² Score |
| :--- | :--- | :--- | :--- |
| **Linear Regression** | **3.1345** | **17.1115** | **0.7746** |
| Ridge Regression | 3.1345 | 17.1115 | 0.7746 |
| Lasso Regression | 3.1879 | 18.8319 | 0.7519 |

## 📈 Bulgular
* **MinTemp** ile **MaxTemp** arasında **0.88** oranında güçlü bir ilişki vardır.
* Model yaklaşık **3.1°C** hata payı ile doğru tahmin yapabilmektedir.
