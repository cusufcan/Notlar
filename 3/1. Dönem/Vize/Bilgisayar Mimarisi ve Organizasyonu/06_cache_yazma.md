# 06 Cache Yazma

### Bellek ve Genel Performans

### Toplam Beklenen Döngü Sayısı:

- Memory stall cycles = Memory accesses x miss rate x miss penalty
- CPU Time = (CPU execution cycles + Memory stall cycles) x Cycle time

### ÖRNEK:

- Diyelim ki programınızdaki komutların %33'ü belleğe erişiyor. Cache hit oranı %97 ve hit alınırsa veri bir saat sinyalinde, alınmazsa 20 saat sinyalinde geliyor.
  - Toplam komut sayısı I ise.
  - Memory stall cycles =
  - = (memory accesses) x (miss rate) x (miss penalty)
  - = 0.33 I x 0.03 x 20 saat sinyali
  - = 0.2 I saat sinyali
