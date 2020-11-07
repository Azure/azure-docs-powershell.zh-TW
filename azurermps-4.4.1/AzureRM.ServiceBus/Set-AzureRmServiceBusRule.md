---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusRule.md
ms.openlocfilehash: 4fb10e2bb438cbc4f40936f9f9ead5c0bb36d861
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625961"
---
# <span data-ttu-id="84013-101">Set-AzureRmServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="84013-101">Set-AzureRmServiceBusRule</span></span>

## <span data-ttu-id="84013-102">摘要</span><span class="sxs-lookup"><span data-stu-id="84013-102">SYNOPSIS</span></span>
<span data-ttu-id="84013-103">針對指定的訂閱更新指定的規則描述。</span><span class="sxs-lookup"><span data-stu-id="84013-103">Updates the specified rule description for the given subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84013-104">句法</span><span class="sxs-lookup"><span data-stu-id="84013-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-InputObject] <RulesAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84013-105">說明</span><span class="sxs-lookup"><span data-stu-id="84013-105">DESCRIPTION</span></span>
<span data-ttu-id="84013-106">**AzureRmServiceBusRule** Cmdlet 會更新指定訂閱之指定規則的描述。</span><span class="sxs-lookup"><span data-stu-id="84013-106">The **Set-AzureRmServiceBusRule** cmdlet updates the description for the specified rule of the given subscription.</span></span>

## <span data-ttu-id="84013-107">示例</span><span class="sxs-lookup"><span data-stu-id="84013-107">EXAMPLES</span></span>

### <span data-ttu-id="84013-108">範例1</span><span class="sxs-lookup"><span data-stu-id="84013-108">Example 1</span></span>
```
PS C:\> $getRule = Get-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
PS C:\> $getRule.SqlFilter.SqlExpression = "mysqlexpression='condition'"
PS C:\> $setRule = Set-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -InputObject $getRule
```

<span data-ttu-id="84013-109">更新主題中的訂閱規則的 sqlexpression **mysqlexpression = ' 條件** 」 `SBEule` `SBSubscription``SBTopic`</span><span class="sxs-lookup"><span data-stu-id="84013-109">updates the sqlexpression **mysqlexpression='condition'** of the rule `SBEule` of the subscription `SBSubscription` in Topic `SBTopic`</span></span>

## <span data-ttu-id="84013-110">參數</span><span class="sxs-lookup"><span data-stu-id="84013-110">PARAMETERS</span></span>

### <span data-ttu-id="84013-111">-確認</span><span class="sxs-lookup"><span data-stu-id="84013-111">-Confirm</span></span>
<span data-ttu-id="84013-112">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="84013-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84013-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="84013-113">-InputObject</span></span>
<span data-ttu-id="84013-114">[一或一條規則定義]。</span><span class="sxs-lookup"><span data-stu-id="84013-114">ServiceBus Rules definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.RulesAttributes
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84013-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="84013-115">-Name</span></span>
<span data-ttu-id="84013-116">規則名稱。</span><span class="sxs-lookup"><span data-stu-id="84013-116">Rule Name.</span></span>

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

### <span data-ttu-id="84013-117">-命名空間</span><span class="sxs-lookup"><span data-stu-id="84013-117">-Namespace</span></span>
<span data-ttu-id="84013-118">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="84013-118">Namespace Name.</span></span>

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

### <span data-ttu-id="84013-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84013-119">-ResourceGroupName</span></span>
<span data-ttu-id="84013-120">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="84013-120">The name of the resource group</span></span>

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

### <span data-ttu-id="84013-121">-訂閱</span><span class="sxs-lookup"><span data-stu-id="84013-121">-Subscription</span></span>
<span data-ttu-id="84013-122">訂閱名稱。</span><span class="sxs-lookup"><span data-stu-id="84013-122">Subscription Name.</span></span>

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

### <span data-ttu-id="84013-123">-主題</span><span class="sxs-lookup"><span data-stu-id="84013-123">-Topic</span></span>
<span data-ttu-id="84013-124">主題名稱。</span><span class="sxs-lookup"><span data-stu-id="84013-124">Topic Name.</span></span>

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

### <span data-ttu-id="84013-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84013-125">-WhatIf</span></span>
<span data-ttu-id="84013-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="84013-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84013-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="84013-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84013-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84013-128">-DefaultProfile</span></span>
<span data-ttu-id="84013-129">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="84013-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84013-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84013-130">CommonParameters</span></span>
<span data-ttu-id="84013-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="84013-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84013-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="84013-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84013-133">輸入</span><span class="sxs-lookup"><span data-stu-id="84013-133">INPUTS</span></span>

### <span data-ttu-id="84013-134">System.object</span><span class="sxs-lookup"><span data-stu-id="84013-134">System.String</span></span>
<span data-ttu-id="84013-135">RulesAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="84013-135">Microsoft.Azure.Commands.ServiceBus.Models.RulesAttributes</span></span>

## <span data-ttu-id="84013-136">輸出</span><span class="sxs-lookup"><span data-stu-id="84013-136">OUTPUTS</span></span>

### <span data-ttu-id="84013-137">RulesAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="84013-137">Microsoft.Azure.Commands.ServiceBus.Models.RulesAttributes</span></span>

## <span data-ttu-id="84013-138">筆記</span><span class="sxs-lookup"><span data-stu-id="84013-138">NOTES</span></span>

## <span data-ttu-id="84013-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="84013-139">RELATED LINKS</span></span>
