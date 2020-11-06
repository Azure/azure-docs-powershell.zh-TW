---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayAuthorizationRule.md
ms.openlocfilehash: 9e4eecad543346efa60dfb0b9a20e31c47a59036
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448017"
---
# <span data-ttu-id="74b49-101">New-AzureRmRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="74b49-101">New-AzureRmRelayAuthorizationRule</span></span>

## <span data-ttu-id="74b49-102">摘要</span><span class="sxs-lookup"><span data-stu-id="74b49-102">SYNOPSIS</span></span>
<span data-ttu-id="74b49-103">針對指定的中繼實體 (Namespace/WcfRelay/HybridConnection) 建立新的授權規則。</span><span class="sxs-lookup"><span data-stu-id="74b49-103">Creates a new authorization rule for the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="74b49-104">句法</span><span class="sxs-lookup"><span data-stu-id="74b49-104">SYNTAX</span></span>

### <span data-ttu-id="74b49-105">NamespaceAuthorizationRuleSet (預設) </span><span class="sxs-lookup"><span data-stu-id="74b49-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74b49-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="74b49-106">WcfRelayAuthorizationRuleSet</span></span>
```
New-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="74b49-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="74b49-107">HybridConnectionAuthorizationRuleSet</span></span>
```
New-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-HybridConnection] <String> [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74b49-108">說明</span><span class="sxs-lookup"><span data-stu-id="74b49-108">DESCRIPTION</span></span>
<span data-ttu-id="74b49-109">**新的-AzureRmRelayAuthorizationRule** Cmdlet 會為指定的中繼實體建立新的授權規則， (命名空間/WcfRelay/HybridConnection) 。</span><span class="sxs-lookup"><span data-stu-id="74b49-109">The **New-AzureRmRelayAuthorizationRule** cmdlet creates a new authorization rule for the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="74b49-110">示例</span><span class="sxs-lookup"><span data-stu-id="74b49-110">EXAMPLES</span></span>

### <span data-ttu-id="74b49-111">範例 1-命名空間</span><span class="sxs-lookup"><span data-stu-id="74b49-111">Example 1 - Namespace</span></span>
```
PS C:\>New-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -Rights "Listen"
```

<span data-ttu-id="74b49-112">建立 `AuthoRule1` 命名空間的 [ **偵聽** ] 許可權 `TestNameSpace-Relay1` 。</span><span class="sxs-lookup"><span data-stu-id="74b49-112">Creates `AuthoRule1` with **Listen** rights for the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="74b49-113">範例 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="74b49-113">Example 2 - WcfRelay</span></span>
```
PS C:\>New-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -Rights "Listen"
```

<span data-ttu-id="74b49-114">`AuthoRule1`使用 WcfRelay 的 [ **偵聽** ] 許可權建立授權規則 `TestWCFRelay1` 。</span><span class="sxs-lookup"><span data-stu-id="74b49-114">Creates authorization rule `AuthoRule1` with **Listen** rights for the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="74b49-115">範例 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="74b49-115">Example 3 - HybridConnection</span></span>
```
PS C:\>New-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -Rights "Listen"
```

<span data-ttu-id="74b49-116">建立 `AuthoRule1` 命名空間的 [ **偵聽** ] 許可權 `TestNameSpace-Relay1` 。</span><span class="sxs-lookup"><span data-stu-id="74b49-116">Creates `AuthoRule1` with **Listen** rights for the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="74b49-117">參數</span><span class="sxs-lookup"><span data-stu-id="74b49-117">PARAMETERS</span></span>

### <span data-ttu-id="74b49-118">-確認</span><span class="sxs-lookup"><span data-stu-id="74b49-118">-Confirm</span></span>
<span data-ttu-id="74b49-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="74b49-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74b49-120">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="74b49-120">-HybridConnection</span></span>
<span data-ttu-id="74b49-121">HybridConnection [名稱]。</span><span class="sxs-lookup"><span data-stu-id="74b49-121">HybridConnection Name.</span></span>

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

### <span data-ttu-id="74b49-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="74b49-122">-Name</span></span>
<span data-ttu-id="74b49-123">AuthorizationRule [名稱]。</span><span class="sxs-lookup"><span data-stu-id="74b49-123">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="74b49-124">-命名空間</span><span class="sxs-lookup"><span data-stu-id="74b49-124">-Namespace</span></span>
<span data-ttu-id="74b49-125">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="74b49-125">Namespace Name.</span></span>

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

### <span data-ttu-id="74b49-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74b49-126">-ResourceGroupName</span></span>
<span data-ttu-id="74b49-127">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="74b49-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="74b49-128">-許可權</span><span class="sxs-lookup"><span data-stu-id="74b49-128">-Rights</span></span>
<span data-ttu-id="74b49-129">權力，例如「聆聽」、「傳送」、「管理」</span><span class="sxs-lookup"><span data-stu-id="74b49-129">Rights, e.g. "Listen","Send","Manage"</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74b49-130">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="74b49-130">-WcfRelay</span></span>
<span data-ttu-id="74b49-131">WcfRelay [名稱]。</span><span class="sxs-lookup"><span data-stu-id="74b49-131">WcfRelay Name.</span></span>

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

### <span data-ttu-id="74b49-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74b49-132">-WhatIf</span></span>
<span data-ttu-id="74b49-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="74b49-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74b49-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="74b49-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74b49-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74b49-135">-DefaultProfile</span></span>
<span data-ttu-id="74b49-136">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="74b49-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74b49-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74b49-137">CommonParameters</span></span>
<span data-ttu-id="74b49-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="74b49-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74b49-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="74b49-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74b49-140">輸入</span><span class="sxs-lookup"><span data-stu-id="74b49-140">INPUTS</span></span>

### <span data-ttu-id="74b49-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74b49-141">-ResourceGroupName</span></span>
 <span data-ttu-id="74b49-142">System.object</span><span class="sxs-lookup"><span data-stu-id="74b49-142">System.String</span></span> 

### <span data-ttu-id="74b49-143">-命名空間</span><span class="sxs-lookup"><span data-stu-id="74b49-143">-Namespace</span></span>
 <span data-ttu-id="74b49-144">System.object</span><span class="sxs-lookup"><span data-stu-id="74b49-144">System.String</span></span> 
 

### <span data-ttu-id="74b49-145">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="74b49-145">-WcfRelay</span></span>
 <span data-ttu-id="74b49-146">System.object</span><span class="sxs-lookup"><span data-stu-id="74b49-146">System.String</span></span> 

### <span data-ttu-id="74b49-147">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="74b49-147">-HybridConnection</span></span>
 <span data-ttu-id="74b49-148">System.object</span><span class="sxs-lookup"><span data-stu-id="74b49-148">System.String</span></span> 
 

### <span data-ttu-id="74b49-149">-名稱</span><span class="sxs-lookup"><span data-stu-id="74b49-149">-Name</span></span>
 <span data-ttu-id="74b49-150">System.object</span><span class="sxs-lookup"><span data-stu-id="74b49-150">System.String</span></span>
 

### <span data-ttu-id="74b49-151">-許可權</span><span class="sxs-lookup"><span data-stu-id="74b49-151">-Rights</span></span>
 <span data-ttu-id="74b49-152">System.object []</span><span class="sxs-lookup"><span data-stu-id="74b49-152">System.String []</span></span>

## <span data-ttu-id="74b49-153">輸出</span><span class="sxs-lookup"><span data-stu-id="74b49-153">OUTPUTS</span></span>

### <span data-ttu-id="74b49-154">AuthorizationRuleAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="74b49-154">Microsoft.Azure.Commands.Relay.Models.AuthorizationRuleAttributes</span></span>

### <span data-ttu-id="74b49-155">範例 1-命名空間</span><span class="sxs-lookup"><span data-stu-id="74b49-155">Example 1 - Namespace</span></span>
<span data-ttu-id="74b49-156">許可權： {偵聽} 名稱： AuthoRule1 類型： Microsoft. 中繼/AuthorizationRules Id：/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="74b49-156">Rights : {Listen} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1</span></span>

### <span data-ttu-id="74b49-157">範例 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="74b49-157">Example 2 - WcfRelay</span></span>
<span data-ttu-id="74b49-158">許可權： {偵聽} 名稱： AuthoRule1 類型： Microsoft. 中繼/AuthorizationRules Id：/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="74b49-158">Rights : {Listen} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1</span></span>

### <span data-ttu-id="74b49-159">範例 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="74b49-159">Example 3 - HybridConnection</span></span>
<span data-ttu-id="74b49-160">許可權： {偵聽} 名稱： AuthoRule1 類型： Microsoft. 中繼/AuthorizationRules Id：/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="74b49-160">Rights : {Listen} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1</span></span>

## <span data-ttu-id="74b49-161">筆記</span><span class="sxs-lookup"><span data-stu-id="74b49-161">NOTES</span></span>

## <span data-ttu-id="74b49-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="74b49-162">RELATED LINKS</span></span>

