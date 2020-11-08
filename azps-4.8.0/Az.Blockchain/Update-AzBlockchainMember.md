---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/update-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Update-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Update-AzBlockchainMember.md
ms.openlocfilehash: 708ad613c2dbab7e7224dbd392809d9502c9b447
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970601"
---
# <span data-ttu-id="fdb5b-101">Update-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="fdb5b-101">Update-AzBlockchainMember</span></span>

## <span data-ttu-id="fdb5b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fdb5b-102">SYNOPSIS</span></span>
<span data-ttu-id="fdb5b-103">更新 blockchain 成員。</span><span class="sxs-lookup"><span data-stu-id="fdb5b-103">Update a blockchain member.</span></span>

## <span data-ttu-id="fdb5b-104">句法</span><span class="sxs-lookup"><span data-stu-id="fdb5b-104">SYNTAX</span></span>

### <span data-ttu-id="fdb5b-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="fdb5b-105">UpdateExpanded (Default)</span></span>
```
Update-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-ConsortiumManagementAccountPassword <SecureString>] [-FirewallRule <IFirewallRule[]>]
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="fdb5b-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="fdb5b-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzBlockchainMember -InputObject <IBlockchainIdentity>
 [-ConsortiumManagementAccountPassword <SecureString>] [-FirewallRule <IFirewallRule[]>]
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="fdb5b-107">說明</span><span class="sxs-lookup"><span data-stu-id="fdb5b-107">DESCRIPTION</span></span>
<span data-ttu-id="fdb5b-108">更新 blockchain 成員。</span><span class="sxs-lookup"><span data-stu-id="fdb5b-108">Update a blockchain member.</span></span>

## <span data-ttu-id="fdb5b-109">示例</span><span class="sxs-lookup"><span data-stu-id="fdb5b-109">EXAMPLES</span></span>

### <span data-ttu-id="fdb5b-110">範例1：更新 blockchain 成員</span><span class="sxs-lookup"><span data-stu-id="fdb5b-110">Example 1: Update a blockchain member</span></span>
```powershell
PS C:\> $passwd2 = 'strongMemberAccountPassword@2' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> Update-AzBlockchainMember -Name dolauli002 -ResourceGroupName testgroup -Password $passwd2

Location Name       Type
-------- ----       ----
eastus   dolauli002 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="fdb5b-111">這個命令會更新 blockchain 成員。</span><span class="sxs-lookup"><span data-stu-id="fdb5b-111">This command updates a blockchain member.</span></span>

### <span data-ttu-id="fdb5b-112">範例2：更新 blockchain 成員</span><span class="sxs-lookup"><span data-stu-id="fdb5b-112">Example 2: Update a blockchain member</span></span>
```powershell
PS C:\> $tag = @{'againupdate'='password'}
PS C:\> $member = Get-AzBlockchainMember -Name $env.blockchainMember -ResourceGroupName $env.resourceGroup
PS C:\> Update-AzBlockchainMember -InputObject $member -Tag $tag

Location Name       Type
-------- ----       ----
eastus   dolauli002 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="fdb5b-113">這個命令會更新 blockchain 成員。</span><span class="sxs-lookup"><span data-stu-id="fdb5b-113">This command updates a blockchain member.</span></span>

## <span data-ttu-id="fdb5b-114">參數</span><span class="sxs-lookup"><span data-stu-id="fdb5b-114">PARAMETERS</span></span>

### <span data-ttu-id="fdb5b-115">-ConsortiumManagementAccountPassword</span><span class="sxs-lookup"><span data-stu-id="fdb5b-115">-ConsortiumManagementAccountPassword</span></span>
<span data-ttu-id="fdb5b-116">設定受管理的聯合會管理帳戶密碼。</span><span class="sxs-lookup"><span data-stu-id="fdb5b-116">Sets the managed consortium management account password.</span></span>

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

### <span data-ttu-id="fdb5b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdb5b-117">-DefaultProfile</span></span>
<span data-ttu-id="fdb5b-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fdb5b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fdb5b-119">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="fdb5b-119">-FirewallRule</span></span>
<span data-ttu-id="fdb5b-120">取得或設定防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="fdb5b-120">Gets or sets the firewall rules.</span></span>
<span data-ttu-id="fdb5b-121">若要建立，請參閱 FIREWALLRULE 屬性和建立雜湊資料表的備忘稿區段。</span><span class="sxs-lookup"><span data-stu-id="fdb5b-121">To construct, see NOTES section for FIREWALLRULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="fdb5b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fdb5b-122">-InputObject</span></span>
<span data-ttu-id="fdb5b-123">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="fdb5b-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="fdb5b-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="fdb5b-124">-Name</span></span>
<span data-ttu-id="fdb5b-125">Blockchain 成員名稱。</span><span class="sxs-lookup"><span data-stu-id="fdb5b-125">Blockchain member name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: BlockchainMemberName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdb5b-126">-Password</span><span class="sxs-lookup"><span data-stu-id="fdb5b-126">-Password</span></span>
<span data-ttu-id="fdb5b-127">設定交易節點 dns 端點的基本授權密碼。</span><span class="sxs-lookup"><span data-stu-id="fdb5b-127">Sets the transaction node dns endpoint basic auth password.</span></span>

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

### <span data-ttu-id="fdb5b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdb5b-128">-ResourceGroupName</span></span>
<span data-ttu-id="fdb5b-129">包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="fdb5b-129">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="fdb5b-130">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="fdb5b-130">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="fdb5b-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fdb5b-131">-SubscriptionId</span></span>
<span data-ttu-id="fdb5b-132">取得唯一識別 Microsoft Azure 訂閱的訂閱 Id。</span><span class="sxs-lookup"><span data-stu-id="fdb5b-132">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="fdb5b-133">訂閱識別碼是每個服務呼叫 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="fdb5b-133">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="fdb5b-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="fdb5b-134">-Tag</span></span>
<span data-ttu-id="fdb5b-135">服務的標記，是描述資源的鍵值對清單。</span><span class="sxs-lookup"><span data-stu-id="fdb5b-135">Tags of the service which is a list of key value pairs that describes the resource.</span></span>

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

### <span data-ttu-id="fdb5b-136">-確認</span><span class="sxs-lookup"><span data-stu-id="fdb5b-136">-Confirm</span></span>
<span data-ttu-id="fdb5b-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fdb5b-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fdb5b-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fdb5b-138">-WhatIf</span></span>
<span data-ttu-id="fdb5b-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fdb5b-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fdb5b-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fdb5b-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fdb5b-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdb5b-141">CommonParameters</span></span>
<span data-ttu-id="fdb5b-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fdb5b-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdb5b-143">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="fdb5b-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdb5b-144">輸入</span><span class="sxs-lookup"><span data-stu-id="fdb5b-144">INPUTS</span></span>

### <span data-ttu-id="fdb5b-145">IBlockchainIdentity （Blockchain）的</span><span class="sxs-lookup"><span data-stu-id="fdb5b-145">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="fdb5b-146">輸出</span><span class="sxs-lookup"><span data-stu-id="fdb5b-146">OUTPUTS</span></span>

### <span data-ttu-id="fdb5b-147">IBlockchainMember （Blockchain）。 Api20180601Preview。</span><span class="sxs-lookup"><span data-stu-id="fdb5b-147">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IBlockchainMember</span></span>

## <span data-ttu-id="fdb5b-148">筆記</span><span class="sxs-lookup"><span data-stu-id="fdb5b-148">NOTES</span></span>

<span data-ttu-id="fdb5b-149">別名</span><span class="sxs-lookup"><span data-stu-id="fdb5b-149">ALIASES</span></span>

<span data-ttu-id="fdb5b-150">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="fdb5b-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="fdb5b-151">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="fdb5b-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fdb5b-152">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="fdb5b-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="fdb5b-153">FIREWALLRULE <IFirewallRule [] >：取得或設定防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="fdb5b-153">FIREWALLRULE <IFirewallRule[]>: Gets or sets the firewall rules.</span></span>
  - <span data-ttu-id="fdb5b-154">`[EndIPAddress <String>]`：取得或設定防火牆規則範圍的結束 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="fdb5b-154">`[EndIPAddress <String>]`: Gets or sets the end IP address of the firewall rule range.</span></span>
  - <span data-ttu-id="fdb5b-155">`[RuleName <String>]`：取得或設定防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="fdb5b-155">`[RuleName <String>]`: Gets or sets the name of the firewall rules.</span></span>
  - <span data-ttu-id="fdb5b-156">`[StartIPAddress <String>]`：取得或設定防火牆規則範圍的起始 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="fdb5b-156">`[StartIPAddress <String>]`: Gets or sets the start IP address of the firewall rule range.</span></span>

<span data-ttu-id="fdb5b-157">INPUTOBJECT <IBlockchainIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="fdb5b-157">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="fdb5b-158">`[BlockchainMemberName <String>]`： Blockchain 成員名稱。</span><span class="sxs-lookup"><span data-stu-id="fdb5b-158">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="fdb5b-159">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="fdb5b-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="fdb5b-160">`[Location <String>]`：位置名稱。</span><span class="sxs-lookup"><span data-stu-id="fdb5b-160">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="fdb5b-161">`[OperationId <String>]`：操作 Id。</span><span class="sxs-lookup"><span data-stu-id="fdb5b-161">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="fdb5b-162">`[ResourceGroupName <String>]`：包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="fdb5b-162">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="fdb5b-163">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="fdb5b-163">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="fdb5b-164">`[SubscriptionId <String>]`：取得唯一識別 Microsoft Azure 訂閱的訂閱 Id。</span><span class="sxs-lookup"><span data-stu-id="fdb5b-164">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="fdb5b-165">訂閱識別碼是每個服務呼叫 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="fdb5b-165">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="fdb5b-166">`[TransactionNodeName <String>]`：交易節點名稱。</span><span class="sxs-lookup"><span data-stu-id="fdb5b-166">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="fdb5b-167">相關連結</span><span class="sxs-lookup"><span data-stu-id="fdb5b-167">RELATED LINKS</span></span>

