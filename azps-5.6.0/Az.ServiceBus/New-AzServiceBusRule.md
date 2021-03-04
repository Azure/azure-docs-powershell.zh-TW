---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/new-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusRule.md
ms.openlocfilehash: 12064269e3a8c2e424bbd0e15888968c679784e4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904337"
---
# <span data-ttu-id="64de8-101">New-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="64de8-101">New-AzServiceBusRule</span></span>

## <span data-ttu-id="64de8-102">簡介</span><span class="sxs-lookup"><span data-stu-id="64de8-102">SYNOPSIS</span></span>
<span data-ttu-id="64de8-103">為給定主題訂閱建立新規則。</span><span class="sxs-lookup"><span data-stu-id="64de8-103">Creates a new rule for a given Subscription of Topic.</span></span> 

## <span data-ttu-id="64de8-104">語法</span><span class="sxs-lookup"><span data-stu-id="64de8-104">SYNTAX</span></span>

### <span data-ttu-id="64de8-105">RulePropertiesSet (預設) </span><span class="sxs-lookup"><span data-stu-id="64de8-105">RulePropertiesSet (Default)</span></span>
```
New-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-SqlExpression] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64de8-106">RuleActionPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="64de8-106">RuleActionPropertiesSet</span></span>
```
New-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-SqlExpression] <String> -ActionSqlExpression <String>
 [-RequiresPreprocessing] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64de8-107">描述</span><span class="sxs-lookup"><span data-stu-id="64de8-107">DESCRIPTION</span></span>
<span data-ttu-id="64de8-108">**New-AzServiceBusRule** Cmdlet 會為給定訂閱建立新規則。</span><span class="sxs-lookup"><span data-stu-id="64de8-108">The **New-AzServiceBusRule** cmdlet Creates a new rule for given subscription.</span></span>

## <span data-ttu-id="64de8-109">例子</span><span class="sxs-lookup"><span data-stu-id="64de8-109">EXAMPLES</span></span>

### <span data-ttu-id="64de8-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="64de8-110">Example 1</span></span>
```
PS C:\> New-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -SqlExpression "mysqlexpression='test'"
```

<span data-ttu-id="64de8-111">此New-AzServiceBusRule Cmdlet 會為指定的訂閱建立新規則。</span><span class="sxs-lookup"><span data-stu-id="64de8-111">The New-AzServiceBusRule cmdlet creates a new rule for the specified Subscription.</span></span>

### <span data-ttu-id="64de8-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="64de8-112">Example 2</span></span>
```
PS C:\> New-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -SqlExpression "mysqlexpression='test'" -ActionSqlExpression "SET myAction='test'" -RequiresPreprocessing
```

<span data-ttu-id="64de8-113">Cmdlet New-AzServiceBusRule使用 ActionFilter 為指定的訂閱建立新規則。</span><span class="sxs-lookup"><span data-stu-id="64de8-113">The New-AzServiceBusRule cmdlet creates a new rule for the specified Subscription with ActionFilter.</span></span>

## <span data-ttu-id="64de8-114">參數</span><span class="sxs-lookup"><span data-stu-id="64de8-114">PARAMETERS</span></span>

### <span data-ttu-id="64de8-115">-ActionSqlExpression</span><span class="sxs-lookup"><span data-stu-id="64de8-115">-ActionSqlExpression</span></span>
<span data-ttu-id="64de8-116">動作 SqlFilter 運算式</span><span class="sxs-lookup"><span data-stu-id="64de8-116">Action SqlFilter Expression</span></span>

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

### <span data-ttu-id="64de8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64de8-117">-DefaultProfile</span></span>
<span data-ttu-id="64de8-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="64de8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64de8-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="64de8-119">-Name</span></span>
<span data-ttu-id="64de8-120">規則名稱</span><span class="sxs-lookup"><span data-stu-id="64de8-120">Rule Name</span></span>

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

### <span data-ttu-id="64de8-121">-命名空間</span><span class="sxs-lookup"><span data-stu-id="64de8-121">-Namespace</span></span>
<span data-ttu-id="64de8-122">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="64de8-122">Namespace Name</span></span>

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

### <span data-ttu-id="64de8-123">-RequiresPreprocessing</span><span class="sxs-lookup"><span data-stu-id="64de8-123">-RequiresPreprocessing</span></span>
<span data-ttu-id="64de8-124">需要預處理的動作</span><span class="sxs-lookup"><span data-stu-id="64de8-124">Action Requires Preprocessing</span></span>

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

### <span data-ttu-id="64de8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64de8-125">-ResourceGroupName</span></span>
<span data-ttu-id="64de8-126">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="64de8-126">The name of the resource group</span></span>

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

### <span data-ttu-id="64de8-127">-SqlExpression</span><span class="sxs-lookup"><span data-stu-id="64de8-127">-SqlExpression</span></span>
<span data-ttu-id="64de8-128">Sql Filter 運算式</span><span class="sxs-lookup"><span data-stu-id="64de8-128">Sql Filter Expression</span></span>

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

### <span data-ttu-id="64de8-129">-訂閱</span><span class="sxs-lookup"><span data-stu-id="64de8-129">-Subscription</span></span>
<span data-ttu-id="64de8-130">訂閱名稱</span><span class="sxs-lookup"><span data-stu-id="64de8-130">Subscription Name</span></span>

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

### <span data-ttu-id="64de8-131">-主題</span><span class="sxs-lookup"><span data-stu-id="64de8-131">-Topic</span></span>
<span data-ttu-id="64de8-132">主題名稱</span><span class="sxs-lookup"><span data-stu-id="64de8-132">Topic Name</span></span>

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

### <span data-ttu-id="64de8-133">-確認</span><span class="sxs-lookup"><span data-stu-id="64de8-133">-Confirm</span></span>
<span data-ttu-id="64de8-134">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="64de8-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64de8-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64de8-135">-WhatIf</span></span>
<span data-ttu-id="64de8-136">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="64de8-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64de8-137">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="64de8-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64de8-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64de8-138">CommonParameters</span></span>
<span data-ttu-id="64de8-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="64de8-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64de8-140">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="64de8-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64de8-141">輸入</span><span class="sxs-lookup"><span data-stu-id="64de8-141">INPUTS</span></span>

### <span data-ttu-id="64de8-142">System.String</span><span class="sxs-lookup"><span data-stu-id="64de8-142">System.String</span></span>

## <span data-ttu-id="64de8-143">輸出</span><span class="sxs-lookup"><span data-stu-id="64de8-143">OUTPUTS</span></span>

### <span data-ttu-id="64de8-144">Microsoft.Azure.Commands.ServiceBus.models.PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="64de8-144">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="64de8-145">筆記</span><span class="sxs-lookup"><span data-stu-id="64de8-145">NOTES</span></span>

## <span data-ttu-id="64de8-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="64de8-146">RELATED LINKS</span></span>
