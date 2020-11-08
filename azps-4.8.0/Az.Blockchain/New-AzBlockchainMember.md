---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/new-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMember.md
ms.openlocfilehash: a6bd4f7d8d3058de948d0ecef636c2ec9e1ca1e9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970607"
---
# <span data-ttu-id="a0984-101">New-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="a0984-101">New-AzBlockchainMember</span></span>

## <span data-ttu-id="a0984-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a0984-102">SYNOPSIS</span></span>
<span data-ttu-id="a0984-103">建立 blockchain 成員。</span><span class="sxs-lookup"><span data-stu-id="a0984-103">Create a blockchain member.</span></span>

## <span data-ttu-id="a0984-104">句法</span><span class="sxs-lookup"><span data-stu-id="a0984-104">SYNTAX</span></span>

```
New-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Consortium <String>] [-ConsortiumManagementAccountPassword <SecureString>]
 [-ConsortiumMemberDisplayName <String>] [-ConsortiumRole <String>] [-FirewallRule <IFirewallRule[]>]
 [-Location <String>] [-Password <SecureString>] [-Protocol <BlockchainProtocol>] [-Sku <String>]
 [-SkuTier <String>] [-Tag <Hashtable>] [-ValidatorNodeSkuCapacity <Int32>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a0984-105">說明</span><span class="sxs-lookup"><span data-stu-id="a0984-105">DESCRIPTION</span></span>
<span data-ttu-id="a0984-106">建立 blockchain 成員。</span><span class="sxs-lookup"><span data-stu-id="a0984-106">Create a blockchain member.</span></span>

## <span data-ttu-id="a0984-107">示例</span><span class="sxs-lookup"><span data-stu-id="a0984-107">EXAMPLES</span></span>

### <span data-ttu-id="a0984-108">範例1：建立新的 blockchain 成員</span><span class="sxs-lookup"><span data-stu-id="a0984-108">Example 1: Create a new blockchain member</span></span>
```powershell
PS C:\> $passwd = 'strongMemberAccountPassword@1' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> $csPasswd = 'strongConsortiumManagementPassword@1' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzBlockchainMember -Name dolauli002 -ResourceGroupName testgroup -Consortium consor002 -ConsortiumManagementAccountPassword $csPasswd -Location eastus -Password $passwd -Protocol Quorum -Sku S0

Location Name       Type
-------- ----       ----
eastus   dolauli002 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="a0984-109">這個命令會建立新的 blockchain 成員。</span><span class="sxs-lookup"><span data-stu-id="a0984-109">This command creates a new blockchain member.</span></span>

## <span data-ttu-id="a0984-110">參數</span><span class="sxs-lookup"><span data-stu-id="a0984-110">PARAMETERS</span></span>

### <span data-ttu-id="a0984-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a0984-111">-AsJob</span></span>
<span data-ttu-id="a0984-112">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="a0984-112">Run the command as a job</span></span>

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

### <span data-ttu-id="a0984-113">-聯合會</span><span class="sxs-lookup"><span data-stu-id="a0984-113">-Consortium</span></span>
<span data-ttu-id="a0984-114">取得或設定 blockchain 成員的聯合會。</span><span class="sxs-lookup"><span data-stu-id="a0984-114">Gets or sets the consortium for the blockchain member.</span></span>

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

### <span data-ttu-id="a0984-115">-ConsortiumManagementAccountPassword</span><span class="sxs-lookup"><span data-stu-id="a0984-115">-ConsortiumManagementAccountPassword</span></span>
<span data-ttu-id="a0984-116">設定受管理的聯合會管理帳戶密碼。</span><span class="sxs-lookup"><span data-stu-id="a0984-116">Sets the managed consortium management account password.</span></span>

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

### <span data-ttu-id="a0984-117">-ConsortiumMemberDisplayName</span><span class="sxs-lookup"><span data-stu-id="a0984-117">-ConsortiumMemberDisplayName</span></span>
<span data-ttu-id="a0984-118">取得聯合會中成員的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="a0984-118">Gets the display name of the member in the consortium.</span></span>

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

### <span data-ttu-id="a0984-119">-ConsortiumRole</span><span class="sxs-lookup"><span data-stu-id="a0984-119">-ConsortiumRole</span></span>
<span data-ttu-id="a0984-120">取得聯盟中成員的角色。</span><span class="sxs-lookup"><span data-stu-id="a0984-120">Gets the role of the member in the consortium.</span></span>

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

### <span data-ttu-id="a0984-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0984-121">-DefaultProfile</span></span>
<span data-ttu-id="a0984-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a0984-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0984-123">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="a0984-123">-FirewallRule</span></span>
<span data-ttu-id="a0984-124">取得或設定要構造的防火牆規則，請參閱 FIREWALLRULE 屬性的記事區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="a0984-124">Gets or sets firewall rules To construct, see NOTES section for FIREWALLRULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="a0984-125">-位置</span><span class="sxs-lookup"><span data-stu-id="a0984-125">-Location</span></span>
<span data-ttu-id="a0984-126">Blockchain 服務的地理位置。</span><span class="sxs-lookup"><span data-stu-id="a0984-126">The GEO location of the blockchain service.</span></span>

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

### <span data-ttu-id="a0984-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="a0984-127">-Name</span></span>
<span data-ttu-id="a0984-128">Blockchain 成員名稱。</span><span class="sxs-lookup"><span data-stu-id="a0984-128">Blockchain member name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BlockchainMemberName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0984-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a0984-129">-NoWait</span></span>
<span data-ttu-id="a0984-130">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="a0984-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a0984-131">-Password</span><span class="sxs-lookup"><span data-stu-id="a0984-131">-Password</span></span>
<span data-ttu-id="a0984-132">設定 blockchain 成員的基本驗證密碼。</span><span class="sxs-lookup"><span data-stu-id="a0984-132">Sets the basic auth password of the blockchain member.</span></span>

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

### <span data-ttu-id="a0984-133">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="a0984-133">-Protocol</span></span>
<span data-ttu-id="a0984-134">取得或設定 blockchain 通訊協定。</span><span class="sxs-lookup"><span data-stu-id="a0984-134">Gets or sets the blockchain protocol.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Support.BlockchainProtocol
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0984-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0984-135">-ResourceGroupName</span></span>
<span data-ttu-id="a0984-136">包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a0984-136">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="a0984-137">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="a0984-137">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="a0984-138">-Sku</span><span class="sxs-lookup"><span data-stu-id="a0984-138">-Sku</span></span>
<span data-ttu-id="a0984-139">取得或設定 Sku 名稱</span><span class="sxs-lookup"><span data-stu-id="a0984-139">Gets or sets Sku name</span></span>

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

### <span data-ttu-id="a0984-140">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="a0984-140">-SkuTier</span></span>
<span data-ttu-id="a0984-141">取得或設定 Sku 層</span><span class="sxs-lookup"><span data-stu-id="a0984-141">Gets or sets Sku tier</span></span>

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

### <span data-ttu-id="a0984-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a0984-142">-SubscriptionId</span></span>
<span data-ttu-id="a0984-143">取得唯一識別 Microsoft Azure 訂閱的訂閱 Id。</span><span class="sxs-lookup"><span data-stu-id="a0984-143">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="a0984-144">訂閱識別碼是每個服務呼叫 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="a0984-144">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a0984-145">-Tag</span><span class="sxs-lookup"><span data-stu-id="a0984-145">-Tag</span></span>
<span data-ttu-id="a0984-146">服務的標記，是描述資源的鍵值對清單。</span><span class="sxs-lookup"><span data-stu-id="a0984-146">Tags of the service which is a list of key value pairs that describes the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0984-147">-ValidatorNodeSkuCapacity</span><span class="sxs-lookup"><span data-stu-id="a0984-147">-ValidatorNodeSkuCapacity</span></span>
<span data-ttu-id="a0984-148">取得或設定節點的容量。</span><span class="sxs-lookup"><span data-stu-id="a0984-148">Gets or sets the nodes capacity.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0984-149">-確認</span><span class="sxs-lookup"><span data-stu-id="a0984-149">-Confirm</span></span>
<span data-ttu-id="a0984-150">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a0984-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0984-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0984-151">-WhatIf</span></span>
<span data-ttu-id="a0984-152">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a0984-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0984-153">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a0984-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0984-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0984-154">CommonParameters</span></span>
<span data-ttu-id="a0984-155">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a0984-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0984-156">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a0984-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0984-157">輸入</span><span class="sxs-lookup"><span data-stu-id="a0984-157">INPUTS</span></span>

## <span data-ttu-id="a0984-158">輸出</span><span class="sxs-lookup"><span data-stu-id="a0984-158">OUTPUTS</span></span>

### <span data-ttu-id="a0984-159">IBlockchainMember （Blockchain）。 Api20180601Preview。</span><span class="sxs-lookup"><span data-stu-id="a0984-159">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IBlockchainMember</span></span>

## <span data-ttu-id="a0984-160">筆記</span><span class="sxs-lookup"><span data-stu-id="a0984-160">NOTES</span></span>

<span data-ttu-id="a0984-161">別名</span><span class="sxs-lookup"><span data-stu-id="a0984-161">ALIASES</span></span>

<span data-ttu-id="a0984-162">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="a0984-162">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a0984-163">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="a0984-163">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a0984-164">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="a0984-164">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a0984-165">FIREWALLRULE <IFirewallRule [] >：取得或設定防火牆規則</span><span class="sxs-lookup"><span data-stu-id="a0984-165">FIREWALLRULE <IFirewallRule[]>: Gets or sets firewall rules</span></span>
  - <span data-ttu-id="a0984-166">`[EndIPAddress <String>]`：取得或設定防火牆規則範圍的結束 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="a0984-166">`[EndIPAddress <String>]`: Gets or sets the end IP address of the firewall rule range.</span></span>
  - <span data-ttu-id="a0984-167">`[RuleName <String>]`：取得或設定防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="a0984-167">`[RuleName <String>]`: Gets or sets the name of the firewall rules.</span></span>
  - <span data-ttu-id="a0984-168">`[StartIPAddress <String>]`：取得或設定防火牆規則範圍的起始 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="a0984-168">`[StartIPAddress <String>]`: Gets or sets the start IP address of the firewall rule range.</span></span>

## <span data-ttu-id="a0984-169">相關連結</span><span class="sxs-lookup"><span data-stu-id="a0984-169">RELATED LINKS</span></span>

