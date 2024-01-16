### A

    Eğer görüntü içinde periyodik olarak değişen şekiller var ise
    (örneğin çubuk şeklinde) görüntü periyodik bir gürültünün etkisinde
    kalmıştır. Periyodik gürültüler genellikle elektriksel ya da
    elektromekanik sebeplerden oluşurlar.
    Periyodik gürültü frekans ile alakalıdır. Bu yüzden frekans uzayı
    filtreleri ile temizlenebilir. Periyodik gürültü için en iyi frekans
    uzayı filtresi çentik filtredir. Çünkü çentik filtre periyodik gürültü
    için geliştirilmiş bir filtredir ve spektrum resimdeki merkezden uzak
    pikleri (periyodik gürültü DC değerini) yok etmemizi sağlar.

#### B

    clear all; clc; close all;
    a = imread('cameraman.tif');
    b = imnoise(a, 'salt & pepper', 0.15);
    c = medfilt2(b);
    figure, imshow(a);
    figure, imshow(b);
    figure, imshow(c);
