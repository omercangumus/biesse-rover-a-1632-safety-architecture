# Biesse Rover A 1632 Smart — İlk 4 Hafta Güvenlik İncelemesi

Bu depo, Biesse Rover A 1632 Smart 5 eksen CNC ahşap işleme merkezi için kamuya açık kaynaklara dayalı bir ön güvenlik ve siber güvenlik incelemesidir. Kullanıcı tarafından paylaşılan çalışma kâğıdındaki Lab 3 risk matrisi ve Lab 4 uzaktan erişim yapısı korunmuştur.

## Dosyalar

| Hafta | Çalışma | Çıktı |
|---|---|---|
| 1 | Makine seçimi, kapsam ve kaynak yöntemi | İnceleme sınırı ve kanıt yaklaşımı |
| 2 | Varlıklar ve güven sınırları | Varlık listesi, bilinenler ve açık sorular |
| 3 | Tehdit ve risk değerlendirmesi | L × S × E puanlı ön risk kaydı, EP04 |
| 4 | Güvenli uzaktan erişim | Hedef mimari gereksinimleri, EP02 ve EP06 |

## Önemli kapsam notları

- İnceleme yalnızca herkese açık kaynaklara dayanır. Biesse, Biesse Turkey veya AİMSAD üyelerinden bilgi istenmemiştir.
- Erişilebilen kullanım kılavuzu, Temmuz 2016 tarihli revizyon 0 kopyasıdır. Bu kopya makine ailesinin bazı koruma işlevlerini anlatır; belirli bir kurulumun seri numarasını, opsiyonlarını veya güncel durumunu kanıtlamaz.
- Kılavuzda koruyucu çit, kapı kilidi, temas matı, acil durdurma ve basınçlı hava kesme vanası anlatılır. Ağ topolojisi, uzaktan servis yolu, kullanıcı hesapları, güvenlik PLC’si modeli veya PL/SIL seviyesi kamuya açık kılavuzdan doğrulanamamıştır.
- Dosyalardaki risk puanları, makine üzerinde ölçüm veya saha incelemesi sonucu değildir. Belirsiz konular “varsayım” veya “doğrulanamadı” olarak işaretlenmiştir.
- Kılavuz, makineyle birlikte bir EC Declaration of Conformity (EC Uygunluk Beyanı) verildiğini belirtir. Erişilebilir kopyada bu makineye seri numarasıyla eşleşen imzalı beyan bulunmadığından, belirli bir makinenin güncel uygunluğu hakkında sonuç çıkarılmamıştır. “CE sertifikası” ifadesi yerine belgenin kendi adı olan Uygunluk Beyanı kullanılmalıdır.
- Biesse’nin Türkiye’de AİMSAD üye dizininde yer alması şirket seçiminin bağlamıdır; staj olanağı veya belirli bir açık pozisyon hakkında kanıt değildir.

## Kaynaklar

Kaynak adları, bağlantılar ve hangi iddiaları destekledikleri [sources.md](sources.md) dosyasındadır.

