# UBI 522 - Makine Öğrenmesi Dönem Projesi

Bu proje, ds004504 EEG veri setini kullanarak katılımcıları dinlenme durumu (resting-state) beyin sinyallerine göre sınıflandırmayı amaçlamaktadır.

## 1. Problem Tanımı

Bu projenin amacı, gözleri kapalı dinlenme durumu (eyes-closed resting-state) EEG kayıtlarından faydalanarak bireyleri üç gruptan birine sınıflandırmaktır: Alzheimer Hastalığı (AD), Frontotemporal Demans (FTD) ve Sağlıklı Kontrol (HC). EEG sinyalleri, insan gözüyle ayırt edilmesi zor olan karmaşık ve gürültülü veriler içerir. Makine öğrenmesi, bu karmaşık sinyallerdeki gizli örüntüleri öğrenerek, bu gruplar arasında nesnel ve otomatik bir ayrım yapma potansiyeli sunmaktadır. Bu çalışma, nörodejeneratif hastalıkların teşhisine yardımcı olabilecek biyobelirteçlerin keşfedilmesine yönelik bir adım niteliğindedir.

## 2. Veri Seti

Projede kullanılan veri seti [OpenNeuro ds004504](https://openneuro.org/datasets/ds004504/versions/1.0.0)'tür. Veri seti, toplam 88 katılımcıdan alınan 'eyes-closed' resting-state EEG kayıtlarını içermektedir. Katılımcı dağılımı şu şekildedir:
- 36 Alzheimer Hastası (AD)
- 23 Frontotemporal Demans Hastası (FTD)
- 29 Sağlıklı Kontrol (CN/HC)

## 3. Kurulum

Projeyi çalıştırmak için gerekli bağımlılıkları yükleyin:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn mne tqdm
```

## 4. Kullanım

Veri hazırlama, model eğitimi ve değerlendirme adımlarını çalıştırmak için ana script'i çalıştırın:

```bash
python projeodevi.py
```

## 5. Yapı

- `projeodevi.py`: Ana script. Veri yükleme, EDA, özellik çıkarma ve modelleme adımlarını içerir.
- `ds004504-download/`: Ham verilerin bulunduğu klasör.
- `results/`: Model sonuçlarının ve görsellerin kaydedileceği klasör.