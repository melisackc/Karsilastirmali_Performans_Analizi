# Karşılaştırmalı Performans Analizi: Sırt Çantası Problemi (Knapsack)

Bu proje, ünlü **Sırt Çantası Problemi (0/1 Knapsack Problem)** için iki farklı çözüm yönteminin performansını ve zaman karmaşıklığını (time complexity) karşılaştırmalı olarak analiz etmektedir.

## 📌 Proje Hakkında
Bu çalışmada, belirli bir kapasiteye (W) sahip bir sırt çantasına, farklı ağırlık (w) ve değerlere (v) sahip eşyaların, toplam değeri en üst düzeye çıkaracak şekilde nasıl yerleştirileceği problemi ele alınmaktadır.

Problemin çözümü için iki farklı algoritma uygulanmış ve çalışma süreleri büyüyen veri setleri üzerinde karşılaştırılmıştır:
1. **Dinamik Programlama (DP - Dynamic Programming):** Problemin optimum (kesin) çözümünü bulur. Alt problemlere bölerek ve sonuçları saklayarak (memoization/tabulation) ilerler. Ancak zaman karmaşıklığı $\mathcal{O}(N \times W)$ olduğundan, yüksek kapasite ve çok sayıda eşya durumunda çalışma süresi büyük ölçüde artar.
2. **Genetik Algoritma (GA - Genetic Algorithm):** Evrimsel ve sezgisel (heuristic) bir yaklaşımdır. Başlangıç popülasyonu oluşturulur; ardından elitizm, turnuva seçilimi (tournament selection), çaprazlama (crossover) ve mutasyon uygulanarak yeni nesiller elde edilir. Kesin bir optimum sonuç garanti etmese de çok büyük veri setlerinde Dinamik Programlamaya göre zaman açısından çok daha avantajlıdır.

## 🛠 Kullanılan Teknolojiler ve Araçlar
* **Python 3:** Algoritmaların geliştirilmesi
* **Jupyter Notebook:** Kodlama ve analiz ortamı
* **NumPy:** Optimizasyon ve matematiksel işlemler
* **Matplotlib:** Performans karşılaştırma grafiklerinin oluşturulması

## 📂 Veri Seti Yapısı
Analizde `ks_100_0` (N=100, W=100000), `ks_1000_0` (N=1000, W=100000) ve `ks_10000_0` (N=10000, W=1000000) gibi farklı büyüklükte örnek dosyalar işlenmektedir. 
* Dosyaların ilk satırı **N (eşya sayısı)** ve **W (çanta kapasitesi)** değerlerini içerir.
* Diğer satırlar sırasıyla her bir eşyanın **değerini (v)** ve **ağırlığını (w)** tutar.

## 🚀 Kurulum ve Çalıştırma
1. Proje dosyalarını bilgisayarınıza indirin.
2. Bilgisayarınızda Python yüklü olduğundan emin olun ve gerekli kütüphaneleri kurun:
   ```bash
   pip install numpy matplotlib
   ```
3. `Algoritma_Analizi_Kaynak_Kodlar.ipynb` dosyasını Jupyter ortamında veya Jupyter destekleyen bir IDE (örn. VS Code) ile açın.
4. Kod içerisinde veri setlerinin bulunduğu dosya yolunu (`ANA_DIZIN`) kendi sisteminize göre ayarlayın.
5. Hücreleri yukarıdan aşağıya çalıştırarak hesaplamaları yapın ve oluşturulan DP vs GA logaritmik karşılaştırma grafiğini görüntüleyin.

## 📊 Performans ve Sonuçlar
Algoritmaların çalışma süreleri logaritmik bir grafik üzerinde karşılaştırılır:
* **Dinamik Programlama**, küçük veri setlerinde kesin ve makul sürede sonuç verirken kapasite ($W$) çok büyük değerlere ulaştığında hem bellek (RAM) tüketimi hem de CPU süresi devasa oranda artmaktadır.
* **Genetik Algoritma**, belirli bir popülasyon (örn: 50) ve nesil sayısında (örn: 100) çalıştığı için süre açısından çok daha istikrarlıdır. Geniş arama uzaylarında kısa sürede kabul edilebilir çözümlere (yaklaşık sonuç) ulaşmak için çok daha iyi ölçeklenir.

## 👨‍💻 İletişim & Kaynak
* **GitHub Repository:** [melisackc/Karsilastirmali_Performans_Analizi](https://github.com/melisackc/Karsilastirmali_Performans_Analizi)