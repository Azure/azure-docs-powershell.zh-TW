---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/update-azmariadbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbVirtualNetworkRule.md
ms.openlocfilehash: 9ec9113ba17ec28e7cef934a4b857e4cbf0acce0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98276776"
---
# <span data-ttu-id="823be-101">Update-AzMariaDbVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="823be-101">Update-AzMariaDbVirtualNetworkRule</span></span>

## <span data-ttu-id="823be-102">摘要</span><span class="sxs-lookup"><span data-stu-id="823be-102">SYNOPSIS</span></span>
<span data-ttu-id="823be-103">建立或更新現有的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="823be-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="823be-104">句法</span><span class="sxs-lookup"><span data-stu-id="823be-104">SYNTAX</span></span>

### <span data-ttu-id="823be-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="823be-105">UpdateExpanded (Default)</span></span>
```
Update-AzMariaDbVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint] [-SubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="823be-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="823be-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMariaDbVirtualNetworkRule -InputObject <IMariaDbIdentity> [-IgnoreMissingVnetServiceEndpoint]
 [-SubnetId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="823be-107">說明</span><span class="sxs-lookup"><span data-stu-id="823be-107">DESCRIPTION</span></span>
<span data-ttu-id="823be-108">建立或更新現有的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="823be-108">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="823be-109">示例</span><span class="sxs-lookup"><span data-stu-id="823be-109">EXAMPLES</span></span>

### <span data-ttu-id="823be-110">範例1：更新 MariaDB 虛擬網路規則</span><span class="sxs-lookup"><span data-stu-id="823be-110">Example 1: Update MariaDB virtual network rule</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name vnet -ResourceGroupName mariadb-test-qu5ov0
PS C:\> Update-AzMariaDbVirtualNetworkRule -ServerName mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 -Name vnetrule-QdMJpU -SubnetId $vnet.Subnets[0].Id -IgnoreMissingVnetServiceEndpoint

Name            Type
----            ----
vnetrule-QdMJpU Microsoft.DBforMariaDB/servers/virtualNetworkRules
```

<span data-ttu-id="823be-111">這個命令會更新虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="823be-111">This command updates a virtual network rule.</span></span>

## <span data-ttu-id="823be-112">參數</span><span class="sxs-lookup"><span data-stu-id="823be-112">PARAMETERS</span></span>

### <span data-ttu-id="823be-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="823be-113">-AsJob</span></span>
<span data-ttu-id="823be-114">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="823be-114">Run the command as a job</span></span>

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

### <span data-ttu-id="823be-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="823be-115">-DefaultProfile</span></span>
<span data-ttu-id="823be-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="823be-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="823be-117">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="823be-117">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="823be-118">在虛擬網路啟用 vnet 服務端點之前，請先建立防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="823be-118">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="823be-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="823be-119">-InputObject</span></span>
<span data-ttu-id="823be-120">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="823be-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="823be-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="823be-121">-Name</span></span>
<span data-ttu-id="823be-122">虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="823be-122">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="823be-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="823be-123">-NoWait</span></span>
<span data-ttu-id="823be-124">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="823be-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="823be-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="823be-125">-PassThru</span></span>
<span data-ttu-id="823be-126">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="823be-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="823be-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="823be-127">-ResourceGroupName</span></span>
<span data-ttu-id="823be-128">包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="823be-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="823be-129">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="823be-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="823be-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="823be-130">-ServerName</span></span>
<span data-ttu-id="823be-131">伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="823be-131">The name of the server.</span></span>

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

### <span data-ttu-id="823be-132">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="823be-132">-SubnetId</span></span>
<span data-ttu-id="823be-133">虛擬網路子網的 ARM 資源 id。</span><span class="sxs-lookup"><span data-stu-id="823be-133">The ARM resource id of the virtual network subnet.</span></span>

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

### <span data-ttu-id="823be-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="823be-134">-SubscriptionId</span></span>
<span data-ttu-id="823be-135">識別 Azure 訂閱的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="823be-135">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="823be-136">-確認</span><span class="sxs-lookup"><span data-stu-id="823be-136">-Confirm</span></span>
<span data-ttu-id="823be-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="823be-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="823be-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="823be-138">-WhatIf</span></span>
<span data-ttu-id="823be-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="823be-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="823be-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="823be-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="823be-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="823be-141">CommonParameters</span></span>
<span data-ttu-id="823be-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="823be-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="823be-143">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="823be-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="823be-144">輸入</span><span class="sxs-lookup"><span data-stu-id="823be-144">INPUTS</span></span>

### <span data-ttu-id="823be-145">IMariaDbIdentity （MariaDb）的</span><span class="sxs-lookup"><span data-stu-id="823be-145">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="823be-146">輸出</span><span class="sxs-lookup"><span data-stu-id="823be-146">OUTPUTS</span></span>

### <span data-ttu-id="823be-147">IVirtualNetworkRule （MariaDb）。 Api20180601Preview。</span><span class="sxs-lookup"><span data-stu-id="823be-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span></span>

## <span data-ttu-id="823be-148">筆記</span><span class="sxs-lookup"><span data-stu-id="823be-148">NOTES</span></span>

<span data-ttu-id="823be-149">別名</span><span class="sxs-lookup"><span data-stu-id="823be-149">ALIASES</span></span>

<span data-ttu-id="823be-150">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="823be-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="823be-151">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="823be-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="823be-152">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="823be-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="823be-153">INPUTOBJECT <IMariaDbIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="823be-153">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="823be-154">`[ConfigurationName <String>]`：伺服器配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="823be-154">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="823be-155">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="823be-155">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="823be-156">`[FirewallRuleName <String>]`：伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="823be-156">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="823be-157">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="823be-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="823be-158">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="823be-158">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="823be-159">`[ResourceGroupName <String>]`：包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="823be-159">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="823be-160">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="823be-160">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="823be-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`：安全警示原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="823be-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="823be-162">`[ServerName <String>]`：伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="823be-162">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="823be-163">`[SubscriptionId <String>]`：識別 Azure 訂閱的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="823be-163">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="823be-164">`[VirtualNetworkRuleName <String>]`：虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="823be-164">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="823be-165">相關連結</span><span class="sxs-lookup"><span data-stu-id="823be-165">RELATED LINKS</span></span>

