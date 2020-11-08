---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/remove-azeventgriddomaintopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomainTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomainTopic.md
ms.openlocfilehash: 6f50f7e4224affb29584022ea8c61a4c0927a60d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94136435"
---
# <span data-ttu-id="1f5ea-101">Remove-AzEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="1f5ea-101">Remove-AzEventGridDomainTopic</span></span>

## <span data-ttu-id="1f5ea-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1f5ea-102">SYNOPSIS</span></span>
<span data-ttu-id="1f5ea-103">移除 Azure 事件 Grid 網域主題。</span><span class="sxs-lookup"><span data-stu-id="1f5ea-103">Removes an Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="1f5ea-104">句法</span><span class="sxs-lookup"><span data-stu-id="1f5ea-104">SYNTAX</span></span>

### <span data-ttu-id="1f5ea-105">DomainTopicNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="1f5ea-105">DomainTopicNameParameterSet (Default)</span></span>
```
Remove-AzEventGridDomainTopic [-ResourceGroupName] <String> [-DomainName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f5ea-106">ResourceIdDomainTopicParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f5ea-106">ResourceIdDomainTopicParameterSet</span></span>
```
Remove-AzEventGridDomainTopic [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f5ea-107">DomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f5ea-107">DomainTopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridDomainTopic [-InputObject] <PSDomainTopic> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f5ea-108">說明</span><span class="sxs-lookup"><span data-stu-id="1f5ea-108">DESCRIPTION</span></span>
<span data-ttu-id="1f5ea-109">移除 Azure 事件 Grid 網域主題。</span><span class="sxs-lookup"><span data-stu-id="1f5ea-109">Removes an Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="1f5ea-110">示例</span><span class="sxs-lookup"><span data-stu-id="1f5ea-110">EXAMPLES</span></span>

### <span data-ttu-id="1f5ea-111">範例1</span><span class="sxs-lookup"><span data-stu-id="1f5ea-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridDomainTopic -ResourceGroupName MyResourceGroupName -DomainName Domain1 -Name Topic1
```

<span data-ttu-id="1f5ea-112">移除 [ \` \` \` \` 資源群組 MyResourceGroupName] 中 [網域 Domain1 \` \` ] 底下的 [事件格線網域] 主題 Topic1。</span><span class="sxs-lookup"><span data-stu-id="1f5ea-112">Removes the Event Grid Domain Topic \`Topic1\` under Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="1f5ea-113">範例2</span><span class="sxs-lookup"><span data-stu-id="1f5ea-113">Example 2</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/Topic1" | Remove-AzEventGridDomainTopic
```

<span data-ttu-id="1f5ea-114">移除 [ \` \` \` \` 資源群組 MyResourceGroupName] 中 [網域 Domain1 \` \` ] 底下的 [事件格線網域] 主題 Topic1。</span><span class="sxs-lookup"><span data-stu-id="1f5ea-114">Removes the Event Grid Domain Topic \`Topic1\` under Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="1f5ea-115">參數</span><span class="sxs-lookup"><span data-stu-id="1f5ea-115">PARAMETERS</span></span>

### <span data-ttu-id="1f5ea-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f5ea-116">-DefaultProfile</span></span>
<span data-ttu-id="1f5ea-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1f5ea-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f5ea-118">-功能變數名稱</span><span class="sxs-lookup"><span data-stu-id="1f5ea-118">-DomainName</span></span>
<span data-ttu-id="1f5ea-119">EventGrid [功能變數名稱]。</span><span class="sxs-lookup"><span data-stu-id="1f5ea-119">EventGrid domain name.</span></span>

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

### <span data-ttu-id="1f5ea-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1f5ea-120">-InputObject</span></span>
<span data-ttu-id="1f5ea-121">EventGrid [網域] 主題物件。</span><span class="sxs-lookup"><span data-stu-id="1f5ea-121">EventGrid Domain Topic object.</span></span>

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

### <span data-ttu-id="1f5ea-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="1f5ea-122">-Name</span></span>
<span data-ttu-id="1f5ea-123">EventGrid [網域主題名稱]。</span><span class="sxs-lookup"><span data-stu-id="1f5ea-123">EventGrid domain topic name.</span></span>

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

### <span data-ttu-id="1f5ea-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1f5ea-124">-PassThru</span></span>
<span data-ttu-id="1f5ea-125">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="1f5ea-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="1f5ea-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f5ea-126">-ResourceGroupName</span></span>
<span data-ttu-id="1f5ea-127">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1f5ea-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="1f5ea-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1f5ea-128">-ResourceId</span></span>
<span data-ttu-id="1f5ea-129">代表事件 Grid 網域主題的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="1f5ea-129">Resource Identifier representing the Event Grid Domain Topic.</span></span>

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

### <span data-ttu-id="1f5ea-130">-確認</span><span class="sxs-lookup"><span data-stu-id="1f5ea-130">-Confirm</span></span>
<span data-ttu-id="1f5ea-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1f5ea-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f5ea-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f5ea-132">-WhatIf</span></span>
<span data-ttu-id="1f5ea-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1f5ea-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f5ea-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1f5ea-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f5ea-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f5ea-135">CommonParameters</span></span>
<span data-ttu-id="1f5ea-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1f5ea-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f5ea-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1f5ea-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f5ea-138">輸入</span><span class="sxs-lookup"><span data-stu-id="1f5ea-138">INPUTS</span></span>

### <span data-ttu-id="1f5ea-139">System.object</span><span class="sxs-lookup"><span data-stu-id="1f5ea-139">System.String</span></span>

### <span data-ttu-id="1f5ea-140">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="1f5ea-140">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

## <span data-ttu-id="1f5ea-141">輸出</span><span class="sxs-lookup"><span data-stu-id="1f5ea-141">OUTPUTS</span></span>

### <span data-ttu-id="1f5ea-142">System.object</span><span class="sxs-lookup"><span data-stu-id="1f5ea-142">System.Boolean</span></span>

## <span data-ttu-id="1f5ea-143">筆記</span><span class="sxs-lookup"><span data-stu-id="1f5ea-143">NOTES</span></span>

## <span data-ttu-id="1f5ea-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="1f5ea-144">RELATED LINKS</span></span>