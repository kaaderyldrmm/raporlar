#BİLGİSAYAR BİLİMLERİ TEMEL KAVRAMLARI

#1. GİRİŞ

Bilgisayar bilimi, bilgisayarların tasarımı ve kullanımı için temel oluşturan teori, deney ve mühendislik çalışmasıdır. Hesaplamaya ve uygulamalarına bilimsel ve pratik bir yaklaşımdır. Bilgisayar bilimi; edinim, temsil, işleme, depolama, iletişim ve erişimin altında yatan yönteme dayalı prosedürlerin veya algoritmaların fizibilitesi, yapısı, ifadesi ve mekanizasyonunun sistematik çalışmasıdır. Bilgisayar biliminin alternatif, daha özlü tanımı "büyük, orta veya küçük ölçekli algoritmik işlemleri otomatikleştirme çalışması" olarak nitelendirilebilir. Verinin işlenmesini, saklanmasını ve aktarılmasını inceleyen temel kavramlar ve kurallar bütünüdür.


#2. BİLGİSAYARIN TEMEL DONANIM BİLEŞENLERİ

#2.1. CPU (İŞLEMCİ)

Bilgisayarın beyin kısmıdır; komutları işler aritmetil ve mantıksal hesaplamalar yapar.
Yazılımlardan ve işletim sisteminden gelen kotumları alır ve çalıştırır.
Bellekten (ram) verileri getirir, gerekli hesaplamaları yapar ve sonuçları tekrar belleğe gönderir.
Bilgisayardaki diğer tüm donanım parçalarının uyum içinde çalışmasını sağlar.
CPU tek başına çalışmaz, çalışan programların ihtiyaç duyduğu veriler RAM'de tutulurken, programların ve dosyaların kalıcı olarak saklanması için depolama birimleri kullanılır.


#2.2 RAM

RAM (Random Access Memory), Türkçede Rastgele Erişimli Bellek olarak adlandırılır. Bilgisayarın çalışması sırasında ihtiyaç duyduğu verileri ve çalışan programların bilgilerini geçici olarak saklayan bir bellek türüdür. CPU'nun (işlemcinin) ihtiyaç duyduğu verilere hızlı bir şekilde erişmesini sağlayarak bilgisayarın daha verimli çalışmasına yardımcı olur.
RAM, bilgisayarın geçici çalışma alanı olarak düşünülebilir. Örneğin bir programı açtığımızda, programın çalışması için gerekli verilerin bir kısmı depolama biriminden RAM'e aktarılır. CPU bu verilere RAM üzerinden hızlı bir şekilde erişir. Aynı anda birden fazla program çalıştırıldığında RAM kullanımı da artar.
RAM'in önemli özelliklerinden biri geçici (volatile) bellek olmasıdır. Bilgisayar kapatıldığında veya elektrik bağlantısı kesildiğinde RAM'de bulunan veriler silinir. Bu nedenle RAM, dosyaların kalıcı olarak saklandığı bir depolama birimi değildir. Dosyaların kalıcı olarak saklanması için HDD veya SSD gibi depolama birimleri kullanılır.
RAM'in temel olarak SRAM (Static RAM) ve DRAM (Dynamic RAM) olmak üzere farklı türleri bulunur. SRAM daha hızlı ve daha pahalıdır ve genellikle işlemcinin önbelleğinde (cache) kullanılır. DRAM ise daha yüksek kapasiteye daha düşük maliyetle ulaşabildiği için bilgisayarların ana belleğinde yaygın olarak kullanılır.
Günümüzde kullanılan RAM'ler DDR (Double Data Rate) teknolojisine dayanmaktadır. DDR3, DDR4 ve DDR5 gibi farklı nesilleri bulunmaktadır. RAM'in kapasitesi genellikle GB (Gigabyte) cinsinden ifade edilir. RAM kapasitesinin yeterli olması, aynı anda daha fazla uygulamanın çalıştırılabilmesine ve sistemin daha rahat çalışmasına katkı sağlar.
Kısaca RAM, CPU ile depolama birimleri arasında hızlı bir çalışma alanı görevi görür. Ancak RAM ile SSD veya HDD aynı şey değildir. RAM geçici olarak veri tutarken, SSD ve HDD verileri bilgisayar kapalıyken de saklayabilen kalıcı depolama birimleridir.


#2.3. DEPOLAMA BİRİMLERİ (HDD VE SSD)

Depolama birimleri, bilgisayardaki verilerin kalıcı olarak saklanmasını sağlayan donanım bileşenleridir. İşletim sistemi, programlar, belgeler, fotoğraflar ve videolar gibi veriler depolama birimlerinde tutulur. RAM'in aksine, depolama birimlerindeki veriler bilgisayar kapatıldığında silinmez.
Günümüzde bilgisayarlarda en yaygın kullanılan depolama birimleri HDD (Hard Disk Drive) ve SSD (Solid State Drive)'dir.
HDD, verileri manyetik diskler üzerinde saklayan bir depolama birimidir. 
İçerisinde dönen plakalar ve bu plakalar üzerindeki verileri okuyup yazan bir okuma-yazma kafası bulunur. 
Mekanik parçalar içerdiği için SSD'lere göre daha yavaştır. Bununla birlikte yüksek depolama kapasitesini daha uygun maliyetle sunabildiği için hâlâ kullanılmaktadır.
SSD, verileri elektronik devreler ve flash bellek teknolojisi kullanarak saklar. HDD'nin aksine hareketli mekanik parçalara sahip değildir. Bu nedenle daha hızlı veri okuma ve yazma işlemleri gerçekleştirebilir, daha sessiz çalışır ve fiziksel darbelere karşı HDD'lere göre daha dayanıklıdır.
HDD ve SSD arasındaki temel fark, verilerin saklanma ve okunma yöntemidir. HDD mekanik ve manyetik bir yapı kullanırken SSD elektronik ve flash tabanlı bir yapı kullanır. Bu nedenle SSD'ler özellikle işletim sisteminin ve uygulamaların daha hızlı açılmasını sağlamak amacıyla yaygın olarak tercih edilmektedir.
Depolama birimlerinin kapasitesi genellikle GB (Gigabyte) veya TB (Terabyte) cinsinden ifade edilir. Örneğin 512 GB veya 1 TB kapasiteli bir SSD, işletim sistemi, programlar ve kişisel dosyalar için belirli miktarda kalıcı depolama alanı sağlar.
Sonuç olarak depolama birimleri, bilgisayardaki verilerin uzun süre saklanmasını sağlar. RAM geçici bir çalışma alanıyken, HDD ve SSD kalıcı depolama alanıdır. Bu nedenle bilgisayarın çalışmasında CPU, RAM ve depolama birimleri farklı ancak birbirini tamamlayan görevler üstlenir.


#2.4. GPU (EKRAN KARTI)

GPU (Graphics Processing Unit), Türkçede Grafik İşlem Birimi olarak adlandırılır. Bilgisayarda görüntülerin, grafiklerin ve görsel işlemlerin oluşturulması ve işlenmesinden sorumlu olan işlem birimidir. GPU, özellikle yüksek miktarda görsel verinin aynı anda işlenmesi gereken durumlarda önemli bir rol oynar.
GPU'lar bilgisayar oyunlarında, video düzenleme programlarında, 3D modelleme uygulamalarında ve grafik tasarım gibi alanlarda yaygın olarak kullanılır. Ayrıca günümüzde yapay zekâ ve makine öğrenmesi gibi yüksek miktarda paralel işlem gerektiren alanlarda da GPU'lardan yararlanılmaktadır.
Bir GPU, çok sayıda küçük işlem birimine sahip olması sayesinde birçok işlemi aynı anda gerçekleştirebilir. Bu özellik, özellikle görüntü oluşturma ve karmaşık grafik hesaplamaları gibi işlemlerde yüksek performans sağlar.
GPU'lar iki temel şekilde bulunabilir: dahili (entegre) GPU ve harici (ayrık) ekran kartı. Dahili GPU işlemciye veya anakarta entegre olarak bulunur ve genellikle daha düşük güç tüketir. Harici ekran kartları ise ayrı bir donanım olarak bilgisayara takılır ve daha yüksek grafik performansı sunabilir.
GPU'nun performansında işlem gücü, bellek kapasitesi ve bellek hızı gibi çeşitli özellikler etkili olabilir. Özellikle yüksek çözünürlüklü oyunlar, profesyonel grafik uygulamaları ve video işleme gibi işlemlerde güçlü bir GPU daha iyi performans sağlayabilir.
Kısaca GPU, bilgisayarın grafik ve görsel işlemlerini gerçekleştiren önemli bir işlem birimidir. Günümüzde yalnızca görüntü oluşturmak için değil, paralel işlem yapabilme özelliği sayesinde farklı hesaplama alanlarında da kullanılmaktadır.


#2.5. ANAKART

Anakart (Motherboard), bilgisayarın temel donanım bileşenlerini bir araya getiren ve bu bileşenlerin birbiriyle iletişim kurmasını sağlayan ana devre kartıdır. CPU, RAM, GPU, depolama birimleri ve diğer donanım bileşenleri anakart üzerinden bilgisayara bağlanır.
Anakart üzerinde farklı donanım bileşenlerinin bağlanabilmesi için çeşitli bağlantı yuvaları ve bileşenler bulunur. Örneğin RAM için bellek yuvaları, ekran kartı gibi genişleme kartları için PCI Express yuvaları ve depolama birimleri için SATA veya M.2 bağlantıları bulunabilir.
Anakartın önemli görevlerinden biri, bağlı donanımlar arasında veri iletişimini sağlamak ve bu bileşenlerin birlikte çalışmasına yardımcı olmaktır. Ayrıca anakart, çeşitli donanım bileşenlerine gerekli elektrik bağlantılarının ulaştırılmasında da rol oynar.
Anakartların üzerinde BIOS veya UEFI adı verilen, bilgisayarın açılış sürecini başlatan ve donanımların temel düzeyde tanınmasını sağlayan bir yazılım sistemi bulunur. Bilgisayar açıldığında sistemin çalışmaya başlaması için gerekli ilk işlemler bu sistem aracılığıyla gerçekleştirilir.
Anakartlar farklı boyutlarda ve özelliklerde üretilebilir. ATX, Micro-ATX ve Mini-ITX gibi farklı anakart standartları bulunmaktadır. Anakart seçimi; kullanılacak işlemci, RAM, ekran kartı ve depolama birimleri gibi diğer donanımlarla uyumlu olmalıdır.
Kısaca anakart, bilgisayarın farklı donanım bileşenlerini birbirine bağlayan ve bu bileşenlerin birlikte çalışmasını sağlayan temel donanım platformudur.


#3. VERİ VE VERİ BİRİMLERİ

Bilgisayarlar, işlem yapabilmek ve bilgileri saklayabilmek için verileri belirli bir biçimde temsil eder. Metinler, sayılar, fotoğraflar, videolar ve ses dosyaları bilgisayar içerisinde sayısal veriler olarak işlenir ve saklanır. Bu verilerin bilgisayar tarafından anlaşılabilmesi için temel olarak 0 ve 1'lerden oluşan ikili sistem kullanılır.
Bilgisayarlarda verilerin miktarını ifade etmek için farklı veri birimleri kullanılır. Bu birimlerin en temel olanları bit ve byte'tır. Daha büyük veri miktarlarını ifade etmek için ise kilobyte (KB), megabyte (MB), gigabyte (GB) ve terabyte (TB) gibi birimler kullanılır.


#3.1. BİT

Bit (Binary Digit), bilgisayarlarda kullanılan en küçük veri birimidir. Bit yalnızca 0 veya 1 değerlerinden birini alabilir. Bu iki değer, bilgisayarın elektronik sistemlerinde farklı durumları temsil etmek için kullanılır.
Bir bit tek başına çok küçük miktarda bilgi ifade eder. Ancak çok sayıda bit bir araya geldiğinde daha karmaşık verilerin temsil edilmesi mümkün olur. Örneğin bilgisayar sistemlerinde sayılar, metinler, görüntüler ve diğer veri türleri çok sayıda bit kullanılarak temsil edilir.


#3.2. BYTE

Byte, 8 bitten oluşan veri birimidir.
1 Byte = 8 Bit
Byte, özellikle bilgisayarlarda veri miktarını ifade etmek için kullanılan temel birimlerden biridir. Daha büyük veri miktarları byte'ın katları olan KB, MB, GB ve TB gibi birimlerle ifade edilir.


#3.3. VERİ DEPOLAMA BİRİMLERİ

Bilgisayarlarda büyük miktardaki verileri ifade etmek için farklı ölçü birimleri kullanılır. Bunların temel sıralaması şu şekildedir:
1 Byte, Kilobyte (KB), Megabyte (MB), Gigabyte (GB), Terabyte (TB)
Bu birimler dosyaların, programların ve depolama cihazlarının kapasitesini ifade etmek için kullanılır. Örneğin bir fotoğraf birkaç megabyte, bir program birkaç gigabyte ve bir SSD yüzlerce gigabyte veya birkaç terabyte kapasiteye sahip olabilir.


#3.4. BİNARY(İKİLİ SAYI SİSTEMİ)

Binary, bilgisayarların verileri temsil etmek için kullandığı ikili sayı sistemidir. Günlük hayatta kullandığımız onluk sayı sisteminde 0'dan 9'a kadar on farklı rakam bulunurken, binary sisteminde yalnızca 0 ve 1 kullanılır.
Bilgisayarların elektronik yapısı iki farklı durumu kolayca temsil edebildiği için ikili sayı sistemi bilgisayar bilimlerinde temel bir yere sahiptir. Programların ve verilerin bilgisayar içerisindeki işlenme ve saklanma süreçlerinde binary sisteminden yararlanılır.
Sonuç olarak bit, byte ve diğer veri birimleri, bilgisayarların verileri nasıl ölçtüğünü ve temsil ettiğini anlamak için temel kavramlardır. Bu kavramların anlaşılması, bilgisayarların çalışma mantığını ve veri depolama kapasitelerini anlamayı kolaylaştırır.


#4. YAZILIM

Yazılım, bilgisayarların ve elektronik cihazların belirli bir işi yapmasını ve donanımların çalışmasını sağlayan komutlar bütünüdür.
İki grupta incelenebilir, sistem yazılımı ve uygulama yazılımı olarak ayrılır.
Sistem yazılımları, bilgisayarın ve donanımın çalışmasını sağlayan arka plan programıdır.
Uygulama yazılımları, kullanıcıların belirli bir işi yapmak için kullandığı programlardır.


#5. İŞLETİM SİSTEMİ

İşletim sistemi yazılımların en temel ve en önemlisidir; donanım kaynaklarını yöneten ve diğer uygulama yazılımlarına zemin hazırlayan özel bir sistem yazılımıdır.
Bir bilgisayarın donanım kaynaklarını yöneten ve uygulama yazılımlarına hizmet sağlayan yazılım katmanıdır.
Donanım ile uygulama yazılımları arasında ara katman görevi görerek, kullanıcıların sisteme erişmesini ve etkileşim kurmasını sağlar.Başlıca örnekleri arasında Microsoft Windows, macOS, GNU/Linux dağıtımları, Android ve iOS yer alır.

WİNDOWS: Bilgisayarlarda en yaygın kullanılan kişisel bilgisayar işletim sistemidir.

macOS: Apple tarafından Mac bilgisayarlar için geliştirilen işetim sistemidir.

Linux: Açık kaynak kodlu, genellikle sunucularda ve ileri düzey bilgisayarlarda kullanılan bir sistemdir.

Android: Mobil cihazlar ve telefonlar için geliştirilmiş yaygın bir mobil işletim sistemidir. 

İOS: Apple'ın iPhone cihazları için özel olarak ürettiği mobil işletim sistemidir.

İşletim sistemleri dijital işlevlere sahip neredeyse tüm cihazlarda bulunur, örneğin motorlu taşıtlarda, beyaz eşyalarda, akıllı saatlerde.
Modern işletim sistemleri, çoklu görev yönetimi, bellek yönetimi, dosya sistemleri ve kullanıcı arabirimi gibi kritik işlevleri yerine getirir ve cihazların performansını optimize eder.


#5.1. DRİVER

Driver, Türkçede sürücü olarak adlandırılan ve işletim sistemi ile donanım bileşenleri arasında iletişim kurulmasını sağlayan özel bir yazılımdır. Bilgisayarın bağlı olan bir donanımı doğru şekilde tanıyabilmesi ve kullanabilmesi için ilgili donanımın sürücüsüne ihtiyaç duyulabilir.
Her donanım bileşeninin çalışma şekli farklı olabileceğinden, işletim sisteminin bu donanımlarla doğrudan iletişim kurabilmesi her zaman mümkün değildir. Driver, işletim sisteminin gönderdiği komutları donanımın anlayabileceği şekilde iletir ve donanımdan gelen bilgilerin işletim sistemi tarafından kullanılmasını sağlar.
Örneğin bilgisayara bir yazıcı bağlandığında, işletim sisteminin yazıcıyı tanıması ve yazdırma işlemlerini gerçekleştirebilmesi için yazıcıya uygun bir sürücü gerekebilir. Benzer şekilde ekran kartı, ses kartı, ağ bağdaştırıcısı ve çeşitli çevre birimleri de sürücüler aracılığıyla işletim sistemiyle iletişim kurar.
Driver, işletim sistemi ile donanım arasında iletişim sağlayan yazılımdır. İşletim sistemi, driver aracılığıyla donanımın özelliklerinden yararlanarak ilgili cihazı kullanabilir.


#6.PROGRAMLAMA VE ALGORİTMA 

#6.1. PROGRAMLAMA

Programlama, bilgisayara belirli bir görevi gerçekleştirmesi için adım adım talimatlar verme sürecidir. Bilgisayarlar verilen talimatları doğrudan insan diliyle değil, programlama dilleri aracılığıyla oluşturulan komutlar şeklinde işler.
Programlama ile bilgisayara hesaplama yapmak, veri işlemek, dosya oluşturmak, kullanıcıdan bilgi almak veya bir uygulamanın belirli işlemleri gerçekleştirmesini sağlamak gibi birçok görev yaptırılabilir. Bu işlemleri gerçekleştirmek için programcı, çözmek istediği probleme uygun bir program oluşturur.
Programlama sürecinde öncelikle çözülmek istenen problem belirlenir. Daha sonra problemin nasıl çözüleceği planlanır ve bu çözüm bir programlama dili kullanılarak kodlara dönüştürülür. Yazılan kod daha sonra bilgisayar tarafından çalıştırılabilir hale getirilir.
Programlama dilleri, bilgisayar ile insan arasında bir iletişim aracı görevi görür. C#, Python, Java, C++ ve JavaScript gibi farklı programlama dilleri bulunmaktadır. Her programlama dilinin kendine özgü kuralları ve kullanım alanları vardır.
Programlama yalnızca kod yazmaktan ibaret değildir. Aynı zamanda problem çözme, mantıksal düşünme, algoritma oluşturma ve hataları tespit edip düzeltme gibi süreçleri de içerir. Bu nedenle programlama, bilgisayar bilimlerinin temel konularından biridir.
Günümüzde web siteleri, mobil uygulamalar, masaüstü programları, oyunlar ve yapay zekâ sistemleri gibi birçok teknoloji programlama kullanılarak geliştirilir.


#6.2. PROGRAMLAMA DİLLERİ

Programlama dili, bilgisayara belirli işlemleri gerçekleştirmesi için talimatlar vermeyi sağlayan kurallar ve sözdizimlerinden oluşan bir iletişim aracıdır.
Bilgisayarlar verilen talimatları doğrudan insan dilinde anlayamadığı için programlama dilleri kullanılır. 
Programcı, yapmak istediği işlemleri programlama dilinin kurallarına uygun şekilde kodlar.Yazılan bu kod daha sonra derleyici veya yorumlayıcı gibi araçlar tarafından bilgisayarın çalıştırabileceği biçime dönüştürülür veya yorumlanır.
Günümüzde birçok farklı programlama dili bulunmaktadır. C#, Python, Java, C++, JavaScript ve Go bunlardan bazılarıdır. 
Programlama dilleri kullanım alanlarına, özelliklerine ve tasarım amaçlarına göre birbirinden farklılık gösterebilir.
Örneğin;
C#, masaüstü uygulamaları, web uygulamaları ve oyun geliştirme gibi farklı alanlarda kullanılabilir. 
Python, kullanım kolaylığı ve geniş kütüphane desteği sayesinde veri bilimi, yapay zekâ ve otomasyon gibi alanlarda yaygın olarak kullanılır. 
JavaScript ise özellikle web uygulamalarının geliştirilmesinde önemli bir yere sahiptir.
Programlama dilleri farklı sözdizimlerine sahip olsa da değişkenler, koşullar, döngüler ve fonksiyonlar gibi birçok ortak programlama kavramını içerir. Bu nedenle bir programlama dilini öğrenirken yalnızca o dilin yazım kurallarını değil, programlama mantığını ve problem çözme yöntemlerini öğrenmek de önemlidir.


#6.3. ALGORİTMA

Algoritma, bir problemi çözmek veya belirli bir görevi gerçekleştirmek için izlenmesi gereken sonlu ve düzenli adımların tamamıdır. Bir algoritma, yapılacak işlemlerin hangi sırayla gerçekleştirileceğini belirler ve problemin çözümüne ulaşmayı amaçlar.
Algoritmalar yalnızca bilgisayar programlarında kullanılmaz. Günlük hayatta gerçekleştirilen birçok işlem de algoritmik bir yapıya sahiptir. Örneğin çay yapmak için suyu kaynatmak, bardağa çay koymak, sıcak su eklemek ve çayın demlenmesini beklemek gibi belirli bir sırayla gerçekleştirilen adımlar bir algoritma olarak düşünülebilir.
Bilgisayar programlarında ise algoritmalar, programın hangi işlemleri gerçekleştireceğini belirlemek için kullanılır.
Programcı öncelikle çözmek istediği problemi belirler ve problemin çözümü için gerekli adımları planlar. Daha sonra bu adımlar seçilen programlama dili kullanılarak koda dönüştürülür.
Algoritma açık ve anlaşılır olmalıdır. Karmaşık problemlerde algoritmanın doğru şekilde oluşturulması, programın daha düzenli ve verimli geliştirilmesine yardımcı olur.
Algoritmalar farklı şekillerde ifade edilebilir. Bunlardan bazıları metinsel anlatım, sözde kod (pseudocode) ve akış şemalarıdır. Sözde kod, algoritmanın programlama diline bağlı kalmadan yazılı olarak ifade edilmesini sağlarken, akış şemaları algoritmanın adımlarını semboller ve oklar kullanarak görsel olarak gösterir.


#6.4. COMPİLER(DERLEYİCİ)

Derleyici (Compiler), yüksek seviyeli bir programlama dilinde yazılan kaynak kodu bilgisayarın doğrudan anlayabileceği makine diline veya başka bir hedef dile çeviren özel bir yazılımdır.
Programcıların yazdığı kod, insanların anlayabileceği programlama dillerinden oluşur. 
Compiler, kaynak kodu analiz eder ve programlama dilinin kurallarına uygun olup olmadığını kontrol eder. Kodda sözdizimi veya bazı derleme hataları bulunuyorsa programcıya hata mesajları verir. Kod başarılı bir şekilde derlendiğinde ise çalıştırılabilir bir çıktı oluşturabilir.
Bilgisayarın bu kodu doğrudan çalıştırabilmesi için belirli bir işlemden geçirilmesi gerekir.
Derleyici, kodu satır satır değil bütün olarak çevirir. aynak kodu analiz ederek çalıştırılabilir bir forma dönüştürülmesini sağlar.
Program çalışmadan önce potansiyel hataları ve yazım yanlışlarını tespit edip raporlar.
Derlenen programlar, makine diline tamamen hazır olduğu için çok hızlı tepki verir.
Derleyiciler, programlama dillerinin bilgisayar sistemleri üzerinde çalışabilmesinde önemli bir rol oynar.