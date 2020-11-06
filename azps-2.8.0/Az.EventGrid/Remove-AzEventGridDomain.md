---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/remove-azeventgriddomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomain.md
ms.openlocfilehash: b46c9be4c8731fa6b9082a8076dd9ae175e62422
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612458"
---
# <span data-ttu-id="4fb39-101">Remove-AzEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="4fb39-101">Remove-AzEventGridDomain</span></span>

## <span data-ttu-id="4fb39-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4fb39-102">SYNOPSIS</span></span>
<span data-ttu-id="4fb39-103">移除 Azure 事件格線網域。</span><span class="sxs-lookup"><span data-stu-id="4fb39-103">Removes an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="4fb39-104">句法</span><span class="sxs-lookup"><span data-stu-id="4fb39-104">SYNTAX</span></span>

### <span data-ttu-id="4fb39-105">DomainNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="4fb39-105">DomainNameParameterSet (Default)</span></span>
```
Remove-AzEventGridDomain [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4fb39-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="4fb39-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridDomain [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4fb39-107">DomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4fb39-107">DomainInputObjectParameterSet</span></span>
```
Remove-AzEventGridDomain [-InputObject] <PSDomain> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4fb39-108">說明</span><span class="sxs-lookup"><span data-stu-id="4fb39-108">DESCRIPTION</span></span>
<span data-ttu-id="4fb39-109">移除 Azure 事件格線網域。</span><span class="sxs-lookup"><span data-stu-id="4fb39-109">Removes an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="4fb39-110">示例</span><span class="sxs-lookup"><span data-stu-id="4fb39-110">EXAMPLES</span></span>

### <span data-ttu-id="4fb39-111">範例1</span><span class="sxs-lookup"><span data-stu-id="4fb39-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridDomain -ResourceGroupName MyResourceGroupName -Name Domain1
```

<span data-ttu-id="4fb39-112">移除 [ \` \` 資源群組 MyResourceGroupName] 中的事件網格網域 Domain1 \` \` 。</span><span class="sxs-lookup"><span data-stu-id="4fb39-112">Removes the Event Grid Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="4fb39-113">範例2</span><span class="sxs-lookup"><span data-stu-id="4fb39-113">Example 2</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/Domains/Domain1" | Remove-AzEventGridDomain
```

<span data-ttu-id="4fb39-114">移除 [ \` \` 資源群組 MyResourceGroupName] 中的事件網格網域 Domain1 \` \` 。</span><span class="sxs-lookup"><span data-stu-id="4fb39-114">Removes the Event Grid Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="4fb39-115">參數</span><span class="sxs-lookup"><span data-stu-id="4fb39-115">PARAMETERS</span></span>

### <span data-ttu-id="4fb39-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fb39-116">-DefaultProfile</span></span>
<span data-ttu-id="4fb39-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4fb39-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4fb39-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4fb39-118">-InputObject</span></span>
<span data-ttu-id="4fb39-119">EventGrid Domain 物件。</span><span class="sxs-lookup"><span data-stu-id="4fb39-119">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="4fb39-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="4fb39-120">-Name</span></span>
<span data-ttu-id="4fb39-121">EventGrid [功能變數名稱]。</span><span class="sxs-lookup"><span data-stu-id="4fb39-121">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: DomainName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fb39-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4fb39-122">-PassThru</span></span>
<span data-ttu-id="4fb39-123">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="4fb39-123">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="4fb39-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fb39-124">-ResourceGroupName</span></span>
<span data-ttu-id="4fb39-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4fb39-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fb39-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4fb39-126">-ResourceId</span></span>
<span data-ttu-id="4fb39-127">代表事件網格網域的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="4fb39-127">Resource Identifier representing the Event Grid Domain.</span></span>

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

### <span data-ttu-id="4fb39-128">-確認</span><span class="sxs-lookup"><span data-stu-id="4fb39-128">-Confirm</span></span>
<span data-ttu-id="4fb39-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4fb39-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4fb39-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fb39-130">-WhatIf</span></span>
<span data-ttu-id="4fb39-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4fb39-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4fb39-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4fb39-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4fb39-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fb39-133">CommonParameters</span></span>
<span data-ttu-id="4fb39-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4fb39-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fb39-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4fb39-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fb39-136">輸入</span><span class="sxs-lookup"><span data-stu-id="4fb39-136">INPUTS</span></span>

### <span data-ttu-id="4fb39-137">System.object</span><span class="sxs-lookup"><span data-stu-id="4fb39-137">System.String</span></span>

### <span data-ttu-id="4fb39-138">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="4fb39-138">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="4fb39-139">輸出</span><span class="sxs-lookup"><span data-stu-id="4fb39-139">OUTPUTS</span></span>

### <span data-ttu-id="4fb39-140">System.object</span><span class="sxs-lookup"><span data-stu-id="4fb39-140">System.Boolean</span></span>

## <span data-ttu-id="4fb39-141">筆記</span><span class="sxs-lookup"><span data-stu-id="4fb39-141">NOTES</span></span>

## <span data-ttu-id="4fb39-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="4fb39-142">RELATED LINKS</span></span>
