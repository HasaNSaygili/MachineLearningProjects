🚀 Electricity Demand Forecasting with XGBoost
Bu proje, geçmiş enerji tüketim verilerini kullanarak gelecekteki elektrik talebini tahmin etmek amacıyla geliştirilmiş bir zaman serisi tahminleme (Time-Series Forecasting) çalışmasıdır. Projede, verilerin temizlenmesi, zaman serisi özelliklerinin çıkarılması ve XGBoost regresyon modeli ile yüksek doğruluklu tahminlerin yapılması süreçleri işlenmiştir.

📊 Proje Özeti
Elektrik talebi tahmini, enerji şebekelerinin yönetimi ve maliyet optimizasyonu için kritiktir. Bu projede:

Veri Kaynağı: Saatlik bazda elektrik talebi, sıcaklık ve nem verilerini içeren zaman serisi veri seti.

Model: Gradient Boosting tabanlı güçlü bir algoritma olan XGBoost Regressor.

Hedef: Mevsimsellik ve trendleri yakalayarak düşük hata payı (RMSE/MAE) ile tahmin üretmek.

🛠️ Kullanılan Teknolojiler ve Kütüphaneler
Python 3.x

Pandas & NumPy: Veri işleme ve temizleme.

Matplotlib & Seaborn: Veri görselleştirme.

XGBoost: Makine öğrenmesi modeli.

Scikit-learn: Model değerlendirme metrikleri (RMSE, MAE).

Joblib: Eğitilmiş modelin kaydedilmesi ve yüklenmesi.

🚀 Proje Adımları
1. Veri Ön İşleme (Data Preprocessing)
Eksik veriler (NaN) zaman serisinin doğasına uygun yöntemlerle doldurulmuştur:

Zaman bileşenleri için ffill() (ileri yönlü doldurma).

Hava durumu verileri için bfill() (geri yönlü doldurma).

Talep verisi için interpolate(method='time') (zaman bazlı interpolasyon).

2. Özellik Mühendisliği (Feature Engineering)
Zaman damgalarından modelin öğrenebileceği sayısal özellikler türetilmiştir:

Saat (Hour)

Haftanın Günü (Day of Week)

Ay (Month)

Yıl (Year)

Yılın Günü (Day of Year)

3. Model Eğitimi
XGBoost modeli aşağıdaki parametrelerle yapılandırılmıştır:

n_estimators = 1000

learning_rate = 0.01

early_stopping_rounds = 50 (Aşırı öğrenmeyi önlemek için).

4. Sonuçlar ve Performans
Modelin test verisi üzerindeki başarısı şu metriklerle doğrulanmıştır:

XGBoost RMSE: 174.82

XGBoost MAE: 123.47

📂 Dosya Yapısı
notebook.ipynb: Tüm analiz ve modelleme kodlarını içeren Jupyter Notebook.

electricity_demand_xgb_model.pkl: Eğitilmiş ve kullanıma hazır XGBoost modeli.

README.md: Proje açıklaması.

💻 Nasıl Kullanılır?
Repoyu bilgisayarınıza indirin (clone).

Gerekli kütüphaneleri kurun: pip install xgboost pandas scikit-learn joblib matplotlib.

Modeli yükleyerek tahmin yapmaya başlayın:

Python

import joblib
model = joblib.load('electricity_demand_xgb_model.pkl')
# Yeni verilerinizle tahmin yapın
# predictions = model.predict(new_data)