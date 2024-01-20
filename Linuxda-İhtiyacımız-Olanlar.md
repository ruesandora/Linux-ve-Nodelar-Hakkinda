# Server-Starter
Serverda Lazım olan paketleri kurabilmek için repo, kısayol.
[KingsHarald](https://github.com/KingsHarald0) § [enzifiri](https://github.com/enzifiri)

### Gcc Install
```
sudo apt-get update && sudo apt-get upgrade -y
apt install curl iptables build-essential git wget jq make gcc nano tmux htop nvme-cli pkg-config libssl-dev libleveldb-dev tar clang bsdmainutils ncdu unzip libleveldb-dev -y
```

## NodeJS and NPM Install
```
curl -sL https://deb.nodesource.com/setup_20.x -o /tmp/nodesource_setup.sh
sudo bash /tmp/nodesource_setup.sh
sudo apt install nodejs
npm install -g npm@10.2.5
```
## Python 3.8 Pip, Python3 Install
```
sudo apt install -y python3-pip
sudo apt install pip
sudo apt install -y build-essential libssl-dev libffi-dev python3-dev
```

## Docker
```
sudo apt update -y && sudo apt upgrade -y
for pkg in docker.io docker-doc docker-compose podman-docker containerd runc; do sudo apt-get remove $pkg; done

sudo apt-get update
sudo apt-get install ca-certificates curl gnupg
sudo install -m 0755 -d /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
sudo chmod a+r /etc/apt/keyrings/docker.gpg

echo \
  "deb [arch="$(dpkg --print-architecture)" signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
  "$(. /etc/os-release && echo "$VERSION_CODENAME")" stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

sudo apt update -y && sudo apt upgrade -y

sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
sudo docker run hello-world
```

## Yarn
```
curl -sSL https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -
echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list
sudo apt-get update -y
sudo apt-get install yarn -y
```

## yarn install komutu error verirse
```
sudo apt remove cmdtest
sudo apt remove yarn
curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -
echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list
sudo apt-get update
sudo apt-get install yarn -y
```

# SİLME KOMUTLARI

## NODE JS SİLME KOMUTU
```
sudo apt remove nodejs
sudo apt purge nodejs
```
## Eğer node JS silinmezse şu komutları uygula
which node
which npm

sunucudan sunucuya değişir tüm klasörler için olan kodları atıyorum buraya
```
sudo rm /usr/local/bin/node
sudo rm /usr/local/bin/npm
sudo rm /usr/bin/node
sudo rm /usr/bin/npm
rm -rf ~/.nvm
rm /root/.nvm/versions/node/v16.20.2/bin/node
rm /root/.nvm/versions/node/v16.20.2/bin/npm
```


