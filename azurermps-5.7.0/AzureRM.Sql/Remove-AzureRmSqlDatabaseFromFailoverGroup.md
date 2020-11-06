---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqldatabasefromfailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseFromFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseFromFailoverGroup.md
ms.openlocfilehash: ba0203b328b1ae75b1f671ed3e9437a47657bb1a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453000"
---
# Remove-AzureRmSqlDatabaseFromFailoverGroup

## 摘要
從 Azure SQL Database 容錯移轉群組中移除一或多個資料庫。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Remove-AzureRmSqlDatabaseFromFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 -Database <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel]>
 [-Force] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 說明
從指定的 Azure SQL Database 容錯移轉群組中移除一或多個資料庫。 資料庫與複製關聯保持不變，但無法再透過容錯移轉群組端點存取它們。

若要取得用以填入 "-Database" 參數的資料庫物件，請在 Get-AzureRmSqlDatabase Cmdlet) 使用 (範例。

必須使用容錯移轉群組的主要伺服器來執行命令。

## 示例

### 範例1
```
PS C:\> $failoverGroup = Get-AzureRmSqlDatabase -ResourceGroupName rg -ServerName primaryserver -DatabaseName db1 | Remove-AzureRmSqlDatabaseFromFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

這個命令會將一個資料庫從容錯移轉群組中移除，只要將它作為管道。

### 範例2
```
PS C:\> $primaryServer = Get-AzureRmSqlServer -ResourceGroupName rg -ServerName primaryserver
PS C:\> $failoverGroup = $primaryServer | Remove-AzureRmSqlDatabaseFromFailoverGroup -FailoverGroupName fg -Database ($primaryServer | Get-AzureRmSqlDatabase)
```

這個命令會從容錯移轉群組中移除所有資料庫。

### 範例3
```
PS C:\> $failoverGroup = Get-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
PS C:\> $databases = Get-AzureRmSqlElasticPoolDatabase -ResourceGroupName rg -ServerName primaryserver -ElasticPoolName pool1
PS C:\> $failoverGroup = $failoverGroup | Remove-AzureRMSqlDatabaseFromFailoverGroup -Database $databases
```

這個命令會從容錯移轉群組中移除彈性池中的所有資料庫。

## 參數

### -資料庫
要從容錯移轉群組中移除之容錯移轉群組主要伺服器上的一個或多個 Azure SQL 資料庫。

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱

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

### -FailoverGroupName
Azure SQL Database 容錯移轉群組的名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Force
跳過確認訊息以執行動作。

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
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
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServerName
容錯移轉群組之主要 Azure SQL Database 伺服器的名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -確認
在執行 Cmdlet 之前提示您進行確認。

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
顯示在執行 Cmdlet 時會發生什麼情況。 未執行 Cmdlet。

```yaml
Type: SwitchParameter
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
[System.object]。清單 ' 1 [AzureSqlDatabaseModel，2.5.0.0，.Sql. .sql，版本 =，Culture = 中性，PublicKeyToken = null]]。））。

## 輸出

### System.object

## 筆記

## 相關連結

[新-AzureRmSqlDatabaseFailoverGroup](./New-AzureRmSqlDatabaseFailoverGroup.md)

[Set-AzureRmSqlDatabaseFailoverGroup](./Set-AzureRmSqlDatabaseFailoverGroup.md)

[AzureRmSqlDatabaseFailoverGroup](./Get-AzureRmSqlDatabaseFailoverGroup.md)

[附加 AzureRmSqlDatabaseToFailoverGroup](./Add-AzureRmSqlDatabaseToFailoverGroup.md)

[切換 AzureRmSqlDatabaseFailoverGroup](./Switch-AzureRmSqlDatabaseFailoverGroup.md)

[移除-AzureRmSqlDatabaseFailoverGroup](./Remove-AzureRmSqlDatabaseFailoverGroup.md)

[SQL 資料庫檔](https://docs.microsoft.com/azure/sql-database/)
