# Installation de Windows

## Créer un compte Windows Local
Au moment de l’installation de Windows « créer un compte en ligne » :  
- Ouvrir un terminal avec "Shift + F10"
```powershell
start ms-cxh:localonly
```

## Fichier de réponse | autounattend.xml
Permet d'automatiser l'installation de Windows

URL pour générer un fichier de réponse : [ICI](https://schneegans.de/windows/unattend-generator/)

## Dual Boot - Syncro heure Windows/Linux
Commande linux permettant de syncroniser l’heure entre les 2 machines du dual boot sinon, Windows prend 2 heures de retard

- Sur Linux, ouvrir un terminal
```bash
timedatectl set-local-rtc 1 –adjust-system-clock
```

==> Forcer Linux à utiliser l'heure locale
==> Linux utilise le temps UTC alors que Windows utilise l'heure locale stocker dans le BIOS
