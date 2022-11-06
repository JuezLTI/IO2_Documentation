<p align="right">
  <a href="README.md">[EN]</a>
  <a href="README_es.md">[ES]</a>
  <a href="README_pt.md">[PT]</a>
  <a href="README_tr.md">[TR]</a>
  <a href="README_sv.md">[SV]</a>
</p>

# Birlikte Çalışabilirlik

JuezLTI LMS – Learning Management System ( Eğitim Yönetim Sistemi) ne entegrasyon için Learning Tools Interoperability (Öğrenim Araçları Birlikte Çalışabilirliği)standartının 1.0 sürümünü kullanır. Bu birlikte çalışılabilirlik standartı Global Learning Consortium\cite (lti 2010) tarafından tasarlanmış ve Moodle, Canvas veya Sakai gibi önde gelen LMS uygulamaları tarafından da desteklenmektedir.

LTI ile bir Hizmet Odaklı Tasarım (SOA ) kullanılarak LMS işlevselliğini genişletmek için bir dizi eğitim servisi kullanılabilir. LMS, öğretmenlerin öğrenme deneyimini geliştirmek amacıyla, farklı kaynakları seçebileceği bir Pazar yeri haline gelir. 

JuezLTI, LTI uygulamalarının geliştirilmesini ve dağıtımını basitleştiren bir çerçeve olan TSUGI yi temel alır. TSUGI nin ilk uygulaması Pyhton eğitimi için bağımsız bir MOOC - py4e.com idi. 
Yazarlarından biri olan Dr. Charles Severance, Sakai, açık kaynaklı LMS kurucusudur ve halen IMS için çalışmaktadır.
LTI sadece kod testleri için değil, aynı zamanda LMS tarafından doğrudan desteklenmeyen karmaşık değerlenedirmeler sağlamak için de 2010 dan beri yaygın olarak kullanılmaktadır. Bunlardan biri de yüksek kalitede dijital hareketsiz görüntüler oluşturmada kullanılan Dig4E dir. 

JuezLTI I kullanmak için öğretmenin projenin internet sitesinden anahtar/parola ikilisini talep etmesi gerekmektedir. 
Öğretmen bu kimlik bilgileri ve sağlanan URL ile LMS de dış etkinlik oluşturur. 
Öğrenciler ise LMS tarafından sağlanan bilgiler kullanılarak doğrudan JuezLTI da tanımlanır. 
Bir öğrenci veya öğretmen aktiviteyi açtığında, LMS kullanıcıyı tanımlamak ve uygun arayüzü görüntülemek için LTI (_framework_TSUGI aracılığıyla) kullanarak JuezLTI ile iletişim kurar.
Ardından LMS, ilgili etkinliği tanımlayan <code>resource_link_id</code> özelliğinin gönderiri. Bu şekilde aynı anahtar kullanılarak farklı etkinlikler eklenebiliir. Son olaarak JuezLTI bir LTI hizmeti kullanarak çözülmüş alıştırmaların derece LMS ye geri bildirir. 

Kısacası JuezLTI ve LMS arasında çift yönlü iletişim vardır. JuezLTI öğrencilerin bilgilerini ve sonuçlarını saklar ve alınan notları LMS ye geri gönderir. 
