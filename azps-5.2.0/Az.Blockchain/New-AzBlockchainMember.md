---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/new-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMember.md
ms.openlocfilehash: a6bd4f7d8d3058de948d0ecef636c2ec9e1ca1e9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98278838"
---
# <span data-ttu-id="6a841-101">New-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="6a841-101">New-AzBlockchainMember</span></span>

## <span data-ttu-id="6a841-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6a841-102">SYNOPSIS</span></span>
<span data-ttu-id="6a841-103">建立 blockchain 成員。</span><span class="sxs-lookup"><span data-stu-id="6a841-103">Create a blockchain member.</span></span>

## <span data-ttu-id="6a841-104">句法</span><span class="sxs-lookup"><span data-stu-id="6a841-104">SYNTAX</span></span>

```
New-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Consortium <String>] [-ConsortiumManagementAccountPassword <SecureString>]
 [-ConsortiumMemberDisplayName <String>] [-ConsortiumRole <String>] [-FirewallRule <IFirewallRule[]>]
 [-Location <String>] [-Password <SecureString>] [-Protocol <BlockchainProtocol>] [-Sku <String>]
 [-SkuTier <String>] [-Tag <Hashtable>] [-ValidatorNodeSkuCapacity <Int32>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6a841-105">說明</span><span class="sxs-lookup"><span data-stu-id="6a841-105">DESCRIPTION</span></span>
<span data-ttu-id="6a841-106">建立 blockchain 成員。</span><span class="sxs-lookup"><span data-stu-id="6a841-106">Create a blockchain member.</span></span>

## <span data-ttu-id="6a841-107">示例</span><span class="sxs-lookup"><span data-stu-id="6a841-107">EXAMPLES</span></span>

### <span data-ttu-id="6a841-108">範例1：建立新的 blockchain 成員</span><span class="sxs-lookup"><span data-stu-id="6a841-108">Example 1: Create a new blockchain member</span></span>
```powershell
PS C:\> $passwd = 'strongMemberAccountPassword@1' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> $csPasswd = 'strongConsortiumManagementPassword@1' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzBlockchainMember -Name dolauli002 -ResourceGroupName testgroup -Consortium consor002 -ConsortiumManagementAccountPassword $csPasswd -Location eastus -Password $passwd -Protocol Quorum -Sku S0

Location Name       Type
-------- ----       ----
eastus   dolauli002 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="6a841-109">這個命令會建立新的 blockchain 成員。</span><span class="sxs-lookup"><span data-stu-id="6a841-109">This command creates a new blockchain member.</span></span>

## <span data-ttu-id="6a841-110">參數</span><span class="sxs-lookup"><span data-stu-id="6a841-110">PARAMETERS</span></span>

### <span data-ttu-id="6a841-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6a841-111">-AsJob</span></span>
<span data-ttu-id="6a841-112">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="6a841-112">Run the command as a job</span></span>

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

### <span data-ttu-id="6a841-113">-聯合會</span><span class="sxs-lookup"><span data-stu-id="6a841-113">-Consortium</span></span>
<span data-ttu-id="6a841-114">取得或設定 blockchain 成員的聯合會。</span><span class="sxs-lookup"><span data-stu-id="6a841-114">Gets or sets the consortium for the blockchain member.</span></span>

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

### <span data-ttu-id="6a841-115">-ConsortiumManagementAccountPassword</span><span class="sxs-lookup"><span data-stu-id="6a841-115">-ConsortiumManagementAccountPassword</span></span>
<span data-ttu-id="6a841-116">設定受管理的聯合會管理帳戶密碼。</span><span class="sxs-lookup"><span data-stu-id="6a841-116">Sets the managed consortium management account password.</span></span>

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

### <span data-ttu-id="6a841-117">-ConsortiumMemberDisplayName</span><span class="sxs-lookup"><span data-stu-id="6a841-117">-ConsortiumMemberDisplayName</span></span>
<span data-ttu-id="6a841-118">取得聯合會中成員的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="6a841-118">Gets the display name of the member in the consortium.</span></span>

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

### <span data-ttu-id="6a841-119">-ConsortiumRole</span><span class="sxs-lookup"><span data-stu-id="6a841-119">-ConsortiumRole</span></span>
<span data-ttu-id="6a841-120">取得聯盟中成員的角色。</span><span class="sxs-lookup"><span data-stu-id="6a841-120">Gets the role of the member in the consortium.</span></span>

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

### <span data-ttu-id="6a841-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a841-121">-DefaultProfile</span></span>
<span data-ttu-id="6a841-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6a841-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a841-123">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="6a841-123">-FirewallRule</span></span>
<span data-ttu-id="6a841-124">取得或設定要構造的防火牆規則，請參閱 FIREWALLRULE 屬性的記事區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="6a841-124">Gets or sets firewall rules To construct, see NOTES section for FIREWALLRULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="6a841-125">-位置</span><span class="sxs-lookup"><span data-stu-id="6a841-125">-Location</span></span>
<span data-ttu-id="6a841-126">Blockchain 服務的地理位置。</span><span class="sxs-lookup"><span data-stu-id="6a841-126">The GEO location of the blockchain service.</span></span>

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

### <span data-ttu-id="6a841-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="6a841-127">-Name</span></span>
<span data-ttu-id="6a841-128">Blockchain 成員名稱。</span><span class="sxs-lookup"><span data-stu-id="6a841-128">Blockchain member name.</span></span>

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

### <span data-ttu-id="6a841-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="6a841-129">-NoWait</span></span>
<span data-ttu-id="6a841-130">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="6a841-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6a841-131">-Password</span><span class="sxs-lookup"><span data-stu-id="6a841-131">-Password</span></span>
<span data-ttu-id="6a841-132">設定 blockchain 成員的基本驗證密碼。</span><span class="sxs-lookup"><span data-stu-id="6a841-132">Sets the basic auth password of the blockchain member.</span></span>

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

### <span data-ttu-id="6a841-133">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="6a841-133">-Protocol</span></span>
<span data-ttu-id="6a841-134">取得或設定 blockchain 通訊協定。</span><span class="sxs-lookup"><span data-stu-id="6a841-134">Gets or sets the blockchain protocol.</span></span>

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

### <span data-ttu-id="6a841-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a841-135">-ResourceGroupName</span></span>
<span data-ttu-id="6a841-136">包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6a841-136">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="6a841-137">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="6a841-137">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="6a841-138">-Sku</span><span class="sxs-lookup"><span data-stu-id="6a841-138">-Sku</span></span>
<span data-ttu-id="6a841-139">取得或設定 Sku 名稱</span><span class="sxs-lookup"><span data-stu-id="6a841-139">Gets or sets Sku name</span></span>

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

### <span data-ttu-id="6a841-140">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="6a841-140">-SkuTier</span></span>
<span data-ttu-id="6a841-141">取得或設定 Sku 層</span><span class="sxs-lookup"><span data-stu-id="6a841-141">Gets or sets Sku tier</span></span>

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

### <span data-ttu-id="6a841-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6a841-142">-SubscriptionId</span></span>
<span data-ttu-id="6a841-143">取得唯一識別 Microsoft Azure 訂閱的訂閱 Id。</span><span class="sxs-lookup"><span data-stu-id="6a841-143">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="6a841-144">訂閱識別碼是每個服務呼叫 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="6a841-144">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="6a841-145">-Tag</span><span class="sxs-lookup"><span data-stu-id="6a841-145">-Tag</span></span>
<span data-ttu-id="6a841-146">服務的標記，是描述資源的鍵值對清單。</span><span class="sxs-lookup"><span data-stu-id="6a841-146">Tags of the service which is a list of key value pairs that describes the resource.</span></span>

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

### <span data-ttu-id="6a841-147">-ValidatorNodeSkuCapacity</span><span class="sxs-lookup"><span data-stu-id="6a841-147">-ValidatorNodeSkuCapacity</span></span>
<span data-ttu-id="6a841-148">取得或設定節點的容量。</span><span class="sxs-lookup"><span data-stu-id="6a841-148">Gets or sets the nodes capacity.</span></span>

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

### <span data-ttu-id="6a841-149">-確認</span><span class="sxs-lookup"><span data-stu-id="6a841-149">-Confirm</span></span>
<span data-ttu-id="6a841-150">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6a841-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a841-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a841-151">-WhatIf</span></span>
<span data-ttu-id="6a841-152">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6a841-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a841-153">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6a841-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a841-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a841-154">CommonParameters</span></span>
<span data-ttu-id="6a841-155">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6a841-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a841-156">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="6a841-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a841-157">輸入</span><span class="sxs-lookup"><span data-stu-id="6a841-157">INPUTS</span></span>

## <span data-ttu-id="6a841-158">輸出</span><span class="sxs-lookup"><span data-stu-id="6a841-158">OUTPUTS</span></span>

### <span data-ttu-id="6a841-159">IBlockchainMember （Blockchain）。 Api20180601Preview。</span><span class="sxs-lookup"><span data-stu-id="6a841-159">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IBlockchainMember</span></span>

## <span data-ttu-id="6a841-160">筆記</span><span class="sxs-lookup"><span data-stu-id="6a841-160">NOTES</span></span>

<span data-ttu-id="6a841-161">別名</span><span class="sxs-lookup"><span data-stu-id="6a841-161">ALIASES</span></span>

<span data-ttu-id="6a841-162">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="6a841-162">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6a841-163">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="6a841-163">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6a841-164">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="6a841-164">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6a841-165">FIREWALLRULE <IFirewallRule [] >：取得或設定防火牆規則</span><span class="sxs-lookup"><span data-stu-id="6a841-165">FIREWALLRULE <IFirewallRule[]>: Gets or sets firewall rules</span></span>
  - <span data-ttu-id="6a841-166">`[EndIPAddress <String>]`：取得或設定防火牆規則範圍的結束 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="6a841-166">`[EndIPAddress <String>]`: Gets or sets the end IP address of the firewall rule range.</span></span>
  - <span data-ttu-id="6a841-167">`[RuleName <String>]`：取得或設定防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="6a841-167">`[RuleName <String>]`: Gets or sets the name of the firewall rules.</span></span>
  - <span data-ttu-id="6a841-168">`[StartIPAddress <String>]`：取得或設定防火牆規則範圍的起始 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="6a841-168">`[StartIPAddress <String>]`: Gets or sets the start IP address of the firewall rule range.</span></span>

## <span data-ttu-id="6a841-169">相關連結</span><span class="sxs-lookup"><span data-stu-id="6a841-169">RELATED LINKS</span></span>

