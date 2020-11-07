---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusRule.md
ms.openlocfilehash: 22e54316bd38907c1ab22e3b2c35e1b6949b0034
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624665"
---
# <span data-ttu-id="9c476-101">New-AzureRmServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="9c476-101">New-AzureRmServiceBusRule</span></span>

## <span data-ttu-id="9c476-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9c476-102">SYNOPSIS</span></span>
<span data-ttu-id="9c476-103">針對特定主題的訂閱建立新規則。</span><span class="sxs-lookup"><span data-stu-id="9c476-103">Creates a new rule for a given Subscription of Topic.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c476-104">句法</span><span class="sxs-lookup"><span data-stu-id="9c476-104">SYNTAX</span></span>

```
New-AzureRmServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-SqlExpression] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c476-105">說明</span><span class="sxs-lookup"><span data-stu-id="9c476-105">DESCRIPTION</span></span>
<span data-ttu-id="9c476-106">**新的-AzureRmServiceBusRule** Cmdlet 會為指定的訂閱建立新的規則。</span><span class="sxs-lookup"><span data-stu-id="9c476-106">The **New-AzureRmServiceBusRule** cmdlet Creates a new rule for given subscription.</span></span>

## <span data-ttu-id="9c476-107">示例</span><span class="sxs-lookup"><span data-stu-id="9c476-107">EXAMPLES</span></span>

### <span data-ttu-id="9c476-108">範例1</span><span class="sxs-lookup"><span data-stu-id="9c476-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -SqlExpression "mysqlexpression='test'"
```

<span data-ttu-id="9c476-109">New-AzureRmServiceBusRule Cmdlet 會為指定的訂閱建立新的規則。</span><span class="sxs-lookup"><span data-stu-id="9c476-109">The New-AzureRmServiceBusRule cmdlet creates a new rule for the specified Subscription.</span></span>

## <span data-ttu-id="9c476-110">參數</span><span class="sxs-lookup"><span data-stu-id="9c476-110">PARAMETERS</span></span>

### <span data-ttu-id="9c476-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c476-111">-DefaultProfile</span></span>
<span data-ttu-id="9c476-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9c476-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c476-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="9c476-113">-Name</span></span>
<span data-ttu-id="9c476-114">規則名稱</span><span class="sxs-lookup"><span data-stu-id="9c476-114">Rule Name</span></span>

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

### <span data-ttu-id="9c476-115">-命名空間</span><span class="sxs-lookup"><span data-stu-id="9c476-115">-Namespace</span></span>
<span data-ttu-id="9c476-116">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="9c476-116">Namespace Name.</span></span>

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

### <span data-ttu-id="9c476-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c476-117">-ResourceGroupName</span></span>
<span data-ttu-id="9c476-118">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="9c476-118">The name of the resource group</span></span>

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

### <span data-ttu-id="9c476-119">-SqlExpression</span><span class="sxs-lookup"><span data-stu-id="9c476-119">-SqlExpression</span></span>
<span data-ttu-id="9c476-120">Sql Fillter 運算式</span><span class="sxs-lookup"><span data-stu-id="9c476-120">Sql Fillter Expression</span></span>

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

### <span data-ttu-id="9c476-121">-訂閱</span><span class="sxs-lookup"><span data-stu-id="9c476-121">-Subscription</span></span>
<span data-ttu-id="9c476-122">訂閱名稱</span><span class="sxs-lookup"><span data-stu-id="9c476-122">Subscription Name</span></span>

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

### <span data-ttu-id="9c476-123">-主題</span><span class="sxs-lookup"><span data-stu-id="9c476-123">-Topic</span></span>
<span data-ttu-id="9c476-124">主題名稱。</span><span class="sxs-lookup"><span data-stu-id="9c476-124">Topic Name.</span></span>

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

### <span data-ttu-id="9c476-125">-確認</span><span class="sxs-lookup"><span data-stu-id="9c476-125">-Confirm</span></span>
<span data-ttu-id="9c476-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9c476-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c476-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c476-127">-WhatIf</span></span>
<span data-ttu-id="9c476-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9c476-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c476-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9c476-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c476-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c476-130">CommonParameters</span></span>
<span data-ttu-id="9c476-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9c476-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c476-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9c476-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c476-133">輸入</span><span class="sxs-lookup"><span data-stu-id="9c476-133">INPUTS</span></span>

### <span data-ttu-id="9c476-134">System.object</span><span class="sxs-lookup"><span data-stu-id="9c476-134">System.String</span></span>

## <span data-ttu-id="9c476-135">輸出</span><span class="sxs-lookup"><span data-stu-id="9c476-135">OUTPUTS</span></span>

### <span data-ttu-id="9c476-136">PSRulesAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="9c476-136">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="9c476-137">筆記</span><span class="sxs-lookup"><span data-stu-id="9c476-137">NOTES</span></span>

## <span data-ttu-id="9c476-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="9c476-138">RELATED LINKS</span></span>

