---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgridtopickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopicKey.md
ms.openlocfilehash: ab9c9401b0f8d929be1a4aa244f407957d886e4c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129535"
---
# <span data-ttu-id="c542d-101">New-AzEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="c542d-101">New-AzEventGridTopicKey</span></span>

## <span data-ttu-id="c542d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c542d-102">SYNOPSIS</span></span>
<span data-ttu-id="c542d-103">再生 Azure 事件格線主題的共用便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="c542d-103">Regenerates the shared access key for an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="c542d-104">句法</span><span class="sxs-lookup"><span data-stu-id="c542d-104">SYNTAX</span></span>

### <span data-ttu-id="c542d-105">TopicNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c542d-105">TopicNameParameterSet (Default)</span></span>
```
New-AzEventGridTopicKey [-ResourceGroupName] <String> [-TopicName] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c542d-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c542d-106">TopicInputObjectParameterSet</span></span>
```
New-AzEventGridTopicKey [-KeyName] <String> [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c542d-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="c542d-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzEventGridTopicKey [-KeyName] <String> [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c542d-108">說明</span><span class="sxs-lookup"><span data-stu-id="c542d-108">DESCRIPTION</span></span>
<span data-ttu-id="c542d-109">再生 Azure 事件格線主題的共用便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="c542d-109">Regenerates the shared access key for an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="c542d-110">示例</span><span class="sxs-lookup"><span data-stu-id="c542d-110">EXAMPLES</span></span>

### <span data-ttu-id="c542d-111">範例1</span><span class="sxs-lookup"><span data-stu-id="c542d-111">Example 1</span></span>
```powershell
PS C:\> New-AzEventGridTopicKey -ResourceGroup MyResourceGroupName -TopicName Topic1 -KeyName key1
```

<span data-ttu-id="c542d-112">針對 \' \` \` 資源群組 MyResourceGroupName 中的 key Key1 "\ 事件格線主題 Topic1，重新產生對應的金鑰 \` \` 。</span><span class="sxs-lookup"><span data-stu-id="c542d-112">Regenerate the key corresponding to key \'key1'\ of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="c542d-113">範例2</span><span class="sxs-lookup"><span data-stu-id="c542d-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | New-AzEventGridTopicKey -KeyName "key1"
```

<span data-ttu-id="c542d-114">針對 \' \` \` 資源群組 MyResourceGroupName 中的 key Key1 "\ 事件格線主題 Topic1，重新產生對應的金鑰 \` \` 。</span><span class="sxs-lookup"><span data-stu-id="c542d-114">Regenerate the key corresponding to key \'key1'\ of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="c542d-115">參數</span><span class="sxs-lookup"><span data-stu-id="c542d-115">PARAMETERS</span></span>

### <span data-ttu-id="c542d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c542d-116">-DefaultProfile</span></span>
<span data-ttu-id="c542d-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="c542d-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c542d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c542d-118">-InputObject</span></span>
<span data-ttu-id="c542d-119">EventGrid 主題物件。</span><span class="sxs-lookup"><span data-stu-id="c542d-119">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="c542d-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="c542d-120">-KeyName</span></span>
<span data-ttu-id="c542d-121">需要再生之金鑰的名稱</span><span class="sxs-lookup"><span data-stu-id="c542d-121">The name of the key that needs to be regenerated</span></span>

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

### <span data-ttu-id="c542d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c542d-122">-ResourceGroupName</span></span>
<span data-ttu-id="c542d-123">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="c542d-123">Resource group name.</span></span>

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

### <span data-ttu-id="c542d-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c542d-124">-ResourceId</span></span>
<span data-ttu-id="c542d-125">代表事件格線主題的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="c542d-125">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="c542d-126">-TopicName</span><span class="sxs-lookup"><span data-stu-id="c542d-126">-TopicName</span></span>
<span data-ttu-id="c542d-127">主題的名稱。</span><span class="sxs-lookup"><span data-stu-id="c542d-127">The name of the topic.</span></span>

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

### <span data-ttu-id="c542d-128">-確認</span><span class="sxs-lookup"><span data-stu-id="c542d-128">-Confirm</span></span>
<span data-ttu-id="c542d-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c542d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c542d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c542d-130">-WhatIf</span></span>
<span data-ttu-id="c542d-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c542d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c542d-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c542d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c542d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c542d-133">CommonParameters</span></span>
<span data-ttu-id="c542d-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c542d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c542d-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c542d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c542d-136">輸入</span><span class="sxs-lookup"><span data-stu-id="c542d-136">INPUTS</span></span>

### <span data-ttu-id="c542d-137">System.object</span><span class="sxs-lookup"><span data-stu-id="c542d-137">System.String</span></span>

### <span data-ttu-id="c542d-138">PSTopic 中的 EventGrid。</span><span class="sxs-lookup"><span data-stu-id="c542d-138">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="c542d-139">輸出</span><span class="sxs-lookup"><span data-stu-id="c542d-139">OUTPUTS</span></span>

### <span data-ttu-id="c542d-140">TopicSharedAccessKeys 中的 EventGrid。</span><span class="sxs-lookup"><span data-stu-id="c542d-140">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="c542d-141">筆記</span><span class="sxs-lookup"><span data-stu-id="c542d-141">NOTES</span></span>

## <span data-ttu-id="c542d-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="c542d-142">RELATED LINKS</span></span>
