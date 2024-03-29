




# Token (Atom)


 - Derleyicinin anlamlandırabildiği en küçük program parçasıdır.

 - Derleyici "Tokenizing" işlemi ile kodu atomlarına ayırır.

Tokenlar aşağıdaki gibi sınıflandırılabilirler:

 1- Keywords (Anahtar Kelime) 
 
 3- Identifiers (İsimler)   	
 
 4- Constant (Sabitler) 
 
 5- Strings	
 
 6- Special Symbols
 
 7- Operators (Operatörler)				


1-Keywords: Programlama dilinde ön tanımlama yapılmış ve rezerve edilmiş 
kelimelerdir.
Bu kelimeleri bir değişken olarak tanımlayıp kullanamayız. Anahtar kelimelere
tekrar tanımlama veya atama yapamayız.

C programlama dilinde anahtar kelimeler aşağıdaki gibidir.

auto  -  double  - int  -  struct  - break -  else  - long  -  switch  - case
enum -   register  - typedef  - char  - extern -  return -  union -  const   
float  - short -  unsigned  - continue - for  - signed - void -  default 
goto -  sizeof -  volatile -  do  -  if   - static  -  while  - inline - restrict 
_Bool -    _Complex -  _Imaginary


2.Identifiers: İsimler Genel terminolojide değişkenleri, fonksiyonları 
ve dizileri tanımlamak için kullanılır.

 - Harfle veya  _ (Underscore) ile başlamalıdır.
 - Sadece harf, sayi ve _ içerebilirler.
 - Anahtar kelimeler kullanılamaz.
 - Boşluk içeremez (whitespace).
 - 31 karakteri geçmemelidir. Geçerse ilk 31 karakter kabul edilir.
 - Büyük-küçük harf duyarlılığı vardır.



 3.Constant: Const belirteci, programcının derleyiciye belirli bir değişkenin
 değerinin değiştirilmemesi gerektiğinin bildirmesini sağlar.
 Ayrıca literals olarak ingilizcede adlandırılabilir.


 
 4.Strings: Değişken tipi char yani karakter olan dizilerdir.
 TR'de "Katar" olarak karşımıza çıkabilir.


 5.Special Symbols: C programlamada bazı özel anlamları olan sembollerdir.
 Bu sebeple farklı amaçlarda kullanılamaz.

 - Brackets[]: Dizilerin tanımlanmasında ve elemanlarının çağırılmasını
 anlamlandıran semboldür.
 
 opening bracket  [
 
 closing bracket  ]

 - Parentheses() : Bu sembol fonksiyon tanımlanmasında ve fonksiyonun 
 çağırılmasında kullanılır.

 - Braces {} : Küme parantezi birden fazla çalıştırılabilir ifade içeren 
 bir kod bloğunun başlangıcını ve sonunu belirtir.  
 
 opening curly brace {
 
 closing curly brace }
 
 ```
 {// Main Block( ana block)

     {
       //Nested Blok(içsel block)
     }
 
 }
 ```

 - Comma ( , ): Birden fazla deyimin ayrımında kullanılır. Mesela fonksiyon
 çağrılırken argümanların ayrımı için kullanılır.

 - Colon ( : ) : Bir başlatma listesi adı verilen bir şeyi çağırırken 
 kullanılır.

 - Semicolon (;): Deyim sonlandırıcı olarak bilinir.Bir mantıksal varlığın 
 sonunu gösterir. Bu nedenle her bir deyimin noktalı virgülle bitmesi gerekir.

 - Asterisk (*) : Pointer değişkeni tanımlamak için kullanılır.,

 - Assignment operator( = ) : Bir değer ataması yapılırken kullanılır.
  
     - Atama Operatörü (=)

 -Pre-processor(#): Ön işlemciye verilen komutlarda kullanılan semboldür.
    - number sign 
    - sharp
    - pound sign 
    - diyez

 6. Operators: C değişkenlerine ve diğer nesnelere uygulandığında bir 
 eylemi tetikleyen sembollerdir. Operatörlerin üzerinde hareket ettiği
 veri öğelerine operant denir.
    - Side effect ( Yan Etki)
    - Sequence Point (Yan Etki Noktası)

 Tekli Operatörler:
 Sadece tek bir işlenene ihtiyaç duyan operatörler, tekli operatörler 
 olarak bilinir.  Örnek artırma ve azaltma operatörleri için


İkili Operatörler:
iki işlenen gerektiren işleçlere ikili işleçler denir. 
İkili operatörler şu şekilde sınıflandırılır:

- Aritmetik operatörler (Arithmetic operators)
- İlişkisel Operatörler (Relational Operators)
- Mantıksal operatörler  (Logical Operators)
- Atama Operatörleri   (Assignment Operators)
- Koşullu Operatörler   (Conditional Operators)
- Bitsel Operatörler  (Bitwise Operators)


#
 
 T bir tür olmak üzere :

 T x;
 
 T:değişken Türü
 
 x:değişkenin ismi
 
 [Tür] [isim] = İlk değer ifadesi:
 
 İnitializer expression:ilk değer ifadesi
 
 Not: Initialization is not a assignment (ilk değer ifadesi bir atama 
 değildir.)

 y = 5; // Bu bir atamadır (assignment).
 
 int y = 5; //Bu bir ilk değer ifadesi. (initialize).

 #
 
# Storage Duration (Ömür)

 - Automatic storage class
 
 - Static storage class
 
 - Dynamic storage class


 Automatic storage duration: Bu nesneler, programın akışı programın 
 çalışma zamanında bir fonksiyona girdiğinde bunlar belleğe yerleşir. Programın
 akışı o koddan çıktığında bellekten boşaltılır.
 örnek olarak bir fonksiyonda tanımlanan int bir değişkene atanan bir değer
 o fonksiyon her çağırıldığında belleğe yerleşir ve o fonksiyondan çıkarken
 o değişkenin bellekteki yeri boşaltılır.
 
 #### TANIMSIZ DAVRANIŞ
 
```
   -> Otomatik ömürlü değişkenler'e ilk değer ataması yapılmazsa hayata
   belirsiz değer (Garbage Value) ile başlar. Eğer değişken bu değeri ile
   kullanılırsa tanımsız davranışa yol açar.
```

 - Static storage class: Programın daha çalışmaya başlamasından, yani 
 main fonksiyonu çalışmaya başlamadan önce çalışmaya başlarlar.
 Programın sonuna kadar da bellekde hayatları devam eder.

 - Statik ömürlü değişkenlerde ilk değer ataması yapılırken sabit ifadesi
 olması gerekir.
 
 Bir nesne Global Değişken ise statik ömürlüdür. Local değişkenler
 otomatik ömürlüdür. Ancak static anahtar kelimesi ile tanımlandığında static
 ömürlü olur. Static ömürlü değişkenler hayata 0 değeri ile başlarlar.
 

 -> Static ömürlü değişkene ilk değer başlatması yapılırken sabit ifade 
 kullanılmalıdır.
 
 	int x = 10 + 20;// global alanda yazılan bu kod kabul görür.
 	int y = x;// ancak bu kod hatalıdır çünkü y 'ye değişken ilk değer
	 ataması yapılmaya çalışılmıştır. 



 
 **Not:** Global değişkenler static ömürlü olmak zorundadır. 
 Ancak lokal değişkeni static yapabilmek için başına static anahtar 
 kelimesini eklememiz gerekir.


```
 #include <stdio.h>

 int g=7 ;// global değişken 
 // global değişken olarak atanan g programın tamamen çalışması bitene kadar
 bellekte yer almaktadır.

 int main()
 {
 
 }
 
 void func()
 {
   int X = 10;
   // local variable 
   // yerel değişken

   /* bu fonksiyon her çağırıldığında x değerine 10 ilk değer 
   ataması yapılarak bellekte yeri oluşturulur. Fonksiyon bittiğinde
   x değeri bellekten silinir.*/
 }
 void func()
 {
   /*eğer bir fonksiyon içerisinde static bir değer tanımlaması yapmak 
   istiyorsak aşağıdaki gibi yapılır.
   static int x = 1; */
   // burada biz "static lokal değişken" tanımlamış olduk

 }

  void func()
 {
   static int x = 10;
   x += 10;
   /*bu fonksiyon ilk çağırıldığında x değişkeni statik lokal değişken
   olarak tanımlanıp ilk değeri verilir ve her çağırılmada tanımlaması 
   tekrar yapılıp ilk değeri verilmez. Yani diğer çağırılmalarda 
   tanımlama kodu işleve girmez.*/

 }
 ```
 **Not:** statik ömürlü değişkenlere ilk değer verilmeden tanımlanırlarsa eğer
 hayata 0 değeri ile başlarlar. 
 Ancak otomatik ömürlü değişkenlere ilk değer verilmezse eğer buna belirsiz 
 değer "garbage value", ya da "indetermined value" denir.
 Eğer bu değişken belirsiz değer halinde kullanılırsa 
 tanımsız davranış "undefined behavior" olarak adlandırılır.

 - Behavior 
 
 - Defined behavior "tanımlı davranış"
  
 - Undefined behavior "tanımsız davranış"

Undefined-Behavior: C programlama dilinde "optimizing compiler" söz
konusu olduğu için aslında biz derleyiciyle şöyle bir anlaşma yapıyoruz. 
Benim yazdığım kodu daha hızlı çalıştırabilecek şekilde optimize ederek 
makine diline optimize ediyor. Ancak bunu yaparken de bir garanti istiyor.
Yazılan kodunda undefined behavior olmaması gerektiği konusunda. 
Olduğu takdirde bu durumu optimize ederken tanımlayamadığı halde 
çalıştırdığı için çeşitli problemlerle karşılaşabiliyor.

Bu sebeple mümkün olan her yerde değişkenlere ilk değer ifadesi verilmelidir.



#


 declare-declaration //Bildirim
 
 define-defination // tanımlama

 Bildirim ismin ne türde oldluğunu anlatan cümledir.
 Eğer bildirim sonucunda derleyici bellekte yer alıyorsa bu tanımlamadır.


 #
 
 # Scope (kapsam)

 Bir tanımlayıcının kapsamı, tanımlayıcının (Identifiers) doğrudan 
 erişebildiği programın bir parçasıdır. C'de tüm tanımlayıcılar kapsamlıdır.

 File scope: Bir tanımlayıcının dosya kapsamı, dosyanın başlangıcından
 başlar ve dosyanın sonunda sona erer.

 Block Scope: Bir tanımlayıcının kapsamı, "{" bloğun açılmasıyla başlar ve "}"
 bloğun bitmesiyle sonunda sona erer. Blok kapsamına sahip tanımlayıcılar kendi blokları
 içinde yereldir.
 
```
 #include <stdio.h>

 int x; 

 int main()
 {

 int x; 

 /*  Burada bir programda aynı iki isim kullanılmış ancak
 kapsamları farklıdır. Bu durumda program sentaks hatası vermez ancak
 kullanım açısından doğru bir kullanım değildir. */
 
 }
 
```
 

 # Look Up(isim arama)


```
  #include <stdio.h>
  
  int x = 20;

  int main()
  {
 	 int x = 10;

	  printf("x=%d\n", x);
  
  /*Burada isim arama söz konusu olduğu için
  printf ile x aranmaya başlar. Bu arama yukarı doğru gerçekleşir ve
  ilk olarak kendi bloğunun içerisinde yukarı doğru arama başlar. Eğer 
  aranan değişkenin ne olduğu bulunursa arama anında biter ve bu değişkenin 
  ne olduğu bulunan değer ile yazdırılır. Yani ekranda x = 10 görürüz.*/
  
  }
``` 

   #### Örnek:
  
  ```
  #include <stdio.h>
  
  int x=36;

  int main()
  {


  printf("[1] x=%d\n", x);
  int x =10;
  printf("[2] x=%d\n", x);
        {


    int x=89;
    printf("[3] x=%d\n", x);


        }
   printf("[4] x=%d\n", x);


  }
  ```
  
  Ekran Çıktısı:
  
```
  [1]=36
  [2]=10
  [3]=89
  [4]=10
```

- Peki yukarıdaki kod parçasında biz statik alanda iken global alanda olan x e ulaşmak istersek bunun bir çözümü var mı? (değişken gölgeleme)
	- C'de bunun bir çözümü yoktur. Buna değişken gölgelenmesi olarak adlandırabiliriz. Ancak C++ da vardır. 


 #### Örnek:
  ```
  #include <stdio.h>

  int main()
  {
  
  int printf=0;
  printf ("selam");

  // Program printf'i main fonksiyonu içerisinde int olarak tanımlandı.
  Sonra printf fonksiyonunu ilk algıladığında keywords olmadığı için
  name look-up yaparken kendi kapsamında arama yapar. Bu kapsamda printf 
  int olarak tanımlandığı için bu kod hata verir.
  Normalde int olarak tanımlanmasaydı printf'i  ilk okuduğunda isim araması 
  yaparak standart kütüphaneye ulaşarak printf fonksiyonunu çağıracaktı.

  
  }
```
  #### Örnek:
  
  ```
  #include <stdio.h>

  int main()
  {
  
  int printf=20;
  printf=30;

  // bu kodda sentaks hatası yoktur. düzgün bir şekilde çalışır.


  
  }
  ```
  #
  
 # Function (Fonksiyonlar) "method, procedure, yordam, altprogram"
 

 
  - to define a function 
  - to call a function
  - to declare a fuction


  double func (int x , int y);

  // Burada "double", fonksiyonun geri dönüş türü (the type of return value).
  
  //"func", fonksiyon ismi.
  
  // "Parantezler", parametre parantezi.
  
  //int x, int y ise parametre değişkenleri (formal parameters) 


  Örnek olarak;
  

  int func(void)   ile int func() aynıdır. Buradaki void fonksiyonun 
  parametre değişkeninin olmadığı anlamına gelir. Void kullanılmasada 
  fonksiyonun parametre değişkeni yoktur.
  Ancak Void kullanılmasının C'de bir avantajı vardır.
  ilerleyen derslerde göreceğiz.

  #
  
  statement

  - expression statement (ifade deyimi)
  - compound statement (bileşik deyim)
  - null statement (boş deyim)
  - control statement (kontrol deyimi)


  - z = 10 (bu bir ifade) "expression"
  
  - z = 10; (bu bir deyim) "expression statement"


 Compound statement örnek olarak
 
  ```
 if(x > 5)
 {

	 ++a;
	 x = 5;

 // if koşulu gibi block içerisindeki deyimlerin bütününe compound (bileşik) 
 deyim denir. Bir blok içerisinde olduğu için bu böyledir.

 }

  ```
 null statement:  ";" kendisinden önce bir ifade olmadan tek başına
 kullanılırsa deyim olur ve null statement denir.
 
 Control statement: Önceden belirlenmiş bir sentaksı olmalı ve en az bir
 anahtar kelime içermelidir.
 - if statement
 - loop statement
 - while statement
 - for statement
 
 #

 Return statement
 
 a-) Bir fonksiyonun kodunun çalışmasını sonlandırmak için
 
 b-) Fonksiyonun kendisini çağıran koda (iletecek ise) bir değer iletmesini
 sağlamak için kullanılır.

 return ; // yalın (ifadesiz) return deyimi
 
 return exp; // ifadeli return deyimi

 **Not:** 
 
  ```
	 void func(void) 
	 {
	 	yukarıdaki fonkiyonun adlandırılmasında ilk void fonksiyonun bir geri 
	 	dönüş değerinin olmadığı anlamına gelir. Parantez içerisindeki void ise
		 fonksiyonun parametre değişkeninin olmadığı anlamına gelir.
 	}

	 //void function: A function doesn't have return value. Geri dönüş mekanizması
 	   ile bir değer gönderilmeyeceği anlamına gelir.
	   
  ```

 örnek olarak :
 
  ```
  
 void func (void)
 {
 // statement
 //statement
 
  if(exp)
      return ;// bu bir yalın return statement'dır.
      
 //statement

 } 
 
```
 **Not:** yalın return statement'ı asla geri dönüş değeri olan bir fonksiyonun 
 içerisinde kullanamayız. Sadece void fonksiyonu içerisinde kullanılır.

 İfadeli return:

 return exp;
 
 Fonksiyonumuzun bir geri dönüş değeri olması gerekiyor. Kullanıldığında 
 yine fonksiyon sonlandırılır ancak bu sefer fonksiyon sonlandırıldığında 
 bir geri dönüş ifadesi gönderilir. Geri dönüş ifadesi genelde 
 fonksiyonda hesaplanır ve geri dönüş değeri olarak verilir.

 return 0; // bu kodda geri dönüş değeri 0'dır.
 
 #### UNDEFINED BEHAVIOR
 
```
 int func (void)
{
	Eğer bir fonksiyonun geri dönüş değeri türü var ise fonksiyonun bir geri
	dönüş değeri olması lazım. Eğer yoksa ve geri dönüş değeri kullanılıyorsa
	Undefined behavior (tanımsız davranış) olur.
}
```

**Not:** C programlama dilinde bir fonksiyon içerisinde bir fonksiyon 
tanımlanamaz. Tüm fonksiyonlar global isim alanında olmalıdır.
Yani C'de nested func ve local func yok.

- Ayrıca C'de global isim alanında bir fonksiyon çağırılamaz.

Test function: Return statement test fonksiyonlarında soruya cevap
vermek amacıyla da kullanılır. Evet/hayır gibi sorular.
	- query function

- Genellikle C'de _bool yerine int geri dönüş değerleri kullanılır.
Eğer geri dönüş değeri sıfır dışı bir değer ise (non-zero value) lojik doğru
anlamına gelmektedir. Eğer sıfır değeri gönderilmişse yanlış olduğu anlamına 
gelir.

- Fonksiyonu çağıran kodun, çağırılan fonksiyonun bir geri dönüş değeri 
olmasına karşın bu geri dönüş değerini kullanılmamasına "to discard the return
value" denir.

- Başarı bilgisi olarak kullanılabilir. Herhangi bir hata durumunda koşul 
ifadeleri ile hata dönütü sağlayabilir.

Eğer toparlarsak bir fonksiyonun geri dönüş değeri neler olabilir?

- Hesaplanan bir değer
- Test fonksiyonları
- Tamamlayıcı bir değer
- Başarı bilgisi
- Ya da hiç olmayabilir (void func)

#

# Fonksiyon çağrıları (to call a function)

Parantez operatörü ile sağlanır.

func() -> bu bir ifadedir. 

Eğer çağırılan fonksiyonun parametre 
değişkeni yoksa bu parantezin içerisine bir argüman yazmak sentaks hatasıdır.
Parametre değişkeni olduğunda ise her bir değişken için kopyalanacak, 
değeri oluşturacak ifade yazılır.

Fonksiyon çağırılırken parantezin içerisine yazılan değerlere argüman denir.

- argument(arguman)
- actual parameter

func(10,20) // expression (ifade)

func(10,20); // statement(deyim)

**örnek:**

```
int main()
{

int x = 10;
int x = 45;
max (x + 30, y - 10);

//Burada max fonksiyonunun argümanı (40, 35)'dir.

}

```
- Aynı geri dönüş değerini elde edeceğimiz şekilde bir fonksiyonu birden 
fazla kere çağırmak kötü kod'dur.

call by value (değerle çağırma)

call by referance (referansla çağrı)

C dilinde tüm fonksiyon çağrıları call by value (değerle çağırma)'dır.
Fakat bu özellik dilden dile değişir.


Call by value olduğuna dair bir örnek:

```
int foo(int x)
{
x = 99;
return x;
}

int main()
{
int x = 10,y;
printf(" x = %d\n ",x);
y = foo(x);
printf(" x = %d\n ",x);
}
```
// Yukarıdaki programda ikinci printf değeri ile yazdırılan x değeri 10'dur.
çünkü x Değeri foo fonksiyonundaki a değerine atanmaz kopyalanır.
Yani foo(x) ifadesi 99'dur. x gönderilen bir ifade ve foo(x) gelen ifadedir.



# Standart Kütüphane (Standard Library)

- Printf standart bir C fonksiyonudur.
- Standart kütüphane alt birimlere bölünmüştür (module).

Variadic Function: Fonksiyon çağırılırken parametre sayısının değişken olduğu fonksiyon türüdür.

Tanımlanma şekli:

```
void func(int x, int y,...)
{
	//Variadic Function
}
//Yukarıdaki tanımlanan fonksiyona en az 2 tane argüman gönderilebilir. 

```
Not: Bazı programlama dillerinde "Default Argument" kavramı vardır. Yani
argüman gönderilmediğinde varsayılan argümanlar kullanılır.

- C'de neler yok !

```
- Nested Function
- Function Over Loading: Bir foksiyonu 2 farklı tür için kullanamazsınız.
Mesela abs fonksiyonunu hem int hem double türü için kullanamazsınız.

```
# CONSTANT (SABİTLER)

- İnteger  Constant ( Tam sayı sabitleri)
- Floating Constant ( Gerçek sayı sabitleri)


Sabitlerin türleri olması gerekir.

- Tam sayı sabitlerinin yazımında 3 farklı sayı sistemi kullanılabilir.
      - Hexadecimal (Onaltılık sayı sistemi)
      - Decimal     (Onluk sayı sistemi)
      - Octal       (Sekizlik sayı sistemi)

x=123; //decimal

x=0123; //octal

x=0x13; //hexadecimal

**Sabitlerin Türleri:**

- Signed int => 783
- Unsigned int => 783U

- Signed long => 7834L ya da 7834l
- Unsigned long => 7834UL -ul

- Signed long long => 7833LL
- Unsigned long long => 7833LLU -ULL

- Float
- Double
- Long Double


#### UNDEFİNED BEHAVİOR

```

İşaretli tamsayı türlerinde yapılan işlemlerde taşma durumu tanımsız davranıştır.


```

Gerçek Sayı Türleri Gösterimi:

- Float -> 2.3F
- Double -> 3.48, 5. , 5.0, .5
- Long Double -> 2.3L

**Not:** Nokta içeren sabitlerin türü double'dır.


Scintific Notation:

Aşağıdaki değerler double türüne aittir.

   - 2.3e5----> 2.3 x 10^5
   - 0.5e-3 --->0.5 x 10^-3

# KARAKTER SABİTLERİ (STRİNG LİTERALS)

C'de karakter sabitlerinin türü int'dir.

"Rasit" --> String Literals

- 'A' Bu karakter, sistemde kullanılan karakter kodlamasında (character encoding)
gerçekleşerek bu karakterin kod numarası tutulur.

'A'---> 65 --ASCII

**Not:** ASCII karakter kodlamasında büyük harf ve küçük harf sıralaması tek bir blok halinde değildir.
Sebebi ise büyük harf ile küçük harf arasındaki sayı farkını 32 yani 2^5 yapabilmektir. 
Böylece bitsel işlemlerde büyük - küçük harf değişimi tek bir biti set - reset yapılarak sağlanabilmektedir.

- Karakter kodlamalarında, harf karakterine Alphabetic Character,
Rakam kodlamalarına ise Numeric/Digit Character denilir.
Alpha-Numeric Character ikisini içeren bir kümedir.

- Control Character: Kontrol karakterleri görüntüsü olmayan özel araçlarla kullanılan karakterlerdir.
Mesela Space, Enter gibi.

- Printable Character: Görüntüsü olan karakterlerdir.

- Punctation Character: Görüntüsü olan ama Alpha-Numeric olmayan karakterlerdir.
	- Mesela . , ! ' ^ gibi karakterler.


- Escape (Kaçış) 
	- Escape Sequence (Kaçış Noktası)

 Bir kodlamada eğer bir karakter özel bir anlamda kullanılıyorsa o karaktere "escape" denir.
 
 \ --> escape olarak kullanıyoruz.
 
 '\'  ---> Yani biz tırnak içerisinde ters bölü yazdığımızda bu ters bölü karakterinin kodu değil
 sadece escape olduğunu ve ayrı bir kurala göre değerlendirilmesi gerektiğini anlıyoruz.
 
- '\a' --> alert(bell)
 
- '\t' --> horizantal tab
 
- '\v' --> vertical tab
 
- '\n' --> new line
 
- '\r' --> carriage return
 
- '\f' --> form feed
 
- '\b' --> back space
 
- '\o' --> null character
 
- '\'' --> single quote
 
- '"' veya '\"' --> double quote
 
- '\' veya '\\' --> backslach
 
- '\?' veya '?' --> question mark
 
 
 # İNPUT-OUTPUT OPERATİON
 
 
- Bir program çalışır haldeyken dış dünya ile veri alış-verişi 
sağlamasına denir.
    - standard input stream (klavye)
    - sandard output stream (consol a  bağlı)
    - standard error stream

- Bir giriş-çıkış işlemi 2 farklı şekilde yapılabilir.
     - Formatted
     - Unformatted

Formatsız: Gönderilen ya da alınan kodları olduğu gibi almaya veya göndermeye yönelik kullanımdır.

Formatlı: Girişin ya da çıkışın insanın anlayacağı formata getirilmesine denir.

- printf ve scanf fonksiyonları formatlıdır.

- Çıktı alınırken formatın türü de önemlidir.

Mesela bir sayı yazdırılacağı zaman hangi sayı sisteminde olduğunu bildirmek bir format bildirimidir.

Output Width(yazma alanı genişliği): Yazma alanı genişliği bir yazı veya rakam dizisini yukarıdan 
aşağı sıralarken hizalamaya yarayan kavramdır.

Fill character -> Bu hizalama yapılırken kullanılan karakterdir. Genelde boşluk karakteri kullanılır.

# PRİNTF FONKSİYONU

Printf fonksiyonu stdio kütüphanesinde bildirilen formatlı çıkış fonksiyonudur.

Tanımlanma şekli:

int printf(const char*p,...);

- C'de yazılar dizilerde tutuluyor. Dizilerin fonksiyonlara gönderilmesi "Call By Referance" biçiminde olmak zorundadır.
Bu yüzden bir fonksiyona bir yazıyı göndermenin yolu yazıyı tutan adresi göndermektir.

Printf fonksiyonu tanımlanırken *p gönderilecek olan adresi ifade etmektedir. 

Yani bir pointer olmasının sebebi bir yazıyı isterken aslında yazının tutulan char dizisinin adresini istiyor olmasıdır.

... ise bu fonksiyonun variadic olduğunu ifade etmektedir.

Printf fonksiyonun sayı sistemlerinin formatları:

%d -->decimal--int türden

%0  --> Octal

%x  --> hexadecimal--sign/unsign int türden

%Ld --> long türden 10 luk sayı sistemi

%u  --> unsigned int

%f  --> double  ve float türünde

%lf --> long double veya float türünde


```
#define _CRT_SECURE_NO_WARNINGS
#include <stdio.h>


int main()
{
    int x = 987;
    printf("%d", printf("%d",printf("%d",x)));
    /*Bu kodun çalışma şekli ilk olarak en içteki printf fonksiyonu çalışır.
    Yani ekrana 987 yazılır. Bir dıştaki printf fonksiyonu bi önceki fonksiyon çalışırken ürettiği değeri yazar.
    Printf fonksiyonu yürütüldüğünde ekrana kaç karakter yazdıysa, yazdığı karakter sayısını üretir. Yani ekrana 
    3 basamaklı olduğu için 3 sayısı yazılır. Bir kez daha yürütüldüğünde 3 sayısı 1 karakterli olduğu için 
    1 sayısı yazdırılır. */
    - Ekran çıktısı: 
    		98731     olur.

}

```


-  %c formatı ASCII'ye göre bir karakterin sayı karşılığını girerseniz eğer o karakteri ekrana yazdırır.

```
int main()
{
	int x;
	printf(" %c", 65);
}

// Ekrana yazılan değer A olur. 
```

# SCANF FONKSİYONU

int scanf(const char *p, ...);

- Scanf fonksiyonu call by referance olmak zorundadır.
	- Örnek olarak scanf("%d", &x); &x kullanılmasının sebebi call by referance olmasıdır.

- Scanf fonksiyonu Satır Tamponlu (Line - Buffered) yapıdadır.
	- Yani new-line karakteri gelene kadar devam eder.

- Örnek olarak :

scanf("%d", &x); Yazıldığında ekrana giriş olarak 1234abc yazıldığında 
ekrana sadece 1234 yazılır. Çünkü %d formatı onluk sayı sisteminde bir tam sayı girilecek demektir.

scanf'in geri dönüş değeri başarılı olup olmadığını anlatmaktadır.

**Uyarı:** Scanf çağrısı yapıldığında standard inputun buffer'ı boş değil ise giriş için bir karakter girilmesi
beklenmez. Bu durumda scanf, standart inputun bufferındaki karakterleri kullanır.


 # OPERATÖRLER (OPERATORS)

- İşleçler
- İşlemci

- C'de 45 tane operatör vardır.
- Sizeof hem anahtar sözcük hem de operatördür.

- a + b --> burada + bir operatör, a ve b operanttır.
- unary operator   --> tek terimli operatör
- binary operator  --> çift terimli operator
- ternary operator --> 3 terimli operator

- a + b  ----> + operatorü ortada olduğu için bu operator burada infix konumda kullanılmıştır.
- !x   ----> burada ! operatörü başta olduğu için prefix konumunda kullanılmıştır.
- y++  ----> burada ++ operatörü sonda kullanıldığı için postfix konumunda kullanılmıştır.

Örnek olarak:

- a+b --> binary infix
- !x  --> unary prefix
- y++ --> unary postfix


- Her operatörün ürettiği bir değer vardır.(Operators generate value),(generate yerine yield,return kullanılabiliyor.)
8*5=40 --> Burada 40 değeri çarpma operatörünün ürettiği değerdir.

- Constraint = Operatörlerle ilgili uyulması gereken kurallara verilen ad'dır.
- Constant(sabit)
 

#### Operatör Önceliği

- precedence
- priority

- Operatör önceliği hangi işlemin daha önce yapılacağını belirleyen kurallar değildir.
- Operatör önceliği bir ifade içinde birden fazla operatör yer aldığında hangi operatörün 
ürettiği değer, hangi operatörün operantı olacağını belirliyor.


# OPERATÖR ÖNCELİK TABLOSU

```

1-)  ( ) [ ] . ->
2-)  + - ! ~ sizeof  type & *0 ++ -- (Sağdan sola)
3-)  *   /  %
4-)  + -
5-)  >>  <<
6-)  > >= < <=
7-)  ==   !=
8-)  &
9-)  ^
10-) |
11-) &&
12-) ||
13-) ? : (sağdan sola)
14-)=  +=  -=  *=  /=  %0  &0  |=  ^=  >>=  <<=  (sağdan sola)
15-) ,

```

-Bazı operatörlerin C'de iki anlamı vardır.

"+" ---> +x veya a+b , +x işaret belirtir. a+b 'deki + ise toplama işlemi.

"*" ---> *ptr (Pointer), a*b(çarpma)

"&" ---> &x (adres tanımlama) , x&y (bitsel işlemler)


- Associativity (öncelik yönü)
   - left associative (soldan sağa)
   - right associative (sağdan sola)

- Side Effect (Yan etki) 
    - !x burada lojik değil operatörünün yan etkisi yoktur. Yani x değişkeninde herhangi bir değişiklik olmaz.
    - ++x burada artı artı operatörünün bir yan etkisi vardır ve x'i 1 artırmıştır.
   
   
   
   **Addition Subtraction (+,-)
   
   - Binary infix operatörlerdir.
   - Ürettikleri değer toplamı ya da farkı olur.
   - Yan etkileri yoktur.
   
   
   #### UNDEFİNED BEHAVİOR
   ```
   
   İşaretli türlerde taşma tanımsız daranıştır.
   
   ```
   
   
   İntegral Promotion: Tam sayıya yükseltmek demektir.
   
   
   **Multiplicative Operators
    
  - "*"  multiplication
   
  - " / " division
  
  - " %"  module
  
   
   - Binary infix operators. (ara ek)
   - Yan etkileri yok.
   
   **Dikkat:** Mod operatörünün operantları gerçek sayı türden olamaz.
   
   - Eğer ekrana %3.5 yazdırmak istersek % operatörünün escape olduğunu unutmamak lazım.
   
   ```
   	double dval=3.5;
   
  	 printf("%% %f",dval);// ekran çıktısı %3.5
   ```
   
   #### UNDEFİNED BEHAVİOR
   
  ```
	  Bölme ve mod operatörünün sağ operantı 0 olamaz. Olması durumunda tanımsız davranış olur.
  
  ```
 
  
  
  - İncreament (++) plus plus
  - Decrement  (--) minus minus
  
  - Ön ek olarak ve son ek olarak kullanılabilirler.
   	- ++x veya x++ şeklinde.
  
  - Bu operatörün operantı Lvalue olmak zorundadır.
  	- "++x" ifadesi rvalue'dür.
   
  - Yan etkisi vardır.
   	- ++x önce x'i artır sonra x'i kullan demek.
   	- x++ önce x'i kullan yan etki noktasına gelince x'i artır demek.
   
  #### Karşılaştırma Operatörleri
   
   - İlişkisel operatörler
   - Relational Operators
   - Comparison Operators
    
   <         >          <=           >=
   
   **Lojik Karşılaştırma Operatörleri
   
  " == "  
   
  " != "
   
  " > " greater
  
  " < " less
  
  " >= " greater than
  
  " >= "less than
  
 - Binary infix Operators
 - Yan etkisi yok !
 
 
 
 - C dilinde karşılaştırma operatörleri int türünden değer üretirler. 
 Diğer dillerde Bool türünden değer üretilir.
 
 örnek:
 ```
 x = y == z; // Burada == operatörü = operatöründen daha önceliklidir. Aşağıdaki ifadeyle aynıdır.
 
 if(y==z)
 
    x=1;
    
 else 
 
    x=0;
    
  ```
  
  #
  
  if(x==5) koşulunu daha güvenli kullanmak istersek 
  
  if(5==x) olarak da kullanılabilir.
  
  #
  
  **Logical Operators
  
  - Önermeler
  
  - lojik değil işlemi (!) ( logical not)
  - lojik ve   (&&)        ( logical and )
  - lojik veya (||)        ( logical or )
  
  
  
  - Short Circuit Behavior (kısa devre davranışı)
  
  Kısa devre davranışına örnek olarak:
  
  expr1 && expr2 // eğer expr1 değişkeni 0 ise expr2'ye bakılmaksızın sonuç olarak 0 değeri üretilir.
  expr1 || expr2 // eğer exp1 değişkeni non-zero bir değer  ise expr2'ye bakılmaksızın 1 değeri üretilir.
  
  
**Uyarı: Lojik && ve || operatörlerinde kısa devre davranışı var olmasına karşın,
 bitsel & ve | operatörlerinde kısa devre davranışı söz konusu değildir.
 
 
 - De Morgan Kuralları:
 
         !(p && q) = !p || !q
	 
         !(p || P) = !p && !q
   
   
  
  
   #### Atama Operatörleri
   
    =      atama operatörü
   
   +=       -=      *=      /=             ----> (İşlemli Atama Operatörleri)
   
   %=     >>=     <=     &=     ^=    |=    ----> (Compound Assignment Operators)
   
   - C dilinde atama operatörleri de diğer tüm operatörler gibi bir değer üretir.
   - Atama operatörünün ürettiği değer nesneye atanan değerdir.
   x = y  ifadesinin ürettiği değer, x'e atanan değer olan y'nin değeridir.
   
   
   örnek:
   
    
   ```
    int x = 10, y = 24, t = 5, z = 7;
    x += y += t *=z %= 5;
    // Atama operatörlerinde işlem önceliği sağdan sola olduğu için sağdan başlanarak sola doğru işlemler yapılır.
   //Sonuç olarak x = 44 , y = 34 , z = 2 , t = 10 değerleri atanmış olur.
   ```
  
    
   **Virgül Operatörü
    
  - Öncelik tablosunda en son sırada. 
  - Binary infix 'dir.
  - Virgül operatörüyle oluşturulmuş ifadeler C dilinde R value olur.
    
  - Sequence Point (Yan Etki Noktası) 
           - sequencing
           
     Bir ifade ile oluşacak yan etkilerin gerçekleşeceği nokta.
     
    Yan etki noktaları:
    - Deyim sonu yani ilk noktalı virgülün olduğu nokta bir yan etki noktasıdır.
    - Bazı operatörlerin operandlarının değerlendirilmesinden sonra.(lojik ve (&&), lojik veya(||), ternary op. , virgül operatörü)
    - Kosul operatorlerinde sonra (if, else if,while )
    
    
   Örnek olarak :
   
```  
  int  y = 0;
    y++ || f(y); // yandaki deyimde lojik veya bir yan etki noktasına sahip olduğu için y, 1 artırıldıktan 
    sonra f fonksiyonuna y değeri 1 olarak gönderilir.
    
```
   
   Örnek olarak :

```
        int x = 10, y;
        x++, y=x; // Bu deyimde virgül bir yan etki noktası olduğu için x değeri 1 artırılıp 
        11 olduktan sonra y değişkenine 11 olarak atanır.
```
    
    
    
   #### Undefined Behavior
   
    
    ``` 
     Bir yan etki noktasından önce bir yan etkiye maruz kalmış nesneyi tekrar kullanırsak bu tanımsız davranış olur.
     
     y = x++ + +x;/* burada x son ek olarak ++ operatörü kullanılarak 1 artırıldığı için x kendi değeriyle yan etki 
     noktasına kadar kullanılarak yan etki noktasında artırılacaktı. Ancak yan etki noktasına gelmeden x bir kez daha kullanıldığı için 
     tanımsız davranış görülüyor.*/
     
     y=x++ + x++;
     x = ++x ;
    ```
     
   **Bir Mülakat Sorusu:
     
```
     int x = 10;
     int y = (x = 7) + x;
     /*Burada yine x'e 7 ataması yapılarak bir yan etkisi vardır. Ancak bu yan etkinin oluşması için kod, yan etki noktasına ulaşmalı.
     Bu kodda yan etki noktasına ulaşılmadan x tekrar kullanılmıştır.*/
```
     
     
  - Her operantın ürettiği değer gibi virgül operatörü de bir değer üretir.
    		- Virgül operatörünün ürettiği değer sağ operantın ürettiği değerdir.
     
  örnek:
     
```
      
      int a, b = 10, c = 20;
      a = (b, c); //Burada a'ya atanan değer 20'dir.
      
```
      
   Block Elimination:
   
  
      if (x>20)
      {
      	a++;
      	b++;
      }
      
yerine 
  
      if(x > 20)
         a++, b++;
	 
Bu bir block elimination örneğidir.
      
      
     
      
  **Dikkat :** Gerçek sayı sabitlerinin yazımında nokta yerine yanlışlıkla virgül karakterinin yazılması çok tipik bir hatadır.
      
      
  Örnek Bir Mülakat Sorusu:
       
```
       double x=2.5;
       
       while(x < 5, 0)  /*Burada tam sayı yazılırken nokta yerine virgül kullanıldığında, virgül operatörünün 
     			  sağ operantı değer üreteceği için while,sonsuz döngüde alır.*/
       {
       		//kodlar
       }
       
```
	
  Örnek:
      
      
       ```
      func(x, y); // Burada fonksiyona 2 argüman gönderilmiş.
      func((x, y)); // Burada ise fonksiyona 1 argüman gönderilmiş. Parantezin içerisindeki virgül operatörünün sağ operantı gönderilmiştir.
      
       ```
      
      
      
      
  # Değer Kategorisi (Value Category)
      
  L Value: Bellekte o ifadenin bir yere karşılık geliyor olması demektir. Sol taraf olan ifadeler nesne gösteren ifadelerdir.
  	 Bu ifadeler adres operatörünün operantı yapılabiliyor. Yani bu bellekta kalıcı bir verlığa ilişkin yeri temsil ediyor.
      
  R Value:  Bir değere sahip olabilmekle birlikte, bellekte bir yere karşılık gelmiyor. Yani bu ifadenin değeri runtime'da hesaplanıyor 
  	olabilir ama o ifade varlık için ayrılmış bellek bloğuna karşılık gelmiyor.
      
   Nasıl anlayabiliriz: Adres operatörünün (&) operantı yapabilirsiz. Eğer oluyorsa L value olmuyorsa R value'dur.
      
      
  # Kontrol Deyimleri (Control Statement)
     
   - İf statement
   - While statement
   - Do while statement
   - For statement
   - Switch statement
   - Goto statement
   - Return statement
   - Break statement
   - Continue statement
     
     
     
     **İf Statement
     
     if(expr) // Conditional expression
     
 		 Statement; //True Path (body)
	 
      Hatırlatma: Lojik değil ifadesinin bir yan etkisi yoktur.
      
      
       ```
      if(x != 0)
          ++a;
	  
	  
      if(x)
          ++b;
	   
	   /* Yukarıdaki iki if'in işlevi aynıdır. */
	   
      
      
      if(x == 0)
          ++b;
	  
	  
      if(!x)
          ++b; 
	  
	  /* Yukarıdaki iki if'in işlemi de aynıdır. */
      
       ```
       
       Örnek yazım şekilleri:
       
      
       ```
       
     --->  if (a = func(), a > 10)
       {       }
       
       ile
       
       a = func();
       if(a > 10)
       {  }
       
       aynıdır.
       
       
     --> if((x = func) < 10)
         {    }
	 
	 
       ```
       
       
       - C dilinde Koşul ifadelerinde yapılan en sık yazım hataları:
       
       
       ```
      
       --> if(x == 5) yerine if(x = 5) yazmak.
       Lojik eşit yerine atama operatörü kullanıldığında x 'e atanan değer yani 5 üretilir.
       if koşul ifadesi olduğu için sorulan soru 0 veya 0 dışında bir değer olduğu için
       bu durumda sıfır dışında bir değer olarak algılar ve x değeri 5 olsa da olmasa da
       if'in içine girilir. Bu hatadan kaçınmak için if(5 == x) şeklinde kullanım söz konusudur.
       
       --> if(5 < x < 20)
       Doğru yazımı if(x > 5 && x < 20) olacaktır.
       Matematiksel notasyon şeklinde yazıldığında ise derleyicinin algılama şekli operatör öncelik sırasına göre
       (5 < x) < 20 olacaktır. Bu değer de her zaman doğru olarak algılanacağı için ve sentaks hatası olmadığı için 
       problemli bir durumdur.
        
       --> if(dval > 4, 5) // burada yazılmak istenen gerçek sayı nokta ile değil de virgül operatörüyle ayrıldığı için
       ve virgül operatörü sağ operantının değerini üreteceği için 5 değeri de lojik doğru olarak algılandığından dolayı
       bu değer her zaman doğru olarak algılanır.
       
       -->if(func()) yerine if(func) yazılması. Sentaks hatası vermez ama istediniz işlemi yapmaz.
       
       -->if(x  != 5 || x != 13) 
         Bu ifade de && operatörü yerine veya operatörü kullanılmış ve her zaman doğru bir ifadedir.
	 
       -->if(x == 3); Bu koşulda noktalı virgül bir ifade olduğu için if'in altındaki kodlar koşturulurken 
       if'in içerisinden çıkılmış olur.
         derleyici bu koşulu şöyle algılar:
	 if(x == 3) 
	     ; //null statement
	 x = 2;
	
	 ```
	 


# Standart getchar,putchar İşlemleri


- Fonksiyon yapıları
      - int getchar(void);
      - int putchar(int);
    
- Standart giriş akımının tamponundan bir karakter alır. (extract eder)
Ve karakter kodunu döndürür.
- scanf ve getchar fonksiyonları aynı buffer'ı kullanır. 

		```
		
		int c;
		
		printf("bir karakter girin:");
		c = getchar();
		printf("c(ascii kodu) = %d , c (girilen karakter) = %c ",c,c);
		//ekrana girilen karakterin ascii kodu ve hangi karakter girildiği yazdırılmıştır.
		
		```
- getchar() fonksiyonu line - buffered fonksiyon, yani ekrana enter (new line) karakteri girelene kadar değer alır ancak tek karakteri (extract) alır.	
	
Buffer (Tampon Bellek) : Ara bellek olarak adlandırılır. 
Bir cihazda verilerin topluca yazılmadan önce biriktirdikleri bellektir.
Bu işlemdeki amaç, ilgili belleğin o anda başka bir işle uğraşırken o işin bitmesini 
beklemeden emir verebilmek  başka bir deyişle hızı artırabilmek.

- getchar fonksiyonu, ekrana girilen değerin bize ascii kodunu decimal olarak gönderir.
- %c formatı ise bir karakterin ascii kodu girildiğinde o karakterin görüntüsünü yazdıran formattır.

  Örnek Soru:
  
  		```
		int c;
		
		printf("Bir giriş yapın:");
		
		while ((c=getchar()) != '\n')
		{
		     printf("%c  %d\n", c, c);
		}
		
		/* Bu programda ekrana enter(new line) karakteri giriline kadar ekrana girilen karakter ve ascii kodu yazdırılır.
		örnek giriş: 14
		
		Ekran Çıktısı: 
		
		1   49
		4   52
		
		*/
		
		
		```
		
 	Yukarıdaki soruya ek olarak ortak buffer'ı daha iyi anlamamız için ;
	
		```
		int c, x;
		
		printf("Bir giris yapin:");
		scanf("%d", &x);
		printf("%d\n", x);
		
		
		while ((c = getchar()) != '\n')
		{
		      printf("%c  %d\n", c, c);
		}
		
		```
	Şimdi yukarıdaki koda aşağıda ekrana girilen değerler ve çıktıları verilmiştir.
	   
	           13abc   		 	12 57 		    ab12				
		   
		   
		   13				12	 	    -85456416
		   a   97			   32		    a   97
		   b   98 			5  53	   	    b   98
		   c   99    			7  55		    1   49
		   						    2   50
								    
	Görüldüğü üzere scanf ve getchar fonksiyonları ortak bellek kullanıyorlar. Ayrıca bir şeye daha dikkat 
	çekmek gerekiyor. 2. ekrana girilen 12 57 değerinde 12'yi scanf yazdırdı ve boşluk(whitespace) atomunu gördüğünde
	yazdırma işlemini durdurdu ve scanf fonksiyonundan çıktı. Sonrasında getchar fonksiyonu boşluk atomunu da yazdırdı. 
	boşluk atomu ascii de 32 kodunu aldığı için karşısına 32 yazıldı.
	Ayrıca bu kodda bir hususa daha dikkat çekmek gerekirse scanf fonksiyonu çağırılırken decimal formatta çağırılıyor 
	yani siz decimal formatta bir değer gönderip enter(new line "\n") kullanırsanız bu karakterde buffer'da kalacağı için while 
	döngüsüne gelindiğinde derleyici new line karakterini görerek while döngüsünün içine girmeden geçer.
	
	
	
	  
```
		    
		    int c;
		    int sum = 0;

	            printf("bir tamsayi giriniz:");

		    while ((c = getchar()) != '\n')
	 	    {
			sum += c - '0';
		    }

		    printf("sum = %d\n", sum);

		    if (sum % 3 == 0)
				printf("evet tam bolunur\n");
		    else
				printf("hayir tam bolunmez:");

```
   Açıklama: Yukarıdaki programda getchar foksiyonu girilen karakterin ascii kodunu girdiği için c'ye atanan değer bir 
   rakamın ascii kodu olur. Bu kod 0'ın kodu olan 48 den çıkarılırsa tam olarak o rakam elde edilir. Bu yüzden c - '0' olarak kullanılmıştır.
   
   
   
   - Tıpkı scanf fonksiyonunda olduğu gibi getchar fonksiyonu da standart inputun buffer'ı boş ise -1 değerini döndürür.
   
   
   - Echo nedir?  
         - Echo girilen karakter ekranda gözükmesine echo denir. Bu sebeple şifre fonksiyonları echo vermeyen fonksiyonlar
         olarak kullanılır.
	 
   
   - getchar' a benzer 2 adet standart olmayan <conio.h> kütüphanesinde fonksiyon vardır.
                  - int _getch(void)
                  - int _getche(void)
                  
	
	Hatırlatma: Line-buffered func new line karakterini görene kadar değer almayan fonksiyondur.
	
    - Bu üç fonksiyonu kıyaslarsak;
    		- getchar() -->  standart kütüphanede / line-Buffered func/ Echo veriyor
    		- _getch()  --> standart kütüphanede değil/ line-buffered değil/echo vermiyor
    		- _getche() --> standard kütüphanede değil/line-buffered değil/ echo veriyor
     
     
     Parola Örneği:
	 
	 			```
		   		#define _CRT_SECURE_NO_WARNINGS

				#include <stdio.h>
				#include <math.h>
				#include <stdlib.h>
				#include <conio.h>





				int main()
				{
					int c1, c2, c3,c4;

					printf("parolayi giriniz:");

					c1 = _getch();
					printf("*");
					c2 = _getch();
					printf("*");
					c3 = _getch();
					printf("*");
					c4 = _getch();
					printf("*");

					printf("\n parola : %c %c %c %c", c1, c2, c3, c4);

	
				}

		
			
				```
	 
	 
	 - int putchar(int);
	 
	 - putchar sizden bir sayı alıyor ve bu sayıyı karakter kodlamasına göre ekrana yazdırıyor.
	 - getchar, standard bufferdan bir karakter alıp onun karakter sayısını yazdırıyor.
	 
	 
	 		- c1 = getchar();//ekrana A yazılırsa 65 sayısını c1'e atar. Giriş Fonksiyonudur.
	 		- c2 = putchar(65)// 65 sayısını fonksiyona gönderir ve ekrana A yazdırır. Çıkış fonksiyonudur.



	
	 
	 
	 
# Ders 14 - Tarih 05.03.2021
	 
	 - Modül bir kütüphanenin modüllerine verilen değerler isimdir.
	 
	 - <ctype.h> 
	 
	 Test fonksiyonları
	 
	 - White space karakterleri:

	 '\n'  , ' ' , '\t' , '\v' , '\f' , '\r'
	 
	 - <ctype.h> kütüphanesi hangi fonksiyonları içerir.
	  
	 -  int isupper(int c);  -->  büyük harf mi?
	 -  int isalpha(int c); -->küçük harf mi?
	 -  int digit (int c);  -->rakam mı?
	 -  int alnum (int c);  -->alpha-numeric mi?
	 -  int isxdigit (int c);  -->hex mi 
	 -  int space(int c);      -->white space mi?
	 -  int ispunct(int c);
	 -  int print(int c);
	 -  int isgraph(int c);
	 -  int isblank(int c);
	 -  int iscntrl(int c);

          
	 
	 Örnek:
	 
	 - İki sayının aynı anda asal olup olmadığına göre koşul içeren bir kod yazalım.


	```
	
	int a, b;
	printf("iki tam sayı giriniz: ")
	scanf("%d%d", &a, &b);
	
	if(isprime(a) == isprime(b))
        /*if'in içerisindeki koşul böümünü böyle kullanırsak isprime fonksiyonu,
	test fonksiyonu olduğu için sıfır veya sıfır dışında bir değer gönderecektir.
	Bu değer eğer sıfır dışında bir değer ise  1 olmak zorunda değildir. Bu da koşulu düzgün 
	kullanmamıza engel olabilir. Bunun yerine aşağıdaki if koşulu şeklinde kullanılabilir.*/
	
	if(!!isprime(a) == !!isprime(b))
	//şeklinde kullanım daha doğru olacaktır.
	
	
	```
	
	
- Ayrıca <ctype.h> fonksiyonun içerisinde büyük harfden küçük harfe ve büyük harften küçük harfe dönüştüren fonksiyonlar vardır.
	   
	       
    - int toupper(int);
    - int tolower(int);
 	
	Örnek: 
	
	```
	
	   #include <ctype.h>
	
	   int ch;
	
	    print ("bir karakter girin:");
	    ch = getchar();
	    printf("%c ==> %c\n",ch,toupper(ch));
	
	
	```
	Ekran Çıktısı:
	
	
	```
	                                    
	      h ==> H  //Eğer h değeri girilmişse.
	
	```
	


 	
	- Basit bir hileyle klavyeyi belirli bir karakter grubu dışındaki 
	 karakterlere kilitleyebiliriz.
	 
	     ```
	     #include<ctype.h>
	     int main()
	     {
	           for(;;)
	           {
	           int c=_getch();
		   
	           if(isxdigit(c))
	           	putchar(c);
             	   }
	     }
	     
	     
	     // Bu program ekrana sadece hex sayı formatında yazdırır.
	     ```
	     
	- Clamp nedir?
	  Bir aralık belirtilir ve bu aralığın dışında olan değerler üst sınırın üzerindeyse üst sınır değeri olarak algılanır.
	  Alt sınırın altındaysa alt sınır değeri olarak algılanır. Örnek vermek gerekirse 18, 36 sınır değerleri olsun
	  eğer 20 sayısı girilirse o sayı 20 olarak kullanılır. Eğer 39 girilirse o sayı 36 olarak, 15 girilirse 18 olarak kullanılır.
	  
	 
	 
	
     # Ternary Operator (Koşul Operatörü)
	
	
	- Conditional Operator
	- Bazı programlama dillerinde var her programlama dilinde yok.
	- 3 operant alan operatör
	- Bu operatörün 2 tane token'ı var.
	               - op1 ? op2 : op3
	-Atama ve virgül operatörlerinden daha öncelikli, diğer tüm operatörler daha öncelikli.
	
	- Op1 lojik yorumlamaya tabi tutulur. 
	                     - Eğer lojik doğru (non-zero) ise op2 elde edilir.
	                     - Eğer lojik yanlış ise op3 elde edilir.
	                      
	- Birinci operanttan sonra yan etki noktası (sequence point) vardır.
	
	Örnek:
	
	     ```
	      m = x > 10 ? a : b
	     //x > 10 ise m'ye a'yı ata, değil ise m'ye b'yi ata.
	     
	     
	     a > b ? a : b;
	     // İki sayıdan büyük olanı üretir.
	     
	     
	     
	     x > 0 ? x : -x
	     // Mutlak değer alma
	     
	     
	     a++ > b ? a : b
	     // Sequence point'i olduğu unutulmamalıdır.
	     // a ile b'nin ilk değerine göre karşılaştırma yapılır sonra artan değeri üretilir.
	          
	     
	     ```
	    
# Ders 15 - 08/03/2021

 # Loop Statement 
 
 - While 
 - Do while 
 - For

	  - break 
	  - continue
	  	
	
- Genellikle yanlış yapılan bir mülakat sorusu:
 
 		  int i = 0;
                  while (i++ < 100);
		  	printf("%d", i);
			
-> Yukarıdaki kodda küme parentezi kullanılmadığı için ilk deyim olarak ; alınmıştır.  Ve i++ olduğu için while'dan çıkıldığında i = 101 olur.




- n Klavyeden girilen bir pozitif sayı olsun. 
	- while(n--) ile while(n-- < 0) arasında bir fark yoktur.




- Maksimum munch kuralı :
		int z = x+++y;
		
Burada x++ derleyicinin algılayabileceği en uzun atom olduğu için x++ +y olarak tokenize edilir.



Örnek: 
```
	int power(int base, int expr)
	{
		int result = 1;
		while(expr--)
			result *= base;
			
		return result ;
	}
	
	int main()
	{
		int x, y;
		printf("iki tam sayı giriniz: ");
		scanf("%d%d", &x, &y);
		printf("%d ussu %d =%d\n", x, y, power(x, y));
		
	}
```
#


- Bir döngüden hangi biçimlerde çıkılır:
	- Kontrol ifadesinin yanlış olması.
	- Döngü gövdesi içinde return deyiminin yürütülmesi.
	- Break Statement.
	- Goto Statement.

- Programın sonlandırılmasını sağlayan bazı C fonksiyonları:
	- abord();
	- exit();

- Break Statement:
 	- Geçerli olabilmesi için ya bir döngü deyiminin gövdesinde, ya da switch deyiminin gövdesinde olması gerekiyor.
	
- Sonsuz Döngü idiomu - infinite Loop

Örnek: 
```
		
		int i = 1, n = 5;
		
		while (i < 100)
		{
			if(i % n == 0);
			{
				printf("%d",i);
				i++;
			}
		}
		//i++'ın yeri yanlış yazıldığı için ilk döngüye 1 ile başlayıp if'e giremediği için sonsuz döngüde kalır.
```

#

Örnek:  e ya da h tuşları dışında bir tuşa basıldığında program tepki vermeyecek. Sadece e ya da h tuşlarına 
basıldığında döngüden çıkacak.


```
#include <conio.h>

int ch;
printf("evet mi hayir mi ? (e) (h)");
while(1)
{
	ch = _getch();
	if(ch == 'e' || ch == 'h')
		break;
}

putchar(ch);

if(ch == 'e')
	printf("\n evet dediniz.\n");
	
else
	printf("\n hayir dediniz\n");
	
	
///Yukarıdaki koda alternatif olarak :

	while((ch == _getch()) != 'e' && ch != 'h')
		;  //Null Statement

```


#

- Nested Loops (İç içe döngüler)

- Break deyimi sadece içinde bulunduğu döngüden çıkış yapar.

- Eğer biz bulunulan iç içe döngüden en dışa çıkmak istersek;
	flags (Bayrak) değişkenleri kullanabiliriz.

		

Peki bayrakları nasıl kullanabiliriz?

```
flag=0
while( ---)
{
	statement;
	statement;
	statement;
	
	while(---)
	{
		if(exp)
		{
			flags=1;
			break;
		}
	}
	
	if(flag)///-------> Burada flag kontrol edildi ve eğer break sebebi ile geliyorsa ikinci break atılıdı.
		break;
}

```


#

- Break yerine programın herhangi bir yerinde goto deyimi kullanılarak gidilecek etiket belirlenip istenilen noktaya ulaşılabilir.
	- etiket - label
	
	

- Continue statement 
	- Yardımcı bir kontrol deyimi
	- Continue sadece döngü deyimlerinin gövdelerinde kullanılır. 
		- break; (loops/switch)
		- continue; (just loops)
	- Continue deyiminin yürütülmesi döngünün kalan kısmını by-pass ediyor yani kalan kısmı yapılmış gibi diğer tura geçiyor.




- if ile alakalı bir not:
 	- if(val <= 0)
 		return val;
	  else 
	  	return val;
		//burada else yazmakla yazmamak arasında bir fark yoktur. (gizli else)
			- redundant else 
			- redundancy = fuzuli



- Basit bir mülakat sorusu: Aşağıdaki kodda yanlışlık nerededir.
 
```
	if(x != 0)
		y = x;
	else 
		y = 0; // if kullanılmasına gerek yoktur. bu kodun karşılığı zaten y = x'dir.
		
		
```

#

- Klavye Kısaltmaları:
	- ctrl k c -> açıklama satırı yap
	- ctrl k u -> açıklama satırını kaldır.
	- ctrl L -> bulunan satırı direk siler.
	- ctrl D -> bulunan satırı aşağıya kopyalar.
	- shift alt -> satırsal olarak seçip satırsal olarak işlem yapabiliriz.
	
	
	
	
	
-For statement
	- for(expr1; expr2; expr3)
	- Eğer expr2'ye hiç birşey yazılmazsa lojik 1 kabul edilir.
	- for(;;) -> infinite loop  <- while(1)
	 
		
	
	
# Ders 16 Tarih 10/03/2021


Örnek:

```

	int x, a;
	scanf("%d", &x);
	
	if(x > 10)
		a = 5;
	else 
		a = 7;
	// Burada  a' ya ilk değer ifadesi verilmek istenmiş, ancak scope farklılığı sebebiyle doğru bir kullanım olmamıştır.
	
	Bunun yerine  a = x > 10 ? 5 : 7; daha doğru bir kullanımdır.
 			- Koşul operatörünün ilk değer verme amaçlı kullanımı oldukça yaygındır.
 ```
 
 #
	
	
Örnek :  Aşağıdaki kodda ya bir karakter ekleyerek ya da bu kodda bir karakteri değiştirerek ekrana 5 kere something yazdırılacaktır.

```
	int n = 5;
	for(int i = 0; i < n; i--)
		printf("something\n");
		
	// cevap:
		- i < n ifadesinde i yerine -i yazmak.
		- i < n ifadesinde < yerine + yazmak.
		- i--  yerine n-- yazmak.
```


#

- Collatz Sanısı 
	- Sayı tek ise 3 katının 1 fazlası alınacak , bulunan sayı çift ise  2'ye bölünecek.
	- Örnek olarak sayı 23 ise 3 katının 1 fazlası 70. 2'ye bölünecek. 35. tekrar  katının 1 fazlası alınır 106 diye devam eder.
	

```
#define _CRT_SECURE_NO_WARNINGS

#include <stdio.h>

void print_collatz(unsigned long long n)
{
	while (n != 1)
	{
		printf("%llu ", n);
		if (n % 2 == 0)
			n /= 2;
		else
			n = n * 3 + 1;
	}
	printf("1\n");

}




int main()
{
	unsigned long long x;
	printf("enter the integer:");
	scanf("%llu", &x);
	print_collatz(x);


}
			
```


#

- Asal Sayı Örneği: Bir aralık girin ve bu aralıktaki bütün asal sayıları ekrana yazdırın.

 
```
#define _CRT_SECURE_NO_WARNINGS

#include <stdio.h>

int isprime(int val)
{
	if (val <= 1)
		return 0;
	if (val % 2 == 0)
		return val == 2;
	if (val % 3 == 0)
		return val == 3;
	if (val % 5 == 0)
		return val == 5;
	for (int i = 7; i * i <= val; i++)   /* Bir sayının asal çarpanları, o sayının karakökü kadar büyük olabilir.*/
	{
		if (val % i == 0)
			return 0;
	}
	return 1;

} 



int main()
{
	int low, high;
	int prime_count=0;
	printf("bir aralik girin:");
	scanf("%d%d", &low, &high);
	for (int i = low; i < high; i++)
	{
		if (isprime(i))
		{
			printf("%d  ", i);
			++prime_count;
		}
	}
	printf("\n [%d  %d  araliginda] %d asal sayi bulundu.\n", low, high, prime_count);

}
```


#


  
- Factorial işlevinin recursive implementasyonu:


```
	int factorial (int n)
	{
		return n < 2 ? 1 : n*factorial(n-1);
	}
```


#

- Mülakat Sorusu: Aşağıdaki kodda ekrana ne yazdırılır?


```
int i = 0;

do
{
	printf("%d\n",i);
	i++;
	if(i < 15)
		continue;
		
}while(0);





// Bu kodda ekrana 0 yazdırılır. Continue komutunu görünce koşul ifadesi neredeyse program oraya dallanır.
```




- Nested Loops:
	 - Armstrong sayısı; bir sayının rakamlarının, basamak sayısı derecesinden kökleri toplamı kendisine eşit ise
	  o sayıya armstrong sayısı denir.
	 
	 
- Örnek: 3 basamaklı armstrong sayılarını bulan programı yazınız:
- 
```
#define _CRT_SECURE_NO_WARNINGS

#include <stdio.h>






int main()
{

	int x = 100;
	for (int i = 1; i < 10; ++i)
	{
		for (int j = 0; j < 10; ++j)
		{
			for (int k = 0; k < 10; ++k)
			{
				if (x == (i * i * i) + (j * j * j) + (k * k * k))
					printf("%d\n", x);
				++x;
			}
	
		}
	}


}
```

#



# DERS 17 - 12/03/2021

- Eğer iç içe döngülerde içteki bir döngüden tüm döngüleri kırarak çıkmak istiyorsak ideal olarak goto deyimi kullanılmalı.



- Fonksiyon Bildirimleri - Function Declaration
	- Bir fonksiyon çağrısı yapıldığında o fonksiyonun tanımı name look up ile bulunur.
	Derleyici o fonksiyonun tanımını neden bulmalı?
		- Çağrıda kullanılan argüman sayısı ile parametre sayısının uyumunu kontrol edecektir.
		- Fonksiyonun parametresi int türden ise ancak bu fonksiyona gönderdiğimiz parametre int türden 
		değil ise dil kurallarına göre derleyicinin tür dönüşümü (type conversion) yapması gerekiyor.
		
- ! Derleyici fonksiyonun kodunu bilmiyor. Fonksiyon çağrısını içeren fonksiyonun koduyla,
 çağırılan fonksiyonun derlenmiş kodunu birleştiren Linker dediğimiz program ,
Derleyici fonksiyonunun çıkış kodlarını da üretiyor. Fonksiyonun geri dönüş değerinin yazılacağı 
adres gibi araya da kendinden sonra birleştirme işlemi yapacak  linker için referans bir isim yazıyor. 
Böyle referanslara external referans deniyor.

- Derleyicinin bir fonksiyon çağrısı karşılığı 
	- Doğru şekilde fonksiyona giriş kodları üretebilmesi için 
	- Doğru şekilde fonksiyondan çıkış kodlarını üretebilmesi için 
	- Programcının yapmış olabileceği lojik hatalara karşı uyarabilmek için çağrılan fonksiyon ile ilgili 
	bazı bilgilere sahip olması gerekiyor.
	- Derleyicinin fonksiyon kodunu görmesi zorunlu değil 
	- Derleyiciye bu bilgileri veren bildirime "function declaration" deniyor.
	

- void func(); ile void func(void); arasındaki fark; parantezin içerisi boş ise bu tanımlamada 
fonksiyunun parametreleri hakkında bilgi vermiyorum anlamına geliyor. Parantezin içerisine void yazıldığında ise fonksiyonun 
geri dönüş değerinin olmadığı bildiriliyor. Bu C diline ait bir kural.


- function prototype scope:
	- Bir fonksiyonun bazı durumlarda kodunu göremeyiz ve sadece bildirimini görebiliriz.
	 Bu bildirimde gönderilen değişkenin ne olduğunu bildirmek için ve sadece bildirim satırındaki parantezi kapsayan scope'dur.
	


- Bir fonksiyonun bildiriminin 2. kez yapılmasına "function redeclaration" denir. Bunlar arasında bir çelişki varsa sentaks hatası olur.


- Function Overloading (işlev Yüklemesi) 
	- Bazı dillerde bir fonksiyon ismi ile paramedic yapısı farklı olarak tanımlanabiliyor. Ancak C'de öyle değil.
	
- .c dosyalarına source file , implementation file , dot c file denebiliyor.
 
- Header File:	 
	 - Header file'ın içerisinde sadece bildirim dosyaları vardır. Fonksiyon tanımı yoktur.
	 
	 - Bir başlık dosyasında neler var?
	 	- Önişlemci komutları var .
	 	- Macrolar var.
	 	- Fonksiyon bildirimleri 
	 	- Tür bildirimleri (user - defined types)
	 	- Tür eş isim bildirimleri


# Ders 18 - 15/03/2021

- Preprocessor:
	- Önişlemcinin , bilgisayarın işlemcisi ya da başka bir donanımsal elemanıyla hiçbir ilgisi yoktur.
	 	- Önişlemci belirli bir işi gören bir yazılım programıdır.
	- Önişlemci, kaynak dosya üzerinde birtakım düzenlemeler ve değişiklikler yapan bir ön programdır.
	- Önişlemci programının bir girdisi bir de çıktısı vardır. Önişlemcinin girdisi kaynak dosyanın kendisidir. 
	Önişlemci programın çıktısı ise derleme modülünün girdisini
oluşturur. Yani kaynak program ilk aşamada önişlemci tarafından ele alınır.
Önişlemci modülü, kaynak dosyada çeşitli metinsel düzenlemeler, değişiklikler yapar. Daha sonra
değiştirilmiş ya da düzenlenmiş olan bu kaynak dosya, derleme modülü tarafından amaç koda dönüştürülür.
	- Yani önişlemcinin görevi kendi komutlarını yürütmek, Bu komutlara "pp directives" denir.
		- #(null directive)
		- #include
		- #define
		- #undef
		- #if 
		- #else
		- #elif
		- #endif
		- #ifdef
		- #ifndef
		- #line
		- #error
		- #pragma
	- Önişlemci komutlarını belirleyen yukarıdaki sözcükler, C dilinin anahtar sözcükleri değildir.
	- Sıra derleyiciye geldiğinde bunlar, önişlemci tarafından kaynak dosyadan silinmiş olur.
	- Önişlemci program, amaç kod oluşturmaya yönelik hiçbir iş yapmaz, kaynak kod içinde bazı metinsel düzenlemeler yapar.
	 Kendisine verilen komutları yerine getirdikten sonra, # ile başlayan satırları kaynak dosyadan siler.
	 Derleme modülüne girecek programda # ile başlayan satırlar artık yer almaz.
	
	
	 	 
	
	     
	     
#İnclude Önişlemci komutu:
	- #include <---.h> veya #include "----.h" olarak gösterilebilir.
	- #include komutu ile, ismi verilen dosyanın içeriği, bu komutun yazıldığı yere yapıştırılır. Bu komut ile önişlemci, 
	belirtilen dosyayı diskten okuyarak komutun yazılı olduğu yere yerleştirir. Bu komutla yapılan iş, metin düzenleyici 
	programlardaki "kopyala - yapıştır" (copy – paste) işlemine benzetilebilir.
	- Dosya ismi eğer açısal ayraç içinde verilmişse, sözkonusu dosya önişlemci tarafından, popüler olarak 
	"default directory" denilen  önceden belirlenmiş bir dizin içinde aranır.
	- Dosya ismi; eğer çift tırnak içinde verilmişse sözkonusu dosya, önişlemci tarafından kaynak dosyanın bulunduğu dizinde arar,
	 eğer burada bulamazsa sistem tarafından berlirlenen dizinde arar.
	
	
- **Başlık Dosyaları Neden Kullanılır?
	- Özellikle büyük programlar, modül ismi verilen ayrı ayrı parçalar halinde yazılır. Bu modüllerden bazılarının amacı,
	diğer modüllere hizmet vermektir. C ve C++ dillerinde, genel hizmet verecek kodlar (server codes), genel olarak iki ayrı dosya halinde yazılır. 
		- Fonksiyon tanımlamaları, global değişken tanımlamaları uzantısı .c olan dosyada yer alır. 
			- Bu dosyaya, kodlama dosyası (implementation file-Source file) denir. 
		- Hizmet alacak kodları (client codes) ilgilendiren bildirimler ise bir başka dosyada tutulur.
			- Bu dosyaya, başlık dosyası (header file) denir. 
	- Bir başlık dosyası, bir modülün arayüzüdür (interface). Modül dışarıyla olan ilişkisini arayüzü ile kurar.
	     
	     
	
	
# #Define Önişlemci komutu:

- #define önişlemci komutunun işlevi, metin düzenleyici programlardaki "bul - değiştir" (find - replace) özelliğine benzetilebilir. 
Bu komut kaynak kod içindeki bir yazıyı başka bir yazı ile değiştirmek için kullanılır. 
		- Object-like macro
	- Önişlemci komutu herhangi bir blokta da tanımlanabilir. Tanımlandığı yerden sonraki tüm kodlarda geçerlidir.
	- #define SIZE 100 komutu ile, kaynak kod içerisinde gördüğü her bir SIZE atomu yerine 100 atomunu yerleştirir.
	 Derleme modülüne girecek kaynak programda, SIZE atomu artık yer almaz.
	- Önişlemci komutları kullanılırken parantezler konusunda dikkatli olunmalıdır. Bir örnekle gösterelim.
	
```
#define MAX 100+200

int main()
{
	int a = 5  *MAX;
	printf("a = %d \n", a);
}
```
#

Yukarıdaki örnekte parentez kullanılmadığı için MAX yerine direk olarak 200 + 100 yazılınca oluşan ifade a = 5 * 100 + 200; olur. Bu da istenen sonucu karşılamayabilir.

#

- Önişlemci tanımlamalarında noktalı virgül kullanılmaz. Kullanılırsa önişlemci onu olduğu gibi (copy-paste) yaptığı için dil kuralına göre hatalar oluşturur.
- Aşağıdaki #define önişlemci komutları geçerli değildir:
		- #define + -
		- #define 100 200

- Bir kodda kullanılan isim sabit mi değişken mi nasıl ayırt edebiliriz?
	- C'de değişken isimleri küçük harfli olarak seçilirler.
	- ALL CAPS= tamamı büyük harfler.
	- C'de all caps isimler macrolarda kullanılmaktadır.
	

- Örnek olarak: 
#
```
#define SIZE 100

int main()
{
	SIZE = 50;
}
// Bu kodun okunma şekli 100 = 0; olacaktır. Ve bu sentaks hatasıdır.
// Ancak bu kodu şu şekilde kullanırsak ;

#define SIZE a[0]

int main()
{
int a[100]

SIZE = 4;---> olarak yazdığımızda bı kodda sentaks hatası yoktur.
}
``` 
#


# Ders 19 - 17/03/2021


- Fonksiyonel Makrolar
	- functional macro
	- function-like makro

- #define max2(a,b)   ((a)>(b))?(a):(b))
	- fonksiyonel makrolar kodu küçük(az) fakat sık çağırılan fonksiyonlara bir alternatif 

- Makro tanımında parantez kullanmamızın sebebini anlatan bir örnek;
```
#define square(a)   a*a
int main()
{
	int x, y;
	printf(" bir tamsayı girin: ");
	scanf("%d", &x);
	y = quare(x + 1); // y = x + 1 * x + 1; derleyici bu şekilde algılayacak.
}

//doğru olan tanım şekli #define square(a)  (a) * (a) şeklindedir.

```
#

- ub oluşturulmamasına dikkat edilmelidir.
```
#define square(a)   (a)*(a)
int main()
{
	int x, y;
	printf(" bir tamsayı girin: ");
	scanf("%d", &x);
	y = square(x++); // y = (x++) * (x++); burada yan etki noktasına gelinmeden x iki kez kullanılmış olur ve bu tanımsız davranıştır.
}
```
   
#

- foo bir fonksiyon olsun.
```
#define SQUARE(a) ((a)*(a))
int main()
{
	int y = 10;
	int z = SQUARE(foo(y)),
	//burada foo fonksiyonu 2 kez çağırılmış oldu. Eğer square bir fonksiyon olsaydı bir kez çağırılıp geri dönüş değeri ile makraya gidilecekti.
}
```
- bir mülakat sorusu: 

```
  int square(int x)
{
	return x * x;
}

#define square(a)  ((a)+(a))


int main()
{
	int ival;
	printf("bir tam sayı giriniz:");
	scanf("%d", &ival);
	int y = square(ival);
	printf("%d", y);

}


- Yukarıdaki fonksiyonda square komutu ile fonksiyon mu çağırılır makro mu??

          - Elbette ki önişlemci komutu çağırılır.önişlemci komutu derleyiciden önce çalışıyor.
           Önişlemci programı define komutunu yürütecek onun çıktısı derleyiciye gidecek.
    
           
	Eğer biz hem makro tanımlayıp hem fonksiyonu tanımlarsak ve seçimi programcıya bırakırsak;
		- fonksiyon çağırılmak istenirse (func)(a,b) şeklinde yazılır.
 ``` 
  
  
  #
  
- Fonksiyonel makrolar ile fonksiyonların karşılaştırmasını yapınız:

	- Makrolar kaynak kodu büyütme eğilimindedir.
       		 - Yani derlenmiş kodun boyutu üzerinde bir kaygınız var ise makro kullanmamanız daha sağlıklı olacaktır.
        	- Ancak ne kadar yer kaplasa da sizin için  kapladığı yerden çok hızı önemli ise daha hızlı olması için makrolar daha avantajlı.
              			- Hızlanmasının sebebi ise fonksiyona giriş ve çıkış kodları üretilmiyor oluşudur.
	- Fonksiyonlar türe bağlı, makrolar türden bağımsızdır.
	- Makro kullanımı durumunda debugger desteği daha az olabileceği göz önünde bulundurulmalıdır.
	- Makrolar, fonksiyonlara göre daha etkin kodun oluşturulmasını sağlayabilirler.
	
	
	
	
- Önişlemci programın kendi operatörleri vardır.
	- preprocessor operator
		- # operetörü  -----> stringificition operator(string yapma operatörü )
		- ## operatörü ------>token-pasting operator (atom yapıştırma operatörü)
		- defined operatörü


- #x -----> derleyiciye "x" bu şekilde görünür. 
 - örnek olarak:
 ```
 	#define str(a)  #a
	
	int main()
	{
		printf(str(github));
	}
	// Derleyicinin gördüğü printf("github");    olur.
	
	
```


- Örnek


```
#define iprint(x)  printf(#x "= %d\n",x)

int main()
{
	int a = 10;
	int b = 7;	
	int c = 11;

	iprint(a);
	iprint(a + b);
	iprint(a * a + b * b + c * c);
	//burada ekran çıktısı 
	a = 10
	a + b = 17
	a * a + b * b + c * c = 590              olur.
}


```

#

- ## operatörü 
	- a##b --->ab olur. Bir nevi birleştirme operatörü.
 örnek:


```
	#define uni(a,b) a##b
	int main()
	{
		int counter = 0
		uni(co, unter) = 20;
		printf("%d", counter);
	
		// ekrana 20 yazılır.
	}
		
```
#


#
- Define farklı bir kullanım şekli;
- 
```
#define PUBLIC

PUBLIC int g=45;
PUBLIC int square(int x)
{
	return x*x;
}
//Bu kodda PUBLIC sözcüğü derlendiğine derleyici, PUBLIC sözcüğünü görmez. 
```


# Conditional Compiling (koşullu derleme)

#undef	#elif
#if 	#endif
#else 	#ifdef
#ifndef


- Koşullu derlemede bir kural vardır. Eğer makronun tanımı yapılmamışsa makro sıfır olarak işleve alınır.

mesela;

```
#if MAX > 10
	typedef int word;
#endif--> bu kodda max 0 alınır ve koda girilmez. Ancak koşul ifadesi >-1 olsaydı eğer koşula direk girilecekti.
```

# Ders 20 - 19/03/2021

- Önişlemci komutlarında elseif merdiveni;

```
#define NEC 1

#if NEC == 0

#else 

#if NEC == 1 

#else
#endif
#endif ------>  Bu şekilde kullanılırsa her if için bir endif yazılması gerekir. Ancak aşağıdaki gibi kullanılırsa ;

#if NEC == 0

#elif NEC == 1

#elif NEC == 2

#endif

```

#

```
 - #ifdef NEC ----> NEC makrosu define edilmişse önişlemci bu aralığa girecek.
 
 #endif
 
 
 
 - #ifndef NEC -----> NEC makrosu tanımlanmadıysa bu aralığa girilecek.
 
 #endif
 
 ```
 
 #
 
 - Defined Operatörü 
 	- defined NEC
 		- Eğer defined komutunun terimi olan isim daha önce tanımlanmış bir simgesel var ise
 		 defined operatörü lojik 1 değerini üretir.yok ise lojik 0 değerini üretir.

#ifdef NEC ile #if defined NEC aynı işlevi yaparlar.
#ifndef NEC ile #if !defined NEC aynı işlevi yaparlar.

- Peki bunlar aynı işlevi yapıyorlarsa hangi noktalarda ihtiyacımız oluyor.

```
#ifdef EMRAH
#ifdef FURKAN
//KODLAR
#endif

yerine 

#if defined EMRAH && FURKAN 
//kodlar
#endif

- Sağladığı kolaylıktan dolayı defined operatörü daha sonradan çıkmıştır.
```

#


- Peki biz bu önişlemci komutlarında koşullu bildirmeleri nerelerede kullanıyoruz??
	- donanıma göre
	- işletim sistemine göre 
	- derleyiciye göre
	- dile göre
	- versiyon/ sürüm kontrolü
	- lokasyona göre


- Multiple inclusion guard (çoklu dahil etmeye karşı önlem gibi)

	- Önişlemci koşullu derleme koşullarının özel bir kullanım biçimidir. Ki bu komutları kullandığımız zaman bir başlık dosyasında
	 önişlemci programı o başlık dosyasına bir kere girer ikinci kez girmeye zorlarsanız ikinci kez girmez. 
	- Peki bunu nasıl sağlıyoruz?
bir başlık dosyasının içine ;
```
#ifndef NUTİLİTY_H
#define NUTİLİTY_H
//kodlar
#endif
---> şeklinde bir koşul ve makro tanımlanırsa ilk girişte koşulda sorgulanan makro tanımlanmadığı için girer ve kodu işler.
Eğer ikinci kez tanımladıysa koşuldaki makro, birinci girişindeki tanımladığı koşul geçemez.

```
- !!!! Multiple inclusion guard her başlık dosyasında olmalıdır. 



- #undef önişlemci komutu
	- #undef NEC
		- Bu önişlemci komutuyla NEC makro tanımsız kabul edilecektir.
		- Daha önce tanımlandıysa NEC makrosu, #undef NEC komutundan sonra tanımlanmamış olarak devam edecektir.
		
		
#### UNDEFİNED BEHAVİOUR

```
- Eğer önişlemci programı bir makronun farklı 2 tanımıyla karşılaşırsa bu durumda tanımsız davranış olur.
 #define SIZE 100
 #define SIZE 500
- Önişlemci programında name look up terimi yoktur. Bu derleyici ile alakalıdır.

```

- Yani biz bir makroyu kullandıktan sonra tekrar değer vermek istersek önce o makroyu #undef komutu ile içeriğini temizlememiz gerekir.



- Pre - defined Symbolic Constant(ön tanımlı sabit)
	- Dil tarafından tanımlı kabul edilen makrolara denir. 
		- __FILE__----> bulunduğu dosyanın ismi  ile yer değiştiren makro.
		- __LINE__----> bulunduğu line'ın numarasıyla yer değiştiren makro.
		- __DATE__----> derlendiği tarih ile yer değiştiren makro.
		- __TIME__----> derlendiği saat ile yer değiştiren makro.
		- __STDC__----> standart bir C derleyiciyse bu makro define edilmiş kabul edilir.
		- __func__----> bulunduğu fonksiyonun ismi ile yer değiştiren makro.



# Ders 21 - 22/03/2021

- Yorum satırları
	- Comment out: Belirli bir kod bütününün bir kısmını deneme amaçlı yorum satırı yapmaya denir.
	- Commit = Kodu repoya yüklemeye denir. Commit edilen kodda kesinlikle comment out bulunmamalı.
	- Mecbur değilseniz kodu büyük fonksiyonlar yazmaktan kaçının.
	- Genelde kodu büyük kodlarda yapılan hatalar; kod tekrarı , fonksiyonlara bölünmemiş olması.


- Go to deyimi:
	- Aynı fonksiyon içerisinde yapılan jump olayına "near jump (lokal jump)" denir.
	- long jump fonksiyonlar arası yapılan jump olayıdır.
	- goto kontrol deyimi C'de local jump yapar.
	- label (etiket): Bir deyimin yerini belirleyen özel isimler.
		- Etiketler function scope kuralına uyar.
		- Etiket aranırken name look-up gibi yukarı doğru değilde fonksiyonun her yerinde arama gerçekleşir.
		- Farklı bir fonksiyondaki etikete dallanamaz.
		- Dikkat: Eğer etiketten sonra herhangi bir deyim olmazsa bu bir sentaks hatasıdır.
	- İç içe döngülerin içinden tek seferde çıkmak için kullanım yaygındır.
	
	
	
- Switch Statement

	- switch(integer expr) --> parentez içerisindeki ifade tam sayı türünden olmak zorunda.
	
 Örnek sentaks: 
 ```
switch( int expr)
case1: statement 
case2: statement
.
.
.
default: // Eğer hiçbir case'e giriş yapmaması durumunda bu etikete girer.

```

Örnek:

```
void print_season(int month)
{
	switch(month)
	{
		case 12:  //fallthrough
		case 1:  //fallthrough
		case2:  printf("winter");break;
		case3:   //fallthrough
		case4:   //fallthrough
		case5: printf("spring"); break;
		case6:  //fallthrough
		case7:  //fallthrough
		case8: printf("summer");
		case9:   //fallthrough
		case10: //fallthrough
		case11: printf("autumn");
		
	}

}---> Case'lerde boşta kalan yani case'den sonra deyim olmadan switch'den çıkan bir case olmamalıdır.

```
- Fallthrough: break komutu kullanmadan 2 case'i birleştirdiğinizde, bu durumu bilerek ve isteyerek yaptığınızı 
yorum satırıyla case'in yanına eklenmelidir ki kodu okuyan kişi, kodu yazan kişinin bunu bilinçli bir şekilde yaptığınızı anlasın.



  
  # Ders 22 - 24/03/2021
  
  
  - Derleyicilerin "kodların bağlanması için " Linker programına hitaben obje kod içine (özel bir notasyon ile) 
  yazdığı isimlere " external referance" denir.
  
  
  #### Tür Dönüşümleri
  
  - ival + dval ---> Bir int türünden değeri bir double türden değerle toplarsanız eğer derleyici arka planda tür dönüşümü yaparak ival'i,
  double türe dönüştürür. Bu olaya ;
  	- implicit type conversion denir.
  		- implicit = örtülü , gizli , kapalı
  	- explicit type conversion : Kodu yazan kişinin bu kodda tür dönüşümü olacağını belirtmesine denir.
  		- type-cast operatörü
  	

- Nerelerde tür dönüşümü yapılıyor?
	- Basit aritmetik dönüşümler
	- Atama tür dönüşümleri
		- Bu dönüşümler geçici nesne (temprory obj) oluşturularak yapıldığı için aslında değişkenin türü değiştirilmiyor.
		
		
- a + b ---> bu işlemde en kapsamlı tür hangisiyse işlem o türde yapılıyor.

1 - long double
  - double
  - float
  
2 - unsigned long long
  - signed long long
  - unsigned long
  - signed long 
  - unsigned int 
  - signed int
  
  
3 -   "integer promotion"
    - unsigned short 
    - signed short 
    - unsigned char
    - signed char
    - char
    - _BOOL
    
    
    
- Rank : Büyüklük derecesi
 	- long double > double > float > long long > long > int

- Aynı türlerin operantlarının rank'ı aynı ise fakat türleri farklı ise, tür dönüşümü her zaman işaretsiz yöne yapılır.

- a + b ---> operantlar farklı rankta fakat büyük olan rank işaretli , küçük olan rank işaretsiz ise ,
 Bu durumda eğer işaretli olan tür işaretsiz olan türün bütün değerlerini tutabiliyorsa 
 tür dönüşümü işaretli ranki yüksek olan türe yapılacak. Aksi halde bunun işaretsiz türüne yapılacak.
 
 - Ranklar aynı işaretler aynı ise işlem yüksek rankta yapılır.
 - Ranklar farklı büyük rank işaretsiz ise yine yüksek rankta yapılır.
 - Rankler farklı büyük rank işaretli ise işlem
 		- ya yüksek rankta
 		- ya da yüksek rankın işaretsiz olanında yapılır.
 
 
```
//c++ 'da tür öğrenme kodu

#include <iostrem>
using namespace std;

int main()
{
	char c1 = 10;
	char c2 = 20; // işlemin sonucunun türü int olacak 
	
	cout << typeid (c1 + c2).name()<<"\n";
}
--------------

short s1 = 10;
short s2 = 20; // int

--------------

unsigned int uval = 5;
int ival = 10// unsigned int 

--------------

long uval = 10;
unsigned int ival = 10;

--------------

long long uval =5; // 8 byte 
unsigned int ival =10;//4 byte  --> long long

--------------  
  
 ``` 
  
  
  
- Yapılan tipik hatalar :

  
 ```
 
 int main()
 {
 	int x = -1;
	unsigned int y = 2;
	
	if (x > y)
		printf("evet dogru\n");
	else
		printf("hayir yanlıs\n");
 }
 ---> Bu kodda işaretli x, bellekte bit olarak tutulurken 1111 1111 1111 
 olarak yani işaret bitleri de olduğu için x>y algılanır.
 
 
 - int x = 10;
   double d1 = x/3;	-->sonuç = 3.00 olur.
   double d2 = x/3.;	---> sonuç = 3.333 olur.
   ```
   
   
  - Hatırlatma : Tam sayi türlerinde taşma tanımsız davranıştır.
  	- İşaretsiz türlerde taşma yoktur.
  	 	- İşaretsiz türlerde tüm işlemler modüler aritmetiğe göre yapılır.
  	 	
Örnek olarak ; 
	- Sistemdeki int türü 2 byte olsun.
	
		int ival = 1000;
		ival * 1000u;--> bunun sonucu 1000000 % 65536 olur.


- Atama tür dönüşümleri:

		 int x; 
		 x = expr; --> expr hangi türde olursa olsun, 
		 tür dönüşümü kendisine atama yapılan nesnenin türüne yapılacak.
		
- Küçük türden büyük türe atama  yapmakta bir sakınca yok.
- Ancak büyük tam sayı türünden küçük tam sayı türüne dönüşümden kaçınmak gerekir.
		 (tanımsız davranış değildir - veri kaybı oluşturur)
		 
- Gerçek sayı türlerinden tam sayı türlerine otomatik dönüşüm yapılmasına izin verilmemelidir.

Bir mülakat sorusu:

```
	int x = 10;
	int y = 20;
	double dval = (y > 10 ? x : 3.)/3;
	printf("dval = %f\n ",dval );
--> Ekran çıktısı 3.3333 olur .

```
- Koşul operatörünün 2. veya 3. operandları arasında tür dönüşümü uygulanır.
	- type-cost (tür dönüştürme ) operatörü
	- -> (tür)expr olarak kullanılır.


# Ders 23 - Tarih 26/03/2021

 Type cast 
 	- (int) dval  
 	
- Nerelerde kullanıyoruz??
	- Bu operatörü kullanmazsak işlem bizim istediğimiz türde yapılmayacak. İşlemin istediğimiz türde yapılmasını sağlamak için kullanılır.
	
- Bir soru:

```
	double dval ;
	printf("[-5 +5] araliginda bir gercek sayi giriniz:");
	scanf("%lf", &dval);
	printf("%lf ====> %d \n", dval, ???);
	
	
	---> ??? yerine öyle bir ifade yazın ki matematiksel yuvarlama işlemini yapsın.
	
	??? ====> dval >= 0 ? (int)(dval + 0.5) : (int)(dval - 0.5))
```
  
  # Rastgele Sayı Üretimi 
  
  - Çekiliş 
  - Eşleşme
  - Şifreleme
  - Game programming 
  - Genetic algorithm 
  - Olasılık hesabı 
  - İstatistiksel hesaplamalar
  - Test kodlarındaki test datası oluşturmak 
  - Bazı arama/sıralama algoritmaları
  
  
  
  	- iki kategoriye ayrılır.
  		- True random generations
  		- Pseudo random generations
  		
  
  
  pseudo random generation 
  	- Seed value ( algoritmayı başlatan değer - tohum değeri)
  	
- Endüstride en çok kullanılan random sayı algoritması 
	- Mersenne twister algorithm
		- Mersenne twister algoritmasının bu kadar çok kullanılmasının nedeni rastgeleliğin 
		birçok kriterini tam olarak karşılaması ve çokta yavaş olmaması.
	
  
  - Üniform Distribution : Üretilecek olan tüm olasılıkların ağırlığı aynı olması.
  
  - Bulunduğu kütüphane ve fonksiyon tanımları:
  	<stdlib.h>
	RAND_MAX
	int rand (void);
	void srand (unsigned int);
	
	
rand() --> fonksiyonun kullanıldığı seed (tohum) değeri 1 olduğu için üretilirken aynı sırada rastgele sayı üretilecektir.


	for (int i = 0; i < 5 ; i++)
	{
		printf(""%d",rand());
	}
-> Bu kodun üreteceği sayıların sırası belirlidir.(Default değer olan 1 değeri gönderilir)
	 Ekran çıktısı:
	 41 19467 6334 26500 19169
	 	olur. Ve bu sıralama ve değerler tohum değeri(seed) sabit olduğu için her seferinde aynı olur.
		
- Farklı tohum değeri gönderilerek farklı sayılar üretilmek istenirse;
srand(num) fonksiyonuna değer gönderilmelidir. Srand fonksiyonuna gönderilen tohum değeri değiştikçe üretilen rastgele sayılar da değişir.

	
		for (unsigned int i = 1; i < 100 ; i++)
		{ 
			srand(i);
			printf("tohum değeri %u için sayı zincirinin ilk 100 sayısı \n",i);
			
			for (int k =0 ; k < 100; ++k)
				printf("%5d ", rand());
				
			getchar();  // her döngüde bir tuşa basana kadar beklemesi için
			system("cls");  // her döngü sonunda ekranı temizliyor.
		}
  
  
  % --> üniform dağılım için kullanılmamalı ! 
  		örneklerde kullanacağız ama üretimde kullanılmamalı.
		
	

- Rastgele büyük harf üretimi:

		for (;;)
		{ 
			putchar(rand() % 26 + 'A');
			_getch();
		}
		
		
- Rastgele alfa-numeric karakter yazdırımı:
	
			int c;
			for (;;)
			{
				for (;;)
				{	
					c = rand() % 128;
					if (isalnum(c))
						break;
				}
				printf("%c ", c);
				_getch();
			}
  
  
  - Yukarıdaki kodu bir C idiyomu ile yazalım:
  	
		int c;
		for(;;)
		{
			while(!ispunct(c = rand() % 128))
			;// null statement
			
			putchar(c);
			_getch();
		}
		
- Yukarıdaki kodda fonksiyona argüman olarak gönderilen ifade atama operatörü ile oluşturulmuş
 Atama operatörünün ürettiği değer nesneye atanan değerdir. İspunct çağrısı punctration karakter olup olmadığını test ediyor. Punct değer olmadığı sürece while döngüsünde dönüyor.
 
 **Randomize idiyomu:
 
 - Calender time (takvim zamanı)
 	- Başarılı bir zaman noktasını (time point) orijin olarak alıyoruz.
 		- O orijin olarak alınan noktaya(değere) epoche denir.

<time.h> -> standart fonksiyon 

- Unix kökenli sistemlerde alınan bu orijin noktası(epoche) tarih olarak 01.01.1970'dir.

Bu idiyomun kullanım şekli ;

	#include <time.h> 
	
	srand((unsigned)time(NULL));
	for(int i = 0; i < 10; ++i)
	{
		printf("%d ",rand());
	}
	// Bu şekilde 10 adet rastgele sayı üretilmiş oldu.
  
  
  
  
  
        for(;;)
	{
		printf("%ld\r",time(NULL));// burada \r aynı satırın başına yazılmasını sağlar. yeni satıra geçilmez.
	}
 	---> Bu kodda ise epoche'den geçen saniye sayısı ekrana yazdırılır.
	
	
- Yazı-Tura sorusu:

	   #define NTOSS 1000000
	   #define HEADS 0
	   
	   int main()
	   {
	   	int heads_counter =0;
		forint i = 0 ; i < NTOSS; ++i)
			if(rand() % 2 == HEADS)
				++heads_counter;
		
		printf(" Tura gelme olasılığı : %.12f\n",(double)heads_counter/NTOSS);
	   }
  
  
  
  - Bir oyun algoritma örneği:
  	- 2 zar atılıyor.
  	- eğer bu iki zarın toplamı 
  	- 7 veya 11 olursa oyun kazanılır.
  	- 2,3 veya 12 olursa kaybedilir.
  	- 4,5,6,8,9 veya 10 olursa zar tekrar atılır ve aynı toplam bulunursa kazanılır. Ancak 7 atılırsa oyun kaybedilir.
  	- Yani örnek vermek gerekirse ;
  		- 7 atılırsa oyun kazanılır.
  		- 3 atılırsa kaybedilir.
  		- 9 atılırsa;
  			- ya tekrar 9 atılana kadar devam edilir ve 9 atıldığında kazanılır.
  			- ya da 7 atılana kadar devam edilir 7 atıldığında kaybedilir.
  		
- Bu oyunu oynaya oyuncunun kazanma olasılığını hesaplayan programı yazınız.


```

#include <stdio.h>
#include <time.h>
#include <stdlib.h>



#define ngames 10'000'000

int roll_dice(void)
{
	int dice_x = rand() % 6 + 1;//mod operatörü kullanımı olasılık hesaplarında yanlıştır. algoritme örneği olarak!!
	int dice_y = rand() % 6 + 1;

	return dice_x + dice_y;

}
//if game returns 1, player wins
//if game returns 0, player loses

int game_(int dice)
{
	int new_dice;
	for (;;)
	{
		new_dice = roll_dice();
		if (new_dice == 7)
			return 0;
		if (new_dice == dice)
			return 1;
	}
}

int game(void)
{
	int dice = roll_dice();

	switch (dice)
	{
	case 7:
	case 11: return 1;
	case 2:
	case 3:
	case 12:return 0;
	default: return game_(dice);
	}
}

int main()
{


	int win_count = 0;

	for (int i = 0; i < ngames; ++i)
	{
		win_count += game();
	}
	printf("oyuncunun kazanma olasiligi %f \n  ", (double)win_count / ngames);
}


```

# Ders 24 31/03/2021

- Global değişken tnaımlamaktan çekinmek gibi bir durum var mı? var .
	 - int g; global değişken kaynak dosyadaki fonksiyonların ortaklaşa kullanıldığı bir değişken.
	 - Global değişkenler yerel değişkenlerin işimizi gördüğü yerde kullanılmamalıdır.(eğer bir mecburiyet durumu yoksa)
	 


- rand() ---> 0 ile RAND_MAX arasında rastgele değer üreten fonksiyon.

- Bir soru:

	- Birim kare içerisinde yarıçapı 1 olan bir çeyrek daire yerleştirilmiştir. 
	Çeyrek dairenin alanının karenin alanına oranını bulan programı yazınız.(pi/4)
	
```
#include <stdio.h>
#include <stdlib.h>
#define NPOINTS 100000


int main()
{
	int inside_cnt = 0;
	for (int i = 0; i < NPOINTS; ++i)
	{
		double dx = (double)rand() / RAND_MAX;
		double dy = (double)rand() / RAND_MAX;

		if (dx * dx + dy * dy <= 1)
			++inside_cnt;

	}
	printf("pi = %.12f \n ", 4. * inside_cnt / NPOINTS);
}
```
	
  
  - Bir ödev sorusu:
   	- Bir oyuncu oyuna 100 dolar ile  girebilmektedir ve kasanın 100 doları vardır.
   	- Her el oyuncu oyuna devam edebilmek için 10 dolar kasaya ödeme yapmaktadır.
   	- Kasa da yazı-tura atmaktadır. 	
   		- Eğer 2 kez yazı gelirse kasa , oyuncuya 35 usd verir.
   		- Eğer 4 kez tura gelirse kasa , oyuncuya 65 usd verir. 
   	- Oyuncunun parası 10 doların altına düştüğünde veya kasa oyuncunun kazandığı parayı ödeyemeyecek kadar parası kaldığında oyun biter.
   
  ```
  #define _CRT_SECURE_NO_WARNINGS

#include <math.h>

#include <conio.h>
#include <ctype.h>
#include "nutility.h"

#include <stdio.h>
#include <time.h>
#include <stdlib.h>

#define NTOSS 100000
#define HEADS      0 
#define TAILS      1

int heads_or_tail(void)
{
	
		if (rand() % 2 == HEADS)
			return HEADS;
		return TAILS;
	
}



int main()
{
	while (1)
	{
		int win = 0, lose = 0;
		for (int i = 0; i < NTOSS; ++i)
		{
			
			int heads = 0, tail = 0, player = 100, bank = 100;

			while (player > 10)
			{
				player -= 10;
				bank += 10;

				if (heads_or_tail() == HEADS)
				{
					tail = 0;
					++heads;
					if (heads == 3)
					{

						bank -= 65;
						if (bank <= 0)
						{
							++win;
							goto bitis;
						}
						player += 65;
						heads = 0;
					}
				}
				else
				{
					heads = 0;
					++tail;
					if (tail == 2)
					{
						bank -= 35;
						if (bank <= 0)
						{
							++win;
							goto bitis;
						}
						player += 35;
						tail = 0;
					}
				}


			}
			++lose;

		bitis:
			;// null statement
		}

		printf("Bu oyunu kazanma olasiliginiz: %.12lf\n ", (double)win / NTOSS);
		_getch();
	}
} 


  ```
  
  # Diziler
  
  - Data structure: işleme sokulacak verilerin işleme sokulabilmesi için bellekte nasıl konumlandırılacağına ilişkin düzenek.

- C'nin standart kütüphanesinde dinamik dizi yoktur. Sadece fixed array mevcuttur.
  
  - Time Complexity: Bir algoritmanın çalışması için gerekli olan süredir.
   Ancak buradaki süre saniyelerin hesaplanmasıyla değil, kaç tane işlem gerçekleştirdiğine göre yapılmaktadır.
   
   - Big O terimleri ve Senaryoları:
   	- O(1) -> Constant
	- O(N) -> Linear
	- O(N^ 2) → Quadratic
	- O(log N) → Logarithmic
	- O(N log N) → Linearithmic
	- O(c^N)→ Exponential
	- O(N!) → Factorial

- int a[100]; --> ilk değer verilmezse çöp değer ile hayata başlar.

- void func(void)
  {
 	 int ax[5];---> çöp değer ile 
  	 static int sa[40]; ---> 0 değeri ile hayata başlar.
  }
  
  
  - C dilinde bir fonksiyonun parametresi bir dizi olamaz. 
  Diziler fonksiyonlardan fonksiyonlara call by value olarak aktarılmıyor.
  - C dilinde bir fonksiyonun geri dönüş değeri türü dizi olamaz.
 
    
    	void func(int a[5])
	{	}---> Dikkat : parametre bir dizi gibi görünse de bir pointer değişkendir.7
	İlerleyen konularda ayrıntılı değineceğiz.
	
	[] ---> index/ subscript
	
#### Undefined Behaviour
#
Dizinin boyutu dışında veya negaitif bir terimine atama yapmak tanımsız davranıştır.
#


- a[5] ---> l value expression.
	- a[5]++
	- ++a[5]
	- &a[5]
	
	
- Bir dizi ismi bir ifade içinde kullanıldığında (birkaç istisnai durum hariç) 
her zaman dizinin ilk elemanının adresine dönüştürülür.
	- Yani a bir ifade içinde kullanıldığında &a[0] gibi düşünülebilir.
  
  
  
  
# Ders 25 02.04.2021

- Array Decay 
	- Array to pointer conversion 

	- int a[10]
	- a ===> &a[0]
	
- Bir dizi tanımlandıktan sonra dizinin ismini bir ifade içerisinde kullanıyorsunuz ve derleyici 
dizi ismini dizinin ilk elemanının adresine dönüştürüyor. İşte buna array decay deniyor.



- Bir mülakat sorusu:

- Aşağıdaki programda 10 adet rastgele şifre üretilmek istenmiştir. 
Ancak şifrelerin hepsi aynı olmaktadır. Hata nerede yapılmıştır???

```
int random_char(void)
{
	int c;
	while(!isalnum(c = rand() % 128)
		; // null statement
		
	return c;
}

void printf_random_password(void)
{
	srand(time(NULL));
	int len = rand() % 5 + 6;
	for (int i = 0; i < len; ++i)
	{
		putchar(randam_char());
	}
	putchar('\n');
}
int main()
{
	for (int i = 0; i < 10; ++i)
	{
		printf_random_password();
	}
}
```
  
- Cevap: Main fonksiyonundaki for döngüsü çok hızlı döndüğü için srand fonksiyonuyla
tohum değeri verme işlemi bir döngünün içerisinde olmamasına dikkat edilmelidir. En uygun yeri 
main fonksiyonun başıdır.


- Dizilere ilk değer verilmesi:
	- int a[10] = {0, 1, 2, 3, 4, 5, 6, 7, 8, 9};
	- int [3] = {1, 2, 3, 4} // geçersiz (boyut aşımı)
	- Dizinin boyutundan daha az ilk değer verildiğinde diğer değerler default olarak 0 ilk değeri alır.
	- int a[5]; ---> Dizinin elemanları hayata çöp değer ile başlar.
	- int a[3] = {1, 2, 3,} --> trailing comma
	- int a[]; --> sentaks hatası
	- int a[] = {1, 2, 3, 4, 5} --> sentaks hatası yok. Dizinin boyutu otomatik olarak 5 algılanır.

- Dizinin boyutunu belirten ifade sabit ifadesi olmalıdır.

		 int x = 5; 
		 int a[x]; --> geçerli değildir.
		 
		 
		 
- int a[] = {[5] = 67, [3] = 45, [1] = 11};// designated initializer
	- 6 elemanlı olarak tanımlamış olur ve değer verilmeyen elemanlar 0 olarak varsayılır.


- Bir döngü içerisinde a[i] ve i[a], ikiside a dizisinin i. elemanı anlamına gelir.


  - Rastgele sayılarla bir dizi oluşturup elemanları toplamını bulan program:


  ```
  #include <stdio.h>
  #include <stdlib.h>
  #include <time.h>
  
  #define SIZE 20
  #define asize(x)  (sizeof(x) /sizeof(x[0]))
  
  void set_array_random(int* p, int size)
  {
	while (size--)
		*p++ = rand() % 1000;
  }
  void print_array(const int* p, int size)
  {
	for (int i = 0; i < size; ++i)
	{
		if (i != 0 && i % 20 == 0)
			printf("\n");
		printf("%3d ", p[i]);
	}
	printf("\n----------------------------------------------\n");
  }
  
  int main()
  {
  	 int a[SIZE]
 	 int sum = 0;
 	 randomize();
 	 set_array_random(a, SIZE);
	 print_array(a, SIZE);
	 for(int i = 0; i < SIZE; ++i)
	 {
	 	sum += a[i];
	 }
  	printf("sum = %d\n ",sum);
  }
  
  ```
  
  - Rastgele oluşturulan bir dizide tek elemanların aritmetik ortalamasını bulunuz.
  
  ```
  #include <stdio.h>
  #include <stdlib.h>
  #include <time.h>
  
  #define SIZE 20
  #define asize(x)  (sizeof(x) /sizeof(x[0]))
  void set_array_random(int* p, int size)
  {
	while (size--)
		*p++ = rand() % 1000;
  }
  void print_array(const int* p, int size)
  {
	for (int i = 0; i < size; ++i)
	{
		if (i != 0 && i % 20 == 0)
			printf("\n");
		printf("%3d ", p[i]);
	}
	printf("\n----------------------------------------------\n");
  }
  
  int main ()
  {
  	int a[SIZE];
	int add_sum = 0;
	int add_cnt = 0;
	
	randomize();
	set_array_random(a,SIZE);
	print_array(a,SIZE);
	
	for(int i = 0; i < SIZE; ++i)
	{
		if(a[i] % 2 != 0)
		{
			odd_sum += a[i];
			++odd_cnt;
		}
	}
	if(odd_cnt)----> paydanın 0 olma ihtimali her zaman göz önünde bulundurulmalıdır.
		printf("teklerin ortalamasi = %f\n",(double)odd_sum/odd_cnt);
	else
		printf(" dizide tek sayi yok.");
  }
  ```
  
  
  - Fundamental Algorithms
  	- Linear search (Doğrusal Arama);
  - 3 farklı Algoritmada ekrana girilen değeri dizinin içinde bulan 
  ve hangi indiste olduğunu gösteren program aşağıdadır.
  
  
  ```
   #include <stdio.h>
  #include <stdlib.h>
  #include <time.h>
  
  #define SIZE 20
  #define asize(x)  (sizeof(x) /sizeof(x[0]))
  void set_array_random(int* p, int size)
  {
	while (size--)
		*p++ = rand() % 1000;
  }
  void print_array(const int* p, int size)
  {
	for (int i = 0; i < size; ++i)
	{
		if (i != 0 && i % 20 == 0)
			printf("\n");
		printf("%3d ", p[i]);
	}
	printf("\n----------------------------------------------\n");
  }
  
  int main()
  {
  	int a[SIZE];
	randomize();
	set_array_random(a,SIZE);
	print_array(a,SIZE);
	int sval;
	printf("Aranacak degeri giriniz:");
	scanf("%d",&sval);
	
	// ilk algoritma
	int i ;
	int fount = 0;
	for(i = 0; i < SIZE; ++i)
	{
		if(a[i] == sval)
		{
			found = 1;
			break;
		}
	}
	if(found)
	{
		printf("bulundu dizinin %d elemani",i);
	}
	else 
		printf("bulunamadi\n"
		
	
	//ikinci algoritma
	int i; 
	for (i = 0; i<SIZE; ++i)
	{
		if(a[i] == sval)
			break;
	}
	if(i < SIZE)
		printf("bulundu dizinin %d elemani.\n",i);
	else
		printf("bulunamadi\n");
	
	
	//Üçüncü algoritma
	
	int i;
	for(i = 0; i < SIZE && a[i] != sval; ++i)
		; // null statement
	
	if(i < SIZE)
		 printf("bulundu dizinin %d elemani",i);
	else 	
		printf("bulunamadi");
		
  }
  ```
  
   
  #### Sizeof Operatörü
  
  - Anahtar sözcükte operatör olan tek anahtar sözcük.
  - Compile - time operator
  	- Diğer operatörlerden farklı olarak bu operatörün ürettiği değer derleme zamanında derleyici 
  	tarafından bir sabit olarak elde edilecek.
	
- sizeof operatörü bir türün storage ihtiyacınının kaç byte olduğunu gösterir.
- sizeof operatörünün ürettiği değer derleyiciye bağlı olan işaretsiz tam sayı türünde bir değerdir.

- Kullanım şekli:

		sizeof(int)
		printf("sizeof(int) = %zu\n",sizeof(int));
		
		

  
- Sabit değer ürettiğine dair;

		int x = 10;
		int a[x];---> sentaks hatası
		int a[sizeof(double)] ---> sentaks hatası değil
	
- sizeof operatörünün operantı herhangi bir ifade olabilir. Bu durumda derleyici operant 
olan ifadenin türüne bakar ve o türün storage değerini elde eder.
	- Bu kullanımda ifadenin parentez içerisinde olması gerekmiyor.

- Örnek olarak : 

		int x = 9;
		printf("%zu\n", sizeof x + 5);  --> ekran 9 değeri yazdırılır.
		printf("%zu\n",sizeof (x + 5));---> ekrana 4 değeri yazdırılır.
		
		char c;
		printf("%zu\n",sizeof c);---> ekrana 1 yazdırılır.
		printf("%zu\n",sizeof +c);---> ekrana 4 değeri yazdırılır.
		
		
- Unevaulated Context 
	- Bazı ifadedeki işlemler için derleyici işlem kodu üretmiyor.
- Dilin kuralları diyor ki, sizeof operatörünün operandı olan ifade için derleyici işlem kodu üretmez.

		int x = 10;
		printf("%zu\n ",sizeof(x++));
		printf("%d\n",x);--> burada x değeri sizeof operatörünün
		içerisindeki ++ operatörünün etkisine maruz kalmadığı için 
		x değeri ekrana 10 olarak yazdırılır.

- Mesela ;

		int foo(void)
		{
			printf("foo fonksiyonu çağırıldı.");
			return 1;
		}
		
		int main()
		{
			unsigned int x  = sizeof(foo());
		}--> foo fonksiyonu çağırılmaz. foo fonksiyonunun geri dönüş türünün byt'ı yazdırılır.
		
		
		

- Array decay de nadir istisnalardan :

		int a[10]; 
		sizeof(a);---> array decay uygulanmaz.
- Örnek olarak:

		char buf[200];
		int a[50];
		double da[20];
		
		printf("sizeof(buf) = %zu \n",sizeof(buf));--->200 * 1 byte = 200
		printf("sizeof(a) = %zu\n",sizeof(a));---> 50 * 4 byte= 200
		printf("sizeof(da) = %zu\n",sizeof(da);---> 20 * 8 = 160
		
		
- sizeof(a[0]) = dizinin bir teriminin byte'ını verir.
- sizeof(a) --> dizinin kaç byte yer kapladığını verir.
- sizeof(a) / sizeof(a[0]); --> dizinin eleman sayısını verir.

- Örnek kullanım:

		int a[] = { 2, 5, 7, 9, 11, 13,}
		for (int i = 0; i < sizeof(a) / sizeof(a[0]); ++i);
			printf("%d ",a[i]);
			
			
			
- Mülakat Sorusu:

		int a[5] = {0, 1, 2, 3, 4};
		for ( int i =-2; i < sizeof(a) / sizeof(a[0]); ++i)
			printf("%d ", a[i+2]);
			
- Yukarıdaki kodun ekran çıktısı ne olur??
	- Ekrana hiçbirşey yazılmaz. Sebebi ise sizeof operatörü işaretsiz tam sayı türündendir. 
	İşaretli -2 sayısı işaretsiz tam sayı türüne dönüştürüldüğünde çok yüksek bir sayı olarak
	dönüşür. Ve bu yüksek sayı ile dizinin boyutu olan ifade kıyaslandığında for döngüsüne 
	girilmeden program biter.
	

		
  
  
  # Ders 26 - 05.04.2021
  
  		int x = 10;
		printf("%zu\n",sizeof(x > 5 ? 1: 2.4)); 
		---> Burada koşul operatörünün ikinci operatörü olan 1 sayısı üretilir ancak double olarak üretileceği için 
		sizeof operatörünün ürettiği değer 8 olacaktır. Yani koşul operatöründe otomatik tür dönüşümü sadece 
		üretilecek değere göre değil de 2. ve 3. operanttan uygun olana yapılır.
  
  
  - Rastgele sayi üreten bir dizi tanımlansın. Dizinin içerisinde sadece 
  1 adet olan aynı sayıdan başka olmayan elemanlar ekrana yazdırılsın.
  	- Print all unique elements of an array.
  	
``` 
#define _CRT_SECURE_NO_WARNINGS

#include <stdio.h>
#include <ctype.h>
#include <stdlib.h>


#define SIZE		10
#define randomize()  srand((unsigned)time(NULL))



int main()
{
	
	int str[SIZE];
	randomize();
	
	for (int i = 0; i < SIZE; ++i) {
		str[i] = rand() % 20;
		printf("%3d ", str[i]);
	}
	printf("\n\n");

	/***1. Çözüm***
	* O(n^2) karmaşıklığında
	
	for (int i = 0; i < SIZE; ++i) {
		int cnt = 0;
		for (int k = 0; k < SIZE; ++k) {
			if (str[i] == str[k] && i != k)
				++cnt;
		}
		if (!cnt)
			printf("%3d ",str[i]);
	}*/

	/***1. Çözüm break statement ile***
	* O(n^2) karmaşıklığında (complexity)
	
	int i, j;
	for (i = 0; i < SIZE; ++i) {
		
		for (j = 0; j < SIZE; ++j) {
			if (i != j && str[i] == str[j])
				break;
		}
		if (j == SIZE)
			printf("%3d ", str[i]);
	}*/
	 
	/***2. Çözüm*** --> Bu çözüm logaritma karmaşıklığı yönünden avantajlı 
	lakin bellek kullanımı bakımından da dezavantajlı olduğu göz önünde bulundurulmalıdır.
	* O(2n) karmaşıklığı (complexity) ile
	
	int cnt[20] = { 0 };
	for (int i = 0; i < SIZE; ++i)
		++cnt[str[i]];

	for (int i = 0; i < 20; ++i) {
		if (cnt[i] == 1)
			printf("%3d ", i);
	}*/



}
```
  
  
  
  - Max Subsequence Algorithm
  	- Subsequence: Bir dizinin içerisinde ardışık n tane elememan. Yani bir tür alt dizi.
  	- Max Subsequence: Öyle bir alt dizi bulunacak ki bu alt dizinin elemanları 
  	toplamı bu dizide bulunabilecek en büyük toplam olacak.  
		- Bu kuralın uygulanabilmesi için dizinin elemanlarından en az biri negatif olmalıdır.
  
```
#define _CRT_SECURE_NO_WARNINGS
#include <stdio.h>
#include <ctype.h>
#include <stdlib.h>
#include "nutility.h"


#define SIZE	10

int main()
{				
	int a[9] = { 2, -5, -8, 4, -3, 6, -5, 7, -1 };

	print_array(a, 9);
	
	int max_so_far = a[0];
	int max_ending_here = 0;
	int start = 0, end = 0, s = 0;

	for (int i = 0; i < 9; ++i) {
		max_ending_here += a[i];
		if (max_so_far < max_ending_here) {
			max_so_far = max_ending_here;
			end = i;
			start = s;
		}
		if (max_ending_here < 0) {
			max_ending_here = 0;
			s = i + 1;
		}
	}
	printf("Maksimum contiguous sum is %d \n", max_so_far);
	printf("Start index is %d\n", start);
	printf("End index is %d\n", end);
}
	
```
  
  
- Sıralama	
	- Sorting Algorithm
  
 - Sorting, belirli bir kurala göre dizinin verilerini konumlandırmak.
 	- Sorting Criteria --> Sıralama Kriteri


- Bubble Sort Algorithm:

        
        int a[SIZE];
        randomize();
        set_array_random(a, SIZE); 
        print_array(a, SIZE);

        for (int i = 0; i < SIZE - 1; ++i) {
		for (int k = 0; k < SIZE - i - 1; ++k) {
			if (a[k] > a[k + 1]) {
				int temp = a[k];
				a[k] = a[k + 1];
				a[k + 1] = temp;
			}
		}
        }
        print_array(a, SIZE);
	
 
 - Tek sayıların sol tarafta sıralı olduğu çiftlerin ise sağ tarafta sıralı olduğu program:
 
```
#define _CRT_SECURE_NO_WARNINGS

#include <stdio.h>
#include <ctype.h>
#include <stdlib.h>
#include "nutility.h"


#define SIZE	20

int main()
{
	int a[SIZE];
	randomize();
	set_array_random(a, SIZE);
	print_array(a, SIZE);

	for (int i = 0; i < SIZE - 1; ++i) {
		for (int k = 0; k < SIZE - i - 1; ++k) {
			if ((a[k] > a[k + 1] && a[k] % 2 == a[k + 1] % 2) || (a[k] % 2 == 0 && a[k + 1] % 2 != 0)) {
				int temp = a[k];
				a[k] = a[k + 1];
				a[k + 1] = temp;
			}
		}
	}
	print_array(a, SIZE);
}
-----------------------------------------------------------------------------------------------------
if ((a[k] > a[k + 1] && a[k] % 2 == a[k + 1] % 2) || (a[k] % 2 == 0 && a[k + 1] % 2 != 0))
- Yukarıdaki koşul ifadesini yakından incelediğimizde eğer -yan yana olan iki indexten;
	- İkiside tek veya ikiside çift ise ve sol index sağdakinden büyükse yer değiştirilir.
	- Ya da soldaki çift ve sağdaki tek ise yer değiştirilir.
```
 
  
  - Merge Algoritması
  	- İki diziyi sıralı bir şekilde birleştirme.
  	
```	
#define _CRT_SECURE_NO_WARNINGS

#include <stdio.h>
#include <ctype.h>
#include <stdlib.h>
#include "nutility.h"


#define SIZE	20



int main()
{
	int a[SIZE];
	int b[SIZE];
	int c[SIZE * 2];

	set_array_random(a, SIZE);
	sort_array(a, SIZE);
	print_array(a, SIZE);

	set_array_random(b, SIZE);
	sort_array(b, SIZE);
	print_array(b, SIZE);

	int idx_a = 0;
	int idx_b = 0;


	for (int i = 0; i < SIZE * 2; ++i) {
		if (idx_a == SIZE)
			c[i] = b[idx_b];
		else if (idx_b == SIZE)
			c[i] = a[idx_a];
		else if (a[idx_a] < b[idx_b])
			c[i] = a[idx_a++];
		else
			c[i] = b[idx_b++];
	}
	print_array(c, SIZE * 2);

} 	
	
```  
 
  - Binary Search 
   	- Sıralı bir veri yapısında bir değer aramaya yönelik bir örnek.
   		- O(log n) karmaşıklığında.
   		
```
#define _CRT_SECURE_NO_WARNINGS

#include <stdio.h>
#include <ctype.h>
#include <stdlib.h>
#include "nutility.h"


#define SIZE	10



int main()
{
	int a[SIZE];
	int num;
	
	randomize();
	set_array_random(a, SIZE);
	sort_array(a, SIZE);
	print_array(a, SIZE);
    
	printf("Bir sayi giriniz: \n");
	scanf("%d", &num);

	int idx_first = 0;
	int idx_last = SIZE - 1;
	int idx_mid;

	while (idx_first <= idx_last) {
		idx_mid = (idx_first + idx_last) / 2;
		if (num == a[idx_mid])
			break;
		if (a[idx_mid] > num)
			idx_last = idx_mid - 1;
		else
			idx_first = idx_mid + 1;
		
	}
		
	if (idx_first > idx_last)
		printf("Aranan sayi bulunamadi \n ");
	else
		printf("Aranan sayi %d indiste bulundu\n", idx_mid);
}
```

# Ders 27 - 07.04.2021
  
  - Partition Algorithm
  	- Bir dizi tanımlayın. Tekler başta, çiftler sonra olacak şekilde sıralayın. 
  	Partisyen noktasının indeksini yazdırın.
```
#define _CRT_SECURE_NO_WARNINGS

#include <stdio.h>
#include <ctype.h>
#include <stdlib.h>
#include "nutility.h"


#define SIZE	10



int main()
{
	int a[SIZE];
	randomize();
	set_array_random(a, SIZE);
	print_array(a, SIZE);

	for (int i = 0; i < SIZE; ++i) {
		for (int k = 0; k < SIZE - i - 1; ++k) {
			if ((a[k] > a[k + 1] && a[k] % 2 == a[k + 1] % 2) || (a[k] % 2 == 0 && a[k + 1] % 2 != 0)) {
				int temp = a[k];
				a[k] = a[k + 1];
				a[k + 1] = temp;
			}
		}
	}
	print_array(a, SIZE);
	int i;
	for (i = 0; i < SIZE; ++i) {
		if (a[i] % 2 == 0)
			break;
	}
	if (i == SIZE)
		printf("Cift sayi yoktur.\n");
	else
		printf("partisyen noktasi %d. sayidir.", i + 1);

}

```
  
  
# String Literals (Yazılar)

- char str[100];
- '\0' ---> null character
- '0'  ---> sıfırn kod numarası [48 ASCII]
  
  - Yazının son karakterinden sonra artık yazının başka bir karakteri olmadığı için
  dizinin o elemanına özel bir değer atanıyor. Bu null karakterdir.
  
  - char[100];
  	- Bu yazının alabileceği en uzun yazı uzunluğu 99'dur. En az 0 uzunluğunda olur. Sebebine gelecek olursak, 
  	100 karakterlik bir dizi ve sonunda null karakter olacağı için 99 karakter alabilir.
	
Örnek: 
```
	int main()
	{
		char str[100];// Eğer burada dizi global isim 
		//alanında tanımlanırsa dizinin diğer elemanlarına 0 değeri atandığı için ub olmaz.
		
		str[0] = 'C';
		str[1] = 'A';
		str[2] = 'N';
		
		for (int i = 0; str[i] != '\0'; ++i) 
			putchar(str[i]);
		
	}// Undefined Behavior olur. Çünkü dizi for döngüsü içerisinde çöp değerleri de kullanıldı.
	// Eğer str[3] = '\0'; eklenirse undefined behavior olmaz.
```
  - String diziler için for döngüsü idiyomları:
  	- for (int i = 0; str[i] != 0; ++i);
  	- for (int i = 0; str[i], ++i);
  	
- C'de yazının uzunluğunu bir fonksiyon çağırmadan ya da bir döngü oluşturmadan bulma şansımız yok.
!!!Yazının boyutu ile dizinin boyutunu karıştırmamak lazım.!!!

- İnitialization
	- char str[100] = { 'R', 'A', 'S', 'I', 'T' };
		- Burada neden UB yok?
			- Bir dizinin ilk değer almasında verilen değerlerin sayısı dizinin boyutundan
			daha az ise geriye kalan bütün elemanlar sıfırlanır. 
			
	- char str[] = { 'R', 'A' };
		- Bu şekilde döngüde kullanılırsa UB olur. Çünkü dizinin boyutu belirtilmediği için
		dizinin boyutu 2 elemanlı alındı. Bu yüzden de dizinin son elemanı 'A' oldu. Yani null statement olmadığı
		için UB oldu.
  
  - char str[] = { 'R', 'A', 'S', '\0' };
  - printf("%zu", sizeof(str));--> Ekrana 4 yazdırılır. 4x1.
  - Yazının uzunluğu ise 3'tür.



- char str[3] = { 'a', 'b', 'c' };	
  for (int i = 0; str[i] != '\0'; ++i)
  	putchar(str[i]);
	- UB olur. Döngü diziyi taşıracaktır.
  
  
  
  - char str[] = "furkan";
    printf("sizeof(str) = %zu\n",sizeof(str));---> ekrana 7 yazdırılır.
    
    
    
    
   - char str[SIZE];
     printf("Bir yazı giriniz:\n ");
     scanf("%s", str);
     	- scanf fonksiyonuna str dizisi array decay olarak adres gönderilmiş.
     	- &str[0] olarak da gönderilebilirdi.
	- Ancak &str olarak gönderilemez. Bu şekilde gönderimin farklı bir anlamı vardır.
     for (int i = 0; str[i] != '\0'; ++i)
     	putchar(str[i]);
		- Bu şekilde içinde boşluk olmayan yazılar alınıp ekrana yazdırılır ancak boşluktan sonrası yazdırılmaz.
		
    
    - str[0] = "ali"; --> Bu c'de bir sentaks hatası değil ama yanlıştır.
     Bir tam sayı değişkene bir adres atamış oluyorsunuz.
     
     
     
     - char[SIZE] = "erdinc kaya";
       printf("isim : %s\n",str);
       		- Tüm ismi yazar.
       		

     
     - **puts fonksiyonu:
     	- Variadic bir fonksiyon değildir.
     
      		char name[100] = "ali";
		char surname[100] = "ertolga";
		
		puts(name); --> ali'yi ekrana yazdırır ve '\n' karakterini kendisi verir.
		
	

  void sgets (char*p)
  {
  	int c;
	while ((c = getchar()) != '\n')
		*p++ = (char)c;
	*p = '\0';
  }
	
  int main()
  {
  	char str[SIZE];
	printf("Bir yazi giriniz: ");
	sgets(str);
	printf("yazi : [%s] \n", str);
  }--> Bu kodda boşluk karakteri olsa dahi tüm satırı diziye alabilecektir.
  
  
  
  
  - Yazının uzunluğunu bulan program:
  
  		char str[SIZE];
		printf("Bir yazi girin: ");
		sgets(str);
		
		int len = 0;
		for (int i = 0; str[i] != 0; ++i)
			++len;
		printf("dizinin uzunlugu : %d", len);
		
		// ya da
		int i;
		for (i = 0; str[i] != '\0'; ++i)
			; // null statement
			
		printf("Uzunluk : %d\n", i);

- Bir yazı girilsin. Girilen yazı ilk olarak girildiği gibi ekrana yazdırılsın.
Sonra sonuna ! konularak yazdırılsın.

```
#define _CRT_SECURE_NO_WARNINGS

#include <stdio.h>
#include <ctype.h>
#include <stdlib.h>
#include "nutility.h"


#define SIZE	100



int main()
{

	char str[SIZE];
	printf("Bir yazi giriniz: ");
	sgets(str);

	/*** 1. Çözüm***
	int i;
	for (i = 0; str[i] != '\0'; ++i)
		putchar(str[i]);
	printf("\n");
	str[i++] = '!';
	str[i] = '\0';

	for (i = 0; str[i] != '\0'; ++i)
		putchar(str[i]);*/

	/*** 2. Çözüm***
	int i;
	for (i = 0; str[i] != '\0'; ++i)
		; // null statement
	printf("[%s] \n",str);
	
	str[i++] = '!';
	str[i] = '\0';
	printf("[%s] \n",str);*/

}

```

- İki kelime toplayan kod:

```
#define _CRT_SECURE_NO_WARNINGS

#include <stdio.h>
#include <ctype.h>
#include <stdlib.h>
#include "nutility.h"


#define SIZE	100



int main()
{
	char s1[SIZE];
	char s2[SIZE];
	char s3[SIZE];

	printf("iki kelime giriniz:");
	scanf("%s%s", s1, s2);

	int i;
	for (i = 0; s1[i] != '\0'; ++i) {
		s3[i] = s1[i];
	}
	int k;
	for (k = 0; s2[k] != '\0'; ++k)
		s3[i + k] = s2[k];
	s3[i + k] = '\0';

	printf("[%s] +[%s] = [%s] ", s1, s2, s3);
}
	
	
```

  
- Ekrana bir yazı girilsin. Girilen yazıda ekrana girilen karakter aratılıp kaç tane olduğu ekrana yazılsın.
```
#define _CRT_SECURE_NO_WARNINGS

#include <stdio.h>
#include <ctype.h>
#include <stdlib.h>
#include "nutility.h"


#define SIZE	100



int main()
{
	char str[SIZE];

	printf("Bir yazi giriniz:\n");
	sgets(str);

	printf("Ekrana bir karakter giriniz: ");
	int c = getchar();
	
	int cnt = 0;

	for (int i = 0; str[i] != '\0'; ++i) {
		if (c == str[i])
			++cnt;
	}
	printf("%d tane \n", cnt);


}
---> Eğer büyük-küçük harf duyarlılığı olmasın dersek

	if(toupper(s[i] == toupper(c))
     olarak if ' i güncelleyebiliriz.
```



 
- Ekrana bir yazı girilecek. Yazıda her harften kaç tane olduğunu ekrana yazdıran program.

```
#define _CRT_SECURE_NO_WARNINGS
#include <stdio.h>
#include <ctype.h>
#include <stdlib.h>
#include "nutility.h"


#define SIZE	100



int main()
{
	char str[SIZE];
	int cnt[26] = { 0 };

	printf("Ekrana bir yazi giriniz: \n");
	sgets(str);

	int i;
	for (i = 0; str[i] != '\0'; ++i) {
		if (isalpha(str[i])) {
			
			++cnt[toupper(str[i]) - 'A'];
		}
	}

	for (int k = 0; k < 26; k++) {
		if(cnt[k] != 0)
			printf("[%c]  [%d]\n", 'A' + k, cnt[k]);
	}
}
```
  
  
  - İlave bir dizi kullanmadan girilen 2 kelimenin yerlerini değiştir.
  ```
  #define _CRT_SECURE_NO_WARNINGS

#include <stdio.h>
#include <ctype.h>
#include <stdlib.h>
#include "nutility.h"


#define SIZE	100



int main()
{
	char str[SIZE];
	printf("Aralarinda tek bir bosluk karakteri olan iki isim giriniz: \n");
	sgets(str);
	printf("[%s] \n", str);

	

	int i;
	int idx_first1, idx_first2, idx_last1, idx_last2;
	idx_first1 = 0;
	for (i = 0; str[i] != ' '; ++i)
		; // null statement
	idx_last1 = --i;
	idx_first2 = i + 2;
	for (; str[i] != '\0'; ++i)
		;
	idx_last2 = --i;
	printf("[%d  %d] [%d   %d] \n", idx_first1, idx_last1, idx_first2, idx_last2);

	//[ahmet necati]
	//[necati ahmet]
	//[nahmet ecati]
	//[neahmet cati]
	//[necahmet ati]
	//[necaahmet ti]
	//[necatahmet i]
	//[necatiahmet ]


	for (int j = 0; idx_first2 != idx_last2 + 1; ++j) {
		for (int k = idx_first2++ - 1; k >= j; k--) {
			printf("%d\n", k);
			char temp = str[k];
			str[k] = str[k + 1];
			str[k + 1] = temp;
		}
			++idx_first1;
			++idx_last1;
	printf("[%d  %d] [%d   %d] \n", idx_first1, idx_last1, idx_first2, idx_last2);
	printf("[%s] \n", str);
	}
	//[6  10] [12   11]
	//[necatiahmet ]
	for (int j = idx_last1; j > idx_first1 - 1; --j) {
		char temp = str[j];
		str[j] = str[j + 1];
		str[j + 1] = temp;
	}
	printf("[%d  %d] [%d   %d] \n", idx_first1, idx_last1, idx_first2, idx_last2);
	printf("[%s] \n", str);
	
	pline();
	printf("[%d  %d] [%d   %d] \n", idx_first1, idx_last1, idx_first2, idx_last2);
	printf("[%s] \n", str);
	

}
	
  ```
  
 - Ekrana bir yazı girilecek bir de karakter girilecek .
  Girilen karakter girilen yazıdan çıkarılacak ve yazının girilen karaktersiz hali ekrana yazdırılacak.
  
```
#define _CRT_SECURE_NO_WARNINGS

#include <stdio.h>
#include <ctype.h>
#include <stdlib.h>
#include "nutility.h"


#define SIZE	100



int main()
{
	char source[SIZE];
	char dest[SIZE];
	printf("Ekrana bir yazi giriniz: \n");
	sgets(source);
	printf("[%s]\n", source);

	printf("Ekrandaki yazidan hangi karakterin cikmasini istersiniz? \n");
	int c = getchar();
	int idx_write = 0;
	for (int i = 0; source[i] != '\0'; ++i) 
		if (source[i] != c) 
			dest[idx_write++] = source[i];
	dest[idx_write] = '\0';
	printf("[%s] \n", dest);

	
}
```
 - Yukarıdaki programı bir de ek bir dizi kullanmadan yapalım.
```
#define _CRT_SECURE_NO_WARNINGS

#include <stdio.h>
#include <ctype.h>
#include <stdlib.h>
#include "nutility.h"


#define SIZE	100


int main()
{
	char str[SIZE];
	printf("Bir yazi giriniz: \n");
	sgets(str);
	printf("Bir karakter giriniz: \n");
	int c = getchar();

	int idx_write = 0;
	for (int i = 0; str[i] != '\0'; ++i)
		if (str[i] != c)
			str[idx_write++] = str[i];
	str[idx_write] = '\0';
	printf("[%s] ", str);

}
```

 - Reverse Algorithm
 	- Bir veri yapısındaki öğeleri ters çeviren algoritma
 ```
 #define _CRT_SECURE_NO_WARNINGS

#include <stdio.h>
#include <ctype.h>
#include <stdlib.h>
#include "nutility.h"
#include <time.h>

#define SIZE	100


int main()
{
	char str[SIZE];
	
	printf("Bir yazi giriniz:\n");
	sgets(str);
	
	int len = 0;
	for (int i = 0; str[i] != '\0'; ++i) {
		++len;
	}

	printf("[%s] \nboyut : %d\n", str, len);

	for (int i = 0; i < len / 2; ++i) {
		char temp = str[i] ;
		str[i] = str[len - i - 1];
		str[len - i - 1] = temp;
	}
	
	printf("[%s] \n", str);



}
 ```
	
  - Ya da
  
  
  ```
  #define _CRT_SECURE_NO_WARNINGS

#include <stdio.h>
#include <ctype.h>
#include <stdlib.h>
#include "nutility.h"
#include <time.h>

#define SIZE	100


int main()
{

	int a[SIZE];
	randomize();
	set_array_random(a, SIZE);
	print_array(a, SIZE);

	for (int i = 0; i < SIZE / 2; ++i) {
		int temp = a[i];
		a[i] = a[SIZE - i - 1];
		a[SIZE - i - 1] = temp;
	}

	print_array(a, SIZE);

}
  
  ```
  
- Örnek mülakat sorusu:
	- Bir yazının tersten ve düzden okunuşu aynı ise polindrom sayıdır.
	
- Para hazır, ama Rıza harap.

```
#define _CRT_SECURE_NO_WARNINGS

#include <stdio.h>
#include <ctype.h>
#include <stdlib.h>
#include "nutility.h"
#include <time.h>

#define SIZE	100


int main()
{
	
		char str[SIZE];
		char temp[SIZE];

		printf("bir yazi giriniz: \n");
		sgets(str);
		printf("[%s]\n", str);

		int len = 0;
		for (int i = 0; str[i] != '\0'; ++i)
			if (isalpha(str[i]))
				temp[len++] = toupper(str[i]);

		int i;
		for (i = 0; i < len / 2; ++i) {
			if (temp[i] != temp[len - 1 - i])
				break;
		}

		if (i == len / 2)
			printf("palindrom yazidir.");
		else
			printf("palindrom degildir.");
	
}
```
  
 - Ekrana bir yazı girelim ve kaç kelimeden oluştuğunu ekrana yazdıralım.
 
```
#define _CRT_SECURE_NO_WARNINGS

#include <stdio.h>
#include <ctype.h>
#include <stdlib.h>
#include "nutility.h"
#include <time.h>

#define SIZE	  100
#define OUTWORD		0
#define INWORD	    1


int main()
{
		char str[SIZE];

		printf("bir yazi giriniz: \n");
		sgets(str);
		printf("[%s]\n", str);
		
		int word_flag = OUTWORD;
		int word_cnt = 0;

		for (int i = 0; str[i] != '\0'; ++i) {
			if (isspace(str[i]))
				word_flag = OUTWORD;
			else if (word_flag == OUTWORD) {
				word_flag = INWORD;
				++word_cnt;
			}
		}
		printf("%d kelime var.", word_cnt);	
}
``` 
  
# Ders 28   09.04.2021
  
  
 - İki yazının eşitliğini sınamak.
 
  
  ```
#define _CRT_SECURE_NO_WARNINGS

#include <stdio.h>
#include <stdlib.h>

#define SIZE	100



int main()
{
	char s1[SIZE];
	char s2[SIZE];

	printf("Iki adet yazi giriniz:\n");
	scanf("%s%s", s1, s2);

	int flag = 0;
	int i = 0;

	while (s1[i] == s2[i]) {
		if (s1[i] == '\n') {
			flag = 1;
			break;
		}
		++i;
	}

	if (flag)
		printf("İki yazi birbirine esit degildir.\n");
	else
		printf("iki yazi birbirine esittir.\n");
}
  ```
  
  
  - Bir mülakat sorusu:
 	- İki değişkeni ara bir değişken tanımlamadan yer değiştiriniz.
 	
		int x, y;
		printf("Iki tam sayi giriniz: \n");
		scanf("%d%d", &x, &y);
		x ^= y; y ^= x, x ^= y;
		
		printf("x = %d , y = %d \n", x, y);


- Unique rand 
 	- #define URAND_MAX   10   , makrosu tanımlıyken fonksiyonun işlevi 0 dahil 9 dahil rastgele bir tamsayı üretmeli.
 	- Her üretilen sayı unique olmalıdır. 
 	- İşlev tüm rastgele sayıları ürettikten sonra geri dönüş değeri olarak -1 değeri döndürmelidir.

```
#define _CRT_SECURE_NO_WARNINGS

#include <stdio.h>
#include "nutility.h"
#include <time.h>

#define URAND_MAX	10

int urand(void)
{
	static int flags[URAND_MAX];
	static int cnt = 0;

	if (cnt == URAND_MAX)
		return -1;
	
	int num = 0;

	while (flags[num = rand() % URAND_MAX])
		;
	cnt++;
	flags[num] = 1;

	return num;
}

int main()
{
	randomize();
	for (int i = 0; i < URAND_MAX; ++i)
		printf("%d ",urand());

	printf("\n");
	printf("hata degeri %d", urand());

}

``` 

- Reverse Copy Algorithm
	- Ekrana girilen sayıyı tersden ekrana yazdıran program:

```
#define _CRT_SECURE_NO_WARNINGS

#include <stdio.h>
#include "nutility.h"
#include <time.h>

#define SIZE	100



int main()
{
	
	char source[SIZE];
	char dest[SIZE];

	printf("Bir yazi giriniz:\n");
	sgets(source);

	printf("[%s] \n", source);

	int len = 0;
	for (int i = 0; source[i] != '\0'; ++i)
		++len;

	printf("%d\n", len);

	int x = 0;

	while (len != 0)
		dest[x++] = source[--len];

	dest[x] = '\0';

	printf("[%s]", dest);

}
```

- Yazıdan sayıya dönüşüm yapmak:


```
#define _CRT_SECURE_NO_WARNINGS

#include <stdio.h>
#include "nutility.h"
#include <time.h>
#include <ctype.h>
#define SIZE	100



int main()
{
	
	char str[SIZE];

	printf("Bir yazi giriniz: \n");
	scanf("%s", str);
	printf("[%s]\n", str);

	int num = 0;

	for (int i = 0; str[i] != '\0'; ++i) 
		num = 10 * num + str[i] - '0';
		
	
	/***8lik sayi sisteminde***
	for (int i = 0; str[i] != '\0'; ++i)
		num = 8 * num + str[i] - '0';*/

	/***2lik sayi sisteminde***
	for (int i = 0; str[i] != '\0'; ++i)
		num = 2 * num + str[i] - '0';*/
   


	/***16lik sayi sisteminde***
	for (int i = 0; str[i] != '\0'; ++i) {
		if (isdigit(str[i]))
			num = 16 * num + str[i] - '0';
		else if (isxdigit(str[i]))
			num = num * 16 + 10 + toupper(str[i]) - 'A';
			
	}*/

	printf("sayi = %d", num);


}
```

  
  
  
- İnline Expansion
	- Bir fonksiyon çağrısında, derleyici çağrılan fonksiyonun tanımını görüyor ise ve eğer uygun bulduğu taktirde 
	fonksiyona giriş çıkış kodunu üretip linker a referans ismi yazmak yerine doğrudan linker ı bypass ediyor.
	Ve bu fonksiyonun derlenmiş koduna yerleştiriyor.
		- Bu işlem fonksiyon makrolarındaki gibi gerçekleşmez.
	
		int square (int x, int y)
		{
			return x * x + y * y;
		}
  		int main()
		{
			int a = 10;
			int b = 20;
			int x = square(x, y);
		}
  
 - Yukarıdaki kodda derlenirken fonksiyon satırı az olduğundan optimize edilip fonksiyon kaldırılıp o kodu 
  fonksiyonsuz kullanılmasına denir. 
	  	- Fonksiyonel makrolardan çok dah güvenlidir.
	  		
- Derleyicinin inline expansion yapması için;
	- Dereyici fonksiyon tanımını mutlaka görmeli.
	- Derleyicinin yaptığı analizle bu açılımdan bir fayda sağlamayacağı sonucunu çıkarmış olmalı.
	- Optimizasyon switchleri
	- Fonksiyondaki kod çok komleks olmamalı.

- İnline anahtar sözcüğü ;
	
		inline int square(int x, int y)
		{
			return x * x + y * y;
		}
  - Bir fonksiyon yukarıdaki gibi tanımlandığında, derleyiciden eğer uygunsa bu fonkiyonu bulunduğu yerde açmasını istiyoruz.
  - İnline fonksiyon başlık dosyalarında tanımlanmalıdır.
  - Normal bir fonksiyon başlık dosyalarında tanımlanmamalı.(linker hatası).
  
  
  # Pointers (İşaretçiler, Göstericiler)
  
  - Pointer adres anlamında kullanılan bir sözcük.
  - Öyle ifadeler olacak ki bu ifadeler bir değişkenin adresi anlamına gelen ifadeler.
  	
		int x = 10;
		&x --> x'in adresi
		
		
 - T x;
 	- Eğer bir ifade T türünden bir nesnenin adresi anlamına geliyorsa o ifadenin türü T* olarak kabul ediliyor.
 	- İnt türden nesne adresi anlamına gelen ifadenin adres türü int* 'dir.
 		 - double*
 		 - char*
	- Farklı türden nesnelerin adresleri farklı türdendir.
	
	
	int x; ---> türü int olan bir değişken
	int* ptr ---> ptr, int türden bir nesnenin adresini (deger olarak) tutacak degisken.
		- ptr is a pointer to int
	
	
	
	
# Ders 29 12/04/2021

  
 #include <stdio.h>
 
 int *gp; --> int türden bir nesnenin adresine tanımlamak amaçlı kullanılmış global pointer değişken
 
 void func(int *ptr)
 {
 	char *p; --> Otomatik ömürlü yerel pointer değişken.
	static double *dp ---> double türken bir nesnenin adresini tutması için tanımlanmış static bir yerel değişken.
 }
  
  - Otomatik ömürlü pointer değişken ilk değer verilmezse çöp değerler hayata başlarlar.
  - Global ömürlü pointer değişkene ve static ömürlü yerel değişkene ilk değer verilmezse ilerde ayrıntılı 
  inceleyeceğimiz özel bir adres sabitiyle hayata başlatılıyor.
  	- Null pointer
  
  
  - Sistemde nesne adresleri hangi türden nesnenin adresi olursa olsun aynı miktarda yer kaplıyor.

	32 bitlik sistem ---> 4 byte
	64 bitlik sistem ---> 8 byte 
	bazı sistemler -----> 2 byte
	

	
  
  		printf("sizeof(char) = %zu \n", sizeof(char));//1
		printf("sizeof(char) = %zu \n", sizeof(char));//4

		printf("sizeof(short) = %zu \n", sizeof(short));//2
		printf("sizeof(short) = %zu \n", sizeof(short));//4

		printf("sizeof(int) = %zu \n", sizeof(int));//4
		printf("sizeof(int) = %zu \n", sizeof(int));//4

		printf("sizeof(double) = %zu \n", sizeof(double));//8
		printf("sizeof(double) = %zu \n", sizeof(double));//4
  
  
  
  
 - int *p1, p2;---> burada iki değişkende pointer değişken değildir.
   p1 --> int* türden
   p2 --> int türden
   
  
 - Her iki değişkenin de pointer olması için

		int *p1, *p2; //olmalı.
		
	

- Bir pointer değişkene adres olmayan ifade atanmaz.

		int x = 10;
		int* p;
		p = x;
		
		
- int a[10]; // buradaki köşeli parantez declaratördür.
  a[5];// Buradaki köşeli parantez operatördür.
  
  
  Pointer Operators:
  
  öncelik seviye tablosu
  
  1-->   []    ->
  2-->   &      *
  
  + [] --> subscript/index operator
  + -> --> member selection op./arrow op
  + &  --> address of op. /adres of
  + *  --> dereferencing / indirection (içerik op)


**Adress of Operator (&)

- 2. öncelik seviyesinde ve sağdan sola öncelik seviyesine sahip.
- Unary prefix

- Adres operatörünün operantının L value expression olması gerekiyor.
- Adres operatörü ile oluşturulan ifadeler R value olmak zorunda.

		int x = 10;
		&x = 15; ---> yanlış kullanımdır. (sentaks hatası) &x R value olduğu için değer ataması yapamayız.
	

  
  
 - int * ptr = &x; ---> Bir pointera ilk değer verilmesi.
  	- Ptr'nin değeri x'in adresi.


- int x = 10;
  int y = 20;
  int * ptr = &x; ---> initialize edildi.
  ptr = &y; ----> ptr'ye y'nin adresi atandı.
  
  - Eğer ptr, bir pointer değişken ise ve ptr'nin değeri x isimli değişkenin adresi ise 
  	- ptr'nin değeri x'in adresi
  	  ptr, x'i gösteriyor demek aynı anlamda.
	  ptr, x'e işaret ediyor.
	  ptr points to x
	  
	  

- int x = 10;
  int y = 20;
  
  int* p1 = &x;
  int* p2 = &y;
  
  p1 = p2; // Bu kod sonrasında p1 y'yi gösteriyorken p2 de y'yi gösteriyordur.
  
 
 
 
 - Pointer değişken söz konusu olduğunda iki ayrı adresten bahsedilebilir.

		int x = 10;
		int* ptr = &x;
		
		//ptr x'in adresini gösterir.
		//&ptr ise ptr'nin adresini gösterir.
		
- int x = 10;
  int *ptr = &x; --> ptr, x'in adresini tutuyor.
  int * p = ptr; --> p, ptr de tutulan  x'in adresini tutuyor.
  

- double x;
  int* p = &x;// Yanlış kullanımdır.(sentaks hatası değildir)
  
  
  - C'de yanlış olmakla beraber farklı adres türleri arasında tür dönüşümü vardır.

 
  - int a[10] = { 0 };
    a ---> &a[0] array decay
    
    int *p = a; // Burada a dizisini p pointer değişkenine atamıyoruz. a dizisinin ilk değerinin adresini atıyoruz.
    
    
  - array decay'in iki istisnası vardı. Pointerlarla ilgili olanu hatırlayalım.
  sizeof operatöründe array decay uygulanmaz.
  	
		int a[5] = { 0 };
		printf("%zu\n", sizeof(a));---> dizinin boyutunu gösterir: 5x4 byte = 20
  		printf("%zu\n", sizeof(&a[0]));----> pointer türü boyutu: 4 byte
		

   - printf işlevi ile bir adresi formatlı olarak std. çıkış akımına yazdırabilirsiniz.
		- Kullanılan format: conversion specifier %p
		
			int x = 10;
			int* ptr = &x;
			printf("&x = %p\n " , &x); --> x'in adresi
			printf("ptr = %p\n" , ptr); --> x'in adresi
			printf("&ptr = %p\n", &ptr); --> ptr'nin adresi
			


 - &x = ptr ; --> Burada x'in adresi değiştirilmeye çalışılmış ancak C'de böyle birşey pek söz konusu değil.

- int a[5] = { 0 };
  int b[5] = { 0 };
  a = b; --> derleyici bunu şu şekilde algılar : &a[0] = &b[0]
   	Ve hata verir. &a[0] L value değildir.
	
**Deferencing / indirection Operatörü ( İçerik Operatörü)

- 2. Öncelik seviyesine sahip
- unary prefiks op.

- İçerik operatörünün operantı adres olmak zorundadır.


- int x = 10;
  int* ptr = &x;
  int a[10] = { 0 };
  *x --> hata verir. x adres değil.
  *&x --> sağdan sola öncelik yönü olduğu için (&x) adres olduğu için hata vermez.
  *a  --> &a[0] array decayden dolayı hata vermez.
  		- Yani sonuç olarak;
  		  *(op) --> burada op adres olmak zorunda.
		  

- İçerik operatörü, operantı olan nesneye erişimi sağlıyor.

- int x = 10;
  *&x = 45; // buradaki kod ile x = 45 yazılması aynı anlama gelir ikiside x'e 45 atamasını yapar.
  	- Ancak tabiki piyasada böyle bir kullanım söz konusu değildir. 
  		- Sadece obfuscation (kodun okunmasını zorlaştırmak amaçlı) kullanılabilir.


- int [] = { 10, 20, 30 };
   *a =22; --> a[0] = 20 oldu.
   
   
- int x = 33;
  int *p = &x;
  *p =77; // x, 77 yapıldı.
   
  
  - İçerik operatörüyle oluşturulan ifade her zaman L value expressiondur.
  
  
  - a[++x] --> x + 1 inci eleman
    ++*a --> ++a[0] 
    
  
  - Pointer (gösteren)
    Pointee (gösterilen)
    
    
    
- int a = 5;
  int b = 8;
  int c = 11;
  
  int *ptr;
  ptr = &y;
  *ptr *= 2;
  ptr = &b;
  *ptr *= 2;
  ptr = &c;
  *ptr *= 2;
   	- Yukarıdaki kod parçacığında a, b, c değerleri iki katına çıkartılmış.
  
  
  - Call by reference

		void func(int* ptr)
		{
			*ptr = 677;
		}
  		int main()
		{
			int x = 10;
			func(&x); --> x değeri 677 olur.
		}
		

- scanf("%d", &x);
  	- scanf'e x'in adresini gönderecek olmamızın sebebi, x'i değiştirecek olması. İşte bu sebeple bu çağrı call by reference olmak zorunda.


- swap fonksiyonu (call by reference)

		void swap(int* a, int* b)
		{
			int temp = *a;
			*a = *b;
			*b = temp;
		}
		int main()
		{
			int x,y;
			printf("iki tamsayi giriniz: ");
			scanf("%d%d ", &x, &y);
			swap(&x, &y);
			
		}--> swap fonksiyonuna x ve y'nin adresleri gönderildi çünkü x ve y'nin değeri fonksiyonun içerisinde değiştirilmek isteniyor.
		Bu yüzden call by reference olmalı.
		

- swap fonksiyonuna farklı bir argüman gönderim şekli örneği:
	
		void swap(int* a, int* b)
		{
			int temp = *a;
			*a = *b;
			*b = temp;
		}
		int main()
		{
			int x = 35, *p1 = &x;
			int y = 45, *p2 = &y;
			
			swap(p1, p2);
			
		}
  
  - Bir örnek:
  
  		void foo(int* a, int*b)
		{
			*a *= *b;
		}
		void func(int* p, int*q)
		{
			*p += *q;
			foo(p, q);
		}
		int main()
		{
			int x = 5, y = 9;
			func(&x, &y);
			printf("x = %d\n, x);
			printf("y = %d\n, y);
			
		}
	
- Eğer bir fonksiyonun sahip olduğu değişkenin çağrılan bir fonksiyon tarafından değiştirilmesi söz konusu ise "call by reference" şarttır.


  		void iscan(int* ptr)
		{
			int c;
			*ptr = 0;
			while ((c = getchar()) != '\n') {
				*ptr = *ptr * 10 + c - '0';
			}
		}

		int main()
		{
			int x;
			printf("bir sayi giriniz:");
			iscan(&x);
			printf("x = %d", x);
		}
  
  
  # Ders 30 - 14.04.2021
  
  - call by reference 
    pass by reference --- same meaning
    
   

- Neden bir fonksiyonun parametre değişkeni pointer olabilir?
	- Bazı fonksiyonlar kendilerini çağıran koda bir değer iletmek istiyorlar.
	  Şimdiye kadar değer iletmenin tek bir yolunu gördük. Geri dönüş değeri.
	  Oysa şimdi bir fonksiyonun başka bir fonksiyona değer iletmesi için ikinci bir mekanizma daha var.
	  Fonksiyona adres gönderilir ve fonksiyonda gönderilen adresten nesneye ulaşılarak nesneye veriler yazılır.
	  
	 
- Örnek olarak iki farklı fonksiyonda dairenin alanı:

1. alternatif:
```
#define _CRT_SECURE_NO_WARNINGS

#include <stdio.h>
#include <time.h>
#include <stdlib.h>
#include <ctype.h>
#include "nutility.h"

#define SIZE	10

double get_circle_area(double radius)
{
	return 3.1415926 * radius * radius;
}

  
int main()
{
	double r, area;
	printf("Yaricap giriniz: ");
	scanf("%lf", &r);
	area = get_circle_area(r);
	printf("dairenin alani = %lf ", area);

}
```
2. alternatif  (pointer ile oluşturma)
```

#define _CRT_SECURE_NO_WARNINGS

#include <stdio.h>
#include <time.h>
#include <stdlib.h>
#include <ctype.h>
#include "nutility.h"

#define SIZE	10

void get_circle_area(double radius, double* parea)
{
	*parea = 3.1415926 * (radius) * (radius);
}

  
int main()
{
	double r, area;
	printf("Yaricap giriniz: ");
	scanf("%lf", &r);
	get_circle_area(r, &area);
	printf("dairenin alani = %lf ", area);

}
```
  
- Bir fonksiyonun varlık nedeni bir değer hesaplaması ise;
   iki ayrı yapı söz konusu olabilir.
  		- Alt fonksiyonda hesaplanan değeri geri dönüş değeri mekanizması yazılan ana fonksiyona iletmesi.
  		- Alt fonksiyonun hesapladığı değeri ana fonksiyondan gönderilen adresteki nesneye yazması. (Pointer kullanarak)


- Hem okunurluk açısından hem de ekstra bir değişken kullanılmamak isteniyorsa geri dönüş mekanizması ile fonksiyon oluşturmak seçilebilir.

- Peki hangi durumlarda pointer kullanarak fonksiyon oluşturuyoruz ?
  
- Return statement ile bir geri dönüş değeri gönderdiğimizde aslında derleyici şöyle bir kod üretiyor. Derleyici fonksiyonun geri dönüş değerinin 
yazılacağı bir bellek alanı ayırıyor. Yani bir geçici nesne oluşturuyor.
	
		geçici_nesne = return statement;
		double area = geçici_nesne;
		
Derleyici özel bir optimizasyon yapmaz ise iki kez blok kopyalaması söz konudur.

- Şimdi eğer iletilecek değer 4 byte , 8 byte gibi büyük olmayan değer ise fonksiyonun geri dönüş değeri mekanizması oluşturmak herhangi bir dezavantaj 
oluşturmuyor. Ancak ilerleyen süreçte karşımıza öyle değerler çıkacak ki bunlar 4 byte , 8 byte gibi değil de 50, 100, 500 byte gibi değerler olacak.
Bu tür değerleri geri dönüş mekanizması ile iletirsek tipik bir fonksiyon çağrısı ve geri dönüş değerini bir değişkende saklama kodunda sizin programın çalışma
zamanında maliyetiniz 2 kat artacak.

- Peki pointerlarla nasıl yapıldığını incelersek;  biz fonksiyona sadece adres gönderdiğimiz için adresde derleyiciye göre değişmekle birlikte 
4 byte yani nesne bellekte ne kadar büyük yer kaplasa da siz adresi gönderdiğiniz için ara kopyalama işlemi yapılmıyor.

- Bu yüzden C'de tipik olarak hesaplanan değer tekse ve bu değer int, double gibi türlerse her zaman tercihimiz return statement olur. Fakat
ne zaman ki hesaplanacak değerin bellekte kapladığı yer çok büyük oluyor.  
işte o zaman gereksiz maliyetten kaçınmak için fonksiyonun parametre değişkeni pointer yapılıyor.

- Özetlersek; Neden fonksiyonun parametresi pointer olur?
	- Geri dönüş mekanizmasını kullanmayıp gönderilen adresteki nesneye yazmak.
	- Kullanılacak nesnenin storage ihtiyacı fazla ise
	- Bir fonksiyon çağırılan koda birden fazla değer iletecekse. Call by value ile return statement
	  sadece bir değer döndürebiliyorken call by reference ile istenilen kadar geri dönüş değeri üretilebilir.
	  
	  
- C dilinde bir fonksiyon başka bir fonksiyona bir dizi gönderecek ise call by reference zorunludur.
- Diziler farklı fonksiyonlarda sadece adres aktarımı ile kullanılabilir.


**Const anahtar sözcüğü ve Const semantiği:

- const int x = 45; --> yazıldığında derleyiciye x'in 45 değeri ile hayata başladığını ve bu değerin x'in ömrünün sonuna kadar değişmeyeceği bilgisi 
veriliyor.

- Neden const değişkenler kullanırız?
	- Yazan programcının kendisine yardımcı olabilmesi için. Mesela ilk yüz asal sayıyı tutan bir sabit dizi düşünelim.
	progra akışında bu diziden kaçıncı asal sayı istenirse olde edilmek amacıyla tanımlanmış olsun. Program akışında herhangi bir sebeple dizinin herhangi
	bir elemanı değiştirilmeye çalışılırsa bu dizinin kullanım amacı bozulacaktır.
	- Okuyana yardımcı olmak.
	- Derleyiciye yardımcı olmak. Derleyiciler bir değişkenin veya bir dizinin hayatı boyunca değişmeyeceğini bilirlerse eğer 
	daha iyi bir kod optimizasyonu yapacaktır.

- const anahtar sözcüğü ile bir değişkene ilk değer verilmeden tanımlanırsa bu yanlıştır. Yani siz x'in çöp değerinin 
ömrü boyunca değişmeyeceği bilgisini veriyorsunuz.

- C dilinde const anahtar sözcüğü ile tanımlanan değişkenler, sabit ifadesi gereken yerlerde kullanılamazlar.

		const int size = 299;
		int a[size] = { 0 };//Geçerli değil.
		
- const x = 10;
  int*P = *&x;
  *p = 35; -- Bu UB dir. Sentaks hatası aşılmış ancak sonucun nasıl olacağı belirsizdir.
  
  
  **Pointer Değişkenler ve Const
  
  - İki kullanım mevcuttur.
  	- int *const ptr = &x;
  	- int const *ptr = &x;
  	
1- int *const ptr = &x; şeklinde kullanım:
	- const pointer
	
		int x = 10;
		int* cont ptr = &x;
 - Yukarıda ptr hayata x'in adresiyle gelecek ve hep x'in adresini tutacak.
	- Ptr hayatu boyunca x'i gösterecek.

- Eğer pointera başka bir adres atamayı denerseniz sentaks hatası.

		ptr = &y;// hata
		*ptr = 98;// x'e 98 atanmış ptr de herhangi bir değişiklik yapılmadığı için kesinlikle karıştırılmamalı.
		
2- int const *ptr = &x; veya const int *ptr = &x;
	- pointer to const int

Bu pointerın gösterdiği nesneye bu pointer yoluyla eriştiğinizde (*ptr), bu nesneye karşılık gelen nesneye bir atama yapamazsınız.
Yani ptr adeta diyor ki benim vasıtamla benim gösterdiğim nesneye salt okuma(access) amaçlı erişebilirsiniz.

		*ptr =  45; --> hata
		int b = *ptr; --> geçerli
		ptr = &y; --> geçerli
		
		
- Yani const ne'den önce gelirse const olan o dur.
	
		int *const p = &x; // p'ye atama yapamazsın.
		const int *p = &x; // *p'ye atama yapamazsın.
		

- const int * const ptr = &x; // Bu durumda iki anlamda birleşiyor.
	- const pointer to const int

		ptr = &x; // hata
		*ptr = &x; // hata
		

- T bir tür olmak üzere
	- void func(T *p)
		- mutator
		- setter
		- set function
		- Yukarıdaki fonksiyon sizden adresinin aldığı değişkeni değiştireceğini anlatıyor.

	- void func(const T* p)
		- getter
		- accessor
		- Bu fonksiyon sizden aldığı adresteki nesnede herhangi bir değişiklik yapılmayacağını sadece okuma amaçlı alındığını anlatıyor.


**Pointer Aritmetiği:

- C dilinde;
	-  bir adresle bir tamsayı toplanabilir.
	-  bir adresle bir tamsayı çıkartılabilir.
- Tüm bu işlemler geçerlidir.

		ptr + i;//legal
		ptr - i;//legal
		i - ptr;//illegal-geçersiz
		Bu ifadelerin sonucu da adrestir.
		
- C dilinde bir adresle 1 toplandığında bir sonraki (aynı türden) nesnenin adresini elde ederiz.

		int a[0] = { 0 };
		printf("&a[0]  = %p\n", &a[0]); // a[0] 'ın adresi
		printf("&a[0] + 1  = %p\n", &a[0] + 1);// a[1]'in adresi


- a + 5 ile &a[5] aynıdır. a + 5 ile kasıt &a[0] adresindeki nesneden 5 nesne sonrasındaki nesne kastedilmiştir.
- &a[5] ise 5. indisteki elemanın adresi kastedilmiştir.

- a[5] ile *(a + 5) aynıdır.


		int a[10] = { 0, 1, 2, 3, 4, 5, 6, 7, 8, 9 };
		int *ptr = a;
		
		for (int i = 0; i < 10; ++i) {
			printf("%d %d %d %d \n", a[i], *(a + i), *(i + a), *ptr);
			++ptr;
		}--> yukarıdaki printf'in içerisindeki tüm formatlar aynı nesneyi gösterir.
		
  
  # Ders 31 - 16.04.2021 
  
  **İndex/subscript Operatörü ( [ ] )
  
  - 1. öncelik seviyesine sahip ve soldan sağa öncelikli (left associative)
  
  		a[b] ----> *(a + b) //derleyici bu halde algılar.
		
- Aşağıdaki kod sadece operatör özelliğini anlamak için yazılyor üretimde böyle bir kullanım söz konusu değildir.

		int x = 10;
		(&x)[0] = 23; // *(&x +0) = 23 olarak algılandı ve x'e 23 ataması yapılmış oldu.
		
- Bir dizi tanımlansın.

		int a[10] = { 0, 1, 2, 3, 4, 5, 6, 7, 8, 9 };
		int *ptr = a + 5;
		
		printf("%d\n", *ptr); // ekrana 5 yazdırılır.
		printf("%d\n", ptr[0]);//ekrana 5 yazdırılır.
		printf("%d\n", ptr[3]);//ekrana 8 yazdırılır.
		printf("%d\n", *(ptr - 3)); //ekrana 2 yazdırılır.
  
  - Yani; 

		ptr[n]   --------   *(ptr + n) //aynı
		&ptr[n]  --------   ptr + n //aynı
		ptr[0]   --------   *ptr //aynı
		
- C dilinde iki adresin toplanması sentaks hatasıdır.

- Adreslerin birbirinden çıkartılması:
  	
		&a[5] - &a[2] // a[3] olur
		(a + 5) - (a + 2) // a[3] yani (a + 3)
		
- C dilinde 2 adresin farkı işaretli türden tam sayıdır.

- Bir dizinin daha büyük indeksli bir elemanını adresinden daha küçük indeksli bir elemanının adresini çıkartırsak
  pozitif bir tam sayı elde ederiz.
- Küçük indeksten büyük indeks çıkarılırsa negatif tam sayı elde ederiz.

		int [10] = { 0, 1, 2, 3, 4, 5, 6, 7, 8, 9 };
		
		int *p1 = a + 5;
		int *p2 = a + 3;
		
		printf("%d\n", p1 - p2); // 2 olur
		printf("%d\n", p2 - p1); // -2 olur
		
- ptr, a isimli bir dizinin bir elemanını göstermektedir. ptr'nin gösterdiği dizi elemanı indisi nedir? 

		ptr - a
		
- ptr, a dizisinin n indisli elemanını göstermektedir. Ptr'nin gösterdiği nesnenin adresi nedir?

		a + n
	
- Yani  C'de bir dizinin indeksini bilmek ile adresini bilmek arasında hiçbir fark yoktur.

- Yani a dizisinin;

		n indeksli elemaının adresi ---> a + n
		ptr de dizi elemanının adresi varsa index öğrenilmek isteniyorsa ----> ptr - a
  
  
- iki adres farkının kullanılabilir olması için bir dizinin içerisindeki adresler olması gerekir.
  Aynı dizi içerisinde olmayan adresler kullanılması sentaks hatası değildir fakat hiçbir anlamı yoktur.
  
		int x = 10, y = 5;
		&y - &x --> anlamsızdır.
		
**Dizilerin Fonksiyonlara Gönderilmesi
		
		void afunc(int* ptr, int size)

- Eğer fonksiyona salt okuma amaçlı gönderilmişse ;

		void afunc(const int* ptr, int size)
  
  
  
- Bir diziyi ekrana yazdıran fonksiyon:

		void printArray(const int *ptr, int size)
		{
			for (int i = 0; i < size; ++i) {
				printf("%d", p[i]);
			}
		}
		int main()
		{
			int a[10] = { 0, 1, 2, 3, 4, 5, 6, 7, 8, 9 };
			printArray(a, 10);
		}
		
  
- Yukarıdaki fonksiyonun sık C'de sık kullanılan bir idiyomatik biçimi

		void printArray(const int *ptr, int size)
		{
		
			while(size--) {
				printf("%d ", *ptr);
				++ptr;
			}
		}
  
  
  - Yukarıdaki fonksiyona çağrı yapılırken istenilen aralığı nasıl yazdırabiliriz ona bakalım:

		printArray(a , SIZE); // SIZE bir makro, a dizisinin tamamı yazdırılır.
		printArray(a, 5); // a dizisinin ilk 5 elemanı yazdırılır.
		printArray(a + 5, 4); // a dizisinin 6. elemanından başlayıp 4 elemanı yazdırılır.
		printArray(a + SIZE - 5, 5);// a dizisinin son beş elemanı yazdırılır.
  
  
  
  - Bir dizinin elemanlarını toplayan fonksiyon:

		int sumArray(const int *ptr, int size)
		{
			int sum = 0;
			
			while (size--) 
				sum += *ptr++;
			
			return sum;
		}
		int main()
		{
			int a[10] = { 0, 1, 2, 3, 4, 5, 6, 7, 8, 9 };
			printf("Toplam = %d", sumArray(a, 10));
		}
  
  - Bir dizide max sayıyı bulan fonksiyon:

		int get_max_val(const int* arr, int size)
		{
			int max = *arr;
	
			while (size--) {
				if (max < *arr)
					max = *arr;
				++arr;
			}
			return max;
		}

  
		int main()
		{
			int a[5] = { 0, 1, 2, 3, 4 };
			printf("%d",get_max_val(a, 5));

		}
  
  
  
 - Bir dizinin fonksiyon içerisinde hem max hem min elemanını bulan fonksiyon:


```
void get_min_max_val(const int* arr, int size, int* max, int* min)
{
	*max = *min = *arr;
	for (int i = 0; i < size; ++i) {
		if (*max < arr[i])
			*max = arr[i];
		if (*min > arr[i])
			*min = arr[i];
	}
}

  
int main()
{
	int a[SIZE];
	randomize();
	set_array_random(a, SIZE);
	print_array(a, SIZE);

	int max, min;
	get_min_max_val(a, SIZE, &max, &min);

	printf("max = %d , min = %d ", max, min);


}  
```

- Bir diziyi bir diziye kopyalayan fonksiyon:

```
void copy_arr(int * pdest, const int* psource, int n)
{
	
	while (n--)
		*pdest++ = *psource++;

}


  
int main()
{
	int a[SIZE];
	int b[SIZE];
	randomize();
	set_array_random(a, SIZE);
	print_array(a, SIZE);

	copy_arr(b, a, SIZE);

	print_array(b, SIZE);

}

```
 
 - Bir tamsayı dizisini ters çevirecek (reverse array) fonksiyonu yazalım:

```
void reverse_arr(int* arr, int size)
{
	for (int i = 0; i < size / 2; ++i) {
		int t = arr[i];
		arr[i] = arr[size - 1 - i];
		arr[size - 1 - i] = t;
	}
}


int main()
{
	int a[SIZE];
	
	randomize();
	set_array_random(a, SIZE);
	print_array(a, SIZE);

	reverse_arr(a, SIZE);

	print_array(a, SIZE);
}
```

  
- Bubble sort algoritmasını bir fonksiyon içerisinde yazarsak:

```
void bsort(int* arr, int size)
{
	for (int i = 0; i < size - 1; ++i) {
		for (int j = 0; j < size - 1 - i; ++j) {
			if (arr[j] > arr[j + 1]) {
				int t = arr[j];
				arr[j] = arr[j + 1];
				arr[j + 1] = t;
			}
		}
	}
}


int main()
{
	int a[SIZE];
	
	randomize();
	set_array_random(a, SIZE);
	print_array(a, SIZE);

	bsort(a, SIZE);

	print_array(a, SIZE);
}
``` 



- Bir fonksiyonun parametresini pointer yapmak iki yolla mümkün:
	- void func(int *p, int size);
	- void func(int p[], int size);
		- [] ifadesinin kullanılmış olması kesinlikle fonksiyon parametresine bir dizinin yazıldığı anlamına gelmiiyor.
		  zaten C'de bir fonksiyon parametresi bir dizi olamaz.
		  
		  
**Geçerli ve Geçersiz Pointerlar (valid&invalid pointers, kullanılabilir & kullanılamaz pointerlar)

- Çöp değer pointer geçersizdir. (indetermined value)


- Bir pointer 3 durumda geçerlidir.
	- pointer değişken hayattaki bir nesnenin adresini tutuyorsa.
	- pointer değişkenin bir dizinin bittiği yerin adresini tutması
			
			int a[5] = {0, 1, 2, 3, 4 };
			int *p = a + 5;
		
	- Yukarıdaki kod satırında dizinin bittiği adres ile pointer ilk değerini almıştır.
	Ancak bu pointer dereferencable'dır. Yani siz bu pointer'ı içerik operatörünün operantı olarak
	kullanırsanız UB olur. Çünkü a[5] 'de herhangi bir dizi elemanı yoktur. 
	
		*p // tanımsız davranış
		
**Pointerlar (adresler) ve Karşılaştırma Operatörleri

< <=  >  >= == !=

- Pointerlar karşılaştırma operatörlerinin operantları olabiliyorlar.

- İki pointerın eşitliğinin doğru sonuçlanması için ;
	+ her iki pointerın da aynı nesnenin adresi olması gerekmektedir.
	+ her iki pointer da aynı dizinin bittiği yerin adresi olmalı.

		int a[5] = { 0, 1, 2, 3, 4 };
		int* pend = a + 5;
		int* p = a;
		
		while (p != pend) {
			printf("%d ", *p);
			++p;
		} ---> dizideki tüm elemanları yazar.
  
  
  - Bir fonksiyonun parametreleriyle dizinin ekrana yazdırılacak olan değerlerini pointer yoluyla fonksiyona bildiren program:
  	- range parameter


```
void printArray(const int* p, const int* pend)
{
	while (p != pend) {
		printf("%3d ", *p);
		++p;
	}
	printf("\n");
}


int main()
{
	int a[SIZE];
	
	randomize();
	set_array_random(a, SIZE);
	print_array(a, SIZE);

	printArray(a, a + SIZE); // tüm diziyi yazdırır
	printArray(a + 2, a + 5);// 2. indis ile 5. indis dahil arasındaki sayıları yazdırır.
}

```


- < <= > >= operatörlerinin doğru ve anlamlı bir şekilde kullanılabilmesi için iki pointerın da aynı dizinin elemanlarını göstermesi gerekiyor.

		a + 2 ile a + 5 'in kıyaslanması gibi
		&a[5] > &a[2]

  	
  
  - reverse algoritmasını adres karşılaştırarak yapalım:
  - 
```
  void reverse_arr(int *p , int size)
{
	int* pe = p + SIZE;

	while (p < pe) {
		swap(p++, --pe);
	}
}


int main()
{
	int a[SIZE];
	
	randomize();
	set_array_random(a, SIZE);
	print_array(a, SIZE);

	reverse_arr(a, SIZE);

	print_array(a, SIZE);
}
```

# Ders 32 - 19.04.2021
  
  
  
  
  **Pointer İdiyomları
  
Hatırlatma : 
- &(op) --> Adres operatörünün operantı L value olmalıdır. Oluşturduğu değer R value'dur.
- *(op) --> Operantı adres olmalıdır.
- ++(op) , (op)++ --> operantları L value olmalıdır. R value oluştururlar.

		&x++ --> Bu bir sentaks hatasıdır. Derleyici bu kodu &(x++) olarak algılar ve  & operatörünün operantı L value olmalıdır. Ancak 
		x++ ifadesinin ürettiği değer R value'dur. 
		
		
  		++&x; --> Sentaks hatasıdır. Bu operatörlerin öncelik sırası sağdan sola olduğu için ilk olarak &x işlemi yapılır ve ürettiği 
		değer R value olur. Ancak ++ operatörünün operantı L value olmalıdır.
 
 
#

		int a[5] = { 0, 1, 2, 3, 4 };
		int* ptr = a;
		*ptr++ = 99; // Derleyici bunu *(ptr++) olarak algılar. Ve böyle bir kullanım
		senktaks hatası olmamakla birlikte sık sık kullanılır.
		*++ptr; Aynı şekilde geçerlidir.
		
#

		a  bir dizi olmak üzere;
		*a++ --> sentaks hatasıdır. Sebebi ise bir dizi ismi ++ operatörünün operantı olamaz. Çünkü
		dizi ismi L value değildir. ++ operatörünün operantı L value olmalıdır.
		
# 
	
- reverse array fonksiyonun daha idiyomatik bir şekli:

		void reverse_array( int *pdest, const int* psource , int n)
		{
			psource += n;
			while (n--)
				*pdest++ = *--psource;
		}
	


- *a++; --> ifadesinin geçersiz olmasına dair;
	- &x ifadesi bir adrestir. R value üretir.
	- ptr ifadesi bir adres ifadesidir ve L value'dır.
	- a ifadesi (array decay) bir adrestir. a = &a[0] olduğundan a ifadesi R value expression olur.
	 Yani ++ operatörünün operantı L value olmalıdır. 
	 - ++a ---> a bir dizi ismi ise sentaks hatasıdır.

- Eğer bir fonksiyon 2 adres alıyor ise ve bir adresten okuma yapacak, diğer adrese değer yazacak ise 
C standart kütüphanede böyle fonksiyonlar yazılacak olan parametreyi birinci parametre olarak tanımlamıştır. 
Biz de fonksiyon oluştururken C standart kütüphanesini taklit etmemizde fayda vardır.
  
 - Bir örnek:

		int a[5] = { 0, 1, 2, 3, 4 };
		int *ptr = a;
		print_array(a, 5);
		++*ptr; ---> dizinin ilk elemanı olan 0 değeri 1 artırılmış oldu. Ancak ptrde herhangi bir değişiklik olmadı.
		print_array(a, 5);
		
		
- Bir mülakat sorusu:
```

void foo(int* ptr, int n)
{
	while (n--)
		++* ptr++;
}

int main()
{
	int a[5] = { 0, 1, 2, 3, 4 }; 
	print_array(a, 5);
	foo(a, 5);---> dizinin birinci indisinde olan 1 değerini 1 artırdı.
	print_array(a, 5);

}
```

# Tür (Eş) İsim Bildirimleri -1-

typedef int word;
- Derleyicinin artık word ismini gördüğünde int ismini algılamasını istiyoruz.

		typedef int* IPTR;
		IPTR p1, p2;
		//açılımı: 
		int* p1, int* p2; olur.
		int* p1, p2; gibi olmaz. Dikkat etmek lazım.
		

1- Hangi türe eş isim verilecekse o türden bir değişken tanımlayın.
2- Tanımlamanın başına typedef yazın.
3- Değişkenin yerine tür eş ismini koyun.

		typedef int INTA10[10]; int[10]  türünün eş ismi.
		INTA10 a, b, c; 
		//açılımı:
		int a[10], b[10], c[10]; olur.
		
- Amaç: int, double, char gibi türlerin daha dar, özelleştirilmiş bir konteks kullanılması ve bu kontekse ilişkin 
bu türlere bir eş isim verilmesi. Okunabilirliği artırmak.

- Örnek olarak biz bir programda int olarak birçok int türden counter tanımlayalım. Sonrasında biz bu programı yazarken int tür 
sınırlarının yetmediğini fark edip counter değişkenilerinin türünü long long int yapmak istersek hepsini tek tek bulup değiştirmemiz
gerekir. Ancak biz ilk başta typedef olarak counter değişkenleri için eş isim kullanırsak işimiz çok daha kolaylaşmış olacaktır.


**Standart Kütüphane ve typedef bildirimleri

size_t standart typedef ismi:
- size_t'nin türü sizeof operatörünün ürettiği değerin türüdür.
- size(x) ---> Bu ifadenin türü size_t ancak size_t derleyiciye göre değişken olduğu için unsigned int,
 unsigned long belki unsigned long long türlerinden birinin eş ismi olabilir. 
  
- Standart kütüphane size_t türünü nerelerde kullanıyor.
	- Fonksiyonların sizeof değeri isteyen parametre türü olarak
	- Eğer bir fonksiyon dizi boyutu türü istiyorsa
	- Yazı uzunluğu türü istenen fonksiyonda
	- Tane-adet türü istenen fonksiyonlarda

		size_t  x = 10;
		printf("%zu", x); --> %zu size_t için format.
		

- #include <stdint.h>
  int x = 0;--> Burada int türü derleyiciden derleyiciye değiştiği için taşınılabilirliği netleştirmek için;
  int32_t x = 0; --> Bu şekilde kullanılırsa bu kullanım standart bir typedef ismidir. Derleyici stdint başlık 
  dosyasında int32_t'yi 4 byte'lık işaretli bir tamsayı türünün eş ismi olarak tanımlamak zorundadır. 
  Yani siz bu kodu hangi derleyicide derlerseniz derleyin artık x değişkeni işaretli 4 byte'lık bir tamsayı türünden olur.
  
  Uint32_t --> işaretsiz 4 byte gerçek sayı türünden
  Uint16_t --> işaretsiz 2 byte'lık gerçek sayı türü
  
  
  		int a[100] = { 0 };
		int* p1 = a + 5;
		int* p2 = a + 65;
		p2 - p1; ---> ptrdiff_t türündendir.
		- Yani iki adres birbirinden çıkarılırsa ptrdiff_t türünden bir tamsayı elde edilir. Yine derleyiciye bağlı bir türdür.

- Bir eş isim bir eş isim içerisinde kullanılabilir.

		typedef int word;
		typedef word* wptr;


- Çelişkili bir örnek:


		typedef int* IPTR;
		int main() 
		{
			int x = 10;
			int y = 45;
			const IPTR ptr = &x;
			//int *const ptr = &x;
			ptr = &y; --> sentaks hatası
			*ptr = 40; --> geçerli 
			
		}
		
- - Eğer ptr'yi const yapmak istersek;

			typedef const int* CPTR; --> olarak kullanılmalıdır.
			int main()
			{
				int x = 10;
				int y = 20;
				CPTR p = &x;
				p = &y; // geçerli
				*p = 83; // geçersiz
			}
			
  # Ders 33 - 21.04.2021
  
  **Adres Döndüren Fonksiyonlar
  
 ```
 #include <stdio.h>
  
 int g = 10; // g nesnesi global isim alanında ilk değeri verildi.

int* foo(void)
{
	return &g; //g global nesnesinin adresi, fonksiyonun geri dönüş değeri olarak gönderildi.
}

int main()
{
	int* ptr = foo();  // fonksiyonun geri dönüş değeri olan, g nesnesinin adresi ptr pointerına ilk değer olarak verildi.
	printf("*ptr = %d\n", *ptr);  

	*ptr = 767; // ptr pointerının sakladığı g nesnesinin adresinden g nesnesine içerik operatörü ile ulaşılarak g nesnesine atama yapıldı.
	printf("*ptr = %d\n", *ptr); 

	*foo() = 98;  // içerik operatörünün operantı, foo fonksiyonun geri dönüş değeridir. foo fonksiyonunun geri dönüş değeri de g nesnesinin adresi olduğu için 
	// yine g global nesnesinin değeri değiştirilmiş oldu.
	
	printf("*ptr = %d\n", *ptr);

}
 ``` 
 
 
#

```
 #include <stdio.h>
 
int g[5] = { 0, 1, 2, 3, 4 };


int* foo(void)
{
	return g;
}

int main()
{
	print_array(g, 5);
	++foo()[2]; // foo()[2] = foo() + 2 = g + 2 = &g[0] + 2 = dizinin 2. indisindeki eleman
	print_array(g, 5);
}

```
 #
 
 ```
  #include <stdio.h>
  
  
 int* get_int(void)
{
	int x; // x otomatik ömürlü olarak bildirildi.
	printf("bir tam sayi giriniz: \n");
	scanf("%d", &x);
	
	return &x; /* x'in adresi geri dönüş değeri olarak gönderildi 
			   lakin x otomatik ömürlü bir değişken olduğu için x'in scope'u bu fonksiyonla sınırlı.
			   Yani gönderilen adreste artık x nesnesi yok. 
			   */
}

int main()
{
	int* ptr;
	ptr = get_int(); /*              ptr pointerına ilk değer olarak fonksiyonun geri dönüş değeri verildi. 
					 Ancak fonksiyonda bahsettiğimiz gibi burada programcı
					 her ne kadar x'in adresini geri dönüş değeri olarak kullanmak istese de 
					 x'in scope'u çağrılan fonksiyonla sınırlı olduğu için x artık bu adreste yer almamaktadır. 
					 Ve bu adres kullanıldığında tanımsız davranışa yol açmaktadır.*/ 
	printf("girilen sayi: &d\n", *ptr);

}

 ```
 #
 **Uyarı :
 		Adres döndüren fonksiyonlar asla otomatik ömürlü bir nesne adresi döndürmemelidir. 
		Eğer geri dönüş değeri otomatik ömürlü bir nesne olması durumunda tanımsız davranışa yol açmaktadır.
 #
 
 - Peki fonksiyonlar hangi adresleri döndürebilir?,
 	- Statik Ömürlü nesnelerin adresleri:
 		- global değişkenler
 		- static yerel değişkenler 
 		- string literalleri (henüz değinmedik)

	- Çağrılan koddan aldığı adresi geri döndürebilir.
		
		
 
 
 - T bir tür olmak üzere 
 
 		T* türü
		const T* türü = T const* türü --> aynılar
		
- Const int* türüne int* türü ilk değer verilmesinde herhangi bir problem yoktur.

		int x = 10;
		const int* p = &x;
		// const int* türüne, int* türü ilk değeri verilmiş
		
- Ancak const int* türünün, int* türüne dönüştürülmesi ciddi bir yanlışlıktır.

		const int x = 10;
		int* p = &x;//  sentaks hatası yoktur. Ama ciddi bir semantik hata vardır.
			    //'initializing': different 'const' qualifiers --> bu uyarıyı alırsınız ama sentaks hatası almazsınız.
		
		*p = 14; // Ve siz const x'e yanlış bir tür dönüştürmesin yapdıktan sonra, 
			 //nesnenin adresini yandaki gibi kullanırsanız tanımsız davranışa yol açmış olursunuz.
			 
			 
- Biz yukarıdaki durumu fonksiyonda geri dönüş adresi yoluyla kullanmak istersek bu dönüşümü bilinçli olarak yapabiliriz. (const cast)
	 
	 	(int*) dönüştürme operatörünü kullanarak.
		

- Buna örnek olarak; bir dizinin adresi bir fonksiyona gönderilsin. Bu fonksiyon bu dizinin en büyük elamanını bulsun ve
		 en büyük elemanının adresini geri dönüş değeri olarak göndersin.		
 
  
  
```
  
  #include <stdio.h>
  
  int* get_array_max(const int* pa, size_t size)
  {
	int* pmax = (int*)pa; //const cast --> dizinin ilk değerinin adresi pmax pointerına atandı.
	for (size_t i = 1; i < size; ++i) {
		if (pa[i] > *pmax) { //pa dizinin i. elemanın içeriği ile pmax dizisinde adresi olan nesnenin içeriği karşılaştırıldı.
			pmax = (int*)(pa + i); // ya da pmax = (int*) &pa[i]; yazılabilir.
		}
	}
	return pmax;  /* Dikkat!! Biz burada otomatik ömürlü bir pointer nesnenin değeri olan adres gönderiyoruz. 
			 Otamatik ömürlü bir nesnenin adresini göndermiyoruz. Geri dönüş değeri içeriğinin adres olması ile
			 geri dönüş değerinin kendisinin adres olması farklı şeylerdir. Geri dönüş değeri otomatik ömürlü bir nesnesin adresini gösteriyorsa eğer
			 fonksiyondan çıkıldığında o adreste herhangi bir nesne olmuyor. Lakin siz otomatik ömürlü bir pointer ile adres gönderdiğinizde 
			 o adresteki nesnenin ömrü bulunduğunuz fonksiyonla sınırlı değil. 
			 */
  }


int main()
{
	int a[SIZE];
	int* pmax;

	randomize();
	set_array_random(a, SIZE);
	print_array(a, SIZE);
	
	pmax = get_array_max(a, SIZE);
	printf("max = %d ve dizinin %d indisli elemani\n", *pmax, pmax - a);

	*pmax = -1;
	print_array(a, SIZE);
	
	// Eğer siz dizinin ilk elemanından başlayıp max elemanına kadar ekrana yazdırmak isterseni eğer :
	
	print_array(a, pmax - pa + 1);
	
	//Eğer max elemandan başlanıp dizinin sonuna kadar yazılması istenirse :
	
	print_array(pmax, SIZE - (pmax - a));

}

 ```
  
  
 # 
 

 
		 void func(int*);
  		 int* foo(void);
		 
		 int main()
		 {
		 	//Benim amacım foo işlevine yapılan çağrıdan elde edilen adresi func işlevine argüman olarak göndermek ise;
			func(foo()); // sık bir kullanım şeklidir.
		 }

  
  - max fonksiyonunda dizinin max değerinin indisinin adresi bulunsun. min fonksiyonunda da dizinin min değerinin adresi döndürülsün.
  		- min değer max değerden önceyse min-max arası ekrana yazdırılsın.
  		- max değeri min değerinden önceyse max-min arası ekrana yazdırılsın.



```

int* get_array_max(const int* pa, size_t size)
{
	int* pmax = (int*)pa; // const cast
	for (size_t i = 1; i < size; ++i)
	{
		if (pa[i] > *pmax) {
			pmax = (int*)(pa + i);
		}
	}
	return pmax;
}
int* get_array_min(const int* pa, size_t size)
{
	int* pmin = (int*)pa; // const cast
	for (size_t i = 1; i < size; ++i)
	{
		if (pa[i] < *pmin) {
			pmin = (int*)(pa + i);
		}
	}
	return pmin;
}

int main()
{
	int a[SIZE];
	int* pmax;
	int* pmin;
	randomize();
	set_array_random(a, SIZE);
	print_array(a, SIZE);

	pmax = get_array_max(a, SIZE);
	pmin = get_array_min(a, SIZE);

	if (pmin > pmax) 
		print_array(pmax, pmin - pmax + 1);
	
	else
		print_array(pmin, pmax - pmin + 1);
		
	//if - else merdiveni yerine --> print_array(pmin > pmax ? pmax : pmin, abs(pmin - pmax) + 1); yazılabilir.
	
	// print_array fonksiyonuna alternatif olarak da;
	
	if (pmin < pmax)
		while (pmin <= pmax)
			printf("%3d ", *pmin++);
	else
		while (pmax <= pmin)
			printf("%3d ", *pmax++);
}
```
  
  
  - O(n^2) karmaşıklığında bir sıralama algoritması:
  	- selection sort (seçme-sıralama algoritması)
  	
```




int* get_array_min(const int* pa, size_t size)
{
	int* pmin = (int*)pa; //const cast
	for (size_t i = 1; i < size; ++i) {
		if (pa[i] < *pmin)
			pmin = (int*)(pa + i); // pmin = (int*)&pa[i]
	}
	return pmin;
}

void selection_sort(const int* pa, size_t size)
{
	for (size_t i = 0; i < size; ++i)
		swap(get_array_min(pa + i, size - i), pa + i);
}




int main()
{
	int a[SIZE];
	randomize();
	set_array_random(a, SIZE);
	print_array(a, SIZE);
	selection_sort(a, SIZE);
	print_array(a, SIZE);
}
```
  
  
  
  
- Dikkat: Eğer bir fonksiyon statik ömürlü bir nesne adresi döndürüyorsa bu fonksiyon hep aynı nesnenin adresini döndürüyor demektir.
  Bu durumda fonksiyona yapılan çağrıdan sonra ilk çağrıdan elde ettiğimiz adresteki değeri kullanmadan tekrar çağırmamalıyız.
  
  
```
  char* get_name(void)
{
	static char str[100];
	scanf("%s", str);
	return str;
}




int main()
{
	printf("3 farkli yazi giriniz:");
	char* p1 = get_name();
	char* p2 = get_name();
	char* p3 = get_name();

	printf("girdiginiz uc isim : %s %s %s", p1, p2, p3);
	/* Programı çalıştırdığımızda ekrana en son girilen değeri 3 kez yazdırıldığı görülecektir. 
	   Ancak beklenen her değerin ayrı ayrı yazdırılmasıdır. Yani bunu düzeltmenin yolu geri dönüş değerini bir değişkene 
	   atamak olabilir.
	*/
}
```


 **NULL Pointer

- NULL bir makrodur. (bir sembolik sabittir)
Bir keyword, identifier değildir.

- NULL makrosu C'nin bazı başlık dosyalarında tanımlanmıştır.
- <stdio.h>, <stdlib.h> vs.
- NULL bir adres sabitidir. (NULL pointer diye okuyunuz.) (NULL gösterici)
- Bu adres sabiti pointer değişkenlere ilk değer olarak verilebilir ya da atanabilir.
- NULL pointer değerini asla pointer olmayan bir değişkene atamayın.
- NULL pointer, herhangi türden bir pointer değişkene atanabilir. 

		int* p = NULL;
		double* = NULL;
		
- Bir pointer değişkenin değeri NULL pointer ise bu pointer geçerli (valid) pointer'dır.
- Değeri NULL pointer olan bir değişken (semantik olarak) hiçbir nesneyi göstermeyen bir değişkendir.


		#include <stdio.h> 
		
		int main()
		{
			int x = 10; 
			int a[5];
			int* p; ---> semantik açıdan geçersiz (çöp değerde)
			int* q = NULL; ---> semantik açıdan geçerli.
			int* ptr = a + 5; --> geçerli / dizinin bir elemanının adresini gösteriyor.
			int* px = &x; ---> x'in adresini gösteriyor ve geçerli.
		}
		

- Değeri NULL pointer olan bir pointer değişkeni, dereferance etmek yani *ptr, ptr[i] gibi kullanmak tanımsız davranıştır.
  Çünkü değeri NULL pointer'sa herhangi bir nesneyi göstermiyor. Ancak içerik(*) operatörünün veya köşeli parantez 
  operatörünün operantı olması için bir adres göstermesi gerekiyor. 
  	
		Yukarda anlatılan durum bir sentaks hatası değildir. Tanımsız davranıştır.
		
- Aynı şekilde değeri NULL pointer olan bir değişkeni toplama, çıkarma, ++, -- veya pointerlar arası çıkarma 
  işlemine sokarsanız tanımsız davranıştır.
  
- Bir pointer değişkenin NULL pointer olup olmadığını sınayabiliriz.

		int x = 10; 
		int* ptr = &x;
		if (ptr == NULL)
			printf("ptr null pointer'dır\n");
		
- Eğer iki pointer değişkenin ikisinin de değeri NULL pointer ise bu iki ptr değişken değerce eşittir.

- İlk değer verilmemiş global ve statik pointer değişkenler hayata NULL pointer ile başlatılır.


		//global alan
		int* p; --> hayata NULL pointer ile başladı.
		int x; --> ilk değeri 0 olarak hayata başladı.
		

- C'de lojik ifade beklenen yerlerde bir adres ifadesi kullanılabilir.
	- Bir adres lojik yorumlamaya tabi tutulduğunda NULL olup olmadığı değerlendirilir.

			if (ptr) --> if (ptr != NULL)
			if (!ptr) --> if (ptr == NULL)
			
- Normal olarak bir pointeir değişkene bir adres atanmalıdır. Bir pointer değişkene bir tam sayı atanması C dilinde yanlıştır.
 Ancak bu durumun bir istisnası vardır.
 	- Eğer bir pointer değişkene 0 tam sayı sabiti atanırsa derleyici o tam sayı sabitini
 	  (implicitly) olarak NULL pointer değerine dönüştürür.
	  
		int * p = NULL ile int* p = 0 aynı işlemi gören ifadelerdir.
		
- Her ne kadar dilin kuralları bu kullanıma izin verse de programcılar özel durumların dışında dikkat çekmesi için daha çok
  NULL makrosu kullanma eğilimindedirler.
  	- Aradaki tek fark şudur;
  	- Eğer 
  	
  			int* ptr = NULL; 
	- Kullanırsanız NULL makrosunu içeren başlık dosyalarından birini include etmeni gerekirken
	
			int *ptr = 0; 
	- Kullanımında herhangi bir başlık dosyası include etmenize gerek yoktur.
  		
  # Ders - 34 - 23.04.2021
  
  
  - Null karakterle karıştırılmamalıdır.
  - NULL pointer conversion
  
  - Bir pointer dizisinde ilk değer verilirken dizide değer verilmeyen elemanlar hayata NULL pointer değeri ile başlarlar.

		 int* func(void); // geri dönüş değeri adres olan bir fonksiyon
		 
- Adres döndüren fonksiyonların bir kısmı başarısızlık bilgisini NULL pointer ile döndürerek çağırana aktarıyorlar.
- Yani en çok kullanıldığı senaryo başarısızlık (işini yapamama) durumunda NULL pointer döndürülüyor.
	- Yalnız bütün adres döndüren fonksiyonlar için böyledir diye düşünmüyoruz asla.
	- Bu farkı biz bilmek zorundayız. Eğer standart C fonksiyonuysa zaten bilmek zorundasınız. 
	Eğer değilse mutlaka dökümantasyonuna bakılmalıdır.
		- Ek olarak adres döndüren bir fonksiyon gördüğümüzde fonksiyonun geri dönüş değerinin 
		  başarısızlık durumunda NULL değerinin geri dönüş değeri olarak döndürülüp döndürülmediği kontrol edilmelidir.
		  
- Bazı fonksiyonlar veri yapılarında arama yapıyorlar. Böyle fonksiyonlara arama(search) fonksiyonu denildiğine değinmiştik
Genellikle C'de arama fonksiyonları adres döndürüyorlar. Aranan değer bulunursa o değere sahip nesnenin adresini, 
bulamaz ise NULL pointer döndürüyor.


- Bir başarısızlık (işini yapamama) durumunda geri dönüş değeri olarak NULL pointer döndüren bir fonksiyon yazalım.
```
#define _CRT_SECURE_NO_WARNINGS

#include <stdio.h>
#include <time.h>
#include <stdlib.h>
#include <ctype.h>
#include <string.h>
#include "nutility.h"

#define SIZE	10


int* search(const int* p, size_t size, int val)
{
	while (size--) {
		if (*p == val)
			return (int*)p; //const cast
		++p;
	}
	return NULL;
}
int* alternatifsearch(const int* p, size_t size, int val)
{
	for (size_t i = 0; i < size; ++i) {
		if (p[i] == val)
			return (int*)(p + i); //const cast
	}
	return NULL;
}

int main()
{
	int a[SIZE];
	int ival;
	int* p;

	randomize();
	set_array_random(a, SIZE);
	print_array(a, SIZE);

	printf("yukaridaki dizide aranacak sayiyi giriniz: ");
	scanf("%d", &ival);
	p = search(a, SIZE, ival);
	if (p != NULL) { //if (p) olarak da kullanılabilir!
		printf("%d indisli elemanda bulundu...\n", p - a);
	
	}

		
}

```
  
- Uyarı: int* search(const int* p, ...); yandaki fonksiyon tanımında geri dönüş değeri adres olduğunu görünce ve bize 
verilen dizinin de okuma amaçlı olduğunu const u görüp anladığımızda aklımıza bu fonksiyonda const cast yapılacağı canlanmalıdır.


- Bir fonksiyonun parametresinin bir pointer olması durumunda, böyle bir fonksiyona bir nesne adresi gönderilmesi gerekiyor.
 Null pointer gönderilirse UB olur.
 	- Ancak bazı fonksiyonları çağıran kodların NULL pointer göndermelerini bir seçenek, opsiyon olarak sunabiliyor. 
 	  Böyle bir seçenek mevcutsa mutlaka dökümante edilmiştir.
 		- Yani fonksiyon bize opsiyonel olarak ya bir nesne adresi ya da NULL pointer isteyebilir. Böyle durumda UB yaşanmaz.


- Konuyu toplarsak 2 uyarımız mevcut. 
	- Adres func()---> adres döndüren fonksiyonların geri dönüş değeri türünün ne anlama geldiğini mutlaka okumalıyız.
	  NULL pointer döndürme durumu var ise (başarısızlık durumunda) ona göre çağrı yapılarak önlem alınmalıdır.
	- void func(int* p) ---> Parametresi pointer olan bir fonksiyonda da mutlaka acaba bu fonksiyona NULL pointer göndermem
	  bana verilmiş bir opsiyon mu değil mi diyerek dökümantasyon incelenmeli ve teyit edilmelidir.
	  
- Bir pointer değişkene NULL makrosu ilk değer verilerek bayrak değişken olarak kullanılabilir.

		int* ptr = NULL;
		if (ptr)
			ptr = &(variable);
		if (!ptr) // ptr değişkeninin hala NULL olup olmadığı kontrol edildi.
			//something
  
  - Null pointerının kullanıldığı bir durum daha var. Ancak bu daha çok dinamik bellek yönetiminde karşımıza çıkmakta. 
  	- Pointer değişkenimiz hayatında devam ederken onun göstermekte olduğu nesnenin hayatı sona eriyor.
  		- (pointer invalidation)

		int* p;
		if (p) {
			int x = 10;
			p = &x;
		}
- Yukarıda p pointerına otomatik ömürlü x nesneinin adresi atandı. Ancak block'dan çıkıldığında x nesnesinin ömrü sona erdi
 ve p pointerı çöp değer halin, aldı. İşte tam da burada NULL makrsou p pointerına atanarak hem p'nin hiçbir nesneyi göstermediği belirtilmek 
 hemde p'yi çöp değerden çıkarıp geçerli bir pointer haline getirmek için kullanılır. Yalnız bu P'yi dereference(*) edebileceğiniz anlamına asla gelmemektedir.
 
 
 
 - NULL Pointer 					NULL Character
  - NULL 						- '\0'
  - yani bir makro önişlemci tarafından			- bildiğimiz tam sayı sabiti.
   bir yer değiştirme işlemine sokuluyor.
   - Bir adres sabitidir.				- bir tamsayı sabiti.
   - pointer değişkene atanır.				- char dizinin elemanına atanır. Ya da 
   							  bir int değişkene atanır.
							  
							  
# Yazılar Üzerinde İşlem Yapan Fonksiyonlar

**<string.h> Kütüphanesi
  
- Hatırlatma olarak bir yazı dizisini ekrana yazdıran puts fonksiyonunu bir de biz yazalım.

```
#define _CRT_SECURE_NO_WARNINGS

#include <stdio.h>
#include <time.h>
#include <stdlib.h>
#include <ctype.h>
#include <string.h>
#include "nutility.h"

#define SIZE	100

void myputs(const char* p)
{
	while (*p != '\0')
		putchar(*p++);

	putchar('\n');
}

void myputs2(const char* p)
{
	for (int i = 0; p[i] != '\0'; ++i)
		putchar(p[i]);

	putchar('\n');
}



int main()
{
	char str[SIZE] = "something about";

	puts(str);
	myputs(str);
	myputs2(str + 9); // about ekrana yazılır.


}
``` 

- sgets() fonksiyonunu yazalım.
```
void mysgets(char* p)
{
	int ch;
	while ((ch = getchar()) != '\n') // getchar fonksiyonun geri 
		*p = (char)ch;		    //dönüş değeri int olduğu için ch int tanımlanıp sonrasında type cast yapıldı.

	*p = '\0';
		
}
```
  
- Dikkat: Eğer siz standart bir C fonksiyonu çağırıyorsanız ve boyut göndermiyorsanız taşma olmaması 
için çok dikkatli olmalısınız.

- <string.h>
- Dikkat!! Öğrenmek amaçlı yazılması haricinde standart C fonksiyonu ile aynı işi yapan bir fonksiyon tanımlamayınız.

	+ strlen    + strcpy
	+ strchr    + strcat
	+ strrchr   + strcmp
	+ strstr    + strncpy
	+ strpbrk   + strncmpt
	+ strspn    + strncmpt
	+ strtcpn   + strcat
	+ strtok
	
- Yazının uzunluğunu ölçen bir örnek:

```
#define _CRT_SECURE_NO_WARNINGS

#include <stdio.h>
#include <time.h>
#include <stdlib.h>
#include <ctype.h>
#include <string.h>
#include "nutility.h"

#define SIZE	100



int main()
{
	char str[SIZE];

	printf("bir yazi giriniz: ");
	sgets(str);
	size_t len = strlen(str); //strlen fonksiyonun geri dönüş türüne göre len fonksiyonun türü belirlendi.
	printf("uzunluk = %zu", len); //%zu size_t formatı

}

```

#
- Bir yazıyı ters çevirip ekrana yazdıran fonksiyon:
```
#define _CRT_SECURE_NO_WARNINGS

#include <stdio.h>
#include <time.h>
#include <stdlib.h>
#include <ctype.h>
#include <string.h>
#include "nutility.h"

#define SIZE	100

void rputs(const char* str)
{
	for (int i = (int)strlen(str) - 1; i >= 0; --i)
		putchar(str[i]);

	putchar('\n');

}


int main()
{
	char str[SIZE];

	printf("bir yazi giriniz: ");
	sgets(str);
	rputs(str);
}

```
# 

- strlen fonksiyonunu biz yazarsak eğer :

```
size_t mystrlen(const char* str)
{
	size_t len = 0;

	while (*str++ != '\0')
		++len;

	return len;
}
alternatif olarak
size_t mystrlen(const char* p)
{
	const char* ps = p;
	
	while(*p)
		++p;
	return p - ps;
}
```

# Ders- 35 - 26.04.2021
- char* strchr(const char *p, int c)
- Yukardaki fonksiyon tanımından, fonksiyonun ikinci parametresinin bir karakter numarası olduğunu görüyoruz. 
  geri dönüş değerinin adres olduğunu görüyoruz.
 - Bu fonksiyona bir dizi adres ve karakter gönderdiğimizde bize o karakter dizide varsa bulunduğu adresi, eğer yoksa NULL pointer döndürüyor.

- Kısa bir örnek:

```
#define _CRT_SECURE_NO_WARNINGS

#include <stdio.h>
#include <time.h>
#include <stdlib.h>
#include <ctype.h>
#include <string.h>
#include "nutility.h"

#define SIZE	100


int main()
{

	char s[SIZE];
	printf("bir yazi giriniz:");
	sgets(s);

	// Bu yazıda a karakterini arayalım.
	char* p = strchr(s, 'a');

	if (p) { //if (p != NULL) 
		printf("aradiginiz karakter girilen yazida %d indisinde.\n", p - s);
		*p = '*';
		puts(s);
	}
	else
		printf("aranan yazi bulunamadi.....\n");

}---> Gönderilen karakteri sağdan sola yazıda ilk gördüğü adreste buldu.

```
#
- Peki biz gönderilen karakterin kaç tane olduğunu bulmak istersek

```
size_t count(const char* p, int ch)
{
	size_t cnt = 0;
	while (*p) {
		if (*p++ == ch)
		  ++cnt;

	}

	return cnt;

} ---> standart bir fonksiyon değil
```

- char* strrchr(const char* p, intc); 
	- Bu standart fonksiyon ise karakter aramasını sağdan sola doğru gerçekleştirir.
- Dikkat: Her ne kadar null karakter yazıya dahil olmasa da strchr ile null karakteri aratabilirsiniz.

- Aşağıda ekrana girilen yazının sonuna ünlem işareti eklemeye bakalım.

		char[SIZE];
		char* p;
		
		printf("Bir yazi giriniz: ");
		sgets(s);
		
		p = strchr(s, '\0'); // yazının bittiği yerin adresini bulduk.
		*p++ = '!'; // Yazının sonuna ! eklendi.
		*p = '\0'; // Yazının bittiğine dair null karakter eklendi.
		
		printf(" (%s) \n", s);
		

- Şimdi bir de strchr() fonksiyonunu biz yazmayı deneyelim:

```
char* mystrchr(const char* p, int val)
{
	while (*p) {
		if (*p == val)
			return (char*)p;
		*p++;
	}

	if (val == '\0') // aranan karakterin null karakter olması ihtimaline karşın
		return (char*)p;

	return NULL;
}

```

#
- Şimdi de strrchr() fonksiyonunu yazalım.

```
char* mystrrchr(const char* p, int val)
{
	const char* pfound = NULL;

	while (*p) {
		if (val == *p)
			pfound = p;
		++p;
	}

	if (val == '\0')
		return (char*)p;

	return pfound;
}

```
#

- Bir yazının adresini tutan pointer'ı yazının sonundaki null karakteri gösterecek hale getirmek için;

+ while (*p != '\0')  //while (*p)
	++p;
	
+ while(*p++)
	;
  --p;
  
+ if(*p)
    while (*++p)
     	;
	
+ p += strlen(p);

+ p = strchr(p, '\0');


- char* strstr( const char *psource, const char* psearched);
	- Yazınin içerisinde yazı arayan fonksiyondur. 1. parametre arama yapılacak dizinin adresidir. 2. parametre ise aranan yazı dizisinin adresi.
	- Geri dönüş değeri ise yazıyı bulduğu takdirde dizinin bulduğu elemanın adresi, Bulamazsa NULL pointer.


- Yazının içerisinde aranan yazıyı yıldız yapan program:

```
#define _CRT_SECURE_NO_WARNINGS

#include <stdio.h>
#include <time.h>
#include <stdlib.h>
#include <ctype.h>
#include <string.h>
#include "nutility.h"

#define SIZE	100


int main()
{

	char source[SIZE];
	char search[SIZE];

	printf("aranacak yaziyi giriniz:\n");
	sgets(source);
	printf("girilen yazinin icerisinde aranacak yaziyi giriniz:\n");
	sgets(search);

	char *p = strstr(source, search);

	if (p) {  // burada dönen adres olduğu için, adresin null olup olmadığı kontrol ediliyor dikkat!!
		printf("aranan yazi bulundu...\n");
		for (int i = 0; i < strlen(search); ++i) {
			*p = '*';
			++p;
		}
		puts(source);
	}
	else
		printf("aranan yazi girilen yazida bulunamadi...\n");

}


```

#
- Şimdi strstr fonksiyonunu yazalım ilki benim yazdığım hali ikincisi Plauger standart c library kitabından alıntı..

```

char* mystrstr(const char* psource, const char* psearch)
{
	const char* temp = psearch;
	while (1) {

		if (*psource == *temp || *temp == '\0' ) {
			if (*temp == '\0')
				return (char*)(psource - strlen(psearch));
			++psource;
			++temp;
			

		}

		else {
			if (*psource == '\0')
				return NULL;
			temp = psearch;
			++psource;
		}

	}
	
}
```

# 
Plauger'ın yazdığı 

```

char* mystrstr(const char* psource, const char* psearch)
{
	if (*psearch == '\0')
		return (char*)psource;
		
	for (; (psource = strchr(psource, *psearch)) != NULL; ++psource) {
		const char* sc1, * sc2;

		for (sc1 = psource, sc2 = psearch; ; ) {
			if (*++sc2 == '\0')
				return (char*)psource;
				
			else if (*++sc1 != *sc2)
				break;
		}
		
	}
	
	return NULL;
}

```
#

- char* strpbrk(const char* psource, const char* pchars);
	- Birinci parametre arama yapılacak olan diziyi, ikinci parametre ise karakterlerin olduğu bir diziyi ifade ediyor. İkinci parametredeki karakterlerden birini, birinci dizide ilk bulduğu adresi geri dönüş değeri olarak döndürüyor. Bulamazsa NULL pointer döndürüyor.

- Bir örnek yazalim:

```
        char source[SIZE];
	char str[] = "aeou";

	printf("aranacak yaziyi giriniz:\n");
	sgets(source);

	char* p = strpbrk(source, str);

	if (p) {
		printf("aranan yazi %d indiste bulundu....\n", p - source);
		*p = '*';
	    puts(source);
	}
	else
		printf("aranan yazi bulunamadi\n");

```

- Şimdi de strpbrk() fonksiyonunu yazalim:

```
char* mystrpbrk(const char* p, const char* ch)
{
	while (*p) {
		if (strchr(ch, *p))
			return (char*)p;
		
		++p;
	}
	return NULL;
}
```


- char* strcopy(char* pdest, const char* psource);
	- Geri dönüş değeri işlem yaptığı dizinin adresidir. İkinci parametredeki dizi birinci parametredeki adrese kopyalanır.

```
#define _CRT_SECURE_NO_WARNINGS

#include <stdio.h>
#include <time.h>
#include <stdlib.h>
#include <ctype.h>
#include <string.h>
#include "nutility.h"

#define SIZE	100





int main()
{

	char source[SIZE];
	char dest[SIZE];

	printf("kopyalanacak yaziyi giriniz:\n");
	sgets(source);

	strcpy(dest, source);

	printf("[%s]  [%s] ", source, dest);


}

```

#

- Dikkat!! : strcpy fonksiyonu pointer hatalarına açık. Yani sizin gönderdiğiniz adresteki dizilerden kopyalanacak olan dizinin boyutu 
yetersiz kaldığında 

- strcpy fonksiyonun bizim yazdığımız hali:

```

char* mystrcpy(char* d, const char* s)
{
	char* p = d;

	while (*p++ = *s++)
		; // null statement

	return d;

}

```

- Overlapped Blocks (Kesişen bloklar)
	- Eğer bir okuma - yazma işlemi kesişen bloklar üstünde yapılıyorsa standart C fonksiyonları işlemin güvenilir 
	  bir şekilde yapılıp yapılamayacağını belirliyor.

	char str[SIZE];
	strcpy(str + 2, str); // Tanımsız Davranış (UB);
	printf("%s\n", str);


- strcpy fonksiyonun standartlarda tanım farklılığı olduğunu görüyoruz. 
 	- char* strcpy(char* dest, const char *src); ----(c99'a kadar)
 	- char* strcpy(char* restrict dest, const char* restrict src); -----(c99'dan sonra)

	- Yukarıdaki restrict anahtar sözcüğü şu anlama gelmektedir. Bu adreslerdeki bellek bloklarının bu işlem yapıldığı sürece 
	bir kesişim kümesi olmadığına güvenerek yapıyorum. Bu duruma uyulmadığı taktirde UB'ye yol açacaktır.
	
- Bu tür kopyalama işlemleri bu güvenceyi veren memove işlemi ile yapılmalıdır.


- char* strcat(char* pdest, const char* psource);
	- cat kısaltması "concatenate = birleştirme" kelimesinden gelmektedir.
	- Bu fonksiyon iki dizideki yazıyı birleştirerek birleştirilen dizinin adresini geri dönüş değeri olarak döndürür.
	

- Kullanım örneği: 

	
		char s1[SIZE], s2[SIZE];
		
		printf("iki isim giriniz: ");
		scanf("%s%s", s1, s2);
		strcat(s1, s2);
		printf("(%s)\n ", s1);

- Yine bu fonksiyonda da taşma durumunu gözetmek sizin sorumluluğunuzda.

- C'nin c11(2011) standartlarııyla opsiyonel olarak _s ile biten fonksiyonlar var. Bu fonksiyonların
 farkı yazma amaçlı alınan dizinin boyutunu da alması ve böylece taşmama garantisi de vermesidir.
 
 - Şimdi strcat fonksiyonunu bir de biz oluşturalım.
 
```
char* mystrcat(char* pdest, const char* psource)
{
	char* p = pdest;

	while (*pdest)
		++pdest;


	while (*pdest++ = *psource++)
		; // null statement

	return p;

}
```
- strcat fonksiyonunun plauger'ın yazdığı şekli:

```
char* mystrcat(char* pdest, const char* psource)
{
	char* s;
	for (s = pdest; *s != '\0'; ++s)
		;
	for (; (*s = *psource) != '\0'; ++s, ++psource)
		;

	return pdest;

}
```
- Alternatif olarak :

```
char* mystrcat(char* pdest, const char* psource)
{
	strcpy(pdest + strlen(pdest), psource);
	return pdest;
}
char* mystrcat(char* pdest, const char* psource)

```


- Bir örnek:

```
	char s1[SIZE];
	char s2[SIZE];
	char s3[SIZE];
	
	printf("İki isim girin: \n");
	scanf("%s%S", s1, s2);
	
	strcpy(s3, s1);
	strcat(s3, s2);
	
	printf("(%s) + (%s) = (%s)", s1, s2, s3);


```

- Yazıların karşılaştırılması strcmp fonksiyonu:

	- Herehangi bir programda c ve ya karşılaştırılsın (yazılan satırlar temsili)

		x ve y compare(date x, date y);
		 
		if (x > y) ----> retval > 0
		if (x < y) ----> retval < 0
		if (x == y)----> retval == 0
		
- Yukarıda anlatılmak istenen fonksiyonun geri dönüş değeri int değerden ve iki yazının kıyaslanması geri dönüş değerinin pozitifliği 
veya negatifliği ile sağlanmaktadır.

- int stcmp(const char* pleft, const char* pright);

		if (strcmp(s1, s2) == 0) ---> s1, s2 birbirine eşitse if in içerisine gir
		if (!strcmp(s1, s2)) ----> s1 , s2 ye eşitse gir


- Yazıların büyüklüğü küçüklüğü konusunda kullanılan algoritma lexicographical compare 'dir.

		- container (collection) comparison
			- Aynı türden ögeleri bir arada tutan veri yapılarına verilen terim


- İki farklı dizi karşılaştırıldığında karşılıklı öğe çiftleri karşılaştırıldığında ilk farklı çift bulunduğunda
  bu çiftten hangisi daha büyükse o dizi büyük olmuş olur. (ASCII'ye göre sayısal olarak karşılaştırmadır bu)
  
  		2 4 7 9 6
		2 4 7 5 1 ----> burada 9 ile 5 ilk farklı olan değerlerdir. 9 daha büyük olduğundan üstteki dizi daha büyük olur.
		
		
		- 2 4 7 9
		  3      ----- burada 2. dizi daha büyük olarak algılanır.
		  
		- 1 2 3 4
		  1 2 3   ---> burada 1. dizi dah büyüktür.
		  
		- cumhuriyet
		  ok   ---> o'nun karakter kodlama karşılığı daha büyük olduğundan 2. dizi büyüktür.
		  
		- can
		  candan   ----> candan büyüktür.
		  
		  
		- masa
		  MASA   ----> masa daha büyüktür.
		  
		  
- Bir örnekle girilen yazılar kıyaslansın:

```
#define _CRT_SECURE_NO_WARNINGS

#include <stdio.h>
#include <time.h>
#include <stdlib.h>
#include <ctype.h>
#include <string.h>
#include "nutility.h"

#define SIZE	100



int main()
{

	char s1[SIZE];
	char s2[SIZE];
	int result;

	printf("iki kelime girin:  ");
	scanf("%s%s", s1, s2);

	result = strcmp(s1, s2);

	if (result > 0)
		printf("%s > %s\n ", s1, s2);
	else if (result < 0)
		printf("%s < %s\n", s1, s2);
	else
		printf("%s = %s\n", s1, s2);

}
```

- Bizim yazdığımız hali:

```
int mystrcmp(const char* pleft, const char* pright)
{
	for (; *pleft == *pright; ++pleft, ++pright) {
		if (*pleft == '\0')
			return 0;
	}
	
	return *pleft - *pright;
}

```


- stricmp fonksiyonu standart değiş ama genel olarak derleyicilerde vardır.
	- Karşılaştırmayı "case insensitive" büyük - küçük harf uyumuna bakmadan yapıyor.

- Uyarı:


		char s1[SIZE];
		char s2[SIZE];
		
		if (s1 == s2) { // always false
			printf("something\n");
		else 
			printf("something....\n");
  
- Yukarıdaki kullanımda array decay özelliği sebebiyle yalnızca dizinin ilk elemanının adresleri karşılaştırılmıştır.


- Yazılarda trim: yazının başındaki ya da sonundaki boşlukların ya da özel karakterlerin yazıdan çıkartılması demektir.


- Bir mülakat sorusu:

		
		int is_at_end(const char* p1, const char* p2)
		- p1 adresindeki yazi p2 adresindeki yazi ile mi bitiyor.

	- eğer doğru ise non-zero, eğer yanlış ise zero değer döner.


		int is_at_end(const char* p1, const char* p2)
		{
			size_t  len_p1 = strlen(p1);
			size_t  len_p2 = strlen(p2);
			
			if (len_p2 > len_p1) --> eğer bu karşılaştırma yapılmazsa tanımsız davranışa yol açılmış olur.
				return 0;
				
			return !strcmp(p1 + len_p1 - len_p2, p2);
				
		}
  
  
  - Ödev sorusu: ikinci yazıyı birinci yazının başına ekleyen fonksiyonu yazınız:
  - char* str_pretend(char* pdest, const char* psource);
- !!!!ara değişken dizi kullanılmadan da çözümü muhakkak vardır deneyiniz.
```

char* str_prepend(char* pdest, const char* psource)  //psource'dan okuduğun yazıyı pdest'in başına yaz
{
	char* p = pdest;

	char temp[SIZE];
	char* ptemp = temp;

	for (; *ptemp = *psource ; ptemp++, psource++)
		;


	for (; *ptemp = *pdest; ++ptemp, ++pdest)
		;

	strcpy(p, &temp);


	return p;

}
```

- standart bir fonksiyon değiş ama strrev fonksiyonu yazıyı tersine çeviriyor.

```
char* mystrrev(char* p)
{
	size_t len = strlen(p);

	for (size_t i = 0; i < len / 2; ++i) {
		char temp = p[i];
		p[i] = p[len - i - 1];
		p[len - i - 1] = temp;

	}

	return p;
}

```

# Ders 36 - 28.04.2021

- String literali aslıdna elemanları char türden olan bir dizidir.

		"Necati" --> 7 elemanlı char dizi türü
		"Necati" --> aslında bu bir dizi olduğu için derleyici bunu adres olarak algılar.
		
- Eğer siz şu şekilde bir kod yazarsanız;

		putchar(*"isim");  --> ekrana i harfi yazdırılır.
		putchar("ismail"[1]); ---> Ekrana s ismi yazdırılı.
		
		printf("%zu\n", strlen("ayse")); //yazının uzunlugu olan 4 yazısı yazdırılır.
		printf("%zu\n", sizeof("ayse")); //ekrana boyut olan 1x5 den 5 yazısı yazdırılır.
		
#

		char *p = "dıgukan";
		
		for (int i = 0; i < 7; ++i)
			putchar(p[i]); --> Ekrana dogukan yazdırılır.
  
  - String literalleri salt okuma amaçlı kullanılabilecek dizilerdir. Bir string literalini değiştirme girişimi UB'dir.

		char *p = "kaya";
		*p = 'm'; // UB 
		

- Bu UB'ye düşme ihtimalini ortadan kaldırmak için doğru kullanım;

		const char* p = "kaya";
		
#


		char* p = "kaya";
		*p = 'm'; // geçerli ama UB
		p[2] = 'n'; // geçerli ama UB
		
		- Ama siz eğer const olarak tanımlasaydınız ub ye yol açmadan sentaks hatası olacaktı.
		

- Bir fonksiyona string literali gönderilirkne de parametre tanımı const olmalıdır. Aksi halde UB'ye yol açabilir.

		char str[SIZE];
		strcpy(str, "mustafa"); // geçerli
		
		char* p = "musa";
		strcat(p, "can"); //UB
		- p'nin gösterdiği "musa" dizisine ekleme yapılacak.

- Bir kullanım şekli;

	
		char str[SIZE];
		printf("bir isim giriniz: ");
		sgets(str);
		
		if (!strcmp(str, "huseyin")) 
		 	//code
			
		- Yukarıda girilen yazının huseyin olup olmadığı sorgulandı.

- String literalleri statik ömürlü dizilerdir.

		const char *p = "erdinc kaya";
		printf(p); //doğru bir kullanımdır.
		
		char str[100] = "ilyas";
		printf(str); //geçerli 
		

- printf("merhaba arkadaslar");

		yukarıdaki bir string literali kullanıldı. Artık bu yazıyı tutan dizi statik ömürlü nesnelerin tutulduğu bellek alanında
		programın başından sonuna kadar kalıyor. Yani özellikle programcının bellek kullanımı açısından bir problemi varsa string
		literalleri idareli kullanılmalıdır.
		
#

		const char* weekday(int daynum)
		{
			switch(daynum) {
				case 1: return "pazartesi";
  				case 2: return "sali";
				case 3: return "carsamba";
				case 4: return "persembe";
				case 5: return "cuma";
				case 6: return "cumartesi";
				case 7: return "pazar";
			}
		}
		

- String litearlleri, programın başıdnan sonuna kadar bellekte kalırlar. 

	- yazı adresi döndüren bir fonksiyonun bir string literali(adresi) döndürmesi UB değildir.
	
	
  		3["aysegul"]; --> *(3 + "aysegul") == ekran 3 yazdırıldı.
		


- Dikkat: kod içerisindeki özdeş(aynı) string literalleri karşılığı derleyicilerin 
	- Bunlları tek dizi olarak tutmaları
	- Ayrı ayrı birden fazla dizi tutmaları 
	
Tamamen derleyiciye bağlıdır. (unspecified behavior)

		const char* p1 = "firat";
		const char* p2 = "firat";
		
		if (p1 == p2) --> iki pointerin eşitliği sınanmış ama derleyiciye göre aynı da olabilir farklı da olabilir. 
		    		  Bu yüzden buna güvenerak asla işlem yapılmamalıdır.
				  
- Dikkat: Adresleri karşılaştırmak ile yazıları karşılaştırmak sık yapılan hatadır.


		char str[SIZE];
		
		if (str == "fadime")
		
		- sentaks hatası yoktur. Ancak alwaysa false'dur. Çünkü str bir adresken "fadime" bir string literalidir.

		- doğru yazımı aşağıda verilmiştir.

		if (!strcmp(str, "fadime")
		
	
  - Açık ara farkla mülakatlarda karşımıza en sık çıkan mülakat sorusu.
# Soru:


- Aşağıdaki iki kod satırı arasındaki farkı açıklayınız:

      
      1- char str[] = "something";
      2- char* p = "think some";
      
      
      
# Cevap: 


**1- 
  - 1.kod satırında char türden bir dizi oluşturulmuş. Bu diziye çift tırnak içindeki yazı ile ilk değer verilmiş. Burada 
  sadece ve sadece bir dizi tanımlanıyor. Yani programın başından sonuna kadar kalacak bir string sabiti yoktur. Bu dizilere ilk değer
  verme sentaksının bir bileşeni. Yani şöyle düşünmemeliyiz. str dizisi something yazısını tutacak ayrıca derleyicinin yazı için 
  ayırdığı bellek alanında yazı programın sonuna kadar kalacak. Böyle bir durum söz konusu asla değildir. Bu kod sadece ilk değer 
  vermenin kısa bir yoludur. Ayrıca str dizini değiştirmenizde hiçbir engel yoktur. Const eklenirse tabiki durum daha farklı olabilir.
  
  **2-
  - 2.kod satırında olay tamamen farklı. Burada ise siz pointer değişken tanımlıyorsunuz. Bu pointer değişkene bir string 
   literalinin adresiyle ilk değer veriyorsunuz. Yani iki tane değişken oluşturdunuz. Birisi string literali, diğeri ise bu literali
   gösteren pointer. Ayrıca bu kod satırı c++'da sentaks hatasıdır. const anahtar sözcüğü ile tanımlanmalıdır. C'de de const anahtar 
   sözcüğüyle tanımlamak daha doğru olacaktır. Aksi halde pointer değişkeni dereference(*) operatörü ile içeriğini değiştirdğinde UB'ye yol
    açabilir.
  
  
  
  
  
#


		char str[100];
		
		//str dizisine "can" yazısını yerleştiren bir kkod yazınız.
		strcpy(str, "can");
		
- ilk değer verme dışında bir sabiti fonksiyon kullanmadan yazamazsınız.

		strcat(str, "dan"); ---> str yazısının sonuna dan ekini eklemiş
		


- Tipik bir c programcısının karşısına çıkabilecek bazı yazı manipülaston işlemlerinden örnekler.
```
#define _CRT_SECURE_NO_WARNINGS

#include <stdio.h>
#include <time.h>
#include <stdlib.h>
#include <ctype.h>
#include <string.h>
#include "Rutility.h"

#define SIZE 100




int main()
{
	char old_file_name[SIZE];
	char new_file_name[SIZE];

	printf("Eski dosya ismini giriniz: \n");
	scanf("%s", old_file_name);

	//1 old_file_name'deki dosya ismini new_file_name dizisine kopyalayınız.
	
	strcpy(new_file_name, old_file_name);
	printf("1  %s\n\n", new_file_name);

	//2 eğer dosya uzantısı yok ise .dat uzantısı olacak biçime getiriniz.

	char *p = strrchr(new_file_name, '.');
	if (!p) {
		strcat(new_file_name, ".dat");

		printf("2   %s\n\n", new_file_name);
	}
	
	// 3 eğer dosya uzantısı .xls ise uzantıyı .doc olarak değiştirin

	  if (!strcmp(p, ".xls")) {
		strcpy(p, ".doc");

		printf("3   %s\n\n", new_file_name);
	}

	// 4 eğer dosya uzantısı .jpg ise uzantıyı silin 

	else if (!strcmp(p, ".jpg")) {
		  *p = '\0';
		printf("4   %s\n\n", new_file_name);
	}



	// 5 bunların hiçbiri değilse .txt uzantılı hale getirin

	else {
		strcpy(p, ".txt");
		printf("5   %s\n\n", new_file_name);
	}

}
```
  
#

- Bir örnek:

		const char *p = ""; //null string literal
		
		printf("%zu\n", strlen(p)); --> ekrana 0 yazar.
		
		printf("%zu\n", sizeof(p)); --> ekrana pointer değişkenin boyutu olan 4 yazar
		
		printf("%zu\n", sizeof("")); --> ekrana 1 yazdırılır.
		

- sizeof'a dair örnekler:


		const char*p = "taylan";
		
		printf("[1]%zu\n", sizeof(*p));
		//sizeof operatörü, operandı olan ifadenin türüne bakar.
		Bu türün sizof değerini üretir. Burda *p char bir tür olduğundan ekrana 1 yazdırılır.
		
		printf("[2]%zu\n", sizeof(*p));
		//sistemdeki pointer sizeof'u bizim derleyici için 4 tür.
		
		void func(const char* ptr)
		{
			printf("[3] %zu\n", sizeof(*ptr));
		}
		
		//yukarıdaki fonksiyon main fonksiyonundan func("mustafa") diye çağırılsın
		Yine ekrana char türünün değeri olan 1 yazdırılır.
		
		
		printf("%zu\n", sizeof(p++)); // 4 ekrana yazdırılır pointer türü
		
		printf("%zu\n", strlen(p));
		//sizeof operatörünün operantı olan ifadede işlem yapılmaz. p'nin değeri değişediği için strlen(p) değeri 6 olur.
		Eğer ++p; ayrı yazılsaydı 5 olurdu.
  
  
  - Karıştırılan tipik bir konu:


	sizeof                                          strlen

- bir operatör					- bir fonksiyon
- anahtar sözcük				- strlen (p) --> bir sabit ifadesi değil
- sizeof(str) --> bir sabit			- rentime'da çağırılıp geri dönüş değeri elde edilir.
- compile time'da değeri belli oluyor




		printf("%zu\n", strlen("ali")); //3
		- adresteki yazının uzunluğu

		printf("%zu\n", sizeof("ali")); // 4
		- Bu dizinin boyutu değerini compile time' da üretecek.

		printf("%zu\n", strlen("")); //yazının boyutunu yazdırdığı için 0 yazdırılır.
		
		printf("%zu\n", sizeof("")); //dizinin boyutunu yazdırdığı için 1 ekrana yazdırır. (\0)

#


		int a[sizeof("alican")]; //geçerli
		int b[strlen("alican")]; // hata, bir sabit ifadesi değildir.
		


**String Literalleriyle İlgili Teknik Detaylar

Hatırlatma: 

		int  a[10];
		printf("%zu\n", sizeof(a)); --> değeri 40 olur
		printf("zu\n", sizeof(&a[0]); --> değeri 4 olur.
		
		
#



		const char* p = "\x42URS\x41";
		puts(p); --> ekrana BURSA  yazdırılır.
		
- x42 gibi \x ile başlayan hex sayı sisteminde karaktere sabiti kullandığında hex sayı sisteminde
bir rakam belirttiği için derleyici bir yerden sonra hata verir.


		const char* p = "\x42babade";
		- karakter sınırı olmadığı için hata

- Ama octal karakter sabitinde 3 karakter sınırı vardır.

		const char* p = "\10235";
		\102 sayısı B harfi olarak algılandı sonrası ekrana normal sayı olarak yazdırıldı.
		ekrana B35 yazdırılmış oldu.
		
		
- \ karakteri, karakter sabitlerinin yazımında escape olarak kullanıldığı için string literali
 içerisinde ters bölü karakterinin kendisini kullanacaksınız \\ şeklinde yazılır.
  
  
  			puts(\\Rasit\\); --> \Rasit\ yazdırılır.
			puts("\"murat\""); --> "murat" yazdırılır.
			- çift tırnak içinde bu geçerlidir.
			
- Uzun string literallerinin birden fazla kod satıra yayılmasının 2 yolu vardır.

				puts("su anda bir hata olustu lutfen \
		devam etmek icin....");
		
- Yukarıdaki yöntemde ikinci stıra geçildiğinde, satıra en başından başlanmalıdır.
	- Genelde bu yol pek tercih edilmez.

			const char* p = "barıs";
			"burak"   "mete";
			puts(p); --> ekrana barısburakmete yazılır. 
			- Daha sık bu şekilde kullanılır.

Bir örnek:  

		
			printf("[1] kayit yenile\n"
			       "[2] kayit ara\n"
			       "[3] kayit sil\n"
			       "[4] kayit degistir\n");

# Pointer Arrays (Pointer Dizileri)

   	 int a = 10;
	 int b = 20; 
	 int c = 30;
	 
	 int* p[] = { &a, &b, &c };
  	 printf("%d\n", *p[0]); --> ekrana 10 yazdırılır.
	 

#

	int* p[] = { &a, &b, &c };
	
	for (int i = 0; i < 3; ++i) {
		printf("%d\n", *p[i]);
	} --Z ekrana a, b ve c nin değerleri yazdırıldı.
	
	**p = 777; yazarsak dizinin ilk elemanını 777 yapmış oluruz.
	
	**p = *p[0] = **(p + 0) dır.
	
	**p --> double indirection ya da double dereferencing 
	
	- ilk içerik operatörü bizi yine bir adres eriştirdiği için ikinci içerik operatörü ile o adresteki içeriğe erişiyoruz.
	
	
- Sentaksı anlamak için bir soru:

		int a[] = { 2, 4, 6, 8 };
		int b[] = { 1, 3, 5, 7 };
		int c[] = { 10, 20, 30 };
		
		int* p[] = { a, b, c };
		
		p[1][2] = 777;
		- [] operatörü soldan sağa öncelik yönüne sahip olduğu için p[1], p pointer dizisinin 1 indislii elemanını gösterir. 
		  Bu elemanda adres olduğu için bu adresteki dizinin 2. indisdeki elemanına 777 sayısı atanmış olur.
		  
		- Eğer yine yukarıdaki kodun devamı olarak ;
	 
 		++p[2];
		++*p[2]; // yazılırsa
		- ilk satırda p[2] ile c dizisinin adresine ulaşmış oluruz. C dizinin ilk adresini bir artırdığımızda 20 sayısının tutulduğu adrese ulaşmış
		 oluyoruz. *p[20] ile 20 sayısının adresinin içerik operatörü ile 20 sayısının kendisine ulaşmış oluyoruz. Bunu artırdığımızda 20 sayısı
		 21 oluyoruz.
		 
		 
  
  #
   		int a = 10; 
		int b = 20;
		int c = 40;
		
		int* p[100] = { &a, &b, &c };
		- Bu boyut tanımlanan içerikten fazla olduğu için geriye kalan elemanlara NULL pointer değeri verilir.
#

		int* const p[] = { &a, &b, &c };
		- dizinin elemanları const demektir. Bu dizinin elemanları hayatları boyunca aynı değeri tutacaklar.
		
		p[1] = &x; // hata olur.
		*p[1] = 88; // geçerlidir. b nesnesinin içeriği değiştirildi.
		
#

		const int* p[] = { &a, &b, &c };
		int const* p[] = { &a, &b, &c };
		
		int ival = *p[1]; // geçerli
		
		*p[1] = 99; // geçersizdir
		p[1] = &x; // geçerli
		
# Ders 37 - 30.04.2021
 
- Elemanları char* türünden olan bir dizi oluşturursam, bu dizinin elemanlarında mantıksal ilişki içindeki yazıların 
adreslerini tutabiliyor.

		const char* pmons[] = {
					"ocak", 
					"subat", 
					"mart",
					"nisan",
					"mayis",
					"haziran",
					"temmuz",
					"agustos",
					"eylul",
					"ekim",
					"kasım",
					"aralık" }; //yandaki dizi belirli bir süre tekrar tanımlanmadan kullanılacaktır.
					
- Dizinin içerisindekiler bildiğimiz string literalleridir. Yani bu yazılar derleyicinin oluşturduğu dizilerde
tutulacak. Ve bu dizinin adresleriyle de bu pointer dizisinin elemanlarına ilk değer vermiş oluyorum.
Biz bu pointer dizisini dolaşırsak  aslıdna bu pointer dizisinin elemanlarından bu yaızların adreslerini elde edebiliriz.
Dolayısıyla bu yazıları kullanabiliriz.
		
- Bu karşımıza çok sık çıkabilecek bir senaryodur.
		
		
		for (size_t i = 0; i < asize(pmons); ++i) 
			printf("%s   %zu\n",  pmons[i], strlen(pmons[i]));
			
- Eğer bir diziyi yukarıdaki gibi sabir bir sırayla kullanarak istiyorsak tanımlanma şekli şöyle olmalıdır.

		char* const pmons[] = { ... }; // gibi
		
- Eğer dizi yukarıdaki gibi tanımlanmazsa 	pmons[1] = "karabuk"; 
gibi kodlarla değiştirilebilir. Hata yoktur ama tanımlanan dizinin amacına göre sabit kalması istendiği taktirde uygulanmalıdır.

- Ayrıca string literalleri tanımlanırken 

		const char* pmons[} = { ... };
		
olarak tanımlanmalıdır. Çünkü string literallerinin içi değiştirilmeye çalışılmasın. Değiştirilmeye çalışıldığı
taktirde UB'ye yol açabilir. Tanımlanmadığını varsayarsak
		
		*pmons[0] = 'a'; gibi bir kod yazıldığında sentaks hatası olmaz ama UB olur.
		
- Bir önceki sayfadaki tanımlamanın devamı olarak

		int n;
		printf("yilin kacinci ayi: ");
		scanf("%d", &n);
		printf("yilin %d. ayi = %s\n", n, pmons[n - 1]);
		

  
  - rastgele bir ay elde etmek istersek:

		randomize();
		for(;;) {
			printf("%s", pmons[rand() % 12]);
			getchar();
		}

- Adresleriyle birlikte yazalım:

		for (int i = 0; i < 12; ++i) 
			 printf("%p   %s\n", pmons[i], pmons[i]);
		
  
- Çok kullanılan idiyomatik bir yapı: 

		char entry[40];
		printf("bir ay ismi giriniz:  \n");
		scanf("%s", entry);
		
		/**** 1. alternatif ****/
		
		int i;
		
		for (i = 0; i < 12; ++i)
			if (!strcmp(entry, pmons[i]))
				break;
			
  		if (i < 12)
			printf("%s yazisi %d. aydir.\n", pmons[i], i + 1);
		else 
			printf("%s yazisi bir ay değildir.\n");
			
  		/**** 2. alternatif ****/

		int i;

		for (i = 0; i < 12 && strcmp(entry, pmons[i]); ++i) 
			; // null satetement 

		if (i < 12)
			printf("%s  yilin %d. ayi \n", entry, i + 1);
		else
			printf("%s gecerli bir ay ismi degildir\n", entry);
	
  - Büyük - küçük harf uyumunu ortadan kaldırmak için _stricmp() fonsksiyonu kullanılır. Standard değildir.


  		const char* p[] = {
					"ocak", 
					"subat", 
					"mart",
					"nisan",
					"mayis",
					"haziran",
					"temmuz",
					"agustos",
					"eylul",
					"ekim",
					"kasım",
					"aralık" };
  
  	- Yukardaki dizi ay dizisi olarak değilde herhangi bir isimleri tutan rastgele yazı dizisi olarak varsayarak bir süre bu dizi 
  	üzerinden işlem yapacağız.
```
#define _CRT_SECURE_NO_WARNINGS

#include <stdio.h>
#include <time.h>
#include <stdlib.h>
#include <ctype.h>
#include <string.h>
#include "Rutility.h"

#define SIZE 100




int main()
{
	const char* p[] = {
					"ocak",
					"subat",
					"mart",
					"nisan",
					"mayis",
					"haziran",
					"temmuz",
					"agustos",
					"eylul",
					"ekim",
					"kasim",
					"aralik" };

	
	for (int i = 0; i < asize(p); ++i)
		printf("%c \n", *p[i]);
	
	printf("\n\n\n");

	for (int i = 0; i < asize(p); ++i)
		putchar(*p[i]), printf("\n");


	printf("\n\n\n");
	
	for (int i = 0; i < asize(p); ++i)
		printf("%c \n", p[i][0]);




}


```
  

#

- Bu yazıların son karakterleri yazdırılsın.
	
		for (int i = 0; i < asize(p); ++i)
			printf("%c \n", p[i][strlen(p[i]) - 1]);
			
  
  - Ekrana bir karakter girilsin. İçinde ekrana girilen karakterden olanlar yazılsın.
```
#define _CRT_SECURE_NO_WARNINGS

#include <stdio.h>
#include <time.h>
#include <stdlib.h>
#include <ctype.h>
#include <string.h>
#include "Rutility.h"

#define SIZE 100




int main()
{

	const char* p[] = {
					"ocak",
					"subat",
					"mart",
					"nisan",
					"mayis",
					"haziran",
					"temmuz",
					"agustos",
					"eylul",
					"ekim",
					"kasim",
					"aralik" };

	
	
	
	int c;
	printf("ekrana bir karakter giriniz:\n");
	scanf("%c", &c);

	for (size_t i = 0; i < asize(p); ++i) {
		if (strchr(p[i], c))
			printf("%s \n", p[i]);
	}


}

```

#
 - Ekrana karakterler girilsin. Bu karakterlerden herhangi birine sahip olanları ekrana yazdıran program:

```
#define _CRT_SECURE_NO_WARNINGS

#include <stdio.h>
#include <time.h>
#include <stdlib.h>
#include <ctype.h>
#include <string.h>
#include "Rutility.h"

#define SIZE 100

int main()
{

	const char* p[] = {
					"ocak",
					"subat",
					"mart",
					"nisan",
					"mayis",
					"haziran",
					"temmuz",
					"agustos",
					"eylul",
					"ekim",
					"kasim",
					"aralik" };

	
	
	
	char str[20];

	printf("karakterleri girin: \n");
	scanf("%s", str);

	for (size_t i = 0; i < asize(str); ++i) {
		if (strpbrk(p[i], str))
			printf("%s\n", p[i]);
	}
}

``` 
 
- İçinde ekrana girilen yazıyı içeren yazıları ekrana yazdıran program:

```
#define _CRT_SECURE_NO_WARNINGS

#include <stdio.h>
#include <time.h>
#include <stdlib.h>
#include <ctype.h>
#include <string.h>
#include "Rutility.h"

#define SIZE 100




int main()
{

	const char* p[] = {
					"ocak",
					"subat",
					"mart",
					"nisan",
					"mayis",
					"haziran",
					"temmuz",
					"agustos",
					"eylul",
					"ekim",
					"kasim",
					"aralik" };

	
	
	
	char str[20];

	printf("karakterleri girin: \n");
	scanf("%s", str);

	for (size_t i = 0; i < asize(str); ++i) {
		if (strstr(p[i], str))
			printf("%s\n", p[i]);
	}
}
```
 
- Ödev: yukarıdaki isimlerden bütün harfleri tek (unique) olan isimleri yazdırınız.

```
#define _CRT_SECURE_NO_WARNINGS

#include <stdio.h>
#include <time.h>
#include <stdlib.h>
#include <ctype.h>
#include <string.h>
#include "Rutility.h"

#define SIZE 100




int main()
{

	const char* p[] = {
					"ocak",
					"subat",
					"mart",
					"nisan",
					"mayis",
					"haziran",
					"temmuz",
					"agustos",
					"eylul",
					"ekim",
					"kasim",
					"aralik" };

	
	
	
	for (int i = 0; i < asize(p); ++i) {

		for (int j = 0; j < asize(p[i]); ++j) {
			char ch = p[i][j];
			
			if (strchr(p[i] + j + 1, ch))
				goto dontwrite;
			
		}
		printf("%s\n", p[i]);
	dontwrite:
		; //null statement

	}

	



}
```
 
 
- Dizinin içerisindeki string literallerini A'dan Z'ye sıralı şekilde düzenleyiniz.

```
#define _CRT_SECURE_NO_WARNINGS

#include <stdio.h>
#include <time.h>
#include <stdlib.h>
#include <ctype.h>
#include <string.h>
#include "Rutility.h"

#define SIZE 100




int main()
{

	const char* p[] = {
					"ocak",
					"subat",
					"mart",
					"nisan",
					"mayis",
					"haziran",
					"temmuz",
					"agustos",
					"eylul",
					"ekim",
					"kasim",
					"aralik" };

	
	for (size_t i = 0; i < asize(p) - 1; ++i) {
		for (size_t j = 0; j < asize(p) - 1 - i; ++j) {
			if (strcmp(p[j], p[j + 1]) > 0) {// B, A --> 66, 65
				const char* ptemp = p[j];
				p[j] = p[j + 1];
				p[j + 1] = ptemp;
			}
		}
	}

	for (size_t i = 0; i < asize(p); ++i)
		printf("%s \n", p[i]);

}
```
#

- Bir mülakat sorusu: Yazının kısa olan başta ve aynı uzunluktakiler de kendi içinde alfabetik sıralı olacak kodu yazınız.

```
#define _CRT_SECURE_NO_WARNINGS

#include <stdio.h>
#include <time.h>
#include <stdlib.h>
#include <ctype.h>
#include <string.h>
#include "Rutility.h"

#define SIZE 100




int main()
{

	const char* p[] = {
					"ocak",
					"subat",
					"mart",
					"nisan",
					"mayis",
					"haziran",
					"temmuz",
					"agustos",
					"eylul",
					"ekim",
					"kasim",
					"aralik" };

	
	for (size_t i = 0; i < asize(p) - 1; ++i) {
		for (size_t j = 0; j < asize(p) - 1 - i; ++j) {
			size_t len_1 = strlen(p[j]);
			size_t len_2 = strlen(p[j + 1]);

			if (len_1 > len_2 || (len_1 == len_2 && strcmp(p[j], p[j + 1]) > 0)){
				const char* ptemp = p[j];
				p[j] = p[j + 1];
				p[j + 1] = ptemp;
			}
		}
	}

	for (size_t i = 0; i < asize(p); ++i)
		printf("%s \n", p[i]);

}
```
  
  
  
  
  
  - Örnek bir hatalı yazım:
 
 		for (size_t i = 0; i < asize(p); ++i) {
			_strrev(p[i]);  // UB olur
			puts(p[i]);
  		}
		- Eğer dizi const olarak tanımlanmadıysa böyle bir kullanım string literalini değiştirme girişiminde bulunduğumuz
		için tanımsız davranış olur.
		
- Bir pointer dizinin son elemanı NULL pointer belirlenebilir. Bu döngülerde son değeri rahat bulmamızı sağlar.

		const char* p[] = { "abc", "def", NULL};
		int i = 0; 
		while (p[i] != NULL)
			printf("%s", p[i++]);
			

- Bir dizinin eleman sayısından az string literali olarak ilk değer verilirse geriye kalan elemanlar NULL pointer olur. Ve siz eğer
tüm diziyi dolaşı dereference etmeye çalışırsanız UB olur.

	const char* p[3] = { "ali", "ata", "bak" };
	for (int i = 0; i < 20; ++i)
	 	puts(p[i]); // UB
		

# Pointer to Pointer (Pointer gösteren pointerlar)

		int x = 10;
		int *ptr = &x;
		
		printf("&x = %p\n", &x);  //x'in adresi 
		printf("ptr = %p\n", ptr); // x'in adresi 
		printf("&x = %p\n", &ptr); // ptr'nin adresi
  
  #
  
  
  
  		T x; // T bir tür ve x'in türü T
 		&x; --> x'in adresinin türü (T*)
		
		T* p;  // p'nin türü (T*)
		&p;  // p'nin adresinin türü (T**)
  
  		T** ptp;  // ptp'nin türü (T**)
		&ptp;   // ptp'nin adresinin türü (T**)
  
  
  - Yani pointer değişkenlerin adresleri ayrı bir türdür.
  - Eğer siz bşr ptr pointer değişkenin adresini bir değişkende tutmak isterseniz

		int x = 10;
		int* ptr = &x; // pointer to int
		int** p = &ptr; //pointer to pointer to int
		int y = 20;
		*p = &y; // ptr artık y'yi gösteriyor.
		**p = 45; // yazdığımızda x'e 45 ataması yapmış oluyoruz (double direction, double dereferencing)
		++**p;  // x'i bir artır.
		
  
  
![image](https://user-images.githubusercontent.com/34141599/118786829-e0beb100-b89a-11eb-9a54-469ff69eb8ea.png)

  
  
  - Bir örnek:


		int a[] = { 5, 10, 15, 20, 30 };
		int* p = a;
		int** ptr = &p;

		++* ptr;  		// ++p yani p bir sonraki adresi göstermeye başladı.
		++** ptr;   		// p nin gösterdiği adresteki içeriği bir arttır.
		print_array(a, 5);	
		
- Nerelerde kullanıldığına dair bir örnek:

```
#define _CRT_SECURE_NO_WARNINGS

#include <stdio.h>
#include <time.h>
#include <stdlib.h>
#include <ctype.h>
#include <string.h>
#include "Rutility.h"

#define SIZE 100


int g;

void func(int** p)
{
	*p = &g;
}

int main()
{
	int* ptr;

	func(&ptr);

}


```
  


- Bir yerel pointer değişkeniniz varsa örneğin int* türden bu pointer değişkeni call by reference biçimiyle bir fonksiyona göndermeniz gerekiyorsa fonksiyonu 
pointer değişkenin adresiyle çağırmalısınız. Bu durumda da fonksiyonun parametre değişkeni pointer to pointer olacaktır.


```
#define _CRT_SECURE_NO_WARNINGS

#include <stdio.h>
#include <time.h>
#include <stdlib.h>
#include <ctype.h>
#include <string.h>
#include "Rutility.h"

#define SIZE 100


void pswap(int** ppval, int** ppnum)  //ppval = &pval, ppnum = &pnum
{
	int* ptemp = *ppval;  // *ppval = pval, *ppnum = pnum
	*ppval = *ppnum;
	*ppnum = ptemp;
}
void myswap(int* pval, int* pnum) //pval = &val, pnum = &num
{
	int temp = *pval;
	*pval = *pnum;
	*pnum = temp;
}

int main()
{
	int val = 5;
	int num = 10;

	int* pval = &val;
	int* pnum = &num;

	printf("*pval = %d, *pnum = %d \n", *pval, *pnum);


	pswap(&pval, &pnum);

	printf("*pval = %d, *pnum = %d ", *pval, *pnum);

	printf("\n\n");

	printf("val = %d, num = %d\n", val, num);

	myswap(&val, &num);

	printf("val = %d, num = %d", val, num);

}


```
  
  #
  
  		int x = 5;
  		int *ptr = &x;
  		func(ptr); // bu fonksiyon x'i değiştirir ancak ptr'yi değiştiremez
		func(&ptr); // bu fonksiyon hem x'i hem ptr'yi değiştirir.
  
```
#define _CRT_SECURE_NO_WARNINGS

#include <stdio.h>
#include <time.h>
#include <stdlib.h>
#include <ctype.h>
#include <string.h>
#include "Rutility.h"

#define SIZE 100

int g = 15;

void func(int* p) 
{
	*p = 9;  // x'in değeri değiştirildi
	p = &g;  /*ptr'nin değerini değiştirme girişiminde bulunuyor fakat burda ptr için hiç bir 
			 değişiklik yapılmıyor. yerel değişken olan p değiştiriliyor sadece */

}
void func2(int** p) // p = &ptr
{
	**p = 4;  // x'in değerini değiştird
	*p = &g;  // ptr'nin değerini değiştirdi
}

int main()
{
	int x = 5;


	int* ptr = &x;

	printf("x = %d,   ptr = %p\n", x, ptr);

	func(ptr); /* sadece x'i değiştirebilir. 
			   ptr'yi değiştiremez çünkü ptr'nin adresine sahip değil*/

	printf("x = %d,   ptr = %p\n", x, ptr);
	
	func2(&ptr); /*hem x'i hem ptr'yi değiştirebilir. 
				 Çünkü fonksiyon her ikisinin de adresine erişebiliyor.
				 */

	printf("x = %d,   ptr = %p, &g = %p\n", x, ptr, &g); 


}  
```
  
- Aşağıdaki fonksiyon ne yapıyor ?? 

```

void foo(int** p1, int** p2)
{
	int temp = **p1;
	**p1 = **p2;
	**p2 = temp;
}

int main()
{


	int x = 10;
	int y = 34;
	int* p = &x;
	int* q = &y;
	
	foo(&p, &q);

	printf("x = %d\n", x);
	printf("y = %d\n", y);

}
```
 - Yukarıdaki kod parçacığı x ile y'nin değerlerini yer değiştiriyor.




- Öyle bir fonksiyon tanımlansın ki,
 Bir tam sayı dizisinin hem en küçük hem de en büyük elemanlarının adreslerini çağıran koda iletsin.
 
 
 
 		void get_min_max(const int* pa, size_t size, int** pmin, int** pmax);
		
		- Bu fonksiyon çağırılırken 1. parametreye 1. dizinin adresi yazılacak, 2. parametreye dizinin boyutunu,
		3. parametreye int* türünden bir nesnenin adresi gönderilecek ki o adresi gönderilen pointer değişkene bu dizinin en 
		küçük elemanının adresini yazacağız 4. parametreye de bu dizinin en büyük elemanının adresi yazılacak.
		
  
```
#define _CRT_SECURE_NO_WARNINGS

#include <stdio.h>
#include <time.h>
#include <stdlib.h>
#include <ctype.h>
#include <string.h>
#include "Rutility.h"

#define SIZE 10


void get_min_max(const int* pa, size_t size, int** pmin, int** pmax)
{
	 *pmin = *pmax = (int*)pa;

	for (size_t i = 1; i < size; ++i) {
		if (pa[i] < **pmin)
			*pmin = (int*)(pa + i);
		if (pa[i] > **pmax)
			*pmax = (int*)(pa + i);
	}
}

int main()
{

	int a[SIZE];
	int* ptr_min;
	int* ptr_max;

	randomize();
	set_array_random(a, SIZE);
	print_array(a, SIZE);

	get_min_max(a, SIZE, &ptr_min, &ptr_max);

	printf("min = %d, max = %d \n", *ptr_min, *ptr_max);
	
	swap(ptr_min, ptr_max);

	print_array(a, SIZE);


}
```
 - get_min_max fonkisiyonuna yapılan çağrıda ptr_min ve ptr_max'in adreslerini Yani pointer değişkenlerin adreslerini gönderdim. 
 Ancak swap çağrısında ise ptr_min ve ptr_max ile swap fonksiyonuna dizinin en küçük ve en büyük elemanlarının adreslerini gönderdim.
 Dolayısı ile swap fonksiyonu ptr_min ve ptr_max'ı değil dizinin en küçük elemanıyla en büyük elemanını takas edecektir.
  
  - Bir pointer dizisini bir fonksiyona gönderip işlem yapmak istersek:


```
void print_names(char** p, size_t size)
{
	for (size_t i = 0; i < size; ++i)
	{
		printf("%s ", p[i]); //p = &p[0]
	} 

	/*alternatif olarak*/
	while (size--)
		printf("%s ", *p++);
}

int main()
{
	char* p[] = { "ali", "ata", "bak" };

	print_names(p, asize(p)); // p = &p[0]


}
```

- İsimleri sıralayan bir program:

```
#define _CRT_SECURE_NO_WARNINGS

#include <stdio.h>
#include <time.h>
#include <stdlib.h>
#include <ctype.h>
#include <string.h>
#include "Rutility.h"

#define SIZE 10

void pswap(char** p1, char** p2)
{
	char* ptemp = *p1;
	*p1 = *p2;
	*p2 = ptemp;
}
void sort_names(char** p, size_t size)
{
	for (size_t i = 0; i < size - 1; ++i) {
		for (size_t j = 0; j < size - 1 - i; ++j) {
			if (strcmp(p[j], p[j + 1]) > 0) {// B, A --> 66, 65 
				pswap(p + j, p + j + 1);
				// pswap(&p[j], &p[j + 1];
			}
		}
	}
}

void print_names(char** p, size_t size)
{
	for (size_t i = 0; i < size; ++i) {
		printf("%s ", p[i]);
	}
}
int main()
{
	char* p[] = { "zehra", "abdi", "hakki", "hekim", "burak", "zeytin" };

	sort_names(p, asize(p));
	
	print_names(p, asize(p));

}
```

- Pointer dizilerinin üstünde işlem yapan fonksiyonların parametrelerinin doğal olarak dizinin ilk elemanının adresini almasını istiyorsak fonksiyonumuzun
 parametresini pointer to pointer yapmalıyız. Çünkü sonuçta bir pointer nesne adresiyle çağırılacaktır.
  
  
  
  # Pointer to Pointer & const keyword
  
  - Hatırlatma:

		int x = 10;
		
		- int * const ptr = &x; --> const pointer
		  ptr = &y; --> hata
		  *ptr = 20; --> geçerli
		  
		- const int* ptr = &x; --> pointer to const
		  int const* ptr = &x; 
		  
		  *ptr = 20; --> hata
		  ptr = &y; --> geçerli
		  
		  
#

		int x = 10;
		int y = 20;
		int z = 30;
		
		int* p = &x;
		int* q = &y;
		
	      - int **const ptr = &p;
	        ptr = &q; --> hata
  		*ptr = &z; --> geçerli
		**ptr = 77; --> geçerli
		
	      - int *const* ptr = &p;
	      	ptr = &q; --> geçerli
		*ptr = &z; --> hata
		**ptr = 77; --> geçerli
		
	      - int const **ptr = &p;
	        const int **ptr = &p;
		ptr = &q; --> geçerli
		*ptr = &x; --> geçerli
		**ptr = 77; --> geçersiz
		
		
		
- Bir önceki yazılan programda fonksiyonları inceleyelim. 

		void print_names(char** pa, size_t size);
		
olarak tanımlanmıştı. Bu fonksiyon gelen diziyi sadece okuma amaçlı kullanacağı için const'u kullanım yerimiz:

		void print_names(char* const* pa, size_t size);

olacaktır. Çünkü * pa'ya atama yapmak demek dizinin elemanlarını değiştirmek demektir.

sort_names fonksiyonu ise dizideki yazılarda değişiklik yapacağı için herhangi bir const keyword'u kullanılmaz.


# Void Pointers

void is a type --> void bir türdür.

- Bir değişkenin türü void olamaz.

	void x; // geçersiz
	
- Elemanları void türden olan bir dizi de olamaz.

		void a[20]; // geçersiz
		
		sizeof(void);  // geçersiz
		
		bir tür istisnası
		
- Bir ifadenin türü void olabilir.

		int val = 10;
		(void)ival; --> void cast
		
- Siz eğer bir fonksiyonun geri dönüş değeri olduğu halde kullanmak istemiyorsanız ve derleyiciden "discard to return value" uyarısını almak 
 istemiyorsanız void cast kullanmalısınız.
 
 		int foo(int)
		{
			//codes
		}
		int main()
		{
			(void)foo(12);  // void cast
		}
  
 - Yukarıda siz hem derleyiciye hem de programı okuyan kişiye fonksiyonun geri dönüş değerini bilerek ve isterek kullanmadığınızdan bahsetmiş oluyorsunuz.


- Lojik yorumlamaya tabii tutulan yerde void bir tür kullanamazsınız. 

		void func(int);
		
		int main()
		{
			if (func(3)){  ---> hataaa
				//codes
			
			}
		}
  
  
  # Ders 38 Tarih 03 05 2021
  
  		int func(int);
	
		int main()
		{
			(void)func(12);
		}
	
	Yukarıda bir fonksiyon tanımında geri dönüş değeri olmasına rağmen void - cast ile bu geri 
	dönüş değerinin kullanılmayacağı belirtilmiştir.
	

		void func(int);
		
	Yukarıdaki fonksiyonun tanımına bakılarak bu fonksiyonun geri dönüş değerinin olmadığı 
	anlamına gelmez. Farklı yollarla iletiyor olabilir. Sadece return value' sı yoktur. 
	Bir değişkenin adresi aracılığıyla geri dönüş değeri gönderebileceği unutulmamalıdır.
	
- C dilinde C++'dan farklı olarak fonksiyon tanımında bir durum söz konusudur.

		void func();
		void func(void);
		
- Yukarıdaki iki tanım arasında bir fark vardır. C'de fonksiyon parametresi içerisine void 
yazıldığında fonksiyonun parametre değişkeninin olmadığı anlamına gelirken parantezin içerisi
boş bırakıldığında bu fonksiyonun parametrik yapısı hakkında bir bilgi verilmediği anlamına 
gelir. C++ da ise bu iki durum arasında bir fark yoktur. 


- Şimdi void ile yeni bir türden bahsedeceğiz. 
- Bir pointerın tanımında, void anahtar sözcüğünden sonra asterisk atomu gelirse, yeni bir tür ile 
 karşılaşmış oluyoruz. Bu türe void pointer türü diyoruz. (void*) türü. 
 
 		void* ptr;
		
- Buradaki fark ise ptr öyle bir pointer ki her türden nesnenin adresini tutabiliyor.
Yani ptr nesnesi yukarıdaki gibi tanımlandığında ptr nesnesine (int, double long vs.) türden nesnelerin adreslerini atayarak kullanabilirsiniz. 
Ancak önceki pointer tanımlamalarına baktığımızda pointer değişkeni tanımlarken biz bir tür belirtiyorduk ve bu pointer nesnesine sadece o türden nesneler atayabiliyorduk.


Yani adete void* türü bize diyor ki türün ne olursa olsun adresini tutabilirim ben sadece adres ile ilgileniyorum türünle ilgilenmiyorum. 

		int x = 10;
		char str[] = "ali";
		double dval = 2.3;

		void* ptr = &x;

		ptr = str;
		ptr = &dval;
		
		// Yukarıdaki atamalardan hepsi geçerlidir.

  
 - Void pointerın en dikkat edilmesi gereken nokta void pointerı dereference ederek bir nesneye
 ulaşıp o nesneye atama yapamazsınız. 
 
 		*ptr = 23; // sentaks hatasıdır.
		++ptr;  // sentaks hatası.
		
- Yani void pointer, pointer aritmetiğine tabi değildir.

- İki void pointer da birbirinden çıkartılamaz.

- Burada akıllara o zaman void pointer değişkeni l value expression mıdır sorusu gelebilir ancak
void ptr l value dur. Ancak onun gösterdiği nesneye erişim söz konusu değildir.

- Peki o zaman void pointerla neler yapabiliriz sorusuna cevaplar verelim:


		int x = 10; 
		
		void* vptr = &x; // bir nesnenin adresini ilk değer olarak verebiliriz.
		
		vptr = NULL; // NULL pointer atanabilir.
		
		if (vptr != NULL) // bir nesnenin NULL pointer olup olmadığı sorgulanabilir.
		if (vptr)
		
		if (vptr == &x)  // bir nesnenin adresine eşit olup olmadığı sınanabilir.
		
		
- C ile C++ arasında bir fark söz konusu:

		int x = 10;
		void* vptr = &x;
		int* iptr;
		
		iptr = vptr; // Bu koda C'de geçerli ve implicit tür dönüşümü gerçekleşirken
		// C++ dilinde void* türünden diğer adreslere örtülü tür dönüşümü geçerli değildir. type cast uygulanmalıdır.
		
- Ancak tabi ki C'de bu özellik olsa dahi tür dönüştürme operatörünün kullanılması daha elzemdir.

		iptr = (int*) vptr;
		
- Bizim tanışmadığımız bir kodlama şekli var.
- Generic programming , yani türden bağımsız programlama demek

- Mesela bizim tanımladığımız fonksiyonlar bir türe hizmet ediyor. 
- Ancak generic fonksiyonlar bu şekilde değil. Yani generic fonksiyonlar bütün türlere hizmet veriyor. Mesela print_array fonksiyonu generic bir fonksiyon olsaydı türü ne olursa olsun dizinin tüm elemanlarını yazdırabilecekti.

- Bir nesne veya nesneler dizisi üzerinde yapılacak bir çok işlem nesnenin türü bilinmeden de yapılabilir. 

- Mesela bir soru: C'nin imkanlarıyla öyle bir swap fonksiyonu yazın ki, iki int nesneyi de takas edebilsin, iki double nesneyi de veya iki int diziyi de takas edebilsin. 
		
		
  		void gswap(void* vpx, void* vpy, size_t sz)
		{
			char* px = vpx;
			char* py = vpy;
			
			while (sz--)
			{
			char temp = *px;
			*px++ = *py;
			*py++ = temp; 
			}
		}
		
	- Yukarıdaki fonksiyonda türden bağımsız olarak bellekte tutulan nesnenin byte larının değişimi yapıldı. Yalnız burada C++ diline göre derlersek sentaks hatası vardır. Çünkü tür dönüşümü implicit olarak yapılamaz(vpx ile px arasında).
	
  
```
  void gswap(void* vpx, void* vpy, size_t sz)
{
	char* px = (char*)vpx;
	char* py = (char*)vpy;

	while (sz--) {
		char temp = *px;
		*px++ = *py;
		*py++ = temp;
	}
}
int main()
{
	int x = 10, y = 20;

	gswap(&x, &y, sizeof(int));

	printf("x = %d, y = %d\n", x, y); // değişimin yapılacağı iki nesnenin türü aynı olmak zorunda.

	double dx = 34.76, dy = 68.23; 

	gswap(&dx, &dy, sizeof(double)); // değişimin yapılacağı iki nesnenin türü aynı olmak zorunda

	printf("dx = %f, dy = %f", dx, dy);

	int a[5] = { 1, 3, 5, 7, 9 };  
	int b[5] = { 2, 4, 6, 8, 10 }; // dizi boyutları aynı olmak zorunda

	gswap(a, b, sizeof a);


}


```
  
  
- Standart olan string.h başlık dosyası içerisinde alan generic fonksiyonlar:

	- memset
	- memcpy
	- memchr
	- memcmp


- memset, bir bellek bloğunun bütün byte larını bir tam sayı değeriyle doldurmak için kullandığımız bir fonksiyon:
	
		void* memset(void* vp, int val, size_t n)
	
	- İlk parametresi set edilecek bellek bloğunun adresini isteyen void pointer,
	- ikinci parametresi her bir byte a yazılacak tam sayı değeri
	- üçüncü parametresi de byte olarak bellek bloğunun büyüklüğü.
  
  - memset fonksiyonu ile bir diziyi sıfırlama

```
	int a[SIZE];
	randomize();
	set_array_random(a, SIZE);
	print_array(a, SIZE);

	memset(a, 0, sizeof(a));
	print_array(a, SIZE);
```
  
- Bir örnek daha

```
	int a[SIZE];
	randomize();
	set_array_random(a, SIZE);
	print_array(a, SIZE);

	int idx;
	int n;

	printf("Hangi indeksten baslanarak kac tane elemean sifirlanacak\n");
	scanf("%d%d", &idx, &n);


	memset(a + idx, 0, n * sizeof(int));
	print_array(a, SIZE);
```

- Char türünden bir örnek:


```
	char str[SIZE] = "NECATI ERGIN";

	memset(str + 2, '*', 2);

	puts(str)

```

- memset fonksiyonunu kendimiz yazarsak;

```
void* memset(void* vptr, int val, size_t size)
{
	char* p = (char*)vptr;

	while (size--)
		*p++ = (char)val;

	return vptr;
}
```

- memcpy, en sık çağırılan standard c fonksiyonlarından biridir.
- Bir bellek bloğunu bir yerden bir yere kopyalıyor. 

		void* memcpy(void* vpdest, const void *vpsource, size_t n);
		
	- Birinci parametre kopyalamanın yapılacağı yerin adresi.
	- Kaynak olarak kullanılacak bellek bloğunun adresi yani sadece okuma amaçlı olduğundan const anahtar sözcüğüyle birlikte.
	- Üçüncü parametre de kaç tane byte kopyalanacağıdır.

- Bir örnek:

```
	int a[SIZE];
	int b[SIZE];
	
	randomize();
	set_array_random(a, SIZE);
	print_array(a, SIZE);

	memcpy(b, a, sizeof(a));
	
	print_array(b, SIZE);
```

- Bir örnek daha

```
	int a[SIZE];
	int b[SIZE] = { 0 };
	
	randomize();
	set_array_random(a, SIZE);
	print_array(a, SIZE);

	int idx_a, idx_b, n;
	printf("a'nin hangi elemanindan baslanacak\n");
	scanf("%d", &idx_a);
	printf("b'nin hangi elemanindan baslanacak\n");
	scanf("%d", &idx_b);
	printf("kac tane eleman kopyalanacak\n");
	scanf("%d", &n);
	

	memcpy(b + idx_b, a + idx_a, n * sizeof(int));
	
	print_array(b, SIZE);

```

- memcpy fonksiyonunu kendimiz yazmak istersek:

```
void* mymemcpy(void* vpdest, const void* vpsource, size_t size)
{
	const char* psource = (const char*)vpsource;
	char* pdest = (char*)vpdest;

	while (size--)
		*pdest++ = *psource++;

	return vpdest;
}
```

- C dökümantasyonuna bakıldığında memcpy fonksiyonunun tanımında restrict anahtar sözcüğünü görüyoruz. Bu kelime ile derleyiciye şunun garantisi verilir. gönderilen iki nesnenin bellek bloğunun herhangi bir durumda kesişmediğinin garantisini vermiş oluruz. Herhangi bir kesişme durumunda UB olur.

- Bir örnek üzerinden bakalım:

		int a[100];
		
		memcpy(a + 20, a + 10, 20 * sizeof(int)); // UB
		
- Yukardaki örnekte görüldüğü üzere yazılan kodda kopyalanan bellek bloğunun kesiştiği görülmektedir.

		void* memcpy(void* restrict vpdest, const void* restrict vpsource, size_t n);
		
- Sıradaki fonksiyon olan memmove fonksiyonuna geldiğimizde, memmove fonksiyonunun restrict olmadığını görüyoruz. Yani bu bellek bloklarının ortak ara kesiti olsada doğru çalışma garantisi veriyor.

		void* memmove(void* vpdest, const void *vpsource, size_t n);
		
- memmove fonksiyonu ile kaydırma türü işlemler yapılmaktadır.

- örnek olarak yukarıdaki yazdığımız kod satırını memmove ile yazarsak;

		int a[100];
		
		memmove(a + 20, a + 10, 20 * sizeof(int));

- Biz bu overlapted olarak str fonksiyonunda dikkat edilmesi gerektiğini aşağıdaki şekilde kullanılmaması gerektiğinden bahsetmiştik.


		char str[100] = "something";
		
		strcpy(str + 2, str); // ub
		
		puts(str);
		
- Biz bunu güvenli bir şekilde kaydırmak isetersek memmove fonksiyonunu kullanabiliriz:

		char str[100] = "something";
		
		memmove(str + 2, str, strlen(str) + 1); // \0 karakter de kopyalandığı için + 1
		
		puts(str);
		
- Yukarıda bir yazıyı 2 indeks sağa kaydırma işlemi yapıldı.


- memmove fonksiyonunu kendimiz yaparsak;

```
void* mymemmove(void* vpdest, const void* vpsource, size_t n)
{
	char* pdest = (char*)vpdest;
	const char* psource = (const char*)vpsource;

	if (pdest < psource) {
		while (n--)
			*pdest++ = *psource++;
	}
	else {
		pdest += n;
		psource += n;
		while (n--)
			*--pdest = *--psource;
	}

	return vpdest;
}
```
- Yukarıda görüldüğü üzere bellek bloklarının çakışması durumunda kopyalama sondan başa doğru yapılmaktadır.



- memchr fonksiyonu ise bir bellek bloğunda bir byte arıyor.

		void* memchr(const void* vp, int val, size_t n);
	
	- Birinci parametre aramanın yapılacağı bellek bloğu.
	- İkinci parametre aranacak olan byte değeri
	- Üçüncü parametre ise aramanın yapılacağı boyut.

- Geri dönüş değeri ise aranan byte bulunduğunda bulunan byte'ın adresini döndürecek, eğer yoksa NULL pointer döndürecek.

- memchr fonksiyonunu öncelikle kendimiz yazalım:

		void* mymemchr(const void* vp, int val, size_t n) 
		{
			const char* p = (const char*)vp;
			
			while (n--) {
				if (*p == val)
					return (char*)p;
				++p;
			}
			
			return NULL;
		}
	
- strchr den farkı ne diye bir soru sorarsak, strchr yazıda bir karakter arıyor ve sonunda null karakter olduğuna güveniyor. Ancak memchr'de bir yazı olması söz konusu değildir.
  
 - Örnek üzerinde baktığımızda;

	char str[100] = "mehmet alican korkmaz";

- Yukarıdaki gibi bir yazı dizisi oluşturulduğunda siz ortadaki alican yazısında 'm' karakterini aramak için yapsanız bunu strchr ile uygulayamazsınız çünkü strchr ile alican yazısının ilk adresini gönderdiğinizde arama null karakteri görene kadar gerçekleşecek. Ancak memchr ile yaparsanız ilk adresi ve boyutu da ek olarak gönderdiğiniz için bu aramayı sağlıklı bir şekilde gerçekleştirip alican yazısında 'm' karakterinin olmadığı bilgisini elde edebilirsiniz.

- Bir örnekte inceleyelim:

```
char str[100] = "32759832446545465465465465487987987981321321658498e79q283749892387598723644652634409457320974281";

	char* p = (char*)memchr(str + 20 , '7', 20);

	if (p != NULL)
		printf("bulundu.. %d indiste", p - str);
	else
		printf("bulunamadi");
```

- Yukarıdaki örnekte 20. indisten başlanarak 20 karakter içerisinde 7 sayısının olup olmadığı arandı.



- Sıradaki fonksiyon memcmp.
- strcmp ile farkını unutmamak lazım. strcmp bir yazıyı karşılaştırıyor. memcmp bir bellek bloğunu karşılaştırıyor. 

	int memcmp(const void* vpx, const void* vpy, size_t n);
 
 - Yukarıdaki memcmp fonksiyonu ilk bellek bloğu büyükse eğer pozitif değer döndürüyor,
 - İkinci bellek bloğu büyükse eğer negatif değer döndürüyor.
 - Eğer eşitse 0 değerini döndürüyor.

- Burada dikkat edilmesi gereken nokta byte olarak karşılaştırma yapıldığı için değerlerin büyüklüğü konusunda bir karşılaştırılmamalıdır. Bu sizi yanıltabilir.

- Bir örnek;

		int a[SIZE] = { 1, 3, 5, 7, 9 };
		int b[SIZE] = { 1, 3, 5, 7, 9 };
		
		if (!memcmp(a, b, sizeof(a)))
			printf("evet iki dizi esit\n");
		else
			printf("hayir iki dizi esit degil\n");
			
			

- Şimdi fonksiyonu kendimiz bir yazalım ki fonksiyonun işlevini daha iyi anlayabilelim:

```
int mymemcmp(const void* vpx, const void* vpy, size_t n)
{
	const unsigned char* px = vpx;
	const unsigned char* py = vpy;

	while (n--) {
		if (*px != *py)
			return *px > *py ? 1 : -1;
		++px;
		++py;
	}

	return 0;
}

```
 
- Yukarıdaki fonksiyonda diğer fonksiyonlardan farklı olarak neden unsigned char kullanıldı diye soracak olursak byte olarak karşılaştırma yapıldığı için işaretli olduğu düşünülürse eğer, işaret biti de devreye girecektir bu sebeple bir byte olarak karşılaştırma söz konusu olduğunda işaretsiz türler kullanılmalıdır.

- Mesela strcmp ile memcmp nin farkını anlayabilmemiz için elimizde iki farklı yazının olduğunu varsayalım. Bu iki yazıdan birinci yazının 5. 6. 7. karakterleri ile, ikinci yazının 3. 4. 5. karakterlerini karşılaştırma şansınız strcmp de yokken memcmp de vardır.

		if (!memcmp(s1 + 4, s2 + 2, 3))
			//code

- Yukarıda ki karşılaştırmayı bahsettiğimiz gibi strcmp ile yapmaya çalışırsak eğer str cmp yazının sonuna kadar olan kısmı ele alacağı için yani null karakter görene kadar, yukarıdaki karşılaştırmayı strcmp ile gerçekleştiremezsiniz.



- Acaba türden bağımsız olarak bir diziyi reverse eden bir fonksiyon yazabilir miyiz??
	- Eğer dizinin başlangıç adresini, sizeof değerini ve dizinin boyutunu bilirsek yazabiliriz.

- Generic bir reverse algoritmasıyla oluşturulmuş fonksiyon:

```
//vp: reverse edilecek dizinin adresi
//size: reverse edilecek dizinin boyutu
//sz: reverse edilecek dizinin sizeof u

void gereverse(void* vptr, size_t size, size_t sz)
{
	char* p = (char*)vptr;

	for (size_t i = 0; i < size / 2; ++i) {
		gswap(p + i * sz, p + (size - 1 - i) * sz, sz);
	}

}

int main()
{
	int a[] = { 0, 2, 4, 6, 8 };
	double b[] = { 1.1, 2.2, 3.3, 4.4, 5.5, 6.6 };

	gereverse(a, asize(a), sizeof(int));
	gereverse(b, asize(b), sizeof(double));

	print_array(a, asize(a));

	for (size_t i = 0; i < asize(b); ++i) {
		printf("%f ", b[i]);
	}

}

```

- Generic reverse fonksiyonun farklı bir yazım şekli;

```
void gereverse(void* vp, size_t size, size_t sz)
{
	char* ps = (char*)vp;
	char* pe = ps + (size - 1) * sz;

	while (ps != pe) {
		gswap(ps, pe, sz);
		ps += sz;
		pe -= sz;
	}
}
```

- Peki biz her generic fonksiyon tanımında void pointer kullanıp byte'sal işlem yaptığımız için char türüne dönüştürüyoruz. Direk olarak fonksiyon tanımlanırken neden char türünde tanımlamıyoruz??

- Bu sorunun cevabı şu şekilde;
	
	- C' ye void pointerlar standartlaştırma sürecinde eklendi. Yoksa geleneksel C de void pointerlar yoktu. Void pointer ın olmadığı dönemde zaten direk olarak char türünde tanımlamalarla generic fonksiyonlar oluşturuluyordu. Ancak siz bir fonksiyonun parametresini char* yaptığınızda, bu fonksiyonun bildirimini okuyan kişinin bu fonksiyonun char yazı türünde bir işlem mi yaptığı yoksa char dizi üzerinde işlem yapan bir fonksiyon mu yoksa generic bir fonksiyon mu olduğu konusunda kafa karıştırıyor. 
			
			void func(char* vpi, size_t n);
			
			int main() 
			{
				int a[100];
				func(a);
			}
			
	- Ayrıca yukarıdaki gibi bir fonksiyon çağrısı yapıldığında c++ da hata verir, C'de uyarı verir. Bu fonksiyonu çağıracak olan kişi de bir yerlerde yanlış yaptığını düşünebilir.
	- Yani void pointerlar tamamen semantik bir yapı. Yani fonksiyonun daha iyi anlaşılabilmesi için kullanılan bir türdür void pointerlar. Yoksa zaten işin arka planında byte'sal işlem döndüğü için char* türü kullanılmalıdır.



- Bir dizide arama yapan fonksiyonu generic olarak nasıl oluşturabiliriz birlikte inceleyelim:

```
void* gesearch(const void* vpa, size_t size, size_t sz, const void* vpkey)
{
	const char* p = (const char*)vpa;

	for (size_t i = 0; i < size; ++i) {
		if (!memcmp(p + i * sz, vpkey, sz)) {
			return (char*)(p + i * sz);
		}
	}

	return NULL;

}

```
- Yukarıdaki arama algoriması fonksiyonun tanımı yapıldı. Birinci parametre arama yapılacak diziyi, ikinci parametre arama yapılacak dizinin boyutunu, üçüncü parametre dizi türünün sizeof değeri, dördüncü parametre ise arama yapılacak nesnenin adresini (yani bellek bloğunu) içermektedir.  Burada bellek bloğu alınmasının sebebi memcmp fonksiyonunun kullanılacak olmasıdır. 
- İlk olarak dizinin başlangıç adresi char* türüne dönüştürülüyor. 
- Dizinin i indisli elemanının adresi : p + i * sz
- Karşılaştırma yapılacak nesnenin adresi vpkey
- İki bellek bloğunun eşitliği memcmp fonksiyonu ile sınanıyor. 
- Ve bunun sonucunda eğer aranan değer bulunursa dizide bulunduğu adres döndürülüyor. Eğer bulunamazsa da NULL pointer döndürülüyor.

- Tüm program aşağıda yer almaktadır:

```
#define SIZE 20
void* gsearch(const void* vptr, size_t size, size_t sz, const void* vpkey)
{
	const char* p = (char*)vptr;

	for (size_t i = 0; i < size; ++i) {
		if (!memcmp(p + i * sz, vpkey, sz))
			return (char*)(p + i * sz);
	}

	return NULL;
}

int main()
{
	int a[SIZE];
	int ival;

	randomize();
	set_array_random(a, SIZE);
	print_array(a, SIZE);

	printf("Aranacak degeri giriniz: \n");
	scanf("%d", &ival);

	int* pival = (int*)gsearch(a, SIZE, sizeof(int), &ival);

	if (pival)
		printf("bulundu.... aranan deger %d indisli elemanda.", pival - a);
	else
		printf("bulunamadi...");


}

```

- gsearch fonksiyonun bir farklı yazım biçimi:

```
void* gsearch(const void* vptr, size_t size, size_t sz, const void* vpkey)
{
	const char* p = (const char*)vptr;

	while (size--) {
		if (!memcmp(p, vpkey, sz))
			return (char*)p;

		p += sz;
	}

	return NULL;
}
````

#


- Yukarıdaki döngüde her döngü adımında p pointer ı sz kadar artırıldığında bir sonraki nesnenin ilk byte'ına geçilmiş olur. 
Ve memcmp ile biz bellek bloğu karşılaştırması yaptığımız için nesneler arası geçişi byte sal olarak bu idiyomla yapıyoruz.


- Türden bağımsız olarak bir diziyi küçükten büyüğe doğru sıralayan bir fonksiyon yazılabilir mi??

	- Bu sorunun iki cevabı var hem yazılabilir hem de yazılamaz. 
	- Şimdiye kadar öğrendiğimiz bilgilerle yazamayız.
	- Neden yazamayıza geldiğimizde, dizinin iki elemanını takas etmede herhangi bir problem yok. 
	ancak birbirine göre büyüklük sorusunun nasıl sorabiliriz. Biz bunların türünü bilmiyoruz. memcmp fonksiyonu ile büyüklük karşılaştırması yapamayız. memcmp bu sayıların türünü bilmiyor. Dizinin elemanlarının türünü bilmeden karşılaştırma yapamam. Bu olay memcmp deki byte karşılaştırmasından çok farklı bir olay. 
	- Ancak böyle bir sıralama yapan generic fonksiyon standart kütüphanede mevcuttur. İsmi qsort olan fonksiyon generic bir sıralama fonksiyonudur. Bunu nasıl yaptığına gelecek olursak., çağıran koddan bir fonksiyon istiyor, dizinin iki elemanının karşılaştırılması için bu gönderilen fonksiyon kullanılır. Yani siz bir fonksiyon ile bir fonksiyona, bir fonksiyon gönderiyorsunuz. Bu yapıyı oluşturmak için fonksiyon pointerları yapısını öğreneceğiz. 
		
  # Ders 39 Tarih 05 05 2021
  
  - Dizi üzerinde yapılan işlemlerden birisi de "fill" doldurma. Fill, bir veri yapısını belirli
  bir değerle set etmedir.
  
  
```
  
void* fill_array(void* vp, size_t size, size_t sz, const void* vpval)
{
	char* p = (char*)vp;

	while (size--) {
		memcpy(p, vpval, sz);
		p += sz;
	}

	return vp;
}

int main()
{
	int a[SIZE];
	int x;
	printf("bir tamsayi giriniz: ");
	scanf("%d", &x);

	fill_array(a, SIZE, sizeof(int), &x);

	print_array(a, SIZE);

	double da[SIZE];
	double dval;
	printf("bir gercek sayi giriniz:  ");
	scanf("%lf", &dval);

	fill_array(da, SIZE, sizeof(double), &dval);

	for (int i = 0; i < SIZE; ++i) {
		printf("%lf ", da[i]);
	}
}
```

- Bir void* türünü gösterecek pointera ihtiyacınız var ise void** türü kullanılır.


		int x = 10;
		double dval 3.4;
		
		void* vptr;
		
		void** vp = &vptr;
		*vp = &dval; // vptr nin içerisinde dval in adresi atandı.
		
		**vp = 10; // geçersizdir. Daha önce de dediğimiz gibi bir void* türü pointerı 
		dereference ederek içeriğini değiştiremeyiz.
  
 - Örnek olarak;

		void func(int x, int y, void** vptr);
		
- Yukarıdaki gibi bir fonksiyon tanımı gördüğünüzde 3. parametrede bir void* türden pointerın
 adresi istendiğini ve bu adrese bir void* türünden bir nesnenin adresi yazılacağını anlıyoruz.
 
 
 		void a[]; // yandaki gibi bir dizinin olması söz konusu değilken
		void* a[]; // yandaki gibi bir dizi olması söz konusudur.
		
		void* a[] = { &x, &dval }; // gibi farklı türlerin adresleriyle ilk değer verilebilir.
		
		
		
  # Function Pointer (Foksiyon Pointerları)
  
  - C dilinde pointerlar ikiye ayrılıyor. Birisi nesne adresleri (object pointers) iken, diğeri fonksiyon adresleri
  (function pointers).
  - Bir nesnenin adresi dediğimizde programın çalışması esnasında o nesnenin bellekte nerede tutultuğunun adresidir.
  - Fonksiyon adresi dediğimizde ise, fonksiyonların kodunun çalışması için makine komutlarına ihtiyacımız var. O
  makine komutlarının da belleğe yüklenmesi gerekiyor. İşte o makine komutlarının belleğe yüklendiği adres de fonksiyonun adresi gibi görülebilir. Dolayısıyla bir fonksiyonun adresi elinizdeyse oradaki komutları 
  çalıştırabilirsiniz. 
  
  - Bir fonksiyonun adresini nasıl elde ediyoruz. 
  	 - fonksiyonun ismini adres operatörünün operandı yaptığınızda elde edersiniz.
  
  		int func(int);
		
		int main()
		{
			&func; // ifadesi func fonksiyonun adresi anlamına geliyor.
		}
		
	- İkinci bir yolu daha mevcut.
		- Nasıl bir dizinin ismi bir ifade içinde kullanıldığında dizinin ilk elemanının adresine 
		dönüştürülüyorsa (array decay), bir fonksiyon ismi de bir ifade içinde kullanıldığında o fonksiyonun
		adresine dönüştürülür. (function to pointer conversion).
		
				&func // func ın adresi
				func // bu da func ın adresidir.
				
	- Her ifadenin bir türü vardır.
	
			&func // fonksiyon adresinin de bir türü vardır. 
			// int (*)(int, ...) // fonksiyonların türlerinin sentaks yapısı yanda gösterilmiştir.
  			// return val (* pointer olduğunu gösteriyor)  (parametre değişkenlerinin türleri)
			
  	- Örnek olarak;

			double foo(double, double); 
			
			int main()
			{
				&foo; // ifadesinin türü: double (*) (double, double) --- olur.
			}
  
  
 
  - Yani fonksiyon adresi türü diye tam olarak tek bir tür yok. Fonksiyon adresleri geri dönüş değeri ve 
  parametrelerin türü ile ilişkilidir. 
  
  - Mesela strcmp fonksiyonun adresinin türüne bakalım:

		&strcmp; // int (*)(const char*, const char*) --- olur.  
		&strlen; // size_t (*)(const char*) -- olur.
  		&isalpha; // int (*)(int) -- olur. 
  
  - Nasıl nesnelerin adreslerini tutan değişkenler oluşturabiliyorsak, fonksiyonların adreslerini tutan değişkenler 
  de oluşturabiliyoruz. İşte böyle nesnelere fonksiyon pointerları diyoruz.
  
  		int foo(int);
		int func(int);
		int main()
		{
			int (*fp)(int) = &foo; // yandaki fp fonskiyon pointer değişkenidir. ilk değer olarak
						// foo nun adresi verilmiş.
						
			fp = &func;    // Burada ise fp fonksiyon pointerına func değişkeninin adresini atamış oluyoruz.
		}
		
- Yukarıdaki bildirimi yaparken & operatörünü kullanmadan da yapabilirdik.

		int foo(int);
		
		int main()
		{
			int (*fp)(int) = foo;  // burada da adres operatörü(&) kullanmadan ilk değer verildi.
		}
  
  	
  		
  - strcmp fonksiyonun adresiyle ismi fp olacak olan değişkene ilk değer verelim.

		int (*fp)(const char*, const char*) = &strcmp;
		int (*fp) (const char*, const char*) = strcmp;
		
  - strlen fonksiyonunu fp isimle fonksiyon pointerıyla ilk değer verelim.

		size_t (*fp)(const char*) = strlen;
		
- Bizim tanımlamış olduğumuz print_array fonksiyonunun adresiyle ilk değer verelim.

		void (*fpx)(const int*, size_t) = &print_array;
		

  #
  
  
  		void func(int x)
		{
			printf(func fonksiyonu cagirildi. x = %d\n", x);
		}
		
		int main()
		{
			func(10);
		}
		
  - Yukarıda bir fonksiyon çağırıldı.
  Fonksiyon çağrı operatörü ( ) , operatör öncelik tablosunda birinci sıradaydı. Peki fonksiyon çağrısının 
  sentaksına bakacak olursak;
  
  		adres(varsa argümanlar) // gördüğünüz üzere fonksiyon isminin olduğu kısım aslında bir adrestir.
		
- Yani yukarıdaki func fonksiyonunu aşağıdaki şekilde de çağırabilirsiniz;

		(&func)(10);
		
- Madem ki bir fonksiyon pointerı, fonksiyonun adresini belirtiyor, o halde çağrı operatörünün operantı da fonksiyon pointerı olabilir. 
 
 
 		 void func(int x)
		{
			printf(func fonksiyonu cagirildi. x = %d\n", x);
		}
		
		int main()
		{
			void (*fptr)(int) = &func;
			
			fptr(10);
		}
  
  
  - Yukarıda gördüğünüz üzere bir fonksiyonu çağırmanın bir başka yolu, bir fonksiyon pointer değişkenini, fonksiyon
  çağrı operatörünün operantı yapmaktır.
  
  
 		void f1(void)
		{
			printf("f1 cagirildi.\n");
		}

		void f2(void)
		{
			printf("f2 cagirildi.\n");
		}

		int main()
		{
			void (*fp)(void);

			fp = f1;
			fp();
			fp = &f2;
			fp();
		}
  
  - Yukarıda gördüğünüz gibi bir değişken ismiyle farklı fonksiyonları çağırma işlemi gerçekleşmiştir.
Ancak dikkat edilmesi gereken nokta fonksiyon pointerının türüyle, fonksiyonun türü kesinlikle uyuşmalıdır.
uyuşmaması durumunda  C'de yanlış ve C++ 'da sentaks hatasıdır.


- Peki biz pointerlarda içerik operatörünü kullanarak içeriğe erişebiliyorken fonksiyon pointerında bu içerik
operatörüyle ne yapabiliriz? Bu sorunun cevabı olarak fonksiyon çağrısının başka bir biçimi ortaya çıkıyor.


		
  
  		void f(void)
		{
			printf("f cagirildi.\n");
		}

		int main()
		{
			void (*fp)(void) = func;
			
			fp();
			(*fp)(); /* ikinci çağırma şekli.
				    ikinci kullanım oldukça yaygındır bunun sebebi pointer olduğunu 
				    okuyan programcıya belirtmektir. */
		}

- Bildiğimiz üzere pointer değişkenlerinin sizeof'u aynıydı ve sistem den sisteme göre değişebilmekteydi. 
(int*, double*) gibi türlerin benim sistemimde storage'ı 4 byte'tır.

- Fonksiyon pointerlarının da sisteme bağlı olarak değişebilmekle birlikte benim sistemimde 4 byte 
olmasına karşın normal pointerlarla aynı storage değerine sahip olacağı garantisi verilemez. 
  
  
- Tüm object pointers sizeof değeri aynıdır.
- Tüm function pointers sizeof değeri aynıdır.
- object pointer sizeof değeri ile function pointer sizeof değeri aynı olmayabilir.
  
  
  
- Fonksiyon pointerlarının en çok kullanıldığı yer fonksiyonların parametre değişkeni olması.
  
  
  		void func(void (*f)(void)); // yandaki fonksiyon bildiriminde, paremetre değişkeninin bir fonksiyon pointerı olarak tanımlandığını görüyoruz.
		
		 
  #
  
  		void func(void (*f)(void))
		{
			//code
		}
		
		void f1(void)
		{
			//code
		}
		
		int main()
		{
			func(&f1);  // f1 fonksiyonu func fonksiyonuna parametre değişkeni olarak gönderildi.
			func(f1);
		}
		
- Yukarıda gördüğünüz üzere bir fonksiyona, bir fonksiyonun adresinin gönderilmesi işlemi gerçekleşmiştir.

- Yukarıda gördüğümüz fonksiyon çağrısında gönderilen fonksiyona  *callback fonksiyonu deniyor. 
  
  
  		func(&f1); // burada f1 bir callback'tir.
		

  
  
  
  - Konuyu çok daha iyi anlamamız için bir örnek;

```

void print_chars(const char* fname, int (*fp)(int))
{
	puts(fname);

	for (int i = 0; i < 128; ++i) {
		if ((*fp)(i))
			printf("%c ", i);
	}

	printf("\n\n");
}

int main()
{
	print_chars("isupper", isupper);  // function convertion kuralı uygulandı.
	print_chars("islower", &islower); // fonksiyon adresiyle gönderildi.
	print_chars("isdigit", &isdigit);
	print_chars("ispunct", &ispunct);
}

```
  

 - Şimdi bir func fonksiyonu tanımlanmış olsun. func fonksiyonunu çağırdığımda default olarak a fonksiyonunu 
 çağırsın. Ben bu func fonksiyonundan a fonksiyonunu değil de b fonksiyonunu çağırmak istersem nasıl bir yol 
 izlemeliyim. (çok sık kullanılan bir C idiyomatik bir yapısıdır.)
 
  
  
  		void a(void)
		{
			printf("a fonksiyonu cagirildi\n");
		}
		
		void b(void)
		{
			printf("b fonksiyonu cagirildi\n");
		}
		
		void (*gfptr)(void) = &a;   /* func fonksiyonun içerisinde default olarak a fonksiyonu çağırılması
					     için global bir fonksiyon pointerı tanımlandı. Böyle global bir
					     fonksiyon pointer ı kullanılmasının sebebi ise  a fonksiyonunu 
					     değiştirerek farklı bir fonksiyon çağırılmasını sağlamaktır.   */
  		
		void func(void)
		{
			gfptr(); /* gfptr global fonksiyon değişkeni kullanılarak ilk a fonksiyonu çağırılıyor.
				 ana kodda sonrasında bu a fonksiyonu değiştirilip b fonksiyonu çağırılacak*/
		}
		
		void set_func(void (*fp)(void))  
		{
			gfptr = fp;  /* görüldüğü üzere bu default a değerinin değiştirilebilmesi için bir set 
				     fonksiyonu kullanıldı. Bu fonksiyonun parametresi de bir fonksiyon pointerı.
				     Yani siz bir fonksiyonun adresini gönderdiğinizde default olarak çağırılacak 
				     olan a fonksiyonunu değiştirmiş oluyorsunuz ve adresi girilen fonksiyon 
				     çağırılmış olacak.
		}
  		
		int main()
		{
			func();   // default olarak a fonksiyonu çağırıldı.
			set_func(&b);  // a fonksiyonunu tutan global fonksiyon pointerı, set fonksiyonu ile değiştirildi.
			func(); // şuan da ise b fonksiyonu çağırıldı. 
		}
		
		
		
  - Yukarıda ayrıca set fonksiyonu kullanılmasının sebebi standart fonksiyonlarda siz tanımlanan global değişkeni
  görmeden set fonksiyonu ile bu global değişkeni değiştireceksiniz. 
  
  
  - Daha önce qsort fonksiyonun, fonksiyon pointerları ile tanımlandığını bu konudan sonra anlatılacağından bahsetmiştik.
	- qsort bir sıralama ilişkisiyle bir fonksiyonu sıralıyor fakat generic bir fonksiyondur kendisi.
	Yani qsort fonksiyonu ile türden bağımsız bir sıralama söz konusudur.
	
		void qsort(void *vpa, size_t size, size_t sz, int (*fp) (const void*, const void*));
  
  	- Geri dönüş değeri void olan bir fonksiyon.
  	- ilk parametresi sıralamanın yapılacağı dizinin adresini içeriyor.
  	- İkinci parametresi dizinin boyutu
  	- Sıralanacak dizinin bir ögesinin sizeof değeri
  	- Sıralanacak dizinin iki elemanının karşılaştırılması amacıyla kullanılacak olan fonksiyonun adresi olan function pointer;
  		- Fakat geri dönüş değeri int olan ve parametre değişkenleri const void* olan iki adet değişken.
  
  		
  #
  
  - Aşağıda kullanım şekline bir örnek verilmiştir.

```

	//qsort icmp fonksiyonuna neyle çağrı yapacak
	//dizinin 2 elemanının adresleriyle (yani 2 elemanın bellek bloklarıyla)

	int icmp(const void* vpx, const void* vpy)
	{
	if (*(const int*)vpx > *(const int*)vpy)
		return 1;
	if (*(const int*)vpx < *(const int*)vpy)
		return - 1;

	return 0;
	
	}



int main()
{
	int a[SIZE];

	randomize();
	set_array_random(a, SIZE);
	print_array(a, SIZE);

	qsort(a, SIZE, sizeof(int), &icmp);
	
	print_array(a, SIZE);
}
```

- Yukarıdaki program parçacığında qsort fonksiyonu ile dizi küçükten büyüğe sıralandı.

#

- Daha iyi anlaşılması için double türü kullanılarak bir örnek:

 ```
 
int dcmp(const void* vpx, const void* vpy)
{
	double x = *(const double*)vpx;
	double y = *(const double*)vpy;

	return x > y ? 1 : x < y ? -1 : 0;
}

int main()
{
	double a[] = { 3.4, 1.1, 0.7, 6.8, 0.98, 2.45, 5.6, -1.2, 3.33 };

	qsort(a, asize(a), sizeof(double), &dcmp); //dcmp callback olarak kullanıldı.

	for (int i = 0; i < asize(a); ++i) {
		printf("%lf ", a[i]);
	}
}

```
  
 - int türlerde aşağıdaki gibi idiyomatik bir yapı mevcut.

		int icmp(const void* vpx, const void* vpy)
		{	
			return *(const int*) vpx - *(const int*)vpy;
		}
		
- Ancak yukarıdaki kullanım söz konusu olduğunda karşımıza taşma durumuyla UB olarak çıkabilir.
Bu yüzden bu idiyom taşmanın olmayacağının garantisini verebileceğiniz durumlarda kullanılması gerekmektedir.


- Şimdi sırada qsort fonksiyonunun benzerini kendimiz yazalım (yalnız bizim fonksiyonumuz bubblesort algoritmasını kullanıcak):

```
int icmp(const void* vpx, const void* vpy)
{
	if (*(const int*)vpx > *(const int*)vpy)
		return 1;
	if (*(const int*)vpx < *(const int*)vpy)
		return -1;

	return 0;

}

void gbsort(void* vpa, size_t size, size_t sz, int(*fp) (const void*, const void*))
{
	char* p = (char*)vpa;

	for (size_t i = 0; i < size - 1; ++i) {
		for (size_t j = 0; j < size - 1 - i; ++j) {
			if (fp(p + j * sz, p + (j + 1) * sz) > 0) {
				gswap(p + j * sz, p + (j + 1) * sz, sz);
			}
		}
	}
}

int main()
{
	int a[SIZE];

	randomize();
	set_array_random(a, SIZE);
	print_array(a, SIZE); 

	gbsort(a, SIZE, sizeof(int), &icmp);

	print_array(a, SIZE);
}
```


- Bir dizinin elemanlarını yazdıran bir generic bir fonksiyon yazalım:

```
void gprint(const void* vpa, size_t size, size_t sz, void (*fpa)(const void*))
{
	const char* p = (const char*)vpa;

	while (size--) {
		fpa(p);
		p += sz;
	}
	printf("\n\n");
}

void iprint(const void* vpa)
{
	printf("%3d ", *(const int*)vpa);
}

void dprint(const void* vpa)
{
	printf("%3f ", *(const double*)vpa);
}

int main()
{
	int a[SIZE];

	randomize();
	set_array_random(a, SIZE);
	print_array(a, SIZE);

	gprint(a, SIZE, sizeof(int), &iprint);

	double b[3] = { 2.4, 3.5, 5.6 };

	gprint(b, 3, sizeof(double), &dprint);

}

```


# Fonksiyon Göstericileri ve typedef bildirimleri

		//Bir fonksiyonun adres türü ile bir fonksiyon pointer ı tanımlansın.
		
			int (*fp)(const void*, const void*);
		
		// şimdi fp'nin adresiyle ilk değerini alan fptr değişkeni tanımlayın.
		// yani pointer to function pointer
		
			int (**fptr)(const void*, const void*) = &fp;
		
		// elemanları fp gibi olan 10 elemanlı bir dizi tanımlayınız. fa
		
			int (*fa[10])(const void*, const void*);
	
		// şimdi öyle bir fonksiyon bildirelim ki, fonksiyon parametresi fp gibi bir pointer olsun.
		
			void f1(int (*fp)(const void*, const void*));
		
		// bu tanımlanan fonksiyonun 2 adet fp gibi pointer a sahip parametresi olsaydı
		
			void f2(int (*fpx)(const void*, const void*), int (*fpy)(const void*, const void*));
			
		// peki ya fonksiyonun geri dönüş değeri de böyle bir pointer olduğunu düşünelim;
		//Bu durumda bildirim çok daha farklı bir hal alıyor. Fonksiyon ismi f3, ilk parametrenin ismi fpx, ikinci parametrenin ismi fpy.
		
		int(* f3(int (*fpx)(const void*, const void*), int (*fpy)(const void*, const void*)))(ccnst void*, const void*);
		
		
- Yukarıda gördüğünüz durum sıkça karşımıza çıkabilecek bir durum olduğu için ve hem yazması hem okunması zor olduğu için tipik olarak typedef bildirimi kullanılır.

- Şimdi typedef de temel kural, hangi türe eş isim vermek istiyorsak o türden bir değişken tanımlanmalıydı.

		typedef int(*FPTR)(const void*, const void*); // typedef bildirimi yapıldı. 
		
		//Şimdi yukarıda verilen bildirimler ver tanımlar aşağıda typedef ile yapılsın.
		
		//int (*fp)(const void*, const void*); typedef'den önce
		FPTR fp; // typedef den sonra
		
		//int(**fptr)(const void*, const void*) = &fp;
		FPTR *fptr = &fp;
		
		//int (*fa[10])(const void*, const void*);
		FPTR fa[10];
		
  		// fonksiyon bildirirken de 
		//void f1(int (*fp)(const void*, const void*));
		void f1(FPTR);
		
		//void f2(int (*fpx)(const void*, const void*), int (*fpy)(const void*, const void*));
		void f2(FPTR, FPTR);
		
		//int(* f3(int (*fpx)(const void*, const void*), int (*fpy)(const void*, const void*)))(ccnst void*, const void*);
		FPTR f3(FPTR, FPTR);
  
  
  #
  
  - Soru: Aşağıdaki char diziyi a dan z ye sıralayın callback fonksiyonunu yazınız:

```
int scmp(const void* vpx, const void* vpy)
{

}

int main()
{
	char* p[] = { "ocak",
				"subat",
				"mart",
				"nisan",
				"mayis",
				"haziran",
				"temmuz",
				"agustos",
				"eylul",
				"ekim",
				"kasim",
				"aralik" };

	qsort(p, asize(p), sizeof(char*), &scmp);

	for (size_t i = 0; i < asize(p); ++i) {
		printf("%s\n", p[i]);
	}
}

```



 #  Ders 40 Tarih 07 05 2020
 
 - Fonksiyon pointer dizileri:

- ctype başlık dosyasındaki test fonksiyonlarının adresleriyle ilk değerlerini
almış bir function pointer oluşturalım.

		int (*fa[])(int) = { &isupper, &islower, &isdigit, &isalnum,
		&isxdigit, &ispucnt &isspace, &isblank, &isprint, &iscntrl };
		
- Eğer yukarıdaki bildirimi typedef bildirimi ile tanımlasaydım;

		typedef int(*FTEST)(int);
		
		FTEST a[] = { &isupper, ... };
		
- Şimdi bir örnekle betimleyelim:
	- Örneğimizde ctype başlık dosyalarının olduğu bir fonksiyon pointer dizisi olacak.
	- Ekrana bir karakter girilecek ve girilen karakter fonksiyon pointerı 
	dizisindeki bütün fonksiyonlar çağırılarak ok veya not ok ekrana yazdırılacak
	- Yani siz 'A' harfi girdiğinizde ekrana sırasıyla ok, not ok gibi yazılar çıkacak
	Bunun anlamı isupper fonksiyonu doğru değerini gönderdiyse ok, yanlış değerini gönderdiyse not ok olarak ekrana yazdırıldığını anlayacağız.
	
		
```
typedef int (*FTEST)(int);

int main()
{
	FTEST fa[] = { &isupper, &islower, &isdigit, &isalnum, &isxdigit, &ispunct, &isspace, &isblank, &isprint, &iscntrl };

	int ch;

	ch = getchar();

	for (size_t i = 0; i < asize(fa); ++i) {
		if (fa[i](ch)) // if ((*fa[i])(ch)), if ((*(fa + i))(ch)) 
			printf("ok \n");
		else
			printf("not ok \n");
	}

}
````
- Yukarıdaki fonksiyonda fa dizisinin alternatif yazım şekilleri yanında verilmiştir.

- Bir lookup table kullanılarak test fonksiyonlarının isimleriyle birlikte yazımı:

```

typedef int (*FTEST)(int);

int main()
{
	FTEST fa[] = { &isupper, &islower, &isdigit, &isalnum, &isxdigit, &ispunct, &isspace, &isblank, &isprint, &iscntrl };
	const char* pa[] = { "isupper", "islower", "isdigit", "isalnum", "isxdigit", "ispunct", "isspace", "isblank", "isprint", "iscntrl "};

	int ch;

	printf("Bir karakter giriniz: \n");
	ch = getchar();

	for (size_t i = 0; i < asize(fa); ++i) {
		if (fa[i](ch))
			printf("%s testi icin ok\n", pa[i]);
		else
			printf("%s testi icin Not ok\n", pa[i]);
			
	}

}
```
- Şimdi ekrana bir karakter girilsin ve sonrasında hangi testin yapılması istendiği girilsin ve sonuc ona göre verilsin.

```

typedef int (*FTEST)(int);

int main()
{
	FTEST fa[] = { &isupper, &islower, &isdigit, &isalnum, &isxdigit, &ispunct, &isspace, &isblank, &isprint, &iscntrl };
	const char* pa[] = { "isupper", "islower", "isdigit", "isalnum", "isxdigit", "ispunct", "isspace", "isblank", "isprint", "iscntrl " };

	char entry[40];
	int ch;
	printf("Bir harf giriniz:\n");
	ch = getchar();
	printf("Bir test fonksiyonu seciniz:\n");
	scanf("%s", entry);

	size_t idx;
	for (idx = 0; idx < asize(pa); ++idx) {
		if (!strcmp(pa[idx], entry))
			break;
	}

	if (idx == asize(pa))
		printf("aradıgınız test fonksiyonu mevcut degildir.\n");
	else if (fa[idx](ch))
		printf("%s fonksiyonu icin %c karakteri ok\n", entry, ch);
	else
		printf("%s fonksiyonu icin %c karakteri not ok\n", entry, ch);
	
}
```

- Fonksiyon pointerı gösteren bir pointerla fonksiyon çağırmaya örnek:

			int square(int x)
			{
				return x * x;
			}

			int main()
			{
				int (*fp)(int) = square;
				int (**fptr)(int) = &fp;

				int x = (*fptr)(20);
	
				printf("x = %d ", x);
			}			


- Geri dönüş değeri bir fonksiyon pointerı olan bir foo  fonksiyonu örneği yapalım:

		int square(int x)
		{
			return x * x;
		}
		
		int (*foo(void))(int) // geri dönüş değeri türü int (*)(int) olan fonksiyon
		{
			return square;
		}
		
		int main()
		{
			printf("%d\n",foo()(20));
		}
		
- Bir de yukarıdaki kodu typedef bildirimiyle yazalım:

```
typedef int (*FPTR)(int);

int square(int x)
{
	return x * x;
}

FPTR foo(void)
{
	return square;
}

int main()
{
	printf("%d", foo()(20));
}
```


- Şimdi ilerde karşımıza sıkça çıkabilecek olan standart fonksiyonlarda 
kullanılan bir şekli kendimiz yazsak betimleyelim ki ilerde çok daha rahat bir
şekilde anlayabilelim.


```
/* Buradan belirtilen kısma kadar ki bölümün .h dosyasında saklandığı varsayılsın*/
typedef void (*FPTR)(void);

// func fonksiyonu default (varsayılan) olarak foo fonksiyonunu cağiracak
void func(void);
FPTR set_func(void);

/*.h dosyasında saklanacak olan kısımın bitiş noktası*/


//------------------------------------------------------------------------------

/* Buradan belirtilen kısma kadar ki bölümün .c dosyasında saklandığı varsayılsın.*/
static void foo(void)  // şimdilik static anahtar sözcüğünü görmezden gelelim
{
	printf("foo cagrildi \n");
}


static FPTR gfp = &foo;  /*func fonksiyonunda default olarak foo fonksiyonu
			cağırılması için gerekli olan global değişken tanımlanıp
			ilk değer olarak default olarak çağırılmasını istediğimiz
			fonksiyon adresi atandı.*/

void func(void)
{
	gfp();  	/* global olarak tanımlanan fonksiyon pointerının 
			gösterdiği fonksiyon çağırıldı.*/
}

FPTR set_func(FPTR f)
{
	FPTR ret = gfp; 	//Bir önceki default değeri saklandı.
	gfp = f;// default değerin yerine gönderilen değer gloabal değişkene atandı.
	return ret;	// Bir önceki tutulan default değer geri dönüş değeri olarak döndürüldü.
}
/*.c dosyasında saklanacak olan kısımın bitiş noktası*/

void myfoo(void)
{
	printf("myfoo cağirildi\n");
}

int main()
{
	func();  // func burada foo işlevini çağıracak

	FPTR f = set_func(&myfoo);
	func();   // func burada myfoo fonksiyonunu çağıracak

	set_func(f);   // set_func 'ın geri dönüş değeri kullanılarak default haline geri çevrildi.

	func();   // func burada tekrar foo işlevini çağıracak
}
```
  
- Şimdi de benzer ama biraz da farklı olan bir çatı tipinden örnek verelim.

```
/*.h dosyası başlangıç*/

typedef void (*FPTR)(void);

void func(void);
void fregister(FPTR f);  // func in hangi fonksiyonları çağıracağını belirleyen claim kod

/*.h dosyası bitiş*/
/*==========================================================*/
/*.c dosyası başlangıç*/

#define N_MAX_FUNC  10
static FPTR ga[N_MAX_FUNC];
static int gcnt = 0;


void fregister(FPTR f)
{
	
	ga[gcnt++] = f;
}

void func(void)
{
	for (int i = 0; i < gcnt; ++i) {
		ga[i]();
	}

}
/*.c dosyası bitiş*/

void f1(void)
{
	printf("f1 cagirildi\n");
}
void f2(void)
{
	printf("f2 cagirildi\n");
}
void f3(void)
{
	printf("f3 cagirildi\n");
}
void f4(void)
{
	printf("f4 cagirildi\n");
}




int main()
{
	fregister(&f1);
	//arada farklı kodlar olabilir.
	fregister(f2);
	fregister(f3);  //fregister a hangi fonksiyonlar gönderildiyse o fonksiyonlar çağırılacak
	fregister(f4);

	func(); /* şimdi func çağırıldığında fregister ile 
			kaydedilen fonksiyonlar çağırılacak  Tabi burada çağırılma sistemi 
			değişebilir. İlk gönderilen ilk çağırılabilir veya son gönderilen ilk 
			çağırılıp son giren ilk çıkar prensibi (step sistemi) uygulanmış olabilir.*/
}

```
- Bu yapıya benzer ancak (step sistemi) son girilen fonksiyonun ilk çağırıldığı 
bir standart fonksiyon örneği: (last in first out)

```

void f1(void)
{
	printf("f1 cagirildi\n");
}
void f2(void)
{
	printf("f2 cagirildi\n");
}
void f3(void)
{
	printf("f3 cagirildi\n");
}
void f4(void)
{
	printf("f4 cagirildi\n");
}




int main()
{
	atexit(f1);
	atexit(f2);
	atexit(f3);
	atexit(f4);
	
	exit(1);
}

```

  
# Çok Boyutlu Diziler

- Multi Dimensional Arrays

		int a[10][20];

- C'de çok boyutlu bir dizi yoktur. Yani C'de çok boyutlu diziler 
elemanları dizi olan dizilerdir.

  - Yani yukarıda a dizisinin elemanları 20 elamanlı int dizilerdir.


  		int a[10][20]; 
		
		printf("asize(a) = %zu\n", asize(a)); // a 'nın boyutunu 10 olarak görürüz.
		
		printf("sizeof(a) = %zu\n", sizeof(a)); // ekrana 4x10x20 = 800 olur.
		
		printf("sizeof(a[0]) = %zu\n", sizeof(a[0]));
		/* yukarıda ise a dizisinin bir elemanının sizeof değeri
		yazdırılacak yani 4 x 20  = 80 olur.*/
		printf("sizeof(a[0][0]) = %zu\n", sizeof(a[0][0]));
		// yukarıda bu sefer a dizisinin ilk elemanının ilk elemanının boyutu olan benim  derleyicime göre 4 yazısı boyut bilgisi olarak ekrana yazılır.
		
		

- Çok boyutlu dizilerde array decay söz konusu olduğunda dizinin ismi 
kullanıldığında dizinin ilk elemanına dönüşür lakin dizinin ilk elemanı yukarıda 
20 boyutlu bir dizi olduğu unutulmamalıdır.

	int a[10][20];
	// a olarak kullanıldığında &a[0] olarak algınır.
	
	int* p = a; // C'de yanlış C++'da sentaks hatasıdır. Çünkü a burada int* bir tür değildir.
	
- Peki çok boyutlu diziler nasıl bir pointer da tutulur

		int a[10][4];
		int(*p)[4] = a;
		//int(*p)[4] = &a[0];
  
  - Elamanları 10 elemanlı double dizi olan boyutu 5 olan a dizisini tanımlayınız:

		double a[5][10];
		

  - p pointerına a'nın ilk elemanının ilk elemanıyla ilk değer verelim:

		int [10][20];
		
		int *p = &a[0][0];
  		//int* p = a[0]; // ikinci bir yolu array decay ile 
		//int* p =(int*)a; // üçüncü bir yol 
		
- Yazım şekillerine örnekler;

		int a[10][20];
		
		a[5][3]; // a'nın 5. elemanın 3. indisi
		(*(a + 5))[3]; // a'nın 5. elemanın 3. indisi
		
		
- Çok boyutlu dizilere ilk değer verilmesi:

		int a[5][4] = {
				{1, 1, 1, 1},
				{2, 2, 2, 2},
				{3, 3, 3, 3},
				{4, 4, 4, 4},
				{5, 5, 5, 5},
				};
				
		for (int i = 0; i < 5; ++i) {
			for (int k = 0; k < 4; ++k) {
				printf("%d ", a[i][k]);
			}
			printf("\n");
		}
		
		
 - İlk değer verilmesi yapılırken eksik bırakılan elemanlar default olarak 0 değerini alır.
 
		 int a[5][4] = {
				{1, 1, 1, 1},
				{2, 2},
				{3, 3, 3, 3},
				{4},
				{5, 5, 5, 5}
				};
				
		for (int i = 0; i < 5; ++i) {
			for (int k = 0; k < 4; ++k) {
				printf("%d ", a[i][k]);
			}
			printf("\n");
		}
  
  
  - Yukarıda ilk değer verilmeyen elemanlar sıfır değerini aldı.


  - İç küme parantezi kullanılmadığı taktirde girilen elemanlar en baştan 
  sırasıyla 4 er 4er değer verilir. Bu da bir kullanım şeklidir.
  
  
   				int a[5][4] = {1, 1, 2, 2, 3, 3, 4, 4, 5, 5, 6, 	};
				
				for (int i = 0; i < 5; ++i) {
					for (int k = 0; k < 4; ++k) {
						printf("%d ", a[i][k]);
					}
					printf("\n");
				}
  
  
  
  - Designater initializer şeklinde ilk değer verme şekli aşağıdadır.
  	
	
		 int a[5][4] = {
				[3] = {3, 3, 3, 3}
				[5] = {5, 5, 5, 5}
				};
				
		for (int i = 0; i < 5; ++i) {
			for (int k = 0; k < 4; ++k) {
				printf("%d ", a[i][k]);
			}
			printf("\n");
		}
  
  
 - Bir mülakat sorusu:

		int a[][] = {1, 2, 3, 4, 5, 6, 7, 8, 9, 10};	
  		int b[3][] = {1, 2, 3, 4, 5, 6, 7, 8, 9, 10};
		int c[][3] = {1, 2, 3, 4, 5, 6, 7, 8, 9, 10};
		
- Yukarıdaki dizilerden hangiler geçerlidir.
 
 - Yalnızca c geçerlidir. Dizilere ilk değer verme sentaksı bize diyor ki 
 dizinin boyutunu vermek zorunda değilsiniz. Yani çok boyutlu dizilerin  boyutu
 ilk köşeli parantez içidir. İkinci köşeli parantez dizinin türüdür.
  
  
  
  
  - Pointer aritmetiğinin çok boyutlu dizilerde kullanımına dair örnek;
  
 ```
 int a[5][4] = {
				{1, 1, 1, 1},
				{2, 2, 2, 2},
				{3, 3, 3, 3},
				{4, 4, 4, 4},
				{5, 5, 5, 5}
	};

	for (int i = 0; i < 5; ++i) {
		for (int k = 0; k < 4; ++k) {
			printf("%d ", a[i][k]);
		}
		printf("\n");
	}

	printf("\n\n");

	int* p = a[0];
	//int * p = &a[0][0];
	//int *p = (int*)a;

	int n = 5 * 4;

	while (n--) {
		printf("%d ", *p++);
	}

 ```
  
-  Bir çok boyutlu dizi tanımlayalım

		int a[5][4];
		
- Yukarıdaki dizinin elemanlarının türü int değildir. Elemanlarının türü

		int[4] 	olur.
		

- typedef bildirimiyle nasıl kullanılıra gelecek olursak;

		typedef int INTA10[10];
		//INTA10 ---> int[10] türünün typedef ismi
	
		int main()
		{
			INTA10 A[20]; // int[20][10];
		}
	
- Yukarıda int[10] türünü typedef bildirimi ile bildirdik. Ve elemanları
10 elemanlı diziler olan 20 elemanlı bir dizi oluşturduk.



  - Bir örnekle pekiştirelim. Bir okul olsun ve her sınıfında 20 öğrenci olsun.
Sınıftaki öğrencilerin notlarını tutulması için şu şekilde bir dizi kullanılabilir.
		
		#define STUDENTS_PER_CLASS 20
		#define NO_OF_CLASS 10
		
		int main()
		{
			int grades[NO_OF_CLASS][STUDENTS_PER_CLASS];
		}
		

# Ders 41 Tarih 10 05 2021

- Çok boyutlu diziler üzerinde işlem yapan fonksiyonlar:

- Şimdi aşağıda üç tane çok boyutlu dizi tanımlansın;

		int a[10][20];  // türü -> int[20] 'dir
		int b[5][8];    // türü -> int[8] 'dir
		int c[6][4];    // türü -> int[4] 'dür
		
- Yukarıda her biri matris olarak kullanılabilir lakin yukarıdaki dizilerin 
türleri birbirinden farklıdır.
  
  - Yani siz bir diziyi fonksiyona göndermek istediğiniz varsayalım:

		void f1(int(*p)[20], size_t size); /* Yukarıdaki a dizisi için
						    türü int(*)[20] olan bir
						    pointer parametre olarak 
						    verilmelidir.*/
		void f2(int(*p)[8], size_t size); // b dizisi için 
		void f3(int(*p)[4], size_t size); // c dizisi için
  		
		int main()
		{
			int a[10][20];  // türü -> int[20] 'dir
			int b[5][8];    // türü -> int[8] 'dir
			int c[6][4];    // türü -> int[4] 'dür
			
			f1(a, 10);
			f2(b, 5);
		}
  
  
- Şimdi bir örnek verelim:

``
void set_random_20(int(*p)[20], size_t size)
{
	for (size_t i = 0; i < size; ++i) {
		for (size_t k = 0; k < 20; ++k) {
			p[i][k] = rand() % 10;
		}
	}
}
void print_array_20(const int(*p)[20], size_t size)
{
	for (size_t i = 0; i < size; ++i) {
		for (size_t k = 0; k < 20; ++k) {
			printf("%d ", p[i][k]);
		}
		printf("\n");
	}
}


int main()
{
	int a[10][20];

	randomize();

	set_random_20(a, 10);
	print_array_20(a, 10);

}
``		
- print_array_20 fonksiyonun farklı bir yazım biçimi:

``

void print_array_20(const int(*p)[20], size_t size)
{
	while (size--) {
		for (int i = 0; i < 20; ++i) {
			printf("%d ", (*p)[i]);
		}
		printf("\n");
		++p;
	}
}
``


- Şimdi öyle bir fonksiyon yazalım ki çok boyutlu dizilerde boyut türü uyuşmasada
fonksiyon geçerli olsun.

``

void set_matrix(int* p, size_t row, size_t col)
{
	for (size_t i = 0; i < row; ++i) {
		for (size_t k = 0; k < col; ++k) {
			p[i * col + k] = rand() % 10;
		}
	}
}

void print_matrix(const int* p, size_t row, size_t col)
{
	for (size_t i = 0; i < row; ++i) {
		for (size_t k = 0; k < col; ++k) {
			printf("%d ", p[i * col + k]);
		}
		printf("\n");
	}

	printf("\n------------------------------\n\n");
}

int main()
{
	int a[5][9];
	int b[3][8];
	int c[2][10];

	randomize();
	
	set_matrix(a[0], 5, 9);
	print_matrix((int*)a, 5, 9);

	set_matrix(&b[0][0], 3, 8);
	print_matrix((int*)b, 3, 8);

	set_matrix(c[0], 2, 10);
	print_matrix(&c[0][0], 2, 10);


}
``

- Fonksiyonların makrolar ile kullanım şekillerine dair bir örnek:

``
#define csmf(col)	void set_matrix_##col(int (*p)[col], size_t size) \
{ \
	for (size_t i = 0; i < size; ++i) { \
		for (size_t k = 0; k < col; ++k) { \
			p[i][k] = rand() % 10; \
		} \
	}\
} \

#define cpmf(col)	void print_matrix_##col(int (*p)[col], size_t size) \
{ \
	for (size_t i = 0; i < size; ++i) { \
		for (size_t k = 0; k < col; ++k) { \
			printf("%d ", p[i][k]); \
		} \
		printf("\n"); \
	}\
	printf("\n-----------------------\n"); \
} \

csmf(9)
cpmf(9)

csmf(20)
cpmf(20)

csmf(40)
cpmf(40)


int main()
{
	int a[5][9];
	int b[7][20];
	int c[12][40];

	randomize();

	set_matrix_9(a, 5);
	print_matrix_9(a, 5);

	set_matrix_20(b, 7);
	print_matrix_20(b, 7);

	set_matrix_40(c, 12);
	print_matrix_40(c, 12);
}

``
  
   - Çok boyutlu dizilerde elemanları char olan dizilere örnekler verelim:


  ``
  char names[][20] = { "ocak", "subat", "mart",
							"nisan", "mayis", "haziran", "temmuz", "agustos",
							"eylul", "ekim", "kasim", "aralik" };

	for (size_t i = 0; i < asize(names); ++i) {
		printf("%s ", names[i]);
	}
	
  ``
  
  - Yalnız burada bir şeye dikkat etmemiz gerekiyor artık yukarıdaki örnekte
  çok boyutlu yazı dizisi mevcut, pointer değil! Yani siz bu dizideki elemanları yazılara yaptığıız tüm işlemlerde kullanabilirsiniz.
  
``
char names[][20] = { "ocak", "subat", "mart",
							"nisan", "mayis", "haziran", "temmuz", "agustos",
							"eylul", "ekim", "kasim", "aralik" };

	for (size_t i = 0; i < asize(names); ++i) {
		_strrev(names[i]);
	}
	for (size_t i = 0; i < asize(names); ++i) {
		printf("%s ", names[i]);
	}
``
  - Yukarıdaki fonksiyon isimleri kendi içinde ters çevirdi.

- Peki bu yazdırma işlemini bir fonksiyona yaptırmak isteseydik nasıl bir yol
izlerdik?

``
void print_names(char(*p)[20], size_t size)
{
	for (size_t i = 0; i < size; ++i) {
		printf("%s ", p[i]);
	}
	printf("\n\n");

}

int main()
{
	char names[][20] = { "ocak", "subat", "mart",
							"nisan", "mayis", "haziran", "temmuz", "agustos",
							"eylul", "ekim", "kasim", "aralik" };

	print_names(names, asize(names));
	
}

``
  
- Yukarıdaki program parçacığında yazdırma fonksiyonun farklı bir yazım biçimi:

``
void print_names(char(*p)[20], size_t size)
{
	while (size--) {
		printf("%s ", *p++);
	}

	printf("\n\n");

}

int main()
{
	char names[][20] = { "ocak", "subat", "mart",
							"nisan", "mayis", "haziran", "temmuz", "agustos",
							"eylul", "ekim", "kasim", "aralik" };

	print_names(names, asize(names));
	
}
``
  
- Şimdi yazıları sıralayalım ama yine dikkat etmeliyiz ki bu bir pointer 
dizi değil.

``
void swap_str(char* px, char* py)
{
	char temp[20]; // gelecek parametrelerin 20 sınırında olduğu kabul ediliyor
	strcpy(temp, px);
	strcpy(px, py);
	strcpy(py, temp);
	
}

void sort_names(char(*p)[20], size_t size)
{
	for (size_t i = 0; i < size - 1; ++i) {
		for (size_t k = 0; k < size - 1 - i; ++k) {
			if (strcmp(p[k], p[k + 1]) > 0)
			swap_str(p[k], p[k + 1]);
		}
	}
}


void print_names(char (*p)[20], size_t size)
{
	for (size_t i = 0; i < size; ++i) {
		printf("%s ", p[i]);
	}
}

int main()
{
	char names[][20] = { "ocak", "subat", "mart",
							"nisan", "mayis", "haziran", "temmuz", "agustos",
							"eylul", "ekim", "kasim", "aralik" };

	sort_names(names, asize(names));
	print_names(names, asize(names));
	
}

``

- Daha önceki konularda da örnek verilmişti hatırlayalım

		char str[] = "mustafa";
		char *p = "erdinc";
		
- Yukarıdaki iki deyim arasındaki fark pointer'a ilk deger verilen erdinc yazısı
programın sonuna kadar bellekte kalacak olan bir string literalidir.
Yani siz böyle bir tanımlama yaptığınızda iki farklı varlık oluşturuyorsunuz.
Birisi p pointer değişkeni diğeri ise erdinc yazısını tutan string literali.
mustafa ise str dizisinin ilk değeri yani programın sonuna kadar kalacak bir 
string literali değil. str dizisine ilk değer olarak atanan bir yazı. Ve str 
dizisi elemanları değiştirildiğinde str mustafa yazısı değişecektir.

- Şimdi aynısı aşağıdada geçerlidir.

		char* p[] = { "ali", "veli", "tan" };
		
- Yukarıdaki yazılar yine programın sonuna kadar kalıcak string literalleridir.

-  Ancak aşağıdaki gibi tanımlandığında

		char p[][20] = { "ali", "veli", "tan", };
		
- Yukarıdaki tanıma göre tanımlanan yazılar string literalleri değildir. 
Dizinin elemanlarıdır ve değiştirilebilirler.



 - Bir konuda daha hatırlatma yapalım:

	 	void foo(int *p, int size);
		void foo(int p[], int size);
		
- Yukarıdaki iki bildirim arasında bir fark yoktu.
Hatta [] içine herhangi bir sayı yazılsa hata olmaz ama yazılan sayının da
bir anlamı yoktu. Ve buna benzer şekilde;

		void foo(int** p, int size);
		void foo(int* p[], int size);
		
- Yukarıdaki iki farklı tanımlamada sentaks olarak derleyiciye aynı anlamı ifade 
etmektedir.

  
- Şimdi elemanları dizi gösteren(yani çok boyutlu) dizilerde de iki farklı
notasyon söz konusu:

		int foo(int(*p)[20], int size);
		int foo(int p[][20], int size);
		

 
 #
 
 # Yazılarla sayılar arasındaki dönüşümler
  
  - Yazıdan sayıya dönüşüm:


		
		char str[SIZE];

		printf("bir tam sayi giriniz:\n");
		scanf("%s ", str);
  			
 - Siz şimdi yukarıdaki kod parçacığına bir tam sayı değeri girdiğinizde mesela
 34 sayısı girildiğinde bu değer karakter olarak tutulacak. Bunu tam sayıya 
 nasıl çevireceğimizi yazılar konusunda bahsetmiştik.
 
 		for (int i = 0; str[i] != '\0'; ++i) {
			printf("%c %d %d\n", str[i], str[i], str[i] - '0');
		}
		
  - Yukarıdaki kod ile dizi dolaşılıyor. İlk sütunda dizinin ilk elemanının
  karakter görüntüsü, ikinci sütunda ascıı karakter kodlamasındaki değeri, 
  üçüncü sütunda ise sayı karşılığı ekrana yazdırılmış oluyor.
  
  
  
  - Şimdi yukarıdaki kod bir çok olumsuz olabilecek durumlar göz ardı edilerek 
  yazıldı. Mesela siz negatif bir tam sayı yazdığınızda ekranda istediğiniz 
  değerleri göremeyeceksiniz. Boşluk karakterleri girildiğinde de bu karakterler
  de rakam karakteri varsayılarak işlem yapılacaktır.
  
  
  
  - Şimdi yukarıdaki yaptığımız işlevi standart bir fonksiyon yaptığından bahsedeceğiz.
  stdlib.h başlık dosyasında yer alan atoi fonksiyonu yazıyı rakama çeviriyor.
  
  
  		int atoi(const char* p);
		
- İsmi nerden geliyor dersek alphabetic to integer yani yazıdan tam sayıya.

		char str[SIZE];

		printf("bir tam sayi giriniz:\n");
		sgets(str);

		int ival = atoi(str);
		printf("ival = %d ", ival);
  
  
  - Tarih konusunda sık kullanılan bir örnek:


			char str[SIZE];

			printf("bir tarih (gg-aa-yyyy) giriniz:\n");
			sgets(str);

			int day, mon, year;

			day = atoi(str);
			mon = atoi(str + 3);
			year = atoi(str + 6);

			printf("%02d-%02d-%d\n", day, mon, year);
  
  
  
  - Şimdi rakamı yazıya nasıl dönüştürebiliyorduk birlikte hatırlayalım:

``
	int ival;
	printf("bir tam sayi giriniz\n");
	scanf("%d", &ival);

	char str[SIZE];

	int temp = ival;
	int idx = 0;

	while (temp != 0) {
		str[idx++] = temp % 10 + '0';
		temp /= 10;
	}
	str[idx] = '\0';

	for (int i = 0; i < idx / 2; ++i) {
		char c = str[i];
		str[i] = str[idx - 1 - i];
		str[idx - 1 - i] = c;
	}

	printf("(%d) (%s)\n", ival, str);
``
  
- Yukarıdaki işlevi yapan stdlib.h başlık dosyasında olan ve standart olmayan 
bir fonksiyon vardır.
		
		char* _itoa(int val, char*buf, int base);
		
- Bir örnekler betimleyelim:

``
	int ival;
	printf("bir tam sayi giriniz\n");
	scanf("%d", &ival);

	char str[SIZE];

	_itoa(ival, str, 10);
	printf("onluk sayi sisteminde (%s)\n", str);

	_itoa(ival, str, 16);
	printf("on altilik sayi sisteminde (%s)\n", str);

	_itoa(ival, str, 8);
	printf("sekizlik sayi sisteminde (%s)\n", str);

	_itoa(ival, str, 2);
	printf("ikilik sayi siteminde (%s)\n", str);
``
  
  
  
 - atoi fonksiyonunun kardeşi olan iki fonksiyon daha mevcuttur.

		long atol(const char* p); // yazıdan long değer çeker
		double atof(const char* p);  // yazıdan double değer çeker
  
  
  #
  
  ``
  char str[SIZE];

	printf("bir yazi giriniz.\n");
	sgets(str); //234.325mehmet
	
	printf("(%s)\n", str);
	int ival = atoi(str);
	double dval = atof(str);

	printf("ival = %d\n", ival);
	printf("dval = %f\n", dval);
	

  ``
  
  
  - Yeni bir standart fonksiyon

		double strtod(const char* pstr, char** p);
		
- İşlevi biraz karışıktır. Fonksiyona pstr olarak bir char* pointer gönderdiğinizi düşünelim. 
Bu yazı pointerının içerisinde 12.765mehmet olsun. Bu yazı dizisindeki rakamları double formatına
dönüştürüyor. Ve dizide ilk sayı formatının dışında olan adresi char** p pointerıyla adresini döndürüyor. Eğer adresi kullanmak istemediğinizde fonksiyonun ikinci parametresi olarak NULL pointer
gönderirseniz adres olayını kullanmamış oluyorsunuz.

- Null pointer kullanarak fonksiyonuuzu kullanalım:

``
	char str[SIZE];

	printf("bir yazi girin:   "); // 12.765ahmet
	sgets(str);
	printf("(%s) \n", str);

	double dval;

	dval = strtod(str, NULL);
	
	printf("dval = %f\n", dval);
``
 
- Şimdide fonksiyonumuzun ikinci parametresini de kullanarak işlevine göz atalım:

``
	char str[SIZE];

	printf("bir yazi girin:   "); // 12.765ahmet
	sgets(str);
	printf("(%s) \n", str);

	double dval;
	char* p;

	dval = strtod(str, &p);
	printf("dval = %f\n", dval);
	printf("idx = %d\n", p - str);  // hangi indexde format dışında bir değer olduğu yazdırıldı.
	puts(p); // ahmet
	
``

- Şimdi yeni bir fonksiyon daha öğrenelim:


		char* strtok(char* p, const char* ptr);
		
- Yukarıdaki fonksiyon gönderilen yazıyı tokenlarına ayırıyor.
	- Birinci parametre tokenlarına ayıracağınız yazıyı gönderiyorsunuz.
	- İkinci parametreye ise ayıraç karakterleri olarak kullanılacak yani tokenların parçası 
	olmayan karakterler olarak ele alınacak.
	- strtok, her çağrıda yazıdaki tokenlardan birinin adresini döndürecek ama ne zaman ki 
	strtok, NULL pointer döndürürse siz yazıda artık yeni bir token olmadığını anlayacaksınız.
	Dolayısıyla strtok'u çağırırken NULL pointer döndürene kadar döngüsel bir yapı içerisinde
	çağıracağız. Yalnız enterasan kısmı şu ki, fonksiyona ilk yapılan çağrıda strtok 
	fonksiyonuna atomlara ayrılacak olan yazının adresini geçiyorsunuz ama ondan sonraki 
	çağrılarda NULL pointer geçiyorsunuz. 
	Dolayısıyla bu döngü aşağıdaki şekilde kuruluyor.
	
	
``
	char str[SIZE];
	printf("bir yazi giriniz:\n");
	sgets(str);
	printf("(%s)\n", str);

	int cnt = 0;
	char* p = strtok(str, " .,;!?:"); /*Burada ikinci parametrede ayrıcı tokenlar 
									  girildi. boşluk karakter, nokta, virgül, 
									  noktalı virgül, ünlem, soru işareti ve iki 
									  nokta. Bu karakterleri gördüğünde alınan ilk 
									  token yazı adresi olarak geri döndürülecek.*/

	while (p) {
		printf("%d. token : %s\n",++cnt, p);
		p = strtok(NULL, " .,;!?:"); /*fonksiyon ikinci çağırılışında ilk parametre
									 NULL pointer olarak gönderildi.*/
	}
``
  
  - Şimdi de ayıraç karakterlerini rakam yaparak bir örnek oluşturalım.

``

	char str[SIZE];
	printf("bir yazi giriniz:\n");
	sgets(str);
	printf("(%s)\n", str);

	int cnt = 0;
	char* p = strtok(str, "0123456789");

	while (p) {
		printf("%d. token : %s\n",++cnt, p);
		p = strtok(NULL, "0123456789"); 
	}
``
  
  
- Bellek üzerinde formatlı okuma yazma işlemleri
	- formatlı çıkış işlemleri
		-  std output 'a yazmak yani ekrana yazdırıyoruz.
		-  formatlanmış veriyi  bir char dizide tutmak (in memory output operation)
		-  Bir dosyaya verilmesi
		
  - Üç tane formatlı çıkış fonksiyonumuz var.
  	- printf - std output
  	- sprintf - çıktıyı belleğe veriyor
  	- fprintf - çıktısını dosyaya veriyor
  	
  
  
  		int sprintf(char* pbuf, const char*, ...);

``
  
	int x = 20;
	double dval = 3.4;

	char str[] = "muratcan";
	char buffer[SIZE];

	//printf("%d %f %s", x, dval, str);
	sprintf(buffer, "%d %f %s", x, dval, str); // ekran çıktısını buffer değişkenine yazdı.
	
	puts(buffer); // yani biz bu buffer yazı dizisini istediğimiz şekilde kullanabiliriz.
	
``
  
- Yukarıdaki fonksiyon son derece önemli ve çok sık kullanılan bir fonksiyon.


- Bir örnek:

``
	char name[SIZE] = "rasit";
	char surname[SIZE] = "kahraman";
	int birth_year = 1998;

	char file_name[SIZE];

	// yukarıdaki verilerden faydalanılarak bir dosya ismi oluşturmamız gereksin
	// rasit_kahraman_1998.txt gibi

	sprintf(file_name, "%s_%s_%d.txt", name, surname, birth_year);

	printf("(%s)", file_name);

``
  
  - Aşağıdaki örnekte formata uygun bir txt dosyası oluşturulup içerisine yazı yazdırılıyor:

``
	char name[SIZE] = "rasit";
	char surname[SIZE] = "kahraman";
	int birth_year = 1998;

	char file_name[SIZE];

	// yukarıdaki verilerden faydalanılarak bir dosya ismi oluşturmamız gereksin
	// rasit_kahraman_1998.txt gibi

	sprintf(file_name, "%s_%s_%d.txt", name, surname, birth_year);

	FILE* f = fopen(file_name, "w");
	fprintf(f, "bugun c dersi yaptik\n");
	fclose(f);

``
  
- Nasıl karşımıza çıkabileceğine dair bir örnek daha verelim:

``
	char name[SIZE] = "rasit";
	char surname[SIZE] = "kahraman";
	int birth_year = 1998;

	char file_name[SIZE];

	//kahraman_rasit_98_001.jpeg
	//kahraman_rasit_98_002.jpeg

	for (int i = 0; i < 100; ++i) {
		sprintf(file_name, "%s_%s_%02d_%03d.jpeg", surname, name, birth_year % 100, i + 1);
		printf("(%s)", file_name);
		getchar();
	}

``
  
  
 - Yukarıdaki çıkış işlemlerinde uygulanan durum giriş fonksiyonlarında da söz konusu


# Ders 42 Tarih 12 05 2021

- scanf'in kardeşlerini görmeden önce scanf fonksiyonunu hatırlayalım:

			int scanf(const char*, ...);
- scanf fonksiyonun geri dönüş değeri kaç adet nesneye yazdıysa o sayıyı döndürüyordu.
eğer yazma esnasında herhangi bir problem durumunda - 1 sayısını hata mesajı olarak döndürüyordu.

- Şimdi diğer alternatif fonksiyonlara gelelim.

			int sscanf(const char* p, const char*, ...);
			
- sscanf fonksiyonunun scanf'den farkı: karakterleri, fonksiyon çağrısında gönderdiğiniz birinci 
parametredeki diziden alıyor.
  
``
	char str[] = "234  567  890";
	int x, y, z;

	sscanf(str, "%d%d%d", &x, &y, &z);

	printf("x = %d, y = %d, z = %d\n", x, y, z);

``
- Bir örnek daha verelim:


``
	char str[] = "12334ahmet";

	int x;
	char s[40];

	sscanf(str, "%d%s", &x, s);

	printf("%d (%s)", x, s);
``
  	
  
  
  - Bir de snprintf fonksiyonu var.
  
  			int snprintf(char* restrict buffer, size_t bufsize, const char* restrict format, ...);
			
- sprintf'den farkı ise dizi boyutu istiyor olmasıdır.
- Birinci parametresi çıkışı yapacağı dizi adresi.
- İkinci parametresi, birinci parametrede istenilen dizinin boyutudur.
- Üçüncü parametresi yine formatlama string literali.
- Dördüncü parametresi ise variadic.




# Programı Sonlandıran Programlar

- exit
- atexit
- abort

- Bir C programı çalıştığında (process), main fonksiyonu çalışıp sonlandığında program da sonlanıyor
- stdlib.h başlık dosyasında bildirilen fonksiyonlardır.
	- Programın iki tane sonlanma biçimi var. 
		- normal termination  (exit fonksiyonuna yapılan çağrıyla programın sonlanması)
		Aslında zaten main fonksiyonu return deyimiyle bittiğinde yine default olarak
		exit fonksiyonu çağırılarak program sonlanmış oluyor
		- abnormal temination (abort fonksiyonuna yapılan çağrıyla programın sonlanması)


- exit fonksiyonunu bildirimini inceleyelim:

			void exit(int status);
			
	- Fonksiyonun geri dönüş değeri yok.
	- int parametresi var ve çağırıldığında process'in sonlanmasını sağlıyor. Ve int argüman
	programın ne nedenle sonlandırıldığı hakkında bilgi veriyor.
		- non-zero değerler başarısızlık (failure)
		- zero ise başarı (success) bilgisini iletiyor.
	- Bu başarı bilgisi okuyana ve işletim sistemine verilen bilgidir.
  
  
  			exit(0); // başarılı
			exit(1); // başarısız
  
  - Okumayı kolaylaştırması açısından stdlib.h başlık dosyasında 2 adet sembolik sabit var.
 	
		EXİT_SUCCESS =>  0
		EXİT_FAILURE =>  1
  
  
  - Şimdi bu exit fonksiyonuna yapılan çağrıda verilen bazı garantiler var. Yani program aniden
  sonlandırılmıyor. 
  	- Bu garantilerin en önemlisi: açık olan dosyaların buffer'larının flush ediliyor olması.
  		- Flush işlemi nedir dersek: Normal olarak dosyaya yazma işlemleri
  		fiziksel olarak doğrudan dosyaya yazılmıyor çoğunlukla, o dosya için bellekte 
		ayrılan bir alana (buffera) yazılıyor. Fakat belirli etmenler tetiklendiğinde 
		mesela o buffer dolduğunda, bufferdaki byte'lar fiziksel olarak dosyaya yazılıyor.
		İşte bu işleme flush(flushing) deniyor. 
		Şimdi mesela örnek olarak siz programda bir dosyaya yazmaya başladınız. Yazdığınız
		bilgiler buffer'da depolandı ve o buffer dolmadığı için de dosyaya aktarılma işlemi
		gerçekleşmediği için halen dosyaya veriler yazılmamış olarak bufferda tutuluyor.
		Siz programı sonlandırdığınızda o bufferdaki bilgiler dosyaya yazılmadı ve veri 
		kaybı söz konusu oluyor. Ama işte exit fonksiyonu programı sonlandırıyorsa, 
		buffer'ların flush edilmesi garantisi vardır. En azından açık olan dosyalarda 
		yazılmamış veriler bırakılmıyor. 
		Ancak abort fonksiyonun  böyle bir garanti vermesi söz konusu değildir.
	

- Bir de exit fonksiyonuna yardımcı fonksiyon:

			int atexit(void (*fp)(void));
			
- Bu fonksiyonla siz bir fonksiyonu kayda alıyorsunuz ve exit fonksiyonunu çağırdığınızda,
atexit'le kayıt edilen fonksiyonlar kayıt edildikleri sırayla çağırılıyor. Yani exit 
programı sonlandırmadan önce atexitle kayıt edilmiş fonksiyonları çağırıp sonlandırıyor.


  - Biz şimdiye kadar bütün programların sonlanmasını main fonksiyonu içerisinde gerçekleştirdik.
  - Oysa çok doğal durumlardan birisi de bir fonksiyonun kodunun çalışması sırasında  programın
  akışının o fonksiyondan onu çağıran fonksiyona geri dönüş yapılmadan  doğrudan o fonksiyon 
  içerisinde sonlanması yani programlar illa main fonksiyonu içerisinde sonlanmak zorunda değildir.
  
 ``
 void f3(void)
{
	printf("f3 basladi\n");
	exit(EXIT_FAILURE);
	printf("f3 sona eriyor\n");
}

void f2(void)
{
	printf("f2 basladi \n");
	f3();
	printf("f2 sona eriyor\n");
}
void f1(void)
{
	printf("f1 basladi\n");ç
	f2();
	printf("f1 sona eriyor\n");
}

int main()
{		
	printf("main basladi\n");

	f1();
	printf("main sona eriyor.\n");

}

 ``
  
  
 - Biz bir fonksiyonun içerisinde fonksiyonu neden sonlandıralım?
 	- Çoğunlukla başarısızlık sebebiyle ancak her zaman değil.
 
 
 - Şimdi atexit fonksiyonun işlevine geri dönelim.
 	- atexit aldığı fonksiyon adreslerini kaydediyor. atexit'in geri dönüş bilgisi başarı 
 	bilgisidir. 0 döndürdüğünde başarılı olmuş non-zero değer döndürmesi durumunda başarızlık
	söz konusudur.  Yani 0 döndüğünde fonksiyon adresi kaydedilmiş, 1 döndürüldüğünde ise 
	kaydedilmediği anlamına geliyor. 
	
  - Peki biz bu fonksiyonları kayıt ediyoruz da noluyor?
   	- Aslında bu fonksiyonların adreslerini, daha önceden öğrendiğimiz bir temaya paralel 
   	olarak, atexit fonksiyonu sizden gizlenen, elemanları function pointer olan bir diziye 
	yazıyor. Kayıttan kastımız budur. exit çağırıldığında ise exit fonksiyonu programı 
	sonlandırmadan önce atexit'in bu adresleri yazdığı fonksiyon pointerı dizisine erişiyor,
	ve oraya adresleri yazılan fonksiyonları çağırıyor. Ama dikkat edilmesi gereken nokta 
	fonksiyonları çağırırken en son kaydedilen ilk çağırılıyor (last in first out)
  
  
  - Bir örnekle inceleyelim:

``
void f3(void)
{
	printf("f3 cagirildi\n");
}

void f2(void)
{
	printf("f2 cagirildi \n");
}
void f1(void)
{
	printf("f1 cagirildi\n");
}

int main()
{		
	atexit(&f1);
	atexit(f2);
	atexit(f3);


	exit(EXIT_FAILURE);

}
``
- Yukarıdaki örnekteki gibi atexit fonksiyonu ile 32 adet fonksiyon adresi kesin olarak 
edebilirsiniz. Ancak 32 den fazla olup olmaması derleyiciye bağlıdır. 


  
- main fonksiyonunda return statement kullanırsanız aslında default olarak exit fonksiyonunu
çağırmış oluyorsunuz.

		return 0; /--> exit(0)  başarılı (success)
		return 1; /--> exit(1)  başarısız (failure)
		

  - C99 standartlarından önce main fonksiyonun içerisine return statement yazmadığınızda çöp
  değer kabul ediliyordu. Ancak C99 standartlarından sonra artık siz yazmasanız dahi default 
  olarak yazmışsınız kabul ediliyor.
  
  
  - Peki neden böyle bir mekanizmaya ihtiyacımız var bunu birlikte inceleyelim:

	- Henüz hiç karşılaşmadık ama kulanacağımız kütüphanelerde çok sık karşımıza çıkacak.
	Programlamada bazı işlemler, bunlar tipik olarak fonksiyon çağrısıyla gerçekleşiyor.
	Bu hizmetleri aldıktan sonra bazı operasyonları yapmanız gerekiyor. Bunlar tipik olarak
	kullanılan kaynakların geri verilmesini sağlayan işlemler.
	Mesela diyelim ki bir kütüphane var siz bu kütüphanede  bir fonksiyonu çağırıyorsunuz
	fakat işiniz bittiğinde bu fonksiyonun edindiği kaynakları geri vermek için bir başka 
	fonksiyonu çağırmanız gerekiyor. İşte bu kaynakları geri veren veya bir takım temizlik
	işlemleri yapan fonksiyonlara popüler olarak cleanup fonksiyonları deniliyor. 
	Mesela birçok kütüphanede ismi Create (ya da open) ile başlayan fonksiyonlar kaynakları ediniyor, ismi
	destroy (ya da close) ile başlayan fonksiyonlar da kaynakları geri veriyor. 
  
  
  - Bir de şöyle bir risk var, diyelim ki kaynakları edindiniz bir şekilde, belirli bir noktada
  kaynakları geri vericeksiniz. Ya bu aralıkta siz kaynakları geri veremeden program sonlanırsa?
  Bu durumda kaynakları geri göndereceğiniz noktaya program gelmediği için kaynakları gönderememiş
  olacaksınız. Böylece belki tahmini mümkün olmayan hasar/zarar oluşmuş olucak. O zaman öyle bir 
  mekanizma kullanılmalı ki kaynakların geri verildiğinde emin olunmalıdır. Peki nasıl emin 
  olabiliriz?  Madem atexit ile gönderilen fonksiyonlar program sonlandığında exit fonksiyonları
  programı sonlandırmadan bunları çağırıyor. O zaman biz de cleanup işlemlerini fonksiyonlara 
  yaptırırız ve bu fonksiyonların adreslerini atexit'e argüman olarak göndeririz ve program her ne 
  zaman sonlanırsa sonlansın cleanup işlemlerinin yapılacağından emin oluruz. 
  
  - Tabi bu illa kullanılması gereken bir mekanizma olarak algılanmamalı ancak bazı durumlarda 
  kullanılması gerekiyor.
  
 - Bir noktada daha hatırlatma yapmak gerekirse aynı fonksiyonu birden fazla kez çağırabilir. 
 Bu durumda iki kez veya istenilen sayı kadar program sonlanmadan önce gönderilen fonksiyonlar 
 çağırılacaktır. 
  
  
  - abort fonksiyonuna geldiğimizde yine stdlib.h başlık dosyasında bildirilen bir sonlandırma 
  fonksiyonu. 
  
  		void abort(void);
		
- abort fonksiyonunun garanti ettiği hiçbir şey yok ve ani bir şekilde programı sonlandırıyor. 
- Ancak abort'un da şöyle bir özelliği var. abort programı sonlandırdığı zaman, hata ekranına,
bu da tipik olarak std output'a bağlı, programın sonlanmasının abort'a yapılan çağrıyla 
gerçekleştiğini bir şekilde yazıyor. Böylece siz örneğin bir programı debug ederken, eğer program 
abort'a yapılan çağrıyla sonlanmışsa siz bunu abort çağırıldığı için sonlandığını anlıyorsunuz
çünkü hata ekranında öyle bir yazı görüyorsunuz. 
  
- Peki neden böyle birşeye ihtiyaç var? nedeni ya biz programı debug ediyoruz, ve bir hata
durumuyla karşılaştığımızda hatayı o anda görmek istiyoruz. Çünkü eğer bir takım işlemlerin 
yapılmasına izin verirsek o hata durumunu yeterince iyi bir şekilde gözlemleyemeden kaçırabilirz.
bu sebeple bahsettiğimiz hata durumu oluştuğunda programın direk sonlanmasını istiyoruz. 
  
  
# Dinamik Bellek Yönetimi (Dynamic Memory Management)

- Programlamanın en önemli araçlarından biriyle tanışıyoruz.
  
  - Biz Ömür (storage duration) 'dan bahsettiğimizde ömürleri üçe ayırmıştık.
  	- automatic  (fonksiyonların içerisinde static anahtar sözcüğü kullanılmadan tanımlanan
  	- static   ( static anahtar sözcüğüyle veya global alanda tanımlanan , string literaller) 
  		- Bellekte bir yer edinmesi ve programın sonuna kadar o yerini korumasıdır. 
  	- dynamic duration

- Dinamik ömürden bahsetmemiştik.
  
  - Dinamik ömür ise programın çalışma zamanında programcı olarak, istenilen herhangi bir zaman 
  noktasında nesneyi hayata getirebileceğiz ve istediğimiz herhangi bir zaman noktasında da 
  nesnenin hayatını bitirebileceğiz.  Yani nesnenin hayatı ne bloklarla sınırlı, ne de programın
  sonuna kadar hayatı devam etmek zorunda. 
  - Bir çok işi gerçekleştirebilmemiz için dinamik ömürlü nesnelere ihtiyacımız var. 
  
  
  
  
  - Bir func fonksiyonu olsun. Kendisini çağıran koda kendisinin oluşturduğu bir nesneyi iletmesini
  sağlamak istiyoruz. 
  
  
  		func(??)
		{
			nesne oluşturuyor
			ve bu nesnenin adresini çağıran koda iletiyor. 
		}
  
  - Yukarıdaki senaryoda automatic ömürlü nesne adresi döndüremeyiz çünkü zaten o nesnenin ömrü 
  fonksiyonun dışına çıkıldığında bitiyor. Eğer static ömürlü bir nesne tanımlayıp göndersek 
  bu sefer de fonksiyon her çağırıldığında hep aynı nesnenin adresi döndürülecektir. Ama biz burada
  fonksiyon her çağırıldığında yeni bir nesne tanımlansın ve o nesnenin adresi döndürülsün 
  istiyoruz. 
  
  - Mesela başka bir senaryo ile örnek verelim. Siz bir dizi oluşturmak istiyorsunuz ama dizinin 
  boyutu programın çalışma esnasında belli oluyor. Yani siz dizide kaç eleman bulunacağı bilgisini
  kullanıcıdan aldığınızı varsayarsak o zaman bu görevi tanımlayamayız. Çünkü dizinin boyutu bir 
  değişken ifadesi olamaz. Ama bu da çok sık duyulan bir ihtiyaçtır.  Yani dizinin boyut bilgisi
  çalışma zamanında elde ediliyor. Kodu yazan kişi bu bilgiye sahip değil. 
  Mesela bir dosyanın içeriğindeki bir yazıyı bir char diziye alacaksınız. Ve dosyaya o an sahip 
  değilsiniz. Dosyanın ne olduğu da çalışma zamanında belli olacak. 
  
  - Dinamik ömürlü nesne ile dinamik bellek yönetimi arasındaki ilişkiye de bir göz atalım. 
  	- Dinamik ömürlü nesne, programın çalışma esnasında herhangi bir noktada nesneyi meydana
  	getirip istenilen herhangi bir noktada da sonlandırabilmektir. Bu dinamik ömürlü nesnelerin
	bir yere sahip olması gerekiyor.  İşte programın çalışma zamanında bu bellek alanının elde 
	edilmesi gerekiyor. Dinamik bellek yönetimi derken, programın çalışma zamanı içinde 
	programın kullanacağı bir bellek alanının elde edilmesi sürecidir.
	- Yani dinamik bellek yönetimi, program çalışırken ortaya çıkan bir storage ihtiyacının
	programın çalışma zamanında çalıştırılan bir kodla elde edilmesi.
  	
  
  - Programın çalışma zamanında bir bellek alanını kullanılır hale getirmek tipik olarak 
  işletim sisteminin fonksiyonları ile yapılıyor. Fakat bunu standart hale getirmek için, 
  yani işletim sisteminde kullanılan ortamdan bağımsız bir şekilde bunu çalıştırıcak bir kod 
  oluşturma fikri bizi standart kütüphaneye götürüyor. Şimdi biz de programın çalışma zamanında 
  bir bellek alanının elde edilmesi ve ihtiyaç duyulan koda bu bellek alanının sunulmasına yönelik
  C'nin standart bazı fonksiyonlarını öğreneceğiz. 
  
  	- malloc 
  	- calloc
  	- realloc
  	- free fonksiyonları.
  	
- Derleme zamanında oluşturulan bellek yönetimine statik(compile-time) bellek yönetimi
- Çalışma zamanında oluşturulan bellek yönetimine dinamik(run-time) bellek yönetimi denir
	- statik (compile-time) bellek yönetimi
	- dinamik (run-time) bellek yönetimi

- Yukarıdaki iki bellek yönetiminde dinamik bellek yönetiminin maliyeti kat be kat daha yüksektir. 
Buradaki maliyetten kasıt çalışma zamanındaki maliyettir. 
Yani verim açısından dinamik bellek yönetimi mecburiyet içermeyen temalarda kullanılmamalı.

- Programın çalışma esnasında dinamik bellek için ayrılan bellekte bir kısım var. Heap (free store) 
olarak adlandırılıyor. 
- Otomatik ömürlü nesnelerin tutulduğu bellek alanına stack (yığın) segment deniyor. 

- Dinamik bellek yönetiminde bir (heap) alanın bir nesne için belli bir süreliğine yer ayırılması 
(allocate), nesnenin ömrü bittiğinde o bellek alanının tekrar serbest hale gelmesine (free, deallocate) deniliyor.

  	
- malloc -> programın çalışma (process) esnasında bir bellek alanı ihtiyacı olduğunda kullanılan 
fonksiyon.
- calloc -> malloc la benzer işi yapıyor ancak farkı, calloc'un parametrik yapısı biraz daha farklı
malloc bellek bloğunun kullanımı bittikten sonra bellek bloğunu garbage value haliyle bırakırken
calloc bellek bloğunun kullanımı bittiğinde o bellek bloğunu sıfırlayarak veriyor.
- realloc -> malloc veya calloc ile yer ayırılan bir bellek bloğunu kimi zaman yeterli olmadığını
öngörerek büyütmek istiyoruz. Ancak tuhaf olsada ayrılan bellek bloğunun fazla gelmesi durumunda
kullanılmayan kısmını geri vermek için de realloc kullanıyoruz. 
- free -> bellek bloğunun kullanılma durumu bittiğinde geri iade edilmesi için kullanılan fonksiyon
  
  
  	void* malloc(size_t n);
	
  - Birinci parametre kaç byte'lık bir bellek bloğuna ihtiyacınız olduğunu giriyorsunuz.
  - Geri dönüş değeri de bu bellek bloğunun adresi. Elde edilememesi durumunda NULL pointer dönüyor.
  - Yani sonuçla dinamik bellek bloğunun da bir sınırı olduğu unutulmamalı. Yer kalmaması durumunda
  NULL pointer döndürüyor. Ve malloc' a bir çağrı yapıldığında mutlaka geri dönüş değeriyle test
  edilmelidir.
  
  
 ``
  	size_t n;  // malloc'un parametrik yapısı size_t olduğu için n nesnesi size_t türünde bildirildi.
	
	printf("kac elemanli bir dizi\n");
	scanf("%zu", &n);

	int* pd = (int*)malloc(n * sizeof(int));

	if (pd == NULL) {
		fprintf(stderr, "bellek yetersiz\n");
		exit(EXIT_FAILURE);
	}
	set_array_random(pd, n);
	print_array(pd, n);

	free(pd);

``
- Daha idiyomatik bir yazım biçimi:

``
	size_t n;
	int* pd;

	printf("kac elemanli bir dizi\n");
	scanf("%zu", &n);

	

	if ((pd = (int*)malloc(n * sizeof(int))) == NULL) {
		fprintf(stderr, "bellek yetersiz\n");
		exit(EXIT_FAILURE);
	}
	set_array_random(pd, n);
	print_array(pd, n);

	free(pd);
``

- Burada bellek bloğunu malloc ile ayırdığımızda çöp değerden kurtarmamız gerektiği unutulmamalıdır.
- memset ile belleği çöp değerden temizleme işlemi:

``
	size_t n;
	int* pd;

	printf("kac elemanli bir dizi\n");
	scanf("%zu", &n);

	

	if ((pd = (int*)malloc(n * sizeof(int))) == NULL) {
		fprintf(stderr, "bellek yetersiz\n");
		exit(EXIT_FAILURE);
	}
	
	memset(pd, 0, n * sizeof(int));
	print_array(pd, n);

	free(pd);
``

 
- Dikkat!   ardışık yapılan malloc çağrıları edinilmiş bellek bloklarını büyütmek zorunda değildir.
asla daha önce edinilmiş bir bellek bloğunu büyütmek için malloc işlevini çağırmayın.


  
  	void free(void *vp);
	
- Daha önce edinilmiş bellek bloğunun adresini, free fonksiyonuna parametre olarak gönderirseniz.
 free fonksiyonu o bellek bloğunu geri veriyor. Yani o bellek bloğunu kullanılma potansiyeline 
 sokuyor.
 - Dinamik belleği kullanacağınız işlem bittiğinde free fonksiyonu çağırılmadan devam edilmesi
 sık yapılan hatalardan biridir. Yani orası sizin kullanımınızdan çıksa dahi hala bloke edilmiş 
 durumda kalır. Dolayısıyla bellek bloğunu geri vermemek yapılabilecek en kaba hatalardan birisidir.
 - memory leakage (bellek sızıntısı)  bellek bloklarının gereksiz yere yer tutularak doldurulması.

- Şimdi şöyle bir soru geliyor akla. Peki dinamik bellekte yer ayırt edip programın sonuna kadar
kullanacaksam ben yine de programın sonunda free ile bellek bloğunu geri iade etmeme gerek var mı?
Böyle bir gereklilik söz konusu değil ancak kodlama disiplini açısından free edilmesi daha elzemdir.

- Dangling pointer: Siz bellek bloğunu tuttuğunuz adresi atamış olduğunu pointerı, bellek bloğunu
free ettiğinizde, bu kullanılan pointer garbage value'de kalır. Yani sizin o pointer'ı içerik olarak
kullanmamanız gerekir. Ancak içerisine başka bir atama yaptığınızda kullanım söz konusudur.


- free fonksiyonuna dair yapılan hatalar:
	- Asla dinamik bellek fonksiyonlarıyla elde *edilmemiş* olan bellek bloklarını free etme 
	girişiminde bulunmayını. (UB)
			
			char str[100];
			
			char *p = str;
			
			//
			free(p); // UB
	
	- free işleviyle dinamik bellek bloğunu küçültemezsiniz (UB)
			
			size_t n;
			int* pd;

			printf("kac elemanli bir dizi\n");
			scanf("%zu", &n);

	

			if ((pd = (int*)malloc(n * sizeof(int))) == NULL) {
				fprintf(stderr, "bellek yetersiz\n");
				exit(EXIT_FAILURE);
			}
			
			free(pd + n / 2);  // UB
	
	- free çağrısından sonra bellek bloğunun adresini tutmakta olan pointer geçersiz(invalid)
	pointer olur. pd'nin değeri NULL pointer olmaz. 
	- free edilmiş bir bellek bloğunun tekrar free edilmesi (UB)
  	- Dinamik bellek bloğunun free edilmemesi (memory leakage)

  
  
  - Şimdi bir örnek yapalım.

``
int icmp(const void* vp1, const void* vp2)
{
	return *(const int*)vp1 - *(const int*)vp2;
}

int get_median(const int* p, size_t size)
{
	int* pd = malloc(size * sizeof(int));
	if (!pd) {
		printf("bellek yetersiz\n");
		exit(EXIT_FAILURE);
	}
	memcpy(pd, p, size * sizeof(int));
	qsort(pd, size, sizeof(*pd), &icmp);
	return pd[size / 2];
}


int main()
{			
	int a[SIZE];

	randomize();
	set_array_random(a, SIZE);
	print_array(a, SIZE);

	printf("median = %d", get_median(a, SIZE));

}

``
- Şimdi siz yukardaki get_median fonksiyonunu bu şekilde tanımladığınızda free fonksiyonu ile 
kullandığınız belleği sonlandırmıyorsunuz. Ve siz bu fonksiyonu her çağırdığınızda yeni bir bellek
alanı açılıyor. Bu fonksiyonu belli bir sayıda çağırdıktan sonra belleğinizde yer kalmayacak
ve dinamik bellek kullanamayacaksınız.

  
  - Fonksiyonun doğru kullanımı:

``

int icmp(const void* vp1, const void* vp2)
{
	return *(const int*)vp1 - *(const int*)vp2;
}

int get_median(const int* p, size_t size)
{
	int* pd = malloc(size * sizeof(int));
	if (!pd) {
		printf("bellek yetersiz\n");
		exit(EXIT_FAILURE);
	}
	memcpy(pd, p, size * sizeof(int));
	qsort(pd, size, sizeof(*pd), &icmp);

	int retval = pd[size / 2];
	free(pd);
	return retval;
}
``

olmalıdır. 
  
  
  - Dikkat ! -> free fonksiyonuna NULL pointer gönderilmesi UB değildir. Ama herhangi bir işlev de
  yapmaz.
  
  
  - Bir de free fonksiyonunun kullanılmasında güvenlik söz konusu. Mesela siz diyelim malloc 
  fonksiyonu ile bir bellek bloğunu ayırt ettiniz, kullandınız ve işiniz bittiğinde free ettiniz.
  free ettiğinizde o adresteki veriler silinmiyor. Yani o bellek bloğunda başkalarının eline 
  geçmesini istemediğiniz bilgileri işliyorsanız o bellek bloğunu temizlemelisiniz. 
  Çünkü orası garbage value iken o bellek bloğundan okuma gerçekleştiğinde eski verilere 
  ulaşılabiliyor. Yani siz bu bilgilere başkasının erişmesini istemediğiniz taktirde o bellek 
  bloğunu free etmeden önce clear da etmelisiniz.  (memset fonksiyonu ile)

		pd = malloc(n * sizeof(int));
		
		// bellek kulanıldı ve iş bitti
		
		memset(pd, 0, n * sizeof(int));
		free(pd);
  
  
  - 20 tane bellek bloğu allocate ediyorsunuz ve her birinin büyüklüğü 1000 byte
  - 1000 tane bellek bloğu allocate ediyorsunuz ve her birinin büyüklüğü 20 byte	
  	- Yukarıdaki her iki durumda da toplam açısından bir fark yoktur ancak bir farkı arka planda oluşmaktadır da. Nedeni şu ki
  	Bu heap alanını kontrol eden bir algoritma var. O algoritmanın da kullandığı bir veri 
	yapısı var. Sonuçta onun da bir veri yapısı var kaydedilen bellek bloklarının adreslerini
	kaydedeceği bir alana ihtiyaç var. Dolayısıyla her malloc çağrısı bu veri yapısına bir giriş
	yapmak demek. Yani siz her bellek bloğunun adresini kaydetmek için ekstra bir bellek alanı 
	kullanıyorsunuz. Yukarıdaki iki durumdaki fark burada oluşuyor. Yani siz her tahsisat için
	bir ek bellek alanı kullandığınız için tahsisat sayısı ek kullanılan bellek alanını 
	arka planda etkiliyor. 
  	
  
 # Ders 43 Tarih 17 05 2021
 
 
  - Eğer bir pointer kullanılarak bir bellek bloğu kullanıldığında ve o bellek
  bloğuyla işimiz tamamlandığında o bellek bloğunu, kullanılan pointer aracılığı
  ile free ettiğimizde o pointerın artık bir nesne göstermediğini belirtmek
  için o pointera NULL pointer atanması programcılar tarafından güzel bir 
  alışkanlık olduğu söylenebilir.
  
  		free(pd); /*pd allocate edilmiş ve kullanımı tamamlanıp free 
				edilen bir bellek bloğu adresi*/
  		pd = NULL;
		

  
  - function wrapper (fonksiyon sarmalayıcısı)
		- Bir fonksiyonu doğrudan çağırmak yerine o fonksiyonu
		çağıran bir fonksiyon oluşturuyoruz ve oluşturulan fonksiyon
		ile çağırıyoruz. 

  	- Yukarıdaki kullanımda birden fazla tema mevcut.
  		- Augmentation --> arttırmak, çoğaltmak
  			- Yani fonksiyonun yaptığı işi yapan ama üzerine
  			ilave bir iş daha yapan bir fonksiyon tanımlanıyor.
		- Mesela malloc fonksiyonunu çağıran ama geri dönüş değerinin 
		NULL pointer olup olmadığını da kontrol eden bir fonksiyon 
		tanımlayalım.
		
``
void* checked_malloc(size_t n)
{
	void* pd;
	if ((pd = malloc(n)) == NULL) {
		fprintf(stderr, "bellek yetersiz\n");
		exit(EXIT_FAILURE);
	}
	return pd;
}

int main()
{
	printf("Bir dizi boyutu giriniz:\n");
	size_t n;
	scanf("%zu", &n);

	int* pd = (int*)checked_malloc(n * sizeof(int));

	randomize();
	set_array_random(pd, n);
	print_array(pd, n);

	free(pd);

	pd = NULL;

}
``


- Fonksiyon Wrapper'a bir örnek daha vermek gerekirse,
Diyelim ki _itoa() fonksiyonunun parametrik yapısını daha farklı şekilde 
kullanmak istiyoruz.
Mesela alışılmış fonksiyonlardan farklı olarak pointer parametre ikinci 
parametre olarak bildirilmiş. Biz bu parametrenin yerini değiştirelim.
Bir de diyelim ki bu fonksiyonu hep 10'luk sayı sistemi için kullanacağız.
Her fonksiyon çağrısında belirtmek istemiyoruz.
Hadi birlikte bir wrapper yazalım.

		char* itostr(char* pbuf, int val)
		{
			return _itoa(val, pbuf, 10);
		}
		
- Yukarıda gördüğünüz gibi function wrapper yapısını kullanarak istediğimiz 
parametrik yapıda çağırabileceğimiz hale getirdik.


#

 
- Bir fonksiyon düşünün, bu fonksiyon yaptığı işle ilgili bir dinamik nesne
oluşturuyor. Yani malloc la nesnenin yerini ayırıyor. Nesneye set ediyor ve bu 
nesnenin adresini döndürüyor. Sonuçta bir nesnenin adresini döndürüyor ama 
şimdiye kadar gördüğümüz fonksiyonlardan farklı olarak dinamik ömürlü bir
nesne adresi döndürüyor. 
Neden bu yapı önemli?
Çünkü böyle bir fonksiyonu çağıran kod şimdiye kadar hiç karşılaşmadığımız bir 
senaryo, bir nesne adresi alacak ama bunun dinamik ömürlü nesne olduğunu bilecek,
ve bu nesneyi kullandıktan sonra free edecek. Yani aslında fonksiyon bunu 
dökümantasyonda bunu bir şekilde belli edecek. 

- Yukarıdaki fonksiyonun en tipik örneği:
- string.h başlık dosyasında
		
		char* _strdup(const char* pstr);

- Verdiğiniz adresteki yazının bir kopyasını çıkartıyor ve kopya yazının adresini
döndürüyor. Ama kopyasını dinamik bir bellek bloğuyla oluşturuyor. Size gelen
bellek bloğunu işiniz bittiğinde free etmeniz gerekiyor. 
Bu ihtiyaç duyulan bir fonksiyon çünkü bazı durumlarda bir yazı üzerinde belli 
değişiklikler yapmamız gerekiyor ama yazının orjinalini bozmamak gibi de bir 
durum söz konusu olduğunda yazının kopyası üzerinde işlem yapabiliyoruz.
		
- Bir örnek verelim;

``
	
	char str[SIZE];

	printf("bir yazi girin: \n");
	sgets(str);

	// bu yazinin tersine ihtiyacımız var
	// ve bu yazının orijinalini de korumamız gerekiyor.

	char* pd = _strdup(str);

	_strrev(pd);
	
	printf("(%s) (%s)\n", str, pd);

	free(pd);
``
- Şimdi konuyu daha iyi anlayabilmek için _strdup fonksiyonunu kendimiz yazalım.

``
char* mystrdup(const char* p)
{
	char* pd = (char*)malloc(strlen(p) + 1);
	if (!pd) {
		fprintf(stderr, "bellek yetersiz\n");
		exit(EXIT_FAILURE);
	}
	
	return strcpy(pd, p);  // idiyomatik olarak
}
``


- Bir örnek yapalım. Bir fonksiyon aldığı iki adresteki yazıları, oluşturduğu dinamik bir bellek
bloğunda birleştirsin. 


``

char* strconcat(const char* p1, const char* p2)
{
	char* pd = (char*)malloc(strlen(p1) + strlen(p2) + 1);
	
	if (pd == NULL) {
		fprintf(stderr, "bellek yetersiz\n");
		exit(EXIT_FAILURE);
	}
	strcpy(pd, p1);
	strcat(pd, p2);
	
	return pd;
	// idiyomatik yazımı:

	//return strcat(strcpy(pd, p1), p2);
}

int main()
{

	char s1[SIZE];
	char s2[SIZE];

	printf("Birinci yaziyi giriniz: ");
	sgets(s1);
	printf("Ikinci yaziyi giriniz:  ");
	sgets(s2);

	char* pd = strconcat(s1, s2);

	printf("(%s) + (%s) = (%s)", s1, s2, pd);

	free(pd);
}
``
  
  
- Yukarıdaki örneklerde gördüğünüz üzere fonksiyonun geri dönüş değerinin dinamik bir bellek
bloğu olması sıklıkla kullanılabiliyor.

- Bir fonksiyonun geri dönüş değerinin dinamik bellek bloğu olup olmadığını nerden anlayabiliriz?
	- Fonksiyonun dökümantasyonundan. Eğer sizde böyle bir fonksiyon yazarsanız mutlak 
	dökümante etmelisiniz.
	

  
  - Mesela bir static oluşturulmuş fonksiyonumuz olsun. (sık yapılan bir hatadır.)
	**dikkat örnekten sonraki açıklamaya bak

``
char* get_name(void)
{
	static char buffer[SIZE];

	printf("Bir isim girin: ");
	sgets(buffer);

	return buffer;
}

int main()
{
	char* p[3];

	for (int i = 0; i < 3; ++i) {
		p[i] = get_name();
	}

	for (int i = 0; i < 3; ++i) {
		puts(p[i]);
	}
}

``
- Yukarıdaki fonksiyonda ekrana hep son girilen değer yazılır. Çünkü burada adres tutulduğu için
siz hep static bir dizinin adresini tutuyorsunuz ve static dizi en son ne yazıldıysa belleğinde 
o yazıyı tutuyor. Ekrana o static diziyi yazdırmaya kalktığınızda ise hep aynı yazılıyor.


``
char* get_name(void)
{
	static char buffer[SIZE];

	printf("Bir isim girin: ");
	sgets(buffer);

	char* pd = (char*)malloc(strlen(buffer) + 1);
	if (!pd)
		return NULL;  // dinamik bellek bloğu döndürüldü

	return strcpy(pd, buffer);
}

int main()
{
	char* p[3];

	for (int i = 0; i < 3; ++i) {
		p[i] = get_name();
	}

	for (int i = 0; i < 3; ++i) {
		puts(p[i]);
	}

	for (int i = 0; i < 3; ++i) {  // Burada da elde edilen her yazı için
									// free fonksiyonuyla bellek iadesi söz konusu
		free(p[i]);
	}
}

``
  
  
- Bir pointer dizi allocate nasıl edebiliriz.
		
		int n;
		
		// code
		
		int** pd = (int**)malloc(n * sizeof(int*)); // türler değişti.
		

- Bir örnek:

- Mülakatta sorulabilecek sorulardan biri:
- Çok boyutlu dinamik dizi oluşturmaya dair

``
// dinamik bir matris oluşturmak
	size_t row, col;

	printf("matrisin sutun ve satir sayisini giriniz:\n");
	scanf("%zu%zu", &row, &col);

	int** pd = (int**)malloc(row * sizeof(int*));
	if (!pd) {
		printf("bellek yetersiz\n");
		exit(EXIT_FAILURE);
	}

	for (size_t i = 0; i < row; ++i) {
		pd[i] = (int*)malloc(col * sizeof(int));
		if (!pd[i]) {
			fprintf(stderr, "bellek yetersiz\n");
			return 1;
		}
	}

	randomize();

	for (size_t i = 0; i < row; ++i) {
		for (size_t k = 0; k < col; ++k) {
			pd[i][k] = rand() % 10;
		}
	}

	for (size_t i = 0; i < row; ++i) {
		for (size_t k = 0; k < col; ++k) {
			printf("%d ",pd[i][k]);
		}
		printf("\n");
	}

	for (size_t i = 0; i < row; ++i) {
		free(pd[i]);
	}

	free(pd);
``
- Yukarıdaki yapı için dezavantaj olarak, normal pointerla yapılan çok boyutlu diziye göre,
bellekte daha fazla boyut alıyor.
- Bu gerçek anlamda bir çok boyutlu dizi değil. 
Mesela birinci dizinin içerisindeki;
		- son eleman, 
		- bir sonraki dizinin ilk elemanını göstermiyor.
 - Aşağıdaki kodu çalıştırdığınızda pointerın gösterdiği noktaya ilerleyerek bakarsanız eğer,
 pointer ikinci satıra geçtiğinde gösterdiği değerler UB oluyor.
 ``
 	size_t row, col;

	printf("Satir ve sutun sayisi giriniz: ");
	scanf("%zu%zu", &row, &col);

	int** pd = (int**)malloc(row * sizeof(int*));

	if (!pd) {
		fprintf(stderr, "bellek yetersiz\n");
		exit(EXIT_FAILURE);
	}

	for (size_t i = 0; i < row; ++i) {
		pd[i] = (int*)malloc(col * sizeof(int));
		if (!pd[i]) {
			fprintf(stderr, "bellek yetersiz\n");
			exit(EXIT_FAILURE);
		}
	}

	randomize();

	for (size_t i = 0; i < row; ++i) {
		for (size_t k = 0; k < col; ++k) {
			pd[i][k] = rand() % 10;
		}
	}

	for (size_t i = 0; i < row; ++i) {
		for (size_t k = 0; k < col; ++k) {
			printf("%d ", pd[i][k]);
		}
		printf("\n");
	}


	int* ptr = pd[0];
	int n = row * col;

	while (n--) {
		printf("%d", *ptr++);
		_getch();
	}

	for (size_t i = 0; i < row; ++i) {
		free(pd[i]);
	}


	free(pd);

	
 ``
  
 - Aşağıda ise farklı bir yapıda dizi tanımlıyoruz.

``
	size_t row, col;

	printf("matrisin satir ve sutun sayisini giriniz:\n");
	scanf("%zu%zu", &row, &col);

	randomize();

	int* pd = (int*)malloc(row * col * sizeof(int));
	if (!pd) {
		fprintf(stderr, "bellek yetersiz\n");
		exit(EXIT_FAILURE);
	}

	// şimdi matrisin bir elemanına erişmek için aritmetik hesaplama gerekiyor.
	// Yani siz pd[0][0] diye bir erişim sağlayamazsınız.
	// Yani aşağıda siz tek bir dinamik dizi oluşturup sonrasında elemanlarına ulaşıyorsunuz.
	for (size_t i = 0; i < row; ++i) {
		for (size_t k = 0; k < col; ++k) {
			pd[i * col + k] = rand() % 10;

		}
	}
	for (size_t i = 0; i < row; ++i) {
		for (size_t k = 0; k < col; ++k) {
			printf("%d", pd[i * col + k]);
		}
		printf("\n");
	}
	printf("-------------------------------------");
	free(pd);
	
``
 
- Yukarıdaki yapının ise bir öncekine göre avantajı daha az bir bellek bloğu kullanmamız oldu.



- Dinamik bellek ile bir başka çok boyutlu dizi oluşturulması:

``
	size_t row, col;
	printf("satir ve sutun sayisi giriniz:\n");
	scanf("%zu%zu", &row, &col);

	int* pd = (int*)malloc(row * col * sizeof(int));

	if (pd == NULL) {
		fprintf(stderr, "bellek yetersiz\n");
		exit(EXIT_FAILURE);
	}

	randomize();

	int** pp = (int**)malloc(row * sizeof(int*));
	if (pp == NULL) {
		fprintf(stderr, "bellek yetersiz\n");
		exit(EXIT_FAILURE);
	}
	
	for (size_t i = 0; i < row; ++i) {
		pp[i] = pd + col * i;
	}

	for (size_t i = 0; i < row; ++i) {
		for (size_t k = 0; k < col; ++k) {
			pp[i][k] = rand() % 10;
		}
	}


	for (size_t i = 0; i < row; ++i) {
		for (size_t k = 0; k < col; ++k) {
			printf("%d", pp[i][k]);
		}
		printf("\n");
	}
	printf("----------------------------------\n");

	free(pd);
	free(pp);
``

- Bir mülakat sorusu:
	- Ekrana dinamik bellek bloğu için ayrılacak int  boyut giriliyor.
	- Ya ekrana 0 değeri girilirse ne olur?
	
	
			a) NULL pointer döndürür.
			b) NULL pointer olmayan bir adres olabilir.
			// yukarıdaki a ve b seçeneklerinin dereference edilmesi UB olur.
			// a ve b seçeneklerinde adreslerin free işlevine gönderilmesi tanımlıdır.


- calloc fonksiyonu:

			void *  calloc(size_t n, size_t sz);
			
- malloc'un tek bir parametresi vardı. 
- Oysa Callocta birinci parametre kaç tane nesne için yer ayırdığım,
- ikinci parametre ise sizeof değerinin ne olduğu oluyor. 

	- Yani 100 elemanlı bir int dizi için malloc çağrısı;
			
			int* p = (int*) malloc(100 * sizeof(int));
	- iken calloc için;

			int* p = (int*)calloc(100, sizeof(int));
	- oluyor.
	- 
- malloc ile calloc'un ikinci farklılığı ise elde ettiği bellek bloğunu sıfırlıyor oluşudur.
	- Yani malloc bellek bloğunu çöp değeriyle alırken calloc sıfırlayarak alıyor.
  
  
``
	size_t n;
	scanf("%zu", &n);

	int* pd = (int*)malloc(n * sizeof(int));

	if (!pd) {
		printf("bellek yetersiz\n");
		return 1;
	}

	int* pp = (int*)calloc(n, sizeof(int));

	if (!pp) {
		printf("bellek yetersiz\n");
		return 1;
	}

	printf("malloc cagrisi\n");
	print_array(pd, n);

	printf("calloc cagrisi\n");
	print_array(pp, n);
``
  
  
  
  - realloc fonksiyonunu inceleyelim:
  	
		void* realloc(void *vp, size_t newsize);
		
- Birinci parametresi büyütme/küçültme işleminin yapılacağı bellek bloğunun adresi,
- İkinci parametresi bellek bloğunun yeni boyutu (yani büyütme miktarı değil)
- Geri dönüş değeri yine başarısızlık durumunda NULL pointer, başarılı olursa 
bellek bloğunun adresi döndürülür. Ancak burda malloc ve calloc'dan farklı bir durum söz konusu.
Geri dönüş değerindeki adres çağrının yapıldığı adres olabildiği gibi olmayadabilir. Bu durum bellek
müsaitliğine göre değişir. Yani bellek müsaitsen aynı adresin sonuna ekleme yapıp aynı adresi 
döndürebilir. Ama bellek çok da müsait değilse bellek bloğunun adresini değiştirerek yeni bir 
adres de döndürebilir.

- realloc için bir örnek:


``
	size_t n, n_add;
	randomize();
	printf("kac tam sayi: ");
	scanf("%zu", &n);
	int* pd = (int*)malloc(n * sizeof(int));
	if (!pd) {
		printf("bellek yetersiz\n");
		return 1;
	}
	set_array_random(pd, n);
	print_array(pd, n);
	printf("kac tam sayi daha ilave edilmesini istiyorsun?\n");

	scanf("%zu", &n_add);
	pd = (int*)realloc(pd, (n + n_add) * sizeof(int));
	if (!pd) {
		printf("bellek yetersiz\n");
		return 1;
	}
	
	set_array_random(pd + n, n_add); /*set_array fonksiyonunu bu şekilde 
									 çağırmamın sebebi baştaki kısıma zaten 
									 değer atanmıştı tekrar o değerleri 
									  değiştirmemem gerekiyor.*/
	print_array(pd, n + n_add); 

	free(pd);
``
  
  
  
- Realloc takes time!! 
	- realloc çağrısı yeni bir bellek biloğu allocate ettiği takdirde normale göre daha
	fazla zaman alır.
- Reallocation invalidates pointers!!!
	- pointerların gösterdiği adres boşta kalabilir yani realloc fonksiyonu bellek adresini
	taşımış olabilir.
	

- realloc çağrılarında 1. parametreye NULL pointer geçilirse realloc, malloc gibi davranır.


  
  - Bir örnek:

``
int ch;
	int ival;
	int* pd = NULL;
	int cnt = 0;

	randomize();

	for (;;) {
		printf("tam sayi girecek misiniz (e) (h) : ");
		while ((ch = _getch()) != 'e' && ch != 'h')
			; // null statement
		printf("%c\n", ch);
		if (ch == 'h')
			break;
		printf("tam sayiyi girin:   ");
		ival = rand() % 1000;
		printf("%d\n", ival);

		pd = (int*)realloc(pd, (cnt + 1) * sizeof(int)); // ilk değer de malloc gibi 
													// davranıyor.

		if (!pd) {
			printf("bellek yetersiz\n");
			return 1;
		}
		pd[cnt++] = ival;
	}
	if (!pd) {
		printf("tam sayi girmediniz\n");
	}
	else {
		printf("toplam %d sayi girdiniz\n", cnt);
		print_array(pd, cnt);
		free(pd);
	}
``
  
  
  # Ders 44 - 24.05.2021
  
  - Veri yapısı: Mantıksal bir ilişki içindeki verileri erişilebilir şekilde belirli bir mantık 
  altında bir arada tutan düzeneklere veri yapısı diyoruz. hash table(içerik tablosu), dinamik dizi,
  bağlı liste, ikili arama ağacı, graph. 
  - Fakat bunlardan en fazla kullanılan dinamik dizi. 
  
  - amortised constant time: normalde constant time ama arada öngörülemeyecek şekilde
   ek olarak bir maliyet daha çıkıyor.
  
  - Dinamik dizi veri yapısı, ögelerin dinamik olarak allocate edilmiş bir bellek alanında ardışık 
  olarak tutulduğu veri yapısı, Burada kapasite(capacity) ve size kavramı var.
  *allocate* edilen bellek blogunun öge cinsinden sayısına kapasite deniyor.
  *Fiilen* tutulmakta olan öge sayısına size deniyor. 
  - size, kapasiteye eşitken, eklenecek yeni bir öge için yer yok demektir. Bu durumda bir ekleme 
  talebinde reallocation (yani bellek bir yerden bir yere taşınıyor) gerçekleşiyor. Ama yeni 
  kapasite, eski kapasiteden bir buçuk veya iki kat gibi bir kat olarak daha büyük bir şekilde
  elde ediliyor. reallocation'ın ciddi bir maliyeti olduğu için realllocation'dan kaçınmak gerekiyor
  Çünkü reallocation zaman alıcı bir işlemdir. Hemde pointerlar geçersiz hale gelebiliyor.
  - Nasıl bundan kaçınabiliriz?
  	- Dinamik dizide örneğin maks 500 öge tutacağınızı önceden öngörüyorsak, baştan 500 tane 
  	ögeyi tutabilecek kapasiteyi baştan ayırma şansınız var. 
		- Bu işleme *reserve* adı veriliyor tipik olarak. 

- ödev: 
  		
			isim girecek misiniz (e) (h) 
			e
			ismi girin : mustafa
			isim girecek misiniz (e) (h) 
			e
			ismi girin : ezgi
			isim girecek misiniz (e) (h) 
			e
			ismi girin : ezgi // aynı isim girince uyarı verecek
			bu isim daha önce girildi.
			yeni isim girin: hakan
			
			ismi girin: name
			
			h yanıtı verildiğinde
			toplam 34 isim girildi. isimler alfabetik olarak ekran yazılcak
			programda (memory leak ) olmayacak.
			

Storage Class Specifiers (Yer Belirleyicileri)

- auto  -> çok az kullanılıyor artık yok sayabiliriz. 
- register
- extern
- static

Type qualifiers (modifiers) (tür niteleyicileri)

- const
- volatile
- restrict (C99)

# Storage Class Specifiers (Yer Belirleyicileri)
  
  - linkage (bağlantı)
 
 
		auto int x = 5; // bir değişkenin otomatik ömürlü olduğunu anlatır.
		
- auto anahtar sözcüğünü global alanda kullanımı sentaks hatası.
- auto keyword, parametre değişkeni olarak da kullanılamaz.  
  
  
  
- register: özetle modu kullanımdan düşmüş anahtar sözcük.
	- Derleyiciye bu değişkenin register'da (yazmaçta) tutulması ricasını istiyorsunuz.
	- register, işlemci de fiilen işlemi yapıldığı bellek alanı. 
	- Programın daha hızlı çalışması için ön bellek alanında tutulmasını istediğimizde 
	kullanıyoruz.
	- Neden kullanımı azaldı? Artık derleyiciler optimizasyonu çok iyi yaptığı için zaten 
	registerda tutulacak nesneleri belirleyip default olarak yapıyor.
	
	- register anahtar sözcüğü :
		- Yerel ve parametre değişkenleri için kullanılabilir.
		- Global değişkenler için kullanımı söz konusu değildir.
	- Register değişkenleri adres operatörünün (&) operantı olması geçersizdir.

			register int x = 10;
			int* p = &x; // hata
			

  - static anahtar sözcüğünün iki anlamı var:
	- global isim alanında kullanılması
	- blok içerisinde ayrı bir anlama sahip.

- Blok içerisinde kullanılan static keyword'un ne anlama geldiğini daha önce gördük.

		void func()
		{
			static int y = 20; // static yerel değişken
			int x = 10; // otomatik yerel değişken
		}
  
  
  
  - static yerel değişken ile global değişken arasındaki fark,
  	- static yerel değişkenleri sadece fonksiyon içerisinde olduğu sürece bellekte korunuyor
  	yani scope'u fonksiyon içerisinde tanımlı.
	- global değişkenlere her yerden ulaşabiliyoruz. Scope'u tüm program boyunca devam etmekte.
	- Yani ikiside static ömürlü iken scope'ları birbirinden farklı.



- Çağrılan bir fonksiyonun çağıran fonksiyona bir değer iletmesi için yollardan biri static bir 
yerel değişkenle değer döndürmek.
	- static yerel değişkenlerin adresini döndüren fonksiyonlar.
	
- rastgele bir password oluşturan fonksiyon.
	- fonksiyona bir adres gönderilir. parolayı o adresteki diziye yazılır.
	- Ben static yerel bir dizide parolayı oluşturup  ve onun adresini döndüreceğiz.
	- Ben her parola talebi için bir dinamik dizi oluşturup o dinamik dizinin
	adresini döndüren bir fonksiyon.
	
	
  
  - fonksiyona bir adres gönderilir. parolayı o adresteki diziye yazılır.
  Yukarıdaki yol için bir örnek:
  
``
char* create_password(char* p)
{
	size_t len= rand() % 8 + 4;

	for (size_t i = 0; i < len; ++i) {
		p[i] = rand() % 26 + 'a';
	}
	p[len] = '\0';
	return p;
}

int main()
{
	char buffer[100];

	randomize();

	create_password(buffer);
	
	printf("parola : (%s)\n", buffer);
}
``


Ben static yerel bir dizide parolayı oluşturup  ve onun adresini döndüreceğiz.
 - yukarıdaki durum için örnek:

``
char* create_password(void)
{
	static char buffer[100];
	size_t len= rand() % 8 + 4;

	for (size_t i = 0; i < len; ++i) {
		buffer[i] = rand() % 26 + 'a';
	}
	buffer[len] = '\0';

	return buffer;
}

int main()
{
	randomize();

	char* p = create_password();
	printf("(%s)\n", p);
	
}
``
Ben her parola talebi için bir dinamik dizi oluşturup o dinamik dizinin
	adresini döndüren bir fonksiyon.
	- Yukarıdaki tanıma bir örnek:
	
``
char* create_password(void)
{
	size_t len= rand() % 8 + 4;

	char* p = (char*)malloc(len + 1);  // sizeof(char) = 1 olduğundan.
	// dinamik bellek alanı kontrolü yapıldığı varsayalım.

	for (size_t i = 0; i < len; ++i) {
		p[i] = rand() % 26 + 'a';
	}
	p[len] = '\0';

	return p;
}

int main()
{
	randomize();

	char* ptr = create_password();


	puts(ptr);
	free(ptr);
	
}
``
  
  
- Bir fonksiyon kendisine daha önce yapılan çağrılardan elde ettiği verileri daha sonraki çağrılarda
kullanıyor.


  
- Bir mülakat sorusu:

	- Bir fonksiyon çağırın ve ekrana o fonksiyon kaçıncı kez çağırıldığını yazdırsın.

			void func(void)
			{
				static int cnt = 0;
				
				printf("%d kez cagirildi\n", ++cnt);
			}
			int main()
			{
				func();
				func();
			}


- İsimlerin bağlantı (linkage) kavramı:

	- Bir isim farklı kaynak dosyalarda aynı isimler kullanıldığında,
			    bu ismin aynı varlığı mı, yoksa farklı varlığı mı gösterdiğini 
			    belirleyen özelliğine isimlerin bağlantı özelliği denir.
		- external linkage: Farklı kaynak dosyalardaki iki aynı isim aynı varlığa işaret
				   ediyorsa external linkage denir.
		- internal linkage: Ama aynı isim farklı dosyalarda kullanılmasıyla birlikte, 
				    farklı varlıkları gösteriyorsa (fonksiyon ismi,değişken ismi vs)
				    internal linkage deniyor.
		- no linkage: Aynı dosyada bile her yerde bilinmeyen kullanılamayan isimlerin
		 bağlantı özelliğine de no linkage deniyor.
		 
  
 - Tanımlanan isimlerin, yani değişken veya fonksiyon ismi gibi, iki şekilde tanımlayabilirsiniz.
 	- Birincisi sadece tanımlanan dosyadan erişim sağlanacak şekilde. (iç bağlantı)
 	- İkincisi ise tüm kaynak dosyalardan erişim sağlanabilecek şekilde. (dış bağlantı)


			//global alanda
			int x = 10; // external linkage (dış bağlantıı)
			//Yani diğer kaynak dosyalarda da x ismi kullanıldığında 
			// yukarıdaki varlığı işaret edicek
			
			// aynı şekilde herhangi bir keyword kullanmadan tanımlanan fonksiyonlar
			// da external linkage oluyor.
			
			void func(int x)
			{
				
			}
			
- Eğer bir kaynak dosyada(.c) tanımı yapılmış bir değişkeni farklı kaynak dosyalarda
kullanmak istiyorsak;
		- O kaynak dosyada tanımı yapılır ve o kaynak dosyaya ilişkin başlık (.h) dosyasında
		da extern anahtar kelimesi ile bildirimi yapılmalı. Bu nesneye erişimin sağlanacağı
		kaynak dosyaya da ilgili başlık dosyası(.h) include edilmelidir.
		
		//nutility.c kaynak dosyasında yazılıyor.
		int g = 10;
		
		// nutility.h 
		extern g;
		
		// main.c 
		
		#include "nutility.h"
		
		int main()
		{
			printf("%d", g);
			g = 20;
			printf("%d", g);
		}
			
- Burada fonksiyon da extern anahtar kelimesi kullanılmasına gerek yoktur.
- Asla ve asla global bir değişkenin tanımı başlık dosyası içerisinde yapmayınız.
  
 
- Peki biz bir değişkenin sadece o kaynak dosyada kullanılması için nasıl bir tanımlama yapmalıyız?
	- Siz global alanda static değişkeni kullandığınızda bu değişken (iç bağlantı- internal 
	linkage) ait demek.
	
			static int g = 20; // internal linkage
			
			int main()
			{
				
			}
  
  - Yukarıdaki durum fonksiyonlar içinde geçerli. Yani siz bir fonksiyonu static anahtar kelimesiyle
  tanımlarsanız, o fonksiyon sadece o kaynak dosya içerisinde erişime olanak sağlıyor.
  
  
  
  - Global bir değişkenin birden fazla kaynak dosyada ismi ile kullanılmasını istiyorum.
  	- Bir kaynak dosyada tanımlayacaksınız.
  	- Başlık dosyasında extern bildirimini yapacaksınız.

  - Global bir değişkeni tek bir kaynak dosyada ismi ile kullanılmasını istiyorsak, diğer kaynak
  dosyalarda kullanılmamasını istemiyorsak;
  	- O kaynak dosya içerisinde 
  	
			static int g = 10; 
			// şeklidne tanımlama yapılır.
  	- Başlık dosyasına bir bildirim konulmaz.

	
  
  
  - Bir fonksiyonun birden fazla kaynak dosyada ismi ile çağırılabilmesini istiyorum.
  	- Bir kaynak dosyada tanımlanacak. Başlık dosyasında "extern" kelimesi kullanılması zorunlu
  	olmadan bildirimi yapılmalı.
	
  - Bir fonksiyonu tek bir kaynak dosyada çağırılmasını istiyorsak (diger kaynak dosyalarda 
  kullanılmasını istemiyorsak);
  		
		static void func(void)
		{
			
		}
	- Başlık dosyasına bildirim konulmayacak.
 - Yukarıdaki yapılara private function deniyor. Yani o fonksiyon sadece o kaynak dosyaya özgü.

# Ders 45 28.05.2021


- Diğer programlama dillerinde bir değişkeni sadece o kaynak dosyaya erişilebilir yapabilmek için
private sözcüğü kullanılıyor. Bizde şöyle bir hile yaparak bunu sağlayabiliriz.

		// kaynak dosyanın içerisinde yazılıyor.
		#define PRIVATE  static
		
		PRIVATE const int primes[] = { 2, 3, 4, 7 ... };
		
		// ilerde OOB konusunda sıkça kullanacağız.
		
		#define PUBLİC  
		
		// dışarıya açılan nesne için kullanım şekli.
		
- İnclude ettiğimiz birden fazla başlık dosyasından gelen isimler çakışırsa;
- Yani siz iki farklı başlık dosyası include ettiniz. 

		#include "rudility.h"
		#include "nudility.h"
- Yukarıdaki iki kaynak dosyada da aynı isimli değişken kullandınız.
Siz bu programı çalıştırmaya çalıştığınızda karşınıza linker hatası çıkacaktır.


- Bir projede dış bağlantıya açılmış isimler tek olmalı, çakışmamalı. Bu durum için
fonksiyonu veya o değişkeni kullanmanıza gerek yoktur. 

- Bu problemin önüne geçmek için başlık dosyasında bildirimler yapılırken isimlere başlık 
dosyasıyla alakalı tipik ön ek kullanılıyor.
	- Buna şöyle diyorlar:
	
			Global Namespace Pollution Problem
			

- C++ ve farklı dillerde, C'nin yapısından farklı olarak namespace tanımlayarak kendi içinde 
namespace oluşturabilirken, C'de sadece global namespace mevcut. Ek bir namespace tanımı 
yapamıyorsunuz.


- Bir de function overloading var. C'de bir fonksiyon ismini farklı iki fonksiyonda kullanamazken,
C++ gibi dillerde iki farklı parametrik yapıya ait fonksiyonu ayrı olarak tanımlayabiliyoruz.


- Bir mülakat sorusu:
		
	- Herhangi bir kaynak dosyanın içerisinde bir fonksiyon tanımlanmış ama bu fonksiyon aynı
	kaynak dosya içerisinde hiç çağırılmamış. Derleyicinin böylesi bir durumda bir uyarı 
	vermesi sizce olumlu olur mu bir fayda sağlar mı, anlamı olur mu?
		
			void func(int x) 
			{
				
			}
	- Fonksiyon yukarıdaki bir yapıda.
	- Cevap şu olmalı:
		
			Tabi ki uyarı mesajı vermemelidir. Bu fonksiyon görüldüğü üzere external 
			yapıda. static anahtar sözcüğü  olmadığına göre dışarıya açılmış bir 
			fonksiyon. O zaman bizim neden bu kaynak dosyada bu fonksiyonu çağırmamız 
			gereksin ki. Diğer modüller tarafından çağırılma ihtimali kesinlikle 
			unutulmamalıdır.
	
	- Eğer soru şu şekilde sorulursa;
	
			static void func(int x)
			{
				
			}
	- Yukarıdaki şekilde tanımlanması, bu fonksiyonun diğer kaynak dosyalardan çağırılması
	ihtimalini ortadan kaldırıyor. Bu sebeple derleyicinin uyarı mesajı vermesi bizim 
	yararımıza olacaktır.
	
			
  - Yani toparlarsak;

		static int x = 10; // x sadece bu kaynak dosyada kullanılabilir.
		static void func(int x)
		{
			//func fonksiyonu sadece bu kaynak dosyada kullanılabilir.
		}
		


- Geriye kalan 3 anahtar sözcüğü kaldı.

		// type qualifiers ( type modifiers)
		- const
		- volatile
		- restrict   C99 ( C++ da yok)


  
 - const anahtarı tekrar edelim:

- const correctness : C ve C++'da yazılan kodların kalitesini belirleyen kriterlerden en
önemlilerinden biridir.(const doğruluğu)
- const anahtar sözcüğünün kullanımı, sentaks açısından bir hata olmasa da semantik açıdan problem 
oluşturan kodlardır. Bu kritere göre const anahtar sözcüğü kullanılması gereken her yer de 
kullanılmış mı onu sorgulayan bir kriterdir.

		const int x = 10; // x hayata 10 ile geldi ve ömrü boyunca değeri 10 olucak.
		

- Value category
	- modifiable L value (değeri değiştirilebilen)
	- non - modifiable L value ( değeri değiştirilemeyen)

- Siz const bir değişken tanımlayıp değiştirmeye kalkarsanız alacağınız hata:

		expression must a modifiable lvalue
		
				- olacaktır. 
  
  
  - Neden const kullanmalıyız??
  	- Kendimize yardımcı oluyoruz. Öyle değerler  var ki değerleri değişmemesi gerekiyor.
  	Değiştirmeniz lojik bir hataya yol açıyor diyelim. Siz const kullandığınızda bu değerleri 
	sabitlemiş oluyorsunuz ve yanlışlıkla bile 
	değişme ihtimalini ortadan kaldırıyorsunuz. Yani const kullanarak bir nesne tanımlandığında
	o nesneyi bir şekilde değiştirmek istendiğinde sentaks hatası alırsınız.
	Mesela bir asal sayı dizisi kullandığınızı varsayalım. Bu dizinin değerlerinin hep sabit
	kalması gerekiyor. Eğer herhangi bir noktada bu değerlerden biri değiştirilirse bu durum 
	ciddi lojik hatalara yol açabilir.
	Yani kısaca lojik açıdan değeri değişmemesi gereken nesneleri const anahtar sözcüğü ile 
	tanımlarız.
	- İkincisi yazdığınız kodu okuyan kişiye de bilgi veriyorsunuz. Yani okuyan kişiye bu 
	verilerin değiştirilmemesi gerektiği bilgisini veriyorsunuz ve kodu okuyan kişi de 
	bu nesneyi ona göre kullanabiliyor.
		- Mutable : Değiştirilebilir.
		- İmmutable : Değiştirilemez. (C'de const)
	
			int const x = 10; // şeklinde kullanım da söz konusudur.
	- const anahtar sözcüğü bir de derleyicinin optimizasyonuna da yardımcı oluyor. 
	siz bir nesnenin değişmeyeceğini derleyiciye bildirdiğinizde derleyici de ona göre 
	bir optimizasyon seçerek daha verimli bir optime sağlıyor.
	
	
	- Asla, asla ve asla const bir değişkeni değiştirme girişiminde bulunmayınız.

			const int x = 10;
			
			int *p = (int*)&x;
			*p = 34; // UB
			
   	- Top level const (const pointer)

			int x = 10;
			int* const p = &x; 
			p = &y; // hata
			*p = 20; // doğru kullanım.

	- pointer to const (low level const)

			int x = 20;
			const int* p = &x;
			*p = 40 // hata
			p = &y // geçerli
			
  	- const pointer to const int
  		
			int x = 10;
			int y = 30;
			const int* const p = &x;
			*p = 30; // hata
			p = &y; // hata
			
	- set function, setter function, mutator function

		void func(T *p);
		// yukarıdaki gibi bir fonksiyon bildirimi gördüğümüzde
		// fonksiyona gönderilen adresteki nesnenin değerini değiştirmek için
		// bu fonksiyon çağırılacağı çıkarımı yapılmalıdır.
		
	- Şimdi çok tartışılan bir konuyu ele alalım. 
		- Bir fonksiyona int bir nesne gönderilsin. Bu fonksiyon çağrısı call by value 
		olduğu için aslında derleyici açısından da kodu okuyan kişi açısından da 
		bir fark teşkil etmiyor. Çünkü fonksiyona gönderilen nesne değiştirilmiyor. 
		Fonksiyona gönderilen nesne kopyalanıyor. Ve bu kopyalanan nesne değiştiriliyor.
		
		
  			void func(const int x);
			void func(int x);
			

  	- Geri dönüş değeri olarak kullanılması:

			const T *func(void);
			
  	- Yukarıdaki fonksiyon kullanıldığında geri dönüş değerinin adresini siz değiştiremezsiniz.
  	Yani size gelen geri dönüş değerini okuyarak ordaki nesneye erişim sağlarsınız ama o 
	pointerdaki adresi değiştiremezsiniz.
  
  
  			const int x; // sentaks hatası değil ama yanlış
			// çöp değeri değiştirmeyeceğim diyorsunuz.
			
			const int x = 20; // x'i burada sabit ifadesi olarak bildirsen de
			int a[x]; // x'in sabit ifadesi gereken yerlerde kullanımı sentaks hatası
			oluyor. 
  
  			// bir kaynak dosyanın içerisinde global alanda tanımlama yapılıyor.
			const int x = 10; /* const anahtar sözcüğünün kullanılması veya 
					   kullanılmaması iç veya dış bağlantı oluşunu etkilemiyor.
					   Yani yukarıdaki const int x nesnesi external(dış) 
					   bağlantıya açık.*/ 
  			static const int x = 10; // iç (internal) bağlantıya ait.
			
			
  
  
  # Volatile Keyword 
  
  - Şimdiye kadar bir değişkenin tanımlanmasından sonra o değişkeni bizim yazdığımız kodlarda
  değiştiğini gördük.
  		
				int x = 10;
				x = 20; // gibi
				func(&x); //fonksiyon x'i değiştirecek gibi
				

  - Öyle senaryolar var ki sizin yazdığınız kod değişkenin değerini  değiştirmese de, program 
  dışı kaynaklar bu değeri değiştirebiliyor. 
  	- Önceden belirlenmiş bir nesnenin adresine dışardan bir erişim ile ulaşılıp 
  	değiştirilebiliyor.
	- Buna kısaca program dışı kaynaklar tarafından değişkenin değiştirilmesi diyoruz.
	- Kesme(inturrupt) ile ilgili olabilir. Program akışı dışında oluşturulmuş bir durum bu.

- Eğer program dışı kaynaklar tarafından bir değişkenin değiştirileceğini derleyici bilmezse,
bir takım optimizasyonlar yapıyor. O bellekteki nesneye erişmek yerine onun daha önce register'da
tutulan değerini kullanabiliyor. Böylece programımızın lojik yapısında belli farklılıklar oluyor.

  - Mesela bir x nesnesi tanımlayalım. Sonra bu x nesnesiyle sonsuz döngüye girelim. 
  Bu durumda siz bu x değişkenini dışarıdan erişilebilir şekilde tanımlamazsanız, 
  x nesnesine dışarıdan erişilip değiştirilse bile derleyici x'in register'daki değerini kullanıyor
  ve sadece kaynak kodlara bakıyor. Bu durumda x değişkeni program dışı kaynaklar tarafından 
  değiştirilse de derleyici bunun farkına varamıyor.  
  
  - İşte böyle durumlarda nesneyi volatile anahtar kelimesi ile tanımlanır. Yani siz derleyiciye ve 
  okuyucuya diyorsunuz ki x değişkeninin değeri sen görmesende program dışı kaynaklar tarafından 
  değiştirilebilir.  Yani derleyiciye diyoruz ki x'i gördüğün yerde herhangi bir optimizasyon 
  yapmayacaksın ve x'in bellek alanına erişip, oradaki değeri tekrar get ediceksin. Yani x her 
  kullanıldığında optimize edilmeden gidip bellek alanına bakarak x'in değerinin okunmasını 
  derleyiciden istemiş oluyorsunuz. 
  
  - Çoğunlukla böyle (memory map) değişkenlerer pointerlar yoluyla ulaşılıyor. 
  - Mesela siz bir tanımlama yaptınız.

		int *p = (int*)0xba12;
		
  - Derleyici p pointerını her kullanımda belleğe gidip değerine bakmak yerine register'da tutup
  belleği açma işleminden optimize edebilir (yaygın kullanılan bir optimizasyon tekniği)
  
  - Ama siz volatile ile tanımladığınızda optimize edilmesini ortadan kaldırıyorsunuz ve derleyici
  her p pointer'ının kullanımında belleğe gidip bakıyor. 
  
  
  - volatile anahtar kelimesi de const'daki gibi konumu önemli:
  
  		volatile int* p = (int*)0xba12;
		*p --> volatile
		p --> volatile değil
		
		int* volatile p = (int*)0xba12;
		p --> volatile 
		*p --> volatile değil 
		
# restrict
- C99 ile standardlara eklendi .
- C++'da bu anahtar sözcük yok.
		
		func(int* restrictp, int* q); 
		// bu fonksiyona geçilen adreslerdeki nesnelerin aynı nesneyi gösterme ihtimali yok.
		
  
- Siz restrict anahtar sözcüğünü kullanmadan bir fonksiyonda adres üzerinden işlem yaparsanız,
derleyici o pointer'ın gösterdiği adresdeki nesnenin değişip değişmeyeceğinden emin olamadığı için
o nesne üzerinde bir optimizasyon yapamıyor. Yani o nesneyi gösteren başka bir pointer olabilir.
Ama siz restrict anahtar sözcüğüyle bunu belirttiğinizde artık derleyiciye garanti vermiş 
oluyorsunuz. Böylece derleyici optimizasyon yapabiliyor.
	- Burada siz fonksiyona verdiğiniz garantiye uymazsanız UB'ye yol açabilir. 
	Yani o fonksiyonda bir nesneyi iki farklı adres gösterirse siz bu verdiğiniz garantiyi
	çiğnemiş oluyorsunuz bu da derleycinin optimizasyonuna göre UB'ye yol açıyor.
	

# Ders 46 - 31 05 2021


# User - Defined Types (Programcı tarafından "kodla" oluşturulan türler)
	


- C dili türleri (data types) iki ana kategoriye ayırıyordu.
	- Basic types (temel türler), 'fundamental types', 'primitive types' da denilebilir.
		- Dil tarafından hazır gelen türler; int, double gibi..
	- User Defined Types
		- Dilin bazı araçlarını kullanarak kendi türümüzü kendimiz oluşturabiliyoruz.
		Bunun için belli bildirimler yapmamız gerekiyor ve üretimde gerçekten bu türler 
		çok sık kullanılıyor.
		Yani User Defined Types, dil ile hazır olarak gelmeyen ancak bir bildirim ile
		kullanılabilir hale getirdiğimiz türler olarak tanımlayabiliriz.
		
		
- User Defined Type'ı oluşturmak için 3 tane araç var:
	- Structures (yapılar)
	- Union (birlikler)
	- Enumarations (numaralandırmalar)



# Structures 

- Yapılar herşeyden önce problem domeninde ya da çözüm domeninde ki varlıkların yazılımsal olarak
 betimlenmesine onların, kod içerisinde temsil edilmesine yarıyorlar.
	- Örneğin matematikteki bir matris, ya da matematikte bir polinom birer yapı ile ifade 
	edilebilir.
	- Diğer taraftan bir dosya, bir resim, bir mp3 dosyası bir yapı ile ifade edilebilir.
	
- Diziyle yapının belli noktalarda benzerliği olsa da dizilerde elemanlar aynı türden olmak zorunda 
iken yapıda böyle bir zorunluluk söz konusu değildir.

	
- Bir yapıyı oluşturmamız için önce bildirimini yapmamız gerekiyor. Bu bildirim ile 
derleyici bu türün varlığından haberdar oluyor.
	- Structure declaration
	
```



		struct Data {
			int a, b, c;
			double dval;
		};
```
- structure tag denilen bir ıdentifier (yukarıda Data) 
- Yukarıdaki structure'ın içinde bildirilen isimlere 'structure members' denir.
- Bir yapının en az bir elemanı olmak zorundadır.

- Yukarıda oluşturulan türün ismi 'struct Data' olur. Yani sadece Data ismini kullanarak 
bir yapıyı kullanamazsınız. 


		struct Data {
			int a, b, c;
			double dval;
		};

		int main()
		{
			struct Data mydata; // Bir ya
		}
- Yukarıda kullanımı gösterilmiştir.
- Bir yapı türünün sizeof değeri (storage ihtiyacı) elemanlarının sizeof değerlerinin toplamı
kadardır. (İleride "alignment" hizalama konusunda eklemeler yapılacaktır.)

- Yukarıdaki bildirim yapıldıktan sonra mydata'nın türü 'struct Data' olur.



- Peki biz bu türü nasıl kullanıyoruz.

- Bu türden bir değişken tanımlanabilir, bu türden bir dizi tanımlanabilir, bir pointer 
tanımlanabilir, bir fonksiyonun geri dönüş türü olabilir.

			
			struct Data func(struct Data*);
			int main()
			{
				struct Data x;
				struct Data a[10];
				struct Data *ptr = &x; 
			}
  
  
- Peki yapı bildirimleri nerede yapılır?

	- Client (kaynak dosyanın dışından erişilebilir) kodları ilgilendiren bildirimler
	Başlık dosyasında yapılır. Yani diğer dosyalar tarafından erişilmesi istendiği taktirde 
	başlık dosyasında yapılır.
	 
	 
  		struct Data g; // yapılar global değişken olarak tanımlanabilirler.
		
		void func(struct Data p) // fonksiyon parametresi olabilirler.
		{
			struct Data x; // otomatik ömürlü bir değişken olabilirler.
			static struct Data y; // statik yerel değişken olabilirler.
		}
- Yani şimdiye kadar değişkenlerde kullanım alanlarının hepsini yapılarda da kullanabiliriz.


		// something.c kaynak dosyasının içinde 
		static struct Data g; // sadece bu kaynak dosyada kullanılabilir
		
		int main()
		{
			const struct Data mydata = { 1, 3, 5, 3.5 }
			// const olarak tanımlayabiliriz. // salt okuma amaçlı erişim
			// yazma amaçlı erişim söz konusu değil.
		}
		
  
 
- Derleyici bir yapı bildirimi gördüğünde o yapı için bir yer ayırmıyor. Çünkü
bu bir bildirim, tanımlama değil. Derleyiciye tür hakkında yani böyle bir tür olduğuna dair 
bilgi veriliyor.


  
- Peki yapının elemanları neler olabilir:

		struct Data {
			int x; 
			double y;
			int *p;
			int a[20];
			char str[40];
			int (*fp)(int); // bir function pointer olabilir.
			int b[2][5]; // iki boyutlu bir dizi de olabilir.
		}
- Peki diğer programlama dillerinden farklı olarak ne yok dersek;
	- Yapıların elemanı fonksiyon olamaz. Diğer programlaam dillerinde yapılara sınıf deniyor
	ve sınıfların içerisinde tanımlanan fonksiyonlara da method deniyor. 
	
	
- Yapıları yapı içerisinde kullanabiliriz:

		struct Data {
			int a, b;
		}
		
		struct Bata {
			double dval;
			struct Data data; // yapı içerisinde yapı kullanıldı.
		}
  
- Yapı nesnesinin elemanlarına erişim için;
	- member selection operators
		- 1. öncelik seviyesinde yer alan '.' ve '->' operatörleridir.
		- 1. öncelik seviyesi soldan sağa (left associative) olduğunu hatırlayalım.

- '.' dot operator (nokta operatörü)
- '->' arrow operator (ok operatörü)

- Yukarıdaki iki operatörün farkına gelecek olursak eğer;

		struct Data {
			int a, b;
			double dval;
		}
		
		int main()
		{
			struct Data mydata;
			mydata.a; // a ya erişim
			struct Data *ptr = &mydata;
			ptr -> a // pointerlardan a'ya erişim için kullanıldığında  yani adres 
		}

- Yani aslında ikisi de bir yapı nesnesinin elemanına erişmek için kullanılıyor.
Ama (.) için yapı nesnesinin elemanını operant olarak kullanıyoruz.
(->) için ise yapı nesnesinin adresini operant olarak kullanıyoruz.


  
- Nokta operatörü sentaksı;
	- Binary operator
	- Sol operantı bir yapı türünden nesne olmak zorunda.
	- Sağ operantı ise yapı nesnesinin sahip olduğu elemanlarından birinin ismi olmak zorunda.
	
	
			yapı_ismi.yapı_elemanının_ismi;
	
	
#

		int main()
		{
			struct Data mydata;
			int x = 10;
			mydata.a = 15; 
			// mydata.a ile x değişkenine yaptığımız herşeyi yapabiliriz.
			// Farkı ise derleyici sadece x için yer ayırırken yapı söz konusu
			// olduğunda derleyici yapıdaki tüm elemanlar için 
			// yer ayırıyor.
			
			++mydata.a; // nokta operatörünün öncelik seviyesi birinci seviyede olduğu
				    // için parantez ile önceliği belirtmemize gerek yoktur.
				    
		}
		

- Array decay yapılarda da geçerli.

		struct Data {
			int x, y;
			int a[5];	
		};
		
		int main()
		{
			struct Data mydata;
			
			int *p = mydata.a; 
			int *p2 = mydata.a[0]; // yukarıdaki gösterim ile bu aynı.
		}
			
 
- Peki yapı nesnesiyle biz neler yapabiliyoruz;

	- Yapı nesnesi bir ifade olarak kullanıldığında, sadece ve sadece 4 tane operatörün
	operandı olabiliyor.
		- nokta operatörü, sizeof operatörü, adres operatörü, atama operatörünün operandı 
		olabilirler ancak ve ancak aynı türden bir başka yapı nesnesi atanabilir.
	
			&mydata // bu ifadenin türü struct Data* olur.
  			struct Data *p = &mydata // gibi kullanım mevcuttur.
  			*p // mydata nesnesi demek
  
 - Yalnız bu atama operatörünün operantı olması konusunda şöyle bir incelik var.
  Siz aynı yapıdaki türleri birbirine atayabilirsiniz. Farklı yapıda aynı türden eleman içeren
  yapıları değil.
  
  		
			struct Data {
				int x, y;
			};
			
			struct Data2 {
				int x, y;
			};
			
			int main()
			{
				struct Data mydata;
				struct Data2 mydata2;
				
				mydata = mydata2; // Bu hatalı bir kullanımdır.
				
				struct Data mydata3;
				
				mydata = mydata3; // doğru kullanımdır.
			}
			
			
  
  - Bu durumun dizilerden farklı olduğuna dikkat çekmek lazım.
	- Dizilerde dizi ismiyle atama yaptığında array decay ile ilk elemanlar atanmış olur.
	- Yapılarda array decay söz konusu değildir yapılar uygunsa tüm elemanlar atanmış olur.
  
```
struct Data {
	int a, b;
	double dval;
};

int main()
{
	struct Data da; 
	da.a = 10;
	da.b = 12;
	da.dval = 3.4;

	struct Data db;
	db = da;
}
```
  
  
  
- Dizileri normalde atama operatörünün operantı olarak kullanamıyorduk (array decay)
Ancak bir yolu var. Dizileri yapı içinde kullanmak:
  
  
```
struct Array {
	int a[100];
};

int main()
{
	struct Array a, b;

	//codes

	a = b; // diziler birbirine kopyalanmış olacak.
}
```


  
- Biz bir yapıyı başka bir yapıya atamayı daha önce bildiğimiz fonksiyonlarla da yapabiliriz.

  
```
struct Data {
	int a, b;
	double dval;
};

int main()
{
	struct Data da; 
	da.a = 10;
	da.b = 12;
	da.dval = 3.4;

	struct Data db;
	memcpy(&db, &da, sizeof(struct Data)); 
}
```
  


- Yapı Nesnelerine İlk Değer Verme (İnitialization of Structure Object):


		struct Data mydata = { 10, 20, 3.4 }; // bildirimdeki sırayla ilk değerler eşlenir.
		
- Eğer ilk değer verilirken bir kaç eleman ilk değer verilir ve ilk değer verilmeyen elemanlar
olursa, ilk değer verilmeyen elemanlar dizilerdeki gibi 0 değerini alır.


 		struct Data mydata = { 0 }; // yapının tüm elemanları sıfır değerini alır.
		
		
- Yapılar bildirilirken yapının içerisinde bir ilk değer verme söz konusu değildir.


		struct Data {
			int x, y = 10; // hata
		};




- Yapının elemanı dizi olduğunda ve yapıya ilk değer verildiğinde küme parentezi içerisinde 
küme parantezi kullanılabilir.

  
  
```
struct Data {
	int x, y;
	int a[4];
	double dval;
	
};

int main()
{
	struct Data mydata = { 10, 20, {1, 2, 3, 4 }, 4.2 };
}

```
  
  
- Dizilerde oluduğu gibi structlarda da designated initialization kullanılailir.


```
struct Data {
	int x, y;
	int a[4];
	double dval;
	
};

int main()
{
	struct Data mydata = { .y = 76, .dval = 3.5, .a = { [2] = 25, [4] = 52 } };
}

```



- Struct'larda bildirimi yaptığınız yerde tanımlamak istediğinizde structun } ile bitimine
ismini de yazarak global alanda tanımlama yapabilirsiniz.

		struct Data {
			int x, y;
			double dval;
		}g = { 1, 2, 3, 4 }, ga; // g burada yapının ismi. İlk değeri verildi.
		// ga ise ilk değer verilmeden global alanda tanımlanan bir yapı olur.
		
		
		
- Yapı türünü bildirirken structure tag(yapı ismi)'ni kullanmadan bildirim yapılabiliyor.

		struct {
			int a, b, c;
		}x, y, z;
		// 3 tane yapı değişkeni kullanılarak yapı bildirildi ama structure tag kullaılmadı.
		



		
- Bir yapı aynı structure tag ile iki kez bildirimi (declaration) yapılamaz.

	
 
 

- Yapı Nesnelerinin Adresleri:
	- Pointerlar konusunda geçerli olan herşey Yapılar içinde geçerlidir.,


- Ok operatörü ( -> )

	- Binary infix bir operatör
	- Sol operantı bir yapı türünden adres olmak zorunda. Yani yapı gösteren bir pointer.
	- Sağ operantı ise sol operanttaki yapının içerisindeki elemanlardan birisi olmak zorunda.


```
struct Employee {
	int id;
	char name[20];
	char surname[24];
	double wage;
};

int main()
{
	struct Employee x = { 1234, "Furkan", "Aksu", 85.90 };

	struct Employee *p = &x;

	printf("%d %s %s %f\n", x.id, x.name, x.surname, x.wage);
	 
	(*p).id = 45; // id değiştirildi.
	p->id = 876; // yine id değiştirildi.
	strcpy(p->name, "Kayhan"); // name değiştirildi.
	strcat(p->surname, "Oglu");
	p->wage += 4.1;
	
	printf("%d %s %s %f\n", x.id, x.name, x.surname, x.wage);
}
```


#

```
struct Employee {
	int id;
	char name[20];
	char surname[24];
	double wage;
};

int main()
{
	struct Employee a[3]; // 3 elemanlı, elemanları yapı olan bir dizi.

	a[0].id = 5; // ilk yapının id sine 5 atandı.
	a->id = 5;  // array decay kullanılarak yukarıdaki işlem yapıldı.
	(a + 2)->wage = 4.5; // a[2].wage ile aynı anlama gelir.
	++(a + 2)->id; // id elemanını bir artırıldı.
}
```

  
# Ders 47 - 02.06.2021


- Yapılar ve typedef bildirimleri:

		struct Data {
			int a, b, c;
			double dval;
		};
		
		typedef struct Data MYDATA;
		 
# 
- Farklı bir tanımlanma şekli:

		typedef struct Data {
			int a, b, c;
			double dval;
		}x;
		
		int maint()
		{
			x mydata = { 1, 2, 3, 4.3 };
		}
  
- Aşağıdaki şekilde tanımlama yapıldığında siz sadece tür eş isimi ile o yapıya ulaşmanıza olanak 
veriyor.

		typedef struct {
			int a, b;
		}Data;
		
		int main()
		{
			Data mydata = { 1, 2 }; 
		}
		

# 


		typedef struct Data {
			int a, b;
		}*DataPtr; // burada tür eş ismini adresi olarak tanımlanmış
  
  
# 

		typedef struct {
			int a, b;
		}Data, *DataPtr;
		
		int main()
		{
			Data mydata = { 2, 4 };
			DataPtr p = &mydata;
		}
  
# 
- Aşağıdaki gibi bir typedef bildirimi ile bildirimi yapılan yapı türünden
yalnızca dinamik ömürlü nesne oluşturulabilir. Yani otomatik ömürlü ya da statik 
ömürlü değişken tanımlama olanağını vermez.

		typedef struct {
			int x, y;
		}*DataPtr;
		
		int main()
		{
			DataPtr  pd = (DataPtr)malloc(sizeof(*pd));
		}
  
  
- Yapılar ve Fonksiyonlar:

	
		struct Data {
			int x, y;
			double dval;
		};
		
		void f1(struct Data); // call by value
		// yukarıdaki fonksiyonu çağırmamız için struct Data türünden bir nesne gönderilmeli.
		
		int main()
		{
			struct Data y = { 1, 3, 2.4 };
			f1(y);
		}
		
- C'de parametresi yapı türünden olan fonksiyonlar sık görülmez. Çünkü call by value durumunda
bir kopyalama söz konusu olduğu için bir bellek bloğu kopyalanıyor ve bu da maliyeti artırıyor.

Bu yüzden call by reference daha yaygın kullanılır. 

		// input parameter
		void f2(const struct Data*); // get - getter - accessor
		// yukarıdaki fonksiyona yapının adresi gönderiliyor. Ve salt okuma amaçlı olduğu
		belirtiliyor.
		
		// output parameter
		void f3(struct Data *p);
		// yukarıdaki fonksiyon bildiriminde ise yine yapının adresi gönderiliyor ve 
		bu yapıda değişiklikler yapılacağı belirtiliyor.
		//setter - mutator
		

#


		struct Data {
			int x, y;
		};
		
		typedef struct Data* DataPtr;
		
		int main() 
		{
			struct Data mydata = { 2, 4 };
			const DataPtr ptr = &mydata;
			
			//struct Data *const ptr = &mydata; burdaki gibi olur türü.
			//const struct Data *ptr = &mydata;
		}
	

#

- Fonksiyonların geri dönüş değerlerinde yapı olma söz konusuna bakacak olursak;

		struct Data f1(???); // bir yapı olabilir.
		struct Data *f2(??); // bir yapı adresi olabilir. (en çok kullanılan)
		const struct Data * f3(???); // const bir yapı adresi olabilir.
		
		
- api -> application programmers' interface

- C tarzı kütüphaneler: Size verilen yapının elemanlarının kullanarak program yazdığınız kütüphaneler.
	- Birinci dezavantajı her bir elemanın ne anlama geldiğini dökümantasyondan bakılarak
	öğrenilmesi gerekiyor.
	
- OOP (nesne yönelimli programlama) tarzı kütüphaneler : Bu tarz kütüphanelerde yapının elemanını
bilmeniz gerekmiyor çünkü yapının elemanlarını siz hiç kullanmayacaksınız. Size verilen 
fonksiyonları çağırıyorsunuz. Yani siz aldığınız adresteki nesneyi elemanlarına erişerek kullanmak
yerine fonksiyonlara gönderiyorsunuz. Herşey fonksiyonlar yoluyla yapılıyor.  Yapı nesnesinin 
değerinin değiştirilmesi yapı nesnesinin değerinin elde edilmesi gibi yapı nesnesiyle alakalı 
bütün işlemler kütüphanenin size sunduğu fonksiyonlar ile yapılıyor. 
	- OOP tarzı yaklaşım daha sağlam siz çünkü elemanları bilmediğiniz için bozamazsınız da.
	Çağırdığınız fonksiyonlar erişecek yani siz erişmeyeceksiniz. Öğrenme kolaylığı var.
	- Yapının elemanlarını siz kullanmadığınız için ilerde yapının elemanlarında bir değişiklik
	yapıldığında sizin yazdığınız kodların değiştirilmesi gerekmeyecek.
	

# time.h Modülü

- Bir kütüphaneyi öğrenirken modülde belli türler öğrenilmesi gerekebiliyor.

		time_t -> typedef bildirimiyle oluşturulmuş türler
		// calender time (takvim zamanı) 
		// epoche -> orijin gibi bir nokta
		// derleyiciye bağlı olarak genellikle long long  türünün eş ismidir.

  		time_t x; // epoch'dan geçen saniye sayısı olarak ele alınacak.
		
- Burada tutulan değere göre tarih olarak hangi zamanda olduğu kıyaslanabilir.

- struct tm bu kütüphanede bulunan C tipi bi yapı türü.
- struct tm -> broken - down time (ayrıştırılmış zaman bilgisi)
- Yani time_t türüne bir saniye değeri atadığınızda bu saniye değerini epoch'a ekleyerek
hangi tarihde günde ve ayda olduğunu öğrenmenize yarayan bir yapı türü.

		struct tm {
			int tm_year; // tarihin yıl değeri ancak 1900 den sonra tuttuğu için
					// bulunulan elemana 1900 eklenmelidir.
			int tm_mon; // tarih in ay değeridir. 0 -> ocak, 1 -> şubat ...
			int tm_mday; // ayın gün değeri tutulur.
			int tm_wday; // ayınz gün değerini tutar. 0 -> pazar, 1 -> pazartesi...
			int tm_yday; // yılın kaçıncı günü olduğunu tutuyor. 0 -> 1 ocak değerini tutmuş olur.
			int tm_hour; // 0 - 23 arasında saat değerini tutuyor.
			int tm_min; // 22.03 için 3 olur
			int tm_sec; // direk olarak tutulur 45 -> 45. saniye
			int tm_isdst; // is daylight saving time ( gün ışığı tasarruf modu)
					// mevsime göre saatin ileri veya geri alınması.
					// eğer değeri -1 ise bu kullanılan sistemde bilginin
					// tutulmadığı anlamına geliyor.
					// eğer değeri 0 ise bu modda olmadığını gösteriyor.
					// eğer negatif değil ve sıfır dışında bir değerse şuan o modda olduğu anlamına geliyor.
			
		};
  
  
- time fonksiyonu çağırıldığı zaman çağırıldığı zamana göre time_t (calender time) değerini veriyor.
Yani epoch'dan geçen saniye sayısını veriyor.

			time_t time(time_t *ptr);
			
- Fonksiyona time_t türünden bir nesnenin adresi gönderilecek, bu adresteki nesne set edilecek 
 epoch'dan geçen saniye sayısıyla set ediliyor.  
  
  		time_t timer;

		time(&timer);

		printf("saniye = %lld\n", timer);
		
- Yukarıdaki kod yazılıp çalıştırıldığında ekrana epoch'dan sonra çalıştırıldığı zamana kadar 
kaç saniye geçtiği ekrana yazdırılır.

		printf("%lld\n", time(NULL));
		printf("%lld\n", time(0));
- Yukarıdaki gibi fonksiyona NULL pointer ya da 0 değeri gönderildiğinde ise direk olarak geri 
dönüş değeri epoch'dan geçen saniye sayını verir.

- Bu fonksiyonun en yaygın kullanım şekli elde ettiğimiz saniyeyi (calender time) insanı 
ilgilendiren forma sokmak. Bunu da localtime fonksiyonu ile yapıyoruz.
- localtime fonksiyonu calender time'ı broken time'a dönüştürüyor.

		struct tm* localtime(const time_t* p);
		
- Geri dönüş değeri bir yapı türünden adres.
- Fonksiyonun parametresi ise sizden okuma amaçlı time_t türünde bir nesnenin adresini istiyor.



- Şimdi bir örnekle inceleyelim: Program çalıştırıldığı zamanki tarih gün ve saat değerini ekrana
yazdırsın. 02 Haziran 2021 Carsamba 22:26:43 gibi..


```
time_t timer; // time_t türünden bir nesne oluşturuldu.
	time(&timer); // time fonksiyonuyla oluşturulan nesne set edildi.

	const char* const pmons[] = {
		"Ocak",
		"Subat",
		"Mart",
		"Nisan",
		"Mayis",
		"Haziran",
		"Temmuz",
		"Agustos",
		"Eylul",
		"Ekim",
		"Kasim",
		"Aralik"
	};
	static const char* const pdays[] = {
		"Pazartesi",
		"Sali",
		"Carsamba",
		"Persembe",
		"Cuma",
		"Cumartesi",
		"Pazar"
	};

	struct tm* p = localtime(&timer); /*Bir tm yapısının adresini tutan pointer 
									  oluşturularak bu pointerın içerisine
									  localtime fonksiyonuna gönderilen epoch'dan geçen
									  saniye değerini gönderip geri dönüş değeri 
									  atandı.*/
	printf("%02d %s %d %s %02d:%02d:%02d\n",
		p->tm_mday, pmons[p->tm_mon], p->tm_year + 1900, pdays[p->tm_wday],
		p->tm_hour, p->tm_min, p->tm_sec);

	// ekrana yazılan yazı
	// 04 Agustos 2021 Persembe 12:19:51
	
	printf("yilin %d. gunu\n", p->tm_yday + 1);
	
	if (p->tm_isdst < 0)
		printf("gun isigi tasarruf modu verisi yok\n");4
	else if (p->tm_isdst)
		printf("gun isigi tasarruf modundayiz\n");
	else
		printf("gun isigi tasarruf modunda degiliz\n");
		
	
```
 
 
 
  
# Ders 48 - 4 Haziran 2021 


- localtime fonksiyonun geri dönüş adresinin pointer olduğunu görüyoruz. Pointerlardan 
hatırlayacak olursak bir fonksiyonun geri dönüş değeri adres olduğunda şu soruyu sormamız 
gerekiyordu. Dinamik ömürlü bir nesnenin adresini mi döndürüyor yoksa statik ömürlü 
bir nesnenin adresini mi döndürüyor. Bunu dökümantasyondan elde etmemiz gerekiyor lakin
bazen dökümantasyon elimizde olmayabiliyor. Bunu aşağıdaki gibi teyit edebiliriz.

		time_t timer;
		time(&timer);
		
		for (int i = 0; i < 10; ++i) {
			printf("%p\n" , localtime(&timer);
		}
		
- Eğer yukarıdaki kodun sonucunda döngünün her turunda aynı adres ekrana yazdırılıyor ise 
 bu fonksiyonun statik ömürlü bir nesne döndürdüğü anlamına geliyor.
- Eğer her turda farklı adres ekrana yazdırılıyor ise dinamik ömürlü bir nesnenin adresinin 
 döndürdüğü anlaşılıyor.
  
  
 # valgrind, free unit test tools -> test yapan yardımcı programlar, ya da analiz yapan programlar
 
 
 - Bir de gmtime fonksiyonu var, localtime fonksiyonundan tek farkı saat bilgisini tüm dünya 
 saatine uygun olarak veriyor. çalışma şekli aynı.
 
 
 
 ```
 void print_date_time(const struct tm* p)
{
	
	static const char* const pdays[] = {
		"Pazar"
		"Pazartesi",
		"Sali",
		"Carsamba",
		"Persembe",
		"Cuma",
		"Cumartesi",
		
	};
	printf("%02d %s %d %s %02d:%02d:%02d\n",
		p->tm_mday, pmons[p->tm_mon], p->tm_year + 1900, pdays[p->tm_wday],
		p->tm_hour, p->tm_min, p->tm_sec);
}

int main()
{
	time_t timer;
	time(&timer);

	struct tm my_local_time = *localtime(&timer);
	struct tm my_gmtime = *gmtime(&timer);

	print_date_time(&my_local_time);
	print_date_time(&my_gmtime);
	
	
}
 ```
 
 
- Tarih ve zaman bilgisini standart ingilizce yazı olarak görmek isterseniz iki fonksiyon mevcut.

		char* ctime(const time_t *p);
		char* asctime(const struct tm *p);

- ctime için bir örnek:

		time_t timer;
		time(&timer);

		printf("(%s)", asctime(&timer));
		
 - asctime fonksiyonun tek farkı ise timer nesnesinin değil de yapının adresini istemesidir.
 
		time_t timer;
		time(&timer);

		struct tm x = *localtime(&timer);

		printf("(%s)", asctime(&x));
  
  
- strftime -> string format time fonskiyonu

		size_t strftime(char *pa, size_t size, const char *pf, const struct tm *p);
		
- Bu fonksiyon bir yazı oluşturucak ve sizin birinci parametreyle gönderdiğiniz adresteki dizide  oluşturucak.
- Fonksiyonun ikinci parametre gönderdiğiniz dizinin boyutu olacak.
- Fonksiyonun son parametresi yazıya dönüştürülecek tarih zaman bilgisini tutan değişkenin adresi
- Fonksiyonun 3. parametresi, formatlama bilgisidir.  Bu formatlama bilgisini reference kitaplardan ya da 
cppreference 'dan bakılabilir.
- Fonksiyonun geri dönüş değeri yazdığı karakter sayısı.

			char str[SIZE];
			time_t timer;
			time(&timer);
			struct tm* p = localtime(&timer);

			strftime(str, SIZE, "date: %A %B %Y", p); //"%A" gün bilgisini veren format
							// %B ise ay bilgisini veren format
							// %Y ise yıl bilgisini verir.
							
			printf("%s", str);


- strftime locale dependant bir fonksiyondur ileride değinilecek bu konuya.


  
  
- Şimdi clock fonksiyonuna bakalım.

		clock_t clock(void);
		
- Fonksiyonun geri dönüş değeri clock time dan kısaltma süre gösteren bir tür eş ismidir.
programın çalışmaya başlamasından yani main fonksiyonun çağırıldığı noktadan itibaren 
clock fonksiyonun çağırıldığı ana kadar ki geçen süreyi bize veriyor.	
	- clock_t türüne ingilizce de clock tick denir. Bu tick denilen olay saniye değildir.
	- Burada bir makro mevcut. "CLOCKS_PER_SEC" makrosu sizin sisteminizde bir tick'in kaç sn
	ye denk geldiğini ölçüyor.
	

```
	int a[SIZE];

	clock_t start = clock();

	set_array_random(a, SIZE);
	sort_array(a, SIZE);

	clock_t end = clock();

	printf("siralama bitti %f saniye \n", (double)(end - start) / CLOCKS_PER_SEC);
	getchar();
	print_array(a, SIZE);
```
  
- Yukarıdaki kodda kaç saniyede bir diziye rastgele eleman atanıp sıralandığının süresini buluyoruz.


- Bir gecikme fonksiyonu yazarak bu aradaki sürede hiçbir şey yapmadan programın beklemesini sağlamak.

```
void wait(double sec)
{
	clock_t start = clock();

	while ((double)(clock() - start) / CLOCKS_PER_SEC < sec)
		; // null statement
}

int main()
{
	for (int i = 0; i < 100; ++i) {
		printf("%d ", i);
		wait(0.5);
	}
}
```


- Standart olmayan ancak C programcılarının sevdiği bir fonksiyon var. Gün ay yıl değerinden 
hareketle haftanın gününü hesaplıyor.
	- Sakamuto algorithm

		int day_of_week(int d, int m, int y)
		{
			return (d += m < 3 ? y-- : y - 2, 23 * m / 9 + d + 4 + y / 4 - y / 100 + y / 400) % 7;
		}
		
- Bir örnek:

```
	static const char* const pdays[] = {
		"Pazar"
		"Pazartesi",
		"Sali",
		"Carsamba",
		"Persembe",
		"Cuma",
		"Cumartesi",

	};

	int d, m, y;
	
	printf("dogum tarihinizi (gun ay yil) giriniz: ");
	scanf("%d%d%d", &d, &m, &y);
	printf("%s\n", pdays[day_of_week(d, m, y)]);
```

  
 - Nesne yönelimli programlamayı C'de daha iyi anlamamız için tarih işlemleri ile ilgili
genel destek veren bir kütüphane oluşturacağız.
	- Yapının elemanlarını client kodun kullanmasını istemiyoruz. Yani kütüphaneden hizmet alan
	kodlar bizim başlık dosyasında bildirdiğimiz external fonksiyonları çağırarak işini görecek.
	Bunlar fonksiyon veya fonksiyonel makrolar olabilir.
	


# Ders 49 - 09.06.2021 



- Bu derste oluşturulan başlık dosyası ve test kodları Date dosyasının içerisinde verilmiştir.


- Complete types (tamamlanmış türler)
- İncomplete types (tamamlanmamaış türler)

- Complete type tanımı yapılmış türlerdir.  İncomplete type ise tanımı ya yapılmamış ya da sentaks'a
göre eksik tanım yapılmış türlerdir.

  
  		struct Yapi; // incomplete type
		// burada derleyiciye Yapi'nın bir struct olduğu bilgisi veriliyor ve
		// içerisindeki nesneler hakkında bilgi verilmiyor.
		
  
 - Bir yapı türünü belirli baplamlarda "incomplete type" olarak kullanabiliriz. 
  
- Incomplete type olarak bir yapıyı nerelerde kullanabiliriz.

		struct Data;
		
	- Fonksiyonların parametre veya geri dönüş değeri türü olarak kullanabilirsiniz.
	
		struct Data;
		
		strucet Data foo(struct Date); // gibi
		
	- Tür eş isimlerinde kullanılabilir. 
  
  		typedef struct Data Data;
  	
	- Global değişkenlerin extern bildirimleri yapılabilir. 
		
		extern struct Data gdata;
		
	- Bir pointer türü tanımlanabilir.

		struct Data;
		
		int main()
		{
			struct Data* ptr = NULL;
		}
	
- Incomplete type ile neleri yapamayız ?

	- Bir yapı türünden değişken tanımlamak: Derleyici bu değişken için yer ayırması gerekiyor.
	Bu yer ayırma işlemi için kaç byte'lık bir yer ayırması gerektiğini bilmesi gerekiyor.

		struct Data;

		int main()
		{
			struct Data x;
		}
	- Bir yapının elemanı incomplete type türünden olamaz.

		struct Data;
		
		struct Database {
			int x;
			struct Data d; // hata
		};
	
	- Aşağıdaki işlemler için yapı türünün complete type olması gerekir.
		- Yapı türünden değişken tanımlamak.
		- Yapı türünden pointer'ları :
			- * operatörünün operantı yapmak
			- -> operatörünün operantı yapmak.


	- sizeof operatörünün operantının complete type olması gerekir.

- Peki nerelerde bu incomplete type olarak yapıları kullanıyoruz?
	- Bir başlık dosyası oluşturulurkan mümkün olduğunda farklı başlık dosyalarının include 
	edilmesinden kaçınılır. 
	Bazı durumlarda başlık dosyası oluşturulurken diğer başlık dosyalarında bulunan 
	yapılar kullanılırken diğer başlık dosyaları include edilmeden incomplete type olarak o yapı 
	kullanılabilir.
	
			//data.h
			struct Neco;
			struct Ali;
			
			struct Neco* foo(struct Ali*); // gibi
			

	- Yukarıdaki durumda bu türleri include edilmeden incomplete type olarak kullanılabilir.



# Ders 50 - 11.06.2021


- Composition:

Bir türün elemanlarından birisinin başka bir türden olması, özellikle user-defined türlerden. 
Bunun C'deki karşılığı bir yapının elemanlarından birisinin başka bir türden olması.
  

- Bir yapının elemanı kendi türünden olamaz.

		struct Date {
			struct Data x; // hata. incomplete type türünde hala.
		};
- Ancak bir yapının elemanı başka bir yapı türünden olabilir.
	
		struct Data {
			int x, y;
			double dval;
		};
		
		struct Nec {
			int a;
			struct Data data;
		};
		
		int main()
		{
			struct Nec nec;
			
			nec.data.x = 15; // Data yapısındaki x'e 15 değeri atandı.
		}
		

- Bir yapının elemanının kendi yapısı olamayacağını belirtmiştik ancak bir yapının elemanı kendi 
 yapısını gösteren bir pointer olabilir. Sebebi ise bir pointerın sizeof değeri derleyicide sabitti.
 sizeof değeri belli olduğu için kendi adresini gösteren bir pointer olmasında bir problem yoktur.
 Buna "Self referential structure" deniliyor.
 
 		// Self Referential Structure
		
		struct Data {
			int x;
			//
			struct Data* p;
		};
		
- Yapı içinde yapı kullanımı için ilk değer verme şekilleri:

		struct Data {
			int x, y;
			double dval;
		};
		
		struct Nec {
			int i;
			struct Data data;
			double dval;
		};
		
		int main()
		{
			struct Nec nec = { 10, { 2, 4, 3.4 }, 3.21 };
			// küme parantezi içinde küme parantezi kullanılmaz ise sıradan 
			// yapı elemanlarını doldurur.
			
			// mesela sadece Data elemanına ilk değer verilmek istense 
			// designated initialize yapılarak
			struct Nec nec = { .data = { 10, 20, 4.5 } };
			// hatta yapının içindeki yapı için de designated initialize kullanılabilir.
			struct Nec nec = { .data = { .y = 40 } };
		}

		
- Bir örnek:

```
#define _CRT_SECURE_NO_WARNINGS

#include <stdio.h>
#include <string.h>
#include <ctype.h>
#include <stdlib.h>
#include <time.h>
#include <math.h>

#include "conio.h"
#include "Rutility.h"

#include "date.h"

#include "Student.h"
#pragma pack(1)
#define SIZE 10000


int scmp(const void* vp1, const void* vp2)
{
	return cmp_student((const Student*)vp1, (const Student*)vp2);
}

int main()
{
	size_t n;

	printf("kac ogrenci: ");
	scanf("%zu", &n);

	Student* pd = (Student*)malloc(n * sizeof(Student));
	if (!pd) {
		fprintf(stderr, "bellek yetersiz!");
		return 1;
	}

	for (size_t i = 0; i < n; ++i) {
		set_student_random(pd + i);
	}

	clock_t start = clock();

	qsort(pd, n, sizeof(*pd), &scmp);

	clock_t end = clock();

	printf("siralama bitti %f saniye\n", (double)(end - start) / CLOCKS_PER_SEC);

	(void)getchar();
	(void)getchar();
	for (size_t i = 0; i < n; ++i) {
		print_student(pd + i);
	}
	free(pd);
}

```
		 
  

- Self - referenced structure
	- Node (düğüm)
		- Aslında Node bir yapı. Kendisi bir veriyi tutuyor. Bunun dışında
		kendisi gibi Node'lara erişmenizi sağlayacak pointer ya da pointerlar tutuyor.
		
			struct Node {
				data
				struct Data* p;
				struct Data2* p;
			};
			
	- Böylece struct Node türünden nesneler, dinamik olarak allocate edildiğinde,
	bunların arasında bir bağlantı oluşturabiliyorum. 
	- Hangi veri yapıları bu Node'ları kullanıyor.
		- Linked list
		- Trees 
			- Özellikle binary search tree
		- Graph
		- Hash Table 
		
	
- Linked lists (bağlı liste) : Her bir eleman bir veri tutarken aynı zamanda bir sonraki elemanı gösteren pointerı
tutuyor. Son eleman NULL pointer'ı gösterir.

- Dynamic Array
	- Her bir eleman için o elemanın sizeof'u kadar yer ayırılıyor.
	- Dinamic bir dizi için allocate yapılırken bir malloc çağrısı yapılıyor.
	- İndex kavramı ile indexi bilinen elemana direk erişim sağlanabiliyor.
	- Elemanlara içerik olarak erişmek istersek eğer bir fark yok linked list ile dynamic
	 Arrayin
	- Eğer siz dinamik diziye bir ekleme yapmak istediğinizde bütün elemanları kaydırma 
	yapmak zorundasınız. Yani siz ne kadar çok eleman eklerseniz o kadar kopyalama yapmak 
	zorundasınız. Aynı işlem silme işlemi için de geçerli.
	- Siz bir sıralama algoritması kullandığınızda nesneleri kopyalayarak bir swap yapma 
	durumundasınız bunun dez avantaju bu neslerin büyük veri yapıları olabilir ve bu 
	da  maliyeti ciddi anlamda büyütecektir.
	- Önişlemci erişimi ile verilere işleme söz konusu olduğu için daha hızlı bir 
	kullanım söz konusu olabiliyor.
	
- Linked list
	- Sadece sizeof değeri kadar değil ek olarak bir de pointer için yer ayırılıyor.
	Yani Node denilen yapı hem içinde tutulacak değeri tutuyor hem de pointer'ı tutuyor.
	Böylece her veri için bir pointer daha fazla bellek alanına ihtiyacım var. 
	- Linked listde allocate yapılırken her bir Node için malloc çağrısı yapılıyor.
	- Burada herhangi bir elemana erişmek için sırasıyla diğer elemanlara erişerek devam
	etmeniz gerekmektedir.
	- Elemanlara içerik olarak erişmek istersek eğer bir fark yok linked list ile dynamic
	 Arrayin
	- Linked list'in avantajı ise konumunu bildiğimiz bir yerden ekleme veya silme işlemi 
	yapmakta. Linked list'te ekleme yapılağında bir düğüm oluşturulup istenilen noktadaki
	düğümlerdeki pointerları eklenilen elemana göre uyarlanarak herhangi bir kopyalama 
	işlemine gerek duyulmadan ekleme yapılabiliyor. Benzer işlem eleman silmek için de geçerli.
	- Singly linked list (tekli bağlı liste) sadece tek bir pointer tuttuğu için bir sonraki
	elemannı gösterdiğinden sadece ileriye doğru bir geçiş söz konusu. Geriye doğru geçiş 
	yapılamıyor. 
	- Siz bir sıralama algoritması kullandığınızda swap işlemi için sadece pointerları 
	swap ederseniz istenilen sonuca çok daha rahat ulaşabilirsiniz. Veriler çok büyük olsa 
	dahi o verilerin pointerlarını swap etmek maliyeti düşürecektir.
	- Linked list'lerde ön işlemciden verilere ulaşmak yerine direk bellekten verilere
	ulaşım söz konusudur.
	
	
  - Şimdi daha önceki oluşturduğumuz başlık dosyaları ile birlikte "studentlist.c", "studentlist.h",
  "Student.h" ve "Student.c" başlık dosyalarını ekleyerek aşağıda oluşturduğumuz test kodlarını
  çalıştırarak oluşturulan başlık ve kaynak dosyaları test edilecek. Bu testin uygulanabilmesi için
  bir önceki sayfadaki başlık ve kaynak dosyalar incelenerek anlamaya çalışılmalıdır.
  
  - İlk olarak yazılan test kodu bize bir listede rastgele 10 öğrenci oluşturulacak.
  Ve sonrasında bu öğrenciler linked list mantığıyla yazdırılacak.
  
  ```
  	Student s;

	randomize();

	for (int i = 0; i < 10; ++i) {
		set_student_random(&s);
		print_student(&s);
		push_front(&s);
	}
	printf("\n");

	printf("listede %zu ogranci var\n", get_size());
	print_list();

	make_empty();

	if (is_empty())
		printf("liste bos\n");

  ```
  
- İkinci test kodunda ise listeye random olarak kaç öğrenci ekleneceği soruluyor ekleme yapılıyor
ve ekrana yazdırılıyor.
 
 ```
 	size_t n;
	Student s;

	printf("listeye kac ogrenci eklenecek: ");
	scanf("%zu", &n);

	randomize();

	for (int i = 0; i < n; ++i) {
		set_student_random(&s);
		push_front(&s);
	}
	printf("listede %zu ogrenci var\n", get_size());
	_getch();
	print_list();
 ```
  
  
- Listeye kaç öğrenci ekleneceği bilgisi kullanıcıdan alınarak ekrana yazdırılır.
Sonrasında ise listedeki öğrenciler baştan birer bire her döngüde siliniyor.

```
	size_t n;
	Student s;

	printf("kac ogrenci: ");
	scanf("%zu", &n);

	for (size_t i = 0; i < n; ++i) {
		set_student_random(&s);
		push_front(&s);
	}

	while (!is_empty()) {
		printf("listede %zu ogrenci var\n", get_size());
		print_list();
		_getch();
		system("cls");
		pop_front();
	}
```
  


# Ders 51 - 14.06.2021


- Handle tekniği: Kütüphane oluştururken ulaşılması istenmeyen verilerin gizlenmesini sağlayan bir 
yol.


- Handle tekniği adlı dosyadan başlık ve kaynak dosyalara ulaşabilirsiniz.
  
- Fopen gibi standart fonksiyonlar handle tekniğine çok benzer şekilde yazılmıştır.


- Yapılara dair bir ayrıntı: Siz eğer bir yapıyı bir yapının içerisinde tanımlarsanız bu içeride 
tanımlanan yapının ömrü ana yapının ömrü kadar değildir. İstenilen yerde kullanılabilir.

			struct Neco {
				struct Data { // nested structure
					int a, b, c;
				}dx, dy, dz;
				
				int x, y, z;
			};
			
			int main()
			{
				struct Data mydata;
			}

 

# Alignment (Hizalama)

- Sizin değişkenleriniz bellekte tutuluyor. İşlemcinin bellekte bu değişkenlere erişebilmesi için
değişkenlerin türlerine bağlı olarak belirli adreslere yerleştirilmesi gerekiyor. 
Örneğin ikinin katları olan adreslere. Belirli değişkenler kolay erişilsin diye örneğin ikinin, 
dördün, sekizin katları olan adreslere yerleştiriliyor. Çünkü bu şekilde işlemci onlara daha kolay
daha düşük maliyetle erişiyor. 

- Her veri türü için "aligment requirement" değeri vardır. Yani işaretsiz tam sayı türünden 
bir değer ( 1 2 4 8 olabilir) 

- Alignment requirement c11 standartlarına kadar bu değeri elde etmek mümkün değildi. 
derleyicilerin eklentileri kullanılıyordu.  Mesela visual studio c11 standartlarını desteklemediği 
için __alignof denilen bir extention kullanılıyor. 

Ancak c11 standartları ile bu bir keyword haline geldi. _Alignof olarak.


	printf("char = %zu\n", __alignof(char));
	printf("short %zu\n", __alignof(short));
	printf("int %zu\n", __alignof(int));
	printf("long %zu\n", __alignof(long));
	printf("long long %zu\n", __alignof(long long));
	printf("float %zu\n", __alignof(float));
	printf("double  %zu\n", __alignof(double));
	
	
- Bu şekilde bir yerleştirme işlemi, işlemcinin o bellek alanlarına daha kolay erişmesini ve 
erişim maliyetinin daha düşük olmasını sağlıyor o yüzden böyle yerleştiriyor. 

- Yani toparlayacak olursak her tür için bir alignment requirement var ve o tür için belleğe 
yerleştirme sistemi o türün alignment requirement değerinin katlarına göre bellekteki adreslere
yerleştiriliyor. Yani int türünün alignment requirement'ı 4 ise bu türün belleğe yerleştiği
adres değerleri (pointerları) 4'ün katları oluyor.

- Alignment requirement daha çok bizi yapı türlerinde ilgilendiriyor. Bir yapıdaki nesnelerin 
belleğe yerleşimi yapı içindeki nesnelerin en büyük alignment requirement değerine göre 
yerleştiriliyor. 
		
		typedef struct {
			char c1;
			int i;
			char c2;
		}Data;
		
		int main()
		{
			printf("sizeof(Data) = %zu\n", sizeof(Data)); //12
		}


 - Yukarıdaki kodda yapının sizeof değerinin 6 olması beklenirken ekrana 12 yazdırıldığı 
 görülür. Sebebi ise alignment requirement'dır. Yukarıdaki yapının alignment requirement'ı 
 4 olduğu için char türünün sizeof'u 1 olmasına rağmen int türünün doğru alignment yerleşimi 
 yapılması için char türü 1 byte'ya yerleştirilip diğer 3 byte atlanır yani o kullanılmayan byte'lar
 boş bırakılır. Buna ingilizce olarak **padding** byte ya da **hole** denilir.
 
 - Yani siz bir yapının elemanlarını bildirme sıranız, yapı türünün sizeof değerini ve yapı 
 nesnelerinin içinde padding byte olup olmadığını ya da kaç tane padding byte olduğunu 
 doğrudan belirliyor. 
 - Peki yapı türünde padding byte bırakılmasının zararları nelerdir?
 	- Mesela yukarıdaki örnek için bellekte 12 byte yer ayırılırken sadece 6 byte'ı 
 	kullanılacaktır. 6 byte'ını hiç kullanmıyorsunuz. Yani siz büyük bir yapı oluşturduğunuzda
	bu yapının büyüklüğüne göre yarı yarıya bir bellek kullanımı zararına yol açacaktır. 
	- padding byte'ları engellemenin iki yolu var. 
		- Yapı bildirilirken ki sıralama padding byte'ları minimal düzeyde kalacak şekilde
		bildirilmeesi. 
				
				struct Data {
					int x;
					char c;
					char y;
				};
		
	- Yukarıdaki gibi yapı bildirildiğinde sizeof değeri 8 e düşer.
  	- Eğer bu şekilde bir minimalize edilme sözkonusu ise uyulması gereken kural
  	alignment requirement'ı büyük olandan küçük olana göre tanımı yapılması gerekmektedir.
	
	- Eğer biz hiç padding byte olmadan yerleştirilmesini istersek ;
		- Donanıma bağlı olarak böyle birşey mümkün olmayabilir. (mikroişlemcinin
		özelliğine göre
		- Derleyiciyi bu şekilde kod üretmeye zorlayabilirsiniz. Ama bu ekstra bir maliyet
		getirir. Mesela visual studio da böyle birşey mümkün.
		
			#pragma pack(1) // standart değil
			#pragma pack(2) // 2 nin katlarına yerleştirilmesi isteniyor.
			
	- Yukarıdaki pack durumunun iyi ve kötü yanları mevcut.
		- Yukarıdaki standart olmayan pragma kullanılırsa yapı nesneleri için bellekte
		daha az yer kaplanacak yani hafıza daha verimli kullanılmış olacak.
		Ama işlem maliyeti artacak. Burada tercihiniz bellekte az yer kaplaması ise yani
		kodun yavaş çalışması sizin için önemli değilse pragma kullanılabilir ama siz kodun
		hızlı çalışmasını istiyorsanız bellek önemli değil diyorsanız yapıda sıralı bir 
		şekilde tanımlama yapmak tercihiniz olabilir. 
	
  
 
 - Uyarılar:
 	- Bir yapının sizeof değerini bir yerder kullanacaksanız hiç bir zaman sabit kullanmayın
 	sizeof operatörünü kullanarak elde etmeye dikkat edin.
	- Yapılar söz konusu olduğunda pointer aritmetiği kullanılmamalıdır çünkü padding byte'lar
	söz konusu olduğunda istediğiniz sonucu elde edemezsiniz.
		
			typedef struct {
				char c1;
				int i;
				char c2;
			}Data;
			
			int main()
			{	
				Data mydata = { 1, 1249, 2 };
				char* p = &mydata.c1;
				int* ptr = (int*)(p + 1);
			}// yukarıda ptr i nesnesini gösteremez.
  
  
- İlla pointer aritmetiği kullanılmak istenirse stddef.h başlık dosyasında bir makro mevcut.

	 		#include <stdio.h>
			#include <stddef.h>
			
			typedef struct {
				char c1;
				int i;
				char c2;
			}Data;
			
			int main()
			{	
				offsetof(Data, i)		
			}
  - offsetof makrosunun ilk parametresi yapı türü, ikinci argüman o yapının elemanlarından birini
  yazıyorsunuz. Bu makronun açılması sonucu oluşan ifadenin türü size_t size 0, 1, 2, 4, 5 gibi
  bir tamsayı değer veriyor. Bu değer gönderilen yapı nesnesinin adresinden başlayarak kaç byte
  sonrasında yer aldığı değerini veriyor. 
  
  
  			#include <stdio.h>
			#include <stddef.h>
			
			typedef struct {
				char c1;
				int i;
				char c2;
			}Data;
			
			int main()
			{	
				Data mydata = { 1, 23432, 2 };
				
				char* p = &mydata.c1;
				
				(int*)(p  + offsetof(Data, i)) // i nesnesinin adresi.
			}
  			
  
  
 - Mülakatlarda sık sorulan sorulardan birisi offsetof makrosunun nasıl implemente edildiği.

 
  		#define moffsetoff(s, e)    (size_t)(&(((s*)0)->e))   
  


- İki adet yapının tanımlansın ve programcı bu yapıların eşitliğini test etmek istiyor olsun.
Burada yapı nesnelerinin == operatörünün operantı olamadığı göz önünde bulundurulmalıdır.
- Bu eşitliği kontrol etmek içi memcmp fonksiyonunu yazarsanız sonuç eşit değil çıkar.
    
                typedef struct {
                        char c1;
                        int i;
                        char c2;
                }Data;
                
                int main()
                {
                        Data x = { 1, 872, 2 };
                        Data y = { 1, 872, 2 };
                        
                        if (!memcmp(&x, &y, sizeof(Data)))
                                printf("esit\n");
                        else
                                printf("esit degil!!\n");
                }

- memcmp fonksiyonu kullanıldığında sonucun eşit çıkmamasının sebebi padding byte'ların çöp değerde 
olması.    

- Siz eğer memcmp fonksiyonu ile kıyaslama yapmak istiyorsanız eğer yapıları bildirdikten sonra memset
fonksiyonu ile tüm byte'ları sıfırlayarak sonrasında tanımını yapmanı gerekiyor.


                typedef struct {
                        char c1;
                        int i;
                        char c2;
                }Data;
                
                int main()
                {
                        Data x;
                        Data y;
                        
                        memset(&x, 0, sizeof(x));
                        memset(&y, 0, sizeof(y));
                        
                       x.c1 = 1;
                       x.i = 872;
                       x.c2 = 1;
                       y.c1 = 1;
                       y.i = 872;
                       y.c2 = 1;
                        
                        if (!memcmp(&x, &y, sizeof(Data)))
                                printf("esit\n");
                        else
                                printf("esit degil!!\n");
                }


# Ders 52 - 16.06.2021



- Union (Birlikler)

        typedef union Data {
                int x, y;
                double d;
                char s[12];
        }Data;


- Yapı nesnesi (alignement durumları sayılmazsa) elemanlarının sizeof değerlerinin toplamı kadar 
bir storage ihtiyacına sahipken, Birlik nesnesi en büyük elemanının sizeof'u kaç byte ise 
o kadar yer kaplıyor. 

                #pragma pack(1)
                
                typedef struct {
                        int i, j; //8
                        double d1, d2;//16
                }snec;

                typedef union {
                        int i, j; // 4
                        double d1, d2;// 8
                }unec;

                int main()
                {
                        printf("sizeof(snec) = %zu\n", sizeof(snec)); // 24
                        printf("sizeof(unec) = %zu\n", sizeof(unec)); //8
                }
                
- Birliklerin tüm elemanlarının adresleri aynıdır. Bir birlik nesnesinin adresi ile elemanlarının 
adresleri aynı. Birlik elemanları aynı bellek alanını paylaşıyorlar.

```
typedef union {
    char c;
    int x;
    double d;
    char str[12];
}unec;

int main()
{
    printf("sizeof(unec) = %zu\n", sizeof(unec));
    unec nec;

    printf("&nec     = %p\n", &nec);
    printf("&nec.c   = %p\n", &nec.c);
    printf("&nec.x   = %p\n", &nec.x);
    printf("&nec.d   = %p\n", &nec.d);
    printf("&nec.str = %p\n", &nec.str);//array decay
}

```

- Yukarıdaki kod çalıştırıldığında tüm adreslerin aynı değerde olduğu görülür.


- Bir hatırlatma: ! mğlakatta karşına çıkabilir.

                       
                int a[10]= { 0 };
                
                //&a[0] ---türü---> (int*)
                //&a    ---türü---> int (*)[10]

- Birlik nesnelerinin elemanlarına ilk değer verilirken dikkat edilmesei gereken husus aynı adrese 
yazıldığı için bir nesneye ilk değer verildiğinde diğer nesnelere de ilk değer verilmiş oluyor. 
Bu durumda yapılardaki gibi bir ilk değer verme söz konusu değil tek bir elemana ilk değer verilebilir.

                
                        typedef union {
                            char c;
                            int x;
                            double d;
                            char str[12];
                        }unec;
                        
                        int main()
                        {
                                unec nec = { 'A' }; // gibi
                                //designated initializer kullanılabilir.
                                //unec nec = { .str = "mustaf" };
                        }


- Bir veriyi iki farklı şekilde temsil etmek(birden fazla farklı şekilde)


- Bir örnekle inceleyelim:
        - Öyle bir tam sayı türü olsun ki, bu tam sayı türünden bir değişken 4 byte yer kaplasın.
        unsigned türden olsun. Fakat ben bu türü kullandığım sistemde 4 byte'ı tek bir tam sayı 
        olarak kullanabileceğim gibi düşük anlamlı ve yüksek anlamlı 2 byte'ı da ayrı ayrı kullanabileyim
        yani hem 4 byte'ı bir bütün olarak kullanabiliyorum, hem de iki ayrı short 16 bitlik 
        değişken olarak kullanabiliyorum. 
        
        
                #define _CRT_SECURE_NO_WARNINGS
                
                #pragme pack(1)
                #include <stdio.h>
                #include <stdint.h>
                
                
                typedef struct {
                    uint16_t low_bytes;
                    uint16_t high_bytes;
                }Myint;

                typedef union {
                    uint32_t uval;
                    Myint m;
                }Utype;

                int main()
                {
                    printf("sizeof(Utype) = %zu\n", sizeof(Utype)); // 4 byte olur.
                }
                
- Yukarıda sizeof değeri görüldüğü üzere birliğin 4 olmaktadır. Yani siz birlikteki uval'ı 4 byte bir
nesne olarak kullabilirsiniz ya da Myint nesnesinden 2 byte nesneler olarak kullanabilirsiniz.

- Farklı yazımı:

                
                typedef union {
                    struct {
                        uint16_t low_bytes;
                        uint16_t high_bytes;
                    }s;
                    uint32_t uval;
                }Utype;
                
- C11 standartlarıyla nested structta ismini kullanmadan da yazabiliriz:


                typedef union {
                    struct {
                        uint16_t low_bytes;
                        uint16_t high_bytes;
                    };
                    uint32_t uval;
                }Utype;


                
- Bir örnekle pekiştirelim:
        - Bir yapı olsun ve bu yapının içerisinde çalışanların bilgileri tutulsun. 
                - id, name, wage, askerlik bilgiler, kızlık soyadı gibi bilgiler.
        - Yukarıda tutulan bilgilerden görüleceği üzere bu yapıda hem askerlik bilgisi hem kızlık
        soyadı bilgisi olamaz bunun için yapının içinde birlik kullanılarak bellekten tasarruf edilebilir.

- Union kullanmadan sizeof değeri 104 byte oluyor.

                typedef struct {
                    uint32_t id;
                    char name[32];
                    double wage;
                    int mil_st;
                    char place[20];
                    int deg;
                    char maiden_name[32];
                }Data;


                int main()
                {
                    printf("sizeof(Utype) = %zu\n", sizeof(Data )); // 104 byte
                }
- Union kullanıldığında ise 76 byte oluyor.
        

                typedef struct {
                    uint32_t id;
                    char name[32];
                    double wage;
                    union {
                        struct {
                            int mil_st;
                            char place[20];
                            int deg;
                        };
                        char maiden_name[32];
                    };
                }Data;


                int main()
                {
                    printf("sizeof(Utype) = %zu\n", sizeof(Data )); // 76 byte
                }
                
- Yukarıdaki örnekte görüldüğü gibi küçük bir örnekte bile büyük bir oranda bellek kazancı sağladık.




- Union için farklı bir kullanım alanına bakalım:
        - Öyle bir değişken ki (önceden belirlenmiş) farklı türlerden değerler tutabilecek.
                - Mesela bizim örneğimizde bir değişken oluşturalım. int, double, yazı ve tarih 
                tutabilsin.
                




                #define INT    0
                #define DOUBLE 1
                #define NAME   2
                #define DATE   3

                typedef struct {
                    int type;
                    union {
                        int ival;
                        double dval;
                        char name[32];
                        Date date;
                    };
                }Data;


                void set_data_random(Data* p)
                {
                    switch (rand() % 4) {
                    case INT: p->type = INT; p->ival = rand(); break;
                    case DOUBLE: p->type = DOUBLE; p->dval = (double)rand() / RAND_MAX; break;
                    case NAME: p->type = NAME; strcpy(p->name, random_name()); break;
                    case DATE: p->type = DATE; set_date_random(&p->date); break;
                    }
                }

                void display_data(const Data* p)
                {
                    switch (p->type) {
                    case INT: printf("(%d)\n", p->ival); break;
                    case DOUBLE:printf("(%f)\n", p->dval); break;
                    case NAME: printf("(%s)\n", p->name); break;
                    case DATE: print_date(&p->date); break;
                    }
                }

                int main()
                {
                    randomize();

                    Data mydata;

                    while (1) {
                        set_data_random(&mydata);
                        display_data(&mydata);
                        getchar();
                    }
                }


- Yukarıdaki örnekte rastgele int, double tarih ve yazı değerleri birlikler kullanılarak atanıp 
yazma işlemi yapıldı.





- Enumarations (Numaralandırmalar)

- Problem domenindeki bazı öğeler, önceden belirlenmiş bir değer kümesindeki değerlerden birini
almak zorunda. Gerçekten de problem ve çözüm domenindeki varlıkların önemli bir kısmı bu şekilde. 
        - Mesela haftanın gününü tutacak bir değişken
        - Bir yazı fontlarını tutan bir değişken
        - Bir iskambil kağıdı oyununda kağıdın rengini tutan değişken (suit)
        - Bir iskambil kağıdının numarası(face)
        - Sistemin durumunu temsil eden değer (açık on, kapalı off, stand_by, hold)
        
- Numaralandırma türü olarak enum kullanılır. enum bir anahtar sözcük.

                enum Color {
                        White, Yellow, Red, Blue, Green, Black // enumaration constant - enumarator
                };


- Yukarıda sentaksı gönderilen enum yapısında elemanlar 0 dan başlayarak sıralı bir şekilde 
numaralandırılır ve ayrıca derleyici tarafından int türüymüş gibi davranılır.
yani sizeof değeri int türünün sizeof değerine eşittir.


                typedef enum {
                        //something
                }Color;

- Eğer siz numaralandırmayı belli bir sıra dışında istediğiniz değerleri vererek yapmak istiyorsanız:

        
                enum Color {
                        White = 25, Yellow, Red, Blue, Green, Black // enumaration constant - enumarator
                };
                
- Eğer belli elemanlara değer verip diğerlerine vermezseniz kurala göre kendisinden bir önceki elemanın
değerinin bir fazlası default olarak verilir.

- Ayrıca bu elemanlara unique değerler verilmesi de gerekmiyor yani aynı değerler verilebilir.

- C'de varlık sebepleri arasında okumayı ve yazmayı kolaylaştırmak ve tür güvenliği (type safety) 
sağlamak.

  
- C'nin en zayıf noktlarından birisi bu konuda mevcut.

                typedef enum {Club, Diamond, Heart, Spade} Suit;
                
                int main() 
                {
                        Suit s;
                        s = 76;
                }
- Yukarıdaki kod sentaks hatası değildir ancak anlamlı da değildir. s'nin değerinin 76 olması 
enum yapısının elemanlarından birine karşılık gelmiyor. Ancak derleyiciler uyarı mesajı bile 
vermiyorlar çünkü onlar int türündeyse bir problem algılamıyorlar. 
Örnek olarak program akışında tanımlanmış bir int değişkeni enum yapısına yanlışlıkla da atadığınızda
herhangi bir hata almayacaksınız.
Bu yüzden enum'lar C'de kullanılırken dikkatli olunmalıdır. 


- Şimdi bir örnek verelim:

                typedef enum {Club, Diamond, Heart, Spade} Suit;
                typedef enum {On, Off, Hold, Standby} pos;
                
                int main() 
                {
                        Suit s;
                        pos p;
                        
                        //
                        s = Standby; // bir hata almazsınız ama istediğiniz şeyi karıştırarak
                                        //farklı bir sonuç elde ettiniz.
                }



- Eğer siz enum elemanlarını ekrana yazdırmak isterseniz bir pointer dizisi oluşturarak bunu 
yapabilirsiniz.

                
                const char* const psuit[] = {"Club", "Diamond", "Heart", "Spade" };
                
                Suit s = Heart;
                
                printf("%s\n", psuit[s]);


- Bir zayıf tarafı da siz enum bir tür kullandığınızda o türün değeri çok küçük de olsa int dışında 
bir türün karşılığı olarak _t türünde kullanamıyor oluşunuz.


-  Bir başka zayıf nokta ise isim çakışması. Bir çok başlık dosyası include edildiğinde başlık 
dosyaları ile eklenen enumlar arasında bir çakışma söz konusu olabiliyor. 

        //screen.h
        //traffic.h
        
        enum ScreenColor {
                White, Gray, Red, Black, Blue
        };
        
        enum TrafficLight {
                Yellow, Green, Red
        };


- Yukarıdaki kodda isim çakışması olduğu için sentaks hatası olur. 
- Genelde bu çakışmayı azaltmak için önekler kullanılır. 
                
                enum ScreenColor {
                        ScreenColorWhite, ScreenColorGray, ScreenColorRed, ScreenColorBlack, ScreenColorBlue
                }; // Gibi

- Numaralandırma türüne dair idiomlar:
        - Numaralandırmada bazı programcılar son elemanı number olarak adlandırır ve bu sayı toplam
        eleman sayısını belirtir.
        
                        enum Color { White, Gray, Yellow, Green, Red, Brown, Black, NoOfColor };
- Bu arada enum değerleri sabir ifadeleridir. 

**Mesela switch deyiminin case ifadeleri constant expression
olmak zorundadır.**              

- Yani dizi boyutuda yapılabilir. Dizi boyutları da constrant expression olmak zorundadır.


- enum türü bir blok içerisinde kullanılabilir ve ömrü o blok içerisinde sınırlı olur.
        - Bu makrolar herhangi bir bloğun içerisinde tanımlansa bile programın sonuna kadar 
        geçerliliğini koruyordu, siz bir blok içerisinde ömür açısında bir makroya alternatif 
        olarak enum kullanabilirsiniz.
        
                        void foo(void)
                        {
                                enum { SIZE =  100 };
                        } // sadece bu blokta geçerli.
                        


- işlenmeyen konular:

        - bitsel işlemler 
        - komut satırı argümanları
        - dosya işlemleri 
        - assertions 
        - variadic functions
        - c99
                - compound literals 
                - vla
                - flexible array


# Ders 53 - 18.06.2021


- Bitsel İşlemler (Bitwise Manipulations / Operations)

    - Bitwise operators
        - ~ (bitwise not)
        - >>, << (bitwise left/right shift) bitsel kaydırma 
        - & (bitwise and) 
        - ^  (bitwise exor)
        - | (bitwise or)
        - |=, >>=, <<=, &= 

- Yukarıdaki operatörlerin hepsi bitsel işlem yapıyor.
- Bu operatörlerin operantları int type türünden olmak zorunda. 


- ~ (bitwise not) 
    - unary prefix bir operatör.
    - Operant tam sayı türünden olmalı. integer promotion burada da geçerli.
    - Operatörün ürettiği değer, operantın bitlerinin tersinin alınmasıyla elde edilen değerdir.
    - Bu operatörün bir yan etkisi yoktur. (no side effect)
    
            int x;
            printf("bir tam sayi girin: ");
            scanf("%d", &x);

            bprint(x);
            bprint(~x);
        
- <<, >> bitwise left/right shift (bitsel sola sağa kaydırma operatörü)


        a << 2
- Yukarıdaki kod için a nın değeri 2 bit sola kaydırılacak. Yani a'nın solundaki iki bit silinecek
ve sağına 2 bit 0 olarak eklenecek.

        1110010101110101 iken
        1001010111010100 olacak.

- Yani burda dikkat edilmesi gereken nokta, sayı işaretli veya işaretsiz türden de olsa her zaman
sağdan yapılan besleme (feed) 0 olacaktır. 

- Operatörün yine yan etkisi yok (no side effect)
- Atama yapmak istiyorsanız:

        a <<= 2; // olarak kullanılabilir.
        

- Eğer sağ operant negatif değerde ise ya da sağ operand, sol operand olan ifadenin ait olduğu türün 
bit sayısına eşit veya büyük değerde ise **tanımsız davranıştır.**

        a << b için;
        a -> int 4 byte 32 bit olduğu için b en fazla 31 bit bir değere sahip olabilir.
        
- Kayan bitler için bir örnek:

            #include <Windows.h> // standart bir fonksiyon değil



            int main()
            {
                int x = 1;

                while (x) {
                    bprint(x);
                    x <<= 1;
                    Sleep(200);
                }


            }
            
- Bitsel sola kaydırma işleminde feed her zaman 0 oluyordu ancak bitsel sağa kaydırmada durum tamamen
aynı değil.
    - Eğer sol operant işaretsiz ise besleme 0 ile yapılır.
    - Eğer sol operant işaretli ama pozitif değer ise besleme yine 0 ile yapılır.
    - Ancak eğer sol operant işaretli ama negatif değer ise 
        - Soldan yapılacak beslemenin 0 veya 1 ile yapılması tamamen derleyiciye bağlıdır.
         ( implementation defined )
        - Besleme 1 ile yapılıyorsa ; aritmetik besleme ( sign extension )
        - Besleme 0 ile yapılıyorsa ; lojik besleme ( logic extension )
        


- Bir idiyomatik ifade:

                (~(~0u >> 1)) -> ifadesinin sonucu 100..00-> 32 bit
                // 0000 0000 0000 0000 0000 0000 0000 0000
                // 1111 1111 1111 1111 1111 1111 1111 1111
                // 1000 0000 0000 0000 0000 0000 0000 0000  olur.
                // bu sayi işaretli olarak kullanılırsa ;
                // işaretli tam sayı türünün en küçük değerine eşit olur. 
        
- Bu sayı limits.h başlık dosyasında INTMIN makrosunun değeridir.


- Aşağı kodda 1 bitini soldan sağa kaydırma işlemi yapıyor.

        unsigned int x = ~(~0u >> 1);

        while (x) {
            bprint(x);
            x >>= 1;
        }

- Bitsel & operatörü:
    - Tam sayıları bitsel işleme sokuyor.


            int x = 154645, y = 9589;

            bprint(x);
            bprint(y);
            bprint(x & y);
            
            
 - Bitsel operatörlerin short circuit behavior yoktur.

  
  
- exor (exclusive or)
    - !!x != !!y  işlemine eşittir. 
    
- İki sayıyı iki kere exor işlemine sokarsanız soldaki değeri tekrar elde edersiniz.

- İki tam sayıyı üçüncü bir değişken olmadan takas etmek mülakat sorusunun cevabıdır.
    - exorswap
    
            int x = 124, y = 687;
	

            x ^= y;
            y ^= x;
            x ^= y;
            printf("x = %d, y = %d ", x, y);
             
- Hatta tek bir satırda da yazılabilir.

            x ^= y, y ^= x, x ^= y;


- Bir mülakat sorusu:
    - İşaretli iki tam sayının x, y zıt işaretli olup olmadığını test eden bir ifade yazınız.

            x ^ y işleminin sıfırdan küçük olması bu testin karşılığıdır.
            
            if ((x ^ y) < 0) 
            

- Bir tam sayının belirli bir bitini bir'lemek ( to set the bit - to turn the bit on)
- Bir tam sayının belirli bir bitini sıfır'lamak ( to reset the bit - to clear the bit- to turn the bit off)
- Bir tam sayının belirli bir bitini değiştirmek (  to flip the bit- to toggle the bit)
- Bir tam sayının belirli bir bitini 1 mi 0 mmı olduğunu anlamak. ( to get the bit )



- bitmask: belirli bitsel manipulasyon için kullanılana sabitler. Değişiklik yapılmak istenen bitin 1
olduğu diğer bitlerin ise 0 olduğu bitsel değerler.

            10110101010011*10010
            00000000000000100000  // bitmask
            10110101010011110010


- x biti set edilecek sayı olsun n set edilecek bitin indeksi olsun.


        x |= (1 << n) // x'in n. bitinin birlenmiş halidir.


- mesela bir sayının 5. bitini 1 leyelim.


            int x = 15;
            
            bprint(x);
            
            x |= 1 << 5; // x sayısının beşinci biti birlendi.
            
            bprint(x);
            

- istenilen bitin birlendiği bir örnek yazalım:


        int x = 0;
        int n;
        
        bprint(x);
        printf("kacinci bit birlensin");
        scanf("%d", &n);
        
        x |= 1 << n;
        
        bprint(x);
        
        
- Bir örnek:


            int x = 0;

            randomize();

            while (x != -1) {
                x |= (1 << (rand() % 32));
                bprint(x);
                Sleep(50); //Windows.h başlık dosyasından.
            }
            bprint(x);



- x biti clear edilecek sayı olsun n clear edilecek bitin indeksi olsun:

            x & ~(1 << n);
            x &= ~(1 << n); // x e sonuç atandı.


- x sayısının 27. biti sıfırlansın.

        int x = -1;
        
        bprint(x);
        
        x &= ~(1 << 27);
        bprint(x);




- Bir örnek:

            int x = 0;

            randomize();

            while (x != -1) {
                x |= (1 << (rand() % 32));
                bprint(x);
                Sleep(50); //Windows.h başlık dosyasından.
            }
            bprint(x);
            
            while (x) {
                x &= ~(1 << (rand() % 32));
                bprint(x);
                Sleep(50); //Windows.h başlık dosyasından.
            }
            bprint(x);


- toggle işlemi: Yani bir bitin tersini alma işlemi:

        x ^= (1 << n) 


- Bir tam sayının bir bitinin ne olduğunu elde etmek:
    - x biti get edilece ksayı olsun n get edilecek bitin indeksi olsun:

            if ( x & (1 << n))

- Bir örnek:

            static char str[40];
            
            _itoa(x, str, 2);
            printf("%032s\n", str);
            
            int n;
            printf("kacinci bit: ");
            scanf("%d", &n);
            
            if (x & (1 << n))
                printf("%d. bit 1\n", n);
            else
                printf("%d. bit 0\n", n);
                
- Daha idiyomatik hali:

            int x;
            printf("bir tamsayi girin: ");
            scanf("%d", &x);
            
            for (int i = 0; i < 32; ++i) {
                printf("sayinin %d. biti %c\n", i, (x & (1 << i)) ? '1': '0');
            }



- Bitsel operatörleri kullanarak bir sayının bitlerini yazan fonksiyon:


		void bit_print(int x)
		{
		    unsigned int mask = ~(~0u >> 1);

		    while (mask) {
			putchar(x & mask ? '1' : '0');
			mask >>= 1
		    }
		    putchar('\n');
		}

- Bu sefer mask i 0 değerleri üzerinden düşünerek yazalım:

		void bit_print(int x)
		{
		    for (int i = sizeof(int) * 8 - 1; i >= 0; --i) {
			putchar((x >> i) & 1 ? '1' : '0');
		    }
		    putchar('\n');
		}



- Bir mülakat sorusu:
	- if (x & 1) ifadesi neyi sorguluyor?
		- x'in sıfırıncı bitiinin 1 olup olmadığı sınanıyor.
		Ayrıca bu ifadenin anlamı ise sayının tek olup olmadığı sınanıyor.
		Yani if (x % 2 != 0) ifadesi ile aynı anlama gelmektedir.
		
		

- Bir soru:
	- x bir tam sayı değişken, x'in en düşük anlamlı 4 biti tam sayı olarak kaçtır. 

			int x = 122532;
			
			bprint(x);
			
			printf("%d\n", x & 15); // 15 -> 1111



- Bir tam sayının set edilmiş bitlerinin sayısını bulmak, yani kaç biti 1 dir.


			int set_bit_count(int x)
			{
			    int cnt = 0;
			    unsigned int mask = ~(~0u >> 1);

			    while (mask) {
				if (x & mask) 
				    ++cnt;
				mask >>= 1;
			    }

			    return cnt;
			}



- Çok meşhur bir mülakat sorusu:
	- Öyle bir ifade yazınız ki, x bir tam sayı değişken olsun, x 2'nin kuvveti mi?
	- Ve bunu bir makro haline getirin.

- Cevap: Bir istisna hariç bir sayı 2 nin kuvveti ise o sayıdan 1 çıkarılıp kendisiyle & işlemine
sokulduğunda sonuç 0 olmalıdır.

		0001 0000
		0000 1111
		
		0000 0000 olur:
		
		!(x & (x - 1))
Buradaki istisna 1 sayısıdır. 1'in bir eksiğiyle 1'i & lerseniz yine 0 elde edersiniz ancak 0, 2'nin 
kuvveti değildir.

		x != 0 && !(x & (x - 1)) 
		x && !(x & (x - 1))  olarak son halini alır. 


# Ders 54- 23.06.2021

- Bit twiddings hacks: Mülakata girmeden önce bitsel manipülasayona dair kısa yolların bulunduğu bir 
döküman kesinlikle incelenmelidir.

 

- Bir byte'ın reverse'ünü elde etmek:
		
		1100 1101
		1011 0011 reverse edilmiş hali.
		

- bit twiddings hacks'e bakınız..



- Meşhur mülakat sorularından bir tanesi:
	- 16 bitlik işaretsiz bir tam sayınız var, bu tam sayının ortasındaki 8 bitin değerini elde edin.

		1001 0101 0101 1001 sayısının ortadaki 8 biti yani
		     0101 0101  kısmını elde etmeniz isteniyor.
		     
- Çözümlerden birisi: sayıyı 4 sağa kaydırıp 16 sayısıyla & lemek

		x >> 4 & 16;
		
- Ama daha kolay bir yolu var:
	- x'i 4 sola kaydır, Bunu da 8 sağa kaydır.

		x << 4 >> 8;
		
- Bir işaretsiz tam sayının bitlerini bir boolean vector olarak kullanmak:


- Bitsel işlemlerin önemli bir kısmıda formatsız veri alış verişi için kullanılır.
	- Acaba biz bir tamsayının belirli bit alanlarını ayrı değişkenler olarak kullanabilir miyiz?

- bitfields members of structures - yapıların bit alanı elemanları:
	- bitsel olarak değişken oluşturma üzerinde belirli işlemler yapma gibi standart olan
	bir yolu.
	
	
		//bitfield member:

		typeddef struct  {
			unsigned int x : 3; // buradaki 3 değerin kaç bitlik alanda tutulacağı.
		}Data;


- Normal yapılara göre bir kısıtlama mevcut. normalde bir yapının elemanın adresi alınabiliyordu.
Ancak bitsel düzeyde olduğunda adresi alınamıyor.

		Data mydata;
		
		&mydata.x; // hata
 

- alignment için kullanılmayacak olan bitler için bir belirtme söz konusu olabilir.

		struct Data {
			unsigned int x : 5;
			unsigned int   : 3; // gibi
			unsigned int y : 4;
			unsigned int z : 3;
		};






- Birlikler ile bitsel işlemlerin birlikte kullanım şekli çok yaygın.
	
		typedef union {
			uint32_t uval;
			struct {
				unsigned int mday : 5;
				unsigned int mon  : 4;
				unsigned int year : 7; // 1980
				unsigned int hour : 5;
				unsigned int min  : 6;
				unsigned int sec  : 5;
			};
		}DateTime;
		
		int main()
		{
			DateTime dt = {
					.mday = 14,
					.mon = 3,
					.year = 1995 - 1980,
					.hour = 21,
					.min = 36,
					.sec = 45 / 2;
					};
					
			printf("%u\n", dt.uval); // değeri :  3029671534
		}
		------- ya da -----------------------------------------------
	
		int main()
		{
			DateTime dt = {
					.uval = 3029671534;
					};
					
			printf("%02u-%02u-%u  %02u:%02u:%02u\n", dt.mday, dt.mon, dt.year + 1980,
							dt.hour, dt.min, dt.sec * 2);
		}





- Bitler e rahat erişim için bir örnek:

		typedef union {
			struct {
				unsigned int bit0 : 1;
				unsigned int bit1 : 1;
				unsigned int bit2 : 1;
				unsigned int bit3 : 1;
				unsigned int bit4 : 1;
				unsigned int bit5 : 1;
				unsigned int bit6 : 1;
				unsigned int bit7 : 1;
				unsigned int bit8 : 1;
				unsigned int bit9 : 1;
				unsigned int bit10 : 1;
				unsigned int bit11 : 1;
				unsigned int bit12 : 1;
				unsigned int bit13 : 1;
				unsigned int bit14 : 1;
				unsigned int bit15 : 1;
				unsigned int bit16 : 1;
				unsigned int bit17 : 1;
				unsigned int bit18 : 1;
				unsigned int bit19 : 1;
				unsigned int bit20 : 1;
				unsigned int bit21 : 1;
				unsigned int bit22 : 1;
				unsigned int bit23 : 1;
				unsigned int bit24 : 1;
				unsigned int bit25 : 1;
				unsigned int bit26 : 1;
				unsigned int bit27 : 1;
				unsigned int bit28 : 1;
				unsigned int bit29 : 1;
				unsigned int bit30 : 1;
				unsigned int bit31 : 1;
			};
			uint32_t uval;
		}Bits;


		int main()
		{
			Bits x = { .uval = 3651910 };
			x.bit7 = 0;

		}




- endianness: Bir değişkenin belleğer byte - byte yerleşimi yapılmasında düşük anlamlı byte'ın 
yüksek numaralı adrese veya düşük numaralı adrese yerleşmesine göre ayrılmasındaki kullanılan terim:


		int  x = 10;
		
		0000 0000 0000 0000 0000 0000 0000 1010
		
		- Düşük anlamlı byte yüksek sayısal adreste, yüksek anlamlı byte düşük sayısal adreste,
			- big-endian
			- motorala tarzı
		4000 -> 0000 0000
		4001 -> 0000 0000
		4002 -> 0000 0000
		4003 -> 0000 1010
		
		
		- Düşük anlamlı byte düşük sayısal adreste, yüksek anlamlı byte yüksek sayısal adreste
			- little endian
			- intel tarzı
		4000 -> 0000 1010
		4001 -> 0000 0000
		4002 -> 0000 0000
		4003 -> 0000 0000
		
		- arm her ikisindede kullanılıyor olabilir.

- Mülakatlarda sık sorulan bir mülakat sorusu: 
	- Öyle bir C kodu yazınız ki, çalıştırıldığı zaman çalıştırıldığı sistemin big endian mı little
	endian mı olduğunu ekrana yazdırsın.
	
		int x = 1;
		
		char *p = (char*)&x
		
		if (*p)
			printf("little endian\n");
		else
			printf("big endian\n");

	- Daha kolay yazımı:

		int x = 1;
		
		char *p = (char*)&x
		
		if (*p)
			printf("little endian\n");
		else
			printf("big endian\n");
			

- Bellekte nasıl tutulduğunu tam olarak gözle görülmek istendiğinde:

		unsigned int x = 0x12AB45DE;

		unsigned char* p = (unsigned char*)&x;

		printf("%p %x\n", p, *p);
		++p;
		printf("%p %x\n", p, *p);
		++p;
		printf("%p %x\n", p, *p);
		++p;
		printf("%p %x\n", p, *p)


- Öyle bir makro yazınız ki big endien ı little endien a, little endien ı big endien e dönüştürsün:

	
		#define enc16(x)  ((uint16_t)(x >> 8)) | ((uint16_t)(x << 8))  // 16 bit için
		#define enc32(x)  ((x >> 24) | (x << 24)) | ((((x << 8) >> 24) << 8) | ((((x << 16) >> 24) << 16))) // 32 bit için


# Ders 55 - 25.06.2021


- Komut Satırı Argümanları:
	- Commend Line Arguments (CLI)


		int main(int argc, char *argv[])
		{


		}	
- argc : komut satırından gönderilen argüman sayısı.
- argv: komut satırından gönderilen argümanların yazılarını gönderen pointer dizi.
	- copy ali.c veli.c için argc si 3 olur ve argv[0] = copy, argv[1] = ali.c, argv[2] = veli.c 
	olur.



- Dosya İşlemleri ( File Operation)
	- Dosya dediğimiz de aklımıza 1 ler ve 0 lar gelmeli ancak burdaki 1 ler ve 0 lar
	bellekteki (ram) veriler değil ikincil saklama ortamındaki 1 ler ve 0 lar gelmeli. 
	- Bu 1 ler ve 0 lar ise ne anlama geliyor dediğimizde aklımıza dosyanın formatı gelmeli(file 
	format). Her dosyanın bir formatı vardır. Yani ikincil saklama ortamlarında tutulan 1 ler ve 
	0 ların ne anlama geldiğini bilmeniz için o dosyanın formatını bilmeniz gerekiyor.
	- Mesela txt formatında her bit byte bir ascıı koduna karşılık gelmektedir.
 


- C'de dosya işlemi yapabilmeniz için fopen fonksiyonuna çağrı yapmanız gerekmektedir.
- fopen fonksiyone bize işlem yapacağımız dosya ile ilgili kritik bilgileri tutan bir yapı nesnesinin
adresini döndürüyor. 

	FILE *f = fopen(??);
	//code
	fclose(f);

- Dosyalar üzerinde hangi işlemler yapılıyor:
	- Dosyadan okuma (read)
	- Dosyaya yazma (write)
	- Dosya konum göstericisi (file pointer)



		FILE * fopen(const char *pfname, const char *popenmode);
	-  Geri dönüş değeri FILE *
	-  Birinci parametresi açılacak dosyanın ismini içeren yazının adresi.
	-  Fonksiyonun ikinci parametresi, dosyanın açış modu dediğimiz bilgiyi içeren yazı adresi. 

- Dosya açış modu bilgisi:
	- Dosya varsa ne olacak yoksa ne olacak.
	- Dosya üzerinde okuma veya yazma işlemi iznimiz var mı?

- Açış modu:
	- Dosyayı okuma (read) modunda açabiliriz.
	- Dosyayı yazma (write) modunda açabiliriz.
	- Dosyanın sonuna ekleme (append) modunda açabiliriz.

- Dosyanın okuma (read) modu varsa; dosya açılır, yoksa açılmaz.
- Dosyanın yazma (write) modu varsa; dosya sıfırlanır (truncate), yoksa oluşturulacak.
- Dosyanın sona ekleme (append) modunda varsa; açılacak, yoksa oluşturulacak.

- Peki neler yapabiliriz:
	- Okuma modunda açıldığında dosya okunabilir ama yazılamaz.
	- Yazma modunda açıldığında dosyaya yazabiliriz ama dosyayı okuyamayız.
	- Sona ekleme modunda, dosyanın sadece sonuna yazabiliriz, ama okuyamayız. 


- Bir de bu modların + 'lı modları mevcut.
	- Artılı okuma modunda hem okuma hem yazma işlemi yapabiliyoruz.
	- Artılı yazma modunda hem yazma hem okuma işlemi de yapabiliyoruz.
	- Artılı sona ekleme modunda sona yazabiliyoruz ve okuyadabiliyoruz.




- Dosyalara text modunda ve binary mod olarak açılabilir.


- Modlar için yazılara bakalım: İlave karakter kullanılmadığında default olarak text modunda dosya açılır.
	- Okuma için -> "r" ---artılı mod için--- "r+"
	- Yazma için -> "w" ---artılı mod için--- "w+"
	- Sona ekleme için -> "a" ---artılı mod için--- "a+"
- Dosyayı binary modda açmak için b eklenir:
	- Okuma için -> "rb" ---artılı mod için--- "r+b" veya "rb+"
	- Yazma için -> "wb" ---artılı mod için--- "w+b" veya "wb+"
	- Sona ekleme için -> "ab" ---artılı mod için--- "a+b" veya "ab+"



- Geri dönüş değeri ise stdio başlık dosyasında typedef i yapılmış bir yapı isimdir (FILE) . 
	 - Geri dönüş değeri NULL pointer ise dosya açma işleminde başarısız olunmuş demektir. 
	 ! geri dönüş değeri mutlaka test edilmelidir.
	 
	
			FILE* f = fopen("mustafa.txt", "r");

			if (!f) {
				fprintf(stderr, "dosya acilamadi\n");
				return 1;
			}

			printf("dosya acildi\n");

			// 
			fclose(f);



- fclose parametrik yapısı:

		int fclose(FILE *);
	- Geri dönüş değeri  fonksiyonun başarısını temsil ediyor. 
		- non-zero değer dönmesi dosyanın kapatılamadığı bilgisini verir.
		- 0 değer dönmesi ise başarılı olduğu bilgisini verir.



			int fcloseall(void); // standard değil
			
	- Aynı zamanda birden fazla dosya açıksa ve tek kodda tüm dosyalar kapatılmak isteniyorsa 
	fcloseall kodu kullanılır.
	- Geri dönüş değeri kapatılan dosya sayısıdır.
	
	
- fgetch(): formatsız okuma fonksiyonu:
	- Bu fonksiyon dosyadan tek bir byte'ı yani tek bir karakteri okuyor. 


- Dosya işlemlerinde hiçbir fonksiyon bizden hangi byte'dan okuma veya yazma işlemini yapacağı 
bilgisini istemez. 
- Bir file pointer yani Dosya Konum Gösterici var. File pointer sizin erişiminize kapatılmış bir 
tam sayı değişken. Bu tam sayı değişken dosyanın neresinden okuma/yazma işlemi yapılacağını 
gösteriyor.
- Dosya işlemlerinin bu şekilde yapılmasına sequential access (sıralı erişim) deniliyor. 
- random access (rastgele erişim) belirli fonksiyonlar yardımıyla file pointer set edilerek
istenilen byte'dan erişimin sağlanmasına deniliyor.




	int fgetc(FILE *);
- Geri dönüş değeri dosyadan okunan byte'ın tam sayı değeri.
- Okuma başarılı ise okunan byte'ın tam sayı değeri döndürülüyor. Eğer başarısız olurs -1 döndürüyor.
- stdio başlık dosyasında fgetc'nin başarısızlık bilgisi sorgulanması için değeri -1 olan
bir makro var :

		#define EOF  	(-1) 
		
		

- Bir örnek:


			FILE* f = fopen("date.h", "r");
			if (!f) {
				fprintf(stderr, "dosya acilamadi\n");
				return 1;
			}

			int c;

			while ((c = fgetc(f)) != EOF) {
				putchar(c); // printf("%c", c);
			}

			fclose(f);















































































  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
