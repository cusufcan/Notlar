# 04 - Cache Bellekler

### Hız Karşılaştırması:

Statik RAM -> En hızlı, Pahalı, En küçük
Dinamik RAM -> Yavaş, Ucuz, Büyük
Hard Diskler -> En yavaş, En ucuz, En büyük

### Hits and Misses:

- Cache Hit: Aranan verinin cache içinde olması demektir.
- Cache Miss: Aranan verinin cache içinde olmaması demektir.
- Hit Rate: 0.0 - 1.0 aralığındadır. Gerçekleşen olumlu işlerin oranı.
- Miss Rate: 1 - hit rate ile bulunur. Gerçekleşen olumsuz işlerin oranı.

### Cache Hit ve Miss Genel Performans Formülü:

- Bir cache bellek yüzde olarak (0.0->1.0) hit oranında bellek işleminin C saat sinyalinde,
- Geri kalan işlerini de miss ya da (1-hit) işlemi de bir üst bellekten C + M saat sinyalinde gerçekştirsin.
  - Niye C+M, çünkü cache'e sorduk yok (C saat sinyali), üst bellekten getirdik (M saat sinyali).
- Bu durumda:
  - Süre = hit x C + miss x (C + M)
  - Süre = (hit + miss) x C + (miss x M) #Not: (hit + miss) = 1
  - Süre = C + (miss x M)

### Örnek:

- L1 cache'imiz 1 saat sinyalinde cevap versin, %95 hit oranı olsun, ana bellek 50 saat sinyalinde cevap versin.
- %95 işlem 1 saat sinyalinde, %5 işlem (1+50) saat sinyalinde gerçekleşir.
  - 1 + (0.05 x 50) = 3.5 saat sinyali (basitleştirilmiş formül)
  - L1 cache olmasa 50 saat sinyaliydi
- Araya bir L2 cache ekleyelim. L2 cache'imiz 10 saat sinyalinde cevap versin, %90 hit oranı olsun. sonuç ne olur?
  - 0.95 + (0.05 x (L2 + RAM Gecikmesi)) haline dönüşür, parantez içini hesaplayalım:
    - L2 + Ram Gecikmesi = 10 + (0.10 x 50) = 15
    - Burası bile 50 yerine 15 saat sinyali.
  - Bulunan değeri parantezin içine yazarsak:
    - 1 + (0.05 x 15) = 1.75
    - L1 + L2 cache daha güzel.
