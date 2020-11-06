---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusSubscription.md
ms.openlocfilehash: 80b3a5ce4cb38222993e69181519a864c578cf67
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454072"
---
# <span data-ttu-id="baf2f-101">Remove-AzureRmServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="baf2f-101">Remove-AzureRmServiceBusSubscription</span></span>

## <span data-ttu-id="baf2f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="baf2f-102">SYNOPSIS</span></span>
<span data-ttu-id="baf2f-103">從指定的服務匯流排命名空間移除主題的訂閱。</span><span class="sxs-lookup"><span data-stu-id="baf2f-103">Removes the subscription to a topic from the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="baf2f-104">句法</span><span class="sxs-lookup"><span data-stu-id="baf2f-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="baf2f-105">說明</span><span class="sxs-lookup"><span data-stu-id="baf2f-105">DESCRIPTION</span></span>
<span data-ttu-id="baf2f-106">**AzureRmServiceBusSubscription** Cmdlet 會從指定的服務匯流排命名空間中移除主題的訂閱。</span><span class="sxs-lookup"><span data-stu-id="baf2f-106">The **Remove-AzureRmServiceBusSubscription** cmdlet removes the subscription to a topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="baf2f-107">示例</span><span class="sxs-lookup"><span data-stu-id="baf2f-107">EXAMPLES</span></span>

### <span data-ttu-id="baf2f-108">範例1</span><span class="sxs-lookup"><span data-stu-id="baf2f-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1
```

<span data-ttu-id="baf2f-109">移除 `SB-TopicSubscription-Example1` `SB-Topic_exampl1` 指定服務匯流排命名空間中主題的訂閱 `SB-Example1` 。</span><span class="sxs-lookup"><span data-stu-id="baf2f-109">Removes the subscription `SB-TopicSubscription-Example1` to the topic `SB-Topic_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

## <span data-ttu-id="baf2f-110">參數</span><span class="sxs-lookup"><span data-stu-id="baf2f-110">PARAMETERS</span></span>

### <span data-ttu-id="baf2f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="baf2f-111">-DefaultProfile</span></span>
<span data-ttu-id="baf2f-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="baf2f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="baf2f-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="baf2f-113">-Name</span></span>
<span data-ttu-id="baf2f-114">訂閱名稱。</span><span class="sxs-lookup"><span data-stu-id="baf2f-114">Subscription Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="baf2f-115">-命名空間</span><span class="sxs-lookup"><span data-stu-id="baf2f-115">-Namespace</span></span>
<span data-ttu-id="baf2f-116">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="baf2f-116">Namespace Name.</span></span>

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

### <span data-ttu-id="baf2f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="baf2f-117">-ResourceGroupName</span></span>
<span data-ttu-id="baf2f-118">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="baf2f-118">The name of the resource group</span></span>

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

### <span data-ttu-id="baf2f-119">-主題</span><span class="sxs-lookup"><span data-stu-id="baf2f-119">-Topic</span></span>
<span data-ttu-id="baf2f-120">主題名稱。</span><span class="sxs-lookup"><span data-stu-id="baf2f-120">Topic Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="baf2f-121">-確認</span><span class="sxs-lookup"><span data-stu-id="baf2f-121">-Confirm</span></span>
<span data-ttu-id="baf2f-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="baf2f-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="baf2f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="baf2f-123">-WhatIf</span></span>
<span data-ttu-id="baf2f-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="baf2f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="baf2f-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="baf2f-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="baf2f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="baf2f-126">CommonParameters</span></span>
<span data-ttu-id="baf2f-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="baf2f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="baf2f-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="baf2f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="baf2f-129">輸入</span><span class="sxs-lookup"><span data-stu-id="baf2f-129">INPUTS</span></span>

### <span data-ttu-id="baf2f-130">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="baf2f-130">-ResourceGroup</span></span>
 <span data-ttu-id="baf2f-131">System.object</span><span class="sxs-lookup"><span data-stu-id="baf2f-131">System.String</span></span>

### <span data-ttu-id="baf2f-132">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="baf2f-132">-NamespaceName</span></span>
 <span data-ttu-id="baf2f-133">System.object</span><span class="sxs-lookup"><span data-stu-id="baf2f-133">System.String</span></span>

### <span data-ttu-id="baf2f-134">-TopicName</span><span class="sxs-lookup"><span data-stu-id="baf2f-134">-TopicName</span></span>
 <span data-ttu-id="baf2f-135">System.object</span><span class="sxs-lookup"><span data-stu-id="baf2f-135">System.String</span></span>

### <span data-ttu-id="baf2f-136">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="baf2f-136">-SubscriptionName</span></span>
 <span data-ttu-id="baf2f-137">System.object</span><span class="sxs-lookup"><span data-stu-id="baf2f-137">System.String</span></span>

## <span data-ttu-id="baf2f-138">輸出</span><span class="sxs-lookup"><span data-stu-id="baf2f-138">OUTPUTS</span></span>

### <span data-ttu-id="baf2f-139">System.object</span><span class="sxs-lookup"><span data-stu-id="baf2f-139">System.Boolean</span></span>

## <span data-ttu-id="baf2f-140">筆記</span><span class="sxs-lookup"><span data-stu-id="baf2f-140">NOTES</span></span>

## <span data-ttu-id="baf2f-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="baf2f-141">RELATED LINKS</span></span>

