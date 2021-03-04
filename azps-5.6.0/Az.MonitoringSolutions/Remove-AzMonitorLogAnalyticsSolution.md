---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/powershell/module/az.monitoringsolutions/remove-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Remove-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Remove-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: f3a41317663c5b1009a45bfe711cdf3410a784c1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910050"
---
# <span data-ttu-id="f6e70-101">Remove-AzMonitorLogAnalyticsSolution</span><span class="sxs-lookup"><span data-stu-id="f6e70-101">Remove-AzMonitorLogAnalyticsSolution</span></span>

## <span data-ttu-id="f6e70-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f6e70-102">SYNOPSIS</span></span>
<span data-ttu-id="f6e70-103">刪除訂閱中的解決方案。</span><span class="sxs-lookup"><span data-stu-id="f6e70-103">Deletes the solution in the subscription.</span></span>

## <span data-ttu-id="f6e70-104">語法</span><span class="sxs-lookup"><span data-stu-id="f6e70-104">SYNTAX</span></span>

### <span data-ttu-id="f6e70-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="f6e70-105">Delete (Default)</span></span>
```
Remove-AzMonitorLogAnalyticsSolution -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f6e70-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f6e70-106">DeleteViaIdentity</span></span>
```
Remove-AzMonitorLogAnalyticsSolution -InputObject <IMonitoringSolutionsIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f6e70-107">描述</span><span class="sxs-lookup"><span data-stu-id="f6e70-107">DESCRIPTION</span></span>
<span data-ttu-id="f6e70-108">刪除訂閱中的解決方案。</span><span class="sxs-lookup"><span data-stu-id="f6e70-108">Deletes the solution in the subscription.</span></span>

## <span data-ttu-id="f6e70-109">例子</span><span class="sxs-lookup"><span data-stu-id="f6e70-109">EXAMPLES</span></span>

### <span data-ttu-id="f6e70-110">範例 1：根據名稱移除監視器記錄分析解決方案</span><span class="sxs-lookup"><span data-stu-id="f6e70-110">Example 1: Remove a monitor log analytics solution by name</span></span>
```powershell
PS C:\> Remove-AzMonitorLogAnalyticsSolution  -ResourceGroupName azureps-manual-test -Name 'Containers(monitoringworkspace-2vob7n)'

```

<span data-ttu-id="f6e70-111">此命令會移除監視器記錄分析解決方案的名稱。</span><span class="sxs-lookup"><span data-stu-id="f6e70-111">This command removes a monitor log analytics solution by name.</span></span>

### <span data-ttu-id="f6e70-112">範例 2：移除監視器記錄分析解決方案</span><span class="sxs-lookup"><span data-stu-id="f6e70-112">Example 2: Remove a monitor log analytics solution by object</span></span>
```powershell
PS C:\> $monitor = Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-manual-test -Name 'Containers(monitoringworkspace-pevful)'
PS C:\> Remove-AzMonitorLogAnalyticsSolution -InputObject $monitor

```

<span data-ttu-id="f6e70-113">此命令會移除監視器記錄分析解決方案 ，並按物件。</span><span class="sxs-lookup"><span data-stu-id="f6e70-113">This command removes a monitor log analytics solution by object.</span></span>

### <span data-ttu-id="f6e70-114">範例 3：根據管線移除監視器記錄分析解決方案</span><span class="sxs-lookup"><span data-stu-id="f6e70-114">Example 3: Remove a monitor log analytics solution by pipeline</span></span>
```powershell
PS C:\> $monitor = Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-manual-test -Name 'Containers(monitoringworkspace-asdehu)' | Remove-AzMonitorLogAnalyticsSolution

```

<span data-ttu-id="f6e70-115">此命令會移除根據管線的監視器記錄分析解決方案。</span><span class="sxs-lookup"><span data-stu-id="f6e70-115">This command removes a monitor log analytics solution by pipeline.</span></span>

## <span data-ttu-id="f6e70-116">參數</span><span class="sxs-lookup"><span data-stu-id="f6e70-116">PARAMETERS</span></span>

### <span data-ttu-id="f6e70-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6e70-117">-DefaultProfile</span></span>
<span data-ttu-id="f6e70-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f6e70-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6e70-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f6e70-119">-InputObject</span></span>
<span data-ttu-id="f6e70-120">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="f6e70-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f6e70-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="f6e70-121">-Name</span></span>
<span data-ttu-id="f6e70-122">使用者解決方案名稱。</span><span class="sxs-lookup"><span data-stu-id="f6e70-122">User Solution Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: SolutionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6e70-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f6e70-123">-PassThru</span></span>
<span data-ttu-id="f6e70-124">命令成功時，會返回 True</span><span class="sxs-lookup"><span data-stu-id="f6e70-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="f6e70-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6e70-125">-ResourceGroupName</span></span>
<span data-ttu-id="f6e70-126">要取得的資源組名。</span><span class="sxs-lookup"><span data-stu-id="f6e70-126">The name of the resource group to get.</span></span>
<span data-ttu-id="f6e70-127">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="f6e70-127">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6e70-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f6e70-128">-SubscriptionId</span></span>
<span data-ttu-id="f6e70-129">獲得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="f6e70-129">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f6e70-130">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="f6e70-130">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6e70-131">-確認</span><span class="sxs-lookup"><span data-stu-id="f6e70-131">-Confirm</span></span>
<span data-ttu-id="f6e70-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f6e70-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6e70-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6e70-133">-WhatIf</span></span>
<span data-ttu-id="f6e70-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f6e70-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6e70-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f6e70-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6e70-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6e70-136">CommonParameters</span></span>
<span data-ttu-id="f6e70-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f6e70-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6e70-138">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f6e70-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6e70-139">輸入</span><span class="sxs-lookup"><span data-stu-id="f6e70-139">INPUTS</span></span>

### <span data-ttu-id="f6e70-140">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.models.IMonitoringSolutionsIdentity</span><span class="sxs-lookup"><span data-stu-id="f6e70-140">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span></span>

## <span data-ttu-id="f6e70-141">輸出</span><span class="sxs-lookup"><span data-stu-id="f6e70-141">OUTPUTS</span></span>

### <span data-ttu-id="f6e70-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f6e70-142">System.Boolean</span></span>

## <span data-ttu-id="f6e70-143">筆記</span><span class="sxs-lookup"><span data-stu-id="f6e70-143">NOTES</span></span>

<span data-ttu-id="f6e70-144">別名</span><span class="sxs-lookup"><span data-stu-id="f6e70-144">ALIASES</span></span>

<span data-ttu-id="f6e70-145">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="f6e70-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f6e70-146">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="f6e70-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f6e70-147">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="f6e70-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f6e70-148">INPUTOBJECT： <IMonitoringSolutionsIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="f6e70-148">INPUTOBJECT <IMonitoringSolutionsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f6e70-149">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="f6e70-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f6e70-150">`[ManagementAssociationName <String>]`：User ManagementAssociation Name.</span><span class="sxs-lookup"><span data-stu-id="f6e70-150">`[ManagementAssociationName <String>]`: User ManagementAssociation Name.</span></span>
  - <span data-ttu-id="f6e70-151">`[ManagementConfigurationName <String>]`：使用者管理組組名。</span><span class="sxs-lookup"><span data-stu-id="f6e70-151">`[ManagementConfigurationName <String>]`: User Management Configuration Name.</span></span>
  - <span data-ttu-id="f6e70-152">`[ProviderName <String>]`：父資源的提供者名稱。</span><span class="sxs-lookup"><span data-stu-id="f6e70-152">`[ProviderName <String>]`: Provider name for the parent resource.</span></span>
  - <span data-ttu-id="f6e70-153">`[ResourceGroupName <String>]`：要取得的資源組名。</span><span class="sxs-lookup"><span data-stu-id="f6e70-153">`[ResourceGroupName <String>]`: The name of the resource group to get.</span></span> <span data-ttu-id="f6e70-154">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="f6e70-154">The name is case insensitive.</span></span>
  - <span data-ttu-id="f6e70-155">`[ResourceName <String>]`：父資源名稱。</span><span class="sxs-lookup"><span data-stu-id="f6e70-155">`[ResourceName <String>]`: Parent resource name.</span></span>
  - <span data-ttu-id="f6e70-156">`[ResourceType <String>]`：父資源的資源類型</span><span class="sxs-lookup"><span data-stu-id="f6e70-156">`[ResourceType <String>]`: Resource type for the parent resource</span></span>
  - <span data-ttu-id="f6e70-157">`[SolutionName <String>]`：使用者解決方案名稱。</span><span class="sxs-lookup"><span data-stu-id="f6e70-157">`[SolutionName <String>]`: User Solution Name.</span></span>
  - <span data-ttu-id="f6e70-158">`[SubscriptionId <String>]`：獲得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="f6e70-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="f6e70-159">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="f6e70-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="f6e70-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="f6e70-160">RELATED LINKS</span></span>

