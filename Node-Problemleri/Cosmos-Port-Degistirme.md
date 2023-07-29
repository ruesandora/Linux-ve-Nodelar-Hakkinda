<h1 align="center"> Cosmos Hub'larında port değiştirme </h1>

> İlk başta aşağıda ki belirtilen komutu kullanarak ve kendi projenize uyarlayarak `config.toml` klasörümüze giriş yapalım.

> Özetle: `.ruesd` değişecek kendi projeniz neyse, mesela .gitopiad giriş yapılacak.

```
nano $HOME/.ruesd/config/config.toml
```

> Sonrasında ilk başlarda olan `proxy_app` isimli portu `36657` veya `36658` olarak değiştirelim.

> `CTRL + W` ile arama yapabilirsiniz.

> Bende `26658` kullanıyor sizde de `26658` veya `26657`'dir.

![image](https://github.com/ruesandora/Linux-ve-Nodelar-Hakkinda/assets/101149671/3e77ef59-0706-426b-a2e6-fe0722a49b45)

> Sonrasında 2 `laddr` tcp portunu `36657` veya `36658` değiştirelim.

> proxy'e 57'yi seçtiyseniz laddr 58 olsun, aynı port olmasın.

> BURAYA DİKKAT: `2 adet laddr portu vardır`, biri 56 diğeri 57 diye biter, 2. portuda bulup 36656 değerini verelim.

![image](https://github.com/ruesandora/Linux-ve-Nodelar-Hakkinda/assets/101149671/d40fbd6e-1a1a-4ca7-a285-4dc750514efa)

> Artık nasıl yapıalcağını biliyorsunuz, sırasıyla:

> `pprof_laddr` portu (bu localhosttur son portumuzla beraber farklıdır) `36660` değerini verebiliriz.

>  son olarak `prometheus_listen_addr` `36660` veya `36661` olarak değişebiliriz.

<h1 align="center"> config/config.toml'dan, config/client.toml'a geçiyoruz</h1>

> Burada node isimli bir port olacak bunu istediğiniz yapabilirsiniz ben 1984 yapıyorum, ama varsayılan `36657`.

```
nano $HOME/.ruesd/config/client.toml
```

<h1 align="center"> config/client.toml'dan, app.toml'a geçiyoruz</h1>

> `app.toml`'dan address isimli `2` portumuz var bu iki portu `10090` ve `10091` şeklinde değiştirelim.

```
nano $HOME/.ruesd/config/app.toml
```

* Rehberi daha bilgi detaylı yapabilirdim ama basit bir şeyi kafa karıştırıcı yapmak istemedim, eksik görürseniz PR atarsınız.




