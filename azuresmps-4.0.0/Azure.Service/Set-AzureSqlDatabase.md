---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 82F4DB8F-8DAF-40D2-8031-3EDBF5D08417
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6274d3851042c15791707807471ae1bc6a2733ab
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967311"
---
# Set-AzureSqlDatabase

## 摘要
設定 Azure SQL 資料庫的屬性。

## 句法

### ByNameWithConnectionCoNtext
```
Set-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -DatabaseName <String>
 [-NewDatabaseName <String>] [-Edition <DatabaseEdition>] [-MaxSizeGB <Int32>] [-MaxSizeBytes <Int64>]
 [-ServiceObjective <ServiceObjective>] [-PassThru] [-Force] [-Sync] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByObjectWithConnectionCoNtext
```
Set-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -Database <Database>
 [-NewDatabaseName <String>] [-Edition <DatabaseEdition>] [-MaxSizeGB <Int32>] [-MaxSizeBytes <Int64>]
 [-ServiceObjective <ServiceObjective>] [-PassThru] [-Force] [-Sync] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByNameWithServerName
```
Set-AzureSqlDatabase -ServerName <String> -DatabaseName <String> [-NewDatabaseName <String>]
 [-Edition <DatabaseEdition>] [-MaxSizeGB <Int32>] [-MaxSizeBytes <Int64>]
 [-ServiceObjective <ServiceObjective>] [-PassThru] [-Force] [-Sync] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByObjectWithServerName
```
Set-AzureSqlDatabase -ServerName <String> -Database <Database> [-NewDatabaseName <String>]
 [-Edition <DatabaseEdition>] [-MaxSizeGB <Int32>] [-MaxSizeBytes <Int64>]
 [-ServiceObjective <ServiceObjective>] [-PassThru] [-Force] [-Sync] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## 說明
**AzureSqlDatabase** Cmdlet 會設定 Azure SQL 資料庫的屬性。
您可以依名稱指定資料庫，或透過管線傳送 Azure SQL Database 物件。
您可以依名稱指定伺服器，或傳遞 Azure SQL Database server 連接內容。
執行 **AzureSqlDatabaseServerCoNtext** Cmdlet 來建立連接內容。
如果您依名稱指定伺服器，此 Cmdlet 會使用目前的 Azure 訂閱資訊來驗證要求。

## 示例

### 範例1：使用連接內容變更資料庫的大小
```
PS C:\> $Database01 = Get-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database01"
PS C:\> Set-AzureSqlDatabase -ConnectionContext $Context -Database $Database01 -MaxSizeGB 20
```

這個範例會在 Azure SQL Database server 連接內容 $CoNtext 中，將名為 Database01 的資料庫大小變更為 20 GB。

### 範例2：使用伺服器名稱變更資料庫的大小
```
PS C:\> $Database01 = Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01"
PS C:\> Set-AzureSqlDatabase -ServerName "lpqd0zbr8y" -Database $Database01 -MaxSizeGB 20
```

這個範例會將名為 Database01 的資料庫大小從伺服器中的 [lpqd0zbr8y] 變更為 20 GB。

## 參數

### -ConnectionCoNtext
指定伺服器的連接內容。

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
指定代表此 Cmdlet 所修改之 Azure SQL 資料庫的物件。

```yaml
Type: Database
Parameter Sets: ByObjectWithConnectionContext, ByObjectWithServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DatabaseName
指定此 Cmdlet 所修改之資料庫的名稱。

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

### -Edition
指定 Azure SQL 資料庫的新版本。
有效值為： 

- 所有
- 網站
- 部門
- 空白
- 標準
-  佳

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
允許動作完成，不會提示您進行確認。

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
指定資料庫的新的最大大小（以位元組為單位）。
您可以指定此參數或 *MaxSizeGB* 參數。
根據版本，請參閱 *MaxSizeGB* 參數以取得可接受的值。

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
指定資料庫的新最大大小（以 gb 為限制）。
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

### -NewDatabaseName
指定資料庫的新名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: NewName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
傳回已更新的 Azure SQL 資料庫。

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
指定包含此 Cmdlet 所修改之資料庫的伺服器名稱。

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

### -ServiceObjective
指定代表新服務目標的物件 (此資料庫的效能層級) 。
有效值為： 

- 基本： dd6d99bb-f193-4ec1-86f2-43d3bccbc49c
- 標準 (S0) ： f1173c43-91bd-4aaa-973c-54e79e15235b
- 標準 (S1) ：1b1ebd4d-d903-4baa-97f9-4ea675f5e928
- 標準 (S2) ：455330e1-00cd-488b-b5fa-177c226f28b7
- * 標準 (S3) ：789681b8-ca10-4eb0-bdf2-e0b050601b40
- Premium (P1) ：7203483a-c4fb-4304-9e9f-17c71c904f5d
- Premium (P2) ： a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0
- Premium (P3) ： a7c4c615-cfb1-464b-b252-925be0a19446

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

### -同步處理
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

### SqlDatabase.. Database （WindowsAzure）

## 筆記

## 相關連結

[Azure SQL 資料庫](https://azure.microsoft.com/en-us/services/sql-database/)

[Azure SQL 資料庫的作業](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[更新資料庫](https://msdn.microsoft.com/en-us/library/azure/dn505718.aspx)

[AzureSqlDatabase](./Get-AzureSqlDatabase.md)

[新-AzureSqlDatabase](./New-AzureSqlDatabase.md)

[移除-AzureSqlDatabase](./Remove-AzureSqlDatabase.md)

[新-AzureSqlDatabaseServerCoNtext](./New-AzureSqlDatabaseServerContext.md)


