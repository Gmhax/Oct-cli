# Oct-cli
# Step by step how to be great!!!!

## FULL FLOW: Octra WebCLI + WireGuard VPN + Wallet
1. Clone the repository
```
git clone https://github.com/octra-labs/webcli.git
cd webcli
```

2. Install dependencies
```
sudo apt update && sudo apt upgrade -y

sudo apt install -y \
wireguard \
wireguard-tools \
libssl-dev \
make \
g++ \
build-essential \
git
```

3. Setup VPN (Proton WireGuard)
- Step A: Download .conf gikan Proton VPN
- Register: [https://account.protonvpn.com](https://account.protonvpn.com/downloads)
- Use free
- Go to WireGuard config generator
- Follow this guide below
<img width="1062" height="591" alt="image" src="https://github.com/user-attachments/assets/5ccaf217-03a2-46d3-9871-a62b5f3bea65" />

- Save the format. 



4. Create config file
```
nano wg0.conf
```
- Paste Proton WireGuard config
- Don’t need DNS in Linux setup, disable it using #

## Move config to WireGuard folder
```
sudo mkdir -p /etc/wireguard
sudo mv wg0.conf /etc/wireguard/
sudo chmod 600 /etc/wireguard/wg0.conf
```
- Start VPN
```
sudo wg-quick up wg0
sudo wg
```

5. Execute:
```
chmod +x setup.sh
./setup.sh
./octra_wallet
```













