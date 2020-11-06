---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2.md
gitcommit: https://github.com/Azure/azure-powershell/blob/7fe7039e96038b4a91513dfda26026ad8e0a352b
ms.openlocfilehash: 8742babd73e28e28797db75952d7eb9e9c8dc4a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450784"
---
# Get-AzureRmDataFactoryV2

## 摘要
取得資料工廠的相關資訊。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Get-AzureRmDataFactoryV2 [-ResourceGroupName] <String> [[-Name] <String>]
```

## 說明
Get-AzureRmDataFactoryV2 Cmdlet 會取得 Azure 資源群組中資料工廠的相關資訊。
如果您指定資料工廠的名稱，此 Cmdlet 會取得該資料工廠的相關資訊。
如果您沒有指定名稱，此 Cmdlet 會取得 Azure 資源群組中所有資料工廠的相關資訊。


## 示例

### 範例1：取得所有資料工廠
```
PS C:\> Get-AzureRmDataFactoryV2 -ResourceGroupName "ADF"

    DataFactoryName   : WikiADF
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataFactory/factories/wikiadf
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
    ProvisioningState : Succeeded

    DataFactoryName   : WikiADF2
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataFactory/factories/wikiadf2
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          :
    ProvisioningState : Succeeded

```

顯示有關 Azure 訂閱中所有資料工廠的資訊。

### 範例2：取得特定的資料工廠
```
PS C:\> $DataFactory = Get-AzureRmDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF"

    DataFactoryName   : WikiADF
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataF
                        actory/factories/wikiadf
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
    ProvisioningState : Succeeded

```

這個命令會在名為「ADF」的資源群組的訂閱中，顯示名為 WikiADF 的資料工廠相關資訊，然後將它儲存在 $DataFactory 變數中。
在後續的 Cmdlet 中指定 DataFactory 參數，以使用 $DataFactory 中儲存的資料工廠。

## 參數

### -名稱
指定要取得資訊之資料工廠的名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: DataFactoryName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
指定 Azure 資源群組的名稱。
這個 Cmdlet 會取得屬於此參數指定之群組之資料工廠的相關資訊。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## 輸入

### System.object


## 輸出

### [System.object]。清單 ' 1 [Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory，DataFactoryV2，版本 = 0.1.9.0，Culture = 中性，PublicKeyToken = null）]
Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory


## 筆記
關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠

## 相關連結
[Set-AzureRmDataFactoryV2]()

[移除-AzureRmDataFactoryV2]()

