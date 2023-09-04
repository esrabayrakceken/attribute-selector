# attribute-selector
## Another variant of Css selector is attribute selector(Css selectorun başka bir çeşidi özellik seçici)
- Belirli bir özniteliğe dayalı olarak öğeleri seçer. (type)
---
```html
<label for="search">Search</label>
<input type="text" placeholder="search" id="search">
<input type="password" placeholder="password" id="password">
```
- password alanında girdiğim bilginin rengi ile oynayalım.
```css
input[type="password"]{
      color:greenyellow;
}
```
- Sadece password alanına girilecek input rengi değişir.
- __input[type="password"]:__ Türü password olan inputları selector olarak seçer.
- __color:greenyellow:__ Sadece password rengini yeşil-sarı ayarlar.
---
```css
input{
      color:greenyellow;
}
```
- Eğer bu şekilde kullansaydım koddaki tüm inputların rengi değişirdi.
- __input:__ Türe bakmaksızın tüm inputları selector olarak seçer.(text,password)
- __color:greenyellow:__ Tüm input renklerini yeşil-sarı ayarlar.
---
- class yapısını da bir tür varsayarak attribute olarak kullanabilriz.
```html
<section class="post">
            <span>Posted by <a href="#213adas">/u/not_funny</a></span>
            <h2>Lol look at this hilarious name <span class="tag">funny</span></h2>
            <button>+Vote</button>
            <hr>
</section>
```
```css
section[class="post"]{
       background-color:purple;
}
```
- __section[class="post"]:__ sınıfı post olan section etiketini selector olarak seçer.
- __background-color:purple:__ Seçilen section arka planını mor yapar.
---
- 2 farklı attribute selectordan daha bahsedelim.
```html
<footer>
        <nav>
            <ul>
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#contact">Contact</a></li>
                <li><a href="https://www.google.com">Google</a></li>
            </ul>
        </nav>
        <a href="#licence">Content is available under these licence</a>
</footer>
``` 
__1.__ Kod içerisinden sadece "google"a özel selector oluşturup stil verelim.(*= seçici)
```css
a[href*="google"]{
       color:pink;
}
```
- __a[href*="google"]:__ Etiketler içinde "google" kelimesini __içeren__ çapa etiketini selector olarak seçer.
- __color:pink:__ "Google" etiketinin rengini pembe yapar.

__2.__ Kod içerisinden sadece "google"a özel selector oluşturup stil verelim.($= seçici)
```css
a[href$=".com"]{
       font-style:italic;
}
```
- __a[href$=".com"]:__ Etiketler içinde ".com" ile __biten__ çapa etiketini selector olarak seçer.
- __font-style:italic:__ "Google" etiketinin stilini italic yapar.
- [Daha fazla attribute selector](https://developer.mozilla.org/en-US/docs/Web/CSS/Attribute_selectors "Bahsetmediğimiz diğer attribute çeşitleri için tık tık")

_İyi kodlamalar.._






  





