# Metodlar
## Küçük
- İlk kural : İnsan okuyacak bunu küçük metod yaz.
- Programdaki her fonksiyon olabildiğince kısa satırlı olmalı.Herbiri olabildiğince açık olmalı.Her biri başka bir hikaye anlatmalı.Ve her biri gelecek sezon ne geleceği konusunda bizi yönlendirmeli.
## Bloklar ve Girintiler
- if,else,while statementları bir satır uzunluğunda olmalı ve o satırda bir metodu çağırmalı.
- Bu ayrıca girintilerin az olmasını sağlayack çünkü içiçe girintiler okunaklığı azaltır.
## Bir Şey Yap
- Fonksiyonlar bir şey yapmalı.Onu iyi yapmalı ve sadece onu yapmalı.
- Bir fonksiyon yazmamızın amacı daha büyük bir kavramı parçalara ayırmaktır.
- Eğer bir fonksiyonun içinden başka isimle bir fonksiyon çıkartabiliyorsanız o fonksiyon birden fazla şey yapıyor demektir.
## Bir Metod Bir Soyutlama
- Method içindeki statementların soyutlama düzeyleri aynı seviyede olmalı.
## Yukarıdan Aşağıya
- Kodu yukarıdan aşağıya doğru okunacak şekilde düzenle ve soyutla.
- Yumurtaları kırmadan pişirme aşamasına geçemezsin.Kahvaltı yap fonksiyonun altında aynı soyutlama düzeyinde yumurtaları kır,pişir ve servis et fonksiyonları olmalı.Kahvaltı yap üst düzey soyutlama yumurtaları kır,pişir ve servis et fonksiyonları alt düzey bir soyutlamadır.
## Switch Statement
- Eğer bir kez kullanılıyorsa, polymorphic objenin yaratılmasında ve bir kalıtım ilişkisinin arkasına gizlenebildiğinde switch statementlar tolere edilebilir.(Abstract factory bunun için uygun bir pattern.)
## Tanımlayıcı İsimlendirme
- Fonksiyonun ne yaptığını iyi tanımlayan bir isim bul.
- Uzun isimlendirmelerden çekinme çünkü uzun ama tanımlayıcı isilendirme kısa ama enigmatic isimlendirmeden iyidir.
- İsimlendirmeye zaman ayırmaktan korkma.
- Tanımlayıcı bir isim seçme modülün ne yaptığını kafanda açıklar ve onu geliştirmeni kolaylaştırır.
- İsimlerin tutarlı olsun.Tutarlı isimlendirme akışı bir hikayeyeyi bölüm bölüm okumak gibidir.
## Metod Parametreleri
- İdeal parametre sayısı sıfır olmalıdır.
- Üç parametre ender bir durumdur ve mümkünse kaçınılmalıdır.   
- Arguman sayısının fazla olması testi de zorlaştırır.
- Çıktı parametresini anlamak girdi parametresini anlamaktan daha zordur.Bu yüzden sıfır argümandan sonra en iyi durum bir girdi parametresi almasıdır metodun.
### Bir Argümanlı Metod
- Bir fonksiyona bir argüman göndermenin iki durumu vardır.
    1. Soru sormak. ```bool IsFileExist(string fileName)```
    2. Operasyon.Bu argümanı alıp işlemek ve çıkan sonucu return etmek.
- üçüncü bir durum da  nadir olsada kulanışlı olan tek parametreli fonksiyonlara örnek eventlerdir.Eventler bu argümanı alır ve onu kullanarak bir state değişikliğne götürür sistemi.
- ```StringBuffer transform(StringBuffer in)``` is better than ```void transform-(StringBuffer out)```
### Flag Argümanlar
- Flag argümanlar çirkindir.
- Bir fonksiyona boolean bir argüman göndermek çok kötü bir pratiktir.
- Bu oluyorsa şu demektir:Fonksiyon birden fazla iş yapıyor.Hemen ikiye bölünmeli.
### İki Argümanlı Metod
- İki argümanlı bir fonksiyonu anlamak bir argümanlı bir fonksiyonu anlamaktan daha zordur.
- İki argümanlı durumlar bazen son derece normal olabiliyor.Mesela Point(int x,int y)
- Doğal uyum ve doğal sıralama fonksiyonun iki argümanlı olmasını gerektirebilir.
### Üç Argümanlı Metod
- Üç argümanlı metodu anlaması daha da zor iki argümanlı metodtan.
- Üç argümanlı bir metod yazmak için iyice düşün.
### Obje Argüman
- iki veya üç argümanı bazen obje yaparak azaltabilirsin.
```
Circle makeCircle(double x, double y, double radius);
Circle makeCircle(Point center, double radius);
```
### Liste Argüman
- İki veya üç argümanı liste argüman yaparak azaltabilirsin.
### Fiiler ve İsimler
- Tek argümanlı fonksiyon ismiyle argüman arasında yani fiil ile isim arasında uyum olmalı.
- Fonsiyonun ismi argümanın niyetini deşifre eder.
## Yan Etkiler
- Yan etkiler yalanlardır.Fonksiyonlar bir şey yapmaya söz vermişlerdir.Bazen gizli görevler de yaparlar.Bu yan etkiler geçici bağımlılıklara neden olur.
- Geçici bağımlılığınız zorunlu olarak varsa muhakkak bunu fonksiyonun isminde belirt.
### Output Argüman
- OOP öncesi output argümanlara ihtiyacımız vardı.Ama artık yok çünkü this keywordu zaten bunu sağlıyor.
- Hem argüman denilince kafamızda uyanan bir **input** olması.
## Command-Query Ayrımı
- Fonksiyonlar ya cevap verir ya da bir iş yapar.Ama ikisini birden yapmamalı.
- İkisini aynı fonksiyonda kullanmak kafa karışıklığına neden olur.
## Exceptionları Tercih Et
- Hata kodları dönmek yerine exceptionları tercih et.Çünkü Hata kodları fiil mi sıfat mı karmaşasından ziyade iç içe if yapılarına neden olur.
### Try/Catch
- Try/Catch blokları kodta çirkin gözükür.
- Try/Catch bloğunu ait olduğu fonksiyona çıkar.
```
public void delete(Page page) {
    try {
        deletePageAndAllReferences(page);
    }
    catch (Exception e) {
        logError(e);
    }
 }

 private void deletePageAndAllReferences(Page page) throws Exception {
    deletePage(page);
    registry.deleteReference(page.name);
    configKeys.deleteKey(page.name.makeKey());
 }

 private void logError(Exception e) {
    logger.log(e.getMessage());
 }
```
- Yukarıdaki delete fonksiyonu aslında sadece error processing ile ilgilidir.Fakat deletePageAndAllReferences fonksiyonu sayfayı silmekle ilgilidir.Error handlingi ayırmak okunaklığı ve düzenlemeyi kolaylaştırır.
### Hata Yönetimi
- Hataları yönetmek bir şeydir ve onu sadece bir fonksiyon yapmalı.Çünkü fonksiyonlar sadece tek şey yapmalı.
### Hata Kodları
- Hata kodları dönmek merkezi bir yerde bu hata kodlarını tutan/açıklayan bir sınıf veya enum gerektirir.Bu enum/sınıftaki değişiklik bütün kodu etkiler.
- Exception döndüğünde ise exception sınıfından türediği için hatalar, değişiklik yapman kodu etkilemez.
## Tekrardan Uzak Dur(DRY)
- Kod tekrarından uzak dur çünkü kodta gereksiz fazlalığa neden olur;bir değişiklik tekrar yazdığın kodu etkiliyorsa tüm bu tekrarlarda bu değişikliği yapman gerekir;tekrar edilen yerlerin hepsinde hata yönetimi yapman gerekir.
- Kod tekrarı belkide bütün yazılımda bütün kötülüklerin anasıdır.Bütün prensipler ve pratikler bunu kontrol altında tutmaya ve önlemeye yöneliktir.
## Yapısal Programlama
- Bazıları Edsger Dijkstra'ın yapısal programa ilkelerini takip ediyor:
**Her fonksiyonun bir girişi ve bir çıkışı olmalıdır.**
- Yani sadece tek bir return durumu olmalı.break ve continue,goto olmaz.
- Fakat bu söylediğimiz prensipleri uygularsak zaten fonksiyonlarımız küçük olacak ve bunlara gerek kalmıyacak çünkü bu prensipler uzun satırlı fonksiyonlarda anlamlıdır.
## Nasıl Böyle Fonksiyon Yazabiliriz?
- Kod yazma diğer yazma faaliyetlerinden biridir.Bir makale yazmadan önce aklımızdaki düşünceleri kağıda döker sonra okuya okuya değişiklik yapa yapa sonunda makalenin son haline ulaşırız.
- Kod yazma da tıpkı bunun gibidir.Fonksiyonları ayırırsın,isimleri değiştirirsin,tekrarları elimine edersin,metodları kısaltır ve yeniden organize edersin.
- Burdaki kuralları en başından itibaren uygulayıp kod yazılamaz.

