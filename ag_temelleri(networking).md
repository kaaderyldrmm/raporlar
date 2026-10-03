## AĞ TEMELLERİ (NETWORKİNG)

#IP 

interneti ya da TCP/IP protokolünü kullanan diğer paket anahtarlamalı ağlara bağlı cihazların, ağ üzerinden birbirleri ile veri alışverişi yapmak için kullandıkları adrestir.
İnternet'e bağlanan her cihaza, İnternet Servis Sağlayıcısı tarafından bir "public" IP adresi atanır ve internete bağlı cihazlar birbirleriyle bu "public" IP adresleri üzerinden ulaşırlar.
IP adresine sahip iki farklı cihaz aynı ağda olmadıkları durumlarda, yönlendiriciler (router) ya da yönlendirme (routing) özelliği olan cihazlar vasıtası ile birbirleri ile iletişim kurarlar.
IP adresi özel (private) IP adresi olarak tanımlanır ve sadece yerel ağlarda iletişim sağlayabilir. Diğer ağlar ile iletişim sağlanabilmesi için cihazın genel (public) IP adresine sahip olması gerekmektedir.

#PORT 

Port, bir bilgisayarda çalışan belirli bir uygulama veya servise ulaşmak için kullanılır. Aynı bilgisayarda aynı anda birçok uygulama çalışabileceği için gelen verinin hangi uygulamaya gönderileceğini belirlemek gerekir. 
Örneğin 192.168.1.10:5000 ifadesinde 192.168.1.10 IP adresini, 5000 ise port numarasını ifade eder. Kısaca IP hangi bilgisayar olduğunu, port ise o bilgisayardaki hangi uygulama veya servise ulaşılacağını belirtir.

#DNS

internete veya bir ağa bağlı bilgisayar, servis ve diğer kaynakların adlandırılmasını ve bu adlar arasındaki iletişimi düzenleyen hiyerarşik ve dağıtılmış bir sistemdir. 
İnternete bağlı her birimin kendine ait bir IP adresi bulunur ve bu IP adresleri kullanıcıların kolayca hatırlayabilmesi için www.siteismi.com gibi alan adlarıyla eşleştirilir. 
DNS sunucuları, alan adlarının hangi IP adreslerine karşılık geldiği bilgisini kayıtlı tutar ve alan adlarını gerekli sayısal IP adreslerine dönüştürür. 
DNS, alan adlarını ve IP adreslerini yönetmek için her alan adına yetkili ad sunucuları atar; bu yapı dağıtılmış ve arızaya toleranslı çalışır ve tek bir merkezi veritabanına ihtiyaç duymaz.
DNS sistemi aynı zamanda alan adı hiyerarşisi ile IP adresleri arasındaki çeviriyi sağlayan bir veritabanı ve iletişim protokolü yapısına sahiptir.
DNS veritabanında IP adresleri (A ve AAAA), posta sunucuları (MX), ad sunucuları (NS), ters DNS aramaları (PTR) ve alan adı takma adları (CNAME) gibi çeşitli kayıtlar bulunabilir. DNS, 1980'lerden beri yaygın olarak kullanılmaktadır.

#TCP

TCP (Transmission Control Protocol), TCP/IP protokol takımının taşıma katmanında yer alan ve IP ağı üzerinden iletişim kuran uygulamalar arasında verilerin güvenilir, sıralı ve hata kontrolü yapılmış şekilde iletilmesini sağlayan bir protokoldür. 
TCP; WWW, e-posta, dosya transferi, uzak yönetim ve akış medyası gibi birçok internet uygulamasında kullanılır. HTTP, HTTPS, POP3, SSH, SMTP, Telnet ve FTP gibi yaygın internet protokollerinin veri iletimi TCP üzerinden gerçekleştirilebilir. 
TCP bağlantı odaklıdır; veri aktarımından önce gönderici ve alıcı arasında bağlantı kurulması gerekir ve bu bağlantı üç aşamalı el sıkışma (3-way handshake) yöntemiyle gerçekleştirilir. TCP ayrıca veri kaybı durumunda yeniden gönderim ve hata tespiti gibi mekanizmalar kullanarak güvenilirliği artırır ve ağ tıkanıklığını önlemeye yönelik işlemler içerir. Ancak bu güvenilirlik mekanizmaları gecikmeyi artırabilir. Güvenilir veri akışının gerekli olmadığı ve hızın öncelikli olduğu durumlarda UDP kullanılabilir. TCP'nin ayrıca hizmeti engelleme (Denial of Service), bağlantı kaçırma, TCP veto ve sıfırlama saldırıları gibi güvenlik açıkları bulunmaktadır.

#UDP

UDP (User Datagram Protocol – Kullanıcı Veribloğu İletişim Kuralları), TCP/IP protokol takımının aktarım katmanında bulunan protokollerden biridir ve verileri bağlantı kurmadan gönderir. UDP, minimum protokol mekanizmasıyla bir uygulamadan diğerine mesaj gönderilmesini sağlar. 
Bağlantı kurulumu, akış kontrolü ve tekrar iletim işlemlerini gerçekleştirmediği için veri iletim süresini azaltır ve fazla bant genişliği kullanmaz. Bu nedenle özellikle geniş alan ağlarında (WAN) ses ve görüntü aktarımı gibi gerçek zamanlı veri iletişimlerinde kullanılır. 
UDP güvenilir olmayan bir aktarım protokolüdür; gönderilen paketin karşı tarafa ulaşıp ulaşmadığını takip etmez ve teslim edildiğine dair onay vermez. Paketin teslim garantisini isteyen uygulamalar TCP'yi kullanır. UDP kullanan protokollere **DNS, TFTP ve SNMP** örnek olarak verilebilir. 
UDP üzerinden güvenilir veri göndermek isteyen bir uygulamanın, bu güvenilirliği kendi yöntemleriyle sağlaması gerekir. UDP ve TCP aynı iletişim yolunu kullandığında ise TCP'nin oluşturduğu yüksek veri trafiği, UDP ile yapılan gerçek zamanlı veri aktarımının servis kalitesini düşürebilir.


#Paket Yapısı Nasıl Çalışır?

İnternette gönderilen veriler tek parça halinde değil, küçük paketler halinde iletilir. Her paket temel olarak başlık (header) ve veri (data/payload) bölümlerinden oluşur. Başlık kısmında kaynak ve hedef IP adresi, port ve protokol gibi iletişimle ilgili bilgiler bulunurken, veri kısmında gönderilmek istenen asıl bilgi yer alır. Paketler ağ üzerinden yönlendiriciler aracılığıyla hedef bilgisayara ulaştırılır. Veri birden fazla pakete bölünmüşse, hedef bilgisayarda bu paketler uygun şekilde işlenerek asıl veri yeniden oluşturulur. Yani veri, paketlere bölünür, başlık bilgileri eklenir, ağ üzerinden gönderilir, hedefte işlenerek yeniden birleştirilir.


#Ping Nedir ve Ne İşe Yarar?

Bir cihazın başka bir cihaza veri gönderip geri alma süresi milisaniye cinsinden ölçülen bir gecikme değeridir.
Ping, bağlantı gei-cikmesimi ölçer yani bilgisayarınızdan veya telefonunuzdan bir sunucuya gönderilen veri paketlerinin gidiş-dönüş süresini gösterir.
Ağ sorunlarını teşhis eder, hedef bir id adresine veya web sitesine ulaşılıp ulaşılmadığını test eder.
Oyun ve uygulama performansını belirler, Online oyunlarda komutların tepki süresini, canlı yayınlarda ve görüntülü görüşmelerde donma veya gecikme olup olmadığını etkiler.


#Traceroute Nedir ve Ne İşe Yarar?

Traceroute ya da izleme yolu açık kaynak kodlu bir ağ analizi yazılımıdır.
Traceroute programı, TCP/IP ağlarında kaynak bilgisayardan hedef bilgisayara giden paketlerin hangi rotayı takip ettiğinin anlaşılması ve rotalardan geçerken meydana gelen gecikmelerin görülebilmesini sağlayan bir ağ aracıdır.
Trauceroute ağda sorun gidermek için kullanılır. Kaynak IP adresinden hedef IP adresine doğru gidilecek rota üzerinde yönlendirme problemlerinin tespit edilmesini sağlar. Ayrıca hedef IP adresine doğru giderken geçilen hostlara verilen IP adreslerini görmeye ve ağ altyapısı hakkında bilgi sahibi olmak için kullanılır.


#Nslookup Nedir ve Ne İşe Yarar?

DNS (Domain Name System) sorgulamak için kullanılan bir komut satırı aracıdır. 
Bir alan adının hangi IP adresine karşılık geldiğini öğrenmek, DNS sunucusunun verdiği yanıtları görmek ve DNS ile ilgili sorunları kontrol etmek için kullanılır.
DNS ile ilgili sorunları kontrol etmek ve bir alan adının hangi DNS sunucusu tarafından çözümlendiğini görmek için de kullanılabilir.
