# Comments
## Yorum Makyaj Mıdır?
- Yorum satırları için en temel motivasyon kötü kodtur.
- Az yorum içeren temiz ve açıklayıcı kod çok yorum içeren karmaşık kodtan daha iyidir.
- Daha düzgün açıklayıcı yoruma harcıyacağın zamanı karmaşık kötü kodu temizlemeye ayır.
## Yorumların Sussun Kodun Açıklasın
- Çoğu durumda yorum yazmak istediğiniz şeyi sağlayan bir fonksiyon ve ismi yazılabilir.
## İyi Yorum
- İyi yorum, yazmamak için bir yol bulabildiğiniz yorumdur.
### Mazur Görülen Yorumlar
- Bazı kodun lisansı,yazarı gibi konularda kodun başına yorum eklenebilir.
- Yine de mümkünse bu yorumları kodun dışında bir dosyada(ReadMe) tutmak daha iyidir.
### Bilgilendirici Yorumlar
- Bazı durumlarda bilgilendirici yorumlar olabilir.
- Regex ifadelerin olduğu kodlarda beklentiyi açıklayıcı yorum yazılabilir.
```
// format matched kk:mm:ss EEE, MMM dd, yyyy
Pattern timeMatcher = Pattern.compile(
 "\\d*:\\d*:\\d* \\w*, \\w* \\d*, \\d*");
```
- Yine de bu tür regex ifadeler ayrı özel bir sınıfa taşınsaydı yoruma gerek kalmıyabilirdi.
### Niyet Beyan Eden Yorumlar
- Bazı yorumlar verilen kararın amacını açıklar.
### Açıklama
- Bazen belirsiz bir argümanı ve dönüş değerini açıklayıcı yorum yazmak kodu okunaklı kılar.
- Ama daha iyisi argümanın ve dönüş değerinin kendini açıklamasıdır.
- Yorum yazmadan önce daha iyi bir yol var mı diye düşün.
### Uyarıcı Yorumlar
- Bazen diğer programcıları belirli durumlar için uyarıcı yorumlar yazmak gerekebilir.
### TODO
- TODO yorumları belirli nedenlerle yapamadığı uygulamayı daha sonra yapmayı düşündüğünü gösterir.Bir hatırlatıcı gibi.
### Vurgu
- Bazı önemsiz gözüken ayrıntıları vurgulamak için yorumlar yazılabilir.
### Belge-Yorum
- Eğer herkese açık bir API yazıyorsan belge yorumları yapmalısın.
- Ama unutma belge yorumları bile karmaşık,anlamsız ve yanlış yönlendirici olabilir.O yüzden yukarıdaki sözleri yine de dikkate al.
## Kötü Yorum
- Çoğu yorum kötü yoruma girer.Kötü kodun mazaretleridirler.
### Mırıltı
- Sırf yapman gerektiğini düşündüğün için ve/veya süreç gerektiği için yorum yazmak bir hacktir.
- Yorumu okuduğumda anlamak için kodun başka parçalarına bakmam gerekiyorsa yorum işini yapamamış demektir.
### Gereksiz Yorum
- Kodundan daha bilgilendirici değilse;kodundan daha okunaklı değilse;kodunu niyetini daha iyi beyan etmiyorsa yorum gereksizdir.
### Yanlış Yönlendirme
- Yorumu yazanın tüm iyi niyetine rağmen doğru olmayan bir yorum yazılabilir ve bu yorum başka bir programcıyı debugging döngüsüne sokabilir.
### Zorunlu Yorumlar
- Her fonksiyonun bir belgesi(summary) olmalı, her değişkenin bir yorumu olmalı gibi saçma kurallar genel kafa karışıklığına ve düzensizliğe neden olur.
### Haberci Yorumlar
- Source kontrol sistemlerinin olmadığı zamanlar kodta yapılan değişikler yorum stırı olarak yazılabilirdi ama artık gerek yok.
### Çöp Yorumlar
- Zaten açıkça belli olanı tekrar eden yorum çöptür.
### Çöpün Çöpü Yorum
- Bir belge yorumun(summary part) zaten açık olanı yazması çöpün çöpüdür.
### Yorum olarak Fonksiyon/Değişken
- Eğer yazdığın yorumu fonksiyon veya değişken olarak yazabiliyorsan yoruma gerek yok.
```
// does the module from the global list <mod> depend on the
// subsystem we are part of?
if (smodule.getDependSubsystems().contains(subSysMod.getSubSystem()))
```
Bunun yerine aşağıdakini yazabilirsin.
```
ArrayList moduleDependees = smodule.getDependSubsystems();
String ourSubSystem = subSysMod.getSubSystem();
if (moduleDependees.contains(ourSubSystem))
```
### Konum İşaretleyici
- Kullanılabileceği zamanlar vardır.Sıklıkla kullanmak kirliliğe neden olr.
- Nadir olsun ki dikkat çeksin.Sık kullanırsan önemini yitirir.
### Süslü Parantez Yorumları
- Uzun fonksiyonlar için süslü arantezlerin üstüne yanına yorum bırakmak anlamlı olsada küçük parçalara ayırmakta fonksiyonları dağınıklığa neden olur.
- Eğer süslü parantez yanına ötesine berisine yorum bırakma ihtiyacı hissediyorsan belkide fonksiyonu küçük parçalara ayırmanın vakti gelmiştir.
### 5N 1K
- Kodu kim yazdı,ne zaman yazdı neden yazdı gibi bilgilerini veren yorumlara gerek yok artık.Git var.Kullan Git gibi source control systemlerini.
### Yorum Satırına Alınmış Kod Parçaları
- Yorun satırına alınmış kod parçası gördüğümüzde silmek istemeyiz çünkü bir nedenle yorum satırına alındığını düşünürüz.Ve yıllarca o yorum satırına alınmış kod öyle orda kalır.
- Altmışlarda bu mantıklıydı ama artık source control sistemlerimiz var.Sil gitsin.
### Html
- Html yorumları gereksizdir.Bu Başka bir tooldan geliyorsa bu o toolun sorumluluğu.Bırakın süslü kodu kendinde kalsın.
### Yerel Bilgi
- Yoruma ihtiyaç duyduğun yorum açıkladığın kodun yakınında olsun.Uzağında olduğunda kod değiştiğinde yorum uzaktaki yerde kalabilir.Farkedilmeyebilir.
### Aşırı Bilgi
- Yorum içinde önceki tartışmalardan ve uzun tanımlardan uzak dur.
### Zayıf Bağlantı
- Yorum ile kod arasındaki bağlantı açık olmalı.Yorumun ne hakkında olduğunu anlamalıyım.Yorumun kodu açıklıyor olması gerekiyor bir de yorumu açıklamaya ihtiyaç olmamalı.
### Fonksiyon Başlıkları
- Kısa olan fonksiyonların yoruma ihtiyacı yoktur.Uygun fonksiyon ismi seç yeterli.
### Döküman Yorum
- Uzun olması daha iyi döküman oluşturulduğunu göstermez.
- Olabildiğince kısa tut.Açıklayıcı yorumun yorumu şeklinde bir uzunluğa gerek yok.