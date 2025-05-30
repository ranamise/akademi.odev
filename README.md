﻿# akademi.odev


**Vectorize** (Vektörleştirme):
Metin verilerini sayısal forma çevirme işlemidir. Bu, makine öğrenmesi algoritmalarının metni işleyebilmesi için gereklidir.

**TF-IDF (Term Frequency – Inverse Document Frequency):**
Her kelimenin bir belge içindeki önemini belirlemek için kullanılır.

* **TF (Term Frequency):** Kelimenin belgede kaç kez geçtiği / Toplam kelime sayısı
  Örnek: "buy cheap cheap office software now"
  cheap = 2 kez geçti → TF(cheap) = 2 / 6 = 0.33
* **IDF (Inverse Document Frequency):**
  Çok sık geçen kelimeler (örneğin "the", "email") daha düşük skor alır.
  Nadir ama anlamlı kelimeler yüksek skor alır.

**TF × IDF = TF-IDF:**
Sık geçen ama genel olarak nadir olan kelimeler vurgulanır.

---

**TfidfVectorizer Ne Yapar?**

* Tüm veri setini tarar.
* Her metni TF-IDF skorlarından oluşan vektöre dönüştürür.
* Ortaya çıkan vektörler **seyrek matris** (sparse matrix) olarak saklanır.

---

**Avantajları**

| Özellik                       | Açıklama                                                  |
| ----------------------------- | --------------------------------------------------------- |
| Önemli kelimeleri öne çıkarır | Nadir ama anlamlı kelimelere yüksek skor verir            |
| Genel kelimeleri ezer         | "the", "email", "please" gibi kelimeler düşük skorludur   |
| Sayısal forma çevirir         | ML modelleri için zorunludur                              |
| Esnektir                      | ngram, max\_df, min\_df gibi ayarlarla özelleştirilebilir |

