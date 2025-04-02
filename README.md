<p align="center">
  <img height="100" height="auto" src="https://github.com/user-attachments/assets/aa5c6cd4-6806-4f29-bb68-3508b10f75b5">
</p>

# Dria Testnet

Official documentation:
>- [Validator setup instructions](https://docs.dria.co/)

Explorer:
>- [Explorer](https://dria.co/edge-ai/my-node)

### Minimum Hardware Requirements
 - 4x CPUs; the faster clock speed the better
 - 16GB RAM
 - 500GB of storage (SSD or NVME)

### Recommended Hardware Requirements 
 - 8x CPUs; the faster clock speed the better
 - 32GB RAM
 - 1TB of storage (SSD or NVME)

 - Ubuntu 22.04

Устанавливаем ноду:

``sudo apt update & sudo apt upgrade -y``

``sudo apt install curl iptables build-essential git wget lz4 jq make gcc nano automake autoconf tmux htop nvme-cli pkg-config libssl-dev libleveldb-dev tar clang bsdmainutils ncdu unzip libleveldb-dev git-all protobuf-compiler screen -y``

``for pkg in docker.io docker-doc docker-compose podman-docker containerd runc; do sudo apt-get remove $pkg; done``

``sudo apt-get install ca-certificates curl gnupg``

``sudo install -m 0755 -d /etc/apt/keyrings``

``curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg``

``sudo chmod a+r /etc/apt/keyrings/docker.gpg``

``echo \
  "deb [arch="$(dpkg --print-architecture)" signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
  "$(. /etc/os-release && echo "$VERSION_CODENAME")" stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null``

``apt install docker.io -y``

``sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin``

``curl -fsSL https://ollama.com/install.sh | sh``

``curl -fsSL https://dria.co/launcher | bash``

``wget https://raw.githubusercontent.com/firstbatchxyz/dkn-compute-node/master/.env.example``

``cp .env.example .env``

``mv .env /root/.dria/bin/``

``screen -S dria``

``cd .dria/bin``

``./dkn-compute-launcher start``

Выбираем Gemini и нажимает Enter

![Termius_ZpDBTVN69i](https://github.com/user-attachments/assets/a8e86bc4-bf56-4ea0-a8d2-6f1d4598fad2)

Чтобы выбрать все модули нажимаем одновременно стрелки влево и вправо <> и Enter. Либо проходитесь по каждому модулю и нажимаете Space чтобы выбрать, далее Enter.

![Termius_A1O8AKqDLl](https://github.com/user-attachments/assets/01feedeb-91fe-439c-8459-7a9cb982689e)

Далее стрелкой вниз выбираем "Go back" и нажимаем Enter.

![Termius_XPhwjAPZXn](https://github.com/user-attachments/assets/14712fea-048b-4484-ae5d-506b98551a3c)

Вставляем свой приватный ключ от кошелька и Enter. Рекомендую создать новый кошелек в целях безопасности.

![Termius_l8lb8VwESi](https://github.com/user-attachments/assets/e77d5048-8f8a-4f15-b7e7-9981a75ef196)

Чтобы модули работали нам нужен API. Переходим на сайт - https://aistudio.google.com/app/apikey Нажимаем "Create API key", копируем его и далее будем редактировать конфиг.

``./dkn-compute-launcher settings``

Выбираем API Keys и нажимаем Enter.

![Termius_sOYo3nahT6](https://github.com/user-attachments/assets/a40f3dc3-e0ec-40a1-8799-7c5744f98bf2)

Далее ищем GEMINI_API_KEY и нажимаем Enter. Вставляем свой API ключ, который скопировали ранее, нажимаем Enter. Далее выходим через "Go back".

![Termius_jfe0tfVHLg](https://github.com/user-attachments/assets/b491995e-fde3-4eb7-8904-9682b999e779)

Сохраняем конфиг "Save & Exit" и нажимаем Enter.

![Termius_wlO9WYMXNQ](https://github.com/user-attachments/assets/216fda0d-ad6c-4a9e-85ee-1afad7d0a8cf)

Чтобы получать на % больше поинтов можете ввести реф. код - m3qEkDpDRljw5vUmuKZr

``./dkn-compute-launcher referrals``

Выбираем "Enter referral code to be referred"

![Termius_I9EZVyv60S](https://github.com/user-attachments/assets/da395ebf-b803-4450-b5b4-cca2b7d8848c)

Вставляем код m3qEkDpDRljw5vUmuKZr и Enter. Выходим через "Go back".

![Termius_nS3enxaOdJ](https://github.com/user-attachments/assets/1031db03-8497-4cda-8d7d-65016cf07e4c)

Запускаем ноду

``./dkn-compute-launcher start``

Выйти из скрина CTRL + A + D

Зайти обратно в скрин:

``screen -r dria``

Для отслеживания статистики переходим на сайт - https://dria.co/edge-ai/my-node Заходим через тот кошелек, который указывали в ноде. В разделе "My node" будет статистика по поинтам, ожидайте примерно 24ч после начнут капать поинты и выполняться задания. Чтобы забрать роль нодера в дискорде, заполните форму - https://form.typeform.com/to/Eav42hR3?typeform-source=www.google.com Но, перед заполнением зайдите в дискорд.
