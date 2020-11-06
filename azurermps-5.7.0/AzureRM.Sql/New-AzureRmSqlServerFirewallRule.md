---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 51AF8EFB-F0C1-41E0-BBC5-E48FB1B8672C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerFirewallRule.md
ms.openlocfilehash: cc0d7163b9251037f4127d8fc6894f74f103436b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450440"
---
# New-AzureRmSqlServerFirewallRule

## 摘要
建立 SQL 資料庫伺服器的防火牆規則。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### UserSpecifiedRuleSet
```
New-AzureRmSqlServerFirewallRule -FirewallRuleName <String> -StartIpAddress <String> -EndIpAddress <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### AzureIpRuleSet
```
New-AzureRmSqlServerFirewallRule [-AllowAllAzureIPs] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明
**AzureRmSqlServerFirewallRule** Cmdlet 會為指定的 Azure SQL 資料庫伺服器建立防火牆規則。

## 示例

### 範例1：建立防火牆規則
```
PS C:\>New-AzureRmSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -FirewallRuleName "Rule01" -StartIpAddress "192.168.0.198" -EndIpAddress "192.168.0.199"
ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 192.168.0.198
EndIpAddress      : 192.168.0.199
FirewallRuleName  : Rule01
```

這個命令會在名為 Server01 的伺服器上建立名為 Rule01 的防火牆規則。
規則包含指定的開始和結束 IP 位址。

### 範例2：建立可讓所有 Azure IP 位址存取伺服器的防火牆規則
```
PS C:\>New-AzureRmSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -AllowAllAzureIPs
```

這個命令會在名為 [ResourceGroup01] 的資源群組所屬的伺服器上建立防火牆規則。
由於使用了 *AllowAllAzureIPs* 參數，因此防火牆規則可讓所有的 Azure IP 位址存取伺服器。

## 參數

### -AllowAllAzureIPs
表示此防火牆規則允許所有 Azure IP 位址存取伺服器。
如果您想要使用 *FirewallRuleName* 、 *StartIpAddress* 和 *EndIpAddress* 參數，則無法使用此參數。
如果您想要允許 Azure Ip 存取伺服器，應該在不使用 *FirewallRuleName* 、 *StartIpAddress* 和 *EndIpAddress* 參數的個別 Cmdlet 呼叫中使用這個參數。

```yaml
Type: SwitchParameter
Parameter Sets: AzureIpRuleSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱

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

### -EndIpAddress
指定此規則 IP 位址範圍的結束值。

```yaml
Type: String
Parameter Sets: UserSpecifiedRuleSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FirewallRuleName
指定新防火牆規則的名稱。

```yaml
Type: String
Parameter Sets: UserSpecifiedRuleSet
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
指定指派給伺服器之資源群組的名稱。

```yaml
Type: String
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
指定 [伺服器名稱]，而不是 [完全限定的 DNS 名稱]。

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StartIpAddress
指定防火牆規則 IP 位址範圍的起始值。

```yaml
Type: String
Parameter Sets: UserSpecifiedRuleSet
Aliases:

Required: True
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

### 所有
這個 Cmdlet 不接受任何輸入。

## 輸出

### AzureSqlServerFirewallRuleModel 中的 [FirewallRule]

## 筆記

## 相關連結

[AzureRmSqlServerFirewallRule](./Get-AzureRmSqlServerFirewallRule.md)

[移除-AzureRmSqlServerFirewallRule](./Remove-AzureRmSqlServerFirewallRule.md)

[Set-AzureRmSqlServerFirewallRule](./Set-AzureRmSqlServerFirewallRule.md)

[SQL 資料庫檔](https://docs.microsoft.com/azure/sql-database/)


