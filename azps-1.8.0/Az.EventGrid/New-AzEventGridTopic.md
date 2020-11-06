---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopic.md
ms.openlocfilehash: 1922d399cf4b7c4fe1295f9a19409094ab5676c9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622315"
---
# <span data-ttu-id="9e95e-101">New-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="9e95e-101">New-AzEventGridTopic</span></span>

## <span data-ttu-id="9e95e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9e95e-102">SYNOPSIS</span></span>
<span data-ttu-id="9e95e-103">建立新的 Azure 事件格線主題。</span><span class="sxs-lookup"><span data-stu-id="9e95e-103">Creates a new Azure Event Grid Topic.</span></span>

## <span data-ttu-id="9e95e-104">句法</span><span class="sxs-lookup"><span data-stu-id="9e95e-104">SYNTAX</span></span>

```
New-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e95e-105">說明</span><span class="sxs-lookup"><span data-stu-id="9e95e-105">DESCRIPTION</span></span>
<span data-ttu-id="9e95e-106">建立新的 Azure 事件格線主題。</span><span class="sxs-lookup"><span data-stu-id="9e95e-106">Creates a new Azure Event Grid Topic.</span></span> <span data-ttu-id="9e95e-107">建立主題之後，應用程式就可以將事件發佈到主題端點。</span><span class="sxs-lookup"><span data-stu-id="9e95e-107">Once the topic is created, an application can publish events to the topic endpoint.</span></span>

## <span data-ttu-id="9e95e-108">示例</span><span class="sxs-lookup"><span data-stu-id="9e95e-108">EXAMPLES</span></span>

### <span data-ttu-id="9e95e-109">範例1</span><span class="sxs-lookup"><span data-stu-id="9e95e-109">Example 1</span></span>
```
PS C:\> New-AzEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1 -Location westus2
```

<span data-ttu-id="9e95e-110">\` \` \` \` 在 [資源群組] MyResourceGroupName 中，在指定的地理位置 Westus2 中 \` \` 建立事件格線主題 Topic1。</span><span class="sxs-lookup"><span data-stu-id="9e95e-110">Creates an Event Grid topic \`Topic1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="9e95e-111">範例2</span><span class="sxs-lookup"><span data-stu-id="9e95e-111">Example 2</span></span>
```
PS C:\> New-AzEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1 -Location westus2 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="9e95e-112">\` \` \` \` 在資源群組 MyResourceGroupName 中，以 \` 指定的標籤「 \` 部門」和「環境」建立事件格線主題 Topic1 在指定的地理位置 westus2 中。</span><span class="sxs-lookup"><span data-stu-id="9e95e-112">Creates an Event Grid topic \`Topic1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\` with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="9e95e-113">參數</span><span class="sxs-lookup"><span data-stu-id="9e95e-113">PARAMETERS</span></span>

### <span data-ttu-id="9e95e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e95e-114">-DefaultProfile</span></span>
<span data-ttu-id="9e95e-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="9e95e-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9e95e-116">-位置</span><span class="sxs-lookup"><span data-stu-id="9e95e-116">-Location</span></span>
<span data-ttu-id="9e95e-117">主題的位置</span><span class="sxs-lookup"><span data-stu-id="9e95e-117">The location of the topic</span></span>

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

### <span data-ttu-id="9e95e-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="9e95e-118">-Name</span></span>
<span data-ttu-id="9e95e-119">主題的名稱。</span><span class="sxs-lookup"><span data-stu-id="9e95e-119">The name of the topic.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e95e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e95e-120">-ResourceGroupName</span></span>
<span data-ttu-id="9e95e-121">應該在其中建立主題的資源群組。</span><span class="sxs-lookup"><span data-stu-id="9e95e-121">The resource group in which the topic should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e95e-122">-Tag</span><span class="sxs-lookup"><span data-stu-id="9e95e-122">-Tag</span></span>
<span data-ttu-id="9e95e-123">代表資源標記的 Hashtables。</span><span class="sxs-lookup"><span data-stu-id="9e95e-123">Hashtables which represents resource Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e95e-124">-確認</span><span class="sxs-lookup"><span data-stu-id="9e95e-124">-Confirm</span></span>
<span data-ttu-id="9e95e-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9e95e-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e95e-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e95e-126">-WhatIf</span></span>
<span data-ttu-id="9e95e-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9e95e-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e95e-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9e95e-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e95e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e95e-129">CommonParameters</span></span>
<span data-ttu-id="9e95e-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9e95e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e95e-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9e95e-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e95e-132">輸入</span><span class="sxs-lookup"><span data-stu-id="9e95e-132">INPUTS</span></span>

### <span data-ttu-id="9e95e-133">System.object</span><span class="sxs-lookup"><span data-stu-id="9e95e-133">System.String</span></span>

### <span data-ttu-id="9e95e-134">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="9e95e-134">System.Collections.Hashtable</span></span>

## <span data-ttu-id="9e95e-135">輸出</span><span class="sxs-lookup"><span data-stu-id="9e95e-135">OUTPUTS</span></span>

### <span data-ttu-id="9e95e-136">PSTopic 中的 EventGrid。</span><span class="sxs-lookup"><span data-stu-id="9e95e-136">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="9e95e-137">筆記</span><span class="sxs-lookup"><span data-stu-id="9e95e-137">NOTES</span></span>

## <span data-ttu-id="9e95e-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="9e95e-138">RELATED LINKS</span></span>
