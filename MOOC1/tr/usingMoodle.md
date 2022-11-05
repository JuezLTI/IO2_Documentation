# Moodle da JuezLTI kullanımı

![Juez in LMS](../docs/img/gettingCredentials/juezLTI_UsingCredentialsInLMS.png)

Moodle 2.2. den sonraki sürümlerde **Dış araç**, kullanıcıların LTI uyumlu öğrenme kaynakları ve diğer sitelerindeki etkinliklerle etkileşim kurmasını sağlar. Yani, Moodle dan JuezLTI kullanmanın doğru yolu 
**Dış araç etkinlikleri** dir.

Moodle resmi sitesinde [Dış araç](https://docs.moodle.org/400/en/External_tool) kullanımının bir özeti vardır.

Moodle sitesindeki ayrıcalıklarınıza bağlı olarak, LTI aracını (tool) etkinlik düzeyinde veya site yönetimi düzeyinde konfigüre edebileceksiniz. 


## Etkinlik Seviyesi

 **Dış araç etkinliği** seçtiğinizde![](../docs/img/gettingCredentials/externalTool2.png) ve ![](../docs/img/gettingCredentials/externalTool.png) Formu doldurmalısınız.
 
- **etkinlik ismi** -  başlık ekle, gerekliyse bir tanım , seçiminize bağlı görünüm seçiminiz.

- **Preconfigured tool** - Moodle araç sağlayıcı ile bu şekilde iletişim kurar. Eğer emin değilseniz varsayılan (default) olarak bırakın. Yöneticiniz bir aracı site genelinde kullanıma sunmuşsa, aracı buradan seçebileceksiniz: ![Preconfiguredtool.png](https://docs.moodle.org/400/en/images_en/7/7c/Preconfiguredtool.png)


- **Tool URL** - Siteye bağlanmak için kullanılan URL budur. Eğer moodle siteniz  [SSL](https://en.wikipedia.org/wiki/Transport_Layer_Security) (is on [HTTPS](https://docs.moodle.org/400/en/HTTPS)) kullanıyorsa [SSL](https://en.wikipedia.org/wiki/Transport_Layer_Security) kullanan bir araç kullanabileceksiniz. URL nin [HTTPS](https://docs.moodle.org/400/en/HTTPS) sahip olduğundan emin olun, aksi taktirde boş bir sayfa görüntüleyebilirsiniz.

    JuezLTI beta sürümünde URL şöyle doldurulmalıdır. [https://beta.juezlti.eu/tsugi/mod/codetest/](https://beta.juezlti.eu/tsugi/mod/codetest/). _Finali unutmayın /_.

- **Container başlat**- dış araç bu şekilde görüntülenecektir.
    Şüpheniz varsa – Default -   default (varsayılan) olarak bırakın
    - Embed (göm) – dış araç Moodle kurs sayfasına bloklar ve gezinme çubuğu ile gömülecektir.
    - Embed (bloklar olmadan göm) – dış araç Moodle kurs sayfasına bloklar olmadan gömülür.
    - Yeni pencere – Dış araç yeni bir pencerede açılacak. (Dış araçla yeni bir pencere veya sekme açılır ve kurs sayfasını içeren eski tarayıcı sayfa değişmeyecektir.) 


_”Daha fazla göster” tıklanarak aşağıdaki ayarlamalar yapılabilir: - **Etkinlik tanımı** - burada basit bir açıklama girin
- **Kurs sayfasında tanımı göster** - etkinlik ismiyle beraber açıklamanın gösterilmesini 
- **Başlangıçta etkinlik ismini göster** - öğrenci bağlantıyı tıkladığından bunun görünmesini sağlayın.
 - **Başlangıçta etkinlik tanımını göster** - öğrenci bağlantıyı tıkladığında bunun görünmesini sağlayın.
 - **Güvenli araç URL si** - Moodle [SSL](https://en.wikipedia.org/wiki/Transport_Layer_Security) kullandığında, araç URL sini geçersiz kılar.(Eğer siteniz [HTTPS](https://docs.moodle.org/400/en/HTTPS) in the wwwroot)kullanacak şekilde yapılandırılmışsa.
- **<u>kullanıcı anahtarı</u>** -   [**anahtar** JuezLTI tarafından verilen](gettingCredentials.md).anahtarı kullanmanız gereken yer burasıdır.
- **<u>paylaşılan parola</u>** - buraya **parola** yazılacak.
- **Özel parametreler** - burayı çoğunlukla boş bırakacaksınız. Kullanabileceğiniz spesifik bir kaynağı görüntüleyebilmeniz amacıyla araç sağlayıcı tarafından verilmiştir. 
- **Icon URL** - URL sini buraya girerek varsayılan dış araç simgesinden farklı bir simge görüntüleyebilirsiniz.
 - **Güvenli Icon URL** - Eğer öğrencileriniz güvenli bir şekilde buraya  [SSL](https://en.wikipedia.org/wiki/Transport_Layer_Security)yoluyla erişiyorsa, buraya farklı bir simge URL si girin.

## Gizlilik

- **Başlatıcının ismini araçla paylaşın** - Öğrencinin adının örnekte olduğu gibi bağlı olunan sitede görüntüleneceği anlamına gelir
 [örnek ](https://docs.moodle.org/400/en/images_en/1/13/demoexternaltool.png)
- **Başlatıcının e-postasını araçla paylaşın** - öğrencinin e-postasının örnekte olduğu gibi bağlı olunan sitede görüntüleneceği anlamına gelir. [örnek](https://docs.moodle.org/400/en/images_en/2/27/externaltoolfrontpage.png)
- **Araçtan seviyeleri Kabul et** - bu işaretlenirse, bağlantı sitesi seviyeleri Moodle ın (gradebook) seviye kayırlarına geri gönderir. Bununla ilgili daha fazla bilfi için [Using External tool](https://docs.moodle.org/400/en/Using_External_tool) 


## Site Yönetim Ayarları

### Site genelinde bir araç ekleme
Bir yönetici; _Site yönetimi> Eklentiler > Etkinlik modülleri > Dış araç > Araçları yönet_  şeklinde manuel olarak yapılandırabilir, böylece site içinde kullanılabilir.

![Dış Araç Ekleme ](https://docs.moodle.org/400/en/images_en/thumb/e/e2/moodle310_external_tool_registration.png/450px-moodle310_external_tool_registration.png)

Bir araç, yönetici tarafından, bir eğitmenin onu bir kursa ekleyebilmesi için etkinlik seçicide (dış araç etkinliğine ilaveten) görüntülenecek şekilde ya-konfigüre edilebilir. Açıklaması varsa etkinlik seçicide görünecektir. 


### Daha fazla detay görüntüleme

 _'Araçları Yönet'_ sayfasında _'Önceden yapılandırılmış araçları yönet'_ I kullanarak önceden konfigüre edilmiş araçları tabular formatta görebilirsiniz.
 Dış araç eklemek, bekleyenleri ve reddedilenleri görmek için tablar mevcuttur:
![Y:eni bir dış araç kurulumu ](https://docs.moodle.org/400/en/images_en/thumb/4/43/LTItype.png/450px-LTItype.png)

Araç kayıtlarını tabular formatta görmek veya sınırlı güçte dış araç eklemek için  _'Dış araç kayıtlarını yönet'_ i ziyaret edin.

Sınırlı güce sahip bir araç ekleme. 
1. Yeni dış araç kaydını yapılandır' a tıklayın.

![Registering an external tool](https://docs.moodle.org/400/en/images_en/thumb/d/d9/LTIreg.png/450px-LTIreg.png)

2. Kurulum sayfasında detayları yapılandırın :

![Registration settings page](https://docs.moodle.org/400/en/images_en/thumb/8/8f/LTIregdetails1.png/450px-LTIregdetails1.png)

_'Üyeler'_, dış aracın, belirli  bağlamda, belirlirole sahip kullanıcıların  bir listesini talep etmesine izin verir, örneğin kursa kayıtlı olanların listesi gibi.

 3. Kaydolmak için kutucuğu işaretleyin: 

![Activating](https://docs.moodle.org/400/en/images_en/thumb/3/3a/ticktoreg.png/450px-ticktoreg.png)

4. Başardınız mesajı aldıktan sonra işlemi tamamlayınıza tıklayın : 

![Kayıtı tamamlama](https://docs.moodle.org/400/en/images_en/thumb/0/05/reqmet.png/300px-reqmet.png)

5. Bütün istenenler tamamlandıktan sonra otomatik olarak kayıt olacaksınız.

 6. Şimdi _Site yönetimi > Eklentiler> Etkinlik modülleri> Dış araç > Dış araç türlerini yönet_  sırasını izle ve 'beklemede sekmesi' tıkla.

7. Etkinleştirmek için onay kutusunu tikle: 

![Beklemede sekmesinden etkinleştirme](https://docs.moodle.org/400/en/images_en/thumb/6/68/pendingactivate.png/450px-pendingactivate.png)

Yukarıdaki adımları görmek için dış araç kaydı ekran görüntülerine bakın.[Dış araç kaydı](http://www.spvsoftwareproducts.com/temp/lti2-moodle/) 
