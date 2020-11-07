---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 4661C479-6E3B-425D-B9D2-B36D7A83130C
online version: ''
schema: 2.0.0
ms.openlocfilehash: c3c55ebd22337a8078f3ae495b3901317f4201e0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967740"
---
# Get-AzureSqlDatabaseImportExportStatus

## 摘要
取得匯入或匯出要求的狀態。

## 句法

### ByConnectionInfo
```
Get-AzureSqlDatabaseImportExportStatus -Username <String> -Password <String> -ServerName <String>
 -RequestId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByRequestObject
```
Get-AzureSqlDatabaseImportExportStatus -Request <ImportExportRequest> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## 說明
**AzureSqlDatabaseImportExportStatus** Cmdlet 會取得匯入或匯出要求的狀態。
Start-AzureSqlDatabaseImport 或 Start-AzureSqlDatabaseExport Cmdlet 會啟動要求。
您可以使用 *request* 參數指定 request 物件，或者您可以使用 *RequestId* 參數以及使用者名稱、 *密碼* 及 *ServerName* 參數來識別 *Username* 要求。

## 示例

### 範例1：取得匯出要求的狀態
```
PS C:\> $ExportRequest = Start-AzureSqlDatabaseExport -SqlConnectionContext $SqlContext -StorageContainer $Container -DatabaseName $DatabaseName -BlobName $BlobName
PS C:\> Get-AzureSqlDatabaseImportExportStatus -Request $ExportRequest
```

第一個命令會建立匯出要求，然後將它儲存在 $ExportRequest 變數中。

第二個命令會取得儲存在 $ExportRequest 中之匯出要求的狀態。

## 參數

### -Password
指定連接至 Azure SQL Database server 所需的密碼。
如果您指定的是 *RequestId* 參數，您必須指定此參數。

```yaml
Type: String
Parameter Sets: ByConnectionInfo
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

### -要求
指定 **ImportExportRequest** 物件。
若要取得匯入或匯出要求物件，請使用 Start-AzureSqlDatabaseImport 或 Start-AzureSqlDatabaseExport Cmdlet。

```yaml
Type: ImportExportRequest
Parameter Sets: ByRequestObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RequestId
指定此 Cmdlet 取得狀態的匯入或匯出作業的 GUID。
如果您指定此 *參數，您* 必須指定使用者名稱、 *密碼* 和 *ServerName* 參數。

```yaml
Type: String
Parameter Sets: ByConnectionInfo
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerName
指定 Azure SQL 資料庫伺服器的名稱。
如果您指定的是 *RequestId* 參數，您必須指定此參數。

```yaml
Type: String
Parameter Sets: ByConnectionInfo
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Username
指定連接至 Azure SQL Database server 所需的使用者名稱。
如果您指定的是 *RequestId* 參數，您必須指定此參數。

```yaml
Type: String
Parameter Sets: ByConnectionInfo
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

## 輸出

### ImportExport. StatusInfo （WindowsAzure） SqlDatabase

## 筆記

## 相關連結

[Azure SQL 資料庫](https://azure.microsoft.com/en-us/services/sql-database/)

[取得匯入匯出資料庫狀態](https://msdn.microsoft.com/en-us/library/azure/dn781289.aspx)

[Azure SQL 資料庫的作業](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[開始-AzureSqlDatabaseExport](./Start-AzureSqlDatabaseExport.md)

[開始-AzureSqlDatabaseImport](./Start-AzureSqlDatabaseImport.md)


