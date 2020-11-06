---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/set-azurermeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Set-AzureRmEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Set-AzureRmEventGridTopic.md
ms.openlocfilehash: c6a975ee5071ff3f31ae3daa0e6e9bf6ed9a42ba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448680"
---
# <span data-ttu-id="74fe6-101">Set-AzureRmEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="74fe6-101">Set-AzureRmEventGridTopic</span></span>

## <span data-ttu-id="74fe6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="74fe6-102">SYNOPSIS</span></span>
<span data-ttu-id="74fe6-103">設定事件格線主題的屬性。</span><span class="sxs-lookup"><span data-stu-id="74fe6-103">Sets the properties of an Event Grid topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="74fe6-104">句法</span><span class="sxs-lookup"><span data-stu-id="74fe6-104">SYNTAX</span></span>

### <span data-ttu-id="74fe6-105">TopicNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="74fe6-105">TopicNameParameterSet (Default)</span></span>
```
Set-AzureRmEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74fe6-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="74fe6-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Set-AzureRmEventGridTopic [-ResourceId] <String> [-Tag] <Hashtable> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74fe6-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="74fe6-107">TopicInputObjectParameterSet</span></span>
```
Set-AzureRmEventGridTopic [-InputObject] <PSTopic> [-Tag] <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74fe6-108">說明</span><span class="sxs-lookup"><span data-stu-id="74fe6-108">DESCRIPTION</span></span>
<span data-ttu-id="74fe6-109">設定事件格線主題的屬性。</span><span class="sxs-lookup"><span data-stu-id="74fe6-109">Sets the properties of an Event Grid topic.</span></span> <span data-ttu-id="74fe6-110">這可以用來取代事件格線主題的標記。</span><span class="sxs-lookup"><span data-stu-id="74fe6-110">This can be used to replace the tags of an Event Grid topic.</span></span>

## <span data-ttu-id="74fe6-111">示例</span><span class="sxs-lookup"><span data-stu-id="74fe6-111">EXAMPLES</span></span>

### <span data-ttu-id="74fe6-112">範例1</span><span class="sxs-lookup"><span data-stu-id="74fe6-112">Example 1</span></span>
```
PS C:\> Set-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="74fe6-113">設定 [資源群組 MyResourceGroupName] 中 Topic1 事件格線主題的屬性 \` \` \` \` ，以使用指定的標記「部門」和「環境」取代標記。</span><span class="sxs-lookup"><span data-stu-id="74fe6-113">Sets the properties of the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` to replace the tags with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="74fe6-114">參數</span><span class="sxs-lookup"><span data-stu-id="74fe6-114">PARAMETERS</span></span>

### <span data-ttu-id="74fe6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74fe6-115">-DefaultProfile</span></span>
<span data-ttu-id="74fe6-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="74fe6-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74fe6-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="74fe6-117">-InputObject</span></span>
<span data-ttu-id="74fe6-118">EventGrid 主題物件。</span><span class="sxs-lookup"><span data-stu-id="74fe6-118">EventGrid Topic object.</span></span>

```yaml
Type: PSTopic
Parameter Sets: TopicInputObjectParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="74fe6-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="74fe6-119">-Name</span></span>
<span data-ttu-id="74fe6-120">EventGrid 主題名稱。</span><span class="sxs-lookup"><span data-stu-id="74fe6-120">EventGrid Topic Name.</span></span>

```yaml
Type: String
Parameter Sets: TopicNameParameterSet
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74fe6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74fe6-121">-ResourceGroupName</span></span>
<span data-ttu-id="74fe6-122">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="74fe6-122">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74fe6-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="74fe6-123">-ResourceId</span></span>
<span data-ttu-id="74fe6-124">EventGrid 主題 ResourceID。</span><span class="sxs-lookup"><span data-stu-id="74fe6-124">EventGrid Topic ResourceID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74fe6-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="74fe6-125">-Tag</span></span>
<span data-ttu-id="74fe6-126">代表資源標記的 Hashtables。</span><span class="sxs-lookup"><span data-stu-id="74fe6-126">Hashtables which represents resource Tag.</span></span>

```yaml
Type: Hashtable
Parameter Sets: TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Hashtable
Parameter Sets: TopicInputObjectParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74fe6-127">-確認</span><span class="sxs-lookup"><span data-stu-id="74fe6-127">-Confirm</span></span>
<span data-ttu-id="74fe6-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="74fe6-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74fe6-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74fe6-129">-WhatIf</span></span>
<span data-ttu-id="74fe6-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="74fe6-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74fe6-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="74fe6-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74fe6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74fe6-132">CommonParameters</span></span>
<span data-ttu-id="74fe6-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="74fe6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74fe6-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="74fe6-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74fe6-135">輸入</span><span class="sxs-lookup"><span data-stu-id="74fe6-135">INPUTS</span></span>

### <span data-ttu-id="74fe6-136">System.object</span><span class="sxs-lookup"><span data-stu-id="74fe6-136">System.String</span></span>
<span data-ttu-id="74fe6-137">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="74fe6-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="74fe6-138">輸出</span><span class="sxs-lookup"><span data-stu-id="74fe6-138">OUTPUTS</span></span>

### <span data-ttu-id="74fe6-139">[EventGrid] 主題。</span><span class="sxs-lookup"><span data-stu-id="74fe6-139">Microsoft.Azure.Management.EventGrid.Models.Topic</span></span>

## <span data-ttu-id="74fe6-140">筆記</span><span class="sxs-lookup"><span data-stu-id="74fe6-140">NOTES</span></span>

## <span data-ttu-id="74fe6-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="74fe6-141">RELATED LINKS</span></span>

