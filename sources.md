# Kaynaklar ve kanıt sınırları

Bu projede yalnızca kamuya açık kaynaklar kullanılmıştır. AİMSAD/SAMİB üyeleriyle iletişime geçilmemiştir.

## 1. Paylaşılan çalışma kâğıdı

- [Kullanıcı tarafından paylaşılan ChatGPT çalışması — Safety Architecture Doldurma](https://chatgpt.com/share/6ad4dff3-6fa0-83eb-a722-ef5db85b8f31)
- Bu çalışma, görülebilen örnek PDF’deki Lab 3 “Threat & Risk + Risk Matrix” ve Lab 4 “Secure Remote Access” yapısını referans alır.
- Şişeleme hattına özgü tehditler veya ekipmanlar bu projeye kopyalanmamıştır; puanlama iskeleti ve teslim türleri uyarlanmıştır.

## 2. Biesse Rover A 1632 Smart kullanım kılavuzu

- [Biesse Rover A 1632 Smart User Manual, kod 5801A0572, rev. 0 (Temmuz 2016) — kamuya açık kopya](https://www.scribd.com/document/1010221318/5801A0572-1034080)
- Kılavuz makineyi “Rover A 1632 Smart NC processing centre” olarak adlandırır; malzeme, çalışma/tehlike alanı, çit/kapı, temas matı, acil durdurma, hareketli bölüm koruması ve basınçlı hava kesme vanası hakkında bilgi verir.
- Kılavuz, EC Declaration of Conformity belgesinin makine ile verildiğini ve beyanda bulunması gereken bilgi alanlarını anlatır. Erişilebilir kopya belirli seri numaralı makineye ait imzalı beyanı sağlamaz.
- Bu kaynak eski tarihli bir kılavuz kopyasıdır; güncel ürün sürümünü veya belirli kurulumun bugün uygun olduğunu kanıtlamaz.

## 3. AİMSAD üye dizini

- [TWM / AİMSAD üye dizini](https://www.twm.com.tr/en/stores)
- Dizinde BIESSE TURKEY Mak. Tic. ve San. A.Ş. listelenir.
- Bu kayıt yalnızca firma/üyelik bağlamıdır; staj pozisyonu, işe alım olanağı veya belirli makine konfigürasyonu hakkında kanıt değildir.

## Kaynak kullanım notu

Kılavuzdaki bilgiler “belgede doğrulandı” olarak, kaynakta bulunmayan ağ ve kurulum bilgileri “açık soru” olarak işaretlenmiştir. Puanlar ve hedef gereksinimler teknik inceleme taslağıdır; saha testi veya uygunluk sertifikasyonu yerine geçmez.


## 4. Zafiyet, SBOM ve OT yama yönetimi

- [NIST SP 800-82 Rev. 3 — Guide to Operational Technology Security](https://csrc.nist.gov/pubs/sp/800/82/r3/final)
- OT varlıklarında yama yönetiminin belgeli olmasını; yamanın nasıl test edileceğinin, ne zaman uygulanacağının ve yama gecikirse hangi telafi edici önlemlerin kullanılacağının belirlenmesini önerir. OT yama dağıtımının planlı duruşta ve yetkin personelce yapılmasını belirtir.
- [CISA — Securing the Software Supply Chain: Recommended Practices for SBOM Consumption](https://www.cisa.gov/sites/default/files/2024-08/SECURING_THE_SOFTWARE_SUPPLY_CHAIN_RECOMMENDED_PRACTICES_FOR_SOFTWARE_BILL_OF_MATERIALS_CONSUMPTION-508.pdf)
- SBOM'ların bileşen görünürlüğü ve CVE/VEX ile zafiyet takibinde kullanımını açıklar. OT'de yama operasyonel etki yaratabiliyorsa ağ segmentasyonu, hizmeti devre dışı bırakma ve diğer risk azaltma seçeneklerini ele alır.
- [NIST National Vulnerability Database — Vulnerability Detail Pages](https://nvd.nist.gov/vuln/Vulnerability-Detail-Pages)
- CVE kayıtlarının ürün/sürüm eşlemesi ve CVSS'nin bir zafiyetin ciddiyetini gösteren ölçü olarak yorumlanması için kullanılır. CVSS puanı tek başına bu makinedeki gerçek riski veya uygulanabilirliği kanıtlamaz.

## 5. hafta senaryo notu

`CVE-XXXX-XXXX` kasıtlı bir yer tutucudur. Component X, 2.4 sürümü, Critical/CVSS 9.8 ve yama mevcut bilgileri yalnızca ders föyünün varsayımsal senaryosudur; Biesse Rover A 1632 Smart için gerçek SBOM, yazılım sürümü, CVE kaydı veya üretici yaması olarak gösterilmez. Makineye özgü uygulanabilirlik kamuya açık kılavuzdan belirlenememiştir.

## 5. CRA bildirim süreleri

- [(AB) 2024/2847 - Cyber Resilience Act](https://eur-lex.europa.eu/eli/reg/2024/2847/oj/eng), madde 14.
- 6. haftada aktif istismar edilen açıklık ile ürün güvenliğini etkileyen ciddi olay için iki ayrı son rapor süresi kullanılır.
- Kaynak, belirli Biesse makinesinin kapsamda olduğunu veya senaryodaki olayın yaşandığını kanıtlamaz.

## 6. Yapay zekâ risk yönetimi

- [NIST AI RMF 1.0 - NIST AI 100-1](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-1.pdf), özellikle MEASURE 2.4-2.6.
- 7. haftanın izleme, güvenilirlik ve güvenli başarısızlık yaklaşımına dayanak sağlar.
- Kamera/YZ akışı, HOLD ve insan onayı eğitim senaryosuna ait tasarım kararlarıdır. Kaynak Biesse'de belirli bir YZ özelliği bulunduğunu göstermez.
