---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 69A26BF3-7FE7-41ED-8C21-C8DC72D09615
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/start-azurermsqlserverupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlServerUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlServerUpgrade.md
ms.openlocfilehash: 279216ad20783017f091143a7c440873c8e04946
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448169"
---
# Start-AzureRmSqlServerUpgrade

## 摘要
開始升級 SQL 資料庫伺服器。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Start-AzureRmSqlServerUpgrade -ServerVersion <String> [-ScheduleUpgradeAfterUtcDateTime <DateTime>]
 [-DatabaseCollection <RecommendedDatabaseProperties[]>]
 [-ElasticPoolCollection <UpgradeRecommendedElasticPoolProperties[]>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzureRmSqlServerUpgrade** Cmdlet 會開始將 Azure SQL Database server 版本11升級到版本12。
您可以使用 Get-AzureRmSqlServerUpgrade Cmdlet 監視升級的進度。

## 示例

### 範例1：升級伺服器
```
PS C:\>Start-AzureRmSqlServerUpgrade -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ServerVersion 12.0
ResourceGroupName               : ResourceGroup01
ServerName                      : Server01
ServerVersion                   : 12.0
ScheduleUpgradeAfterUtcDateTime : 
DatabaseCollection              :
```

這個命令會升級指派給資源群組 TesourceGroup01 的名為 server01 的伺服器。

### 範例2：使用排程時間和資料庫建議來升級伺服器
```
PS C:\>$ScheduleTime = (Get-Date).AddMinutes(5).ToUniversalTime()
PS C:\> $DatabaseMap = New-Object -TypeName Microsoft.Azure.Management.Sql.Models.RecommendedDatabaseProperties
PS C:\> $DatabaseMap.Name = "contosodb"
PS C:\> $DatabaseMap.TargetEdition = "Standard"
PS C:\> $DatabaseMap.TargetServiceLevelObjective = "S0"
PS C:\> Start-AzureRmSqlServerUpgrade -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ServerVersion 12.0 -ScheduleUpgradeAfterUtcDateTime $ScheduleTime -DatabaseCollection ($DatabaseMap)
```

第一個命令會在未來使用 Get-Date Cmdlet 來建立5分鐘的時間。
該命令會將 $ScheduleTime 中的日期儲存在變數中。
如需詳細資訊，請輸入 `Get-Help Get-Date` 。
第二個命令會建立 **RecommendedDatabaseProperties** 物件，然後將該物件儲存在 $DatabaseMap 的變數中。
接下來的三個命令會將值指派給儲存在 $DatabaseMap 的物件屬性。
最後一個命令會將名為 Server01 的現有伺服器升級為版本12.0。
在執行命令之後，最早要升級的時間是由 $ScheduleTime 變數所指定。
升級之後，資料庫 contosodb 將執行標準版，並擁有服務層級目標 S0。

## 參數

### -DatabaseCollection
指定此 Cmdlet 用來進行伺服器升級的 **RecommendedDatabaseProperties** 物件陣列。

```yaml
Type: Microsoft.Azure.Management.Sql.LegacySdk.Models.RecommendedDatabaseProperties[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱

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

### -ElasticPoolCollection
指定要用於伺服器升級的 **UpgradeRecommendedElasticPoolProperties** 物件陣列。

```yaml
Type: Microsoft.Azure.Management.Sql.LegacySdk.Models.UpgradeRecommendedElasticPoolProperties[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
指定指派給伺服器之資源群組的名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ScheduleUpgradeAfterUtcDateTime
指定要升級伺服器的最早時間（做為 **DateTime** 物件）。
在 ISO8601 格式中指定一個值，並以 [ (UTC]) 的 [協調世界時間]。
如需詳細資訊，請輸入 `Get-Help Get-Date` 。

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerName
指定此 Cmdlet 升級的伺服器名稱。

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

### -ServerVersion
指定此 Cmdlet 升級伺服器的版本。
唯一有效的值是12.0。

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

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### System.object

## 輸出

### AzureSqlServerUpgradeStartModel 中的 [ServerUpgrade]

## 筆記

## 相關連結

[AzureRmSqlServerUpgrade](./Get-AzureRmSqlServerUpgrade.md)

[停止 AzureRmSqlServerUpgrade](./Stop-AzureRmSqlServerUpgrade.md)

[SQL 資料庫檔](https://docs.microsoft.com/azure/sql-database/)


