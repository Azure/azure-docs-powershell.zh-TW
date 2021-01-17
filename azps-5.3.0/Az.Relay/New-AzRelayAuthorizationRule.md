---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/new-azrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayAuthorizationRule.md
ms.openlocfilehash: 39bba687e355b1742210fb0c37fc8f1a65d957a0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98286612"
---
# <span data-ttu-id="2a085-101">New-AzRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="2a085-101">New-AzRelayAuthorizationRule</span></span>

## <span data-ttu-id="2a085-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2a085-102">SYNOPSIS</span></span>
<span data-ttu-id="2a085-103">針對指定的中繼實體 (Namespace/WcfRelay/HybridConnection) 建立新的授權規則。</span><span class="sxs-lookup"><span data-stu-id="2a085-103">Creates a new authorization rule for the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="2a085-104">句法</span><span class="sxs-lookup"><span data-stu-id="2a085-104">SYNTAX</span></span>

### <span data-ttu-id="2a085-105">NamespaceAuthorizationRuleSet (預設) </span><span class="sxs-lookup"><span data-stu-id="2a085-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a085-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="2a085-106">WcfRelayAuthorizationRuleSet</span></span>
```
New-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2a085-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="2a085-107">HybridConnectionAuthorizationRuleSet</span></span>
```
New-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2a085-108">說明</span><span class="sxs-lookup"><span data-stu-id="2a085-108">DESCRIPTION</span></span>
<span data-ttu-id="2a085-109">**新的-AzRelayAuthorizationRule** Cmdlet 會為指定的中繼實體建立新的授權規則， (命名空間/WcfRelay/HybridConnection) 。</span><span class="sxs-lookup"><span data-stu-id="2a085-109">The **New-AzRelayAuthorizationRule** cmdlet creates a new authorization rule for the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="2a085-110">示例</span><span class="sxs-lookup"><span data-stu-id="2a085-110">EXAMPLES</span></span>

### <span data-ttu-id="2a085-111">範例1：命名空間</span><span class="sxs-lookup"><span data-stu-id="2a085-111">Example 1: Namespace</span></span>
```powershell
PS C:\>New-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -Rights "Listen"

Rights : {Listen}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1
```

<span data-ttu-id="2a085-112">建立 `AuthoRule1` 命名空間的 [ **偵聽** ] 許可權 `TestNameSpace-Relay1` 。</span><span class="sxs-lookup"><span data-stu-id="2a085-112">Creates `AuthoRule1` with **Listen** rights for the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="2a085-113">範例2： WcfRelay</span><span class="sxs-lookup"><span data-stu-id="2a085-113">Example 2: WcfRelay</span></span>
```powershell
PS C:\>New-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -Rights "Listen"

Rights : {Listen}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1
```

<span data-ttu-id="2a085-114">`AuthoRule1`使用 WcfRelay 的 [**偵聽**] 許可權建立授權規則 `TestWCFRelay1` 。</span><span class="sxs-lookup"><span data-stu-id="2a085-114">Creates authorization rule `AuthoRule1` with **Listen** rights for the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="2a085-115">範例3： HybridConnection</span><span class="sxs-lookup"><span data-stu-id="2a085-115">Example 3: HybridConnection</span></span>
```powershell
PS C:\>New-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -Rights "Listen"

Rights : {Listen}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="2a085-116">`AuthoRule1`使用 [混合式連接] 的 [**聆聽**] 權利建立 `TestHybridConnection` 。</span><span class="sxs-lookup"><span data-stu-id="2a085-116">Creates `AuthoRule1` with **Listen** rights for the Hybrid Connection `TestHybridConnection`.</span></span>

## <span data-ttu-id="2a085-117">參數</span><span class="sxs-lookup"><span data-stu-id="2a085-117">PARAMETERS</span></span>

### <span data-ttu-id="2a085-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a085-118">-DefaultProfile</span></span>
<span data-ttu-id="2a085-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2a085-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a085-120">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="2a085-120">-HybridConnection</span></span>
<span data-ttu-id="2a085-121">HybridConnection [名稱]。</span><span class="sxs-lookup"><span data-stu-id="2a085-121">HybridConnection Name.</span></span>

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

### <span data-ttu-id="2a085-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="2a085-122">-Name</span></span>
<span data-ttu-id="2a085-123">AuthorizationRule [名稱]。</span><span class="sxs-lookup"><span data-stu-id="2a085-123">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="2a085-124">-命名空間</span><span class="sxs-lookup"><span data-stu-id="2a085-124">-Namespace</span></span>
<span data-ttu-id="2a085-125">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="2a085-125">Namespace Name.</span></span>

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

### <span data-ttu-id="2a085-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a085-126">-ResourceGroupName</span></span>
<span data-ttu-id="2a085-127">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="2a085-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="2a085-128">-許可權</span><span class="sxs-lookup"><span data-stu-id="2a085-128">-Rights</span></span>
<span data-ttu-id="2a085-129">權力，例如「聆聽」、「傳送」、「管理」</span><span class="sxs-lookup"><span data-stu-id="2a085-129">Rights, e.g. "Listen","Send","Manage"</span></span>

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

### <span data-ttu-id="2a085-130">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="2a085-130">-WcfRelay</span></span>
<span data-ttu-id="2a085-131">WcfRelay [名稱]。</span><span class="sxs-lookup"><span data-stu-id="2a085-131">WcfRelay Name.</span></span>

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

### <span data-ttu-id="2a085-132">-確認</span><span class="sxs-lookup"><span data-stu-id="2a085-132">-Confirm</span></span>
<span data-ttu-id="2a085-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2a085-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a085-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a085-134">-WhatIf</span></span>
<span data-ttu-id="2a085-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2a085-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a085-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2a085-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a085-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a085-137">CommonParameters</span></span>
<span data-ttu-id="2a085-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2a085-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a085-139">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2a085-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a085-140">輸入</span><span class="sxs-lookup"><span data-stu-id="2a085-140">INPUTS</span></span>

### <span data-ttu-id="2a085-141">System.object</span><span class="sxs-lookup"><span data-stu-id="2a085-141">System.String</span></span>

### <span data-ttu-id="2a085-142">System.object []</span><span class="sxs-lookup"><span data-stu-id="2a085-142">System.String[]</span></span>

## <span data-ttu-id="2a085-143">輸出</span><span class="sxs-lookup"><span data-stu-id="2a085-143">OUTPUTS</span></span>

### <span data-ttu-id="2a085-144">PSAuthorizationRuleAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="2a085-144">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="2a085-145">筆記</span><span class="sxs-lookup"><span data-stu-id="2a085-145">NOTES</span></span>

## <span data-ttu-id="2a085-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="2a085-146">RELATED LINKS</span></span>
