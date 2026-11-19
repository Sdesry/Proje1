# BIL545 Proje 1 — Online Alışverişte Satın Alma Niyeti

> Veri Madenciliğinde İleri Konular · Üsküdar Üniversitesi · 2026–2027 Güz

Bu depo, **tek kişi tarafından** yürütülen Proje 1 (vize) çalışmasını içerir. Grup tipi **1 kişi** olduğundan temel kapsam (Bölüm 1, 2 ve 3) uygulanmıştır.

## Grup

| Üye | Öğrenci no |
|---|---|
| [ÖĞRENCİ ADI SOYADI — MEHMET TANKUT YOLSAL] | [ÖĞRENCİ NO — 264329014] |

- **Grup adı:** Bireysel çalışma
- **İletişim sorumlusu:** Öğrenci (iletişim bilgileri öğrenci tarafından eklenecek)

## Araştırma sorusu

Bir e-ticaret oturumunun kaydedilmiş davranışsal özellikleri, satın almayla sonuçlanan oturumları güvenilir biçimde ayırt etmede ne kadar etkilidir? **Oturum sonuna doğru oluşan PageValues ve benzeri özellikler, erken gerçek zamanlı tahminle aynı şey değildir.**

## Veri

| Alan | Bilgi |
|---|---|
| Veri kümesi | Online Shoppers Purchasing Intention Dataset |
| Kaynak | https://archive.ics.uci.edu/dataset/468/online+shoppers+purchasing+intention+dataset |
| Lisans | CC BY 4.0 |
| Boyut | 12.330 oturum; 17 girdi + Revenue hedefi |
| Hedef | Revenue: oturum satın almayla sonuçlandı mı? |
| Pozitif sınıf | 1.908 / 12.330 (%15,47) |
| Eksik veri | Orijinal veri içinde tespit edilmedi |
| Tekrarlı girdi | 125 aynı girdi satırı |

**Verinin indirilmesi:** Ham veri GitHub'a eklenmez. Notebook, `ucimlrepo` ile UCI ID **468** üzerinden yükler.

## Depo yapısı

```text
.
├── README.md
└── proje1/
    └── BIL545_Proje1_TekKisi.ipynb

# proje2/ öğretim üyesinin Proje 1 geri bildiriminden sonra oluşturulacaktır.
```

## Çalıştırma

1. [Proje 1 notebook'unu Colab'da açın](https://colab.research.google.com/drive/1DjIXIR5Aj2YvRaRqwghx6aBIVSZ9EyZZ). Teslimde GitHub'daki dosyanın aynı son sürüm olduğundan emin olun.
2. İnternet erişimi gereklidir; ilk hücrelerde UCI verisi indirilir. `ucimlrepo`, `mlxtend`, scikit-learn ve diğer bağımlılıklar notebook hücrelerinde belirtilmiştir.
3. **Çalışma Zamanı → Tümünü çalıştır** ile baştan sona doğrulayın. Kayıtlı çıktılar mevcut olsa da yeniden baştan sona çalıştırma ayrıca kontrol edilmelidir.
4. Weka bağımsız kontrolü için Python çıktılarını Weka sonuçlarıyla Bölüm 1.7 ve 3.4'te karşılaştırın. Weka işlemleri ayrı programda öğrenci tarafından yürütülmüştür.
5. Nihai `.ipynb` dosyasını hem GitHub'a hem **STIX** ödev alanına aynı sürümle yükleyin.

## Sonuç özeti — Proje 1

- **Baseline:** DummyClassifier doğruluk **0,8453 ± 0,0002** görünmesine rağmen balanced accuracy **0,5000**, F1 **0,0000**; sınıf dengesizliği nedeniyle tek başına accuracy yanıltıcıdır.
- **Model karşılaştırması (5 kat × 2 tekrar, grup-korumalı):** Gradient Boosting average precision (AP) **0,7571 ± 0,0161**; Random Forest **0,7339 ± 0,0206**. Random Forest F1 ve balanced accuracy'de daha güçlüdür. GB ana ölçüt AP'ye göre Proje 2'ye geçici model olarak aktarılmıştır.
- **Sızıntı deneyi:** Doğru pipeline balanced accuracy **0,8180 ± 0,0121**, AP **0,6532 ± 0,0259**; bilerek yanlış küresel seçimin AP'si **0,6534 ± 0,0260**. Skorların benzer olması sızıntılı kurulumu geçerli kılmaz.
- **İstatistiksel karşılaştırma:** 5×2 CV t(5)=**1,4244**, nominal p=**0,213645**; GB'nin RF'ye istatistiksel üstünlüğü gösterilemedi. Aynı veriyle yapılan ön seçim nedeniyle test keşifseldir.
- **Veri küpü:** Kasım ayında satın alma oranı **%25,35**; hafta sonu **%17,40**, hafta içi **%14,89**. Karşılaştırılabilir tüm alt gruplarda tutarlı Simpson tersine dönüşü bulunmadı.
- **Birliktelik:** Apriori ve FP-Growth aynı sık kümeleri üretti: min_support %3 / %5 / %10 için **1305 / 909 / 417** (maksimum 3 öğe). Weka Apriori'nin ilk üç düzey toplamları da aynı çıktı. Weka'nın kural sıralaması/budaması doğrudan eşdeğer değildir.
- **Null-invariance:** 200 ilgisiz yapay oturum sonrası lift **4,79116 → 4,86887** değişirken Kulczynski **0,50068** sabit kaldı.

Bu değerler kayıtlı Colab çıktılarından alınmıştır; **bağımsız, kilitli test kümesi başarımı iddia edilmez**. Gerçek kullanıcı kimlikleri bulunmadığından yalnızca tam aynı girdiler gruplanabilmiştir.

## Proje 2

Proje 2, Proje 1 geri bildirimi alındıktan sonra başlayacaktır. Proje 2'ye aktarım için Colab'da oluşturulan `p1_proje2_aktarim.zip` paketi; temiz veri, model hattı, deney protokolü ve SHA-256 bütünlük manifesti içerir. **Paketin Drive/GitHub'da ayrıca saklandığı henüz doğrulanmış değildir.**

## Katkı beyanı

| Üye | Çalıştığı alt başlıklar ve işler | Sunumda anlattığı alt başlık |
|---|---|---|
| Tek kişi — [ad soyad eklenecek] | Proje 1 Bölüm 1–3: Colab/Weka deneylerini çalıştırma ve çıktıları inceleme; yapay zekâ yardımıyla kod, analiz ve metinlerin hazırlanması | [Sunumda gerçekten anlatılan başlıklar sonradan eklenecek] |

## Yapay zekâ beyanı

**ChatGPT (OpenAI)**; yönerge analizi, deney ve notebook kodlarının önemli kısmının yazılması, akademik yorum taslakları, model ve istatistiksel yöntemlerin açıklanması, Drive/GitHub sürüm işlemleri, README taslağı ve Weka karşılaştırmalarında kullanılmıştır. **Öğrenci**, Colab hücrelerini çalıştırmış, gerçek çıktılarını incelemiş ve Weka ZeroR/J48/Apriori deneylerini bağımsız olarak uygulamıştır. Bu katkı beyanı akademik dürüstlük ve commit geçmişiyle tutarlılık amacı taşır.

## Kaynaklar

- Sakar & Kastro (2018). *Online Shoppers Purchasing Intention Dataset*, UCI. https://doi.org/10.24432/C5F88Q
- Kaufman ve diğerleri (2012). *Leakage in data mining: Formulation, detection, and avoidance*.
- Dietterich (1998). *Approximate statistical tests for comparing supervised classification learning algorithms*.
- Wu, Chen & Han (2010). *Re-examination of interestingness measures in pattern mining: A unified framework*.
- Weka Apriori resmi dokümantasyonu: https://weka.sourceforge.io/doc.stable-3-8/weka/associations/Apriori.html
- mlxtend Apriori: https://rasbt.github.io/mlxtend/user_guide/frequent_patterns/apriori/
