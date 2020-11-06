---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: 62edcb426fe62f834b876b0dd4e2006712f81348
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93620636"
---
# <span data-ttu-id="99bd3-101">New-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="99bd3-101">New-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="99bd3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="99bd3-102">SYNOPSIS</span></span>
<span data-ttu-id="99bd3-103">針對指定的服務匯流排指定命名空間或佇列或主題，建立新的授權規則。</span><span class="sxs-lookup"><span data-stu-id="99bd3-103">Creates a new authorization rule for the specified Service Bus given Namespace or Queue or Topic.</span></span>

## <span data-ttu-id="99bd3-104">句法</span><span class="sxs-lookup"><span data-stu-id="99bd3-104">SYNTAX</span></span>

### <span data-ttu-id="99bd3-105">NamespaceAuthorizationRuleSet (預設) </span><span class="sxs-lookup"><span data-stu-id="99bd3-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99bd3-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="99bd3-106">QueueAuthorizationRuleSet</span></span>
```
New-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="99bd3-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="99bd3-107">TopicAuthorizationRuleSet</span></span>
```
New-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="99bd3-108">說明</span><span class="sxs-lookup"><span data-stu-id="99bd3-108">DESCRIPTION</span></span>
<span data-ttu-id="99bd3-109">**新的-AzServiceBusAuthorizationRule** Cmdlet 會針對指定的服務匯流排命名空間或佇列或主題建立新的授權規則。</span><span class="sxs-lookup"><span data-stu-id="99bd3-109">The **New-AzServiceBusAuthorizationRule** cmdlet creates a new authorization rule for the specified Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="99bd3-110">示例</span><span class="sxs-lookup"><span data-stu-id="99bd3-110">EXAMPLES</span></span>

### <span data-ttu-id="99bd3-111">範例1</span><span class="sxs-lookup"><span data-stu-id="99bd3-111">Example 1</span></span>
```
PS C:\> New-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="99bd3-112">`AuthoRule1`使用 [ **偵聽** ] 和 [ **傳送** ] 許可權來建立命名空間 `SB-Example1` 。</span><span class="sxs-lookup"><span data-stu-id="99bd3-112">Creates `AuthoRule1` with **Listen** and **Send** rights for the namespace `SB-Example1`.</span></span>

### <span data-ttu-id="99bd3-113">範例2</span><span class="sxs-lookup"><span data-stu-id="99bd3-113">Example 2</span></span>
```
PS C:\> New-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="99bd3-114">`AuthoRule1`使用 [ **偵聽** ] 和 [ **傳送** ] 許可權來建立佇列 `SBQueue` 。</span><span class="sxs-lookup"><span data-stu-id="99bd3-114">Creates `AuthoRule1` with **Listen** and **Send** rights for the queue `SBQueue`.</span></span>

### <span data-ttu-id="99bd3-115">範例3</span><span class="sxs-lookup"><span data-stu-id="99bd3-115">Example 3</span></span>
```
PS C:\> New-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="99bd3-116">`AuthoRule1`使用 [ **聆聽** ] 和 [ **傳送** ] 權利建立主題 `SBTopic` 。</span><span class="sxs-lookup"><span data-stu-id="99bd3-116">Creates `AuthoRule1` with **Listen** and **Send** rights for the topic `SBTopic`.</span></span>

## <span data-ttu-id="99bd3-117">參數</span><span class="sxs-lookup"><span data-stu-id="99bd3-117">PARAMETERS</span></span>

### <span data-ttu-id="99bd3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99bd3-118">-DefaultProfile</span></span>
<span data-ttu-id="99bd3-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="99bd3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99bd3-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="99bd3-120">-Name</span></span>
<span data-ttu-id="99bd3-121">AuthorizationRule 名稱</span><span class="sxs-lookup"><span data-stu-id="99bd3-121">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="99bd3-122">-命名空間</span><span class="sxs-lookup"><span data-stu-id="99bd3-122">-Namespace</span></span>
<span data-ttu-id="99bd3-123">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="99bd3-123">Namespace Name</span></span>

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

### <span data-ttu-id="99bd3-124">-佇列</span><span class="sxs-lookup"><span data-stu-id="99bd3-124">-Queue</span></span>
<span data-ttu-id="99bd3-125">佇列名稱</span><span class="sxs-lookup"><span data-stu-id="99bd3-125">Queue Name</span></span>

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

### <span data-ttu-id="99bd3-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99bd3-126">-ResourceGroupName</span></span>
<span data-ttu-id="99bd3-127">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="99bd3-127">Resource Group Name</span></span>

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

### <span data-ttu-id="99bd3-128">-許可權</span><span class="sxs-lookup"><span data-stu-id="99bd3-128">-Rights</span></span>
<span data-ttu-id="99bd3-129">權力，例如「聆聽」、「傳送」、「管理」</span><span class="sxs-lookup"><span data-stu-id="99bd3-129">Rights, e.g. "Listen","Send","Manage"</span></span>

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

### <span data-ttu-id="99bd3-130">-主題</span><span class="sxs-lookup"><span data-stu-id="99bd3-130">-Topic</span></span>
<span data-ttu-id="99bd3-131">主題名稱</span><span class="sxs-lookup"><span data-stu-id="99bd3-131">Topic Name</span></span>

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

### <span data-ttu-id="99bd3-132">-確認</span><span class="sxs-lookup"><span data-stu-id="99bd3-132">-Confirm</span></span>
<span data-ttu-id="99bd3-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="99bd3-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99bd3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99bd3-134">-WhatIf</span></span>
<span data-ttu-id="99bd3-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="99bd3-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99bd3-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="99bd3-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99bd3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99bd3-137">CommonParameters</span></span>
<span data-ttu-id="99bd3-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="99bd3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99bd3-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="99bd3-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99bd3-140">輸入</span><span class="sxs-lookup"><span data-stu-id="99bd3-140">INPUTS</span></span>

### <span data-ttu-id="99bd3-141">System.object</span><span class="sxs-lookup"><span data-stu-id="99bd3-141">System.String</span></span>

### <span data-ttu-id="99bd3-142">System.object []</span><span class="sxs-lookup"><span data-stu-id="99bd3-142">System.String[]</span></span>

## <span data-ttu-id="99bd3-143">輸出</span><span class="sxs-lookup"><span data-stu-id="99bd3-143">OUTPUTS</span></span>

### <span data-ttu-id="99bd3-144">PSSharedAccessAuthorizationRuleAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="99bd3-144">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="99bd3-145">筆記</span><span class="sxs-lookup"><span data-stu-id="99bd3-145">NOTES</span></span>

## <span data-ttu-id="99bd3-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="99bd3-146">RELATED LINKS</span></span>
