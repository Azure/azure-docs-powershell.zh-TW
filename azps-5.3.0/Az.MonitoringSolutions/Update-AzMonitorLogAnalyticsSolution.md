---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitoringsolutions/update-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Update-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Update-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: a39f347497fe6be31ccb26ce1f726d1eebe155e5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435288"
---
# <span data-ttu-id="6d5a0-101">Update-AzMonitorLogAnalyticsSolution</span><span class="sxs-lookup"><span data-stu-id="6d5a0-101">Update-AzMonitorLogAnalyticsSolution</span></span>

## <span data-ttu-id="6d5a0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6d5a0-102">SYNOPSIS</span></span>
<span data-ttu-id="6d5a0-103">更新解決方案的標記。</span><span class="sxs-lookup"><span data-stu-id="6d5a0-103">Update the tags of a solution.</span></span>

## <span data-ttu-id="6d5a0-104">句法</span><span class="sxs-lookup"><span data-stu-id="6d5a0-104">SYNTAX</span></span>

### <span data-ttu-id="6d5a0-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="6d5a0-105">UpdateExpanded (Default)</span></span>
```
Update-AzMonitorLogAnalyticsSolution -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6d5a0-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="6d5a0-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMonitorLogAnalyticsSolution -InputObject <IMonitoringSolutionsIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6d5a0-107">說明</span><span class="sxs-lookup"><span data-stu-id="6d5a0-107">DESCRIPTION</span></span>
<span data-ttu-id="6d5a0-108">更新解決方案的標記。</span><span class="sxs-lookup"><span data-stu-id="6d5a0-108">Update the tags of a solution.</span></span>

## <span data-ttu-id="6d5a0-109">示例</span><span class="sxs-lookup"><span data-stu-id="6d5a0-109">EXAMPLES</span></span>

### <span data-ttu-id="6d5a0-110">範例1：依名稱更新監視器 log analytics 方案</span><span class="sxs-lookup"><span data-stu-id="6d5a0-110">Example 1: Update a monitor log analytics solution by name</span></span>
```powershell
PS C:\> Update-AzMonitorLogAnalyticsSolution -ResourceGroupName lucas-manual-test -Name 'Containers(monitoringworkspace-2vob7n)' -Tag @{'Operation'='update';'Param'='Tag'}

Name                                   Type                                     Location
----                                   ----                                     --------
Containers(monitoringworkspace-2vob7n) Microsoft.OperationsManagement/solutions East US
```

<span data-ttu-id="6d5a0-111">這個命令會依名稱更新監視器記錄分析方案。</span><span class="sxs-lookup"><span data-stu-id="6d5a0-111">This command updates a monitor log analytics solution by name.</span></span>

### <span data-ttu-id="6d5a0-112">範例2：依物件更新監視記錄分析解決方案</span><span class="sxs-lookup"><span data-stu-id="6d5a0-112">Example 2: Update a monitor log analytics solution by object</span></span>
```powershell
PS C:\> $monitor = Get-AzMonitorLogAnalyticsSolution -ResourceGroupName lucas-manual-test -Name 'Containers(monitoringworkspace-2vob7n)'
PS C:\> Update-AzMonitorLogAnalyticsSolution -InputObject $monitor -Tag @{'Operation'='update';'Param'='Tag'}

Name                                   Type                                     Location
----                                   ----                                     --------
Containers(monitoringworkspace-2vob7n) Microsoft.OperationsManagement/solutions East US
```

<span data-ttu-id="6d5a0-113">這個命令會依物件更新顯示器記錄分析方案。</span><span class="sxs-lookup"><span data-stu-id="6d5a0-113">This command updates a monitor log analytics solution by object.</span></span>

## <span data-ttu-id="6d5a0-114">參數</span><span class="sxs-lookup"><span data-stu-id="6d5a0-114">PARAMETERS</span></span>

### <span data-ttu-id="6d5a0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d5a0-115">-DefaultProfile</span></span>
<span data-ttu-id="6d5a0-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6d5a0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d5a0-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6d5a0-117">-InputObject</span></span>
<span data-ttu-id="6d5a0-118">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="6d5a0-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6d5a0-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="6d5a0-119">-Name</span></span>
<span data-ttu-id="6d5a0-120">使用者方案名稱。</span><span class="sxs-lookup"><span data-stu-id="6d5a0-120">User Solution Name.</span></span>

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

### <span data-ttu-id="6d5a0-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d5a0-121">-ResourceGroupName</span></span>
<span data-ttu-id="6d5a0-122">要取得之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6d5a0-122">The name of the resource group to get.</span></span>
<span data-ttu-id="6d5a0-123">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="6d5a0-123">The name is case insensitive.</span></span>

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

### <span data-ttu-id="6d5a0-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6d5a0-124">-SubscriptionId</span></span>
<span data-ttu-id="6d5a0-125">取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="6d5a0-125">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="6d5a0-126">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="6d5a0-126">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="6d5a0-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="6d5a0-127">-Tag</span></span>
<span data-ttu-id="6d5a0-128">資源標記</span><span class="sxs-lookup"><span data-stu-id="6d5a0-128">Resource tags</span></span>

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

### <span data-ttu-id="6d5a0-129">-確認</span><span class="sxs-lookup"><span data-stu-id="6d5a0-129">-Confirm</span></span>
<span data-ttu-id="6d5a0-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6d5a0-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d5a0-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d5a0-131">-WhatIf</span></span>
<span data-ttu-id="6d5a0-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6d5a0-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d5a0-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6d5a0-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d5a0-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d5a0-134">CommonParameters</span></span>
<span data-ttu-id="6d5a0-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6d5a0-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d5a0-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="6d5a0-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d5a0-137">輸入</span><span class="sxs-lookup"><span data-stu-id="6d5a0-137">INPUTS</span></span>

### <span data-ttu-id="6d5a0-138">IMonitoringSolutionsIdentity （MonitoringSolutions）的</span><span class="sxs-lookup"><span data-stu-id="6d5a0-138">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span></span>

## <span data-ttu-id="6d5a0-139">輸出</span><span class="sxs-lookup"><span data-stu-id="6d5a0-139">OUTPUTS</span></span>

### <span data-ttu-id="6d5a0-140">ISolution （MonitoringSolutions）。 Api20151101Preview。</span><span class="sxs-lookup"><span data-stu-id="6d5a0-140">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.Api20151101Preview.ISolution</span></span>

## <span data-ttu-id="6d5a0-141">筆記</span><span class="sxs-lookup"><span data-stu-id="6d5a0-141">NOTES</span></span>

<span data-ttu-id="6d5a0-142">別名</span><span class="sxs-lookup"><span data-stu-id="6d5a0-142">ALIASES</span></span>

<span data-ttu-id="6d5a0-143">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="6d5a0-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6d5a0-144">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="6d5a0-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6d5a0-145">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="6d5a0-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6d5a0-146">INPUTOBJECT <IMonitoringSolutionsIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="6d5a0-146">INPUTOBJECT <IMonitoringSolutionsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6d5a0-147">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="6d5a0-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6d5a0-148">`[ManagementAssociationName <String>]`：使用者 ManagementAssociation 名稱。</span><span class="sxs-lookup"><span data-stu-id="6d5a0-148">`[ManagementAssociationName <String>]`: User ManagementAssociation Name.</span></span>
  - <span data-ttu-id="6d5a0-149">`[ManagementConfigurationName <String>]`：使用者管理配置名稱。</span><span class="sxs-lookup"><span data-stu-id="6d5a0-149">`[ManagementConfigurationName <String>]`: User Management Configuration Name.</span></span>
  - <span data-ttu-id="6d5a0-150">`[ProviderName <String>]`：父資源的提供者名稱。</span><span class="sxs-lookup"><span data-stu-id="6d5a0-150">`[ProviderName <String>]`: Provider name for the parent resource.</span></span>
  - <span data-ttu-id="6d5a0-151">`[ResourceGroupName <String>]`：要取得之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6d5a0-151">`[ResourceGroupName <String>]`: The name of the resource group to get.</span></span> <span data-ttu-id="6d5a0-152">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="6d5a0-152">The name is case insensitive.</span></span>
  - <span data-ttu-id="6d5a0-153">`[ResourceName <String>]`：父資源名稱。</span><span class="sxs-lookup"><span data-stu-id="6d5a0-153">`[ResourceName <String>]`: Parent resource name.</span></span>
  - <span data-ttu-id="6d5a0-154">`[ResourceType <String>]`：父資源的資源類型</span><span class="sxs-lookup"><span data-stu-id="6d5a0-154">`[ResourceType <String>]`: Resource type for the parent resource</span></span>
  - <span data-ttu-id="6d5a0-155">`[SolutionName <String>]`：使用者方案名稱。</span><span class="sxs-lookup"><span data-stu-id="6d5a0-155">`[SolutionName <String>]`: User Solution Name.</span></span>
  - <span data-ttu-id="6d5a0-156">`[SubscriptionId <String>]`：取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="6d5a0-156">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="6d5a0-157">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="6d5a0-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="6d5a0-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="6d5a0-158">RELATED LINKS</span></span>

