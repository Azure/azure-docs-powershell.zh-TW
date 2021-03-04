---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/remove-azeventgriddomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomain.md
ms.openlocfilehash: 703b01ef012f77126e0db3d425cd892fa7256317
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905102"
---
# <span data-ttu-id="d6bd8-101">Remove-AzEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="d6bd8-101">Remove-AzEventGridDomain</span></span>

## <span data-ttu-id="d6bd8-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d6bd8-102">SYNOPSIS</span></span>
<span data-ttu-id="d6bd8-103">移除 Azure 事件格線網域。</span><span class="sxs-lookup"><span data-stu-id="d6bd8-103">Removes an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="d6bd8-104">語法</span><span class="sxs-lookup"><span data-stu-id="d6bd8-104">SYNTAX</span></span>

### <span data-ttu-id="d6bd8-105">DomainNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="d6bd8-105">DomainNameParameterSet (Default)</span></span>
```
Remove-AzEventGridDomain [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6bd8-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6bd8-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridDomain [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6bd8-107">DomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6bd8-107">DomainInputObjectParameterSet</span></span>
```
Remove-AzEventGridDomain [-InputObject] <PSDomain> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6bd8-108">描述</span><span class="sxs-lookup"><span data-stu-id="d6bd8-108">DESCRIPTION</span></span>
<span data-ttu-id="d6bd8-109">移除 Azure 事件格線網域。</span><span class="sxs-lookup"><span data-stu-id="d6bd8-109">Removes an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="d6bd8-110">例子</span><span class="sxs-lookup"><span data-stu-id="d6bd8-110">EXAMPLES</span></span>

### <span data-ttu-id="d6bd8-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="d6bd8-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridDomain -ResourceGroupName MyResourceGroupName -Name Domain1
```

<span data-ttu-id="d6bd8-112">移除資源群組 \` \` \` MyResourceGroupName 中的事件格線網域 \` 1。</span><span class="sxs-lookup"><span data-stu-id="d6bd8-112">Removes the Event Grid Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="d6bd8-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="d6bd8-113">Example 2</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/Domains/Domain1" | Remove-AzEventGridDomain
```

<span data-ttu-id="d6bd8-114">移除資源群組 \` \` \` MyResourceGroupName 中的事件格線網域 \` 1。</span><span class="sxs-lookup"><span data-stu-id="d6bd8-114">Removes the Event Grid Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="d6bd8-115">參數</span><span class="sxs-lookup"><span data-stu-id="d6bd8-115">PARAMETERS</span></span>

### <span data-ttu-id="d6bd8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6bd8-116">-DefaultProfile</span></span>
<span data-ttu-id="d6bd8-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d6bd8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6bd8-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d6bd8-118">-InputObject</span></span>
<span data-ttu-id="d6bd8-119">EventGrid 網域物件。</span><span class="sxs-lookup"><span data-stu-id="d6bd8-119">EventGrid Domain object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomain
Parameter Sets: DomainInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6bd8-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="d6bd8-120">-Name</span></span>
<span data-ttu-id="d6bd8-121">EventGrid 功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="d6bd8-121">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: DomainName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6bd8-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d6bd8-122">-PassThru</span></span>
<span data-ttu-id="d6bd8-123">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="d6bd8-123">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="d6bd8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6bd8-124">-ResourceGroupName</span></span>
<span data-ttu-id="d6bd8-125">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d6bd8-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6bd8-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d6bd8-126">-ResourceId</span></span>
<span data-ttu-id="d6bd8-127">代表事件格線網域的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="d6bd8-127">Resource Identifier representing the Event Grid Domain.</span></span>

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

### <span data-ttu-id="d6bd8-128">-確認</span><span class="sxs-lookup"><span data-stu-id="d6bd8-128">-Confirm</span></span>
<span data-ttu-id="d6bd8-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="d6bd8-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6bd8-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6bd8-130">-WhatIf</span></span>
<span data-ttu-id="d6bd8-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d6bd8-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6bd8-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d6bd8-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6bd8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6bd8-133">CommonParameters</span></span>
<span data-ttu-id="d6bd8-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d6bd8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6bd8-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d6bd8-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6bd8-136">輸入</span><span class="sxs-lookup"><span data-stu-id="d6bd8-136">INPUTS</span></span>

### <span data-ttu-id="d6bd8-137">System.String</span><span class="sxs-lookup"><span data-stu-id="d6bd8-137">System.String</span></span>

### <span data-ttu-id="d6bd8-138">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="d6bd8-138">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="d6bd8-139">輸出</span><span class="sxs-lookup"><span data-stu-id="d6bd8-139">OUTPUTS</span></span>

### <span data-ttu-id="d6bd8-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d6bd8-140">System.Boolean</span></span>

## <span data-ttu-id="d6bd8-141">筆記</span><span class="sxs-lookup"><span data-stu-id="d6bd8-141">NOTES</span></span>

## <span data-ttu-id="d6bd8-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="d6bd8-142">RELATED LINKS</span></span>
