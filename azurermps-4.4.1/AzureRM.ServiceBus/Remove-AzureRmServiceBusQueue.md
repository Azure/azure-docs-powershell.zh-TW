---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusQueue.md
ms.openlocfilehash: 8c5c614a041ff0e4ab9bc4fdc0aea944901d1efc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447983"
---
# <span data-ttu-id="58c6c-101">Remove-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="58c6c-101">Remove-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="58c6c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="58c6c-102">SYNOPSIS</span></span>
<span data-ttu-id="58c6c-103">從指定的服務匯流排命名空間中移除佇列。</span><span class="sxs-lookup"><span data-stu-id="58c6c-103">Removes the queue from the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58c6c-104">句法</span><span class="sxs-lookup"><span data-stu-id="58c6c-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusQueue -ResourceGroupName <String> -Namespace <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58c6c-105">說明</span><span class="sxs-lookup"><span data-stu-id="58c6c-105">DESCRIPTION</span></span>
<span data-ttu-id="58c6c-106">**AzureRmServiceBusQueue** Cmdlet 會從指定的服務匯流排命名空間中移除佇列。</span><span class="sxs-lookup"><span data-stu-id="58c6c-106">The **Remove-AzureRmServiceBusQueue** cmdlet removes the queue from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="58c6c-107">示例</span><span class="sxs-lookup"><span data-stu-id="58c6c-107">EXAMPLES</span></span>

### <span data-ttu-id="58c6c-108">範例1</span><span class="sxs-lookup"><span data-stu-id="58c6c-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1
```

<span data-ttu-id="58c6c-109">`SB-Queue_exampl1`從命名空間移除佇列 `SB-Example1` 。</span><span class="sxs-lookup"><span data-stu-id="58c6c-109">Removes the queue `SB-Queue_exampl1` from the namespace `SB-Example1`.</span></span>

## <span data-ttu-id="58c6c-110">參數</span><span class="sxs-lookup"><span data-stu-id="58c6c-110">PARAMETERS</span></span>

### <span data-ttu-id="58c6c-111">-確認</span><span class="sxs-lookup"><span data-stu-id="58c6c-111">-Confirm</span></span>
<span data-ttu-id="58c6c-112">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="58c6c-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58c6c-113">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58c6c-113">-WhatIf</span></span>
<span data-ttu-id="58c6c-114">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="58c6c-114">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58c6c-115">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="58c6c-115">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58c6c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58c6c-116">-DefaultProfile</span></span>
<span data-ttu-id="58c6c-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="58c6c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58c6c-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="58c6c-118">-Name</span></span>
<span data-ttu-id="58c6c-119">佇列名稱。</span><span class="sxs-lookup"><span data-stu-id="58c6c-119">Queue Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58c6c-120">-命名空間</span><span class="sxs-lookup"><span data-stu-id="58c6c-120">-Namespace</span></span>
<span data-ttu-id="58c6c-121">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="58c6c-121">Namespace Name.</span></span>

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

### <span data-ttu-id="58c6c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58c6c-122">-ResourceGroupName</span></span>
<span data-ttu-id="58c6c-123">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="58c6c-123">The name of the resource group</span></span>

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

### <span data-ttu-id="58c6c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58c6c-124">CommonParameters</span></span>
<span data-ttu-id="58c6c-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="58c6c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58c6c-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="58c6c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58c6c-127">輸入</span><span class="sxs-lookup"><span data-stu-id="58c6c-127">INPUTS</span></span>

### <span data-ttu-id="58c6c-128">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="58c6c-128">-ResourceGroup</span></span>
 <span data-ttu-id="58c6c-129">System.object</span><span class="sxs-lookup"><span data-stu-id="58c6c-129">System.String</span></span>

### <span data-ttu-id="58c6c-130">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="58c6c-130">-NamespaceName</span></span>
 <span data-ttu-id="58c6c-131">System.object</span><span class="sxs-lookup"><span data-stu-id="58c6c-131">System.String</span></span>

### <span data-ttu-id="58c6c-132">-QueueName</span><span class="sxs-lookup"><span data-stu-id="58c6c-132">-QueueName</span></span>
 <span data-ttu-id="58c6c-133">System.object</span><span class="sxs-lookup"><span data-stu-id="58c6c-133">System.String</span></span>

## <span data-ttu-id="58c6c-134">輸出</span><span class="sxs-lookup"><span data-stu-id="58c6c-134">OUTPUTS</span></span>

### <span data-ttu-id="58c6c-135">System.object</span><span class="sxs-lookup"><span data-stu-id="58c6c-135">System.Object</span></span>

## <span data-ttu-id="58c6c-136">筆記</span><span class="sxs-lookup"><span data-stu-id="58c6c-136">NOTES</span></span>

## <span data-ttu-id="58c6c-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="58c6c-137">RELATED LINKS</span></span>

