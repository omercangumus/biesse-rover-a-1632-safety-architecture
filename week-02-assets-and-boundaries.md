# Hafta 2 — Varlıklar ve güven sınırları

Bu kayıt, üretici kılavuzunun kamuya açık kopyasında tarif edilen unsurları proje için modellenen varlıklardan ayırır. Belirli bir kurulumun gerçek ağ yapısı bilinmiyor.

## Varlık listesi

| ID | Varlık | Durum | Güvenlik / güvenlik-kritik önem |
|---|---|---|---|
| A01 | NC kontrolü ve operatör paneli | Makine ailesinin kontrolü kılavuzda anlatılır; kesin donanım ve sürüm bilinmiyor | İş programı ve makine durumunun kontrol edildiği nokta |
| A02 | NC iş programları ve işleme parametreleri | Analiz varlığı; dosya biçimi ve saklama yeri bilinmiyor | Yetkisiz değişiklik yanlış takım yolu veya işleme hareketi doğurabilir |
| A03 | X/Y/Z hareketleri, işleme kafası ve takım | Makinenin işleme işlevi kılavuzda anlatılır; kurulu opsiyonlar değişebilir | Hareketli parçalar operatör için fiziksel tehlike oluşturabilir |
| A04 | İşleme alanı ve çalışma masası | Kılavuzda çalışma ve tehlike alanları tarif edilir | Malzeme ve iş parçası güvenli tutulmalı; erişim kontrolü gerekir |
| A05 | Koruyucu çit, kapılar ve kilitleme anahtarı | Kılavuzda belgelenmiştir | Tehlikeli alana girişi sınırlar; kapı açılınca makineyi durdurma işlevi anlatılır |
| A06 | Temas matı | Kılavuzda belgelenmiştir | Tehlikeli alana giriş algılandığında makineyi durdurma işlevi anlatılır |
| A07 | Acil durdurma ve durdurma/reset kontrolleri | Kılavuzda belgelenmiştir | Acil durumda makineyi durdurur; reset ve programa yeniden başlama ayrı ele alınır |
| A08 | Hareketli bölüm koruması ve esnek perdeler | Kılavuzda belgelenmiştir | Takım/parça teması ve talaş fırlaması gibi tehlikeleri azaltmaya yardımcı olur |
| A09 | Basınçlı hava kesme vanası | Kılavuzda belgelenmiştir | Bakımda enerjiyi ayırma içindir; bazı parçalarda artık basınç veya yerçekimi riski kalabilir |
| A10 | Operatör ve bakım personeli | Analiz varlığı | Makineyle fiziksel olarak etkileşir; yetki ve çalışma yöntemleri önemlidir |
| A11 | Uzak servis oturumu / servis bilgisayarı | Açık soru; mevcut olduğu doğrulanmadı | Varsa makine kontrolüne erişim yolu olabilir; bu dosyada yalnızca hedef mimari olarak ele alınır |

## Güven ve fiziksel sınırlar

| Sınır | Kamuya açık kaynakta bilinen | Bilinmeyen |
|---|---|---|
| Tehlike alanı | Kılavuz, hareketli parçaların kapladığı alanı tehlike alanı olarak tanımlar | Belirli kurulumdaki yerleşim ve koruyucu çevre ölçüleri |
| Operatör erişimi | Çit/kapı ve temas matının koruyucu işlevleri anlatılır | Sensör modeli, bakım geçmişi ve kurulu devre ayrıntıları |
| Kontrol ile proses | NC kontrolü ile hareketli işleme prosesi makine işlevinin parçasıdır | Gerçek kontrol mimarisi, sürücü/topoloji, kullanıcı rolleri |
| Makine ile dış ağ | Kılavuzda gerçek ağ bağlantısı veya uzaktan erişim topolojisi doğrulanmadı | Makinenin internete, ofis ağına veya servis ağına bağlı olup olmadığı |
| Emniyet işlevleri | Acil durdurma, kapı/çit, temas matı gibi işlevler açıklanır | Güvenlik PLC’si modeli ve PL/SIL derecesi |

## Hedef zon modeli — öneri, mevcut kurulum tarifi değil

Uzaktan bakım gerçekten gerekiyorsa, proje için önerilen sınırlar şöyledir:

1. İnternet/kurumsal ağ, makine kontrolüne doğrudan erişmemeli.
2. Onaylı bağlantı, OT DMZ’deki kontrollü bir geçiş sistemine ulaşmalı.
3. Servis kullanıcısı, süreli ve kayıtlı oturumla yalnızca gereken makine/servis yetkisini almalı.
4. NC kontrolü ile emniyet işlevleri arasındaki sınır korunmalı; uzaktan erişim koruyucu kapı, mat veya acil durdurmayı devre dışı bırakamamalı.

## Kaynakta doğrulanamayan kritik bilgiler

- Belirli makinede Ethernet veya internet bağlantısı olup olmadığı
- Uzaktan servis yazılımı, VPN, hesap ve kimlik doğrulama yöntemi
- Emniyet devresinin bileşenleri ve PL/SIL sınıfı
- Makinenin güncel CE/EC Uygunluk Beyanı ve seri numarası eşleşmesi
- Makinenin mevcut bakım ve doğrulama kayıtları

## Hafta 2 teslimi

- Başlıca makine, insan, veri ve koruma varlıkları listelendi.
- Fiziksel ve siber güven sınırları ayrıldı.
- Doğrulanmamış kurulum bilgileri açık soru olarak kaydedildi.

