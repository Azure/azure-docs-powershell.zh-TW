---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/powershell/module/az.relay/set-azrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayAuthorizationRule.md
ms.openlocfilehash: 3165905cc86d2255670127cd90c015ce20096c14
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914561"
---
# <span data-ttu-id="5c540-101">Set-AzRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="5c540-101">Set-AzRelayAuthorizationRule</span></span>

## <span data-ttu-id="5c540-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5c540-102">SYNOPSIS</span></span>
<span data-ttu-id="5c540-103">更新指定轉場實體的指定授權規則描述 (命名空間/WcfRelay/HybridConnection) 。</span><span class="sxs-lookup"><span data-stu-id="5c540-103">Updates the specified authorization rule description for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="5c540-104">語法</span><span class="sxs-lookup"><span data-stu-id="5c540-104">SYNTAX</span></span>

### <span data-ttu-id="5c540-105">命名空間驗證RuleSet (預設) </span><span class="sxs-lookup"><span data-stu-id="5c540-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c540-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="5c540-106">WcfRelayAuthorizationRuleSet</span></span>
```
Set-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> [[-InputObject] <PSAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c540-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="5c540-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Set-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> [[-InputObject] <PSAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c540-108">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5c540-108">AuthoRuleInputObjectSet</span></span>
```
Set-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5c540-109">AuthoRulePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="5c540-109">AuthoRulePropertiesSet</span></span>
```
Set-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Name] <String> [-Rights] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c540-110">描述</span><span class="sxs-lookup"><span data-stu-id="5c540-110">DESCRIPTION</span></span>
<span data-ttu-id="5c540-111">**Set-AzRelayAuthorizationRule** Cmdlet 會更新指定轉寄實體 (命名空間/WcfRelay/HybridConnection) 之指定授權規則的描述。</span><span class="sxs-lookup"><span data-stu-id="5c540-111">The **Set-AzRelayAuthorizationRule** cmdlet updates the description for the specified authorization rule of the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="5c540-112">例子</span><span class="sxs-lookup"><span data-stu-id="5c540-112">EXAMPLES</span></span>

### <span data-ttu-id="5c540-113">範例 1.1 - 命名空間與 InputObject</span><span class="sxs-lookup"><span data-stu-id="5c540-113">Example 1.1 - Namespace with InputObject</span></span>
```
PS C:\>
PS C:\> $getAutoRule = Get-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -AuthorizationRuleName
 AuthoRule1
PS C:\> $getAutoRule.Rights.Add("Send")
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -AuthorizationRule AuthoRule1 -InputObject $getAutoRule

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1
```

<span data-ttu-id="5c540-114">從 **命名空間** 中授權規則的存取權新增 `AuthoRule1` `TestNameSpace-Relay1` Send。</span><span class="sxs-lookup"><span data-stu-id="5c540-114">Adds **Send** from the access rights of the authorization rule `AuthoRule1` in namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="5c540-115">範例 1.2 - 命名空間與 Rights 參數</span><span class="sxs-lookup"><span data-stu-id="5c540-115">Example 1.2 - Namespace with Rights parameter</span></span>
```
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -AuthorizationRule AuthoRule1 -Rights "Send"

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1
```

<span data-ttu-id="5c540-116">從 **命名空間** 中授權規則的存取權新增 `AuthoRule1` `TestNameSpace-Relay1` Send。</span><span class="sxs-lookup"><span data-stu-id="5c540-116">Adds **Send** from the access rights of the authorization rule `AuthoRule1` in namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="5c540-117">範例 2.1 - WcfRelay with InputObject</span><span class="sxs-lookup"><span data-stu-id="5c540-117">Example 2.1 - WcfRelay with InputObject</span></span>
```
PS C:\> $getWcfRelayAutho = Get-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1
PS C:\> $getWcfRelayAutho.Rights.Add("Send")
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -InputObject $getWcfRelayAutho

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1
```

<span data-ttu-id="5c540-118">將 **Send** 新增到 `AuthoRule1` WcfRelay 授權規則的存取權 `TestWCFRelay1` 。</span><span class="sxs-lookup"><span data-stu-id="5c540-118">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="5c540-119">範例 2.2 - WcfRelay with Rights 參數</span><span class="sxs-lookup"><span data-stu-id="5c540-119">Example 2.2 - WcfRelay with Rights parameter</span></span>
```
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -Rights "Send"

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1
```

<span data-ttu-id="5c540-120">將 **Send** 新增到 `AuthoRule1` WcfRelay 授權規則的存取權 `TestWCFRelay1` 。</span><span class="sxs-lookup"><span data-stu-id="5c540-120">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="5c540-121">範例 3.1 - HybridConnection with InputObject</span><span class="sxs-lookup"><span data-stu-id="5c540-121">Example 3.1 - HybridConnection with InputObject</span></span>
```
PS C:\> $GetHybirdAutho = Get-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1
PS C:\> $GetHybirdAutho.Rights.Add("Send")
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -InputObject $GetHybirdAutho

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="5c540-122">將 **Send** 新增到 `AuthoRule1` HybridConnection 之授權規則的存取權 `TestHybridConnection` 。</span><span class="sxs-lookup"><span data-stu-id="5c540-122">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection`.</span></span>

### <span data-ttu-id="5c540-123">範例 3.2 - HybridConnection with Rights 參數</span><span class="sxs-lookup"><span data-stu-id="5c540-123">Example 3.2 - HybridConnection with Rights parameter</span></span>
```
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -Rights "Send"

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="5c540-124">將 **Send** 新增到 `AuthoRule1` HybridConnection 之授權規則的存取權 `TestHybridConnection` 。</span><span class="sxs-lookup"><span data-stu-id="5c540-124">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection`.</span></span>

## <span data-ttu-id="5c540-125">參數</span><span class="sxs-lookup"><span data-stu-id="5c540-125">PARAMETERS</span></span>

### <span data-ttu-id="5c540-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c540-126">-DefaultProfile</span></span>
<span data-ttu-id="5c540-127">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5c540-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c540-128">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="5c540-128">-HybridConnection</span></span>
<span data-ttu-id="5c540-129">HybridConnection 名稱。</span><span class="sxs-lookup"><span data-stu-id="5c540-129">HybridConnection Name.</span></span>

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

### <span data-ttu-id="5c540-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5c540-130">-InputObject</span></span>
<span data-ttu-id="5c540-131">轉遞授權規則物件。</span><span class="sxs-lookup"><span data-stu-id="5c540-131">Relay AuthorizationRule Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes
Parameter Sets: NamespaceAuthorizationRuleSet, WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes
Parameter Sets: AuthoRuleInputObjectSet
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c540-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="5c540-132">-Name</span></span>
<span data-ttu-id="5c540-133">AuthorizationRule Name.</span><span class="sxs-lookup"><span data-stu-id="5c540-133">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="5c540-134">-命名空間</span><span class="sxs-lookup"><span data-stu-id="5c540-134">-Namespace</span></span>
<span data-ttu-id="5c540-135">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="5c540-135">Namespace Name.</span></span>

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

### <span data-ttu-id="5c540-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c540-136">-ResourceGroupName</span></span>
<span data-ttu-id="5c540-137">資源組名。</span><span class="sxs-lookup"><span data-stu-id="5c540-137">Resource Group Name.</span></span>

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

### <span data-ttu-id="5c540-138">-Rights</span><span class="sxs-lookup"><span data-stu-id="5c540-138">-Rights</span></span>
<span data-ttu-id="5c540-139">許可權，例如 @ ("Listen"，"Send"，"Manage") </span><span class="sxs-lookup"><span data-stu-id="5c540-139">Rights, e.g. @("Listen","Send","Manage")</span></span>

```yaml
Type: System.String[]
Parameter Sets: NamespaceAuthorizationRuleSet, WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: AuthoRulePropertiesSet
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c540-140">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="5c540-140">-WcfRelay</span></span>
<span data-ttu-id="5c540-141">WcfRelay 名稱。</span><span class="sxs-lookup"><span data-stu-id="5c540-141">WcfRelay Name.</span></span>

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

### <span data-ttu-id="5c540-142">-確認</span><span class="sxs-lookup"><span data-stu-id="5c540-142">-Confirm</span></span>
<span data-ttu-id="5c540-143">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="5c540-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c540-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c540-144">-WhatIf</span></span>
<span data-ttu-id="5c540-145">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5c540-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c540-146">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5c540-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c540-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c540-147">CommonParameters</span></span>
<span data-ttu-id="5c540-148">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5c540-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c540-149">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="5c540-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c540-150">輸入</span><span class="sxs-lookup"><span data-stu-id="5c540-150">INPUTS</span></span>

### <span data-ttu-id="5c540-151">System.String</span><span class="sxs-lookup"><span data-stu-id="5c540-151">System.String</span></span>

### <span data-ttu-id="5c540-152">Microsoft.Azure.Commands.Relay.models.PSAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="5c540-152">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span></span>

### <span data-ttu-id="5c540-153">System.String[]</span><span class="sxs-lookup"><span data-stu-id="5c540-153">System.String[]</span></span>

## <span data-ttu-id="5c540-154">輸出</span><span class="sxs-lookup"><span data-stu-id="5c540-154">OUTPUTS</span></span>

### <span data-ttu-id="5c540-155">Microsoft.Azure.Commands.Relay.models.PSAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="5c540-155">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="5c540-156">筆記</span><span class="sxs-lookup"><span data-stu-id="5c540-156">NOTES</span></span>

## <span data-ttu-id="5c540-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="5c540-157">RELATED LINKS</span></span>
