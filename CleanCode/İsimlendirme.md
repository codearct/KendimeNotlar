# Anlamlı İsimlendirmeler
## Niyetini Belli Et
- İsimlendirmelerin bağlamın niyetini belli etsin.
- Merak etme isimlendirme için harcadığın zaman isimlendirmeye dikkat etmediğinde harcıyacağın zamandan fazla olmayacak.
- Değişken,metod ve sınıf isimleri onların neden varolduğunu,ne için ve nasıl kullanılacağını açıklayıcı olsun.
- İsimlendirilen değişken,metod ve sınıflara açıklayıcı notlar ekliyorsan isimlendirmen yanlış demektir.
## Yanlış Yönlendirme
- İsimlendirmelerin yanlış ipuçları vermesin.
- Yerleşmiş anlamların dışında bir anlama gelen isimlendirmeler kullanma.
## Anlamlı Ayrımlar Yap
- İsimler farklıysa kodun içindeki anlamları da farklı olmalı.
- Dilimizin döndüğü isimleri kullan
    - Sayıları isimlerin sonuna yazmak(a1,a2...)niyet belli eden isimlendirme olmuyor.
    - Eş anlama gelebilecek geniş anlamlı **Info** ve **Data** gibi isimlendirmelerden uzak dur.
## Telaffuz Edebil
- Eğer telaffuz edemiyorsan neyi tartışabiliriz?
- Programlama aynı zamanda sosyal bir aktivitedir.
## Aradığında Bul
- Tek harfli kelimeler ve sabit rakamlar aradığını bulmakta seni zorlar.
- İsmin uzunluğu bulunduğu bağlamın uzunluğu ile doğru orantılı olmalı.
- değişkeni ve sabiti kod gövdesinin birçok yerinde kullanılırsan aradığında bulabileceğin şekilde isimlendir.
## Şifrelerden Kaçın
- Zaten çözmemiz gereken yeterince kod gövdesi varken sen de şifreli isimler koyarak geliştirici arkadaşları yorma.
## Macar Notasyonu 
- Hungarian Notation, DOS’un ilk zamanlarında Microsoft’un mimarlarından olan, Macar Dr. Charles Simonyi tarafından geliştirilmiş bir isimlendirme standardıdır. Bu standardın en belirgin tarafı, tip bilgisinin ismin başına kısaltma olarak gelmesidir.
- Nesnelerimiz güçlü tiplere sahip oldukları ve derlemeden önce tip hatalarını daha kolay yakalayabildiğimiz için artık Macar Notasyonundan kaçın.
## Ön Ekler
- İsimlerin önüne ismin çeşidini belli edecek ön isimler koymana gerek yok bunlar hep eskide kaldı.(değişkenlerin önüne v_,parametrelerin önüne p_ koyma!)
## Arayüz Öneki
- Üzgünüm Uncle Bob sana katılmıyorum.Interface sınıfların önüne "**I**" önekini getirmeye devam edeceğim.
## Zekisin Anladık
- Verdiğin kısaltmaları sen anlıyor olabilirsin ama biz senin kadar zeki değiliz o yüzden lütfen bizim de anlayacağımız isimlendirmeler koy.
## Sınıflar
- Sınıf isimleri tür olarak "isim" ve isim odaklı olmalı "fiil" ve fiil odaklı değil.
## Metodlar
- metod isimleri "fiil" ve fiil odaklı olmalı.
## Küçük Tatlılıklar
- Kodda küçük şakalar tatlılıklar yapma.Mizahçı karakterini bir kenara koy ve tavrını şakacı ifadelerden değil açık ifadelerden yana koy.
- Ne demek istiyorsan onu söyle.Ne söyleniyorsa onu anla.
## Bir Kavram Bir Kelime
- Her kavram için bir kelime seç ve birbirine bağla.
- Mesela bütün databaseden okuma operasyonlarını **Get** kelimesiyle işaretle ve hep bunu kullan.
- Tutarlı bir sözlük gibi kavram kelime ilişkisi kodu kullananlar için de büyük nimettir.
## Kelime Oyunu Yapma
- İki amaç için tek bir kelime kullanma
- Database e birşey eklemeyi **add** kelimesiyle karşıladıysan listeye birşey eklemeyi **add** ile karşılama.Onun yerine **insert** de ve **bir kavram için bir kelime** kuralına uy.
- Yazar olarak görevimiz kodu olabildiğince kolay anlaşılır yapmaktır.Akademik makale yazmıyoruz.
## Tanıdık İsimler
- Kodumuzu programcılar okuyacak bu yüzden onların aşina olduğu kelimeleri kullan.
## Problem Domain
- Her kelimenin anlamını domain expertlere sorduklarında cevap alabilmeleri için domain içinden kelimeler kullan.
## Anlamlı Bağlamlar
- Değişkenleri,metodları,sınıfları öyle bir isimlendirmelisin ki okuyucu bağlamı kolayca anlayabilmeli.
- En son çare ön ek.Mesela  addrFirstName, addrLastName, addrState...
## Gereksiz Bağlamlar
- Gereksiz bağlamlar eklemene gerek yok.**Address** isimli sınıfın yeterliyse **CustomerAddress** diye isimlendirmene gerek yok.
- Açıklayıcı olduğu sürece kısa isimlendirmeler tercih edilmelidir.
