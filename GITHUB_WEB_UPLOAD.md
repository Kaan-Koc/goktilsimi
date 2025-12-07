# 🚀 GitHub'a Kod Yükleme - Web Yöntemi (Git Gerektirmez)

## ✅ Hazırlık: Ne Yapacağız?

GitHub hesabınızda yeni bir repository oluşturup kodları web arayüzünden yükleyeceğiz.

---

## 📋 Adım 1: GitHub'da Repo Oluştur

GitHub repo oluşturma sayfası tarayıcınızda açık. (Giriş yapmadıysanız önce giriş yapın)

### Formu Doldurun:

1. **Repository name:** `astroloji-fal-sitesi`

2. **Description (opsiyonel):** `AI destekli astroloji ve fal platformu - GökTılsımı`

3. **Public** seçili olmalı (✅)

4. **Add a README file** - TIKLAMAYIN (❌)

5. **Add .gitignore** - "Node" seçin

6. **Choose a license** - "ISC License" seçin (opsiyonel)

7. **Create repository** butonuna tıklayın

---

## 📤 Adım 2: Dosyaları Yükle

Repo oluştuktan sonra:

### 2.1. Uploading Files

Repository sayfasında **"uploading an existing file"** linkini göreceksiniz. Tıklayın.

### 2.2. Dosya Seç

**İki yöntem:**

**Yöntem A: Sürükle-Bırak (Kolay)**
1. Windows Explorer'da şu klasörü açın:
   ```
   C:\Users\TR\.gemini\antigravity\scratch\astroloji-fal-sitesi
   ```

2. **node_modules klasörü HARİÇ** tüm dosyaları seçin:
   - `Ctrl+A` (hepsini seç)
   - `Ctrl+Click` node_modules'e tıkla (çıkar)
   - `Ctrl+Click` database.db'ye tıkla (çıkar)

3. Seçili dosyaları GitHub sayfasına sürükle-bırak

**Yöntem B: Choose Files**
1. "choose your files" butonuna tıkla
2. Çoklu seçim yap (Ctrl tuşuyla)
3. Upload

### 2.3. Commit

Altta:
- **Commit message:** `Initial commit - Production ready`
- **Commit changes** butonuna tıkla

Yükleme 2-5 dakika sürebilir (internet hızınıza bağlı)

---

## ⚠️ Önemli: node_modules Yüklemeyin!

**node_modules** klasörünü YÜKLEMEYIN çünkü:
- 200MB+ boyutunda
- Render.com zaten `npm install` ile kendi kuracak
- GitHub limitleri aşabilir

**Yüklenecekler:**
- ✅ server/
- ✅ public/
- ✅ package.json
- ✅ package-lock.json
- ✅ .env.example
- ✅ .gitignore
- ✅ README.md
- ✅ Diğer tüm dosyalar

**Yüklenmeyecekler:**
- ❌ node_modules/
- ❌ database.db (production'da yeni oluşur)
- ❌ *.log dosyaları

---

## ✅ Adım 3: Kontrol

Yükleme tamamlandıktan sonra repo sayfasında şunları görmelisiniz:

```
astroloji-fal-sitesi/
├── DEPLOYMENT_RENDER.md
├── DEPLOYMENT_CLOUDFLARE.md
├── DOMAIN_GUIDE.md
├── README.md
├── package.json
├── server/
├── public/
└── ... diğer dosyalar
```

**Repository URL'iniz:**
```
https://github.com/YOUR_USERNAME/astroloji-fal-sitesi
```

Bu URL'i bir sonraki adımda Render.com'da kullanacağız!

---

## 🚀 Sonraki Adım: Render.com

Kodlar GitHub'a yüklendikten sonra banasınız**"tamam"** yazın, Render.com deployment'a geçelim!

---

## 💡 Alternatif: ZIP Yükleme

Eğer sürükle-bırak çalışmazsa:

1. Proje klasörünü ZIP'leyin (node_modules hariç)
2. GitHub'da "Add file" → "Upload files"
3. ZIP'i yükleyin
4. GitHub otomatik extract edecek

**Ben sizin için zaten bir ZIP hazırlıyorum...** ⏳
