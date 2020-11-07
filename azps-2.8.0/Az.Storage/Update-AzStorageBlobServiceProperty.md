---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azstorageblobserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageBlobServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageBlobServiceProperty.md
ms.openlocfilehash: 195bc966bb47bf921eb0150272cfb9af6d73c63a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792919"
---
# Update-AzStorageBlobServiceProperty

## 摘要
修改 Azure 儲存區 Blob 服務的服務屬性。

## 句法

### AccountName (預設) 
```
Update-AzStorageBlobServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultServiceVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### AccountObject
```
Update-AzStorageBlobServiceProperty -StorageAccount <PSStorageAccount> [-DefaultServiceVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### BlobServicePropertiesResourceId
```
Update-AzStorageBlobServiceProperty [-ResourceId] <String> [-DefaultServiceVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明
**AzStorageBlobServiceProperty** Cmdlet 會修改 Azure Storage Blob 服務的服務屬性。

## 示例

### 範例1：將 Blob 服務 DefaultServiceVersion 設定為2018-03-28
```
C:\PS> Update-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -DefaultServiceVersion 2018-03-28 

StorageAccountName ResourceGroupName DefaultServiceVersion DeleteRetentionPolicy.Enabled DeleteRetentionPolicy.Days
------------------ ----------------- --------------------- ----------------------------- --------------------------
myresourcegroup    mystorageaccount  2018-03-28            False
```

這個命令會將 Blob 服務的 DefaultServiceVersion 設定為2018-03-28。

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

### -DefaultServiceVersion
要設定的預設服務版本

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

### -ResourceGroupName
資源組名稱。

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
輸入儲存空間帳戶資源識別碼，或 [Blob 服務屬性] 資源 Id。

```yaml
Type: System.String
Parameter Sets: BlobServicePropertiesResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccount
儲存空間帳戶物件

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -StorageAccountName
儲存空間帳戶名稱。

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName, Name

Required: True
Position: 1
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

### PSStorageAccount 中的 [管理]。

### System.object

## 輸出

### PSBlobServiceProperties 中的 [管理]。

## 筆記

## 相關連結
