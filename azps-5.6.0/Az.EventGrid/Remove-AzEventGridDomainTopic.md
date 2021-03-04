---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/remove-azeventgriddomaintopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomainTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomainTopic.md
ms.openlocfilehash: 517044655ee1af7748906e2f9e9787c99813c6a8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911966"
---
# <span data-ttu-id="ce445-101">Remove-AzEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="ce445-101">Remove-AzEventGridDomainTopic</span></span>

## <span data-ttu-id="ce445-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ce445-102">SYNOPSIS</span></span>
<span data-ttu-id="ce445-103">移除 Azure 事件格線網域主題。</span><span class="sxs-lookup"><span data-stu-id="ce445-103">Removes an Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="ce445-104">語法</span><span class="sxs-lookup"><span data-stu-id="ce445-104">SYNTAX</span></span>

### <span data-ttu-id="ce445-105">DomainTopicNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="ce445-105">DomainTopicNameParameterSet (Default)</span></span>
```
Remove-AzEventGridDomainTopic [-ResourceGroupName] <String> [-DomainName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce445-106">ResourceIdDomainTopicParameterSet</span><span class="sxs-lookup"><span data-stu-id="ce445-106">ResourceIdDomainTopicParameterSet</span></span>
```
Remove-AzEventGridDomainTopic [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce445-107">DomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ce445-107">DomainTopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridDomainTopic [-InputObject] <PSDomainTopic> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce445-108">描述</span><span class="sxs-lookup"><span data-stu-id="ce445-108">DESCRIPTION</span></span>
<span data-ttu-id="ce445-109">移除 Azure 事件格線網域主題。</span><span class="sxs-lookup"><span data-stu-id="ce445-109">Removes an Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="ce445-110">例子</span><span class="sxs-lookup"><span data-stu-id="ce445-110">EXAMPLES</span></span>

### <span data-ttu-id="ce445-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="ce445-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridDomainTopic -ResourceGroupName MyResourceGroupName -DomainName Domain1 -Name Topic1
```

<span data-ttu-id="ce445-112">移除資源群組 \` \` MyResourceGroupName 中網域1 下的事件格線 \` \` \` 網域主題主題 \` 1。</span><span class="sxs-lookup"><span data-stu-id="ce445-112">Removes the Event Grid Domain Topic \`Topic1\` under Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="ce445-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="ce445-113">Example 2</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/Topic1" | Remove-AzEventGridDomainTopic
```

<span data-ttu-id="ce445-114">移除資源群組 \` \` MyResourceGroupName 中網域1 下的事件格線 \` \` \` 網域主題主題 \` 1。</span><span class="sxs-lookup"><span data-stu-id="ce445-114">Removes the Event Grid Domain Topic \`Topic1\` under Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="ce445-115">參數</span><span class="sxs-lookup"><span data-stu-id="ce445-115">PARAMETERS</span></span>

### <span data-ttu-id="ce445-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce445-116">-DefaultProfile</span></span>
<span data-ttu-id="ce445-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ce445-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce445-118">-DomainName</span><span class="sxs-lookup"><span data-stu-id="ce445-118">-DomainName</span></span>
<span data-ttu-id="ce445-119">EventGrid 功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="ce445-119">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce445-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ce445-120">-InputObject</span></span>
<span data-ttu-id="ce445-121">EventGrid 網域主題物件。</span><span class="sxs-lookup"><span data-stu-id="ce445-121">EventGrid Domain Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic
Parameter Sets: DomainTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce445-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="ce445-122">-Name</span></span>
<span data-ttu-id="ce445-123">EventGrid 網域主題名稱。</span><span class="sxs-lookup"><span data-stu-id="ce445-123">EventGrid domain topic name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases: DomainTopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce445-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ce445-124">-PassThru</span></span>
<span data-ttu-id="ce445-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="ce445-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="ce445-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce445-126">-ResourceGroupName</span></span>
<span data-ttu-id="ce445-127">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ce445-127">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce445-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ce445-128">-ResourceId</span></span>
<span data-ttu-id="ce445-129">代表事件格線網域主題的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="ce445-129">Resource Identifier representing the Event Grid Domain Topic.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdDomainTopicParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce445-130">-確認</span><span class="sxs-lookup"><span data-stu-id="ce445-130">-Confirm</span></span>
<span data-ttu-id="ce445-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ce445-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce445-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce445-132">-WhatIf</span></span>
<span data-ttu-id="ce445-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ce445-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce445-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ce445-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce445-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce445-135">CommonParameters</span></span>
<span data-ttu-id="ce445-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ce445-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce445-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ce445-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce445-138">輸入</span><span class="sxs-lookup"><span data-stu-id="ce445-138">INPUTS</span></span>

### <span data-ttu-id="ce445-139">System.String</span><span class="sxs-lookup"><span data-stu-id="ce445-139">System.String</span></span>

### <span data-ttu-id="ce445-140">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="ce445-140">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

## <span data-ttu-id="ce445-141">輸出</span><span class="sxs-lookup"><span data-stu-id="ce445-141">OUTPUTS</span></span>

### <span data-ttu-id="ce445-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ce445-142">System.Boolean</span></span>

## <span data-ttu-id="ce445-143">筆記</span><span class="sxs-lookup"><span data-stu-id="ce445-143">NOTES</span></span>

## <span data-ttu-id="ce445-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="ce445-144">RELATED LINKS</span></span>
