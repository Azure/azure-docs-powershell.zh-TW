---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/remove-azservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusSubscription.md
ms.openlocfilehash: 1423c0c0c67b12b1cb2fcb6bf682d3ed60aae9c6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912582"
---
# <span data-ttu-id="4f63b-101">Remove-AzServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="4f63b-101">Remove-AzServiceBusSubscription</span></span>

## <span data-ttu-id="4f63b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4f63b-102">SYNOPSIS</span></span>
<span data-ttu-id="4f63b-103">從指定的 Service Bus 命名空間移除主題的訂閱。</span><span class="sxs-lookup"><span data-stu-id="4f63b-103">Removes the subscription to a topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="4f63b-104">語法</span><span class="sxs-lookup"><span data-stu-id="4f63b-104">SYNTAX</span></span>

### <span data-ttu-id="4f63b-105">SubscriptionPropertiesSet (預設) </span><span class="sxs-lookup"><span data-stu-id="4f63b-105">SubscriptionPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4f63b-106">SubscriptionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4f63b-106">SubscriptionInputObjectSet</span></span>
```
Remove-AzServiceBusSubscription [-InputObject] <PSSubscriptionAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f63b-107">SubscriptionResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="4f63b-107">SubscriptionResourceIdSet</span></span>
```
Remove-AzServiceBusSubscription [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f63b-108">描述</span><span class="sxs-lookup"><span data-stu-id="4f63b-108">DESCRIPTION</span></span>
<span data-ttu-id="4f63b-109">**Remove-AzServiceBusSubscription** Cmdlet 會從指定的 Service Bus 命名空間移除主題的訂閱。</span><span class="sxs-lookup"><span data-stu-id="4f63b-109">The **Remove-AzServiceBusSubscription** cmdlet removes the subscription to a topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="4f63b-110">例子</span><span class="sxs-lookup"><span data-stu-id="4f63b-110">EXAMPLES</span></span>

### <span data-ttu-id="4f63b-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="4f63b-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1
```

<span data-ttu-id="4f63b-112">移除指定 Service Bus 命名空間 `SB-TopicSubscription-Example1` `SB-Topic_exampl1` 中主題的訂閱 `SB-Example1` 。</span><span class="sxs-lookup"><span data-stu-id="4f63b-112">Removes the subscription `SB-TopicSubscription-Example1` to the topic `SB-Topic_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

### <span data-ttu-id="4f63b-113">範例 2：InputObject - Using Variable：</span><span class="sxs-lookup"><span data-stu-id="4f63b-113">Example 2: InputObject - Using Variable:</span></span>
```powershell
PS C:\> $inputobject = Get-AzServiceBusSubscription <params>
PS C:\> Remove-AzServiceBusSubscription -InputObject $inputobject
```

### <span data-ttu-id="4f63b-114">範例 3：InputObject - 使用管道：</span><span class="sxs-lookup"><span data-stu-id="4f63b-114">Example 3: InputObject - Using Piping:</span></span>
```powershell
PS C:\>Get-AzServiceBusSubscription <params> |Remove-AzServiceBusSubscription
```

### <span data-ttu-id="4f63b-115">範例 4：ResourceId - Using Variable：</span><span class="sxs-lookup"><span data-stu-id="4f63b-115">Example 4: ResourceId - Using Variable:</span></span>
```powershell
PS C:\> $resourceid = Get-AzServiceBusSubscription <params>
PS C:\> Remove-AzServiceBusSubscription -ResourceId $resourceid.Id
```

### <span data-ttu-id="4f63b-116">範例 5：ResourceId - 使用字串值：</span><span class="sxs-lookup"><span data-stu-id="4f63b-116">Example 5: ResourceId - Using string value:</span></span>
```powershell
PS C:\> Remove-AzServiceBusSubscription -ResourceId "/subscriptions/Subscriptionid/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName/subscriptions/SubscriptionName"
```

<span data-ttu-id="4f63b-117">移除 -ResourceId 參數的 $resourceid/string 中透過 ARM Id 提供的訂閱</span><span class="sxs-lookup"><span data-stu-id="4f63b-117">Removes the subscription provided through ARM Id in $resourceid/string for -ResourceId parameter</span></span> 

## <span data-ttu-id="4f63b-118">參數</span><span class="sxs-lookup"><span data-stu-id="4f63b-118">PARAMETERS</span></span>

### <span data-ttu-id="4f63b-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4f63b-119">-AsJob</span></span>
<span data-ttu-id="4f63b-120">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="4f63b-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4f63b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f63b-121">-DefaultProfile</span></span>
<span data-ttu-id="4f63b-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4f63b-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f63b-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4f63b-123">-InputObject</span></span>
<span data-ttu-id="4f63b-124">Service Bus 訂閱物件</span><span class="sxs-lookup"><span data-stu-id="4f63b-124">Service Bus Subscription Object</span></span>

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

### <span data-ttu-id="4f63b-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="4f63b-125">-Name</span></span>
<span data-ttu-id="4f63b-126">訂閱名稱</span><span class="sxs-lookup"><span data-stu-id="4f63b-126">Subscription Name</span></span>

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

### <span data-ttu-id="4f63b-127">-命名空間</span><span class="sxs-lookup"><span data-stu-id="4f63b-127">-Namespace</span></span>
<span data-ttu-id="4f63b-128">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="4f63b-128">Namespace Name</span></span>

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

### <span data-ttu-id="4f63b-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4f63b-129">-PassThru</span></span>
<span data-ttu-id="4f63b-130">如果命令成功，指定此選項會返回 True。</span><span class="sxs-lookup"><span data-stu-id="4f63b-130">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="4f63b-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f63b-131">-ResourceGroupName</span></span>
<span data-ttu-id="4f63b-132">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="4f63b-132">The name of the resource group</span></span>

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

### <span data-ttu-id="4f63b-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4f63b-133">-ResourceId</span></span>
<span data-ttu-id="4f63b-134">服務母線訂閱資源識別碼</span><span class="sxs-lookup"><span data-stu-id="4f63b-134">Service Bus Subscription Resource Id</span></span>

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

### <span data-ttu-id="4f63b-135">-主題</span><span class="sxs-lookup"><span data-stu-id="4f63b-135">-Topic</span></span>
<span data-ttu-id="4f63b-136">主題名稱</span><span class="sxs-lookup"><span data-stu-id="4f63b-136">Topic Name</span></span>

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

### <span data-ttu-id="4f63b-137">-確認</span><span class="sxs-lookup"><span data-stu-id="4f63b-137">-Confirm</span></span>
<span data-ttu-id="4f63b-138">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="4f63b-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f63b-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f63b-139">-WhatIf</span></span>
<span data-ttu-id="4f63b-140">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4f63b-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f63b-141">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4f63b-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f63b-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f63b-142">CommonParameters</span></span>
<span data-ttu-id="4f63b-143">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4f63b-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f63b-144">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="4f63b-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f63b-145">輸入</span><span class="sxs-lookup"><span data-stu-id="4f63b-145">INPUTS</span></span>

### <span data-ttu-id="4f63b-146">System.String</span><span class="sxs-lookup"><span data-stu-id="4f63b-146">System.String</span></span>

### <span data-ttu-id="4f63b-147">Microsoft.Azure.Commands.ServiceBus.models.PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="4f63b-147">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="4f63b-148">輸出</span><span class="sxs-lookup"><span data-stu-id="4f63b-148">OUTPUTS</span></span>

### <span data-ttu-id="4f63b-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4f63b-149">System.Boolean</span></span>

## <span data-ttu-id="4f63b-150">筆記</span><span class="sxs-lookup"><span data-stu-id="4f63b-150">NOTES</span></span>

## <span data-ttu-id="4f63b-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="4f63b-151">RELATED LINKS</span></span>
