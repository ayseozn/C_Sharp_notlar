
``` C#
using System;

namespace HelloWorld
{
  class Program
  {
    static void Main(string[] args)
    {
      Console.WriteLine("Hello World!");    
    }
  }
}
```

``using System`` : system sınıfının kullanılabileceği anlamına gelir.

``namespace`` : 

``class`` : Veri ve yöntemler için bir kapsayıcıdır ve programınıza işlevsellik getirir. C# dilinde çalışan her kod satırı bir sınıfın içinde olmalıdır.

``Console.Write();`` : çıktı almak, metin yazdırmak için kullanılır.

``Console.WriteLine();`` : Write den tek farkı çıktıyı yazdırdıktan sonra \n atar.

## C# Değişkenleri:
int, double, char, string, bool

    type variableName = value;

``const`` : değişkeni "sabit" olarak bildirecektir, yani değiştirilemez ve salt okunurdu

```
const int myNum = 15;
myNum = 20; // error
```

Not: Değeri atamadan sabit bir değişken bildiremezsiniz. Bunu yaparsanız bir hata oluşur: Bir const alanı bir değer sağlanmasını gerektirir .

#### Değişkenlere isim vermenin genel kuralları şunlardır:

- İsimler harf, rakam ve alt çizgi karakterini (_) içerebilir
- İsimler bir harf veya alt çizgi ile başlamalıdır
- İsimler küçük harfle başlamalı ve boşluk içeremez
- İsimler büyük/küçük harfe duyarlıdır ("myVar" ve "myvar" farklı değişkenlerdir)
- intAyrılmış sözcükler (C# anahtar sözcükleri gibi, or gibi double) ad olarak kullanılamaz.

## Data Type (veri tipleri):
- int : 4 bytes (tam sayı) -2147483648 ile 2147483647
- long : 8 bytes (tam sayı) -9223372036854775808 ile 9223372036854775807
- float : 4 bytes (kayan noktalı sayılar) (değer F ile sonlanmalı ör: 2.3F)
- double : 8 bytes (kayan noktalı sayılar) (değer D ile sonlanmalı ör: 2.3D)
- bool : 1 bit (true, false)
- char : 2 bytes
- string : 2 bytes per character (karakter başına 2 byte)

Kayan noktalı bir sayı, aynı zamanda 10'un kuvvetini belirtmek için "e" ile gösterilen bir bilimsel sayı da olabilir. örn: 35e3F, 12E4D

## Type Casting (Tür Dönüşümü):

- ##### Implicit Casting (kapalı Dönüşüm) (otomatik):
  
  Daha küçük bir türü daha büyük bir tür boyutuna dönüştürme.
  
  char-> int-> long-> float->double

  ```C#
  int myInt = 9;
  double myDouble = myInt; 
  ```

- ##### Explicit Casting (açık dönüşüm) (manuel):
  
  daha büyük bir türü daha küçük boyutlu bir türe dönüştürme.

  double-> float-> long-> int->char

  ```C#
  double myDouble = 9.78;
  int myInt = (int) myDouble;
  ```
## Type Conversion Methods (Tür Dönüştürme Yöntemleri)

```Convert.ToBoolean```, ```Convert.ToDouble```, ```Convert.ToString```, ```Convert.ToInt32(int)```, ```Convert.ToInt64()```

```C#
int myInt = 10;
Console.WriteLine(Convert.ToString(myInt)); 
```

## Get User Input (Kullanıcı Girişi Alma)
konsoldan girdi almak için  ``Console.ReadLine()`` kullanırız. Bize standart girişten bir satır okur, bu methot bir string döndürür, bu nedenle başka bir tür almak istersem tür dönüşümü gerekir.

 ```C#
Console.WriteLine("Enter your age:");
int age = Console.ReadLine();

Console.WriteLine("Enter your age:");
int age = Console.ReadLine(); //yanlış kullanım
int age = Convert.ToInt32(Console.ReadLine()); // doğru kullanım
```
hatalı tür dönüşümü durumdalarında exception fırlatır.

## Operatörler

Aritmetik Operatörler:
- ```+``` : x + y;
- ```-``` : x - y;
- ```*``` : x * y; 
- ```/``` : x / y; (bölme)
- ```%``` : x % y; (bölme işleminin kalanı)
- ```++``` : x++; 1 arttırır
- ```--``` : x--; 1 azaltır
  
Atama Operatörleri:
- ```=``` : x = 10; atama operatörü
- ```+=``` : x += 5; toplama atama operatörü (x = x + 5)
- ```-=``` : x -= 5; çıkartma atama operatörü
- ```*=``` : x *= 3;    (x = x * 3)
- ```/=``` : x /= 3;    (x = x / 3)
- ```%=``` : x %= 3;    (x = x % 3)
- ```&=``` : x &= 3;    (x = x & 3)
- ```|=``` : 	x |= 3;   (x = x | 3)
- ```^=``` : x ^= 3;    (x = x ^ 3)
- ```>>=``` : x >>= 3;   (x = x >> 3)
- ```<<=``` : 	x <<= 3;   (x = x << 3)

Karşılaştırma Operatörleri:
- ```==``` : eşit
- ```!=``` : eşit değil
- ```>``` : büyüktür
- ```<``` : küçüktür
- ```>=``` : büyük eşit
- ```<=``` : küçük eşit

Mantıksal Operatörler:
- ```&&``` : mantıksal ve operatörü
- ```||``` : mantıksal yada operatörü
- ```!``` : mantıksal değil operatörü

## Matematik

Max : x ve y'nin en büyük değerini bulmak için kullanılır.

```C#
Math.Max(5, 10);
```

Min : x ve y'nin en küçük değerini bulmak için kullanılır.

```C#
Math.Min(5, 10);
```

Sqrt (karekök) : x'in karekökünü döndürür.

```C#
Math.Sqrt(64);
```

Abs (mutlak değer) : x'in mutlak değerini döner.

```C#
Math.Abs(-4.7);
```

Round (yuvarlama) : bir sayıyı en yakın sayıya yuvarlar.

```C#
Math.Round(9.99);
```
## Strings (Dizeler)

Çift tırnak işaretiyle çevrelenmiş bir karakter koleksiyonunu içerir:

```C#
string greeting = "Hello";
```

Lenght : Dizenin uzunluğunu bulmak için kullanılır.

ToUpper : Dizenin harflerini büyük harf yapar.

ToLower : Dizenin harflerini küçük harf yapar.

```C#
string txt = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";
Console.WriteLine("The length of the txt string is: " + txt.Length);

Console.WriteLine(txt.ToUpper());
Console.WriteLine(txt.ToLower());
```
#### String Concatenation (Dize Bağlantısı) :
'+' ve string.Concat() iki dizeyi birleştirmek için kullanılır.

```C#
string firstName = "John ";
string lastName = "Doe";
string name = firstName + lastName;
Console.WriteLine(name);
string name2 = string.Concat(firstName, lastName);
Console.WriteLine(name2);
```
#### String Interpolation :
Değişkenlerin ve ifadelerin doğrudan bir dize içine gömülerek kullanılmasını sağlayan bir özelliktir.  C# 6 ve sonrası sürümlerde kullanılır.

Süslü parantezler içinde yalnızca değişken değil, aynı zamanda işlemler veya ifadeler de kullanılabilir.

$ işareti unutmamalıdır.

```C#
//String Interpolation
string isim = "Ahmet";
int yas = 25;
string mesaj = $"Merhaba, benim adım {isim} ve {yas} yaşındayım.";
Console.WriteLine(mesaj); //çıktı: Merhaba, benim adım Ahmet ve 25 yaşındayım.

DateTime bugun = DateTime.Now;
Console.WriteLine($"Bugünün tarihi: {bugun:dd/MM/yyyy}"); // Çıktı: Bugünün tarihi: 23/10/2024

double fiyat = 99.99;
Console.WriteLine($"Ürün fiyatı: {fiyat:C}"); // Çıktı: Ürün fiyatı: ₺99.99

int a = 10, b = 20;
Console.WriteLine($"a + b = {a + b}"); // Çıktı: a + b = 30
```
#### Access Strings : 
dizedeki bir karaktere erişim de [] kullanılır. karakterin dizindeki konumu bulmak için ``IndexOf()`` kullanılır.

Substring(); methodu bir dizeden belirli bir alt dizeyi almak için kullanılır.
 
```C#
string myString = "Hello";
Console.WriteLine(myString[0]);
Console.WriteLine(myString.IndexOf("l")); // çıktı 2 olur

string metin = "Programlama";
string altDize = metin.Substring(6); // "lama"

int charPos = metin.IndexOf("g");
string lastName = name.Substring(charPos);
Console.WriteLine(lastName); //çıktı:ramlama
```
#### Special Characters (özel karakterler)

- \' :
- \" :
- \\ :
- \n : yeni satır.
- \t : tab atar.
- \b :

## Booleans
sadece True ve False değeri alabilir.

True / False

## if .. else

if true koşulunu sağladığında if bloğu içerisindeki kod çalışır.

else if: if koşulu false ile yeni koşul belirtmek için kullanılır.

else:  if veya else if koşulu true olmadığı durumda çalışır. her zaman kullanmak zorunlu deildir. else if olmadan sadece if ilede kullanılır.

```C#
if (20 > 18) 
{
  Console.WriteLine("20 is greater than 18");
}
else if(20 < 18)
{
  Console.WriteLine(if false ile girer);
}
else
{
  Console.WriteLine("if ve elseif koşulu sağlanmadı");
}
```
#### Short Hand If...Else

```C#
variable = (condition) ? expressionTrue :  expressionFalse;
```
## Switch Statements

```C#
/*
switch(expression) 
{
  case x:
    // code block
    break;
  case y:
    // code block
    break;
  default:
    // code block
    break;
} */

int day = 4;
switch (day) 
{
  case 1:
    Console.WriteLine("Monday");
    break;
  case 2:
    Console.WriteLine("Tuesday");
    break;
  case 3:
    Console.WriteLine("Wednesday");
    break;
  case 4:
    Console.WriteLine("Thursday");
    break;
  case 5:
    Console.WriteLine("Friday");
    break;
  case 6:
    Console.WriteLine("Saturday");
    break;
  case 7:
    Console.WriteLine("Sunday");
    break;
}
```
## loop (Döngü)
Döngüler, belirtilen bir koşul sağlandığı sürece bir kod bloğunu çalıştırabilir. kullanışlıdırlar çünkü zamandan tasarruf ederler, hataları azaltır ve kodun daha okunabilir olmasını sağlarlar.

### While Loop:
belirtilen koşul true olduğu sürece kod bloğunda döngü oluşturulur.

```c#
while (condition) 
{
  // code block to be executed
}
```
Not: Koşulda kullanılan değişkeni arttırmayı unutmayın, aksi takdirde döngü asla sonlanmayacaktır!

### Do/While Loop:
do/while, while döngüsünün bir çeşididir. bu döngü koşulu kontrol etmeden önce kod bloğunu bir kez yürütür, ardından koşulun doğru olduğu sürece döngüyü tekrarlar. Koşul yanlış bile olsa en az bir kere çalışır.

```C#
/*
do 
{
  // code block to be executed
}
while (condition);
*/
int i = 0;
do 
{
  Console.WriteLine(i);
  i++;
}
while (i < 5);
```

### For Loop:
Kod bloğunda kaç kez döngü oluşturmak istediğinizi bilddiğinizde while yerine for u tercih edebilirsiniz.
```C#
/*
for (statement 1; statement 2; statement 3) 
{
  // code block to be executed
}*/

for (int i = 0; i < 5; i++) 
{
  Console.WriteLine(i);
}
```
- statement1: kod bloğundan önce yürütülür. sadece bir kere çalışır.
- statement2: Kod bloğunun yürütülmesi için koşulu tanımlar.
- statement3: Kod bloğu yürütüldükten sonra yürütülür. Her defasında çalışır.

### Nested Loops(İç İçe Döngüler):
 bir döngüyü başka bir döngünün içerisine yerleştirmek mümkündür.
```C#
// Outer loop
for (int i = 1; i <= 2; ++i) 
{
  Console.WriteLine("Outer: " + i);  // Executes 2 times

  // Inner loop
  for (int j = 1; j <= 3; j++) 
  {
    Console.WriteLine(" Inner: " + j); // Executes 6 times (2 * 3)
  }
}
```
### Foreach Loop(Foreach Döngüsü):
Foreach döngüsü:  bir koleksiyon veya dizi içerisindeki öğeleri sırayla dolaşmak için kullanılan bir döngüdür.

Avantajları: Döngü sırasında koleksiyonun sınırlarını aşma riski yoktur.

Dezavantaj: elemanlara doğrudan erişim sağlanamaz ve elemanlarda değişiklik yapılamaz.
```C#
/*
foreach (type variableName in arrayName)
{
    // variableName ile yapılacak işlemler
}*/

//string
string[] isimler = { "Ali", "Ayşe", "Mehmet", "Zeynep" };

foreach (string isim in isimler)
{
    Console.WriteLine(isim);
}

//
List<int> sayilar = new List<int> { 1, 2, 3, 4, 5 };

foreach (int sayi in sayilar)
{
    // sayi = sayi * 2; // Geçersiz, derleme hatası
    Console.WriteLine(sayi * 2); // Geçerli, çıktıda değişikliği gösterir
}
```
- variableName: Döngü sırasında her bir öğeyi temsil eden değişken
- arrayName: Üzerinde iterasyon yapılan koleksiyon(dizi, liste,vb)
## Break ve Continue:

### Break:
swich yapısında atmak için kullanılır.
if koşulunda koşuldan çıkmak için kullanılabilir.
bir döngüden çıkmak için kullanılabilir.
```C#
for (int i = 0; i < 10; i++) 
{
  if (i == 4) 
  {
    break;
  }
  Console.WriteLine(i);
}
```
### Continue:
Belirtilen bir koşul gerçekleştiğinde döngüdeki bir yenilemeyi keser ve döngüdeki sonraki yenilemeye geçer.
```C#
//for
for (int i = 0; i < 10; i++) 
{
  if (i == 4) 
  {
    continue;
  }
  Console.WriteLine(i);
}

//while
int i = 0;
while (i < 10) 
{
  if (i == 4) 
  {
    i++;
    continue;
  }
  Console.WriteLine(i);
  i++;
}
// 4 yazılmaz, i=4 durumunda kod devam etmez döngünün başına döner ve i=5 durumundan devam eder.
```
## Arrays(Diziler)
Diziler: Her değer için ayrı ayrı değişkenler tanımlamak yerine, tek bir değişkende birden fazla değeri toplamak için kullanılır.

!! Diziyi bildirmek için değişken türü [] ile tanımlanır. değerler, {} içerisinde virgülle ayrılmış şekilde yazılır
```C#
string[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
```
NOT: Dizi oluşturmanın birden fazla yöntemi vardır, bu yöntem sadece bir tanesi.

#### Dizi Elemanlarına Erişim:
Dizi elemanlarına index numarasına başvurarak erişilir.
```C#
string[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
Console.WriteLine(cars[0]); // Outputs Volvo
```
#### Dizi Elemanını Değiştirmek:
```C#
string[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
cars[0] = "Opel";
Console.WriteLine(cars[0]);
```
#### Dizi Uzunluğu
Dizi uzunluğu bulmak için ``Lenghth()`` özelliği kullanılabilir. Döngü kullanarak null' a gelene kadar da saydırılabilir(kötü bir ecole42 alışkanlığı).
```C#
string[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
Console.WriteLine(cars.Length);
```
#### Dizilerde Döngü:
```C#
string[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
for (int i = 0; i < cars.Length; i++) 
{
  Console.WriteLine(cars[i]);
}
```
#### Dizilerde Sıralama:
Bir çok dizi sırama yöntemi vardır, misal ``Sort()``: diziyi alfabetik veya artan şekilde sıralar.

```C#
// Sort a string
string[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
Array.Sort(cars);
foreach (string i in cars)
{
  Console.WriteLine(i);
}
 
// Sort an int
int[] myNumbers = {5, 1, 8, 9};
Array.Sort(myNumbers);
foreach (int i in myNumbers)
{
  Console.WriteLine(i);
}
```
#### System.Linq Namespace:
Min, Max, ve Sum gibi diğer dizi yöntemleri System.Linq ad alanında bulunabilir.
```C#
using System;
using System.Linq;

namespace MyApplication
{
  class Program
  {
    static void Main(string[] args)
    {
      int[] myNumbers = {5, 1, 8, 9};
      Console.WriteLine(myNumbers.Max());  // returns the largest value
      Console.WriteLine(myNumbers.Min());  // returns the smallest value
      Console.WriteLine(myNumbers.Sum());  // returns the sum of elements
    }
  }
}
```
## Multidimensional Arrays(Çok Boyutlu Diziler)
Çok boyutlu dizi temelde dizilerin dizisidir.

.

.

.

## C# Methods():
Methodlar belirli eylemleri gerçekleştirmek için kullanılır. diğer bir ismiyle fonksiyonlar. Methodlar yanlızca çağırıldığında çalışan bir kod bloğudur. Parametre olarak bilinen verileri bir methoda geçirebilirsiniz.(main() de bir methoddur)

```C#
class Program
{
  static void MyMethod() 
  {
    // code to be executed
  }
}
```
- myMethod() : fonksiyonun(methodun) adıdır.
- static: fonksiyonun program sınıfına ait olduğunu ve program sınıfının bir nesnesi olmadığı anlamına gelir.
- void: fonksiyonun bir dönüş değeri olmadığını gösterir.

### Call a Method(Methodu çağırma yöntemi):
```C#
static void MyMethod() 
{
  Console.WriteLine("I just got executed!");
}

static void Main(string[] args)
{
  MyMethod();
}
```
### Method Parameters:
```C#
static void MyMethod(string fname) 
{
  Console.WriteLine(fname + " Refsnes");
}

static void MyMethod1(string fname, int age) 
{
  Console.WriteLine(fname + " is " + age);
}

static void Main(string[] args)
{
  MyMethod("Liam");
  MyMethod("Jenny");

  MyMethod1("Liam", 5);
  MyMethod1(5, "Liam"); // hatalı kullanım
}
```
- Bir parametre metoda geçirildiğinde, buna argüman denir. fname prametredir, Liam argümandır.
- fonksiyonun birden fazla parametresi varsa argümanlar aynı sıra ile girilmelidir.
- parametre türü ile argüman türü farklı olmamalıdır. fname kısmına string haricinde bir argüman(örn:3.24) atayamazsınız.

### Default Parameter Value(Varsayılan Parametre Değeri):
``=`` işaretini kullanarak default parametre değeride kullanabilirsiniz.

```C#
static void MyMethod(string country = "Norway") 
{
  Console.WriteLine(country);
}

static void Main(string[] args)
{
  MyMethod("USA");
  MyMethod(); // argüman girilmezse konsola Norway basılır. 
}
```
### Return Values(Dönüş Değeri):
Fonksiyonun bir değer döndürmesini isterseniz daha önceki örneklerdeki void yerine dönmesini istediğiniz türü yazmalısınız. (orn: string)
```C#
static int MyMethod(int x) 
{
  return 5 + x;
}

static void Main(string[] args)
{
  Console.WriteLine(MyMethod(3)); // çıktı 8 olur
  int sonuc = MyMethod(5);
  Console.WriteLine(sonuc); // çıktısı 10.
}
```
### Named Arguments(Adlandırılmış Argümanlar.)
key: value dizimiyle argüman göndermek mümkündür. bu şekilde kullanımda argümanlar belirli bir sırayla gitmek zorunda değildir.
```C#
static void MyMethod(string child1, string child2, string child3) 
{
  Console.WriteLine("The youngest child is: " + child3);
}

static void Main(string[] args)
{
  MyMethod(child3: "John", child1: "Liam", child2: "Liam");
}//çıktı john olur
```
### Method Overloading(Fonksiyonların Aşırı Yüklenmesi):
Method Overloading ile birden fazla method farklı parametre türü veya sayısı ile aynı isme sahip olabilir.
```C#
static int PlusMethod(int x, int y)
{
  return x + y;
}

static double PlusMethod(double x, double y)
{
  return x + y;
}

static string PlusMethod(string name)
{
  return name;
}

static void Main(string[] args)
{
  Console.WriteLine(PlusMethod(2, 3));
  Console.WriteLine(PlusMethod(4.21, 5.7));
  Console.WriteLine(PlusMethod("ayse"));
}
```
# OOP(Nesne Yönelimli Programlama)
İşlemsel programlama, veriler üzerinde işlemler gerçekleştiren prosedürler veya yöntemler yazmakla ilgilidir; nesne yönelimli programlama ise hem verileri hem de yöntemleri içeren nesneler oluşturmakla ilgilidir.

##### OOP/Prosedürel Programlama:
- OOP daha hızlı ve yürütülmesi daha kolaydır.


#### OOP kavramlar:
- Class(Sınıf): Nesnelerin yapısını ve davranışını tanımlayan bir şablon.
- Nesne(Object): Sınıfların örneğidir. Sınıfta tanımlanan özelliklere ve methodlara sahiptir.
- Kapsülleme(Encapsulation): Verilerin ve metotların bir sınıf içinde bir araya getirilmesi.
- Kalıtım(Inheritance): Bir sınıfın başka bir sınıftan türetilmesi, böylece miras alması.
- Polimorfizm(Polymorphism): Aynı method adının farklı şekillerde kullanılması.
- Soyutlama(Abstraction): Karmaşıklığı gizleyip sadece gerekli olan kısımların ortaya çıkarılması
























