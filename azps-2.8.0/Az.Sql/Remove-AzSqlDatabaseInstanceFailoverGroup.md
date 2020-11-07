---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 8027af33b9ea4f4184c10963da69e8be3b4e3961
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792699"
---
# Remove-AzSqlDatabaseInstanceFailoverGroup

## 摘要
移除實例容錯移轉群組。

## 句法

### RemoveIFGDefault (預設) 
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String>
 [-Name] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### 從資源識別碼中移除實例容錯移轉群組
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### 從 AzureSqlInstanceFailoverGroupModel 實例定義中移除實例容錯移轉群組
```
Remove-AzSqlDatabaseInstanceFailoverGroup -InputObject <AzureSqlInstanceFailoverGroupModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明
這個命令會移除具有指定名稱的實例容錯移轉群組，並讓所有資料庫保持不變。 將會從 DNS 登出偵聽程式端點。

應使用實例容錯移轉群組的主要區域來執行命令。

## 示例

### 範例1
```
PS C:\> Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location -Name fg | Remove-AzSqlDatabaseInstanceFailoverGroup
```

移除實例容錯移轉群組。

## 參數

### -DefaultProfile
用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
跳過確認訊息以執行動作。

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

### -InputObject
要移除的實例容錯移轉群組物件

```yaml
Type: AzureSqlInstanceFailoverGroupModel
Parameter Sets: Remove a Instance Failover Group from AzureSqlInstanceFailoverGroupModel instance definition
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -位置
要從中取得實例容錯移轉群組的本機區功能變數名稱稱。

```yaml
Type: String
Parameter Sets: RemoveIFGDefault, Remove a Instance Failover Group from Resource Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -名稱
要移除之實例容錯移轉群組的名稱。

```yaml
Type: String
Parameter Sets: RemoveIFGDefault
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
資源群組的名稱。

```yaml
Type: String
Parameter Sets: RemoveIFGDefault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
要移除之實例容錯移轉群組的資源識別碼。

```yaml
Type: String
Parameter Sets: Remove a Instance Failover Group from Resource Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
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
Default value: None
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### AzureSqlInstanceFailoverGroupModel 中的 [InstanceFailoverGroup]
System.object

## 輸出

### AzureSqlInstanceFailoverGroupModel 中的 [InstanceFailoverGroup]

## 筆記

## 相關連結
