# Merge Sort

## Proje 2 - [16,21,11,8,12,22] -> Merge Sort ve Big-O Gösterimi

Dizide bulunan elemanların her birini ayrı bir dizi ve tek eleman kalana kadar böl ve sıralayarak birleştir.

1. Verilen dizi 2 ye bölünerek **[16,21,11]** ve **[8,12,22]** olacak şekilde 2 dizi elde edilir.
2. Elde edilen diziler de sırayla ikiye bölünür, önce ilk elde ettiğimiz dizi bölünür. Yani; **[16]** ve **[21,11]** olarak 2 yeni dizi daha elde ederiz.
3. **[21,11]** dizisi de bölünerek **[21]** ve **[11]** dizileri oluşturulur.
4. Elde edilen ilk dizideki bütün elemanlar tek kalana bölme işlemi bitince ikinci diziye geçilir ve böylece **[8]** **[12,22]** dizileri elde edilir.
5. **[12,22]** dizisi de bölünerek **[12]** ve **[22]** dizileri oluşturulur.  
`Bölmeler sonucunda elimizde; [16],[21],[11],[8],[12],[22] dizileri olur.`
> İlk bölme gerçekleştikten sonra elde edilen 2 dizi sol ve sağ olarak ayrılır bu sebeple önce sol sonra sağ tarafı tek eleman kalana kadar böleriz ve birleştirirken aynı hiyerarşi takip edilir. Önce sol sonra sağ birleştilir ve en sonunda 2 dizi birleştirilerek sıralanmış şekilde tek dizi elde edilir.
6. Şimdi sırayla soldan başlayarak sıralama işlemi yapılarak birleştirme işlemi başlar. Sol taraf için önce 11 ile 21 elemanı karşılaştırılarak **[11,21]** dizisi oluşturulur.
7. '16' elemanı da sırayla 11 ve 21 ile karşılaştırılarak diziye eklenir ve **[11,16,21]** dizisi oluşturulur.
8. Sağ taraf birleştirilmeye başlar ve 8 ile 12 elemanı karşılaştırılır ve **[8,12]** dizisi oluşturulur.
9. '22' elemanı da sırayla 8 ve 12 elemanları ile karşılaştırılarak diziye eklenir ve **[8,12,22]** dizisi oluşturulur.
10. **[11,16,21]** ve **[8,12,22]** dizilerinin elemanları son birleştirme için karşılaştırılır.
- 11 > 8 = **[8]**
- 11 < 12 = **[8,11]** 
- 16 > 12 = **[8,11,12]**
- 16 < 22 = **[8,11,12,16]**
- 21 < 22 = **[8,11,12,16,21]**
- Son eleman 22 de eklenir ve **[8,11,12,16,21,22]** dizisini elde ederiz.

### Merge Sort her durumda bölme ve birleştirme işlemini yaptığından dolayı her zaman **O(n log n)** çalışır.