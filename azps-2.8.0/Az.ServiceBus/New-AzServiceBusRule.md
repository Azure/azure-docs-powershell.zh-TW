---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusRule.md
ms.openlocfilehash: f3d9c9029b1c87e6d58dde21eac9d41857f53ab8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93791037"
---
# <span data-ttu-id="ee385-101">New-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="ee385-101">New-AzServiceBusRule</span></span>

## <span data-ttu-id="ee385-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ee385-102">SYNOPSIS</span></span>
<span data-ttu-id="ee385-103">針對特定主題的訂閱建立新規則。</span><span class="sxs-lookup"><span data-stu-id="ee385-103">Creates a new rule for a given Subscription of Topic.</span></span> 

## <span data-ttu-id="ee385-104">句法</span><span class="sxs-lookup"><span data-stu-id="ee385-104">SYNTAX</span></span>

### <span data-ttu-id="ee385-105">RulePropertiesSet (預設) </span><span class="sxs-lookup"><span data-stu-id="ee385-105">RulePropertiesSet (Default)</span></span>
```
New-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-SqlExpression] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee385-106">RuleActionPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="ee385-106">RuleActionPropertiesSet</span></span>
```
New-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-SqlExpression] <String> -ActionSqlExpression <String>
 [-RequiresPreprocessing] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee385-107">說明</span><span class="sxs-lookup"><span data-stu-id="ee385-107">DESCRIPTION</span></span>
<span data-ttu-id="ee385-108">**新的-AzServiceBusRule** Cmdlet 會為指定的訂閱建立新的規則。</span><span class="sxs-lookup"><span data-stu-id="ee385-108">The **New-AzServiceBusRule** cmdlet Creates a new rule for given subscription.</span></span>

## <span data-ttu-id="ee385-109">示例</span><span class="sxs-lookup"><span data-stu-id="ee385-109">EXAMPLES</span></span>

### <span data-ttu-id="ee385-110">範例1</span><span class="sxs-lookup"><span data-stu-id="ee385-110">Example 1</span></span>
```
PS C:\> New-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -SqlExpression "mysqlexpression='test'"
```

<span data-ttu-id="ee385-111">New-AzServiceBusRule Cmdlet 會為指定的訂閱建立新的規則。</span><span class="sxs-lookup"><span data-stu-id="ee385-111">The New-AzServiceBusRule cmdlet creates a new rule for the specified Subscription.</span></span>

### <span data-ttu-id="ee385-112">範例2</span><span class="sxs-lookup"><span data-stu-id="ee385-112">Example 2</span></span>
```
PS C:\> New-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -SqlExpression "mysqlexpression='test'" -ActionSqlExpression "SET myAction='test'" -RequiresPreprocessing
```

<span data-ttu-id="ee385-113">New-AzServiceBusRule Cmdlet 會使用 ActionFilter 為指定的訂閱建立新規則。</span><span class="sxs-lookup"><span data-stu-id="ee385-113">The New-AzServiceBusRule cmdlet creates a new rule for the specified Subscription with ActionFilter.</span></span>

## <span data-ttu-id="ee385-114">參數</span><span class="sxs-lookup"><span data-stu-id="ee385-114">PARAMETERS</span></span>

### <span data-ttu-id="ee385-115">-ActionSqlExpression</span><span class="sxs-lookup"><span data-stu-id="ee385-115">-ActionSqlExpression</span></span>
<span data-ttu-id="ee385-116">Action SqlFilter 運算式</span><span class="sxs-lookup"><span data-stu-id="ee385-116">Action SqlFilter Expression</span></span>

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

### <span data-ttu-id="ee385-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee385-117">-DefaultProfile</span></span>
<span data-ttu-id="ee385-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ee385-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee385-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="ee385-119">-Name</span></span>
<span data-ttu-id="ee385-120">規則名稱</span><span class="sxs-lookup"><span data-stu-id="ee385-120">Rule Name</span></span>

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

### <span data-ttu-id="ee385-121">-命名空間</span><span class="sxs-lookup"><span data-stu-id="ee385-121">-Namespace</span></span>
<span data-ttu-id="ee385-122">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="ee385-122">Namespace Name</span></span>

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

### <span data-ttu-id="ee385-123">-RequiresPreprocessing</span><span class="sxs-lookup"><span data-stu-id="ee385-123">-RequiresPreprocessing</span></span>
<span data-ttu-id="ee385-124">動作需要預處理</span><span class="sxs-lookup"><span data-stu-id="ee385-124">Action Requires Preprocessing</span></span>

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

### <span data-ttu-id="ee385-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee385-125">-ResourceGroupName</span></span>
<span data-ttu-id="ee385-126">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="ee385-126">The name of the resource group</span></span>

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

### <span data-ttu-id="ee385-127">-SqlExpression</span><span class="sxs-lookup"><span data-stu-id="ee385-127">-SqlExpression</span></span>
<span data-ttu-id="ee385-128">Sql 篩選運算式</span><span class="sxs-lookup"><span data-stu-id="ee385-128">Sql Filter Expression</span></span>

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

### <span data-ttu-id="ee385-129">-訂閱</span><span class="sxs-lookup"><span data-stu-id="ee385-129">-Subscription</span></span>
<span data-ttu-id="ee385-130">訂閱名稱</span><span class="sxs-lookup"><span data-stu-id="ee385-130">Subscription Name</span></span>

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

### <span data-ttu-id="ee385-131">-主題</span><span class="sxs-lookup"><span data-stu-id="ee385-131">-Topic</span></span>
<span data-ttu-id="ee385-132">主題名稱</span><span class="sxs-lookup"><span data-stu-id="ee385-132">Topic Name</span></span>

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

### <span data-ttu-id="ee385-133">-確認</span><span class="sxs-lookup"><span data-stu-id="ee385-133">-Confirm</span></span>
<span data-ttu-id="ee385-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ee385-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee385-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee385-135">-WhatIf</span></span>
<span data-ttu-id="ee385-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ee385-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee385-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ee385-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee385-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee385-138">CommonParameters</span></span>
<span data-ttu-id="ee385-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ee385-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee385-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ee385-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee385-141">輸入</span><span class="sxs-lookup"><span data-stu-id="ee385-141">INPUTS</span></span>

### <span data-ttu-id="ee385-142">System.object</span><span class="sxs-lookup"><span data-stu-id="ee385-142">System.String</span></span>

## <span data-ttu-id="ee385-143">輸出</span><span class="sxs-lookup"><span data-stu-id="ee385-143">OUTPUTS</span></span>

### <span data-ttu-id="ee385-144">PSRulesAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ee385-144">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="ee385-145">筆記</span><span class="sxs-lookup"><span data-stu-id="ee385-145">NOTES</span></span>

## <span data-ttu-id="ee385-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="ee385-146">RELATED LINKS</span></span>
