# Banking Fraud Detection & Robustness Testing (NLP)
Bu proje, bankacılık sektöründe müşteri iletişim kanalları üzerinden gerçekleştirilen dolandırıcılık (Fraud) girişimlerini tespit etmek 
ve bu tespitleri yapan modellerin AI Testing (Yapay Zeka Testi) metodolojileriyle dayanıklılığını ölçmek amacıyla geliştirilmiştir.

Proje; sadece bir sınıflandırma modeli değil, aynı zamanda modelin uç durumlarda (Edge Cases) ve yanıltıcı saldırılarda (Adversarial Attacks) 
nasıl performans gösterdiğini analiz eden kapsamlı bir test çalışmasıdır.

**Projenin Temel Amaçları**
1. [ ] Dolandırıcılık Tespiti: Müşteri mesajlarındaki sosyal mühendislik ve oltalama (phishing) girişimlerini NLP teknikleriyle saptamak.
2. [ ] Model Şeffaflığı (Explainable AI): Modelin hangi kelimelere neden önem verdiğini (Feature Importance) görselleştirerek "Kara Kutu" (Black Box) sorununu ortadan kaldırmak.
3. [ ] Robusness (Dayanıklılık) Analizi: Modelin karakter manipülasyonları ve bağlamsal hatalara karşı direncini test etmek.

**Mimarisi ve Veri Akışı**
Proje, klasik Makine Öğrenmesi (Machine Learning) yöntemlerini modern veri işleme teknikleriyle birleştirir:

1. Veri Hazırlama: Bankacılık senaryolarını içeren sentetik bir veri kümesinin oluşturulması.
2. Feature Engineering: Metinlerin TF-IDF Vectorization (N-gram=1,2) yöntemiyle sayısal vektörlere dönüştürülmesi.
3. Model Eğitimi: Çoklu karar ağacı yapısına sahip Random Forest Classifier algoritması ile dengeli (balanced) eğitim.
4. Değerlendirme: Karmaşıklık Matrisi (Confusion Matrix) ve temel metrikler (Accuracy, Recall, Precision, F1) üzerinden analiz.


**Profesyonel AI Testing: Edge Case Senaryoları**
* Adversarial Text Manipulation (Yanıltıcı Metin Manipülasyonu)
* Semantic Ambiguity (Anlamsal Belirsizlik & False Positive Kontrolü)
* Out-of-Distribution (Kapsam Dışı Veri / Anlamsız Girişler)
* Overfitting vs. Professional Language (Maskelenmiş Dolandırıcılık)

**Öne Çıkan Bulgular ve Görselleştirmeler**
1. Karar Mekanizması (Feature Importance)
Modelin dolandırıcılık tespiti yaparken "hemen", "şüpheli", "iade" ve "şifrenizi" gibi kelimelere en yüksek ağırlığı verdiği saptanmıştır. 
Bu durum, modelin dolandırıcılık dilindeki "aciliyet" ve "hassas veri talebi" örüntülerini öğrendiğini kanıtlar.

2. Performans Metrikleri
Modelimiz Recall: 1.00 değerine ulaşarak test verisindeki tüm dolandırıcılık vakalarını yakalamayı başarmıştır. 
Ancak Precision: 0.67 değeri, bazı masum müşteri taleplerinin "False Positive" olarak işaretlendiğini göstermektedir. 
Bu durum, bankacılık güvenliğinde "güvenli bölgede kalma" stratejisiyle uyumludur.

**Kurulum ve Kullanım**
Repo'yu Klonlayın:
git clone https://github.com/kullaniciadi/banking-fraud-ai-testing.git

**Gereksinimleri Yükleyin:**

pip install pandas scikit-learn matplotlib seaborn

**Notebook'u Çalıştırın:**
aiTestingDemo.ipynb dosyasını Jupyter Notebook veya VS Code üzerinden açarak tüm hücreleri sırayla çalıştırabilirsiniz.