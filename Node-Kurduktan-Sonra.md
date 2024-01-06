<h1 align="center"> Node kurduktan sonra yapılması gerekenler </h1>

 * Bir node kurduktan sonra, yapmamız gereken bazı işlemler ve bazı önlemler vardır, aynı zamanda alacağımız bu önlemler `node taşıma` işlemi yapmak istediğimiz zamanda ihtiyacımıza yarayacak.
 * Temelden başlayalım:

1. Node'u güncel tutmak: Blockchain ağları sürekli gelişmektedir ve node'unuzu bu gelişmelerle uyumlu hale getirmek gerekiyor. Bu nedenle, node'unuzu ara ara güncellemeniz ve en güncel sürümünü kullanmanız önemlidir.


2. Node'u izlemek ve yönetmek: Node'unuzu ara ara kontrol etmek gerekir. Bu, node'unuzun performansını izlemek ve gerekirse ayarlarını değiştirmek için gereklidir. 

3. Gerekli dosyaları kaydetmek ve saklamak: Bir node/validatör kurduktan sonra (testnete göre değişir) bazı şeyleri saklamak gerekir. Örneğin `Cosmos` projelerinde en önemli iki şey `priv_validator_key.json` dosyası (ismi değişkenlik gösterebilir buna yakındır) ve node kurarken oluşturduğunuz cüzdan bilgileri. `priv_validator_key.json` nerede? WinSCP veya Mobaxterm kullanıyoruz burada ve `/root/.gitopia/config` klasörünün içinde olur. `.gitopia` klasörü gözükmüyorsa root'un içinde `CTRL ALT H` yaparak görebilirisiniz.


![image](https://user-images.githubusercontent.com/101149671/205723332-37585e1b-30d7-444b-8b87-c1734f07c0c2.png)


Cosmos projeleri dışında saklanması gereken şeyler genellikle şunlar oluyor:

Projelerden örnek vereceğim, bir node kurarken en önemli kısım neresiyse orası saklanır zaten:

Exorde cüzdan adresi

Ziesha Network 12 kelime

Gitopia priv validatör key json

## Özet:

 * Node'u güncel tutmak ve ara ara kontrol etmek
 * Gerekli bilgileri kaydetmek

<h1 align="center"> Node Nasıl Taşınır? </h1>

* Bir node kurdunuz, daha sonra sunucunuzun süresi bitti veya farklı bir sunucuya geçiş yapmak istiyorsunuz o node'u oraya nasıl taşıyacaksınız? bir kaç örnek vereyim:

1. Ziesha Network: Taşıyacağınız sunucuda node'unuzu kurarsınız, nodu çalıştırma aşamasına geldiğinde eski node'u durdurup bir önce ki node'da ki 12 kelimeyi ve discord handle kullanarak node'unuzu kurarsınız. Diğer sunucudan burada ki sunucuya taşınmış olur.

2. Cosmos projeleri: priv validator ve 12 kelimeyi yukarıda anlattığım gibi saklamıştık. Diğer sunucuda aynı şekilde node'u kuruyoruz, diğer sunucuda kurulum yaparken node'u durdurun. Daha sonra taşıyacağınız sunucuda diğer node'da kullandığınız 12 kelimeyi recover edin. (Recover gibi komutlar için sözlük). Winscp ile `/root/.projeismi/config` klasörünün içine `priv_validator_key.json` dosyasını aktarıyoruz ve node'u çalıştırıyoruz.




