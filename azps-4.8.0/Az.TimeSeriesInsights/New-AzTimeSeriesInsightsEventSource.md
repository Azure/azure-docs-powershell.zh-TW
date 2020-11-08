---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/new-aztimeseriesinsightseventsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsEventSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsEventSource.md
ms.openlocfilehash: 1c5e14fa71ded51d91792f462d01cb463ff36c61
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128415"
---
# <span data-ttu-id="88583-101">New-AzTimeSeriesInsightsEventSource</span><span class="sxs-lookup"><span data-stu-id="88583-101">New-AzTimeSeriesInsightsEventSource</span></span>

## <span data-ttu-id="88583-102">摘要</span><span class="sxs-lookup"><span data-stu-id="88583-102">SYNOPSIS</span></span>
<span data-ttu-id="88583-103">在指定的環境下建立事件來源。</span><span class="sxs-lookup"><span data-stu-id="88583-103">Create an event source under the specified environment.</span></span>

## <span data-ttu-id="88583-104">句法</span><span class="sxs-lookup"><span data-stu-id="88583-104">SYNTAX</span></span>

### <span data-ttu-id="88583-105">eventhub (預設) </span><span class="sxs-lookup"><span data-stu-id="88583-105">eventhub (Default)</span></span>
```
New-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 -ConsumerGroupName <String> -EventHubName <String> -EventSourceResourceId <String> -KeyName <String>
 -Kind <Kind> -Location <String> -ServiceBusNameSpace <String> -SharedAccessKey <SecureString>
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-TimeStampPropertyName <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="88583-106">iothub</span><span class="sxs-lookup"><span data-stu-id="88583-106">iothub</span></span>
```
New-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 -ConsumerGroupName <String> -EventSourceResourceId <String> -IoTHubName <String> -KeyName <String>
 -Kind <Kind> -Location <String> -SharedAccessKey <SecureString> [-SubscriptionId <String>] [-Tag <Hashtable>]
 [-TimeStampPropertyName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="88583-107">說明</span><span class="sxs-lookup"><span data-stu-id="88583-107">DESCRIPTION</span></span>
<span data-ttu-id="88583-108">在指定的環境下建立事件來源。</span><span class="sxs-lookup"><span data-stu-id="88583-108">Create an event source under the specified environment.</span></span>

## <span data-ttu-id="88583-109">示例</span><span class="sxs-lookup"><span data-stu-id="88583-109">EXAMPLES</span></span>

### <span data-ttu-id="88583-110">範例1：在指定的環境下建立 eventhub 事件來源</span><span class="sxs-lookup"><span data-stu-id="88583-110">Example 1: Create an eventhub event source under the specified environment</span></span>
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

<span data-ttu-id="88583-111">這個命令會在指定的環境下建立 eventhub 事件來源。</span><span class="sxs-lookup"><span data-stu-id="88583-111">This command creates an eventhub event source under the specified environment.</span></span>

### <span data-ttu-id="88583-112">範例2：在指定的環境下建立 iothub 事件來源</span><span class="sxs-lookup"><span data-stu-id="88583-112">Example 2: Create an iothub event source under the specified environment</span></span>
```powershell
PS C:\> $ev = New-AzIotHub -ResourceGroupName testgroup -Location eastus -Name iotname001 -SkuName S1 -Units 100
PS C:\> $ks = Get-AzIotHubKey -ResourceGroupName testgroup -Name iotname001
PS C:\> $k  = $ks[0].PrimaryKey | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzTimeSeriesInsightsEventSource -ResourceGroupName testgroup -Name iots001 -EnvironmentName tsitest001 -Kind Microsoft.IoTHub -ConsumerGroupName testgroup -Location eastus -KeyName RootManageSharedAccessKey -IoTHubName iotname001 -EventSourceResourceId $ev.id -SharedAccessKey $k

Location Name    Type                                                   Kind
-------- ----    ----                                                   ----
eastus   iots001 Microsoft.TimeSeriesInsights/Environments/EventSources Microsoft.IoTHub
```

<span data-ttu-id="88583-113">這個命令會在指定的環境下建立 iothub 事件來源。</span><span class="sxs-lookup"><span data-stu-id="88583-113">This command creates an iothub event source under the specified environment.</span></span>

## <span data-ttu-id="88583-114">參數</span><span class="sxs-lookup"><span data-stu-id="88583-114">PARAMETERS</span></span>

### <span data-ttu-id="88583-115">-ConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="88583-115">-ConsumerGroupName</span></span>
<span data-ttu-id="88583-116">包含要讀取事件之分區的事件/iot 中樞的消費者群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="88583-116">The name of the event/iot hub's consumer group that holds the partitions from which events will be read.</span></span>

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

### <span data-ttu-id="88583-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88583-117">-DefaultProfile</span></span>
<span data-ttu-id="88583-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="88583-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88583-119">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="88583-119">-EnvironmentName</span></span>
<span data-ttu-id="88583-120">與指定的資源群組相關聯之時間序列 Insights 環境的名稱。</span><span class="sxs-lookup"><span data-stu-id="88583-120">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="88583-121">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="88583-121">-EventHubName</span></span>
<span data-ttu-id="88583-122">事件中心的名稱。</span><span class="sxs-lookup"><span data-stu-id="88583-122">The name of the event hub.</span></span>

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

### <span data-ttu-id="88583-123">-EventSourceResourceId</span><span class="sxs-lookup"><span data-stu-id="88583-123">-EventSourceResourceId</span></span>
<span data-ttu-id="88583-124">Azure 資源管理器中事件來源的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="88583-124">The resource id of the event source in Azure Resource Manager.</span></span>

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

### <span data-ttu-id="88583-125">-IoTHubName</span><span class="sxs-lookup"><span data-stu-id="88583-125">-IoTHubName</span></span>
<span data-ttu-id="88583-126">Iot 中樞的名稱。</span><span class="sxs-lookup"><span data-stu-id="88583-126">The name of the iot hub.</span></span>

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

### <span data-ttu-id="88583-127">-KeyName</span><span class="sxs-lookup"><span data-stu-id="88583-127">-KeyName</span></span>
<span data-ttu-id="88583-128">可授與事件/iot 中心存取時間數列 Insights 服務存取權的 SAS 金鑰名稱。</span><span class="sxs-lookup"><span data-stu-id="88583-128">The name of the SAS key that grants the Time Series Insights service access to the event/iot hub.</span></span>

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

### <span data-ttu-id="88583-129">類型</span><span class="sxs-lookup"><span data-stu-id="88583-129">-Kind</span></span>
<span data-ttu-id="88583-130">事件來源的類型。</span><span class="sxs-lookup"><span data-stu-id="88583-130">The kind of the event source.</span></span>

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

### <span data-ttu-id="88583-131">-位置</span><span class="sxs-lookup"><span data-stu-id="88583-131">-Location</span></span>
<span data-ttu-id="88583-132">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="88583-132">The location of the resource.</span></span>

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

### <span data-ttu-id="88583-133">-名稱</span><span class="sxs-lookup"><span data-stu-id="88583-133">-Name</span></span>
<span data-ttu-id="88583-134">事件來源的名稱。</span><span class="sxs-lookup"><span data-stu-id="88583-134">Name of the event source.</span></span>

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

### <span data-ttu-id="88583-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88583-135">-ResourceGroupName</span></span>
<span data-ttu-id="88583-136">Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="88583-136">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="88583-137">-ServiceBusNameSpace</span><span class="sxs-lookup"><span data-stu-id="88583-137">-ServiceBusNameSpace</span></span>
<span data-ttu-id="88583-138">包含事件中樞之服務匯流排的名稱。</span><span class="sxs-lookup"><span data-stu-id="88583-138">The name of the service bus that contains the event hub.</span></span>

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

### <span data-ttu-id="88583-139">-SharedAccessKey</span><span class="sxs-lookup"><span data-stu-id="88583-139">-SharedAccessKey</span></span>
<span data-ttu-id="88583-140">此共用訪問金鑰的值，可授與事件/iot 中心的讀取存取權。</span><span class="sxs-lookup"><span data-stu-id="88583-140">The value of the shared access key that grants the Time Series Insights service read access to the event/iot hub.</span></span>

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

### <span data-ttu-id="88583-141">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="88583-141">-SubscriptionId</span></span>
<span data-ttu-id="88583-142">Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="88583-142">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="88583-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="88583-143">-Tag</span></span>
<span data-ttu-id="88583-144">資源之其他屬性的鍵值對。</span><span class="sxs-lookup"><span data-stu-id="88583-144">Key-value pairs of additional properties for the resource.</span></span>

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

### <span data-ttu-id="88583-145">-TimeStampPropertyName</span><span class="sxs-lookup"><span data-stu-id="88583-145">-TimeStampPropertyName</span></span>
<span data-ttu-id="88583-146">將用來做為事件來源的時間戳記的事件屬性。</span><span class="sxs-lookup"><span data-stu-id="88583-146">The event property that will be used as the event source's timestamp.</span></span>

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

### <span data-ttu-id="88583-147">-確認</span><span class="sxs-lookup"><span data-stu-id="88583-147">-Confirm</span></span>
<span data-ttu-id="88583-148">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="88583-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88583-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88583-149">-WhatIf</span></span>
<span data-ttu-id="88583-150">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="88583-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88583-151">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="88583-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88583-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88583-152">CommonParameters</span></span>
<span data-ttu-id="88583-153">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="88583-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88583-154">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="88583-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88583-155">輸入</span><span class="sxs-lookup"><span data-stu-id="88583-155">INPUTS</span></span>

## <span data-ttu-id="88583-156">輸出</span><span class="sxs-lookup"><span data-stu-id="88583-156">OUTPUTS</span></span>

### <span data-ttu-id="88583-157">IEventSourceResource （TimeSeriesInsights）。 Api20200515。</span><span class="sxs-lookup"><span data-stu-id="88583-157">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEventSourceResource</span></span>

## <span data-ttu-id="88583-158">筆記</span><span class="sxs-lookup"><span data-stu-id="88583-158">NOTES</span></span>

<span data-ttu-id="88583-159">別名</span><span class="sxs-lookup"><span data-stu-id="88583-159">ALIASES</span></span>

## <span data-ttu-id="88583-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="88583-160">RELATED LINKS</span></span>

