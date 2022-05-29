# Manual de PowerShell

## Temas Varios

### Ejecutar sentencia al iniciar la consola

Para poder ejecutar una sentencia al iniciar la consola, se debe crear o modificar el archivo `Microsoft.PowerShell_profile.ps1` en la carpeta `C:\Users\[USUARIO]\Documents\WindowsPowerShell` , si en el archivo o carpeta no existen en esa ruta, se deben crear. Por ejemplo, el siguiente script es para imprimir un saludo al iniciar la consola (el texto fue generado en el siguiente link para texto [ASCII](https://patorjk.com/software/taag/#p=display&f=Graffiti&t=Type%20Something%20)):

```powershell
Get-Date -format "yyyy-MM-dd ss:mm:HH"
Write-Host " "
Write-Host "ooooo ooooo             o888                   ooooooooooo        oooo                                            oooo "
Write-Host " 888   888    ooooooo    888    ooooooo         888    88    ooooo888    oooooooo8   ooooooo   oo oooooo     ooooo888  "
Write-Host " 888ooo888  888     888  888    ooooo888        888ooo8    888    888  888    88o    ooooo888   888    888 888    888  "
Write-Host " 888   888  888     888  888  888    888        888    oo  888    888   888oo888o  888    888   888        888    888  "
Write-Host "o888o o888o   88ooo88   o888o  88ooo88 8o      o888ooo8888   88ooo888o 888     888  88ooo88 8o o888o         88ooo888o "
Write-Host "                                                                        888ooo888                                      "
Get-Date -format "yyyy-MM-dd ss:mm:HH"
```

Este sería su ejecución:

![](images\2022-05-29-00-24-40-image.png)

Para poder probar las sentencias, se puede usar el editor `Windows PowerShell ISE` para validar su ejecución. 
