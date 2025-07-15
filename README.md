# Statlog Image Segmentation Projesi

---

## 📄 Proje Özeti

Bu proje, Statlog (Image Segmentation) veri seti üzerinde hem gözetimli sınıflama hem de gözetimsiz kümeleme yöntemlerini kapsamlı bir şekilde inceleyen bir Jupyter Notebook içerir. Aşamalar:

1. **Kurulum & Veri Yükleme**: Gerekli kütüphanelerin kurulumu, veri setinin okunması ve ilk kontroller.
2. **Veri Analizi**

   * A1. Veri Seti Tanıtımı ve Temel İstatistikler
   * A2. Eksik Veri & Aykırı Değer Analizi
   * A3. Özellik Ayırt Ediciliği (Random Forest ile önem skoru)
3. **Sınıflama Modelleri**

   * B1. Kullanılan Algoritmalar (k-NN, SVM, Random Forest)
   * B2. Pipeline & GridSearchCV ile Hiperparametre Optimizasyonu
   * B3. Test Verisi Üzerinde Performans Değerlendirmesi
4. **Kümeleme Analizi**

   * C1. K-Means, Agglomerative, DBSCAN Yöntemleri
   * C2. Performans Ölçütleri (ARI, NMI)
   * C3. Yorumlar ve Sonuçlar
5. **Sonuç ve Öneriler**: Modellerin karşılaştırması, ileri adımlar.

---

## 📂 Dosya Yapısı

```
statlog-image-segmentation/
├── segment.dat                     # Ham veri dosyası
├── Statlog(ImageSegmentation).ipynb # Ana Jupyter Notebook
├── README.md                       # Proje açıklaması
```

---

## ⚙️ Kurulum ve Çalıştırma

1. **Depoyu klonlayın**

   ```bash
   git clone https://github.com/MusapYildiz/statlog-image-segmentation.git
   cd statlog-image-segmentation
   ```
2. **Sanal ortam oluşturun ve aktif edin**

   ```bash
   python3 -m venv venv
   source venv/bin/activate      # Windows: venv\Scripts\activate
   ```
3. **Bağımlılıkları yükleyin**

   ```bash
   pip install -r requirements.txt
   ```
4. **Notebook’u çalıştırın**

   ```bash
   jupyter notebook Statlog\(ImageSegmentation\).ipynb
   ```

> **Not:** Eğer `requirements.txt` dosyası yoksa aşağıdaki komutla paketleri yükleyebilirsiniz:
>
> ```bash
> pip install pandas numpy matplotlib seaborn scikit-learn scipy
> ```

---

## 🛠️ Kullanılan Teknolojiler & Kütüphaneler

* Python 3.x
* Pandas, NumPy: Veri işlemleri
* Matplotlib, Seaborn: Görselleştirme
* Scikit-Learn: Modelleme, GridSearchCV
* SciPy: İstatistiksel analiz (Z-score)
* Jupyter Notebook: Dokümantasyon ve interaktif analiz

---

## 📊 Notebook Bölümleri

### 0. Kurulum ve Veri Yükleme

* Kütüphane importları, sabitlerin tanımı.
* `segment.dat` dosyasının okunması ve sütun adlarının atanması.

### A. Veri Analizi

* **A1.** Veri setindeki örnek sayısı, özellik sayısı, sınıf dağılımı.
* **A2.** Eksik değer kontrolü; IQR ve Z-score yöntemleriyle aykırı değer tespiti.
* **A3.** Random Forest ile `feature_importances_` kullanarak ilk 10 özelliğin görselleştirilmesi.

### B. Sınıflama

* **B1.** k-NN, SVM, Random Forest algoritmalarının tanıtımı ve karakteristikleri.
* **B2.** Pipeline & `GridSearchCV` ile en iyi hiperparametrelerin seçimi ve 5-kat çapraz doğrulama sonuçları.
* **B3.** Test verisi üzerinde confusion matrix, classification report ve heatmap ile performans analizi.

### C. Kümeleme

* **C1.** K-Means, Agglomerative Clustering, DBSCAN yöntemlerinin uygulanması.
* **C2.** ARI ve NMI skorlarının hesaplanması ve DataFrame’de gösterilmesi.
* **C3.** Yorumlar: Algoritmaların avantajları ve sınırlılıkları.

### D. Sonuç ve Öneriler

* Sınıflama ve kümeleme sonuçlarının karşılaştırılması.
* İleri adımlar: PCA, aykırı değer temizleme, hiperparametre optimizasyonu.

---

## 🎯 Özet Sonuçlar

| Analiz Türü | En Başarılı Yöntem      | Metrik                 |
| ----------- | ----------------------- | ---------------------- |
| Sınıflama   | Random Forest           | Accuracy \~ %95+       |
| Kümeleme    | K-Means / Agglomerative | ARI ≈ 0.34, NMI ≈ 0.55 |

**Öneriler:** Boyutsal indirgeme (PCA), ileri hiperparametre ayarı ve aykırı değer temizliği ile performans artırılabilir.

---

## 📖 Lisans ve Katkıda Bulunma

* **Lisans:** MIT License
* **Katkıda Bulunma:** Fork & pull request gönderebilirsiniz.

---

*Not: Notebook orijinal kaynağı: [Google Colab](https://colab.research.google.com/drive/1nY367y7ONkEOYYlWnH8alhmaQYnQ9ajo)*
