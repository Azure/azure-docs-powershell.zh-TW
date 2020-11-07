---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: A2C22A8A-EF50-4BE3-82DF-5ED6F69C00CA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 457775a74fb7921a3c8b6b5e635bd7df7e704faa
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967014"
---
# Get-AzureSqlDatabaseServiceObjective

## 摘要
取得 Azure SQL 資料庫伺服器的服務目標。

## 句法

### ByConnectionCoNtext (預設) 
```
Get-AzureSqlDatabaseServiceObjective -Context <IServerDataServiceContext>
 [-ServiceObjective <ServiceObjective>] [-ServiceObjectiveName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### ByServerName
```
Get-AzureSqlDatabaseServiceObjective -ServerName <String> [-ServiceObjective <ServiceObjective>]
 [-ServiceObjectiveName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 說明
**AzureSqlDatabaseServiceObjective** Cmdlet 會取得 Azure SQL 資料庫伺服器的服務目標。
服務目標稱為效能等級。
如果您沒有指定服務目標，這個 Cmdlet 會傳回指定伺服器的所有有效服務目標。

這個 Cmdlet 適用于基本、標準和 Premium 服務層級。

## 示例

### 範例1：使用連接內容取得所有服務目標
```
PS C:\> Get-AzureSqlDatabaseServiceObjective -Context $Context
```

這個命令會取得連接內容 $CoNtext 所指定之伺服器的所有服務目標。

### 範例2：使用伺服器名稱取得所有服務目標
```
PS C:\> Get-AzureSqlDatabaseServiceObjective -ServerName "Server01"
```

這個命令會取得伺服器名為 Server01 的所有服務目標。

## 參數

### -內容
指定伺服器的連接內容。

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByConnectionContext
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
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

### -ServiceObjective
指定代表此 Cmdlet 所取得之服務目標的物件。
有效值為： 

- 基本： dd6d99bb-f193-4ec1-86f2-43d3bccbc49c
- 標準 (S0) ： f1173c43-91bd-4aaa-973c-54e79e15235b
- 標準 (S1) ：1b1ebd4d-d903-4baa-97f9-4ea675f5e928
- 標準 (S2) ：455330e1-00cd-488b-b5fa-177c226f28b7
- * 標準 (S3) ：789681b8-ca10-4eb0-bdf2-e0b050601b40
- Premium (P1) ：7203483a-c4fb-4304-9e9f-17c71c904f5d
- Premium (P1) ：7203483a-c4fb-4304-9e9f-17c71c904f5d
- Premium (P2) ： a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0
- Premium (P3) ： a7c4c615-cfb1-464b-b252-925be0a19446

* 標準 (S3) 是最新的 SQL 資料庫更新 V12 (preview) 的一部分。
如需詳細資訊，請參閱 azure [SQL 資料庫 V12 Preview 中的新功能](https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/) (`https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/` azure library 中的) 。

```yaml
Type: ServiceObjective
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ServiceObjectiveName
指定要取得之服務目標的名稱。
有效值為： Basic、S0、S1、S2、S3、P1、P2 及 P3。

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

### SqlDatabase. ServiceObjective （WindowsAzure）

## 輸出

### IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.ServiceObjective\>

## 筆記

## 相關連結

[Azure SQL 資料庫](https://msdn.microsoft.com/library/ee336279.aspx)

[取得服務層級目標](https://msdn.microsoft.com/en-us/library/azure/dn505709.aspx)

[Azure SQL 資料庫的作業](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[新-AzureSqlDatabaseServerCoNtext](./New-AzureSqlDatabaseServerContext.md)


