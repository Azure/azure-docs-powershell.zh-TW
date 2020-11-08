---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubConsumerGroup.md
ms.openlocfilehash: f84464d366ae84cf0a83ecc616a80b90475af8d7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129531"
---
# <span data-ttu-id="3f6d2-101">Remove-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="3f6d2-101">Remove-AzEventHubConsumerGroup</span></span>

## <span data-ttu-id="3f6d2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3f6d2-102">SYNOPSIS</span></span>
<span data-ttu-id="3f6d2-103">刪除指定的事件中樞消費者群組。</span><span class="sxs-lookup"><span data-stu-id="3f6d2-103">Deletes the specified Event Hubs consumer group.</span></span>

## <span data-ttu-id="3f6d2-104">句法</span><span class="sxs-lookup"><span data-stu-id="3f6d2-104">SYNTAX</span></span>

### <span data-ttu-id="3f6d2-105">ConsumergroupPropertiesSet (預設) </span><span class="sxs-lookup"><span data-stu-id="3f6d2-105">ConsumergroupPropertiesSet (Default)</span></span>
```
Remove-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3f6d2-106">ConsumergroupInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="3f6d2-106">ConsumergroupInputObjectSet</span></span>
```
Remove-AzEventHubConsumerGroup [-InputObject] <PSConsumerGroupAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f6d2-107">ConsumergroupResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f6d2-107">ConsumergroupResourceIdParameterSet</span></span>
```
Remove-AzEventHubConsumerGroup [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f6d2-108">說明</span><span class="sxs-lookup"><span data-stu-id="3f6d2-108">DESCRIPTION</span></span>
<span data-ttu-id="3f6d2-109">Remove-AzEventHubConsumerGroup Cmdlet 會從指定的事件中心移除並刪除指定的消費者群組。</span><span class="sxs-lookup"><span data-stu-id="3f6d2-109">The Remove-AzEventHubConsumerGroup cmdlet removes and deletes the specified consumer group from the given Event Hub.</span></span>

## <span data-ttu-id="3f6d2-110">示例</span><span class="sxs-lookup"><span data-stu-id="3f6d2-110">EXAMPLES</span></span>

### <span data-ttu-id="3f6d2-111">範例1</span><span class="sxs-lookup"><span data-stu-id="3f6d2-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyConsumerGroupName
```

<span data-ttu-id="3f6d2-112">從事件中心 MyEventHubName 中刪除消費者群組 \` MyConsumerGroupName \` \` \` ，並將其範圍設定為 \` MyNamespaceName \` 命名空間。</span><span class="sxs-lookup"><span data-stu-id="3f6d2-112">Deletes the consumer group \`MyConsumerGroupName\` from the Event Hub \`MyEventHubName\`, scoped to the \`MyNamespaceName\` namespace.</span></span>

### <span data-ttu-id="3f6d2-113">範例2：使用 InputObject 的變數</span><span class="sxs-lookup"><span data-stu-id="3f6d2-113">Example 2: InputObject - Using Variable</span></span>
```powershell
PS C:\> $inputobject = Get-AzEventHubConsumerGroup <params>
PS C:\> Remove-AzEventHubConsumerGroup -InputObject $inputobject
```

### <span data-ttu-id="3f6d2-114">範例3：使用 [InputObject] 管道</span><span class="sxs-lookup"><span data-stu-id="3f6d2-114">Example 3: InputObject - Using Piping</span></span>
```powershell
PS C:\> Get-AzEventHubConsumerGroup <params> | Remove-AzEventHubConsumerGroup
```

### <span data-ttu-id="3f6d2-115">範例4：使用變數的 ResourceId</span><span class="sxs-lookup"><span data-stu-id="3f6d2-115">Example 4: ResourceId Using Variable</span></span>
```powershell
PS C:\> $resourceid = Get-AzEventHubConsumerGroup <params>
PS C:\> Remove-AzEventHubConsumerGroup -ResourceId $resourceid.Id
```

### <span data-ttu-id="3f6d2-116">範例5：使用字串的 ResourceId</span><span class="sxs-lookup"><span data-stu-id="3f6d2-116">Example 5: ResourceId Using string</span></span>
```powershell
PS C:\> Remove-AzEventHubConsumerGroup -ResourceId "/subscriptions/xxx-xxxx-xxxxx-xxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName/eventhubs/EventHubName/consumergroups/ConsumerGroupName"
```

## <span data-ttu-id="3f6d2-117">參數</span><span class="sxs-lookup"><span data-stu-id="3f6d2-117">PARAMETERS</span></span>

### <span data-ttu-id="3f6d2-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3f6d2-118">-AsJob</span></span>
<span data-ttu-id="3f6d2-119">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="3f6d2-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3f6d2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f6d2-120">-DefaultProfile</span></span>
<span data-ttu-id="3f6d2-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3f6d2-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f6d2-122">-EventHub</span><span class="sxs-lookup"><span data-stu-id="3f6d2-122">-EventHub</span></span>
<span data-ttu-id="3f6d2-123">EventHub 名稱</span><span class="sxs-lookup"><span data-stu-id="3f6d2-123">EventHub Name</span></span>

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

### <span data-ttu-id="3f6d2-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3f6d2-124">-InputObject</span></span>
<span data-ttu-id="3f6d2-125">ConsumerGroup 物件</span><span class="sxs-lookup"><span data-stu-id="3f6d2-125">ConsumerGroup Object</span></span>

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

### <span data-ttu-id="3f6d2-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="3f6d2-126">-Name</span></span>
<span data-ttu-id="3f6d2-127">ConsumerGroup 名稱</span><span class="sxs-lookup"><span data-stu-id="3f6d2-127">ConsumerGroup Name</span></span>

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

### <span data-ttu-id="3f6d2-128">-命名空間</span><span class="sxs-lookup"><span data-stu-id="3f6d2-128">-Namespace</span></span>
<span data-ttu-id="3f6d2-129">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="3f6d2-129">Namespace Name</span></span>

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

### <span data-ttu-id="3f6d2-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3f6d2-130">-PassThru</span></span>
<span data-ttu-id="3f6d2-131">如果命令成功，則指定此值會傳回 true。</span><span class="sxs-lookup"><span data-stu-id="3f6d2-131">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="3f6d2-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f6d2-132">-ResourceGroupName</span></span>
<span data-ttu-id="3f6d2-133">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="3f6d2-133">Resource Group Name</span></span>

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

### <span data-ttu-id="3f6d2-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3f6d2-134">-ResourceId</span></span>
<span data-ttu-id="3f6d2-135">ConsumerGroup 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="3f6d2-135">ConsumerGroup Resource Id</span></span>

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

### <span data-ttu-id="3f6d2-136">-確認</span><span class="sxs-lookup"><span data-stu-id="3f6d2-136">-Confirm</span></span>
<span data-ttu-id="3f6d2-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3f6d2-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f6d2-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f6d2-138">-WhatIf</span></span>
<span data-ttu-id="3f6d2-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3f6d2-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f6d2-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3f6d2-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f6d2-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f6d2-141">CommonParameters</span></span>
<span data-ttu-id="3f6d2-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3f6d2-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f6d2-143">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3f6d2-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f6d2-144">輸入</span><span class="sxs-lookup"><span data-stu-id="3f6d2-144">INPUTS</span></span>

### <span data-ttu-id="3f6d2-145">System.object</span><span class="sxs-lookup"><span data-stu-id="3f6d2-145">System.String</span></span>

### <span data-ttu-id="3f6d2-146">PSConsumerGroupAttributes 的 [.]</span><span class="sxs-lookup"><span data-stu-id="3f6d2-146">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="3f6d2-147">輸出</span><span class="sxs-lookup"><span data-stu-id="3f6d2-147">OUTPUTS</span></span>

### <span data-ttu-id="3f6d2-148">System.void</span><span class="sxs-lookup"><span data-stu-id="3f6d2-148">System.Void</span></span>

## <span data-ttu-id="3f6d2-149">筆記</span><span class="sxs-lookup"><span data-stu-id="3f6d2-149">NOTES</span></span>

## <span data-ttu-id="3f6d2-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="3f6d2-150">RELATED LINKS</span></span>