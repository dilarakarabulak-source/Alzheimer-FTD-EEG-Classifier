# UBI 522 - Makine Öğrenmesi Dönem Projesi

## Alzheimer ve FTD EEG Spektral Sınıflandırma Sistemi

Bu proje, `ds004504` EEG veri setini kullanarak katılımcıları dinlenme durumu (resting-state) beyin sinyallerine göre diferansiyel tanıyla sınıflandırmayı amaçlayan uçtan uca bir makine öğrenmesi pipeline hattıdır.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/dilarakarabulak-source/Alzheimer-FTD-EEG-Classifier/blob/main/eeg_dementia_classifier.ipynb)

---

## 1. Problem Tanımı
Bu projenin amacı, gözleri kapalı dinlenme durumu (eyes-closed resting-state) EEG kayıtlarından faydalanarak bireyleri üç gruptan birine sınıflandırmaktır: Alzheimer Hastalığı (AD), Frontotemporal Demans (FTD) ve Sağlıklı Kontrol (CN/HC). 

EEG sinyalleri, insan gözüyle ayırt edilmesi zor olan karmaşık ve gürültülü veriler içerir. Geliştirilen bu biyomedikal yapay zeka sistemi; ham sinyallerin Güç Spektral Yoğunluğu (PSD), Sürekli Dalgacık Dönüşümü (CWT) ve Empirik Mod Ayrışımı (EMD) özniteliklerini birleştiren özgün bir **Çoklu Görünüm Özellik Füzyonu (Multi-View Feature Fusion)** hattı sunar. Bu çalışma, nörodejenere hastalıkların erken teşhisine yardımcı olabilecek dijital biyobelirteçlerin keşfedilmesine yönelik objektif ve otomatik bir adım niteliğindedir.

## 2. Veri Seti
Projede kullanılan veri seti OpenNeuro `ds004504`'tür. Veri seti, toplam 88 katılımcıdan alınan 'eyes-closed' resting-state EEG kayıtlarını içermektedir. Katılımcı popülasyon dağılımı şu şekildedir:

* **36** Alzheimer Hastası (AD)
* **23** Frontotemporal Demans Hastası (FTD)
* **29** Sağlıklı Kontrol (CN/HC)

## 3. Kurulum
Projeyi yerel bilgisayarınızda (VS Code vb.) veya bulutta sorunsuz replike edebilmek için gerekli tüm bağımlılıkları tek seferde yükleyin:

```bash
pip install -r requirements.txt
