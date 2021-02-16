---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHub.md
ms.openlocfilehash: 15704f90530c332eddfeaf4a9e13fe2d7767bfa4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100133231"
---
# <span data-ttu-id="778e4-101">Set-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="778e4-101">Set-AzEventHub</span></span>

## <span data-ttu-id="778e4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="778e4-102">SYNOPSIS</span></span>
<span data-ttu-id="778e4-103">更新指定的事件中樞。</span><span class="sxs-lookup"><span data-stu-id="778e4-103">Updates the specified Event Hub.</span></span>

## <span data-ttu-id="778e4-104">句法</span><span class="sxs-lookup"><span data-stu-id="778e4-104">SYNTAX</span></span>

### <span data-ttu-id="778e4-105">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="778e4-105">EventhubInputObjectSet</span></span>
```
Set-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSEventHubAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="778e4-106">EventhubPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="778e4-106">EventhubPropertiesSet</span></span>
```
Set-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-messageRetentionInDays <Int64>] [-partitionCount <Int64>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="778e4-107">說明</span><span class="sxs-lookup"><span data-stu-id="778e4-107">DESCRIPTION</span></span>
<span data-ttu-id="778e4-108">Set-AzEventHub Cmdlet 會更新指定事件中樞的屬性。</span><span class="sxs-lookup"><span data-stu-id="778e4-108">The Set-AzEventHub cmdlet updates the properties of the specified Event Hub.</span></span>

## <span data-ttu-id="778e4-109">示例</span><span class="sxs-lookup"><span data-stu-id="778e4-109">EXAMPLES</span></span>

### <span data-ttu-id="778e4-110">範例1</span><span class="sxs-lookup"><span data-stu-id="778e4-110">Example 1</span></span>
<span data-ttu-id="778e4-111">若要使用捕獲描述屬性來更新 Eventhub，請依照下列步驟進行。</span><span class="sxs-lookup"><span data-stu-id="778e4-111">To update Eventhub with Capture description properties, please follow the below steps.</span></span> 

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

<span data-ttu-id="778e4-112">更新 \` \` MyCreatedEventHub 物件所代表的事件中樞 \` MyEventHubName \` ，設定 CaptureDescription 屬性</span><span class="sxs-lookup"><span data-stu-id="778e4-112">Updates the Event Hub \`MyEventHubName\` represented by the \`MyCreatedEventHub\` object, setting the CaptureDescription properties</span></span>

### <span data-ttu-id="778e4-113">範例2</span><span class="sxs-lookup"><span data-stu-id="778e4-113">Example 2</span></span>
```
PS C:\> Set-AzEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName -InputObject MyCreatedEventHub -messageRetentionInDays 4 -partitionCount 2
```

<span data-ttu-id="778e4-114">更新 \` \` MyCreatedEventHub 物件所代表的事件中樞 \` MyEventHubName \` ，將郵件保留期間設定為4天，並將分區數量設為2。</span><span class="sxs-lookup"><span data-stu-id="778e4-114">Updates the Event Hub \`MyEventHubName\` represented by the \`MyCreatedEventHub\` object, setting the message retention period to 4 days, and the number of partitions to 2.</span></span>

## <span data-ttu-id="778e4-115">參數</span><span class="sxs-lookup"><span data-stu-id="778e4-115">PARAMETERS</span></span>

### <span data-ttu-id="778e4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="778e4-116">-DefaultProfile</span></span>
<span data-ttu-id="778e4-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="778e4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="778e4-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="778e4-118">-InputObject</span></span>
<span data-ttu-id="778e4-119">EventHub 物件</span><span class="sxs-lookup"><span data-stu-id="778e4-119">EventHub object</span></span>

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

### <span data-ttu-id="778e4-120">-messageRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="778e4-120">-messageRetentionInDays</span></span>
<span data-ttu-id="778e4-121">Eventhub 郵件保留天數</span><span class="sxs-lookup"><span data-stu-id="778e4-121">Eventhub Message Retention In Days</span></span>

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

### <span data-ttu-id="778e4-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="778e4-122">-Name</span></span>
<span data-ttu-id="778e4-123">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="778e4-123">Namespace Name</span></span>

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

### <span data-ttu-id="778e4-124">-命名空間</span><span class="sxs-lookup"><span data-stu-id="778e4-124">-Namespace</span></span>
<span data-ttu-id="778e4-125">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="778e4-125">Namespace Name</span></span>

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

### <span data-ttu-id="778e4-126">-partitionCount</span><span class="sxs-lookup"><span data-stu-id="778e4-126">-partitionCount</span></span>
<span data-ttu-id="778e4-127">Eventhub PartitionCount</span><span class="sxs-lookup"><span data-stu-id="778e4-127">Eventhub PartitionCount</span></span>

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

### <span data-ttu-id="778e4-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="778e4-128">-ResourceGroupName</span></span>
<span data-ttu-id="778e4-129">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="778e4-129">Resource Group Name</span></span>

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

### <span data-ttu-id="778e4-130">-確認</span><span class="sxs-lookup"><span data-stu-id="778e4-130">-Confirm</span></span>
<span data-ttu-id="778e4-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="778e4-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="778e4-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="778e4-132">-WhatIf</span></span>
<span data-ttu-id="778e4-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="778e4-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="778e4-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="778e4-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="778e4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="778e4-135">CommonParameters</span></span>
<span data-ttu-id="778e4-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="778e4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="778e4-137">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="778e4-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="778e4-138">輸入</span><span class="sxs-lookup"><span data-stu-id="778e4-138">INPUTS</span></span>

### <span data-ttu-id="778e4-139">System.object</span><span class="sxs-lookup"><span data-stu-id="778e4-139">System.String</span></span>

### <span data-ttu-id="778e4-140">PSEventHubAttributes 的 [.]</span><span class="sxs-lookup"><span data-stu-id="778e4-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

### <span data-ttu-id="778e4-141">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="778e4-141">System.Nullable\`1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="778e4-142">輸出</span><span class="sxs-lookup"><span data-stu-id="778e4-142">OUTPUTS</span></span>

### <span data-ttu-id="778e4-143">PSEventHubAttributes 的 [.]</span><span class="sxs-lookup"><span data-stu-id="778e4-143">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="778e4-144">筆記</span><span class="sxs-lookup"><span data-stu-id="778e4-144">NOTES</span></span>

## <span data-ttu-id="778e4-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="778e4-145">RELATED LINKS</span></span>
