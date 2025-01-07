# OOP-notes
Object Oriented Programming Notes

OBJECT
⦁	Nesne Tabanlı Programlama da en küçük parça Object yani nesnedir.

⦁	Nesneler içerisinde veri tutabilecek alanlar oluştururlar.(Bu alanlara field denir).

⦁	Metotlar, propertyler ve indexer ile nesne içerisinde işlemler gerçekleştirilebilir.

⦁	Nesne oluşturmadan önce Class oluşturulmalıdır.

⦁	Class modellenerek nesneler oluşturulur.

⦁	Developerların direkt stack’e erişimi vardır. Ancak Heap’e yoktur.

⦁	Stack de tanımladığımız değerler referans ile Heap’e erişebilir.

⦁	Referanslar stack de tutulur.


CLASS

⦁	Bir Nesne için bir Sınıf oluşturulup modellenir.

⦁	Classlar bir referans türüdür.

⦁	Nesneyi referans edebilmek için o nesne’nin ait olduğu class kullanılarak edilir.
Ex: ClassName name;  Burada name’e biz referans alma, referans noktası vs.

⦁	Referans türlü değer/değişken özünde Nullable yapıdadır. Yani name Nullable.



FIELD

⦁	Nesne içerisinde verileri tuttuğumuz alandır.

⦁	Field’lar da default değerler türüne göre atanır. 

Ex: sınıf içerisindeki field kısmında int a; a 0 dır.


PROPERTY

⦁	Esasında kendisi bir metotdur. Farkı parametre almaz, get ve set blokları vardır.

⦁	Set ile değer atanır, get ile değer okunup return edilir.

⦁	Field’lara direkt erişilmesini istemeyiz. Bu durumda Verileri kontrollü şekilde dışarıya açmak isteriz ve ona göre public, private Access Modifier’ı ayarlarız.

⦁	Yani property yapıları nesne içerisinde ki field’ın dışarıya kontrollü şekilde açılmasını ve dışarıdan kontrollü değer alınmasını sağlayan yapıdır.
Property’lerin bu işlevine Kapsülleme(Encapsulation) denir.

⦁	Property kullanılırken aslında kapsülleme de yapılmaktadır.

⦁	Duruma göre değer atama istenmiyor ise set veya değer okunması istenmiyor ise get kullanılmadan halledilebilir. Yani ikisi birden kullanılma söz konusu değil.

PROP

Field tanımlanmasına gerek yoktur.
⦁	*** Kısa yoldan prop tab tab yaptığımız kısımda da Kapsülleme işlemi yapılır. Fieldlarımıza müdahele olsun olmasın direkt erişim yapılmasını istemeyiz. 
⦁	Arka planda zaten field oluşturaktadır.


THIS KEYWORD

⦁	Class dan bir nesne oluşturulduğunda this keywordü oluşturulan nesneyi temsil eder.

⦁	Bir constructer dan başka bir constructer ı çağırmak için kullanılır.	

⦁	Field ile metot içerisinde tanımlanan değişken isimleri aynı olması durumunda this kullanılarak field olana erişilmek istenebilir. 


OBJECT (TEKRAR EK BİLGİ)

⦁	Nesneler Complex Değer olarak geçer, Classlar Complex Type olarak.

⦁	Object oluşturulurken new operatörü kullanılır, new Type() burada ki parantez constructor metodunu temsil eder. Bu bir operasyon olduğu için bir metot içerisinde oluşturulmalıdır.

⦁	Nesne bir organızmadır, günlük hayatta karşılaştığımız her şey nesne olabilir.




REFERANS NEDİR?

⦁	Ram’in stack bölgesinde tanımlanan ve Heap bölgesindeki Object’leri referans eden/işaretleyen değişkenlerdir.

⦁	Class, Interface ve AbstractClass’lar ile stack de referans türlü değişken oluşturulabilir ancak Sadece ve Sadece Class dan object üretilir. 
Daha sonralar da AbstractClass üzerinden derleme esnasında da nesne üretilme durumu vardır. 
Record da vardır.(Ve ilerde çok kullanılmaktadır, nesne üretir.)

⦁	NullReferanceException hatası oluşturulan referansın bir nesnesi yoksa bu hata alınır. Ex: MyClass m1 = null;   “Bir Nesne oluşturulmamış”.

⦁	Referanssız Nesneler: new MyClass();  “Bu durumda nesne heap de oluşturulur ancak bir erişimi olmadığından daha sonra erişilemez.”

⦁	Heap içerisinde referanssız oluşturulmuş nesneler Garbage Collector(Çöp toplayıcı) ile temizlenir. BELLEK OPTIMIZASYONU’DUR.



ENCAPSULATION (KAPSÜLLEME)

⦁	Kapsülleme, nesnelerimizdeki field’ların kontrollü bir şekilde dışarıya açılmasıdır.

⦁	Nesnelerimizin dışarıdan değişmesine kapayıp korumak anlamınla gelir.

⦁	Kapsülleme Yöntemleri; 1- Metot ile Kapsülleme 2- Property ile Kapsülleme



RECORDS 
Init-Only Properties
⦁	Record u anlayabilmek için önce init only properties özelliğini anlamalıyız.
⦁	Runtime da değerin değişmemesi istendiği durumda kullanılmaktadır.
⦁	Projeyi ayağa kaldırırken objemize değer atamak istiyorsak kullanırız.

⦁	Eğer biz bir objeyi bütünsel olarak değişmez yapmak istiyorsak yani (readonly), bu yüzden Record yapısı kullanılır.

⦁	Record, bir objenin tamamen sabit/değişmez olarak kalmasını sağlamakta ve bu durumu güvence altına almaktadır.

⦁	Record Class gibidir, özünde nesnedirler ama Class’da Nesnenin kendisi ön plandadır, Record’da ise Nesnenin değerleri ön plandadır.

⦁	Instance’lar bizim Object lerimizdir.

⦁	Recordlarda aynı Class gibidirler. Propertyleri, metotları, fieldları, constructor metotları vardır. Referans türlü yapılardır.
 
⦁	İlla Record sınıfında property tanımlanırken init kullanmak zorunlu değildir ama amaca hizmet etmesi için kullanılması doğrudur.

⦁	Tüm Member’lar init ile işaretlenir.


⦁	RECORD kullanılma sebebi: Class’lar üzerinden de propertyleri init ile işaretleyerek değiştirilmez yapıp Object Initializer kısmında değer ataması yapabiliyoruz. Amma velakin, daha sonra bu propertyler üzerinden değişiklik yapmak istersek ilgili class üzerinden yeni bir nesne tanımlanıp değişmeyecek olan değeri önceden tanımlanmış referans nesnesi üzerinden alınıp atanmakta ama değişecek kısım yeniden atanmaktadır. Bu ilerde can sıkıcı durumlara getirebilmektedir, ne kadar fazla property o kadar sıkıntı.

Eğer bunu Record’lar üzerinden gerçekleştirirsek bize koplayama durumlarında With Expression yönteminden faydalanılabilmekte ve istenilen özellikleri hızlıca değiştirebilmekteyiz.



POSITIONAL RECORD
Bu kullanım ile hem constructor hemde deconstructer daha efektif kullanılmakta
Bu kullanım sadece RECORD’a özeldir.
İmza şekli: record MyRecord(type name, type name)
Bu parametrelerin karşılıkları olan property’ler otomatik olarak compiler seviyesinde oluşturulacaktır. INIT olacak şekilde.



ÖZEL SINIF ELEMANLARI

⦁	CONSTRUCTOR METOT

⦁	Yapıcı metotdur. Nesne ilk ayağa kaldırılırken ilk configuration’ları yaptığımız metot.

⦁	Nesne üretilirken ilk tetiklenen fonksiyondur. Ex: new MyClass(); 
Burdaki parantez Constructor metotudur.

⦁	Consturctor, nesne hafızada oluşturulduktan sonra tetiklenir.

⦁	Constructor metot adı – Class adı ile aynı olmak zorundadır.
Geri dönüş değeri olmaz.
Genellikle public olmalıdır,  private durumu da vardır.

⦁	Her sınıfın içerisinde tanımlanmamış olsa dahi default bir constructor vardır.

⦁	Constructor’lar parametre alabilen yapılardır.

⦁	Ctor kısayolu ile hızlı constructor metot oluşturulabilir.

⦁	Birden fazla Constructor metot oluşturulabilir, isimler aynı olmak zorundadır, ancak parametre türleri veya sayıları farklı olmak koşuluyla overloading yapılır.

⦁	Constructor metot tetiklenmez ise O sınıftan bir object oluşturulamaz.

⦁	Singleton Desing Pattern’da constructor private olup dışarıdan yani               (Sınıfın dışından) nesne üretilmesi istenmeme durumu vardır.
Tek bir nesne oluşturmak hedefleniyorsa Singleton Desing Pattern kullanılır.
DESIGN PATTERN: OOP’den faydalanarak tekrar eden stratejiler anlamına gelmektedir.


⦁	DESTRUCTOR METOT

⦁	Yıkıcı metot’dur.
Bir nesne yok edilirken çağrılan metot’dur.
Sadece Class yapılanmasında mevcuttur.
Bir class sadece tek bir destructor metot içerir.
Parametre almaz.

⦁	Nesnenin silinebilmesi için erişilemez olması lazım.
Referanssız olması bir etken
Oluşturulan nesnenin kullanıldığı scope sone ermiş olması etken

Garbage Collector Tarafından İmha edilir.
⦁	GC nin işine developer’lar karışmaz. 
⦁	İstediği zaman kafasına göre temizler ve bellek optimizasyonu sağlar.
⦁	Nesne ölmeden son mesajını vermek için Destructor metot çalışır


⦁	DECONSTRUCT METOT

⦁	Sınıf ismiyle aynı isimde değil ‘Deconstruct’ adında oluşturulur.
Özetle özel field’ları hızlıca kullanmak istersek kullanılırız.
Geriye Tuple bir değer döndürür.


⦁	STATIC CONSTRUCTOR

⦁	İlk tetiklenen metotdur.
Ama İlk nesne üretilirken tetiklenen fonksiyondur.
Constructor her seferinde nesne üretildiğinde tetiklenir.

⦁	Uygulama bazlı datalarımızı yerleştirdiğimiz alandır.

⦁	Geri dönüş değeri ve Access Modifier ı yoktur.
Ex: static MyClass(){}
Parametre almaz.

⦁	Önemli: Static Constructor tetiklemek için illa bir ilk nesne üretilmesine gerek yoktur, İlgili sınıf içerisinde herhangi bir static yapının tetiklenmesi yeterli olacaktır.

⦁	Singleton Desing Pattern da static constructor kullanılır.
Ex: Veritabanımızda olan bir context (Bağlantı işlemi gerçekleştiren örneğin ) bunu sürekli kullanmak yerine bir kere bir sınıfta oluşturup sürekli onu çağırarak gerçekleştiririz.
Sonradan üretilen nesneler bize ilk üretilen nesnenin değerini getirir.
Burda static olan getInstance tetiklendiği için static ctor tetiklenecektir. Ve bir kere tetiklenecektir.



INHERITANCE (KALITIM)

⦁	: Operatörü ile gerçekleştirilir.
⦁	Ex: class MyClass : UstClass
⦁	OOP’nin en önemli konusudur.
Kodun maliyetini düşüren bir yapı sağlar.
Mimarisel olarak tasarımda avantaj sağlar.
EX: Erkek ve Kadın Ortak Noktaları İnsan, İnsan adında bir üst sınıftan ortak veriler çekliebilir ikisi içinde mesela isimleri soyisimleri yaşları vs. insan sınıfında tanımlanır.


BASE CLASS – DERIVED CLASS

⦁	Kalıtım veren class’a Base Class (Parent Class) 
Kalıtım  alan class’a Derived Class (Child Class)   DENMEKTEDİR. 

⦁	Bir Class’ın sadece bir Base Class’ı vardır.
Baba-Çocuk ilişkisi
⦁	Bir sınıf tek bir sınıftan kalıtım alabilir. Birden fazla kalıtım alamaz.

⦁	Bir sınıftan nesne üretilirken üst sınıfdan kalıtım aldıysa eğer önce o sınıflardan nesne üretilir daha sonra kendisinden nesne üretir.
A         new B(); dersek
B:A    Burada önce A nesnesi üretilecek sonra B nesnesi üretilecekdir.
           Heap’de A nesnesi önce sonra B nesnesi oluşturulur.
⦁	Bilgi: A sınıfından bir member’ı kullanıken aslında o sınıf üzerinden erişilerek kullanırız.  

⦁	BaseClass’ımızda birden fazla constructor tanımlanmış olabilir bu yüzden hangisini tetikleyebileceğimizi seçebilmekteyiz.
Bunu da base Keyword’ü ile gerçekleştirebilmekteyiz.


⦁	Eğer base class’da parametresiz default bir constructor var ise derived class’da base ile bir etkileşim yapmak zorunda değiliz. Çünkü varsayılan olarak boş parametreli constructor tetiklenir.

⦁	Base Class içerisinde birden fazla constructor olması durumunda, Derived Class İçerisinde olan ctor’da : base() ile Base Class’da ki overload olmuş constructor’lardan hangisini kullanacağımızı seçebilmekteyiz.


⦁	C# dilinde istisnasız tüm sınıflar OBJECT class ından türemektedir.
İstisna Durum İleri Zaman Konusu: Delegate, bir nesnedir object den türemez.



SANAL YAPILAR

⦁	Bir sınıf içerisindeki yapının nesne içerisinde olup olmayacağını run-time zamanında belirlemek istiyorsak sanal yapılanmalar ile sağlanabilmektedir.

⦁	Bu sanal yapılar Metot ya da Property olabilir.
⦁	Yani sanal yapılanmalarda Name Hiding’de olduğu gibi bir isimsel çakışmadan ziyade Parent Class’dan gelen yapının Child Class içerisinde iptal edilip yani ezilerek yeniden yapılandırılmasıdır.

⦁	İşte burada bir sınıfta tanımlanmış yapının iptal edilip edilmeme durumuna göre tanımlandığı sınıftan mı yoksa bu sınıfın torunlarından mı çağırılacağı run-time esnasında gerçekleşecektir.

⦁	Derleme anında belirlenemediği için run-time da belirlenir. 
Buna da Geç Bağlama (Late Binding) denir.

⦁	Bir member’ın ezilip yeniden yapılanmasını istiyorsak kesinlikle o member’ın SANAL YAPIDA olması gerekmektedir.

⦁	Bir sınıfta Sanal Bir Yapı oluşturmak istiyorsak: İlgili member’ın (metot ya da property) imzasının virtual keyword’ü ile işaretlenmesi gerekmektedir.
Ex: public virtual void MyMethod(){}

⦁	Virtual ile işaretlenmiş member, derived class’da ezilip yeniden yapılandırmak istiyorsak override keyword’ü ile tekrardan aynı member yeniden oluşturulur.

⦁	İlla override ile ezmek zorunda değiliz. 
Ezmezsek eğer Run-Time esnasında MyMethod MyClass içerisindeki metot’dan gelecektir.
⦁	Virtual ile işaretlenmemiş bir member’ı child class’da override ile ezemeyiz.

⦁	Child class’lardan birinde override edilmiş member, ondan sonraki alt child sınıflarında o override edilmiş hali kalıtım alan sınıflara aktarılacaktır..
Ex: Büyük Dede’de olan member Baba’da ezildiğini düşünelim ve Baba’dan kalıtım alan bana ezilmiş olan yapılanma aktarılacaktır.
Benden sonraki nesilde tekrar ezilmiş yapılanma ezilebilir.



POLIMORFIZM (ÇOK BİÇİMLİLİK)

⦁	Polimorfizm: İki ya da daha fazla nesne’nin aynı tür Class tarafından karşılanabilmesidir/referans edilebilmesidir.

⦁	Bir nesne’nin kalıtımsal olarak ilişkisi olan diğer nesnelerin referansıyla işaretlenebilmesini sağlar.

⦁	OOP ile geliştirilen koda manevratik nitelik kazandıran ve yaklaşım sergilememizi sağlayan özelliktir.

⦁	Bir sınıftan üretilen nesne ancak o nesne’nin referansıyla işaretlenebiliyordu. Yani Polimorfizm dışında.

⦁	Ancak Polimorfizm’de bu durum oluşturulan nesne’nin türünün dışında farklı türlerdeki referanslarla işaretlenme imkanı sağlar. (Bu türler kalıtım aldığı sınıflar…) 

⦁	Bir nesnenin birden fazla referans ile işaretlenebilmesi, o nesnenin birden fazla türün davranışını sergileyebilmesini sağlar.

⦁	Ex: Kartal bir kartal iken aynı zamanda kuş’tur.
Yani çoklu-form (polimorfizm)
⦁	Polimorfizm olabilmesi için teknik olarak kalıtımsal olması gerekmektedir.

⦁	Temel programlamadan basit örnek: String aslında hem String hem Object’dir
Yani string’i object ile de referans edebiliriz string ile de.

⦁	Interface , Abstract Class da polimorfizm kullanılmaktadır.
⦁	Önemli: Referans eden kısım (SOL Kısım) – Referans alması gereken kısmın Büyüğü/Atası/KalıtımVeren kısmı olmalıdır.



⦁	Interface kavramı:
Bir sınıfın içinde barındıracağı member’ların Şablonu’nun oluşturulduğu yapıdır.
Interface içine yanlızca bu imzalar tanımlanır. 
Bu interface’i kullanacak sınıfta bu imzalar zorunlu olarak oluşturulacaktır.
Bu olay o sınıfın interface’i implement etmesi sonucunda oluşturur.
Oluşturma işlemi gerçekleşmez ise compiler hata verecektir.

⦁	Interface’in bu özelliği sayesinde Can-Do ilişkisi ortaya çıkmaktadır.

⦁	Bu ilişki bir nesne’nin  davranışlarını/kabiliyetlerini belirtmektedir.
Bu interface’e baktığımızda bu interface yapısını kullanan sınıflarda hangi davranışlar var anlayabilmekteyiz.

⦁	Interface’de access modifier’lar yoktur. Zaten uygulanması zorunludur ilgili sınıfta. Opel implemente ediliyor Araba interface’inden.
⦁	Opel sınıfı içerisinde bu imzaları gövdeleriyle beraber kullanmak zorundadır.

⦁	Interface sınıfı içerisinde sadece imza tutulmaktadır.


ABSTRACTION (soyutlama)

⦁	Abstraction bir davranıştır.
⦁	Örnek: User işlemleri yapan bir sıfınımız mevcut ve içerisinde kullanıcı işlemlerini yapan memberlar var.
Bu sınıf üzerinden bir nesne oluşturulup kullanıcı doğrulama işlemi için ValidateUser metotunu kullanmak istiyoruz.
Birden fazla member olduğu için (bazen yüzlerce member olabilmekte.) geliştirici istediği member’ı kolaylıkla seçip kullanabilmesi lazım.

⦁	!!! Yani işimize yaramayan member’ları soyutlarız buna abstraction denir.

⦁	Gerekli olan member’ı getirebilmek için ilgili memberları temsil edecek referansa ihtiyaç olacaktır.

⦁	Abstraction uygularken genellikle – Interface ve Abstract class lar üzerinden uygulamak daha elverişli olabilir.

⦁	Bir class birden fazla interface’i implemente edebiliyor.




ABSTRACT CLASS 

⦁	Yarı somut – Yarı soyut sınıftır.

⦁	Abstract class kullanmak tercihtir.

⦁	Abstract class türünden bir referans ile heap de olan nesneye erişim sağlayabiliriz.

⦁	Abstract Class referans türlüdür.

⦁	Abstract Class dan direkt nesne üretilmez. Ancak Implement verdiği sınıf hiyerarşik durumda alt dan bir sınıf üzerinden nesne üretilirse Abstract Class dan bir nesne üretilir.

⦁	Abstract class ı implement’e eden sınıf (Mclass) terminolojik olarak: Concrete Class olarak adlandırılır.

⦁	Abstract Class – Abstract Class’a kalıtım verir. Implementation olmaz.

⦁	Abstract Class – class ile interface arasında kalmış bir yapıdır.



INTERFACE

⦁	Nesnelere direkt olarak bir şablon oluşturulmasına yarayan bir arayüz.

⦁	Interface özünde abstraction davranışını uygular.

⦁	Bizler bir class olmasını istediğimiz Member’ları oluşturmadan önce – Interface içerisinde imzaları ile şablon oluştururuz.

⦁	Interace içerisindeki imzalar zoraki uygulattırmaktadır.

⦁	Interface içerisine bakıldığında bu interace’i implement eden sınıfta can-do ilişkisi ile neleri yapabileceği görülebilir.

⦁	Özünde bir SÖZLEŞME’dir

⦁	Referans türlüdür.

⦁	Nesne oluşturulamaz. Ama referans noktası oluşturulabilir. Abstract Class’a benzer bir yapıdır.

⦁	Bir sınıf birden fazla interface’ı kalıtım olarak alabilir. Ama birden fazla class’dan kalıtım alamaz.

⦁	Interface yapısının içinde Class’larda oluşturulacak olan member’ların sadece imzaları oluşturulur.

⦁	İçerisinde static yapı olamaz.

⦁	Erişim belirleyici yazılmaz imzalara.

⦁	Constructor’ları yoktur.
