**URL pour installer/gérer les extensions : [ICI](https://extensions.gnome.org/)**

**Pré-requis :**
- Posséder l'extension navigateur : "Intégration à GNOME Shell"
- Posséder le paquet :
```bash
sudo apt install chrome-gnome-shell
```


| Extensions                                   | Descriptif                                                                                                                                          |
| -------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------- |
| AppIndicator and KStatusNotifierItem Support | Permet d'avoir les applications en cours d'execution dans la barre en haut à droite<br>https://github.com/ubuntu/gnome-shell-extension-appindicator |
| Dash to Dock                                 | Gérer le dock des applications<br>https://micheleg.github.io/dash-to-dock/                                                                          |
| Logo Menu                                    | Avoir le Logo en haut à gauche avec le menu<br>https://github.com/Aryan20/Logomenu                                                                  |
| Linuxtricks-monitor-indicator                | Permet d'avoir les informations de CPU, Mem, Swap, Load<br>https://github.com/aaaaadrien/linuxtricks-monitor-indicator                              |
| Quick Settings Audio Panel                   | Create a new panel containing volumes and media control in the quick settings<br>https://github.com/Rayzeq/quick-settings-audio-panel               |


##### Erreur connue : 
```html
Although GNOME Shell integration extension is running, native host connector is not detected. Refer [documentation](https://gnome.pages.gitlab.gnome.org/gnome-browser-integration/pages/installation-guide.html) for instructions about installing connector.
```

##### Solution :
- Vérifier que votre navigateur (Brave par exemple) <u> ne soit pas installé</u>  via snap mais via apt :
```bash
aurelien@aurelien-Legion:~$ which brave 
/snap/bin/brave
```
- Installé votre navigateur avec un package apt !