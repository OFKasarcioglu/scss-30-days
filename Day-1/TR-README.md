## **Gün 1: SCSS Nedir ve Neden Kullanılır?**

**SCSS Nedir?**  
SCSS, CSS’in daha gelişmiş bir versiyonu gibidir. CSS’te genellikle aynı kodu tekrar etmek zorunda kalırsınız. Örneğin:

```css
body {
  font-size: 16px;
  color: black;
}

.header {
  font-size: 16px;
  color: black;
}
```

Aynı renk ve yazı boyutunu her yerde yazmanız gerekir. SCSS, bu tür işleri çok daha kolay hale getirir. Örneğin:

```scss
$renk: black;
$font-boyutu: 16px;

body {
  font-size: $font-boyutu;
  color: $renk;
}

.header {
  font-size: $font-boyutu;
  color: $renk;
}
```

Bir gün rengi değiştirmek isterseniz, yalnızca `$renk` değişkenini güncellersiniz ve tüm kodlarınız otomatik olarak yeni rengi kullanır.

**Neden SCSS Kullanmalıyım?**

**Kolaylık:** Renkleri ve yazı boyutlarını değişkenlerle yönetebilirsiniz.  
**Düzen:** Kodunuzu daha düzgün ve yapısal hale getirebilirsiniz.  
**Verimlilik:** Aynı kodu tekrar tekrar yazmaktan kurtulabilirsiniz.  
**Modülerlik:** Kodunuzu daha küçük, yeniden kullanılabilir parçalara bölebilirsiniz.

**SCSS Nasıl Kullanılır?**

1. **SCSS’i çalıştırmak için bir programa ihtiyacınız olacak.**  
   - Node.js’i indirin ve bilgisayarınıza kurun.  
2. **Node.js’i kurduktan sonra komut satırını açın ve şunu çalıştırın:**

```bash
npm install -g sass
```

3. **Bir `.scss` dosyası oluşturun.** Örneğin:

```scss
$renk: blue;

body {
  background-color: $renk;
}
```

4. **SCSS’i çalıştırın ve bir CSS dosyasına dönüştürün:**

```bash
sass input.scss output.css
```

5. **Artık `output.css` dosyasını tarayıcınızda kullanabilirsiniz!**

**SCSS ile Daha Neler Yapılabilir?**

**İç İçe Yazım:** Kodları başka kodların içine yerleştirebilirsiniz.

```scss
.header {
  h1 {
    color: blue;
  }
}
```

Bu kod, `.header h1 { color: blue; }` haline gelir.

**Mixins:** Sıkça kullandığınız kod parçalarını şablon olarak kaydedebilir ve istediğiniz yerde yeniden kullanabilirsiniz.

```scss
@mixin ortala {
  display: flex;
  justify-content: center;
  align-items: center;
}

.kutu {
  @include ortala;
  height: 100px;
  width: 100px;
  background-color: red;
}
```

**Matematik:** Renkleri karıştırabilir, boyutları çarparak veya ekleyerek ayarlayabilirsiniz.

```scss
$temel-renk: #333;
$ikinci-renk: lighten($temel-renk, 20%);
```

SCSS, CSS yazmayı daha düzenli ve eğlenceli hale getirir. Tek yapmanız gereken bir SCSS dosyası yazıp, bunu bir CSS dosyasına derlemektir. Geri kalan her şey, renkler, fontlar, düzen, hepsi çok daha kolay olacaktır. 😊
