# Yapay Sinir Ağı (ANN) ile Maaş Tahmini

Bu proje, bir veri setindeki iş ilanlarının maaşlarını tahmin etmek amacıyla bir Yapay Sinir Ağı (ANN) modeli kullanır. Model, çeşitli iş bilgilerini ve özelliklerini kullanarak maaş tahminleri yapar.

## Proje İçeriği
- Veri Seti: İş ilanlarına dair özellikler ve maaş bilgilerini içeren bir CSV dosyası.
- Model: Yapay Sinir Ağı (ANN) kullanılarak oluşturulmuş bir regresyon modeli.
- Kütüphaneler: pandas, numpy, scikit-learn, TensorFlow ve matplotlib
## Veri Seti
Veri seti Data-Science-Job_Listing.csv adında bir CSV dosyasıdır ve aşağıdaki sütunları içerir:

- Position: İş pozisyonu
- Job Title: İş unvanı
- Company Name: Şirket adı
- Location: Lokasyon
- Salary: Maaş (temizlenmiş ve sayısal değerlere dönüştürülmüş)
- Date: İş ilanı tarihi
- Logo: Şirket logosu
- Job Link: İş ilanı bağlantısı
- Company Rating: Şirket puanı
## Verilerin İşlenmesi
Maaş Verilerinin Temizlenmesi:

Maaş bilgileri, sayısal olmayan karakterler temizlenerek ve aralıklar ortalamaya dönüştürülerek işlenmiştir.
Eksik değerler ortalama ile doldurulmuştur.
## Kategorik Değişkenlerin Kodlanması:

- Kategorik değişkenler (örn. pozisyon, iş unvanı) one-hot encoding yöntemi ile kodlanmıştır.
Veri Normalizasyonu:

- Sayısal özellikler StandardScaler ile normalize edilmiştir.
## Eğitim ve Test Verilerine Ayırma:

Veriler, eğitim (%80) ve test (%20) setlerine ayrılmıştır.
## Model
Model Yapısı:
- Giriş Katmanı: 128 nöron, ReLU aktivasyon fonksiyonu
- Gizli Katman: 64 nöron, ReLU aktivasyon fonksiyonu
- Gizli Katman: 32 nöron, ReLU aktivasyon fonksiyonu
- Çıkış Katmanı: 1 nöron, lineer aktivasyon fonksiyonu
## Model Derleme
- Optimizer: Adam (öğrenme oranı: 0.001)
- Kayıp Fonksiyonu: Mean Squared Error
- Performans Ölçütü: Mean Absolute Error
## Eğitim
- Epochs: 100
- Batch Size: 32
- Validation Split: %20
## Sonuçlar
Modelin performansı test seti üzerinde değerlendirildi ve Ortalama Mutlak Hata (MAE) hesaplandı.

## Görselleştirmeler
- Eğitim ve Doğrulama Kaybı: Eğitim sürecinde modelin kaybının değişimi çizilmiştir.
- Gerçek vs Tahmin Edilen Maaşlar: Gerçek ve tahmin edilen maaşların karşılaştırılması yapılmıştır.
- Rastgele Örnek Tahmini: Rastgele seçilen bir örnek için gerçek ve tahmin edilen maaşlar yan yana gösterilmiştir.
## Gereksinimler
Bu projeyi çalıştırmak için aşağıdaki kütüphanelerin yüklü olması gerekmektedir:

- pandas
- numpy
- scikit-learn
- tensorflow
- matplotlib
## Gerekli kütüphaneleri yüklemek için:


pip install pandas numpy scikit-learn tensorflow matplotlib
## Kullanım
Veri setinizi uygun bir dizine yerleştirin ve df değişkenine dosya yolunu atayın.
Kodu çalıştırarak veri işleme ve model eğitim işlemlerini gerçekleştirin.
Eğitim ve doğrulama süreçlerinin görselleştirmelerine ve sonuçlarına erişebilirsiniz.
## Katkıda Bulunanlar
[İbrahim Püsküllü] - Proje Yapan 
Lisans
Bu proje MIT Lisansı altında lisanslanmıştır.
