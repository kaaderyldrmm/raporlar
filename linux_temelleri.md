# LİNUX TEMELLERİ

## TERMİNAL KOMUTLARI

### ls Komutu

Linux terminalinde bulunduğun dizindeki dosya ve klasörleri listelemek için kullanılır. 
Örneğin, ls komutunu yazdığında mevcut klasörde bulunan dosyaları ve alt klasörleri görebilirsin. 
ls -l komutu dosyaların izinleri, boyutları ve değiştirilme tarihleri gibi ayrıntılı bilgileri gösterirken, ls -a komutu gizli dosyaları da listeler. Bu komut, bir dizinin içeriğini görüntüleyerek hangi dosyaların bulunduğunu anlamamızı sağlar.

###  cd Komutu

İngilizce Change Directory ifadesinin kısaltmasıdır ve terminalde dizinler arasında geçiş yapmak için kullanılır. 
Örneğin, cd Belgeler komutu Belgeler klasörüne girmemizi, cd .. komutu ise bir üst dizine geçmemizi sağlar. 
cd ~ komutu kullanıcının ev dizinine gitmek için kullanılır. 
Bu komut sayesinde dosya ve klasörler arasında gezinerek çalışmak istediğimiz dizimize ulaşabiliriz.

###  grep Komutu

Dosyaların içindeki belirli kelimeleri, metinleri veya karakter kalıplarını aramak için kullanılır. 
Örneğin, grep "Linux" notlar.txt komutu, notlar.txt dosyasının içinde Linux kelimesinin geçtiği satırları gösterir. 
grep -i seçeneği büyük ve küçük harf ayrımını ortadan kaldırırken, grep -n seçeneği eşleşen satırların numaralarını da gösterir. 
Bu komut özellikle büyük metin dosyalarında, günlük kayıtlarında ve yazılım projelerinde belirli ifadeleri hızlıca bulmak için kullanılır.

###  mkdir Komutu
İngilizce Make Directory ifadesinin kısaltmasıdır ve yeni bir dizin, yani klasör oluşturmak için kullanılır.
Örneğin, mkdir Proje komutu mevcut dizinde Proje adında yeni bir klasör oluşturur. Birden fazla klasör oluşturmak için birden fazla klasör adı yazılabilir.
mkdir -p Yazilim/CSharp/OOP komutu ise gerekli üst klasörleri de oluşturarak iç içe dizinler meydana getirir.
Bu komut, dosyaları düzenli biçimde saklamak ve projeler için klasör yapısı oluşturmak amacıyla kullanılır.

### chmod Komutu

Linux sistemlerinde dosya ve klasörlerin erişim izinlerini değiştirmek için kullanılır. Bu izinler, dosyanın kimler tarafından okunabileceğini, değiştirilebileceğini veya çalıştırılabileceğini belirler.
Örneğin, chmod +x script.sh komutu dosyaya çalıştırma izni ekler. chmod 755 script.sh komutu dosya sahibine okuma, yazma ve çalıştırma izinleri verirken diğer kullanıcılara okuma ve çalıştırma izinleri verir.
Bu komut, sistem güvenliğini ve dosyalara erişimi kontrol etmek açısından önemlidir; izinler değiştirilirken dikkatli olunmalıdır.

### top Komutu

Linux sisteminde çalışan işlemleri ve bu işlemlerin sistem kaynaklarını ne ölçüde kullandığını gerçek zamanlıya yakın şekilde görüntülemek için kullanılır.
Komut çalıştırıldığında işlem kimlikleri (PID), işlemci kullanımı (CPU), bellek kullanımı (RAM) ve çalışan programların adları gibi bilgiler gösterilir.
Bu sayede hangi işlemlerin daha fazla sistem kaynağı tükettiği görülebilir ve bilgisayarın performansı takip edilebilir. 
top ekranından çıkmak için q tuşuna basılır. Bu komut özellikle sistem performansını izlemek ve kaynak tüketimini incelemek için kullanılır.



## PAKET YÖNETİMİ

Linux'ta paket yönetimi, bilgisayara yazılım yüklemeyi, yüklenmiş yazılımları güncellemeyi, kaldırmayı ve yazılımların ihtiyaç duyduğu diğer paketleri yönetmeyi sağlayan sistemdir.
Paket yöneticisi, yazılım paketlerini depolardan bulur, indirir ve gerekli bağımlılıkları da mümkün olduğunca otomatik olarak kurar.

- Paket (package), bir yazılımın kurulabilmesi için gereken dosyaları ve paket yöneticisinin kullandığı bilgileri içeren yazılım birimidir.

- Depo (repository) ise yazılım paketlerinin ve bunlara ilişkin bilgilerin sunulduğu kaynaktır.

Paket yöneticileri, bu depolardan yararlanarak yazılımların kurulmasını ve güncellenmesini kolaylaştırır.

### 1. APT

APT, .deb paketleri kullanan Debian tabanlı Linux dağıtımlarında yazılım yüklemek, güncellemek ve kaldırmak için kullanılan paket yönetim aracıdır.

APT'nin temel komutları şunlardır:

- sudo apt update: Paket depolarındaki mevcut paket listelerini ve sürüm bilgilerini yeniler. Bu komut tek başına kurulu yazılımları güncellemez; hangi paketlerin güncellenebilir olduğunu öğrenmek için yerel paket listesini tazeler.

- sudo apt upgrade: Paket listeleri yenilendikten sonra kurulu paketlerin güncellenebilir sürümlerini yükler. Güncelleme sırasında mevcut sistemin bağımlılık koşulları dikkate alınır.

- sudo apt install git: Git yazılımını kurar. Paket yöneticisi Git'in ihtiyaç duyduğu diğer paketleri de belirleyip gerekli olanları kurabilir.

- sudo apt remove git: Git paketini kaldırır ancak bazı yapılandırma dosyalarını sistemde bırakabilir.

- sudo apt purge git: Git paketini kaldırırken pakete ait sistem yapılandırma dosyalarını da kaldırmayı amaçlar. Kullanıcı dizinindeki tüm Git ayarlarının silineceği anlamına gelmez.

- sudo apt autoremove: Artık başka paketler tarafından gereksinim duyulmayan ve otomatik yüklenmiş bazı paketleri kaldırmayı önerir veya yapılandırmaya göre kaldırır. Silinecek paketleri kontrol etmek önemlidir.

- apt search python3: Depolardaki paketler arasında Python 3 ile ilgili paketleri arar.

Burada sudo, komutu yönetici yetkisiyle çalıştırmak için kullanılır. Paket kurma, kaldırma ve sistem güncelleme gibi işlemler genellikle bu yetkiyi gerektirir.

### 2. PACMAN 

Pacman, Arch Linux ailesinde yazılımları kurmak, güncellemek ve kaldırmak için kullanılan paket yöneticisidir. 
APT'den farklı bir komut yapısına sahiptir ve paket işlemlerinde harflerle gösterilen seçenekleri sıkça kullanır.

Pacman'ın temel komutları şunlardır:

- sudo pacman -Syu: Paket veritabanlarını senkronize eder ve kurulu paketleri günceller. Arch Linux'ta sistem genelindeki güncellemeler için yaygın olarak kullanılan komuttur.

- sudo pacman -S git: Git paketini kurar. Buradaki -S, depolardan paket senkronizasyonu ve kurulum işlemleri için kullanılır.

- sudo pacman -R git: Git paketini kaldırır. Temel -R seçeneği, - bağımlılıkların ve yapılandırma dosyalarının tümünü otomatik olarak temizlemek anlamına gelmez.

- pacman -Ss python: Depolarda Python ile ilgili paketleri arar. Buradaki -Ss, depo paketleri içinde arama yapar.
- pacman -Qs python: Sistemde kurulu paketler arasında Python ile ilgili paketleri arar.
- pacman -Qi git: Git paketi kuruluysa paketin sürümü, açıklaması ve bağımlılıkları gibi ayrıntıları gösterir.

Pacman kullanırken önemli bir nokta, Arch Linux'ta sistem güncellemelerini parça parça yapmak yerine genel sistem güncellemesini tercih etmektir. Bu nedenle sudo pacman -Syu komutu, yalnızca bir paketi kurmaktan farklı olarak paket veritabanlarını da yenileyip sistem paketlerini günceller.

### 3. DNF

DNF, RPM paket biçimini kullanan sistemlerde yazılımları yönetmek için kullanılan paket yöneticisidir. Bağımlılıkları çözer, paketleri depolardan indirir ve kurulum işlemlerini gerçekleştirir.

DNF'nin temel komutları şunlardır:

- sudo dnf check-update: Depolarda bulunan güncellemeleri kontrol eder. Bazı sistemlerde güncelleme mevcut olduğunda sıfırdan farklı bir çıkış kodu döndürebilir; bu tek başına bir hata olduğu anlamına gelmez.

- sudo dnf upgrade: Kurulu paketlerin mevcut güncellemelerini yükler. Fedora'da sistemin güncel tutulması için kullanılan temel komutlardan biridir.

- sudo dnf install git: Git paketini ve gerekli bağımlılıklarını kurar.

- sudo dnf remove git: Git paketini kaldırır. Paket kaldırılırken başka yazılımların ihtiyaç duyduğu bağımlılıklar etkilenebilir.

- dnf search python: Depolarda Python ile ilgili paketleri arar.
dnf info git: Git paketi hakkında sürüm, açıklama ve depo bilgileri gibi ayrıntıları gösterir.

### PAKET YÖNETİMİ NEDEN ÖNEMLİDİR ?

Paket yönetimi, Linux sistemini güvenli ve güncel tutmanın temel parçalarından biridir. Yazılımları depolardan kurmak, bağımlılıkların yönetilmesini kolaylaştırır ve güncellemeleri takip etmeyi sağlar. Özellikle yazılım geliştirme alanında Git, Python, derleyiciler ve çeşitli geliştirme araçlarını kurarken bu komutlara ihtiyaç duyarız. 
Sunucu yönetiminde ise paketleri güncel tutmak, güvenlik düzeltmelerini uygulamak ve gereksiz yazılımları kaldırmak önemlidir.


## DOSYA İZİNLERİ

Linux temellerinde dosya izinleri oldukça önemli bir konudur. Çünkü Linux, kullanıcıların hangi dosyalara erişebileceğini, hangi dosyaları değiştirebileceğini ve hangi programları çalıştırabileceğini izinler aracılığıyla kontrol eder.

### 1. Dosya İzinleri Nedir ?
Linux'ta dosya izinleri, bir dosya veya klasör üzerinde hangi kullanıcıların hangi işlemleri yapabileceğini belirleyen kurallardır. Örneğin, bir dosyayı okuyabilmiz, içeriğini değiştirebilmiz veya bir betik dosyasını çalıştırabilmiz sahip olduğumuz izinlere bağlıdır. 
Bu sistem, kullanıcıların birbirlerinin dosyalarına izinsiz müdahale etmesini önlemeye ve sistemin güvenliğini sağlamaya yardımcı olur. Linux'ta izinler temel olarak üç kullanıcı kategorisi ve üç temel izin üzerinden düzenlenir.

### 2. Kullanıcı Kategorileri

Linux dosya izinlerinde üç temel kullanıcı kategorisi bulunur.

User (u), dosyanın sahibini ifade eder. Group (g), dosyayla ilişkilendirilmiş gruba ait kullanıcıları ifade eder. Others (o) ise dosyanın sahibi veya ilgili grup üyesi olmayan diğer kullanıcıları kapsar.
Örneğin, bir dosyanın sahibi dosyayı okuyup değiştirebilirken aynı gruptaki diğer kullanıcılar yalnızca okuyabilir, diğer kullanıcıların ise dosyaya erişimi tamamen engellenebilir. Böylece dosyalar üzerindeki erişim, kullanıcı kategorilerine göre ayrı ayrı kontrol edilebilir.

### 3. Temel Dosya İzinleri

Linux'ta üç temel izin vardır: 

Read (r), Write (w) ve Execute (x). Okuma izni, dosyanın içeriğini görüntülemeye; yazma izni, dosyanın içeriğini değiştirmeye; çalıştırma izni ise uygun bir dosyanın program veya betik olarak çalıştırılmasına izin verir. 

Klasörlerde bu izinlerin anlamı biraz farklıdır:
okuma izni klasördeki isimleri listelemeyi, yazma izni klasör içindeki dosya ve dizin girişlerini değiştirmeyi, çalıştırma izni ise klasöre erişmeyi ve içindeki öğelere ulaşmayı sağlar. Klasörlerde dosya silme işlemi, yalnızca silinecek dosyanın yazma iznine değil, çoğunlukla üst klasörün yazma ve erişim izinlerine de bağlıdır.

### 4. ls -l ile Dosya İzinlerini Görüntüleme

Dosya izinlerini görmek için terminalde ls -l komutunu kullanabilirsin. Bu komut dosya ve klasörleri ayrıntılı biçimde listeler ve izinleri satırın başında gösterir. Örneğin, aşağıdaki çıktıyı inceleyelim:

-rwxr-xr-- 1 ali gelistirici 1200 Oct 15 script.sh


İlk karakter olan -, bunun normal bir dosya olduğunu belirtir. İlk karakter d olsaydı bunun bir klasör olduğunu anlardın. Sonraki dokuz karakter üç gruba ayrılır: rwx, r-x ve r--. İlk grup dosya sahibinin, ikinci grup dosyanın ait olduğu grubun, üçüncü grup ise diğer kullanıcıların izinlerini gösterir. Bu örnekte dosyanın sahibi okuyabilir, yazabilir ve çalıştırabilir; gruptaki kullanıcılar okuyup çalıştırabilir; diğer kullanıcılar ise yalnızca okuyabilir.

### 5. Sayısal İzinler 755, 644 ve 700 Ne Demektir ?

Linux'ta izinleri yalnızca r, w ve x harfleriyle değil, sayısal değerlerle de ifade edebilirsin. Okuma izni 4, yazma izni 2 ve çalıştırma izni 1 değerindedir. İstenen izinlerin sayısal değerleri toplanarak her kullanıcı kategorisinin izin değeri elde edilir. 

Örneğin, rwx için \(4+2+1=7\), r-x için \(4+1=5\), r-- için ise 4 elde edilir.
- 755: Dosya sahibi tüm izinlere sahiptir; grup ve diğer kullanıcılar okuyabilir ve çalıştırabilir. Özellikle erişilebilir olması gereken klasörlerde yaygın bir izin düzenidir.
- 644: Dosya sahibi okuyabilir ve yazabilir; grup ve diğer kullanıcılar yalnızca okuyabilir. Metin ve yapılandırma dosyalarında sık görülür.
- 700: Yalnızca dosya sahibi okuyabilir, yazabilir ve çalıştırabilir; grup ve diğer kullanıcıların hiçbir izni yoktur. Kişiye özel dosyalar ve dizinler için kullanılabilir.

Bu nedenle chmod 755 dosya.sh komutu, dosyanın izinlerini sayısal olarak 755 şeklinde ayarlar. Ancak her dosyaya 755 vermek doğru değildir; izinler dosyanın amacına ve güvenlik gereksinimlerine göre seçilmelidir.


### 6. chmod ile Dosya İzinlerini Değiştirme

chmod, Linux'ta dosya ve klasör izinlerini değiştirmek için kullanılır. 

Örneğin, chmod +x script.sh komutu dosyaya çalıştırma izni ekler. chmod u-w notlar.txt komutu dosya sahibinin yazma iznini kaldırır. chmod g+r notlar.txt komutu gruba okuma izni ekler. Sayısal kullanımda ise chmod 644 notlar.txt komutu izinleri dosya sahibi için okuma-yazma, grup ve diğer kullanıcılar için yalnızca okuma olacak şekilde düzenler. Bu komutla izinleri ihtiyaca göre değiştirebilir, dosyalara gereksiz erişimi sınırlandırabilirsin.

### 7. chown ve chgrp Komutları

Dosya izinlerinin yanında dosyanın sahibini ve bağlı olduğu grubu da bilmek gerekir. chown komutu dosyanın sahibini değiştirmek için kullanılır; örneğin sudo chown ali notlar.txt komutu dosyanın sahibini ali olarak ayarlamayı amaçlar. chgrp komutu ise dosyanın grubunu değiştirir; örneğin sudo chgrp gelistirici notlar.txt komutu dosyanın grubunu gelistirici olarak ayarlar. Bu işlemler için gerekli yetkilere sahip olman gerekir. Dosya sahibi veya grup değiştiğinde dosyanın izin harfleri aynı kalabilir, ancak izinlerin hangi kullanıcı ve gruplara uygulandığı değişebilir.

### Dosya İzinleri Neden Önemlidir?

Dosya izinleri, Linux sistemlerinde güvenliği ve erişim kontrolünü sağlamanın temel yollarından biridir. Örneğin, bir sunucuda parola içeren bir dosyanın bütün kullanıcılar tarafından okunabilmesi güvenlik riski oluşturabilir. Benzer şekilde, yalnızca yönetici tarafından değiştirilmesi gereken sistem dosyalarına gereğinden fazla yazma izni verilmesi sistemin zarar görmesine yol açabilir. Bu nedenle dosya izinleri belirlenirken yalnızca gerekli kullanıcılara gerekli izinlerin verilmesi, yani en az ayrıcalık ilkesi, temel bir güvenlik yaklaşımıdır.

## SERVİS YÖNETİMİ

### Linux'ta Servis Nedir?

Linux'ta servis (service), işletim sistemi veya diğer yazılımlar için belirli görevleri arka planda yerine getiren bir programdır. 
Örneğin, bilgisayarın ağ bağlantısını yöneten, web sitesi sunan veya belirli zamanlarda yedekleme yapan programlar servis olarak çalışabilir. Bazı servisler bilgisayar açıldığında otomatik başlatılırken bazıları yalnızca ihtiyaç duyulduğunda çalıştırılır. Servisler genellikle kullanıcıdan sürekli bir etkileşim beklemeden görevlerini yerine getirir. Linux'ta bu tür arka plan süreçleri çoğunlukla daemon olarak da adlandırılır.
Örneğin, bir web sunucusu olan Nginx, web sayfalarını ziyaretçilere sunmak için arka planda çalışabilir. Bilgisayarında Nginx servisi çalışmıyorsa web sunucusu hizmeti de kullanılamayabilir.

### systemctl Nedir?

systemctl, Linux'ta systemd sistem ve servis yöneticisiyle iletişim kurmak için kullanılan komut satırı aracıdır. Servisleri başlatmak, durdurmak, yeniden başlatmak, durumlarını kontrol etmek ve sistem açılışında otomatik çalışıp çalışmayacaklarını ayarlamak için kullanılır. systemd kullanan birçok Linux dağıtımında servis yönetiminin temel araçlarından biridir.
Örneğin, bilgisayarında SSH servisi varsa bu servisin çalışıp çalışmadığını kontrol etmek için systemctl komutunu kullanabilirsin. Ancak her Linux dağıtımı systemd kullanmaz; dolayısıyla systemctl her sistemde kullanılabilir değildir.

###  Temel Systemctl Komutları
systemctl status: Bir servisin çalışma durumunu ve ilgili bilgileri görüntüler. Örneğin, systemctl status ssh komutu SSH servisinin çalışıp çalışmadığını, son durumunu ve bazı günlük bilgilerini gösterir. Servis adı dağıtıma göre ssh veya sshd olabilir.

- sudo systemctl start nginx: Nginx servisini başlatır. Bu komut, servisi o anda çalıştırır; ancak bilgisayar yeniden başlatıldığında otomatik olarak başlayacağını garanti etmez.

- sudo systemctl stop nginx: Çalışan Nginx servisini durdurur. Servisin sunduğu hizmet, yeniden başlatılana kadar kullanılamayabilir.

- sudo systemctl restart nginx: Nginx servisini yeniden başlatır. Yapılandırma veya yazılım değişikliklerinden sonra kullanılabilir; fakat servis yeniden başlatılırken hizmette kısa süreli kesinti yaşanabilir.

- sudo systemctl reload nginx: Servis destekliyorsa yapılandırma ayarlarını yeniden yükler. restart komutundan farklı olarak servisin tamamen durdurulup başlatılması yerine ayarların yeniden okunmasını sağlar.

- sudo systemctl enable nginx: Nginx servisinin sistem açılışında otomatik başlatılmasını etkinleştirir. Bu komut, servisi mutlaka o anda başlatmaz.

- sudo systemctl disable nginx: Nginx servisinin açılışta otomatik başlatılmasını devre dışı bırakır. Servis o anda çalışıyor olabilir; disable komutu tek başına onu durdurmaz.

- sudo systemctl enable --now nginx: Servisi hem hemen başlatır hem de sistem açılışında otomatik çalışacak şekilde etkinleştirir.

### Servisin Durumları Ne Anlama Gelir?
Bir servisin durumunu kontrol ettiğinde farklı ifadeler görebilirsin. active (running), servisin çalıştığını; inactive (dead), şu anda çalışmadığını; failed ise servisin başlatılamadığını veya bir hata nedeniyle başarısız duruma geçtiğini belirtir. enabled, servisin sistem açılışında otomatik başlatılmasının etkinleştirildiğini; disabled ise bu otomatik başlatma ayarının etkin olmadığını ifade eder. Burada önemli bir ayrıntı vardır: Bir servisin enabled olması onun mutlaka çalıştığı, disabled olması da mutlaka durmuş olduğu anlamına gelmez. Çalışma durumu ile açılış ayarı farklı kavramlardır.

### Sistemdeki Servisleri Listeleme

Linux'ta hangi servislerin bulunduğunu ve hangi durumda olduklarını incelemek için de systemctl kullanılır. 
systemctl list-units --type=service komutu, sistem tarafından o anda yüklenmiş olan servis birimlerini listeler. systemctl list-units --type=service --state=running komutu ise çalışan servisleri gösterir. Bilgisayarda tanımlı servis birimlerinin tamamını, o anda çalışıp çalışmadıklarına bakmaksızın görmek için systemctl list-unit-files --type=service komutu kullanılabilir. Bu komutlar, sistemde hangi hizmetlerin bulunduğunu ve bunların nasıl yapılandırıldığını anlamana yardımcı olur.

### Servis Kayıtlarını İnceleme: journalctl

Bir servis başlatılamıyorsa veya beklenmedik şekilde hata veriyorsa yalnızca systemctl status çıktısı yeterli olmayabilir. Bu durumda journalctl, systemd günlük kayıtlarını görüntülemek için kullanılır. Örneğin, journalctl -u nginx komutu Nginx servisiyle ilişkili günlük kayıtlarını gösterir. journalctl -u nginx -f komutu ise yeni kayıtları takip etmeyi sağlar; çıkmak için Ctrl + C tuşlarına basabilirsin. Bu kayıtlar, servis hatalarını araştırırken ve sorunun nedenini anlamaya çalışırken oldukça faydalıdır.

