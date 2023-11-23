# 03 - Ana Bellek Yapısı

### RAM Adres Dağıtımı:

- Örneğin bilgisayarınızda 8GB bellek olsun, 4GB+4GB = 8GB:
  2^3 (8 çevrimi) x 2^30 (gb çevrimi) -> (3 + 30) 33 bit adres uzayı.
- Her kartta 8 ön yüzde, 8 arka yüzde aynı boyda entegre vardır.
- O halde her biri 4GB/16 = 256 MB tutuyor. 256MB:
  2^8 (256 çevrimi) x 2^20 (mb çevrimi) -> (8 + 20) 28 bit adrestir.

### Adres şöyle dağıtılır:

- 0/1 (kart için 1 bit)
- 4 bit (entegre seçim için)
- 28 bit: 256MB için (ulaşılmak istenen byte için)

### SRAM / DRAM / ROM / EEPROM:

- SRAM (statik) durağan rastgele erişimli bir bellektir. (ön bellek)
- SDRAM ise dinamik rastgele erişimli bir bellektir. (ana bellek)
- ROM (Read Only Memory) yazılamaz bellektir, sadece okunur.
- EEPROM eletonik olarak yazılabilen, istemezsek silinmeyen bir bellektir.
  (BIOS belleği)

### Temel Bellek Donanım Yapısı:

- Belleğin MHz değeri kadar, CAS değeri de önemlidir.
- DDR 3 CAS 7-9nsn iyidir. DDR4'te 18nsn var.
- Intel-i7 için toplamda (L3'e sorma) 42 saat sinyali + (Bellek gecikmesi) 87nsn.
