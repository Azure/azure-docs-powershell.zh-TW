---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/update-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Update-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Update-AzBlockchainTransactionNode.md
ms.openlocfilehash: dcff41ecac3181da09ee2f1cf0673e4225c2802d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127962"
---
# Update-AzBlockchainTransactionNode

## 摘要
更新交易節點。

## 句法

### UpdateExpanded (預設) 
```
Update-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-FirewallRule <IFirewallRule[]>] [-Password <SecureString>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### UpdateViaIdentityExpanded
```
Update-AzBlockchainTransactionNode -InputObject <IBlockchainIdentity> [-FirewallRule <IFirewallRule[]>]
 [-Password <SecureString>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## 說明
更新交易節點。

## 示例

### 範例1：更新 transcation 節點
```powershell
PS C:\> $tag = @{'key1'='update'}
PS C:\> Update-AzBlockchainTransactionNode -BlockchainMemberName dolauli002 -Name transacnode002 -ResourceGroupName testgroup -Tag $tag

Name           Type                                                    Location
----           ----                                                    --------
transacnode002 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

這個命令會更新交易節點。

### 範例2：更新 transcation 節點
```powershell
PS C:\> $tag = @{'key2'='update'}
PS C:\> $tNode = Get-AzBlockchainMember -BlockchainMemberName dolauli002 -ResourceGroupName testgroup -Name transacnode002
PS C:\> Update-AzBlockchainTransactionNode -InputObject $tNode -Tag $tag

Name           Type                                                    Location
----           ----                                                    --------
transacnode002 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

這個命令會更新交易節點。

## 參數

### -BlockchainMemberName
Blockchain 成員名稱。

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FirewallRule
取得或設定防火牆規則。
若要建立，請參閱 FIREWALLRULE 屬性和建立雜湊資料表的備忘稿區段。

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IFirewallRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -名稱
交易節點名稱。

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: TransactionNodeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Password
設定交易節點 dns 端點的基本授權密碼。

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
包含資源之資源群組的名稱。
您可以從 Azure 資源管理器 API 或入口網站取得此值。

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
取得唯一識別 Microsoft Azure 訂閱的訂閱 Id。
訂閱識別碼是每個服務呼叫 URI 的一部分。

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
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
Default value: None
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。

## 輸入

### IBlockchainIdentity （Blockchain）的

## 輸出

### ITransactionNode （Blockchain）。 Api20180601Preview。

## 筆記

別名

複雜的參數屬性

若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。 如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。


FIREWALLRULE <IFirewallRule [] >：取得或設定防火牆規則。
  - `[EndIPAddress <String>]`：取得或設定防火牆規則範圍的結束 IP 位址。
  - `[RuleName <String>]`：取得或設定防火牆規則的名稱。
  - `[StartIPAddress <String>]`：取得或設定防火牆規則範圍的起始 IP 位址。

INPUTOBJECT <IBlockchainIdentity> ：身分識別參數
  - `[BlockchainMemberName <String>]`： Blockchain 成員名稱。
  - `[Id <String>]`：資源身分識別路徑
  - `[Location <String>]`：位置名稱。
  - `[OperationId <String>]`：操作 Id。
  - `[ResourceGroupName <String>]`：包含資源之資源群組的名稱。 您可以從 Azure 資源管理器 API 或入口網站取得此值。
  - `[SubscriptionId <String>]`：取得唯一識別 Microsoft Azure 訂閱的訂閱 Id。 訂閱識別碼是每個服務呼叫 URI 的一部分。
  - `[TransactionNodeName <String>]`：交易節點名稱。

## 相關連結

