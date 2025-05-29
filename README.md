# Göz Hastalıklarının Teşhisi için Görüntü İşleme ve Derin Öğrenme Projesi

Bu proje, fundus görüntülerinden **Glokom**, **Diyabetik Retinopati**, **Katarakt** ve **Normal** göz sınıflarının teşhisini yapabilen bir görüntü işleme ve yapay zeka sistemini içermektedir. Çalışma, segmentasyon, öznitelik mühendisliği, makine öğrenmesi ve derin öğrenme yaklaşımlarını bir araya getirmektedir.

## 📌 Proje Başlığı

**Segmentasyon, Öznitelik Mühendisliği ve Çoklu Hastalık Sınıflandırma ile Göz Hastalık Teşhisi**

## 🔬 Projenin Amacı

Fundus görüntüleri üzerinden:

- Görüntü işleme teknikleri ile damar yapıları, optik disk, mikroanevrizmalar ve eksüda gibi yapıları tespit etmek
- Öznitelikler çıkararak makine öğrenmesiyle sınıflandırma yapmak
- Derin öğrenme modelleri ile dört sınıflı hastalık teşhisi gerçekleştirmek
- Sonuçları kullanıcı dostu bir arayüz ile görselleştirmek

## 📁 Kullanılan Veri Setleri

- **Kaggle** üzerinden temin edilen fundus retina görüntüleri
- **IDRiD** veri seti (Indian Diabetic Retinopathy Image Dataset)

## ⚙️ Kullanılan Teknikler

### Görüntü İşleme

- Histogram eşitleme, CLAHE
- Kontrast iyileştirme
- Morfolojik işlemler
- Segmentasyon: Optik disk, damarlar, mikroanevrizmalar, eksüdalar

### Makine Öğrenmesi

- Öznitelik çıkarımı (alan, doluluk oranı, damar uzunluğu, kenar yoğunluğu, vs.)
- Sınıflandırma algoritmaları: Random Forest, SVM, Logistic Regression, KNN
- En yüksek başarı: **Random Forest** + GridSearchCV

### Derin Öğrenme

- Transfer öğrenme ile modeller: ResNet18, DenseNet121, MobileNetV2, EfficientNetB0/B3
- En başarılı model: **ResNet18**

### Özellik Seçimi ve Boyut İndirgeme

- PCA (Principal Component Analysis)
- Relief algoritması

## 🧪 Model Başarıları

| Model | Accuracy (Test) |
|-------|-----------------|
| ResNet18 | %93.02 |
| MobileNetV2 | %91.67 |
| EfficientNetB3 | %88.05 |
| DenseNet121 | %90.52 |

## 🖥️ Uygulama ve Arayüz

Projenin son aşamasında, Gradio kullanılarak bir **web arayüzü** geliştirilmiştir. Kullanıcılar:

- Fundus görüntüsü yükleyebilir
- Seçilen modellerin tahmin sonuçlarını görüntüleyebilir
- Tahminleri olasılık dağılımları ile görebilir

> **Not:** Bu arayüz demo amaçlıdır ve gerçek tıbbi tanı yerine geçmez.

## 🧠 Gereksinimler

- Python >= 3.8
- PyTorch
- OpenCV
- Scikit-learn
- Gradio
- NumPy, Matplotlib, Pandas, PIL

```bash
pip install -r requirements.txt
