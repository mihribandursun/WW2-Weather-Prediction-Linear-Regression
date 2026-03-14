# WW2-Weather-Prediction-Linear-Regression
Linear regression model to predict maximum temperature using World War II weather data.

World War II Weather Prediction - Linear Regression
Bu proje, 2. Dünya Savaşı sırasında toplanan tarihsel verileri kullanarak günlük Maksimum Sıcaklık (MaxTemp) tahminlemesi yapmayı amaçlamaktadır. Proje kapsamında kapsamlı veri temizliği, keşifçi veri analizi (EDA) ve çeşitli doğrusal regresyon modelleri (Linear, Lasso, Ridge, ElasticNet) uygulanmıştır.

📋 Proje Özeti
Veri seti, o dönemdeki hava istasyonlarından gelen günlük yağış, kar ve sıcaklık değerlerini içermektedir. Temel odak noktamız, bağımsız değişkenler (özellikle MinTemp ve Precip) ile bağımlı değişken (MaxTemp) arasındaki ilişkiyi modellemektir.

🛠️ Kullanılan Teknolojiler
Python (Temel dil)

Pandas & NumPy (Veri manipülasyonu ve temizliği)

Matplotlib & Seaborn (Veri görselleştirme ve korelasyon analizi)

Scikit-Learn (Makine öğrenmesi modelleri ve değerlendirme metrikleri)

🧹 Veri Temizleme ve Hazırlık
Proje sürecinde uygulanan adımlar:

Gereksiz Sütunların Temizlenmesi: %50'den fazlası boş olan sütunlar (WindGustSpd, PoorWeather vb.) elendi.

Veri Tipi Dönüşümü: Sayısal olması gereken ancak "T" (Trace) veya hatalı metinler içeren sütunlar pd.to_numeric(..., errors='coerce') ile temizlendi.

Eksik Veri Yönetimi: Tahminleme için kritik olan MaxTemp ve MinTemp sütunlarındaki boş satırlar temizlendi.

Ölçeklendirme: Modellerin daha iyi performans göstermesi için StandardScaler uygulandı.

📊 Model Performansı
Farklı regresyon algoritmaları test edilmiş olup, temel modellerin performans metrikleri aşağıdadır:

Model	MAE	MSE	R² Score
Linear Regression	3.1345	17.1115	0.7746
Ridge Regression	3.1345	17.1115	0.7746
Lasso Regression	3.1879	18.8319	0.7519
ElasticNet	3.4883	26.1159	0.6560
Not: Linear ve Ridge modelleri birbirine çok yakın en yüksek performansı sergilemiştir.

📈 Bulgular
Minimum Sıcaklık (MinTemp) ile Maksimum Sıcaklık (MaxTemp) arasında çok güçlü bir pozitif korelasyon (0.88) saptanmıştır.

Yağış miktarının (Precip) sıcaklık üzerindeki etkisi istatistiksel olarak mevcut olsa da, korelasyon katsayısı oldukça düşüktür.

Modelimiz, günlük sıcaklığı yaklaşık 3.1°C hata payı ile tahmin edebilmektedir.

🚀 Nasıl Çalıştırılır?
Veri setini Kaggle üzerinden indirin.

Gerekli kütüphaneleri yükleyin: pip install pandas numpy matplotlib seaborn scikit-learn

LinearRegressionExercise.ipynb dosyasını Jupyter Notebook veya VS Code üzerinden çalıştırın.
