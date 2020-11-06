---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/new-azurermeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHub.md
ms.openlocfilehash: 74921cb6ccfc77e2c45d734316cb2a67817c7ede
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445604"
---
# <span data-ttu-id="b31c1-101">New-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="b31c1-101">New-AzureRmEventHub</span></span>

## <span data-ttu-id="b31c1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b31c1-102">SYNOPSIS</span></span>
<span data-ttu-id="b31c1-103">建立新的事件中樞。</span><span class="sxs-lookup"><span data-stu-id="b31c1-103">Creates a new Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b31c1-104">句法</span><span class="sxs-lookup"><span data-stu-id="b31c1-104">SYNTAX</span></span>

### <span data-ttu-id="b31c1-105">EventhubPropertiesSet (預設) </span><span class="sxs-lookup"><span data-stu-id="b31c1-105">EventhubPropertiesSet (Default)</span></span>
```
New-AzureRmEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-MessageRetentionInDays <Int64>] [-PartitionCount <Int64>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b31c1-106">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b31c1-106">EventhubInputObjectSet</span></span>
```
New-AzureRmEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSEventHubAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b31c1-107">說明</span><span class="sxs-lookup"><span data-stu-id="b31c1-107">DESCRIPTION</span></span>
<span data-ttu-id="b31c1-108">New-AzureRmEventHub Cmdlet 會建立新的 Azure 事件中樞。</span><span class="sxs-lookup"><span data-stu-id="b31c1-108">The New-AzureRmEventHub cmdlet creates a new Azure Event Hub.</span></span>
<span data-ttu-id="b31c1-109">若要使用 [捕獲描述] 屬性建立 Eventhub，請依照下列步驟 (範例 2) 。</span><span class="sxs-lookup"><span data-stu-id="b31c1-109">To create Eventhub with Capture description properties, please follow the below steps (Examples 2).</span></span> 

## <span data-ttu-id="b31c1-110">示例</span><span class="sxs-lookup"><span data-stu-id="b31c1-110">EXAMPLES</span></span>

### <span data-ttu-id="b31c1-111">範例 1-建立新的 EventHub</span><span class="sxs-lookup"><span data-stu-id="b31c1-111">Example 1  - Create new EventHub</span></span>
```
PS C:\> New-AzureRmEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Name MyEventHubName
```

<span data-ttu-id="b31c1-112">\` \` 使用 [資源群組] MyResourceGroupName，在 WestUS 位置建立名為 MyEventHubName 的事件中心，以及兩個分區 \` \` \` \` 。</span><span class="sxs-lookup"><span data-stu-id="b31c1-112">Creates an Event Hub named \`MyEventHubName\` with a 3-day message retention period and two partitions, in the \`WestUS\` location, with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="b31c1-113">範例2更新 Eventhub （含 "CaptureDescription"）</span><span class="sxs-lookup"><span data-stu-id="b31c1-113">Example 2 Update Eventhub with 'CaptureDescription'</span></span>
```
PS C:\> New-AzureRmEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Name MyEventHubName -MessageRetentionInDays 3 -PartitionCount 2

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

<span data-ttu-id="b31c1-114">\` \` \` \` 使用資源群組 MyResourceGroupName，在 WestUS 位置中建立一個名為 MyEventHubName 的事件中心，其中包含為期3天的郵件保持期、2個分區和 CaptureDescription 屬性 \` \` 。</span><span class="sxs-lookup"><span data-stu-id="b31c1-114">Creates an Event Hub named \`MyEventHubName\` with a 3-day message retention period, 2 partitions and CaptureDescription properties in the \`WestUS\` location, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="b31c1-115">參數</span><span class="sxs-lookup"><span data-stu-id="b31c1-115">PARAMETERS</span></span>

### <span data-ttu-id="b31c1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b31c1-116">-DefaultProfile</span></span>
<span data-ttu-id="b31c1-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b31c1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b31c1-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b31c1-118">-InputObject</span></span>
<span data-ttu-id="b31c1-119">EventHub 輸入物件</span><span class="sxs-lookup"><span data-stu-id="b31c1-119">EventHub Input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes
Parameter Sets: EventhubInputObjectSet
Aliases: EventHubObj

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b31c1-120">-MessageRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="b31c1-120">-MessageRetentionInDays</span></span>
<span data-ttu-id="b31c1-121">Eventhub 郵件保留天數</span><span class="sxs-lookup"><span data-stu-id="b31c1-121">Eventhub Message Retention In Days</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: EventhubPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b31c1-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="b31c1-122">-Name</span></span>
<span data-ttu-id="b31c1-123">Eventhub 名稱</span><span class="sxs-lookup"><span data-stu-id="b31c1-123">Eventhub Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b31c1-124">-命名空間</span><span class="sxs-lookup"><span data-stu-id="b31c1-124">-Namespace</span></span>
<span data-ttu-id="b31c1-125">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="b31c1-125">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b31c1-126">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="b31c1-126">-PartitionCount</span></span>
<span data-ttu-id="b31c1-127">Eventhub PartitionCount</span><span class="sxs-lookup"><span data-stu-id="b31c1-127">Eventhub PartitionCount</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: EventhubPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b31c1-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b31c1-128">-ResourceGroupName</span></span>
<span data-ttu-id="b31c1-129">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="b31c1-129">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b31c1-130">-確認</span><span class="sxs-lookup"><span data-stu-id="b31c1-130">-Confirm</span></span>
<span data-ttu-id="b31c1-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b31c1-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b31c1-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b31c1-132">-WhatIf</span></span>
<span data-ttu-id="b31c1-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b31c1-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b31c1-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b31c1-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b31c1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b31c1-135">CommonParameters</span></span>
<span data-ttu-id="b31c1-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b31c1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b31c1-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b31c1-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b31c1-138">輸入</span><span class="sxs-lookup"><span data-stu-id="b31c1-138">INPUTS</span></span>

### <span data-ttu-id="b31c1-139">System.object</span><span class="sxs-lookup"><span data-stu-id="b31c1-139">System.String</span></span>

### <span data-ttu-id="b31c1-140">PSEventHubAttributes 的 [.]</span><span class="sxs-lookup"><span data-stu-id="b31c1-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

### <span data-ttu-id="b31c1-141">系統為 Nullable "1 [[System.object，mscorlib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="b31c1-141">System.Nullable\`1[[System.Int64, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="b31c1-142">輸出</span><span class="sxs-lookup"><span data-stu-id="b31c1-142">OUTPUTS</span></span>

### <span data-ttu-id="b31c1-143">PSEventHubAttributes 的 [.]</span><span class="sxs-lookup"><span data-stu-id="b31c1-143">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="b31c1-144">筆記</span><span class="sxs-lookup"><span data-stu-id="b31c1-144">NOTES</span></span>

## <span data-ttu-id="b31c1-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="b31c1-145">RELATED LINKS</span></span>
