---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/set-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHub.md
ms.openlocfilehash: 70c059598f895ee933abefb0b71aa36d5ce0f6f7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909026"
---
# <span data-ttu-id="e2c42-101">Set-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="e2c42-101">Set-AzEventHub</span></span>

## <span data-ttu-id="e2c42-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e2c42-102">SYNOPSIS</span></span>
<span data-ttu-id="e2c42-103">更新指定的事件中樞。</span><span class="sxs-lookup"><span data-stu-id="e2c42-103">Updates the specified Event Hub.</span></span>

## <span data-ttu-id="e2c42-104">語法</span><span class="sxs-lookup"><span data-stu-id="e2c42-104">SYNTAX</span></span>

### <span data-ttu-id="e2c42-105">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e2c42-105">EventhubInputObjectSet</span></span>
```
Set-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSEventHubAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e2c42-106">EventhubPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="e2c42-106">EventhubPropertiesSet</span></span>
```
Set-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-messageRetentionInDays <Int64>] [-partitionCount <Int64>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2c42-107">描述</span><span class="sxs-lookup"><span data-stu-id="e2c42-107">DESCRIPTION</span></span>
<span data-ttu-id="e2c42-108">Cmdlet Set-AzEventHub更新指定事件中樞的屬性。</span><span class="sxs-lookup"><span data-stu-id="e2c42-108">The Set-AzEventHub cmdlet updates the properties of the specified Event Hub.</span></span>

## <span data-ttu-id="e2c42-109">例子</span><span class="sxs-lookup"><span data-stu-id="e2c42-109">EXAMPLES</span></span>

### <span data-ttu-id="e2c42-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="e2c42-110">Example 1</span></span>
<span data-ttu-id="e2c42-111">若要使用捕獲描述屬性更新 Eventhub，請遵循下列步驟。</span><span class="sxs-lookup"><span data-stu-id="e2c42-111">To update Eventhub with Capture description properties, please follow the below steps.</span></span> 

```
PS C:\> $createdEventHub = Get-AzEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyCreatedEventHub
PS C:\> $ceatedEventHub.CaptureDescription = New-Object -TypeName Microsoft.Azure.Commands.EventHub.Models.PSCaptureDescriptionAttributes
PS C:\> $createdEventHub.CaptureDescription.Enabled = $true
PS C:\> $createdEventHub.CaptureDescription.IntervalInSeconds  = 120
PS C:\> $createdEventHub.CaptureDescription.Encoding  = "Avro"
PS C:\> $createdEventHub.CaptureDescription.SizeLimitInBytes = 10485763
PS C:\> $createdEventHub.CaptureDescription.Destination.Name = "EventHubArchive.AzureBlockBlob"
PS C:\> $createdEventHub.CaptureDescription.Destination.BlobContainer = "container"
PS C:\> $createdEventHub.CaptureDescription.Destination.ArchiveNameFormat = "{Namespace}/{EventHub}/{PartitionId}/{Year}/{Month}/{Day}/{Hour}/{Minute}/{Second}"
PS C:\> $createdEventHub.CaptureDescription.Destination.StorageAccountResourceId = "/subscriptions/{SubscriptionId}/resourceGroups/MyResourceGroupName/providers/Microsoft.ClassicStorage/storageAccounts/arjunteststorage"
PS C:\> Set-AzEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName -InputObject $createdEventHub 
```

<span data-ttu-id="e2c42-112">更新 \` MyEventHubHub 物件所代表的 \` 事件中樞 \` MyEventHubName， \` 設定 CaptureDescription 屬性</span><span class="sxs-lookup"><span data-stu-id="e2c42-112">Updates the Event Hub \`MyEventHubName\` represented by the \`MyCreatedEventHub\` object, setting the CaptureDescription properties</span></span>

### <span data-ttu-id="e2c42-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="e2c42-113">Example 2</span></span>
```
PS C:\> Set-AzEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName -InputObject MyCreatedEventHub -messageRetentionInDays 4 -partitionCount 2
```

<span data-ttu-id="e2c42-114">更新 \` \` \` MyCreaedEventHub 物件所代表的事件中樞 MyEventHubName，將郵件保留期間設定為 4 天，以及磁碟分割數目設定 \` 為 2。</span><span class="sxs-lookup"><span data-stu-id="e2c42-114">Updates the Event Hub \`MyEventHubName\` represented by the \`MyCreatedEventHub\` object, setting the message retention period to 4 days, and the number of partitions to 2.</span></span>

## <span data-ttu-id="e2c42-115">參數</span><span class="sxs-lookup"><span data-stu-id="e2c42-115">PARAMETERS</span></span>

### <span data-ttu-id="e2c42-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2c42-116">-DefaultProfile</span></span>
<span data-ttu-id="e2c42-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e2c42-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2c42-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e2c42-118">-InputObject</span></span>
<span data-ttu-id="e2c42-119">EventHub 物件</span><span class="sxs-lookup"><span data-stu-id="e2c42-119">EventHub object</span></span>

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

### <span data-ttu-id="e2c42-120">-messageRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="e2c42-120">-messageRetentionInDays</span></span>
<span data-ttu-id="e2c42-121">事件hub 郵件保留天數</span><span class="sxs-lookup"><span data-stu-id="e2c42-121">Eventhub Message Retention In Days</span></span>

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

### <span data-ttu-id="e2c42-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="e2c42-122">-Name</span></span>
<span data-ttu-id="e2c42-123">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="e2c42-123">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2c42-124">-命名空間</span><span class="sxs-lookup"><span data-stu-id="e2c42-124">-Namespace</span></span>
<span data-ttu-id="e2c42-125">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="e2c42-125">Namespace Name</span></span>

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

### <span data-ttu-id="e2c42-126">-partitionCount</span><span class="sxs-lookup"><span data-stu-id="e2c42-126">-partitionCount</span></span>
<span data-ttu-id="e2c42-127">Eventhub PartitionCount</span><span class="sxs-lookup"><span data-stu-id="e2c42-127">Eventhub PartitionCount</span></span>

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

### <span data-ttu-id="e2c42-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2c42-128">-ResourceGroupName</span></span>
<span data-ttu-id="e2c42-129">資源組名</span><span class="sxs-lookup"><span data-stu-id="e2c42-129">Resource Group Name</span></span>

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

### <span data-ttu-id="e2c42-130">-確認</span><span class="sxs-lookup"><span data-stu-id="e2c42-130">-Confirm</span></span>
<span data-ttu-id="e2c42-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="e2c42-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2c42-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2c42-132">-WhatIf</span></span>
<span data-ttu-id="e2c42-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e2c42-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2c42-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e2c42-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2c42-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2c42-135">CommonParameters</span></span>
<span data-ttu-id="e2c42-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e2c42-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2c42-137">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="e2c42-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2c42-138">輸入</span><span class="sxs-lookup"><span data-stu-id="e2c42-138">INPUTS</span></span>

### <span data-ttu-id="e2c42-139">System.String</span><span class="sxs-lookup"><span data-stu-id="e2c42-139">System.String</span></span>

### <span data-ttu-id="e2c42-140">Microsoft.Azure.Commands.EventHub.models.PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="e2c42-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

### <span data-ttu-id="e2c42-141">System.Nullable'1[[System.Int64， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e2c42-141">System.Nullable\`1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="e2c42-142">輸出</span><span class="sxs-lookup"><span data-stu-id="e2c42-142">OUTPUTS</span></span>

### <span data-ttu-id="e2c42-143">Microsoft.Azure.Commands.EventHub.models.PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="e2c42-143">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="e2c42-144">筆記</span><span class="sxs-lookup"><span data-stu-id="e2c42-144">NOTES</span></span>

## <span data-ttu-id="e2c42-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="e2c42-145">RELATED LINKS</span></span>
