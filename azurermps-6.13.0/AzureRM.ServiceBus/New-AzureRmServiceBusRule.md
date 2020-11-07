---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusRule.md
ms.openlocfilehash: 6ef5b99f916724dcdb746d67a6f9373e4bbfc9ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624339"
---
# <span data-ttu-id="57aab-101">New-AzureRmServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="57aab-101">New-AzureRmServiceBusRule</span></span>

## <span data-ttu-id="57aab-102">摘要</span><span class="sxs-lookup"><span data-stu-id="57aab-102">SYNOPSIS</span></span>
<span data-ttu-id="57aab-103">針對特定主題的訂閱建立新規則。</span><span class="sxs-lookup"><span data-stu-id="57aab-103">Creates a new rule for a given Subscription of Topic.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57aab-104">句法</span><span class="sxs-lookup"><span data-stu-id="57aab-104">SYNTAX</span></span>

### <span data-ttu-id="57aab-105">RulePropertiesSet (預設) </span><span class="sxs-lookup"><span data-stu-id="57aab-105">RulePropertiesSet (Default)</span></span>
```
New-AzureRmServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-SqlExpression] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57aab-106">RuleActionPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="57aab-106">RuleActionPropertiesSet</span></span>
```
New-AzureRmServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-SqlExpression] <String> -ActionSqlExpression <String>
 [-RequiresPreprocessing] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57aab-107">說明</span><span class="sxs-lookup"><span data-stu-id="57aab-107">DESCRIPTION</span></span>
<span data-ttu-id="57aab-108">**新的-AzureRmServiceBusRule** Cmdlet 會為指定的訂閱建立新的規則。</span><span class="sxs-lookup"><span data-stu-id="57aab-108">The **New-AzureRmServiceBusRule** cmdlet Creates a new rule for given subscription.</span></span>

## <span data-ttu-id="57aab-109">示例</span><span class="sxs-lookup"><span data-stu-id="57aab-109">EXAMPLES</span></span>

### <span data-ttu-id="57aab-110">範例1</span><span class="sxs-lookup"><span data-stu-id="57aab-110">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -SqlExpression "mysqlexpression='test'"
```

<span data-ttu-id="57aab-111">New-AzureRmServiceBusRule Cmdlet 會為指定的訂閱建立新的規則。</span><span class="sxs-lookup"><span data-stu-id="57aab-111">The New-AzureRmServiceBusRule cmdlet creates a new rule for the specified Subscription.</span></span>


### <span data-ttu-id="57aab-112">範例2</span><span class="sxs-lookup"><span data-stu-id="57aab-112">Example 2</span></span>
```
PS C:\> New-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -SqlExpression "mysqlexpression='test'" -ActionSqlExpression "SET myAction='test'" -RequiresPreprocessing
```

<span data-ttu-id="57aab-113">New-AzureRmServiceBusRule Cmdlet 會使用 ActionFilter 為指定的訂閱建立新規則。</span><span class="sxs-lookup"><span data-stu-id="57aab-113">The New-AzureRmServiceBusRule cmdlet creates a new rule for the specified Subscription with ActionFilter.</span></span>

## <span data-ttu-id="57aab-114">參數</span><span class="sxs-lookup"><span data-stu-id="57aab-114">PARAMETERS</span></span>

### <span data-ttu-id="57aab-115">-ActionSqlExpression</span><span class="sxs-lookup"><span data-stu-id="57aab-115">-ActionSqlExpression</span></span>
<span data-ttu-id="57aab-116">Action SqlFillter 運算式</span><span class="sxs-lookup"><span data-stu-id="57aab-116">Action SqlFillter Expression</span></span>

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

### <span data-ttu-id="57aab-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57aab-117">-DefaultProfile</span></span>
<span data-ttu-id="57aab-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="57aab-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57aab-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="57aab-119">-Name</span></span>
<span data-ttu-id="57aab-120">規則名稱</span><span class="sxs-lookup"><span data-stu-id="57aab-120">Rule Name</span></span>

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

### <span data-ttu-id="57aab-121">-命名空間</span><span class="sxs-lookup"><span data-stu-id="57aab-121">-Namespace</span></span>
<span data-ttu-id="57aab-122">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="57aab-122">Namespace Name</span></span>

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

### <span data-ttu-id="57aab-123">-RequiresPreprocessing</span><span class="sxs-lookup"><span data-stu-id="57aab-123">-RequiresPreprocessing</span></span>
<span data-ttu-id="57aab-124">動作需要預處理</span><span class="sxs-lookup"><span data-stu-id="57aab-124">Action Requires Preprocessing</span></span>

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

### <span data-ttu-id="57aab-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57aab-125">-ResourceGroupName</span></span>
<span data-ttu-id="57aab-126">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="57aab-126">The name of the resource group</span></span>

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

### <span data-ttu-id="57aab-127">-SqlExpression</span><span class="sxs-lookup"><span data-stu-id="57aab-127">-SqlExpression</span></span>
<span data-ttu-id="57aab-128">Sql Fillter 運算式</span><span class="sxs-lookup"><span data-stu-id="57aab-128">Sql Fillter Expression</span></span>

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

### <span data-ttu-id="57aab-129">-訂閱</span><span class="sxs-lookup"><span data-stu-id="57aab-129">-Subscription</span></span>
<span data-ttu-id="57aab-130">訂閱名稱</span><span class="sxs-lookup"><span data-stu-id="57aab-130">Subscription Name</span></span>

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

### <span data-ttu-id="57aab-131">-主題</span><span class="sxs-lookup"><span data-stu-id="57aab-131">-Topic</span></span>
<span data-ttu-id="57aab-132">主題名稱</span><span class="sxs-lookup"><span data-stu-id="57aab-132">Topic Name</span></span>

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

### <span data-ttu-id="57aab-133">-確認</span><span class="sxs-lookup"><span data-stu-id="57aab-133">-Confirm</span></span>
<span data-ttu-id="57aab-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="57aab-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57aab-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57aab-135">-WhatIf</span></span>
<span data-ttu-id="57aab-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="57aab-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57aab-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="57aab-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57aab-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57aab-138">CommonParameters</span></span>
<span data-ttu-id="57aab-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="57aab-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="57aab-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="57aab-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57aab-141">輸入</span><span class="sxs-lookup"><span data-stu-id="57aab-141">INPUTS</span></span>

### <span data-ttu-id="57aab-142">System.object</span><span class="sxs-lookup"><span data-stu-id="57aab-142">System.String</span></span>


## <span data-ttu-id="57aab-143">輸出</span><span class="sxs-lookup"><span data-stu-id="57aab-143">OUTPUTS</span></span>

### <span data-ttu-id="57aab-144">PSRulesAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="57aab-144">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>


## <span data-ttu-id="57aab-145">筆記</span><span class="sxs-lookup"><span data-stu-id="57aab-145">NOTES</span></span>

## <span data-ttu-id="57aab-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="57aab-146">RELATED LINKS</span></span>
