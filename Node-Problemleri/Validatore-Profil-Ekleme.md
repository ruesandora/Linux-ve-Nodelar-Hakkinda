<h1 align="center"> Keybase </h1>

<h1 align="center"> Kolay ve basit bir şekilde validatorumuze resim ekleyelim </h1>

> [Keybase](https://keybase.io/rues) üzerinden bir hesap oluşturuyoruz.

> `Hesap oluşturduğunuzda beni ve arkadaşlarınızı takip etmeyi unutmayın.`

> Sonra aşağıda ki adımları takip ediyoruz:

> Görselde ki gibi bir profil oluştuktan sonra keyimize `16 haneli olur` tıklıyoruz.

![image](https://github.com/ruesandora/Linux-ve-Nodelar-Hakkinda/assets/101149671/091c4b82-c0f1-4fdf-8481-ee07bc1a1471)

> Aşağıda ki görselde gördüğünüz gibi 2 tür `key` var:

![image](https://github.com/ruesandora/Linux-ve-Nodelar-Hakkinda/assets/101149671/c7d061d5-8ef7-4590-ad65-152cb86554d9)

> İkisinide kaydedip saklayalım bir yere.

> Kaybederseniz de `keybase.io/hesapisminiz` şeklinde google'da arama yaparak bulabilirsiniz.

<h1 align="center"> Şimdi key'imizi kullanalım </h1>

> Aşağıda gördüğünüz gibi validatör oluşturma komutu var, komutun arasında `--identity` flagını göreceksiniz.

> Bu flagın karşısına iki keyden birisini yazın (Bazen ilki çalışır bazen 2.'si ama genelde ikiside çalışır)

> Artık `validatör` profilinizde `keybase` hesabınızda kullandığınız fotoğraf mevcut duruma gelecektir.

```
bonus-blockd tx staking create-validator \
--amount 900000ubonus \
--pubkey $(bonus-blockd tendermint show-validator) \
--moniker "yourMonikerName" \

==> ==> ==> --identity "yourKeybaseId" \ <== <== <==

--details "yourDetails" \
--website "yourWebsite" \
--chain-id blocktopia-01 \
--commission-rate 0.05 \
--commission-max-rate 0.20 \
--commission-max-change-rate 0.01 \
--min-self-delegation 1 \
--from yourWalletName \
--gas-adjustment 1.4 \
--gas auto \
-y
```
