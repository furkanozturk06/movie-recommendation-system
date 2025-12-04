# 🎬 Apriori Algorithm-Based Movie Recommendation System

![Language](https://img.shields.io/badge/language-Python-blue) ![Algorithm](https://img.shields.io/badge/algorithm-Apriori-orange) ![Dataset](https://img.shields.io/badge/dataset-MovieLens%2020M-lightgrey)

Bu proje, **MovieLens 20M** veri setini ve **Apriori Algoritmasını** kullanarak, kullanıcıların izleme alışkanlıklarını analiz eden ve bu analizler doğrultusunda kişiselleştirilmiş film önerileri sunan kapsamlı bir öneri sistemidir.

## 📝 Proje Özeti ve Amacı

Kullanıcıların geçmiş izleme davranışlarına dayanarak, film türleri arasındaki ilişkileri ve popüler filmlerin hangi kategorilerle ilişkilendirildiğini ortaya çıkarmayı hedefler. **Birliktelik Kuralları (Association Rules)** kullanılarak, "Bu filmi izleyenler, şu filmi de izledi" mantığıyla çalışan isabetli bir öneri motoru geliştirilmiştir.

**Temel Hedef:** Kullanıcı deneyimini iyileştiren, yüksek doğruluk oranına sahip ve çeşitlilik sunan bir öneri sistemi mimarisi oluşturmak.

## 📊 Veri Seti: MovieLens 20M

Projede GroupLens Research tarafından sağlanan **MovieLens 20M** veri seti kullanılmıştır.
* **İçerik:** Kullanıcı derecelendirmeleri, etiketler, zaman damgaları ve film meta verileri.
* **İşlem:** Veri temizleme aşamasında eksik veriler giderilmiş ve analiz için **Kullanıcı-Film Matrisi** oluşturulmuştur.

## ⚙️ Algoritma ve Yöntemler

Projenin merkezinde **Veri Madenciliği** alanında sıkça kullanılan **Apriori Algoritması** yer almaktadır.

### Kullanılan Teknikler
1.  **Apriori Algoritması:** Sık öğe kümelerini (frequent itemsets) belirlemek ve birliktelik kurallarını çıkarmak için kullanılmıştır.
    * *Minimum Destek (Support):* %40 olarak belirlenmiştir.
2.  **Üçgen Ağaç (Triangular Tree) Yapısı:** Algoritmanın performansını artırmak ve bellek yönetimini optimize etmek amacıyla özel veri yapıları kullanılmıştır.
3.  **Metrikler:** Destek (Support), Güven (Confidence) ve Kaldıraç (Lift) değerleri hesaplanarak ilişkilerin gücü ölçülmüştür.

## 🚀 Öneri Sistemi Modülleri

Sistem, kullanıcı arayüzü üzerinden 4 farklı türde öneri sunmaktadır:

| Öneri Türü | Açıklama |
| :--- | :--- |
| **1. Birliktelik Kuralları** | Kullanıcıların beğendiği filmler arasındaki ilişki analizine dayalı öneriler. |
| **2. Kişiselleştirilmiş** | Kullanıcının geçmiş izleme geçmişine özel sunulan öneriler. |
| **3. Tür Bazlı** | Kullanıcının seçtiği spesifik bir film türüne (Aksiyon, Dram vb.) göre öneriler. |
| **4. İsim Bazlı** | Belirli bir film adına göre benzer filmlerin önerilmesi. |

## 📈 Değerlendirme ve Sonuçlar

Sistemin performansı aşağıdaki kriterlere göre analiz edilmiştir:

* **Doğruluk:** Yüksek. Kullanıcıların önerilen filmleri beğenme oranı tatmin edici düzeydedir.
* **Çeşitlilik:** Önerilen filmlerin tür çeşitliliği başarılıdır.
* **Zaman Verimliliği:** Büyük veri setlerinde (Big Data) Apriori algoritmasının işlem maliyeti nedeniyle süre artışı gözlemlenmiştir.
* **Kapsam:** Bazı niş film türlerinde veri azlığı nedeniyle eksiklikler tespit edilmiştir.

> **Sonuç:** Apriori algoritması, ilişkileri kurmada yüksek doğruluk sağlasa da, veri seti büyüdükçe çalışma süresi artmaktadır. Gelecek geliştirmelerde hibrit algoritmalar düşünülebilir.

## 💻 Ekran Görüntüleri ve Kod Yapısı

*(ekran görüntülerini uygun zamanda ekleyeceğim)*

| Algoritma Çıktısı | Öneri Arayüzü |
| :---: | :---: |
| ![Code Snippet](https://via.placeholder.com/300x200?text=Apriori+Kod+Ornegi) | ![UI Example](https://via.placeholder.com/300x200?text=Oneri+Ekrani) |

## 🛠️ Kurulum

1.  Projeyi klonlayın:
    ```bash
    git clone [https://github.com/kullaniciadi/film-oneri-sistemi.git](https://github.com/kullaniciadi/film-oneri-sistemi.git)
    ```
2.  Gerekli kütüphaneleri yükleyin:
    ```bash
    pip install pandas numpy mlxtend
    ```
3.  Veri setini `data/` klasörüne indirin ve projeyi çalıştırın:
    ```bash
    python main.py
    ```

## 👨‍💻 Geliştirici

**Furkan Öztürk**
* Kocaeli Üniversitesi - Yazılım Mühendisliği
* İletişim: [furknozturk06@gmail.com](mailto:furknozturk06@gmail.com)

---
*Bu proje Kocaeli Üniversitesi Yazılım Mühendisliği bölümü kapsamında geliştirilmiştir.*
