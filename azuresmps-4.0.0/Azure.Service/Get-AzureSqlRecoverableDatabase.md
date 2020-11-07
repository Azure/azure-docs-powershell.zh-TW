---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 83E8DAD8-151A-408D-819F-274CB813ABDA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6f9a5753fdf4f87afc6baacbe9fc4c33c9be08ef
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93968005"
---
# Get-AzureSqlRecoverableDatabase

## 摘要
從指定的伺服器取得可復原的資料庫。

## 句法

### AllDatabasesOnGivenServer (預設) 
```
Get-AzureSqlRecoverableDatabase -ServerName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### GivenDatabaseOnGivenServer
```
Get-AzureSqlRecoverableDatabase -ServerName <String> -DatabaseName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### GivenDatabaseObject
```
Get-AzureSqlRecoverableDatabase -Database <RecoverableDatabase> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## 說明
**AzureSqlRecoverableDatabase** Cmdlet 會從指定的伺服器取得可復原的資料庫。
這個 Cmdlet 會在伺服器上取得特定的可復原資料庫或所有可復原的資料庫。

## 示例

### 範例1：取得所有可復原的資料庫
```
PS C:\> Get-AzureSqlRecoverableDatabase -ServerName "Server01"
```

這個命令會取得伺服器上名為 Server01 的所有可復原資料庫。

### 範例2：取得特定的可復原資料庫
```
PS C:\> Get-AzureSqlRecoverableDatabase -ServerName "Server01" -DatabaseName "Database17"
```

這個命令會在名為 Server01 的伺服器上檢索名為 Database17 的資料庫。

## 參數

### -資料庫
指定代表此 Cmdlet 所取得的可復原資料庫的物件。

```yaml
Type: RecoverableDatabase
Parameter Sets: GivenDatabaseObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DatabaseName
指定此 Cmdlet 取得的可復原資料庫的名稱。

```yaml
Type: String
Parameter Sets: GivenDatabaseOnGivenServer
Aliases: 

Required: True
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
指定此 Cmdlet 取得可復原資料庫的伺服器名稱。

```yaml
Type: String
Parameter Sets: AllDatabasesOnGivenServer, GivenDatabaseOnGivenServer
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

### RecoverableDatabase （WindowsAzure）。

## 輸出

### IEnumerable\<Microsoft.WindowsAzure.Management.Sql.Models.RecoverableDatabase\>

## 筆記
* 您必須使用以憑證為基礎的驗證才能執行這個 Cmdlet。 在執行此 Cmdlet 的電腦上執行下列命令： 

`PS C:\\\> $subId = \<Subscription ID\>`
`PS C:\\\> $thumbprint = \<Certificate Thumbprint\>`
`PS C:\\\> $myCert = Get-Item Cert:\CurrentUser\My\$thumbprint`
`PS C:\\\> Set-AzureSubscription -SubscriptionName "mySubscription" -SubscriptionId $subId -Certificate $myCert`
`PS C:\\\> Select-AzureSubscription -SubscriptionName "mySubscription"`

## 相關連結

[Azure SQL 資料庫](https://azure.microsoft.com/en-us/services/sql-database/)

[取得可復原的資料庫](https://msdn.microsoft.com/en-us/library/azure/dn800985.aspx)

[Azure SQL 資料庫的作業](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[開始-AzureSqlDatabaseRecovery](./Start-AzureSqlDatabaseRecovery.md)


