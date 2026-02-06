# Gestion des applications et fonctionnalités Windows
Doc : [ici](https://www.malekal.com/desinstaller-les-applications-preinstallees-de-windows-10-11/i)

- **Lister les ID des applications**
  ```powershell
  Get-AppxPackage -AllUsers | Select Name, PackageFullName
  ```

- **Lister les fonctionnalités facultatives**
  ```powershell
  Get-WindowsOptionalFeature -Online
  ```

- **Désactiver/supprimer une fonctionnalité (exemple : Windows Media Player)**
  ```powershell
  Get-WindowsOptionalFeature -Online | Where-Object { \$_.FeatureName -like "*Media*" }
  Disable-WindowsOptionalFeature -Online -FeatureName "WindowsMediaPlayer" -Remove
  ```

