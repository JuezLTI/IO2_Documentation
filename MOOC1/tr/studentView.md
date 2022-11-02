# Öğrenci Görünümü

![Öğrenci Görünümü diyagramı](../docs/img/studentView/studentViewUsageDiagram.png)

Eğitmenler **harici tool etkinliği** oluşturduğunda ![](../docs/img/gettingCredentials/externalTool2.png) veya ![](../docs/img/gettingCredentials/externalTool.png), öğrenciler kendi kurs sayfalarında görebilirler:
 
![Harici Aktivite Seç](../docs/img/studentView/selectingExternalActivity.png)

Öğrencinin yapması gereken tek şey Harici Aktiviteye tıklamaktır, bu durmda _kolay alıştırma_ oluşur. 

Aşağıdaki görüntüye benzer bir öğrenci görünümü oluşur:

![Öğrenci form sayfası](../docs/img/studentView/studentViewFormPage.png)

Sayfanın üst kısmında aktiviteyi oluşturan alıştırmaların listesi gösterilir: 

![Öğrenci görünümü alıştırma listesi](../docs/img/studentView/studentViewListExercises.png)

Yukarıdaki örnek üç alıştırmadan oluşan bir aktivite örneğidir. Her birinde olası üç durum gösterilmiştir: 

- _turuncu_: Öğrenci alıştırmayı cevaplamadı.
- _yeşil_: öğrenci alıştırmayı çözdü.
- _kırmızı_: öğrenci alıştırmaya yanlış cevap verdi.

Öğrenci alıştırmalar arasında gezinmek için alıştırma listesini kullanabilir ve üzerlerine tıklayabilir. 

Alıştırma listesinden sonra, alıştırma başlığı ve komut bulunabilir.

![Öğrenci görünümü Başlık ve Komut](../docs/img/studentView/studentViewTitleStatement.png)

Ve test seti 

![Öğrenci Görünümü test seti](../docs/img/studentView/studentViewTests.png)

Bu testlerde öğrenci her bir girdiye karşılık gelen çıktıyı görebilir. Yukarıdaki örnekte kod ‘Charles’ ı alırsa, ‘merhaba Charles’ olarak dönmesi gerekir.

Öğrenci, çözümün hangi dilde kodlanacağını önceden seçerek çözümünü _kod Çözüm_ alanına kodlamalıdır:

![Öğrenci Görünümü Cevap ](../docs/img/studentView/studentViewAnswer.png)

Öğrenci sayfanın sonunda notunu ve cevabına verilen geribildirimi görecektir.

Aşağıda iki farklı kodun sonuçlarını görebilirsiniz: 

- Yanlış cevap:

```
import java.util.Scanner;

public class Main {

    public static void main(String[] args)
    {
        Scanner input = new Scanner (System.in);
        String name = input.next();
        System.out.print("Hello "+name+"!!");
    }
}
```
![Öğrenci görünümü yanlış cevap](../docs/img/studentView/studentViewWrongAnswer.png)

- Doğru cevap :

```
import java.util.Scanner;

public class Main {

    public static void main(String[] args)
    {
        Scanner input = new Scanner (System.in);
        String name = input.next();
        System.out.print("Hello "+name);
    }
}
```
![ÖğrencGörünümü doğru cevap](../docs/img/studentView/studentViewRightAnswer.png)

