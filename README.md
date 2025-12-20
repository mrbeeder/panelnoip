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
