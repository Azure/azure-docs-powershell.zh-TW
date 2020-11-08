---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusRule.md
ms.openlocfilehash: d667049fb512545aebfd9681b3ad3d9f44651951
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127332"
---
# <span data-ttu-id="847c9-101">New-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="847c9-101">New-AzServiceBusRule</span></span>

## <span data-ttu-id="847c9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="847c9-102">SYNOPSIS</span></span>
<span data-ttu-id="847c9-103">針對特定主題的訂閱建立新規則。</span><span class="sxs-lookup"><span data-stu-id="847c9-103">Creates a new rule for a given Subscription of Topic.</span></span> 

## <span data-ttu-id="847c9-104">句法</span><span class="sxs-lookup"><span data-stu-id="847c9-104">SYNTAX</span></span>

### <span data-ttu-id="847c9-105">RulePropertiesSet (預設) </span><span class="sxs-lookup"><span data-stu-id="847c9-105">RulePropertiesSet (Default)</span></span>
```
New-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-SqlExpression] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="847c9-106">RuleActionPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="847c9-106">RuleActionPropertiesSet</span></span>
```
New-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-SqlExpression] <String> -ActionSqlExpression <String>
 [-RequiresPreprocessing] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="847c9-107">說明</span><span class="sxs-lookup"><span data-stu-id="847c9-107">DESCRIPTION</span></span>
<span data-ttu-id="847c9-108">**新的-AzServiceBusRule** Cmdlet 會為指定的訂閱建立新的規則。</span><span class="sxs-lookup"><span data-stu-id="847c9-108">The **New-AzServiceBusRule** cmdlet Creates a new rule for given subscription.</span></span>

## <span data-ttu-id="847c9-109">示例</span><span class="sxs-lookup"><span data-stu-id="847c9-109">EXAMPLES</span></span>

### <span data-ttu-id="847c9-110">範例1</span><span class="sxs-lookup"><span data-stu-id="847c9-110">Example 1</span></span>
```
PS C:\> New-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -SqlExpression "mysqlexpression='test'"
```

<span data-ttu-id="847c9-111">New-AzServiceBusRule Cmdlet 會為指定的訂閱建立新的規則。</span><span class="sxs-lookup"><span data-stu-id="847c9-111">The New-AzServiceBusRule cmdlet creates a new rule for the specified Subscription.</span></span>

### <span data-ttu-id="847c9-112">範例2</span><span class="sxs-lookup"><span data-stu-id="847c9-112">Example 2</span></span>
```
PS C:\> New-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -SqlExpression "mysqlexpression='test'" -ActionSqlExpression "SET myAction='test'" -RequiresPreprocessing
```

<span data-ttu-id="847c9-113">New-AzServiceBusRule Cmdlet 會使用 ActionFilter 為指定的訂閱建立新規則。</span><span class="sxs-lookup"><span data-stu-id="847c9-113">The New-AzServiceBusRule cmdlet creates a new rule for the specified Subscription with ActionFilter.</span></span>

## <span data-ttu-id="847c9-114">參數</span><span class="sxs-lookup"><span data-stu-id="847c9-114">PARAMETERS</span></span>

### <span data-ttu-id="847c9-115">-ActionSqlExpression</span><span class="sxs-lookup"><span data-stu-id="847c9-115">-ActionSqlExpression</span></span>
<span data-ttu-id="847c9-116">Action SqlFilter 運算式</span><span class="sxs-lookup"><span data-stu-id="847c9-116">Action SqlFilter Expression</span></span>

```yaml
Type: System.String
Parameter Sets: RuleActionPropertiesSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="847c9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="847c9-117">-DefaultProfile</span></span>
<span data-ttu-id="847c9-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="847c9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="847c9-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="847c9-119">-Name</span></span>
<span data-ttu-id="847c9-120">規則名稱</span><span class="sxs-lookup"><span data-stu-id="847c9-120">Rule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="847c9-121">-命名空間</span><span class="sxs-lookup"><span data-stu-id="847c9-121">-Namespace</span></span>
<span data-ttu-id="847c9-122">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="847c9-122">Namespace Name</span></span>

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

### <span data-ttu-id="847c9-123">-RequiresPreprocessing</span><span class="sxs-lookup"><span data-stu-id="847c9-123">-RequiresPreprocessing</span></span>
<span data-ttu-id="847c9-124">動作需要預處理</span><span class="sxs-lookup"><span data-stu-id="847c9-124">Action Requires Preprocessing</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RuleActionPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="847c9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="847c9-125">-ResourceGroupName</span></span>
<span data-ttu-id="847c9-126">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="847c9-126">The name of the resource group</span></span>

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

### <span data-ttu-id="847c9-127">-SqlExpression</span><span class="sxs-lookup"><span data-stu-id="847c9-127">-SqlExpression</span></span>
<span data-ttu-id="847c9-128">Sql 篩選運算式</span><span class="sxs-lookup"><span data-stu-id="847c9-128">Sql Filter Expression</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="847c9-129">-訂閱</span><span class="sxs-lookup"><span data-stu-id="847c9-129">-Subscription</span></span>
<span data-ttu-id="847c9-130">訂閱名稱</span><span class="sxs-lookup"><span data-stu-id="847c9-130">Subscription Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="847c9-131">-主題</span><span class="sxs-lookup"><span data-stu-id="847c9-131">-Topic</span></span>
<span data-ttu-id="847c9-132">主題名稱</span><span class="sxs-lookup"><span data-stu-id="847c9-132">Topic Name</span></span>

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

### <span data-ttu-id="847c9-133">-確認</span><span class="sxs-lookup"><span data-stu-id="847c9-133">-Confirm</span></span>
<span data-ttu-id="847c9-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="847c9-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="847c9-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="847c9-135">-WhatIf</span></span>
<span data-ttu-id="847c9-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="847c9-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="847c9-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="847c9-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="847c9-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="847c9-138">CommonParameters</span></span>
<span data-ttu-id="847c9-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="847c9-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="847c9-140">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="847c9-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="847c9-141">輸入</span><span class="sxs-lookup"><span data-stu-id="847c9-141">INPUTS</span></span>

### <span data-ttu-id="847c9-142">System.object</span><span class="sxs-lookup"><span data-stu-id="847c9-142">System.String</span></span>

## <span data-ttu-id="847c9-143">輸出</span><span class="sxs-lookup"><span data-stu-id="847c9-143">OUTPUTS</span></span>

### <span data-ttu-id="847c9-144">PSRulesAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="847c9-144">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="847c9-145">筆記</span><span class="sxs-lookup"><span data-stu-id="847c9-145">NOTES</span></span>

## <span data-ttu-id="847c9-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="847c9-146">RELATED LINKS</span></span>
