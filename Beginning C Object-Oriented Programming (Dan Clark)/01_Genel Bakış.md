- Bu bölümde bunları öğrenicez

1. OOP nedir?
2. OOP neden bu kadar önemli hale geldi?
3. Dili OOP yapan karakteristiklikler nelerdir?
4. Tarihi ve gelişimi nedir?

## OOP Nedir?

- OOP bir görevi başarmak için objeler arasındaki etkileşim üzerine kuruludur.
- Objeler birbirlerine mesaj gönderip alırlar ve bu mesajların cevabına göre de aksiyon alırlar.
- Böylece kullanıcılar görevin sonucuyla ilgilenir ve iç süreçlerinden izole edilmiş olurlar.

## OOP Tarihi

- 1960 ların ortalarında Simula programlama dili ile gün yüzüne çıkmaya başladı.
- 1970 lerde SmalkTalk ile daha da gelişti.
- 1980 lerde C++ ve Eiffel gibi OOP temelli diller popüler hale geldi.
- 1990 larda Javanın ortaya çıkmasıyla ilgi çekmeye devam etti.
- Tataaaaaa 2002 C#

## Neden OOP?

- 1970 ve 80 lerde prosedürel programlama dilleri olan C,Pascal,Fortran iş hayatında kullanılan yaygın dillerdi.
- Prosedürel programlama birkaç yüz satırlık bir kodda sorun çıkarmıyordu.Fakat kod büyümeye başladığında yönetmesi ve debug etmesi zorlaşıyordu.
- Kodu yönetebilmek için kodu prosedürlere ve fonksiyonlara bölen Yapısal Programlama tanıtıldı.Fakat zamanla eksiklikleri gün yüzüne çıkmaya başladı.

  - Bakımı zordu.
  - Mevcut kodu tüm sistemi etkilemeden değiştirmek zordu.
  - Yeni program yapmak demek yeniden yazmak demekti.Önceki eforlarınız çöpe gidiyordu.
  - Takım çalışmasına uygun değildi çünkü programcılar kodun tamamını bilmek zorundaydılar kodun bir kısmını izole edemiyorlardı.
  - İş modelini programın modeline dönüştürmesi zordu.
  - Yapısal programlama programı izole etmede başarılıydı fakat diğer sistemlerle entegre olmakda başarısızdı.

- Tüm bu eksikliklerin üzerine bilgisayar dünyasındaki gelişmeler Yapısal Programlama üzerinde daha da fazla baskıya neden oldu.
  - Programcı olmayanlar programı kullanabilmek için arayüz ve masaüstü uygulama talebinde bulunmaya başladılar.
  - Kullanıcılar daha fazla sezgisel ve daha az yapısal etkileşim istediler programla.
  - Bilgisayar sistemleri iş mantığının,arayüzün ve veritabanının birbirine daha az bağımlı olduğu dağıtık sistemlere doğru evrildi ve internete-intranete erişim sağlandı.
- Tüm bu nedenlerden ve aşağıdaki faydalarından dolayı geliştiriciler OOP ye yöneldi.
  - iş modelinden yazılım modeline geçiş daha sezgisel
  - Kodun bakımının kolaylığı ve kodun değiştirilmesindeki esneklik ve hız
  - Takım çalışmasına uygun ve bir takımın kodun bir parçasına yoğunlaşmasına izin vermesi
  - Yazılan kod parçalarının başka kodlarda tekrar kullanılabilmesi ve 3. parti uygulama olarak başka programcıların kullanımına açılabilmesi.
  - Dağıtık sistemlere entegre olmasındaki kolaylık
  - Modern işletim sistemleriyle gelişmiş entegrasyon
  - Kullanıcılar için daha sezgisel arayüzlerin yapılabilmesi

## OOP Karakteristikleri

### Obje

- Obje veriler ve bu verileri kullanan prosedürleri kendi bünyesinde birleştiren yapıdır.

### Soyutlama

- Dış dünyadaki bir objeyle etkileşime girdiğimizde aslında o objenin bütün özellikleriyle ilgilenmeyiz.Belli başlı özellikleriyle ilgileniriz aslında.
- Mesela bir araba sürücüsü olarak arabanın hızıyla ve gittiği yönle ilgiliyimdir ama motorun dakikada kaç devir yaptığınla ilgilenmem fakat bir araba yarışçısı bunu da dikkate almalıdır.
- İşte OOP dünyasındaki objelerde sadece uygulamanın ihtiyacı olan bilgiyle ilgili olmalıdır.

### Kapsülleme

- Kapsülleme kullanıcıdan gizlenen veriye kullanıcının direk erişiminin olmamasıdır.Kullanıcı bu veriye erişmek istiyorsa bu veriden sorumlu objeyle etkileşime girmelidir.
- Datanı kapsüllemek datanın ait olduğu sistemi daha güvenli ve güvenilir yapar.

### Çok Biçimlilik

- Çok biçimlilik iki farklı objeye gelen aynı isteğin kendilerine özgü bir şekilde cevap verebilmesidir.
- OOP dünyasında bu işlem "overloading" denen bir işlem ile yapılır.

### Kalıtım

- Bir çok gerçek dünya objesini sınıflandırırız."Köpekler dört ayaklıdır" gibi.Belli ortak özelliklerine göre alt sınıflara ayırırız.Ayrıca objeleri sadece ortak özelliklerine göre ortak davranış biçimlerine göre de ayırırız.
- Dünyayı anlamak istiyorsak objeleri sınıflandırmalıyız belli hiyerarşilerle.
- OOP dünyasında da objelerimizi genel özellik ve işlevlerine göre sınıflandırmalıyız.Bu objelerle çalışmamızı kolaylaştırırz ve dış dünyayla benzerliğinden dolayı sezgisel anlaşılması kolay hale getirir.
- Kalıtım ebeveyn objelerde kullandığımız ortak özellikleri çocuk objelere aktarabildiğimiz için otomatik olarak program yazmamızı da kolaylaştırır.

### Birleşim

- Bir obje beraber çalıştığı objelerin birleşiminden oluşabilir.
- Mesela araba objesi tekerlekler ve motor adlı iki objenin birleşimidir.
