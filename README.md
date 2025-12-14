# Hydrofor-Control-Panel-SELV-Based-Safety-Design
This project documents a simple hydrofor (booster pump) control panel designed to prevent dry running when the water level in the storage tank drops below a critical threshold. The system was intentionally designed using SELV (Safety Extra-Low Voltage) principles to reduce electrical shock risk in wet environments.

# Hidrofor Kontrol Panosu – SELV Tabanlı Güvenli Tasarım

## Genel Bakış

Bu proje, su deposundaki seviye kritik değerin altına düştüğünde hidroforun kuru çalışmasını önlemek amacıyla hazırlanmış basit bir kontrol panosunu dokümante eder. Sistem, özellikle ıslak ve nemli ortamlarda elektrik çarpması riskini azaltmak için **SELV (Safety Extra-Low Voltage / Güvenli Ekstra Düşük Gerilim)** prensiplerine göre tasarlanmıştır.

Bu depodaki ana odak yalnızca sistemin çalışması değil, **gerçekçi hata senaryoları altında elektriksel güvenliğin nasıl artırılabileceğidir**.

---

## Projenin Amacı

* Hidroforun susuz kaldığında çalışmasını engellemek
* Su seviyesine bağlı olarak pompa enerjisini otomatik kesmek
* Kullanıcıyı pano üzerindeki basit göstergelerle bilgilendirmek
* Bunu yaparken **endüstriyel olmayan, erişilebilir malzemelerle** yüksek güvenlik seviyesi elde etmek

---

## Sistem Tanımı

* Su deposuna yerleştirilen bir şamandıra anahtarı seviye bilgisini sağlar
* Seviye düştüğünde kontrol devresi pompayı devre dışı bırakır
* **Kontrol devresi 12V DC** ile çalışır
* **Güç devresi (220V AC)** kontrol devresinden elektriksel olarak izoledir

---

## Bu Uygulamada Elektrik Güvenliği Neden Kritik?

Su deposu ve hidrofor ortamları doğası gereği **ıslak veya nemlidir**. Bu koşullarda:

* İnsan derisinin elektriksel direnci ciddi şekilde düşer
* Temas alanı büyür
* Elektrik akımının vücut içinden geçmesi kolaylaşır

Alternatif akım (AC) altında kas tetanisi oluşabilir ve kişi iletkeni istemsiz şekilde bırakamayabilir. Bu durum, ıslak ortamlarda elektrik çarpmasının çok daha tehlikeli olmasına neden olur.

---

## SELV (Safety Extra-Low Voltage) Yaklaşımı

Bu projede **IEC 60364-4-41** standardında tanımlanan SELV yaklaşımı esas alınmıştır.

### SELV Nedir?

* Gerilim **50V AC RMS** veya **120V DC (dalgalanmasız)** değerlerini aşmaz
* Yüksek gerilimli devrelerden **galvanik izolasyon** sağlanır
* Normal çalışma ve tekil hata durumlarında elektrik çarpması riski sınırlıdır

### Neden 12V DC Seçildi?

* SELV sınırlarının çok altında bir gerilim seviyesi
* Kolay temin edilebilir bileşenlerle uygulanabilir
* Basit kontrol mantıkları için yeterlidir
* İzolasyon zayıflasa veya su teması olsa bile risk ciddi ölçüde azalır

Tasarımda, **hataların kaçınılmaz olduğu** varsayılmış ve risk gerilim seviyesini düşürerek kaynağında azaltılmıştır.

---

## Su, Deri Direnci ve Elektrik Çarpması

Elektrik çarpmasının şiddetini belirleyen temel parametre gerilim değil, **vücuttan geçen akımdır**. Bu akımı belirleyen en kritik faktör ise insan vücudunun elektriksel direncidir.

İnsan vücudunda en büyük direnç, iç organlar değil **deri tabakasıdır**. Kuru ve sağlam deri yüksek direnç gösterirken, suyla temas bu direnci ciddi biçimde düşürür.

### Kuru ve Islak Deri Direnci

Yaklaşık değerlerle:

* **Kuru deri:** 50–100 kΩ
* **Nemli deri:** 5–10 kΩ
* **Islak deri / suya temas:** 1–2 kΩ (bazı durumlarda daha düşük)

Bu düşüş, aynı gerilim altında vücuttan geçen akımın katlanarak artmasına neden olur.

### Su Neden Riski Artırır?

* Su iyon içerir ve iletkendir (özellikle musluk ve depo suyu)
* Temas alanını büyütür, noktasal teması yaygın temasa dönüştürür
* Deri üzerindeki koruyucu tabakayı devre dışı bırakır
* Akımın derin dokulara ulaşmasını kolaylaştırır

Bu nedenle su, elektriği "nötralize eden" değil, **insan vücudu açısından riski büyüten** bir ortamdır.

---

## Gerilim ve Akım Karşılaştırması (Basitleştirilmiş)

Islak insan vücudunda direnç yaklaşık **1–2 kΩ** seviyesine kadar düşebilir.

| Senaryo      | Gerilim | Tahmini Akım |
| ------------ | ------- | ------------ |
| Şebeke AC    | 220V    | ~110–220 mA  |
| SELV Kontrol | 12V     | ~6–12 mA     |

**IEC 60479-1** standardına göre kalp üzerinden geçen yaklaşık **50 mA ve üzeri AC akımlar** ventriküler fibrilasyona yol açabilir ve ölümcül olabilir. SELV kontrol devresi bu seviyelerin oldukça altındadır.

---

## Tasarım Felsefesi: Fail-Safe Yaklaşım

Bu proje şunları varsaymaz:

* Endüstriyel sertifikalı muhafazalar
* IP68 sınıfı profesyonel sensörler
* Çok katmanlı endüstriyel koruma sistemleri

Bunun yerine **fail-safe (hata durumunda güvenli)** tasarım yaklaşımı benimsenmiştir:

* Hatalar mümkündür
* Hata oluştuğunda sonuç tehlikeli olmamalıdır
* Güvenlik, ideal koşullara değil tasarım kararlarına dayanmalıdır

SELV kullanımı, anormal koşullarda dahi riskin sınırlı kalmasını sağlar.

---

## Kapsam ve Sınırlamalar

* Ev tipi ve küçük ölçekli hidrofor sistemleri için tasarlanmıştır
* Sertifikalı endüstriyel panoların yerine geçmez
* Güç devresinde uygun topraklama ve kaçak akım koruması gereklidir

---

## Referanslar

* IEC 60364-4-41 – Elektrik çarpmasına karşı koruma
* IEC 60479-1 – Elektrik akımının insan vücudu üzerindeki etkileri

---

## Not

Bu depo, belirli bir uygulamayı eleştirmek için değil; **güvenli tasarım yaklaşımını** örneklemek için hazırlanmıştır. Sınırlı imkânlarla dahi temel elektrik mühendisliği prensipleri uygulanarak anlamlı güvenlik kazanımları elde edilebileceğini göstermeyi amaçlar.

