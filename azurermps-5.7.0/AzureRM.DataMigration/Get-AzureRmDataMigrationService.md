---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/get-azurermdatamigrationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationService.md
ms.openlocfilehash: cac57ff34d925d553c25d97facd81dba017a25c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450616"
---
# Get-AzureRmDataMigrationService

## 摘要
檢索與 Azure Database 遷移服務實例相關聯的屬性。 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### ResourceGroupSet (預設) 
```
Get-AzureRmDataMigrationService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
```

### ResourceIdParameterSet
```
Get-AzureRmDataMigrationService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
```

### ServiceNameGroupSet
```
Get-AzureRmDataMigrationService [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>]
```
## 說明
Get-AzureRmDataMigrationService Cmdlet 會根據服務名稱和 Azure 資源群組名稱，以輸入參數，來檢索與 Azure Database 遷移服務實例相關聯的屬性。 

## 示例

### 範例1
```
PS C:\> Get-AzureRmDataMigrationService -ResourceGroupName testResourceGroup -Name testService
```

上述範例會檢索稱為 testService 的 Azure 資料庫移轉服務實例的屬性。 

### 範例2
```
PS C:\> Get-AzureRmDataMigrationService -ResourceGroupName testResourceGroup 
```

上述範例會在名為 testResourceGroup 的資源群組中，檢索 Azure 資料庫移轉服務。 

## 參數

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。

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

### -名稱
資料移轉服務的名稱。

```yaml
Type: String
Parameter Sets: ServiceNameGroupSet
Aliases: ServiceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
資源群組的名稱。

```yaml
Type: String
Parameter Sets: ResourceGroupSet
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ServiceNameGroupSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
DataMigrationService 資源識別碼。

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
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

### System.object. IList "1 [Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService、DataMigration、Version = 0.1.0.0、Culture = 中性、PublicKeyToken = null）]


## 筆記

## 相關連結





