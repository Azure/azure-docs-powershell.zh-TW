---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: BC00DEF9-6A93-4DF5-8E5B-C488551BA1D1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/import-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Import-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Import-AzureRmRedisCache.md
ms.openlocfilehash: 278afd493d66fdc817bd61b0a11e15b1c6b54391
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452771"
---
# Import-AzureRmRedisCache

## 摘要
從 blob 匯入資料到 Azure Redis Cache。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Import-AzureRmRedisCache [-ResourceGroupName <String>] -Name <String> -Files <String[]> [-Format <String>]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明
匯 **入-AzureRmRedisCache** Cmdlet 會將資料從 blob 匯入到 Azure Redis Cache。

## 示例

### 範例1：匯入資料
```
PS C:\>Import-AzureRmRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Files @("https://mystorageaccount.blob.core.windows.net/container22/blobname?sv=2015-04-05&sr=b&sig=caIwutG2uDa0NZ8mjdNJdgOY8%2F8mhwRuGNdICU%2B0pI4%3D&st=2016-05-27T00%3A00%3A00Z&se=2016-05-28T00%3A00%3A00Z&sp=rwd") -Force
```

這個命令會將 SAS URL 所指定的 blob 中的資料匯入 Azure Redis Cache。

## 參數

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -檔案
指定其內容此 Cmdlet 匯入到快取的 blob 的 SAS Url。 您可以使用下列 PowerShell 命令產生 SAS Url： $storageAccountCoNtext = New-AzureStorageContext-StorageAccountName "storageName"-StorageAccountKey "key" $sasKeyForBlob = New-AzureStorageBlobSASToken 容器 "容器"-blob "blobName"-許可權 "rwdl"-StartTime ( [System. DateTime]：： Now) 。AddMinutes (-15) -ExpiryTime ( [System. DateTime]：：現在) 。AddHours (5) -CoNtext $storageAccountCoNtext-FullUri Import-AzureRmRedisCache-ResourceGroupName "ResourceGroupName"-Name "cacheName"- ($sasKeyForBlob) 

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Force
強制執行命令，而不要求使用者確認。

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

### -Format
指定 blob 的格式。
目前的 rdb 是唯一支援的格式。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -名稱
指定快取的名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
指示這個 Cmdlet 會傳回一個布林值，指出該作業是否會成功。
根據預設，這個 Cmdlet 不會產生任何輸出。

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

### -ResourceGroupName
指定包含快取的資源群組的名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Default value: False
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### System.object

### System.object []

## 輸出

### System.object

## 筆記
* 關鍵字： azure、azurerm、arm、資源、管理、manager、redis、cache、web、webapp、網站

## 相關連結

[Export-AzureRmRedisCache](./Export-AzureRmRedisCache.md)

[新-AzureRmRedisCache](./New-AzureRmRedisCache.md)

[移除-AzureRmRedisCache](./Remove-AzureRmRedisCache.md)

[Reset-AzureRmRedisCache](./Reset-AzureRmRedisCache.md)

[Set-AzureRmRedisCache](./Set-AzureRmRedisCache.md)


