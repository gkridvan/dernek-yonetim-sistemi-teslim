# Dernek Yönetim Sistemi • Kullanıcı Kılavuzu (v2.0)

Bu kılavuz, uygulamayı teslim klasöründen çalıştırma, temel işlemler (üye/ödeme/gider), “Yardımcı” seçimi, dışa aktarım ve yedekleme gibi konuları adım adım açıklar. Yeni başlayanlar için sade, gerektiğinde detaylıdır.

## 1) Sistem Gereksinimleri
- Windows 10/11 (64-bit)
- Teslim klasöründeki EXE dosyasından direkt çalışır (kurulum gerektirmez)
- PDF yazdırma için yüklü bir yazıcı sürücüsü önerilir (şart değil)

## 2) Kurulum ve İlk Giriş
1) Size verilen teslim klasörünü bilgisayarınızda uygun bir konuma kopyalayın (örn. Masaüstü).
2) Klasör içindeki `DernekYonetimSistemi.exe` dosyasını çalıştırın.
3) İlk giriş için kullanıcı adı: `admin`, parola: `admin123`.
4) Girişten sonra üst menüden “Kullanıcı > Şifre Değiştir” ile parolanızı hemen güncelleyin.

Bilgi: Uygulama ilk açılışta penceresini ekranı kaplayacak şekilde açar. Açık/Koyu tema ayarı mevcuttur.

## 3) Arayüz Hızlı Tur
- Sol menü: Üyeler • Ödemeler • Diğer Kişiler • Bildirim Zili • Tema • Çıkış
- Üst menü: Dosya (Dışa Aktar, Yedek) • Düzenle (Yeni Üye/Ödeme) • Görünüm (Sütunlar, Tema) • Ayarlar • Yardım
- Sayfalar tablo odaklıdır; arama kutuları ve hızlı filtreler bulunur.

## 4) Üyeler Sayfası
- Yeni Üye: “Düzenle > Yeni Üye” veya Ctrl+N
- Arama/Filtre/Sıralama: Üstteki arama kutusunu ve sütun başlıklarını kullanın.
- Vefat İşaretleme: Üyeyi vefat olarak işaretleyebilir, geri alabilir veya silebilirsiniz.
- Yardımcı (yeni):
	- Üye kartında “Üye Bilgileri” bölümünde “Yardımcı” alanından, üyenin yakınları listeden seçilebilir.
	- Yakınlar kartlarında “⭐ Yardımcı Yap” ve “Yardımcıyı Kaldır” butonları (düzenleme modunda) görünür.
	- Üyeler tablosunda “Yardımcı” sütununu “Görünüm > Sütunlar > Üyeler” menüsünden açıp/kapatabilirsiniz.
	- Mevcut yardımcı yakını, kartlarda yıldız (⭐) ile vurgulanır.

### Etiket/Adres Dışa Aktarımı (Seçim Odaklı)
- Seçin: Üye tablosunda etiketini yazdırmak istediğiniz satırları (Ctrl/Shift ile çoklu) seçin.
- Dışa aktar: Üst menü “Dosya > Dışa Aktar…” (Ctrl+E) veya sayfadaki küçük 🖨 butonunu kullanın.
- Format seçin: PDF / Excel / CSV / TXT.
- Not: Artık dışa aktarım “yalnızca seçili satırlar” mantığıyla çalışır. Görünür tüm satırları almak isterseniz “Hepsini Seç” (Ctrl+A) yapın.
- PDF’te başlık “Üye Listesi” olarak çıkar ve Türkçe karakterler için gerekli font paketlemede dahildir.

## 5) Üye Kartı (Detay)
- Sekmeler: Üye Bilgileri • Yakınlar • Ödemeler • Notlar
- Yardımcı seçimi iki yerden yapılabilir:
	1) Üye Bilgileri alanındaki “Yardımcı” açılır listeden bir yakını seçip “Kaydet”.
	2) Yakın kartındaki “⭐ Yardımcı Yap” ile anında atama; “Yardımcıyı Kaldır” ile kaldırma.
- Yakın Adresi Otomatik Doldurma: Eksik yakın adresleri, üye adresi ile güvenli bir şekilde tamamlanmıştır.

## 6) Ödemeler Sayfası
- Yeni Ödeme: “Düzenle > Yeni Ödeme” veya Ctrl+P
- Yıllık Aidat Oluştur: Tüm aktif üyeler için toplu kayıt (Ctrl+Y)
- Ödeme Türleri: Aidat, Bağış, Üye Gideri, Etkinlik, Kayıt Ücreti, Diğer
	- “Üye Gideri”: Bireysel üyelere bağlı harcamalar içindir.
	- “Dernek Giderleri” (aşağıda) derneğin kurumsal/organizasyonel giderleri içindir; Ödemeler’den ayrıdır.
- Dışa Aktar: Ctrl+E ile sadece seçili satırlar dışa aktarılır.

Not: Bir üye vefat olarak işaretlendiğinde oluşturulan “Üye Gideri” ödemesi listede görünür ve “Vefat Edenler” sayfasındaki ilgili sütunda da yer alır. Vefat tarihi ve ilgili gider tarihi varsayılan olarak bugünün tarihiyle başlatılır; istenirse düzenlenebilir.

## 7) Dernek Giderleri (Yeni Sayfa)
- Konum: Üst menüden veya ana sayfa sekmelerinden “Giderler/Dernek Giderleri”.
- Ekle: Tarih • Kategori • Tutar • Açıklama alanlarını doldurun.
	- Akıllı Kategori Önerileri ve “Kaydet & Yeni” ile seri giriş yapılabilir.
	- Tutar ve tarih alanlarında geçerlilik kontrolleri vardır; hatalı giriş engellenir.
- Düzenle/Sil: Satırı seçip sağ tık menüsünden veya butonlardan işlemleri yapın.
- Özet: Sayfa üstünde yıl ve kategori bazlı toplamlar gösterilir.
- Dışa Aktar: Seçili giderleri PDF/Excel/CSV/TXT olarak dışa aktarın (Ctrl+E). ID sütunu otomatik hariç tutulur.

### Hızlı Filtreleme ve Pivot
- Başlıkta “Grupla” kutusunun yanında “Kategori” açılır listesi bulunur. Buradan bir kategori seçerek tabloyu anında filtreleyebilirsiniz. “Tümü” seçimi filtreyi temizler.
- 📊 Pivot Dışa Aktarım: Seçili veya seçtiğiniz kategoriye göre alt kategorileri sütunlara dağıtarak tek satırlık özet bir rapor alabilirsiniz. Dışa aktarım penceresinde formatı (Excel/PDF/CSV/TXT) seçin.

## 8) Dışa Aktarım Ayrıntıları
- Formatlar: PDF (.pdf), Excel (.xlsx), CSV (.csv), Metin (.txt)
- Sütun Seçimi: Dışa aktarım penceresinde hangi sütunların dahil edileceğini işaretleyin.
- Yerleşim (PDF): Tablo çok genişse otomatik yatay (landscape) alınır; satırlar otomatik kaydırılır.
- PDF Başlığı: B/W (siyah-beyaz) çıktı uyumlu olacak şekilde başlık satırında arka plan kullanılmaz; üst-alt çizgiler ve biraz daha büyük yazı tipiyle vurgulanır.
- Excel: Tutarlar sayısal olarak yazılır; filtre/toplamlar Excel’de yapılabilir.

## 9) Yedekleme ve Geri Yükleme
- Günlük Otomatik Yedek: Uygulama açılışında bir kez alınır; `backups/` klasöründe tutulur.
- Manuel Yedek: Dosya > “Yedek Al” (Ctrl+Shift+B). USB/harici diske kopyalamanız önerilir.
- Yedekten Geri Yükle: Dosya > “Yedekten Geri Yükle”. İşlem öncesi mevcut veritabanı otomatik `pre_restore_backup.db` olarak yedeklenir ve işlem sonrası uygulama yeniden başlatılır.
- Veritabanı Dosyası: `association.db` (EXE’nin olduğu klasörde). Taşırken kapalı olduğundan emin olun.

## 10) Bildirimler
- Yaş/ödeme gibi kurallara bağlı bilgilendirmeler yapılır; sol üstte çan ikonunda sayı görünür.
- Kısayol: Ctrl+B

## 11) Klavye Kısayolları
- Ctrl+N: Yeni Üye
- Ctrl+P: Yeni Ödeme
- Ctrl+Y: Yıllık Aidat Oluştur
- Ctrl+E: Dışa Aktar (seçili satırlar)
- Ctrl+B: Bildirimler
- Ctrl+Shift+B: Yedek Al
- Ctrl+Shift+L: Oturumu Kapat
- Ctrl+Q: Uygulamadan Çık (onay ister)
- F1: Hakkında • F5: Yenile

## 12) Sık Sorulanlar (SSS)
1) Yardımcı nedir? Nasıl seçerim?
	 - Bir üyenin işlemleri sırasında iletişim kurulacak öncelikli yakınıdır. Üye kartında “Yardımcı” listesinden seçebilir veya Yakın kartındaki “⭐ Yardımcı Yap” ile atayabilirsiniz.
2) Etiket yazdırırken kimler çıkar?
	 - Sadece tablodan seçtiğiniz satırlar dışa aktarılır. Tümünü istiyorsanız Ctrl+A ile hepsini seçin.
3) “Üye Gideri” ile “Dernek Giderleri” farkı nedir?
	 - Üye Gideri: Bireysel üyeye bağlı (Ödemeler sayfası). Dernek Giderleri: Kurumsal/organizasyonel giderler (Giderler sayfası).
4) PDF’te Türkçe karakter sorunu olur mu?
	 - Teslim EXE paketinin içinde gerekli fontlar vardır; PDF’ler Türkçe karakterlerle sorunsuz oluşturulur.

## 13) Sorun Giderme
- PDF sığmıyor: Gereksiz sütunları geçici gizleyin; uygulama geniş tabloları otomatik landscape alır.
- Kısayol çalışmıyor/çakışıyor: Aynı kısayolu kullanan farklı bir menü öğesi olabilir. Çakışmaları engellemek için kısayolu değiştirin.
- Yedekten dönüş hatası: Yedek dosyasının sağlam olduğundan emin olun; dosya başka bir programda açık olabilir.
- Antivirüs uyarısı: EXE doğrulandığında klasörü güvenilir listeye ekleyin. Uygulama dış ağ bağlantısı kurmaz.

## 14) Destek
Sorun veya öneri iletirken `logs/app.log` ve `logs/auth_audit.log` dosyalarını eklemeniz incelemeyi hızlandırır.
