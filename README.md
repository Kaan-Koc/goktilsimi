# Yıldız Fal - Astroloji ve Fal Platformu

## 📋 Proje Hakkında

Yıldız Fal, yapay zeka destekli profesyonel bir astroloji ve fal platformudur. Kullanıcılar burç yorumları, kahve falı, tarot, numeroloji ve daha fazlasına erişebilir.

## ✨ Özellikler

- 🌟 Günlük/Haftalık/Aylık Burç Yorumları
- ☕ Kahve Falı
- 🎴 Tarot Falı
- 🔢 Numeroloji
- 🌌 Yıldız Haritası
- 💕 Aşk Uyumu

## 🚀 Kurulum

### Gereksinimler

- Node.js 18+
- NPM veya Yarn

### Adımlar

1. **Bağımlılıkları yükleyin:**

```bash
npm install
```

2. **Çevre değişkenlerini ayarlayın:**

`.env.example` dosyasını `.env` olarak kopyalayın ve düzenleyin:

```bash
cp .env.example .env
```

`.env` dosyasında şunları ayarlayın:

- `GROQ_API_KEY`: Groq API anahtarınız (https://console.groq.com)
- `JWT_SECRET`: Güvenli bir JWT secret key
- `SMTP_HOST`, `SMTP_PORT`, `SMTP_USER`, `SMTP_PASS`: Email servisi ayarları
- `EMAIL_FROM`: Gönderen email adresi

3. **Sunucuyu başlatın:**

```bash
npm start
```

veya geliştirme modu için:

```bash
npm run dev
```

4. **Tarayıcınızda açın:**

```
http://localhost:3000
```

## 📁 Proje Yapısı

```
astroloji-fal-sitesi/
├── public/              # Frontend dosyaları
│   ├── css/            # Stil dosyaları
│   ├── js/             # JavaScript dosyaları
│   ├── features/       # Özellik sayfaları
│   └── *.html          # HTML sayfaları
├── server/             # Backend
│   ├── routes/         # API route'ları
│   ├── services/       # AI ve diğer servisler
│   ├── database/       # Database şeması
│   └── server.js       # Ana sunucu dosyası
└── package.json
```

## 🔑 İlk Kullanım

1. Siteye kayıt olun
2. İlk kayıt olan kullanıcı otomatik admin olur
3. Özellikleri keşfedin ve falınızı görün!

## 💰 Gelir Modeli

- Google AdSense entegrasyonu ile reklam geliri
- Ücretsiz kullanıcı hesapları
- AI destekli içerikler

## 🛡️ Güvenlik

- JWT tabanlı authentication
- Bcrypt ile şifre hash'leme
- SQL injection koruması
- CORS ayarları

## 📱 Responsive Tasarım

Tüm cihazlarda mükemmel görünüm:

- 📱 Mobil (iOS/Android)
- 📲 Tablet
- 💻 Masaüstü

## 🤖 AI Entegrasyonu

- Groq API (llama-3.3-70b-versatile ve llama-3.2-90b-vision-preview)
- 25+ farklı falcı karakteri
- Gerçekçi gecikme mekanizmaları (20-60 saniye)
- Kişiselleştirilmiş, bağlam-bilinçli yorumlar
- Vision AI ile kahve falı görsel analizi

## ⚠️ Önemli Notlar

- Bu site eğlence amaçlıdır
- Ciddi kararlar için profesyonel danışmanlık alınız
- AI yorumları gerçek falcı yorumları değildir

## 📄 Lisans

ISC

## 👨‍💻 Geliştirici

Yıldız Fal Ekibi
