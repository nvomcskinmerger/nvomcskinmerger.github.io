# 🎨 NVO MC SKIN MERGER

<div align="center">

## Next-Generation Minecraft Skin Merger

**Minecraft skinlerini birleştir, düzenle, önizle ve PNG olarak dışa aktar.**

[🌐 Live Demo](https://nvomcskinmerger.github.io/) · [💻 GitHub](https://github.com/nvomcskinmerger/nvomcskinmerger.github.io) · [🐛 Report a Bug](https://github.com/nvomcskinmerger/nvomcskinmerger.github.io/issues)

![Version](https://img.shields.io/badge/version-V1.1.1-8A2BE2?style=for-the-badge)
![License](https://img.shields.io/badge/license-MIT-success?style=for-the-badge)
![Platform](https://img.shields.io/badge/platform-Web-blue?style=for-the-badge)
![Minecraft](https://img.shields.io/badge/Minecraft-Skins-62B47A?style=for-the-badge)

</div>

---

## 📌 V1.1.1 Güncellemesi

**NVO MC SKIN MERGER V1.1.1** ile merger sistemi yeniden düzenlendi ve
mevcut mergerlerin durumları arayüzde açıkça gösterilecek şekilde
belgelendi.

### Durum etiketleri

| Etiket | Anlamı |
|---|---|
| 🟢 **GÜNCELLENDİ** | Merger aktif ve V1.1.1 kapsamında güncellenmiştir. |
| 🔵 **YENİ** | V1.1.1 ile eklenen yeni merger/özelliktir. |
| 🔴 **HATALI** | Bilinen bir hata nedeniyle şu anda güvenilir değildir. |
| ⚫ **KULLANIM DIŞI** | Artık kullanılmayan veya projeden kaldırılmıştır. |

> **V1.1.1 mevcut durum:** Bu sürümde aşağıdaki listede **HATALI** veya
> **KULLANIM DIŞI** olarak işaretlenen aktif bir merger yoktur.
> Mevcut mergerler **GÜNCELLENDİ** durumundadır.

---

# 🧩 Merger Durumları

Aşağıdaki liste mevcut proje dosyasındaki merger aileleri ve proje
README'sinde tanımlanan kullanıcı-facing isimler temel alınarak
hazırlanmıştır.

| # | Merger | V1.1.1 Durumu |
|---:|---|---|
| 1 | **50/50 / Half** | 🟢 Güncellendi |
| 2 | **Top / Bottom** | 🟢 Güncellendi |
| 3 | **Head Swap** | 🟢 Güncellendi |
| 4 | **Body Swap** | 🟢 Güncellendi |
| 5 | **Arm Swap** | 🟢 Güncellendi |
| 6 | **Leg Swap** | 🟢 Güncellendi |
| 7 | **Arms + Legs Swap** | 🟢 Güncellendi |
| 8 | **Head + Legs Swap** | 🟢 Güncellendi |
| 9 | **Head + Torso Swap** | 🟢 Güncellendi |
| 10 | **Base Only** | 🟢 Güncellendi |
| 11 | **Outer Overlay** | 🟢 Güncellendi |
| 12 | **Reverse Overlay** | 🟢 Güncellendi |
| 13 | **Front / Back** | 🟢 Güncellendi |
| 14 | **Blend** | 🟢 Güncellendi |
| 15 | **Checker Blend** | 🟢 Güncellendi |
| 16 | **Gradient Blend** | 🟢 Güncellendi |
| 17 | **Alternating Parts** | 🟢 Güncellendi |
| 18 | **Cross Limb Swap** | 🟢 Güncellendi |
| 19 | **Chimera / Random Mix** | 🟢 Güncellendi |
| 20 | **3 Skin Merger** | 🟢 Güncellendi |
| 21 | **4 Skin Merger** | 🟢 Güncellendi |
| 22 | **5 Skin Merger** | 🟢 Güncellendi |

### Durum özeti

- 🟢 **GÜNCELLENDİ:** Mevcut aktif mergerler.
- 🔵 **YENİ:** Şu anda ayrı bir yeni etiketi gerektiren aktif merger yok.
- 🔴 **HATALI:** Şu anda bildirilen aktif hatalı merger yok.
- ⚫ **KULLANIM DIŞI:** Kullanım dışı olarak işaretlenen aktif merger yok.

---

# ✨ Proje Hakkında

**NVO MC SKIN MERGER**, Minecraft skinlerini tarayıcı üzerinden
birleştirmek ve ortaya çıkan texture'ı kontrol etmek için hazırlanmış
browser-first bir uygulamadır.

Temel hedefler:

- Minecraft skinlerini hızlı şekilde birleştirmek
- Mevcut merger mekaniklerini korumak
- Minecraft UV yapısını dikkate almak
- Base ve overlay katmanlarını işlemek
- 2D texture sonucunu görmek
- 3D karakter önizlemesi yapmak
- Sonucu PNG olarak dışa aktarmak
- Birden fazla skin ile zincirleme çalışma yapmak

Uygulama masaüstü bir resim düzenleyicisine ihtiyaç duymadan tarayıcı
üzerinden çalışacak şekilde tasarlanmıştır.

---

# 🧩 Çoklu Skin Merger Sistemi

## 3 Skin Merger

3 Skin sistemi aşamalı olarak çalışır:

```text
Skin 1 ─┐
        ├── 50/50 ──┐
Skin 2 ─┘           │
                    ├── Top / Bottom ──> RESULT
Skin 3 ─────────────┘
```

İşlem sırası:

1. Skin 1 + Skin 2
2. Mevcut 50/50 merger
3. Ara sonuç + Skin 3
4. Mevcut Top / Bottom merger
5. Final sonuç

Bu yapı ayrı bir alternatif split sistemi yerine mevcut merger
mekaniklerinin zincirlenmesini esas alır.

---

## 4 Skin Merger

4 Skin sistemi iki adet 50/50 işlemini daha sonra Top / Bottom işlemiyle
birleştirir:

```text
Skin 1 ─┐
        ├── 50/50 ──┐
Skin 2 ─┘           │
                    ├── Top / Bottom ──> FINAL
Skin 3 ─┐           │
        ├── 50/50 ──┘
Skin 4 ─┘
```

İşlem sırası:

1. Skin 1 + Skin 2 → 50/50
2. Skin 3 + Skin 4 → 50/50
3. İki ara sonuç → Top / Bottom
4. Final sonuç

---

## 5 Skin Merger

5 Skin Merger, basitçe PNG'yi beş dikey kolon halinde kesmek yerine
**Minecraft model geometrisi ve UV bölgeleri üzerinden** beş eşit dikey
banda ayırma mantığı kullanır.

```text
Skin 1 ─┐
Skin 2 ─┤
Skin 3 ─┼── 5 eşit UV / model bandı ──> RESULT
Skin 4 ─┤
Skin 5 ─┘
```

Önemli noktalar:

- Tam olarak **5 skin** kullanılır.
- Bölme Minecraft modelinin yatay genişliği esas alınarak yapılır.
- İlgili UV yüzleri ayrı ayrı işlenir.
- Ön, arka, üst, alt ve yan yüzlerin UV yönleri korunur.
- Steve / Alex kol genişliği dikkate alınır.
- Base ve overlay katmanları UV bölgeleri üzerinden işlenir.
- **6 Skin Merger mevcut sürümün bir parçası değildir.**

---

# 🎯 Merger Aileleri

## Core

- 50/50 / Half
- Top / Bottom
- Head Swap
- Body Swap
- Arm Swap
- Leg Swap
- Arms + Legs Swap
- Head + Legs Swap
- Head + Torso Swap

## Texture / Overlay

- Base Only
- Outer Overlay
- Reverse Overlay
- Front / Back
- Blend
- Checker Blend
- Gradient Blend

## Advanced

- Alternating Parts
- Cross Limb Swap
- Chimera / Random Mix
- Custom Selective Merger

## Multi-Skin

- 3 Skin Merger
- 4 Skin Merger
- 5 Skin Merger

> **6 Skin Merger:** V1.1.1 kapsamında bulunmamaktadır.

---

# 🎨 Custom Selective Merger

Custom Selective Merger, tek bir global merger seçmek yerine belirli
vücut bölgelerini ayrı ayrı kontrol etmeye yönelik gelişmiş çalışma
alanıdır.

Genel akış:

```text
Base body seç
     ↓
Skin 1 / Skin 2 kaynaklarını seç
     ↓
Overlay katmanlarını kontrol et
     ↓
Sonucu önizle
     ↓
Final texture oluştur
```

Desteklenen hızlı seçim mantığı:

- All Skin 1
- All Skin 2
- Overlays Off

---

# 👤 Minecraft Kullanıcı Adı ile Skin Getirme

Uygulamada PNG yüklemenin yanında Minecraft kullanıcı adı üzerinden skin
yükleme workflow'u bulunur.

```text
Minecraft kullanıcı adı
        ↓
      GETİR
        ↓
     Skin yükle
        ↓
      Önizle
        ↓
       Merge
```

3, 4 ve 5 Skin workflow'larında ek skin alanları aynı temel yükleme
mantığını kullanacak şekilde tasarlanmıştır.

> Kullanıcı adıyla skin getirme özelliği harici profil/skin servislerine
> ve normal internet bağlantısına bağlıdır.

---

# 📐 Skin Formatları

Uygulama Minecraft skin texture çözünürlüklerini kontrol eder.

Desteklenen çözünürlükler:

| Çözünürlük | Durum |
|---|---|
| 64 × 32 | ✅ |
| 64 × 64 | ✅ |
| 128 × 64 | ✅ |
| 128 × 128 | ✅ |

UV-aware işlemlerde özellikle aşağıdaki bilgiler korunmalıdır:

- Texture koordinatları
- Head / torso / arm / leg bölgeleri
- Base layer
- Overlay layer
- Steve / Alex kol yapısı
- Texture çözünürlüğü

---

# 🧊 3D Önizleme

Uygulama yalnızca düz PNG sonucuna bakmakla sınırlı değildir.

3D skin viewer üzerinden karakteri incelemek ve mevcut animasyon
kontrollerini kullanmak mümkündür.

Örnek kontroller:

- 🚶 Walk
- 🏃 Run
- 🧍 Idle
- 🔄 Rotate

3D görüntü, UV üzerinde doğru görünen bir texture'ın Minecraft
karakterinde de doğru görünüp görünmediğini kontrol etmek için özellikle
faydalıdır.

---

# 🖼️ Sonuç ve Önizleme

Merge işleminden sonra workflow içerisinde:

- Final PNG
- UV texture görüntüsü
- Sonuç bilgileri
- Before / After karşılaştırması
- 3D karakter önizlemesi
- Sonucu tekrar Skin 1 olarak kullanma
- PNG dışa aktarma

gibi işlemler kullanılabilir.

Zincirleme kullanım:

```text
Skin 1 + Skin 2
      ↓
    RESULT
      ↓
Result → Skin 1
      ↓
Yeni Skin 2
      ↓
 NEXT MERGE
```

---

# 🔐 Giriş ve Hesap Özellikleri

Uygulamada Google / Firebase tabanlı hesap özellikleri bulunabilir.

Hesap gerektiren özellikler ile temel merger işlemleri birbirinden
ayrılacak şekilde tasarlanmıştır.

**Önemli:**

> Skin merge işleminin kendisi Google hesabıyla giriş yapılmasını
> gerektirmemelidir. Hesap gereksinimleri history, gallery veya korumalı
> hesap özellikleri gibi alanlarla sınırlı olabilir.

---

# 🛡️ Gizlilik

Skin işleme mümkün olan yerlerde browser-side olarak gerçekleştirilir.

Yüklenen skin dosyalarının işlenmesi ile hesap / Firebase özellikleri
aynı şey değildir.

Harici skin servisleri kullanıldığında, kullanıcı adı üzerinden skin
getirme işlemi ilgili harici servisin çalışma koşullarına bağlıdır.

Projeyi fork ederken storage, analytics, authentication veya harici
servislerde değişiklik yapılırsa gizlilik metinleri de yeniden kontrol
edilmelidir.

---

# ⚡ Kullanım

## 1. Siteyi aç

**https://nvomcskinmerger.github.io/**

## 2. Merger seç

İhtiyacına göre:

- 2 Skin
- 3 Skin
- 4 Skin
- 5 Skin
- Core mergerler
- Texture / Overlay mergerler
- Advanced mergerler
- Custom Selective Merger

kullanılabilir.

## 3. Skinleri yükle

Her slot için:

- PNG yükleyebilir
- Minecraft kullanıcı adı kullanabilir
- Skin önizlemesini kontrol edebilir
- Model / çözünürlük bilgilerini inceleyebilirsin

## 4. Merge yap

Seçilen mergeri çalıştır.

3, 4 ve 5 Skin sistemlerinde gerekli çoklu-skin işlemleri kendi
workflow'una göre gerçekleştirilir.

## 5. Sonucu kontrol et

Kontrol edilebilecek alanlar:

- 2D texture
- UV
- Before / After
- 3D karakter

## 6. Dışa aktar

Final PNG'yi indir.

---

# 💻 Teknoloji

NVO MC SKIN MERGER browser-first bir yapı kullanır.

### Frontend

- HTML5
- CSS3
- JavaScript
- Canvas API

### Rendering

- HTML Canvas
- WebGL tabanlı 3D skin viewer workflow
- Minecraft UV texture mapping

### Servisler

- Firebase Authentication
- Firebase ile ilişkili hesap/history özellikleri
- Harici Minecraft skin/profile servisleri

### Hosting

- GitHub Pages

### Ana uygulama

```text
index.html
```

Ana uygulama tek sayfalı web uygulaması mantığında çalışır ve statik
hosting için uygundur.

---

# 📂 Repository Yapısı

```text
nvomcskinmerger.github.io/
│
├── index.html
├── README.md
├── LICENSE
├── og-preview.png
├── favicon.png
├── favicon-512.png
└── apple-touch-icon.png
```

| Dosya | Görevi |
|---|---|
| `index.html` | Ana web uygulaması |
| `README.md` | Proje dokümantasyonu |
| `og-preview.png` | Open Graph / sosyal medya önizlemesi |
| `favicon.png` | Tarayıcı faviconu |
| `favicon-512.png` | Büyük uygulama ikonu |
| `apple-touch-icon.png` | Apple touch icon |
| `LICENSE` | MIT lisansı |

---

# 🌐 GitHub Pages

Proje statik hosting için uygundur.

1. Repository'yi fork veya clone et.
2. **Settings → Pages** bölümünü aç.
3. Yayınlanacak branch'i seç.
4. Repository root'u kaynak olarak seç.
5. Kaydet.
6. GitHub Pages deployment'ının tamamlanmasını bekle.

Ana uygulama için geleneksel Node.js veya PHP sunucusu gerekmez.

---

# 🧪 Kontrol ve Uyumluluk

Merge işleminden önce temel input kontrolleri yapılmalıdır.

Kontrol edilen durumlar arasında:

- PNG olmayan dosyalar
- Geçersiz PNG verisi
- Desteklenmeyen çözünürlükler
- Aşırı büyük dosyalar
- Uyumsuz skin formatları
- Okunamayan image data

bulunabilir.

## Tarayıcı

Modern tarayıcı kullanılması önerilir:

- Chrome
- Edge
- Firefox
- Safari

3D preview için WebGL desteği gereklidir.

---

# 🐛 Hata Ayıklama

## Merge çalışmıyor

Şunları kontrol et:

1. Gerekli skin slotlarının tamamı dolu mu?
2. 3 Skin için Skin 1–3 hazır mı?
3. 4 Skin için Skin 1–4 hazır mı?
4. 5 Skin için Skin 1–5 hazır mı?
5. Skin çözünürlükleri uyumlu mu?
6. PNG dosyaları geçerli mi?
7. Tarayıcı console'unda JavaScript hatası var mı?

## 5 Skin sonucu yanlış görünüyorsa

5 Skin sistemi basit PNG kolon kesme yöntemi değildir.

Özellikle kontrol edilmesi gerekenler:

- Skin UV layout'u
- Base / overlay yapısı
- Steve / Alex model tipi
- Texture çözünürlüğü
- Ön / arka / üst / alt yüzlerin yönleri
- Yan yüzlerin UV yönleri

3D preview sonucu kontrol etmek için kullanılmalıdır.

## Kullanıcı adı ile skin gelmiyor

Olası nedenler:

- Geçersiz Minecraft kullanıcı adı
- Oyuncu bulunamıyor
- Harici skin servisi geçici olarak çalışmıyor
- Network / CORS / browser kısıtlaması
- Geçici servis kesintisi

Gerekirse skin PNG olarak manuel yüklenebilir.

## 3D preview görünmüyor

Kontrol et:

- WebGL açık mı?
- Donanım hızlandırma aktif mi?
- Browser console hata veriyor mu?
- Oluşturulmuş bir sonuç var mı?

---

# 🧠 Tasarım İlkeleri

## 1. Mevcut merger mekaniklerini koru

Yeni özellikler mevcut merger mantığını gereksiz yere değiştirmeden
genişletilmelidir.

## 2. UV-aware işlem

Minecraft skinleri sıradan düz resimler değildir.

Bu nedenle merger işlemleri mümkün olduğunca:

- UV koordinatlarını
- model yüzlerini
- base layer'ı
- overlay layer'ı
- Steve / Alex farklarını

dikkate almalıdır.

## 3. Hızlı browser workflow

```text
Skin
 ↓
Merge
 ↓
Preview
 ↓
Export
```

## 4. Kademeli kullanım

Basit mergerlerden gelişmiş işlemlere kadar farklı kullanım seviyeleri
sunulur.

## 5. Creator-first UX

Amaç, kullanıcıyı karmaşık bir image editor workflow'una zorlamadan hızlı
skin denemeleri yapabilmesini sağlamaktır.

---

# 🤝 Katkıda Bulunma

Katkılar memnuniyetle karşılanır.

```bash
git clone https://github.com/nvomcskinmerger/nvomcskinmerger.github.io.git
cd nvomcskinmerger.github.io
```

Önerilen süreç:

1. Yeni branch oluştur.
2. Değişikliği yap.
3. Etkilenen mergerleri test et.
4. Farklı skin çözünürlüklerini test et.
5. 3 / 4 / 5 Skin workflowlarını ilgili değişikliklerde test et.
6. Username skin loading etkileniyorsa onu test et.
7. 3D preview etkileniyorsa onu test et.
8. Pull request aç.

### Bug report

Mümkün olduğunda şunları ekle:

- Tarayıcı ve sürümü
- İşletim sistemi
- Skin çözünürlüğü
- Merger adı
- Skin sayısı
- Tekrarlama adımları
- Console hatası
- Screenshot / video

---

# 🗺️ Roadmap

Gelecekte değerlendirilebilecek geliştirmeler:

- [ ] Daha gelişmiş texture kontrolleri
- [ ] Daha fazla multi-skin workflow
- [ ] Geliştirilmiş 3D editing
- [ ] Daha hassas layer kontrolleri
- [ ] Ek export seçenekleri
- [ ] Daha iyi mobil kullanım
- [ ] Daha fazla preview özelleştirmesi
- [ ] Genişletilmiş gallery özellikleri
- [ ] Gelişmiş skin analizi
- [ ] Büyük texturelarda performans iyileştirmeleri
- [ ] Creator-focused ek araçlar

---

# 📊 Proje Durumu

**Version: `V1.1.1`**

### V1.1.1 durum politikası

Bu sürümde mergerlerin yanında durum etiketi kullanılabilir:

- 🟢 **GÜNCELLENDİ**
- 🔵 **YENİ**
- 🔴 **HATALI**
- ⚫ **KULLANIM DIŞI**

**Mevcut V1.1.1 durumunda aktif mergerler güncellenmiş durumdadır.
Şu anda HATALI veya KULLANIM DIŞI olarak işaretlenecek aktif merger
bulunmamaktadır.**

Repository:

https://github.com/nvomcskinmerger/nvomcskinmerger.github.io

Live application:

https://nvomcskinmerger.github.io/

---

# 📄 License

Bu proje **MIT License** ile yayınlanmaktadır.

Detaylar için [`LICENSE`](./LICENSE) dosyasına bakın.

Copyright © 2026 **NVO MC Skin Merger / nvomcskinmerger**

---

# ⚠️ Trademark Notice

Minecraft, **Mojang AB / Microsoft Corporation**'ın ticari markasıdır.

NVO MC Skin Merger bağımsız bir projedir ve Mojang veya Microsoft ile
bağlantılı, onlar tarafından onaylanmış, sponsorluğu yapılmış veya resmi
olarak desteklenen bir proje değildir.

Google ve Google logosu Google LLC'nin ticari markalarıdır.

---

# 💙 Credits

Minecraft skin oluşturma topluluğu için **NVO MC Skin Merger** tarafından
geliştirilmiştir.

Proje işine yarıyorsa GitHub repository'sine ⭐ bırakabilirsin.

<div align="center">

### ⭐ Star the project if you find it useful!

**NVO MC SKIN MERGER — V1.1.1**

*Merge your skins. Build your character. Create something unique.*

</div>
