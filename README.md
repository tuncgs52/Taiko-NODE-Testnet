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


# Dosyamızı Ayarlıyoruz.

```
cp .env.sample .env
```

# Simdi Alchemyden rpc alacağız.
> ## [BURAYA BASIN]([https://scan.mindnetwork.xyz/](https://alchemy.com/?r=Tg4MzUyMTk1NjI3M)https://alchemy.com/?r=Tg4MzUyMTk1NjI3M)

 Hesap oluşturun, Ardından "APPS" Kısmına geliyoruz. 
"Create New App" Diyoruz. Aşağıdaki Gibi Sepolia Ağını Seçiyoruz. Create App diyoruz ve rpc'yi oluşturuyoruz.

![Ekran görüntüsü 2023-09-29 224039](https://github.com/tuncgs52/Takio-Testnet/assets/80161670/830bb4bf-d97e-4661-9cb5-4396fe76f222)

"Apı Key" basın. Rpc Bilgileri Gözükecek.
![Ekran görüntüsü 2023-09-29 233801](https://github.com/tuncgs52/Takio-Testnet/assets/80161670/fbca28e8-23e9-47c8-b89a-138971c96c15)



# Sunucumuzda Düzenleyeceğimiz Yerlere Gelelim.
İlk önce klasörün içine giriyoruz.

```
cd simple-taiko-node
```

```
nano .env
```
1-) İlk Yere Alchemydeki "RPC" Bilgilerimizi giriyoruz.
![Ekran görüntüsü 2023-09-29 231647](https://github.com/tuncgs52/Takio-Testnet/assets/80161670/2661a09c-8ddd-41ee-a2a1-6bcffbc378fe)

"L1_ENDPOINT_HTTP" Yazan Yere SS'teki Linki Kopyalayarak Giriyoruz.
![Ekran görüntüsü 2023-09-29 231436](https://github.com/tuncgs52/Takio-Testnet/assets/80161670/e160c67d-d49d-48cb-84b9-f2aa2e11ae6b)

"L1_ENDPOINT_WS" Bu kısmada Alttaki SS Linkini Kopyalayarak Giriyoruz.
![Ekran görüntüsü 2023-09-29 232234](https://github.com/tuncgs52/Takio-Testnet/assets/80161670/a28b9342-2c34-4a51-80d6-4cfa020a6548)

2-) "ENABLE_PROVER=false" Burayı "true" Yapıyoruz.
![Ekran görüntüsü 2023-09-29 232703](https://github.com/tuncgs52/Takio-Testnet/assets/80161670/a7c9017b-72e2-494e-b67a-15d6c7f4964f)

3-) En Son deposit ettiğimiz taiko cüzdanın private keyini "L1_PROVER_PRIVATE_KEY=" alanına giriyoruz.
![Ekran görüntüsü 2023-09-29 233033](https://github.com/tuncgs52/Takio-Testnet/assets/80161670/1ceb3e76-9d12-4030-af97-726e8d0607a8)

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


