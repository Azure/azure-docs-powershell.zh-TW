---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/new-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: 08560730438fe5bca85a78e8a7f75f427c07de0d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908737"
---
# <span data-ttu-id="6c53f-101">New-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="6c53f-101">New-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="6c53f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6c53f-102">SYNOPSIS</span></span>
<span data-ttu-id="6c53f-103">為指定的 Service Bus 指定命名空間或佇列或主題建立新授權規則。</span><span class="sxs-lookup"><span data-stu-id="6c53f-103">Creates a new authorization rule for the specified Service Bus given Namespace or Queue or Topic.</span></span>

## <span data-ttu-id="6c53f-104">語法</span><span class="sxs-lookup"><span data-stu-id="6c53f-104">SYNTAX</span></span>

### <span data-ttu-id="6c53f-105">命名空間驗證RuleSet (預設) </span><span class="sxs-lookup"><span data-stu-id="6c53f-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c53f-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="6c53f-106">QueueAuthorizationRuleSet</span></span>
```
New-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6c53f-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="6c53f-107">TopicAuthorizationRuleSet</span></span>
```
New-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6c53f-108">描述</span><span class="sxs-lookup"><span data-stu-id="6c53f-108">DESCRIPTION</span></span>
<span data-ttu-id="6c53f-109">**New-AzServiceBusAuthorizationRule** Cmdlet 會為指定的 Service Bus 命名空間或佇列或主題建立新授權規則。</span><span class="sxs-lookup"><span data-stu-id="6c53f-109">The **New-AzServiceBusAuthorizationRule** cmdlet creates a new authorization rule for the specified Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="6c53f-110">例子</span><span class="sxs-lookup"><span data-stu-id="6c53f-110">EXAMPLES</span></span>

### <span data-ttu-id="6c53f-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="6c53f-111">Example 1</span></span>
```
PS C:\> New-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="6c53f-112">使用 `AuthoRule1` 命名空間 **的 Listen** 和 **Send** 許可權建立 `SB-Example1` 。</span><span class="sxs-lookup"><span data-stu-id="6c53f-112">Creates `AuthoRule1` with **Listen** and **Send** rights for the namespace `SB-Example1`.</span></span>

### <span data-ttu-id="6c53f-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="6c53f-113">Example 2</span></span>
```
PS C:\> New-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="6c53f-114">使用 `AuthoRule1` 佇列 **的聆聽** 和 **傳送** 許可權建立 `SBQueue` 。</span><span class="sxs-lookup"><span data-stu-id="6c53f-114">Creates `AuthoRule1` with **Listen** and **Send** rights for the queue `SBQueue`.</span></span>

### <span data-ttu-id="6c53f-115">範例 3</span><span class="sxs-lookup"><span data-stu-id="6c53f-115">Example 3</span></span>
```
PS C:\> New-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="6c53f-116">使用 `AuthoRule1` 主題 **的聆聽** 和 **傳送** 許可權建立 `SBTopic` 。</span><span class="sxs-lookup"><span data-stu-id="6c53f-116">Creates `AuthoRule1` with **Listen** and **Send** rights for the topic `SBTopic`.</span></span>

## <span data-ttu-id="6c53f-117">參數</span><span class="sxs-lookup"><span data-stu-id="6c53f-117">PARAMETERS</span></span>

### <span data-ttu-id="6c53f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c53f-118">-DefaultProfile</span></span>
<span data-ttu-id="6c53f-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="6c53f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c53f-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="6c53f-120">-Name</span></span>
<span data-ttu-id="6c53f-121">AuthorizationRule Name</span><span class="sxs-lookup"><span data-stu-id="6c53f-121">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="6c53f-122">-命名空間</span><span class="sxs-lookup"><span data-stu-id="6c53f-122">-Namespace</span></span>
<span data-ttu-id="6c53f-123">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="6c53f-123">Namespace Name</span></span>

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

### <span data-ttu-id="6c53f-124">-佇列</span><span class="sxs-lookup"><span data-stu-id="6c53f-124">-Queue</span></span>
<span data-ttu-id="6c53f-125">佇列名稱</span><span class="sxs-lookup"><span data-stu-id="6c53f-125">Queue Name</span></span>

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

### <span data-ttu-id="6c53f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c53f-126">-ResourceGroupName</span></span>
<span data-ttu-id="6c53f-127">資源組名</span><span class="sxs-lookup"><span data-stu-id="6c53f-127">Resource Group Name</span></span>

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

### <span data-ttu-id="6c53f-128">-Rights</span><span class="sxs-lookup"><span data-stu-id="6c53f-128">-Rights</span></span>
<span data-ttu-id="6c53f-129">許可權，例如「聆聽」、「傳送」、「管理」</span><span class="sxs-lookup"><span data-stu-id="6c53f-129">Rights, e.g. "Listen","Send","Manage"</span></span>

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

### <span data-ttu-id="6c53f-130">-主題</span><span class="sxs-lookup"><span data-stu-id="6c53f-130">-Topic</span></span>
<span data-ttu-id="6c53f-131">主題名稱</span><span class="sxs-lookup"><span data-stu-id="6c53f-131">Topic Name</span></span>

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

### <span data-ttu-id="6c53f-132">-確認</span><span class="sxs-lookup"><span data-stu-id="6c53f-132">-Confirm</span></span>
<span data-ttu-id="6c53f-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="6c53f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c53f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c53f-134">-WhatIf</span></span>
<span data-ttu-id="6c53f-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6c53f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c53f-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6c53f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c53f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c53f-137">CommonParameters</span></span>
<span data-ttu-id="6c53f-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6c53f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c53f-139">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="6c53f-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c53f-140">輸入</span><span class="sxs-lookup"><span data-stu-id="6c53f-140">INPUTS</span></span>

### <span data-ttu-id="6c53f-141">System.String</span><span class="sxs-lookup"><span data-stu-id="6c53f-141">System.String</span></span>

### <span data-ttu-id="6c53f-142">System.String[]</span><span class="sxs-lookup"><span data-stu-id="6c53f-142">System.String[]</span></span>

## <span data-ttu-id="6c53f-143">輸出</span><span class="sxs-lookup"><span data-stu-id="6c53f-143">OUTPUTS</span></span>

### <span data-ttu-id="6c53f-144">Microsoft.Azure.Commands.ServiceBus.models.PSSharedAccesssAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="6c53f-144">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="6c53f-145">筆記</span><span class="sxs-lookup"><span data-stu-id="6c53f-145">NOTES</span></span>

## <span data-ttu-id="6c53f-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="6c53f-146">RELATED LINKS</span></span>
