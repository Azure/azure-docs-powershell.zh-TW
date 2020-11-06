---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/test-azurermservicebusname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Test-AzureRmServiceBusName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Test-AzureRmServiceBusName.md
ms.openlocfilehash: e7fafeeee8a377cc9bb7eb9ce514c0a0d7b89c9f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448209"
---
# Test-AzureRmServiceBusName

## 摘要
檢查 (DR 設定名稱的指定命名空間名稱或別名的可用性)  

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### AliasCheckNameAvailabilitySet
```
Test-AzureRmServiceBusName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### NamespaceCheckNameAvailabilitySet
```
Test-AzureRmServiceBusName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 說明
**AzureRmServiceBusName** Cmdlet 會檢查命名空間名稱或別名 (DR 配置名稱是否可用) 

## 示例

### 範例1
```
PS C:\> Test-AzureRmServiceBusName -Namespace MyNameSapceName
```

將命名空間名稱 ' MyNameSapceName ' 的可用性傳回狀態傳回 True

### 範例2
```
PS C:\> Test-AzureRmServiceBusName -Namespace MyNameSapceName
```

傳回命名空間名稱 ' MyNameSapceName ' 的可用性狀態為 False，原因如下

### 範例3
```
PS C:\> Test-AzureRmServiceBusName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```

## 參數

### -AliasName
DR 配置名稱-別名名稱

```yaml
Type: System.String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -命名空間
已將命名空間名稱

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
資源群組名稱

```yaml
Type: System.String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### System.object

## 輸出

### PSCheckNameAvailabilityResultAttributes 中的 [.]

## 筆記

## 相關連結
