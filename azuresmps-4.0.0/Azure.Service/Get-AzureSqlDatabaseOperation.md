---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 56026A74-A6DC-47A5-9643-5828C3D0E83B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 32219154f2036ee028b05a369c46be1d8e1def87
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967739"
---
# Get-AzureSqlDatabaseOperation

## 摘要
取得 Azure 伺服器上資料庫作業的狀態。

## 句法

### ByConnectionCoNtext (預設) 
```
Get-AzureSqlDatabaseOperation -ConnectionContext <IServerDataServiceContext> [-Database <Database>]
 [-DatabaseName <String>] [-OperationGuid <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByServerName
```
Get-AzureSqlDatabaseOperation -ServerName <String> [-Database <Database>] [-DatabaseName <String>]
 [-OperationGuid <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 說明
**AzureSqlDatabaseOperation** Cmdlet 會取得指定 Azure 伺服器上資料庫作業的狀態。
如果您只指定 *ServerName* 或 *ConnectionCoNtext* 參數，則 Cmdlet 會取得伺服器的所有資料庫作業。
如果您同時使用 *database* 或 *DatabaseName* 參數指定資料庫，此 Cmdlet 會取得指定資料庫的所有操作。
如果您指定的是操作 GUID 以及 *ServerName* 或 *ConnectionCoNtext* ，則此 Cmdlet 會取得單一資料庫操作。

## 示例

### 範例1：取得資料庫所有資料庫作業的狀態
```
PS C:\> $Operations = Get-AzureSqlDatabaseOperation -ConnectionContext $Context -DatabaseName "Database17"
```

這個命令會取得伺服器上名為 Database17 的所有資料庫作業的狀態，而該伺服器已在連接內容 $CoNtext 指定的資料庫上。

### 範例2：取得伺服器所有資料庫作業的狀態
```
PS C:\> $Operations = Get-AzureSqlDatabaseOperation -ConnectionContext $Context
```

這個命令會在伺服器上取得連接內容 $CoNtext 指定的所有資料庫作業狀態。

## 參數

### -ConnectionCoNtext
指定伺服器的連接內容。

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByConnectionContext
Aliases: Context

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -資料庫
指定代表 Azure SQL 資料庫的物件。
如果您指定此參數，您必須指定 *ServerName* 參數或 *ConnectionCoNtext* 參數。

```yaml
Type: Database
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DatabaseName
指定資料庫的名稱。
如果您指定此參數，您必須指定 *ServerName* 參數或 *ConnectionCoNtext* 參數。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OperationGuid
指定代表此 Cmdlet 取得狀態之特定資料庫作業的操作 ID。
您可以要求 Azure SQL 資料庫或伺服器的所有資料庫作業來取得作業 Id。
如果您指定此參數，您必須指定 *ServerName* 參數或 *ConnectionCoNtext* 參數。

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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
指定伺服器的名稱。

```yaml
Type: String
Parameter Sets: ByServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### SqlDatabase.. Database （WindowsAzure）

### WindowsAzure. SqlDatabase. SqlDatabaseServerCoNtext

### Guid.empty

## 輸出

### DatabaseOperationResponseList [] SqlDatabase. WindowsAzure. []
如果您有多個作業，這個 Cmdlet 就會傳回 **DatabaseOperationResponseList** 物件的陣列。

### SqlDatabase. DatabaseOperationResponse （WindowsAzure）的

## 筆記

## 相關連結

[Azure SQL 資料庫](https://msdn.microsoft.com/library/ee336279.aspx)

[資料庫操作狀態](https://msdn.microsoft.com/en-us/library/azure/dn720371.aspx)

[Azure SQL 資料庫的作業](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[AzureSqlDatabase](./Get-AzureSqlDatabase.md)

[新-AzureSqlDatabaseServerCoNtext](./New-AzureSqlDatabaseServerContext.md)


