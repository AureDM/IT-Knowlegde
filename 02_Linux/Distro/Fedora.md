## Nettoyage Fedora après Fresh Install
---
#### **Paramétrage de DNF (Fedora)**

- **Affiner le paramétrage de DNF**
  ```bash
  sudo nano /etc/dnf/dnf.conf
  ```
  Ajouter les lignes suivantes :
  ```ini
  fastestmirror=true  # Détection des miroirs les plus rapides
  max_parallel_downloads=10  # Téléchargement de 10 paquets en parallèle
  countme=false  # Désactiver les requêtes de comptage envoyées à Fedora
  ```
  *Un miroir est un serveur qui héberge une copie des packages logiciels, des mises à jour et des fichiers nécessaires pour Fedora.*

---
#### **Mise à jour du système**

- Nettoyer les fichiers résiduels
  ```bash
  sudo dnf clean all
  ```

---
#### **Mise à jour des firmwares *(pas faire si VM)***

  ```bash
  sudo fwupdmgr refresh  # Rafraîchir la base de données
  sudo fwupdmgr update   # Mettre à jour les micro-logiciels
  ```

---
#### **Installation des dépôts RPM Fusion**

*Dépôt tiers pour Fedora/RHEL, fournissant des logiciels libres et non-libres (codecs, pilotes, logiciels propriétaires).*

- **Installer le dépôt Free (logiciels libres)**
  ```bash
  sudo dnf install --nogpgcheck https://download1.rpmfusion.org/free/fedora/rpmfusion-free-release-$(rpm -E %fedora).noarch.rpm
  ```

- **Installer le dépôt Non-Free (logiciels non-libres)**
  ```bash
  sudo dnf install --nogpgcheck https://download1.rpmfusion.org/nonfree/fedora/rpmfusion-nonfree-release-$(rpm -E %fedora).noarch.rpm
  ```

- **Mettre à jour le système**
  ```bash
  sudo dnf upgrade
  ```

- **Activer les applications graphiques dans GNOME Logiciels** *(ex: VLC)*
  ```bash
  sudo dnf install rpmfusion-free-appstream-data rpmfusion-nonfree-appstream-data
  ```

---
#### **Installation des codecs multimédias**

```bash
sudo dnf install gstreamer1-plugins-{base,good,bad-free,good-extras,bad-free-extras,ugly-free,bad-freeworld,ugly}
```

---
#### **Activer l'accélération vidéo**

```bash
sudo dnf swap mesa-va-drivers mesa-va-drivers-freeworld  
sudo dnf swap mesa-vdpau-drivers mesa-vdpau-drivers-freeworld
```
*swap : permet de désinstaller le 1e paquet pour installer le 2e*

---
#### **Personnalisation de GNOME**

- **Installer GNOME Tweaks** *(pour personnaliser l'environnement GNOME)*
  ```bash
  sudo dnf install gnome-tweaks
  ```

- **Installer le gestionnaire d'extensions et quelques extensions utiles**
  ```bash
  sudo dnf install gnome-extensions-app gnome-shell-extension-dash-to-dock gnome-shell-extension-appindicator
  ```
