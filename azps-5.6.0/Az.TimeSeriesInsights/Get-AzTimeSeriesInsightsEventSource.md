---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/powershell/module/az.timeseriesinsights/get-aztimeseriesinsightseventsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsEventSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsEventSource.md
ms.openlocfilehash: c28d33e4da860a68227228564c55a151a3068329
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908326"
---
# <span data-ttu-id="db12d-101">Get-AzTimeSeriesInsightsEventSource</span><span class="sxs-lookup"><span data-stu-id="db12d-101">Get-AzTimeSeriesInsightsEventSource</span></span>

## <span data-ttu-id="db12d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="db12d-102">SYNOPSIS</span></span>
<span data-ttu-id="db12d-103">在指定的環境中，使用指定名稱獲得事件來源。</span><span class="sxs-lookup"><span data-stu-id="db12d-103">Gets the event source with the specified name in the specified environment.</span></span>

## <span data-ttu-id="db12d-104">語法</span><span class="sxs-lookup"><span data-stu-id="db12d-104">SYNTAX</span></span>

### <span data-ttu-id="db12d-105">清單 (預設) </span><span class="sxs-lookup"><span data-stu-id="db12d-105">List (Default)</span></span>
```
Get-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="db12d-106">獲取</span><span class="sxs-lookup"><span data-stu-id="db12d-106">Get</span></span>
```
Get-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="db12d-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="db12d-107">GetViaIdentity</span></span>
```
Get-AzTimeSeriesInsightsEventSource -InputObject <ITimeSeriesInsightsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="db12d-108">描述</span><span class="sxs-lookup"><span data-stu-id="db12d-108">DESCRIPTION</span></span>
<span data-ttu-id="db12d-109">在指定的環境中，使用指定名稱獲得事件來源。</span><span class="sxs-lookup"><span data-stu-id="db12d-109">Gets the event source with the specified name in the specified environment.</span></span>

## <span data-ttu-id="db12d-110">例子</span><span class="sxs-lookup"><span data-stu-id="db12d-110">EXAMPLES</span></span>

### <span data-ttu-id="db12d-111">範例 1：列出指定環境中的所有事件來源</span><span class="sxs-lookup"><span data-stu-id="db12d-111">Example 1: List all event sources under the specified environment</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsEventSource -ResourceGroupName testgroup -EnvironmentName tsitest001

ConsumerGroupName     : testgroup2
EventHubName          : hubname001
EventSourceResourceId : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup2/providers/Microsoft.EventHub/namespaces/spacename001/eventhubs/hu 
                        bname001
Id                    : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/tsitest001/eve 
                        ntsources/estest001
KeyName               : RootManageSharedAccessKey
Kind                  : Microsoft.EventHub
Location              : eastus
Name                  : estest001
ServiceBusNamespace   : spacename001
Tag                   : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
TimestampPropertyName :
Type                  : Microsoft.TimeSeriesInsights/Environments/EventSources

ConsumerGroupName     : testgroup2
EventSourceResourceId : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup2/providers/Microsoft.Devices/IotHubs/iotname001
Id                    : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/tsitest001/eve 
                        ntsources/iots001
IotHubName            : iotname001
KeyName               : RootManageSharedAccessKey
Kind                  : Microsoft.IoTHub
Location              : eastus
Name                  : iots001
Tag                   : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
TimestampPropertyName :
Type                  : Microsoft.TimeSeriesInsights/Environments/EventSources
```

<span data-ttu-id="db12d-112">此命令會列出指定環境下的所有事件來源。</span><span class="sxs-lookup"><span data-stu-id="db12d-112">This command lists all event sources under the specified environments.</span></span>

### <span data-ttu-id="db12d-113">範例 2：根據名稱取得指定的事件來源</span><span class="sxs-lookup"><span data-stu-id="db12d-113">Example 2: Get a specified event source by name</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsEventSource -ResourceGroupName testgroup -EnvironmentName tsitest001 -Name iots001

ConsumerGroupName     : testgroup2
EventSourceResourceId : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup2/providers/Microsoft.Devices/IotHubs/iotname001
Id                    : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/tsitest001/eve
                        ntsources/iots001
IotHubName            : iotname001
KeyName               : RootManageSharedAccessKey
Kind                  : Microsoft.IoTHub
Location              : eastus
Name                  : iots001
Tag                   : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
TimestampPropertyName :
Type                  : Microsoft.TimeSeriesInsights/Environments/EventSources
```

<span data-ttu-id="db12d-114">此命令會獲得特定的事件來源。</span><span class="sxs-lookup"><span data-stu-id="db12d-114">This command gets a specific event source.</span></span>

### <span data-ttu-id="db12d-115">範例 3：根據物件取得指定的事件來源</span><span class="sxs-lookup"><span data-stu-id="db12d-115">Example 3: Get a specified event source by object</span></span>
```powershell
PS C:\> $es = Get-AzTimeSeriesInsightsEventSource -ResourceGroupName tsi-test-i01k5l -EnvironmentName tsi-envv8u56x -Name tsi-esrfyi9h
PS C:\> Get-AzTimeSeriesInsightsEventSource -InputObject $es

ConsumerGroupName     : tsi-test-i01k5l
EventHubName          : eventhubname-d2rvmp
EventSourceResourceId : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/tsi-test-i01k5l/providers/Microsoft.EventHub/namespaces/eventhubspace-0t3khp/eventhubs/eventhubname-d2rvmp
Id                    : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/tsi-test-i01k5l/providers/Microsoft.TimeSeriesInsights/environments/tsi-envv8u56x/eventsources/tsi-esrfyi9h
KeyName               : RootManageSharedAccessKey
Kind                  : Microsoft.EventHub
Location              : eastus2
Name                  : tsi-esrfyi9h
ServiceBusNamespace   : eventhubspace-0t3khp
Tag                   : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
TimestampPropertyName :
Type                  : Microsoft.TimeSeriesInsights/Environments/EventSources
```

<span data-ttu-id="db12d-116">此命令會獲得特定的事件來源。</span><span class="sxs-lookup"><span data-stu-id="db12d-116">This command gets a specific event source.</span></span>

## <span data-ttu-id="db12d-117">參數</span><span class="sxs-lookup"><span data-stu-id="db12d-117">PARAMETERS</span></span>

### <span data-ttu-id="db12d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db12d-118">-DefaultProfile</span></span>
<span data-ttu-id="db12d-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="db12d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db12d-120">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="db12d-120">-EnvironmentName</span></span>
<span data-ttu-id="db12d-121">與指定資源群組相關聯的時間序列深入資訊環境名稱。</span><span class="sxs-lookup"><span data-stu-id="db12d-121">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db12d-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="db12d-122">-InputObject</span></span>
<span data-ttu-id="db12d-123">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="db12d-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="db12d-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="db12d-124">-Name</span></span>
<span data-ttu-id="db12d-125">與指定環境相關聯的時間序列深入資訊事件來源名稱。</span><span class="sxs-lookup"><span data-stu-id="db12d-125">The name of the Time Series Insights event source associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: EventSourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db12d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db12d-126">-ResourceGroupName</span></span>
<span data-ttu-id="db12d-127">Azure 資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="db12d-127">Name of an Azure Resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db12d-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="db12d-128">-SubscriptionId</span></span>
<span data-ttu-id="db12d-129">Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="db12d-129">Azure Subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db12d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db12d-130">CommonParameters</span></span>
<span data-ttu-id="db12d-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="db12d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db12d-132">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="db12d-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db12d-133">輸入</span><span class="sxs-lookup"><span data-stu-id="db12d-133">INPUTS</span></span>

### <span data-ttu-id="db12d-134">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="db12d-134">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="db12d-135">輸出</span><span class="sxs-lookup"><span data-stu-id="db12d-135">OUTPUTS</span></span>

### <span data-ttu-id="db12d-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEventSourceResource</span><span class="sxs-lookup"><span data-stu-id="db12d-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEventSourceResource</span></span>

## <span data-ttu-id="db12d-137">筆記</span><span class="sxs-lookup"><span data-stu-id="db12d-137">NOTES</span></span>

<span data-ttu-id="db12d-138">別名</span><span class="sxs-lookup"><span data-stu-id="db12d-138">ALIASES</span></span>

<span data-ttu-id="db12d-139">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="db12d-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="db12d-140">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="db12d-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="db12d-141">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="db12d-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="db12d-142">INPUTOBJECT： <ITimeSeriesInsightsIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="db12d-142">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="db12d-143">`[AccessPolicyName <String>]`：存取策略的名稱。</span><span class="sxs-lookup"><span data-stu-id="db12d-143">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="db12d-144">`[EnvironmentName <String>]`：環境名稱</span><span class="sxs-lookup"><span data-stu-id="db12d-144">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="db12d-145">`[EventSourceName <String>]`：與指定環境相關聯的時間序列深入資訊事件來源名稱。</span><span class="sxs-lookup"><span data-stu-id="db12d-145">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="db12d-146">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="db12d-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="db12d-147">`[ReferenceDataSetName <String>]`：參照資料集的名稱。</span><span class="sxs-lookup"><span data-stu-id="db12d-147">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="db12d-148">`[ResourceGroupName <String>]`：Azure 資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="db12d-148">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="db12d-149">`[SubscriptionId <String>]`：Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="db12d-149">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="db12d-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="db12d-150">RELATED LINKS</span></span>

