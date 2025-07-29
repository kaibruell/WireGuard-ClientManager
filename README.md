# WireGuard VPN mit ClientManager

WireGuard VPN-Server mit Docker und erweiterte Client-Verwaltung über Bash-Skripte.

## Setup

1. **Server starten**:
   ```bash
   docker-compose up -d
   ```

2. **In Container einsteigen**:
   ```bash
   docker exec -it wireguard bash
   ```

3. **ClientManager verwenden**:
   ```bash
   cd /ClientManager
   chmod +x wg-manager.sh
   ./wg-manager.sh help
   ```

## Befehle

```bash
# Alle Clients auflisten
./wg-manager.sh list-peers

# Client hinzufügen
./wg-manager.sh add-peer "client-name"

# Client entfernen
./wg-manager.sh remove-peer "client-name"

# Max. Clients setzen
./wg-manager.sh set-max-clients 10
```

## Konfiguration

- **Server IP**: 46.202.153.125:51820
- **VPN Netzwerk**: 10.13.13.0/24
- **Max Clients**: 5 (konfigurierbar)

Client-Configs unter: `/config/peer_<name>/`