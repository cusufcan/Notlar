# 05 Gelişmiş Cache Bellekler

- Cache indeks değeri adresin sağda kalan son 8 bitidir.

### Cache Kaç Blok Tutar?

- 8-bit indeks -> 2^8 = 256 blok
  Bu cache yapısı için kaç bit kullanılır (veri, tag, valid bitleri toplamı)?
- tag boyutu = 24 bit (32 bit adres - 8 bit indeks)
- (24 tag biti + 1 valid biti + 8 veri biti) x 256 blok
- = 33 bit x 256 = 8448 bit

### Ortalama Bellek Erişim Zamanı:

### AMAT:

AMAT = Hit time + (Miss rate x Miss penalty)

### AMAT ÖRNEK:

1000 satırlık bir programda %33 oranında bellek kullanımı var. Cache'in hit oranı %97 ve aranan bilgi cache'de ise (hit time) 1 saat sinyalinde CPU'ya geliyor, ama değilse (miss penalty) 54+1 saat sinyali sürüyor.
AMAT HESAPLAMASI NASIL OLUR?

AMAT = Hit time + (Miss rate x Miss penalty)
= 1 saat sinyali + (0,03 x 55 saat sinyali)
= 2.65 saat sinyali

### AMAT ZAMAN ÖLÇME NASIL OLUR?

komut = 1000
oran = 0.33
amat saat = 2.65
kalan oran = 0.67
kalan saat = 1

T = (komut) x ((oran) x (amat) + (geriye kalan komutlar) x (kalan saat))
= 1000 x (0.33 x 2.65 + 0.67 x 1)
= 1000 x 1,5445 = 1545 saat sinyali

### Miss Rate Nasıl Düşürülür?

- Az önce sadece L1 konuşuyorduk, L2 cache de koymamız gerekli.
