### A

        clear all; clc; close all;
        A = imread('manzara.tif);
        imshow(A);
        H = [0.25 0.50 0.25; 0.50 1.00 0.50; 0.25 0.50 0.25] / 4;
        B = uint8(filter2(H, A));
        figure, imshow(B);

        Ortalama filtredir. Gürültüyü temizlerken kenar bölgelerinin
        bulanıklaşmasına sebep olur. Komşu piksellerin ağırlıkları farklıdır.
        Bu yüzden ağırlıklı ortalama olarak isimlendirilir.

### B

        clear all; clc; close all;
        A = imread('manzara.tif);
        imshow(A);
        H = [1 1 1; 1 1 1; 1 1 1] / 9;
        B = uint8(filter2(H, A));
        figure, imshow(B);

        Ortalama filtredir. Gürültüyü temizlerken kenar bölgelerinin
        bulanıklaşmasına sebep olur. Komşu piksellerin ağırlıkları aynıdır.

### C

        clear all; clc; close all;
        A = imread('manzara.tif');
        imshow(A);
        H = [-1 -1 -1; -1 8 -1; -1 -1 -1];
        B = uint8(fliter2(H, A));
        figure, imshow(B);

        Laplasyon filtredir. Gürültülü piksellerde ve kenar bölgelerinde
        tepki verir. Diğer bölgelerin karanlık olmasına sebep olur. Filtre
        değerlerinin toplamı sıfır olduğu için ortalaması alınmaz.

### D

        clear all; clc; close all;
        A = imread('manzara.tif');
        imshow(A);
        H = [-1 -2 -1; 0 0 0; 1 2 1];
        B = uint8(filter2(H, A));
        figure, imshow(B);

        Laplasyon filtre ile benzer özellikler gösterir. Ancak sadece yatay
        kenarlara tepki verecek şekilde tasarlanmıştır. Filtre ile elde
        edilen matris orijinal görüntüye eklendiğinde kenarlardaki
        bulanıklaşmayı giderir.
