---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/powershell/module/az.blockchain/update-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Update-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Update-AzBlockchainMember.md
ms.openlocfilehash: 833e660980d82c32667d166dbeed4520686d1124
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907817"
---
# <span data-ttu-id="9fe21-101">Update-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="9fe21-101">Update-AzBlockchainMember</span></span>

## <span data-ttu-id="9fe21-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9fe21-102">SYNOPSIS</span></span>
<span data-ttu-id="9fe21-103">更新網路管理成員。</span><span class="sxs-lookup"><span data-stu-id="9fe21-103">Update a blockchain member.</span></span>

## <span data-ttu-id="9fe21-104">語法</span><span class="sxs-lookup"><span data-stu-id="9fe21-104">SYNTAX</span></span>

### <span data-ttu-id="9fe21-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="9fe21-105">UpdateExpanded (Default)</span></span>
```
Update-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-ConsortiumManagementAccountPassword <SecureString>] [-FirewallRule <IFirewallRule[]>]
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="9fe21-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="9fe21-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzBlockchainMember -InputObject <IBlockchainIdentity>
 [-ConsortiumManagementAccountPassword <SecureString>] [-FirewallRule <IFirewallRule[]>]
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="9fe21-107">描述</span><span class="sxs-lookup"><span data-stu-id="9fe21-107">DESCRIPTION</span></span>
<span data-ttu-id="9fe21-108">更新網路管理成員。</span><span class="sxs-lookup"><span data-stu-id="9fe21-108">Update a blockchain member.</span></span>

## <span data-ttu-id="9fe21-109">例子</span><span class="sxs-lookup"><span data-stu-id="9fe21-109">EXAMPLES</span></span>

### <span data-ttu-id="9fe21-110">範例 1：更新成員</span><span class="sxs-lookup"><span data-stu-id="9fe21-110">Example 1: Update a blockchain member</span></span>
```powershell
PS C:\> $passwd2 = 'strongMemberAccountPassword@2' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> Update-AzBlockchainMember -Name dolauli002 -ResourceGroupName testgroup -Password $passwd2

Location Name       Type
-------- ----       ----
eastus   dolauli002 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="9fe21-111">此命令會更新更新成員。</span><span class="sxs-lookup"><span data-stu-id="9fe21-111">This command updates a blockchain member.</span></span>

### <span data-ttu-id="9fe21-112">範例 2：更新成員</span><span class="sxs-lookup"><span data-stu-id="9fe21-112">Example 2: Update a blockchain member</span></span>
```powershell
PS C:\> $tag = @{'againupdate'='password'}
PS C:\> $member = Get-AzBlockchainMember -Name $env.blockchainMember -ResourceGroupName $env.resourceGroup
PS C:\> Update-AzBlockchainMember -InputObject $member -Tag $tag

Location Name       Type
-------- ----       ----
eastus   dolauli002 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="9fe21-113">此命令會更新更新成員。</span><span class="sxs-lookup"><span data-stu-id="9fe21-113">This command updates a blockchain member.</span></span>

## <span data-ttu-id="9fe21-114">參數</span><span class="sxs-lookup"><span data-stu-id="9fe21-114">PARAMETERS</span></span>

### <span data-ttu-id="9fe21-115">-ConsortiumManagementAccountPassword</span><span class="sxs-lookup"><span data-stu-id="9fe21-115">-ConsortiumManagementAccountPassword</span></span>
<span data-ttu-id="9fe21-116">設定受管理的聯合會管理帳戶密碼。</span><span class="sxs-lookup"><span data-stu-id="9fe21-116">Sets the managed consortium management account password.</span></span>

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

### <span data-ttu-id="9fe21-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fe21-117">-DefaultProfile</span></span>
<span data-ttu-id="9fe21-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9fe21-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9fe21-119">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="9fe21-119">-FirewallRule</span></span>
<span data-ttu-id="9fe21-120">獲取或設定防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="9fe21-120">Gets or sets the firewall rules.</span></span>
<span data-ttu-id="9fe21-121">若要建構，請參閱 FIREWALLRULE 屬性的附注區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="9fe21-121">To construct, see NOTES section for FIREWALLRULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="9fe21-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9fe21-122">-InputObject</span></span>
<span data-ttu-id="9fe21-123">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="9fe21-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9fe21-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="9fe21-124">-Name</span></span>
<span data-ttu-id="9fe21-125">進位成員名稱。</span><span class="sxs-lookup"><span data-stu-id="9fe21-125">Blockchain member name.</span></span>

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

### <span data-ttu-id="9fe21-126">-密碼</span><span class="sxs-lookup"><span data-stu-id="9fe21-126">-Password</span></span>
<span data-ttu-id="9fe21-127">設定交易節點 dns 端點的基本驗證密碼。</span><span class="sxs-lookup"><span data-stu-id="9fe21-127">Sets the transaction node dns endpoint basic auth password.</span></span>

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

### <span data-ttu-id="9fe21-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fe21-128">-ResourceGroupName</span></span>
<span data-ttu-id="9fe21-129">包含資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="9fe21-129">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="9fe21-130">您可以從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="9fe21-130">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="9fe21-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9fe21-131">-SubscriptionId</span></span>
<span data-ttu-id="9fe21-132">獲得可唯一識別 Microsoft Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="9fe21-132">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="9fe21-133">訂閱識別碼是每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="9fe21-133">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="9fe21-134">-標記</span><span class="sxs-lookup"><span data-stu-id="9fe21-134">-Tag</span></span>
<span data-ttu-id="9fe21-135">服務標記是描述資源的金鑰值組清單。</span><span class="sxs-lookup"><span data-stu-id="9fe21-135">Tags of the service which is a list of key value pairs that describes the resource.</span></span>

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

### <span data-ttu-id="9fe21-136">-確認</span><span class="sxs-lookup"><span data-stu-id="9fe21-136">-Confirm</span></span>
<span data-ttu-id="9fe21-137">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="9fe21-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9fe21-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9fe21-138">-WhatIf</span></span>
<span data-ttu-id="9fe21-139">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9fe21-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9fe21-140">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9fe21-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9fe21-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fe21-141">CommonParameters</span></span>
<span data-ttu-id="9fe21-142">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9fe21-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fe21-143">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9fe21-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fe21-144">輸入</span><span class="sxs-lookup"><span data-stu-id="9fe21-144">INPUTS</span></span>

### <span data-ttu-id="9fe21-145">Microsoft.Azure.PowerShell.Cmdlets.Ident.Models.IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="9fe21-145">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="9fe21-146">輸出</span><span class="sxs-lookup"><span data-stu-id="9fe21-146">OUTPUTS</span></span>

### <span data-ttu-id="9fe21-147">Microsoft.Azure.PowerShell.Cmdlets.Azer.Models.Api20180601Preview.IBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="9fe21-147">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IBlockchainMember</span></span>

## <span data-ttu-id="9fe21-148">筆記</span><span class="sxs-lookup"><span data-stu-id="9fe21-148">NOTES</span></span>

<span data-ttu-id="9fe21-149">別名</span><span class="sxs-lookup"><span data-stu-id="9fe21-149">ALIASES</span></span>

<span data-ttu-id="9fe21-150">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="9fe21-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9fe21-151">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="9fe21-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9fe21-152">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="9fe21-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9fe21-153">FIREWALLRULE <IFirewallRule[]>：獲取或設定防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="9fe21-153">FIREWALLRULE <IFirewallRule[]>: Gets or sets the firewall rules.</span></span>
  - <span data-ttu-id="9fe21-154">`[EndIPAddress <String>]`：獲取或設定防火牆規則範圍的結束 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="9fe21-154">`[EndIPAddress <String>]`: Gets or sets the end IP address of the firewall rule range.</span></span>
  - <span data-ttu-id="9fe21-155">`[RuleName <String>]`：獲取或設定防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="9fe21-155">`[RuleName <String>]`: Gets or sets the name of the firewall rules.</span></span>
  - <span data-ttu-id="9fe21-156">`[StartIPAddress <String>]`：獲取或設定防火牆規則範圍的起始 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="9fe21-156">`[StartIPAddress <String>]`: Gets or sets the start IP address of the firewall rule range.</span></span>

<span data-ttu-id="9fe21-157">INPUTOBJECT： <IBlockchainIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="9fe21-157">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9fe21-158">`[BlockchainMemberName <String>]`：進位會員名稱。</span><span class="sxs-lookup"><span data-stu-id="9fe21-158">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="9fe21-159">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="9fe21-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9fe21-160">`[Location <String>]`：位置名稱。</span><span class="sxs-lookup"><span data-stu-id="9fe21-160">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="9fe21-161">`[OperationId <String>]`：操作識別碼。</span><span class="sxs-lookup"><span data-stu-id="9fe21-161">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="9fe21-162">`[ResourceGroupName <String>]`：包含資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="9fe21-162">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="9fe21-163">您可以從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="9fe21-163">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="9fe21-164">`[SubscriptionId <String>]`：獲得可唯一識別 Microsoft Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="9fe21-164">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="9fe21-165">訂閱識別碼是每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="9fe21-165">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="9fe21-166">`[TransactionNodeName <String>]`：交易處理節點名稱。</span><span class="sxs-lookup"><span data-stu-id="9fe21-166">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="9fe21-167">相關連結</span><span class="sxs-lookup"><span data-stu-id="9fe21-167">RELATED LINKS</span></span>

