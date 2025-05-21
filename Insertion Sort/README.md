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

#


## Big-O Gösterimi ve Time Complexity Case'leri 
- **Worst Case:     O(n²)**
- **Best Case:      O(n)**
- **Avarage Case:   O(n²)**

- [2,6,16,18,22,27] dizisine göre '18' elemanı 3. indiste yer alır yani ortada. Bu sebeple, **Avarage Case - O(n²)** kapsamına girer.

# Selection Sort
### **[7,3,5,8,2,9,4,15,6]** dizisinin Selection Sort'a göre ilk 4 adımını yazınız.


1 - İlk indiste yer alan eleman en düşük değer olarak belirlenip diğer elemanlar ile kontrole girerek dizideki asıl en küçük değer bulunacak. Buna göre; 7 > 3 sorgusunda en küçük değer 3 olacak. 3 < 5, 3 < 8 kontrollerinden sonra 3 > 2 sorgusunda en küçük değer 2 olacak ve diğer sorgularda sonuç değişmeyeceği için ilk indisteki eleman ile yer değişterecek ve güncel array **[2,3,5,8,7,9,4,15,6]** olacak.

2 - İlk aşamadan sonra 0. indiste bulunan eleman kontrol dışında tutulacak. Böylece 1. indiste bulunan '3' elemanı minimum değer varsayılıp sağa doğru kontrole girecek, buna göre hiç dizide devam eden hiç bir eleman 3'ten küçük olmayacağı için hiç bir yer değişimi olmayacak ve array olduğu gibi kalacak. **[2,3,5,8,7,9,4,15,6]**

3 - İkinci aşamadan sona 0. ve 1. indiste bulunan elemanlar kontrol dışında tutulacak. Böylece 2. indiste bulunan '5' elemanı minimum değer varsayılıp sağa doğru kontrole girecek, buna göre 5 < 8, 5 < 7, 5 < 9 kontrollerinden sonra 5 > 4 kontrolü gerçekleşecek ve minimum değer 4 olarak belirlenecek. Devam eden kontrollerde sonuç değişmeyeceği için '4' elemanı ile '5' elemanı yer değişterecek ve güncel array **[2,3,4,8,7,9,5,15,6]** olacak.

4 - Üçüncü aşamadan sonra 0.-1.-2. indisleri kontrol dışında kalarak başlangıçta minimum değer '8' elemanı olacak ve devam eden elemanlar ile kontrol sonucunda minimum değer önce '7' sonrasında '5' olacak ve '5' elemanı ile '8' elemanı yer değiştirerek güncel array **[2,3,4,5,7,9,8,15,6]** olacak.

Selection Sort'un ilk 4 aşaması bu şekilde olup bütün liste sıralanana kadar tekrar edecek. Açıklamalar olmadan aşamaları yazmak gerekirse;

- **[7,3,5,8,2,9,4,15,6]** ---> **[2,3,5,8,7,9,4,15,6]**
- **[2,3,5,8,7,9,4,15,6]** ---> **[2,3,5,8,7,9,4,15,6]**
- **[2,3,5,8,7,9,4,15,6]** ---> **[2,3,4,8,7,9,5,15,6]**
- **[2,3,4,8,7,9,5,15,6]** ---> **[2,3,4,5,7,9,8,15,6]**