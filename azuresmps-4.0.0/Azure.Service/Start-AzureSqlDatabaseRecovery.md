---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: F63769D6-9A31-4A67-972A-1E0428853C86
online version: ''
schema: 2.0.0
ms.openlocfilehash: 88f61718e363a630b70519590025a6da80364aeb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93966869"
---
# Start-AzureSqlDatabaseRecovery

## 摘要
啟動資料庫的還原要求。

## 句法

### BySourceDatabaseName
```
Start-AzureSqlDatabaseRecovery -SourceServerName <String> -SourceDatabaseName <String>
 [-TargetServerName <String>] [-TargetDatabaseName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### BySourceDatabaseObject
```
Start-AzureSqlDatabaseRecovery -SourceDatabase <RecoverableDatabase> [-TargetServerName <String>]
 [-TargetDatabaseName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 說明
**Start-AzureSqlDatabaseRecovery** Cmdlet 會針對即時或刪除的資料庫啟動還原要求。
這個 Cmdlet 支援基本的復原，該恢復會使用資料庫最近已知可用的備份。
[恢復] 作業會建立新的資料庫。
如果您在同一個伺服器上復原即時資料庫，您必須為新資料庫指定不同的名稱。

若要為資料庫執行時間點還原，請改用 **Start AzureSqlDatabaseRestore** Cmdlet。

## 示例

### 範例1：復原指定為物件的資料庫
```
PS C:\> $Database = Get-AzureSqlRecoverableDatabase -ServerName "Server01" -DatabaseName "Database17" 
PS C:\> $Operation = Start-AzureSqlDatabaseRecovery -SourceDatabase $Database -TargetDatabaseName "DatabaseRestored"
```

第一個命令會使用 **AzureSqlRecoverableDatabase** Cmdlet 取得資料庫物件。
該命令會將該物件儲存在 $Database 變數中。

第二個命令會恢復儲存在 $Database 中的資料庫。

### 範例2：復原名稱指定的資料庫
```
PS C:\> $Operation = Start-AzureSqlDatabaseRecovery -SourceServerName "Server01" -SourceDatabaseName "Database17" -TargetDatabaseName "DatabaseRestored"
```

這個命令會使用資料庫名稱來恢復資料庫。

## 參數

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

### -SourceDatabase
指定代表此 Cmdlet 所恢復之資料庫的資料庫物件。

```yaml
Type: RecoverableDatabase
Parameter Sets: BySourceDatabaseObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SourceDatabaseName
指定此 Cmdlet 要恢復的資料庫的名稱。

```yaml
Type: String
Parameter Sets: BySourceDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceServerName
指定源資料庫處於即時及正在執行的伺服器名稱，或在刪除之前執行源資料庫的伺服器名稱。

```yaml
Type: String
Parameter Sets: BySourceDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetDatabaseName
指定復原資料庫的名稱。
如果來源資料庫仍在使用中，若要將其復原至同一個伺服器，您必須指定與源資料庫名稱不同的名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetServerName
指定要還原資料庫的伺服器名稱。
您可以將資料庫還原至同一個伺服器或另一個伺服器。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### RecoverableDatabase （WindowsAzure）。

## 輸出

### RecoverDatabaseOperation （WindowsAzure）。

## 筆記
* 您必須使用以憑證為基礎的驗證才能執行這個 Cmdlet。 在執行此 Cmdlet 的電腦上執行下列命令： 

`PS C:\\\> $subId = \<Subscription ID\>`
`PS C:\\\> $thumbprint = \<Certificate Thumbprint\>`
`PS C:\\\> $myCert = Get-Item Cert:\CurrentUser\My\$thumbprint`
`PS C:\\\> Set-AzureSubscription -SubscriptionName "mySubscription" -SubscriptionId $subId -Certificate $myCert`
`PS C:\\\> Select-AzureSubscription -SubscriptionName "mySubscription"`

## 相關連結

[Azure SQL 資料庫](https://azure.microsoft.com/en-us/services/sql-database/)

[建立資料庫恢復要求](https://msdn.microsoft.com/en-us/library/dn800986.aspx)

[Azure SQL Database 中的異地複製](https://azure.microsoft.com/en-us/documentation/articles/sql-database-business-continuity-scenarios/)

[Azure SQL 資料庫的作業](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[AzureSqlRecoverableDatabase](./Get-AzureSqlRecoverableDatabase.md)

[開始-AzureSqlDatabaseRestore](./Start-AzureSqlDatabaseRestore.md)


