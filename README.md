API E2E Automation: Booking Management
Bu çalışma, Restful-Booker API'si üzerinde kurgulanmış, uçtan uca (End-to-End) bir test otomasyon sürecini içerir. Projenin ana odağı, manuel müdahaleyi sıfıra indiren API Chaining ve Dinamik Değişken Yönetimi tekniklerini uygulamaktır.

Teknik Kapsam
Proje, bir rezervasyonun yaşam döngüsünü tam otomatize bir şekilde test eder:

Dinamik Yetkilendirme: POST /auth isteğiyle alınan token, environment değişkenine atanarak sonraki tüm isteklerde otomatik kullanılır.
Request Chaining: Yeni oluşturulan rezervasyonun bookingid değeri yanıt içerisinden (response body) çekilir ve GET, PUT, DELETE isteklerine dinamik olarak aktarılır.
Validasyonlar: JavaScript tabanlı scriptler ile durum kodları (200, 201), yanıt süreleri ve veri doğruluğu (payload integrity) her adımda kontrol edilir.

Kullanılan Araçlar
Platform: Postman (v10.x)

Betik Dili: JavaScript (Tests & Pre-request Scripts)
Ortam Yönetimi: Postman Environment Variables

Çalıştırma Talimatı
Testleri yerel ortamınızda koşturmak için:
Depoda bulunan .postman_collection.json ve .postman_environment.json dosyalarını indirin.
Postman uygulamasında her iki dosyayı da Import edin.
Sağ üst köşedeki ortam menüsünden Otel_Rezervasyon_Test (veya ilgili environment) seçimini yapın.
Koleksiyonu Runner ile başlatarak tüm adımların başarı durumunu gözlemleyin.
