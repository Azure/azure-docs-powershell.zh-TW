---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: F4FE79DB-B481-49BD-A33B-7C642A136890
online version: ''
schema: 2.0.0
ms.openlocfilehash: 588fcf73c258364e41117eed05c62de7eaa231e9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967419"
---
# New-AzureSqlDatabase

## 摘要
建立 Azure SQL 資料庫。

## 句法

### ByConnectionCoNtext
```
New-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -DatabaseName <String>
 [-Collation <String>] [-Edition <DatabaseEdition>] [-ServiceObjective <ServiceObjective>] [-MaxSizeGB <Int32>]
 [-MaxSizeBytes <Int64>] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByServerName
```
New-AzureSqlDatabase -ServerName <String> -DatabaseName <String> [-Collation <String>]
 [-Edition <DatabaseEdition>] [-ServiceObjective <ServiceObjective>] [-MaxSizeGB <Int32>]
 [-MaxSizeBytes <Int64>] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明
**新的-AzureSqlDatabase** Cmdlet 會建立 Azure SQL 資料庫。
您可以使用您使用 **AzureSqlDatabaseServerCoNtext** Cmdlet 建立的 Azure SQL Database server 連接內容來指定伺服器。
或者，如果您指定伺服器名稱，此 Cmdlet 會使用目前的 Azure 訂閱資訊來驗證存取伺服器的要求。

當您透過指定 Azure SQL 資料庫伺服器建立新資料庫時， **新的 AzureSqlDatabase** Cmdlet 會使用指定的伺服器名稱和目前的 Azure 訂閱資訊來建立暫時的線上內容，以執行操作。

## 示例

### 範例1：建立資料庫
```
PS C:\> $Database01 = New-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database01" -Edition "Business" -MaxSizeGB 50 -Collation "SQL_Latin1_General_CP1_CI_AS"
```

這個命令會建立一個名為 Database1 的 Azure SQL 資料庫，以供 Azure SQL Database server 連接內容 $CoNtext 使用。

### 範例2：在目前的訂閱中建立資料庫
```
PS C:\> $Database01 = New-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01" -Edition "Business" -MaxSizeGB 50 -Collation "SQL_Latin1_General_CP1_CI_AS"
```

這個範例會在指定的 Azure SQL 資料庫伺服器（名為 lpqd0zbr8y）中建立名為 Database1 的資料庫。
此 Cmdlet 會使用目前的 Azure 訂閱資訊來驗證存取伺服器的要求。

## 參數

### -排序規則
指定新資料庫的排序規則。

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

### -ConnectionCoNtext
指定此 Cmdlet 建立資料庫的伺服器連接內容。

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByConnectionContext
Aliases: Context

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DatabaseName
指定新資料庫的名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Edition
指定新 Azure SQL 資料庫的版本。
有效值為： 

- 所有
- 網站
- 部門
- 空白
- 標準
-  佳

預設值為 [Web]。

```yaml
Type: DatabaseEdition
Parameter Sets: (All)
Aliases: 

Required: False
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

### -MaxSizeBytes
指定資料庫的最大大小（以位元組為單位）。
您可以指定此參數或 *MaxSizeGB* 參數。
根據版本，請參閱 *MaxSizeGB* 參數描述，以取得可接受的值。

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxSizeGB
以千百萬位元組指定資料庫的大小上限。
您可以指定此參數或 *MaxSizeBytes* 參數。
根據版本，可接受的值會有所不同。

基本版本值：1或2

標準版值：1、2、5、10、20、30、40、50、100、150、200或250

津貼版本值：1、2、5、10、20、30、40、50、100、150、200、250、300、400或500

網頁版值：1或5

商務版值：10、20、30、40、50、100或150

```yaml
Type: Int32
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
指定要包含新資料庫之 Azure SQL 資料庫伺服器的名稱。

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
指定代表新服務目標的物件 (此資料庫的效能層級) 。
這個值代表指派給此資料庫的資源層級。
有效值為： 

基本： dd6d99bb-f193-4ec1-86f2-43d3bccbc49c 標準 (S0) ： f1173c43-91bd-4aaa-973c-54e79e15235b 標準 (S1) ：1b1ebd4d-d903-4baa-97f9-4ea675f5e928 標準 (S2) ： 455330e1-00cd-488b-b5fa-177c226f28b7 * 標準 (S3) ： 789681b8-ca10-4eb0-bdf2-e0b050601b40 premium (P1) ： 7203483a-c4fb-4304-9e9f-17c71c904f5d Premium () ： 7203483a-c4fb-4304-9e9f-17c71c904f5d Premium (P2) ： a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0 Premium (P3) ： a7c4c615-cfb1-464b-b252-925be0a19446

* 標準 (S3) 是最新的 SQL 資料庫更新 V12 (preview) 的一部分。
如需詳細資訊，請參閱 Azure SQL 資料庫 V12 Preview 的新增功能 https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/ 。

```yaml
Type: ServiceObjective
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

## 輸出

### SqlDatabase.. Database （WindowsAzure）

## 筆記
* 若要刪除由 **新的 AzureSqlDatabase** 所建立的資料庫，請使用 Remove-AzureSqlDatabase Cmdlet。

## 相關連結

[Azure SQL 資料庫](https://azure.microsoft.com/en-us/services/sql-database/)

[建立資料庫](https://msdn.microsoft.com/en-us/library/azure/dn505701.aspx)

[Azure SQL 資料庫的作業](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[AzureSqlDatabase](./Get-AzureSqlDatabase.md)

[新-AzureSqlDatabaseServerCoNtext](./New-AzureSqlDatabaseServerContext.md)

[移除-AzureSqlDatabase](./Remove-AzureSqlDatabase.md)

[Set-AzureSqlDatabase](./Set-AzureSqlDatabase.md)


