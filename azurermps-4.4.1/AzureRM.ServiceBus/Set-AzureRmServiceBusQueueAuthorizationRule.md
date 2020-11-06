---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusQueueAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusQueueAuthorizationRule.md
ms.openlocfilehash: 166b47a231b2ca6fc2cf74137212e60123f25445
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455592"
---
# <span data-ttu-id="2543f-101">Set-AzureRmServiceBusQueueAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="2543f-101">Set-AzureRmServiceBusQueueAuthorizationRule</span></span>

## <span data-ttu-id="2543f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2543f-102">SYNOPSIS</span></span>
<span data-ttu-id="2543f-103">更新特定服務匯流排佇列的指定授權規則描述。</span><span class="sxs-lookup"><span data-stu-id="2543f-103">Updates the specified authorization rule description for the given Service Bus queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2543f-104">句法</span><span class="sxs-lookup"><span data-stu-id="2543f-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusQueueAuthorizationRule [-ResourceGroup] <String> [-NamespaceName] <String>
 [-QueueName] <String> [-AuthRuleObj] <SharedAccessAuthorizationRuleAttributes>
 [[-AuthorizationRuleName] <String>] [[-Rights] <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2543f-105">說明</span><span class="sxs-lookup"><span data-stu-id="2543f-105">DESCRIPTION</span></span>
<span data-ttu-id="2543f-106">**AzureRmServiceBusQueueAuthorizationRule** Cmdlet 會更新特定服務匯流排佇列之指定授權規則的描述。</span><span class="sxs-lookup"><span data-stu-id="2543f-106">The **Set-AzureRmServiceBusQueueAuthorizationRule** cmdlet updates the description for the specified authorization rule of the given Service Bus queue.</span></span>

## <span data-ttu-id="2543f-107">示例</span><span class="sxs-lookup"><span data-stu-id="2543f-107">EXAMPLES</span></span>

### <span data-ttu-id="2543f-108">範例1</span><span class="sxs-lookup"><span data-stu-id="2543f-108">Example 1</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusQueueAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthorizationRuleName SBAuthoRule1

PS C:\> $authRuleObj.Rights.Add("Manage")

PS C:\> Set-AzureRmServiceBusQueueAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthRuleObj $authRuleObj
```

<span data-ttu-id="2543f-109">將 **管理** 新增到佇列授權規則的存取權限 `SBAuthoRule1` `SB-Queue_exampl1` 。</span><span class="sxs-lookup"><span data-stu-id="2543f-109">Adds **Manage** to the access rights of the authorization rule `SBAuthoRule1` of the queue `SB-Queue_exampl1`.</span></span>

## <span data-ttu-id="2543f-110">參數</span><span class="sxs-lookup"><span data-stu-id="2543f-110">PARAMETERS</span></span>

### <span data-ttu-id="2543f-111">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="2543f-111">-AuthorizationRuleName</span></span>
<span data-ttu-id="2543f-112">授權規則名稱。</span><span class="sxs-lookup"><span data-stu-id="2543f-112">The authorization rule name.</span></span> <span data-ttu-id="2543f-113">如果未指定 **-AuthruleObj** ，則為必要。</span><span class="sxs-lookup"><span data-stu-id="2543f-113">Required if **-AuthruleObj** is not specified.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2543f-114">-AuthRuleObj</span><span class="sxs-lookup"><span data-stu-id="2543f-114">-AuthRuleObj</span></span>
<span data-ttu-id="2543f-115">服務匯流排佇列授權規則物件。</span><span class="sxs-lookup"><span data-stu-id="2543f-115">The Service Bus queue authorization rule object.</span></span>

```yaml
Type: SharedAccessAuthorizationRuleAttributes
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2543f-116">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="2543f-116">-NamespaceName</span></span>
<span data-ttu-id="2543f-117">服務匯流排命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="2543f-117">The Service Bus namespace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2543f-118">-QueueName</span><span class="sxs-lookup"><span data-stu-id="2543f-118">-QueueName</span></span>
<span data-ttu-id="2543f-119">服務匯流排佇列名稱。</span><span class="sxs-lookup"><span data-stu-id="2543f-119">The Service Bus queue name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2543f-120">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2543f-120">-ResourceGroup</span></span>
<span data-ttu-id="2543f-121">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2543f-121">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2543f-122">-許可權</span><span class="sxs-lookup"><span data-stu-id="2543f-122">-Rights</span></span>
<span data-ttu-id="2543f-123">權力;例如 @ ( 「聆聽」、「傳送」、「管理」 ) 。</span><span class="sxs-lookup"><span data-stu-id="2543f-123">The rights; for example @("Listen","Send","Manage").</span></span> <span data-ttu-id="2543f-124">如果未指定 ' AuthruleObj」，則為必要。</span><span class="sxs-lookup"><span data-stu-id="2543f-124">Required if 'AuthruleObj' not specified.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2543f-125">-確認</span><span class="sxs-lookup"><span data-stu-id="2543f-125">-Confirm</span></span>
<span data-ttu-id="2543f-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2543f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2543f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2543f-127">-WhatIf</span></span>
<span data-ttu-id="2543f-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2543f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2543f-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2543f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2543f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2543f-130">CommonParameters</span></span>
<span data-ttu-id="2543f-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2543f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2543f-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2543f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2543f-133">輸入</span><span class="sxs-lookup"><span data-stu-id="2543f-133">INPUTS</span></span>

### <span data-ttu-id="2543f-134">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2543f-134">-ResourceGroup</span></span>
 <span data-ttu-id="2543f-135">System.object</span><span class="sxs-lookup"><span data-stu-id="2543f-135">System.String</span></span>

### <span data-ttu-id="2543f-136">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="2543f-136">-NamespaceName</span></span>
 <span data-ttu-id="2543f-137">System.object</span><span class="sxs-lookup"><span data-stu-id="2543f-137">System.String</span></span>

### <span data-ttu-id="2543f-138">-QueueName</span><span class="sxs-lookup"><span data-stu-id="2543f-138">-QueueName</span></span>
 <span data-ttu-id="2543f-139">System.object</span><span class="sxs-lookup"><span data-stu-id="2543f-139">System.String</span></span>

### <span data-ttu-id="2543f-140">-AuthRuleObj</span><span class="sxs-lookup"><span data-stu-id="2543f-140">-AuthRuleObj</span></span>
 <span data-ttu-id="2543f-141">SharedAccessAuthorizationRuleAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="2543f-141">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="2543f-142">輸出</span><span class="sxs-lookup"><span data-stu-id="2543f-142">OUTPUTS</span></span>

### <span data-ttu-id="2543f-143">SharedAccessAuthorizationRuleAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="2543f-143">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="2543f-144">筆記</span><span class="sxs-lookup"><span data-stu-id="2543f-144">NOTES</span></span>

## <span data-ttu-id="2543f-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="2543f-145">RELATED LINKS</span></span>

