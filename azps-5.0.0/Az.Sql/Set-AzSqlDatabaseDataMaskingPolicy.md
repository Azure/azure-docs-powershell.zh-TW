---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 1B138185-E836-414F-93CD-7BAE7F474E73
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasedatamaskingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingPolicy.md
ms.openlocfilehash: d4a167871e452cb12533e38793fae463ba6f8dc8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94140244"
---
# Set-AzSqlDatabaseDataMaskingPolicy

## 摘要
為資料庫設定資料遮罩。

## 句法

```
Set-AzSqlDatabaseDataMaskingPolicy [-PassThru] [-PrivilegedUsers <String>] [-DataMaskingState <String>]
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明
**AzSqlDatabaseDataMaskingPolicy** Cmdlet 會設定 Azure SQL 資料庫的資料遮罩原則。
若要使用這個 Cmdlet，請使用 [ *ResourceGroupName* ]、[ *ServerName* ] 和 [ *DatabaseName* ] 參數來識別資料庫。
您可以設定 *DataMaskingState* 參數，以指定是否已啟用或停用資料遮罩作業。
如果 Cmdlet 成功且使用 *PassThru* 參數，則它會傳回描述目前資料遮罩原則的物件（除了資料庫識別碼之外）。
資料庫識別碼包括但不限於、 **ResourceGroupName** 、 **ServerName** 和 **DatabaseName** 。
Azure 上的 SQL Server Stretch Database 服務也支援此 Cmdlet。

## 示例

### 範例1：設定資料庫的資料遮罩原則
```
PS C:\>Set-AzSqlDatabaseDataMaskingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01 -PrivilegedUsers "public" -DataMaskingState "Enabled"
```

這個命令會在名為 server01 的伺服器上，為名為 database01 的資料庫設定資料遮罩原則。

## 參數

### -DatabaseName
指定設定策略之資料庫的名稱。

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

### -DataMaskingState
指定是否已啟用或停用資料遮罩操作。
此參數可接受的值為：
- 後
- 已停用預設值。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
傳回代表您正在使用之專案的物件。
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

### -PrivilegedUsers
指定以分號分隔的許可權使用者識別碼清單。
允許這些使用者查看遮罩資料。

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

### -ResourceGroupName
指定指派給資料庫之資源群組的名稱。

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
指定裝載資料庫的伺服器名稱。

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
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。

## 輸入

### System.object

## 輸出

### DatabaseDataMaskingPolicyModel 中的 [DataMasking]

## 筆記

## 相關連結

[AzSqlDatabaseDataMaskingPolicy](./Get-AzSqlDatabaseDataMaskingPolicy.md)

[AzSqlDatabaseDataMaskingRule](./Get-AzSqlDatabaseDataMaskingRule.md)

[新-AzSqlDatabaseDataMaskingRule](./New-AzSqlDatabaseDataMaskingRule.md)

[移除-AzSqlDatabaseDataMaskingRule](./Remove-AzSqlDatabaseDataMaskingRule.md)

[Set-AzSqlDatabaseDataMaskingRule](./Set-AzSqlDatabaseDataMaskingRule.md)

[SQL 資料庫檔](https://docs.microsoft.com/azure/sql-database/)


