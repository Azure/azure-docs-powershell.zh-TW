---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/set-azurermeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHub.md
ms.openlocfilehash: e5f3041038c79a12a6e9fb92937679f538ce22b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449180"
---
# <span data-ttu-id="73e78-101">Set-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="73e78-101">Set-AzureRmEventHub</span></span>

## <span data-ttu-id="73e78-102">摘要</span><span class="sxs-lookup"><span data-stu-id="73e78-102">SYNOPSIS</span></span>
<span data-ttu-id="73e78-103">更新指定的事件中樞。</span><span class="sxs-lookup"><span data-stu-id="73e78-103">Updates the specified Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73e78-104">句法</span><span class="sxs-lookup"><span data-stu-id="73e78-104">SYNTAX</span></span>

### <span data-ttu-id="73e78-105">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="73e78-105">EventhubInputObjectSet</span></span>
```
Set-AzureRmEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSEventHubAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="73e78-106">EventhubPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="73e78-106">EventhubPropertiesSet</span></span>
```
Set-AzureRmEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-messageRetentionInDays <Int64>] [-partitionCount <Int64>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73e78-107">說明</span><span class="sxs-lookup"><span data-stu-id="73e78-107">DESCRIPTION</span></span>
<span data-ttu-id="73e78-108">Set-AzureRmEventHub Cmdlet 會更新指定事件中樞的屬性。</span><span class="sxs-lookup"><span data-stu-id="73e78-108">The Set-AzureRmEventHub cmdlet updates the properties of the specified Event Hub.</span></span>

## <span data-ttu-id="73e78-109">示例</span><span class="sxs-lookup"><span data-stu-id="73e78-109">EXAMPLES</span></span>

### <span data-ttu-id="73e78-110">範例1</span><span class="sxs-lookup"><span data-stu-id="73e78-110">Example 1</span></span>
<span data-ttu-id="73e78-111">若要使用捕獲描述屬性來更新 Eventhub，請依照下列步驟進行。</span><span class="sxs-lookup"><span data-stu-id="73e78-111">To update Eventhub with Capture description properties, please follow the below steps.</span></span> 

```
PS C:\> $CreatedEventHub = Get-AzureRmEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName
PS C:\> $createdEventHub.CaptureDescription = New-Object -TypeName Microsoft.Azure.Commands.EventHub.Models.PSCaptureDescriptionAttributes
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

<span data-ttu-id="73e78-112">更新由 \` \` MyCreatedEventHub 物件所代表的事件中樞 MyEventHubName \` \` ，將郵件保留期間設定為4天，磁碟分割數量為2和 CaptureDescription 屬性</span><span class="sxs-lookup"><span data-stu-id="73e78-112">Updates the Event Hub \`MyEventHubName\` represented by the \`MyCreatedEventHub\` object, setting the message retention period to 4 days, the number of partitions to 2 and CaptureDescription properties</span></span>

### <span data-ttu-id="73e78-113">範例2</span><span class="sxs-lookup"><span data-stu-id="73e78-113">Example 2</span></span>
```
PS C:\> Set-AzureRmEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName -InputObject MyCreatedEventHub -messageRetentionInDays 4 -partitionCount 2
```

<span data-ttu-id="73e78-114">更新 \` \` MyCreatedEventHub 物件所代表的事件中樞 \` MyEventHubName \` ，將郵件保留期間設定為4天，並將分區數量設為2。</span><span class="sxs-lookup"><span data-stu-id="73e78-114">Updates the Event Hub \`MyEventHubName\` represented by the \`MyCreatedEventHub\` object, setting the message retention period to 4 days, and the number of partitions to 2.</span></span>

## <span data-ttu-id="73e78-115">參數</span><span class="sxs-lookup"><span data-stu-id="73e78-115">PARAMETERS</span></span>

### <span data-ttu-id="73e78-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73e78-116">-DefaultProfile</span></span>
<span data-ttu-id="73e78-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="73e78-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73e78-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="73e78-118">-InputObject</span></span>
<span data-ttu-id="73e78-119">EventHub 物件</span><span class="sxs-lookup"><span data-stu-id="73e78-119">EventHub object</span></span>

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

### <span data-ttu-id="73e78-120">-messageRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="73e78-120">-messageRetentionInDays</span></span>
<span data-ttu-id="73e78-121">Eventhub 郵件保留天數</span><span class="sxs-lookup"><span data-stu-id="73e78-121">Eventhub Message Retention In Days</span></span>

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

### <span data-ttu-id="73e78-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="73e78-122">-Name</span></span>
<span data-ttu-id="73e78-123">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="73e78-123">Namespace Name</span></span>

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

### <span data-ttu-id="73e78-124">-命名空間</span><span class="sxs-lookup"><span data-stu-id="73e78-124">-Namespace</span></span>
<span data-ttu-id="73e78-125">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="73e78-125">Namespace Name</span></span>

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

### <span data-ttu-id="73e78-126">-partitionCount</span><span class="sxs-lookup"><span data-stu-id="73e78-126">-partitionCount</span></span>
<span data-ttu-id="73e78-127">Eventhub PartitionCount</span><span class="sxs-lookup"><span data-stu-id="73e78-127">Eventhub PartitionCount</span></span>

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

### <span data-ttu-id="73e78-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73e78-128">-ResourceGroupName</span></span>
<span data-ttu-id="73e78-129">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="73e78-129">Resource Group Name</span></span>

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

### <span data-ttu-id="73e78-130">-確認</span><span class="sxs-lookup"><span data-stu-id="73e78-130">-Confirm</span></span>
<span data-ttu-id="73e78-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="73e78-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73e78-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73e78-132">-WhatIf</span></span>
<span data-ttu-id="73e78-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="73e78-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73e78-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="73e78-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73e78-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73e78-135">CommonParameters</span></span>
<span data-ttu-id="73e78-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="73e78-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73e78-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="73e78-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73e78-138">輸入</span><span class="sxs-lookup"><span data-stu-id="73e78-138">INPUTS</span></span>

### <span data-ttu-id="73e78-139">System.object</span><span class="sxs-lookup"><span data-stu-id="73e78-139">System.String</span></span>

### <span data-ttu-id="73e78-140">PSEventHubAttributes 的 [.]</span><span class="sxs-lookup"><span data-stu-id="73e78-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

### <span data-ttu-id="73e78-141">系統為 Nullable "1 [[System.object，mscorlib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="73e78-141">System.Nullable\`1[[System.Int64, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="73e78-142">輸出</span><span class="sxs-lookup"><span data-stu-id="73e78-142">OUTPUTS</span></span>

### <span data-ttu-id="73e78-143">PSEventHubAttributes 的 [.]</span><span class="sxs-lookup"><span data-stu-id="73e78-143">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="73e78-144">筆記</span><span class="sxs-lookup"><span data-stu-id="73e78-144">NOTES</span></span>

## <span data-ttu-id="73e78-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="73e78-145">RELATED LINKS</span></span>
