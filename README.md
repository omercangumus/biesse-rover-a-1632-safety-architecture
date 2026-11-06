# Biesse Rover A 1632 Smart — İlk 7 Hafta Güvenlik İncelemesi

Bu depo, Biesse Rover A 1632 Smart 5 eksen CNC ahşap işleme merkezi için kamuya açık kaynaklara dayalı bir ön güvenlik ve siber güvenlik incelemesidir. PDF, Safety 4.0 Bootcamp föyünün yedi laboratuvarını kapakla birlikte 8 sayfada birleştirir. Föy düzeni ve renkler korunarak içerik Biesse makinesine uyarlanmıştır.

> **Ana teslim:** [İlk yedi hafta güvenlik incelemesi - PDF, 8 sayfa](Biesse-Rover-A-1632-Safety-Review.pdf). Markdown dosyaları düzenlenebilir çalışma kaynaklarıdır.

## Dosyalar

| Hafta | Çalışma | Çıktı | Düzenlenebilir not |
|---|---|---|---|
| 1 | Makine seçimi, kapsam ve kaynak yöntemi | İnceleme sınırı ve kanıt yaklaşımı | [Hafta 1](week-01-scope-and-method.md) |
| 2 | Varlıklar ve güven sınırları | Varlık listesi, bilinenler ve açık sorular | [Hafta 2](week-02-assets-and-boundaries.md) |
| 3 | Tehdit ve risk değerlendirmesi | L × S × E puanlı ön risk kaydı, EP04 | [Hafta 3](week-03-threat-risk-matrix.md) |
| 4 | Güvenli uzaktan erişim | Hedef mimari gereksinimleri, EP02 ve EP06 | [Hafta 4](week-04-secure-remote-access.md) |
| 5 | SBOM, CVE ve yama kararı | Senaryo bazlı uygulanabilirlik, test ve telafi edici önlem, EP09–EP11 | [Hafta 5](week-05-sbom-cve-patch.md) |
| 6 | CRA olay simülasyonu | Incident Workflow, EP13 | [Hafta 6](week-06-cra-incident-simulation.md) |
| 7 | Yapay zekâ güvenliği | AI Fail-Safe Decision, EP03 + EP15 | [Hafta 7](week-07-ai-safety-challenge.md) |

## Ayrı hafta PDF'leri

| Hafta | İndirme |
|---|---|
| 5 | [Week-05-SBOM-CVE-Patch.pdf](Week-05-SBOM-CVE-Patch.pdf?raw=true) |
| 6 | [Week-06-CRA-Incident-Simulation.pdf](Week-06-CRA-Incident-Simulation.pdf?raw=true) |
| 7 | [Week-07-AI-Safety-Challenge.pdf](Week-07-AI-Safety-Challenge.pdf?raw=true) |

## Önemli kapsam notları

- İnceleme yalnızca herkese açık kaynaklara dayanır. Biesse, Biesse Turkey veya AİMSAD/SAMİB üyelerinden bilgi istenmemiştir.
- Erişilebilen kullanım kılavuzu, Temmuz 2016 tarihli revizyon 0 kopyasıdır. Bu kopya makine ailesinin bazı koruma işlevlerini anlatır; belirli bir kurulumun seri numarasını, opsiyonlarını veya güncel durumunu kanıtlamaz.
- Kılavuzda koruyucu çit, kapı kilidi, temas matı, acil durdurma ve basınçlı hava kesme vanası anlatılır. Ağ topolojisi, uzaktan servis yolu, kullanıcı hesapları, güvenlik PLC’si modeli veya PL/SIL seviyesi kamuya açık kılavuzdan doğrulanamamıştır.
- 5. hafta tablosundaki Component X, sürüm 2.4, `CVE-XXXX-XXXX`, CVSS 9.8 ve yama bilgisi yalnızca eğitim senaryosudur. Rover A 1632 Smart'ta bu yazılımın veya zafiyetin bulunduğu iddia edilmez.
- 6. haftadaki servis hesabı olayı ve 7. haftadaki kamera/YZ kalite kontrol akışı eğitim senaryolarıdır; Biesse'de yaşanmış olay veya mevcut ürün özelliği olarak sunulmaz. CRA kapsamında üretici yükümlülüğü ile tesisin kendi olay müdahalesi ayrı değerlendirilir.
- Dosyalardaki risk puanları, makine üzerinde ölçüm veya saha incelemesi sonucu değildir. Belirsiz konular “varsayım” veya “doğrulanamadı” olarak işaretlenmiştir.
- Kılavuz, makineyle birlikte bir EC Declaration of Conformity (EC Uygunluk Beyanı) verildiğini belirtir. Erişilebilir kopyada bu makineye seri numarasıyla eşleşen imzalı beyan bulunmadığından, belirli bir makinenin güncel uygunluğu hakkında sonuç çıkarılmamıştır. “CE sertifikası” ifadesi yerine belgenin kendi adı olan Uygunluk Beyanı kullanılmalıdır.
- Biesse’nin Türkiye’de AİMSAD üye dizininde yer alması şirket seçiminin bağlamıdır; staj olanağı veya belirli bir açık pozisyon hakkında kanıt değildir.

## Kaynaklar

Kaynak adları, bağlantılar ve hangi iddiaları destekledikleri [sources.md](sources.md) dosyasındadır.
