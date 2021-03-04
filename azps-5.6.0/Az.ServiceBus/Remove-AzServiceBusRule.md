---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/remove-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusRule.md
ms.openlocfilehash: 673e67b9611cfab468c1c6f83393515bd4997e97
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917897"
---
# <span data-ttu-id="b812c-101">Remove-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="b812c-101">Remove-AzServiceBusRule</span></span>

## <span data-ttu-id="b812c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b812c-102">SYNOPSIS</span></span>
<span data-ttu-id="b812c-103">移除指定訂閱的指定規則。</span><span class="sxs-lookup"><span data-stu-id="b812c-103">Removes the specified rule of a given subscription .</span></span>

## <span data-ttu-id="b812c-104">語法</span><span class="sxs-lookup"><span data-stu-id="b812c-104">SYNTAX</span></span>

### <span data-ttu-id="b812c-105">RulePropertiesSet (預設) </span><span class="sxs-lookup"><span data-stu-id="b812c-105">RulePropertiesSet (Default)</span></span>
```
Remove-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b812c-106">RuleResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b812c-106">RuleResourceIdSet</span></span>
```
Remove-AzServiceBusRule [-InputObject] <PSTopicAttributes> [-ResourceId] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b812c-107">描述</span><span class="sxs-lookup"><span data-stu-id="b812c-107">DESCRIPTION</span></span>
<span data-ttu-id="b812c-108">**Remove-AzServiceBusRule** Cmdlet 會移除給定主題訂閱的規則。</span><span class="sxs-lookup"><span data-stu-id="b812c-108">The **Remove-AzServiceBusRule** cmdlet removes the rule of a subscription of given topic.</span></span>

## <span data-ttu-id="b812c-109">例子</span><span class="sxs-lookup"><span data-stu-id="b812c-109">EXAMPLES</span></span>

### <span data-ttu-id="b812c-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="b812c-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
```

<span data-ttu-id="b812c-111">移除指定 `SBRule` 主題 `SBSubscription` 的訂閱規則 `SBTopic` 。</span><span class="sxs-lookup"><span data-stu-id="b812c-111">Removes the rule `SBRule` of subscription `SBSubscription` of specified topic `SBTopic`.</span></span>

### <span data-ttu-id="b812c-112">範例 2：InputObject - Using Variable：</span><span class="sxs-lookup"><span data-stu-id="b812c-112">Example 2: InputObject - Using Variable:</span></span>
```powershell
PS C:\> $inputobject = Get-AzServiceBusRule <params>
PS C:\> Remove-AzServiceBusRule -InputObject $inputobject
```

<span data-ttu-id="b812c-113">移除透過 -InputObject 參數$inputobject提供的規則</span><span class="sxs-lookup"><span data-stu-id="b812c-113">Removes the rule provided through $inputobject for -InputObject parameter</span></span>

### <span data-ttu-id="b812c-114">範例 3：InputObject - 使用管道：</span><span class="sxs-lookup"><span data-stu-id="b812c-114">Example 3: InputObject - Using Piping:</span></span>
```powershell
PS C:\> Get-AzServiceBusRule <params> | Remove-AzServiceBusRule
```

### <span data-ttu-id="b812c-115">範例 4：ResourceId - Using Variable</span><span class="sxs-lookup"><span data-stu-id="b812c-115">Example 4: ResourceId - Using Variable</span></span>
```powershell
PS C:\> $resourceid = Get-AzServiceBusRule <params>
PS C:\> Remove-AzServiceBusRule -ResourceId $resourceid.Id
```

### <span data-ttu-id="b812c-116">範例 5：ResourceId - 使用字串值</span><span class="sxs-lookup"><span data-stu-id="b812c-116">Example 5: ResourceId - Using string value</span></span>
```powershell
PS C:\> Remove-AzServiceBusRule -ResourceId "/subscriptions/xxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName/subscriptions/SubscriptionName/rules/RuleName"
```

<span data-ttu-id="b812c-117">移除 -ResourceId 參數的 $resourceid/string 中透過 ARM Id 提供的規則</span><span class="sxs-lookup"><span data-stu-id="b812c-117">Removes the rule provided through ARM Id in $resourceid/string for -ResourceId parameter</span></span> 

## <span data-ttu-id="b812c-118">參數</span><span class="sxs-lookup"><span data-stu-id="b812c-118">PARAMETERS</span></span>

### <span data-ttu-id="b812c-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b812c-119">-AsJob</span></span>
<span data-ttu-id="b812c-120">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b812c-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b812c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b812c-121">-DefaultProfile</span></span>
<span data-ttu-id="b812c-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b812c-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b812c-123">-強制</span><span class="sxs-lookup"><span data-stu-id="b812c-123">-Force</span></span>
<span data-ttu-id="b812c-124">請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="b812c-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="b812c-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b812c-125">-InputObject</span></span>
<span data-ttu-id="b812c-126">服務母線規則物件</span><span class="sxs-lookup"><span data-stu-id="b812c-126">Service Bus Rule Object</span></span>

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

### <span data-ttu-id="b812c-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="b812c-127">-Name</span></span>
<span data-ttu-id="b812c-128">規則名稱</span><span class="sxs-lookup"><span data-stu-id="b812c-128">Rule Name</span></span>

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

### <span data-ttu-id="b812c-129">-命名空間</span><span class="sxs-lookup"><span data-stu-id="b812c-129">-Namespace</span></span>
<span data-ttu-id="b812c-130">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="b812c-130">Namespace Name</span></span>

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

### <span data-ttu-id="b812c-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b812c-131">-PassThru</span></span>
<span data-ttu-id="b812c-132">如果命令成功，指定此選項會返回 True。</span><span class="sxs-lookup"><span data-stu-id="b812c-132">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="b812c-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b812c-133">-ResourceGroupName</span></span>
<span data-ttu-id="b812c-134">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="b812c-134">The name of the resource group</span></span>

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

### <span data-ttu-id="b812c-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b812c-135">-ResourceId</span></span>
<span data-ttu-id="b812c-136">服務母線規則資源識別碼</span><span class="sxs-lookup"><span data-stu-id="b812c-136">Service Bus Rule Resource Id</span></span>

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

### <span data-ttu-id="b812c-137">-訂閱</span><span class="sxs-lookup"><span data-stu-id="b812c-137">-Subscription</span></span>
<span data-ttu-id="b812c-138">訂閱名稱</span><span class="sxs-lookup"><span data-stu-id="b812c-138">Subscription Name</span></span>

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

### <span data-ttu-id="b812c-139">-主題</span><span class="sxs-lookup"><span data-stu-id="b812c-139">-Topic</span></span>
<span data-ttu-id="b812c-140">主題名稱</span><span class="sxs-lookup"><span data-stu-id="b812c-140">Topic Name</span></span>

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

### <span data-ttu-id="b812c-141">-確認</span><span class="sxs-lookup"><span data-stu-id="b812c-141">-Confirm</span></span>
<span data-ttu-id="b812c-142">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b812c-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b812c-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b812c-143">-WhatIf</span></span>
<span data-ttu-id="b812c-144">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b812c-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b812c-145">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b812c-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b812c-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b812c-146">CommonParameters</span></span>
<span data-ttu-id="b812c-147">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b812c-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b812c-148">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="b812c-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b812c-149">輸入</span><span class="sxs-lookup"><span data-stu-id="b812c-149">INPUTS</span></span>

### <span data-ttu-id="b812c-150">System.String</span><span class="sxs-lookup"><span data-stu-id="b812c-150">System.String</span></span>

### <span data-ttu-id="b812c-151">Microsoft.Azure.Commands.ServiceBus.models.PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="b812c-151">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="b812c-152">輸出</span><span class="sxs-lookup"><span data-stu-id="b812c-152">OUTPUTS</span></span>

### <span data-ttu-id="b812c-153">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b812c-153">System.Boolean</span></span>

## <span data-ttu-id="b812c-154">筆記</span><span class="sxs-lookup"><span data-stu-id="b812c-154">NOTES</span></span>

## <span data-ttu-id="b812c-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="b812c-155">RELATED LINKS</span></span>
