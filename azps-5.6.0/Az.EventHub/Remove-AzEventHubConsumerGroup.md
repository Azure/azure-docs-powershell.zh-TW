---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/remove-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubConsumerGroup.md
ms.openlocfilehash: 8f5f1ae36355f1f8d76476e5eee69f63187847ec
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912397"
---
# <span data-ttu-id="22ab7-101">Remove-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="22ab7-101">Remove-AzEventHubConsumerGroup</span></span>

## <span data-ttu-id="22ab7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="22ab7-102">SYNOPSIS</span></span>
<span data-ttu-id="22ab7-103">刪除指定的事件中樞消費者群組。</span><span class="sxs-lookup"><span data-stu-id="22ab7-103">Deletes the specified Event Hubs consumer group.</span></span>

## <span data-ttu-id="22ab7-104">語法</span><span class="sxs-lookup"><span data-stu-id="22ab7-104">SYNTAX</span></span>

### <span data-ttu-id="22ab7-105">ConsumergroupPropertiesSet (預設) </span><span class="sxs-lookup"><span data-stu-id="22ab7-105">ConsumergroupPropertiesSet (Default)</span></span>
```
Remove-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="22ab7-106">ConsumergroupInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="22ab7-106">ConsumergroupInputObjectSet</span></span>
```
Remove-AzEventHubConsumerGroup [-InputObject] <PSConsumerGroupAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22ab7-107">ConsumergroupResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="22ab7-107">ConsumergroupResourceIdParameterSet</span></span>
```
Remove-AzEventHubConsumerGroup [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22ab7-108">描述</span><span class="sxs-lookup"><span data-stu-id="22ab7-108">DESCRIPTION</span></span>
<span data-ttu-id="22ab7-109">Cmdlet Remove-AzEventHubConsumerGroup會從指定的事件中樞移除並刪除指定的消費者群組。</span><span class="sxs-lookup"><span data-stu-id="22ab7-109">The Remove-AzEventHubConsumerGroup cmdlet removes and deletes the specified consumer group from the given Event Hub.</span></span>

## <span data-ttu-id="22ab7-110">例子</span><span class="sxs-lookup"><span data-stu-id="22ab7-110">EXAMPLES</span></span>

### <span data-ttu-id="22ab7-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="22ab7-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyConsumerGroupName
```

<span data-ttu-id="22ab7-112">從事件中樞 \` MyEventHubName 刪除消費者群組 MyConsumerGroupName ，此名稱範圍為 \` \` \` \` MyNamespaceName \` 命名空間。</span><span class="sxs-lookup"><span data-stu-id="22ab7-112">Deletes the consumer group \`MyConsumerGroupName\` from the Event Hub \`MyEventHubName\`, scoped to the \`MyNamespaceName\` namespace.</span></span>

### <span data-ttu-id="22ab7-113">範例 2：InputObject - Using Variable</span><span class="sxs-lookup"><span data-stu-id="22ab7-113">Example 2: InputObject - Using Variable</span></span>
```powershell
PS C:\> $inputobject = Get-AzEventHubConsumerGroup <params>
PS C:\> Remove-AzEventHubConsumerGroup -InputObject $inputobject
```

### <span data-ttu-id="22ab7-114">範例 3：InputObject - 使用管道</span><span class="sxs-lookup"><span data-stu-id="22ab7-114">Example 3: InputObject - Using Piping</span></span>
```powershell
PS C:\> Get-AzEventHubConsumerGroup <params> | Remove-AzEventHubConsumerGroup
```

### <span data-ttu-id="22ab7-115">範例 4：ResourceId Using Variable</span><span class="sxs-lookup"><span data-stu-id="22ab7-115">Example 4: ResourceId Using Variable</span></span>
```powershell
PS C:\> $resourceid = Get-AzEventHubConsumerGroup <params>
PS C:\> Remove-AzEventHubConsumerGroup -ResourceId $resourceid.Id
```

### <span data-ttu-id="22ab7-116">範例 5：ResourceId Using 字串</span><span class="sxs-lookup"><span data-stu-id="22ab7-116">Example 5: ResourceId Using string</span></span>
```powershell
PS C:\> Remove-AzEventHubConsumerGroup -ResourceId "/subscriptions/xxx-xxxx-xxxxx-xxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName/eventhubs/EventHubName/consumergroups/ConsumerGroupName"
```

## <span data-ttu-id="22ab7-117">參數</span><span class="sxs-lookup"><span data-stu-id="22ab7-117">PARAMETERS</span></span>

### <span data-ttu-id="22ab7-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="22ab7-118">-AsJob</span></span>
<span data-ttu-id="22ab7-119">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="22ab7-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="22ab7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22ab7-120">-DefaultProfile</span></span>
<span data-ttu-id="22ab7-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="22ab7-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22ab7-122">-EventHub</span><span class="sxs-lookup"><span data-stu-id="22ab7-122">-EventHub</span></span>
<span data-ttu-id="22ab7-123">EventHub 名稱</span><span class="sxs-lookup"><span data-stu-id="22ab7-123">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: ConsumergroupPropertiesSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22ab7-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="22ab7-124">-InputObject</span></span>
<span data-ttu-id="22ab7-125">ConsumerGroup 物件</span><span class="sxs-lookup"><span data-stu-id="22ab7-125">ConsumerGroup Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes
Parameter Sets: ConsumergroupInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="22ab7-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="22ab7-126">-Name</span></span>
<span data-ttu-id="22ab7-127">ConsumerGroup 名稱</span><span class="sxs-lookup"><span data-stu-id="22ab7-127">ConsumerGroup Name</span></span>

```yaml
Type: System.String
Parameter Sets: ConsumergroupPropertiesSet
Aliases: ConsumerGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22ab7-128">-命名空間</span><span class="sxs-lookup"><span data-stu-id="22ab7-128">-Namespace</span></span>
<span data-ttu-id="22ab7-129">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="22ab7-129">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: ConsumergroupPropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22ab7-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="22ab7-130">-PassThru</span></span>
<span data-ttu-id="22ab7-131">如果命令成功，指定此選項會返回 True。</span><span class="sxs-lookup"><span data-stu-id="22ab7-131">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="22ab7-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22ab7-132">-ResourceGroupName</span></span>
<span data-ttu-id="22ab7-133">資源組名</span><span class="sxs-lookup"><span data-stu-id="22ab7-133">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ConsumergroupPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22ab7-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="22ab7-134">-ResourceId</span></span>
<span data-ttu-id="22ab7-135">ConsumerGroup 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="22ab7-135">ConsumerGroup Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ConsumergroupResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22ab7-136">-確認</span><span class="sxs-lookup"><span data-stu-id="22ab7-136">-Confirm</span></span>
<span data-ttu-id="22ab7-137">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="22ab7-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22ab7-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22ab7-138">-WhatIf</span></span>
<span data-ttu-id="22ab7-139">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="22ab7-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22ab7-140">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="22ab7-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22ab7-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22ab7-141">CommonParameters</span></span>
<span data-ttu-id="22ab7-142">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="22ab7-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22ab7-143">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="22ab7-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22ab7-144">輸入</span><span class="sxs-lookup"><span data-stu-id="22ab7-144">INPUTS</span></span>

### <span data-ttu-id="22ab7-145">System.String</span><span class="sxs-lookup"><span data-stu-id="22ab7-145">System.String</span></span>

### <span data-ttu-id="22ab7-146">Microsoft.Azure.Commands.EventHub.models.PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="22ab7-146">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="22ab7-147">輸出</span><span class="sxs-lookup"><span data-stu-id="22ab7-147">OUTPUTS</span></span>

### <span data-ttu-id="22ab7-148">System.Void</span><span class="sxs-lookup"><span data-stu-id="22ab7-148">System.Void</span></span>

## <span data-ttu-id="22ab7-149">筆記</span><span class="sxs-lookup"><span data-stu-id="22ab7-149">NOTES</span></span>

## <span data-ttu-id="22ab7-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="22ab7-150">RELATED LINKS</span></span>
