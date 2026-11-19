# BIL545 Proje 1 — Online Alışverişte Satın Alma Niyeti

> BIL545 · Veri Madenciliğinde İleri Konular · 2026–2027 Güz · Üsküdar Üniversitesi

Bu depo dersin **Proje 1 (vize)** çalışmasını içerir. Çalışma tek kişi tarafından yürütülmektedir. **Ek paket 1 ve Ek paket 2 zorunlu değildir.**

## Grup

| Üye | Öğrenci no |
|---|---|
| [Ad Soyad — doldurulacak] | [Öğrenci no — doldurulacak] |

- **Grup adı:** Bireysel çalışma
- **İletişim sorumlusu:** Öğrenci
- **Grup tipi:** 1 kişi (temel kapsam: Bölüm 1–3)

## Soru

Bir e-ticaret oturumunun kaydedilmiş davranışsal özellikleri, satın almayla sonuçlanan oturumları güvenilir biçimde ayırt etmede ne kadar etkilidir?

Bu sorunun olası kullanım alanı, e-ticaret ziyaretçi oturumlarının satın alma sonucuyla ilişkili özelliklerini incelemektir. **Tamamen oturum bitmeden yapılacak gerçek zamanlı tahmin ayrı bir problem olup, özelliklerin hangi anda bilindiği ayrıca değerlendirilmelidir.**

## Veri

| Alan | Bilgi |
|---|---|
| **Veri kümesi** | Online Shoppers Purchasing Intention Dataset |
| **Kaynak** | [UCI Machine Learning Repository — Dataset 468](https://archive.ics.uci.edu/dataset/468/online+shoppers+purchasing+intention+dataset) |
| **Lisans** | CC BY 4.0 |
| **Boyut** | 12.330 oturum × 17 girdi özelliği (ek olarak 1 hedef sütun) |
| **Hedef değişken** | `Revenue`: oturum satın almayla sonuçlandı mı? |
| **Atıf** | Sakar, C. & Kastro, Y. (2018). Online Shoppers Purchasing Intention Dataset. UCI. https://doi.org/10.24432/C5F88Q |

**Verinin indirilmesi:** Veri dosyası GitHub deposuna konulmaz. Proje 1 notebook'undaki veri yükleme hücresi `ucimlrepo` üzerinden UCI veri kümesini **id=468** kullanarak indirir.

## Depo yapısı

```text
.
├── README.md
└── proje1/
    └── BIL545_Proje1_TekKisi.ipynb

# proje2/ ileride Proje 2 başladığında eklenecektir.
```

## Çalıştırma

1. [Proje 1 notebook'unu Google Colab'da açın](https://colab.research.google.com/github/Sdesry/Proje1/blob/main/proje1/BIL545_Proje1_TekKisi.ipynb).
2. Colab'da **Dosya → Drive'a kopya kaydet** ile çalışma kopyasını oluşturun.
3. İnternet bağlantısıyla **Çalışma Zamanı → Tümünü çalıştır** seçin. İlk çalıştırma UCI veri kümesini indirir.
4. Notebook'ta `[DOLDURULACAK]` ve `Yorum` alanlarını gerçek deney sonuçlarıyla tamamlayın.
5. Teslim öncesi notebook'un baştan sona hatasız çalıştığını doğrulayın, GitHub ve STIX'teki son `.ipynb` dosyalarının birebir aynı olmasını sağlayın.

**Önemli:** Notebook henüz hazırlık aşamasındadır, tamamlanmış proje değildir. Weka'da ZeroR, J48 ve Apriori kontrolleri de yapılacaktır.

## Sonuç özeti

### Proje 1 (vize)

- **Baseline:** Henüz çalıştırılmadı.
- **En iyi model:** Henüz belirlenmedi.
- **Sızıntı deneyi:** Henüz çalıştırılmadı.
- **Önemli bulgular:** Deneyler tamamlandıktan sonra yazılacak.

### Proje 2 (final)

Proje 1 sonuçları ve öğretim üyesi geri bildirimiyle daha sonra hazırlanacak.

## Katkı beyanı

| Üye | Çalıştığı alt başlıklar ve işler | Sunumda anlattığı alt başlık |
|---|---|---|
| [Ad Soyad — doldurulacak] | Proje 1 Bölüm 1–3: bireysel çalışma; ayrıntılar deneylerin sonunda doldurulacak | Henüz belirlenmedi |

## Yapay zekâ beyanı

ChatGPT; proje planlama, yönerge ve notebook şablonunu yorumlama, başlangıç README ve Colab hazırlığı için kullanılmıştır. Sonraki kod, analiz ve raporlama katkıları çalışma sırasında bu bölümde güncellenecektir. Deneyler Colab'da öğrenci tarafından çalıştırılır, sonuçları doğrulanır.

## Kaynaklar

- [UCI Online Shoppers Purchasing Intention Dataset](https://archive.ics.uci.edu/dataset/468/online+shoppers+purchasing+intention+dataset)
- [Veri kümesi DOI](https://doi.org/10.24432/C5F88Q)
- Kaufman, S. vd. (2012), *Leakage in data mining: Formulation, detection, and avoidance*.
- Dietterich, T. G. (1998), *Approximate statistical tests for comparing supervised classification learning algorithms*.
- Wu, T., Chen, Y. ve Han, J. (2010), *Re-examination of interestingness measures in pattern mining*.
