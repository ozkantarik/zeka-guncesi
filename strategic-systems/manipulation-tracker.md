## MAES – Manipülasyon Algılama ve Eşlik Sistemi (Manipulation Accompaniment Engine System)

### 🎯 Amaç

Bu modül, Project Pattern kapsamında manipülatif piyasa davranışlarını **önceden tespit edip**, **kendimiz manipülasyon yapmadan**, bu manipülasyonlardan **kar sağlayan stratejik yapı** sunar.

> "Sisteme açıkça ne istediğini söylemeden,
> davranışları yönlendirerek insanların, botların veya piyasanın kendi iç mantığıyla
> istenen sonucu kendiliğinden üretmesini sağlamak."

Bu felsefe üzerine kurulu olan modül, yüksek frekanslı botlardan insan psikolojisine kadar geniş bir yelpazede manipülasyonun **dönüştürücü zekâsına eşlik etmeyi** hedefler.

---

### 🧠 MAES – 3 Katmanlı Zekâ Stratejisi

#### 1. Pattern Maskeleme Tespiti (Masked Pattern Watcher)

* Piyasadaki **görünürdeki sinyallerle**, **gerçek amaçların uyuşmadığı durumlar** aranır
* Kötü haber + dump görünümlü sell wall → arkada low volume accumulation
* İyi haber + pump görünümü → arkada sell-off

**Yöntem:**

* Gerçekleşen işlem hacmi ile orderbook hacmi karşılaştırılır
* Sürekli yenilenen ama gerçekleşmeyen emir davranışları tespit edilir
* Yön sinyali ile likidite dağılımı uyumsuzluğu çıkarılır

#### 2. Sentiment & Fiyat Diverjansı (Sentiment Pivot Engine)

* Sosyal medya, haber akışı ve Telegram üzerinden alınan veri ile
* Fiyat hareketi arasındaki korelasyon karşılaştırılır

**Yöntem:**

* Sentiment pozitif ama fiyat yükselmiyor → satış baskısı maskelemesi
* Sentiment negatif ama fiyat düşmüyor → dipten toplama ihtimali

#### 3. Aktör Profili Çıkarımı (Footprint Actor Profiling)

* Hareketin kimin tarafından yapıldığı analiz edilir
* Aynı anda birçok borsada eş zamanlı hamle var mı?
* Spike hareket retail mi? Whale mi? Algo botu mu?

**Yöntem:**

* Order matching pattern analizi
* Alım/satım tarafında hangi emir türü (limit/market) baskın?
* Pasif likidite toplayıcı mı, agresif hacim kırıcı mı?

---

### 🛠️ Uygulama Önerileri

* Spot piyasada: düşük hacimli altcoin'lerde yön değiştirme stratejileri
* Futures piyasada: funding rate, likidasyon baskısı gibi tetikleyici yapılarla birlikte çalıştırılır
* Sentiment analiz API'leriyle real-time veri alımı önerilir

---

### 📎 Vizyoner Fark

Bu modül, piyasanın ne dediğine değil:

> "**Piyasanın oyuncularının neyi söyleyip aslında ne yaptığına**" bakar.

Amaç:

* Ön sinyal değil → **niyet** yakalamak
* Fiyat tahmini değil → **algı okuması** yapmak
* Hareketin değil → **hareketi oluşturan zekânın** izini sürmek

---

### 🧬 Projeksiyon

Gelecekte bu yapı şu modüllerle entegre edilebilir:

* Trade Reason Visualizer
* Sentiment Synced Execution Engine
* Pattern Memory Oracle

---

### ✅ Statü

MAES v0.1 – tanımsal strateji olarak hazır. Gerçek zamanlı botlarla entegre edilmek üzere altyapı planlaması başlatılabilir.
