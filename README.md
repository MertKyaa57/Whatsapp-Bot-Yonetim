# WhatsApp Bot Yönetim Paneli

Modern, responsive ve kullanıcı dostu WhatsApp Bot yönetim paneli. Tailwind CSS ve DaisyUI ile tasarlanmış, Node.js backend ile çalışan kapsamlı bir yönetim sistemi.

## 🚀 Özellikler

### 📊 Dashboard (Genel Bakış)
- Anlık aktif kullanıcı sayısı
- Günlük/haftalık/güncel mesaj istatistikleri
- Son 10 kullanıcı mesajı
- Bot durumu (online/offline)
- Gerçek zamanlı güncelleme

### 👥 Kullanıcı Yönetimi
- WhatsApp numarası listesi
- Son mesaj zamanı takibi
- Kullanıcı durumu (aktif/engelli)
- Manuel mesaj gönderme
- Kullanıcı engelleme/engel kaldırma
- Arama ve filtreleme

### ⚡ Komut Yönetimi
- Mevcut komut listesi
- Yeni komut oluşturma
- Komut düzenleme/silme
- Tetikleyici kelimeler
- Komut açıklamaları
- Aktif/pasif durumu

### 🤖 Otomasyon / Yanıtlar
- Anahtar kelime tabanlı yanıtlar
- Otomatik karşılama mesajları
- Zamanlanmış mesajlar
- Tab yapısında düzenli arayüz

### 📝 Log Yönetimi
- Gelen ve giden mesajlar
- Hata ve uyarı logları
- Tarih aralığı filtreleme
- Log tipi filtreleme
- Arama fonksiyonu
- CSV formatında dışa aktarım
- Log temizleme

### ⚙️ Ayarlar
- WhatsApp oturum yönetimi
- QR kod ile bağlantı
- Bot ismi ve durum mesajı
- Otomatik yanıt ayarları
- Çevrim dışı mesajı
- Yedekleme ve geri yükleme
- Veri dışa aktarımı

### 🔔 Bildirim Sistemi
- Masaüstü bildirimleri
- Uygulama içi bildirimler
- Bildirim türü ayarları
- Ses seviyesi kontrolü
- Bildirim süresi ayarları
- Test bildirimi gönderme

## 🛠️ Teknolojiler

### Frontend
- **HTML5** - Semantik yapı
- **Tailwind CSS** - Utility-first CSS framework
- **DaisyUI** - Tailwind CSS component library
- **Alpine.js** - Minimal JavaScript framework
- **Vanilla JavaScript** - Modern ES6+ syntax

### Backend
- **Node.js** - JavaScript runtime
- **Express.js** - Web framework
- **whatsapp-web.js** - WhatsApp Web API
- **qrcode-terminal** - QR kod terminal çıktısı
- **CORS** - Cross-origin resource sharing

## 📦 Kurulum

### Gereksinimler
- Node.js (v14 veya üzeri)
- npm veya yarn
- Modern web tarayıcısı

### Adım 1: Projeyi İndirin
```bash
git clone <repository-url>
cd whatsapp-bot-panel
```

### Adım 2: Backend Bağımlılıklarını Yükleyin
```bash
cd backend
npm install
```

### Adım 3: Backend'i Başlatın
```bash
npm start
# veya
node bot.js
```

### Adım 4: Frontend'i Açın
Tarayıcınızda `frontend/index.html` dosyasını açın veya bir local server kullanın:

```bash
# Python ile
python -m http.server 8000

# Node.js ile
npx serve frontend
```

## 🔧 Kullanım

### İlk Kurulum
1. Backend'i başlatın
2. Terminal'de QR kod görünecek
3. WhatsApp uygulamanızdan QR kodu tarayın
4. Yönetim panelini açın (`frontend/index.html`)
5. Dashboard'da bot durumunu kontrol edin

### Temel Kullanım
1. **Dashboard**: Genel istatistikleri görüntüleyin
2. **Kullanıcılar**: Gelen mesajları ve kullanıcıları yönetin
3. **Komutlar**: Bot komutlarını oluşturun ve düzenleyin
4. **Otomasyon**: Anahtar kelime yanıtları ayarlayın
5. **Loglar**: Sistem loglarını inceleyin
6. **Ayarlar**: Bot ayarlarını yapılandırın
7. **Bildirimler**: Bildirim tercihlerini ayarlayın

## 📡 API Endpoints

### Bot Durumu
- `GET /status` - Bot durumunu getir
- `GET /stats` - İstatistikleri getir

### Mesaj İşlemleri
- `POST /send-test` - Test mesajı gönder
- `POST /send-message` - Kullanıcıya mesaj gönder

### Kullanıcı Yönetimi
- `GET /users` - Tüm kullanıcıları getir
- `POST /block-user` - Kullanıcı engelle
- `POST /unblock-user` - Kullanıcı engelini kaldır

### Komut Yönetimi
- `GET /commands` - Tüm komutları getir
- `POST /save-command` - Komut kaydet/güncelle
- `POST /delete-command` - Komut sil

### Otomasyon
- `POST /save-keyword` - Anahtar kelime yanıtı kaydet
- `POST /delete-keyword` - Anahtar kelime yanıtı sil

### Log Yönetimi
- `POST /filter-logs` - Logları filtrele
- `GET /export-logs` - Logları dışa aktar
- `POST /clear-logs` - Logları temizle

### Ayarlar
- `POST /save-settings` - Bot ayarlarını kaydet
- `POST /disconnect` - WhatsApp bağlantısını kes
- `GET /backup` - Veri yedekleme
- `POST /restore` - Veri geri yükleme

### Dışa Aktarım
- `GET /export-commands` - Komutları dışa aktar
- `GET /export-users` - Kullanıcıları dışa aktar

## 🎨 Tema ve Özelleştirme

### Karanlık/Aydınlık Mod
- Sağ üst köşedeki toggle ile tema değiştirme
- Otomatik tema kaydetme
- Tüm sayfalarda tutarlı tema

### Responsive Tasarım
- Mobil uyumlu arayüz
- Tablet ve desktop optimizasyonu
- Drawer menü sistemi

### DaisyUI Bileşenleri
- Modern kart tasarımları
- Tutarlı buton stilleri
- Modal ve dropdown menüler
- Form elemanları

## 🔒 Güvenlik

### Veri Güvenliği
- Yerel dosya tabanlı veri saklama
- JSON formatında şifrelenmemiş veri
- CORS koruması
- Input validasyonu

### WhatsApp Güvenliği
- LocalAuth stratejisi
- QR kod ile güvenli bağlantı
- Oturum yönetimi
- Bağlantı durumu takibi

## 📁 Dosya Yapısı

```
whatsapp-bot-panel/
├── backend/
│   ├── bot.js              # Ana bot dosyası
│   ├── package.json        # Backend bağımlılıkları
│   └── data/               # Veri dosyaları
│       ├── logs.json       # Sistem logları
│       ├── users.json      # Kullanıcı verileri
│       ├── commands.json   # Komut verileri
│       ├── keywords.json   # Anahtar kelime yanıtları
│       └── settings.json   # Bot ayarları
├── frontend/
│   ├── index.html          # Dashboard
│   ├── users.html          # Kullanıcı yönetimi
│   ├── commands.html       # Komut yönetimi
│   ├── automation.html     # Otomasyon
│   ├── logs.html           # Log yönetimi
│   ├── settings.html       # Ayarlar
│   ├── notifications.html  # Bildirimler
│   ├── script.js           # Ortak JavaScript
│   └── style.css           # Özel stiller
└── README.md               # Bu dosya
```

## 🚨 Sorun Giderme

### Yaygın Sorunlar

**QR Kod Görünmüyor**
- Backend'in çalıştığından emin olun
- Terminal çıktısını kontrol edin
- WhatsApp uygulamasını yeniden başlatın

**Bağlantı Kesiliyor**
- İnternet bağlantınızı kontrol edin
- WhatsApp Web oturumunu kontrol edin
- Bot'u yeniden başlatın

**Frontend Bağlanamıyor**
- Backend'in 3000 portunda çalıştığını kontrol edin
- CORS ayarlarını kontrol edin
- Tarayıcı konsolunda hata mesajlarını inceleyin

### Log Dosyaları
- Backend logları terminal'de görünür
- Frontend hataları tarayıcı konsolunda
- Veri dosyaları `backend/data/` klasöründe

## 🤝 Katkıda Bulunma

1. Fork yapın
2. Feature branch oluşturun (`git checkout -b feature/amazing-feature`)
3. Değişikliklerinizi commit edin (`git commit -m 'Add amazing feature'`)
4. Branch'inizi push edin (`git push origin feature/amazing-feature`)
5. Pull Request oluşturun

## 📄 Lisans

Bu proje MIT lisansı altında lisanslanmıştır. Detaylar için `LICENSE` dosyasına bakın.

## 📞 Destek

Sorularınız veya önerileriniz için:
- Issue açın
- Email gönderin
- Dokümantasyonu inceleyin

## 🔄 Güncellemeler

### v1.0.0
- İlk sürüm
- Temel bot yönetimi
- Dashboard ve istatistikler
- Kullanıcı yönetimi
- Komut sistemi
- Log yönetimi
- Ayarlar paneli
- Bildirim sistemi

---

**Not**: Bu proje WhatsApp'ın resmi API'si değildir. whatsapp-web.js kütüphanesi kullanılarak geliştirilmiştir. Kullanım sorumluluğu size aittir. 
## Yazarlar ve Teşekkür

- [@MertKyaa57](https://www.github.com/MertKyaa57) tasarım ve geliştirme için.

  
## Geri Bildirim

Herhangi bir geri bildiriminiz varsa, lütfen info@nexacode.com.tr adresinden bize ulaşın.

  
