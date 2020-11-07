---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusRule.md
ms.openlocfilehash: 0beea3a39fdad5348d84f42ff2fe95cbf3ed6b9e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792093"
---
# <span data-ttu-id="545e5-101">Set-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="545e5-101">Set-AzServiceBusRule</span></span>

## <span data-ttu-id="545e5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="545e5-102">SYNOPSIS</span></span>
<span data-ttu-id="545e5-103">針對指定的訂閱更新指定的規則描述。</span><span class="sxs-lookup"><span data-stu-id="545e5-103">Updates the specified rule description for the given subscription.</span></span>

## <span data-ttu-id="545e5-104">句法</span><span class="sxs-lookup"><span data-stu-id="545e5-104">SYNTAX</span></span>

```
Set-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-InputObject] <PSRulesAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="545e5-105">說明</span><span class="sxs-lookup"><span data-stu-id="545e5-105">DESCRIPTION</span></span>
<span data-ttu-id="545e5-106">**AzServiceBusRule** Cmdlet 會更新指定訂閱之指定規則的描述。</span><span class="sxs-lookup"><span data-stu-id="545e5-106">The **Set-AzServiceBusRule** cmdlet updates the description for the specified rule of the given subscription.</span></span>

## <span data-ttu-id="545e5-107">示例</span><span class="sxs-lookup"><span data-stu-id="545e5-107">EXAMPLES</span></span>

### <span data-ttu-id="545e5-108">範例1</span><span class="sxs-lookup"><span data-stu-id="545e5-108">Example 1</span></span>
```
PS C:\> $getRule = Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
PS C:\> $getRule.SqlFilter.SqlExpression = "mysqlexpression='condition'"
PS C:\> $setRule = Set-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -InputObject $getRule
```

<span data-ttu-id="545e5-109">在主題中更新訂閱規則的 sql expression **mysqlexpression = "condition"** `SBRule` `SBSubscription``SBTopic`</span><span class="sxs-lookup"><span data-stu-id="545e5-109">Updates the sql expression **mysqlexpression='condition'** of the rule `SBRule` of the subscription `SBSubscription` in Topic `SBTopic`</span></span>

## <span data-ttu-id="545e5-110">參數</span><span class="sxs-lookup"><span data-stu-id="545e5-110">PARAMETERS</span></span>

### <span data-ttu-id="545e5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="545e5-111">-DefaultProfile</span></span>
<span data-ttu-id="545e5-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="545e5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="545e5-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="545e5-113">-InputObject</span></span>
<span data-ttu-id="545e5-114">[一或一條規則定義]。</span><span class="sxs-lookup"><span data-stu-id="545e5-114">ServiceBus Rules definition.</span></span>

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

### <span data-ttu-id="545e5-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="545e5-115">-Name</span></span>
<span data-ttu-id="545e5-116">規則名稱。</span><span class="sxs-lookup"><span data-stu-id="545e5-116">Rule Name.</span></span>

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

### <span data-ttu-id="545e5-117">-命名空間</span><span class="sxs-lookup"><span data-stu-id="545e5-117">-Namespace</span></span>
<span data-ttu-id="545e5-118">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="545e5-118">Namespace Name.</span></span>

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

### <span data-ttu-id="545e5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="545e5-119">-ResourceGroupName</span></span>
<span data-ttu-id="545e5-120">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="545e5-120">The name of the resource group</span></span>

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

### <span data-ttu-id="545e5-121">-訂閱</span><span class="sxs-lookup"><span data-stu-id="545e5-121">-Subscription</span></span>
<span data-ttu-id="545e5-122">訂閱名稱。</span><span class="sxs-lookup"><span data-stu-id="545e5-122">Subscription Name.</span></span>

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

### <span data-ttu-id="545e5-123">-主題</span><span class="sxs-lookup"><span data-stu-id="545e5-123">-Topic</span></span>
<span data-ttu-id="545e5-124">主題名稱。</span><span class="sxs-lookup"><span data-stu-id="545e5-124">Topic Name.</span></span>

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

### <span data-ttu-id="545e5-125">-確認</span><span class="sxs-lookup"><span data-stu-id="545e5-125">-Confirm</span></span>
<span data-ttu-id="545e5-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="545e5-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="545e5-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="545e5-127">-WhatIf</span></span>
<span data-ttu-id="545e5-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="545e5-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="545e5-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="545e5-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="545e5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="545e5-130">CommonParameters</span></span>
<span data-ttu-id="545e5-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="545e5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="545e5-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="545e5-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="545e5-133">輸入</span><span class="sxs-lookup"><span data-stu-id="545e5-133">INPUTS</span></span>

### <span data-ttu-id="545e5-134">System.object</span><span class="sxs-lookup"><span data-stu-id="545e5-134">System.String</span></span>

### <span data-ttu-id="545e5-135">PSRulesAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="545e5-135">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="545e5-136">輸出</span><span class="sxs-lookup"><span data-stu-id="545e5-136">OUTPUTS</span></span>

### <span data-ttu-id="545e5-137">PSRulesAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="545e5-137">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="545e5-138">筆記</span><span class="sxs-lookup"><span data-stu-id="545e5-138">NOTES</span></span>

## <span data-ttu-id="545e5-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="545e5-139">RELATED LINKS</span></span>
