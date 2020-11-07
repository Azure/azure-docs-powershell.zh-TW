---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2E7E20CD-6A2B-455E-9476-8E0827429162
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlservercommunicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerCommunicationLink.md
ms.openlocfilehash: b2d4d5e86870bf0c69e506f387f6309dbcc8af7a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792759"
---
# Get-AzSqlServerCommunicationLink

## 摘要
取得資料庫伺服器間彈性資料庫事務的通訊連結。

## 句法

```
Get-AzSqlServerCommunicationLink [[-LinkName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明
**AzSqlServerCommunicationLink** Cmdlet 會針對 Azure SQL 資料庫中彈性資料庫交易取得伺服器對伺服器通訊連結。
指定伺服器通訊連結的名稱，以查看該連結的屬性。

## 示例

### 範例1：取得伺服器的所有通訊連結
```
PS C:\> Get-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17"
```

這個命令會針對名為 ContosoServer17 的伺服器，取得彈性資料庫事務的所有伺服器與伺服器通訊連結。

### 範例2：取得伺服器的特定通訊連結
```
PS C:\> Get-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01"
```

這個命令會取得名為 Link01 的伺服器到伺服器通訊連結。

### 範例3：使用篩選取得伺服器的所有通訊連結
```
PS C:\> Get-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link*"
```

這個命令會針對以「連結」開頭的伺服器（名為 ContosoServer17）取得彈性資料庫交易的所有伺服器到伺服器通訊連結。

## 參數

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

### -LinkName
指定此 Cmdlet 所取得之伺服器通訊連結的名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### -ResourceGroupName
指定 *ServerName* 參數所指定之伺服器所屬之資源群組的名稱。

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
指定伺服器的名稱。
此伺服器包含此 Cmdlet 取得的通訊連結。

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
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。

## 輸入

### System.object

## 輸出

### AzureSqlServerCommunicationLinkModel 中的 [ServerCommunicationLink]

## 筆記
* 關鍵字： azure、azurerm、arm、資源、管理、manager、sql、database、mssql

## 相關連結

[新-AzSqlServerCommunicationLink](./New-AzSqlServerCommunicationLink.md)

[移除-AzSqlServerCommunicationLink](./Remove-AzSqlServerCommunicationLink.md)

[SQL 資料庫檔](https://docs.microsoft.com/azure/sql-database/)
