# Vize Örnek Sorular

### 1. Anabelleklerin yavaş çalışmasının ardındaki nedenler nelerdir?

    - İçindeki sütun seçme işlemi yavaştır.
    - Zamanının yüzde beşinde bilgilerini tazelemeyle uğramaktadır.

### Önbelleklerin yapı ve amaçları için aşağıdakilerden doğru olanları işaretleyiniz.

    - İnternet önbelleği olarak çalışan firmalar vardır.
    - Ortalama bellek erişim süresinde düşük miss oranı olumlu etkilidir.
    - L2 önbelleği L3'ten küçük ve hızlıdır.
    - L3 önbellek sonradan kullanılmıştır, çok çekirdekli yapılarda gereklidir.

### 3. Intel I7 yapısından tanıdığımız çekirdekler arası ortak kullanılan önbellek seviyesi nedir?

    - L3 cache

### 4. 3 boyutlu SSD disklerin esas getirisi nedir?

    - Fiziksel hareket olmaması

### 5. 7200 RPM bir diskte kafanın biz ize ulaşması 4 milisaniye, bir sektörde 4KB, bir izde 1024 sektör olan bir diskin bağlı olduğu bus 500MB/sn'dir.

    a) Ortalama dönüş gecikmesi nedir?
        - Cevap:
        - 60sn/7200 = 8.33msn -> yarısı = 4.17msn
    b) Bir dosyanın ilk sektörüne ulaşmak en az, en çok ve ortalama ne kadar sürer?
        - Cevap:
        - En az => 4msn,
        - En çok => 4 + 8.33 = 12.33msn
        - Ortalama => 4 + 4.17 = 8.17msn
    c) 1GB bir dosyanın peş peşe sektörlerde olduğu duurmda, diskin kaç iz okunması gerekir?
        - Cevap:
        - 1024 (sektör/iz) * 4 (KB/sektör) = 4 (MB/iz) var.
        - 1024MB / 4 (MB/iz) = 256 iz
    d) Aynı 1GB dosyanın, sisteme bir SSD disk takılsaydı, sadece bus hızına göre maksimum ne kadar sürede okunması gerekirdi?
        - Cevap:
        - 1024MB / 500 (MB/sn) = 2.05sn

### 6. Ortalama Bellek Erişim Süresi (AMAT) = hit_time + (miss_ratio \* miss_penalty) olarak veriliyor. Buna göre aşağıdaki sistemin AMAT değeri sistemde L2 olup olmaması durumlarında nedir?

    - L1 cache hit_time = 5 cycles, hit ratio = %90
    - L2 cache hit_time = 12 cycles, hit ratio = %95
    - Main memory access time 70 cycles.

    - Cevap:
    - = 1 + (5 + (0.1 * 70)) : L2 YOKSA,
    - = 1 + (5 + (0.1 * [12 + (0.05 * 70)])) : L2 VARSA

    NOT: L2 hesabı => [12 + (0.05 * 70)]
        - 12 => L2 hit_time
        - 0.05 => L2 miss_ratio
        - 70 => main memory access_time
