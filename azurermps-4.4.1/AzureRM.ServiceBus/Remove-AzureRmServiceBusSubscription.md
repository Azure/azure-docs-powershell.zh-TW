---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusSubscription.md
ms.openlocfilehash: c3d4ca61f0bbdc5dcea2eb41a9da0f5de1112719
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447980"
---
# <span data-ttu-id="27f59-101">Remove-AzureRmServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="27f59-101">Remove-AzureRmServiceBusSubscription</span></span>

## <span data-ttu-id="27f59-102">摘要</span><span class="sxs-lookup"><span data-stu-id="27f59-102">SYNOPSIS</span></span>
<span data-ttu-id="27f59-103">從指定的服務匯流排命名空間移除主題的訂閱。</span><span class="sxs-lookup"><span data-stu-id="27f59-103">Removes the subscription to a topic from the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="27f59-104">句法</span><span class="sxs-lookup"><span data-stu-id="27f59-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusSubscription -ResourceGroupName <String> -Namespace <String> -Topic <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27f59-105">說明</span><span class="sxs-lookup"><span data-stu-id="27f59-105">DESCRIPTION</span></span>
<span data-ttu-id="27f59-106">**AzureRmServiceBusSubscription** Cmdlet 會從指定的服務匯流排命名空間中移除主題的訂閱。</span><span class="sxs-lookup"><span data-stu-id="27f59-106">The **Remove-AzureRmServiceBusSubscription** cmdlet removes the subscription to a topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="27f59-107">示例</span><span class="sxs-lookup"><span data-stu-id="27f59-107">EXAMPLES</span></span>

### <span data-ttu-id="27f59-108">範例1</span><span class="sxs-lookup"><span data-stu-id="27f59-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1
```

<span data-ttu-id="27f59-109">移除 `SB-TopicSubscription-Example1` `SB-Topic_exampl1` 指定服務匯流排命名空間中主題的訂閱 `SB-Example1` 。</span><span class="sxs-lookup"><span data-stu-id="27f59-109">Removes the subscription `SB-TopicSubscription-Example1` to the topic `SB-Topic_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

## <span data-ttu-id="27f59-110">參數</span><span class="sxs-lookup"><span data-stu-id="27f59-110">PARAMETERS</span></span>

### <span data-ttu-id="27f59-111">-確認</span><span class="sxs-lookup"><span data-stu-id="27f59-111">-Confirm</span></span>
<span data-ttu-id="27f59-112">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="27f59-112">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27f59-113">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27f59-113">-WhatIf</span></span>
<span data-ttu-id="27f59-114">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="27f59-114">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27f59-115">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="27f59-115">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27f59-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27f59-116">-DefaultProfile</span></span>
<span data-ttu-id="27f59-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="27f59-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="27f59-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="27f59-118">-Name</span></span>
<span data-ttu-id="27f59-119">訂閱名稱。</span><span class="sxs-lookup"><span data-stu-id="27f59-119">Subscription Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27f59-120">-命名空間</span><span class="sxs-lookup"><span data-stu-id="27f59-120">-Namespace</span></span>
<span data-ttu-id="27f59-121">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="27f59-121">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27f59-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27f59-122">-ResourceGroupName</span></span>
<span data-ttu-id="27f59-123">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="27f59-123">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27f59-124">-主題</span><span class="sxs-lookup"><span data-stu-id="27f59-124">-Topic</span></span>
<span data-ttu-id="27f59-125">主題名稱。</span><span class="sxs-lookup"><span data-stu-id="27f59-125">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27f59-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27f59-126">CommonParameters</span></span>
<span data-ttu-id="27f59-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="27f59-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27f59-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="27f59-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27f59-129">輸入</span><span class="sxs-lookup"><span data-stu-id="27f59-129">INPUTS</span></span>

### <span data-ttu-id="27f59-130">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="27f59-130">-ResourceGroup</span></span>
 <span data-ttu-id="27f59-131">System.object</span><span class="sxs-lookup"><span data-stu-id="27f59-131">System.String</span></span>

### <span data-ttu-id="27f59-132">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="27f59-132">-NamespaceName</span></span>
 <span data-ttu-id="27f59-133">System.object</span><span class="sxs-lookup"><span data-stu-id="27f59-133">System.String</span></span>

### <span data-ttu-id="27f59-134">-TopicName</span><span class="sxs-lookup"><span data-stu-id="27f59-134">-TopicName</span></span>
 <span data-ttu-id="27f59-135">System.object</span><span class="sxs-lookup"><span data-stu-id="27f59-135">System.String</span></span>

### <span data-ttu-id="27f59-136">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="27f59-136">-SubscriptionName</span></span>
 <span data-ttu-id="27f59-137">System.object</span><span class="sxs-lookup"><span data-stu-id="27f59-137">System.String</span></span>

## <span data-ttu-id="27f59-138">輸出</span><span class="sxs-lookup"><span data-stu-id="27f59-138">OUTPUTS</span></span>

### <span data-ttu-id="27f59-139">System.object</span><span class="sxs-lookup"><span data-stu-id="27f59-139">System.Boolean</span></span>

## <span data-ttu-id="27f59-140">筆記</span><span class="sxs-lookup"><span data-stu-id="27f59-140">NOTES</span></span>

## <span data-ttu-id="27f59-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="27f59-141">RELATED LINKS</span></span>

