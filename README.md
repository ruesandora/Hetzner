<h1 align="center"> Hetzner Hakkında ve Kullanımı </h1>

<h1 align="center"> Neden Hetzner hocam? </h1>

```
# Daha önce neden hetzner kullandığımı ve sunucu kıyaslaması yapmıştım, dolayısıyla özet geçeceğim. 
 
> Hetzner VPSde de, VDS'de de en ucuzu.
>> Bugün 2 CPU 2 RAM andromeda kurdum 3$'a, farklı firmalardan almak istesem 13-18$ arası ödemek durumundayım.
>>> Lokasyon tercihlerinde ek ücret yok, setup fee yok. (kurulum ücreti genelde 5-7 dolardır)
>>>> Refle üye olduysanız 20$ hediye ediyor ve istediğin zaman istediğiniz kadar sunucuda kullanabiliyorsunuz.
>>>>> Yeni kullanıcının test etmesi ve emin olması için 20$ hele ki Türk insanına bal gibidir.

> Hetzner VPS'ler arasında en verimlisi (fiyatının ucuzluğuna rağmen.) Herhangi bir node patlaması veya benzeri bir şey yaşamadım.
>> Sunucu satın aldığınızda sunucu aktifken işletim sistemi değiştirebiliyorsunuz (data gider)
>>> Sunucu satın aldığınızda 48 saat içersinde sunucu elinize ulaşacak diye bir şey yok, anında veriliyor. (Şu an 10 sunucum var)

> Arayüz olarak kullanımı çok kolay, sunuculara isim verme, sunucuyu resetleme, şifre değiştirme, snapshot alma, IP değişme, çok kolay.
>> Bunları kısaca aşağıda anlatacağım.

> Ve hayat kurtaran kullandıkça ödeme, saatlik ücret ve paranın boşa gitmesi yok.
>> Hetznerde bir sunucu aldınız, bir süre kullandınız, kapattınız ücret yok (veya bir kaç cent)
>>> Sunucu aldınız, ödeme yapmıyorsunuz, kullanıyorsunuz, 1 ay sonra (genellikle ayın 1'i ve 3'ü arası) ödeme istiyor.
>>>> Sunucu iadesi diye bir şey yok, işini bitti mi, delete tuşuna basıp kapatıyorsunuz, ne kadar kullandıysanız alıyor sadece. Bazende almıyorlar düşük kullanımda.

> Daha fazla özellik olabilir aklıma gelmiyor, doğaçlama yazdım, iyi veya kötü yanlarını eklemek isteyen pull request yapabilir.

# Kötü yanları:

> Hetzner ödeme vb. konularda bu kadar kolaylık sağladığı için haliyle KYC mevcut.
>> KYC Hetzner'in en sevmediğim özelliği, sonuna kadar haklılar lakin KYC genel olarak sevmiyorum ve paylaşmak hoşuma gitmiyor.
>>> Sanırım her sanal kartı kullanamıyoruz, ödeme konusunda visa istiyor, kaydı kaydederken insanı kanser edebiliyor.
>>>> Kripto para ile ödeme yok. (Burası kötü mü bilmiyorum :P)
>>>>> Hetzner'de ref paylaşabilmek için belli bir miktar para harcamak veya zaman harcamak gerekiyor. Ben çok kullandığım için açık.
```

<h1 align="center"> Nasıl kullanıyorum? </h1>

> Hetzner'in 20 dolar bakiyesini almak isteyenlere [link](https://hetzner.cloud/?ref=gIFAhUnYYjD3)

```
> Öncelikle, hetznerin  bir çok subdomain'i var haliyle bir çok servisi var. VDS, VPS, cloud servis, storage vs vs..
>> VPS'ler için bu linkten ve arayüzde hetzner'i kullanmalısınız: https://console.hetzner.cloud/projects (Görsel bırakıyorum aşağıya)
```

![image](https://github.com/ruesandora/Hetzner/assets/101149671/51ab9fa6-6c23-43fb-82f0-0b94827ef3ff)

<h1 align="center"> Step by Step anlatım </h1>

```
> New Project kısmından eğer yeni bir proje ise yeni bir alan açıyorum.
>> Daha sonra Sağ üstten add server diyerek serverimi oluşturmaya başlıyorum.
```
![image](https://github.com/ruesandora/Hetzner/assets/101149671/ebf828b7-23c3-423d-8fe9-e285e5372015)

```
> Lokasyon seçiyoruz.
>> Tecrübeyle sabit, Alman sunucuları en iyi çalışanlar. (Hetzner bir Alman şirketi)
>>> Bir işletim sistemi seçiyoruz, genelde Ubuntu 20.04 tercihimdir, en stabil çalışan budur.
>>>> Daha sonra sunucu seçiyorum, genellikle 7 ila 3 dolarlık sunucuları kullanıyorum.
>>>>> Sunucu tercihi tamamen oluşturacağınız projeye bağlı.
>>>>>> Son olarakta en alttan server name'i proje ismi yapıp sağ taraftan Create&Buy now diyerek sunucumu oluşturuyorum.
>>>>>>> Bir kaç tuşta oluşuyor.
```

<h1 align="center"> En güzel kısım </h1>

> Burada her bir özelliğe bir numara verdim, no-1, no-2.. diye, görselden bakarak hetzneri tam olarak öğrenebilirsiniz.

``` 
# No-1, Burada Hetzner IPv4 ve IPv6 adreslerimiz yazar. SSH bağlantısı (sunucuya bağlanma) yaparken IPv4 (1. olan) kullanırız.
# No-2, Sunucuyu açtığından beri ne kadar tutmuş ve kapatırsan ne kadar ödeyeceğin yazar. Misal benimki $0.30 tutmuş şu an.
# No-3, Sunucuyu komple kapatma, delete derken sunucunun ismini yazıp delete yapıyorsunuz.
# No-4, Rescue, sık kullanırım (unuttuğum için), sunucuya bağlanamadığımda şifreyi değişirm. Burada root password diyerek şifre değiştiriyoruz.
# No-5, Rescale, sunucuyu yükseltmek istediğinizde kullanabileceğiniz alan. (kötü taraf düşürme yok)
# No-6, Rebuild, Sunucunuzu işletim sitemini değiştirmek istediğinizde kulalnabilirsiniz. Mesela ubuntu 18'den 20'ye çıkarmak gibi. (data gider)
# No-7, Buradan direkt sunucunuza SSH bağlantısı yapabilirsiniz, bunuda putty mutty uğraştırdıgı zman kullanırım.
# No-8, Sunucuyu silceksiniz veya reset atacaksınız snapshot almak istersenz buradan alabilirsiniz.
```

![Hetzner anlatım](https://github.com/ruesandora/Hetzner/assets/101149671/2e592842-9178-47f4-8c14-dcb0bb9ebfd3)

> No-9'u ayrı olarak paylaşmak istedim, altta ki görselde ki gibi sunucunuz hakkında veri alabilirsiniz.

> Bazı projeler bu veriyi istiyor, oldukça güzel.

![image](https://github.com/ruesandora/Hetzner/assets/101149671/1ec09ac1-9653-4b07-8c94-c4b5c381cae7)

> Başkada bir şey yok her halde, varsa bana PR gönderebilirsiniz, si yu later.















