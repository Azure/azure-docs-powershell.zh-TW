---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusRule.md
ms.openlocfilehash: 08f3fb2654d4c0b64900a4f15bbb7816e6d44c6f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450485"
---
# <span data-ttu-id="eb312-101">Remove-AzureRmServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="eb312-101">Remove-AzureRmServiceBusRule</span></span>

## <span data-ttu-id="eb312-102">摘要</span><span class="sxs-lookup"><span data-stu-id="eb312-102">SYNOPSIS</span></span>
<span data-ttu-id="eb312-103">移除指定訂閱的指定規則。</span><span class="sxs-lookup"><span data-stu-id="eb312-103">Removes the speficied rule of a given subscription .</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb312-104">句法</span><span class="sxs-lookup"><span data-stu-id="eb312-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb312-105">說明</span><span class="sxs-lookup"><span data-stu-id="eb312-105">DESCRIPTION</span></span>
<span data-ttu-id="eb312-106">**AzureRmServiceBusRule** Cmdlet 會移除指定主題的訂閱規則。</span><span class="sxs-lookup"><span data-stu-id="eb312-106">The **Remove-AzureRmServiceBusRule** cmdlet removes the rule of a subscription of given topic.</span></span>

## <span data-ttu-id="eb312-107">示例</span><span class="sxs-lookup"><span data-stu-id="eb312-107">EXAMPLES</span></span>

### <span data-ttu-id="eb312-108">範例1</span><span class="sxs-lookup"><span data-stu-id="eb312-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
```

<span data-ttu-id="eb312-109">移除 `SBRule` 指定主題的訂閱規則 `SBSubscription` `SBTopic` 。</span><span class="sxs-lookup"><span data-stu-id="eb312-109">Removes the rule `SBRule` of subscription `SBSubscription` of specified topic `SBTopic`.</span></span>

## <span data-ttu-id="eb312-110">參數</span><span class="sxs-lookup"><span data-stu-id="eb312-110">PARAMETERS</span></span>

### <span data-ttu-id="eb312-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb312-111">-DefaultProfile</span></span>
<span data-ttu-id="eb312-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="eb312-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb312-113">-Force</span><span class="sxs-lookup"><span data-stu-id="eb312-113">-Force</span></span>
<span data-ttu-id="eb312-114">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="eb312-114">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb312-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="eb312-115">-Name</span></span>
<span data-ttu-id="eb312-116">規則名稱。</span><span class="sxs-lookup"><span data-stu-id="eb312-116">Rule Name.</span></span>

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

### <span data-ttu-id="eb312-117">-命名空間</span><span class="sxs-lookup"><span data-stu-id="eb312-117">-Namespace</span></span>
<span data-ttu-id="eb312-118">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="eb312-118">Namespace Name.</span></span>

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

### <span data-ttu-id="eb312-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eb312-119">-PassThru</span></span>
<span data-ttu-id="eb312-120">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="eb312-120">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb312-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb312-121">-ResourceGroupName</span></span>
<span data-ttu-id="eb312-122">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="eb312-122">The name of the resource group</span></span>

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

### <span data-ttu-id="eb312-123">-訂閱</span><span class="sxs-lookup"><span data-stu-id="eb312-123">-Subscription</span></span>
<span data-ttu-id="eb312-124">訂閱名稱。</span><span class="sxs-lookup"><span data-stu-id="eb312-124">Subscription Name.</span></span>

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

### <span data-ttu-id="eb312-125">-主題</span><span class="sxs-lookup"><span data-stu-id="eb312-125">-Topic</span></span>
<span data-ttu-id="eb312-126">主題名稱。</span><span class="sxs-lookup"><span data-stu-id="eb312-126">Topic Name.</span></span>

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

### <span data-ttu-id="eb312-127">-確認</span><span class="sxs-lookup"><span data-stu-id="eb312-127">-Confirm</span></span>
<span data-ttu-id="eb312-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="eb312-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb312-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb312-129">-WhatIf</span></span>
<span data-ttu-id="eb312-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="eb312-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb312-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="eb312-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb312-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb312-132">CommonParameters</span></span>
<span data-ttu-id="eb312-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="eb312-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb312-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="eb312-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb312-135">輸入</span><span class="sxs-lookup"><span data-stu-id="eb312-135">INPUTS</span></span>

### <span data-ttu-id="eb312-136">System.object</span><span class="sxs-lookup"><span data-stu-id="eb312-136">System.String</span></span>

## <span data-ttu-id="eb312-137">輸出</span><span class="sxs-lookup"><span data-stu-id="eb312-137">OUTPUTS</span></span>

### <span data-ttu-id="eb312-138">System.object</span><span class="sxs-lookup"><span data-stu-id="eb312-138">System.Boolean</span></span>

## <span data-ttu-id="eb312-139">筆記</span><span class="sxs-lookup"><span data-stu-id="eb312-139">NOTES</span></span>

## <span data-ttu-id="eb312-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="eb312-140">RELATED LINKS</span></span>

