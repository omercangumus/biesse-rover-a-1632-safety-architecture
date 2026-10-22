# Hafta 3 — Tehdit ve risk matrisi

Bu çalışma, paylaşılan PDF’deki Lab 3 yaklaşımını kullanır. Puanlar sahada ölçülmüş olasılıklar değildir; kamuya açık bilgiyle hazırlanmış ilk sınıf değerlendirmesidir.

## Puanlama yöntemi

Her etken 1–3 arasında puanlanır:

- L — Olasılık: Senaryonun gerçekleşme olasılığı
- S — Şiddet: Gerçekleşirse doğabilecek sonucun ağırlığı
- E — Maruziyet: İnsanların veya varlıkların senaryoya ne ölçüde maruz kaldığı
- Toplam risk puanı = L × S × E

| Puan | Seviye |
|---:|---|
| 18–27 | Kritik |
| 9–17 | Yüksek |
| 4–8 | Orta |
| 1–3 | Düşük |

S = 3 olan senaryolar, toplam puan düşük çıksa bile ayrıca öncelikli incelenir. Derecelendirme gerçek ağ, çalışma sıklığı, iş parçası kütlesi, koruyucu testleri ve bakım kayıtları öğrenildiğinde yeniden yapılmalıdır.

## Ön risk kaydı

| ID | Tehdit senaryosu | L | S | E | Puan / seviye | Gerekçe ve kanıt | Önerilen azaltımlar |
|---|---|---:|---:|---:|---|---|---|
| R01 | Yetkisiz veya hatalı bir kişi NC programını/işleme parametresini değiştirir; hatalı takım yolu veya beklenmeyen işleme hareketi iş parçasını ya da takımı fırlatabilir ve operatörü yaralayabilir. | 2 | 3 | 2 | 12 / Yüksek | Bu dijital erişim yolu kurulumda doğrulanmamıştır; senaryo koşulludur. Kılavuz işleme sırasında hareketli parçalar ve tehlike alanı bulunduğunu belirtir. | Bireysel kullanıcı hesabı ve asgari yetki; değişiklik onayı; program yedeği ve geri yükleme; işe başlamadan önce güvenli kontrol/ilk parça doğrulaması; ağ erişimini sınırlandırma. |
| R02 | Bir kişi çalışma sırasında tehlike alanına girer; koruyucu kapı/çit veya temas matı etkisiz kalır ya da devre dışı bırakılmıştır. | 1 | 3 | 2 | 6 / Orta — S=3 nedeniyle öncelikli | Kılavuz çit/kapı ve temas matı durdurma işlevlerini belgeler. Belirli kurulumun test ve bakım kayıtları bilinmediği için puan geçicidir. | Koruyucuları günlük kullanımdan önce kontrol etme; arıza varsa çalışmayı durdurma; koruyucuyu devre dışı bırakmayı yasaklama; periyodik işlev testi ve kayıt. |
| R03 | Yükleme/boşaltma sırasında büyük veya ağır panel kayar ya da düşer; el/ayak ezilmesi veya çarpma yaralanması olur. | 2 | 2 | 2 | 8 / Orta | Kılavuz malzemenin elle veya uygun yardımcı cihazla yüklenip boşaltılabildiğini belirtir. Gerçek panel ölçüleri, ağırlığı ve kaldırma yardımcıları bilinmiyor. | İş parçasına uygun kaldırma/taşıma yardımcısı; yükün sabitlenmesi; el/ayakları sıkışma alanlarından uzak tutma; operatör eğitimi ve güvenli yükleme yöntemi. |

## Öncelik sırası

1. R01 — Yüksek; dijital erişim yolu doğrulanmalı ve iş programı değişikliği kontrol altına alınmalı.
2. R02 — Toplam puanı orta olsa da S=3; makinede koruyucu işlevlerin çalıştığı doğrulanmalı.
3. R03 — Orta; gerçek iş parçası boyutu/ağırlığı ve taşıma yöntemiyle yeniden puanlanmalı.

## Kalan belirsizlikler

- NC kontrolünde kullanıcı hesabı, parola politikası ve değişiklik kaydı var mı?
- Makineye uzaktan erişim veya taşınabilir ortamla program aktarımı yapılıyor mu?
- Koruyucu kapı ve temas matı hangi test sıklığında doğrulanıyor?
- Tipik iş parçası boyutu/ağırlığı ve kullanılan kaldırma ekipmanı nedir?

Bu sorular üreticiye yöneltilmemiştir. Gerçek saha değerlendirmesinde makine sahibi işletmenin yetkili kayıtlarıyla cevaplanmalıdır.

## Hafta 3 teslimi

- Ön Risk Kaydı hazırlandı.
- Risk puanlama anahtarı ve S=3 öncelik kuralı uygulandı.
- Çıktı: EP04 — Risk Assessment.

