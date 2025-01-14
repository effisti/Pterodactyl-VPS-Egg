<div align="center">

# CristalCloud VPS

[![License](https://img.shields.io/github/license/ysdragon/Pterodactyl-VPS-Egg)](https://github.com/ysdragon/Pterodactyl-VPS-Egg/blob/main/LICENSE)
[![CodeFactor](https://www.codefactor.io/repository/github/ysdragon/pterodactyl-vps-egg/badge)](https://www.codefactor.io/repository/github/ysdragon/pterodactyl-vps-egg)

Een krachtig en lichtgewicht Virtual Private Server (VPS) egg voor Pterodactyl Panel, dat meerdere architecturen en besturingssystemen ondersteunt.
</div>

## ✨ Functies

- 🚀 Eenvoudige implementatie en beheer
- 🔧 Aanpasbare configuraties
- 🔄 Ondersteuning voor meerdere architectuur
- 🖥️ Ruim aanbod aan besturingssystemen
- 🔌 Ondersteuning voor meerdere poorten (TCP/UDP)
   - Dynamische poorttoewijzing
- 🚀 Aangepaste SSH-server

## 🏗️ Ondersteunde architecturen

| Architectuur | Staat | Opmerkingen |
|------------|--------|-------|
| amd64 | ✅ Volledige ondersteuning | Aanbevolen voor de meeste gebruikers |
| arm64 | ✅ Volledige ondersteuning | Ideaal voor ARM-gebaseerde servers |
| riscv64 | ⚠️Beperkte ondersteuning | Vereist aangepaste rootfs-images |

> [!BELANGRIJK]
> Voor de `riscv64`-architectuur moet u uw eigen rootfs-images leveren of hosten. Momenteel biedt alleen Chimera Linux native ondersteuning voor riscv64 in deze egg.

## <img width="20" height="20" src="https://www.kernel.org/theme/images/logos/favicon.png" /> Available Linux Distributions

### Enterprise Linux
- <img width="16" height="16" src="https://rockylinux.org/favicon.png" /> Rocky Linux
- <img width="16" height="16" src="https://almalinux.org/fav/favicon.ico" /> AlmaLinux
- <img width="16" height="16" src="https://www.centos.org/assets/img/favicon.png" /> CentOS
- <img width="16" height="16" src="https://www.oracle.com/asset/web/favicons/favicon-32.png" /> Oracle Linux

### Debian-based
- <img width="16" height="16" src="https://netplan.readthedocs.io/en/latest/_static/favicon.png" /> Ubuntu
- <img width="16" height="16" src="https://www.debian.org/favicon.ico" /> Debian
- <img width="16" height="16" src="https://github.com/bin456789/reinstall/assets/7548515/f74b3d5b-085f-4df3-bcc9-8a9bd80bb16d" /> Kali Linux
- <img width="16" height="16" src="https://www.devuan.org/ui/img/favicon.ico" /> Devuan Linux

### Other Distributions
- <img width="16" height="16" src="https://www.alpinelinux.org/alpine-logo.ico" /> Alpine Linux
- <img width="16" height="16" src="https://archlinux.org/static/favicon.png" /> Arch Linux
- <img width="16" height="16" src="https://www.gentoo.org/assets/img/logo/gentoo-g.png" /> Gentoo Linux
- <img width="16" height="16" src="https://voidlinux.org/assets/img/favicon.png" /> Void Linux
- <img width="16" height="16" src="http://www.slackware.com/favicon.ico" /> Slackware Linux
- <img width="16" height="16" src="https://static.opensuse.org/favicon.ico" /> openSUSE
- <img width="16" height="16" src="https://fedoraproject.org/favicon.ico" /> Fedora
- <img width="16" height="16" src="https://chimera-linux.org/assets/icons/favicon48.png" /> Chimera Linux
- <img width="16" height="16" src="https://djeqr6to3dedg.cloudfront.net/repo-logos/library/amazonlinux/live/logo-1720462149317.png" /> Amazon Linux
- <img width="16" height="16" src="https://www.plamolinux.org/images/garland_logo.jpg" /> Plamo Linux
- <img width="16" height="16" src="https://linuxmint.com/web/img/favicon.ico" /> Linux Mint
- <img width="16" height="16" src="https://en.altlinux.org/favicon.svg" /> Alt Linux
- <img width="16" height="16" src="https://www.openeuler.org/favicon.ico" /> openEuler

## 🚀 Snelle start

1. **Download de egg**
   - Download het configuratiebestand `egg-vps.json` naar uw lokale machine.
2. **Importeren naar Pterodactyl**
   - Navigeer naar het beheerdersdashboard
   - Ga naar Nest > Import Egg
   - Upload het `egg-vps.json`-bestand
   - Configureer indien nodig

3. **Implementeer uw VPS**
   - Maak een nieuwe server met behulp van het VPS-Egg
   - Configureer bronnen
   - Start uw exemplaar

## Hoe SSH gebruiken?

#### Installeer de aangepaste SSH-server:
   - Na het installeren van de gewenste distro gebruikt u het commando `install-ssh` om onze aangepaste SSH-server te installeren.

#### Configuratieopties

Het configuratiebestand bevindt zich op `/.ssh_config` en ondersteunt de volgende opties:

- `SSH_PORT`: De poort waarop de SSH-server zal luisteren. De standaardwaarde is `2222`.
- `SSH_USER`: De gebruikersnaam voor SSH-authenticatie.
- `SSH_PASSWORD`: Het wachtwoord voor SSH-authenticatie.
- `SSH_TIMEOUT`: De time-outduur in seconden voor SSH-verbindingen. Laat het leeg of stel het in op `0` om de time-out uit te schakelen.
- `SFTP_ENABLE`: SFTP in- of uitschakelen. Stel in op 'true' om SFTP in te schakelen.

#### Voorbeeld `/.ssh_config` Configuratie

Hier is een voorbeeldconfiguratiebestand:

```ini
SSH_PORT=50000
SSH_USER=user
SSH_PASSWORD=123123
SSH_TIMEOUT=0
SFTP_ENABLE=true
```

## Bijdragen

Bijdragen zijn welkom. Als u suggesties, verbeteringen of bugfixes heeft, kunt u een pull-verzoek indienen.

## Licentie
Dit project is open-source en beschikbaar onder de MIT-licentie. Zie de [LICENTIE](https://github.com/effisti/Pterodactyl-VPS-Egg/blob/main/LICENSE) bestand voor meer details.
