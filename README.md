# veriisleme
 Veri Setinin Kullanım Amacı
Bu veri seti, modern savaş temalı bir birinci şahıs nişancı (FPS) oyununun tasarım sürecini analiz etmek, test etmek ve geliştirmek amacıyla hazırlanmıştır. Veri seti, oyun içi deneyimleri, oyuncu etkileşimlerini, görev akışlarını, kullanıcı arayüzlerini ve oyun tasarım öğelerini içeren detaylı betimlemelerden oluşur.

Kullanım Alanları:
 Oyun Tasarımı Analizi: FPS oyunlarında görev yapısı, seviye ilerlemesi ve oyuncu motivasyonları gibi konuların incelenmesi.

 Yapay Zekâ Eğitimi: Oyuncu davranışlarını taklit edebilecek yapay zekâ modellerinin eğitilmesi.

 Metin Madenciliği & NLP: Oyun senaryoları ve tasarım dökümanları üzerinden duygu analizi, tema sınıflandırması veya otomatik özetleme çalışmaları.

 Oyun Testi Otomasyonu: Tasarım dokümanları ile oyun test senaryoları arasında tutarlılık kontrolü yapılması.

 Eğitim Amaçlı: Oyun geliştirme üzerine çalışan öğrenciler ve araştırmacılar için örnek bir kaynak olarak kullanılması.

 --------------------
1. Gerekli Ortamı Kurun
Python 3.8+ sürümüne sahip olduğunuzdan emin olun. Ardından aşağıdaki komutla bağımlılıkları yükleyin:

pip install nltk

2. Veriyi Hazırlayın
Veri setini proje dizinine yerleştirin veya aşağıdaki komutla indirin (örnek):
python download_data.py
Veriyi ön işlemek için:
python preprocess.py --input data/raw --output data/processed

3. Modeli Eğitin
Aşağıdaki komutla modeli eğitmeye başlayabilirsiniz:
python train_model.py --data data/processed --epochs 20 --batch_size 32
Eğitim tamamlandığında model models/ klasörüne kaydedilecektir.

4. Modeli Test Edin
Eğitilmiş modeli test etmek için:
python evaluate.py --model models/best_model.pth --data data/test

6. (Opsiyonel) Modeli Kullanarak Tahmin Yapın
Yeni bir veriyle tahmin yapmak için:
python predict.py --input sample_input.json --model models/best_model.pth
---------------------------------------------------------------------------
Kullanılacak kütüphaneler

nltk
string
re
