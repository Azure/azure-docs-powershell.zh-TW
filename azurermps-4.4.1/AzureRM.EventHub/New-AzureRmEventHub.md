---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHub.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 656e010a05ce1272355f689be8513ecadd330e7a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456671"
---
# <span data-ttu-id="a7acb-101">New-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="a7acb-101">New-AzureRmEventHub</span></span>

## <span data-ttu-id="a7acb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a7acb-102">SYNOPSIS</span></span>
<span data-ttu-id="a7acb-103">建立新的事件中樞。</span><span class="sxs-lookup"><span data-stu-id="a7acb-103">Creates a new Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a7acb-104">句法</span><span class="sxs-lookup"><span data-stu-id="a7acb-104">SYNTAX</span></span>

### <span data-ttu-id="a7acb-105">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a7acb-105">EventhubInputObjectSet</span></span>
```
New-AzureRmEventHub [-ResourceGroupName] <String> -Namespace <String> [[-Location] <String>] -Name <String>
 [-InputObject <EventHubAttributes>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="a7acb-106">EventhubPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="a7acb-106">EventhubPropertiesSet</span></span>
```
New-AzureRmEventHub [-ResourceGroupName] <String> -Namespace <String> [[-Location] <String>] -Name <String>
 [-MessageRetentionInDays <Int64>] [-PartitionCount <Int64>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="a7acb-107">說明</span><span class="sxs-lookup"><span data-stu-id="a7acb-107">DESCRIPTION</span></span>
<span data-ttu-id="a7acb-108">New-AzureRmEventHub Cmdlet 會建立新的 Azure 事件中樞。</span><span class="sxs-lookup"><span data-stu-id="a7acb-108">The New-AzureRmEventHub cmdlet creates a new Azure Event Hub.</span></span>
<span data-ttu-id="a7acb-109">若要使用 [捕獲描述] 屬性建立 Eventhub，請依照下列步驟 (範例 2) 。</span><span class="sxs-lookup"><span data-stu-id="a7acb-109">To create Eventhub with Capture description properties, please follow the below steps (Examples 2).</span></span> 


## <span data-ttu-id="a7acb-110">示例</span><span class="sxs-lookup"><span data-stu-id="a7acb-110">EXAMPLES</span></span>

### <span data-ttu-id="a7acb-111">範例1</span><span class="sxs-lookup"><span data-stu-id="a7acb-111">Example 1</span></span>
```
PS C:\> New-AzureRmEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location WestUS -EventHubName MyEventHubName -MessageRetentionInDays 3 -PartitionCount 2
```

<span data-ttu-id="a7acb-112">\` \` 使用 [資源群組] MyResourceGroupName，在 WestUS 位置建立名為 MyEventHubName 的事件中心，以及兩個分區 \` \` \` \` 。</span><span class="sxs-lookup"><span data-stu-id="a7acb-112">Creates an Event Hub named \`MyEventHubName\` with a 3-day message retention period and two partitions, in the \`WestUS\` location, with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="a7acb-113">範例2</span><span class="sxs-lookup"><span data-stu-id="a7acb-113">Example 2</span></span>
```
PS C:\> New-AzureRmEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location WestUS -EventHubName MyEventHubName -MessageRetentionInDays 3 -PartitionCount 2

PS C:\> $CreatedEventHub = Get-AzureRmEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName

PS C:\> $createdEventHub.CaptureDescription = New-Object -TypeName Microsoft.Azure.Commands.EventHub.Models.CaptureDescriptionAttributes

PS C:\> $createdEventHub.CaptureDescription.Enabled = $true
PS C:\> $createdEventHub.CaptureDescription.IntervalInSeconds  = 120
PS C:\> $createdEventHub.CaptureDescription.Encoding  = "Avro"
PS C:\> $createdEventHub.CaptureDescription.SizeLimitInBytes = 10485763
PS C:\> $createdEventHub.CaptureDescription.Destination.Name = "EventHubArchive.AzureBlockBlob"
PS C:\> $createdEventHub.CaptureDescription.Destination.BlobContainer = "container"
PS C:\> $createdEventHub.CaptureDescription.Destination.ArchiveNameFormat = "{Namespace}/{EventHub}/{PartitionId}/{Year}/{Month}/{Day}/{Hour}/{Minute}/{Second}"
PS C:\> $createdEventHub.CaptureDescription.Destination.StorageAccountResourceId = "/subscriptions/{SubscriptionId}/resourceGroups/MyResourceGroupName/providers/Microsoft.ClassicStorage/storageAccounts/arjunteststorage"
PS C:\> Set-AzureRmEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName -InputObject MyCreatedEventHub -messageRetentionInDays 4 -partitionCount 2
```

<span data-ttu-id="a7acb-114">\` \` \` \` 使用資源群組 MyResourceGroupName，在 WestUS 位置中建立一個名為 MyEventHubName 的事件中心，其中包含為期3天的郵件保持期、2個分區和 CaptureDescription 屬性 \` \` 。</span><span class="sxs-lookup"><span data-stu-id="a7acb-114">Creates an Event Hub named \`MyEventHubName\` with a 3-day message retention period, 2 partitions and CaptureDescription properties in the \`WestUS\` location, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="a7acb-115">參數</span><span class="sxs-lookup"><span data-stu-id="a7acb-115">PARAMETERS</span></span>

### <span data-ttu-id="a7acb-116">-位置</span><span class="sxs-lookup"><span data-stu-id="a7acb-116">-Location</span></span>
<span data-ttu-id="a7acb-117">命名空間地理位置。</span><span class="sxs-lookup"><span data-stu-id="a7acb-117">Namespace geographic location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7acb-118">-MessageRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="a7acb-118">-MessageRetentionInDays</span></span>
<span data-ttu-id="a7acb-119">事件中心訊息保留時間（天）。</span><span class="sxs-lookup"><span data-stu-id="a7acb-119">Event Hubs message retention time in days.</span></span>

```yaml
Type: Int64
Parameter Sets: EventhubPropertiesSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7acb-120">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="a7acb-120">-PartitionCount</span></span>
<span data-ttu-id="a7acb-121">事件中心中的分區數。</span><span class="sxs-lookup"><span data-stu-id="a7acb-121">Number of partitions in the Event Hub.</span></span>

```yaml
Type: Int64
Parameter Sets: EventhubPropertiesSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7acb-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7acb-122">-ResourceGroupName</span></span>
<span data-ttu-id="a7acb-123">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="a7acb-123">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7acb-124">-確認</span><span class="sxs-lookup"><span data-stu-id="a7acb-124">-Confirm</span></span>
<span data-ttu-id="a7acb-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a7acb-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7acb-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7acb-126">-WhatIf</span></span>
<span data-ttu-id="a7acb-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a7acb-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7acb-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a7acb-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7acb-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a7acb-129">-InputObject</span></span>
<span data-ttu-id="a7acb-130">EventHub 輸入物件。</span><span class="sxs-lookup"><span data-stu-id="a7acb-130">EventHub Input object.</span></span>

```yaml
Type: EventHubAttributes
Parameter Sets: EventhubInputObjectSet
Aliases: EventHubObj

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7acb-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="a7acb-131">-Name</span></span>
<span data-ttu-id="a7acb-132">Eventhub Name。</span><span class="sxs-lookup"><span data-stu-id="a7acb-132">Eventhub Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7acb-133">-命名空間</span><span class="sxs-lookup"><span data-stu-id="a7acb-133">-Namespace</span></span>
<span data-ttu-id="a7acb-134">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="a7acb-134">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="a7acb-135">輸入</span><span class="sxs-lookup"><span data-stu-id="a7acb-135">INPUTS</span></span>

### <span data-ttu-id="a7acb-136">System.object</span><span class="sxs-lookup"><span data-stu-id="a7acb-136">System.String</span></span>

## <span data-ttu-id="a7acb-137">輸出</span><span class="sxs-lookup"><span data-stu-id="a7acb-137">OUTPUTS</span></span>

### <span data-ttu-id="a7acb-138">EventHubAttributes 的 [.]</span><span class="sxs-lookup"><span data-stu-id="a7acb-138">Microsoft.Azure.Commands.EventHub.Models.EventHubAttributes</span></span>

## <span data-ttu-id="a7acb-139">筆記</span><span class="sxs-lookup"><span data-stu-id="a7acb-139">NOTES</span></span>

## <span data-ttu-id="a7acb-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="a7acb-140">RELATED LINKS</span></span>

