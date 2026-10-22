# Hafta 1 — Makine seçimi, kapsam ve yöntem

## Amaç

Biesse Rover A 1632 Smart 5 eksen CNC ahşap işleme merkezinin kamuya açık belgelerine dayanarak güvenlik ve siber güvenlik incelemesinin sınırını belirlemek. Bu çalışma, üreticiyle görüşme veya belirli bir makinenin sahada incelenmesi değildir.

## Makine tanımı

- Üretici: Biesse
- Proje için seçilen makine: Rover A 1632 Smart, 5 eksen CNC ahşap işleme merkezi
- İncelenen temel kaynak: Biesse imzalı Rover A 1632 Smart NC processing centre User Manual, kod 5801A0572, revizyon 0, Temmuz 2016 tarihli kamuya açık kopya
- Sürüm sınırı: Kılavuz, aile/model hakkında bilgi verir. Belirli bir makinenin seri numarası, üretim yılı, sipariş seçenekleri ve kurulu yazılımı bilinmiyor.

“5 eksen” proje kapsamında seçilen konfigürasyondur. Her kurulumda aynı mil kafası veya opsiyon bulunduğu bu açık kaynakla kanıtlanmış sayılmaz.

## İnceleme kapsamı

### Dahil

- Makine operatörü ve bakım personelinin makine çevresindeki işleri
- Ahşap veya kılavuzda belirtilen ahşap türevi malzemenin yüklenmesi, işlenmesi ve boşaltılması
- NC kontrolü, iş programları ve makine hareketleriyle ilgili olası dijital riskler
- Kılavuzda anlatılan fiziksel koruyucular ve durdurma işlevleri
- Olası uzaktan destek için hedef güvenlik gereksinimleri
- EC Uygunluk Beyanı gibi uygunluk kanıtlarının kamuya açık kopyada ne ölçüde incelenebildiği

### Hariç

- Fabrikanın gerçek kurumsal/OT ağı ve makineye bağlı diğer sistemler
- Belirli bir kurulumun gerçek IP adresleri, hesapları, portları, uzaktan erişim yazılımı veya servis tüneli
- Kaynak koda, konfigürasyona, loglara veya üretim ağına erişim
- Belirli seri numaralı makinenin CE uygunluğu, saha doğrulaması veya mevzuat uygunluk kararı
- Üreticiye ya da üye firmalara soru gönderme

## Kanıt etiketleri

| Etiket | Anlamı |
|---|---|
| Belgede doğrulandı | Kamuya açık kılavuzda veya dizinde açıkça yazan bilgi |
| Analiz | Kaynaklardan hareketle yapılan güvenlik yorumu |
| Varsayım | Risk senaryosu kurmak için kullanılan, gerçek kurulumda doğrulanmamış kabul |
| Öneri | Hedef güvenli çalışma için önerilen gereksinim; mevcut Biesse tasarımının tarifi değildir |
| Açık soru | Kamuya açık kaynakların yanıtlamadığı nokta |

## Yöntem

1. Makineyi ve kaynak sınırını tanımla.
2. Fiziksel, dijital ve güvenlikle ilgili varlıkları çıkar.
3. Tehdit senaryolarını Lab 3’teki L × S × E matrisiyle önceliklendir.
4. Lab 4’te uzaktan erişim için hedef gereksinimleri yaz ve emniyet işlevlerinin bağımsızlığını değerlendir.
5. Her bulguyu kaynağa bağla; bilinmeyen kurulumu gerçekmiş gibi anlatma.

## Hafta 1 teslimi

- Makine ve inceleme sınırı yazıldı.
- Kaynak ve kanıt etiketleri belirlendi.
- Hafta 2 varlık ve sınır analizine geçiş hazırlandı.

