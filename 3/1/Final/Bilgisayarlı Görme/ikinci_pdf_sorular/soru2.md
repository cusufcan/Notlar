### A

    clear all; clc; close all;
    A = imread('manzara.jpg');
    R = A(:, :, 1);
    G = A(:, :, 2);
    B = A(:, :, 3);
    son = cat(3, B, G, R);
    figure, imshow(son);

### B

    clear all; clc; close all;
    A = imreaed('manzara.jpg');
    GrayImage = rgb2gray(A);
    R = GrayImage;
    G = GrayImage;
    B = GrayImage;
    for i = 1 : 64
        for j = 1 : 64
            if GrayImage(i, j) > 100 and GrayImage(i, j) < 150
                R(i, j) = 0;
                G(i, j) = 0;
                B(i, j) = 255;
            end
        end
    end
    son = cat(3, R, G, B);
    figure, imshow(son);

### C

    clear all; clc; close all;
    A = imread('manzara.jpg');
    imshow(A);
    R = A(:, :, 1);
    G = A(:, :, 2);
    B = A(:, :, 3);
    R = R + 50;
    G = G + 50;
    B = B - 75;
    son = cat(3, R, G, B);
    figure, imshow(son);
