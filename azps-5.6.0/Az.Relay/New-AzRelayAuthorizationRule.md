---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/powershell/module/az.relay/new-azrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayAuthorizationRule.md
ms.openlocfilehash: d0faea052141420db88f58fd6513c2d6822f56c7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914597"
---
# <span data-ttu-id="d99c1-101">New-AzRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="d99c1-101">New-AzRelayAuthorizationRule</span></span>

## <span data-ttu-id="d99c1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d99c1-102">SYNOPSIS</span></span>
<span data-ttu-id="d99c1-103">為指定的 Relay 實體建立新授權規則， (命名空間/WcfRelay/HybridConnection) 。</span><span class="sxs-lookup"><span data-stu-id="d99c1-103">Creates a new authorization rule for the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="d99c1-104">語法</span><span class="sxs-lookup"><span data-stu-id="d99c1-104">SYNTAX</span></span>

### <span data-ttu-id="d99c1-105">命名空間驗證RuleSet (預設) </span><span class="sxs-lookup"><span data-stu-id="d99c1-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d99c1-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="d99c1-106">WcfRelayAuthorizationRuleSet</span></span>
```
New-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d99c1-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="d99c1-107">HybridConnectionAuthorizationRuleSet</span></span>
```
New-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d99c1-108">描述</span><span class="sxs-lookup"><span data-stu-id="d99c1-108">DESCRIPTION</span></span>
<span data-ttu-id="d99c1-109">**New-AzRelayAuthorizationRule** Cmdlet 會為指定的轉寄實體 (命名空間/WcfRelay/HybridConnection) 。</span><span class="sxs-lookup"><span data-stu-id="d99c1-109">The **New-AzRelayAuthorizationRule** cmdlet creates a new authorization rule for the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="d99c1-110">例子</span><span class="sxs-lookup"><span data-stu-id="d99c1-110">EXAMPLES</span></span>

### <span data-ttu-id="d99c1-111">範例 1：命名空間</span><span class="sxs-lookup"><span data-stu-id="d99c1-111">Example 1: Namespace</span></span>
```powershell
PS C:\>New-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -Rights "Listen"

Rights : {Listen}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1
```

<span data-ttu-id="d99c1-112">使用 `AuthoRule1` 命名空間 **的 Listen** 許可權建立 `TestNameSpace-Relay1` 。</span><span class="sxs-lookup"><span data-stu-id="d99c1-112">Creates `AuthoRule1` with **Listen** rights for the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="d99c1-113">範例 2：WcfRelay</span><span class="sxs-lookup"><span data-stu-id="d99c1-113">Example 2: WcfRelay</span></span>
```powershell
PS C:\>New-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -Rights "Listen"

Rights : {Listen}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1
```

<span data-ttu-id="d99c1-114">使用 `AuthoRule1` WcfRelay 的 **「** 聆聽」許可權建立授權規則 `TestWCFRelay1` 。</span><span class="sxs-lookup"><span data-stu-id="d99c1-114">Creates authorization rule `AuthoRule1` with **Listen** rights for the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="d99c1-115">範例 3：HybridConnection</span><span class="sxs-lookup"><span data-stu-id="d99c1-115">Example 3: HybridConnection</span></span>
```powershell
PS C:\>New-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -Rights "Listen"

Rights : {Listen}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="d99c1-116">使用 `AuthoRule1` 混合 **式連接的聆聽** 許可權建立 `TestHybridConnection` 。</span><span class="sxs-lookup"><span data-stu-id="d99c1-116">Creates `AuthoRule1` with **Listen** rights for the Hybrid Connection `TestHybridConnection`.</span></span>

## <span data-ttu-id="d99c1-117">參數</span><span class="sxs-lookup"><span data-stu-id="d99c1-117">PARAMETERS</span></span>

### <span data-ttu-id="d99c1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d99c1-118">-DefaultProfile</span></span>
<span data-ttu-id="d99c1-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d99c1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d99c1-120">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="d99c1-120">-HybridConnection</span></span>
<span data-ttu-id="d99c1-121">HybridConnection 名稱。</span><span class="sxs-lookup"><span data-stu-id="d99c1-121">HybridConnection Name.</span></span>

```yaml
Type: System.String
Parameter Sets: HybridConnectionAuthorizationRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d99c1-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="d99c1-122">-Name</span></span>
<span data-ttu-id="d99c1-123">AuthorizationRule Name.</span><span class="sxs-lookup"><span data-stu-id="d99c1-123">AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d99c1-124">-命名空間</span><span class="sxs-lookup"><span data-stu-id="d99c1-124">-Namespace</span></span>
<span data-ttu-id="d99c1-125">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="d99c1-125">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d99c1-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d99c1-126">-ResourceGroupName</span></span>
<span data-ttu-id="d99c1-127">資源組名。</span><span class="sxs-lookup"><span data-stu-id="d99c1-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="d99c1-128">-Rights</span><span class="sxs-lookup"><span data-stu-id="d99c1-128">-Rights</span></span>
<span data-ttu-id="d99c1-129">許可權，例如「聆聽」、「傳送」、「管理」</span><span class="sxs-lookup"><span data-stu-id="d99c1-129">Rights, e.g. "Listen","Send","Manage"</span></span>

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

### <span data-ttu-id="d99c1-130">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="d99c1-130">-WcfRelay</span></span>
<span data-ttu-id="d99c1-131">WcfRelay 名稱。</span><span class="sxs-lookup"><span data-stu-id="d99c1-131">WcfRelay Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WcfRelayAuthorizationRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d99c1-132">-確認</span><span class="sxs-lookup"><span data-stu-id="d99c1-132">-Confirm</span></span>
<span data-ttu-id="d99c1-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="d99c1-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d99c1-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d99c1-134">-WhatIf</span></span>
<span data-ttu-id="d99c1-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d99c1-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d99c1-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d99c1-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d99c1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d99c1-137">CommonParameters</span></span>
<span data-ttu-id="d99c1-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d99c1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d99c1-139">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="d99c1-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d99c1-140">輸入</span><span class="sxs-lookup"><span data-stu-id="d99c1-140">INPUTS</span></span>

### <span data-ttu-id="d99c1-141">System.String</span><span class="sxs-lookup"><span data-stu-id="d99c1-141">System.String</span></span>

### <span data-ttu-id="d99c1-142">System.String[]</span><span class="sxs-lookup"><span data-stu-id="d99c1-142">System.String[]</span></span>

## <span data-ttu-id="d99c1-143">輸出</span><span class="sxs-lookup"><span data-stu-id="d99c1-143">OUTPUTS</span></span>

### <span data-ttu-id="d99c1-144">Microsoft.Azure.Commands.Relay.models.PSAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="d99c1-144">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="d99c1-145">筆記</span><span class="sxs-lookup"><span data-stu-id="d99c1-145">NOTES</span></span>

## <span data-ttu-id="d99c1-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="d99c1-146">RELATED LINKS</span></span>
