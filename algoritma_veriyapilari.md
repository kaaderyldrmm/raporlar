# ALGORİTME VE VERİ YAPILARI MANTIĞI

## NEDEN VERİ YAPISI VAR ?

Veri yapıları, programlarda kullanılan verileri düzenli bir şekilde saklamak, bu verilere kolayca ulaşmak ve veriler üzerinde işlem yapmak için kullanılır. 
Bir program geliştirirken öğrenci notları, ürünler, müşteriler veya kargo bilgileri gibi çok sayıda veriyle çalışabiliriz. Bu verileri birbirinden bağımsız değişkenlerde saklamak yerine belirli bir düzen içerisinde tutmak, programı daha kolay yönetmemizi sağlar. Örneğin, bir okul otomasyonunda 500 öğrencinin notlarını takip etmek istediğimizi düşünelim. Her öğrenci için ayrı bir değişken oluşturmak yerine, bu notları bir dizi (array) içerisinde saklayabiliriz. Böylece bütün notlara ulaşabilir, notların ortalamasını hesaplayabilir veya en yüksek notu bulabiliriz. Veri yapıları, verilerin nasıl saklanacağına ve düzenleneceğine karar vermemize yardımcı olur. Her veri yapısının kullanım amacı da farklı olabilir. Örneğin, diziler birden fazla veriyi bir arada tutmak için, kuyruklar verileri geliş sırasına göre işlemek için, yığınlar ise son eklenen veriye ilk ulaşılması gereken durumlarda kullanılır. Doğru veri yapısını seçmek, özellikle çok fazla veriyle çalışırken işlemleri daha düzenli ve verimli hâle getirebilir.

Algoritma ve veri yapıları birbiriyle ilişkili olsa da farklı kavramlardır. Veri yapısı, verileri nasıl sakladığımızı; algoritma ise bir problemi çözmek için hangi adımları izlediğimizi ifade eder. Örneğin, öğrenci notlarını bir dizide sakladığımızda veri yapısını kullanmış oluruz. Bu notların arasından en yüksek olanı bulmak için notları karşılaştırıp en büyük değeri belirlediğimizde ise bir algoritma uygulamış oluruz. Yazılım geliştirirken önce problemi anlamak, verileri nasıl saklayacağımıza karar vermek, ardından problemi çözecek adımları belirlemek önemlidir. Bu nedenle algoritma ve veri yapılarını öğrenmek, yalnızca kod yazmayı değil, karşılaştığımız problemleri mantıklı, düzenli ve verimli bir şekilde çözmeyi de öğretir.



## Big-O MANTIĞI NEDİR ?

Big-O, bir algoritmanın yaptığı işin, üzerinde çalıştığı veri miktarı arttıkça nasıl büyüdüğünü anlamamızı sağlayan bir gösterimdir. Başka bir deyişle, veri sayısı arttığında algoritmanın ne kadar daha fazla işlem yapacağını anlamamıza yardımcı olur. Burada önemli olan yalnızca algoritmanın kaç saniyede çalıştığı değildir. Bilgisayarın donanımı değişebilir, ancak algoritmanın işlem sayısının veri miktarıyla nasıl değiştiğini inceleyerek farklı algoritmaları karşılaştırabiliriz.

Örneğin, bir sınıfta 10 öğrenci olduğunu ve öğretmenin belirli bir öğrenciyi bulmak istediğini düşünelim. Öğretmen öğrencileri tek tek kontrol ederse en fazla 10 öğrenciyi incelemesi gerekir. Ancak sınıfta 1.000 öğrenci olursa, aradığı öğrenci son sıradaysa 1.000 öğrenciyi kontrol etmesi gerekebilir. İşte Big-O, veri miktarı arttığında algoritmanın çalışma yükünün nasıl değiştiğini anlamamızı sağlar.


## Array, Linked List, Stack, Queue, HashMap Farkı

### Array

Array, yani dizi, birden fazla veriyi belirli bir sıra içerisinde saklar. Her elemanın bir indeks numarası vardır ve indeksler 0'dan başlar. Dizinin en önemli özelliklerinden biri, indeksini bildiğimiz elemana doğrudan ulaşabilmemizdir.
Örneğin, beş öğrencinin notunu bir dizide sakladığımızda üçüncü öğrencinin notuna notlar[2] yazarak ulaşabiliriz. Bu işlem O(1) zaman karmaşıklığındadır. Ancak klasik C# dizilerinin boyutu oluşturulurken belirlenir; sonradan doğrudan büyütülemez.

Eleman sayısı belli olduğunda ve verilere indeks üzerinden hızlıca ulaşmak istediğimizde kullanırız.

### Linked List

Linked List, yani bağlı liste, verilerin düğümler (node) aracılığıyla birbirine bağlandığı bir yapıdır. Her düğüm genellikle kendi verisini ve bir sonraki düğümün bağlantısını tutar. Array'den farklı olarak elemanların bellekte yan yana bulunması gerekmez.

Örneğin, bir bağlı listede beş eleman varsa dördüncü elemana ulaşmak için genellikle ilk düğümden başlayıp bağlantıları sırayla takip ederiz. Bu yüzden belirli bir konumdaki elemana erişmek O(n) olabilir. Buna karşılık, zaten bilinen bir düğümün yanına eleman eklemek veya silmek, bağlantıları güncelleyerek O(1) zamanda yapılabilir.

Eleman ekleme ve silme işlemlerinin belirli konumlarda sık yapıldığı durumlarda, özellikle ilgili düğüme zaten erişimimiz varsa kullanırız.


### Stack (Yığın)

Stack, üst üste konmuş tabaklar gibi çalışır. Temel mantığı LIFO (Last In, First Out), yani son giren ilk çıkar kuralıdır. Yeni eleman en üste eklenir ve elemanlar en üstten çıkarılır.

Örneğin, bir tabağı yığının en üstüne koyarsan, önce o tabağı alırsın. Daha önce koyduğun tabaklara ulaşmak için üsttekileri çıkarman gerekir.

C# dilinde Stack<T> koleksiyonu kullanılır. Push() eleman ekler, Pop() en üstteki elemanı çıkarıp döndürür, Peek() ise çıkarmadan en üstteki elemanı gösterir.

Geri alma (Undo) işlemlerinde, tarayıcı geçmişinde geri gitme mantığında ve fonksiyon çağrılarının takibinde kullanılır.

### Queue

Queue, yani kuyruk, marketteki sıra gibi çalışır. Temel mantığı FIFO (First In, First Out), yani ilk giren ilk çıkar kuralıdır. İlk eklenen eleman ilk çıkarılır.

Örneğin, bir yazıcıya üç belge gönderildiğinde belgelerin geliş sırasına göre yazdırılması istenebilir. İlk gönderilen belge önce işlenir. C# dilindeki Queue<T> koleksiyonunda Enqueue() eleman ekler, Dequeue() sıradaki elemanı çıkarıp döndürür, Peek() ise sıradaki elemanı çıkarmadan gösterir.

### HashMap

HashMap, verileri bir anahtar (key) ve ona karşılık gelen değer (value) şeklinde saklar. C# dilindeki karşılığına en yakın yaygın koleksiyon Dictionary<TKey, TValue> sınıfıdır.

Örneğin, öğrenci numarasını anahtar, öğrencinin adını değer olarak tutabiliriz. Böylece öğrenciyi bulmak için listedeki herkesi sırayla kontrol etmek yerine öğrenci numarasıyla arama yapabiliriz. Uygun koşullarda ekleme, arama ve silme işlemleri ortalama O(1) zaman alır; ancak bazı durumlarda daha yavaş olabilir.

Bir veriye belirli ve benzersiz bir anahtar üzerinden hızlıca ulaşmak istediğimizde. Aynı anahtar ikinci kez eklenemez.

### Bu veri yapılarının temel farkı, verileri saklama ve onlara erişme biçimleridir. Array, verilere indeks numarasıyla doğrudan ulaşmayı sağlarken Linked List, verileri birbirine bağlı düğümler hâlinde tutar. Stack, son eklenen veriyi ilk çıkarır (LIFO); Queue ise ilk eklenen veriyi ilk çıkarır (FIFO). HashMap (Dictionary) ise diğerlerinden farklı olarak verileri anahtar-değer ilişkisiyle saklar ve anahtar üzerinden hızlı erişim sağlar. Kısacası Array indeksle, Linked List bağlantılarla, Stack ve Queue belirli bir sırayla, HashMap ise anahtar üzerinden veri yönetir.