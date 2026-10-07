## DOSYA SİSTEMLERİ VE DEPOLAMA MANTIĞI


### 1. NTFS Nedir?

NTFS (New Technology File System), Microsoft tarafından geliştirilen ve özellikle Windows sistemlerinde kullanılan dosya sistemidir.
Windows'ta bilgisayarın ana diski çoğunlukla NTFS olarak biçimlendirilir.

#### NTFS'nin Temel Özellikleri

- Windows'un temel dosya sistemidir.

- Büyük dosya ve diskleri destekler.

- Dosya ve klasör izinleri konusunda gelişmiştir.
- Dosya sıkıştırma desteği vardır.
- Şifreleme özellikleriyle birlikte kullanılabilir.
- Dosya sistemi hatalarına karşı journaling (günlükleme) kullanır.


#### Journaling nedir?

Bilgisayara dosya kaydedildiği zaman dosyanın diske yazılması sırasında bilgisayar aniden kapanırsa, dosya sisteminde tutarsızlık oluşabilir. NTFS, yapılacak bazı değişiklikleri önceden bir günlükte takip eder. Sistem beklenmedik şekilde kapanırsa, dosya sisteminin toparlanmasına yardımcı olur.


### 2. ext4 Nedir?

ext4 (Fourth Extended Filesystem), Linux dünyasında çok yaygın kullanılan dosya sistemlerinden biridir. Özellikle Linux işletim sistemlerinde disk bölümlerinde sıkça karşına çıkar. 

#### ext4'ün temel özellikleri

- Linux sistemlerinde yaygın kullanılır.
- Büyük dosya ve diskleri destekler.
- Journaling özelliğine sahiptir.
- Dosya sistemi hatalarına karşı dayanıklıdır.
- Performans ve güvenilirlik açısından uzun süredir kullanılan olgun bir dosya sistemidir.
- Extent adı verilen yapı sayesinde büyük dosya bloklarını daha verimli yönetebilir.


### 3. APFS Nedir?

APFS (Apple File System), Apple tarafından geliştirilen modern dosya sistemidir. Özellikle macOS, iOS, iPadOS, watchOS ve tvOS gibi Apple işletim sistemlerinde kullanılır. APFS, Apple'ın eski HFS+ dosya sisteminin yerine geliştirilmiştir.

#APFS'nin temel özellikleri

- Apple cihazları için tasarlanmıştır.

- SSD ve flash depolama için optimize edilmiştir.

- Encryption (şifreleme) desteği güçlüdür.

- Snapshots desteği vardır.

- Copy-on-Write yaklaşımını kullanır.

- Aynı fiziksel depolama alanını birden fazla APFS biriminin paylaşmasına olanak sağlayan space sharing özelliği vardır.


### NTFS – ext4 – APFS Farkları Nelerdir?

NTFS ile ext4 arasındaki fark, öncelikle hangi işletim sisteminde kullanıldıklarıdır. NTFS Windows için geliştirilmiştir ve Windows'un güvenlik, izin ve dosya yönetimi özellikleriyle güçlü bir şekilde entegre çalışır. ext4 ise Linux sistemleri için geliştirilmiştir ve Linux ortamında kararlı, güvenilir ve performanslı çalışmasıyla öne çıkar.

NTFS ile APFS arasındaki fark, NTFS'nin Windows odaklı, APFS'nin ise Apple sistemleri odaklı olmasıdır. APFS özellikle SSD ve flash depolama için tasarlanmıştır ve snapshot, Copy-on-Write ve güçlü şifreleme gibi modern özelliklere sahiptir. NTFS ise Windows ortamındaki dosya ve klasör yönetimi, izinler ve güvenlik özellikleri konusunda öne çıkar.

ext4 ile APFS arasındaki fark, ext4'ün Linux sistemlerinde yaygın ve geleneksel bir dosya sistemi olması, APFS'nin ise Apple tarafından özellikle modern flash ve SSD depolama için geliştirilmiş olmasıdır. APFS snapshot ve Copy-on-Write gibi özellikleri yerleşik olarak sunarken ext4 daha klasik ve olgun bir dosya sistemi yaklaşımına sahiptir.

#### Üçünün arasındaki en temel fark ise tasarım amaçlarıdır. NTFS Windows, ext4 Linux, APFS ise Apple cihazları ve işletim sistemleri için optimize edilmiştir.



### Blok Yapısı Nedir?

Blok, diskin veri depolamak için ayrılmış küçük ve sabit boyutlu alanlarından biridir. Dosya sistemi, dosyaları doğrudan “diskin tamamına” yazmak yerine diski bloklara ayırır ve dosyaların verilerini bu bloklarda saklar.
Her blok belirli bir miktarda veri taşıyabilir.
Bloklara ihtiyaç duyulmasının sebebi ise, işletim sisteminin diskteki verileri düzenli bir şekilde yönetmesi gerekir. Dosya sistemi, hangi blokların dolu, hangilerinin boş olduğunu takip eder. Yeni bir dosya oluşturduğunda dosya sistemi boş blokları bulur ve dosyanın verilerini bu alanlara yerleştirir.
Dosyanın kullandığı blokların diskte yan yana olması da zorunlu değildir; dosyanın parçaları farklı bloklarda bulunabilir.



### HDD'nin Çalışma Prensibi

HDD (Hard Disk Drive), verileri manyetik olarak dönen disklerin üzerine kaydederek çalışan bir depolama birimidir. 
HDD'nin içerisinde plaka (platter), motor, okuma/yazma kafası ve aktüatör kolu gibi mekanik parçalar bulunur. Plakalar yüksek hızda dönerken okuma/yazma kafası bu plakaların üzerindeki manyetik alanları okuyarak veya değiştirerek veri işlemlerini gerçekleştirir. Bir dosya kaydedildiğinde veriler diskin üzerindeki farklı bölümlere manyetik olarak yazılır. Dosya okunmak istendiğinde ise okuma/yazma kafası ilgili bölgeye hareket eder ve veriyi okur. Bu nedenle HDD'de veriye ulaşmak için hem plakanın doğru konuma dönmesi hem de kafanın doğru konuma hareket etmesi gerekir. Mekanik parçalar kullandığı için HDD'ler SSD'lere göre daha yavaş çalışır ancak genellikle büyük depolama kapasitesi açısından daha ekonomik bir seçenektir.



### SSD'nin Çalışma Prensibi

SSD (Solid State Drive) ise verileri hareketli mekanik parçalar kullanmadan flash bellek hücrelerinde elektriksel olarak saklar. 
SSD içerisinde temel olarak NAND flash bellek, kontrolcü ve önbellek gibi bileşenler bulunur. Bir dosya kaydedildiğinde dosyanın verileri NAND flash bellek içerisindeki hücrelere elektriksel durumlar şeklinde yazılır.

Dosya okunmak istendiğinde SSD'nin kontrolcüsü ilgili bellek hücrelerini bulur ve verileri elektronik olarak okur. HDD'de olduğu gibi plakaların dönmesini veya okuma/yazma kafasının fiziksel olarak hareket etmesini beklemek gerekmez. Bu nedenle SSD'lerde erişim süresi çok daha düşüktür ve veri işlemleri daha hızlı gerçekleşir. Ayrıca hareketli parça bulunmadığı için SSD'ler mekanik darbelere karşı HDD'lere göre daha dayanıklıdır.

#### En Temle Fark
HDD, veriyi dönen manyetik plakalar ve hareket eden okuma/yazma kafası kullanarak depolar. SSD ise veriyi hareketli parça olmadan elektronik olarak flash bellek hücrelerinde depolar. Bu nedenle HDD'nin çalışma mantığı daha çok mekanik + manyetik, SSD'nin çalışma mantığı ise elektronik + flash bellek temellidir.
