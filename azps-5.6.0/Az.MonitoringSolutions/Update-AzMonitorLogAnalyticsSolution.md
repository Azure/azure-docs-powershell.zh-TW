---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/powershell/module/az.monitoringsolutions/update-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Update-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Update-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: e1c1181dc81d5d15fbaed02fa255961cefe2ae28
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910042"
---
# <span data-ttu-id="02540-101">Update-AzMonitorLogAnalyticsSolution</span><span class="sxs-lookup"><span data-stu-id="02540-101">Update-AzMonitorLogAnalyticsSolution</span></span>

## <span data-ttu-id="02540-102">簡介</span><span class="sxs-lookup"><span data-stu-id="02540-102">SYNOPSIS</span></span>
<span data-ttu-id="02540-103">更新解決方案的標記。</span><span class="sxs-lookup"><span data-stu-id="02540-103">Update the tags of a solution.</span></span>

## <span data-ttu-id="02540-104">語法</span><span class="sxs-lookup"><span data-stu-id="02540-104">SYNTAX</span></span>

### <span data-ttu-id="02540-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="02540-105">UpdateExpanded (Default)</span></span>
```
Update-AzMonitorLogAnalyticsSolution -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="02540-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="02540-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMonitorLogAnalyticsSolution -InputObject <IMonitoringSolutionsIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="02540-107">描述</span><span class="sxs-lookup"><span data-stu-id="02540-107">DESCRIPTION</span></span>
<span data-ttu-id="02540-108">更新解決方案的標記。</span><span class="sxs-lookup"><span data-stu-id="02540-108">Update the tags of a solution.</span></span>

## <span data-ttu-id="02540-109">例子</span><span class="sxs-lookup"><span data-stu-id="02540-109">EXAMPLES</span></span>

### <span data-ttu-id="02540-110">範例 1：根據名稱更新監視器記錄分析解決方案</span><span class="sxs-lookup"><span data-stu-id="02540-110">Example 1: Update a monitor log analytics solution by name</span></span>
```powershell
PS C:\> Update-AzMonitorLogAnalyticsSolution -ResourceGroupName lucas-manual-test -Name 'Containers(monitoringworkspace-2vob7n)' -Tag @{'Operation'='update';'Param'='Tag'}

Name                                   Type                                     Location
----                                   ----                                     --------
Containers(monitoringworkspace-2vob7n) Microsoft.OperationsManagement/solutions East US
```

<span data-ttu-id="02540-111">此命令會更新監視器記錄分析解決方案的名稱。</span><span class="sxs-lookup"><span data-stu-id="02540-111">This command updates a monitor log analytics solution by name.</span></span>

### <span data-ttu-id="02540-112">範例 2：根據物件更新監視器記錄分析解決方案</span><span class="sxs-lookup"><span data-stu-id="02540-112">Example 2: Update a monitor log analytics solution by object</span></span>
```powershell
PS C:\> $monitor = Get-AzMonitorLogAnalyticsSolution -ResourceGroupName lucas-manual-test -Name 'Containers(monitoringworkspace-2vob7n)'
PS C:\> Update-AzMonitorLogAnalyticsSolution -InputObject $monitor -Tag @{'Operation'='update';'Param'='Tag'}

Name                                   Type                                     Location
----                                   ----                                     --------
Containers(monitoringworkspace-2vob7n) Microsoft.OperationsManagement/solutions East US
```

<span data-ttu-id="02540-113">此命令會按物件更新監視器記錄分析解決方案。</span><span class="sxs-lookup"><span data-stu-id="02540-113">This command updates a monitor log analytics solution by object.</span></span>

## <span data-ttu-id="02540-114">參數</span><span class="sxs-lookup"><span data-stu-id="02540-114">PARAMETERS</span></span>

### <span data-ttu-id="02540-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02540-115">-DefaultProfile</span></span>
<span data-ttu-id="02540-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="02540-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02540-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="02540-117">-InputObject</span></span>
<span data-ttu-id="02540-118">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="02540-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="02540-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="02540-119">-Name</span></span>
<span data-ttu-id="02540-120">使用者解決方案名稱。</span><span class="sxs-lookup"><span data-stu-id="02540-120">User Solution Name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: SolutionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02540-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02540-121">-ResourceGroupName</span></span>
<span data-ttu-id="02540-122">要取得的資源組名。</span><span class="sxs-lookup"><span data-stu-id="02540-122">The name of the resource group to get.</span></span>
<span data-ttu-id="02540-123">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="02540-123">The name is case insensitive.</span></span>

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

### <span data-ttu-id="02540-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="02540-124">-SubscriptionId</span></span>
<span data-ttu-id="02540-125">獲得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="02540-125">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="02540-126">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="02540-126">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="02540-127">-標記</span><span class="sxs-lookup"><span data-stu-id="02540-127">-Tag</span></span>
<span data-ttu-id="02540-128">資源標記</span><span class="sxs-lookup"><span data-stu-id="02540-128">Resource tags</span></span>

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

### <span data-ttu-id="02540-129">-確認</span><span class="sxs-lookup"><span data-stu-id="02540-129">-Confirm</span></span>
<span data-ttu-id="02540-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="02540-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02540-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02540-131">-WhatIf</span></span>
<span data-ttu-id="02540-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="02540-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02540-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="02540-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02540-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02540-134">CommonParameters</span></span>
<span data-ttu-id="02540-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="02540-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02540-136">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="02540-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02540-137">輸入</span><span class="sxs-lookup"><span data-stu-id="02540-137">INPUTS</span></span>

### <span data-ttu-id="02540-138">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.models.IMonitoringSolutionsIdentity</span><span class="sxs-lookup"><span data-stu-id="02540-138">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span></span>

## <span data-ttu-id="02540-139">輸出</span><span class="sxs-lookup"><span data-stu-id="02540-139">OUTPUTS</span></span>

### <span data-ttu-id="02540-140">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.models.Api20151101Preview.ISolution</span><span class="sxs-lookup"><span data-stu-id="02540-140">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.Api20151101Preview.ISolution</span></span>

## <span data-ttu-id="02540-141">筆記</span><span class="sxs-lookup"><span data-stu-id="02540-141">NOTES</span></span>

<span data-ttu-id="02540-142">別名</span><span class="sxs-lookup"><span data-stu-id="02540-142">ALIASES</span></span>

<span data-ttu-id="02540-143">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="02540-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="02540-144">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="02540-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="02540-145">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="02540-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="02540-146">INPUTOBJECT： <IMonitoringSolutionsIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="02540-146">INPUTOBJECT <IMonitoringSolutionsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="02540-147">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="02540-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="02540-148">`[ManagementAssociationName <String>]`：User ManagementAssociation Name.</span><span class="sxs-lookup"><span data-stu-id="02540-148">`[ManagementAssociationName <String>]`: User ManagementAssociation Name.</span></span>
  - <span data-ttu-id="02540-149">`[ManagementConfigurationName <String>]`：使用者管理組組名。</span><span class="sxs-lookup"><span data-stu-id="02540-149">`[ManagementConfigurationName <String>]`: User Management Configuration Name.</span></span>
  - <span data-ttu-id="02540-150">`[ProviderName <String>]`：父資源的提供者名稱。</span><span class="sxs-lookup"><span data-stu-id="02540-150">`[ProviderName <String>]`: Provider name for the parent resource.</span></span>
  - <span data-ttu-id="02540-151">`[ResourceGroupName <String>]`：要取得的資源組名。</span><span class="sxs-lookup"><span data-stu-id="02540-151">`[ResourceGroupName <String>]`: The name of the resource group to get.</span></span> <span data-ttu-id="02540-152">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="02540-152">The name is case insensitive.</span></span>
  - <span data-ttu-id="02540-153">`[ResourceName <String>]`：父資源名稱。</span><span class="sxs-lookup"><span data-stu-id="02540-153">`[ResourceName <String>]`: Parent resource name.</span></span>
  - <span data-ttu-id="02540-154">`[ResourceType <String>]`：父資源的資源類型</span><span class="sxs-lookup"><span data-stu-id="02540-154">`[ResourceType <String>]`: Resource type for the parent resource</span></span>
  - <span data-ttu-id="02540-155">`[SolutionName <String>]`：使用者解決方案名稱。</span><span class="sxs-lookup"><span data-stu-id="02540-155">`[SolutionName <String>]`: User Solution Name.</span></span>
  - <span data-ttu-id="02540-156">`[SubscriptionId <String>]`：獲得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="02540-156">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="02540-157">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="02540-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="02540-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="02540-158">RELATED LINKS</span></span>

