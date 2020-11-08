---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlVirtualNetworkRule.md
ms.openlocfilehash: f98c24ab0be3b2c35ac43642fb9d4bbf0b421c7e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127562"
---
# <span data-ttu-id="69860-101">Update-AzMySqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="69860-101">Update-AzMySqlVirtualNetworkRule</span></span>

## <span data-ttu-id="69860-102">摘要</span><span class="sxs-lookup"><span data-stu-id="69860-102">SYNOPSIS</span></span>
<span data-ttu-id="69860-103">建立或更新現有的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="69860-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="69860-104">句法</span><span class="sxs-lookup"><span data-stu-id="69860-104">SYNTAX</span></span>

### <span data-ttu-id="69860-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="69860-105">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -SubnetId <String> [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="69860-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="69860-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlVirtualNetworkRule -InputObject <IMySqlIdentity> -SubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="69860-107">說明</span><span class="sxs-lookup"><span data-stu-id="69860-107">DESCRIPTION</span></span>
<span data-ttu-id="69860-108">建立或更新現有的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="69860-108">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="69860-109">示例</span><span class="sxs-lookup"><span data-stu-id="69860-109">EXAMPLES</span></span>

### <span data-ttu-id="69860-110">範例1：依名稱更新 MySql 虛擬網路規則</span><span class="sxs-lookup"><span data-stu-id="69860-110">Example 1: Update MySql Virtual Network Rule by name</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.Network/virtualNetworks/MySqlVNet/subnets/MysqlSubnet2"
PS C:\> Update-AzMySqlVirtualNetworkRule -Name $env.VNetName -ResourceGroupName $env.resourceGroup -ServerName $env.serverName -SubnetId $ID

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="69860-111">這個 Cmdlet 會依名稱更新 MySql 虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="69860-111">This cmdlet updates MySql Virtual Network Rule by name.</span></span>

### <span data-ttu-id="69860-112">範例2：依身分識別更新 MySql 虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="69860-112">Example 2: Update MySql Virtual Network Rule by identity.</span></span>
```powershell
PS C:\> $SubnetID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.Network/virtualNetworks/MySqlVNet/subnets/MysqlSubnet1"
PS C:\> $VNetID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/virtualNetworkRules/vnet"
PS C:\> Update-AzMySqlVirtualNetworkRule -InputObject $VNetID -SubnetId $SubnetID

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="69860-113">這些 Cmdlet 會依身分識別來更新 MySql 虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="69860-113">These cmdlets update MySql Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="69860-114">參數</span><span class="sxs-lookup"><span data-stu-id="69860-114">PARAMETERS</span></span>

### <span data-ttu-id="69860-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="69860-115">-AsJob</span></span>
<span data-ttu-id="69860-116">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="69860-116">Run the command as a job</span></span>

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

### <span data-ttu-id="69860-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69860-117">-DefaultProfile</span></span>
<span data-ttu-id="69860-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="69860-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69860-119">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="69860-119">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="69860-120">在虛擬網路啟用 vnet 服務端點之前，請先建立防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="69860-120">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="69860-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="69860-121">-InputObject</span></span>
<span data-ttu-id="69860-122">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="69860-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="69860-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="69860-123">-Name</span></span>
<span data-ttu-id="69860-124">虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="69860-124">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="69860-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="69860-125">-NoWait</span></span>
<span data-ttu-id="69860-126">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="69860-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="69860-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="69860-127">-PassThru</span></span>
<span data-ttu-id="69860-128">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="69860-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="69860-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69860-129">-ResourceGroupName</span></span>
<span data-ttu-id="69860-130">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="69860-130">The name of the resource group.</span></span>
<span data-ttu-id="69860-131">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="69860-131">The name is case insensitive.</span></span>

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

### <span data-ttu-id="69860-132">-ServerName</span><span class="sxs-lookup"><span data-stu-id="69860-132">-ServerName</span></span>
<span data-ttu-id="69860-133">伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="69860-133">The name of the server.</span></span>

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

### <span data-ttu-id="69860-134">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="69860-134">-SubnetId</span></span>
<span data-ttu-id="69860-135">虛擬網路子網的 ARM 資源 id。</span><span class="sxs-lookup"><span data-stu-id="69860-135">The ARM resource id of the virtual network subnet.</span></span>

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

### <span data-ttu-id="69860-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="69860-136">-SubscriptionId</span></span>
<span data-ttu-id="69860-137">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="69860-137">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="69860-138">-確認</span><span class="sxs-lookup"><span data-stu-id="69860-138">-Confirm</span></span>
<span data-ttu-id="69860-139">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="69860-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69860-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69860-140">-WhatIf</span></span>
<span data-ttu-id="69860-141">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="69860-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69860-142">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="69860-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69860-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69860-143">CommonParameters</span></span>
<span data-ttu-id="69860-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="69860-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69860-145">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="69860-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69860-146">輸入</span><span class="sxs-lookup"><span data-stu-id="69860-146">INPUTS</span></span>

### <span data-ttu-id="69860-147">IMySqlIdentity 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="69860-147">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="69860-148">輸出</span><span class="sxs-lookup"><span data-stu-id="69860-148">OUTPUTS</span></span>

### <span data-ttu-id="69860-149">IVirtualNetworkRule 中的 Api20171201 （）。</span><span class="sxs-lookup"><span data-stu-id="69860-149">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="69860-150">筆記</span><span class="sxs-lookup"><span data-stu-id="69860-150">NOTES</span></span>

<span data-ttu-id="69860-151">別名</span><span class="sxs-lookup"><span data-stu-id="69860-151">ALIASES</span></span>

<span data-ttu-id="69860-152">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="69860-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="69860-153">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="69860-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="69860-154">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="69860-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="69860-155">INPUTOBJECT <IMySqlIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="69860-155">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="69860-156">`[ConfigurationName <String>]`：伺服器配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="69860-156">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="69860-157">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="69860-157">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="69860-158">`[FirewallRuleName <String>]`：伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="69860-158">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="69860-159">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="69860-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="69860-160">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="69860-160">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="69860-161">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="69860-161">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="69860-162">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="69860-162">The name is case insensitive.</span></span>
  - <span data-ttu-id="69860-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`：安全警示原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="69860-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="69860-164">`[ServerName <String>]`：伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="69860-164">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="69860-165">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="69860-165">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="69860-166">`[VirtualNetworkRuleName <String>]`：虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="69860-166">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="69860-167">相關連結</span><span class="sxs-lookup"><span data-stu-id="69860-167">RELATED LINKS</span></span>
