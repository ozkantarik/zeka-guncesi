## MAES Core v1.0 – Manipülasyon Algılama ve Eşlik Sistemi

### 🎯 Vizyon

Project Pattern kapsamında geliştirilen MAES, piyasa manipülasyonlarını **biz manipülatör olmadan** algılayan, **manipüle edenlerin stratejilerine eşlik ederek kazanç sağlayan** bir yapay zekâ sistemidir.

> "Piyasanın doğasına doğru görünen ama aslında manipüle edilen şeyleri, biz manipülasyon yapmadan fark edip onların oyunu üzerinden kazanç sağlarız."

Bu sistemin hedefi, sadece fiyat sinyallerine değil, **niyete** ve **zekâ düzeyine** odaklanarak pozisyon almaktır.

---

### 🧠 MAES Zekâ Katmanları

#### 1. Cognitive Intent Tracker (Zihinsel İz Sürücü)

* **Amaç:** Piyasada gerçekleşen hacim, fiyat ve haber senkronizasyonlarından "neden" davranışı çıkarımı yapmak
* **Yöntem:**

  * Hızlı yön değişimi + sentiment değişimi + haber yoğunluğu = "algı yönetimi" şüphesi
  * İşlem hacmi ile oynanmayan ama yön sinyali veren formasyonlarda "düşük frekanslı yönlendirme" belirleme
  * Piyasanın beklediği davranışa değil, büyük aktörlerin çelişkili hareketlerine odaklanma

#### 2. Strategic Behavior Divergence Engine (Davranış-Yön Sapması Motoru)

* **Amaç:** Piyasa fiyat yönü ile aktörlerin davranışları arasında "anlam farkı" oluştuğu anı bulmak
* **Yöntem:**

  * Yüksek satış baskısı görünümünde, küçük hacimli ama sürekli alım = dipten toplama
  * Olumlu haberin fiyatlamaya yansımaması = haber boşaltımı/satış hazırlığı
  * Kısa vadeli long pozisyonlar + funding negatife dönerken yüksek alım = yön değiştirme manipülasyonu

#### 3. Narrative Fracture Detector (Anlatı-Kırılma Tetikçisi)

* **Amaç:** Sosyal medya, haber, forumlarda yayılan "kitle anlatısı" ile gerçek emir davranışı arasındaki kopuşu tespit etmek
* **Yöntem:**

  * Pozitif anlatı + düşen fiyat = yavaş yavaş boşaltım süreci
  * Negatif anlatı + stabil fiyat + agresif market buy = "planlı yön değiştirme"
  * "FOMO hikâyesi" ile "fear-induced entry" anlarını zamanlama

#### 4. Actor Pattern Profiler (Oyuncu Profilleyici)

* **Amaç:** Hangi tür oyuncuların sahnede olduğunu anlamak (whale, retail, HFT, manipülatör grup)
* **Yöntem:**

  * Market buy/sell dominansı
  * Takas yapan adreslerin önceki davranış geçmişi
  * Çoklu borsalardaki eş zamanlı davranış eşleşmesi

---

### ⚙️ Teknik Bileşenler

* **Real-time Orderbook Tracker:** Spread sıkışması + agresif emir takibi
* **Sentiment Aggregator:** Twitter, Telegram, Reddit, haber siteleri üzerinden kelime analizi (OpenAI embedding veya özel NLP)
* **Liquidity Heatmaps:** Fiyat hareketlerinin geçtiği bölgelerde anlık likidite yoğunluğu tespiti
* **Intent-Based Signal Mapper:** Tüm sinyallerin "neye yönlendirme yapmak istiyor" açısından etiketlenmesi

---

### 🧪 İlk MVP Senaryosu – MAES Scout Bot

#### Hedef:

* Düşük hacimli altcoinlerde yapılan manipülasyonları erken algılayıp pozisyon açmak

#### Davranış:

1. Negatif sentiment + stable fiyat + küçük agresif alım = satın alma tetikleyicisi
2. Pump öncesi ani funding rate değişimi + pozitif anlatı = pozisyon kapatma uyarısı
3. Market buy dominansı + sosyal medya FOMO = çıkış sinyali

---

### 🧭 Genişletilebilirlik

* MAES gelecekte şunlarla entegre edilebilir:

  * Pattern Memory Oracle (önceki benzer manipülasyon örnekleriyle eşleştirme)
  * Sentiment Synced Execution Engine (sinir ağı destekli karar motoru)
  * Trade Reason Visualizer (algoritmanın neden o işlemi yaptığını görsel açıklama)

---

### ✅ Statü

MAES Core v1.0 hazır.
Algoritmik modüllerle entegre edilerek gerçek zamanlı kullanım için
MVP geliştirme ve data pipeline kurulumu bir sonraki adımdır.
