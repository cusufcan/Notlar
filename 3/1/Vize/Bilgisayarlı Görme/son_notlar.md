### Saat Yonunun Tersine Cevirme

    clear all; clc; close all;
    A=imread('cameraman.tif');
    imshow(A);
    for i=1:256
        for j=1:256
            B(j,i)=A(i,j);
        end
    end
    figure,imshow(B);

### Kirpma Uygulamasi (ROI)

    clear all; clc; close all;
    A=imread('cameraman.tif');
    imshow(A);
    n1=35;n2=95;
    m1=50;m2=40;
    for i=1:m1
        for j=1:m2
            B(i,j) = A(i+n1,j+n2);
        end
    end
    figure,imshow(B);

### Parlaklik Ayari

    clear all; clc; close all;
    A=imread('cameraman.tif');
    imshow(A);
    B=A+50;
    C=A-50;
    figure,imshow(B);
    figure,imshow(C);

### Oteleme

    clear all; clc; close all;
    A=imread('cameraman.tif');
    imshow(A);
    n1=50;n2=70;
    for i=n1:256+n1-1
        for j=n2:256+n2-1
            B(i,j)=A(i-n1+1,j-n2+1);
        end
    end
    figure,imshow(B);

### Boyut Degistirme (Buyutme)

    clear all; clc; close all;
    A=imread('cameraman.tif');
    imshow(A);
    for i=1:512
        for j=1:512
            B(i,j)=A(ceil(i/2),ceil(j/2));
        end
    end
    figure,imshow(B);

### Boyut Degistirme (Kucultme)

    clear all; clc; close all;
    A=imread('cameraman.tif');
    imshow(A);
    for i=1:128
        for j=1:128
            B(i,j)=A(i*2,j*2);
        end
    end
    figure,imshow(B);

### Boyut Degistirme (imresize)

    clear all; clc; close all;
    A=imread('cameraman.tif');
    imshow(A);
    B=imresize(A,1.95,'bicubic');
    figure,imshow(B);

### Kontrast Ayari

    clear all; clc; close all;
    A=imread('cameraman.tif');
    imshow(A);
    B=A*2.5;
    figure,imshow(B);

### Log Fonk İle Karsitlik Ayari

    clear all; clc; close all;
    A=imread('cameraman.tif');
    imshow(A);
    B=uint8(100*log10(double(A+1)));
    figure,imshow(B);

### Ussel Fonk Ile Karsitlik Ayari

    clear all; clc; close all;
    A=imread('cameraman.tif');
    imshow(A);
    B=uint8(1.3*(double(A).^0.8));
    figure,imshow(B);

### Esikleme

    clear all; clc; close all;
    A=imread('cameraman.tif');
    imshow(A);
    for i=1:256
        for j=1:256
            if A(i,j)<=40
                B(i,j)=0;
            else
                B(i,j)=255;
            end
        end
    end
    figure,imshow(B);

### Negatif Olusturma

    clear all; clc; close all;
    A=imread('cameraman.tif');
    imshow(A);
    for i=1:256
        for j=1:256
        B(i,j)=255-A(i,j);
        end
    end
    figure,imshow((B));

### Histogram Olusturma

    clear all; clc; close all;
    A=imread('cameraman.tif');
    imshow(A);
    B=imhist(A);
    figure,plot(B);

### Histogram Cikarma

    clear all; clc; close all;
    A=imread('cameraman.tif');
    imshow(A);
    figure;imhist(A);
    %figure,imshow((B));

### Tuz Biber Gurultusu Ekleme

    clear all; clc; close all;
    a=imread('cameraman.tif');
    imshow(a);
    b=imnoise(a,'salt & pepper');
    figure,imshow(b);
    c=imnoise(a,'salt & pepper',0.1);
    figure,imshow(c);

### Tuz Biber Gurultusu Ekleme

    clear all; clc; close all;
    a=imread('cameraman.tif');
    imshow(a);
    b=imnoise(a,'salt & pepper');
    figure,imshow(b);
    c=medfilt2(b);
    figure,imshow(c);
