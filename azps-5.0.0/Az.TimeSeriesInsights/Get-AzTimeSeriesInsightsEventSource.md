---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/get-aztimeseriesinsightseventsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsEventSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsEventSource.md
ms.openlocfilehash: 5590a89b22c0adc3dfb2df88e6b977dec268a822
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139352"
---
# <span data-ttu-id="04e71-101">Get-AzTimeSeriesInsightsEventSource</span><span class="sxs-lookup"><span data-stu-id="04e71-101">Get-AzTimeSeriesInsightsEventSource</span></span>

## <span data-ttu-id="04e71-102">摘要</span><span class="sxs-lookup"><span data-stu-id="04e71-102">SYNOPSIS</span></span>
<span data-ttu-id="04e71-103">在指定的環境中，以指定的名稱取得事件來源。</span><span class="sxs-lookup"><span data-stu-id="04e71-103">Gets the event source with the specified name in the specified environment.</span></span>

## <span data-ttu-id="04e71-104">句法</span><span class="sxs-lookup"><span data-stu-id="04e71-104">SYNTAX</span></span>

### <span data-ttu-id="04e71-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="04e71-105">List (Default)</span></span>
```
Get-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="04e71-106">獲取</span><span class="sxs-lookup"><span data-stu-id="04e71-106">Get</span></span>
```
Get-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="04e71-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="04e71-107">GetViaIdentity</span></span>
```
Get-AzTimeSeriesInsightsEventSource -InputObject <ITimeSeriesInsightsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="04e71-108">說明</span><span class="sxs-lookup"><span data-stu-id="04e71-108">DESCRIPTION</span></span>
<span data-ttu-id="04e71-109">在指定的環境中，以指定的名稱取得事件來源。</span><span class="sxs-lookup"><span data-stu-id="04e71-109">Gets the event source with the specified name in the specified environment.</span></span>

## <span data-ttu-id="04e71-110">示例</span><span class="sxs-lookup"><span data-stu-id="04e71-110">EXAMPLES</span></span>

### <span data-ttu-id="04e71-111">範例1：列出指定環境下的所有事件來源</span><span class="sxs-lookup"><span data-stu-id="04e71-111">Example 1: List all event sources under the specified environment</span></span>
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

<span data-ttu-id="04e71-112">這個命令會列出指定環境下的所有事件來源。</span><span class="sxs-lookup"><span data-stu-id="04e71-112">This command lists all event sources under the specified environments.</span></span>

### <span data-ttu-id="04e71-113">範例2：依名稱取得指定的事件來源</span><span class="sxs-lookup"><span data-stu-id="04e71-113">Example 2: Get a specified event source by name</span></span>
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

<span data-ttu-id="04e71-114">這個命令會取得特定的事件來源。</span><span class="sxs-lookup"><span data-stu-id="04e71-114">This command gets a specific event source.</span></span>

### <span data-ttu-id="04e71-115">範例3：透過物件取得指定的事件來源</span><span class="sxs-lookup"><span data-stu-id="04e71-115">Example 3: Get a specified event source by object</span></span>
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

<span data-ttu-id="04e71-116">這個命令會取得特定的事件來源。</span><span class="sxs-lookup"><span data-stu-id="04e71-116">This command gets a specific event source.</span></span>

## <span data-ttu-id="04e71-117">參數</span><span class="sxs-lookup"><span data-stu-id="04e71-117">PARAMETERS</span></span>

### <span data-ttu-id="04e71-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04e71-118">-DefaultProfile</span></span>
<span data-ttu-id="04e71-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="04e71-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04e71-120">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="04e71-120">-EnvironmentName</span></span>
<span data-ttu-id="04e71-121">與指定的資源群組相關聯之時間序列 Insights 環境的名稱。</span><span class="sxs-lookup"><span data-stu-id="04e71-121">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="04e71-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="04e71-122">-InputObject</span></span>
<span data-ttu-id="04e71-123">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="04e71-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="04e71-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="04e71-124">-Name</span></span>
<span data-ttu-id="04e71-125">與指定環境相關聯之時間序列 Insights 事件來源的名稱。</span><span class="sxs-lookup"><span data-stu-id="04e71-125">The name of the Time Series Insights event source associated with the specified environment.</span></span>

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

### <span data-ttu-id="04e71-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04e71-126">-ResourceGroupName</span></span>
<span data-ttu-id="04e71-127">Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="04e71-127">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="04e71-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="04e71-128">-SubscriptionId</span></span>
<span data-ttu-id="04e71-129">Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="04e71-129">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="04e71-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04e71-130">CommonParameters</span></span>
<span data-ttu-id="04e71-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="04e71-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04e71-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="04e71-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04e71-133">輸入</span><span class="sxs-lookup"><span data-stu-id="04e71-133">INPUTS</span></span>

### <span data-ttu-id="04e71-134">ITimeSeriesInsightsIdentity （TimeSeriesInsights）的</span><span class="sxs-lookup"><span data-stu-id="04e71-134">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="04e71-135">輸出</span><span class="sxs-lookup"><span data-stu-id="04e71-135">OUTPUTS</span></span>

### <span data-ttu-id="04e71-136">IEventSourceResource （TimeSeriesInsights）。 Api20200515。</span><span class="sxs-lookup"><span data-stu-id="04e71-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEventSourceResource</span></span>

## <span data-ttu-id="04e71-137">筆記</span><span class="sxs-lookup"><span data-stu-id="04e71-137">NOTES</span></span>

<span data-ttu-id="04e71-138">別名</span><span class="sxs-lookup"><span data-stu-id="04e71-138">ALIASES</span></span>

<span data-ttu-id="04e71-139">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="04e71-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="04e71-140">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="04e71-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="04e71-141">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="04e71-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="04e71-142">INPUTOBJECT <ITimeSeriesInsightsIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="04e71-142">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="04e71-143">`[AccessPolicyName <String>]`：存取原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="04e71-143">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="04e71-144">`[EnvironmentName <String>]`：環境的名稱</span><span class="sxs-lookup"><span data-stu-id="04e71-144">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="04e71-145">`[EventSourceName <String>]`：與指定環境相關聯之時間序列 Insights 事件來源的名稱。</span><span class="sxs-lookup"><span data-stu-id="04e71-145">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="04e71-146">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="04e71-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="04e71-147">`[ReferenceDataSetName <String>]`：參照資料集的名稱。</span><span class="sxs-lookup"><span data-stu-id="04e71-147">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="04e71-148">`[ResourceGroupName <String>]`： Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="04e71-148">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="04e71-149">`[SubscriptionId <String>]`： Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="04e71-149">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="04e71-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="04e71-150">RELATED LINKS</span></span>

