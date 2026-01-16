# ⚡ Electricity Demand Forecasting with XGBoost

Bu proje, geçmiş enerji tüketim verilerini, sıcaklık ve nem gibi dış faktörlerle birleştirerek gelecekteki elektrik talebini tahmin etmek amacıyla geliştirilmiştir. Zaman serisi analizi ve güçlü bir makine öğrenmesi algoritması olan **XGBoost** kullanılarak yüksek doğruluklu sonuçlar elde edilmiştir.

## 🚀 Proje Genel Bakış
Elektrik dağıtım şirketleri ve enerji yöneticileri için talebi önceden bilmek, maliyet tasarrufu ve operasyonel verimlilik sağlar. Bu çalışma:
- Zaman serisi verilerindeki eksik değerleri akıllı yöntemlerle doldurur.
- Tarih verisinden mevsimsel özellikler (saat, gün, ay vb.) türetir.
- XGBoost Regressor kullanarak gelecekteki talebi tahmin eder.

## 🛠️ Teknik Araçlar
- **Dil:** Python
- **Kütüphaneler:** `pandas`, `numpy`, `xgboost`, `matplotlib`, `scikit-learn`, `joblib`
- **Algoritma:** XGBoost (Extreme Gradient Boosting)

## 📊 Veri Hazırlama ve Özellik Mühendisliği
Proje akışında aşağıdaki veri ön işleme adımları uygulanmıştır:
- **Eksik Veri Yönetimi:** `ffill`, `bfill` ve zaman bazlı `interpolate` yöntemleri kullanılarak veri bütünlüğü sağlandı.
- **Feature Engineering:** Modelin zamanı anlaması için `hour`, `dayofweek`, `month`, `year` ve `dayofyear` özellikleri oluşturuldu.

## 📈 Model Performansı
Modelin başarısını ölçmek için kullanılan hata metrikleri:
- **RMSE (Root Mean Squared Error):** 174.82
- **MAE (Mean Absolute Error):** 123.47



### Tahmin Grafiği
Modelin test verisi üzerindeki performansı (Gerçek vs Tahmin):



## 📂 Dosyalar
- `notebook.ipynb`: Tüm kodları ve veri analizini içeren çalışma dosyası.
- `electricity_demand_xgb_model.pkl`: Eğitilmiş, kullanıma hazır model dosyası.

   
