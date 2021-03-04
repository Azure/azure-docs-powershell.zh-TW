---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/powershell/module/az.relay/remove-azrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayAuthorizationRule.md
ms.openlocfilehash: 1284780428fdaacfc255faf2ac640565eec44950
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914574"
---
# <span data-ttu-id="2e96e-101">Remove-AzRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="2e96e-101">Remove-AzRelayAuthorizationRule</span></span>

## <span data-ttu-id="2e96e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2e96e-102">SYNOPSIS</span></span>
<span data-ttu-id="2e96e-103">移除來自命名空間/WcfRelay/HybridConnection (之給定 Relay 實體的混合式連接) 。</span><span class="sxs-lookup"><span data-stu-id="2e96e-103">Removes the authorization rule of a HybridConnection from the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="2e96e-104">語法</span><span class="sxs-lookup"><span data-stu-id="2e96e-104">SYNTAX</span></span>

### <span data-ttu-id="2e96e-105">命名空間驗證RuleSet (預設) </span><span class="sxs-lookup"><span data-stu-id="2e96e-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e96e-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="2e96e-106">WcfRelayAuthorizationRuleSet</span></span>
```
Remove-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2e96e-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="2e96e-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Remove-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-HybridConnection] <String> [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e96e-108">描述</span><span class="sxs-lookup"><span data-stu-id="2e96e-108">DESCRIPTION</span></span>
<span data-ttu-id="2e96e-109">**Remove-AzRelayAuthorizationRule** Cmdlet 會移除給定轉寄實體的授權規則 (命名空間/WcfRelay/HybridConnection) 。</span><span class="sxs-lookup"><span data-stu-id="2e96e-109">The **Remove-AzRelayAuthorizationRule** cmdlet removes the authorization rule of the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="2e96e-110">例子</span><span class="sxs-lookup"><span data-stu-id="2e96e-110">EXAMPLES</span></span>

### <span data-ttu-id="2e96e-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="2e96e-111">Example 1</span></span>
```
PS C:\> Remove-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1
```

<span data-ttu-id="2e96e-112">移除命名空間的授權 `AuthoRule1` 規則 `TestNameSpace-Relay1` 。</span><span class="sxs-lookup"><span data-stu-id="2e96e-112">Removes the authorization rule `AuthoRule1` of the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="2e96e-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="2e96e-113">Example 2</span></span>
```
PS C:\> Remove-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWcfRelay -Name AuthoRule1
```

<span data-ttu-id="2e96e-114">從命名空間移除 `AuthoRule1` WcfRelay `TestWcfRelay` 的授權規則 `TestNameSpace-Relay1` 。</span><span class="sxs-lookup"><span data-stu-id="2e96e-114">Removes the authorization rule `AuthoRule1` of the WcfRelay `TestWcfRelay` from the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="2e96e-115">範例 3</span><span class="sxs-lookup"><span data-stu-id="2e96e-115">Example 3</span></span>
```
PS C:\> Remove-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1
```

<span data-ttu-id="2e96e-116">移除命名空間中 `AuthoRule1` HybridConnection `TestHybridConnection` 的授權規則 `TestNameSpace-Relay1` 。</span><span class="sxs-lookup"><span data-stu-id="2e96e-116">Removes the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="2e96e-117">參數</span><span class="sxs-lookup"><span data-stu-id="2e96e-117">PARAMETERS</span></span>

### <span data-ttu-id="2e96e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e96e-118">-DefaultProfile</span></span>
<span data-ttu-id="2e96e-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2e96e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e96e-120">-強制</span><span class="sxs-lookup"><span data-stu-id="2e96e-120">-Force</span></span>
<span data-ttu-id="2e96e-121">請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="2e96e-121">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e96e-122">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="2e96e-122">-HybridConnection</span></span>
<span data-ttu-id="2e96e-123">HybridConnection 名稱。</span><span class="sxs-lookup"><span data-stu-id="2e96e-123">HybridConnection Name.</span></span>

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

### <span data-ttu-id="2e96e-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="2e96e-124">-Name</span></span>
<span data-ttu-id="2e96e-125">AuthorizationRule Name.</span><span class="sxs-lookup"><span data-stu-id="2e96e-125">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="2e96e-126">-命名空間</span><span class="sxs-lookup"><span data-stu-id="2e96e-126">-Namespace</span></span>
<span data-ttu-id="2e96e-127">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="2e96e-127">Namespace Name.</span></span>

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

### <span data-ttu-id="2e96e-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2e96e-128">-PassThru</span></span>
<span data-ttu-id="2e96e-129">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="2e96e-129">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e96e-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e96e-130">-ResourceGroupName</span></span>
<span data-ttu-id="2e96e-131">資源組名。</span><span class="sxs-lookup"><span data-stu-id="2e96e-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="2e96e-132">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="2e96e-132">-WcfRelay</span></span>
<span data-ttu-id="2e96e-133">WcfRelay 名稱。</span><span class="sxs-lookup"><span data-stu-id="2e96e-133">WcfRelay Name.</span></span>

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

### <span data-ttu-id="2e96e-134">-確認</span><span class="sxs-lookup"><span data-stu-id="2e96e-134">-Confirm</span></span>
<span data-ttu-id="2e96e-135">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="2e96e-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e96e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e96e-136">-WhatIf</span></span>
<span data-ttu-id="2e96e-137">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2e96e-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e96e-138">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2e96e-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e96e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e96e-139">CommonParameters</span></span>
<span data-ttu-id="2e96e-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2e96e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e96e-141">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="2e96e-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e96e-142">輸入</span><span class="sxs-lookup"><span data-stu-id="2e96e-142">INPUTS</span></span>

### <span data-ttu-id="2e96e-143">System.String</span><span class="sxs-lookup"><span data-stu-id="2e96e-143">System.String</span></span>

## <span data-ttu-id="2e96e-144">輸出</span><span class="sxs-lookup"><span data-stu-id="2e96e-144">OUTPUTS</span></span>

### <span data-ttu-id="2e96e-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2e96e-145">System.Boolean</span></span>

## <span data-ttu-id="2e96e-146">筆記</span><span class="sxs-lookup"><span data-stu-id="2e96e-146">NOTES</span></span>

## <span data-ttu-id="2e96e-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="2e96e-147">RELATED LINKS</span></span>
