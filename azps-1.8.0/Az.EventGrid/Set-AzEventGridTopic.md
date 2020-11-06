---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/set-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Set-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Set-AzEventGridTopic.md
ms.openlocfilehash: bcba056777cd9a5eef42799b170c2dad69c8bbf9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622309"
---
# <span data-ttu-id="c8a3c-101">Set-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="c8a3c-101">Set-AzEventGridTopic</span></span>

## <span data-ttu-id="c8a3c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c8a3c-102">SYNOPSIS</span></span>
<span data-ttu-id="c8a3c-103">設定事件格線主題的屬性。</span><span class="sxs-lookup"><span data-stu-id="c8a3c-103">Sets the properties of an Event Grid topic.</span></span>

## <span data-ttu-id="c8a3c-104">句法</span><span class="sxs-lookup"><span data-stu-id="c8a3c-104">SYNTAX</span></span>

### <span data-ttu-id="c8a3c-105">TopicNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c8a3c-105">TopicNameParameterSet (Default)</span></span>
```
Set-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8a3c-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8a3c-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Set-AzEventGridTopic [-ResourceId] <String> [-Tag] <Hashtable> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8a3c-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8a3c-107">TopicInputObjectParameterSet</span></span>
```
Set-AzEventGridTopic [-InputObject] <PSTopic> [-Tag] <Hashtable> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8a3c-108">說明</span><span class="sxs-lookup"><span data-stu-id="c8a3c-108">DESCRIPTION</span></span>
<span data-ttu-id="c8a3c-109">設定事件格線主題的屬性。</span><span class="sxs-lookup"><span data-stu-id="c8a3c-109">Sets the properties of an Event Grid topic.</span></span> <span data-ttu-id="c8a3c-110">這可以用來取代事件格線主題的標記。</span><span class="sxs-lookup"><span data-stu-id="c8a3c-110">This can be used to replace the tags of an Event Grid topic.</span></span>

## <span data-ttu-id="c8a3c-111">示例</span><span class="sxs-lookup"><span data-stu-id="c8a3c-111">EXAMPLES</span></span>

### <span data-ttu-id="c8a3c-112">範例1</span><span class="sxs-lookup"><span data-stu-id="c8a3c-112">Example 1</span></span>
```
PS C:\> Set-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="c8a3c-113">設定 [資源群組 MyResourceGroupName] 中 Topic1 事件格線主題的屬性 \` \` \` \` ，以使用指定的標記「部門」和「環境」取代標記。</span><span class="sxs-lookup"><span data-stu-id="c8a3c-113">Sets the properties of the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` to replace the tags with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="c8a3c-114">參數</span><span class="sxs-lookup"><span data-stu-id="c8a3c-114">PARAMETERS</span></span>

### <span data-ttu-id="c8a3c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8a3c-115">-DefaultProfile</span></span>
<span data-ttu-id="c8a3c-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="c8a3c-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c8a3c-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c8a3c-117">-InputObject</span></span>
<span data-ttu-id="c8a3c-118">EventGrid 主題物件。</span><span class="sxs-lookup"><span data-stu-id="c8a3c-118">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="c8a3c-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="c8a3c-119">-Name</span></span>
<span data-ttu-id="c8a3c-120">EventGrid 主題名稱。</span><span class="sxs-lookup"><span data-stu-id="c8a3c-120">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="c8a3c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8a3c-121">-ResourceGroupName</span></span>
<span data-ttu-id="c8a3c-122">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="c8a3c-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="c8a3c-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c8a3c-123">-ResourceId</span></span>
<span data-ttu-id="c8a3c-124">EventGrid 主題 ResourceID。</span><span class="sxs-lookup"><span data-stu-id="c8a3c-124">EventGrid Topic ResourceID.</span></span>

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

### <span data-ttu-id="c8a3c-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="c8a3c-125">-Tag</span></span>
<span data-ttu-id="c8a3c-126">代表資源標記的 Hashtables。</span><span class="sxs-lookup"><span data-stu-id="c8a3c-126">Hashtables which represents resource Tag.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Hashtable
Parameter Sets: TopicInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8a3c-127">-確認</span><span class="sxs-lookup"><span data-stu-id="c8a3c-127">-Confirm</span></span>
<span data-ttu-id="c8a3c-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c8a3c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8a3c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8a3c-129">-WhatIf</span></span>
<span data-ttu-id="c8a3c-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c8a3c-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8a3c-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c8a3c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8a3c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8a3c-132">CommonParameters</span></span>
<span data-ttu-id="c8a3c-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c8a3c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8a3c-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c8a3c-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8a3c-135">輸入</span><span class="sxs-lookup"><span data-stu-id="c8a3c-135">INPUTS</span></span>

### <span data-ttu-id="c8a3c-136">System.object</span><span class="sxs-lookup"><span data-stu-id="c8a3c-136">System.String</span></span>

### <span data-ttu-id="c8a3c-137">PSTopic 中的 EventGrid。</span><span class="sxs-lookup"><span data-stu-id="c8a3c-137">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="c8a3c-138">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="c8a3c-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="c8a3c-139">輸出</span><span class="sxs-lookup"><span data-stu-id="c8a3c-139">OUTPUTS</span></span>

### <span data-ttu-id="c8a3c-140">PSTopic 中的 EventGrid。</span><span class="sxs-lookup"><span data-stu-id="c8a3c-140">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="c8a3c-141">筆記</span><span class="sxs-lookup"><span data-stu-id="c8a3c-141">NOTES</span></span>

## <span data-ttu-id="c8a3c-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="c8a3c-142">RELATED LINKS</span></span>
