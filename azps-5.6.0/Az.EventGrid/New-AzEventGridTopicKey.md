---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/new-azeventgridtopickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopicKey.md
ms.openlocfilehash: aa59b4046a775c41dd3b44142d0a407c94ff1f4c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911977"
---
# <span data-ttu-id="76aa4-101">New-AzEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="76aa4-101">New-AzEventGridTopicKey</span></span>

## <span data-ttu-id="76aa4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="76aa4-102">SYNOPSIS</span></span>
<span data-ttu-id="76aa4-103">重新產生 Azure 事件格線主題的共用便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="76aa4-103">Regenerates the shared access key for an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="76aa4-104">語法</span><span class="sxs-lookup"><span data-stu-id="76aa4-104">SYNTAX</span></span>

### <span data-ttu-id="76aa4-105">TopicNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="76aa4-105">TopicNameParameterSet (Default)</span></span>
```
New-AzEventGridTopicKey [-ResourceGroupName] <String> [-TopicName] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76aa4-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="76aa4-106">TopicInputObjectParameterSet</span></span>
```
New-AzEventGridTopicKey [-KeyName] <String> [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76aa4-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="76aa4-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzEventGridTopicKey [-KeyName] <String> [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76aa4-108">描述</span><span class="sxs-lookup"><span data-stu-id="76aa4-108">DESCRIPTION</span></span>
<span data-ttu-id="76aa4-109">重新產生 Azure 事件格線主題的共用便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="76aa4-109">Regenerates the shared access key for an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="76aa4-110">例子</span><span class="sxs-lookup"><span data-stu-id="76aa4-110">EXAMPLES</span></span>

### <span data-ttu-id="76aa4-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="76aa4-111">Example 1</span></span>
```powershell
PS C:\> New-AzEventGridTopicKey -ResourceGroup MyResourceGroupName -TopicName Topic1 -KeyName key1
```

<span data-ttu-id="76aa4-112">在資源群組 \' \` \` \` MyResourceGroupName 中重新產生對應到 Event Grid 主題 Topic1 之 key key1'\ 的金鑰 \` 。</span><span class="sxs-lookup"><span data-stu-id="76aa4-112">Regenerate the key corresponding to key \'key1'\ of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="76aa4-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="76aa4-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | New-AzEventGridTopicKey -KeyName "key1"
```

<span data-ttu-id="76aa4-114">在資源群組 \' \` \` \` MyResourceGroupName 中重新產生對應到 Event Grid 主題 Topic1 之 key key1'\ 的金鑰 \` 。</span><span class="sxs-lookup"><span data-stu-id="76aa4-114">Regenerate the key corresponding to key \'key1'\ of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="76aa4-115">參數</span><span class="sxs-lookup"><span data-stu-id="76aa4-115">PARAMETERS</span></span>

### <span data-ttu-id="76aa4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76aa4-116">-DefaultProfile</span></span>
<span data-ttu-id="76aa4-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="76aa4-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="76aa4-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="76aa4-118">-InputObject</span></span>
<span data-ttu-id="76aa4-119">EventGrid Topic 物件。</span><span class="sxs-lookup"><span data-stu-id="76aa4-119">EventGrid Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: TopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76aa4-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="76aa4-120">-KeyName</span></span>
<span data-ttu-id="76aa4-121">需要重新產生之金鑰的名稱</span><span class="sxs-lookup"><span data-stu-id="76aa4-121">The name of the key that needs to be regenerated</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76aa4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76aa4-122">-ResourceGroupName</span></span>
<span data-ttu-id="76aa4-123">資源組名。</span><span class="sxs-lookup"><span data-stu-id="76aa4-123">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76aa4-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="76aa4-124">-ResourceId</span></span>
<span data-ttu-id="76aa4-125">代表事件格線主題的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="76aa4-125">Resource Identifier representing the Event Grid Topic.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76aa4-126">-TopicName</span><span class="sxs-lookup"><span data-stu-id="76aa4-126">-TopicName</span></span>
<span data-ttu-id="76aa4-127">主題的名稱。</span><span class="sxs-lookup"><span data-stu-id="76aa4-127">The name of the topic.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76aa4-128">-確認</span><span class="sxs-lookup"><span data-stu-id="76aa4-128">-Confirm</span></span>
<span data-ttu-id="76aa4-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="76aa4-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76aa4-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76aa4-130">-WhatIf</span></span>
<span data-ttu-id="76aa4-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="76aa4-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76aa4-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="76aa4-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76aa4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76aa4-133">CommonParameters</span></span>
<span data-ttu-id="76aa4-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="76aa4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76aa4-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="76aa4-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76aa4-136">輸入</span><span class="sxs-lookup"><span data-stu-id="76aa4-136">INPUTS</span></span>

### <span data-ttu-id="76aa4-137">System.String</span><span class="sxs-lookup"><span data-stu-id="76aa4-137">System.String</span></span>

### <span data-ttu-id="76aa4-138">Microsoft.Azure.Commands.EventGrid.models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="76aa4-138">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="76aa4-139">輸出</span><span class="sxs-lookup"><span data-stu-id="76aa4-139">OUTPUTS</span></span>

### <span data-ttu-id="76aa4-140">Microsoft.Azure.management.EventGrid.models.TopicSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="76aa4-140">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="76aa4-141">筆記</span><span class="sxs-lookup"><span data-stu-id="76aa4-141">NOTES</span></span>

## <span data-ttu-id="76aa4-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="76aa4-142">RELATED LINKS</span></span>
