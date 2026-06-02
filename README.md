# Alzheimer-FTD-EEG-Classifier
Machine Learning project for differential diagnosis of AD and FTD using resting-state EEG data
# Alzheimer & FTD EEG Spektral Sınıflandırma Projesi

Bu proje, dinlenme hali (resting-state) skalp EEG kayıtlarını kullanarak Alzheimer Hastalığı (AD) ve Frontotemporal Demans (FTD) hastalıklarının erken evre diferansiyel tanısını gerçekleştirmek üzere tasarlanmış uçtan uca bir makine öğrenmesi pipeline hattıdır.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/dilarakarabulak-source/Alzheimer-FTD-EEG-Classifier/blob/main/eeg_dementia_classifier.ipynb)

## 🌟 Öne Çıkan Özellikler & Yenilikler
* **Çoklu Görünüm Özellik Füzyonu (Multi-View Fusion):** Ham sinyaller yerine Güç Spektral Yoğunluğu (PSD), Sürekli Dalgacık Dönüşümü (CWT) ve Empirik Mod Ayrışımı (EMD) özniteliklerinin hibrit kombinasyonu kullanılmıştır.
* **Hilesiz Doğrulama (LOSO CV):** Modeller, klinik yapay zekanın en katı protokolü olan *Leave-One-Subject-Out* (Her Seferinde Bir Hastayı Dışarıda Bırakma) yöntemiyle, hasta sızıntısı *(data leakage)* olmadan dürüstçe test edilmiştir.
* **Bulut Tabanlı & %100 Tekrarlanabilir (Reproducible):** 90.9 MB'lık dev öznitelik matrisi doğrudan entegre Google Drive hattından; klinik etiketler ise OpenNeuro (`ds004504`) sunucularından canlı olarak çekilir. Dış bağımlılık sıfırdır.

## 📌 Proje Yapısı
* `eeg_dementia_classifier.ipynb`: Veri çekme, EDA popülasyon grafikleri, Theta gücü analizi, LOSO döngüsü ve 4'lü şampiyon hata matrislerini üreten ana Jupyter Notebook dosyası.
* `requirements.txt`: Çalışma ortamının (VS Code / Colab) hatasız replike edilebilmesi için gerekli kütüphane ve versiyon dökümleri.

## 🚀 Kurulum ve Çalıştırma

### Yerel Ortam (VS Code / Local PC)
Projeyi yerel bilgisayarınızda çalıştırmak isterseniz, terminal üzerinden bağımlılıkları tek tıkla yükleyebilirsiniz:
```bash
pip install -r requirements.txt
