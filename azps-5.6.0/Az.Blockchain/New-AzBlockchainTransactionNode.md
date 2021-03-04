---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/powershell/module/az.blockchain/new-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNode.md
ms.openlocfilehash: 78d3d6449eb5a487c6c4a8a60a732c30fa502600
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905202"
---
# <span data-ttu-id="885af-101">New-AzBlockchainTransactionNode</span><span class="sxs-lookup"><span data-stu-id="885af-101">New-AzBlockchainTransactionNode</span></span>

## <span data-ttu-id="885af-102">簡介</span><span class="sxs-lookup"><span data-stu-id="885af-102">SYNOPSIS</span></span>
<span data-ttu-id="885af-103">建立或更新交易節點。</span><span class="sxs-lookup"><span data-stu-id="885af-103">Create or update the transaction node.</span></span>

## <span data-ttu-id="885af-104">語法</span><span class="sxs-lookup"><span data-stu-id="885af-104">SYNTAX</span></span>

```
New-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-FirewallRule <IFirewallRule[]>] [-Location <String>] [-Password <SecureString>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="885af-105">描述</span><span class="sxs-lookup"><span data-stu-id="885af-105">DESCRIPTION</span></span>
<span data-ttu-id="885af-106">建立或更新交易節點。</span><span class="sxs-lookup"><span data-stu-id="885af-106">Create or update the transaction node.</span></span>

## <span data-ttu-id="885af-107">例子</span><span class="sxs-lookup"><span data-stu-id="885af-107">EXAMPLES</span></span>

### <span data-ttu-id="885af-108">範例 1：建立位點交易節點</span><span class="sxs-lookup"><span data-stu-id="885af-108">Example 1: Create a blockchain transaction node</span></span>
```powershell
PS C:\> $passwd = 'strongMemberAccountPassword@1' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -Name tranctionnode001 -ResourceGroupName testgroup -Location eastus -Password $passwd

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="885af-109">此命令會建立一個位點交易節點。</span><span class="sxs-lookup"><span data-stu-id="885af-109">This command creates a blockchain transaction node.</span></span>

## <span data-ttu-id="885af-110">參數</span><span class="sxs-lookup"><span data-stu-id="885af-110">PARAMETERS</span></span>

### <span data-ttu-id="885af-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="885af-111">-AsJob</span></span>
<span data-ttu-id="885af-112">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="885af-112">Run the command as a job</span></span>

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

### <span data-ttu-id="885af-113">-有一個產品名稱</span><span class="sxs-lookup"><span data-stu-id="885af-113">-BlockchainMemberName</span></span>
<span data-ttu-id="885af-114">進位成員名稱。</span><span class="sxs-lookup"><span data-stu-id="885af-114">Blockchain member name.</span></span>

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

### <span data-ttu-id="885af-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="885af-115">-DefaultProfile</span></span>
<span data-ttu-id="885af-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="885af-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="885af-117">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="885af-117">-FirewallRule</span></span>
<span data-ttu-id="885af-118">獲取或設定防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="885af-118">Gets or sets the firewall rules.</span></span>
<span data-ttu-id="885af-119">若要建構，請參閱 FIREWALLRULE 屬性的附注區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="885af-119">To construct, see NOTES section for FIREWALLRULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="885af-120">-位置</span><span class="sxs-lookup"><span data-stu-id="885af-120">-Location</span></span>
<span data-ttu-id="885af-121">獲取或設定交易節點位置。</span><span class="sxs-lookup"><span data-stu-id="885af-121">Gets or sets the transaction node location.</span></span>

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

### <span data-ttu-id="885af-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="885af-122">-Name</span></span>
<span data-ttu-id="885af-123">交易節點名稱。</span><span class="sxs-lookup"><span data-stu-id="885af-123">Transaction node name.</span></span>

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

### <span data-ttu-id="885af-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="885af-124">-NoWait</span></span>
<span data-ttu-id="885af-125">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="885af-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="885af-126">-密碼</span><span class="sxs-lookup"><span data-stu-id="885af-126">-Password</span></span>
<span data-ttu-id="885af-127">設定交易節點 dns 端點的基本驗證密碼。</span><span class="sxs-lookup"><span data-stu-id="885af-127">Sets the transaction node dns endpoint basic auth password.</span></span>

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

### <span data-ttu-id="885af-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="885af-128">-ResourceGroupName</span></span>
<span data-ttu-id="885af-129">包含資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="885af-129">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="885af-130">您可以從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="885af-130">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="885af-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="885af-131">-SubscriptionId</span></span>
<span data-ttu-id="885af-132">獲得可唯一識別 Microsoft Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="885af-132">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="885af-133">訂閱識別碼是每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="885af-133">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="885af-134">-確認</span><span class="sxs-lookup"><span data-stu-id="885af-134">-Confirm</span></span>
<span data-ttu-id="885af-135">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="885af-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="885af-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="885af-136">-WhatIf</span></span>
<span data-ttu-id="885af-137">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="885af-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="885af-138">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="885af-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="885af-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="885af-139">CommonParameters</span></span>
<span data-ttu-id="885af-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="885af-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="885af-141">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="885af-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="885af-142">輸入</span><span class="sxs-lookup"><span data-stu-id="885af-142">INPUTS</span></span>

## <span data-ttu-id="885af-143">輸出</span><span class="sxs-lookup"><span data-stu-id="885af-143">OUTPUTS</span></span>

### <span data-ttu-id="885af-144">Microsoft.Azure.PowerShell.Cmdlets.Azure.Models.Api20180601Preview.ITransactionNode</span><span class="sxs-lookup"><span data-stu-id="885af-144">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.ITransactionNode</span></span>

## <span data-ttu-id="885af-145">筆記</span><span class="sxs-lookup"><span data-stu-id="885af-145">NOTES</span></span>

<span data-ttu-id="885af-146">別名</span><span class="sxs-lookup"><span data-stu-id="885af-146">ALIASES</span></span>

<span data-ttu-id="885af-147">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="885af-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="885af-148">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="885af-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="885af-149">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="885af-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="885af-150">FIREWALLRULE <IFirewallRule[]>：獲取或設定防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="885af-150">FIREWALLRULE <IFirewallRule[]>: Gets or sets the firewall rules.</span></span>
  - <span data-ttu-id="885af-151">`[EndIPAddress <String>]`：獲取或設定防火牆規則範圍的結束 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="885af-151">`[EndIPAddress <String>]`: Gets or sets the end IP address of the firewall rule range.</span></span>
  - <span data-ttu-id="885af-152">`[RuleName <String>]`：獲取或設定防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="885af-152">`[RuleName <String>]`: Gets or sets the name of the firewall rules.</span></span>
  - <span data-ttu-id="885af-153">`[StartIPAddress <String>]`：獲取或設定防火牆規則範圍的起始 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="885af-153">`[StartIPAddress <String>]`: Gets or sets the start IP address of the firewall rule range.</span></span>

## <span data-ttu-id="885af-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="885af-154">RELATED LINKS</span></span>

