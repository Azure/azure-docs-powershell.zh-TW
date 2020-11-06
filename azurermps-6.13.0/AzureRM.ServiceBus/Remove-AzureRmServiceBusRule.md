---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusRule.md
ms.openlocfilehash: dc75d9895d5e56f7cd7915947ff8a63ac54f2a3c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449742"
---
# <span data-ttu-id="a72d1-101">Remove-AzureRmServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="a72d1-101">Remove-AzureRmServiceBusRule</span></span>

## <span data-ttu-id="a72d1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a72d1-102">SYNOPSIS</span></span>
<span data-ttu-id="a72d1-103">移除指定訂閱的指定規則。</span><span class="sxs-lookup"><span data-stu-id="a72d1-103">Removes the speficied rule of a given subscription .</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a72d1-104">句法</span><span class="sxs-lookup"><span data-stu-id="a72d1-104">SYNTAX</span></span>

### <span data-ttu-id="a72d1-105">RulePropertiesSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a72d1-105">RulePropertiesSet (Default)</span></span>
```
Remove-AzureRmServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a72d1-106">RuleResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a72d1-106">RuleResourceIdSet</span></span>
```
Remove-AzureRmServiceBusRule [-InputObject] <PSTopicAttributes> [-ResourceId] <String> [-PassThru] [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a72d1-107">說明</span><span class="sxs-lookup"><span data-stu-id="a72d1-107">DESCRIPTION</span></span>
<span data-ttu-id="a72d1-108">**AzureRmServiceBusRule** Cmdlet 會移除指定主題的訂閱規則。</span><span class="sxs-lookup"><span data-stu-id="a72d1-108">The **Remove-AzureRmServiceBusRule** cmdlet removes the rule of a subscription of given topic.</span></span>

## <span data-ttu-id="a72d1-109">示例</span><span class="sxs-lookup"><span data-stu-id="a72d1-109">EXAMPLES</span></span>

### <span data-ttu-id="a72d1-110">範例1</span><span class="sxs-lookup"><span data-stu-id="a72d1-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
```

<span data-ttu-id="a72d1-111">移除 `SBRule` 指定主題的訂閱規則 `SBSubscription` `SBTopic` 。</span><span class="sxs-lookup"><span data-stu-id="a72d1-111">Removes the rule `SBRule` of subscription `SBSubscription` of specified topic `SBTopic`.</span></span>

### <span data-ttu-id="a72d1-112">範例 2.1-使用變數：</span><span class="sxs-lookup"><span data-stu-id="a72d1-112">Example 2.1 - InputObject - Using Variable:</span></span>
```
PS C:\> $inputobject = Get-AzureRmServiceBusRule <params>
PS C:\> Remove-AzureRmServiceBusRule -InputObject $inputobject
```

<span data-ttu-id="a72d1-113">移除透過 $inputobject for-InputObject 參數提供的規則</span><span class="sxs-lookup"><span data-stu-id="a72d1-113">Removes the rule provided through $inputobject for -InputObject parameter</span></span>

### <span data-ttu-id="a72d1-114">範例 2.2-使用管道的 InputObject：</span><span class="sxs-lookup"><span data-stu-id="a72d1-114">Example 2.2 - InputObject - Using Piping:</span></span>
```
PS C:\> Get-AzureRmServiceBusRule <params> | Remove-AzureRmServiceBusRule
```

### <span data-ttu-id="a72d1-115">範例 3.1-使用變數的 ResourceId</span><span class="sxs-lookup"><span data-stu-id="a72d1-115">Example 3.1 - ResourceId - Using Variable</span></span>
```
PS C:\> $resourceid = Get-AzureRmServiceBusRule <params>
PS C:\> Remove-AzureRmServiceBusRule -ResourceId $resourceid.Id
```

### <span data-ttu-id="a72d1-116">範例 3.1-使用中字串值的 ResourceId</span><span class="sxs-lookup"><span data-stu-id="a72d1-116">Example 3.1 - ResourceId - Using string value</span></span>
```
PS C:\> Remove-AzureRmServiceBusRule -ResourceId "/subscriptions/xxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName/subscriptions/SubscriptionName/rules/RuleName"
```

<span data-ttu-id="a72d1-117">在 $resourceid/string 中移除透過 ARM Id 提供的規則</span><span class="sxs-lookup"><span data-stu-id="a72d1-117">Removes the rule provided through ARM Id in $resourceid/string for -ResourceId parameter</span></span> 

## <span data-ttu-id="a72d1-118">參數</span><span class="sxs-lookup"><span data-stu-id="a72d1-118">PARAMETERS</span></span>

### <span data-ttu-id="a72d1-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a72d1-119">-AsJob</span></span>
<span data-ttu-id="a72d1-120">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a72d1-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a72d1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a72d1-121">-DefaultProfile</span></span>
<span data-ttu-id="a72d1-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a72d1-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a72d1-123">-Force</span><span class="sxs-lookup"><span data-stu-id="a72d1-123">-Force</span></span>
<span data-ttu-id="a72d1-124">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="a72d1-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="a72d1-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a72d1-125">-InputObject</span></span>
<span data-ttu-id="a72d1-126">服務匯流排規則物件</span><span class="sxs-lookup"><span data-stu-id="a72d1-126">Service Bus Rule Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes
Parameter Sets: RuleResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a72d1-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="a72d1-127">-Name</span></span>
<span data-ttu-id="a72d1-128">規則名稱</span><span class="sxs-lookup"><span data-stu-id="a72d1-128">Rule Name</span></span>

```yaml
Type: System.String
Parameter Sets: RulePropertiesSet
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a72d1-129">-命名空間</span><span class="sxs-lookup"><span data-stu-id="a72d1-129">-Namespace</span></span>
<span data-ttu-id="a72d1-130">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="a72d1-130">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: RulePropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a72d1-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a72d1-131">-PassThru</span></span>
<span data-ttu-id="a72d1-132">如果命令成功，則指定此值會傳回 true。</span><span class="sxs-lookup"><span data-stu-id="a72d1-132">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="a72d1-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a72d1-133">-ResourceGroupName</span></span>
<span data-ttu-id="a72d1-134">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="a72d1-134">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: RulePropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a72d1-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a72d1-135">-ResourceId</span></span>
<span data-ttu-id="a72d1-136">服務匯流排規則資源識別碼</span><span class="sxs-lookup"><span data-stu-id="a72d1-136">Service Bus Rule Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: RuleResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a72d1-137">-訂閱</span><span class="sxs-lookup"><span data-stu-id="a72d1-137">-Subscription</span></span>
<span data-ttu-id="a72d1-138">訂閱名稱</span><span class="sxs-lookup"><span data-stu-id="a72d1-138">Subscription Name</span></span>

```yaml
Type: System.String
Parameter Sets: RulePropertiesSet
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a72d1-139">-主題</span><span class="sxs-lookup"><span data-stu-id="a72d1-139">-Topic</span></span>
<span data-ttu-id="a72d1-140">主題名稱</span><span class="sxs-lookup"><span data-stu-id="a72d1-140">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: RulePropertiesSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a72d1-141">-確認</span><span class="sxs-lookup"><span data-stu-id="a72d1-141">-Confirm</span></span>
<span data-ttu-id="a72d1-142">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a72d1-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a72d1-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a72d1-143">-WhatIf</span></span>
<span data-ttu-id="a72d1-144">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a72d1-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a72d1-145">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a72d1-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a72d1-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a72d1-146">CommonParameters</span></span>
<span data-ttu-id="a72d1-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a72d1-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a72d1-148">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a72d1-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a72d1-149">輸入</span><span class="sxs-lookup"><span data-stu-id="a72d1-149">INPUTS</span></span>

### <span data-ttu-id="a72d1-150">System.object</span><span class="sxs-lookup"><span data-stu-id="a72d1-150">System.String</span></span>

### <span data-ttu-id="a72d1-151">PSTopicAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a72d1-151">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>
<span data-ttu-id="a72d1-152">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="a72d1-152">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="a72d1-153">輸出</span><span class="sxs-lookup"><span data-stu-id="a72d1-153">OUTPUTS</span></span>

### <span data-ttu-id="a72d1-154">System.object</span><span class="sxs-lookup"><span data-stu-id="a72d1-154">System.Boolean</span></span>

## <span data-ttu-id="a72d1-155">筆記</span><span class="sxs-lookup"><span data-stu-id="a72d1-155">NOTES</span></span>

## <span data-ttu-id="a72d1-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="a72d1-156">RELATED LINKS</span></span>
