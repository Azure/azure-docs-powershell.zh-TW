---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B3813F54-E5B7-4605-BB1C-67417FDDB076
online version: ''
schema: 2.0.0
ms.openlocfilehash: a3f9817ebe556bc80364d012040387cca72c56c4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967554"
---
# Remove-AzureSqlDatabase

## 摘要
刪除 Azure SQL 資料庫。

## 句法

### ByNameWithConnectionCoNtext
```
Remove-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -DatabaseName <String> [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByObjectWithConnectionCoNtext
```
Remove-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -Database <Database> [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameWithServerName
```
Remove-AzureSqlDatabase -ServerName <String> -DatabaseName <String> [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByObjectWithServerName
```
Remove-AzureSqlDatabase -ServerName <String> -Database <Database> [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明
**AzureSqlDatabase** Cmdlet 會依伺服器連接內容或伺服器名稱來刪除 Azure SQL 資料庫。
您可以使用 **新的 AzureSqlDatabaseServerCoNtext** Cmdlet 來建立 Azure SQL Database server 連接內容，然後將它與此 Cmdlet 搭配使用。

當您透過指定 Azure SQL 資料庫伺服器名稱來刪除資料庫時， **AzureSqlDatabase** Cmdlet 會使用名稱和目前的 Azure 訂閱資訊來執行作業。

## 示例

### 範例1：移除資料庫
```
PS C:\> Remove-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database01"
```

這個命令會從 Azure SQL Database server 連接內容 $CoNtext 中移除名為 Database01 的資料庫。

### 範例2：使用伺服器名稱移除資料庫
```
PS C:\> Remove-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01"
```

這個命令會從 Azure SQL Database server （名為 lpqd0zbr8y）移除名為 Database01 的資料庫。

### 範例3：使用管線移除資料庫
```
PS C:\> $Database01 | Remove-AzureSqlDatabase -ConnectionContext $Context
PS C:\> $Database01 | Remove-AzureSqlDatabase -ServerName "lpqd0zbr8y"
```

這個範例示範透過管線傳遞資料庫物件的替代方法。

## 參數

### -ConnectionCoNtext
指定此 Cmdlet 從中移除資料庫的伺服器的線上內容。

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByNameWithConnectionContext, ByObjectWithConnectionContext
Aliases: Context

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -資料庫
指定代表此 Cmdlet 移除之資料庫的物件。

```yaml
Type: Database
Parameter Sets: ByObjectWithConnectionContext, ByObjectWithServerName
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DatabaseName
指定此 Cmdlet 移除之資料庫的名稱。

```yaml
Type: String
Parameter Sets: ByNameWithConnectionContext, ByNameWithServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
允許動作完成，不會提示使用者確認。

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

### -設定檔
指定此 Cmdlet 讀取的 Azure 設定檔。
如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerName
指定此 Cmdlet 刪除資料庫的伺服器名稱。

```yaml
Type: String
Parameter Sets: ByNameWithServerName, ByObjectWithServerName
Aliases: 

Required: True
Position: Named
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
顯示在執行 Cmdlet 時會發生什麼情況。
未執行 Cmdlet。

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

### SqlDatabase.. Database （WindowsAzure）

## 輸出

## 筆記
* 根據此操作的嚴重性，此 Cmdlet 會提示您進行確認。 若要略過確認，請指定 *Force* 參數。

## 相關連結

[Azure SQL 資料庫](https://azure.microsoft.com/en-us/services/sql-database/)

[刪除資料庫](https://msdn.microsoft.com/en-us/library/azure/dn505705.aspx)

[Azure SQL 資料庫的作業](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[AzureSqlDatabase](./Get-AzureSqlDatabase.md)

[新-AzureSqlDatabase](./New-AzureSqlDatabase.md)

[新-AzureSqlDatabaseServerCoNtext](./New-AzureSqlDatabaseServerContext.md)

[Set-AzureSqlDatabase](./Set-AzureSqlDatabase.md)


