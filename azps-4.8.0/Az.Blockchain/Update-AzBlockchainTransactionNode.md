---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/update-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Update-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Update-AzBlockchainTransactionNode.md
ms.openlocfilehash: dcff41ecac3181da09ee2f1cf0673e4225c2802d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93971492"
---
# <span data-ttu-id="16634-101">Update-AzBlockchainTransactionNode</span><span class="sxs-lookup"><span data-stu-id="16634-101">Update-AzBlockchainTransactionNode</span></span>

## <span data-ttu-id="16634-102">摘要</span><span class="sxs-lookup"><span data-stu-id="16634-102">SYNOPSIS</span></span>
<span data-ttu-id="16634-103">更新交易節點。</span><span class="sxs-lookup"><span data-stu-id="16634-103">Update the transaction node.</span></span>

## <span data-ttu-id="16634-104">句法</span><span class="sxs-lookup"><span data-stu-id="16634-104">SYNTAX</span></span>

### <span data-ttu-id="16634-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="16634-105">UpdateExpanded (Default)</span></span>
```
Update-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-FirewallRule <IFirewallRule[]>] [-Password <SecureString>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="16634-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="16634-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzBlockchainTransactionNode -InputObject <IBlockchainIdentity> [-FirewallRule <IFirewallRule[]>]
 [-Password <SecureString>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="16634-107">說明</span><span class="sxs-lookup"><span data-stu-id="16634-107">DESCRIPTION</span></span>
<span data-ttu-id="16634-108">更新交易節點。</span><span class="sxs-lookup"><span data-stu-id="16634-108">Update the transaction node.</span></span>

## <span data-ttu-id="16634-109">示例</span><span class="sxs-lookup"><span data-stu-id="16634-109">EXAMPLES</span></span>

### <span data-ttu-id="16634-110">範例1：更新 transcation 節點</span><span class="sxs-lookup"><span data-stu-id="16634-110">Example 1: Update a transcation node</span></span>
```powershell
PS C:\> $tag = @{'key1'='update'}
PS C:\> Update-AzBlockchainTransactionNode -BlockchainMemberName dolauli002 -Name transacnode002 -ResourceGroupName testgroup -Tag $tag

Name           Type                                                    Location
----           ----                                                    --------
transacnode002 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="16634-111">這個命令會更新交易節點。</span><span class="sxs-lookup"><span data-stu-id="16634-111">This command updates a transaction node.</span></span>

### <span data-ttu-id="16634-112">範例2：更新 transcation 節點</span><span class="sxs-lookup"><span data-stu-id="16634-112">Example 2: Update a transcation node</span></span>
```powershell
PS C:\> $tag = @{'key2'='update'}
PS C:\> $tNode = Get-AzBlockchainMember -BlockchainMemberName dolauli002 -ResourceGroupName testgroup -Name transacnode002
PS C:\> Update-AzBlockchainTransactionNode -InputObject $tNode -Tag $tag

Name           Type                                                    Location
----           ----                                                    --------
transacnode002 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="16634-113">這個命令會更新交易節點。</span><span class="sxs-lookup"><span data-stu-id="16634-113">This command updates a transaction node.</span></span>

## <span data-ttu-id="16634-114">參數</span><span class="sxs-lookup"><span data-stu-id="16634-114">PARAMETERS</span></span>

### <span data-ttu-id="16634-115">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="16634-115">-BlockchainMemberName</span></span>
<span data-ttu-id="16634-116">Blockchain 成員名稱。</span><span class="sxs-lookup"><span data-stu-id="16634-116">Blockchain member name.</span></span>

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

### <span data-ttu-id="16634-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16634-117">-DefaultProfile</span></span>
<span data-ttu-id="16634-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="16634-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16634-119">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="16634-119">-FirewallRule</span></span>
<span data-ttu-id="16634-120">取得或設定防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="16634-120">Gets or sets the firewall rules.</span></span>
<span data-ttu-id="16634-121">若要建立，請參閱 FIREWALLRULE 屬性和建立雜湊資料表的備忘稿區段。</span><span class="sxs-lookup"><span data-stu-id="16634-121">To construct, see NOTES section for FIREWALLRULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="16634-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="16634-122">-InputObject</span></span>
<span data-ttu-id="16634-123">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="16634-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="16634-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="16634-124">-Name</span></span>
<span data-ttu-id="16634-125">交易節點名稱。</span><span class="sxs-lookup"><span data-stu-id="16634-125">Transaction node name.</span></span>

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

### <span data-ttu-id="16634-126">-Password</span><span class="sxs-lookup"><span data-stu-id="16634-126">-Password</span></span>
<span data-ttu-id="16634-127">設定交易節點 dns 端點的基本授權密碼。</span><span class="sxs-lookup"><span data-stu-id="16634-127">Sets the transaction node dns endpoint basic auth password.</span></span>

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

### <span data-ttu-id="16634-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16634-128">-ResourceGroupName</span></span>
<span data-ttu-id="16634-129">包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="16634-129">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="16634-130">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="16634-130">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="16634-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="16634-131">-SubscriptionId</span></span>
<span data-ttu-id="16634-132">取得唯一識別 Microsoft Azure 訂閱的訂閱 Id。</span><span class="sxs-lookup"><span data-stu-id="16634-132">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="16634-133">訂閱識別碼是每個服務呼叫 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="16634-133">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="16634-134">-確認</span><span class="sxs-lookup"><span data-stu-id="16634-134">-Confirm</span></span>
<span data-ttu-id="16634-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="16634-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16634-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16634-136">-WhatIf</span></span>
<span data-ttu-id="16634-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="16634-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16634-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="16634-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16634-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16634-139">CommonParameters</span></span>
<span data-ttu-id="16634-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="16634-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16634-141">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="16634-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16634-142">輸入</span><span class="sxs-lookup"><span data-stu-id="16634-142">INPUTS</span></span>

### <span data-ttu-id="16634-143">IBlockchainIdentity （Blockchain）的</span><span class="sxs-lookup"><span data-stu-id="16634-143">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="16634-144">輸出</span><span class="sxs-lookup"><span data-stu-id="16634-144">OUTPUTS</span></span>

### <span data-ttu-id="16634-145">ITransactionNode （Blockchain）。 Api20180601Preview。</span><span class="sxs-lookup"><span data-stu-id="16634-145">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.ITransactionNode</span></span>

## <span data-ttu-id="16634-146">筆記</span><span class="sxs-lookup"><span data-stu-id="16634-146">NOTES</span></span>

<span data-ttu-id="16634-147">別名</span><span class="sxs-lookup"><span data-stu-id="16634-147">ALIASES</span></span>

<span data-ttu-id="16634-148">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="16634-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="16634-149">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="16634-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="16634-150">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="16634-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="16634-151">FIREWALLRULE <IFirewallRule [] >：取得或設定防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="16634-151">FIREWALLRULE <IFirewallRule[]>: Gets or sets the firewall rules.</span></span>
  - <span data-ttu-id="16634-152">`[EndIPAddress <String>]`：取得或設定防火牆規則範圍的結束 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="16634-152">`[EndIPAddress <String>]`: Gets or sets the end IP address of the firewall rule range.</span></span>
  - <span data-ttu-id="16634-153">`[RuleName <String>]`：取得或設定防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="16634-153">`[RuleName <String>]`: Gets or sets the name of the firewall rules.</span></span>
  - <span data-ttu-id="16634-154">`[StartIPAddress <String>]`：取得或設定防火牆規則範圍的起始 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="16634-154">`[StartIPAddress <String>]`: Gets or sets the start IP address of the firewall rule range.</span></span>

<span data-ttu-id="16634-155">INPUTOBJECT <IBlockchainIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="16634-155">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="16634-156">`[BlockchainMemberName <String>]`： Blockchain 成員名稱。</span><span class="sxs-lookup"><span data-stu-id="16634-156">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="16634-157">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="16634-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="16634-158">`[Location <String>]`：位置名稱。</span><span class="sxs-lookup"><span data-stu-id="16634-158">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="16634-159">`[OperationId <String>]`：操作 Id。</span><span class="sxs-lookup"><span data-stu-id="16634-159">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="16634-160">`[ResourceGroupName <String>]`：包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="16634-160">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="16634-161">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="16634-161">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="16634-162">`[SubscriptionId <String>]`：取得唯一識別 Microsoft Azure 訂閱的訂閱 Id。</span><span class="sxs-lookup"><span data-stu-id="16634-162">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="16634-163">訂閱識別碼是每個服務呼叫 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="16634-163">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="16634-164">`[TransactionNodeName <String>]`：交易節點名稱。</span><span class="sxs-lookup"><span data-stu-id="16634-164">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="16634-165">相關連結</span><span class="sxs-lookup"><span data-stu-id="16634-165">RELATED LINKS</span></span>

