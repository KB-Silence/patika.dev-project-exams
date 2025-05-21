# Insertion Sort Projesi

## Proje 1 - [22, 27, 16, 2, 18, 6] -> Insertion Sort

Yukarıda verilen dizinin sort türüne göre aşamaları;

1 - **[22,27,16,2,18,6]** -> 22 < 27 olduğu için 3.elemana geçilir (2.indis). 27 > 16 kontrolü yapar, 27 den küçük olduğundan dolayı bir solundaki eleman ile de kontrol yapılır 22 > 16 olduğu için 2.indisteki '16' elemanı 0. indiste yer alır ve güncel array **[16,22,27,2,18,6]** olur.

2 - 3.indisteki elemandan sola doğru kontrol etmeye başlar. 2 < 27, bir soldakini de kontrol eder 2 < 22, bir soldakini de kontrol eder 2 < 16 ve 3.indisteki '2' elemanı böylelikle array'in en başına 0. indise yerleşir ve güncel array **[2,16,22,27,18,6]** olur.

3 - 4.indisteki elemandan sola doğru kontrol etmeye başlar. 18 < 27, soldan bir sonraki indisi kontrol eder, 18 < 22, soldan bir sonraki indisi kontrol eder, 18 > 16 olacağından dolayı araya girerek 2. indise yerleşir ve güncel array **[2,16,18,22,27,6]** olur.

4 - Son indisi(5.indis) kontrol etmeye başlar, 6 < 27 olduğundan bir soldaki elemana gider, 6 < 22 olur ve bir soldakini kontrol eder 6 < 18 olur ve bir soldakinden devam eder, 6 < 16 olur ve ilk indise geldiğince 6 > 2 olacağından araya girerek 1. indise yerleşir ve arrayin son hali **[2,6,16,18,22,27]** olur.

### Açıklamalar olmadan yazarsak;
- [22,27,16,2,18,6] ---> [16,22,27,2,18,6]
- [16,22,27,2,18,6] ---> [2,16,22,27,18,6]
- [2,16,22,27,18,6] ---> [2,16,18,22,27,6]
- [2,16,18,22,27,6] ---> [2,6,16,18,22,27]

