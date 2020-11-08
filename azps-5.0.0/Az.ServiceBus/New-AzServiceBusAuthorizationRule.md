---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: beba9c457378949dfe82811186bde84522b46ae5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137129"
---
# <span data-ttu-id="320c6-101">New-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="320c6-101">New-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="320c6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="320c6-102">SYNOPSIS</span></span>
<span data-ttu-id="320c6-103">針對指定的服務匯流排指定命名空間或佇列或主題，建立新的授權規則。</span><span class="sxs-lookup"><span data-stu-id="320c6-103">Creates a new authorization rule for the specified Service Bus given Namespace or Queue or Topic.</span></span>

## <span data-ttu-id="320c6-104">句法</span><span class="sxs-lookup"><span data-stu-id="320c6-104">SYNTAX</span></span>

### <span data-ttu-id="320c6-105">NamespaceAuthorizationRuleSet (預設) </span><span class="sxs-lookup"><span data-stu-id="320c6-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="320c6-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="320c6-106">QueueAuthorizationRuleSet</span></span>
```
New-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="320c6-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="320c6-107">TopicAuthorizationRuleSet</span></span>
```
New-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="320c6-108">說明</span><span class="sxs-lookup"><span data-stu-id="320c6-108">DESCRIPTION</span></span>
<span data-ttu-id="320c6-109">**新的-AzServiceBusAuthorizationRule** Cmdlet 會針對指定的服務匯流排命名空間或佇列或主題建立新的授權規則。</span><span class="sxs-lookup"><span data-stu-id="320c6-109">The **New-AzServiceBusAuthorizationRule** cmdlet creates a new authorization rule for the specified Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="320c6-110">示例</span><span class="sxs-lookup"><span data-stu-id="320c6-110">EXAMPLES</span></span>

### <span data-ttu-id="320c6-111">範例1</span><span class="sxs-lookup"><span data-stu-id="320c6-111">Example 1</span></span>
```
PS C:\> New-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="320c6-112">`AuthoRule1`使用 [ **偵聽** ] 和 [ **傳送** ] 許可權來建立命名空間 `SB-Example1` 。</span><span class="sxs-lookup"><span data-stu-id="320c6-112">Creates `AuthoRule1` with **Listen** and **Send** rights for the namespace `SB-Example1`.</span></span>

### <span data-ttu-id="320c6-113">範例2</span><span class="sxs-lookup"><span data-stu-id="320c6-113">Example 2</span></span>
```
PS C:\> New-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="320c6-114">`AuthoRule1`使用 [ **偵聽** ] 和 [ **傳送** ] 許可權來建立佇列 `SBQueue` 。</span><span class="sxs-lookup"><span data-stu-id="320c6-114">Creates `AuthoRule1` with **Listen** and **Send** rights for the queue `SBQueue`.</span></span>

### <span data-ttu-id="320c6-115">範例3</span><span class="sxs-lookup"><span data-stu-id="320c6-115">Example 3</span></span>
```
PS C:\> New-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="320c6-116">`AuthoRule1`使用 [ **聆聽** ] 和 [ **傳送** ] 權利建立主題 `SBTopic` 。</span><span class="sxs-lookup"><span data-stu-id="320c6-116">Creates `AuthoRule1` with **Listen** and **Send** rights for the topic `SBTopic`.</span></span>

## <span data-ttu-id="320c6-117">參數</span><span class="sxs-lookup"><span data-stu-id="320c6-117">PARAMETERS</span></span>

### <span data-ttu-id="320c6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="320c6-118">-DefaultProfile</span></span>
<span data-ttu-id="320c6-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="320c6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="320c6-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="320c6-120">-Name</span></span>
<span data-ttu-id="320c6-121">AuthorizationRule 名稱</span><span class="sxs-lookup"><span data-stu-id="320c6-121">AuthorizationRule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="320c6-122">-命名空間</span><span class="sxs-lookup"><span data-stu-id="320c6-122">-Namespace</span></span>
<span data-ttu-id="320c6-123">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="320c6-123">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="320c6-124">-佇列</span><span class="sxs-lookup"><span data-stu-id="320c6-124">-Queue</span></span>
<span data-ttu-id="320c6-125">佇列名稱</span><span class="sxs-lookup"><span data-stu-id="320c6-125">Queue Name</span></span>

```yaml
Type: System.String
Parameter Sets: QueueAuthorizationRuleSet
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="320c6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="320c6-126">-ResourceGroupName</span></span>
<span data-ttu-id="320c6-127">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="320c6-127">Resource Group Name</span></span>

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

### <span data-ttu-id="320c6-128">-許可權</span><span class="sxs-lookup"><span data-stu-id="320c6-128">-Rights</span></span>
<span data-ttu-id="320c6-129">權力，例如「聆聽」、「傳送」、「管理」</span><span class="sxs-lookup"><span data-stu-id="320c6-129">Rights, e.g. "Listen","Send","Manage"</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: Listen, Send, Manage

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="320c6-130">-主題</span><span class="sxs-lookup"><span data-stu-id="320c6-130">-Topic</span></span>
<span data-ttu-id="320c6-131">主題名稱</span><span class="sxs-lookup"><span data-stu-id="320c6-131">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: TopicAuthorizationRuleSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="320c6-132">-確認</span><span class="sxs-lookup"><span data-stu-id="320c6-132">-Confirm</span></span>
<span data-ttu-id="320c6-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="320c6-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="320c6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="320c6-134">-WhatIf</span></span>
<span data-ttu-id="320c6-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="320c6-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="320c6-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="320c6-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="320c6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="320c6-137">CommonParameters</span></span>
<span data-ttu-id="320c6-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="320c6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="320c6-139">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="320c6-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="320c6-140">輸入</span><span class="sxs-lookup"><span data-stu-id="320c6-140">INPUTS</span></span>

### <span data-ttu-id="320c6-141">System.object</span><span class="sxs-lookup"><span data-stu-id="320c6-141">System.String</span></span>

### <span data-ttu-id="320c6-142">System.object []</span><span class="sxs-lookup"><span data-stu-id="320c6-142">System.String[]</span></span>

## <span data-ttu-id="320c6-143">輸出</span><span class="sxs-lookup"><span data-stu-id="320c6-143">OUTPUTS</span></span>

### <span data-ttu-id="320c6-144">PSSharedAccessAuthorizationRuleAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="320c6-144">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="320c6-145">筆記</span><span class="sxs-lookup"><span data-stu-id="320c6-145">NOTES</span></span>

## <span data-ttu-id="320c6-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="320c6-146">RELATED LINKS</span></span>