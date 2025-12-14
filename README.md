# Hydrofor-Control-Panel-SELV-Based-Safety-Design
EU/This project documents a simple hydrofor (booster pump) control panel designed to prevent dry running when the water level in the storage tank drops below a critical threshold. The system was intentionally designed using SELV (Safety Extra-Low Voltage) principles to reduce electrical shock risk in wet environments.

TR/Bu proje, su deposundaki seviye kritik bir eşik değerin altına düştüğünde hidroforun (basınç artırıcı pompa) kuru çalışmasını önlemek amacıyla tasarlanmış basit bir kontrol panosunu dokümante etmektedir. Sistem, ıslak ortamlarda elektrik çarpması riskini azaltmak için bilinçli olarak SELV (Safety Extra-Low Voltage / Güvenli Ekstra Düşük Gerilim) prensiplerine göre tasarlanmıştır.

# Water Level Based Booster Pump Protection Panel  
# Su Seviyesine Bağlı Hidrofor Koruma Panosu

---

## General Overview  
## Genel Bakış

**EN**  
This project documents a simple control panel designed to prevent dry running of a booster pump when the water level in a storage tank drops below a critical threshold. The system is designed according to SELV (Safety Extra-Low Voltage) principles to reduce the risk of electric shock, particularly in wet and humid environments.

The main focus of this repository is not only system functionality, but also how electrical safety can be increased under realistic fault scenarios.

**TR**  
Bu proje, su deposundaki seviye kritik değerin altına düştüğünde hidroforun kuru çalışmasını önlemek amacıyla tasarlanmış basit bir kontrol panosunu dokümante eder. Sistem, özellikle ıslak ve nemli ortamlarda elektrik çarpması riskini azaltmak için SELV (Safety Extra-Low Voltage / Güvenli Ekstra Düşük Gerilim) prensiplerine göre tasarlanmıştır.

Bu deponun ana odağı yalnızca sistemin çalışması değil, gerçekçi hata senaryoları altında elektriksel güvenliğin nasıl artırılabileceğidir.

---

## Project Objectives  
## Projenin Amacı

**EN**
- Prevent the booster pump from operating without water  
- Automatically disconnect pump power based on water level  
- Provide basic user feedback through simple panel indicators  
- Achieve a high level of electrical safety using accessible, non-industrial components  

**TR**
- Hidroforun susuz kaldığında çalışmasını engellemek  
- Su seviyesine bağlı olarak pompa enerjisini otomatik olarak kesmek  
- Kullanıcıyı pano üzerindeki basit göstergelerle bilgilendirmek  
- Endüstriyel olmayan, erişilebilir malzemelerle yüksek güvenlik seviyesi elde etmek  

---

## System Description  
## Sistem Tanımı

**EN**
- A float switch installed in the water tank provides level information  
- When the water level drops, the control circuit disables the pump  
- The control circuit operates at 12V DC  
- The power circuit (220V AC) is electrically isolated from the control circuit  

**TR**
- Su deposuna yerleştirilen bir şamandıra anahtarı seviye bilgisini sağlar  
- Seviye düştüğünde kontrol devresi pompayı devre dışı bırakır  
- Kontrol devresi 12V DC ile çalışır  
- Güç devresi (220V AC), kontrol devresinden elektriksel olarak izoledir  

---

## Why Electrical Safety Is Critical in This Application  
## Bu Uygulamada Elektrik Güvenliği Neden Kritik?

**EN**  
Water tanks and booster pump installations are inherently wet or humid environments. Under these conditions:
- Human skin resistance decreases significantly  
- Contact area increases  
- Electrical current passes through the body more easily  

Under alternating current (AC), muscle tetany may occur, preventing a person from releasing a live conductor involuntarily. This makes electric shock significantly more dangerous in wet environments.

**TR**  
Su deposu ve hidrofor ortamları doğası gereği ıslak veya nemlidir. Bu koşullarda:
- İnsan derisinin elektriksel direnci ciddi şekilde düşer  
- Temas alanı büyür  
- Elektrik akımının vücut içinden geçmesi kolaylaşır  

Alternatif akım (AC) altında kas tetanisi oluşabilir ve kişi iletkeni istemsiz şekilde bırakamayabilir. Bu durum, ıslak ortamlarda elektrik çarpmasını çok daha tehlikeli hale getirir.

---

## SELV (Safety Extra-Low Voltage) Approach  
## SELV (Güvenli Ekstra Düşük Gerilim) Yaklaşımı

**EN**  
This project follows the SELV concept as defined in IEC 60364-4-41.

### What Is SELV?
- Voltage does not exceed 50V AC RMS or 120V DC (ripple-free)  
- Galvanic isolation from higher-voltage circuits is provided  
- Electric shock risk is limited under normal operation and single-fault conditions  

**TR**  
Bu projede IEC 60364-4-41 standardında tanımlanan SELV yaklaşımı esas alınmıştır.

### SELV Nedir?
- Gerilim 50V AC RMS veya 120V DC (dalgalanmasız) değerlerini aşmaz  
- Yüksek gerilimli devrelerden galvanik izolasyon sağlanır  
- Normal çalışma ve tekil hata durumlarında elektrik çarpması riski sınırlıdır  

---

## Why 12V DC Was Selected  
## Neden 12V DC Seçildi?

**EN**
- Far below SELV voltage limits  
- Easily implemented with commonly available components  
- Sufficient for basic control logic  
- Even in case of insulation failure or water contact, risk remains limited  

The design assumes that faults are inevitable and reduces risk at its source by lowering voltage levels.

**TR**
- SELV sınırlarının çok altında bir gerilim seviyesi  
- Kolay temin edilebilir bileşenlerle uygulanabilir  
- Basit kontrol mantıkları için yeterlidir  
- İzolasyon zayıflasa veya su teması olsa bile risk ciddi ölçüde azalır  

Tasarımda, hataların kaçınılmaz olduğu varsayılmış ve risk, gerilim seviyesini düşürerek kaynağında azaltılmıştır.

---

## Water, Skin Resistance, and Electric Shock  
## Su, Deri Direnci ve Elektrik Çarpması

**EN**  
The severity of electric shock is determined by the current flowing through the body, not the voltage itself. The most critical factor influencing this current is the electrical resistance of the human body.

The highest resistance is provided by the skin. While dry skin has high resistance, contact with water drastically reduces it.

**TR**  
Elektrik çarpmasının şiddetini belirleyen temel parametre gerilim değil, vücuttan geçen akımdır. Bu akımı belirleyen en kritik faktör ise insan vücudunun elektriksel direncidir.

İnsan vücudunda en büyük direnç, iç organlar değil deri tabakasıdır. Kuru ve sağlam deri yüksek direnç gösterirken, suyla temas bu direnci ciddi biçimde düşürür.

---

## Typical Skin Resistance Values  
## Kuru ve Islak Deri Direnci

**EN (Approximate values)**
- Dry skin: 50–100 kΩ  
- Moist skin: 5–10 kΩ  
- Wet skin / water contact: 1–2 kΩ  

**TR (Yaklaşık değerler)**
- Kuru deri: 50–100 kΩ  
- Nemli deri: 5–10 kΩ  
- Islak deri / suya temas: 1–2 kΩ  

---

## Voltage and Current Comparison (Simplified)  
## Gerilim ve Akım Karşılaştırması (Basitleştirilmiş)

**EN**
| Scenario | Voltage | Estimated Current |
|--------|--------|------------------|
| Mains AC | 220V | ~110–220 mA |
| SELV Control | 12V | ~6–12 mA |

**TR**
| Senaryo | Gerilim | Tahmini Akım |
|-------|--------|--------------|
| Şebeke AC | 220V | ~110–220 mA |
| SELV Kontrol | 12V | ~6–12 mA |

According to IEC 60479-1, AC currents above approximately 50 mA may be fatal.

---

## Design Philosophy: Fail-Safe Approach  
## Tasarım Felsefesi: Fail-Safe Yaklaşım

**EN**
- Faults are possible  
- Unsafe outcomes must be prevented  
- Safety must rely on design decisions, not ideal conditions  

**TR**
- Hatalar mümkündür  
- Hata oluştuğunda sonuç tehlikeli olmamalıdır  
- Güvenlik, ideal koşullara değil tasarım kararlarına dayanmalıdır  

---

## Scope and Limitations  
## Kapsam ve Sınırlamalar

**EN**
- Designed for residential and small-scale systems  
- Does not replace certified industrial panels  
- Proper grounding and RCD protection are required  

**TR**
- Ev tipi ve küçük ölçekli sistemler için tasarlanmıştır  
- Sertifikalı endüstriyel panoların yerine geçmez  
- Uygun topraklama ve kaçak akım koruması gereklidir  

---

## References  
## Referanslar

- IEC 60364-4-41 – Protection against electric shock  
- IEC 60479-1 – Effects of current on the human body  

---

## Note  
## Not

**EN**  
This repository demonstrates a safety-oriented design mindset using fundamental electrical engineering principles.

**TR**  
Bu depo, temel elektrik mühendisliği prensipleriyle güvenli tasarım yaklaşımını örneklemeyi amaçlar.

