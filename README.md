🧩 NVO Minecraft Skin Merger

«Minecraft skinlerini hızlı, kolay ve gelişmiş bir arayüz üzerinden birleştirin.»

"Version" (https://img.shields.io/badge/version-1.0.0-blue)
"Minecraft" (https://img.shields.io/badge/Minecraft-Skin-green)
"HTML" (https://img.shields.io/badge/HTML5-orange)
"CSS" (https://img.shields.io/badge/CSS3-blue)
"JavaScript" (https://img.shields.io/badge/JavaScript-yellow)
"License" (https://img.shields.io/badge/license-MIT-lightgrey)

NVO Minecraft Skin Merger, Minecraft skinlerini farklı birleştirme yöntemleriyle tek bir skin üzerinde bir araya getirmek için geliştirilmiş web tabanlı bir araçtır.

Proje tamamen tarayıcı üzerinden çalışacak şekilde tasarlanmıştır. Kullanıcılar skin dosyalarını yükleyebilir veya Minecraft kullanıcı adı üzerinden skin getirebilir ve ardından seçilen merger sistemiyle skinleri birleştirebilir.

---

✨ Özellikler

🎨 Gelişmiş Skin Birleştirme

NVO Minecraft Skin Merger birden fazla skinin tek bir sonuç üzerinde birleştirilmesini destekler.

Desteklenen sistemler:

- 🧩 2 Skin Merger
- 🧩 3 Skin Merger
- 🧩 4 Skin Merger
- ⚡ 50/50 Skin Merger
- ↕️ Üst / Alt Skin Merger

Mevcut merger sistemleri korunarak yeni özelliklerin aynı sistem üzerine eklenmesi hedeflenmiştir.

---

🧩 2 Skin Merger

İki farklı Minecraft skinini birleştirmek için kullanılır.

50/50 Merger

İki skinin ilgili bölümleri mevcut merger algoritması kullanılarak birleştirilir.

Skin 1
   +
Skin 2
   ↓
50/50 Merger
   ↓
Sonuç Skin

---

🧩 3 Skin Merger

Üç farklı skinin aşamalı olarak birleştirilmesini sağlar.

İşlem sırası:

Skin 1 + Skin 2
       ↓
    50/50
       ↓
Ara Sonuç
       +
     Skin 3
       ↓
   Üst / Alt
       ↓
Final Skin

Bu sistem sayesinde ilk iki skin mevcut 50/50 merger sistemiyle birleştirilir ve ortaya çıkan sonuç üçüncü skin ile Üst / Alt yöntemiyle birleştirilir.

---

🧩 4 Skin Merger

Dört farklı Minecraft skinini tek sonuçta birleştirmek için kullanılır.

İşlem sırası:

Skin 1 + Skin 2          Skin 3 + Skin 4
      ↓                         ↓
   50/50                     50/50
      ↓                         ↓
 Ara Sonuç 1              Ara Sonuç 2
          \                   /
           \                 /
            ↓               ↓
             Üst / Alt
                 ↓
             Final Skin

İşlem aşamaları

1. aşama

Skin 1 + Skin 2 → 50/50

2. aşama

Skin 3 + Skin 4 → 50/50

3. aşama

Ara Sonuç 1 + Ara Sonuç 2 → Üst / Alt

Sonuç olarak dört skin tek bir Minecraft skininde birleştirilir.

---

👤 Minecraft Kullanıcı Adı ile Skin Getirme

Skin dosyası yüklemek zorunda kalmadan Minecraft kullanıcı adı üzerinden skin getirme özelliği kullanılabilir.

Örneğin:

Minecraft Kullanıcı Adı
        ↓
      Getir
        ↓
Minecraft Skin
        ↓
Skin Merger

Bu özellik Skin 1 ve Skin 2'nin yanı sıra desteklenen çoklu skin alanlarında da kullanılabilir.

---

🖥️ Modern Arayüz

V1.0.0 ile proje yeni nesil bir arayüz yaklaşımıyla geliştirilmektedir.

Arayüzde:

- Modern kart yapısı
- Glass / modern UI görünümü
- Skin önizleme alanları
- Dosya yükleme alanları
- Minecraft kullanıcı adı alanı
- Skin temizleme kontrolleri
- Merger seçim ekranı
- Sonuç önizlemesi
- Durum ve işlem bildirimleri

bulunur.

Amaç yalnızca görsel olarak modern bir arayüz oluşturmak değil, mevcut Merger mekaniklerini bozmadan daha kullanışlı bir deneyim sunmaktır.

---

🧱 Desteklenen Skin Yapıları

Proje farklı Minecraft skin formatlarını kontrol ederek uygun işlem akışını kullanır.

Desteklenen yapılar arasında:

- "64x32"
- "64x64"
- "128x64"
- "128x128"

gibi skin çözünürlükleri için mevcut dönüştürme ve kontrol mekanizmaları bulunmaktadır.

Skin yükleme sırasında çözünürlük ve model bilgileri kontrol edilir.

---

⚙️ Nasıl Çalışır?

Genel işlem akışı:

             ┌───────────────┐
             │ Skin Yükleme  │
             └───────┬───────┘
                     │
                     ▼
             ┌───────────────┐
             │ Format Kontrol│
             └───────┬───────┘
                     │
                     ▼
             ┌───────────────┐
             │ Model Kontrol │
             └───────┬───────┘
                     │
                     ▼
             ┌───────────────┐
             │ Merger Seçimi │
             └───────┬───────┘
                     │
          ┌──────────┼──────────┐
          ▼          ▼          ▼
       2 Skin      3 Skin      4 Skin
          │          │          │
          └──────────┼──────────┘
                     ▼
             ┌───────────────┐
             │ Merge Engine  │
             └───────┬───────┘
                     │
                     ▼
             ┌───────────────┐
             │ Sonuç Önizleme│
             └───────────────┘

---

🛠️ Teknolojiler

Proje temel olarak web teknolojileri kullanılarak geliştirilmiştir.

Frontend

- HTML5
- CSS3
- JavaScript
- Canvas API

Canvas Engine

Skin birleştirme işlemleri tarayıcının Canvas API'si üzerinden gerçekleştirilir.

Bu sayede skin parçaları piksel seviyesinde işlenebilir.

---

📁 Proje Yapısı

Projenin temel yapısı tek HTML dosyası üzerine kurulabilir:

nvomcskinmerger.github.io/
│
├── index.html
├── README.md
└── LICENSE

Tek dosyalı kullanım sayesinde projeyi herhangi bir sunucuya veya statik hosting hizmetine kolayca yüklemek mümkündür.

---

🚀 Kurulum

Projeyi çalıştırmak için herhangi bir özel backend kurulumu gerekmez.

1. Repoyu klonlayın

git clone https://github.com/nvomcskinmerger/nvomcskinmerger.github.io.git

2. Proje klasörüne girin

cd nvomcskinmerger.github.io

3. Siteyi açın

"index.html" dosyasını doğrudan tarayıcıda açabilir veya herhangi bir statik web sunucusu kullanabilirsiniz.

Örneğin:

python -m http.server 8000

Ardından:

http://localhost:8000

adresini açabilirsiniz.

---

📖 Kullanım

1️⃣ Skin yükleyin

Skin alanlarından:

- Bilgisayarınızdan ".png" skin yükleyebilir
- Minecraft kullanıcı adı girerek skin getirebilirsiniz.

---

2️⃣ Merger türünü seçin

İhtiyacınıza göre:

2 Skin
3 Skin
4 Skin

merger sistemlerinden birini seçin.

---

3️⃣ Skinleri kontrol edin

Yüklenen skinlerin:

- Önizlemesini
- Çözünürlüğünü
- Model bilgisini

kontrol edin.

---

4️⃣ Birleştirin

Gerekli skinler yüklendikten sonra:

Birleştir

butonunu kullanarak işlemi başlatın.

---

5️⃣ Sonucu alın

Birleştirme tamamlandığında oluşturulan skin sonuç alanında görüntülenir.

---

🔧 Hata Kontrolleri

Proje skin yükleme sırasında çeşitli kontroller gerçekleştirir.

Örneğin:

- Geçersiz dosya
- Desteklenmeyen çözünürlük
- Eksik skin
- Model uyumsuzluğu
- Eksik çoklu skin alanı

gibi durumlarda kullanıcıya durum bildirimi gösterilir.

Bu kontroller, merger motorunun hatalı veya eksik veriyle çalışmasını önlemeye yardımcı olur.

---

🔐 Gizlilik

Skin dosyaları kullanıcının tarayıcısı üzerinden işlenebilecek şekilde tasarlanmıştır.

Projenin temel amacı, skin birleştirme işlemini mümkün olduğunca istemci tarafında gerçekleştirmektir.

«Not: Harici skin servisleri veya API'ler kullanıldığında ilgili servisin kendi gizlilik politikaları geçerli olabilir.»

---

🌐 GitHub Pages

Proje statik HTML/CSS/JavaScript yapısında olduğu için GitHub Pages üzerinde yayınlanabilir.

Genel yapı:

GitHub Repository
       ↓
GitHub Pages
       ↓
NVO Minecraft Skin Merger

Repository içerisindeki "index.html" dosyasını ana sayfa olarak kullanabilirsiniz.

---

🗺️ Roadmap

V1.0.0

- [x] Temel Skin Merger
- [x] 2 Skin Merger
- [x] 3 Skin Merger
- [x] 4 Skin Merger
- [x] 50/50 Merger
- [x] Üst / Alt Merger
- [x] Skin önizleme
- [x] Minecraft kullanıcı adı ile skin getirme
- [x] Çoklu skin yükleme
- [x] Model kontrolü
- [x] Çözünürlük kontrolü
- [x] Modern arayüz çalışmaları

🔮 Gelecek Sürümler

Planlanan geliştirmeler:

- [ ] Daha gelişmiş merger seçenekleri
- [ ] Daha fazla skin formatı
- [ ] Gelişmiş önizleme
- [ ] Undo / Redo sistemi
- [ ] Daha gelişmiş skin düzenleme
- [ ] Piksel bazlı düzenleme
- [ ] Daha fazla model desteği
- [ ] Mobil arayüz iyileştirmeleri
- [ ] Performans optimizasyonları
- [ ] Yeni tema seçenekleri

---

🐛 Bug Report

Bir hata bulduysanız GitHub üzerinden Issues bölümünü kullanabilirsiniz.

Bir bug bildirirken mümkünse aşağıdaki bilgileri ekleyin:

Minecraft Skin Merger Version:
Browser:
Operating System:

Merger Type:
Skin Resolution:

Problem:

Örneğin:

Version: V1.0.0
Browser: Chrome
OS: Windows 11

Merger Type: 4 Skin
Resolution: 64x64

Problem:
Skin 3 kullanıcı adıyla yüklendiğinde merger çalışmıyor.

---

🤝 Katkıda Bulunma

Projeye katkıda bulunmak istiyorsanız:

1. Repository'yi Fork edin.
2. Yeni bir branch oluşturun.

git checkout -b feature/yeni-ozellik

3. Değişikliklerinizi yapın.
4. Commit oluşturun.

git commit -m "feat: yeni merger özelliği"

5. Branch'i gönderin.

git push origin feature/yeni-ozellik

6. Pull Request oluşturun.

---

📌 Sürüm Sistemi

Proje sürümleri aşağıdaki formatı takip eder:

MAJOR.MINOR.PATCH

Örneğin:

V1.0.0

MAJOR

Büyük sistem değişiklikleri.

MINOR

Yeni özellikler.

PATCH

Hata düzeltmeleri ve küçük geliştirmeler.

---

📜 License

Bu proje MIT License altında dağıtılmaktadır.

Projeyi kullanabilir, değiştirebilir ve geliştirebilirsiniz. Ancak projeyi dağıtırken lisans koşullarına uymanız gerekir.

---

⭐ Destek Ol

Projeyi beğendiyseniz GitHub repository'sine ⭐ Star bırakabilirsiniz.

Bug bildirmek, fikir paylaşmak veya geliştirmeye katkıda bulunmak için Issues ve Pull Requests bölümlerini kullanabilirsiniz.

---

🚀 NVO Minecraft Skin Merger

Yeni nesil arayüz.
Aynı güçlü Merger sistemi.
Daha fazla skin. Daha fazla kontrol.

V1.0.0 — The new beginning. 🧩🔥
