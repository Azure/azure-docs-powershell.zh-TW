---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/remove-aztimeseriesinsightseventsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEventSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEventSource.md
ms.openlocfilehash: 7f647da2543a4675dad53f88e2494aa7f6c39419
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93968901"
---
# <span data-ttu-id="7cb7f-101">Remove-AzTimeSeriesInsightsEventSource</span><span class="sxs-lookup"><span data-stu-id="7cb7f-101">Remove-AzTimeSeriesInsightsEventSource</span></span>

## <span data-ttu-id="7cb7f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7cb7f-102">SYNOPSIS</span></span>
<span data-ttu-id="7cb7f-103">刪除指定訂閱、資源群組和環境中具有指定名稱的事件來源</span><span class="sxs-lookup"><span data-stu-id="7cb7f-103">Deletes the event source with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="7cb7f-104">句法</span><span class="sxs-lookup"><span data-stu-id="7cb7f-104">SYNTAX</span></span>

### <span data-ttu-id="7cb7f-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="7cb7f-105">Delete (Default)</span></span>
```
Remove-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7cb7f-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7cb7f-106">DeleteViaIdentity</span></span>
```
Remove-AzTimeSeriesInsightsEventSource -InputObject <ITimeSeriesInsightsIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7cb7f-107">說明</span><span class="sxs-lookup"><span data-stu-id="7cb7f-107">DESCRIPTION</span></span>
<span data-ttu-id="7cb7f-108">刪除指定訂閱、資源群組和環境中具有指定名稱的事件來源</span><span class="sxs-lookup"><span data-stu-id="7cb7f-108">Deletes the event source with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="7cb7f-109">示例</span><span class="sxs-lookup"><span data-stu-id="7cb7f-109">EXAMPLES</span></span>

### <span data-ttu-id="7cb7f-110">範例1：依名稱移除指定的事件來源</span><span class="sxs-lookup"><span data-stu-id="7cb7f-110">Example 1: Remove a specified event source by name</span></span>
```powershell
PS C:\> Remove-AzTimeSeriesInsightsEventSource -EnvironmentName tsitest001 -Name iots001 -ResourceGroupName testgroup

```

<span data-ttu-id="7cb7f-111">這會移除特定的事件來源。</span><span class="sxs-lookup"><span data-stu-id="7cb7f-111">This removes a specific event source.</span></span>

### <span data-ttu-id="7cb7f-112">範例2：依物件移除指定的事件來源</span><span class="sxs-lookup"><span data-stu-id="7cb7f-112">Example 2: Remove a specified event source by object</span></span>
```powershell
PS C:\> $es = Get-AzTimeSeriesInsightsEventSource -EnvironmentName tsitest001 -ResourceGroupName testgroup -Name iots001
PS C:\> Remove-AzTimeSeriesInsightsEventSource -InputObject $es

```

<span data-ttu-id="7cb7f-113">這會移除特定的事件來源。</span><span class="sxs-lookup"><span data-stu-id="7cb7f-113">This removes a specific event source.</span></span>

## <span data-ttu-id="7cb7f-114">參數</span><span class="sxs-lookup"><span data-stu-id="7cb7f-114">PARAMETERS</span></span>

### <span data-ttu-id="7cb7f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cb7f-115">-DefaultProfile</span></span>
<span data-ttu-id="7cb7f-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7cb7f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7cb7f-117">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="7cb7f-117">-EnvironmentName</span></span>
<span data-ttu-id="7cb7f-118">與指定的資源群組相關聯之時間序列 Insights 環境的名稱。</span><span class="sxs-lookup"><span data-stu-id="7cb7f-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="7cb7f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7cb7f-119">-InputObject</span></span>
<span data-ttu-id="7cb7f-120">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="7cb7f-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7cb7f-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="7cb7f-121">-Name</span></span>
<span data-ttu-id="7cb7f-122">與指定環境相關聯之時間序列 Insights 事件來源的名稱。</span><span class="sxs-lookup"><span data-stu-id="7cb7f-122">The name of the Time Series Insights event source associated with the specified environment.</span></span>

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

### <span data-ttu-id="7cb7f-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7cb7f-123">-PassThru</span></span>
<span data-ttu-id="7cb7f-124">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="7cb7f-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="7cb7f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cb7f-125">-ResourceGroupName</span></span>
<span data-ttu-id="7cb7f-126">Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7cb7f-126">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="7cb7f-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7cb7f-127">-SubscriptionId</span></span>
<span data-ttu-id="7cb7f-128">Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="7cb7f-128">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="7cb7f-129">-確認</span><span class="sxs-lookup"><span data-stu-id="7cb7f-129">-Confirm</span></span>
<span data-ttu-id="7cb7f-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7cb7f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7cb7f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cb7f-131">-WhatIf</span></span>
<span data-ttu-id="7cb7f-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7cb7f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7cb7f-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7cb7f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7cb7f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cb7f-134">CommonParameters</span></span>
<span data-ttu-id="7cb7f-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7cb7f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cb7f-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="7cb7f-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cb7f-137">輸入</span><span class="sxs-lookup"><span data-stu-id="7cb7f-137">INPUTS</span></span>

### <span data-ttu-id="7cb7f-138">ITimeSeriesInsightsIdentity （TimeSeriesInsights）的</span><span class="sxs-lookup"><span data-stu-id="7cb7f-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="7cb7f-139">輸出</span><span class="sxs-lookup"><span data-stu-id="7cb7f-139">OUTPUTS</span></span>

### <span data-ttu-id="7cb7f-140">System.object</span><span class="sxs-lookup"><span data-stu-id="7cb7f-140">System.Boolean</span></span>

## <span data-ttu-id="7cb7f-141">筆記</span><span class="sxs-lookup"><span data-stu-id="7cb7f-141">NOTES</span></span>

<span data-ttu-id="7cb7f-142">別名</span><span class="sxs-lookup"><span data-stu-id="7cb7f-142">ALIASES</span></span>

<span data-ttu-id="7cb7f-143">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="7cb7f-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7cb7f-144">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="7cb7f-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7cb7f-145">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="7cb7f-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7cb7f-146">INPUTOBJECT <ITimeSeriesInsightsIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="7cb7f-146">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7cb7f-147">`[AccessPolicyName <String>]`：存取原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="7cb7f-147">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="7cb7f-148">`[EnvironmentName <String>]`：環境的名稱</span><span class="sxs-lookup"><span data-stu-id="7cb7f-148">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="7cb7f-149">`[EventSourceName <String>]`：與指定環境相關聯之時間序列 Insights 事件來源的名稱。</span><span class="sxs-lookup"><span data-stu-id="7cb7f-149">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="7cb7f-150">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="7cb7f-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7cb7f-151">`[ReferenceDataSetName <String>]`：參照資料集的名稱。</span><span class="sxs-lookup"><span data-stu-id="7cb7f-151">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="7cb7f-152">`[ResourceGroupName <String>]`： Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7cb7f-152">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="7cb7f-153">`[SubscriptionId <String>]`： Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="7cb7f-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="7cb7f-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="7cb7f-154">RELATED LINKS</span></span>
