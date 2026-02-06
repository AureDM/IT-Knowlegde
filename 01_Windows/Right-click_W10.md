# Retrouver le menu clic droit de Windows 10
Permet d'éviter de cloquer à chaque fois sur "Afficher + d'options"

Doc : [ICI](https://www.01net.com/astuces/windows-11-comment-retrouver-lancien-menu-contextuel-du-clic-droit.html)

- Ouvrir un cmd admin
- Taper la commande suivante :
```powershell
reg add “HKCU\Software\Classes\CLSID{86ca1aa0-34aa-4e8b-a509-50c905bae2a2}\inprocServer32” /f /ve
```
