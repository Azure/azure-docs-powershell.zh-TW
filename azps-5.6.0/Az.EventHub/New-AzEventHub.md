---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/new-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHub.md
ms.openlocfilehash: 366bb4879b2db8bbb4a4335442a4abc6f07a5221
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903217"
---
# <span data-ttu-id="a4cff-101">New-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="a4cff-101">New-AzEventHub</span></span>

## <span data-ttu-id="a4cff-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a4cff-102">SYNOPSIS</span></span>
<span data-ttu-id="a4cff-103">建立新事件中樞。</span><span class="sxs-lookup"><span data-stu-id="a4cff-103">Creates a new Event Hub.</span></span>

## <span data-ttu-id="a4cff-104">語法</span><span class="sxs-lookup"><span data-stu-id="a4cff-104">SYNTAX</span></span>

### <span data-ttu-id="a4cff-105">EventhubPropertiesSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a4cff-105">EventhubPropertiesSet (Default)</span></span>
```
New-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-MessageRetentionInDays <Int64>] [-PartitionCount <Int64>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4cff-106">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a4cff-106">EventhubInputObjectSet</span></span>
```
New-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSEventHubAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a4cff-107">描述</span><span class="sxs-lookup"><span data-stu-id="a4cff-107">DESCRIPTION</span></span>
<span data-ttu-id="a4cff-108">Cmdlet New-AzEventHub會建立一個新的 Azure 事件中樞。</span><span class="sxs-lookup"><span data-stu-id="a4cff-108">The New-AzEventHub cmdlet creates a new Azure Event Hub.</span></span>
<span data-ttu-id="a4cff-109">若要使用捕獲描述屬性建立 Eventhub，請遵循下列步驟 (範例 2) 。</span><span class="sxs-lookup"><span data-stu-id="a4cff-109">To create Eventhub with Capture description properties, please follow the below steps (Examples 2).</span></span> 

## <span data-ttu-id="a4cff-110">例子</span><span class="sxs-lookup"><span data-stu-id="a4cff-110">EXAMPLES</span></span>

### <span data-ttu-id="a4cff-111">範例 1：- 建立新 EventHub</span><span class="sxs-lookup"><span data-stu-id="a4cff-111">Example 1: - Create new EventHub</span></span>
```powershell
PS C:\> New-AzEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Name MyEventHubName
```

<span data-ttu-id="a4cff-112">使用資源群組 \` \` \` \` \` MyResourceGroupName，在 WestUS 位置建立名為 MyEventHubName 的事件中樞，其郵件保留期間為 3 天，且有兩個磁碟分割 \` 。</span><span class="sxs-lookup"><span data-stu-id="a4cff-112">Creates an Event Hub named \`MyEventHubName\` with a 3-day message retention period and two partitions, in the \`WestUS\` location, with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="a4cff-113">範例 2：Update Eventhub with 'CaptureDescription'</span><span class="sxs-lookup"><span data-stu-id="a4cff-113">Example 2: Update Eventhub with 'CaptureDescription'</span></span>
```powershell
PS C:\> New-AzEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Name MyEventHubName -MessageRetentionInDays 3 -PartitionCount 2

PS C:\> $CreatedEventHub = Get-AzEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName

PS C:\> $createdEventHub.CaptureDescription = New-Object -TypeName Microsoft.Azure.Commands.EventHub.Models.PSCaptureDescriptionAttributes

PS C:\> $createdEventHub.CaptureDescription.Enabled = $true
PS C:\> $createdEventHub.CaptureDescription.IntervalInSeconds  = 120
PS C:\> $createdEventHub.CaptureDescription.Encoding  = "Avro"
PS C:\> $createdEventHub.CaptureDescription.SizeLimitInBytes = 10485763
PS C:\> $createdEventHub.CaptureDescription.Destination.Name = "EventHubArchive.AzureBlockBlob"
PS C:\> $createdEventHub.CaptureDescription.Destination.BlobContainer = "container"
PS C:\> $createdEventHub.CaptureDescription.Destination.ArchiveNameFormat = "{Namespace}/{EventHub}/{PartitionId}/{Year}/{Month}/{Day}/{Hour}/{Minute}/{Second}"
PS C:\> $createdEventHub.CaptureDescription.Destination.StorageAccountResourceId = "/subscriptions/{SubscriptionId}/resourceGroups/MyResourceGroupName/providers/Microsoft.ClassicStorage/storageAccounts/arjunteststorage"
PS C:\> Set-AzEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName -InputObject MyCreatedEventHub -messageRetentionInDays 4 -partitionCount 2
```

<span data-ttu-id="a4cff-114">使用資源群組 \` \` \` \` \` MyResourceGroupName，在 WestUS 位置中建立名為 MyEventHubName 的事件中樞，其為 3 天的郵件保留期間、2 個磁碟分割和 CaptureDescription 屬性 \` 。</span><span class="sxs-lookup"><span data-stu-id="a4cff-114">Creates an Event Hub named \`MyEventHubName\` with a 3-day message retention period, 2 partitions and CaptureDescription properties in the \`WestUS\` location, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="a4cff-115">參數</span><span class="sxs-lookup"><span data-stu-id="a4cff-115">PARAMETERS</span></span>

### <span data-ttu-id="a4cff-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4cff-116">-DefaultProfile</span></span>
<span data-ttu-id="a4cff-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a4cff-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4cff-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a4cff-118">-InputObject</span></span>
<span data-ttu-id="a4cff-119">EventHub 輸入物件</span><span class="sxs-lookup"><span data-stu-id="a4cff-119">EventHub Input object</span></span>

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

### <span data-ttu-id="a4cff-120">-MessageRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="a4cff-120">-MessageRetentionInDays</span></span>
<span data-ttu-id="a4cff-121">事件hub 郵件保留天數</span><span class="sxs-lookup"><span data-stu-id="a4cff-121">Eventhub Message Retention In Days</span></span>

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

### <span data-ttu-id="a4cff-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="a4cff-122">-Name</span></span>
<span data-ttu-id="a4cff-123">Eventhub 名稱</span><span class="sxs-lookup"><span data-stu-id="a4cff-123">Eventhub Name</span></span>

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

### <span data-ttu-id="a4cff-124">-命名空間</span><span class="sxs-lookup"><span data-stu-id="a4cff-124">-Namespace</span></span>
<span data-ttu-id="a4cff-125">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="a4cff-125">Namespace Name</span></span>

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

### <span data-ttu-id="a4cff-126">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="a4cff-126">-PartitionCount</span></span>
<span data-ttu-id="a4cff-127">Eventhub PartitionCount</span><span class="sxs-lookup"><span data-stu-id="a4cff-127">Eventhub PartitionCount</span></span>

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

### <span data-ttu-id="a4cff-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4cff-128">-ResourceGroupName</span></span>
<span data-ttu-id="a4cff-129">資源組名</span><span class="sxs-lookup"><span data-stu-id="a4cff-129">Resource Group Name</span></span>

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

### <span data-ttu-id="a4cff-130">-確認</span><span class="sxs-lookup"><span data-stu-id="a4cff-130">-Confirm</span></span>
<span data-ttu-id="a4cff-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a4cff-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4cff-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4cff-132">-WhatIf</span></span>
<span data-ttu-id="a4cff-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a4cff-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4cff-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a4cff-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4cff-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4cff-135">CommonParameters</span></span>
<span data-ttu-id="a4cff-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a4cff-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4cff-137">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="a4cff-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4cff-138">輸入</span><span class="sxs-lookup"><span data-stu-id="a4cff-138">INPUTS</span></span>

### <span data-ttu-id="a4cff-139">System.String</span><span class="sxs-lookup"><span data-stu-id="a4cff-139">System.String</span></span>

### <span data-ttu-id="a4cff-140">Microsoft.Azure.Commands.EventHub.models.PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="a4cff-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

### <span data-ttu-id="a4cff-141">System.Nullable'1[[System.Int64， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a4cff-141">System.Nullable\`1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="a4cff-142">輸出</span><span class="sxs-lookup"><span data-stu-id="a4cff-142">OUTPUTS</span></span>

### <span data-ttu-id="a4cff-143">Microsoft.Azure.Commands.EventHub.models.PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="a4cff-143">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="a4cff-144">筆記</span><span class="sxs-lookup"><span data-stu-id="a4cff-144">NOTES</span></span>

## <span data-ttu-id="a4cff-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="a4cff-145">RELATED LINKS</span></span>
