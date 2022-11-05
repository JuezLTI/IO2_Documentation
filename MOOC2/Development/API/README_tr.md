<p align="right">
  <a href="README.md">[EN]</a>
  <a href="README_es.md">[ES]</a>
  <a href="README_pt.md">[PT]</a>
  <a href="README_tr.md">[TR]</a>
  <a href="README_sv.md">[SV]</a>
</p>


# Internal/ Dahili API

 [Architecture](../Architecture/README.md) açıklandığı gibi JuezLTI farklı modüllerden oluşturulmuştur. Yapısında aşağıdaki dört tür modülü barındırır. 
 - **Öğrenci Görünümü** - Öğrencilerin alıştırmaları çözmeye çalıştığı alan; 
 - **Değerlendirici** Önceki modüledeki çalışmaların gönderildiği alan;
 - **Geribildirim Yöneticisi** - pÖğrenci için anlamlı mesajlar üretmek için, doğrulayıcılar tarafından oluşturulan raporları oluşturur; 
- **Merkezi havuz/depo** - Alıştırmaları ve diğer konfigürasyonları içerir. 

 Bu katılımcıların çoğu tekil olmakla beraber **Değerlendirici**bir kaç alanı bir modül olduğu belirtilmelidir.Programlama dili, biçimlendirme dili ve veritabanı için ayrı birer değerlendirici vardır.  Proje sırasında geliştirilen doğrulayıcılara ek olarak, herhangi bir kurumun kendi doğrulayıcılarını uygulayabilmesi için genişletilmesine çalışılmıştır. 

Aşağıdaki diyagram bu modüller arasındaki iletişimi göstermektedir. **Öğrenci Görünümü** kullanılarak, öğrenci denediği çözümü uygun **Değerlendirici** ye gönderir. Bu modül,**merkezi depo/havuz** dan alınan bir alıştırmayı kullanarak bu girişimi değerlendirir ve bir **rapor** üretir. Doğrulayıcı ise **Öğrenci Görünümü** kullanıcına sunulmak üzere  bir **geribildirim** raporunu**Geribildirim Yöneticisi** ne gönderir.

![Modüller arası İletişim](generic-evaluator-architecture.svg)

Modüller arası iletişim dahili [API formalized in Swagger](https://github.com/JuezLTI/APIs/blob/d981488ba77f238f2aaeb6f862ab1c2a0e8252d9/v2/API.yaml#L16) tarafından düzenlenir. Alıştırmalar ve raporlar dışında yapılandırılmamış olan bir çok veri sırasıyla şunları kullanır:

- [`YAPExIL`](YAPExIL/README.md) -  a programming exercise format;
- [`PEARL`](PEARL/README.md) a common format for evaluation reports.
