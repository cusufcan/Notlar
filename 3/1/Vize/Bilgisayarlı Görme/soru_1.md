# 1. Soru

### Aşağıdaki 8x8 boyutunda ve 8 (23 −3 𝑏𝑖𝑡) seviyeli gri görüntüyü 3x3 boyutlarında verilen 2 filtre (aşağıda verilen) ile filtreleyerek filtrelenmiş görüntü değerlerini yandaki boş matrislere yazınız.

    [ 0 7 6 6 1 5 6 7 ]    *    [ 1 0 -1]    =    [ 0 0 7 7 1 0 0 7 ]
    [ 0 4 5 3 4 4 4 4 ]         [ 2 0 -2]         [ 0 0 2 6 0 0 0 7 ]
    [ 3 3 3 4 4 4 4 6 ]         [ 1 0 -1]         [ 0 1 5 0 0 0 0 7 ]
    [ 6 7 0 1 1 3 3 3 ]                           [ 0 7 7 0 0 0 0 7 ]
    [ 1 1 2 2 1 3 3 3 ]                           [ 0 5 5 1 0 0 1 7 ]
    [ 3 4 2 3 2 2 1 1 ]                           [ 0 3 6 1 1 0 1 5 ]
    [ 2 5 0 0 0 0 0 0 ]                           [ 0 7 7 0 1 1 2 2 ]
    [ 3 4 0 1 1 1 1 0 ]                           [ 0 7 7 0 1 0 1 1 ]

    - İlk hücrenin hesaplanması

    (0 * 0) + (-2 * 7) + (0 * 0) + (-1 * 4) = -18
    Taşma olduğu için sonuç 0 alınır. (3 bit için görüntü değerleri 0 ile 7 aralığında olabilir)

    - İkinci hücrenin hesaplanması

    (2 * 0) + (0 * 7) + (-2 * 6) + (1 * 0) + (0 * 4) + (-1 * 5) = -17
    Taşmadan dolayı 0

    - Üçüncü hücrenin hesaplanması

    (1 * 0) + (0 * 7) + (-1 * 6) + (2 * 0) + (0 * 4) + (-2 * 5) + (1 * 3) + (0 * 3) + (-1 * 3) = -16
    Taşmadan dolayı 0
