
![Logo](https://raw.githubusercontent.com/GilbertoShimokawaFalcao/C7FS/main/_Extra/ArtImage.png)
# C7FS - Versão software atualizada de 12/03/2023

CRONOS, CUSTOM, CONNECT, CREATE, CUT, COPY, CLEAR - FILE SYSTEM -> Crie diretórios e manipule volume de dados de seus Servidores, celulares ou até mesmo de seus diretórios do seu computador, FTP to FTP, Android, etc de forma automatizada. Chega de perder horas procurando o que salvar onde salvar, concentre tudo em um único local ou apague tudo que é desnecessário.

## Autor
Gilberto Shimokawa Falcão.
## Exemplos de uso (Leia nosso manual 'Manual C7FS' para mais detalhes)

#### Criando log da aplicação
```javascript
CRONOS = [cronoslog]
```

#### Criando apelidos para atalhos
```javascript
CUSTOM [cronoslog] = D:\Backup\C7FSHUBDownloads\_!CronosLog
CUSTOM [util] = D:\Backup\C7FSHUBDownloads\UtilVerificar
CUSTOM [lixo] = D:\Backup\C7FSHUBDownloads\Lixo
CUSTOM [ftp] = ftp://192.168.0.12:3456
CUSTOM [transfertopc] = ftp://192.168.0.12:3456/!TransferToPC/
CUSTOM [Whatssap] = ftp://192.168.0.12:3456/Android/media/com.whatsapp/WhatsApp
```
#### Estabelecendo conexão via FTP
```javascript
CONNECT ftp://192.168.0.12:3456 = meuLogin,minhaSenha
```
#### Criando diretórios
```javascript
CREATE
[util]\LocalPC
[util]\PictureDCIM_etc
[util]\TransferPC
[util]\AndroidDownloads
[util]\zap\imagens
[util]\zap\Videos
[util]\zap\Comuns
[util]\zap\Documentos
[util]\zap\ProfileFotos
[util]\zap\Walpappers
```
#### Recortando arquivos de diretórios
```javascript
CUT
C:\Users\UserDesktop\Videos\Captures\
C:\Users\UserDesktop\Pictures\Screenshots\
C:\Users\UserDesktop\Downloads\

FOR
[util]\LocalPC

CUT
[ftp]/Download/

FOR
[util]\AndroidDownloads

CUT
[transfertopc]

FOR
[util]\TransferPC

CUT
[ftp]/CubeCallRecorder/All/.props/
[ftp]/DCIM/.globalTrash/
[ftp]/DCIM/Camera/
[ftp]/DCIM/Screenshots/
[ftp]/Pictures/.thumbnails/
[ftp]/Pictures/Memedroid Images/
[ftp]/Pictures/Memes/
[ftp]/Pictures/Messenger/
[ftp]/Pictures/sticker.ly/
[ftp]/Pictures/Whatsapp/
[ftp]/SquarePic/.crop/

FOR
[util]\PictureDCIM_etc

CUT
[Whatssap]/Media/WhatsApp Documents/

FOR
[util]\zap\Documentos

CUT
[Whatssap]/Media/WhatsApp Images/

FOR 
[util]\zap\imagens

CUT
[Whatssap]/Media/WhatsApp Video/

FOR
[util]\zap\Videos

CUT
[Whatssap]/Media/WhatsApp Animated Gifs/
[Whatssap]/Media/.Statuses/

FOR
[util]\zap\Comuns

CUT
[Whatssap]/Media/WhatsApp Profile Photos/

FOR
[util]\zap\ProfileFotos
```

#### Copiando arquivos de um diretório
```javascript
COPY
[Whatssap]/Media/WallPaper/

FOR
[util]\zap\Walpappers
```

#### Eliminando diretórios e conteúdo de diretórios
```javascript
CLEAR
C:\Users\UserDesktop\AppData\Local\Temp\
C:\Users\UserDesktop\Searches\
[Whatssap]/Media/.Links/
[Whatssap]/Media/WhatsApp Voice Notes/
[Whatssap]/Media/WhatsApp Audio/
[Whatssap]/.Shared/
[Whatssap]/.StickerThumbs/
[Whatssap]/.Thumbs/
[Whatssap]/.trash/
[Whatssap]/Backups/
[Whatssap]/Databases/
```
