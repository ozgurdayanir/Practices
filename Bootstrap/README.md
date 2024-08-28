# Bootstrap 5.3 Grid Sistemi (TR)

Bu belge, **Bootstrap 5.3** sürümünde kullanılan grid (ızgara) sistemini açıklamaktadır. Bootstrap grid sistemi, esnek bir yerleşim sistemi sunar ve sayfa düzenlerini hızlı bir şekilde oluşturmaya yardımcı olur.

## İçindekiler
1. [Grid Sistemi Nedir?](#grid-sistemi-nedir)
2. [Temel Yapı](#temel-yapı)
3. [Satırlar ve Sütunlar](#satırlar-ve-sütunlar)
4. [Kırılma Noktaları](#kırılma-noktaları)
5. [Diğer Örnekler](#diğer-örnekler)

## Grid Sistemi Nedir?
Bootstrap grid sistemi, sayfayı 12 eşit sütuna böler. Bu sütunlar, sayfa düzenini oluşturmak için satırlar içinde gruplanır. Grid sistemi, mobil cihazlardan büyük ekranlara kadar her cihazda esnek ve uyumlu yerleşim sağlar.

## Temel Yapı
Grid sistemi, üç ana öğeye dayanır:
- **Container (Kapsayıcı)**: İçeriği sarar ve sayfa genişliğini kontrol eder.
- **Row (Satır)**: Satırları temsil eder. Sütunlar bu satırların içine yerleştirilir.
- **Column (Sütun)**: İçeriği taşıyan ve ekran boyutuna göre hizalanan sütunlardır.

### Örnek:

Üç eşit sütun örneği

```html
<div class="container">
    <div class="row">
        <div class="col bg-success">
            1. Sütun
        </div>
        <div class="col bg-danger">
            2. Sütun
        </div>
        <div class="col bg-primary">
            3. Sütun
        </div>
    </div>
</div>
```

## Satırlar ve Sütunlar
**.row sınıfı** sütunları içinde barındıran satırı tanımlar.
**-.col sınıfı** bir sütunu temsil eder ve otomatik olarak eşit genişlikte dağıtılır.

Sütunlar, .col- ile başlayıp ardından bir sayı (1-12) eklenerek genişletilebilir.

### Örnek:

Farklı genişliğe sahip sütun örneği:

- Bu örnekte ```col-4``` class'ı tanımlanan sütun **4** kolonluk bir alan kaplar.
- ```col-8``` class'ı tanımlanan sütun **8** kolonluk alan kaplar.

*Sütunlara cihazlar için bir kırılma noktası tanımlanmadığı için her cihazda aynı alanı kaplar.*
```html
<div class="container">
  <div class="row">
    <div class="col-4 bg-success">
      4/12 Genişliğinde Sütun
    </div>
    <div class="col-8 bg-danger">
      8/12 Genişliğinde Sütun
    </div>
  </div>
</div>
```
## Kırılma Noktaları
Kırılma noktaları, farklı ekran boyutları için farklı düzenler tanımlamaya olanak tanır. Bootstrap, şu beş kırılma noktasını içerir:

- **.col-:** En küçük cihazlar (mobile phone) *(varsayılan)*
- **.col-sm-:** Küçük cihazlar(mobile phone) *(≥576px)*
- **.col-md-:** Orta cihazlar (tablet) *(≥768px)*
- **.col-lg-:** Orta - büyük cihazlar (notebook) *(≥992px)*
- **.col-xl-:** Büyük cihazlar (laptop) *(≥1200px)*
- **.col-xxl-:** En büyük cihazlar (large screens) *(≥1400px)*

### Örnek

- Bu örnekte 1. Sütun ```"col-md-6"``` class'ı almış ve herhangi bir ```-sm``` ve ```col-``` class'ı tanımlanmadığı için "md" ekran boyutuna gelene kadar **12** kolonluk bir alan kaplar. 
- Ardından "md" ekran boyutundan "lg" ekran boyutuna kadar ```"col-md-6"``` class'ı tanımlandığı için **6** kolonluk bir alan kaplar. 
- Aynı şekilde 2. Sütun da bu class'a sahip olduğu için **6** kolonluk alan kaplayarak ekranı ikiye bölen **2 sütun** elde edilir. 
- "Lg" ekran boyutuna ulaşıldığında 1. Sütunun ```"col-lg-4"``` class'ı bu sütunun **4** kolonluk bir alan kaplamasını sağlarken 2. Sütunun ```"col-lg-8"``` class'ı bu sütunun **8** kolon yer kaplamasını sağlar. Yani kapsayıcının **3'te 1'ini 1. Sütun kaplarken kalan 3'te 2'sini 2. Sütun kaplar.**

```html
<div class="container">
    <div class="row">
        <div class="col-md-6 col-lg-4 bg-success">
            1. Sütun
        </div>
        <div class="col-md-6 col-lg-8 bg-danger">
            2. Sütun
        </div>
    </div>
</div>
```
## Diğer Örnekler

*Örnekleri responsive olarak inceleyebilirsiniz.*

### Aynı kırılma noktasında eşit genişlikteki sütunlar

```html 
<!--md kırılma noktasında 3 eşit sütun örneği.
    md boyutuna gelene kadar 12 kolon alan kaplar ve alt alta gelirler.-->
<div class="container">
    <div class="row">
        <div class="col-md-4 bg-success">
            Sütun 1
        </div>
        <div class="col-md-4 bg-danger">
            Sütun 2
        </div>
        <div class="col-md-4 bg-primary">
            Sütun 3
        </div>
    </div>
</div>
```
---

### Farklı kırılma noktalarında eşit genişlikteki sütunlar
```html
<!--Oluşturulan her eşit sütun için:
    sm ve daha küçük ekranda 6 kolonluk alan kaplar
    md classı tanımlanmadığı için sm'dan lg'ye kadar 6 kolonluk alan kaplar.
    lg ekranlarda 3 kolonluk alan kaplar
    xl ekranlarda 2 kolonluk alan kaplar-->
<div class="container">
    <div class="row">
        <div class="col-sm-6 col-lg-3 col-xl-2 bg-primary">
            Column
        </div>
        <div class="col-sm-6 col-lg-3 col-xl-2 bg-primary">
            Column
        </div>
            <div class="col-sm-6 col-lg-3 col-xl-2 bg-primary">
            Column
        </div>
            <div class="col-sm-6 col-lg-3 col-xl-2 bg-primary">
            Column
            </div>
        <div class="col-sm-6 col-lg-3 col-xl-2 bg-primary">
            Column
        </div>
        <div class="col-sm-6 col-lg-3 col-xl-2 bg-primary">
            Column
        </div>
    </div>
</div>
```