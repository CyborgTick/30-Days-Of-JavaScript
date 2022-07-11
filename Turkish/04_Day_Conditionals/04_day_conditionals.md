<div align="center">
  <h1> 30 Days Of JavaScript: Conditionals [ Koşullar ]</h1>
  <a class="header-badge" target="_blank" href="https://www.linkedin.com/in/asabeneh/">
  <img src="https://img.shields.io/badge/style--5eba00.svg?label=LinkedIn&logo=linkedin&style=social">
  </a>
  <a class="header-badge" target="_blank" href="https://twitter.com/Asabeneh">
  <img alt="Twitter Follow" src="https://img.shields.io/twitter/follow/asabeneh?style=social">
  </a>

  <sub>Author:
  <a href="https://www.linkedin.com/in/asabeneh/" target="_blank">Asabeneh Yetayeh</a><br>
  <small> January, 2020</small>
  </sub>
</div>

[<< Gün 3](../03_Day_Booleans_operators_date/03_booleans_operators_date.md) | [Gün 5 >>](../05_Day_Arrays/05_day_arrays.md)

![Thirty Days Of JavaScript](../../images/banners/day_1_4.png)

- [📔 Gün 4](#-gün-4)
	- [Conditionals - Koşullar](#conditionals-koşullar)
		- [If](#if)
		- [If Else](#if-else)
		- [If  Else if Else](#if--else-if-else)
		- [Switch](#switch)
		- [Ternary Operatörü](#ternary-operatörü)
	- [💻 Egzersizler](#-exercises)
		- [Egzersiz: Seviye 1](#egzersiz-seviye-1)
		- [Egzersiz: Seviye 2](#egzersiz-seviye-2)
		- [Egzersiz: Seviye 3](#egzersiz-seviye-3)

# 📔 Gün 4

## Conditionals - Koşullar

Koşullu ifadeler, farklı koşullara dayalı kararlar vermek için kullanılır.
Varsayılan olarak, JavaScript komut dosyasındaki ifadeler yukarıdan aşağıya doğru uygulanır. İşleme mantığı bunu gerektiriyorsa, ardışık yürütme akışı iki şekilde değiştirilebilir:

- Koşullu yürütme: Belirli bir ifade doğruysa, bir veya daha fazla ifadeden oluşan bir blok yürütülür.
- Tekrarlayan yürütme : Belirli bir ifade doğru olduğu sürece, bir veya daha fazla ifadeden oluşan bir blok tekrar tekrar yürütülecektir. Bu bölümde _if_, _else_ , _else if_ deyimlerini ele alacağız. Önceki bölümlerde öğrendiğimiz karşılaştırma ve mantıksal operatörler burada faydalı olacaktır.

Koşullar aşağıdaki yollarla uygulanabilir:

- if
- if else
- if else if else
- switch
- ternary operator

### If

JavaScript ve diğer programlama dillerinde _if_ anahtar kelimesi, bir koşulun doğru olup olmadığını kontrol etmek ve blok kodunu yürütmek için kullanılır. Bir if koşulu kullanmak oluşturmak için normal parantez ve küme parantezlerine ihtiyaç duyurulur. ({})

```js
// syntax
if (condition) {
  //kodun bu kısmı doğru koşul için çalışır
}
```

**Örnek:**

```js
let num = 3
if (num > 0) {
  console.log(`${num} is a positive number`)
}
//  3 pozitif bir sayıdır
```

Yukarıdaki koşul örneğinde görebileceğiniz gibi 3, 0'dan büyüktür, yani pozitif bir sayıdır. Koşul doğruydu ve kod bloğu yürütüldü. Ancak koşul yanlışsa herhangi bir sonuç göremeyiz.

```js
let isRaining = true
if (isRaining) {
  console.log('Remember to take your rain coat.')
}
```
Aynısı ikinci koşul için de geçerlidir, isRaining false ise if bloğu yürütülmez ve herhangi bir çıktı görmeyiz. Yanlış bir koşulun sonucunu görmek için, _else_ ile başka bir bloğumuz olmalıdır.

### If Else

Koşul doğruysa, ilk blok yürütülür, doğru değilse, __else__ koşul yürütülür.

```js
// syntax
if (condition) {
  // kodun bu kısmı doğru koşul için çalışır
} else {
  // kodun bu kısmı yanlış koşul için çalışır
}
```

```js
let num = 3
if (num > 0) {
  console.log(`${num} is a positive number`)
} else {
  console.log(`${num} is a negative number`)
}
//  3 pozitif bir sayıdır

num = -3
if (num > 0) {
  console.log(`${num} is a positive number`)
} else {
  console.log(`${num} is a negative number`)
}
//  -3 negatif bir sayıdır
```

```js
let isRaining = true
if (isRaining) {
  console.log('You need a rain coat.')
} else {
  console.log('No need for a rain coat.')
}
// Bir yağmurluğa ihtiyacın var.

isRaining = false
if (isRaining) {
  console.log('You need a rain coat.')
} else {
  console.log('No need for a rain coat.')
}
// Yağmurluğa gerek yok.
```

Son koşul yanlıştır, bu nedenle else bloğu yürütülmüştür. Ya ikiden fazla koşulumuz varsa? Bu durumda *else if* koşullarını kullanırdık.


### If  Else if Else

Hayatımızda günlük kararlar veririz. Kararları bir veya iki koşulu kontrol ederek değil, birden çok koşula göre veririz. Günlük hayatımızda olduğu gibi programlama da şartlarla doludur. Birden fazla koşulumuz olduğunda *else if* kullanırız. 

```js
// syntax
if (condition) {
     // code
} else if (condition) {
   // code
} else {
    //  code

}
```

**Örnek:**

```js
let a = 0
if (a > 0) {
  console.log(`${a} is a positive number`)
} else if (a < 0) {
  console.log(`${a} is a negative number`)
} else if (a == 0) {
  console.log(`${a} is zero`)
} else {
  console.log(`${a} is not a number`)
}
```

```js
// if else if else
let weather = 'sunny'
if (weather === 'rainy') {
  console.log('You need a rain coat.')
} else if (weather === 'cloudy') {
  console.log('It might be cold, you need a jacket.')
} else if (weather === 'sunny') {
  console.log('Go out freely.')
} else {
  console.log('No need for rain coat.')
}
```

#### Çevirmen Açıklaması

Arkadaşlar anlatıcı belirtmemiş lakin ben araya bunu şıkıştırayım. if doğruluğu kontrol eder bir kere kullanılır, else ise if çalışmadığında devreye girer buda bir kere kullanılır. 
Birden fazla if yada else kullanamazsınız. Zaten birden fazla koşulu sorgulamak için else if blogu bulunmaktadır. Normalde else if açıklamasında bunu anlamanız gerekir.
Lakin ekstra bir açıklama yapalım kafanızda tam oturmuş olsun konu. Mutlu kalın.


### Switch

Switch, **if else if else** için bir alternatiftir.
Switch ifadesi bir *switch* anahtar sözcüğüyle başlar, ardından bir parantez ve kod bloğu gelir. Kod bloğunun içinde farklı durumlarımız olacak. Case bloğu, switch parantezindeki değer vaka değeriyle eşleşirse çalışır. Break ifadesi, koşul yerine getirildikten sonra kod yürütmesini sonlandırmak içindir. Default blok, tüm durumlar koşulu karşılamıyorsa çalışır.


```js
switch(caseValue){
  case 1:
    // code
    break
  case 2:
   // code
   break
  case 3:
   // code
   break
  default:
   // code
}
```

```js
let weather = 'cloudy'
switch (weather) {
  case 'rainy':
    console.log('You need a rain coat.')
    break
  case 'cloudy':
    console.log('It might be cold, you need a jacket.')
    break
  case 'sunny':
    console.log('Go out freely.')
    break
  default:
    console.log(' No need for rain coat.')
}

// Switch Diğer Örnekler
let dayUserInput = prompt('What day is today ?')
let day = dayUserInput.toLowerCase()

switch (day) {
  case 'monday':
    console.log('Today is Monday')
    break
  case 'tuesday':
    console.log('Today is Tuesday')
    break
  case 'wednesday':
    console.log('Today is Wednesday')
    break
  case 'thursday':
    console.log('Today is Thursday')
    break
  case 'friday':
    console.log('Today is Friday')
    break
  case 'saturday':
    console.log('Today is Saturday')
    break
  case 'sunday':
    console.log('Today is Sunday')
    break
  default:
    console.log('It is not a week day.')
}

```

// Durumlarda koşulları kullanmak için örnekler

```js
let num = prompt('Enter number');
switch (true) {
  case num > 0:
    console.log('Number is positive');
    break;
  case num == 0:
    console.log('Numbers is zero');
    break;
  case num < 0:
    console.log('Number is negative');
    break;
  default:
    console.log('Entered value was not a number');
}
```

### Ternary Operatörü

Koşullar yazmanın başka bir yolu da üçlü operatörleri kullanmaktır. Bunu diğer bölümlerde ele aldık, ancak burada da belirtmek gerekir.

```js
let isRaining = true
isRaining
  ? console.log('You need a rain coat.')
  : console.log('No need for a rain coat.')
```

🌕  Olağanüstü birisin ve olağanüstü bir potansiyelin var. 4. gün zorluklarını yeni tamamladınız ve mükemmelliğe giden yolda dört adım öndesiniz. Şimdi beyniniz ve kasınız için bazı egzersizler yapın.  

## 💻 Egzersizler

### Egzersiz: Seviye 1

1. prompt(“Enter your age:”) ile kullanıcı girdisi alın. Kullanıcı 18 veya daha büyükse, geri bildirimde bulunun:'Sürecek kadar yaşlısınız', ancak 18 değilse, 18 yaşına girmesi gereken yıl sayısını beklemeye başlayarak başka bir geri bildirim verin.

   ```sh
   Enter your age: 30
   You are old enough to drive.

   Enter your age:15
   You are left with 3 years to drive.
   ```

1. if… else kullanarak myAge ve yourAge değerlerini karşılaştırın. Karşılaştırmaya dayanarak ve sonucu kimin daha yaşlı olduğunu (ben veya siz) belirterek konsola kaydedin. Yaşı girdi olarak almak için komut prompt(“Enter your age:”) kullanın.

   ```sh
   Enter your age: 30
   You are 5 years older than me.
   ```

1. a, b'den büyükse, 'a b'den büyüktür', aksi takdirde 'a, b'den küçüktür' döndürür. şekilde uygulamaya çalışın

    - using if else
    - ternary operator.

    ```js
      let a = 4
      let b = 3
    ```

    ```sh
      4 is greater than 3
    ```

1. Çift sayılar 2'ye tam bölünür kalan sıfırdır. Bir sayının çift olup olmadığını veya JavaScript kullanıp kullanmadığını nasıl kontrol edersiniz?

    ```sh
    Enter a number: 2
    2 is an even number

    Enter a number: 9
    9 is is an odd number.
    ```

### Egzersiz: Seviye 2

1. Öğrencilere puanlarına göre not verebilecek bir kod yazın:
   - 80-100, A
   - 70-89, B
   - 60-69, C
   - 50-59, D
   - 0-49, F
1. Mevsimin Sonbahar, Kış, İlkbahar veya Yaz olup olmadığını kontrol edin.
  Değerler :
    - Eylül, Ekim veya Kasım, mevsim sonbahardır.
    - Aralık, Ocak veya Şubat, mevsim kıştır.
    - Mart, Nisan veya Mayıs mevsimi bahardır
    - Haziran, Temmuz veya Ağustos, mevsim yazdır
    
1. Bir günün hafta sonu mu yoksa iş günü mü olduğunu kontrol edin. Komut dosyanız girdi olarak gün alacaktır.

```sh
    What is the day  today? Saturday
    Saturday is a weekend.

    What is the day today? saturDaY
    Saturday is a weekend.

    What is the day today? Friday
    Friday is a working day.

    What is the day today? FrIDAy
    Friday is a working day.
  ```

### Egzersiz: Seviye 3

1. Bir aydaki gün sayısını söyleyen bir program yazın.

  ```sh
    Enter a month: January
    January has 31 days.

    Enter a month: JANUARY
    January has 31 day

    Enter a month: February
    February has 28 days.

    Enter a month: FEbruary
    February has 28 days.
  ```

1. Bir aydaki gün sayısını söyleyen bir program yazın, şimdi artık yılı düşünün.


🎉 TEBRİKLER ! 🎉

[<< Gün 3](../03_Day_Booleans_operators_date/03_booleans_operators_date.md) | [Gün 5 >>](../05_Day_Arrays/05_day_arrays.md)
