# 5. Soru

### cameraman.tif isimli görüntü üzerinde aşağıda verilen işlemleri gerçekleştirmek için gerekli programları yazınız. (görüntü boyutu 256x256 kabul edilecek)

### a- Görüntü boyutlarını (512x512) yapan programı yazınız.

    clear all;clc;close all;
    a=imread('Cameraman.tif');
    b=imresize(a,2);
    imshow(a)
    figure,imshow(b)

### b-f(50,50)’inci pikselden itibaren 100x100 piksel boyutlarındaki kısmını keserek ekrana basınız. (kırpma işlemi)

    clear all;clc;close all;
    a=imread('Cameraman.tif');
    for i=50:149
    for j=50:149
    b(i-49,j-49)=a(i,j);
    end
    end
    imshow(a)
    figure,imshow(b)

### c- görüntünün negatifini alan programı yazınız.

    clear all;clc;close all;
    a=imread('Cameraman.tif');
    b=255-a;
    imshow(a)
    figure,imshow(b)

### d- görüntüyü 3x3 ortalama filtre ile filtreleyen programı yazınız.

    clear all;clc;close all;
    a=imread('Cameraman.tif');
    h = fspecial('average',3);
    b=imfilter(a,h);
    imshow(a)
    figure,imshow(b)

### e- görüntüyü 3x3 medyan filtre ile filtreleyen programı yazınız.

    clear all;clc;close all;
    a=imread('Cameraman.tif');
    b = medfilt2(a);
    imshow(a)
    figure,imshow(b)
