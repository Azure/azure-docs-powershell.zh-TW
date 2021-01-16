---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHub.md
ms.openlocfilehash: a5a1f0bbe0f353014047e795c467a645e244f125
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98289131"
---
# <span data-ttu-id="3eb41-101">Set-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="3eb41-101">Set-AzEventHub</span></span>

## <span data-ttu-id="3eb41-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3eb41-102">SYNOPSIS</span></span>
<span data-ttu-id="3eb41-103">更新指定的事件中樞。</span><span class="sxs-lookup"><span data-stu-id="3eb41-103">Updates the specified Event Hub.</span></span>

## <span data-ttu-id="3eb41-104">句法</span><span class="sxs-lookup"><span data-stu-id="3eb41-104">SYNTAX</span></span>

### <span data-ttu-id="3eb41-105">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="3eb41-105">EventhubInputObjectSet</span></span>
```
Set-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSEventHubAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3eb41-106">EventhubPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="3eb41-106">EventhubPropertiesSet</span></span>
```
Set-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-messageRetentionInDays <Int64>] [-partitionCount <Int64>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3eb41-107">說明</span><span class="sxs-lookup"><span data-stu-id="3eb41-107">DESCRIPTION</span></span>
<span data-ttu-id="3eb41-108">Set-AzEventHub Cmdlet 會更新指定事件中樞的屬性。</span><span class="sxs-lookup"><span data-stu-id="3eb41-108">The Set-AzEventHub cmdlet updates the properties of the specified Event Hub.</span></span>

## <span data-ttu-id="3eb41-109">示例</span><span class="sxs-lookup"><span data-stu-id="3eb41-109">EXAMPLES</span></span>

### <span data-ttu-id="3eb41-110">範例1</span><span class="sxs-lookup"><span data-stu-id="3eb41-110">Example 1</span></span>
<span data-ttu-id="3eb41-111">若要使用捕獲描述屬性來更新 Eventhub，請依照下列步驟進行。</span><span class="sxs-lookup"><span data-stu-id="3eb41-111">To update Eventhub with Capture description properties, please follow the below steps.</span></span> 

```
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

<span data-ttu-id="3eb41-112">更新由 \` \` MyCreatedEventHub 物件所代表的事件中樞 MyEventHubName \` \` ，將郵件保留期間設定為4天，磁碟分割數量為2和 CaptureDescription 屬性</span><span class="sxs-lookup"><span data-stu-id="3eb41-112">Updates the Event Hub \`MyEventHubName\` represented by the \`MyCreatedEventHub\` object, setting the message retention period to 4 days, the number of partitions to 2 and CaptureDescription properties</span></span>

### <span data-ttu-id="3eb41-113">範例2</span><span class="sxs-lookup"><span data-stu-id="3eb41-113">Example 2</span></span>
```
PS C:\> Set-AzEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName -InputObject MyCreatedEventHub -messageRetentionInDays 4 -partitionCount 2
```

<span data-ttu-id="3eb41-114">更新 \` \` MyCreatedEventHub 物件所代表的事件中樞 \` MyEventHubName \` ，將郵件保留期間設定為4天，並將分區數量設為2。</span><span class="sxs-lookup"><span data-stu-id="3eb41-114">Updates the Event Hub \`MyEventHubName\` represented by the \`MyCreatedEventHub\` object, setting the message retention period to 4 days, and the number of partitions to 2.</span></span>

## <span data-ttu-id="3eb41-115">參數</span><span class="sxs-lookup"><span data-stu-id="3eb41-115">PARAMETERS</span></span>

### <span data-ttu-id="3eb41-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3eb41-116">-DefaultProfile</span></span>
<span data-ttu-id="3eb41-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3eb41-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3eb41-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3eb41-118">-InputObject</span></span>
<span data-ttu-id="3eb41-119">EventHub 物件</span><span class="sxs-lookup"><span data-stu-id="3eb41-119">EventHub object</span></span>

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

### <span data-ttu-id="3eb41-120">-messageRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="3eb41-120">-messageRetentionInDays</span></span>
<span data-ttu-id="3eb41-121">Eventhub 郵件保留天數</span><span class="sxs-lookup"><span data-stu-id="3eb41-121">Eventhub Message Retention In Days</span></span>

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

### <span data-ttu-id="3eb41-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="3eb41-122">-Name</span></span>
<span data-ttu-id="3eb41-123">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="3eb41-123">Namespace Name</span></span>

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

### <span data-ttu-id="3eb41-124">-命名空間</span><span class="sxs-lookup"><span data-stu-id="3eb41-124">-Namespace</span></span>
<span data-ttu-id="3eb41-125">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="3eb41-125">Namespace Name</span></span>

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

### <span data-ttu-id="3eb41-126">-partitionCount</span><span class="sxs-lookup"><span data-stu-id="3eb41-126">-partitionCount</span></span>
<span data-ttu-id="3eb41-127">Eventhub PartitionCount</span><span class="sxs-lookup"><span data-stu-id="3eb41-127">Eventhub PartitionCount</span></span>

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

### <span data-ttu-id="3eb41-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3eb41-128">-ResourceGroupName</span></span>
<span data-ttu-id="3eb41-129">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="3eb41-129">Resource Group Name</span></span>

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

### <span data-ttu-id="3eb41-130">-確認</span><span class="sxs-lookup"><span data-stu-id="3eb41-130">-Confirm</span></span>
<span data-ttu-id="3eb41-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3eb41-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3eb41-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3eb41-132">-WhatIf</span></span>
<span data-ttu-id="3eb41-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3eb41-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3eb41-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3eb41-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3eb41-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3eb41-135">CommonParameters</span></span>
<span data-ttu-id="3eb41-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3eb41-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3eb41-137">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3eb41-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3eb41-138">輸入</span><span class="sxs-lookup"><span data-stu-id="3eb41-138">INPUTS</span></span>

### <span data-ttu-id="3eb41-139">System.object</span><span class="sxs-lookup"><span data-stu-id="3eb41-139">System.String</span></span>

### <span data-ttu-id="3eb41-140">PSEventHubAttributes 的 [.]</span><span class="sxs-lookup"><span data-stu-id="3eb41-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

### <span data-ttu-id="3eb41-141">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="3eb41-141">System.Nullable\`1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="3eb41-142">輸出</span><span class="sxs-lookup"><span data-stu-id="3eb41-142">OUTPUTS</span></span>

### <span data-ttu-id="3eb41-143">PSEventHubAttributes 的 [.]</span><span class="sxs-lookup"><span data-stu-id="3eb41-143">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="3eb41-144">筆記</span><span class="sxs-lookup"><span data-stu-id="3eb41-144">NOTES</span></span>

## <span data-ttu-id="3eb41-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="3eb41-145">RELATED LINKS</span></span>
