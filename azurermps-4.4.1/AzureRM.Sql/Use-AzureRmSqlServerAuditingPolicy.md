---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 381F5B34-983C-4733-B384-35D6579B79A2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Use-AzureRmSqlServerAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Use-AzureRmSqlServerAuditingPolicy.md
ms.openlocfilehash: 9e3e94109904bc14f22e2ca2c08936316ed597db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451583"
---
# Use-AzureRmSqlServerAuditingPolicy

## 摘要
指定資料庫使用其主機伺服器的審核原則。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Use-AzureRmSqlServerAuditingPolicy [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzureRmSqlServerAuditingPolicy** Cmdlet 會指定資料庫使用其主機伺服器的審核原則。
指定 [ *ResourceGroupName* ]、[ *伺服器名稱* ] 和 [ *DatabaseName* ] 參數來識別資料庫。
如果沒有為資料庫伺服器定義審核原則，此 Cmdlet 會失敗。

如果主機使用伺服器層級審核，就會移除威脅偵測。

## 示例

### 範例1：將資料庫設定為使用其伺服器的審核原則
```
PS C:\>Use-AzureRmSqlServerAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server02" -DatabaseName "Database01"
```

這個命令指定 Server02 上名為 Database01 的資料庫會使用伺服器的審核原則。

## 參數

### -DatabaseName
指定將使用審核原則之資料庫的名稱。

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

### -ResourceGroupName
指定指派給伺服器之資源群組的名稱。

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
指定託管使用審核原則之資料庫的伺服器名稱。

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

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。

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

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

## 輸出

### DatabaseAuditingPolicyModel 中的 [.Sql.]

## 筆記

## 相關連結

[AzureRmSqlDatabaseAuditingPolicy](./Get-AzureRmSqlDatabaseAuditingPolicy.md)

[AzureRmSqlServerAuditingPolicy](./Get-AzureRmSqlServerAuditingPolicy.md)

[Set-AzureRmSqlDatabaseAuditingPolicy](./Set-AzureRmSqlDatabaseAuditingPolicy.md)

[Set-AzureRmSqlServerAuditingPolicy](./Set-AzureRmSqlServerAuditingPolicy.md)

[SQL 資料庫檔](https://docs.microsoft.com/azure/sql-database/)


