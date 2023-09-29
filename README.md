# Takio-Testnet

![rzm5azrr](https://github.com/tuncgs52/Takio-Testnet/assets/80161670/712a3f97-7bfb-4a1c-b742-bb9cf17f179a)

# Taiko nedir?
Taiko, merkezi olmayan, Ethereum eşdeğeri bir ZK-Rollup'tır. 

# İlk Önce Gerekli Kütüphaneleri indiriyoruz.

```
sudo apt update
```

```
sudo apt upgrade
```

```
apt install docker-compose
```

```
sudo apt-get update && sudo apt install jq && sudo apt install apt-transport-https ca-certificates curl software-properties-common -y && curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add - && sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu focal stable" && sudo apt-get install docker-ce docker-ce-cli containerd.io docker-compose-plugin && sudo apt-get install docker-compose-plugin
```

# Repoyu klonluyoruz.

```
git clone https://github.com/taikoxyz/simple-taiko-node.git
cd simple-taiko-node
```


# Dosya İsmini Değiştitin.

```
cp .env.sample .env
```


Klasörün içine girin.

```
nano .env
```

# Simdi Alchemyden rpc alacağız.
> ## [BURAYA BASIN]([https://scan.mindnetwork.xyz/](https://alchemy.com/?r=Tg4MzUyMTk1NjI3M)https://alchemy.com/?r=Tg4MzUyMTk1NjI3M)

 Hesap oluşturun, Ardından "APPS" Kısmına geliyoruz. 
"Create New App" Diyoruz. Aşağıdaki Gibi Sepolia Ağını Seçiyoruz.

![Ekran görüntüsü 2023-09-29 224039](https://github.com/tuncgs52/Takio-Testnet/assets/80161670/830bb4bf-d97e-4661-9cb5-4396fe76f222)

"Apı Key" basın. Rpc Bilgileri Gözükecek.
![Ekran görüntüsü 2023-09-29 224039](https://github.com/tuncgs52/Takio-Testnet/assets/80161670/5ad5041a-37b0-4d1f-a526-4068fb3418eb)

Sunucumuzda Düzenleyeceğimiz Yerlere Gelelim.



