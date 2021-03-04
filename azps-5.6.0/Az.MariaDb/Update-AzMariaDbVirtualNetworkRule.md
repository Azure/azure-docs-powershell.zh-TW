---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/powershell/module/az.mariadb/update-azmariadbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbVirtualNetworkRule.md
ms.openlocfilehash: cbb774e0a4bedb66a32839c069c305317c8e9f43
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915418"
---
# <span data-ttu-id="e390f-101">Update-AzMariaDbVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="e390f-101">Update-AzMariaDbVirtualNetworkRule</span></span>

## <span data-ttu-id="e390f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e390f-102">SYNOPSIS</span></span>
<span data-ttu-id="e390f-103">建立或更新現有的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="e390f-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="e390f-104">語法</span><span class="sxs-lookup"><span data-stu-id="e390f-104">SYNTAX</span></span>

### <span data-ttu-id="e390f-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="e390f-105">UpdateExpanded (Default)</span></span>
```
Update-AzMariaDbVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint] [-SubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e390f-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="e390f-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMariaDbVirtualNetworkRule -InputObject <IMariaDbIdentity> [-IgnoreMissingVnetServiceEndpoint]
 [-SubnetId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="e390f-107">描述</span><span class="sxs-lookup"><span data-stu-id="e390f-107">DESCRIPTION</span></span>
<span data-ttu-id="e390f-108">建立或更新現有的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="e390f-108">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="e390f-109">例子</span><span class="sxs-lookup"><span data-stu-id="e390f-109">EXAMPLES</span></span>

### <span data-ttu-id="e390f-110">範例 1：更新 MariaDB 虛擬網路規則</span><span class="sxs-lookup"><span data-stu-id="e390f-110">Example 1: Update MariaDB virtual network rule</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name vnet -ResourceGroupName mariadb-test-qu5ov0
PS C:\> Update-AzMariaDbVirtualNetworkRule -ServerName mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 -Name vnetrule-QdMJpU -SubnetId $vnet.Subnets[0].Id -IgnoreMissingVnetServiceEndpoint

Name            Type
----            ----
vnetrule-QdMJpU Microsoft.DBforMariaDB/servers/virtualNetworkRules
```

<span data-ttu-id="e390f-111">此命令會更新虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="e390f-111">This command updates a virtual network rule.</span></span>

## <span data-ttu-id="e390f-112">參數</span><span class="sxs-lookup"><span data-stu-id="e390f-112">PARAMETERS</span></span>

### <span data-ttu-id="e390f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e390f-113">-AsJob</span></span>
<span data-ttu-id="e390f-114">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="e390f-114">Run the command as a job</span></span>

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

### <span data-ttu-id="e390f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e390f-115">-DefaultProfile</span></span>
<span data-ttu-id="e390f-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e390f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e390f-117">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="e390f-117">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="e390f-118">在啟用 vnet 服務端點之前建立防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="e390f-118">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="e390f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e390f-119">-InputObject</span></span>
<span data-ttu-id="e390f-120">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="e390f-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e390f-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="e390f-121">-Name</span></span>
<span data-ttu-id="e390f-122">虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="e390f-122">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: VirtualNetworkRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e390f-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e390f-123">-NoWait</span></span>
<span data-ttu-id="e390f-124">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="e390f-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e390f-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e390f-125">-PassThru</span></span>
<span data-ttu-id="e390f-126">命令成功時，會返回 True</span><span class="sxs-lookup"><span data-stu-id="e390f-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="e390f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e390f-127">-ResourceGroupName</span></span>
<span data-ttu-id="e390f-128">包含資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="e390f-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="e390f-129">您可以從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="e390f-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="e390f-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e390f-130">-ServerName</span></span>
<span data-ttu-id="e390f-131">伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="e390f-131">The name of the server.</span></span>

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

### <span data-ttu-id="e390f-132">-子網Id</span><span class="sxs-lookup"><span data-stu-id="e390f-132">-SubnetId</span></span>
<span data-ttu-id="e390f-133">虛擬網路子網的 ARM 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="e390f-133">The ARM resource id of the virtual network subnet.</span></span>

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

### <span data-ttu-id="e390f-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e390f-134">-SubscriptionId</span></span>
<span data-ttu-id="e390f-135">可識別 Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="e390f-135">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="e390f-136">-確認</span><span class="sxs-lookup"><span data-stu-id="e390f-136">-Confirm</span></span>
<span data-ttu-id="e390f-137">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="e390f-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e390f-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e390f-138">-WhatIf</span></span>
<span data-ttu-id="e390f-139">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e390f-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e390f-140">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e390f-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e390f-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e390f-141">CommonParameters</span></span>
<span data-ttu-id="e390f-142">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e390f-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e390f-143">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e390f-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e390f-144">輸入</span><span class="sxs-lookup"><span data-stu-id="e390f-144">INPUTS</span></span>

### <span data-ttu-id="e390f-145">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.models.IAzaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="e390f-145">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="e390f-146">輸出</span><span class="sxs-lookup"><span data-stu-id="e390f-146">OUTPUTS</span></span>

### <span data-ttu-id="e390f-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.models.Api20180601Preview.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="e390f-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span></span>

## <span data-ttu-id="e390f-148">筆記</span><span class="sxs-lookup"><span data-stu-id="e390f-148">NOTES</span></span>

<span data-ttu-id="e390f-149">別名</span><span class="sxs-lookup"><span data-stu-id="e390f-149">ALIASES</span></span>

<span data-ttu-id="e390f-150">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="e390f-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e390f-151">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="e390f-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e390f-152">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="e390f-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e390f-153">INPUTOBJECT： <IMariaDbIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="e390f-153">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e390f-154">`[ConfigurationName <String>]`：伺服器組組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e390f-154">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="e390f-155">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="e390f-155">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="e390f-156">`[FirewallRuleName <String>]`：伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="e390f-156">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="e390f-157">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="e390f-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e390f-158">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="e390f-158">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="e390f-159">`[ResourceGroupName <String>]`：包含資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="e390f-159">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="e390f-160">您可以從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="e390f-160">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="e390f-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`：安全性警示策略的名稱。</span><span class="sxs-lookup"><span data-stu-id="e390f-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="e390f-162">`[ServerName <String>]`：伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="e390f-162">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="e390f-163">`[SubscriptionId <String>]`：識別 Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="e390f-163">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="e390f-164">`[VirtualNetworkRuleName <String>]`：虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="e390f-164">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="e390f-165">相關連結</span><span class="sxs-lookup"><span data-stu-id="e390f-165">RELATED LINKS</span></span>

