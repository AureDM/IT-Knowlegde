# Rediriger des ports entre hôte et VM
- Aller dans les paramètres de la VM : Configuration > Réseaux > Advanced > Redirection de ports
	![[Pasted image 20260206230712.png]]
	***IP hôte** : loopback PC / **IP invité** : IP attribuée à la VM*

- Se connecter en SSH sur la VM : 
```powershell
ssh username@127.0.0.1 -p 2222
```
