# 🚀 Render.com Deployment Rehberi

Bu rehber, Astroloji ve Fal sitenizi Render.com'a nasıl deploy edeceğinizi adım adım anlatır.

## 📋 Ön Gereksinimler

- ✅ GitHub hesabı
- ✅ Groq API anahtarı ([console.groq.com](https://console.groq.com))
- ✅ Email servisi ayarları (Brevo, Gmail veya başka SMTP)

---

## 1️⃣ GitHub'a Kod Yükleme

### Eğer henüz GitHub repo'nuz yoksa:

```bash
# Proje klasörüne gidin
cd C:\Users\TR\.gemini\antigravity\scratch\astroloji-fal-sitesi

# Git başlat
git init

# Dosyaları ekle
git add .

# İlk commit
git commit -m "Initial commit: Astroloji ve Fal Sitesi"

# GitHub'da yeni repo oluşturun (https://github.com/new)
# Sonra aşağıdaki komutları çalıştırın (YOUR_USERNAME'i değiştirin):

git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/astroloji-fal-sitesi.git
git push -u origin main
```

---

## 2️⃣ Render.com'da Web Service Oluşturma

1. **Render.com'a gidin:** [https://render.com](https://render.com)

2. **Sign Up / Login:** GitHub hesabınızla giriş yapın

3. **New Web Service:**
   - Dashboard'da **"New +"** butonuna tıklayın
   - **"Web Service"** seçin

4. **Repository Bağlantısı:**
   - GitHub repo'nuzu seçin: `astroloji-fal-sitesi`
   - **"Connect"** butonuna tıklayın

---

## 3️⃣ Web Service Yapılandırması

### ⚙️ Temel Ayarlar

| Alan | Değer |
|------|-------|
| **Name** | `astroloji-fal-sitesi` (istediğiniz isim) |
| **Region** | Frankfurt veya en yakın |
| **Branch** | `main` |
| **Root Directory** | `.` (boş bırakın) |
| **Runtime** | `Node` |
| **Build Command** | `npm install` |
| **Start Command** | `npm start` |

### 💰 Plan Seçimi

- **Free** - Ücretsiz (15 dakika inaktivite sonrası sleep mode)
- **Starter ($7/ay)** - Her zaman aktif, daha hızlı

> **Not:** Free plan ile başlayıp ihtiyaç duyduğunuzda upgrade yapabilirsiniz.

---

## 4️⃣ Environment Variables (Çevre Değişkenleri)

**"Environment Variables"** bölümüne şu değerleri ekleyin:

### 🔑 Zorunlu Değişkenler

```
NODE_ENV=production
PORT=3000
```

```
GROQ_API_KEY=gsk_YOUR_GROQ_API_KEY_HERE
```
> Groq API anahtarınızı buraya yapıştırın: https://console.groq.com

```
JWT_SECRET=your-super-secret-jwt-key-change-this-in-production
```
> Güvenli, rastgele bir string oluşturun (min 32 karakter)

### 📧 Email Servisi (Brevo örneği)

```
SMTP_HOST=smtp-relay.brevo.com
SMTP_PORT=587
SMTP_USER=your-smtp-user@smtp-brevo.com
SMTP_PASS=your-smtp-password-here
EMAIL_FROM="Yıldız Fal <noreply@yourdomain.com>"
```

> **Alternatif Email Servisleri:**
> - **Gmail:** `smtp.gmail.com:587` (App Password gerekli)
> - **SendGrid:** `smtp.sendgrid.net:587`
> - **Mailgun:** `smtp.mailgun.org:587`

### 🌐 CORS (İsteğe Bağlı)

Eğer frontend'i farklı bir domain'de host edecekseniz:

```
ALLOWED_ORIGINS=https://yourdomain.com,https://www.yourdomain.com
```

---

## 5️⃣ Database Yapılandırması

Render.com SQLite'ı destekler ama **ephemeral** (geçici) dosya sistemi kullanır. İki seçenek:

### Seçenek A: SQLite (Ücretsiz, Basit)

✅ Küçük-orta trafik için yeterli
⚠️ Her deploy'da database sıfırlanabilir

**Çözüm:** Render Disks kullanın:
1. Dashboard'da **"Disks"** sekmesine gidin
2. **"Add Disk"** tıklayın
3. **Mount Path:** `/data`
4. **Size:** 1GB (free tier)

Sonra `.env`'e ekleyin:
```
DB_PATH=/data/astroloji-fal.db
```

### Seçenek B: PostgreSQL (Önerilen - Yüksek Trafik İçin)

1. Render'da **"New +"** > **"PostgreSQL"** seçin
2. Database oluşturun (Free tier mevcut)
3. Internal Database URL'i kopyalayın
4. `server/database/db.js` dosyasını PostgreSQL için güncelleyin

---

## 6️⃣ Deploy Başlatma

1. Tüm ayarları yaptıktan sonra **"Create Web Service"** butonuna tıklayın

2. Render otomatik olarak:
   - Kodu çeker
   - `npm install` çalıştırır
   - `npm start` ile başlatır

3. **Build logs** bölümünden ilerlemeyi izleyin

4. **✅ Deploy başarılı!** Yeşil "Live" işareti göreceksiniz

---

## 7️⃣ Sitenizi Test Edin

Render size bir URL verecek:
```
https://astroloji-fal-sitesi-XXXX.onrender.com
```

### Test Checklist:

- [ ] Ana sayfa açılıyor
- [ ] Kullanıcı kaydı çalışıyor
- [ ] Login çalışıyor
- [ ] Fal özellikleri (kahve, tarot, vb.) çalışıyor
- [ ] Admin paneline erişim var
- [ ] Email gönderimi çalışıyor

---

## 8️⃣ Custom Domain Bağlama (İsteğe Bağlı)

Kendi domain'iniz varsa (örn: `www.yildizfal.com`):

1. Render Dashboard'da **"Settings"** > **"Custom Domain"**
2. Domain'inizi ekleyin
3. DNS sağlayıcınızda (GoDaddy, Namecheap vb.) CNAME kaydı ekleyin:
   ```
   CNAME www -> astroloji-fal-sitesi-XXXX.onrender.com
   ```
4. SSL sertifikası otomatik oluşturulacak (Let's Encrypt)

---

## 🔧 Deployment Sonrası Bakım

### Otomatik Deployment

Her `git push` yaptığınızda Render otomatik deploy eder:

```bash
git add .
git commit -m "Yeni özellik eklendi"
git push
```

### Logları Görüntüleme

- Render Dashboard > **"Logs"** sekmesi
- Canlı hata ayıklama için kullanın

### Environment Variables Güncelleme

- Dashboard > **"Environment"** sekmesi
- Değişiklikten sonra **"Save Changes"** > Otomatik redeploy

---

## 🚨 Sorun Giderme

### Build Hatası

```
Error: Cannot find module 'xyz'
```
**Çözüm:** `package.json`'a eksik paketi ekleyin ve push edin

### Database Sıfırlanıyor

**Çözüm:** Render Disk kullanın veya PostgreSQL'e geçin

### Free Tier Sleep Mode

**Sorun:** 15 dakika inaktivite sonrası site uyuyor (ilk istek yavaş)

**Çözümler:**
1. Starter Plan'e ($7/ay) geçin
2. UptimeRobot gibi servisle 10 dakikada bir ping gönderin

### Rate Limit Hataları

Groq API limitleri:
- Free tier: Dakikada 30 istek
- Paid tier: Daha yüksek limitler

**Çözüm:** Upgrade yapın veya caching ekleyin

---

## 📊 Performans Optimizasyonu

### 1. CDN Kullanımı

Render otomatik CDN sağlar, statik dosyalar hızlı yüklenir.

### 2. Caching

Redis ekleyerek sık kullanılan fal sonuçlarını önbelleğe alın.

### 3. Database Indexing

Yüksek trafik için PostgreSQL + proper indexes kullanın.

---

## ✅ Tamamlandı!

Siteniz artık canlıda! 🎉

**Yardım için:**
- Render Docs: https://render.com/docs
- Render Community: https://community.render.com

**Başarılar! 🌟**
