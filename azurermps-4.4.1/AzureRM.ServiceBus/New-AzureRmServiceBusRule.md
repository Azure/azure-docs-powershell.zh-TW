---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusRule.md
ms.openlocfilehash: 39cd0759f18c84f78a2e6a75f8e1c9b257fb9da9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626217"
---
# <span data-ttu-id="f50f1-101">New-AzureRmServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="f50f1-101">New-AzureRmServiceBusRule</span></span>

## <span data-ttu-id="f50f1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f50f1-102">SYNOPSIS</span></span>
<span data-ttu-id="f50f1-103">針對特定主題的訂閱建立新規則。</span><span class="sxs-lookup"><span data-stu-id="f50f1-103">Creates a new rule for a given Subscription of Topic.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f50f1-104">句法</span><span class="sxs-lookup"><span data-stu-id="f50f1-104">SYNTAX</span></span>

```
New-AzureRmServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-SqlExpression] <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="f50f1-105">說明</span><span class="sxs-lookup"><span data-stu-id="f50f1-105">DESCRIPTION</span></span>
<span data-ttu-id="f50f1-106">**新的-AzureRmServiceBusRule** Cmdlet 會為指定的訂閱建立新的規則。</span><span class="sxs-lookup"><span data-stu-id="f50f1-106">The **New-AzureRmServiceBusRule** cmdlet Creates a new rule for given subscription.</span></span>

## <span data-ttu-id="f50f1-107">示例</span><span class="sxs-lookup"><span data-stu-id="f50f1-107">EXAMPLES</span></span>

### <span data-ttu-id="f50f1-108">範例1</span><span class="sxs-lookup"><span data-stu-id="f50f1-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -SqlExpression "mysqlexpression='test'"
```

<span data-ttu-id="f50f1-109">**新的-AzureRmServiceBusRule** Cmdlet 會為指定的訂閱建立新的規則。</span><span class="sxs-lookup"><span data-stu-id="f50f1-109">The **New-AzureRmServiceBusRule** cmdlet creates a new rule for the specified Subscription.</span></span>

## <span data-ttu-id="f50f1-110">參數</span><span class="sxs-lookup"><span data-stu-id="f50f1-110">PARAMETERS</span></span>

### <span data-ttu-id="f50f1-111">-確認</span><span class="sxs-lookup"><span data-stu-id="f50f1-111">-Confirm</span></span>
<span data-ttu-id="f50f1-112">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f50f1-112">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f50f1-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="f50f1-113">-Name</span></span>
<span data-ttu-id="f50f1-114">規則名稱</span><span class="sxs-lookup"><span data-stu-id="f50f1-114">Rule Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f50f1-115">-命名空間</span><span class="sxs-lookup"><span data-stu-id="f50f1-115">-Namespace</span></span>
<span data-ttu-id="f50f1-116">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="f50f1-116">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f50f1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f50f1-117">-ResourceGroupName</span></span>
<span data-ttu-id="f50f1-118">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="f50f1-118">The name of the resource group</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f50f1-119">-SqlExpression</span><span class="sxs-lookup"><span data-stu-id="f50f1-119">-SqlExpression</span></span>
<span data-ttu-id="f50f1-120">Sql Fillter 運算式</span><span class="sxs-lookup"><span data-stu-id="f50f1-120">Sql Fillter Expression</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f50f1-121">-訂閱</span><span class="sxs-lookup"><span data-stu-id="f50f1-121">-Subscription</span></span>
<span data-ttu-id="f50f1-122">訂閱名稱</span><span class="sxs-lookup"><span data-stu-id="f50f1-122">Subscription Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f50f1-123">-主題</span><span class="sxs-lookup"><span data-stu-id="f50f1-123">-Topic</span></span>
<span data-ttu-id="f50f1-124">主題名稱。</span><span class="sxs-lookup"><span data-stu-id="f50f1-124">Topic Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f50f1-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f50f1-125">-WhatIf</span></span>
<span data-ttu-id="f50f1-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f50f1-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f50f1-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f50f1-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="f50f1-128">輸入</span><span class="sxs-lookup"><span data-stu-id="f50f1-128">INPUTS</span></span>

### <span data-ttu-id="f50f1-129">System.object</span><span class="sxs-lookup"><span data-stu-id="f50f1-129">System.String</span></span>


## <span data-ttu-id="f50f1-130">輸出</span><span class="sxs-lookup"><span data-stu-id="f50f1-130">OUTPUTS</span></span>

### <span data-ttu-id="f50f1-131">RulesAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f50f1-131">Microsoft.Azure.Commands.ServiceBus.Models.RulesAttributes</span></span>


## <span data-ttu-id="f50f1-132">筆記</span><span class="sxs-lookup"><span data-stu-id="f50f1-132">NOTES</span></span>

## <span data-ttu-id="f50f1-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="f50f1-133">RELATED LINKS</span></span>

