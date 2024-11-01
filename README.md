
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

- Implicit Casting (kapalı Dönüşüm) (otomatik)
  
  Daha küçük bir türü daha büyük bir tür boyutuna dönüştürme.
  
  char-> int-> long-> float->double

  ```C#
  int myInt = 9;
  double myDouble = myInt; 
  ```

- Explicit Casting (açık dönüşüm) (manuel)
  
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

- \'
- \"
- \\
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














