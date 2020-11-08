---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgriddomainkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomainKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomainKey.md
ms.openlocfilehash: 6afb01ef46ba4f9c627f20a1c49ab58c2a79f252
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128729"
---
# <span data-ttu-id="68ddb-101">New-AzEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="68ddb-101">New-AzEventGridDomainKey</span></span>

## <span data-ttu-id="68ddb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="68ddb-102">SYNOPSIS</span></span>
<span data-ttu-id="68ddb-103">重新產生 Azure 事件 Grid 網域的共用便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="68ddb-103">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="68ddb-104">句法</span><span class="sxs-lookup"><span data-stu-id="68ddb-104">SYNTAX</span></span>

### <span data-ttu-id="68ddb-105">DomainNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="68ddb-105">DomainNameParameterSet (Default)</span></span>
```
New-AzEventGridDomainKey [-ResourceGroupName] <String> [-DomainName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68ddb-106">DomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="68ddb-106">DomainInputObjectParameterSet</span></span>
```
New-AzEventGridDomainKey [-Name] <String> [-DomainInputObject] <PSDomain>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68ddb-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="68ddb-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzEventGridDomainKey [-Name] <String> [-DomainResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68ddb-108">說明</span><span class="sxs-lookup"><span data-stu-id="68ddb-108">DESCRIPTION</span></span>
<span data-ttu-id="68ddb-109">重新產生 Azure 事件 Grid 網域的共用便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="68ddb-109">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="68ddb-110">示例</span><span class="sxs-lookup"><span data-stu-id="68ddb-110">EXAMPLES</span></span>

### <span data-ttu-id="68ddb-111">範例1</span><span class="sxs-lookup"><span data-stu-id="68ddb-111">Example 1</span></span>

<span data-ttu-id="68ddb-112">重新產生對應至 \' \` \` 資源群組 MyResourceGroupName 中的 key Key1 "\ 事件 Grid 網域 Domain1 \` ] 的索引鍵 \` 。</span><span class="sxs-lookup"><span data-stu-id="68ddb-112">Regenerate the key corresponding to key \'key1'\ of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> New-AzEventGridDomainKey -ResourceGroup MyResourceGroupName -DomainName Domain1 -Name key1

Key1                                         Key2
----                                         ----
<New Value for Key1>                        <Old Value for Key2>
```

### <span data-ttu-id="68ddb-113">範例2</span><span class="sxs-lookup"><span data-stu-id="68ddb-113">Example 2</span></span>

<span data-ttu-id="68ddb-114">重新產生對應至 \' \` \` 資源群組 MyResourceGroupName 中的 key Key1 "\ 事件 Grid 網域 Domain1 \` ] 的索引鍵 \` 。</span><span class="sxs-lookup"><span data-stu-id="68ddb-114">Regenerate the key corresponding to key \'key1'\ of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomain -ResourceGroup MyResourceGroupName -Name Domain1 | New-AzEventGridTopicKey -KeyName "key1"

Key1                                         Key2
----                                         ----
<New Value for Key1>                        <Old Value for Key2>
```

### <span data-ttu-id="68ddb-115">範例3</span><span class="sxs-lookup"><span data-stu-id="68ddb-115">Example 3</span></span>

<span data-ttu-id="68ddb-116">\' \` \` 在資源群組 MyResourceGroupName 中， \` \` 使用它的完整資源識別碼，重新產生對應至 key Key2 "\" 的事件 Grid 網域 Domain1 的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="68ddb-116">Regenerate the key corresponding to key \'key2'\ of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` using its full resource Id.</span></span>

```powershell
PS C:\> New-AzEventGridDomainKey -ResourceId /subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1 -KeyName Key2

Key1                                         Key2
----                                         ----
<Old Value for Key1>                        <New Value for Key2>
```

## <span data-ttu-id="68ddb-117">參數</span><span class="sxs-lookup"><span data-stu-id="68ddb-117">PARAMETERS</span></span>

### <span data-ttu-id="68ddb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68ddb-118">-DefaultProfile</span></span>
<span data-ttu-id="68ddb-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="68ddb-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68ddb-120">-DomainInputObject</span><span class="sxs-lookup"><span data-stu-id="68ddb-120">-DomainInputObject</span></span>
<span data-ttu-id="68ddb-121">EventGrid Domain 物件。</span><span class="sxs-lookup"><span data-stu-id="68ddb-121">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="68ddb-122">-功能變數名稱</span><span class="sxs-lookup"><span data-stu-id="68ddb-122">-DomainName</span></span>
<span data-ttu-id="68ddb-123">EventGrid [功能變數名稱]。</span><span class="sxs-lookup"><span data-stu-id="68ddb-123">EventGrid domain name.</span></span>

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

### <span data-ttu-id="68ddb-124">-DomainResourceId</span><span class="sxs-lookup"><span data-stu-id="68ddb-124">-DomainResourceId</span></span>
<span data-ttu-id="68ddb-125">代表事件網格網域的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="68ddb-125">Resource Identifier representing the Event Grid Domain.</span></span>

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

### <span data-ttu-id="68ddb-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="68ddb-126">-Name</span></span>
<span data-ttu-id="68ddb-127">需要再生之金鑰的名稱</span><span class="sxs-lookup"><span data-stu-id="68ddb-127">The name of the key that needs to be regenerated</span></span>

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

### <span data-ttu-id="68ddb-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68ddb-128">-ResourceGroupName</span></span>
<span data-ttu-id="68ddb-129">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="68ddb-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="68ddb-130">-確認</span><span class="sxs-lookup"><span data-stu-id="68ddb-130">-Confirm</span></span>
<span data-ttu-id="68ddb-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="68ddb-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68ddb-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68ddb-132">-WhatIf</span></span>
<span data-ttu-id="68ddb-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="68ddb-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68ddb-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="68ddb-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68ddb-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68ddb-135">CommonParameters</span></span>
<span data-ttu-id="68ddb-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="68ddb-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68ddb-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="68ddb-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68ddb-138">輸入</span><span class="sxs-lookup"><span data-stu-id="68ddb-138">INPUTS</span></span>

### <span data-ttu-id="68ddb-139">System.object</span><span class="sxs-lookup"><span data-stu-id="68ddb-139">System.String</span></span>

### <span data-ttu-id="68ddb-140">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="68ddb-140">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="68ddb-141">輸出</span><span class="sxs-lookup"><span data-stu-id="68ddb-141">OUTPUTS</span></span>

### <span data-ttu-id="68ddb-142">DomainSharedAccessKeys 中的 EventGrid。</span><span class="sxs-lookup"><span data-stu-id="68ddb-142">Microsoft.Azure.Management.EventGrid.Models.DomainSharedAccessKeys</span></span>

## <span data-ttu-id="68ddb-143">筆記</span><span class="sxs-lookup"><span data-stu-id="68ddb-143">NOTES</span></span>

## <span data-ttu-id="68ddb-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="68ddb-144">RELATED LINKS</span></span>