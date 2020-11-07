---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/new-azurermdatamigrationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationService.md
ms.openlocfilehash: 46455cbf411228f008bdc15c27f78715ccea0e89
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625903"
---
# New-AzureRmDataMigrationService

## 摘要
建立 Azure Database 遷移服務的新實例。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
New-AzureRmDataMigrationService -ResourceGroupName <String> -ServiceName <String> -Location <String>
 -Sku <String> -VirtualSubnetId <String> [-DefaultProfile <IAzureContextContainer>]
```

## 說明
New-AzureRmDataMigrationService Cmdlet 會建立 Azure Database 遷移服務的新實例。 這個 Cmdlet 會採用現有 Azure 資源群組的名稱、要建立的 Azure 資料庫移轉服務新實例的唯一名稱、該實例的提供區域、DMS Worker SKU 的名稱，以及該服務要駐留的 Azure 虛擬子網的名稱。 訂閱名稱不提供任何參數，因為使用者需要指定 Azure 登入會話或執行 Get-AzureRmSubscription 的預設訂閱– SubscriptionName "MySubscription" |Select-AzureRmSubscription 選取另一個訂閱。

## 示例

### 範例1
```
PS C:\> New-AzureRmDataMigrationService -ResourceGroupName myResourceGroup -ServiceName TestService -Location "Central US" -Sku Basic_2vCores -VirtualSubnetId $virtualSubNetId
```

上述範例示範如何在美國中北部地方建立名為 TestService 的 Azure 資料庫移轉服務的新實例。


## 參數

### -DefaultProfile
用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -位置
要建立之 Azure 資料庫移轉服務實例的位置，對應至 Azure 區域。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
資源群組的名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceName
Azure 資料庫移轉服務實例的名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Sku
Azure 資料庫移轉服務實例的 sku。 可能的值目前 Basic_1vCore、Basic_2vCores、GeneralPurpose_4vCores

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VirtualSubnetId
指定虛擬網路下要用於 Azure 資料庫移轉服務實例之子網的名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```




## 輸出

### Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService


## 筆記

## 相關連結

