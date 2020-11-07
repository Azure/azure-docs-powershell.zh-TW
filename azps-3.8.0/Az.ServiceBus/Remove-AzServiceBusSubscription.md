---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusSubscription.md
ms.openlocfilehash: 0f767b2c59a7cbf297c652873d4be1c064aec296
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957037"
---
# <span data-ttu-id="7f61e-101">Remove-AzServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="7f61e-101">Remove-AzServiceBusSubscription</span></span>

## <span data-ttu-id="7f61e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7f61e-102">SYNOPSIS</span></span>
<span data-ttu-id="7f61e-103">從指定的服務匯流排命名空間移除主題的訂閱。</span><span class="sxs-lookup"><span data-stu-id="7f61e-103">Removes the subscription to a topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="7f61e-104">句法</span><span class="sxs-lookup"><span data-stu-id="7f61e-104">SYNTAX</span></span>

### <span data-ttu-id="7f61e-105">SubscriptionPropertiesSet (預設) </span><span class="sxs-lookup"><span data-stu-id="7f61e-105">SubscriptionPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7f61e-106">SubscriptionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="7f61e-106">SubscriptionInputObjectSet</span></span>
```
Remove-AzServiceBusSubscription [-InputObject] <PSSubscriptionAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f61e-107">SubscriptionResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="7f61e-107">SubscriptionResourceIdSet</span></span>
```
Remove-AzServiceBusSubscription [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f61e-108">說明</span><span class="sxs-lookup"><span data-stu-id="7f61e-108">DESCRIPTION</span></span>
<span data-ttu-id="7f61e-109">**AzServiceBusSubscription** Cmdlet 會從指定的服務匯流排命名空間中移除主題的訂閱。</span><span class="sxs-lookup"><span data-stu-id="7f61e-109">The **Remove-AzServiceBusSubscription** cmdlet removes the subscription to a topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="7f61e-110">示例</span><span class="sxs-lookup"><span data-stu-id="7f61e-110">EXAMPLES</span></span>

### <span data-ttu-id="7f61e-111">範例1</span><span class="sxs-lookup"><span data-stu-id="7f61e-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1
```

<span data-ttu-id="7f61e-112">移除 `SB-TopicSubscription-Example1` `SB-Topic_exampl1` 指定服務匯流排命名空間中主題的訂閱 `SB-Example1` 。</span><span class="sxs-lookup"><span data-stu-id="7f61e-112">Removes the subscription `SB-TopicSubscription-Example1` to the topic `SB-Topic_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

### <span data-ttu-id="7f61e-113">範例 2.1-使用變數：</span><span class="sxs-lookup"><span data-stu-id="7f61e-113">Example 2.1 - InputObject - Using Variable:</span></span>
```
PS C:\> $inputobject = Get-AzServiceBusSubscription <params>
PS C:\> Remove-AzServiceBusSubscription -InputObject $inputobject
```

### <span data-ttu-id="7f61e-114">範例 2.2-使用管道的 InputObject：</span><span class="sxs-lookup"><span data-stu-id="7f61e-114">Example 2.2 - InputObject - Using Piping:</span></span>
```
PS C:\>Get-AzServiceBusSubscription <params> |Remove-AzServiceBusSubscription
```

### <span data-ttu-id="7f61e-115">範例 3.1-使用變數：</span><span class="sxs-lookup"><span data-stu-id="7f61e-115">Example 3.1 - ResourceId - Using Variable:</span></span>
```
PS C:\> $resourceid = Get-AzServiceBusSubscription <params>
PS C:\> Remove-AzServiceBusSubscription -ResourceId $resourceid.Id
```

### <span data-ttu-id="7f61e-116">範例 3.2-使用中的字串值：</span><span class="sxs-lookup"><span data-stu-id="7f61e-116">Example 3.2 - ResourceId - Using string value:</span></span>
```
PS C:\> Remove-AzServiceBusSubscription -ResourceId "/subscriptions/Subscriptionid/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName/subscriptions/SubscriptionName"
```

<span data-ttu-id="7f61e-117">移除透過 $resourceid/string 中的 ARM Id 提供的訂閱（針對 ResourceId 參數）</span><span class="sxs-lookup"><span data-stu-id="7f61e-117">Removes the subscription provided through ARM Id in $resourceid/string for -ResourceId parameter</span></span> 

## <span data-ttu-id="7f61e-118">參數</span><span class="sxs-lookup"><span data-stu-id="7f61e-118">PARAMETERS</span></span>

### <span data-ttu-id="7f61e-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7f61e-119">-AsJob</span></span>
<span data-ttu-id="7f61e-120">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="7f61e-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7f61e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f61e-121">-DefaultProfile</span></span>
<span data-ttu-id="7f61e-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7f61e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f61e-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7f61e-123">-InputObject</span></span>
<span data-ttu-id="7f61e-124">服務匯流排訂閱物件</span><span class="sxs-lookup"><span data-stu-id="7f61e-124">Service Bus Subscription Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes
Parameter Sets: SubscriptionInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f61e-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="7f61e-125">-Name</span></span>
<span data-ttu-id="7f61e-126">訂閱名稱</span><span class="sxs-lookup"><span data-stu-id="7f61e-126">Subscription Name</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionPropertiesSet
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f61e-127">-命名空間</span><span class="sxs-lookup"><span data-stu-id="7f61e-127">-Namespace</span></span>
<span data-ttu-id="7f61e-128">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="7f61e-128">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionPropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f61e-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7f61e-129">-PassThru</span></span>
<span data-ttu-id="7f61e-130">如果命令成功，則指定此值會傳回 true。</span><span class="sxs-lookup"><span data-stu-id="7f61e-130">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="7f61e-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f61e-131">-ResourceGroupName</span></span>
<span data-ttu-id="7f61e-132">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="7f61e-132">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionPropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f61e-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7f61e-133">-ResourceId</span></span>
<span data-ttu-id="7f61e-134">服務匯流排訂閱資源識別碼</span><span class="sxs-lookup"><span data-stu-id="7f61e-134">Service Bus Subscription Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f61e-135">-主題</span><span class="sxs-lookup"><span data-stu-id="7f61e-135">-Topic</span></span>
<span data-ttu-id="7f61e-136">主題名稱</span><span class="sxs-lookup"><span data-stu-id="7f61e-136">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionPropertiesSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f61e-137">-確認</span><span class="sxs-lookup"><span data-stu-id="7f61e-137">-Confirm</span></span>
<span data-ttu-id="7f61e-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7f61e-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f61e-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f61e-139">-WhatIf</span></span>
<span data-ttu-id="7f61e-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7f61e-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f61e-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7f61e-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f61e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f61e-142">CommonParameters</span></span>
<span data-ttu-id="7f61e-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7f61e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f61e-144">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7f61e-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f61e-145">輸入</span><span class="sxs-lookup"><span data-stu-id="7f61e-145">INPUTS</span></span>

### <span data-ttu-id="7f61e-146">System.object</span><span class="sxs-lookup"><span data-stu-id="7f61e-146">System.String</span></span>

### <span data-ttu-id="7f61e-147">PSSubscriptionAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="7f61e-147">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="7f61e-148">輸出</span><span class="sxs-lookup"><span data-stu-id="7f61e-148">OUTPUTS</span></span>

### <span data-ttu-id="7f61e-149">System.object</span><span class="sxs-lookup"><span data-stu-id="7f61e-149">System.Boolean</span></span>

## <span data-ttu-id="7f61e-150">筆記</span><span class="sxs-lookup"><span data-stu-id="7f61e-150">NOTES</span></span>

## <span data-ttu-id="7f61e-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="7f61e-151">RELATED LINKS</span></span>
