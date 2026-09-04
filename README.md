<div align="center">
  <img src="https://raw.githubusercontent.com/Parsozkn/Ankora-Linux/main/Ankora%20G%C3%BCncel%20Logo.jpg" alt="Ankora OS Logo" width="220" style="border-radius: 50%;">
</div>

<p align="left">
  <img src="https://img.shields.io/badge/S%C3%9CR%C3%9CM-2.0_(Z%C3%9CMR%C3%9CT)-0085d1?style=for-the-badge&labelColor=383838" alt="Sürüm">
  <img src="https://img.shields.io/badge/TABAN-ARCH_LINUX-1793d1?style=for-the-badge&labelColor=383838" alt="Taban">
  <img src="https://img.shields.io/badge/MASA%C3%9CST%C3%9C-XFCE_%7C_KDE-0085d1?style=for-the-badge&labelColor=383838" alt="Masaüstü">
  <img src="https://img.shields.io/badge/L%C3%B0SANS-A%C3%87IK_KAYNAK-41a013?style=for-the-badge&labelColor=383838" alt="Lisans">
</p>

# Ankora Linux AI Arch (Ankora OS - AI Arch Edition)

Ankora OS AI Arch; Arch Linux tabanlı, rolling release (yuvarlanan sürüm) modelini benimseyen, yüksek performans ve kararlılık odaklı modern bir Linux dağıtımı projesidir. Sistem, doğrudan terminale entegre çalışan yerel (lokal/çevrimdışı) AI asistanı ve geliştiricilere özel araçlarla donatılmıştır.

[🇬🇧 Click here for English README (English README için tıklayın)](README_EN.md)

---

## 📌 Ankora OS AI Arch Nedir?

Ankora OS AI Arch, Arch Linux'un sunduğu en güncel paket ekosistemini ve esnekliği, Ankora'nın optimize edilmiş çekirdek parametreleri ve yerel yapay zeka entegrasyonuyla birleştirir. Sistem, gereksiz telemetri ve arka plan yüklerinden arındırılmış olup, donanım kaynaklarını en üst düzeyde verimlilikle kullanır.

Sistemde yer alan dahili yapay zeka bileşeni, herhangi bir bulut sunucusuna veya API anahtarına ihtiyaç duymadan tamamen yerel kaynaklarınızla (çevrimdışı) çalışır. Terminal üzerinden anında teknik destek, komut yardımı ve hata ayıklama sağlar.

---

## 🛠 Temel Mühendislik Tercihleri ve Mimarisi

### 1. Arch Linux & Rolling Release (Yuvarlanan Sürüm)
* **Her Zaman Güncel:** En yeni çekirdek (kernel), sürücü ve yazılım güncellemelerine anında erişim.
* **AUR Desteği:** Arch User Repository (AUR) aracılığıyla binlerce topluluk paketine sorunsuz erişim.

### 2. Çevrimdışı Terminal AI Asistanı (`yardimci`)
Terminalde `yardimci` komutuyla çağrılan yapay zeka aracı:
* Verilerinizi hiçbir üçüncü şahıs veya bulut servisleriyle paylaşmaz, tamamen yerel bellek üzerinde çalışır.
* Shell komutları, paket yönetimi, konfigürasyon hataları ve kod blokları için akıllı ve hızlı çözümler üretir.

### 3. Gelişmiş Bellek Yönetimi (ZRAM + SWAP)
* **ZRAM Entegrasyonu:** RAM üzerinde gerçek zamanlı sıkıştırma uygulayarak disk I/O gecikmelerini önler ve OOM (Out-Of-Memory) kilitlenmelerini engeller.
* **vm.swappiness & Cache Optimizasyonları:** Disk okuma/yazma döngülerini en aza indirerek sistemin tepkiselliğini artırır.

### 4. Özel Ankora Araçları (Ankora Utilities)
Sistem yönetimi ve bakımını kolaylaştırmak amacıyla geliştirilen yerel araçlar:
* `ankora-backup`: Kolay ve hızlı sistem yedekleme aracı.
* `ankora-cleaner`: Gereksiz önbellek, eski günlük dosyaları ve artık paketleri temizleme aracı.

### 5. Görsel Tutarlılık & Hafif Masaüstü
* **XFCE & KDE Plasma:** Çift masaüstü kirliliği olmadan optimize edilmiş, tutarlı ve şık bir arayüz.
* **Fairy Wren Simge Seti:** Görsel bütünlük sağlayan özel simge paketi.
* **Bloat-Free:** Varsayılan olarak gelen gereksiz ve şişkin uygulamalar (LibreOffice vb.) temizlenmiş, yerine hafif ve işlevsel alternatifler eklenmiştir.

---

## 📊 Sürüm Karşılaştırma Tablosu

| Sürüm Adı | Sistem Tabanı | Yayın Tipi | Odak Noktası | Durum |
| :--- | :--- | :--- | :--- | :--- |
| **Ankora AI Debian** | Debian 13 (Trixie) | Sabit / Stable | Yüksek sistem stabilitesi, düşük kaynak kullanımı | **Aktif Sürüm** |
| **Ankora AI Arch** | Arch Linux | Rolling Release | En güncel paketler, yerel Ankora araçları (`ankora-backup`, `ankora-cleaner`) | **Aktif Sürüm / Geliştirme** |
| **Ankora Kurumsal** | Debian LTS | Sabit / LTS | Merkezi yönetim profilleri, sıkılaştırılmış güvenlik (AppArmor) | **Planlama** |
| **Ankora Geliştirici** | Debian / Arch | Özel Derleme | Hazır derleyici araçları (GCC, Rust, Go, Python) ve Zsh terminal yapısı | **Özel Sürüm** |

---

## 📋 Sistem Gereksinimleri

| Bileşen | Minimum Gereksinim | Önerilen Sistem |
| :--- | :--- | :--- |
| **İşlemci (CPU)** | 64-bit Çift Çekirdek (1.5 GHz) | 64-bit Dört Çekirdek (2.0 GHz+) |
| **Bellek (RAM)** | 2 GB (ZRAM Aktif) | 4 GB ve üzeri (AI modelleri için 8 GB+) |
| **Depolama** | 15 GB Boş Disk Alanı | 25 GB SSD Depolama |
| **Ekran Kartı** | KMS destekli herhangi bir GPU | Vulkan / OpenGL 4.5 destekli GPU |

---

## ⚡ Kurulum ve Kullanım Talimatları

### 1. ISO İmajını Diske Yazdırma
Linux terminali üzerinden `dd` komutu ile önyüklenebilir USB oluşturabilirsiniz:

```bash
sudo dd if=ankora-ai-arch-x86_64.iso of=/dev/sdX bs=4M status=progress conv=fsync
```

*(Lütfen `/dev/sdX` kısmını kendi USB sürücünüzün adıyla değiştirin.)*

### 2. Calamares Grafiksel Kurulumu
Sistem canlı oturumda (Live Mode) açıldığında masaüstündeki **"Install Ankora OS"** kısayoluna tıklayarak kullanıcı dostu Calamares yükleyicisiyle kurulumu başlatabilirsiniz.

---

## 🌐 Topluluk ve İletişim

Ankora OS tamamen açık kaynaklı bir topluluk projesidir. Katkıda bulunmak, hata bildirmek veya görüşlerinizi paylaşmak için aşağıdaki bağlantıları kullanabilirsiniz:

* 💬 **Topluluk Forumu:** [Ankalab Flarum Cloud](https://ankalab.flarum.cloud)
* 🌍 **Resmi Web Sitemiz:** [ankora.xo.je](http://ankora.xo.je) 
* 🐞 **Hata Bildirimi:** GitHub üzerindeki [Issues](../../issues) sekmesini kullanabilir veya forumda başlık açabilirsiniz.

---

### Lisans ve Kaynak Kodu

Ankora OS AI Arch, **Arch Linux** üzerine inşa edilmiştir. Temel sistem, Linux Çekirdeği ve upstream paketleri kendi orijinal lisansları (çoğunlukla GPL) altında dağıtılır.

Ankora OS'e özel geliştirilen tüm yapılandırmalar, masaüstü özelleştirmeleri, grafik tasarımları ve betikler (bu depoda yer alan kaynaklar) **MIT Lisansı** ile korunmaktadır.
