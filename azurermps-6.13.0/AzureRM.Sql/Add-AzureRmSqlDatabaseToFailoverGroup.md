---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/add-azurermsqldatabasetofailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Add-AzureRmSqlDatabaseToFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Add-AzureRmSqlDatabaseToFailoverGroup.md
ms.openlocfilehash: c195215bb38152287e1aa65457a5a0ff4b5452cf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449711"
---
# Add-AzureRmSqlDatabaseToFailoverGroup

## 摘要
將一或多個資料庫新增至 Azure SQL Database [容錯移轉] 群組。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Add-AzureRmSqlDatabaseToFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 -Database <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel]>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
在 Azure SQL Database 容錯移轉群組的主要伺服器上新增一個或多個資料庫至該容錯移轉群組。 資料庫不得是現有複製關聯中的次要資料庫。 該命令會將任何已新增資料庫的異地複製，啟動至容錯移轉群組的次要伺服器。
若要取得用以填入 "-Database" 參數的資料庫物件，請在 Get-AzureRmSqlDatabase Cmdlet) 使用 (範例。
必須使用容錯移轉群組的主要伺服器來執行命令。

## 示例

### 範例1
```
PS C:\> $failoverGroup = Get-AzureRmSqlDatabase -ResourceGroupName rg -ServerName primaryserver -DatabaseName db1 | Add-AzureRmSqlDatabaseToFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

這個命令會將一個資料庫新增至容錯移轉群組，方法是將它輸送。

### 範例2
```
PS C:\> $primaryServer = Get-AzureRmSqlServer -ResourceGroupName rg -ServerName primaryserver
PS C:\> $failoverGroup = $primaryServer | Add-AzureRmSqlDatabaseToFailoverGroup -FailoverGroupName fg -Database ($primaryServer | Get-AzureRmSqlDatabase)
```

這個命令會將伺服器中的所有資料庫新增至 [容錯移轉] 群組。

### 範例3
```
PS C:\> $failoverGroup = Get-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
PS C:\> $databases = Get-AzureRmSqlElasticPoolDatabase -ResourceGroupName rg -ServerName primaryserver -ElasticPoolName pool1
PS C:\> $failoverGroup = $failoverGroup | Add-AzureRmSqlDatabaseToFailoverGroup -Database $databases
```

這個命令會將彈性池中的所有資料庫新增至容錯移轉群組。

## 參數

### -資料庫
要新增至容錯移轉群組之 [容錯移轉] 群組主要伺服器上的一個或多個 Azure SQL 資料庫。

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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
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
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
資源群組的名稱。

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

### -ServerName
容錯移轉群組之主要 Azure SQL Database 伺服器的名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### System.object

### [System.object]。清單 ' 1 [AzureSqlDatabaseModel，4.11.0.0，.Sql. .sql，版本 =，Culture = 中性，PublicKeyToken = null]]。））。

## 輸出

### AzureSqlFailoverGroupModel 中的 [FailoverGroup]

## 筆記

## 相關連結

[新-AzureRmSqlDatabaseFailoverGroup](./New-AzureRmSqlDatabaseFailoverGroup.md)

[Set-AzureRmSqlDatabaseFailoverGroup](./Set-AzureRmSqlDatabaseFailoverGroup.md)

[AzureRmSqlDatabaseFailoverGroup](./Get-AzureRmSqlDatabaseFailoverGroup.md)

[移除-AzureRmSqlDatabaseFromFailoverGroup](./Remove-AzureRmSqlDatabaseFromFailoverGroup.md)

[切換 AzureRmSqlDatabaseFailoverGroup](./Switch-AzureRmSqlDatabaseFailoverGroup.md)

[移除-AzureRmSqlDatabaseFailoverGroup](./Remove-AzureRmSqlDatabaseFailoverGroup.md)

[SQL 資料庫檔](https://docs.microsoft.com/azure/sql-database/)
