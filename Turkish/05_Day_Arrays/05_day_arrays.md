



<div  align="center">

<h1> 30 Days Of JavaScript: Arrays</h1>

<a  class="header-badge"  target="_blank"  href="https://www.linkedin.com/in/asabeneh/">

<img  src="https://img.shields.io/badge/style--5eba00.svg?label=LinkedIn&logo=linkedin&style=social">

</a>

<a  class="header-badge"  target="_blank"  href="https://twitter.com/Asabeneh">

<img  alt="Twitter Follow"  src="https://img.shields.io/twitter/follow/asabeneh?style=social">

</a>

  

<sub>Author:

<a  href="https://www.linkedin.com/in/asabeneh/"  target="_blank">Asabeneh Yetayeh</a><br>

<small> January, 2020</small>

</sub>

</div>

  

[<< Gün 4](../04_Day_Conditionals/04_day_conditionals.md) | [Gün 6 >>](../06_Day_Loops/06_day_loops.md)

  

![Day 5](../../images/banners/day_1_5.png)

  

- [📔 Gün 5](#-day-5)

	- [Diziler ( Array )](#arrays)

		- [Boş bir dizi nasıl oluşturulur](#boş-bir-dizi-nasıl-oluşturulur)

		- [Değerlere sahip bir dizi nasıl oluşturulur](#değerlere-sahip-bir-dizi-nasıl-oluşturulur)

		- [split kullanarak dizi oluşturmak](#split-kullanarak-dizi-oluşturmak)

		- [index kullanarak dizi elemanlarına ulaşmak](#index-kullanarak-dizi-elemanlarına-ulaşmak)

		- [Dizi elemanlarını düzenlemek](#dizi-elemanlarını-düzenlemek)

		- [Dizileri manüple edebilecek metotlar](#dizileri-manüple-edebilecek-metotlar)

			- [Dizi Constructor'ı ( yapıcı metot )](#dizi-constructor)

			- [fill ile statik değerler yaratmak](#fill-ile-statik-değerler-yaratmak)

			- [concat kullanarak dizileri birleştirmek](#concat-kullanarak-dizileri-birleştirmek)

			- [Dizi uzunluğuna ulaşmak ( length )](#dizi-uzunluğuna-ulaşmak)

			- [arr dizisinin içindeki index'e ulaşmak](#arr-dizisinin-içindeki-indexe-ulaşmak)

			- [Dizinin içindeki son index'e ulaşmak](#dizinin-içindeki-son-indexe-ulaşmak)

			- [Diziyi kontrol etmek](#diziyi-kontrol-etmek)

			- [Diziyi string'e çevirmek](#diziyi-stringe-çevirmek)

			- [Dizi elemanlarını Joinlemek](#dizi-elemanlarını-joinlemek)

			- [Dizi elemanlarını Slice etmek ( kesmek )](#dizi-elemanlarını-slice-etmek)

			- [Dizlerde Splice metodu](#dizilerde-splice-metodu)

			- [push kullanarak diziye eleman eklemek](#push-kullanarak-diziye-eleman-eklemek)

			- [pop kıllanarak diziden eleman çıkarmak](#pop-kullanarak-diziden-eleman-çıkarmak)

			- [Dizinin en başından eleman kaldırmak](#dizinin-en-başından-eleman-kaldırmak)

			- [Dizinin en başına eleman ekleme](#dizinin-en-başına-eleman-eklemek)

			- [Dizi sırasını ters'e çevirmek](#dizi-sırasını-terse-çevirmek)

			- [Dizi elemanlarını sıralamak](#dizi-elemanlarını-sıralamak)

			- [Dizi içinde Diziler](#dizi-içinde-diziler)

	- [💻 Egzersizler](#-Egzersizler)

		- [Egzersiz: Seviye 1](#egzersiz-seviye-1)

		- [Egzersiz: Seviye 2](#egzersiz-seviye-2)

		- [Egzersiz: Seviye 3](#egzersiz-seviye-3)

  

# 📔 Gün 5

  

## Diziler

  

Değişkenlerin aksine, diziler _Çoklu değerleri_ depolayabilirler. Dizi'deki her bir değer  _index_'e sahiptir, ve her index _bellek adresindeki bir referans_'ı işaret eder. Bu _index'ler_  kullanılarak her bir değere ulaşım sağlanabilir. Bir dizinin index'i  _sıfır_'dan başlar ve dizinin son elemanının index'i, dizinin uzunluğundan bir eksiktir.

  

Bir dizi, sıralı ve değiştirilebilirdir. Farklı veri türlerinin bir koleksiyonudur. Bir dizi, tekrar edilen elemanların ve farklı veri türlerinin depolanmasına izin verir.  Bir dizi boş olabilir veya farklı veri türü değerlerine sahip olabilir.

  

### Boş bir dizi nasıl oluşturulur

  

JavaScript'te birçok farklı yol ile dizi oluşturabiliriz. Bir dizi oluşturmanın farklı yollarını görelim.

Bir dizi değişkeni tanımlamak için _let_ yerine _const_ kullanmak çok yaygındır. Const kullanıyorsanız, bu değişken adını bir daha kullanmayacağınız anlamına gelir.

  

- Array constructor'ı ( yapıcı metot ) kullanmak

  

```js

// syntax

const  arr = Array()

// ya da

// let arr = new Array()

console.log(arr) // []

```

  

- Köşeli parantez kullanmak([])

  

```js

// syntax

// Bu boş bir dizi oluşturmak için en çok tavsiye edilen yöntemdir

const  arr = []

console.log(arr)

```

  

### Değerlere sahip bir dizi nasıl oluşturulur

  

Başlangıç değerine sahip bir dizi. _length_ özelliğini kullanarak dizinin uzuluğunu bulabiliriz.

  

```js

const  numbers = [0, 3.14, 9.81, 37, 98.6, 100] // sayı dizisi

const  fruits = ['banana', 'orange', 'mango', 'lemon'] // string dizisi, meyveler

const  vegetables = ['Tomato', 'Potato', 'Cabbage', 'Onion', 'Carrot'] // string dizisi, sebzeler

const  animalProducts = ['milk', 'meat', 'butter', 'yoghurt'] // string dizisi, ürünler

const  webTechs = ['HTML', 'CSS', 'JS', 'React', 'Redux', 'Node', 'MongDB'] // string dizisi, web teknolojileri

const  countries = ['Finland', 'Denmark', 'Sweden', 'Norway', 'Iceland'] // string dizisi, ülkeler

  

// Diziyi ve dizinin uzunluğunu yazdırmak

  

console.log('Numbers:', numbers)

console.log('Number of numbers:', numbers.length)

  

console.log('Fruits:', fruits)

console.log('Number of fruits:', fruits.length)

  

console.log('Vegetables:', vegetables)

console.log('Number of vegetables:', vegetables.length)

  

console.log('Animal products:', animalProducts)

console.log('Number of animal products:', animalProducts.length)

  

console.log('Web technologies:', webTechs)

console.log('Number of web technologies:', webTechs.length)

  

console.log('Countries:', countries)

console.log('Number of countries:', countries.length)

```

  

```sh

Numbers: [0, 3.14, 9.81, 37, 98.6, 100]

Number of numbers: 6

Fruits: ['banana', 'orange', 'mango', 'lemon']

Number of fruits: 4

Vegetables: ['Tomato', 'Potato', 'Cabbage', 'Onion', 'Carrot']

Number of vegetables: 5

Animal products: ['milk', 'meat', 'butter', 'yoghurt']

Number of animal products: 4

Web technologies: ['HTML', 'CSS', 'JS', 'React', 'Redux', 'Node', 'MongDB']

Number of web technologies: 7

Countries: ['Finland', 'Estonia', 'Denmark', 'Sweden', 'Norway']

Number of countries: 5

```

  

- Dizinin farklı veri tiplerinde elemanları olabilir.

  

```js

const  arr = [

'Asabeneh',

250,

true,

{ country:  'Finland', city:  'Helsinki' },

{ skills: ['HTML', 'CSS', 'JS', 'React', 'Python'] }

] // arr farklı veri tipleri içerir.

console.log(arr)

```

  

### Split kullanarak dizi oluşturmak
  

Önceki bölümde gördüğümüz gibi, bir diziyi farklı şekillerde bölebilir ve diziyi değiştirebiliriz. Aşağıdaki örneklere bir göz atalım.

  

```js

let  js = 'JavaScript'

const  charsInJavaScript = js.split('')

  

console.log(charsInJavaScript) // ["J", "a", "v", "a", "S", "c", "r", "i", "p", "t"]

  

let  companiesString = 'Facebook, Google, Microsoft, Apple, IBM, Oracle, Amazon'

const  companies = companiesString.split(',')

  

console.log(companies) // ["Facebook", " Google", " Microsoft", " Apple", " IBM", " Oracle", " Amazon"]

let  txt =

'I love teaching and empowering people. I teach HTML, CSS, JS, React, Python.'

const  words = txt.split(' ')

  

console.log(words)

// metnin özel karakterleri var, sadece kelimeleri nasıl alabileceğinizi düşünün

// ["I", "love", "teaching", "and", "empowering", "people.", "I", "teach", "HTML,", "CSS,", "JS,", "React,", "Python"]

```

  

### index kullanarak dizi elemanlarına ulaşmak

  

Dizide elemanların indexlerini kullanarak o elemana ulaşabiliriz. Dizinin index'i 0'dan başlar. Aşşağıdaki resm her elemanın indexini açıkça göstermektedir.

  

![arr index](../images/array_index.png)

  

```js

const  fruits = ['banana', 'orange', 'mango', 'lemon']

let  firstFruit = fruits[0] // 1. eleman'a o elemanın indexini kullanarak erişiyoruz.
  

console.log(firstFruit) // banana

  

secondFruit = fruits[1]

console.log(secondFruit) // orange

  

let  lastFruit = fruits[3]

console.log(lastFruit) // lemon

// Son eleman devam eden örnekteki gibi hesaplanabilir

  

let  lastIndex = fruits.length - 1

lastFruit = fruits[lastIndex]

  

console.log(lastFruit) // lemon

```

  

```js

const  numbers = [0, 3.14, 9.81, 37, 98.6, 100] // sayı dizisi

  

console.log(numbers.length) // => dizinin uzunluğunu bilebiliriz. O da 6'dır

console.log(numbers) // -> [0, 3.14, 9.81, 37, 98.6, 100]

console.log(numbers[0]) // -> 0

console.log(numbers[5]) // -> 100

  

let  lastIndex = numbers.length - 1;

console.log(numbers[lastIndex]) // -> 100

```

  

```js

const  webTechs = [

'HTML',

'CSS',

'JavaScript',

'React',

'Redux',

'Node',

'MongoDB'

] // Web teknolojilerinin Listesi

  

console.log(webTechs) // Dizi elemanlarının hepsi

console.log(webTechs.length) // => dizinin uzunluğunu bilebiliriz. O da 7'dir

console.log(webTechs[0]) // -> HTML

console.log(webTechs[6]) // -> MongoDB

  

let  lastIndex = webTechs.length - 1

console.log(webTechs[lastIndex]) // -> MongoDB

```

  

```js

const  countries = [

'Albania',

'Bolivia',

'Canada',

'Denmark',

'Ethiopia',

'Finland',

'Germany',

'Hungary',

'Ireland',

'Japan',

'Kenya'

] // List of countries

  

console.log(countries) // -> Dizideki tüm ülkeler

console.log(countries[0]) // -> Albania

console.log(countries[10]) // -> Kenya

  

let  lastIndex = countries.length - 1;

console.log(countries[lastIndex]) // -> Kenya

```

  

```js

const  shoppingCart = [

'Milk',

'Mango',

'Tomato',

'Potato',

'Avocado',

'Meat',

'Eggs',

'Sugar'

] // Ürünler listesi

  

console.log(shoppingCart) // -> shoppingCart Dizisi elemanlarının hepsi

console.log(shoppingCart[0]) // -> Milk

console.log(shoppingCart[7]) // -> Sugar

  

let  lastIndex = shoppingCart.length - 1;

console.log(shoppingCart[lastIndex]) // -> Sugar

```

  

### Dizi elemanlarını düzenlemek

  

Bir dizi değiştirilebilir. Dizi yaratıldıktan sonra, elemanların içeriklerini değiştirebilir, modifiye edebiliriz. 

  

```js

const  numbers = [1, 2, 3, 4, 5]

numbers[0] = 10  // index 0'daki 1 elemanını 10 elemanı olarak değiştirdik

numbers[1] = 20  // index 2'deki 2 elemanını 20 elemanı olarak değiştirdik

  

console.log(numbers) // [10, 20, 3, 4, 5]

  

const  countries = [

'Albania',

'Bolivia',

'Canada',

'Denmark',

'Ethiopia',

'Finland',

'Germany',

'Hungary',

'Ireland',

'Japan',

'Kenya'

]

  

countries[0] = 'Afghanistan'  // Albania yerini Afghanistan aldı

let  lastIndex = countries.length - 1

countries[lastIndex] = 'Korea'  // Kenya yerini Korea aldı

  

console.log(countries)

```

  

```sh

["Afghanistan", "Bolivia", "Canada", "Denmark", "Ethiopia", "Finland", "Germany", "Hungary", "Ireland", "Japan", "Korea"]

```

  

### Dizileri manüple edebilecek metotlar

  

Diziyi manüple edebilmek için farklı metotlar vardır. Bunlar dizilerle uğraşmak için kullanışlı yöntemlerden bazılarıdır. Bu yöntemler: _Array, length, concat, indexOf, slice, splice, join, toString, includes, lastIndexOf, isArray, fill, push, pop, shift, unshift_

  

#### Dizi Constructor


  

Array:Bir dizi yaratmak için kullanılır.

  

```js

const  arr = Array() // boş bir dizi yaratır

console.log(arr)

  

const  eightEmptyValues = Array(8) // sekiz tane boş değer yaratır

console.log(eightEmptyValues) // [empty x 8]

```

  

#### fill ile statik değerler yaratmak

  

fill: Bütün dizi elemanlarını statik değerle doldurur.

  

```js

const  arr = Array() // Boş bir dizi yaratır

console.log(arr)

  

const  eightXvalues = Array(8).fill('X') // 'X'değerine sahip 8 tane eleman oluşuturur.

console.log(eightXvalues) // ['X', 'X','X','X','X','X','X','X']

  

const  eight0values = Array(8).fill(0) // '0' değerine sahip 8 tane eleman oluşturur.

console.log(eight0values) // [0, 0, 0, 0, 0, 0, 0, 0]

  

const  four4values = Array(4).fill(4) //'4' değerine sahip 8 tane eleman oluşturur.

console.log(four4values) // [4, 4, 4, 4]

```

  

#### Concat kullanarak dizileri birleştirmek

  

concat: İki diziyi birbiri ile birleştirir.

// Çevirmen notu : concat sadece iki diziyi birleştirmez. ikiden fazla sayıda diziyi birleştirmenize izin verir.

  

```js

const  firstList = [1, 2, 3]

const  secondList = [4, 5, 6]

const  thirdList = firstList.concat(secondList)

  

console.log(thirdList) // [1, 2, 3, 4, 5, 6]

```

  

```js

const  fruits = ['banana', 'orange', 'mango', 'lemon'] // meyveler dizisi

const  vegetables = ['Tomato', 'Potato', 'Cabbage', 'Onion', 'Carrot'] // sebzeler dizisi

const  fruitsAndVegetables = fruits.concat(vegetables) // iki diziyi birleştirdik

  

console.log(fruitsAndVegetables)

```

  

```sh

["banana", "orange", "mango", "lemon", "Tomato", "Potato", "Cabbage", "Onion", "Carrot"]

```

  

#### Dizi uzunluğuna ulaşmak

  

Length:Dizi uzunluğunu bildirir.

  

```js

const  numbers = [1, 2, 3, 4, 5]

console.log(numbers.length) // -> Dizinin uzunluğu 5'tir

```

  

#### Arr dizisinin içindeki indexe ulaşmak

  

indexOf: O elemanın dizide olup olmadığını kontrol eder.Eğer o eleman dizide mevcutsa index numarasını, mevcut değilse -1 döner.
  

```js

const  numbers = [1, 2, 3, 4, 5]

  

console.log(numbers.indexOf(5)) // -> 4

console.log(numbers.indexOf(0)) // -> -1

console.log(numbers.indexOf(1)) // -> 0

console.log(numbers.indexOf(6)) // -> -1

```

  

Bir dizide mevcut olup olmadığını kontrol edin.

  

- Listedeki elemanları kontrol edin.

```js

// dizide bir banana olup olmadığını kontrol edelim

  

const  fruits = ['banana', 'orange', 'mango', 'lemon']

let  index = fruits.indexOf('banana') // 0

  

if(index === -1){

console.log('This fruit does not exist in the array')

} else {

console.log('This fruit does exist in the array')

}

// This fruit does exist in the array

  

// Burada ayrıca kısa if kullanabilirz.

index === -1 ? console.log('This fruit does not exist in the array'): console.log('This fruit does exist in the array')

  

// dizide bir avocado olup olmadığını kontrol edelim

let  indexOfAvocado = fruits.indexOf('avocado') // -1, eğer eleman dizide yoksa -1 döner

if(indexOfAvocado === -1){

console.log('This fruit does not exist in the array')

} else {

console.log('This fruit does exist in the array')

}

// This fruit does not exist in the array

```

  

#### Dizinin içindeki son indexe ulaşmak

  

lastIndexOf: Dizideki son elemanın pozisyonunu verir. Eğer mevcutsa o elemanın index numarasını döner, mevcut değilse -1 döner.

  

```js

const  numbers = [1, 2, 3, 4, 5, 3, 1, 2]

  

console.log(numbers.lastIndexOf(2)) // 7

console.log(numbers.lastIndexOf(0)) // -1

console.log(numbers.lastIndexOf(1)) // 6

console.log(numbers.lastIndexOf(4)) // 3

console.log(numbers.lastIndexOf(6)) // -1

```

  

includes:Bir dizide bir öğenin olup olmadığını kontrol etmek için kullanılır.Mevcut ise, true değerini döndürür, aksi takdirde false değerini döndürür.

  

```js

const  numbers = [1, 2, 3, 4, 5]

  

console.log(numbers.includes(5)) // true

console.log(numbers.includes(0)) // false

console.log(numbers.includes(1)) // true

console.log(numbers.includes(6)) // false

  

const  webTechs = [

'HTML',

'CSS',

'JavaScript',

'React',

'Redux',

'Node',

'MongoDB'

] // Web teknolojileri dizisi

  

console.log(webTechs.includes('Node')) // true

console.log(webTechs.includes('C')) // false

```

  

#### Diziyi kontrol etmek

  

Array.isArray: Veri tipinin bir dizi olup olmadığını kontrol etmek için kullanılır.
  

```js

const  numbers = [1, 2, 3, 4, 5]

console.log(Array.isArray(numbers)) // true

  

const  number = 100

console.log(Array.isArray(number)) // false

```

  

#### Diziyi stringe çevirmek

  

toString:Diziyi string bir ifadeye çevirir.

  

```js

const  numbers = [1, 2, 3, 4, 5]

console.log(numbers.toString()) // 1,2,3,4,5

  

const  names = ['Asabeneh', 'Mathias', 'Elias', 'Brook']

console.log(names.toString()) // Asabeneh,Mathias,Elias,Brook

```

  

#### Dizi elemanlarını Joinlemek
  

join: Dizinin elemanlarını birleştirmek için kullanılır, join yönteminde ilettiğimiz argüman dizide birleştirilir ve bir dizi olarak döndürülür. Varsayılan olarak bir virgül ile birleşir, ancak elemanlar arasında birleştirilebilecek farklı dizi parametreleri iletebiliriz.

  

```js

const  numbers = [1, 2, 3, 4, 5]

console.log(numbers.join()) // 1,2,3,4,5

  

const  names = ['Asabeneh', 'Mathias', 'Elias', 'Brook']

  

console.log(names.join()) // Asabeneh,Mathias,Elias,Brook

console.log(names.join('')) //AsabenehMathiasEliasBrook

console.log(names.join(' ')) //Asabeneh Mathias Elias Brook

console.log(names.join(', ')) //Asabeneh, Mathias, Elias, Brook

console.log(names.join(' # ')) //Asabeneh # Mathias # Elias # Brook

  

const  webTechs = [

'HTML',

'CSS',

'JavaScript',

'React',

'Redux',

'Node',

'MongoDB'

] // List of web technologies

  

console.log(webTechs.join()) // "HTML,CSS,JavaScript,React,Redux,Node,MongoDB"

console.log(webTechs.join(' # ')) // "HTML # CSS # JavaScript # React # Redux # Node # MongoDB"

```

  

#### Dizi elemanlarını slice etmek

  

Slice: Bir aralıktaki çoklu elemanları dilimler İki parametre alır. Bu parametreler, başlangıç ve bitiş konumlarıdır. Bitiş konumunu dahil etmez.
  

```js

const  numbers = [1,2,3,4,5]

  

console.log(numbers.slice()) // -> Bütün öğeyi kopyalar

console.log(numbers.slice(0)) // -> Bütün öğeyi kopyalar

console.log(numbers.slice(0, numbers.length)) // Bütün öğeyi kopyalar

console.log(numbers.slice(1,4)) // -> [2,3,4] // son elemanı dahil etmez

```

  

#### Dizilerde splice metodu

  

Splice: üç parametre alır :başlangıç konumu, kaldırılması gereken eleman sayısı ve  eklenmesi gereken eleman sayısı.

  

```js

const  numbers = [1, 2, 3, 4, 5]

numbers.splice()

console.log(numbers) // -> Bütün elemanları kaldırır

  

```

  

```js

const  numbers = [1, 2, 3, 4, 5]

numbers.splice(0,1)

console.log(numbers) // ilk elemanı kaldırır

```

  

```js

const  numbers = [1, 2, 3, 4, 5, 6]

numbers.splice(3, 3, 7, 8, 9)

console.log(numbers.splice(3, 3, 7, 8, 9)) // -> [1, 2, 3, 7, 8, 9] //2 eleman kaldırdı ve yerine 3 eleman ekledi

```

  

#### Push kullanarak diziye eleman eklemek

  

Push: Dizinin sonuna eleman ekler.Varolan bir diziye eleman eklemek için push metodunu kullanırız.
  

```js

// syntax

const  arr = ['item1', 'item2','item3']

arr.push('new item')

console.log(arr)

// ['item1', 'item2','item3','new item']

```

  

```js

const  numbers = [1, 2, 3, 4, 5]

numbers.push(6)

console.log(numbers) // -> [1,2,3,4,5,6]

  

numbers.pop() // -> Dizinin sonundan bir eleman çıkarır.

console.log(numbers) // -> [1,2,3,4,5]

```

  

```js

let  fruits = ['banana', 'orange', 'mango', 'lemon']

fruits.push('apple')

console.log(fruits) // ['banana', 'orange', 'mango', 'lemon', 'apple']

  

fruits.push('lime')

console.log(fruits) // ['banana', 'orange', 'mango', 'lemon', 'apple', 'lime']

```

  

#### pop kıllanarak diziden eleman çıkarmak

  

pop: Dizinin sonundaki elemanı siler.

  

```js

const  numbers = [1, 2, 3, 4, 5]

numbers.pop() // -> Sondaki elemanı siler

console.log(numbers) // -> [1,2,3,4]

```

  

#### Dizinin en başından eleman kaldırmak

  

shift: Dizinin en başındaki elemanı siler.

  

```js

const  numbers = [1, 2, 3, 4, 5]

numbers.shift() // -> baştan bir elemanı kaldırır.

console.log(numbers) // -> [2,3,4,5]

```

  

#### Dizinin en başına eleman eklemek

  

unshift: Dizinin başına dizi elemanı ekler.

  

```js

const  numbers = [1, 2, 3, 4, 5]

numbers.unshift(0) // -> en başa eleman ekler

console.log(numbers) // -> [0,1,2,3,4,5]

```

  

#### Dizi sırasını terse çevirmek

  

reverse: Dizi sıralamasını terse çevirir.

  

```js

const  numbers = [1, 2, 3, 4, 5]

numbers.reverse() // -> ters dizi sırası

console.log(numbers) // [5, 4, 3, 2, 1]

  

numbers.reverse()

console.log(numbers) // [1, 2, 3, 4, 5]

```

  

#### Dizi elemanlarını sıralamak
  

sort: Dizi elemanlarını alfabetik sırada düzenleyin.Sort call back fonksyonu alır, sort'un call back fonksiyonu ile nasıl kullandığımızı ilerleyen bölümlerde göreceğiz.

  

```js

const  webTechs = [

'HTML',

'CSS',

'JavaScript',

'React',

'Redux',

'Node',

'MongoDB'

]

  

webTechs.sort()

console.log(webTechs) // ["CSS", "HTML", "JavaScript", "MongoDB", "Node", "React", "Redux"]

  

webTechs.reverse() // sortladıktan sonra reverse edebiliriz.

console.log(webTechs) // ["Redux", "React", "Node", "MongoDB", "JavaScript", "HTML", "CSS"]

```

  

### Dizi içinde diziler

  

Diziler farklı veri tiplerinde elemanları ve yeni bir dizi de depolayabilirler Şimdi dizi içinde bir dizi tanımlayalım.
  

```js

const  firstNums = [1, 2, 3]

const  secondNums = [1, 4, 9]

  

const  arrayOfArray = [[1, 2, 3], [1, 2, 3]]

console.log(arrayOfArray[0]) // [1, 2, 3]

  

const  frontEnd = ['HTML', 'CSS', 'JS', 'React', 'Redux']

const  backEnd = ['Node','Express', 'MongoDB']

const  fullStack = [frontEnd, backEnd]

console.log(fullStack) // [["HTML", "CSS", "JS", "React", "Redux"], ["Node", "Express", "MongoDB"]]

console.log(fullStack.length) // 2

console.log(fullStack[0]) // ["HTML", "CSS", "JS", "React", "Redux"]

console.log(fullStack[1]) // ["Node", "Express", "MongoDB"]

```

  

🌕 Çalışkansınız ve zaten çok şey başardınız. 5. gün zorluklarını yeni tamamladınız ve mükemmelliğe giden yolda 5 adım öndesiniz. Şimdi beyniniz ve kasınız için bazı egzersizler yapın.

  

## 💻 Egzersizler

  

### Egzersiz: Seviye 1

  

```js

const  countries = [

'Albania',

'Bolivia',

'Canada',

'Denmark',

'Ethiopia',

'Finland',

'Germany',

'Hungary',

'Ireland',

'Japan',

'Kenya'

]

  

const  webTechs = [

'HTML',

'CSS',

'JavaScript',

'React',

'Redux',

'Node',

'MongoDB'

]

```

  

1. _boş_ bir dizi yaratın;

2. Eleman sayısı 5'ten fazla olan bir dizi yaratın.

3. Yarattığınız dizinin uzunluğunu bulun ( length ).

4. Dizinizdeki ilk elemanı, ortadaki elemanı ve sondaki elemanı bulun.

5.  _mixedDataTypes_ adında bir dizi yaratın,dizinin içine farklı veri tiplerinde elemanlar koyun ve bu dizinin uzunluğunu bulun. Dizinin uzunluğu 5'ten büyük olmalıdır.

6. ItCompanies adlı bir dizi değişkeni oluşturun ve Facebook, Google, Microsoft, Apple, IBM, Oracle ve Amazon'a başlangıç değerleri atayın.

7. _console.log()_ kullanarak dizinizi yazdırın.

8. Dizinin içindeki şirketlerin sayısın yazdırın.

9. Dizinin içindeki ilk, ortadaki ve son elemanı yazdırın.

10. Dizideki her şirketi yazdırın.

11. Her bir şirketin adını tek tek büyük harfleri ile değişterin ( ör: facebook -> FACEBOOK) ve her birini yazdırın.

12. Diziyi bir cümle gibi yazdırın: Facebook, Google, Microsoft, Apple, IBM,Oracle and Amazon are big IT companies.

13. itCompanies dizisinde belirli bir şirketin olup olmadığını kontrol edin.  Varsa şirketi geri döndürün, aksi takdirde _not found_ geri döndürün.

14. Birden fazla 'o' harfi içeren şirketleri filter metodunu kullanmadan filtreleyin.

15.  _sort()_ metodunu kullanarak diziyi sıralayın.

16.  _reverse()_ metodunu kullanarak diziyi tersine çevirin.

17. Diziden ilk 3 şirketi dilimleyin ( Slice edin ).

18. Diziden son 3 şirketi dilimleyin ( Slice edin ).

19. Ortadaki IT şirketini ya da şirketlerini diziden dilimleyin ( Slice edin ).

20. İlk IT şirketini diziden kaldırın.

21. Ortadaki IT şirketini ya da şirketlerini diziden kaldırın.

22. Sondaki IT şirketini diziden kaldırın.

23. Bütün IT şirketlerini kaldırın.

  

### Egzersiz: Seviye 2

  

1.Ayrı bir country.js dosyası oluşturun ve country dizisini bu dosyaya kaydedin, ayrı bir web_techs.js dosyası oluşturun ve webTechs dizisini bu dosyaya kaydedin. Daha sonra Main.js dosyasından her iki dosyaya da erişim sağlayın.

1. Önce bütün noktalama işaretlerini kaldırın ve ve string ifadeyi dizi olarak değiştirin ve dizideki kelime sayısını sayın.
  

```js

let  text =

'I love teaching and empowering people. I teach HTML, CSS, JS, React, Python.'

console.log(words)

console.log(words.length)

```

  

```sh

["I", "love", "teaching", "and", "empowering", "people", "I", "teach", "HTML", "CSS", "JS", "React", "Python"]

13

```

  

1. Aşşağıdaki alışveriş sepetindeki elemanları ekleyin, silin , düzenleyin. 

  

```js

const  shoppingCart = ['Milk', 'Coffee', 'Tea', 'Honey']

```

  

- Eğer alışveriş sepetine zaten 'Meat' eklenmemişse en başa ekleyin.  

- Eğer alışveriş sepetine zaten 'Sugar' eklenmemişse en sona ekleyin.  

- Eğer bala alerjiniz varsa 'Honey' elemanını diziden silin.

- 'Tea' elemanını 'Green Tea' olarak güncelleyin.

1. countries dizisinde 'Ethiopia' olup olmadığını kontrol edin. Eğer varsa  'ETHIOPIA' yazdırın. eğer yoksa bunu countries dizisine ekleyin.

2. webTechs dizisinde Sass olup olmadığını kontrol edin eğer varsa 'Sass is a CSS preprocess' yazdırın.  Eğer yoksa diziye Sass elemanını ekleyip diziyi yazdırın

4. Aşağıdaki iki değişkeni birleştirin ve bir fullStack değişkeninde atayın.

  

```js

const  frontEnd = ['HTML', 'CSS', 'JS', 'React', 'Redux']

const  backEnd = ['Node','Express', 'MongoDB']

console.log(fullStack)

```

  

```sh

["HTML", "CSS", "JS", "React", "Redux", "Node", "Express", "MongoDB"]

```

  

### Egzersiz: Seviye 3

  

1. Aşağıdaki dizide 10 öğrencinin yaşı vardır:

  

```js

const  ages = [19, 22, 19, 24, 20, 25, 26, 24, 25, 24]

```

  

- Diziyi sıralayın ve en küçük ve en büyük yaşı bulun

- Medyan yaşı bulun(dizinin ortasındaki eleman ama ortada iki eleman varsa  elemanlar ikiye bölünür)

- Ortalama yaşı bulun(tüm elemanlar eleman sayısına bölünür)

- Yaş aralığını bulun (maks - min)

- _abs()_ metodunu kullanarak (min - ortalama) ve (maks - ortalama) değerlerini karşılaştırın, 

1. [countries array](https://github.com/Asabeneh/30DaysOfJavaScript/tree/master/data/countries.js) dizisinden ilk 10 ülkeyi dilimleyin ( Slice edin )

1.  [countries array](https://github.com/Asabeneh/30DaysOfJavaScript/tree/master/data/countries.js) dizisinden ortadaki ülkeleri bulun.

2. countries dizisini çift ise iki eşit diziye bölün. countries dizisi çift değilse, ilk yarı için bir ülke fazla olarak bölün

🎉 TEBRİKLER ! 🎉

  

[<< Gün 4](../04_Day_Conditionals/04_day_Conditionals.md) | [Gün 6 >>](../06_Day_Loops/06_day_loops.md)