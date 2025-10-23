---
noteId: "f9ab8c40877811f080b1856a701bf9c8"
tags: []

---

# Dernek Yönetim Sistemi v2.0

Enterprise düzeyinde, modern ve ölçeklenebilir dernek yönetimi için PyQt5 tabanlı desktop uygulaması.

## ✨ Özellikler

### 📊 **Gelişmiş Üye Yönetimi**
- Kapsamlı üye profilleri (kişisel bilgiler, yakınlar, notlar)
- Akıllı arama ve filtreleme sistemi
- Otomatik üye numarası atama
- Detaylı üye raporları ve istatistikler
- Üye geçmişi takibi

### 💰 **Akıllı Ödeme Sistemi**
- Otomatik ödeme hesaplaması (yaş bazlı kayıt ücretleri)
- Çoklu para birimi desteği (€, $, £, ₺)
- Toplu ödeme işlemleri
- Ödeme durumu takibi ve raporları
- Tarih aralığı bazlı analiz

### 👨‍👩‍👧‍👦 **Aile Yönetimi**
- Detaylı yakın bilgileri
- Partner ve çocuk doğum tarihlerini otomatik takip
- Aile bağlantıları görselleştirme

### 📈 **Kapsamlı Raporlama**
- Üye özet raporları
- Finansal analiz raporları  
- Ödenmemiş aidatlar listesi
- Excel, PDF, TXT formatlarında export
- Özelleştirilebilir rapor filtreleri

### 🎨 **Modern Enterprise UI**
- Material Design inspired interface
- Açık/Koyu tema ile göz rahatlığı
- Responsive ve kullanıcı dostu tasarım
- Keyboard shortcuts desteği
- Multi-monitor uyumluluğu

### 🔧 **Enterprise Features**
- Yapılandırılabilir ayarlar sistemi
- Kapsamlı logging ve audit trail
- Otomatik backup sistemi  
- Data validation ve error handling
- Performance optimization

## 🏗️ **Modern Mimari**

### **Clean Architecture + Layered Pattern**

```
┌─────────────────────────────────┐
│          UI Layer               │  ← PyQt5 Pages, Dialogs, Widgets
├─────────────────────────────────┤
│       Service Layer             │  ← Business Logic, Validation
├─────────────────────────────────┤
│     Repository Layer            │  ← Data Access, Query Optimization  
├─────────────────────────────────┤
│       Database Layer            │  ← SQLite + Connection Management
├─────────────────────────────────┤
│    Infrastructure Layer         │  ← Logging, Config, Cache, Utils
└─────────────────────────────────┘
```

### **Design Patterns**
- **Repository Pattern**: Database abstraction
- **Service Layer Pattern**: Business logic separation  
- **Observer Pattern**: UI data synchronization
- **Singleton Pattern**: Configuration management
- **Factory Pattern**: Widget creation
- **Strategy Pattern**: Export functionality

## Kurulum

### Gereksinimler
```bash
pip install -r requirements.txt
```

### Çalıştırma
```bash
python main.py
```

## GitHub’a Hazırlık

Bu depoyu GitHub’a açmadan önce aşağıdaki adımları uygulayın:

1. Gizli dosyalar ve yerel artefaktlar için .gitignore eklendi.
    - Aşağıdaki dosya/klasörler GitHub’a gönderilmez: veritabanları (*.db), `backups/`, `logs/`, `__pycache__/`, `build/`, `payments_debug.txt`, `app_auth.json`, `login_settings.json` vb.
2. Örnek yapılandırma dosyaları eklendi:
    - `app_auth.example.json` → Yerelde `app_auth.json` olarak kopyalayın ve doldurun (hash’ler ile).
    - `login_settings.example.json` → Yerelde `login_settings.json` olarak kopyalayın (opsiyonel).
3. Mevcut repoda gizli veriler varsa (örn. `app_auth.json` içindeki kullanıcı hash’leri), geçmişten tamamen kaldırmak için Git geçmişi temizliği önerilir.
    - Not: Bunun için `git filter-repo` veya GitHub’ın “Remove sensitive data” rehberini takip edin.
4. Sürekli entegrasyon (CI) eklendi: `.github/workflows/ci.yml`
    - Bağımlılıkları kurar ve proje dosyalarını derleyerek (compileall) sentaks kontrolü yapar.

### Yerel yapılandırma

Uygulama varsayılan `config.json` ile çalışır. Hassas bilgiler `app_auth.json` içinde tutulur ve GitHub’a gönderilmez. Yeni kurulumda şu adımları izleyin:

```bash
# Örnekten gerçek dosyayı oluşturun
copy app_auth.example.json app_auth.json   # Windows PowerShell

# Dosyayı düzenleyip admin hesabını özelleştirin
# password_hash / recovery_answer_hash alanlarını güvenli hash’lerle doldurun
```

## Proje Yapısı

```
dernek-yonetim-sistemi/
├── main.py                 # Ana uygulama dosyası
├── requirements.txt        # Python bağımlılıkları
├── database/
│   └── database.py        # Veritabanı işlemleri
├── modules/
│   ├── app_functions.py   # Uygulama fonksiyonları
│   └── ui_functions.py    # UI yardımcı fonksiyonları
└── widgets/
    ├── members_page.py    # Üyeler sayfası
    ├── dues_page.py       # Aidatlar sayfası
    └── relatives_page.py  # Yakınlar sayfası
```

## Kullanım

### İlk Çalıştırma
1. Uygulamayı çalıştırın: `python main.py`
2. Sol menüden istediğiniz sayfaya geçin
3. Tema değiştirmek için sol alttaki tema butonunu kullanın

### Üye Ekleme
1. "Üyeler" sayfasına gidin
2. Sol taraftaki formu doldurun
3. "Ekle" butonuna tıklayın

### Aidat Ekleme
1. "Aidatlar" sayfasına gidin
2. Üye seçin ve aidat bilgilerini girin
3. "Ekle" butonuna tıklayın

### Yakın Ekleme
1. "Yakınlar" sayfasına gidin
2. Önce üye seçin
3. Yakın bilgilerini girin ve "Ekle" butonuna tıklayın

## Veritabanı

Uygulama SQLite veritabanı kullanır ve aşağıdaki tabloları içerir:

- **members**: Üye bilgileri
- **dues**: Aidat kayıtları
- **relatives**: Yakın bilgileri

Veritabanı dosyası (`association.db`) otomatik olarak oluşturulur.

## Özelleştirme

### Tema Değiştirme
- Uygulama içinden sol alttaki tema butonunu kullanın
- Kod seviyesinde `modules/ui_functions.py` dosyasından tema renklerini değiştirebilirsiniz

### Yeni Özellik Ekleme
- Yeni sayfalar için `widgets/` klasörüne yeni dosyalar ekleyin
- Veritabanı değişiklikleri için `database/database.py` dosyasını güncelleyin
- Ana pencereye yeni sayfaları `main.py` dosyasından ekleyin

## Lisans

Bu proje MIT lisansı altında lisanslanmıştır.

Detaylar için `LICENSE` dosyasına bakın.

## Katkıda Bulunma

1. Projeyi fork edin
2. Yeni bir branch oluşturun (`git checkout -b feature/yeni-ozellik`)
3. Değişikliklerinizi commit edin (`git commit -am 'Yeni özellik eklendi'`)
4. Branch'inizi push edin (`git push origin feature/yeni-ozellik`)
5. Pull Request oluşturun

## Destek

Herhangi bir sorun yaşarsanız veya öneriniz varsa, lütfen issue açın.

