---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/get-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Get-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Get-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 16873efe9ba51eb71821fe7149c5abb1f316c4eb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623697"
---
# Get-AzureRmPowerBIEmbeddedCapacity

## 摘要
取得 PowerBI 內嵌容量的詳細資料。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Get-AzureRmPowerBIEmbeddedCapacity [[-ResourceGroupName] <String>] 
    [<CommonParameters>]

Get-AzureRmPowerBIEmbeddedCapacity [-ResourceGroupName] <String> [-Name] <String> 
    [<CommonParameters>]
```

## 說明
Get-AzureRmPowerBIEmbeddedCapacity Cmdlet 會取得 PowerBI 內嵌容量的詳細資料。

## 示例

### 範例1：取得資源群組容量
```
PS C:\>Get-AzureRmPowerBIEmbeddedCapacity -ResourceGroupName "testRG"
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {admin@microsoft.com}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {}

Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/mycapacity
ResourceGroup          : testRG
Name                   : mycapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {admin@microsoft.com}
Sku                    : A4
Tier                   : PBIE_Azure
Tag                    : {}
```

這個命令會在名為 testRG 的資源群組中取得所有的 Azure PowerBI 內嵌容量

### 範例2：取得容量
```
PS C:\>Get-AzureRmPowerBIEmbeddedCapacity -ResourceGroupName "testRG" -Name "testcapacity"
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {admin@microsoft.com}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {}

```

這個命令會在名為 testRG 的資源群組中，取得名為 testcapacity 的 Azure PowerBI 內嵌的容量。

## 參數

### -ResourceGroupName
容量所屬之 Azure 資源群組的名稱

```yaml
Type: String
Parameter Sets: ByResourceGroup, ByCapacity
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```

### -名稱
PowerBI 內嵌容量的名稱

```yaml
Type: String
Parameter Sets: ByCapacity
Aliases: 

Required: True
Position: 1
Default value: None
Accept wildcard characters: False
```

### -ResourceId
Azure 資源識別碼

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### 所有
這個 Cmdlet 不接受任何輸入。

## 輸出

### PSPowerBIEmbeddedCapacity><的 [清單]

## 筆記

## 相關連結

[新-AzureRmPowerBIEmbeddedCapacity ](./New-AzureRmPowerBIEmbeddedCapacity.md)

[移除-AzureRmPowerBIEmbeddedCapacity ](./Remove-AzureRmPowerBIEmbeddedCapacity.md)
