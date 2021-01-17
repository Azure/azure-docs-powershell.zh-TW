---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/update-azpostgresqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlVirtualNetworkRule.md
ms.openlocfilehash: a430247083e84b3d35f820b3c1e2d5f04f4979b5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98437339"
---
# <span data-ttu-id="a487e-101">Update-AzPostgreSqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="a487e-101">Update-AzPostgreSqlVirtualNetworkRule</span></span>

## <span data-ttu-id="a487e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a487e-102">SYNOPSIS</span></span>
<span data-ttu-id="a487e-103">建立或更新現有的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="a487e-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="a487e-104">句法</span><span class="sxs-lookup"><span data-stu-id="a487e-104">SYNTAX</span></span>

### <span data-ttu-id="a487e-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="a487e-105">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -SubnetId <String> [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a487e-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="a487e-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlVirtualNetworkRule -InputObject <IPostgreSqlIdentity> -SubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a487e-107">說明</span><span class="sxs-lookup"><span data-stu-id="a487e-107">DESCRIPTION</span></span>
<span data-ttu-id="a487e-108">建立或更新現有的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="a487e-108">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="a487e-109">示例</span><span class="sxs-lookup"><span data-stu-id="a487e-109">EXAMPLES</span></span>

### <span data-ttu-id="a487e-110">範例1：依名稱更新 PostgreSql 虛擬網路規則</span><span class="sxs-lookup"><span data-stu-id="a487e-110">Example 1: Update PostgreSql Virtual Network Rule by name</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.Network/virtualNetworks/PostgreSqlVNet/subnets/default2"
PS C:\> Update-AzPostgreSqlVirtualNetworkRule -Name vnet -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -SubnetId $ID

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="a487e-111">這個 Cmdlet 會依名稱更新 PostgreSql 虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="a487e-111">This cmdlet updates PostgreSql Virtual Network Rule by name.</span></span>

### <span data-ttu-id="a487e-112">範例2：依身分識別來更新 PostgreSql 虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="a487e-112">Example 2: Update PostgreSql Virtual Network Rule by identity.</span></span>
```powershell
PS C:\> $SubnetID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.Network/virtualNetworks/PostgreSqlVNet/subnets/default"
PS C:\> $VNetID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/virtualNetworkRules/vnet"
PS C:\> Update-AzPostgreSqlVirtualNetworkRule -InputObject $VNetID -SubnetId $SubnetID

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="a487e-113">這些 Cmdlet 會依身分識別來更新 PostgreSql 虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="a487e-113">These cmdlets update PostgreSql Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="a487e-114">參數</span><span class="sxs-lookup"><span data-stu-id="a487e-114">PARAMETERS</span></span>

### <span data-ttu-id="a487e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a487e-115">-AsJob</span></span>
<span data-ttu-id="a487e-116">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="a487e-116">Run the command as a job</span></span>

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

### <span data-ttu-id="a487e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a487e-117">-DefaultProfile</span></span>
<span data-ttu-id="a487e-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a487e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a487e-119">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="a487e-119">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="a487e-120">在虛擬網路啟用 vnet 服務端點之前，請先建立防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="a487e-120">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="a487e-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a487e-121">-InputObject</span></span>
<span data-ttu-id="a487e-122">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="a487e-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a487e-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="a487e-123">-Name</span></span>
<span data-ttu-id="a487e-124">虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="a487e-124">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="a487e-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a487e-125">-NoWait</span></span>
<span data-ttu-id="a487e-126">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="a487e-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a487e-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a487e-127">-PassThru</span></span>
<span data-ttu-id="a487e-128">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="a487e-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="a487e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a487e-129">-ResourceGroupName</span></span>
<span data-ttu-id="a487e-130">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a487e-130">The name of the resource group.</span></span>
<span data-ttu-id="a487e-131">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="a487e-131">The name is case insensitive.</span></span>

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

### <span data-ttu-id="a487e-132">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a487e-132">-ServerName</span></span>
<span data-ttu-id="a487e-133">伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="a487e-133">The name of the server.</span></span>

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

### <span data-ttu-id="a487e-134">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="a487e-134">-SubnetId</span></span>
<span data-ttu-id="a487e-135">虛擬網路子網的 ARM 資源 id。</span><span class="sxs-lookup"><span data-stu-id="a487e-135">The ARM resource id of the virtual network subnet.</span></span>

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

### <span data-ttu-id="a487e-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a487e-136">-SubscriptionId</span></span>
<span data-ttu-id="a487e-137">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="a487e-137">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="a487e-138">-確認</span><span class="sxs-lookup"><span data-stu-id="a487e-138">-Confirm</span></span>
<span data-ttu-id="a487e-139">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a487e-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a487e-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a487e-140">-WhatIf</span></span>
<span data-ttu-id="a487e-141">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a487e-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a487e-142">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a487e-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a487e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a487e-143">CommonParameters</span></span>
<span data-ttu-id="a487e-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a487e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a487e-145">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a487e-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a487e-146">輸入</span><span class="sxs-lookup"><span data-stu-id="a487e-146">INPUTS</span></span>

### <span data-ttu-id="a487e-147">IPostgreSqlIdentity （PostgreSql）的</span><span class="sxs-lookup"><span data-stu-id="a487e-147">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="a487e-148">輸出</span><span class="sxs-lookup"><span data-stu-id="a487e-148">OUTPUTS</span></span>

### <span data-ttu-id="a487e-149">IVirtualNetworkRule （PostgreSql）。 Api20171201。</span><span class="sxs-lookup"><span data-stu-id="a487e-149">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="a487e-150">筆記</span><span class="sxs-lookup"><span data-stu-id="a487e-150">NOTES</span></span>

<span data-ttu-id="a487e-151">別名</span><span class="sxs-lookup"><span data-stu-id="a487e-151">ALIASES</span></span>

<span data-ttu-id="a487e-152">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="a487e-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a487e-153">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="a487e-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a487e-154">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="a487e-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a487e-155">INPUTOBJECT <IPostgreSqlIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="a487e-155">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a487e-156">`[ConfigurationName <String>]`：伺服器配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="a487e-156">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="a487e-157">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="a487e-157">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="a487e-158">`[FirewallRuleName <String>]`：伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="a487e-158">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="a487e-159">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="a487e-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a487e-160">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="a487e-160">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="a487e-161">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a487e-161">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="a487e-162">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="a487e-162">The name is case insensitive.</span></span>
  - <span data-ttu-id="a487e-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`：安全警示原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="a487e-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="a487e-164">`[ServerName <String>]`：伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="a487e-164">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="a487e-165">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="a487e-165">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="a487e-166">`[VirtualNetworkRuleName <String>]`：虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="a487e-166">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="a487e-167">相關連結</span><span class="sxs-lookup"><span data-stu-id="a487e-167">RELATED LINKS</span></span>

