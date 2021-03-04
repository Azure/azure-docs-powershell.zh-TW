---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: A82392AA-B12B-443E-8704-7CF5A9F8ED58
online version: https://docs.microsoft.com/powershell/module/az.keyvault/backup-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultKey.md
ms.openlocfilehash: 3123d0fa188e0e9a4c419ceaa567969fc3a2f8b6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908177"
---
# Backup-AzKeyVaultKey

## 簡介
備份金鑰庫中的金鑰。

## 語法

### ByKeyName (預設) 
```
Backup-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### HsmByKeyName
```
Backup-AzKeyVaultKey -HsmName <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByKey
```
Backup-AzKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 描述
**Backup-AzKeyVaultKey** Cmdlet 會下載金鑰並儲存于檔案中，以備份金鑰保存庫中的指定金鑰。
如果金鑰有多個版本，備份會包含所有版本。
由於下載的內容已加密，因此無法在 Azure 金鑰保存庫外部使用。
您可以將備份金鑰還原到訂閱中任何備份的金鑰庫。
使用此 Cmdlet 的一般原因如下： 
- 您想要代管金鑰的一份副本，以便擁有離線副本，以防您不小心在金鑰保存庫中刪除金鑰。
 
- 您使用 Key Vault 建立金鑰，而現在想要將金鑰複製至不同的 Azure 區域，以便從分散式應用程式的所有實例使用該金鑰。
使用 **Backup-AzKeyVaultKey** Cmdlet 以加密格式來取回金鑰，然後使用 Restore-AzKeyVaultKey Cmdlet，並指定第二個地區的金鑰保存庫。

## 例子

### 範例 1：使用自動產生的檔案名備份金鑰
```powershell
PS C:\Users\username\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'

C:\Users\username\mykeyvault-mykey-1527029447.01191
```

此命令會從名為 MyKeyVault 的金鑰保存庫中，從名為 MyKeyVault 的金鑰中，將該金鑰的備份儲存到自動為您命名的檔案，並顯示檔案名。

### 範例 2：將金鑰備份到指定的檔案名
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

此命令會從名稱為 MyKeyVault 的金鑰保存庫中，從名為 MyKeyVault 的金鑰中，將該金鑰的備份儲存到名為 Backup.blob 的檔案。

### 範例 3：將先前所取的金鑰備份到指定的檔案名，覆寫目標檔案而不提示。
```powershell
PS C:\> $key = Get-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'
PS C:\> Backup-AzKeyVaultKey -Key $key -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

此命令會建立名為 $key 的金鑰備份。名稱為 $key。保存庫名稱為名為 Backup.blob 的檔案，如果檔案已存在，會以無提示方式覆寫檔案。

## 參數

### -DefaultProfile
用於與 Azure 通訊的認證、帳戶、租使用者和訂閱

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

### -強制
覆寫已存在的檔案

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

### -HsmName
HSM 名稱。 Cmdlet 會根據名稱和目前選取的環境，建構受管理 HSM 的 FQDN。

```yaml
Type: System.String
Parameter Sets: HsmByKeyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
要備份的金鑰組合，從呼叫的取回輸出中輸入。

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem
Parameter Sets: ByKey
Aliases: Key

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -名稱
指定要備份的金鑰名稱。

```yaml
Type: System.String
Parameter Sets: ByKeyName, HsmByKeyName
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OutputFile
指定儲存備份 Blob 的輸出檔案。
如果您未指定此參數，此 Cmdlet 會產生您的檔案名。
如果您指定現有輸出檔案的名稱，作業將不會完成，並返回備份檔案已存在的錯誤訊息。

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
指定包含要備份之金鑰的金鑰庫名稱。

```yaml
Type: System.String
Parameter Sets: ByKeyName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -確認
執行 Cmdlet 之前，提示您確認。

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
顯示 Cmdlet 執行時會發生什麼情況。
不會執行 Cmdlet。

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
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)

## 輸入

### Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultKeyIdentityItem

## 輸出

### System.String

## 筆記

## 相關連結

[Add-AzKeyVaultKey](./Add-AzKeyVaultKey.md)

[Get-AzKeyVaultKey](./Get-AzKeyVaultKey.md)

[Remove-AzKeyVaultKey](./Remove-AzKeyVaultKey.md)

[Restore-AzKeyVaultKey](./Restore-AzKeyVaultKey.md)

