# Taiko-Testnet

![rzm5azrr](https://github.com/tuncgs52/Taiko-NODE-Testnet/assets/80161670/97082dcb-8753-4479-abef-496118fcaa54)



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


# Dosyamızı Ayarlıyoruz.

```
cp .env.sample .env
```

# Simdi Alchemyden rpc alacağız.
> ## [BURAYA BASIN]([https://scan.mindnetwork.xyz/](https://alchemy.com/?r=Tg4MzUyMTk1NjI3M)https://alchemy.com/?r=Tg4MzUyMTk1NjI3M)

 Hesap oluşturun, Ardından "APPS" Kısmına geliyoruz. 
"Create New App" Diyoruz. Aşağıdaki Gibi Sepolia Ağını Seçiyoruz. Create App diyoruz ve rpc'yi oluşturuyoruz.

![Ekran görüntüsü 2023-09-29 224039](https://github.com/tuncgs52/Taiko-NODE-Testnet/assets/80161670/6458d157-9e11-45e2-b0e1-2a336162b122)


"Apı Key" basın. Rpc Bilgileri Gözükecek.
![Ekran görüntüsü 2023-09-29 233801](https://github.com/tuncgs52/Taiko-NODE-Testnet/assets/80161670/cab50bde-37a1-4c4c-930b-afc6bbb28c59)




# Sunucumuzda Düzenleyeceğimiz Yerlere Gelelim.
İlk önce klasörün içine giriyoruz.

```
cd simple-taiko-node
```

```
nano .env
```
1-) SS'teki yerleri rpc bilgilerimizle dolduruyoruz.

![Ekran görüntüsü 2023-09-29 231647](https://github.com/tuncgs52/Taiko-NODE-Testnet/assets/80161670/da9fed14-331b-4932-b24e-a5cb7b1d6105)


"L1_ENDPOINT_HTTP" Yazan Yere SS'teki Linki Kopyalayarak Giriyoruz.
![Ekran görüntüsü 2023-09-29 231436](https://github.com/tuncgs52/Taiko-NODE-Testnet/assets/80161670/64800fcf-de86-4997-8cc8-716b0e0dedcd)


"L1_ENDPOINT_WS" Bu kısmada Alttaki SS Linkini Kopyalayarak Giriyoruz.
![Ekran görüntüsü 2023-09-29 232234](https://github.com/tuncgs52/Taiko-NODE-Testnet/assets/80161670/8f5c0ab3-50b6-4b59-b3c0-0e686026c238)


2-) "ENABLE_PROVER=false" Burayı "true" Yapıyoruz.
![Ekran görüntüsü 2023-09-29 232703](https://github.com/tuncgs52/Taiko-NODE-Testnet/assets/80161670/3c5fe91f-95b5-4a82-bba9-33ce690174f4)


3-) En Son deposit ettiğimiz taiko cüzdanın private keyini "L1_PROVER_PRIVATE_KEY=" alanına giriyoruz.
![Ekran görüntüsü 2023-09-29 233033](https://github.com/tuncgs52/Taiko-NODE-Testnet/assets/80161670/e0a312fc-e364-449f-b4ed-84dd2e8f45cc)

CTRL X Y ENTER, yapıp kaydedip çıkıyoruz.

# Son Olarak Node'yi başlatıyoruz.

```
screen -S taiko
```

```
docker compose up -d
```

LOGLAR GÖZÜKMEZSE

```
docker compose logs -f
```


