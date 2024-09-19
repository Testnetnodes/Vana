

<h1 align="center"> Vana </h1>

![Testnetnodes](https://github.com/Testnetnodes/Crossfi-/assets/115115403/967ab38c-faf5-4fbe-9e84-3323da53d6e6)

 * [Topluluk Twitter](https://twitter.com/testnetnodes)<br>
 * [Vana Website](https://www.vana.org)<br>
 * [Discord](https://discord.gg/YxW8aVh9)<br>
 * [Twitter](https://x.com/withvana)<br>
 * [Explorer](https://satori.vanascan.io)<br>


 ## 💻 Sistem Gereksinimleri
| Bileşenler | Minimum Gereksinimler | 
| ------------ | ------------ |
| CPU |	2 Cores |
| RAM	| 4+ GB |
| Storage	| 50++ GB SSD |
| Ubuntu 22.04 |

### 🚧 Sistem Paketlerini Güncelleme ve Yükseltme
```
sudo apt update && sudo apt upgrade -y
```

### 💻 Gerekli Paketleri Yükleme
```
sudo apt install -y curl gnupg
```

### 💻 Node.js ve npm Kurulumu
```
curl -fsSL https://deb.nodesource.com/setup_18.x | sudo -E bash -
sudo apt install -y nodejs
```

### 💻 Npm'yi güncelleyelim
```
sudo npm install -g npm@10.8.3
```

### 💻 Reponun Klonlanması
```
git clone https://github.com/vana-com/vana-dlp-chatgpt.git
cd vana-dlp-chatgpt
```

### 💻 Python 3.11 ile Poetry Kurulumu
```
sudo add-apt-repository ppa:deadsnakes/ppa
sudo apt update
sudo apt install python3.11 python3.11-venv python3.11-dev
```

### 💻 Python 3.11 ile Poetry'yi kullan
```
poetry env use python3.11
poetry install
poetry run python --version
poetry check
poetry --version
```
![image](https://github.com/user-attachments/assets/15e718d2-c696-4dd2-be12-555921c2e955)

### 💻 .env Dosyasının Düzenlenmesi

```
cp .env.example .env
nano .env
```

```
# The network to use, currently Vana Satori testnet
OD_CHAIN_NETWORK=satori
OD_CHAIN_NETWORK_ENDPOINT=https://rpc.satori.vana.org

# Optional: OpenAI API key for additional data quality check
OPENAI_API_KEY="sk-nXXXXX"

# Optional: Your own DLP smart contract address once deployed to the network, useful for local testing
DLP_CONTRACT_ADDRESS=0xa0519f5ADc4e82729b21Ef1586d397260D9B9E45
DLP_MOKSHA_CONTRACT=0xee4e3Fd107BE4097718B8aACFA3a8d2d9349C9a5
DLP_SATORI_CONTRACT=0xa0519f5ADc4e82729b21Ef1586d397260D9B9E45

# Optional: Your own DLP token contract address once deployed to the network, useful for local testing
DLP_TOKEN_VANA_CONTRACT=0x3db29b7ED68Ca561794039B4D675f68fb64D6ac3
DLP_TOKEN_MOKSHA_CONTRACT=0xF1925473bA6aa147EeB2529197C2704454D66b43
DLP_TOKEN_SATORI_CONTRACT=0x3db29b7ED68Ca561794039B4D675f68fb64D6ac3

# The private key for the DLP, follow "Generate validator encryption keys" section in the README
PRIVATE_FILE_ENCRYPTION_PUBLIC_KEY_BASE64=XXXXX
```

### 💻 Vana CLI Kurulumu
```
pip install vana
```
![image](https://github.com/user-attachments/assets/3fd43a47-58a0-4b57-b196-2af62aaefb25)

### 💻 Paket Hatası Verirse Kodu Yazıyoruz !!
```
sudo apt --fix-broken install
sudo apt update
sudo apt upgrade
```

### 💻 Bozuk paketler düzeltildikten sonra, python3.12-venv paketini yüklüyoruz
```
sudo apt install python3.12-venv
```

### 💻 Sanal Ortam Oluşturun ve Etkinleştirin
```
apt install python3.12-venv
python3 -m venv venv
source venv/bin/activate
```

### 💻 Sanal ortam etkinleştirildikten sonra Vana'yı yükleyin
```
pip install vana
```
Bu koddan sonra biraz bekliyoruz.. ( pip install vana )

![image](https://github.com/user-attachments/assets/e90cc0ac-cf87-4bb6-a344-360a6290f7e3)


### 💻 Cüzdan Oluşturma ve Anahtar Yönetimi ( Hiçbiryeri Değiştirmiyoruz,ben değiştirmediğim için kodları ona göre yazdım karar sizin )
```
vanacli wallet create --wallet.name default --wallet.hotkey default
```
Kodu girdikten sonra şifremizi belirliyoruz unutmayın.Bize cold key ve hot key bilgilerini verecek
Anımsatıcı ifadeleri güvenli bir şekilde saklayın ; cüzdanınızı kurtarmak için bunlara ihtiyacınız olacak !!

![image](https://github.com/user-attachments/assets/d5b45dca-60ff-4e64-b811-c225f58d974a)

### 💻 MetaMask'a Satori Testnet Ağını ekleyin

- Network Name: Satori Testnet
- RPC URL: https://rpc.satori.vana.org
- Chain ID: 14801
- Currency: VANA
- Explorer: https://satori.vanascan.io/

![image](https://github.com/user-attachments/assets/7e273088-5a86-4c03-9a73-69d1cd1f301f)

### 💻 Cüzdanlarımızın Private Keylerini Alıyoruz ( Coldkey / Hotkey )
```
vanacli wallet export_private_key
```

Kodu girdikten sonra,wallet name yazan yeri enterla geçiyoruz.Key type yerine coldkey yazıyoruz enter'a basıyoruz.Daha sonra yes diyoruz enter'a basıyoruz.Son olarakda yukarıda cüzdan oluştururken kullandığımız şifreyi yazıp Enter'a basıyoruz.Çıkan yedekleri kaydetmeyi unutmayın !

Enter wallet name (default):
Enter key type [coldkey/hotkey] (coldkey):coldkey
Enter your coldkey password:
Your coldkey private key:

![image](https://github.com/user-attachments/assets/6fe64fb1-0639-4c32-ad21-11238b644a42)

```
vanacli wallet export_private_key
```

Kodu girdikten sonra,wallet name yazan yeri enterla geçiyoruz.Key type yerine hotkey yazıyoruz enter'a basıyoruz.Daha sonra yes diyoruz enter'a basıyoruz.Son olarakda yukarıda cüzdan oluştururken kullandığımız şifreyi yazıp Enter'a basıyoruz.Çıkan yedekleri kaydetmeyi unutmayın !

Enter wallet name (default):
Enter key type [coldkey/hotkey] (coldkey):hotkey
Enter your coldkey password:
Your coldkey private key:

![image](https://github.com/user-attachments/assets/3ba60a7b-56c5-46ec-b081-9de0f67f3ec9)

Coldkey : Şahıs tarafından yönetilen işlemler için (örneğin, stake etme). 
Hotkey : Doğrulayıcı tarafından yönetilen işlemler için (örneğin, puan gönderme).

🚧 Privatesini Aldığımız 2 cüzdanıda ( hotkey-coldkey ) metamaskımıza import ediyoruz.

🚧 Cüzdanları import ettikten sonra,2 cüzdanımızada aşağıdaki linke girip test token istiyoruz

https://faucet.vana.org

Not: Musluk günde bir kez kullanılabilir.

![image](https://github.com/user-attachments/assets/1d50175c-ce76-46ec-8cb7-aef9832a8d4f)

### 💻 DLP oluşturuyoruz
```
./keygen.sh
```
Kodu girdikten sonra,ilk olarak moniker adımızı daha sonra mail adresimizi yazıyoruz.Son olarak 3.kısımda 0'a basıp enter ile devam ediyoruz.

![image](https://github.com/user-attachments/assets/781db9a7-2fc1-458c-85f4-15b83f93b608)

### 💻 DLP Akıllı Sözleşme deposunu klonlayın
```
cd
git clone https://github.com/vana-com/vana-dlp-smart-contracts.git
cd vana-dlp-smart-contracts
```

### 💻 Bağımlılıkları yükleyelim
```
curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -
echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list
nvm install 18.8.0 && nvm use 18.8.0
npm install -g yarn
yarn --version
yarn install
npm install --save-dev hardhat
cat ~/.vana/wallets/default/hotkeys/default
```

🚧 Son komuttan sonra (cat) çıktıyı kaydetmeyi unutmayın !!!!

Şimdi ise Nano içini kendi bilgilerimize göre düzenleyeceğiz
```
nano .env
```

Orjinal Hali
```
DEPLOYER_PRIVATE_KEY=0x... (your coldkey private key)
OWNER_ADDRESS=0x... (your coldkey address)
SATORI_RPC_URL=https://rpc.satori.vana.org
DLP_NAME=... (your DLP name)
DLP_TOKEN_NAME=... (your DLP token name)
DLP_TOKEN_SYMBOL=... (your DLP token symbol)
```

Düzenlenmiş Hali
```
DEPLOYER_PRIVATE_KEY=0x0a8f9aa4a265ecfa1......bb49b2dd9ebbdb       ( Coldkey Private Keyinizi Yazıyorsunuz )
OWNER_ADDRESS=0xF7044371218AEBa5....63916bA418                     ( Coldkey Cüzdan Adresinizi Yazıyorsunuz )
SATORI_RPC_URL=https://rpc.satori.vana.org
DLP_NAME=testnetnodes                                              ( Yukarda Oluşturduğunuz Moniker Adınız )
DLP_TOKEN_NAME=testnetnodes                                        ( Oluşturmak istediğiniz Token Adı )
DLP_TOKEN_SYMBOL=tstnds                                            ( Oluşturduğunuz Tokenini Sembolü )
```

![image](https://github.com/user-attachments/assets/9aa7fd21-b95f-4139-8939-81709f9cf888)

Bilgilerinizi düzenledikten sonra CTRL+X+Y ile kaydedip çıkıyorsunuz.

### 💻 Deploy Contrats
```
npx hardhat deploy --network satori --tags DLPDeploy
```

🚧 Eğer bu şekil bi hata alırsanız,alttaki çözüm yolunu deneyin

![image](https://github.com/user-attachments/assets/26f8e4be-1785-4fe0-b862-2f6d1e53b8b5)

```
nvm use 18.8.0
yarn install
apt update
npx hardhat deploy --network satori --tags DLPDeploy
```

🚧 DataLiquidityPoolToken deployed ve DataLiquidityPool çıktısını kaydetmeyi unutmayın.

![image](https://github.com/user-attachments/assets/b368bbfe-f7b9-4021-a43e-5a5f44f52a58)

Sayfanın en üstünde bulunan explorer'a gidip deploy çıktılarını aratın,eğerki success diyorsa olmuştur

![image](https://github.com/user-attachments/assets/79eb7a97-2e39-4788-87ff-016c43825d0a)


### 💻 Validatör Oluşturma
```
cd
cd vana-dlp-chatgpt
cat public_key_base64.asc
```

🚧 Son komutu girince çok uzun bi çıktı verecek,kaydetmeyi unutmayın.Az sonra lazım olacak

![image](https://github.com/user-attachments/assets/9416b6a2-25f4-4322-8af4-238889ef18e1)

```
nano .env
```

🚧 Nano'nun içinde yukarıda belirttiğim 5 yeri değiştireceğiz..

![image](https://github.com/user-attachments/assets/9b278992-66e8-48bb-868a-2ff00352556c)

DLP_CONTRACT_ADDRESS=0xaYOURDLPADDRESS
DLP_SATORI_CONTRACT=0xaYOURDLPADDRESS
DLP_TOKEN_VANA_CONTRACT=0x6381YOURDLPTOKEN-ADDRESS
DLP_TOKEN_SATORI_CONTRACT=0x6381YOURDLPTOKEN-ADDRESS
PRIVATE_FILE_ENCRYPTION_PUBLIC_KEY_BASE64=YOUR PUBLIC_KEYBASE64

DLP_CONTRACT_ADDRESS=0xaYOURDLPADDRESS        ( Buraya Token Deploy Ederken Aldığımız Yedeklerden DataLiquidityPool çıktısını yazacağız )
DLP_SATORI_CONTRACT=0xaYOURDLPADDRESS         ( Buraya Token Deploy Ederken Aldığımız Yedeklerden DataLiquidityPool çıktısını yazacağız )

DLP_TOKEN_VANA_CONTRACT=0x6381YOURDLPTOKEN-ADDRESS          ( Buraya Token Deploy Ederken Aldığımız Yedeklerden DataLiquidityPoolToken çıktısını yazacağız )
DLP_TOKEN_SATORI_CONTRACT=0x6381YOURDLPTOKEN-ADDRESS        ( Buraya Token Deploy Ederken Aldığımız Yedeklerden DataLiquidityPoolToken çıktısını yazacağız )

PRIVATE_FILE_ENCRYPTION_PUBLIC_KEY_BASE64=   ( Buraya yukarıda cat public_key_base64.asc komutuyla almış olduğumuz çıktının tamamını yazacağız.Dikkat edin çok uzun eksik yapıştırmayın )

🚧  Daha sonrasında ise CTRL+X+Y ile kaydedip çıkıyoruz.

### 💻 Token Transferi yapıyoruz

🚧🚧 ÇOK ÇOK ÖNEMLİ BURAYI ATLAMAYIN SAKIN :)

Çıktıdaki transaction adresini tarayıcımıza yapıştırıyoruz ( Benimkisi Bu Mesela : https://satori.vanascan.io/tx/0x0dc847a30c2df14bcc6f345024b5f6255c90f14b243f73df631951c25d1ffa46 )
Resimde belirttiğim gibi token adımıza tıklıyoruz,benimkisi tstnds
Açılan sayfada ise ikinci resimde belirttiğim gibi Metamask işaretine basıp token kontratını Metamaskımıza ekliyoruz

![image](https://github.com/user-attachments/assets/ce3cd8bd-2d97-41df-acbf-df9bf47e87dd)

![image](https://github.com/user-attachments/assets/2b1aaa7b-32a6-41b2-bc3f-1a0b935ca02a)

Daha sonra Cold Wallet adresimizden 11 adet ( Oluşturduğumuz Tokenden ) ( tstnds ) 11 adet Hot Wallet adresimize gönderiyoruz.

### 💻 Validatörümüzü aktif hale getiriyoruz
```
./vanacli dlp register_validator --stake_amount 10
```
Şifre hariç 1. ve 2.adımı enterla geçiyoruz

![image](https://github.com/user-attachments/assets/82525523-c670-477a-9c17-d65f4b33e452)

Bu şekilde bi çıktı aldıysanız herşey yolunda demek :) Transaction a bakın succesfull diyorsa işlemlere devam ediyoruz.Çok az kaldı dayananın !!!

![image](https://github.com/user-attachments/assets/12b23307-7d1f-4fca-a365-28ee2c77f24d)

2024-09-19 00:51:07.180 |       INFO       |  - View transaction on block explorer: https://satori.vanascan.io/tx/0x0dc847a30c2df14bcc6f345024b5f6255c90f14b243f73df631951c25d1ffa46 -
2024-09-19 00:51:07.180 |       INFO       |  - Registered validator 0x5DfCCaa3515619a53cE5a11CD5e2168A577eD580 with owner 0xF7044371218AEBa5EdE1502cA9652e63916bA418 and staked 10.0 DLPTokens

```
./vanacli dlp approve_validator --validator_address=<your hotkey address from MetaMask>              
```

ÖRN : 
./vanacli dlp approve_validator --validator_address=0x5DfCCaa3515619a53cE5a11CD5e2168A577eD580    ( Hotkey Cüzdanınızın Adresini Yazıyorsunuz )

### 💻 Herşey Hazır Son Rütuşlar :)
```
screen -S vana
poetry run python -m chatgpt.nodes.validator
```

Çıkan çıktı aşağıdaki gibiyse işlem tamam elinize sağlık :) Forklamayı unutmayın

![image](https://github.com/user-attachments/assets/7561c2ac-ad6e-4ff2-84fe-ac3c387b4db4)
























































