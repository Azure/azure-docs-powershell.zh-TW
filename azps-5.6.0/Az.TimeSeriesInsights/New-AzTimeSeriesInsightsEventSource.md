---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/powershell/module/az.timeseriesinsights/new-aztimeseriesinsightseventsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsEventSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsEventSource.md
ms.openlocfilehash: fa2573a774df86ee96563e90b617db43aed0b1c3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913293"
---
# <span data-ttu-id="0f34f-101">New-AzTimeSeriesInsightsEventSource</span><span class="sxs-lookup"><span data-stu-id="0f34f-101">New-AzTimeSeriesInsightsEventSource</span></span>

## <span data-ttu-id="0f34f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0f34f-102">SYNOPSIS</span></span>
<span data-ttu-id="0f34f-103">在指定的環境中建立事件來源。</span><span class="sxs-lookup"><span data-stu-id="0f34f-103">Create an event source under the specified environment.</span></span>

## <span data-ttu-id="0f34f-104">語法</span><span class="sxs-lookup"><span data-stu-id="0f34f-104">SYNTAX</span></span>

### <span data-ttu-id="0f34f-105">eventhub (預設) </span><span class="sxs-lookup"><span data-stu-id="0f34f-105">eventhub (Default)</span></span>
```
New-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 -ConsumerGroupName <String> -EventHubName <String> -EventSourceResourceId <String> -KeyName <String>
 -Kind <Kind> -Location <String> -ServiceBusNameSpace <String> -SharedAccessKey <SecureString>
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-TimeStampPropertyName <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0f34f-106">iothub</span><span class="sxs-lookup"><span data-stu-id="0f34f-106">iothub</span></span>
```
New-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 -ConsumerGroupName <String> -EventSourceResourceId <String> -IoTHubName <String> -KeyName <String>
 -Kind <Kind> -Location <String> -SharedAccessKey <SecureString> [-SubscriptionId <String>] [-Tag <Hashtable>]
 [-TimeStampPropertyName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0f34f-107">描述</span><span class="sxs-lookup"><span data-stu-id="0f34f-107">DESCRIPTION</span></span>
<span data-ttu-id="0f34f-108">在指定的環境中建立事件來源。</span><span class="sxs-lookup"><span data-stu-id="0f34f-108">Create an event source under the specified environment.</span></span>

## <span data-ttu-id="0f34f-109">例子</span><span class="sxs-lookup"><span data-stu-id="0f34f-109">EXAMPLES</span></span>

### <span data-ttu-id="0f34f-110">範例 1：在指定的環境中建立事件hub 事件來源</span><span class="sxs-lookup"><span data-stu-id="0f34f-110">Example 1: Create an eventhub event source under the specified environment</span></span>
```powershell
PS C:\> New-AzEventHubNamespace -Name spacename002 -ResourceGroupName testgroup -Location eastus
PS C:\> $ev = New-AzEventHub -ResourceGroupName testgroup -NamespaceName spacename002 -Name hubname001 -MessageRetentionInDays 3 -PartitionCount 2
PS C:\> $ks = Get-AzEventHubKey -ResourceGroupName testgroup -NamespaceName spacename002 -AuthorizationRuleName RootManageSharedAccessKey
PS C:\> $k  = $ks.PrimaryKey | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzTimeSeriesInsightsEventSource -ResourceGroupName testgroup -Name estest001 -EnvironmentName tsitest001 -Kind Microsoft.EventHub -ConsumerGroupName testgroup -Location eastus -KeyName RootManageSharedAccessKey -ServiceBusNameSpace spacename002 -EventHubName hubname001 -EventSourceResourceId $ev.id -SharedAccessKey $k

Kind               Location Name      Type
----               -------- ----      ----
Microsoft.EventHub eastus   estest001 Microsoft.TimeSeriesInsights/Environments/EventSources
```

<span data-ttu-id="0f34f-111">此命令會建立指定環境下的 eventhub 事件來源。</span><span class="sxs-lookup"><span data-stu-id="0f34f-111">This command creates an eventhub event source under the specified environment.</span></span>

### <span data-ttu-id="0f34f-112">範例 2：在指定的環境中建立 iothub 事件來源</span><span class="sxs-lookup"><span data-stu-id="0f34f-112">Example 2: Create an iothub event source under the specified environment</span></span>
```powershell
PS C:\> $ev = New-AzIotHub -ResourceGroupName testgroup -Location eastus -Name iotname001 -SkuName S1 -Units 100
PS C:\> $ks = Get-AzIotHubKey -ResourceGroupName testgroup -Name iotname001
PS C:\> $k  = $ks[0].PrimaryKey | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzTimeSeriesInsightsEventSource -ResourceGroupName testgroup -Name iots001 -EnvironmentName tsitest001 -Kind Microsoft.IoTHub -ConsumerGroupName testgroup -Location eastus -KeyName RootManageSharedAccessKey -IoTHubName iotname001 -EventSourceResourceId $ev.id -SharedAccessKey $k

Location Name    Type                                                   Kind
-------- ----    ----                                                   ----
eastus   iots001 Microsoft.TimeSeriesInsights/Environments/EventSources Microsoft.IoTHub
```

<span data-ttu-id="0f34f-113">此命令會建立指定環境下的 iothub 事件來源。</span><span class="sxs-lookup"><span data-stu-id="0f34f-113">This command creates an iothub event source under the specified environment.</span></span>

## <span data-ttu-id="0f34f-114">參數</span><span class="sxs-lookup"><span data-stu-id="0f34f-114">PARAMETERS</span></span>

### <span data-ttu-id="0f34f-115">-ConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="0f34f-115">-ConsumerGroupName</span></span>
<span data-ttu-id="0f34f-116">事件/iot 中樞的消費者群組名稱，其包含要讀取事件的磁碟分割。</span><span class="sxs-lookup"><span data-stu-id="0f34f-116">The name of the event/iot hub's consumer group that holds the partitions from which events will be read.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f34f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f34f-117">-DefaultProfile</span></span>
<span data-ttu-id="0f34f-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="0f34f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f34f-119">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="0f34f-119">-EnvironmentName</span></span>
<span data-ttu-id="0f34f-120">與指定資源群組相關聯的時間序列深入資訊環境名稱。</span><span class="sxs-lookup"><span data-stu-id="0f34f-120">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f34f-121">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="0f34f-121">-EventHubName</span></span>
<span data-ttu-id="0f34f-122">事件中樞的名稱。</span><span class="sxs-lookup"><span data-stu-id="0f34f-122">The name of the event hub.</span></span>

```yaml
Type: System.String
Parameter Sets: eventhub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f34f-123">-EventSourceResourceId</span><span class="sxs-lookup"><span data-stu-id="0f34f-123">-EventSourceResourceId</span></span>
<span data-ttu-id="0f34f-124">Azure Resource Manager 中事件來源的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="0f34f-124">The resource id of the event source in Azure Resource Manager.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f34f-125">-IoTHubName</span><span class="sxs-lookup"><span data-stu-id="0f34f-125">-IoTHubName</span></span>
<span data-ttu-id="0f34f-126">iot 中樞的名稱。</span><span class="sxs-lookup"><span data-stu-id="0f34f-126">The name of the iot hub.</span></span>

```yaml
Type: System.String
Parameter Sets: iothub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f34f-127">-KeyName</span><span class="sxs-lookup"><span data-stu-id="0f34f-127">-KeyName</span></span>
<span data-ttu-id="0f34f-128">將時間序列深入資訊服務存取權授予事件/iot 中樞的 SAS 金鑰名稱。</span><span class="sxs-lookup"><span data-stu-id="0f34f-128">The name of the SAS key that grants the Time Series Insights service access to the event/iot hub.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f34f-129">-Kind</span><span class="sxs-lookup"><span data-stu-id="0f34f-129">-Kind</span></span>
<span data-ttu-id="0f34f-130">事件來源類型。</span><span class="sxs-lookup"><span data-stu-id="0f34f-130">The kind of the event source.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Support.Kind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f34f-131">-位置</span><span class="sxs-lookup"><span data-stu-id="0f34f-131">-Location</span></span>
<span data-ttu-id="0f34f-132">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="0f34f-132">The location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f34f-133">-名稱</span><span class="sxs-lookup"><span data-stu-id="0f34f-133">-Name</span></span>
<span data-ttu-id="0f34f-134">事件來源的名稱。</span><span class="sxs-lookup"><span data-stu-id="0f34f-134">Name of the event source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EventSourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f34f-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f34f-135">-ResourceGroupName</span></span>
<span data-ttu-id="0f34f-136">Azure 資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0f34f-136">Name of an Azure Resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f34f-137">-ServiceBusNameSpace</span><span class="sxs-lookup"><span data-stu-id="0f34f-137">-ServiceBusNameSpace</span></span>
<span data-ttu-id="0f34f-138">包含事件中樞的服務母線名稱。</span><span class="sxs-lookup"><span data-stu-id="0f34f-138">The name of the service bus that contains the event hub.</span></span>

```yaml
Type: System.String
Parameter Sets: eventhub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f34f-139">-SharedAccessKey</span><span class="sxs-lookup"><span data-stu-id="0f34f-139">-SharedAccessKey</span></span>
<span data-ttu-id="0f34f-140">共用便捷鍵的值，可授予時間序列深入資訊服務讀取事件/iot 中樞的存取權。</span><span class="sxs-lookup"><span data-stu-id="0f34f-140">The value of the shared access key that grants the Time Series Insights service read access to the event/iot hub.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f34f-141">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0f34f-141">-SubscriptionId</span></span>
<span data-ttu-id="0f34f-142">Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="0f34f-142">Azure Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f34f-143">-標記</span><span class="sxs-lookup"><span data-stu-id="0f34f-143">-Tag</span></span>
<span data-ttu-id="0f34f-144">資源的其他屬性的金鑰值組。</span><span class="sxs-lookup"><span data-stu-id="0f34f-144">Key-value pairs of additional properties for the resource.</span></span>

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

### <span data-ttu-id="0f34f-145">-TimeStampPropertyName</span><span class="sxs-lookup"><span data-stu-id="0f34f-145">-TimeStampPropertyName</span></span>
<span data-ttu-id="0f34f-146">將用來做為事件來源之時間戳記的事件屬性。</span><span class="sxs-lookup"><span data-stu-id="0f34f-146">The event property that will be used as the event source's timestamp.</span></span>

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

### <span data-ttu-id="0f34f-147">-確認</span><span class="sxs-lookup"><span data-stu-id="0f34f-147">-Confirm</span></span>
<span data-ttu-id="0f34f-148">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="0f34f-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f34f-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f34f-149">-WhatIf</span></span>
<span data-ttu-id="0f34f-150">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0f34f-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f34f-151">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0f34f-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f34f-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f34f-152">CommonParameters</span></span>
<span data-ttu-id="0f34f-153">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0f34f-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f34f-154">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0f34f-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f34f-155">輸入</span><span class="sxs-lookup"><span data-stu-id="0f34f-155">INPUTS</span></span>

## <span data-ttu-id="0f34f-156">輸出</span><span class="sxs-lookup"><span data-stu-id="0f34f-156">OUTPUTS</span></span>

### <span data-ttu-id="0f34f-157">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEventSourceResource</span><span class="sxs-lookup"><span data-stu-id="0f34f-157">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEventSourceResource</span></span>

## <span data-ttu-id="0f34f-158">筆記</span><span class="sxs-lookup"><span data-stu-id="0f34f-158">NOTES</span></span>

<span data-ttu-id="0f34f-159">別名</span><span class="sxs-lookup"><span data-stu-id="0f34f-159">ALIASES</span></span>

## <span data-ttu-id="0f34f-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="0f34f-160">RELATED LINKS</span></span>

