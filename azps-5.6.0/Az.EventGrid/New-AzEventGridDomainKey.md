---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/new-azeventgriddomainkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomainKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomainKey.md
ms.openlocfilehash: 297abcdf06d1efbe5cf7e39e310d2c2d422a6324
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911986"
---
# <span data-ttu-id="07984-101">New-AzEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="07984-101">New-AzEventGridDomainKey</span></span>

## <span data-ttu-id="07984-102">簡介</span><span class="sxs-lookup"><span data-stu-id="07984-102">SYNOPSIS</span></span>
<span data-ttu-id="07984-103">重新產生 Azure 事件格線網域的共用便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="07984-103">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="07984-104">語法</span><span class="sxs-lookup"><span data-stu-id="07984-104">SYNTAX</span></span>

### <span data-ttu-id="07984-105">DomainNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="07984-105">DomainNameParameterSet (Default)</span></span>
```
New-AzEventGridDomainKey [-ResourceGroupName] <String> [-DomainName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07984-106">DomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="07984-106">DomainInputObjectParameterSet</span></span>
```
New-AzEventGridDomainKey [-Name] <String> [-DomainInputObject] <PSDomain>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07984-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="07984-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzEventGridDomainKey [-Name] <String> [-DomainResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07984-108">描述</span><span class="sxs-lookup"><span data-stu-id="07984-108">DESCRIPTION</span></span>
<span data-ttu-id="07984-109">重新產生 Azure 事件格線網域的共用便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="07984-109">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="07984-110">例子</span><span class="sxs-lookup"><span data-stu-id="07984-110">EXAMPLES</span></span>

### <span data-ttu-id="07984-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="07984-111">Example 1</span></span>

<span data-ttu-id="07984-112">在資源群組 \' \` \` \` MyResourceGroupName 中重新產生對應到 Event Grid 網域網域 1 之 key key1'\ 的金鑰 \` 。</span><span class="sxs-lookup"><span data-stu-id="07984-112">Regenerate the key corresponding to key \'key1'\ of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> New-AzEventGridDomainKey -ResourceGroup MyResourceGroupName -DomainName Domain1 -Name key1

Key1                                         Key2
----                                         ----
<New Value for Key1>                        <Old Value for Key2>
```

### <span data-ttu-id="07984-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="07984-113">Example 2</span></span>

<span data-ttu-id="07984-114">在資源群組 \' \` \` \` MyResourceGroupName 中重新產生對應到 Event Grid 網域網域 1 之 key key1'\ 的金鑰 \` 。</span><span class="sxs-lookup"><span data-stu-id="07984-114">Regenerate the key corresponding to key \'key1'\ of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomain -ResourceGroup MyResourceGroupName -Name Domain1 | New-AzEventGridTopicKey -KeyName "key1"

Key1                                         Key2
----                                         ----
<New Value for Key1>                        <Old Value for Key2>
```

### <span data-ttu-id="07984-115">範例 3</span><span class="sxs-lookup"><span data-stu-id="07984-115">Example 3</span></span>

<span data-ttu-id="07984-116">使用資源群組 \' \` \` \` MyResourceGroupName 的完整資源識別碼，重新產生對應至 Event Grid 網域網域1 key key2'\ 的 \` 金鑰。</span><span class="sxs-lookup"><span data-stu-id="07984-116">Regenerate the key corresponding to key \'key2'\ of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` using its full resource Id.</span></span>

```powershell
PS C:\> New-AzEventGridDomainKey -ResourceId /subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1 -KeyName Key2

Key1                                         Key2
----                                         ----
<Old Value for Key1>                        <New Value for Key2>
```

## <span data-ttu-id="07984-117">參數</span><span class="sxs-lookup"><span data-stu-id="07984-117">PARAMETERS</span></span>

### <span data-ttu-id="07984-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07984-118">-DefaultProfile</span></span>
<span data-ttu-id="07984-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="07984-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07984-120">-DomainInputObject</span><span class="sxs-lookup"><span data-stu-id="07984-120">-DomainInputObject</span></span>
<span data-ttu-id="07984-121">EventGrid 網域物件。</span><span class="sxs-lookup"><span data-stu-id="07984-121">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="07984-122">-DomainName</span><span class="sxs-lookup"><span data-stu-id="07984-122">-DomainName</span></span>
<span data-ttu-id="07984-123">EventGrid 功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="07984-123">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07984-124">-DomainResourceId</span><span class="sxs-lookup"><span data-stu-id="07984-124">-DomainResourceId</span></span>
<span data-ttu-id="07984-125">代表事件格線網域的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="07984-125">Resource Identifier representing the Event Grid Domain.</span></span>

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

### <span data-ttu-id="07984-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="07984-126">-Name</span></span>
<span data-ttu-id="07984-127">需要重新產生之金鑰的名稱</span><span class="sxs-lookup"><span data-stu-id="07984-127">The name of the key that needs to be regenerated</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07984-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07984-128">-ResourceGroupName</span></span>
<span data-ttu-id="07984-129">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="07984-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="07984-130">-確認</span><span class="sxs-lookup"><span data-stu-id="07984-130">-Confirm</span></span>
<span data-ttu-id="07984-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="07984-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07984-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07984-132">-WhatIf</span></span>
<span data-ttu-id="07984-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="07984-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07984-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="07984-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07984-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07984-135">CommonParameters</span></span>
<span data-ttu-id="07984-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="07984-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07984-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="07984-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07984-138">輸入</span><span class="sxs-lookup"><span data-stu-id="07984-138">INPUTS</span></span>

### <span data-ttu-id="07984-139">System.String</span><span class="sxs-lookup"><span data-stu-id="07984-139">System.String</span></span>

### <span data-ttu-id="07984-140">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="07984-140">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="07984-141">輸出</span><span class="sxs-lookup"><span data-stu-id="07984-141">OUTPUTS</span></span>

### <span data-ttu-id="07984-142">Microsoft.Azure.management.EventGrid.models.DomainSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="07984-142">Microsoft.Azure.Management.EventGrid.Models.DomainSharedAccessKeys</span></span>

## <span data-ttu-id="07984-143">筆記</span><span class="sxs-lookup"><span data-stu-id="07984-143">NOTES</span></span>

## <span data-ttu-id="07984-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="07984-144">RELATED LINKS</span></span>
