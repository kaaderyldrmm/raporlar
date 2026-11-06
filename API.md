# API MANTIĞI (REST & JSON TEMELLERİ)

## API Nedir ve Neden Var?

API (Application Programming Interface), Türkçesiyle Uygulama Programlama Arayüzü, farklı yazılım uygulamalarının birbiriyle iletişim kurmasını sağlayan bir arayüzdür. Bir yazılımın başka bir yazılımdan veri almasına, veri göndermesine veya belirli işlemleri gerçekleştirmesine olanak tanır. API, iki sistem arasında bir iletişim köprüsü görevi görerek uygulamaların birbirleriyle uyumlu şekilde çalışmasını sağlar.

API'lerin temel amacı, farklı yazılım sistemleri arasında veri alışverişini kolaylaştırmak ve sistemlerin birlikte çalışabilmesini sağlamaktır. Günümüzde birçok uygulama, ihtiyaç duyduğu verileri veya hizmetleri başka sistemlerden API aracılığıyla alır. Örneğin bir hava durumu uygulaması, hava durumu bilgilerini kendi bünyesinde oluşturmak yerine başka bir servisin API'sini kullanarak sıcaklık, nem ve rüzgâr bilgilerini alabilir. Benzer şekilde alışveriş siteleri ödeme işlemlerinde bankaların veya ödeme kuruluşlarının API'lerinden yararlanabilir. Bu sayede her yazılımın bütün özellikleri sıfırdan geliştirmesine gerek kalmaz, zaman ve kaynak tasarrufu sağlanır.

API'nin çalışma mantığı istemci (Client), istek (Request), sunucu (Server) ve yanıt (Response) kavramlarına dayanır. İstemci, bilgi almak veya bir işlem gerçekleştirmek amacıyla API'ye istek gönderir. API bu isteği ilgili sunucuya iletir. Sunucu isteği değerlendirerek gerekli işlemi gerçekleştirir ve sonucu API aracılığıyla istemciye gönderir. İstemci de gelen yanıtı işleyerek kullanıcıya sunar. Bu iletişim süreci, uygulamaların arka planda birbirleriyle veri alışverişi yapmasını sağlar.

API'ler aracılığıyla gerçekleştirilen veri alışverişinde JSON (JavaScript Object Notation) ve XML (Extensible Markup Language) gibi veri formatları kullanılabilir. JSON, verilerin anahtar-değer çiftleri şeklinde düzenlendiği, okunması ve işlenmesi kolay bir veri formatıdır. XML ise verileri etiketler aracılığıyla yapılandıran bir işaretleme dilidir. Bu formatlar, farklı programlama dilleri ve platformlar arasında veri aktarımını kolaylaştırır.

API'ler çalışma ve tasarım yaklaşımlarına göre farklı türlere ayrılır. REST API, HTTP protokolünü kullanarak istemci ve sunucu arasında veri alışverişi sağlayan, günümüzde yaygın olarak kullanılan bir yaklaşımdır. SOAP API, XML tabanlı ve belirli iletişim standartlarına sahip bir web servis protokolüdür. GraphQL API, istemcilerin ihtiyaç duydukları verileri belirterek daha esnek sorgular oluşturmasına olanak tanır. Web API ise web üzerinden farklı uygulamaların iletişim kurmasını sağlayan API'ler için kullanılan genel bir ifadedir.

Özellikle REST API kullanımında GET, POST, PUT, PATCH ve DELETE gibi HTTP metotlarından yararlanılır. GET metodu sunucudan veri almak, POST metodu yeni veri oluşturmak, PUT metodu mevcut veriyi güncellemek, PATCH metodu verinin belirli alanlarını değiştirmek ve DELETE metodu veriyi silmek amacıyla kullanılır. Örneğin bir e-ticaret sisteminde ürünleri listelemek için GET, yeni bir ürün eklemek için POST, ürün bilgilerini güncellemek için PUT ve ürünü silmek için DELETE isteği gönderilebilir.

API iletişiminde önemli kavramlardan biri de Endpoint olarak adlandırılan erişim adresidir. Endpoint, API içerisinde belirli bir kaynağa veya işleme ulaşmak için kullanılan adrestir. Bir diğer önemli kavram olan HTTP Status Code ise gönderilen isteğin sonucunu belirtir. Örneğin 200 kodu isteğin başarılı olduğunu, 404 kodu istenen kaynağın bulunamadığını, 500 kodu ise sunucu tarafında bir hata meydana geldiğini ifade eder.

API güvenliği de yazılım sistemleri açısından önemli bir konudur. Authentication (Kimlik Doğrulama), sisteme erişmek isteyen kullanıcının kimliğinin doğrulanmasını ifade eder. Authorization (Yetkilendirme) ise doğrulanan kullanıcının hangi kaynaklara erişebileceğini ve hangi işlemleri gerçekleştirebileceğini belirler. Bu mekanizmalar sayesinde yetkisiz erişimler sınırlandırılır ve sistemlerin güvenliği artırılır.

API kullanmanın en önemli avantajlarından biri farklı yazılım sistemlerinin birbirleriyle entegre çalışabilmesidir. Bunun yanında veri paylaşımını kolaylaştırması, geliştirme sürecinde zaman kazandırması, mevcut hizmetlerin tekrar kullanılmasına olanak tanıması ve web, mobil ve masaüstü uygulamalarının ortak sistemlerle iletişim kurabilmesini sağlaması da önemli avantajları arasındadır.

Sonuç olarak API, günümüzde dijital sistemlerin ve yazılım uygulamalarının birbirleriyle iletişim kurmasını sağlayan temel teknolojilerden biridir. Bankacılık, e-ticaret, sosyal medya, sağlık, ulaşım ve hava durumu gibi birçok alanda kullanılmaktadır. Farklı sistemler arasında güvenli, düzenli ve hızlı veri alışverişi sağlayarak modern yazılım ekosisteminin gelişmesine katkıda bulunur.


## JSON Yapısı

JSON (JavaScript Object Notation), verilerin düzenli ve anlaşılır bir biçimde saklanmasını ve sistemler arasında aktarılmasını sağlayan bir veri formatıdır. Genellikle anahtar-değer (key-value) yapısını kullanır. JSON içerisinde metin, sayı, mantıksal değer, dizi ve nesne gibi veri türleri bulunabilir.


Örneğin bir kullanıcıya ait bilgiler şu şekilde gösterilebilir:

     {

     "id": 1,

     "name": "Ahmet",

     "age": 25,

     "isActive": true
     
     }

Bu yapıda id, name, age ve isActive anahtar; karşılarında bulunan değerler ise ilgili bilgilerdir. JSON, farklı yazılım sistemlerinin ortak bir veri formatı üzerinden iletişim kurmasını kolaylaştırır.




## Basit Bir Endpoint Nasıl Tasarlanır?

Endpoint, bir API içerisinde belirli bir kaynağa erişmek veya işlem gerçekleştirmek için kullanılan URL adresidir. Endpoint tasarlanırken öncelikle hangi kaynağa erişileceği belirlenir. Örneğin bir kullanıcı yönetim sistemi geliştirildiğinde kullanıcılarla ilgili işlemler için /api/users adresi kullanılabilir. Bu adres üzerinden GET metodu ile kullanıcılar listelenebilir, POST metodu ile yeni kullanıcı oluşturulabilir. Belirli bir kullanıcının bilgilerine erişmek veya bu bilgileri güncellemek için /api/users/1 adresi kullanılabilir. DELETE metodu ile de aynı adres üzerinden ilgili kullanıcı silinebilir. Endpoint tasarımında adreslerin anlaşılır, tutarlı ve kaynak odaklı olması önemlidir.

