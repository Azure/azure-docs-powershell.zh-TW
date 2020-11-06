---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueueAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueueAuthorizationRule.md
ms.openlocfilehash: 098c61be4eaf405d3c3a031601b48f20de1e234a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446661"
---
# <span data-ttu-id="138c8-101">New-AzureRmServiceBusQueueAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="138c8-101">New-AzureRmServiceBusQueueAuthorizationRule</span></span>

## <span data-ttu-id="138c8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="138c8-102">SYNOPSIS</span></span>
<span data-ttu-id="138c8-103">針對指定的服務匯流排佇列建立新的授權規則。</span><span class="sxs-lookup"><span data-stu-id="138c8-103">Creates a new authorization rule for the specified Service Bus queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="138c8-104">句法</span><span class="sxs-lookup"><span data-stu-id="138c8-104">SYNTAX</span></span>

```
New-AzureRmServiceBusQueueAuthorizationRule [-ResourceGroup] <String> -Namespace <String> -Queue <String>
 -Name <String> [-Rights] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="138c8-105">說明</span><span class="sxs-lookup"><span data-stu-id="138c8-105">DESCRIPTION</span></span>
<span data-ttu-id="138c8-106">**新的-AzureRmServiceBusQueueAuthorizationRule** Cmdlet 會為指定的服務匯流排佇列建立新的授權規則。</span><span class="sxs-lookup"><span data-stu-id="138c8-106">The **New-AzureRmServiceBusQueueAuthorizationRule** cmdlet creates a new authorization rule for the specified Service Bus queue.</span></span>

## <span data-ttu-id="138c8-107">示例</span><span class="sxs-lookup"><span data-stu-id="138c8-107">EXAMPLES</span></span>

### <span data-ttu-id="138c8-108">範例1</span><span class="sxs-lookup"><span data-stu-id="138c8-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusQueueAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthorizationRuleName SBAuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="138c8-109">`SBAuthoRule1`使用佇列的 [ **偵聽] 和 [傳送** ] 許可權建立授權規則 `SB-Queue_exampl1` 。</span><span class="sxs-lookup"><span data-stu-id="138c8-109">Creates authorization rule `SBAuthoRule1` with **Listen and Send** rights for the queue `SB-Queue_exampl1`.</span></span>

## <span data-ttu-id="138c8-110">參數</span><span class="sxs-lookup"><span data-stu-id="138c8-110">PARAMETERS</span></span>

### <span data-ttu-id="138c8-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="138c8-111">-ResourceGroup</span></span>
<span data-ttu-id="138c8-112">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="138c8-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="138c8-113">-許可權</span><span class="sxs-lookup"><span data-stu-id="138c8-113">-Rights</span></span>
<span data-ttu-id="138c8-114">指定許可權;例如，</span><span class="sxs-lookup"><span data-stu-id="138c8-114">Specifies the rights; for example,</span></span>  
<span data-ttu-id="138c8-115">@ ( 「聆聽」、「傳送」、「管理」 ) </span><span class="sxs-lookup"><span data-stu-id="138c8-115">@("Listen","Send","Manage")</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="138c8-116">-確認</span><span class="sxs-lookup"><span data-stu-id="138c8-116">-Confirm</span></span>
<span data-ttu-id="138c8-117">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="138c8-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="138c8-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="138c8-118">-WhatIf</span></span>
<span data-ttu-id="138c8-119">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="138c8-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="138c8-120">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="138c8-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="138c8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="138c8-121">-DefaultProfile</span></span>
<span data-ttu-id="138c8-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="138c8-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="138c8-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="138c8-123">-Name</span></span>
<span data-ttu-id="138c8-124">AuthorizationRule [名稱]。</span><span class="sxs-lookup"><span data-stu-id="138c8-124">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="138c8-125">-命名空間</span><span class="sxs-lookup"><span data-stu-id="138c8-125">-Namespace</span></span>
<span data-ttu-id="138c8-126">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="138c8-126">Namespace Name.</span></span>

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

### <span data-ttu-id="138c8-127">-佇列</span><span class="sxs-lookup"><span data-stu-id="138c8-127">-Queue</span></span>
<span data-ttu-id="138c8-128">佇列名稱。</span><span class="sxs-lookup"><span data-stu-id="138c8-128">Queue Name.</span></span>

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

### <span data-ttu-id="138c8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="138c8-129">CommonParameters</span></span>
<span data-ttu-id="138c8-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="138c8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="138c8-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="138c8-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="138c8-132">輸入</span><span class="sxs-lookup"><span data-stu-id="138c8-132">INPUTS</span></span>

### <span data-ttu-id="138c8-133">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="138c8-133">-ResourceGroup</span></span>
 <span data-ttu-id="138c8-134">System.object</span><span class="sxs-lookup"><span data-stu-id="138c8-134">System.String</span></span>
 

### <span data-ttu-id="138c8-135">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="138c8-135">-NamespaceName</span></span>
 <span data-ttu-id="138c8-136">System.object</span><span class="sxs-lookup"><span data-stu-id="138c8-136">System.String</span></span>
 

### <span data-ttu-id="138c8-137">-QueueName</span><span class="sxs-lookup"><span data-stu-id="138c8-137">-QueueName</span></span>
 <span data-ttu-id="138c8-138">System.object</span><span class="sxs-lookup"><span data-stu-id="138c8-138">System.String</span></span>
 

### <span data-ttu-id="138c8-139">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="138c8-139">-AuthorizationRuleName</span></span>
 <span data-ttu-id="138c8-140">System.object</span><span class="sxs-lookup"><span data-stu-id="138c8-140">System.String</span></span>

## <span data-ttu-id="138c8-141">輸出</span><span class="sxs-lookup"><span data-stu-id="138c8-141">OUTPUTS</span></span>

### <span data-ttu-id="138c8-142">SharedAccessAuthorizationRuleAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="138c8-142">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>
<span data-ttu-id="138c8-143">識別碼：/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/SB-Queue_exampl1/authorizati onRules/SBAuthoRule1 類型： AuthorizationRules Name： SBAuthoRule1 Location：西美式標籤：許可權： {偵聽、傳送}</span><span class="sxs-lookup"><span data-stu-id="138c8-143">Id       : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/SB-Queue_exampl1/authorizati onRules/SBAuthoRule1 Type     : Microsoft.ServiceBus/AuthorizationRules Name     : SBAuthoRule1 Location : West US Tags     : Rights   : {Listen, Send}</span></span>

## <span data-ttu-id="138c8-144">筆記</span><span class="sxs-lookup"><span data-stu-id="138c8-144">NOTES</span></span>

## <span data-ttu-id="138c8-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="138c8-145">RELATED LINKS</span></span>

