---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/set-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusRule.md
ms.openlocfilehash: 2caf2ccfe0d3428515812aa2dfeafc1237f820f5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909321"
---
# <span data-ttu-id="295bd-101">Set-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="295bd-101">Set-AzServiceBusRule</span></span>

## <span data-ttu-id="295bd-102">簡介</span><span class="sxs-lookup"><span data-stu-id="295bd-102">SYNOPSIS</span></span>
<span data-ttu-id="295bd-103">更新指定訂閱的指定規則描述。</span><span class="sxs-lookup"><span data-stu-id="295bd-103">Updates the specified rule description for the given subscription.</span></span>

## <span data-ttu-id="295bd-104">語法</span><span class="sxs-lookup"><span data-stu-id="295bd-104">SYNTAX</span></span>

```
Set-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-InputObject] <PSRulesAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="295bd-105">描述</span><span class="sxs-lookup"><span data-stu-id="295bd-105">DESCRIPTION</span></span>
<span data-ttu-id="295bd-106">**Set-AzServiceBusRule** Cmdlet 會更新指定訂閱之指定規則的描述。</span><span class="sxs-lookup"><span data-stu-id="295bd-106">The **Set-AzServiceBusRule** cmdlet updates the description for the specified rule of the given subscription.</span></span>

## <span data-ttu-id="295bd-107">例子</span><span class="sxs-lookup"><span data-stu-id="295bd-107">EXAMPLES</span></span>

### <span data-ttu-id="295bd-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="295bd-108">Example 1</span></span>
```
PS C:\> $getRule = Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
PS C:\> $getRule.SqlFilter.SqlExpression = "mysqlexpression='condition'"
PS C:\> $setRule = Set-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -InputObject $getRule
```

<span data-ttu-id="295bd-109">更新 Topic 中訂閱規則的 sql 運算式 **mysqlexpression='condition'** `SBRule` `SBSubscription``SBTopic`</span><span class="sxs-lookup"><span data-stu-id="295bd-109">Updates the sql expression **mysqlexpression='condition'** of the rule `SBRule` of the subscription `SBSubscription` in Topic `SBTopic`</span></span>

## <span data-ttu-id="295bd-110">參數</span><span class="sxs-lookup"><span data-stu-id="295bd-110">PARAMETERS</span></span>

### <span data-ttu-id="295bd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="295bd-111">-DefaultProfile</span></span>
<span data-ttu-id="295bd-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="295bd-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="295bd-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="295bd-113">-InputObject</span></span>
<span data-ttu-id="295bd-114">ServiceBus 規則定義。</span><span class="sxs-lookup"><span data-stu-id="295bd-114">ServiceBus Rules definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="295bd-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="295bd-115">-Name</span></span>
<span data-ttu-id="295bd-116">規則名稱。</span><span class="sxs-lookup"><span data-stu-id="295bd-116">Rule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="295bd-117">-命名空間</span><span class="sxs-lookup"><span data-stu-id="295bd-117">-Namespace</span></span>
<span data-ttu-id="295bd-118">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="295bd-118">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="295bd-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="295bd-119">-ResourceGroupName</span></span>
<span data-ttu-id="295bd-120">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="295bd-120">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="295bd-121">-訂閱</span><span class="sxs-lookup"><span data-stu-id="295bd-121">-Subscription</span></span>
<span data-ttu-id="295bd-122">訂閱名稱。</span><span class="sxs-lookup"><span data-stu-id="295bd-122">Subscription Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="295bd-123">-主題</span><span class="sxs-lookup"><span data-stu-id="295bd-123">-Topic</span></span>
<span data-ttu-id="295bd-124">主題名稱。</span><span class="sxs-lookup"><span data-stu-id="295bd-124">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="295bd-125">-確認</span><span class="sxs-lookup"><span data-stu-id="295bd-125">-Confirm</span></span>
<span data-ttu-id="295bd-126">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="295bd-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="295bd-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="295bd-127">-WhatIf</span></span>
<span data-ttu-id="295bd-128">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="295bd-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="295bd-129">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="295bd-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="295bd-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="295bd-130">CommonParameters</span></span>
<span data-ttu-id="295bd-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="295bd-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="295bd-132">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="295bd-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="295bd-133">輸入</span><span class="sxs-lookup"><span data-stu-id="295bd-133">INPUTS</span></span>

### <span data-ttu-id="295bd-134">System.String</span><span class="sxs-lookup"><span data-stu-id="295bd-134">System.String</span></span>

### <span data-ttu-id="295bd-135">Microsoft.Azure.Commands.ServiceBus.models.PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="295bd-135">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="295bd-136">輸出</span><span class="sxs-lookup"><span data-stu-id="295bd-136">OUTPUTS</span></span>

### <span data-ttu-id="295bd-137">Microsoft.Azure.Commands.ServiceBus.models.PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="295bd-137">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="295bd-138">筆記</span><span class="sxs-lookup"><span data-stu-id="295bd-138">NOTES</span></span>

## <span data-ttu-id="295bd-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="295bd-139">RELATED LINKS</span></span>
