# ☁️ Beedercloud Panel

██████╗ ███████╗███████╗██████╗ ███████╗██████╗ 
██╔══██╗██╔════╝██╔════╝██╔══██╗██╔════╝██╔══██╗
██████╔╝█████╗  █████╗  ██║  ██║█████╗  ██████╔╝
██╔══██╗██╔══╝  ██╔══╝  ██║  ██║██╔══╝  ██╔══██╗
██████╔╝███████╗███████╗██████╔╝███████╗██║  ██║
╚═════╝ ╚══════╝╚══════╝╚═════╝ ╚══════╝╚═╝  ╚═╝
              B E E D E R C L O U D

---

## 🚀 Giới thiệu

**Beedercloud** là nền tảng quản lý máy chủ & game server tối ưu,  
hoạt động tốt trên **VPS không cần IPv4**, hỗ trợ:

- IPv6 native
- Cloudflare Tunnel / ngrok / cloudflared
- Bảo mật cao – dễ mở rộng
- Tối ưu cho Game Server & Bot

---

## 🐦 Cài đặt Pterodactyl Panel (Không cần IPv4)

> Yêu cầu: Ubuntu 20.04 / 22.04 / 24.04

## Cài Dash Helictyl v4
> Nếu cần cài dash : helictyl v14 link ()

### 1️⃣ Chuẩn bị hệ thống
```bash
apt update -y && apt upgrade -y
apt install curl sudo git -y

1️⃣ Cài Docker (nếu chưa có)
curl -fsSL https://get.docker.com | sh
systemctl enable --now docker

2️⃣ Cài Docker Compose v2 (plugin)
mkdir -p ~/.docker/cli-plugins
curl -SL https://github.com/docker/compose/releases/latest/download/docker-compose-linux-x86_64 \
-o ~/.docker/cli-plugins/docker-compose
chmod +x ~/.docker/cli-plugins/docker-compose

3️⃣ Kiểm tra
docker compose version

Lệnh cài 
# Cài Cloudflare để lấy link 
get https://github.com/cloudflare/cloudflared/releases/latest/download/cloudflared-linux-amd64 -O cloudflared


chmod +x cloudflared

sudo mv cloudflared /usr/local/bin/

nohup cloudflared tunnel --url http://localhost:80 > cloudflared.log 2>&1 &

cat cloudflared.log

nếu lỗi link không vào được chạy (BETA)


# Panel cài đặt #
bash <(curl -s https://raw.githubusercontent.com/trockboppro/pterodactyl/refs/heads/main/panel)
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# Wings #
sudo su
bash <(curl -s https://raw.githubusercontent.com/trockboppro/pterodactyl/refs/heads/main/wings)

-----------------------------------------
cd pterodactyl
------------------------------------------
sudo su
------------------------------------------
nano /etc/pterodactyl/config.yml
------------------------------------------
pass vô config , config node của bạn
------------------------------------------
cd wings
------------------------------------------
docker-compose up -d --force-recreate


