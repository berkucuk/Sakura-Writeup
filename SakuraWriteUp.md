# Tryhacme Sakura WriteUp

Questions :
1-Saldırgan hangi kullanıcı adını kullanıyor?
2-Saldırganın kullandığı tam e-posta adresi nedir?
3-Saldırganın tam gerçek adı nedir?
4-Saldırgan hangi kripto para birimi için kripto para cüzdanına sahip?
5-Saldırganın kripto para cüzdan adresi nedir?
6-Saldırgan 23 Ocak 2021 UTC'de hangi madencilik havuzundan ödeme aldı?
7-Saldırgan, kripto para cüzdanını kullanarak başka hangi kripto para birimini değiştirdi?
8-Saldırganın şu anki Twitter hesabı nedir?
9-Saldırganın WiFi SSID'lerini ve şifrelerini kaydettiği konumun URL'si nedir?
10-Saldırganın Ev WiFi'sinin BSSID'si nedir?
11-Saldırganın uçağa binmeden önce fotoğraf paylaştığı konuma en yakın havalimanı hangisidir?
12-Saldırgan son konaklamasını hangi havaalanında yaptı?
13-Saldırgan tarafından eve son uçuşlarındayken paylaşılan haritada hangi göl görülebilir?
14-Saldırgan muhtemelen hangi şehri "ev" olarak görüyor?

# 1-Saldırgan hangi kullanıcı adını kullanıyor?
![Alt text](https://raw.githubusercontent.com/Berkkucukk/Sakura-writeup/main/exif.png)
Bize verilmiş olan .svg uzantılı fotoğrafı tarayıcımızda veya text editör yardımıyla açtığımız zaman, içerisinde /home/SakuraSnowAngelAiko/Desktop/pwnedletter.png şeklinde bir path buluyoruz. Buradan home klasöründeki kullanıcı adı bize tam adı veriyor.

# 2-Saldırganın kullandığı tam e-posta adresi nedir?
![Alt text](https://github.com/Berkkucukk/Sakura-writeup/blob/main/hash.png?raw=true)
![Alt text](https://raw.githubusercontent.com/Berkkucukk/Sakura-writeup/main/gpg.png)

Bulduğumuz sosyal medya hesaplarını incelediğimiz zaman github'da bir gpg key olduğunu görüyoruz. Bu keyi indirip bir linux cihazımızdan import ettiğimiz zaman bize tam e-posta adresini vermiş oluyor.

# 3-Saldırganın tam gerçek adı nedir?
![Alt text](https://raw.githubusercontent.com/Berkkucukk/Sakura-writeup/main/twitter.png)
LinkedIn proifinden tam adına ulaşabiliriz.

# 4-Saldırgan hangi kripto para birimi için kripto para cüzdanına sahip?
![Alt text](https://github.com/Berkkucukk/Sakura-writeup/blob/main/eth.png?raw=true)
Bulduğumuz GitHub hesabında "ethwallet" adında bir repo olduğunu görüyoruz. Bu repository'nin geçmiş bölümünde ilk yüklendiği haline erişebiliriz. Reponun geçmişine gittiğimiz zaman içerisinde ethereum cüzdanı olduğunu görüyoruz. Buradan ethereum kullandığını öğrenmiş oluyoruz.

# 5-Saldırganın kripto para cüzdan adresi nedir?

Ethwallet GitHub reposunu incelediğimiz zaman eti wallet adresini öğrenmiş oluyorduk.

# 6-Saldırgan 23 Ocak 2021 UTC'de hangi madencilik havuzundan ödeme aldı?
![Alt text](https://github.com/Berkkucukk/Sakura-writeup/blob/main/eth2.png?raw=true)

Bulduğumuz Ethereum cüzdanını herhangi bir eti wallet search sitesinde aratarak o cüzdan ile yapılan tüm işlemleri görebiliyoruz. 23 ocak 2021 tarihinde ethermine pool'undan bir giriş olduğunu görüyoruz.


# 7-Saldırgan, kripto para cüzdanını kullanarak başka hangi kripto para birimini değiştirdi?

![Alt text](https://github.com/Berkkucukk/Sakura-writeup/blob/main/eth3.png?raw=true)
Bu kripto para cüzdanını incelemeye devam ettiğimiz zaman tether adında coin işlemleri görüyoruz.

# 8-Saldırganın şu anki Twitter hesabı nedir?
![Alt text](https://github.com/Berkkucukk/Sakura-writeup/blob/main/twitter.png?raw=true)
Bize verilen görüntü içerisinde twitter username'i @AikoAbe3 bir dm görüyoruz. Bu username'e gidildiği zaman şu anda kullandığı twitter hesabını bulmuş olduk.

# 9-Saldırganın WiFi SSID'lerini ve şifrelerini kaydettiği konumun URL'si nedir?
![Alt text](https://github.com/Berkkucukk/Sakura-writeup/blob/main/wifi.png?raw=true)
deeppastebin onion site suanda aktif durumda olmadığı için Tryhackme hint bölümünden ipucu alıyoruz. İpucundaki erlin sonuna Twitter'da paylaştığı 0a5c6e136a98a60b8a21643ce8c15a74 keyini ekleyerek şifrelerini kaydettiği url'i elde etmiş oluyoruz.

# 10-Saldırganın Ev WiFi'sinin BSSID'si nedir?
![Alt text](https://github.com/Berkkucukk/Sakura-writeup/blob/main/wifi2.png?raw=true)
deeppaste onion sitesinde "Ev WiFi: DK1F-G Fsdf324T@@" bilgisine ulaşıyoruz. Burada elde ettiğimiz ssid'yi https://wigle.net/ sitesinde advenced scan yaparak nerede bulunduğunu ve BSSID bilgisine ulaşıyoruz.

# 11-Saldırganın uçağa binmeden önce fotoğraf paylaştığı konuma en yakın havalimanı hangisidir?
![Alt text](https://github.com/Berkkucukk/Sakura-writeup/blob/main/airport1.png?raw=true)
Bu tweet'te  Aiko, "Eve gitmeden önce bazı son dakika kiraz çiçeklerine göz atın!" şeklinde paylaştığı fotoğrafı inceliyoruz. Fotoğrafta, Washington Anıtı uzakta görünüyor. Washington Anıtı yakınındaki havaalanlarını aramak için bir harita kullandım ve havaalanı koduDCA  olan Ronald Reagan Washington Ulusal Havalimanı'nı buldum.


# 12-Saldırgan son konaklamasını hangi havaalanında yaptı?
![Alt text](https://github.com/Berkkucukk/Sakura-writeup/blob/main/airport1.png?raw=true)

Saldırgandan gelen bir sonraki tweet, son konaklamaları için ziyaret ettikleri birinci sınıf bir salonun adını gösteriyor. Salonun Japan Airlines'a (JAL) ait olduğunu görebiliyorum ve Google'da  Sakura lounge için bir arama, Tokyo Uluslararası Havalimanı, Haneda'da (HND) bulunduğunu gösteriyor.



# 13-Saldırgan tarafından eve son uçuşlarındayken paylaşılan haritada hangi göl görülebilir?
![Alt text](https://github.com/Berkkucukk/Sakura-writeup/blob/main/lake.png?raw=true)
Japonya'nın bu bölgesine zaten bir harita üzerinde bakıyordum ve Inawashiro Gölü adını buldum.

# 14-Saldırgan muhtemelen hangi şehri "ev" olarak görüyor?

Wigle.net sitesine ssid'yi aradığımız zaman bize evinin adresini vermiş oluyor.


