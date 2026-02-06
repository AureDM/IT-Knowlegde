# Powershell

## Commandes Powershell

| Commande | Résultat |
| - | - |
| `powercfg /energy` | Analyse la consommation d’énergie et génère un rapport (problèmes liés à l’autonomie, performances, veille) |
| `powercfg /batteryreport` | Génère un rapport détaillé sur l’état et l’historique de la batterie (capacité, cycles, usure) |
| `chkdsk` | Vérifie et répare les erreurs du disque (système de fichiers, secteurs défectueux) |
| `sfc /scannow` | Analyse et répare les fichiers système Windows corrompus |
| `DISM /Online /Cleanup-Image /CheckHealth` | Vérifie rapidement si l’image système est endommagée |
| `DISM /Online /Cleanup-Image /ScanHealth` | Analyse plus en profondeur l’image Windows pour détecter des corruptions |
| `DISM /Online /Cleanup-Image /RestoreHealth` | Répare l’image système endommagée en téléchargeant des fichiers sains |
| `tasklist | findstr script` | Liste les processus actifs et filtre ceux contenant "script" |
| `taskkill /f /pid …` | Termine de force un processus en fonction de son PID |
| `netsh wlan show wlanreport` | Crée un rapport HTML complet sur les connexions Wi-Fi (qualité, erreurs, historique) |
| `netsh interface show interface` | Affiche l’état des interfaces réseau (activées, connectées, etc.) |
| `netsh interface ip show address | findstr "IP Address"` | Montre les adresses IP assignées aux interfaces réseau |
| `netsh advfirewall set allprofiles state off` | Désactive les pare-feux |
| `netstat -a -f` | Affiche toutes les connexions réseau actives + résolution des adresses en noms DNS |
| `netstat -o` | Liste les connexions réseau avec le PID du processus associé (utile pour identifier quel programme utilise un port) |
| `netstat -e -t 5` | Affiche les statistiques Ethernet toutes les 5 secondes |
| `route print` | Affiche les routes configurées |
| `shutdown /r /fw /f /t 0` | Redémarre immédiatement le PC (/r), force la fermeture des apps (/f), et ouvre le firmware/BIOS UEFI au redémarrage (/fw) |
| `PowerShell -ExecutionPolicy Unrestricted -File "chemin\vers\desinstaller_apps.ps1"` | Lance un script PowerShell (ici, un script de désinstallation d’applications) |

