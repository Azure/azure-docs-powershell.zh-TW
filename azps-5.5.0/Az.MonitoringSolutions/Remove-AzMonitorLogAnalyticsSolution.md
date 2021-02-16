---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitoringsolutions/remove-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Remove-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Remove-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: 3766211a5ac69c416e2b36dd272dfd140193e848
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100132683"
---
# <span data-ttu-id="d19a4-101">Remove-AzMonitorLogAnalyticsSolution</span><span class="sxs-lookup"><span data-stu-id="d19a4-101">Remove-AzMonitorLogAnalyticsSolution</span></span>

## <span data-ttu-id="d19a4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d19a4-102">SYNOPSIS</span></span>
<span data-ttu-id="d19a4-103">刪除訂閱中的方案。</span><span class="sxs-lookup"><span data-stu-id="d19a4-103">Deletes the solution in the subscription.</span></span>

## <span data-ttu-id="d19a4-104">句法</span><span class="sxs-lookup"><span data-stu-id="d19a4-104">SYNTAX</span></span>

### <span data-ttu-id="d19a4-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="d19a4-105">Delete (Default)</span></span>
```
Remove-AzMonitorLogAnalyticsSolution -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d19a4-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d19a4-106">DeleteViaIdentity</span></span>
```
Remove-AzMonitorLogAnalyticsSolution -InputObject <IMonitoringSolutionsIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d19a4-107">說明</span><span class="sxs-lookup"><span data-stu-id="d19a4-107">DESCRIPTION</span></span>
<span data-ttu-id="d19a4-108">刪除訂閱中的方案。</span><span class="sxs-lookup"><span data-stu-id="d19a4-108">Deletes the solution in the subscription.</span></span>

## <span data-ttu-id="d19a4-109">示例</span><span class="sxs-lookup"><span data-stu-id="d19a4-109">EXAMPLES</span></span>

### <span data-ttu-id="d19a4-110">範例1：依名稱移除監視記錄分析方案</span><span class="sxs-lookup"><span data-stu-id="d19a4-110">Example 1: Remove a monitor log analytics solution by name</span></span>
```powershell
PS C:\> Remove-AzMonitorLogAnalyticsSolution  -ResourceGroupName azureps-manual-test -Name 'Containers(monitoringworkspace-2vob7n)'

```

<span data-ttu-id="d19a4-111">這個命令會依名稱移除監視記錄分析方案。</span><span class="sxs-lookup"><span data-stu-id="d19a4-111">This command removes a monitor log analytics solution by name.</span></span>

### <span data-ttu-id="d19a4-112">範例2：依物件移除監視記錄分析解決方案</span><span class="sxs-lookup"><span data-stu-id="d19a4-112">Example 2: Remove a monitor log analytics solution by object</span></span>
```powershell
PS C:\> $monitor = Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-manual-test -Name 'Containers(monitoringworkspace-pevful)'
PS C:\> Remove-AzMonitorLogAnalyticsSolution -InputObject $monitor

```

<span data-ttu-id="d19a4-113">這個命令會依物件移除監視記錄分析方案。</span><span class="sxs-lookup"><span data-stu-id="d19a4-113">This command removes a monitor log analytics solution by object.</span></span>

### <span data-ttu-id="d19a4-114">範例3：依管道移除顯示器記錄分析解決方案</span><span class="sxs-lookup"><span data-stu-id="d19a4-114">Example 3: Remove a monitor log analytics solution by pipeline</span></span>
```powershell
PS C:\> $monitor = Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-manual-test -Name 'Containers(monitoringworkspace-asdehu)' | Remove-AzMonitorLogAnalyticsSolution

```

<span data-ttu-id="d19a4-115">這個命令會依管道移除監視記錄分析方案。</span><span class="sxs-lookup"><span data-stu-id="d19a4-115">This command removes a monitor log analytics solution by pipeline.</span></span>

## <span data-ttu-id="d19a4-116">參數</span><span class="sxs-lookup"><span data-stu-id="d19a4-116">PARAMETERS</span></span>

### <span data-ttu-id="d19a4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d19a4-117">-DefaultProfile</span></span>
<span data-ttu-id="d19a4-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d19a4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d19a4-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d19a4-119">-InputObject</span></span>
<span data-ttu-id="d19a4-120">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="d19a4-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d19a4-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="d19a4-121">-Name</span></span>
<span data-ttu-id="d19a4-122">使用者方案名稱。</span><span class="sxs-lookup"><span data-stu-id="d19a4-122">User Solution Name.</span></span>

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

### <span data-ttu-id="d19a4-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d19a4-123">-PassThru</span></span>
<span data-ttu-id="d19a4-124">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="d19a4-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="d19a4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d19a4-125">-ResourceGroupName</span></span>
<span data-ttu-id="d19a4-126">要取得之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d19a4-126">The name of the resource group to get.</span></span>
<span data-ttu-id="d19a4-127">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="d19a4-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="d19a4-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d19a4-128">-SubscriptionId</span></span>
<span data-ttu-id="d19a4-129">取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="d19a4-129">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d19a4-130">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="d19a4-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d19a4-131">-確認</span><span class="sxs-lookup"><span data-stu-id="d19a4-131">-Confirm</span></span>
<span data-ttu-id="d19a4-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d19a4-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d19a4-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d19a4-133">-WhatIf</span></span>
<span data-ttu-id="d19a4-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d19a4-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d19a4-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d19a4-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d19a4-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d19a4-136">CommonParameters</span></span>
<span data-ttu-id="d19a4-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d19a4-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d19a4-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d19a4-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d19a4-139">輸入</span><span class="sxs-lookup"><span data-stu-id="d19a4-139">INPUTS</span></span>

### <span data-ttu-id="d19a4-140">IMonitoringSolutionsIdentity （MonitoringSolutions）的</span><span class="sxs-lookup"><span data-stu-id="d19a4-140">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span></span>

## <span data-ttu-id="d19a4-141">輸出</span><span class="sxs-lookup"><span data-stu-id="d19a4-141">OUTPUTS</span></span>

### <span data-ttu-id="d19a4-142">System.object</span><span class="sxs-lookup"><span data-stu-id="d19a4-142">System.Boolean</span></span>

## <span data-ttu-id="d19a4-143">筆記</span><span class="sxs-lookup"><span data-stu-id="d19a4-143">NOTES</span></span>

<span data-ttu-id="d19a4-144">別名</span><span class="sxs-lookup"><span data-stu-id="d19a4-144">ALIASES</span></span>

<span data-ttu-id="d19a4-145">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="d19a4-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d19a4-146">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="d19a4-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d19a4-147">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="d19a4-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d19a4-148">INPUTOBJECT <IMonitoringSolutionsIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="d19a4-148">INPUTOBJECT <IMonitoringSolutionsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d19a4-149">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="d19a4-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d19a4-150">`[ManagementAssociationName <String>]`：使用者 ManagementAssociation 名稱。</span><span class="sxs-lookup"><span data-stu-id="d19a4-150">`[ManagementAssociationName <String>]`: User ManagementAssociation Name.</span></span>
  - <span data-ttu-id="d19a4-151">`[ManagementConfigurationName <String>]`：使用者管理配置名稱。</span><span class="sxs-lookup"><span data-stu-id="d19a4-151">`[ManagementConfigurationName <String>]`: User Management Configuration Name.</span></span>
  - <span data-ttu-id="d19a4-152">`[ProviderName <String>]`：父資源的提供者名稱。</span><span class="sxs-lookup"><span data-stu-id="d19a4-152">`[ProviderName <String>]`: Provider name for the parent resource.</span></span>
  - <span data-ttu-id="d19a4-153">`[ResourceGroupName <String>]`：要取得之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d19a4-153">`[ResourceGroupName <String>]`: The name of the resource group to get.</span></span> <span data-ttu-id="d19a4-154">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="d19a4-154">The name is case insensitive.</span></span>
  - <span data-ttu-id="d19a4-155">`[ResourceName <String>]`：父資源名稱。</span><span class="sxs-lookup"><span data-stu-id="d19a4-155">`[ResourceName <String>]`: Parent resource name.</span></span>
  - <span data-ttu-id="d19a4-156">`[ResourceType <String>]`：父資源的資源類型</span><span class="sxs-lookup"><span data-stu-id="d19a4-156">`[ResourceType <String>]`: Resource type for the parent resource</span></span>
  - <span data-ttu-id="d19a4-157">`[SolutionName <String>]`：使用者方案名稱。</span><span class="sxs-lookup"><span data-stu-id="d19a4-157">`[SolutionName <String>]`: User Solution Name.</span></span>
  - <span data-ttu-id="d19a4-158">`[SubscriptionId <String>]`：取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="d19a4-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="d19a4-159">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="d19a4-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="d19a4-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="d19a4-160">RELATED LINKS</span></span>

