---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/remove-azurermeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubConsumerGroup.md
ms.openlocfilehash: 2ef6227acf398b228d6ca5ffe4fad3d39ec75723
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449185"
---
# <span data-ttu-id="f28d4-101">Remove-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="f28d4-101">Remove-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="f28d4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f28d4-102">SYNOPSIS</span></span>
<span data-ttu-id="f28d4-103">刪除指定的事件中樞消費者群組。</span><span class="sxs-lookup"><span data-stu-id="f28d4-103">Deletes the specified Event Hubs consumer group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f28d4-104">句法</span><span class="sxs-lookup"><span data-stu-id="f28d4-104">SYNTAX</span></span>

### <span data-ttu-id="f28d4-105">ConsumergroupPropertiesSet (預設) </span><span class="sxs-lookup"><span data-stu-id="f28d4-105">ConsumergroupPropertiesSet (Default)</span></span>
```
Remove-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f28d4-106">ConsumergroupInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f28d4-106">ConsumergroupInputObjectSet</span></span>
```
Remove-AzureRmEventHubConsumerGroup [-InputObject] <PSConsumerGroupAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f28d4-107">ConsumergroupResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f28d4-107">ConsumergroupResourceIdParameterSet</span></span>
```
Remove-AzureRmEventHubConsumerGroup [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f28d4-108">說明</span><span class="sxs-lookup"><span data-stu-id="f28d4-108">DESCRIPTION</span></span>
<span data-ttu-id="f28d4-109">Remove-AzureRmEventHubConsumerGroup Cmdlet 會從指定的事件中心移除並刪除指定的消費者群組。</span><span class="sxs-lookup"><span data-stu-id="f28d4-109">The Remove-AzureRmEventHubConsumerGroup cmdlet removes and deletes the specified consumer group from the given Event Hub.</span></span>

## <span data-ttu-id="f28d4-110">示例</span><span class="sxs-lookup"><span data-stu-id="f28d4-110">EXAMPLES</span></span>

### <span data-ttu-id="f28d4-111">範例1</span><span class="sxs-lookup"><span data-stu-id="f28d4-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyConsumerGroupName
```

<span data-ttu-id="f28d4-112">從事件中心 MyEventHubName 中刪除消費者群組 \` MyConsumerGroupName \` \` \` ，並將其範圍設定為 \` MyNamespaceName \` 命名空間。</span><span class="sxs-lookup"><span data-stu-id="f28d4-112">Deletes the consumer group \`MyConsumerGroupName\` from the Event Hub \`MyEventHubName\`, scoped to the \`MyNamespaceName\` namespace.</span></span>

### <span data-ttu-id="f28d4-113">範例 2.1-使用變數的 InputObject</span><span class="sxs-lookup"><span data-stu-id="f28d4-113">Example 2.1 - InputObject - Using Variable</span></span>
```
PS C:\> $inputobject = Get-AzureRmEventHubConsumerGroup <params>
PS C:\> Remove-AzureRmEventHubConsumerGroup -InputObject $inputobject
```

### <span data-ttu-id="f28d4-114">範例 2.2-使用管道的 InputObject</span><span class="sxs-lookup"><span data-stu-id="f28d4-114">Example 2.2 - InputObject - Using Piping</span></span>
```
PS C:\> Get-AzureRmEventHubConsumerGroup <params> | Remove-AzureRmEventHubConsumerGroup
```

### <span data-ttu-id="f28d4-115">範例 3.1-使用 Vairable 的 ResourceId</span><span class="sxs-lookup"><span data-stu-id="f28d4-115">Example 3.1 - ResourceId Using Vairable</span></span>
```
PS C:\> $resourceid = Get-AzureRmEventHubConsumerGroup <params>
PS C:\> Remove-AzureRmEventHubConsumerGroup -ResourceId $resourceid.Id
```

### <span data-ttu-id="f28d4-116">範例 3.2-使用字串的 ResourceId</span><span class="sxs-lookup"><span data-stu-id="f28d4-116">Example 3.2 - ResourceId Using string</span></span>
```
PS C:\> Remove-AzureRmEventHubConsumerGroup -ResourceId "/subscriptions/xxx-xxxx-xxxxx-xxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName/eventhubs/EventHubName/consumergroups/ConsumerGroupName"
```

## <span data-ttu-id="f28d4-117">參數</span><span class="sxs-lookup"><span data-stu-id="f28d4-117">PARAMETERS</span></span>

### <span data-ttu-id="f28d4-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f28d4-118">-AsJob</span></span>
<span data-ttu-id="f28d4-119">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f28d4-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f28d4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f28d4-120">-DefaultProfile</span></span>
<span data-ttu-id="f28d4-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f28d4-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f28d4-122">-EventHub</span><span class="sxs-lookup"><span data-stu-id="f28d4-122">-EventHub</span></span>
<span data-ttu-id="f28d4-123">EventHub 名稱</span><span class="sxs-lookup"><span data-stu-id="f28d4-123">EventHub Name</span></span>

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

### <span data-ttu-id="f28d4-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f28d4-124">-InputObject</span></span>
<span data-ttu-id="f28d4-125">ConsumerGroup 物件</span><span class="sxs-lookup"><span data-stu-id="f28d4-125">ConsumerGroup Object</span></span>

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

### <span data-ttu-id="f28d4-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="f28d4-126">-Name</span></span>
<span data-ttu-id="f28d4-127">ConsumerGroup 名稱</span><span class="sxs-lookup"><span data-stu-id="f28d4-127">ConsumerGroup Name</span></span>

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

### <span data-ttu-id="f28d4-128">-命名空間</span><span class="sxs-lookup"><span data-stu-id="f28d4-128">-Namespace</span></span>
<span data-ttu-id="f28d4-129">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="f28d4-129">Namespace Name</span></span>

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

### <span data-ttu-id="f28d4-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f28d4-130">-PassThru</span></span>
<span data-ttu-id="f28d4-131">如果命令成功，則指定此值會傳回 true。</span><span class="sxs-lookup"><span data-stu-id="f28d4-131">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="f28d4-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f28d4-132">-ResourceGroupName</span></span>
<span data-ttu-id="f28d4-133">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="f28d4-133">Resource Group Name</span></span>

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

### <span data-ttu-id="f28d4-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f28d4-134">-ResourceId</span></span>
<span data-ttu-id="f28d4-135">ConsumerGroup 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="f28d4-135">ConsumerGroup Resource Id</span></span>

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

### <span data-ttu-id="f28d4-136">-確認</span><span class="sxs-lookup"><span data-stu-id="f28d4-136">-Confirm</span></span>
<span data-ttu-id="f28d4-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f28d4-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f28d4-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f28d4-138">-WhatIf</span></span>
<span data-ttu-id="f28d4-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f28d4-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f28d4-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f28d4-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f28d4-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f28d4-141">CommonParameters</span></span>
<span data-ttu-id="f28d4-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f28d4-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f28d4-143">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f28d4-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f28d4-144">輸入</span><span class="sxs-lookup"><span data-stu-id="f28d4-144">INPUTS</span></span>

### <span data-ttu-id="f28d4-145">System.object</span><span class="sxs-lookup"><span data-stu-id="f28d4-145">System.String</span></span>

### <span data-ttu-id="f28d4-146">PSConsumerGroupAttributes 的 [.]</span><span class="sxs-lookup"><span data-stu-id="f28d4-146">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>
<span data-ttu-id="f28d4-147">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="f28d4-147">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="f28d4-148">輸出</span><span class="sxs-lookup"><span data-stu-id="f28d4-148">OUTPUTS</span></span>

### <span data-ttu-id="f28d4-149">System.void</span><span class="sxs-lookup"><span data-stu-id="f28d4-149">System.Void</span></span>

## <span data-ttu-id="f28d4-150">筆記</span><span class="sxs-lookup"><span data-stu-id="f28d4-150">NOTES</span></span>

## <span data-ttu-id="f28d4-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="f28d4-151">RELATED LINKS</span></span>
