# Hydrofor-Control-Panel-SELV-Based-Safety-Design
EU/This project documents a simple hydrofor (booster pump) control panel designed to prevent dry running when the water level in the storage tank drops below a critical threshold. The system was intentionally designed using SELV (Safety Extra-Low Voltage) principles to reduce electrical shock risk in wet environments.

TR/Bu proje, su deposundaki seviye kritik bir eşik değerin altına düştüğünde hidroforun (basınç artırıcı pompa) kuru çalışmasını önlemek amacıyla tasarlanmış basit bir kontrol panosunu dokümante etmektedir. Sistem, ıslak ortamlarda elektrik çarpması riskini azaltmak için bilinçli olarak SELV (Safety Extra-Low Voltage / Güvenli Ekstra Düşük Gerilim) prensiplerine göre tasarlanmıştır.

# Su Seviyesine Bağlı Hidrofor Koruma Panosu  
# Water Level Based Booster Pump Protection Panel

---

## Genel Bakış / General Overview

**TR**  
Bu proje, su deposundaki seviye kritik değerin altına düştüğünde hidroforun kuru çalışmasını önlemek amacıyla tasarlanmış basit bir kontrol panosunu dokümante eder. Sistem, özellikle ıslak ve nemli ortamlarda elektrik çarpması riskini azaltmak için SELV (Safety Extra-Low Voltage / Güvenli Ekstra Düşük Gerilim) prensiplerine göre tasarlanmıştır.

Bu deponun ana odağı yalnızca sistemin çalışması değil, gerçekçi hata senaryoları altında elektriksel güvenliğin nasıl artırılabileceğidir.

**EN**  
This project documents a simple control panel designed to prevent dry running of a booster pump when the water level in a storage tank drops below a critical threshold. The system is designed according to SELV (Safety Extra-Low Voltage) principles to reduce the risk of electric shock, particularly in wet and humid environments.

The main focus of this repository is not only system functionality, but also how electrical safety can be increased under realistic fault scenarios.

---

## Projenin Amacı / Project Objectives

**TR**
- Hidroforun susuz kaldığında çalışmasını engellemek  
- Su seviyesine bağlı olarak pompa enerjisini otomatik kesmek  
- Kullanıcıyı pano üzerindeki basit göstergelerle bilgilendirmek  
- Endüstriyel olmayan, erişilebilir malzemelerle yüksek güvenlik seviyesi elde etmek  

**EN**
- Prevent the booster pump from operating without water  
- Automatically disconnect pump power based on water level  
- Provide basic user feedback through simple panel indicators  
- Achieve a high level of electrical safety using accessible, non-industrial components  

---

## Sistem Tanımı / System Description

**TR**
- Su deposuna yerleştirilen bir şamandıra anahtarı seviye bilgisini sağlar  
- Seviye düştüğünde kontrol devresi pompayı devre dışı bırakır  
- Kontrol devresi 12V DC ile çalışır  
- Güç devresi (220V AC), kontrol devresinden elektriksel olarak izoledir  

**EN**
- A float switch installed in the water tank provides level information  
- When the water level drops, the control circuit disables the pump  
- The control circuit operates at 12V DC  
- The power circuit (220V AC) is electrically isolated from the control circuit  

---

## Bu Uygulamada Elektrik Güvenliği Neden Kritik? / Why Electrical Safety Is Critical in This Application

**TR**  
Su deposu ve hidrofor ortamları doğası gereği ıslak veya nemlidir. Bu koşullarda:
- İnsan derisinin elektriksel direnci ciddi şekilde düşer  
- Temas alanı büyür  
- Elektrik akımının vücut içinden geçmesi kolaylaşır  

Alternatif akım (AC) altında kas tetanisi oluşabilir ve kişi iletkeni istemsiz şekilde bırakamayabilir. Bu durum, ıslak ortamlarda elektrik çarpmasını çok daha tehlikeli hale getirir.

**EN**  
Water tanks and booster pump installations are inherently wet or humid environments. Under these conditions:
- Human skin resistance decreases significantly  
- Contact area increases  
- Electrical current passes through the body more easily  

Under alternating current (AC), muscle tetany may occur, preventing a person from releasing a live conductor involuntarily. This makes electric shock significantly more dangerous in wet environments.

---

## SELV (Güvenli Ekstra Düşük Gerilim) Yaklaşımı / SELV (Safety Extra-Low Voltage) Approach

**TR**  
Bu projede IEC 60364-4-41 standardında tanımlanan SELV yaklaşımı esas alınmıştır.

**SELV Nedir?**
- Gerilim 50V AC RMS veya 120V DC (dalgalanmasız) değerlerini aşmaz  
- Yüksek gerilimli devrelerden galvanik izolasyon sağlanır  
- Normal çalışma ve tekil hata durumlarında elektrik çarpması riski sınırlıdır  

**EN**  
This project follows the SELV concept as defined in IEC 60364-4-41.

**What Is SELV?**
- Voltage does not exceed 50V AC RMS or 120V DC (ripple-free)  
- Galvanic isolation from higher-voltage circuits is provided  
- Electric shock risk is limited under normal operation and single-fault conditions  

---

## Neden 12V DC Seçildi? / Why 12V DC Was Selected

**TR**
- SELV sınırlarının çok altında bir gerilim seviyesi  
- Kolay temin edilebilir bileşenlerle uygulanabilir  
- Basit kontrol mantıkları için yeterlidir  
- İzolasyon zayıflasa veya su teması olsa bile risk ciddi ölçüde azalır  

Tasarımda, hataların kaçınılmaz olduğu varsayılmış ve risk, gerilim seviyesini düşürerek kaynağında azaltılmıştır.

**EN**
- Far below SELV voltage limits  
- Easily implemented with commonly available components  
- Sufficient for basic control logic  
- Even in case of insulation failure or water contact, risk remains limited  

The design assumes that faults are inevitable and reduces risk at its source by lowering voltage levels.

---

## Su, Deri Direnci ve Elektrik Çarpması / Water, Skin Resistance, and Electric Shock

**TR**  
Elektrik çarpmasının şiddetini belirleyen temel parametre gerilim değil, vücuttan geçen akımdır. Bu akımı belirleyen en kritik faktör ise insan vücudunun elektriksel direncidir.

**EN**  
The severity of electric shock is determined by the current flowing through the body, not the voltage itself. The most critical factor influencing this current is the electrical resistance of the human body.

---

## Kuru ve Islak Deri Direnci / Typical Skin Resistance Values

**TR (Yaklaşık değerler)**
- Kuru deri: 50–100 kΩ  
- Nemli deri: 5–10 kΩ  
- Islak deri / suya temas: 1–2 kΩ  

**EN (Approximate values)**
- Dry skin: 50–100 kΩ  
- Moist skin: 5–10 kΩ  
- Wet skin / water contact: 1–2 kΩ  

---

## Gerilim ve Akım Karşılaştırması (Basitleştirilmiş) / Voltage and Current Comparison (Simplified)

| Senaryo / Scenario | Gerilim / Voltage | Tahmini Akım / Estimated Current |
|-------------------|------------------|----------------------------------|
| Şebeke AC / Mains AC | 220V | ~110–220 mA |
| SELV Kontrol / SELV Control | 12V | ~6–12 mA |

**TR**

IEC 60479-1 standardına göre kalp üzerinden geçen yaklaşık 50 mA ve üzeri AC akımlar ölümcül olabilir.

**EN**

According to IEC 60479-1, alternating currents of approximately 50 mA and above passing through the heart may be fatal.

---

## Tasarım Felsefesi: Fail-Safe Yaklaşım / Design Philosophy: Fail-Safe Approach

**TR**
- Hatalar mümkündür  
- Hata oluştuğunda sonuç tehlikeli olmamalıdır  
- Güvenlik, ideal koşullara değil tasarım kararlarına dayanmalıdır  

**EN**
- Faults are possible  
- Unsafe outcomes must be prevented  
- Safety must rely on design decisions, not ideal conditions  

---

## Kapsam ve Sınırlamalar / Scope and Limitations

**TR**
- Ev tipi ve küçük ölçekli sistemler için tasarlanmıştır  
- Sertifikalı endüstriyel panoların yerine geçmez  
- Güç devresinde uygun topraklama ve kaçak akım koruması gereklidir  

**EN**
- Designed for residential and small-scale systems  
- Does not replace certified industrial panels  
- Proper grounding and RCD protection are required  

---

## Referanslar / References

**TR**
- IEC 60364-4-41 – Elektrik çarpmasına karşı koruma  
- IEC 60479-1 – Elektrik akımının insan vücudu üzerindeki etkileri  

**EN**
- IEC 60364-4-41 – Protection against electric shock  
- IEC 60479-1 – Effects of current on the human body  

---

## Not / Note

**TR**  
Bu depo, sınırlı imkânlarla dahi temel elektrik mühendisliği prensipleri kullanılarak anlamlı güvenlik kazanımları elde edilebileceğini göstermeyi amaçlar.

**EN**  
This repository demonstrates that meaningful safety improvements can be achieved using fundamental electrical engineering principles, even with limited resources.
