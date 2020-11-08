---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultCertificate.md
ms.openlocfilehash: 51d322ea738a56e4b1fa24cccdb7bb59a6cd0d21
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93969673"
---
# Backup-AzKeyVaultCertificate

## 摘要
在金鑰保存庫中備份憑證。

## 句法

### ByCertificateName (預設) 
```
Backup-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByCertificate
```
Backup-AzKeyVaultCertificate [-InputObject] <PSKeyVaultCertificateIdentityItem> [[-OutputFile] <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明
**AzKeyVaultCertificate** Cmdlet 會透過下載並儲存在檔案中，以備份金鑰儲存庫中指定的憑證。
如果憑證有多個版本，則備份中會包含其所有版本。
因為下載的內容是經過加密的，所以無法在 Azure 金鑰保存庫外部使用。
只要電子倉庫位於同一個 Azure 地理位置，您就可以將已備份的憑證還原到其備份之訂閱中的任何重要電子倉庫。
使用此 Cmdlet 的常見原因如下： 
- 您想要保留憑證的離線複本，以防您不小心刪除電子倉庫中的原始版本。
 
- 您是使用金鑰保存庫建立憑證，現在想要將物件克隆至不同的 Azure 區域，這樣您就可以從分散式應用程式的所有實例中使用它。
使用 **AzKeyVaultCertificate** Cmdlet，以加密格式來檢索憑證，然後使用 **Restore-AzKeyVaultCertificate** Cmdlet，並在第二個區域中指定一個金鑰保險存儲區。

## 示例

### 範例1：使用自動產生的檔案名備份憑證
```powershell
PS C:\Users\username\> Backup-AzKeyVaultCertificate -VaultName 'mykeyvault' -Name 'mycert'

C:\Users\username\mykeyvault-mycert-1527029447.01191
```

這個命令會從名為 MyKeyVault 的主要保存庫中檢索名為 MyCert 的憑證，並將該憑證的備份儲存到自動為您命名的檔案，並顯示檔案名。

### 範例2：將憑證備份到指定的檔案名
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyCert' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

這個命令會從名為 MyKeyVault 的主要保存庫中檢索名為 MyCert 的憑證，並將該憑證的備份儲存到名為 [Backup.] 的檔案。

### 範例3：將先前檢索的憑證備份到指定的檔案名，不需提示即覆寫目的地檔案。
```powershell
PS C:\> $cert = Get-AzKeyVaultCertificate -VaultName 'MyKeyVault' -Name 'MyCert'
PS C:\> Backup-AzKeyVaultCertificate -Certificate $cert -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

這個命令會建立名為 $cert 的憑證備份。名為 $cert 的保存庫中的名稱。VaultName 到名為 Backup 的檔案，如果檔案已存在，則會以無訊息方式覆蓋該檔案。

## 參數

### -DefaultProfile
用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
覆寫指定的檔案（如果有的話）

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
要備份的機密，從檢索呼叫的輸出中流水線。

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem
Parameter Sets: ByCertificate
Aliases: Certificate

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -名稱
[秘密名稱]。
Cmdlet 會從保存庫名稱、目前已選取的環境和密碼來構造秘密的 FQDN。

```yaml
Type: System.String
Parameter Sets: ByCertificateName
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OutputFile
輸出檔案。
儲存憑證備份的輸出檔案。
如果未指定，將會產生預設檔案名。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VaultName
保存庫名稱。
Cmdlet 根據名稱和目前所選的環境來構造電子倉庫的 FQDN。

```yaml
Type: System.String
Parameter Sets: ByCertificateName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -確認
在執行 Cmdlet 之前提示您進行確認。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
顯示在執行 Cmdlet 時會發生什麼情況。
未執行 Cmdlet。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。

## 輸入

### PSKeyVaultCertificateIdentityItem 中的 KeyVault。

## 輸出

### System.object

## 筆記

## 相關連結
