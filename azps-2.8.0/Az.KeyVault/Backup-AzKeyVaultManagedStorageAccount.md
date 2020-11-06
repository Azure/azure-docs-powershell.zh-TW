---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: bf1441c62287e786b0c71e705a0b340e5c51f424
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612152"
---
# Backup-AzKeyVaultManagedStorageAccount

## 摘要
備份 KeyVault 管理的儲存空間帳戶。

## 句法

### ByStorageAccountName (預設) 
```
Backup-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByStorageAccount
```
Backup-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [[-OutputFile] <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 說明
**AzKeyVaultManagedStorageAccount** Cmdlet 會將指定的受管理儲存空間帳戶下載，並儲存在檔案中，以在金鑰保存庫中備份。
因為下載的內容是經過加密的，所以無法在 Azure 金鑰保存庫外部使用。
只要電子倉庫位於同一個 Azure 地理位置，您就可以將備份的儲存空間帳戶還原到其備份之訂閱中的任何重要電子倉庫。
使用此 Cmdlet 的常見原因如下： 
- 您想要保留儲存空間帳戶的離線複本，以防您不小心從 vault 刪除原始文檔。
 
- 您使用 [主要電子倉庫] 建立受管理的儲存空間帳戶，現在想要將物件克隆至不同的 Azure 區域，這樣您就可以從分散式應用程式的所有實例中使用它。
使用 **AzKeyVaultManagedStorageAccount** Cmdlet 以加密格式來檢索受管理的儲存空間帳戶，然後使用 **Restore-AzKeyVaultManagedStorageAccount** Cmdlet，並在第二個區域中指定一個金鑰 vault。

## 示例

### 範例1：使用自動產生的檔案名備份受管理的儲存空間帳戶
```powershell
PS C:\Users\username\> Backup-AzKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -Name 'MyMSAK'

C:\Users\username\mykeyvault-mymsak-1527029447.01191
```

這個命令會從名為 MyKeyVault 的主要保存庫中檢索名為 MyMSAK 的受管理儲存空間帳戶，並將該受管理的儲存空間帳戶的備份儲存到自動為您命名的檔案，並顯示檔案名。

### 範例2：將受管理的儲存空間帳戶備份到指定的檔案名
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyMSAK' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

這個命令會從名為 MyKeyVault 的主要保存庫中檢索名為 MyMSAK 的受管理儲存空間帳戶，並將該受管理的儲存空間帳戶的備份儲存到名為 [Backup.] 的檔案。

### 範例3：將先前檢索到的受管理儲存空間帳戶備份到指定的檔案名，不需提示即覆寫目的地檔案。
```powershell
PS C:\> $msak = Get-AzKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -Name 'MyMSAK'
PS C:\> Backup-AzKeyVaultManagedStorageAccount -StorageAccount $msak -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

這個命令會建立名為 $msak 的受管理儲存空間帳戶的備份。名為 $msak 的保存庫中的名稱。VaultName 到名為 Backup 的檔案，如果檔案已存在，則會以無訊息方式覆蓋該檔案。

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
要備份的儲存帳戶套件，從 [檢索呼叫] 的輸出中進行流水線。

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem
Parameter Sets: ByStorageAccount
Aliases: StorageAccount

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
Parameter Sets: ByStorageAccountName
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OutputFile
輸出檔案。
儲存儲存空間帳戶備份的輸出檔案。
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
Parameter Sets: ByStorageAccountName
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
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### PSKeyVaultManagedStorageAccountIdentityItem 中的 KeyVault。

## 輸出

### System.object

## 筆記

## 相關連結
