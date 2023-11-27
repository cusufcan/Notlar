# Kendi Notlarım

### Hit Oranı Elle Hesaplama Sorusu

- L1 cache tuttuğu bloklarda yan yana 64 byte saklasın.
  Büyük tamsayı dizilerde beklenen oran ne olur?

        + Tamsayılar 4 byte'dır.
        + 64 byte'a kaç tane 4 byte sığar?
        + 64/4 = 16 tane sığar.
        + İlk değer hatalı çıkar => 1/16
        + Diğer değerler doğru => 15/16
        + Yani miss oranı => 15/16 => %93.75 olur.

### AMAT Sorusu

- L1 cache hit alırsa 5 saat sinyalinde cevap dönüyor, hit oranı da %80.
- L2 cache hit alırsa 15 saat sinyalinde cevap dönüyor, hit oranı da %95.
- L3 verilmemiş, RAM bize 200 saat sinyalinde cevap dönüyor.

        + En kolayı tersten gitmektir.
        + AMAT_L2 = 15 + (0.05 x 200) = 25 saat sinyali
        + AMAT_L1 = 5 + (0.2 x 25) = 10 saat sinyali

### AMAT Sorusu 2

- Ortalama Bellek Erişim Süresi (AMAT) = hit_time + (miss_ratio \* miss_penalty) olarak veriliyor. Buna göre aşağıdaki sistemin AMAT değeri sistemde L2 olup olmaması durumlarında nedir?
- L1 cache hit_time = 5 cycles, hit ratio = %90
- L2 cache hit_time = 12 cycles, hit ratio = %95
- Main memory access time 70 cycles.

          - Cevap:
          AMAT_L1 = 5 + (0.1 * 70) : L2 YOKSA,
          AMAT_L1 = 5 + (0.1 * [12 + (0.05 * 70)]) : L2 VARSA

          NOT: L2 hesabı => [12 + (0.05 * 70)]
              - 12 => L2 hit_time
              - 0.05 => L2 miss_ratio
              - 70 => main memory access_time

### Tag | Set Index | Offset Sorusu

- 32 bitlik adresler kullanan bir sistemde, 32KB’lık bir 4-way set associative cache’de bloklarda 64 byte yan yana tutuluyor. Tag, Set Index ve Offset kaçtır?

        + Set Adeti kaçtır?
        + Set Adeti = 32 * 1024 byte / 64 byte yan yana / 4-way set
        + Set Adeti = 128 set var.
        + Set Index nedir peki?
        + Set Index => 2^n = 128 => n = 7'dir.

        + Offset bitleri ne kadardır?
        + Offset => 2^n = 64 byte => n = 6 bittir.

        Sonuçta Tag Bitleri => 32 - 7 - 6 = 19 bittir.

### Dönüş Gecikmesi Sorusu

- 7200 RPM bir diskte kafanın biz ize ulaşması 4 milisaniye, bir sektörde 4KB, bir izde 1024 sektör olan bir diskin bağlı olduğu bus 500MB/sn'dir.

        a) Ortalama dönüş gecikmesi nedir?
            - Cevap:
            - 60sn/7200 = 8.33msn (0.00833 sn) -> yarısı = 4.17msn

        b) Bir dosyanın ilk sektörüne ulaşmak en az, en çok ve ortalama ne kadar sürer?
            - Cevap:
            - En az => 4msn (direkt ulaşıyor)
            - Ortalama => 4 + 4.17 = 8.17msn (ort. dönüş geck. ekle)
            - En çok => 4 + 8.33 = 12.33msn (dönüş geck. ekle)

        c) 1GB bir dosyanın peş peşe sektörlerde olduğu duurmda, diskin kaç iz okunması gerekir?
            - Cevap:
            - 1024 (sektör/iz) * 4 (KB/sektör) = 4 (MB/iz) var.
            - 1024MB / 4 (MB/iz) = 256 iz okuması gerekir.

        d) Aynı 1GB dosyanın, sisteme bir SSD disk takılsaydı, sadece bus hızına göre maksimum ne kadar sürede okunması gerekirdi?
            - Cevap:
            - 1024MB / 500 (MB/sn) = 2.05sn
