## İŞLETİM SİSTEMLERİ TEMELLERİ (OS BASİC)


#KERNEL NEDİR?

İşletim sistemi çekirdeği, kısaca çekirdek veya kernel işletim sistemindeki her şeyin üzerinde denetimi olan merkezi yazılım bileşenidir.
Uygulamalar ve donanım arasında bir köprü görevi görür.
Çekirdeğin görevleri sistemin kaynaklarını yönetmeyi de kapsamaktadır.
İşletim sistemi görevleri, tasarımları ve uygulanmalarına göre farklı çekirdekler tarafından farklı şekillerde yapılır.
Çekirdek veya kernel; monolitik, mikro ve hibrit çekirdek olarak türlere ayrılır.

# Monolitik Çekirdek
İşletim sisteminin temel işlemlerini tek bir çekirdek katmanında yönetir. Aygıt sürücüleri ve işletim sistemi hizmetleri de çekirdek modunda çalışır. Yapısının daha basit olması nedeniyle donanımlarla uyumluluğu yüksektir ve performans açısından avantaj sağlayabilir. Ancak çekirdekte meydana gelen bir hata veya güvenlik açığı tüm sistemi etkileyebilir. **Linux** monolitik çekirdek yapısına örnek olarak verilebilir.

# Mikro Çekirdek
İşletim sisteminin yalnızca temel hizmetlerini çekirdek modunda çalıştırır. Uygulamalar ve aygıt sürücüleri gibi diğer hizmetler ise daha kısıtlı olan kullanıcı modunda çalışır. Kullanıcı modundaki programlar çekirdeğe ve donanıma doğrudan erişemez; ihtiyaç duydukları işlemler için çekirdek ile iletişim kurarlar. Bu yapı, sistemi daha güvenli ve modüler hâle getirir. Ancak işlemler arasındaki iletişim nedeniyle monolitik çekirdeğe göre daha yavaş olabilir.
**QNX** ve **Minix** mikro çekirdek mimarisine örnek olarak verilebilir.

# Hibrit Çekirdek
Monolitik ve mikro çekirdek mimarilerinin bazı özelliklerini bir arada kullanır. İşletim sistemi hizmetlerinin bir kısmı çekirdek modunda, bir kısmı ise kullanıcı alanında çalışır. Bu yapı ile performans ve güvenlik arasında bir denge kurulması amaçlanır. **Windows** ve **macOS** hibrit çekirdek mimarisine örnek olarak verilebilir.


#LİNUX ÇEKİRDEĞİ

UNIX benzeri ve monolitik bir çekirdek mimarisine sahiptir. İlk olarak 80386 tabanlı IBM PC uyumlu bilgisayarlar için geliştirilmiş olsa da günümüzde **x86, ARM ve RISC-V** gibi birçok farklı işlemci mimarisini desteklemektedir.
Linux çekirdeğinin önemli özelliklerinden biri **dinamik modül desteğidir**. İşletim sistemi çalışırken ihtiyaç duyulan aygıt sürücüleri ve diğer çekirdek bileşenleri modüller aracılığıyla sisteme eklenebilir. Örneğin, bir Ethernet kartının sürücüsü sistem çalışırken çekirdeğe yüklenebilir. Kullanılmayan modüller de daha sonra bellekten kaldırılabilir. Bu özellik, Linux çekirdeğinin esnek ve modüler bir yapıya sahip olmasını sağlar.
Linux sistemlerinde çekirdek modülleri genellikle **.ko (Kernel Object)** uzantısıyla kullanılır. Bu modüller, kullanıcı modunda çalışan uygulamalardan farklı olarak çekirdek ile birlikte çalışır.



#SÜREÇ (PROCESS) NEDİR?

Process, çalışan bir programın işletim sistemi tarafından oluşturulmuş çalışma hâlidir.
Açılan her bir program yada uygulama işletim sistemi tarafından **procces** olarak ele alınır.
Program, diskte duran çalıştırılabilir dosyadır.
Process'in kendine ait kaynakları vardır, bir procces çalılırken işletim sistemi ona çeşitli kaynaklar tahsis eder.

#İŞ PARÇACIĞI (THREAD) NEDİR?

Thread, bir process içerisindeki işlerin yürütüldüğü en temel çalışma birimlerinden biridir.
Yani, Process bir çalışma ortamıysa, thread o ortamda işi yapan çalışandır.
Bir process'in birden fazla thread'i olabilir.


## İkisi arasındaki en önemli far bellek paylaşımıdır. İki farklı bellek arasında bir tane thread açılabilir. Bu nedenle thread'ler arasında veri paylaşımı daha kolay olabilir. Fakat bunun bir dezavantajı da vardır: aynı veriye aynı anda erişmeye çalışırlarsa senkronizasyon problemleri ortaya çıkabilir.



#BELLEK YÖNETİMİ

Bellek yönetimi, işletim sisteminin bilgisayarın ana belleği olan RAM'i düzenli ve verimli bir şekilde kullanmasını sağlayan işlemlerin bütünüdür. Bilgisayarda aynı anda birçok program çalışabildiği için her programın belleğe ihtiyacı vardır. 
İşletim sistemi, hangi programın ne kadar belleğe ihtiyaç duyduğunu takip eder ve uygun bellek alanlarını programlara tahsis eder. Programların kullandığı bellek alanlarının birbirleriyle karışmasını önlemek ve bir programın başka bir programa ait belleğe izinsiz erişmesini engellemek de işletim sisteminin görevlerinden biridir. Böylece sistemin güvenli ve kararlı bir şekilde çalışması sağlanır.

Bellek yönetiminde önemli kavramlardan biri sanal bellektir (Virtual Memory). 
Sanal bellek, programların fiziksel RAM'i doğrudan kullanmak yerine kendilerine ait bir sanal adres alanı varmış gibi çalışmasını sağlar. İşletim sistemi ve donanımdaki bellek yönetim birimleri, programların kullandığı sanal adresleri fiziksel RAM'deki adreslerle eşleştirir. Bu yapı sayesinde her programın bellek alanı diğerlerinden izole edilebilir ve RAM daha verimli kullanılabilir.

İşletim sistemi belleği yönetirken sayfalama (paging) yönteminden de yararlanabilir. Bu yöntemde bellek, page (sayfa) adı verilen sabit boyutlu küçük parçalara ayrılır. Programların kullandığı sanal bellek sayfalara bölünür ve bu sayfalar fiziksel bellekte farklı konumlarda tutulabilir. RAM'de yeterli alan bulunmadığında, daha az kullanılan bazı sayfalar geçici olarak depolama alanına taşınabilir ve ihtiyaç olduğunda tekrar RAM'e getirilebilir. Bu işlem sanal belleğin kullanılmasını mümkün kılar; ancak depolama birimleri RAM'den daha yavaş olduğu için bu işlemin aşırı gerçekleşmesi bilgisayarın yavaşlamasına neden olabilir.

Bellek yönetimi ayrıca programların kullandığı stack (yığın) ve heap (öbek) gibi bellek alanlarıyla da ilişkilidir. Stack genellikle metot çağrıları ve yerel değişkenler gibi kısa süreli ve düzenli şekilde kullanılan verilerle ilişkilidir. 
Heap ise program çalışırken dinamik olarak oluşturulan nesnelerin tutulduğu alandır. Örneğin C# programlarında new anahtar kelimesiyle oluşturulan nesneler heap ile ilişkilidir. C# gibi yönetilen programlama dillerinde kullanılmayan nesnelerin belleğinin geri kazanılmasında Garbage Collector (Çöp Toplayıcı) görev alır.

Kısacası bellek yönetimi, işletim sisteminin RAM'i programlar arasında düzenli bir şekilde paylaştırmasını, programların birbirlerinin belleğine izinsiz erişmesini engellemesini, belleğin gerektiğinde sanal bellek ve sayfalama gibi yöntemlerle yönetilmesini ve kullanılmayan bellek alanlarının yeniden kullanılabilmesini sağlayan mekanizmadır. Bu nedenle bellek yönetimi, işletim sisteminin hem performansını hem de güvenliğini doğrudan etkileyen temel görevlerden biridir.



#CPU ZAMANLAYICILARI (CPU SCHEDULİNG)

CPU zamanlayıcısı, işletim sisteminin işlemcinin hangi process (süreç) veya thread'e (iş parçacığına) ne zaman çalışması gerektiğine karar veren mekanizmadır. Bilgisayarda aynı anda birçok program çalışıyor gibi görünse de CPU'nun işlem yapabilme kapasitesi sınırlıdır. Özellikle tek çekirdekli bir işlemcide aynı anda yalnızca bir işlem yürütülebilir. İşletim sistemi bu nedenle çalışan işlemler arasında CPU'yu paylaştırır ve hangi işlemin ne zaman çalışacağını belirler. Çok çekirdekli işlemcilerde ise birden fazla işlem aynı anda yürütülebilir, ancak yine de hangi thread'in hangi CPU çekirdeğinde çalışacağı gibi kararların verilmesi gerekir.

CPU zamanlamasının temel amacı, işlemcinin verimli kullanılmasını sağlamaktır. Örneğin bilgisayarında aynı anda bir tarayıcı, Visual Studio ve müzik uygulaması açık olsun. Sen Visual Studio'da kod yazarken müzik uygulamasının da çalışmaya devam etmesi gerekir. İşletim sistemi, CPU zamanlayıcısı aracılığıyla bu programların içerisindeki çalışmaya hazır thread'ler arasında işlemci zamanını paylaştırır. Bu nedenle kullanıcı açısından programlar aynı anda çalışıyor gibi görünür.

Zamanlayıcı bir thread'i CPU üzerinde çalıştırırken belirli bir süre sonra başka bir thread'e geçebilir. Bu geçişe context switch (bağlam değiştirme) denir. Örneğin CPU önce Thread A'yı çalıştırırken daha sonra Thread B'ye geçerse işletim sistemi Thread A'nın çalışma durumuyla ilgili bilgileri saklar ve Thread B'nin daha önce saklanan durumunu yükleyerek çalışmasına devam eder. Daha sonra tekrar Thread A'ya dönülebilir. Bu işlemler çok hızlı gerçekleştiği için kullanıcı genellikle bu geçişleri fark etmez.

CPU zamanlamasında farklı zamanlama algoritmaları kullanılabilir. Bunlardan biri First Come, First Served (FCFS) yöntemidir. Bu yöntemde CPU'yu kullanmak için önce gelen işlem önce çalıştırılır. Bir diğer yöntem Shortest Job First (SJF) olup tahmini çalışma süresi daha kısa olan işlemlere öncelik verir. Round Robin yönteminde ise işlemlere belirli bir zaman dilimi (time slice / quantum) verilir ve süre dolduğunda sıradaki işleme geçilir. Ayrıca işletim sistemleri işlemlere verilen öncelik (priority) değerlerini de kullanabilir; daha yüksek öncelikli işlemler CPU'ya erişimde öncelik kazanabilir.

Burada önemli olan nokta, CPU zamanlayıcısının yalnızca "hangi program çalışacak?" sorusuna cevap vermemesidir. Aslında daha alt seviyede hangi hazır thread'in CPU üzerinde çalışacağına karar verir. Bir process'in içerisinde birden fazla thread bulunabileceği için zamanlayıcı çoğu modern işletim sisteminde thread'leri planlama birimi olarak ele alır.






