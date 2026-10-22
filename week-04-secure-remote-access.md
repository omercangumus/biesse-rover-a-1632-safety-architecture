# Hafta 4 — Güvenli uzaktan erişim

Bu çalışma, paylaşılan PDF’deki Lab 4 yaklaşımını Biesse Rover A 1632 Smart için bir hedef mimari gereksinim setine çevirir. Kılavuzdan mevcut bir Biesse uzaktan erişim mimarisi çıkarılamamıştır. Aşağıdaki maddeler mevcut ürün tasarımının tarifi değil, uzaktan servis gerekiyorsa uygulanması önerilen kurallardır.

## Güvenlik amacı

Yetkili servis işini mümkün kılarken internetten veya kurumsal ağdan NC kontrolüne doğrudan erişimi önlemek; uzaktan erişim kesildiğinde veya kötüye kullanıldığında koruyucu kapı, temas matı ve acil durdurma işlevlerinin güvenli çalışmasını sürdürmek.

## Hedef erişim akışı

| Adım | Gereksinim |
|---|---|
| 1. Onay | Servis ihtiyacı, iş emri, kullanıcı ve süre işletme tarafından önceden onaylanır. |
| 2. Kimlik | VPN ve MFA kullanılır; her servis kullanıcısına ayrı adlandırılmış hesap verilir. Ortak/varsayılan hesap kullanılmaz. |
| 3. Geçiş | Oturum doğrudan internete açık NC kontrolüne gitmez; OT DMZ’deki kontrollü jump host üzerinden geçer. |
| 4. Yetki | Hesap yalnızca onaylı makineye ve gereken işleme erişir. Oturum süreli açılır ve iş bitince kapatılır. |
| 5. Kayıt | Onaylayan, kullanıcı, başlangıç/bitiş zamanı, hedef ve yapılan değişiklikler kayda alınır. |
| 6. Değişiklik kontrolü | NC programı veya parametre değişiklikleri yedeklenir, yetkili kişi tarafından incelenir ve yerel güvenli doğrulamadan sonra üretime alınır. |
| 7. Kapatma | Servis oturumu sonlandırılır, geçici yetki kaldırılır ve iş emriyle kayıtlar eşleştirilir. |

## Emniyet işlevlerinin bağımsızlığı

- Uzaktan oturum; koruyucu çit/kapı, temas matı veya acil durdurmayı devre dışı bırakamamalı ya da köprüleyememelidir.
- Emniyet işlevlerinin çalışması, VPN, jump host, kurumsal ağ veya internet bağlantısına bağlı olmamalıdır.
- Uzaktan bağlantının kesilmesi emniyet sisteminin güvenli davranışını bozmamalıdır.
- Koruyucu durdurmadan sonra reset ile üretim programını yeniden başlatma ayrı adımlar olarak kalmalıdır. Kılavuz, durdurma/reset ile programın yeniden başlatılmasını ayrı anlatır.
- Emniyet ayarlarının değişmesi gerekiyorsa uzaktan oturum üzerinden doğrudan değişiklik yapılmamalı; makine sahibi işletmenin kontrollü bakım ve doğrulama süreci uygulanmalıdır.

## Güvenlik gereksinimleri

| ID | Gereksinim | Doğrulama kanıtı |
|---|---|---|
| RA-01 | Uzaktan erişim varsayılan olarak kapalı olmalı; yalnızca onaylı iş emri ve belirli zaman aralığında açılmalı. | İş emri ve bağlantı kayıtları |
| RA-02 | VPN + MFA ve kullanıcı başına ayrı hesap kullanılmalı. | Erişim politikası ve hesap listesi |
| RA-03 | NC kontrolüne doğrudan internet erişimi olmamalı; kontrollü OT DMZ/jump host kullanılmalı. | Güncel, yetkili ağ şeması ve kural incelemesi |
| RA-04 | Her kullanıcı asgari yetkiyle çalışmalı; ortak/varsayılan hesaplar kaldırılmalı veya kapatılmalı. | Hesap/rol dökümü |
| RA-05 | Oturum zamanı, kullanıcı, hedef, onay ve yapılan değişiklikler kayıt altına alınmalı. | Zaman damgalı oturum ve değişiklik kayıtları |
| RA-06 | Program/parametre değişiklikleri yedeklenmeli ve yerel güvenli doğrulamadan geçmeli. | Değişiklik kaydı, yedek ve doğrulama formu |
| RA-07 | Uzaktan bağlantı, makinenin emniyet işlevlerine müdahale veya bunları atlatma yolu vermemeli. | Yetkili fonksiyon testi ve mimari inceleme |
| RA-08 | Oturum bitince bağlantı ve geçici yetkiler kapatılmalı; kayıtlar saklanmalı. | Oturum kapanış kaydı |

## Analiz sorusu: Saldırgan uzaktan erişimi ele geçirirse emniyet işlevi etkilenir mi?

Mevcut kurulum için kamuya açık kaynaklardan yanıt verilemez; uzaktan erişim yolu ve emniyet mimarisi açıklanmamıştır. Hedef tasarımda cevap “hayır” olmalıdır: saldırganın uzaktan oturum yetkisi, koruyucuların veya acil durdurmanın işlevini değiştirememelidir. Bu iddia yalnızca mimari ve yetkili testlerle doğrulanabilir; bu masa başı çalışmada test yapılmamıştır.

## Hafta 4 teslimi

- Hedef uzaktan erişim gereksinimleri yazıldı.
- Emniyet işlevlerinin uzaktan erişimden bağımsız kalması şartı tanımlandı.
- Çıktı: EP02 — Secure Architecture ve EP06 — Remote Access Controls.

