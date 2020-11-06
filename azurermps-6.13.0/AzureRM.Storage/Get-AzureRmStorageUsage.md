---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: 11AAA319-DDBB-4156-9BE7-4DE8B80A904C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstorageusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageUsage.md
ms.openlocfilehash: c63573da3c12eb54329d05f49615057d0595b77c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450161"
---
# Get-AzureRmStorageUsage

## 摘要
取得目前訂閱的儲存資源使用量。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Get-AzureRmStorageUsage [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzureRmStorageUsage** Cmdlet 會取得目前訂閱之 Azure 儲存空間的資源使用量。

## 示例

### 範例1：取得儲存資源使用量
```
PS C:\>Get-AzureRmStorageUsage
```

這個命令會取得目前訂閱的儲存資源使用量。
 

### 範例2：取得指定位置的儲存資源使用量
```
PS C:\>Get-AzureRmStorageUsage -Location 'West US'

LocalizedName : Storage Accounts
Name          : StorageAccounts
Unit          : Count
CurrentValue  : 18
Limit         : 250
```

這個命令會在目前的訂閱下，取得指定位置的儲存資源使用量。

## 參數

### -DefaultProfile
用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。

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

### -位置
指示在指定位置取得儲存資源的使用量。
如果未指定，將會取得訂閱下所有位置的儲存資源使用量。

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

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### 所有

## 輸出

### PSUsage 中的 [管理]。

## 筆記

## 相關連結

[Azure 儲存管理器 Cmdlet](./AzureRM.Storage.md)


