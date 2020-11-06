---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusQueue.md
ms.openlocfilehash: 28c6bf4d463331755121e8a1ea14bf7f93407017
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450484"
---
# <span data-ttu-id="6e495-101">Remove-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="6e495-101">Remove-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="6e495-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6e495-102">SYNOPSIS</span></span>
<span data-ttu-id="6e495-103">從指定的服務匯流排命名空間中移除佇列。</span><span class="sxs-lookup"><span data-stu-id="6e495-103">Removes the queue from the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6e495-104">句法</span><span class="sxs-lookup"><span data-stu-id="6e495-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e495-105">說明</span><span class="sxs-lookup"><span data-stu-id="6e495-105">DESCRIPTION</span></span>
<span data-ttu-id="6e495-106">**AzureRmServiceBusQueue** Cmdlet 會從指定的服務匯流排命名空間中移除佇列。</span><span class="sxs-lookup"><span data-stu-id="6e495-106">The **Remove-AzureRmServiceBusQueue** cmdlet removes the queue from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="6e495-107">示例</span><span class="sxs-lookup"><span data-stu-id="6e495-107">EXAMPLES</span></span>

### <span data-ttu-id="6e495-108">範例1</span><span class="sxs-lookup"><span data-stu-id="6e495-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1
```

<span data-ttu-id="6e495-109">`SB-Queue_exampl1`從命名空間移除佇列 `SB-Example1` 。</span><span class="sxs-lookup"><span data-stu-id="6e495-109">Removes the queue `SB-Queue_exampl1` from the namespace `SB-Example1`.</span></span>

## <span data-ttu-id="6e495-110">參數</span><span class="sxs-lookup"><span data-stu-id="6e495-110">PARAMETERS</span></span>

### <span data-ttu-id="6e495-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e495-111">-DefaultProfile</span></span>
<span data-ttu-id="6e495-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6e495-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6e495-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="6e495-113">-Name</span></span>
<span data-ttu-id="6e495-114">佇列名稱。</span><span class="sxs-lookup"><span data-stu-id="6e495-114">Queue Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e495-115">-命名空間</span><span class="sxs-lookup"><span data-stu-id="6e495-115">-Namespace</span></span>
<span data-ttu-id="6e495-116">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="6e495-116">Namespace Name.</span></span>

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

### <span data-ttu-id="6e495-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e495-117">-ResourceGroupName</span></span>
<span data-ttu-id="6e495-118">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="6e495-118">The name of the resource group</span></span>

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

### <span data-ttu-id="6e495-119">-確認</span><span class="sxs-lookup"><span data-stu-id="6e495-119">-Confirm</span></span>
<span data-ttu-id="6e495-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6e495-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e495-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e495-121">-WhatIf</span></span>
<span data-ttu-id="6e495-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6e495-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e495-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6e495-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e495-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e495-124">CommonParameters</span></span>
<span data-ttu-id="6e495-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6e495-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e495-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6e495-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e495-127">輸入</span><span class="sxs-lookup"><span data-stu-id="6e495-127">INPUTS</span></span>

### <span data-ttu-id="6e495-128">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6e495-128">-ResourceGroup</span></span>
 <span data-ttu-id="6e495-129">System.object</span><span class="sxs-lookup"><span data-stu-id="6e495-129">System.String</span></span>

### <span data-ttu-id="6e495-130">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="6e495-130">-NamespaceName</span></span>
 <span data-ttu-id="6e495-131">System.object</span><span class="sxs-lookup"><span data-stu-id="6e495-131">System.String</span></span>

### <span data-ttu-id="6e495-132">-QueueName</span><span class="sxs-lookup"><span data-stu-id="6e495-132">-QueueName</span></span>
 <span data-ttu-id="6e495-133">System.object</span><span class="sxs-lookup"><span data-stu-id="6e495-133">System.String</span></span>

## <span data-ttu-id="6e495-134">輸出</span><span class="sxs-lookup"><span data-stu-id="6e495-134">OUTPUTS</span></span>

### <span data-ttu-id="6e495-135">System.object</span><span class="sxs-lookup"><span data-stu-id="6e495-135">System.Object</span></span>

## <span data-ttu-id="6e495-136">筆記</span><span class="sxs-lookup"><span data-stu-id="6e495-136">NOTES</span></span>

## <span data-ttu-id="6e495-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="6e495-137">RELATED LINKS</span></span>

