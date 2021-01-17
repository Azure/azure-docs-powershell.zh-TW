---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/update-aztimeseriesinsightseventsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsEventSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsEventSource.md
ms.openlocfilehash: e87487e55ce285aa5c430dabaa274ee70c34ba00
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98288015"
---
# <span data-ttu-id="568b5-101">Update-AzTimeSeriesInsightsEventSource</span><span class="sxs-lookup"><span data-stu-id="568b5-101">Update-AzTimeSeriesInsightsEventSource</span></span>

## <span data-ttu-id="568b5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="568b5-102">SYNOPSIS</span></span>
<span data-ttu-id="568b5-103">在指定的訂閱、資源群組和環境中，以指定的名稱更新事件來源。</span><span class="sxs-lookup"><span data-stu-id="568b5-103">Updates the event source with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="568b5-104">句法</span><span class="sxs-lookup"><span data-stu-id="568b5-104">SYNTAX</span></span>

### <span data-ttu-id="568b5-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="568b5-105">UpdateExpanded (Default)</span></span>
```
Update-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="568b5-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="568b5-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzTimeSeriesInsightsEventSource -InputObject <ITimeSeriesInsightsIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="568b5-107">說明</span><span class="sxs-lookup"><span data-stu-id="568b5-107">DESCRIPTION</span></span>
<span data-ttu-id="568b5-108">在指定的訂閱、資源群組和環境中，以指定的名稱更新事件來源。</span><span class="sxs-lookup"><span data-stu-id="568b5-108">Updates the event source with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="568b5-109">示例</span><span class="sxs-lookup"><span data-stu-id="568b5-109">EXAMPLES</span></span>

### <span data-ttu-id="568b5-110">範例1：依名稱更新指定的事件來源</span><span class="sxs-lookup"><span data-stu-id="568b5-110">Example 1: Update a specified event source by name</span></span>
```powershell
PS C:\> Update-AzTimeSeriesInsightsEventSource -EnvironmentName tsitest001 -Name iots001 -ResourceGroupName testgroup -Tag @{"tgk"="001"}

ConsumerGroupName     : testgroup2
EventSourceResourceId : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup2/providers/Microsoft.Devices/IotHubs/iotname001
Id                    : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/tsitest001/eventsources/iots001
IotHubName            : iotname001
KeyName               : RootManageSharedAccessKey
Kind                  : Microsoft.IoTHub
Location              : eastus
Name                  : iots001
Tag                   : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
TimestampPropertyName :
Type                  : Microsoft.TimeSeriesInsights/Environments/EventSources
```

<span data-ttu-id="568b5-111">這個命令會更新特定的事件來源。</span><span class="sxs-lookup"><span data-stu-id="568b5-111">This command updates a specific event source.</span></span>

### <span data-ttu-id="568b5-112">範例3：依物件更新指定的事件來源</span><span class="sxs-lookup"><span data-stu-id="568b5-112">Example 3: Update a specified event source by object</span></span>
```powershell
PS C:\> $es = Get-AzTimeSeriesInsightsEventSource -EnvironmentName tsitest001 -ResourceGroupName testgroup -Name iots001
PS C:\> Update-AzTimeSeriesInsightsEventSource -InputObject $es -Tag @{"tgb"="002"}

ConsumerGroupName     : testgroup2
EventSourceResourceId : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup2/providers/Microsoft.Devices/IotHubs/iotname001
Id                    : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/tsitest001/eventsources/iots001
IotHubName            : iotname001
KeyName               : RootManageSharedAccessKey
Kind                  : Microsoft.IoTHub
Location              : eastus
Name                  : iots001
Tag                   : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
TimestampPropertyName :
Type                  : Microsoft.TimeSeriesInsights/Environments/EventSources
```

<span data-ttu-id="568b5-113">這個命令會更新特定的事件來源。</span><span class="sxs-lookup"><span data-stu-id="568b5-113">This command updates a specific event source.</span></span>

## <span data-ttu-id="568b5-114">參數</span><span class="sxs-lookup"><span data-stu-id="568b5-114">PARAMETERS</span></span>

### <span data-ttu-id="568b5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="568b5-115">-DefaultProfile</span></span>
<span data-ttu-id="568b5-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="568b5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="568b5-117">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="568b5-117">-EnvironmentName</span></span>
<span data-ttu-id="568b5-118">與指定的資源群組相關聯之時間序列 Insights 環境的名稱。</span><span class="sxs-lookup"><span data-stu-id="568b5-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="568b5-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="568b5-119">-InputObject</span></span>
<span data-ttu-id="568b5-120">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="568b5-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="568b5-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="568b5-121">-Name</span></span>
<span data-ttu-id="568b5-122">與指定環境相關聯之時間序列 Insights 事件來源的名稱。</span><span class="sxs-lookup"><span data-stu-id="568b5-122">The name of the Time Series Insights event source associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: EventSourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="568b5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="568b5-123">-ResourceGroupName</span></span>
<span data-ttu-id="568b5-124">Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="568b5-124">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="568b5-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="568b5-125">-SubscriptionId</span></span>
<span data-ttu-id="568b5-126">Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="568b5-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="568b5-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="568b5-127">-Tag</span></span>
<span data-ttu-id="568b5-128">事件來源之其他屬性的鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="568b5-128">Key-value pairs of additional properties for the event source.</span></span>

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

### <span data-ttu-id="568b5-129">-確認</span><span class="sxs-lookup"><span data-stu-id="568b5-129">-Confirm</span></span>
<span data-ttu-id="568b5-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="568b5-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="568b5-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="568b5-131">-WhatIf</span></span>
<span data-ttu-id="568b5-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="568b5-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="568b5-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="568b5-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="568b5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="568b5-134">CommonParameters</span></span>
<span data-ttu-id="568b5-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="568b5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="568b5-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="568b5-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="568b5-137">輸入</span><span class="sxs-lookup"><span data-stu-id="568b5-137">INPUTS</span></span>

### <span data-ttu-id="568b5-138">ITimeSeriesInsightsIdentity （TimeSeriesInsights）的</span><span class="sxs-lookup"><span data-stu-id="568b5-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="568b5-139">輸出</span><span class="sxs-lookup"><span data-stu-id="568b5-139">OUTPUTS</span></span>

### <span data-ttu-id="568b5-140">IEventSourceResource （TimeSeriesInsights）。 Api20200515。</span><span class="sxs-lookup"><span data-stu-id="568b5-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEventSourceResource</span></span>

## <span data-ttu-id="568b5-141">筆記</span><span class="sxs-lookup"><span data-stu-id="568b5-141">NOTES</span></span>

<span data-ttu-id="568b5-142">別名</span><span class="sxs-lookup"><span data-stu-id="568b5-142">ALIASES</span></span>

<span data-ttu-id="568b5-143">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="568b5-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="568b5-144">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="568b5-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="568b5-145">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="568b5-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="568b5-146">INPUTOBJECT <ITimeSeriesInsightsIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="568b5-146">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="568b5-147">`[AccessPolicyName <String>]`：存取原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="568b5-147">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="568b5-148">`[EnvironmentName <String>]`：環境的名稱</span><span class="sxs-lookup"><span data-stu-id="568b5-148">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="568b5-149">`[EventSourceName <String>]`：與指定環境相關聯之時間序列 Insights 事件來源的名稱。</span><span class="sxs-lookup"><span data-stu-id="568b5-149">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="568b5-150">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="568b5-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="568b5-151">`[ReferenceDataSetName <String>]`：參照資料集的名稱。</span><span class="sxs-lookup"><span data-stu-id="568b5-151">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="568b5-152">`[ResourceGroupName <String>]`： Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="568b5-152">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="568b5-153">`[SubscriptionId <String>]`： Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="568b5-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="568b5-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="568b5-154">RELATED LINKS</span></span>

