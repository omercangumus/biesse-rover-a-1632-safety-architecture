# Hafta 7 - AI Safety Challenge

**Makine:** Biesse Rover A 1632 Smart  
**Tarih:** 06.11.2026  
**Çıktı:** AI Fail-Safe Decision - Evidence Pack EP03 + EP15  
**Teslim:** [Doldurulmuş PDF](Week-07-AI-Safety-Challenge.pdf)

## Senaryo ve kapsam

Kamera tabanlı bir kalite kontrol modeli kusurlu parçaya yanlışlıkla OK verebilir. Rover A 1632 Smart'ta bu YZ özelliği kamuya açık kaynakla doğrulanmamıştır. Aşağıdaki akış yalnızca eğitim senaryosudur.

Kamera görüntüsü modele gider; OK/RED çıktısı yetkili insanın parça hakkındaki kararını destekler. YZ, kapı kilidini, acil durdurmayı veya güvenli duruşu yönetmez. Bu emniyet işlevleri bağımsız, doğrulanmış korumalarla yürür.

## Üç başarısızlıkta karar

| Başarısızlık | Senaryodaki güvenli davranış |
|---|---|
| Model yanlış sınıflandırdı | Parçayı HOLD durumunda tut; ikinci kontrol/insan onayı olmadan serbest bırakma; kararı kaydet. YZ emniyet zincirine girmez. |
| Girdi manipüle edildi | Bütünlük, zaman veya görüntü kalitesi kontrolü başarısızsa sonucu reddet; parçayı HOLD et; yetkili manuel incelemeye yönlendir ve olayı kaydet. |
| Güven skoru düştü veya model yanıt vermedi | Temsilî test ve risk değerlendirmesiyle belirlenen eşiğin altında HOLD ve yetkili insan incelemesi uygula. YZ olmadan devam ancak önceden doğrulanmış alternatif yöntem varsa mümkündür. |

HOLD, parçanın kalite açısından serbest bırakılmasını bekletir; makinenin emniyet işlevinin yerine geçmez. Güven eşiği ve alternatif yöntem sahada doğrulanmış sayılmaz.

## Kaynak ve yorum sınırı

[NIST AI RMF 1.0](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-1.pdf), geçerlilik/güvenilirlik, güvenli başarısızlık ve izleme yaklaşımı için referanstır. HOLD ve insan incelemesi bu eğitim senaryosunun tasarım kararlarıdır; NIST'in belirli bir Biesse makinesi için verdiği talimatlar değildir.
