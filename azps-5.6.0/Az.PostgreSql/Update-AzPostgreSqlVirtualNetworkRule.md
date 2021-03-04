---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/update-azpostgresqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlVirtualNetworkRule.md
ms.openlocfilehash: 89c11be18fbb603f2b05fa9768a3ce05d51ddd86
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907581"
---
# <span data-ttu-id="99a8e-101">Update-AzPostgreSqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="99a8e-101">Update-AzPostgreSqlVirtualNetworkRule</span></span>

## <span data-ttu-id="99a8e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="99a8e-102">SYNOPSIS</span></span>
<span data-ttu-id="99a8e-103">建立或更新現有的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="99a8e-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="99a8e-104">語法</span><span class="sxs-lookup"><span data-stu-id="99a8e-104">SYNTAX</span></span>

### <span data-ttu-id="99a8e-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="99a8e-105">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -SubnetId <String> [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="99a8e-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="99a8e-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlVirtualNetworkRule -InputObject <IPostgreSqlIdentity> -SubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="99a8e-107">描述</span><span class="sxs-lookup"><span data-stu-id="99a8e-107">DESCRIPTION</span></span>
<span data-ttu-id="99a8e-108">建立或更新現有的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="99a8e-108">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="99a8e-109">例子</span><span class="sxs-lookup"><span data-stu-id="99a8e-109">EXAMPLES</span></span>

### <span data-ttu-id="99a8e-110">範例 1：依名稱更新 PostgreSql 虛擬網路規則</span><span class="sxs-lookup"><span data-stu-id="99a8e-110">Example 1: Update PostgreSql Virtual Network Rule by name</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.Network/virtualNetworks/PostgreSqlVNet/subnets/default2"
PS C:\> Update-AzPostgreSqlVirtualNetworkRule -Name vnet -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -SubnetId $ID

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="99a8e-111">此 Cmdlet 會依名稱更新 PostgreSql 虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="99a8e-111">This cmdlet updates PostgreSql Virtual Network Rule by name.</span></span>

### <span data-ttu-id="99a8e-112">範例 2：依身分識別更新 PostgreSql 虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="99a8e-112">Example 2: Update PostgreSql Virtual Network Rule by identity.</span></span>
```powershell
PS C:\> $SubnetID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.Network/virtualNetworks/PostgreSqlVNet/subnets/default"
PS C:\> $VNetID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/virtualNetworkRules/vnet"
PS C:\> Update-AzPostgreSqlVirtualNetworkRule -InputObject $VNetID -SubnetId $SubnetID

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="99a8e-113">這些 Cmdlet 會依身分識別更新 PostgreSql 虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="99a8e-113">These cmdlets update PostgreSql Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="99a8e-114">參數</span><span class="sxs-lookup"><span data-stu-id="99a8e-114">PARAMETERS</span></span>

### <span data-ttu-id="99a8e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="99a8e-115">-AsJob</span></span>
<span data-ttu-id="99a8e-116">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="99a8e-116">Run the command as a job</span></span>

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

### <span data-ttu-id="99a8e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99a8e-117">-DefaultProfile</span></span>
<span data-ttu-id="99a8e-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="99a8e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99a8e-119">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="99a8e-119">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="99a8e-120">在啟用 vnet 服務端點之前建立防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="99a8e-120">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="99a8e-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="99a8e-121">-InputObject</span></span>
<span data-ttu-id="99a8e-122">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="99a8e-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="99a8e-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="99a8e-123">-Name</span></span>
<span data-ttu-id="99a8e-124">虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="99a8e-124">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="99a8e-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="99a8e-125">-NoWait</span></span>
<span data-ttu-id="99a8e-126">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="99a8e-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="99a8e-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="99a8e-127">-PassThru</span></span>
<span data-ttu-id="99a8e-128">命令成功時，會返回 True</span><span class="sxs-lookup"><span data-stu-id="99a8e-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="99a8e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99a8e-129">-ResourceGroupName</span></span>
<span data-ttu-id="99a8e-130">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="99a8e-130">The name of the resource group.</span></span>
<span data-ttu-id="99a8e-131">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="99a8e-131">The name is case insensitive.</span></span>

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

### <span data-ttu-id="99a8e-132">-ServerName</span><span class="sxs-lookup"><span data-stu-id="99a8e-132">-ServerName</span></span>
<span data-ttu-id="99a8e-133">伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="99a8e-133">The name of the server.</span></span>

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

### <span data-ttu-id="99a8e-134">-子網Id</span><span class="sxs-lookup"><span data-stu-id="99a8e-134">-SubnetId</span></span>
<span data-ttu-id="99a8e-135">虛擬網路子網的 ARM 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="99a8e-135">The ARM resource id of the virtual network subnet.</span></span>

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

### <span data-ttu-id="99a8e-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="99a8e-136">-SubscriptionId</span></span>
<span data-ttu-id="99a8e-137">目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="99a8e-137">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="99a8e-138">-確認</span><span class="sxs-lookup"><span data-stu-id="99a8e-138">-Confirm</span></span>
<span data-ttu-id="99a8e-139">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="99a8e-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99a8e-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99a8e-140">-WhatIf</span></span>
<span data-ttu-id="99a8e-141">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="99a8e-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99a8e-142">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="99a8e-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99a8e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99a8e-143">CommonParameters</span></span>
<span data-ttu-id="99a8e-144">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="99a8e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99a8e-145">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="99a8e-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99a8e-146">輸入</span><span class="sxs-lookup"><span data-stu-id="99a8e-146">INPUTS</span></span>

### <span data-ttu-id="99a8e-147">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="99a8e-147">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="99a8e-148">輸出</span><span class="sxs-lookup"><span data-stu-id="99a8e-148">OUTPUTS</span></span>

### <span data-ttu-id="99a8e-149">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="99a8e-149">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="99a8e-150">筆記</span><span class="sxs-lookup"><span data-stu-id="99a8e-150">NOTES</span></span>

<span data-ttu-id="99a8e-151">別名</span><span class="sxs-lookup"><span data-stu-id="99a8e-151">ALIASES</span></span>

<span data-ttu-id="99a8e-152">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="99a8e-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="99a8e-153">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="99a8e-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="99a8e-154">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="99a8e-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="99a8e-155">INPUTOBJECT： <IPostgreSqlIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="99a8e-155">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="99a8e-156">`[ConfigurationName <String>]`：伺服器組組的名稱。</span><span class="sxs-lookup"><span data-stu-id="99a8e-156">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="99a8e-157">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="99a8e-157">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="99a8e-158">`[FirewallRuleName <String>]`：伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="99a8e-158">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="99a8e-159">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="99a8e-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="99a8e-160">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="99a8e-160">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="99a8e-161">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="99a8e-161">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="99a8e-162">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="99a8e-162">The name is case insensitive.</span></span>
  - <span data-ttu-id="99a8e-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`：安全性警示策略的名稱。</span><span class="sxs-lookup"><span data-stu-id="99a8e-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="99a8e-164">`[ServerName <String>]`：伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="99a8e-164">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="99a8e-165">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="99a8e-165">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="99a8e-166">`[VirtualNetworkRuleName <String>]`：虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="99a8e-166">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="99a8e-167">相關連結</span><span class="sxs-lookup"><span data-stu-id="99a8e-167">RELATED LINKS</span></span>

