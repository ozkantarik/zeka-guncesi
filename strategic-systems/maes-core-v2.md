## MAES Core v1.0 – Manipülasyon Algılama ve Eşlik Sistemi

### 🎯 Temel Hedef

MAES (Manipulation Accompaniment Engine System), piyasada yapılan manipülasyonlara katılmadan, onları önceden algılayıp **onların stratejilerinden önce konum alarak** kâr etmeyi hedefler.

Amaç:

> "Piyasanın doğasına ‘doğru’ görünen ama aslında manipüle edilen şeyleri, bizim manipülasyon yapmadan fark edip onların oyunu üzerinden kazanç sağlamak."

---

### 🧠 MAES Yaklaşım Katmanları

#### 1. **Davranışsal İz Sürme (Cognitive Footprint)**

* Gerçek zamanlı emir defteri, hacim, emir türleri, işlem dağılımı analiz edilir
* Amaç: klasik teknik göstergeler yerine **davranış profilini** çözmek
* Hacim hareketlerinin ardındaki **niyet haritası** çıkarılır

#### 2. **Sentiment-Fiyat Çelişkisi Dedektörü**

* Haber başlıkları, sosyal medya akışı, tweet hacmi gibi göstergelerden sentiment skoru oluşturulur
* Fiyat hareketi ile bu sentiment karşılaştırılır
* ⇒ Pozitif sentiment + düşük momentum = manipülatif satış potansiyeli
* ⇒ Negatif sentiment + güçlü yataylık = toplama evresi sinyali

#### 3. **Senaryo Simülasyon Motoru**

* Küçük haberler + hacim düşüşü + spike artışı zinciri taranır
* Bu zincirli yapıların geçmiş başarı oranı analiz edilir
* ⇒ "Fiyat neden burada bu şekilde hareket ediyor olabilir?" sorusu üzerinden açıklayıcı modeller türetilir

#### 4. **Ajan Bazlı Profilleme (Actor Modeling)**

* Market maker, whale, retail, bot gibi aktör profilleri çıkarılır
* Belirli saatlerde, hacim bölgelerinde hangi tür aktörlerin aktif olduğuna dair sürekli izleme yapılır
* Hareketin kaynağı → niyetin profili → pozisyon fırsatı

---

### 🛠️ Uygulama Senaryosu (Basit Bot Örneği)

* Olumsuz haber yayılıyor
* Emir defterinde agresif satışlar var ama gerçek satış hacmi düşük
* Aynı anda küçük agresif alımlar görülüyor (ping volume)
* MAES:

  * ✅ Bu dump “gerçek değil”
  * ✅ Retail korkutuluyor
  * ✅ Whale/Smart Money toplama yapıyor olabilir
* → Az hacimli long pozisyon açılır
* Fiyat spike yaparsa pozisyon genişletilir, sonra satılır

---

### 🔄 Entegrasyon Önerileri

* **Real-time orderbook veri feed**
* **Sentiment API (X, Telegram, Reddit, haber)**
* **Footprint analiz sağlayıcıları (Heatmap, Cluster chart)**
* **Trade Reason Visualizer ile bağlantı**

---

### 💡 Felsefi Zemin

MAES, teknik analiz yapan bir bot değil, **piyasa psikolojisini okuyan bir stratejik akıl katmanı**dır.

> "Manipülatörü manipüle etmeden, manipülasyon niyetini okuyarak onun önüne geçmek."

---

### ✅ Statü

MAES Core v1.0 olarak dokümante edildi.
Test edilecek ilk strateji: Sentiment-Piyasa Davranışı Çelişki Modülü.
