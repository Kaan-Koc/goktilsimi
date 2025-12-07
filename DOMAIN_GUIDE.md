# 🌐 Domain Satın Alma Rehberi

## 🎯 Domain Önerileri - GökTılsımı

Sitenizin adı **"GökTılsımı"** olduğu için şu domain isimlerini önerebilirim:

### ✨ Öncelikli Öneriler

1. **goktilsimi.com** ⭐ (En ideal)
   - Kısa, akılda kalıcı
   - Türkçe karakter yok (SEO+)
   
2. **yildizfal.com** ⭐
   - Sektörü anlatıyor
   - Kolay yazılır
   
3. **astrofal.com**
   - Uluslararası geçer
   - Astroloji vurgusu

4. **falim.com** / **falci.com**
   - Çok kısa
   - Marka değeri yüksek
   
5. **gokharita.com**
   - Alternatif
   - Yıldız haritası vurgusu

### 🔍 Domain Müsaitlik Kontrolü

Domain'lerin müsait olup olmadığını şu sitelerden kontrol edebilirsiniz:
- [Namecheap](https://www.namecheap.com)
- [GoDaddy](https://www.godaddy.com)
- [Porkbun](https://porkbun.com) (en ucuz)
- [Google Domains](https://domains.google) (artık Squarespace)

---

## 💰 Domain Fiyatları

### Türkiye'de Popüler Sağlayıcılar

| Sağlayıcı | .com Fiyatı (Yıllık) | Özellikler |
|-----------|---------------------|------------|
| **Porkbun** | ~$10 (₺300) | ✅ En ucuz, ücretsiz WHOIS gizleme |
| **Namecheap** | ~$13 (₺390) | ✅ Kolay kullanım, iyi destek |
| **GoDaddy** | ~$15 (₺450) | ✅ Türkçe arayüz, yaygın |
| **Cloudflare** | ~$10 (₺300) | ✅ Maliyet fiyatı (kârsız satar) |
| **Natro** | ~₺350 | ✅ Türk firma, TL ile ödeme |

### 💡 İpucu
İlk yıl genelde indirimli olur (örn. $8), yenilemede normal fiyat devreye girer.

---

## 📋 Domain Alma Adımları

### 1. Domain Seçimi
```
✅ Kısa olsun (max 15 karakter)
✅ Kolay yazılsın
✅ Türkçe karakter kullanmayın (SEO için)
✅ Marka kimliğini yansıtsın
✅ .com tercih edin (.net, .org 2. seçenek)
```

### 2. Satın Alma (Porkbun Örneği)

**Adım 1:** [porkbun.com](https://porkbun.com) adresine gidin

**Adım 2:** Domain arama kutusuna yazın (örn: `goktilsimi`)

**Adım 3:** Müsaitlik kontrolü:
- ✅ Yeşil = Müsait
- ❌ Kırmızı = Alınmış

**Adım 4:** Sepete ekle
- 1 yıl → $9.55
- 2 yıl → $19.10 (tavsiye: 2 yıl alın)
- WHOIS Privacy: Ücretsiz ✅

**Adım 5:** Ödeme
- Kredi kartı / PayPal
- Türk kartları çalışır

---

## 🔧 Domain'i Render.com'a Bağlama

Domain aldıktan sonra Render'a nasıl bağlayacağınız:

### Render.com Tarafında

1. **Dashboard → Your Web Service**
2. **Settings → Custom Domains**
3. **Add Custom Domain** butonuna tıklayın
4. Domain'inizi girin: `www.goktilsimi.com`
5. Render size DNS kayıtlarını verecek

### Domain Sağlayıcınızda (Porkbun Örneği)

1. **Domain Management → DNS**
2. Şu kayıtları ekleyin:

**A Record (Root domain için):**
```
Type: A
Host: @
Answer: [Render'ın verdiği IP]
TTL: 600
```

**CNAME Record (www için):**
```
Type: CNAME
Host: www
Answer: [your-app].onrender.com
TTL: 600
```

3. **Kaydet** ve bekleyin (5-30 dakika DNS yayılması)

### SSL Sertifikası
Render otomatik Let's Encrypt SSL kurar. 24 saat içinde HTTPS aktif olur.

---

## 🌟 Domain İsimlendirme İpuçları

### ✅ İyi Örnekler
- `kahvefali.com` - Net, açıklayıcı
- `yildizfalci.com` - Marka + servis
- `falistan.com` - Yaratıcı, akılda kalıcı

### ❌ Kaçınılacaklar
- `kahve-fali-tarot-burc.com` - Çok uzun
- `gök-tılsımı.com` - Tire kullanımı (SEO-)
- `goktilsimi123.com` - Sayılar (profesyonel değil)

---

## 🎯 SEO İçin Domain Stratejisi

### Ana Domain: `goktilsimi.com`
```
www.goktilsimi.com → Ana site
goktilsimi.com → Redirect to www
```

### Alt Domainler (İleride)
```
blog.goktilsimi.com → Blog
admin.goktilsimi.com → Admin panel
api.goktilsimi.com → API
```

---

## 💳 Ödeme ve Yenileme

### Auto-Renewal (Otomatik Yenileme)
✅ **Açık tutun!** Domain'in süresi dolmasın

### Hatırlatıcılar
- 90 gün önce: İlk hatırlatma
- 30 gün önce: Son hatırlatma
- Süre dolunca: 30 gün grace period (ek ücretle)

### Domain Kaybetmemek İçin
1. Otomatik yenilemeyi açın
2. Doğru email adresinizi kaydedin
3. Kredi kartı bilgilerini güncel tutun

---

## 🔒 WHOIS Privacy

**WHOIS:** Domain sahibinin bilgileri (ad, email, telefon)

**Privacy Protection:**
- ✅ Kişisel bilgilerinizi gizler
- ✅ Spam email/telefon engeller
- ✅ Porkbun'da **ücretsiz**
- ⚠️ GoDaddy'de ek ücret ($10/yıl)

**Mutlaka açın!**

---

## 📊 Domain vs Subdomain

### Seçenek 1: Kendi Domain
```
www.goktilsimi.com
```
**Avantajlar:**
- ✅ Profesyonel
- ✅ Marka kimliği
- ✅ SEO+ (güven)
- ✅ Email adresi: info@goktilsimi.com

**Maliyet:** ~$10/yıl

### Seçenek 2: Render Subdomain (Ücretsiz)
```
astroloji-fal.onrender.com
```
**Avantajlar:**
- ✅ Ücretsiz
- ✅ Hemen kullanıma hazır

**Dezavantajlar:**
- ❌ Marka değeri düşük
- ❌ Uzun URL
- ❌ SEO-

---

## 🎁 Domain Promosyonları

### İlk Alım İndirimleri

**Porkbun:**
- İlk .com: $9.32 (normal $11.83)
- Promo kodu: `WELCOME` (ekstra indirim)

**Namecheap:**
- İlk .com: $8.88 (yenileme $13.48)
- Promo kodu arayın: `NEWCOM599`

**GoDaddy:**
- İlk .com: $0.99 (promo dönemlerinde)
- ⚠️ Yenileme pahalı ($17.99)

### 💡 İpucu
GoDaddy'den ilk yıl ucuza alıp durumu sağlayıcıya transfer edebilirsiniz (Porkbun'a).

---

## 🚀 Hızlı Başlangıç Planı

### Domain Alım Süreci (15 Dakika)

1. **5 dk:** Domain ismi karar verin
2. **2 dk:** Müsaitlik kontrolü yapın
3. **5 dk:** Satın alın (Porkbun öneriyorum)
4. **3 dk:** WHOIS Privacy açın

### Render'a Bağlama (10 Dakika)

1. **2 dk:** Render'da custom domain ekleyin
2. **5 dk:** DNS kayıtlarını güncelleyin
3. **3 dk:** HTTPS kontrolü yapın

**Toplam süre:** 25 dakika
**Maliyet:** ~$10/yıl

---

## ❓ Sık Sorulan Sorular

### Domain almadan önce siteyi deploy edebilir miyim?
✅ Evet! Render subdomain ile başlayın: `astroloji-fal.onrender.com`

### Domain'i sonradan bağlayabilir miyim?
✅ Evet, istediğiniz zaman. DNS değişikliği yeterli.

### .com.tr daha mı iyi?
❌ Türkiye odaklıysanız iyi ama:
- Global erişim azalır
- E-devlet onayı gerekir (.tr için)
- .com daha evrensel

### Domain transferi zor mu?
❌ Kolay! Auth code alıp yeni sağlayıcıya veriyorsunuz. 5 gün sürer.

### Email hosting gerekli mi?
❌ Hayır, ama profesyonel görünmek için önerilir:
- **Google Workspace:** $6/ay (info@goktilsimi.com)
- **Zoho Mail:** Ücretsiz (5 email max)
- **Forwarder:** Porkbun ücretsiz email yönlendirme

---

## 🎬 Özetlersek

**Önerim:**

1. **Domain:** `goktilsimi.com` veya `yildizfal.com`
2. **Sağlayıcı:** Porkbun (ucuz, kaliteli)
3. **Süre:** 2 yıl alın (indirim)
4. **WHOIS Privacy:** Açık
5. **Deployment:** Önce Render subdomain, sonra custom domain bağlayın

**Maliy et:** ~$20 (2 yıllık)

Başka sorunuz varsa sorabilirsiniz! 🌟
