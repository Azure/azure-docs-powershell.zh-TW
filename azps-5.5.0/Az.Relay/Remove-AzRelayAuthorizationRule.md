---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/remove-azrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayAuthorizationRule.md
ms.openlocfilehash: f99330a7611964e8db3d41f4ece56bb247c1c403
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100128482"
---
# <span data-ttu-id="34c8d-101">Remove-AzRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="34c8d-101">Remove-AzRelayAuthorizationRule</span></span>

## <span data-ttu-id="34c8d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="34c8d-102">SYNOPSIS</span></span>
<span data-ttu-id="34c8d-103">從指定的中繼實體中移除 HybridConnection 的授權規則， (命名空間/WcfRelay/HybridConnection) 。</span><span class="sxs-lookup"><span data-stu-id="34c8d-103">Removes the authorization rule of a HybridConnection from the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="34c8d-104">句法</span><span class="sxs-lookup"><span data-stu-id="34c8d-104">SYNTAX</span></span>

### <span data-ttu-id="34c8d-105">NamespaceAuthorizationRuleSet (預設) </span><span class="sxs-lookup"><span data-stu-id="34c8d-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34c8d-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="34c8d-106">WcfRelayAuthorizationRuleSet</span></span>
```
Remove-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="34c8d-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="34c8d-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Remove-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-HybridConnection] <String> [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34c8d-108">說明</span><span class="sxs-lookup"><span data-stu-id="34c8d-108">DESCRIPTION</span></span>
<span data-ttu-id="34c8d-109">**AzRelayAuthorizationRule** Cmdlet 會移除指定之中繼實體的授權規則 (命名空間/WcfRelay/HybridConnection) 。</span><span class="sxs-lookup"><span data-stu-id="34c8d-109">The **Remove-AzRelayAuthorizationRule** cmdlet removes the authorization rule of the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="34c8d-110">示例</span><span class="sxs-lookup"><span data-stu-id="34c8d-110">EXAMPLES</span></span>

### <span data-ttu-id="34c8d-111">範例1</span><span class="sxs-lookup"><span data-stu-id="34c8d-111">Example 1</span></span>
```
PS C:\> Remove-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1
```

<span data-ttu-id="34c8d-112">移除命名空間的授權規則 `AuthoRule1` `TestNameSpace-Relay1` 。</span><span class="sxs-lookup"><span data-stu-id="34c8d-112">Removes the authorization rule `AuthoRule1` of the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="34c8d-113">範例2</span><span class="sxs-lookup"><span data-stu-id="34c8d-113">Example 2</span></span>
```
PS C:\> Remove-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWcfRelay -Name AuthoRule1
```

<span data-ttu-id="34c8d-114">`AuthoRule1`從命名空間移除 WcfRelay 的授權規則 `TestWcfRelay` `TestNameSpace-Relay1` 。</span><span class="sxs-lookup"><span data-stu-id="34c8d-114">Removes the authorization rule `AuthoRule1` of the WcfRelay `TestWcfRelay` from the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="34c8d-115">範例3</span><span class="sxs-lookup"><span data-stu-id="34c8d-115">Example 3</span></span>
```
PS C:\> Remove-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1
```

<span data-ttu-id="34c8d-116">`AuthoRule1`從命名空間移除 HybridConnection 的授權規則 `TestHybridConnection` `TestNameSpace-Relay1` 。</span><span class="sxs-lookup"><span data-stu-id="34c8d-116">Removes the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="34c8d-117">參數</span><span class="sxs-lookup"><span data-stu-id="34c8d-117">PARAMETERS</span></span>

### <span data-ttu-id="34c8d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34c8d-118">-DefaultProfile</span></span>
<span data-ttu-id="34c8d-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="34c8d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34c8d-120">-Force</span><span class="sxs-lookup"><span data-stu-id="34c8d-120">-Force</span></span>
<span data-ttu-id="34c8d-121">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="34c8d-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="34c8d-122">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="34c8d-122">-HybridConnection</span></span>
<span data-ttu-id="34c8d-123">HybridConnection [名稱]。</span><span class="sxs-lookup"><span data-stu-id="34c8d-123">HybridConnection Name.</span></span>

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

### <span data-ttu-id="34c8d-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="34c8d-124">-Name</span></span>
<span data-ttu-id="34c8d-125">AuthorizationRule [名稱]。</span><span class="sxs-lookup"><span data-stu-id="34c8d-125">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="34c8d-126">-命名空間</span><span class="sxs-lookup"><span data-stu-id="34c8d-126">-Namespace</span></span>
<span data-ttu-id="34c8d-127">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="34c8d-127">Namespace Name.</span></span>

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

### <span data-ttu-id="34c8d-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="34c8d-128">-PassThru</span></span>
<span data-ttu-id="34c8d-129">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="34c8d-129">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="34c8d-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34c8d-130">-ResourceGroupName</span></span>
<span data-ttu-id="34c8d-131">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="34c8d-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="34c8d-132">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="34c8d-132">-WcfRelay</span></span>
<span data-ttu-id="34c8d-133">WcfRelay [名稱]。</span><span class="sxs-lookup"><span data-stu-id="34c8d-133">WcfRelay Name.</span></span>

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

### <span data-ttu-id="34c8d-134">-確認</span><span class="sxs-lookup"><span data-stu-id="34c8d-134">-Confirm</span></span>
<span data-ttu-id="34c8d-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="34c8d-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34c8d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34c8d-136">-WhatIf</span></span>
<span data-ttu-id="34c8d-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="34c8d-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34c8d-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="34c8d-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34c8d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34c8d-139">CommonParameters</span></span>
<span data-ttu-id="34c8d-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="34c8d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34c8d-141">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="34c8d-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34c8d-142">輸入</span><span class="sxs-lookup"><span data-stu-id="34c8d-142">INPUTS</span></span>

### <span data-ttu-id="34c8d-143">System.object</span><span class="sxs-lookup"><span data-stu-id="34c8d-143">System.String</span></span>

## <span data-ttu-id="34c8d-144">輸出</span><span class="sxs-lookup"><span data-stu-id="34c8d-144">OUTPUTS</span></span>

### <span data-ttu-id="34c8d-145">System.object</span><span class="sxs-lookup"><span data-stu-id="34c8d-145">System.Boolean</span></span>

## <span data-ttu-id="34c8d-146">筆記</span><span class="sxs-lookup"><span data-stu-id="34c8d-146">NOTES</span></span>

## <span data-ttu-id="34c8d-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="34c8d-147">RELATED LINKS</span></span>
