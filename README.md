# BakeryFlow

Flask ve MySQL tabanlı rol bazlı fırın yönetim ve sipariş operasyon sistemi

## Genel Bakış

`BakeryFlow`, müşteri, yönetici ve kurye taraflarını tek uygulama içinde bir araya getiren full-stack bir fırın operasyon projesi. Bu projede amaç sadece ürün satışı yapmak değil; ürün, stok, sipariş, teslimat ve kullanıcı etkileşimini tek bir iş akışı içinde modellemekti.

## Kapsanan İş Alanları

| Alan | Kapsam |
| --- | --- |
| Ürün Yönetimi | kategori, ürün, aktif / pasif yönetimi |
| Müşteri Deneyimi | kayıt, giriş, profil, adres, favori, yorum |
| Sipariş Akışı | sepet, ödeme tipi, sipariş durumu, sipariş detayı |
| Operasyon | stok takibi, stok hareketleri, sipariş logları |
| Kurye Süreci | sipariş atama, taşıma, teslim durumu |
| Yönetim Paneli | müşteri, kurye, kupon, mesaj ve ayar ekranları |

## Rol Bazlı Yapı

### Müşteri Katmanı

Müşteri tarafında geliştirilen temel akışlar:

- ürünleri inceleme
- ürün arama
- sepete ürün ekleme
- kupon uygulama
- sipariş oluşturma
- adres yönetimi
- favorilere ekleme
- yorum bırakma
- sipariş geçmişini takip etme

### Yönetici Katmanı

Yönetici tarafında ele alınan başlıca alanlar:

- ürün ve kategori yönetimi
- siparişleri izleme ve güncelleme
- kurye operasyonunu takip etme
- kupon ve kampanya alanları
- mesaj ve yorum moderasyonu
- sistem ayarları

### Kurye Katmanı

Kurye paneli üzerinden:

- atanmış siparişleri görüntüleme
- teslimat sürecini yönetme
- sipariş durumunu değiştirme
- operasyonel iletişim akışına katılma

## Teknik Yapı

Proje teknik olarak şu bileşenlerden oluşuyor:

- Flask tabanlı backend
- Jinja2 template tabanlı server-side UI
- MySQL veritabanı
- SQL tabanlı veri modeli
- tek dosyada yoğunlaşan route ve iş kuralı yapısı

## Veri Modeli

`firin_db.sql` üzerinden görülen ana tablolar:

- `kullanici`
- `adres`
- `kategori`
- `urun`
- `stok`
- `siparis`
- `siparis_detay`
- `siparis_durum_log`
- `sepet`
- `favoriler`
- `yorum`
- `kupon`
- `stok_hareketi`

Bu yapı, yalnızca katalog verisini değil; sipariş yaşam döngüsünü ve operasyonel geçmişi de izlenebilir hale getiriyor.

## Öne Çıkan Dosyalar

| Dosya / Klasör | Rolü |
| --- | --- |
| `app.py` | uygulamanın ana backend ve route merkezi |
| `firin_db.sql` | veritabanı şeması ve seed veriler |
| `ER_DIYAGRAMI.md` | veri ilişkilerinin görsel / mantıksal karşılığı |
| `templates/` | müşteri, yönetici ve kurye ekranları |
| `static/` | görseller ve yardımcı statik varlıklar |

## Repo Yapısı

```text
BakeryFlow/
|-- app.py
|-- firin_db.sql
|-- ER_DIYAGRAMI.md
|-- requirements.txt
|-- start_firin.bat
|-- static/
|-- templates/
`-- README.md
```

## Kullanılan Teknolojiler

- Python
- Flask
- MySQL
- Jinja2
- HTML / CSS
