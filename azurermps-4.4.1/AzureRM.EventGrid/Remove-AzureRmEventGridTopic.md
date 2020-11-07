---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Remove-AzureRmEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Remove-AzureRmEventGridTopic.md
ms.openlocfilehash: aecbc105a87cc058567cb0ff35f0bb0e8cc84c7a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626306"
---
# <span data-ttu-id="903c8-101">Remove-AzureRmEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="903c8-101">Remove-AzureRmEventGridTopic</span></span>

## <span data-ttu-id="903c8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="903c8-102">SYNOPSIS</span></span>
<span data-ttu-id="903c8-103">移除 Azure 事件格線主題。</span><span class="sxs-lookup"><span data-stu-id="903c8-103">Removes an Azure Event Grid Topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="903c8-104">句法</span><span class="sxs-lookup"><span data-stu-id="903c8-104">SYNTAX</span></span>

### <span data-ttu-id="903c8-105">TopicNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="903c8-105">TopicNameParameterSet (Default)</span></span>
```
Remove-AzureRmEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="903c8-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="903c8-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzureRmEventGridTopic [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="903c8-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="903c8-107">TopicInputObjectParameterSet</span></span>
```
Remove-AzureRmEventGridTopic [-InputObject] <PSTopic> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="903c8-108">說明</span><span class="sxs-lookup"><span data-stu-id="903c8-108">DESCRIPTION</span></span>
<span data-ttu-id="903c8-109">移除 Azure 事件格線主題。</span><span class="sxs-lookup"><span data-stu-id="903c8-109">Removes an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="903c8-110">示例</span><span class="sxs-lookup"><span data-stu-id="903c8-110">EXAMPLES</span></span>

### <span data-ttu-id="903c8-111">範例1</span><span class="sxs-lookup"><span data-stu-id="903c8-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1
```

<span data-ttu-id="903c8-112">移除 [ \` \` 資源] 群組 MyResourceGroupName 中的事件格線主題 Topic1 \` \` 。</span><span class="sxs-lookup"><span data-stu-id="903c8-112">Removes the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="903c8-113">範例2</span><span class="sxs-lookup"><span data-stu-id="903c8-113">Example 2</span></span>
```
PS C:\> Get-AzureRmResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1" | Remove-AzureRmEventGridTopic
```

<span data-ttu-id="903c8-114">移除 [ \` \` 資源] 群組 MyResourceGroupName 中的事件格線主題 Topic1 \` \` 。</span><span class="sxs-lookup"><span data-stu-id="903c8-114">Removes the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="903c8-115">參數</span><span class="sxs-lookup"><span data-stu-id="903c8-115">PARAMETERS</span></span>

### <span data-ttu-id="903c8-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="903c8-116">-InputObject</span></span>
<span data-ttu-id="903c8-117">EventGrid 主題物件。</span><span class="sxs-lookup"><span data-stu-id="903c8-117">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="903c8-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="903c8-118">-Name</span></span>
<span data-ttu-id="903c8-119">EventGrid 主題名稱。</span><span class="sxs-lookup"><span data-stu-id="903c8-119">EventGrid Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="903c8-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="903c8-120">-PassThru</span></span>
<span data-ttu-id="903c8-121">傳回移除操作的狀態。</span><span class="sxs-lookup"><span data-stu-id="903c8-121">Returns the status of the Remove operation.</span></span> <span data-ttu-id="903c8-122">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="903c8-122">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="903c8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="903c8-123">-ResourceGroupName</span></span>
<span data-ttu-id="903c8-124">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="903c8-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="903c8-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="903c8-125">-ResourceId</span></span>
<span data-ttu-id="903c8-126">EventGrid 主題 ResourceID。</span><span class="sxs-lookup"><span data-stu-id="903c8-126">EventGrid Topic ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="903c8-127">-確認</span><span class="sxs-lookup"><span data-stu-id="903c8-127">-Confirm</span></span>
<span data-ttu-id="903c8-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="903c8-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="903c8-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="903c8-129">-WhatIf</span></span>
<span data-ttu-id="903c8-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="903c8-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="903c8-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="903c8-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="903c8-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="903c8-132">-DefaultProfile</span></span>
<span data-ttu-id="903c8-133">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="903c8-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="903c8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="903c8-134">CommonParameters</span></span>
<span data-ttu-id="903c8-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="903c8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="903c8-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="903c8-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="903c8-137">輸入</span><span class="sxs-lookup"><span data-stu-id="903c8-137">INPUTS</span></span>

### <span data-ttu-id="903c8-138">System.object</span><span class="sxs-lookup"><span data-stu-id="903c8-138">System.String</span></span>
<span data-ttu-id="903c8-139">PSTopic 中的 EventGrid。</span><span class="sxs-lookup"><span data-stu-id="903c8-139">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="903c8-140">輸出</span><span class="sxs-lookup"><span data-stu-id="903c8-140">OUTPUTS</span></span>

### <span data-ttu-id="903c8-141">System.object</span><span class="sxs-lookup"><span data-stu-id="903c8-141">System.Object</span></span>

## <span data-ttu-id="903c8-142">筆記</span><span class="sxs-lookup"><span data-stu-id="903c8-142">NOTES</span></span>

## <span data-ttu-id="903c8-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="903c8-143">RELATED LINKS</span></span>

