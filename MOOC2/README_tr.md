<p align="right">
  <a href="README.md">[EN]</a>
  <a href="README_es.md">[ES]</a>
  <a href="README_pt.md">[PT]</a>
  <a href="README_tr.md">[TR]</a>
  <a href="README_sv.md">[SV]</a>
</p>

# Yayılım/Uygulama   Kılavuzu 
İkinci bölüm JuezLTI ın kurulumuna ve eğitim kurumlarının LMS (Learning Management System)- Eğitim Yönetim Sistemlerine entegrasyonuna odaklanacaktır. Konsorsiyum projenin yönetimi sırasında kullanımı için ücretsiz bir platform (JuezLTI merkezi) sunacak olmakla beraber, JuezLTI, onu tam anlamıyla öğrenmek ve kullanmak isteyen kurumların sunucularında kuruluma izin verecek şekilde tasarlanmıştır.

Bu görev, eğitim araçlarının entegrasyonunda uzman olmaları ve Docker Kapsayıcılarının (containers) geliştirilmesi görevini üstlenmelerinden dolayı aslen Edf [EdF](http://www.edf.global/) tarafından yürütülecektir

Bu Docker kapsayıcıları sayesinde JuezLTI, basit ve modüler bir kuruluma sahip olacak ve her kurumun bulut bilişim sağlayıcıları aracılığıyla sunucularına kurulacak modülleri (programlama, veritabanları, işaretleme dilleri) veya bulutta dağıtılmış kurumlarını kolayca yapılandırılmasına izin verecektir.

Bunların hepsi aşağıdaki bölümler altında ikinci bölümde tanımlanacaktır:
- Kurum içinde JuezLTI kurulumu
- Bulutta JuezLTI dağıtımı
- JuezLTI Yapılandırılması
- JuezLTI ve LMS arasında iletişim
- Alıştırma havuzlarının entegrasyonu 

# Gelişim Kılavuzu
JuezLTI herhangi bir kurum veya geliştiricinin, aracın işlevlerini kurumun özelliklerine uyarlayarak genişletilmesine olanak tanıyan bir Apache 2.0 lisansı ile piyasaya sunulacaktır.Programlama işlevini kolaylaştırmak için özel bir kılavuza ihtiyaç duyulmaktadır.

Bu kılavuz esas olarak INESC TEC [INESC TEC] (http://www.inesctec.pt/) tarafından geliştirilecek ve aşağıdaki bölümlerden oluşacaktır:
 - [LTI standartı](Development/LTI/README.md)
- [JuezLTI mimarisi](Development/Architecture/README.md)
- TSUGI ile modül geliştirme
- [Internal API](Development/API/README.md)
- JuezLTI kullanıcı gelişimi
- JuezLTI ile alıştırmaların geliştirilmesi
