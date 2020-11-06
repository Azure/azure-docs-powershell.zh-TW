---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHub.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 2ff36708ba9b8303c8b8763146c81ee4e4d8b209
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451695"
---
# <span data-ttu-id="1d47c-101">Set-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="1d47c-101">Set-AzureRmEventHub</span></span>

## <span data-ttu-id="1d47c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1d47c-102">SYNOPSIS</span></span>
<span data-ttu-id="1d47c-103">更新指定的事件中樞。</span><span class="sxs-lookup"><span data-stu-id="1d47c-103">Updates the specified Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1d47c-104">句法</span><span class="sxs-lookup"><span data-stu-id="1d47c-104">SYNTAX</span></span>

### <span data-ttu-id="1d47c-105">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="1d47c-105">EventhubInputObjectSet</span></span>
```
Set-AzureRmEventHub [-ResourceGroupName] <String> -Namespace <String> -Name <String>
 [-InputObject <EventHubAttributes>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="1d47c-106">EventhubPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="1d47c-106">EventhubPropertiesSet</span></span>
```
Set-AzureRmEventHub [-ResourceGroupName] <String> -Namespace <String> -Name <String>
 [-messageRetentionInDays <Int64>] [-partitionCount <Int64>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="1d47c-107">說明</span><span class="sxs-lookup"><span data-stu-id="1d47c-107">DESCRIPTION</span></span>
<span data-ttu-id="1d47c-108">Set-AzureRmEventHub Cmdlet 會更新指定事件中樞的屬性。</span><span class="sxs-lookup"><span data-stu-id="1d47c-108">The Set-AzureRmEventHub cmdlet updates the properties of the specified Event Hub.</span></span>

## <span data-ttu-id="1d47c-109">示例</span><span class="sxs-lookup"><span data-stu-id="1d47c-109">EXAMPLES</span></span>

### <span data-ttu-id="1d47c-110">範例1</span><span class="sxs-lookup"><span data-stu-id="1d47c-110">Example 1</span></span>
<span data-ttu-id="1d47c-111">若要使用捕獲描述屬性來更新 Eventhub，請依照下列步驟進行。</span><span class="sxs-lookup"><span data-stu-id="1d47c-111">To update Eventhub with Capture description properties, please follow the below steps.</span></span> 

```
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

<span data-ttu-id="1d47c-112">更新由 \` \` MyCreatedEventHub 物件所代表的事件中樞 MyEventHubName \` \` ，將郵件保留期間設定為4天，磁碟分割數量為2和 CaptureDescription 屬性</span><span class="sxs-lookup"><span data-stu-id="1d47c-112">Updates the Event Hub \`MyEventHubName\` represented by the \`MyCreatedEventHub\` object, setting the message retention period to 4 days, the number of partitions to 2 and CaptureDescription properties</span></span>

### <span data-ttu-id="1d47c-113">範例2</span><span class="sxs-lookup"><span data-stu-id="1d47c-113">Example 2</span></span>

```
PS C:\> Set-AzureRmEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName -InputObject MyCreatedEventHub -messageRetentionInDays 4 -partitionCount 2
```

<span data-ttu-id="1d47c-114">更新 \` \` MyCreatedEventHub 物件所代表的事件中樞 \` MyEventHubName \` ，將郵件保留期間設定為4天，並將分區數量設為2。</span><span class="sxs-lookup"><span data-stu-id="1d47c-114">Updates the Event Hub \`MyEventHubName\` represented by the \`MyCreatedEventHub\` object, setting the message retention period to 4 days, and the number of partitions to 2.</span></span>

## <span data-ttu-id="1d47c-115">參數</span><span class="sxs-lookup"><span data-stu-id="1d47c-115">PARAMETERS</span></span>

### <span data-ttu-id="1d47c-116">-messageRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="1d47c-116">-messageRetentionInDays</span></span>
<span data-ttu-id="1d47c-117">事件中心訊息保留期間（以天為單位）。</span><span class="sxs-lookup"><span data-stu-id="1d47c-117">Event Hub message retention period, in days.</span></span>

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

### <span data-ttu-id="1d47c-118">-partitionCount</span><span class="sxs-lookup"><span data-stu-id="1d47c-118">-partitionCount</span></span>
<span data-ttu-id="1d47c-119">這個事件中樞上的磁碟分割數目。</span><span class="sxs-lookup"><span data-stu-id="1d47c-119">Number of partitions on this Event Hub.</span></span>

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

### <span data-ttu-id="1d47c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d47c-120">-ResourceGroupName</span></span>
<span data-ttu-id="1d47c-121">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="1d47c-121">Resource group name.</span></span>

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

### <span data-ttu-id="1d47c-122">-確認</span><span class="sxs-lookup"><span data-stu-id="1d47c-122">-Confirm</span></span>
<span data-ttu-id="1d47c-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1d47c-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d47c-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d47c-124">-WhatIf</span></span>
<span data-ttu-id="1d47c-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1d47c-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d47c-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1d47c-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d47c-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1d47c-127">-InputObject</span></span>
<span data-ttu-id="1d47c-128">EventHub 物件。</span><span class="sxs-lookup"><span data-stu-id="1d47c-128">EventHub object.</span></span>

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

### <span data-ttu-id="1d47c-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="1d47c-129">-Name</span></span>
<span data-ttu-id="1d47c-130">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="1d47c-130">Namespace Name.</span></span>

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

### <span data-ttu-id="1d47c-131">-命名空間</span><span class="sxs-lookup"><span data-stu-id="1d47c-131">-Namespace</span></span>
<span data-ttu-id="1d47c-132">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="1d47c-132">Namespace Name.</span></span>

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

## <span data-ttu-id="1d47c-133">輸入</span><span class="sxs-lookup"><span data-stu-id="1d47c-133">INPUTS</span></span>

### <span data-ttu-id="1d47c-134">System.object</span><span class="sxs-lookup"><span data-stu-id="1d47c-134">System.String</span></span>

## <span data-ttu-id="1d47c-135">輸出</span><span class="sxs-lookup"><span data-stu-id="1d47c-135">OUTPUTS</span></span>

### <span data-ttu-id="1d47c-136">EventHubAttributes 的 [.]</span><span class="sxs-lookup"><span data-stu-id="1d47c-136">Microsoft.Azure.Commands.EventHub.Models.EventHubAttributes</span></span>

## <span data-ttu-id="1d47c-137">筆記</span><span class="sxs-lookup"><span data-stu-id="1d47c-137">NOTES</span></span>

## <span data-ttu-id="1d47c-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="1d47c-138">RELATED LINKS</span></span>

