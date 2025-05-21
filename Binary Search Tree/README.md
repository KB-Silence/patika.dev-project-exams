# Binary Search Tree

## Proje 3 - [7,5,1,8,3,6,0,9,4,2] dizisinin Binary-Search-Tree aşamalarını yazınız.

- Verilen diziye göre Root = '7' elemanıdır. BST yapısında ekstra bir durum belirtilmediyse ilk indexteki eleman root olarak kabul edilir.
- BST yapısında hiyerarşik olarak her düğüm sol ve sağ olmak üzere sadece 2'ye ayrılabilir ve kök değerden küçük değer sola, büyük değer sağa eklenir.
- Dizi aksi belirtilmedikçe soldan sağa doğru işlenir ve ilk gelen sayı kök değer olur diğer sayılar sırayla karşılaştırılarak ağaca eklenir. Buna göre;

1. Kök değer 7'dir. Yani ağacımızın başlangıç noktası 7'dir.
2. Birinci indexteki eleman kök değerden küçük olduğundan dolayı '5' elemanı kök değerin soluna yerleştirilir.  
```
      7
     / 
    5   
```
3. İkinci indexteki eleman kök değerden küçük olduğundan dolayı soldan devam eder ve '5' elemanı ile karşılaştırmaya girer, 5'ten küçük değer olduğu için 5'in soluna yerleştirilir.
```
      7
     / 
    5   
   /
  1 
```
4. Üçüncü indexteki '8' elemanı kök değerden büyük olduğundan dolayı ağacın sağ tarafa eklenir.
```
      7
     / \
    5   8
   /     
  1   
```
5. Dördüncü indexteki '3' elemanı kök değerden küçük olduğundan dolayı sol taraftan karşılaştırmaya devam eder. 5'ten küçük olduğu için soldan devam eder ve 1'den büyük olduğu için, 1'in sağına eklenir.
```
      7
     / \
    5   8
   /     
  1       
   \
    3
```
6. Beşinci indexteki '6' elemanı kök değerden küçük olduğundan dolayı sol taraftan karşılaştırmaya devam eder. 5'ten büyük olduğu için, 5'in sağına eklenir.
```
      7
     / \
    5   8
   / \    
  1   6    
   \
    3
```
7. Altıncı indexteki '0' elemanı kök değerden küçük olduğundan dolayı soldan devam eder. 5'ten küçük olduğu için soldan ilerler ve 1'den de küçük olduğu için, 1'in soluna eklenir.
```
      7
     / \
    5   8
   / \    
  1   6     
 / \
0   3
```
8. Yedinci indexteki '9' elemanı kök değerden büyük olduğundan dolayı sağdan devam eder. 8'den de büyük olduğu için, 8'in sağına eklenir.
```
      7
     / \
    5   8
   / \   \
  1   6   9
 / \
0   3
```
9. Sekizinci indexteki '4' elemanı kök değerden küçük olduğundan dolayı soldan devam eder. 5'ten küçük olduğu için solu takip eder ve 1'den büyük olduğu için sağ taraftan devam ederek 3'ten büyük olması sebebiyle 3'ün sağına eklenir.
```
      7
     / \
    5   8
   / \   \
  1   6   9
 / \
0   3
     \
      4
```
10. Dokuzuncu indexteki '2' elemanı kök değerden küçük olduğundan dolayı soldan devam eder. 5'ten küçük olduğu için solu takip eder ve 1'den büyük olduğu için sağ taraftan devam eder. 3'ten küçük olması sebebiyle 3'ün soluna eklenir.
```
      7
     / \
    5   8
   / \   \
  1   6   9
 / \
0   3
   / \
  2   4
```

Böylelike ağacımızın yapısı yukardaki gibi olur.

### Görselleştirme ve açıklamadan özetlemek gerekirse;
- Root 7'dir.
- 5, 7'nin soluna eklenir.
- 1, 5'in soluna eklenir.
- 8, 7'nin sağına eklenir.
- 3, 1'in sağına eklenir.
- 6, 5'in sağına eklenir.
- 0, 1'in soluna eklenir.
- 9, 8'in sağına eklenir.
- 4, 3'ün sağına eklenir.
- 2, 3'ün soluna eklenir.