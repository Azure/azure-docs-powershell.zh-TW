---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/set-azurermrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayAuthorizationRule.md
ms.openlocfilehash: 91f37ad2ed49b4c1bd39306be803776ddce9ecff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454144"
---
# <span data-ttu-id="017cd-101">Set-AzureRmRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="017cd-101">Set-AzureRmRelayAuthorizationRule</span></span>

## <span data-ttu-id="017cd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="017cd-102">SYNOPSIS</span></span>
<span data-ttu-id="017cd-103">針對指定的中繼實體 (Namespace/WcfRelay/HybridConnection) 更新指定的授權規則描述。</span><span class="sxs-lookup"><span data-stu-id="017cd-103">Updates the specified authorization rule description for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="017cd-104">句法</span><span class="sxs-lookup"><span data-stu-id="017cd-104">SYNTAX</span></span>

### <span data-ttu-id="017cd-105">NamespaceAuthorizationRuleSet (預設) </span><span class="sxs-lookup"><span data-stu-id="017cd-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <AuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="017cd-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="017cd-106">WcfRelayAuthorizationRuleSet</span></span>
```
Set-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> [[-InputObject] <AuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="017cd-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="017cd-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Set-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-HybridConnection] <String> [-Name] <String> [[-InputObject] <AuthorizationRuleAttributes>]
 [[-Rights] <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="017cd-108">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="017cd-108">AuthoRuleInputObjectSet</span></span>
```
Set-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <AuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="017cd-109">AuthoRulePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="017cd-109">AuthoRulePropertiesSet</span></span>
```
Set-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Name] <String> [-Rights] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="017cd-110">說明</span><span class="sxs-lookup"><span data-stu-id="017cd-110">DESCRIPTION</span></span>
<span data-ttu-id="017cd-111">**AzureRmRelayAuthorizationRule** Cmdlet 會更新指定之中繼實體的特定授權規則的描述， (命名空間/WcfRelay/HybridConnection) 。</span><span class="sxs-lookup"><span data-stu-id="017cd-111">The **Set-AzureRmRelayAuthorizationRule** cmdlet updates the description for the specified authorization rule of the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="017cd-112">示例</span><span class="sxs-lookup"><span data-stu-id="017cd-112">EXAMPLES</span></span>

### <span data-ttu-id="017cd-113">範例 1.1-具有 InputObject 的命名空間</span><span class="sxs-lookup"><span data-stu-id="017cd-113">Example 1.1 - Namespace with InputObject</span></span>
```
PS C:\>
PS C:\> $getAutoRule = Get-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -AuthorizationRuleName
 AuthoRule1
PS C:\> $getAutoRule.Rights.Add("Send")
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -AuthorizationRule AuthoRule1 -InputObject $getAutoRule
```

<span data-ttu-id="017cd-114">從命名空間中授權規則的存取權利新增 [ **傳送** ] `AuthoRule1` `TestNameSpace-Relay1` 。</span><span class="sxs-lookup"><span data-stu-id="017cd-114">Adds **Send** from the access rights of the authorization rule `AuthoRule1` in namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="017cd-115">範例 1.2-含許可權參數的命名空間</span><span class="sxs-lookup"><span data-stu-id="017cd-115">Example 1.2 - Namespace with Rights parameter</span></span>
```
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -AuthorizationRule AuthoRule1 -Rights "Send"
```

<span data-ttu-id="017cd-116">從命名空間中授權規則的存取權利新增 [ **傳送** ] `AuthoRule1` `TestNameSpace-Relay1` 。</span><span class="sxs-lookup"><span data-stu-id="017cd-116">Adds **Send** from the access rights of the authorization rule `AuthoRule1` in namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="017cd-117">範例 2.1-使用 InputObject WcfRelay</span><span class="sxs-lookup"><span data-stu-id="017cd-117">Example 2.1 - WcfRelay with InputObject</span></span>
```
PS C:\> $getWcfRelayAutho = Get-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1
PS C:\> $getWcfRelayAutho.Rights.Add("Send")
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -InputObject $getWcfRelayAutho
```

<span data-ttu-id="017cd-118">將 [ **傳送** ] 新增至 WcfRelay 授權規則的存取權 `AuthoRule1` `TestWCFRelay1` 。</span><span class="sxs-lookup"><span data-stu-id="017cd-118">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="017cd-119">範例 2.2-使用許可權參數 WcfRelay</span><span class="sxs-lookup"><span data-stu-id="017cd-119">Example 2.2 - WcfRelay with Rights parameter</span></span>
```
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -Rights "Send"
```

<span data-ttu-id="017cd-120">將 [ **傳送** ] 新增至 WcfRelay 授權規則的存取權 `AuthoRule1` `TestWCFRelay1` 。</span><span class="sxs-lookup"><span data-stu-id="017cd-120">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="017cd-121">範例 3.1-使用 InputObject HybridConnection</span><span class="sxs-lookup"><span data-stu-id="017cd-121">Example 3.1 - HybridConnection with InputObject</span></span>
```
PS C:\> $GetHybirdAutho = Get-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1
PS C:\> $GetHybirdAutho.Rights.Add("Send")
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -InputObject $GetHybirdAutho
```

<span data-ttu-id="017cd-122">將 [ **傳送** ] 新增至 HybridConnection 授權規則的存取權 `AuthoRule1` `TestHybridConnection` 。</span><span class="sxs-lookup"><span data-stu-id="017cd-122">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection`.</span></span>

### <span data-ttu-id="017cd-123">範例 3.2-使用許可權參數 HybridConnection</span><span class="sxs-lookup"><span data-stu-id="017cd-123">Example 3.2 - HybridConnection with Rights parameter</span></span>
```
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -Rights "Send"
```

<span data-ttu-id="017cd-124">將 [ **傳送** ] 新增至 HybridConnection 授權規則的存取權 `AuthoRule1` `TestHybridConnection` 。</span><span class="sxs-lookup"><span data-stu-id="017cd-124">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection`.</span></span>

## <span data-ttu-id="017cd-125">參數</span><span class="sxs-lookup"><span data-stu-id="017cd-125">PARAMETERS</span></span>

### <span data-ttu-id="017cd-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="017cd-126">-DefaultProfile</span></span>
<span data-ttu-id="017cd-127">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="017cd-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="017cd-128">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="017cd-128">-HybridConnection</span></span>
<span data-ttu-id="017cd-129">HybridConnection [名稱]。</span><span class="sxs-lookup"><span data-stu-id="017cd-129">HybridConnection Name.</span></span>

```yaml
Type: String
Parameter Sets: HybridConnectionAuthorizationRuleSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="017cd-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="017cd-130">-InputObject</span></span>
<span data-ttu-id="017cd-131">中繼 AuthorizationRule 物件</span><span class="sxs-lookup"><span data-stu-id="017cd-131">Relay AuthorizationRule Object</span></span>

```yaml
Type: AuthorizationRuleAttributes
Parameter Sets: NamespaceAuthorizationRuleSet, WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: AuthorizationRuleAttributes
Parameter Sets: AuthoRuleInputObjectSet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="017cd-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="017cd-132">-Name</span></span>
<span data-ttu-id="017cd-133">AuthorizationRule [名稱]。</span><span class="sxs-lookup"><span data-stu-id="017cd-133">AuthorizationRule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="017cd-134">-命名空間</span><span class="sxs-lookup"><span data-stu-id="017cd-134">-Namespace</span></span>
<span data-ttu-id="017cd-135">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="017cd-135">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="017cd-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="017cd-136">-ResourceGroupName</span></span>
<span data-ttu-id="017cd-137">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="017cd-137">Resource Group Name.</span></span>

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

### <span data-ttu-id="017cd-138">-許可權</span><span class="sxs-lookup"><span data-stu-id="017cd-138">-Rights</span></span>
<span data-ttu-id="017cd-139">權力，例如 @ ( 「聆聽」、「傳送」、「管理」 ) </span><span class="sxs-lookup"><span data-stu-id="017cd-139">Rights, e.g. @("Listen","Send","Manage")</span></span>

```yaml
Type: String[]
Parameter Sets: NamespaceAuthorizationRuleSet, WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String[]
Parameter Sets: AuthoRulePropertiesSet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="017cd-140">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="017cd-140">-WcfRelay</span></span>
<span data-ttu-id="017cd-141">WcfRelay [名稱]。</span><span class="sxs-lookup"><span data-stu-id="017cd-141">WcfRelay Name.</span></span>

```yaml
Type: String
Parameter Sets: WcfRelayAuthorizationRuleSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="017cd-142">-確認</span><span class="sxs-lookup"><span data-stu-id="017cd-142">-Confirm</span></span>
<span data-ttu-id="017cd-143">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="017cd-143">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="017cd-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="017cd-144">-WhatIf</span></span>
<span data-ttu-id="017cd-145">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="017cd-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="017cd-146">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="017cd-146">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="017cd-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="017cd-147">CommonParameters</span></span>
<span data-ttu-id="017cd-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="017cd-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="017cd-149">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="017cd-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="017cd-150">輸入</span><span class="sxs-lookup"><span data-stu-id="017cd-150">INPUTS</span></span>

### <span data-ttu-id="017cd-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="017cd-151">-ResourceGroupName</span></span>
 <span data-ttu-id="017cd-152">System.object</span><span class="sxs-lookup"><span data-stu-id="017cd-152">System.String</span></span> 

### <span data-ttu-id="017cd-153">-命名空間</span><span class="sxs-lookup"><span data-stu-id="017cd-153">-Namespace</span></span>
 <span data-ttu-id="017cd-154">System.object</span><span class="sxs-lookup"><span data-stu-id="017cd-154">System.String</span></span> 
 

### <span data-ttu-id="017cd-155">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="017cd-155">-WcfRelay</span></span>
 <span data-ttu-id="017cd-156">System.object</span><span class="sxs-lookup"><span data-stu-id="017cd-156">System.String</span></span> 

### <span data-ttu-id="017cd-157">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="017cd-157">-HybridConnection</span></span>
 <span data-ttu-id="017cd-158">System.object</span><span class="sxs-lookup"><span data-stu-id="017cd-158">System.String</span></span> 
 

### <span data-ttu-id="017cd-159">-名稱</span><span class="sxs-lookup"><span data-stu-id="017cd-159">-Name</span></span>
 <span data-ttu-id="017cd-160">System.object</span><span class="sxs-lookup"><span data-stu-id="017cd-160">System.String</span></span>

### <span data-ttu-id="017cd-161">-InputObject</span><span class="sxs-lookup"><span data-stu-id="017cd-161">-InputObject</span></span>
 <span data-ttu-id="017cd-162">AuthorizationRuleAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="017cd-162">Microsoft.Azure.Commands.Relay.Models.AuthorizationRuleAttributes</span></span>
 

### <span data-ttu-id="017cd-163">-許可權</span><span class="sxs-lookup"><span data-stu-id="017cd-163">-Rights</span></span>
 <span data-ttu-id="017cd-164">System.object []</span><span class="sxs-lookup"><span data-stu-id="017cd-164">System.String []</span></span>

## <span data-ttu-id="017cd-165">輸出</span><span class="sxs-lookup"><span data-stu-id="017cd-165">OUTPUTS</span></span>

### <span data-ttu-id="017cd-166">AuthorizationRuleAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="017cd-166">Microsoft.Azure.Commands.Relay.Models.AuthorizationRuleAttributes</span></span>

### <span data-ttu-id="017cd-167">範例 1-命名空間</span><span class="sxs-lookup"><span data-stu-id="017cd-167">Example 1 - Namespace</span></span>
<span data-ttu-id="017cd-168">許可權： {偵聽，傳送} 名稱： AuthoRule1 類型： Microsoft. 中繼/AuthorizationRules Id：/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="017cd-168">Rights : {Listen, Send} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1</span></span>

### <span data-ttu-id="017cd-169">範例 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="017cd-169">Example 2 - WcfRelay</span></span>
<span data-ttu-id="017cd-170">許可權： {偵聽，傳送} 名稱： AuthoRule1 類型： Microsoft. 中繼/AuthorizationRules Id：/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="017cd-170">Rights : {Listen, Send} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1</span></span>

### <span data-ttu-id="017cd-171">範例 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="017cd-171">Example 3 - HybridConnection</span></span>
<span data-ttu-id="017cd-172">許可權： {偵聽，傳送} 名稱： AuthoRule1 類型： Microsoft. 中繼/AuthorizationRules Id：/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="017cd-172">Rights : {Listen, Send} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1</span></span>

## <span data-ttu-id="017cd-173">筆記</span><span class="sxs-lookup"><span data-stu-id="017cd-173">NOTES</span></span>

## <span data-ttu-id="017cd-174">相關連結</span><span class="sxs-lookup"><span data-stu-id="017cd-174">RELATED LINKS</span></span>

