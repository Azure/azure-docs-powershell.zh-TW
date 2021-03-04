---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/powershell/module/az.blockchain/new-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMember.md
ms.openlocfilehash: 15af3a6bb7e80020cd014bfbdd8ff944cafd187a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916595"
---
# <span data-ttu-id="af10c-101">New-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="af10c-101">New-AzBlockchainMember</span></span>

## <span data-ttu-id="af10c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="af10c-102">SYNOPSIS</span></span>
<span data-ttu-id="af10c-103">建立一個會員。</span><span class="sxs-lookup"><span data-stu-id="af10c-103">Create a blockchain member.</span></span>

## <span data-ttu-id="af10c-104">語法</span><span class="sxs-lookup"><span data-stu-id="af10c-104">SYNTAX</span></span>

```
New-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Consortium <String>] [-ConsortiumManagementAccountPassword <SecureString>]
 [-ConsortiumMemberDisplayName <String>] [-ConsortiumRole <String>] [-FirewallRule <IFirewallRule[]>]
 [-Location <String>] [-Password <SecureString>] [-Protocol <BlockchainProtocol>] [-Sku <String>]
 [-SkuTier <String>] [-Tag <Hashtable>] [-ValidatorNodeSkuCapacity <Int32>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="af10c-105">描述</span><span class="sxs-lookup"><span data-stu-id="af10c-105">DESCRIPTION</span></span>
<span data-ttu-id="af10c-106">建立一個會員。</span><span class="sxs-lookup"><span data-stu-id="af10c-106">Create a blockchain member.</span></span>

## <span data-ttu-id="af10c-107">例子</span><span class="sxs-lookup"><span data-stu-id="af10c-107">EXAMPLES</span></span>

### <span data-ttu-id="af10c-108">範例 1：建立新進會員</span><span class="sxs-lookup"><span data-stu-id="af10c-108">Example 1: Create a new blockchain member</span></span>
```powershell
PS C:\> $passwd = 'strongMemberAccountPassword@1' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> $csPasswd = 'strongConsortiumManagementPassword@1' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzBlockchainMember -Name dolauli002 -ResourceGroupName testgroup -Consortium consor002 -ConsortiumManagementAccountPassword $csPasswd -Location eastus -Password $passwd -Protocol Quorum -Sku S0

Location Name       Type
-------- ----       ----
eastus   dolauli002 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="af10c-109">此命令會建立一個新的中央管理成員。</span><span class="sxs-lookup"><span data-stu-id="af10c-109">This command creates a new blockchain member.</span></span>

## <span data-ttu-id="af10c-110">參數</span><span class="sxs-lookup"><span data-stu-id="af10c-110">PARAMETERS</span></span>

### <span data-ttu-id="af10c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="af10c-111">-AsJob</span></span>
<span data-ttu-id="af10c-112">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="af10c-112">Run the command as a job</span></span>

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

### <span data-ttu-id="af10c-113">-Consortium</span><span class="sxs-lookup"><span data-stu-id="af10c-113">-Consortium</span></span>
<span data-ttu-id="af10c-114">為平臺成員獲取或設定聯合企業。</span><span class="sxs-lookup"><span data-stu-id="af10c-114">Gets or sets the consortium for the blockchain member.</span></span>

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

### <span data-ttu-id="af10c-115">-ConsortiumManagementAccountPassword</span><span class="sxs-lookup"><span data-stu-id="af10c-115">-ConsortiumManagementAccountPassword</span></span>
<span data-ttu-id="af10c-116">設定受管理的聯合會管理帳戶密碼。</span><span class="sxs-lookup"><span data-stu-id="af10c-116">Sets the managed consortium management account password.</span></span>

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

### <span data-ttu-id="af10c-117">-ConsortiumMemberDisplayName</span><span class="sxs-lookup"><span data-stu-id="af10c-117">-ConsortiumMemberDisplayName</span></span>
<span data-ttu-id="af10c-118">在聯合企業中，獲得成員顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="af10c-118">Gets the display name of the member in the consortium.</span></span>

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

### <span data-ttu-id="af10c-119">-ConsortiumRole</span><span class="sxs-lookup"><span data-stu-id="af10c-119">-ConsortiumRole</span></span>
<span data-ttu-id="af10c-120">在聯合企業中獲得成員的角色。</span><span class="sxs-lookup"><span data-stu-id="af10c-120">Gets the role of the member in the consortium.</span></span>

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

### <span data-ttu-id="af10c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af10c-121">-DefaultProfile</span></span>
<span data-ttu-id="af10c-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="af10c-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af10c-123">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="af10c-123">-FirewallRule</span></span>
<span data-ttu-id="af10c-124">若要建立防火牆規則，請參閱 FIREWALLRULE 屬性的 NOTES 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="af10c-124">Gets or sets firewall rules To construct, see NOTES section for FIREWALLRULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="af10c-125">-位置</span><span class="sxs-lookup"><span data-stu-id="af10c-125">-Location</span></span>
<span data-ttu-id="af10c-126">定位點服務的 GEO 位置。</span><span class="sxs-lookup"><span data-stu-id="af10c-126">The GEO location of the blockchain service.</span></span>

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

### <span data-ttu-id="af10c-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="af10c-127">-Name</span></span>
<span data-ttu-id="af10c-128">進位成員名稱。</span><span class="sxs-lookup"><span data-stu-id="af10c-128">Blockchain member name.</span></span>

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

### <span data-ttu-id="af10c-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="af10c-129">-NoWait</span></span>
<span data-ttu-id="af10c-130">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="af10c-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="af10c-131">-密碼</span><span class="sxs-lookup"><span data-stu-id="af10c-131">-Password</span></span>
<span data-ttu-id="af10c-132">設定電腦群組件成員的基本驗證密碼。</span><span class="sxs-lookup"><span data-stu-id="af10c-132">Sets the basic auth password of the blockchain member.</span></span>

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

### <span data-ttu-id="af10c-133">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="af10c-133">-Protocol</span></span>
<span data-ttu-id="af10c-134">獲取或設定修正程式通訊協定。</span><span class="sxs-lookup"><span data-stu-id="af10c-134">Gets or sets the blockchain protocol.</span></span>

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

### <span data-ttu-id="af10c-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af10c-135">-ResourceGroupName</span></span>
<span data-ttu-id="af10c-136">包含資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="af10c-136">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="af10c-137">您可以從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="af10c-137">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="af10c-138">-SKU</span><span class="sxs-lookup"><span data-stu-id="af10c-138">-Sku</span></span>
<span data-ttu-id="af10c-139">獲取或設定 SKU 名稱</span><span class="sxs-lookup"><span data-stu-id="af10c-139">Gets or sets Sku name</span></span>

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

### <span data-ttu-id="af10c-140">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="af10c-140">-SkuTier</span></span>
<span data-ttu-id="af10c-141">獲取或設定 SKU 層級</span><span class="sxs-lookup"><span data-stu-id="af10c-141">Gets or sets Sku tier</span></span>

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

### <span data-ttu-id="af10c-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="af10c-142">-SubscriptionId</span></span>
<span data-ttu-id="af10c-143">獲得可唯一識別 Microsoft Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="af10c-143">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="af10c-144">訂閱識別碼是每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="af10c-144">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="af10c-145">-標記</span><span class="sxs-lookup"><span data-stu-id="af10c-145">-Tag</span></span>
<span data-ttu-id="af10c-146">服務標記是描述資源的金鑰值組清單。</span><span class="sxs-lookup"><span data-stu-id="af10c-146">Tags of the service which is a list of key value pairs that describes the resource.</span></span>

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

### <span data-ttu-id="af10c-147">-ValidatorNodeSku一文</span><span class="sxs-lookup"><span data-stu-id="af10c-147">-ValidatorNodeSkuCapacity</span></span>
<span data-ttu-id="af10c-148">獲取或設定節點容量。</span><span class="sxs-lookup"><span data-stu-id="af10c-148">Gets or sets the nodes capacity.</span></span>

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

### <span data-ttu-id="af10c-149">-確認</span><span class="sxs-lookup"><span data-stu-id="af10c-149">-Confirm</span></span>
<span data-ttu-id="af10c-150">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="af10c-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af10c-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af10c-151">-WhatIf</span></span>
<span data-ttu-id="af10c-152">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="af10c-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af10c-153">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="af10c-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af10c-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af10c-154">CommonParameters</span></span>
<span data-ttu-id="af10c-155">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="af10c-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af10c-156">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="af10c-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af10c-157">輸入</span><span class="sxs-lookup"><span data-stu-id="af10c-157">INPUTS</span></span>

## <span data-ttu-id="af10c-158">輸出</span><span class="sxs-lookup"><span data-stu-id="af10c-158">OUTPUTS</span></span>

### <span data-ttu-id="af10c-159">Microsoft.Azure.PowerShell.Cmdlets.Azer.Models.Api20180601Preview.IBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="af10c-159">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IBlockchainMember</span></span>

## <span data-ttu-id="af10c-160">筆記</span><span class="sxs-lookup"><span data-stu-id="af10c-160">NOTES</span></span>

<span data-ttu-id="af10c-161">別名</span><span class="sxs-lookup"><span data-stu-id="af10c-161">ALIASES</span></span>

<span data-ttu-id="af10c-162">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="af10c-162">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="af10c-163">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="af10c-163">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="af10c-164">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="af10c-164">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="af10c-165">FIREWALLRULE <IFirewallRule[]>：獲取或設定防火牆規則</span><span class="sxs-lookup"><span data-stu-id="af10c-165">FIREWALLRULE <IFirewallRule[]>: Gets or sets firewall rules</span></span>
  - <span data-ttu-id="af10c-166">`[EndIPAddress <String>]`：獲取或設定防火牆規則範圍的結束 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="af10c-166">`[EndIPAddress <String>]`: Gets or sets the end IP address of the firewall rule range.</span></span>
  - <span data-ttu-id="af10c-167">`[RuleName <String>]`：獲取或設定防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="af10c-167">`[RuleName <String>]`: Gets or sets the name of the firewall rules.</span></span>
  - <span data-ttu-id="af10c-168">`[StartIPAddress <String>]`：獲取或設定防火牆規則範圍的起始 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="af10c-168">`[StartIPAddress <String>]`: Gets or sets the start IP address of the firewall rule range.</span></span>

## <span data-ttu-id="af10c-169">相關連結</span><span class="sxs-lookup"><span data-stu-id="af10c-169">RELATED LINKS</span></span>

