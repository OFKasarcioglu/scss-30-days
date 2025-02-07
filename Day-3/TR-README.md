## **Gün 3: İç İçe Kurallar (Nesting) Nedir ve Nasıl Kullanılır?**

**Hedefimiz:**  
1. SCSS’te iç içe kuralların ne olduğunu öğrenmek  
2. İç içe kurallar kullanarak kodu daha düzenli hale getirmek  
3. Daha az tekrar ve daha temiz bir yapı oluşturmak  

---

**📌 İç İçe Kurallar Nedir?**  
CSS’te bir seçici, başka bir seçicinin içinde yer almaz. Her şeyi baştan yazmak gerekir. Örneğin:

```css
.header {
  background-color: blue;
}
.header h1 {
  color: white;
}
.header p {
  font-size: 16px;
}
```

Bu tür durumlarda, `.header` seçicisini sürekli tekrar etmek zorunda kalıyoruz. SCSS’te ise iç içe kurallar kullanarak bu yapıyı daha sade bir hale getirebiliriz.

---

**📌 SCSS’te İç İçe Kuralların Kullanımı:**  
SCSS’te iç içe kurallar şu şekilde yazılır:

```scss
.header {
  background-color: blue;

  h1 {
    color: white;
  }

  p {
    font-size: 16px;
  }
}
```

Bu kod, derlendiğinde şu hale gelir:

```css
.header {
  background-color: blue;
}
.header h1 {
  color: white;
}
.header p {
  font-size: 16px;
}
```

**Neden Daha İyi?**  
- Daha **temiz** bir görünüm: `.header` seçicisini her seferinde tekrar yazmaya gerek yok.  
- Daha **düzenli**: İç içe kurallar sayesinde hangi elementlerin hangi kapsayıcının içinde olduğunu hemen anlıyoruz.

---

**📌 Kombinasyon Seçicileri ve İç İçe Yazım:**  
SCSS’te sadece eleman seçicilerini değil, diğer kombinasyonları da iç içe yazabilirsiniz:

```scss
.header {
  background-color: blue;

  h1 {
    color: white;

    &:hover {
      color: gray;
    }
  }

  .button {
    background-color: red;

    &:active {
      background-color: darkred;
    }
  }
}
```

Bu, şu şekilde derlenir:

```css
.header {
  background-color: blue;
}
.header h1 {
  color: white;
}
.header h1:hover {
  color: gray;
}
.header .button {
  background-color: red;
}
.header .button:active {
  background-color: darkred;
}
```

---

**📌 Kullanım İpuçları:**  
- **Düzeyi abartmayın:** İç içe kuralların düzeyi çok derin olmamalı. Eğer çok fazla iç içe yapı kullanırsanız, kodunuzu okumak ve yönetmek zorlaşır.  
- **Kapsayıcılar:** Sadece gerçekten kapsayıcı bir yapıya sahipseniz iç içe kurallar kullanın.  
- **Hızlı düzenleme:** Bir düzenleme yapmak gerektiğinde tüm ilgili stilleri tek bir yerde görüp değiştirebilirsiniz.

---

**Ödev:**  
1. `.navbar` adında bir sınıf tanımlayın.  
   - `background-color` verin.  
   - `a` öğesi için bir `hover` rengi ekleyin.  
2. `.sidebar` adında bir sınıf tanımlayın.  
   - `ul` ve `li` stillerini iç içe yazın.  
3. Bu iç içe kuralları kullanarak kodu hem düzenli hem de okunaklı hale getirin.

---

SCSS’te iç içe kurallar, kodu daha sade ve düzenli tutmamıza yardımcı olur. **Hadi bu düzenlemeleri deneyelim!** 🚀
