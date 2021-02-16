---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/new-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNode.md
ms.openlocfilehash: c5b5e761306c37e67f6b6a2398a5985872722efa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127990"
---
# <span data-ttu-id="5de42-101">New-AzBlockchainTransactionNode</span><span class="sxs-lookup"><span data-stu-id="5de42-101">New-AzBlockchainTransactionNode</span></span>

## <span data-ttu-id="5de42-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5de42-102">SYNOPSIS</span></span>
<span data-ttu-id="5de42-103">建立或更新交易節點。</span><span class="sxs-lookup"><span data-stu-id="5de42-103">Create or update the transaction node.</span></span>

## <span data-ttu-id="5de42-104">句法</span><span class="sxs-lookup"><span data-stu-id="5de42-104">SYNTAX</span></span>

```
New-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-FirewallRule <IFirewallRule[]>] [-Location <String>] [-Password <SecureString>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5de42-105">說明</span><span class="sxs-lookup"><span data-stu-id="5de42-105">DESCRIPTION</span></span>
<span data-ttu-id="5de42-106">建立或更新交易節點。</span><span class="sxs-lookup"><span data-stu-id="5de42-106">Create or update the transaction node.</span></span>

## <span data-ttu-id="5de42-107">示例</span><span class="sxs-lookup"><span data-stu-id="5de42-107">EXAMPLES</span></span>

### <span data-ttu-id="5de42-108">範例1：建立 blockchain 交易節點</span><span class="sxs-lookup"><span data-stu-id="5de42-108">Example 1: Create a blockchain transaction node</span></span>
```powershell
PS C:\> $passwd = 'strongMemberAccountPassword@1' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -Name tranctionnode001 -ResourceGroupName testgroup -Location eastus -Password $passwd

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="5de42-109">這個命令會建立 blockchain 交易節點。</span><span class="sxs-lookup"><span data-stu-id="5de42-109">This command creates a blockchain transaction node.</span></span>

## <span data-ttu-id="5de42-110">參數</span><span class="sxs-lookup"><span data-stu-id="5de42-110">PARAMETERS</span></span>

### <span data-ttu-id="5de42-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5de42-111">-AsJob</span></span>
<span data-ttu-id="5de42-112">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="5de42-112">Run the command as a job</span></span>

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

### <span data-ttu-id="5de42-113">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="5de42-113">-BlockchainMemberName</span></span>
<span data-ttu-id="5de42-114">Blockchain 成員名稱。</span><span class="sxs-lookup"><span data-stu-id="5de42-114">Blockchain member name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5de42-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5de42-115">-DefaultProfile</span></span>
<span data-ttu-id="5de42-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5de42-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5de42-117">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="5de42-117">-FirewallRule</span></span>
<span data-ttu-id="5de42-118">取得或設定防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="5de42-118">Gets or sets the firewall rules.</span></span>
<span data-ttu-id="5de42-119">若要建立，請參閱 FIREWALLRULE 屬性和建立雜湊資料表的備忘稿區段。</span><span class="sxs-lookup"><span data-stu-id="5de42-119">To construct, see NOTES section for FIREWALLRULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="5de42-120">-位置</span><span class="sxs-lookup"><span data-stu-id="5de42-120">-Location</span></span>
<span data-ttu-id="5de42-121">取得或設定交易節點的位置。</span><span class="sxs-lookup"><span data-stu-id="5de42-121">Gets or sets the transaction node location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5de42-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="5de42-122">-Name</span></span>
<span data-ttu-id="5de42-123">交易節點名稱。</span><span class="sxs-lookup"><span data-stu-id="5de42-123">Transaction node name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TransactionNodeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5de42-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="5de42-124">-NoWait</span></span>
<span data-ttu-id="5de42-125">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="5de42-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="5de42-126">-Password</span><span class="sxs-lookup"><span data-stu-id="5de42-126">-Password</span></span>
<span data-ttu-id="5de42-127">設定交易節點 dns 端點的基本授權密碼。</span><span class="sxs-lookup"><span data-stu-id="5de42-127">Sets the transaction node dns endpoint basic auth password.</span></span>

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

### <span data-ttu-id="5de42-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5de42-128">-ResourceGroupName</span></span>
<span data-ttu-id="5de42-129">包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5de42-129">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="5de42-130">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="5de42-130">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5de42-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5de42-131">-SubscriptionId</span></span>
<span data-ttu-id="5de42-132">取得唯一識別 Microsoft Azure 訂閱的訂閱 Id。</span><span class="sxs-lookup"><span data-stu-id="5de42-132">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="5de42-133">訂閱識別碼是每個服務呼叫 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="5de42-133">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5de42-134">-確認</span><span class="sxs-lookup"><span data-stu-id="5de42-134">-Confirm</span></span>
<span data-ttu-id="5de42-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5de42-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5de42-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5de42-136">-WhatIf</span></span>
<span data-ttu-id="5de42-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5de42-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5de42-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5de42-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5de42-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5de42-139">CommonParameters</span></span>
<span data-ttu-id="5de42-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5de42-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5de42-141">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5de42-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5de42-142">輸入</span><span class="sxs-lookup"><span data-stu-id="5de42-142">INPUTS</span></span>

## <span data-ttu-id="5de42-143">輸出</span><span class="sxs-lookup"><span data-stu-id="5de42-143">OUTPUTS</span></span>

### <span data-ttu-id="5de42-144">ITransactionNode （Blockchain）。 Api20180601Preview。</span><span class="sxs-lookup"><span data-stu-id="5de42-144">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.ITransactionNode</span></span>

## <span data-ttu-id="5de42-145">筆記</span><span class="sxs-lookup"><span data-stu-id="5de42-145">NOTES</span></span>

<span data-ttu-id="5de42-146">別名</span><span class="sxs-lookup"><span data-stu-id="5de42-146">ALIASES</span></span>

<span data-ttu-id="5de42-147">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="5de42-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5de42-148">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="5de42-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5de42-149">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="5de42-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5de42-150">FIREWALLRULE <IFirewallRule [] >：取得或設定防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="5de42-150">FIREWALLRULE <IFirewallRule[]>: Gets or sets the firewall rules.</span></span>
  - <span data-ttu-id="5de42-151">`[EndIPAddress <String>]`：取得或設定防火牆規則範圍的結束 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="5de42-151">`[EndIPAddress <String>]`: Gets or sets the end IP address of the firewall rule range.</span></span>
  - <span data-ttu-id="5de42-152">`[RuleName <String>]`：取得或設定防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="5de42-152">`[RuleName <String>]`: Gets or sets the name of the firewall rules.</span></span>
  - <span data-ttu-id="5de42-153">`[StartIPAddress <String>]`：取得或設定防火牆規則範圍的起始 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="5de42-153">`[StartIPAddress <String>]`: Gets or sets the start IP address of the firewall rule range.</span></span>

## <span data-ttu-id="5de42-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="5de42-154">RELATED LINKS</span></span>

