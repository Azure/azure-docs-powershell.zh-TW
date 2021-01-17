---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVault.md
ms.openlocfilehash: d1cf3757596a56336c25c46bd6c4e38687888d6e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98436493"
---
# Restore-AzKeyVault

## 摘要
從備份中完整還原受管理的 HSM。

## 句法

### InteractiveStorageName (預設) 
```
Restore-AzKeyVault -BackupFolder <String> [-KeyName <String>] [-PassThru] [-HsmName] <String>
 -StorageAccountName <String> -StorageContainerName <String> -SasToken <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InteractiveStorageUri
```
Restore-AzKeyVault -BackupFolder <String> [-KeyName <String>] [-PassThru] [-HsmName] <String>
 -StorageContainerUri <Uri> -SasToken <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### InputObjectStorageUri
```
Restore-AzKeyVault -BackupFolder <String> [-KeyName <String>] [-PassThru] -StorageContainerUri <Uri>
 -SasToken <SecureString> -HsmObject <PSManagedHsm> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### InputObjectStorageName
```
Restore-AzKeyVault -BackupFolder <String> [-KeyName <String>] [-PassThru] -StorageAccountName <String>
 -StorageContainerName <String> -SasToken <SecureString> -HsmObject <PSManagedHsm>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明
從儲存在儲存空間帳戶中的備份中完整還原受管理的 HSM。
使用 [ `Backup-AzKeyVault` 備份]。

## 示例

### 範例1
```powershell
PS C:\> $sasToken = ConvertTo-SecureString -AsPlainText -Force "?sv=2019-12-12&ss=bfqt&srt=sco&sp=rwdlacupx&se=2020-10-12T14:42:19Z&st=2020-10-12T06:42:19Z&spr=https&sig=******"
PS C:\> Restore-AzKeyVault -HsmName myHsm -StorageContainerUri "https://{accountName}.blob.core.windows.net/{containerName}" -BackupFolder "mhsm-myHsm-2020101308504935" -SasToken $sasToken
```

這個範例會將儲存在存儲容器 "mhsm-myHsm-2020101308504935" 的資料夾（"HTTPs：//{accountName"）中的備份還原儲存在

## 參數

### -BackupFolder
備份的資料夾名稱，例如 ' mhsm-*-2020101309020403」。它也可以嵌套，例如「備份/mhsm-*-2020101309020403」。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -HsmName
HSM 的名稱。

```yaml
Type: System.String
Parameter Sets: InteractiveStorageName, InteractiveStorageUri
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HsmObject
受管理的 HSM 物件

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: InputObjectStorageUri, InputObjectStorageName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -KeyName
要還原的索引鍵名。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
還原 HSM 時，傳回 true。

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

### -SasToken
共用存取簽名 (SAS) 權杖來驗證儲存空間帳戶。

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccountName
儲存備份的儲存空間帳戶名稱。

```yaml
Type: System.String
Parameter Sets: InteractiveStorageName, InputObjectStorageName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageContainerName
要儲存備份之 blob 容器的名稱。

```yaml
Type: System.String
Parameter Sets: InteractiveStorageName, InputObjectStorageName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageContainerUri
儲存備份的儲存空間容器 URI。

```yaml
Type: System.Uri
Parameter Sets: InteractiveStorageUri, InputObjectStorageUri
Aliases:

Required: True
Position: Named
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

### 所有

## 輸出

### System.object

## 筆記

## 相關連結
