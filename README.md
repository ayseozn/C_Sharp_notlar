
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

Convert.ToBoolean, Convert.ToDouble, Convert.ToString, Convert.ToInt32( int), Convert.ToInt64( )

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
yanlış bir girdi

















