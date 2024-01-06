## VPS Serverınızı nasıl VPN olarak kullanabilirsiniz bunu anlatıcam.

Bildiğiniz gibi neredeyse bütün programlar ve sosyal medyalar kişisel bilgilerinizi alıp ürün niyetine satıyor... <br> Geçenlerde ülkemizde yaşanan üzücü patlama olayından sonra internet kullanımımız yavaşlatıldı ve neredeyse sosyal medyalara erişemeyecek durumda bırakıldık. İnternetten indirdiğiniz çoğu ücretsiz VPNler sizi adeta izleyip verilerinizi depoluyor ve bunu kendi çıkartları için kullanıyor. Ben de bundan kaçınmak için araştırmaya başladım ve vps serverların aynı zamanda vpn olarak kullanılabildiğini öğrendim. <br> <br>  Genelde çoğumuz VPSleri Ağ testnetlerini kullanmak için aldık, bu işlem VPS serverınıza ve içinde bulunan node'a hiç bir zarar vermez, uptimeı düşürmez rahatlıkla kullanabilirsiniz. 

## İhtiyacımız olan programlar
### 1) VPS Sunucu
  - Aktif bir sunucuya ihtiyacınız var, sunucu özellikleri fark etmiyor en düşük sistemlerde de çalışır.
  
### 2) Sunucunuza bağlanmak için herhangi bir ssh terminali (mobaxterm üzerinden anlatıcam)
  - Mobaxterm, gitbash, termius ya da sunucunuzun web terminalini kullanabilirsiniz
  
### 3) OpenVPN [link](https://openvpn.net/client-connect-vpn-for-windows/)
  - Bunu hem sunucumuza hem de vpni kullanmak istediğimiz cihaza indireceğiz. Sunucumuza kuracağımız ayrı cihaza kuracağımız ayrı programlar. Aşağıda windows için kurulumu bırakıyorum isteyen inceleyebilir. Diğer cihazlarda da mantık aynı şekilde. <br> (Appstore / Playstore / Windows / MAC Mevcut)

### 4) WinScp [link](https://winscp.net/eng/download.php)
  - Oluşturduğumuz .ovpn dosyasını sunucudan bilgisayarımıza indirmek için kullanacağız.
  
## Kurulum Aşamasına Geçelim

  - Öncelikle sunucunuza bağlanın ve aşağıdaki komutları yazarak işlemlere başlayın <br>
  `sudo su` <br>
  `cd` <br>
  `wget https://git.io/vpn -O openvpn-install.sh && bash openvpn-install.sh` <br>
  
  ### Karşınıza gelen soruları aşağıdaki gibi cevaplayın.
  ![image](https://user-images.githubusercontent.com/76253089/208157916-4e73f97a-27b9-42e3-a44b-48719ea7a07e.png)
  
  ### Son kısımda herhangi bi tuşa basıp kurulumun bitmesini bekleyin.
  ![image](https://user-images.githubusercontent.com/76253089/208158038-b3b92867-9dab-46b7-84d6-73b340019500.png)
  <br>
  <br>
  
  # Kurulum bitti, şimdi .ovpn uzantılı dosyamızı oluşturalım.
  ## Aşağıdaki komutu girin ve 1) Add a new client'i seçin
  `wget https://git.io/vpn -O openvpn-install.sh && bash openvpn-install.sh` <br>
  <br>
  ![image](https://user-images.githubusercontent.com/76253089/208158342-f24e15b1-d326-4296-9e13-66bf105e7156.png)
  
  ## isim olarak vpstovpn girin, entera bastıktan sonra dosyamız oluşacak şimdi bu dosyayı WinScp aracılığı ile bilgisayarımıza indirelim.
  ![image](https://user-images.githubusercontent.com/76253089/208158501-77cd8c7d-f27a-45ed-8eb8-3ba20240d48b.png)

  ## WinScpyi açın ve sunucu bilgilerinizi girip bağlanın.
  ![image](https://user-images.githubusercontent.com/76253089/208159256-9c7b69a9-795a-4064-9b03-d55b7bb1237f.png)

  ## En son oluşturduğumuz vpstovpn.ovpn dosyasını alıp masaüstümüze sürükleyelim otomatikmen inecektir.
  ![image](https://user-images.githubusercontent.com/76253089/208159732-07a51e94-4471-4d90-bd41-3282ec67f603.png)
  
  # Şimdi dosyayı cihazımıza indirdiğimiz OpenVPN uygulamasına aktarıcaz ve vpnimizi kullanmaya başlıycaz (sunucuya kurduğumuz openvpn farklı)
  ## OpenVPNi indirmediyseniz [buradan indirin](https://openvpn.net/client-connect-vpn-for-windows/) kurulumu yapın.
  
  ## OpenVPNi açtıktan sonra küçültülmüş olarak açılacak. Simgesine sağ tıklayın ve import kısmından import file'a basın. Oluşturduğumuz vpstovpn dosyasını seçin.
  ![image](https://user-images.githubusercontent.com/76253089/208160375-a0430f4b-2d36-41ba-98be-8c4e26dbacdc.png)
  
  ## Şimdi vpnimize bağlanıcaz 
  ![image](https://user-images.githubusercontent.com/76253089/208160602-18d7e4e0-053c-4010-a8df-2e2cc8484dfd.png)
  ![image](https://user-images.githubusercontent.com/76253089/208160890-8c8a9d8b-f3dd-4fec-a488-62a75efb8d08.png)
  
  ## Bu işlemlerden sonra başarılı şekilde vpninizi kullanıyor olacaksınız. İsterseniz what is my sitelerinden ipnizi kontrol edebilirsiniz. vpstovpn dosyasını telefonunuza ya da tabletinize aktarıp aynı şekilde kullanabilirsiniz. Mobil mağazanızda OpenVpni indirin dosyayı import edin ve bağlanın.

  ## İşinize yaradıysa repoyu yıldızlamayı unutmayın <3
  ![image](https://user-images.githubusercontent.com/76253089/208162651-4ccbca04-c344-4281-b16a-e9b43263480f.png)
  
