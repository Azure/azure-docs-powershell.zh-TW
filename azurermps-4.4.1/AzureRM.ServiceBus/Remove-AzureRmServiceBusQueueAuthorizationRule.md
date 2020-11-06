---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusQueueAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusQueueAuthorizationRule.md
ms.openlocfilehash: 93efa23e802c3470d1bd1470cadd0f070cc34422
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447984"
---
# <span data-ttu-id="7e608-101">Remove-AzureRmServiceBusQueueAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="7e608-101">Remove-AzureRmServiceBusQueueAuthorizationRule</span></span>

## <span data-ttu-id="7e608-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7e608-102">SYNOPSIS</span></span>
<span data-ttu-id="7e608-103">從指定的服務匯流排命名空間移除佇列的授權規則。</span><span class="sxs-lookup"><span data-stu-id="7e608-103">Removes the authorization rule of a queue from the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e608-104">句法</span><span class="sxs-lookup"><span data-stu-id="7e608-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusQueueAuthorizationRule [-ResourceGroup] <String> -Namespace <String> -Queue <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e608-105">說明</span><span class="sxs-lookup"><span data-stu-id="7e608-105">DESCRIPTION</span></span>
<span data-ttu-id="7e608-106">**AzureRmServiceBusQueueAuthorizationRule** Cmdlet 會從指定的服務匯流排命名空間中移除佇列的授權規則。</span><span class="sxs-lookup"><span data-stu-id="7e608-106">The **Remove-AzureRmServiceBusQueueAuthorizationRule** cmdlet removes the authorization rule of a queue from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="7e608-107">示例</span><span class="sxs-lookup"><span data-stu-id="7e608-107">EXAMPLES</span></span>

### <span data-ttu-id="7e608-108">範例1</span><span class="sxs-lookup"><span data-stu-id="7e608-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusQueueAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthorizationRuleName SBAuthoRule1
```

<span data-ttu-id="7e608-109">`SBAuthoRule1`從命名空間移除佇列的授權規則 `SB-Queue_exampl1` `SB-Example1` 。</span><span class="sxs-lookup"><span data-stu-id="7e608-109">Removes the authorization rule `SBAuthoRule1` of the queue `SB-Queue_exampl1` from the namespace `SB-Example1`.</span></span>

## <span data-ttu-id="7e608-110">參數</span><span class="sxs-lookup"><span data-stu-id="7e608-110">PARAMETERS</span></span>

### <span data-ttu-id="7e608-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7e608-111">-ResourceGroup</span></span>
<span data-ttu-id="7e608-112">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7e608-112">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e608-113">-確認</span><span class="sxs-lookup"><span data-stu-id="7e608-113">-Confirm</span></span>
<span data-ttu-id="7e608-114">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7e608-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e608-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e608-115">-WhatIf</span></span>
<span data-ttu-id="7e608-116">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7e608-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e608-117">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7e608-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e608-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e608-118">-DefaultProfile</span></span>
<span data-ttu-id="7e608-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7e608-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e608-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="7e608-120">-Name</span></span>
<span data-ttu-id="7e608-121">[佇列 AuthorizationRule] 名稱。</span><span class="sxs-lookup"><span data-stu-id="7e608-121">Queue AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e608-122">-命名空間</span><span class="sxs-lookup"><span data-stu-id="7e608-122">-Namespace</span></span>
<span data-ttu-id="7e608-123">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="7e608-123">Namespace Name.</span></span>

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

### <span data-ttu-id="7e608-124">-佇列</span><span class="sxs-lookup"><span data-stu-id="7e608-124">-Queue</span></span>
<span data-ttu-id="7e608-125">佇列名稱。</span><span class="sxs-lookup"><span data-stu-id="7e608-125">Queue Name.</span></span>

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

### <span data-ttu-id="7e608-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e608-126">CommonParameters</span></span>
<span data-ttu-id="7e608-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7e608-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e608-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7e608-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e608-129">輸入</span><span class="sxs-lookup"><span data-stu-id="7e608-129">INPUTS</span></span>

### <span data-ttu-id="7e608-130">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7e608-130">-ResourceGroup</span></span>
 <span data-ttu-id="7e608-131">System.object</span><span class="sxs-lookup"><span data-stu-id="7e608-131">System.String</span></span>

### <span data-ttu-id="7e608-132">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="7e608-132">-NamespaceName</span></span>
 <span data-ttu-id="7e608-133">System.object</span><span class="sxs-lookup"><span data-stu-id="7e608-133">System.String</span></span>

### <span data-ttu-id="7e608-134">-QueueName</span><span class="sxs-lookup"><span data-stu-id="7e608-134">-QueueName</span></span>
 <span data-ttu-id="7e608-135">System.object</span><span class="sxs-lookup"><span data-stu-id="7e608-135">System.String</span></span>

### <span data-ttu-id="7e608-136">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="7e608-136">-AuthorizationRuleName</span></span>
 <span data-ttu-id="7e608-137">System.object</span><span class="sxs-lookup"><span data-stu-id="7e608-137">System.String</span></span>

## <span data-ttu-id="7e608-138">輸出</span><span class="sxs-lookup"><span data-stu-id="7e608-138">OUTPUTS</span></span>

### <span data-ttu-id="7e608-139">System.object</span><span class="sxs-lookup"><span data-stu-id="7e608-139">System.Object</span></span>

## <span data-ttu-id="7e608-140">筆記</span><span class="sxs-lookup"><span data-stu-id="7e608-140">NOTES</span></span>

## <span data-ttu-id="7e608-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="7e608-141">RELATED LINKS</span></span>

