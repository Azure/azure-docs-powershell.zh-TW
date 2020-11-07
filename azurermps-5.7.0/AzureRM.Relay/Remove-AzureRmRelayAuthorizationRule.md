---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/remove-azurermrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayAuthorizationRule.md
ms.openlocfilehash: 62d37b30f20cf6d0738cfc927c266d6869be5586
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624686"
---
# <span data-ttu-id="65734-101">Remove-AzureRmRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="65734-101">Remove-AzureRmRelayAuthorizationRule</span></span>

## <span data-ttu-id="65734-102">摘要</span><span class="sxs-lookup"><span data-stu-id="65734-102">SYNOPSIS</span></span>
<span data-ttu-id="65734-103">從指定的中繼實體中移除 HybridConnection 的授權規則， (命名空間/WcfRelay/HybridConnection) 。</span><span class="sxs-lookup"><span data-stu-id="65734-103">Removes the authorization rule of a HybridConnection from the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65734-104">句法</span><span class="sxs-lookup"><span data-stu-id="65734-104">SYNTAX</span></span>

### <span data-ttu-id="65734-105">NamespaceAuthorizationRuleSet (預設) </span><span class="sxs-lookup"><span data-stu-id="65734-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65734-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="65734-106">WcfRelayAuthorizationRuleSet</span></span>
```
Remove-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="65734-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="65734-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Remove-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-HybridConnection] <String> [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65734-108">說明</span><span class="sxs-lookup"><span data-stu-id="65734-108">DESCRIPTION</span></span>
<span data-ttu-id="65734-109">**AzureRmRelayAuthorizationRule** Cmdlet 會移除指定之中繼實體的授權規則 (命名空間/WcfRelay/HybridConnection) 。</span><span class="sxs-lookup"><span data-stu-id="65734-109">The **Remove-AzureRmRelayAuthorizationRule** cmdlet removes the authorization rule of the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="65734-110">示例</span><span class="sxs-lookup"><span data-stu-id="65734-110">EXAMPLES</span></span>

### <span data-ttu-id="65734-111">範例1</span><span class="sxs-lookup"><span data-stu-id="65734-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1
```

<span data-ttu-id="65734-112">移除命名空間的授權規則 `AuthoRule1` `TestNameSpace-Relay1` 。</span><span class="sxs-lookup"><span data-stu-id="65734-112">Removes the authorization rule `AuthoRule1` of the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="65734-113">範例2</span><span class="sxs-lookup"><span data-stu-id="65734-113">Example 2</span></span>
```
PS C:\> Remove-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWcfRelay -Name AuthoRule1
```

<span data-ttu-id="65734-114">`AuthoRule1`從命名空間移除 WcfRelay 的授權規則 `TestWcfRelay` `TestNameSpace-Relay1` 。</span><span class="sxs-lookup"><span data-stu-id="65734-114">Removes the authorization rule `AuthoRule1` of the WcfRelay `TestWcfRelay` from the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="65734-115">範例3</span><span class="sxs-lookup"><span data-stu-id="65734-115">Example 3</span></span>
```
PS C:\> Remove-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1
```

<span data-ttu-id="65734-116">`AuthoRule1`從命名空間移除 HybridConnection 的授權規則 `TestHybridConnection` `TestNameSpace-Relay1` 。</span><span class="sxs-lookup"><span data-stu-id="65734-116">Removes the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="65734-117">參數</span><span class="sxs-lookup"><span data-stu-id="65734-117">PARAMETERS</span></span>

### <span data-ttu-id="65734-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65734-118">-DefaultProfile</span></span>
<span data-ttu-id="65734-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="65734-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65734-120">-Force</span><span class="sxs-lookup"><span data-stu-id="65734-120">-Force</span></span>
<span data-ttu-id="65734-121">不要求確認</span><span class="sxs-lookup"><span data-stu-id="65734-121">Do not ask for confirmation</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65734-122">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="65734-122">-HybridConnection</span></span>
<span data-ttu-id="65734-123">HybridConnection [名稱]。</span><span class="sxs-lookup"><span data-stu-id="65734-123">HybridConnection Name.</span></span>

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

### <span data-ttu-id="65734-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="65734-124">-Name</span></span>
<span data-ttu-id="65734-125">AuthorizationRule [名稱]。</span><span class="sxs-lookup"><span data-stu-id="65734-125">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="65734-126">-命名空間</span><span class="sxs-lookup"><span data-stu-id="65734-126">-Namespace</span></span>
<span data-ttu-id="65734-127">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="65734-127">Namespace Name.</span></span>

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

### <span data-ttu-id="65734-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="65734-128">-PassThru</span></span>
<span data-ttu-id="65734-129">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="65734-129">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65734-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65734-130">-ResourceGroupName</span></span>
<span data-ttu-id="65734-131">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="65734-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="65734-132">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="65734-132">-WcfRelay</span></span>
<span data-ttu-id="65734-133">WcfRelay [名稱]。</span><span class="sxs-lookup"><span data-stu-id="65734-133">WcfRelay Name.</span></span>

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

### <span data-ttu-id="65734-134">-確認</span><span class="sxs-lookup"><span data-stu-id="65734-134">-Confirm</span></span>
<span data-ttu-id="65734-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="65734-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65734-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65734-136">-WhatIf</span></span>
<span data-ttu-id="65734-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="65734-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65734-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="65734-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65734-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65734-139">CommonParameters</span></span>
<span data-ttu-id="65734-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="65734-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65734-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="65734-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65734-142">輸入</span><span class="sxs-lookup"><span data-stu-id="65734-142">INPUTS</span></span>

### <span data-ttu-id="65734-143">System.object</span><span class="sxs-lookup"><span data-stu-id="65734-143">System.String</span></span>

## <span data-ttu-id="65734-144">輸出</span><span class="sxs-lookup"><span data-stu-id="65734-144">OUTPUTS</span></span>

### <span data-ttu-id="65734-145">System.object</span><span class="sxs-lookup"><span data-stu-id="65734-145">System.Boolean</span></span>

## <span data-ttu-id="65734-146">筆記</span><span class="sxs-lookup"><span data-stu-id="65734-146">NOTES</span></span>

## <span data-ttu-id="65734-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="65734-147">RELATED LINKS</span></span>
