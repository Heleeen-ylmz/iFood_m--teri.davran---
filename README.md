# 📊 Maven Analytics - iFood Müşteri Segmentasyonu ve Davranış Analizi

Bu proje, **Maven Analytics** platformunda yer alan iFood şirketine ait müşteri verileri kullanılarak, veri ön işleme, istatistiksel hipotez testleri ve makine öğrenmesi tabanlı müşteri segmentasyonu süreçlerini kapsayan uçtan uca (*End-to-End*) bir veri analitiği çalışmasıdır.

Şirket cirosunu optimize etmek ve pazarlama departmanına nokta atışı müşteri personaları sunmak amacıyla gerçekleştirilmiştir.

---

## 🚀 Proje Adımları ve Metodoloji

### 1. Veri Ön İşleme (Data Preprocessing) & SQL Aktarımı
* Ham veriler incelenerek eksik, hatalı ve uç değerler (outliers) temizlenmiştir.
* Doğum yılı ve müşteri gelirleri gibi kritik sütunlar analiz standartlarına uygun hale getirilmiştir.
* Temizlenen veriler ilişkisel veri tabanı yönetim mantığına uygun olarak `sqlite3` ile `ifood_analiz.db` veritabanına taşınmıştır.

### 2. Keşifçi Veri Analizi (EDA) & Hipotez Testleri
* Müşterilerin demografik özellikleri ile alışveriş alışkanlıkları arasındaki ilişkiler incelenmiştir.
* **Müşteri Şikayetleri (`Complain`)** ve **Evdeki Çocuk/Genç Durumu** arasındaki ilişkiler istatistiksel hipotez testleri (Korelasyon ve Parametrik/Non-Parametrik testler) kullanılarak doğrulanmıştır.

### 3. Makine Öğrenmesi ile Kümeleme (K-Means Clustering)
* Algoritmanın mesafe tabanlı kararlı çalışabilmesi için veriler `StandardScaler` ile ölçeklenmiştir.
* **Dirsek Metodu (Elbow Method)** kullanılarak veri seti için en ideal küme sayısı matematiksel olarak **$K=4$** olarak tespit edilmiştir.
* Model eğitildikten sonra her müşterinin yanına ait olduğu küme etiketleri (`Cluster`) eklenerek sonuçlar SQL veritabanına `segmented_marketing_data` adıyla kaydedilmiştir.

---

## 🎯 Müşteri Personaları (Kümelerin Analizi)

Yapılan modelleme sonucunda müşteri kitlemiz 4 ana karaktere ayrılmıştır:

| Küme (Cluster) | Persona Adı | Gelir Seviyesi | Öne Çıkan Davranış | Şikayet Oranı | Pazarlama Stratejisi |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Cluster 3** | **Seçkin Gurmeler (VIP)** | Zirve (~80k) | En yüksek Et harcaması, az web ziyareti | %0.53 | Premium üyelik, özel tadım davetleri |
| **Cluster 0** | **Sadık Şarap Severler** | Yüksek (~67k) | En yüksek Şarap harcaması, düzenli takip | %0.39 (En Mutlu) | Yıllanmış özel koleksiyonlar, sadakat ödülleri |
| **Cluster 1** | **Temkinli Orta Sınıf** | Orta (~46k) | Evde ergen/genç var, ölçülü tüketim | %1.54 (En Yüksek) | Kullanıcı dostu arayüz desteği, operasyonel iyileştirme |
| **Cluster 2** | **Dijital Fırsatçılar** | Düşük (~33k) | Evde küçük çocuk var, en sık web ziyareti | %0.98 | Ev ekonomisi aile paketleri, kombo indirim kuponları |

---

## 🛠️ Kullanılan Teknolojiler

* **Programlama Dili:** Python
* **Veri Yönetimi & SQL:** SQLite3, Pandas
* **Veri Görselleştirme:** Matplotlib, Seaborn
* **Makine Öğrenmesi:** Scikit-Learn (KMeans, StandardScaler)
* **İş Zekası (Gelecek Adım):** Power BI (Dashboard Tasarımı)

---

## 📂 Dosya Yapısı

* `keşif_analizi.ipynb` -> İlk veri inceleme ve temizlik adımları
* `hipotez_testleri.ipynb` -> İstatistiksel hipotez süreçleri
* `müşteri_segmentasyonu.ipynb` -> K-Means modelleme ve görselleştirme adımları
* `ifood_analiz.db` -> Projenin tüm verilerini tutan SQLite veritabanı dosyası
*
