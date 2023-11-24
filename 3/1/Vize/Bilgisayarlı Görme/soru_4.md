# 4. Soru

### a. Ortalama (yumuşatma) filtre hakkında kısaca bilgi veriniz.

    - Ortalama filtreleri, filtre maskesi içine denk gelen piksel değerleri ile filtre değerlerinin birebir çarpımlarının
    toplamının ortalamasını alan filtrelerdir. Filtre içindeki değerler ortalamaya dahil edilecek piksel değerlerinin
    ağırlıklarını temsil eder.
    Ortalama filtreler görüntü içindeki gürültülerin temizlenmesi için kullanılır. Ancak gürültüleri temizlerken
    görüntü içinde kenar bölgelerde bulanıklaşmaya sebep olurlar. Özellikle filtre boyutu büyüdükçe gürültü
    daha iyi temizlenir bulanıklaşma da gittikçe artar.

### b. Tuz-Biber gürültüsünü en iyi hangi filtre ile temizleyebiliriz? Sebebini kısaca açıklayınız.

    -Tuz biber gürültüsünü en iyi medyan filtre temizler. Çünkü tuz biber gürültüsü görüntü içindeki rasgele
    seçilen piksel değerlerinin 0 yada 255 değerleri ile bozulması şeklinde meydana gelir. Ortalama alan filtreler
    bu değerlerinde ortalamayı etkilemesi sebebiyle iyi sonuç vermezler. Ancak medyan filtre ortanca değeri
    bularak filtreleme işlemini gerçekleştirdiği için bu değerlerin olumsuz etkisinden etkilenmez.
