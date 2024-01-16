### A

    clear all; clc; close all;
    cm = imread('kiktap.jpg');
    imshow(cm);
    cf = fftshift(fft2(cm));
    [x, y] = meshgrid(-64:63, -64:63);
    z = sqrt(x.^2 + y.^2);
    c = (z < 30);
    cf1 = cf.*c;
    s = ifft2(cf1);
    figure, imshow(mat2gray(1 + abs(s)));

### B

    clear all; clc; close all;
    a = imread('cameraman.tif');
    [x, y] = meshgrid(1:256, 1:256);
    p = 5 + sin(x / 1.8 + y / 1.2);
    tp = (((double(a) / 128) + b) / 8);
    figure, imshow(tp);
    af = fftshift(fft2(tp));
    figure, imshow(mat2gray(log10(1 + abs(af))));
    af(95:98, :) = 0;
    af(163:165, :) = 0;
    af(:, 105:108) = 0;
    af(:, 150:153) = 0;
    figure, imshow(mat2gray(log10(1 + abs(af))));
    b = ifft2(af);
    figure, imshow(mat2gray(1 + abs(b)));
