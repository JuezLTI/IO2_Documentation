<p align="right">
  <a href="README.md">[EN]</a>
  <a href="README_es.md">[ES]</a>
  <a href="README_pt.md">[PT]</a>
  <a href="README_tr.md">[TR]</a>
  <a href="README_sv.md">[SV]</a>
</p>

# LTI Standartı

Information Management System IMS de, Learning Tool Interoperability-Öğrenme araçları birlikte çalışabilirliği, (LTI) spesifikasyonu; üçüncü taraf içeriği bir LMS veya platform içindeki kurslara entegre etmenin standart bir yolu şeklinde tanımlanabilir. LTI olmasaydı, LMS ve   içerik sağlayıcılar özel ayarlara dayalı çalışabilirdi, bu da birlikte çalışabilirlik ve ölçeklenebilirlik konusunda önyargılara sebep olurdu. Bu spesifikasyon, benzer applikasyonlarla güvenli veri alışverişi için çoklu servisleri desteklemek amacıyla, web uygulamalarını başlatmak için basit bir mekanizmadan geliştirilmiştir. 
LTI önce gelen tüm  LMS  satıcıları tarafından referans olarak gösterilen ve desteklenen bir standarttır bu nedenle de eğitimsel web uygulamalarının faydasını maksimize eder. 

Bugünlerde IMS konsorsiyumu 1.3 sürümünün benimsenmesini önermektedir. Özetle LTI 1.3 öğrencilerin kimliğini güvenli bir şekilde doğrulamak ve LMS ile dış öğrenme arası arasında güvenli veri aktarımı için OAuth2 ve JSON web tokenları (JWTs) imzalı mesajlar kullanır. 

Bu sürüm, LTI1.3 ün merkezinde herhangi bir aracın, herhangi bir LMS ile entegrasyonunu zenginleştirmek için yeni özellikler ekleyen ve bir hizmet paketi olarak tanımlanan LTI Advantage içerir. LTI Advantage ın üç özellik hizmeti şulardır; 

- İsimler ve Rol temin servisleri (NPRS) : Araca belli bir bağlam (örneğin kurs veya grup) için kullanıcı listelerine ve rollerine erişim izni verir.NPRS dış aracın, onu başlatan bağlamdan bir üye listesi istemesine izin verir. Araç üye listesini aldığında henüz aracı kurmamış/başlatmamış olsalar bile içerikte kayıtlı tüm öğrenci ve öğretmenleri okur.

 - Ödev ve Not Servisleri (AGS) ssignment and Grade Services (AGS): Öğretmenlerin üçüncü tarafa araçları ve LMS leri arasında notları sekronize etmelerine olanak tanır. Bu servis sayısal puanları ve öğretmen yorumlarını bir LMS not defterine dönüştürür. Örneğin bir öğretmen, bir öğrencinin ödeve ne zaman başladığını veya bitirip bitirmediğini görebilir. Öğretmen tarafından manuel bir input girilmesi gerekse bile, öğretmen not durumunu görebilir. 


 - Derin bağlantı (DL) : Bir LMS ye LTI bağlantıları eklemek için daha akıcı bir yaklaşım sunar. Derin bağlantı mesajları, dış öğrenme araçlarının LMS içinde iç araçlar gibi görünmesine izin verir. Derin bağlantı ile dış öğrenme araçları artık öğretmenlerin araç içindeki belirli bir içeriği veya etkinlikleri yapılandırmasına izin verir. LTI 1.1 de öğretmen sınıfın yalnızca belirli bir kaynağı kullanmasını istese bile, tüm araç içeriğinin gösterilmesi gerekiyordu. Derin bağlantı öğretmenlerin ihtiyaç duydukları içeriği seçmelerine ve bu içeriği kurslarında başlatmak için bağlantıyı paylaşmalarına olanak tanır. Örneğin, öğrenciler bir bağlantı seçtiğinde onları aracı başlatmaya ve ardından o bölüme gitmeye zorlamak yerine, öğretmenin bir e-kitaptan bir bölümüm configure etmesine izin verebilir. 

    
LTI 1.3 ü kullanmaya başlamak dikkatle alınması gereken bir karardır. Öğrencinin LMS den bir etkinlik başlattığı, bunu dış araçta çözdüğü ve ardından notun LMS not defterine geri bildirildiği çoğu durumda LTI 1.1 yeterlidir. Ancak yeni LTI 1.3 özellikleri konu ile alakalı alanlarda uygulanabilir. Örneğin skor tablolarının kullanımı dikkate alındığında provizyon hizmetlerinden elde edilen isimler ve roller , skor tablolarını ilk kez gönderilmeden önce öğrencilerin isimleriyle doldurmak için kullanılabilir; derin bağlantılar araç tarafından çalışma sırasında oluşturulan skor tablolarını LMS içine gömmek için kullanılabilir.  
