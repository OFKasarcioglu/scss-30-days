## **Gün 2: SCSS Değişkenleri Nedir ve Nasıl Kullanılır?**

**Hedefimiz:**  
1. **Değişkenlerin mantığını anlamak**  
2. **SCSS'te değişken tanımlamayı öğrenmek**  
3. **Değişkenlerle yazımı daha kolay hale getirmek**  

---

**📌 Değişkenler Nedir?**  
SCSS’te değişkenler, tekrarlayan değerleri bir defa tanımlayarak her yerde kullanmamıza olanak sağlar. Bu, özellikle renkler, font boyutları ve genişlik/uzunluk gibi sürekli kullandığımız değerler için çok işe yarar.

---

**📌 Değişken Tanımlama:**  
Değişkenler `$` işaretiyle tanımlanır:  
```scss
$ana-renk: #3498db;  
$font-boyutu: 16px;  
$margin: 10px;
```

Artık bu değişkenleri istediğimiz her yerde kullanabiliriz:  
```scss
body {
  color: $ana-renk;
  font-size: $font-boyutu;
  margin: $margin;
}
```

Eğer bir gün `$ana-renk` değişirse, sadece değişkeni güncelleriz ve tüm kodlar otomatik olarak bu yeni rengi kullanır.

---

**📌 Neden Değişken Kullanmalıyım?**  

1. **Kodunuzu Daha Kolay Yönetmek:** Eğer projenizde bir ana renk, bir vurgu rengi ve birkaç font boyutu varsa, tüm bu değerleri değişkenlerle tanımlayabilirsiniz.  
2. **Hata Yapma Riskini Azaltmak:** Renk kodlarını tekrar tekrar yazmak yerine, bir değişken kullanarak yanlış renk kodu yazma ihtimalini ortadan kaldırırsınız.  
3. **Daha Kolay Güncellemeler:** Bir projede renk paletini değiştirmek istiyorsanız, değişkenleri düzenlemeniz yeterlidir.

---

**📌 Renk Paleti Örneği:**  
```scss
// Renk değişkenleri
$ana-renk: #3498db;  
$vurgu-renk: #e74c3c;  
$arka-plan-renk: #ecf0f1;

// Yazı boyutları
$ana-font-boyutu: 16px;  
$baslik-font-boyutu: 24px;

// Kenar boşlukları
$ana-margin: 10px;
```

Bu değişkenleri istediğiniz yerde kullanabilirsiniz:  
```scss
h1 {
  color: $vurgu-renk;
  font-size: $baslik-font-boyutu;
}

p {
  color: $ana-renk;
  margin-bottom: $ana-margin;
}
```

---

**Ödev:**  

1. **Renk Paleti:**  
   - Ana renk, vurgu renk, arka plan rengi için 3 farklı değişken tanımlayın.  
2. **Font Boyutları:**  
   - Ana metin ve başlıklar için farklı yazı boyutları tanımlayın.  
3. **Stiller:**  
   - Bu değişkenleri kullanarak bir `h1`, `h2`, ve `p` için basit stiller oluşturun.  
---

