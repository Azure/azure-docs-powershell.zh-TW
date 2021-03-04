---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/powershell/module/az.timeseriesinsights/remove-aztimeseriesinsightseventsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEventSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEventSource.md
ms.openlocfilehash: 9dcce9640500b1fa1aeebea8f5f3169e0a527b6f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912157"
---
# <span data-ttu-id="e0309-101">Remove-AzTimeSeriesInsightsEventSource</span><span class="sxs-lookup"><span data-stu-id="e0309-101">Remove-AzTimeSeriesInsightsEventSource</span></span>

## <span data-ttu-id="e0309-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e0309-102">SYNOPSIS</span></span>
<span data-ttu-id="e0309-103">刪除指定訂閱、資源群組及環境中具有指定名稱的事件來源</span><span class="sxs-lookup"><span data-stu-id="e0309-103">Deletes the event source with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="e0309-104">語法</span><span class="sxs-lookup"><span data-stu-id="e0309-104">SYNTAX</span></span>

### <span data-ttu-id="e0309-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="e0309-105">Delete (Default)</span></span>
```
Remove-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e0309-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e0309-106">DeleteViaIdentity</span></span>
```
Remove-AzTimeSeriesInsightsEventSource -InputObject <ITimeSeriesInsightsIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e0309-107">描述</span><span class="sxs-lookup"><span data-stu-id="e0309-107">DESCRIPTION</span></span>
<span data-ttu-id="e0309-108">刪除指定訂閱、資源群組及環境中具有指定名稱的事件來源</span><span class="sxs-lookup"><span data-stu-id="e0309-108">Deletes the event source with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="e0309-109">例子</span><span class="sxs-lookup"><span data-stu-id="e0309-109">EXAMPLES</span></span>

### <span data-ttu-id="e0309-110">範例 1：根據名稱移除指定的事件來源</span><span class="sxs-lookup"><span data-stu-id="e0309-110">Example 1: Remove a specified event source by name</span></span>
```powershell
PS C:\> Remove-AzTimeSeriesInsightsEventSource -EnvironmentName tsitest001 -Name iots001 -ResourceGroupName testgroup

```

<span data-ttu-id="e0309-111">這會移除特定事件來源。</span><span class="sxs-lookup"><span data-stu-id="e0309-111">This removes a specific event source.</span></span>

### <span data-ttu-id="e0309-112">範例 2：根據物件移除指定的事件來源</span><span class="sxs-lookup"><span data-stu-id="e0309-112">Example 2: Remove a specified event source by object</span></span>
```powershell
PS C:\> $es = Get-AzTimeSeriesInsightsEventSource -EnvironmentName tsitest001 -ResourceGroupName testgroup -Name iots001
PS C:\> Remove-AzTimeSeriesInsightsEventSource -InputObject $es

```

<span data-ttu-id="e0309-113">這會移除特定事件來源。</span><span class="sxs-lookup"><span data-stu-id="e0309-113">This removes a specific event source.</span></span>

## <span data-ttu-id="e0309-114">參數</span><span class="sxs-lookup"><span data-stu-id="e0309-114">PARAMETERS</span></span>

### <span data-ttu-id="e0309-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0309-115">-DefaultProfile</span></span>
<span data-ttu-id="e0309-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e0309-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0309-117">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="e0309-117">-EnvironmentName</span></span>
<span data-ttu-id="e0309-118">與指定資源群組相關聯的時間序列深入資訊環境名稱。</span><span class="sxs-lookup"><span data-stu-id="e0309-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="e0309-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e0309-119">-InputObject</span></span>
<span data-ttu-id="e0309-120">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="e0309-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e0309-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="e0309-121">-Name</span></span>
<span data-ttu-id="e0309-122">與指定環境相關聯的時間序列深入資訊事件來源名稱。</span><span class="sxs-lookup"><span data-stu-id="e0309-122">The name of the Time Series Insights event source associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: EventSourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0309-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e0309-123">-PassThru</span></span>
<span data-ttu-id="e0309-124">命令成功時，會返回 True</span><span class="sxs-lookup"><span data-stu-id="e0309-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="e0309-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0309-125">-ResourceGroupName</span></span>
<span data-ttu-id="e0309-126">Azure 資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e0309-126">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="e0309-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e0309-127">-SubscriptionId</span></span>
<span data-ttu-id="e0309-128">Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="e0309-128">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="e0309-129">-確認</span><span class="sxs-lookup"><span data-stu-id="e0309-129">-Confirm</span></span>
<span data-ttu-id="e0309-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="e0309-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0309-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0309-131">-WhatIf</span></span>
<span data-ttu-id="e0309-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e0309-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0309-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e0309-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0309-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0309-134">CommonParameters</span></span>
<span data-ttu-id="e0309-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e0309-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0309-136">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e0309-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0309-137">輸入</span><span class="sxs-lookup"><span data-stu-id="e0309-137">INPUTS</span></span>

### <span data-ttu-id="e0309-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="e0309-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="e0309-139">輸出</span><span class="sxs-lookup"><span data-stu-id="e0309-139">OUTPUTS</span></span>

### <span data-ttu-id="e0309-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e0309-140">System.Boolean</span></span>

## <span data-ttu-id="e0309-141">筆記</span><span class="sxs-lookup"><span data-stu-id="e0309-141">NOTES</span></span>

<span data-ttu-id="e0309-142">別名</span><span class="sxs-lookup"><span data-stu-id="e0309-142">ALIASES</span></span>

<span data-ttu-id="e0309-143">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="e0309-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e0309-144">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="e0309-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e0309-145">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="e0309-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e0309-146">INPUTOBJECT： <ITimeSeriesInsightsIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="e0309-146">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e0309-147">`[AccessPolicyName <String>]`：存取策略的名稱。</span><span class="sxs-lookup"><span data-stu-id="e0309-147">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="e0309-148">`[EnvironmentName <String>]`：環境名稱</span><span class="sxs-lookup"><span data-stu-id="e0309-148">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="e0309-149">`[EventSourceName <String>]`：與指定環境相關聯的時間序列深入資訊事件來源名稱。</span><span class="sxs-lookup"><span data-stu-id="e0309-149">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="e0309-150">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="e0309-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e0309-151">`[ReferenceDataSetName <String>]`：參照資料集的名稱。</span><span class="sxs-lookup"><span data-stu-id="e0309-151">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="e0309-152">`[ResourceGroupName <String>]`：Azure 資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e0309-152">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="e0309-153">`[SubscriptionId <String>]`：Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="e0309-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="e0309-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="e0309-154">RELATED LINKS</span></span>

