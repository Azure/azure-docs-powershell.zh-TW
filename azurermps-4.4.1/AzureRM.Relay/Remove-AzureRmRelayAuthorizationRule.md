---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayAuthorizationRule.md
ms.openlocfilehash: 8eaf2ff99fe7f3ea49d73af95eb4482c645be59f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625080"
---
# <span data-ttu-id="58fce-101">Remove-AzureRmRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="58fce-101">Remove-AzureRmRelayAuthorizationRule</span></span>

## <span data-ttu-id="58fce-102">摘要</span><span class="sxs-lookup"><span data-stu-id="58fce-102">SYNOPSIS</span></span>
<span data-ttu-id="58fce-103">從指定的中繼實體中移除 HybridConnection 的授權規則， (命名空間/WcfRelay/HybridConnection) 。</span><span class="sxs-lookup"><span data-stu-id="58fce-103">Removes the authorization rule of a HybridConnection from the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58fce-104">句法</span><span class="sxs-lookup"><span data-stu-id="58fce-104">SYNTAX</span></span>

### <span data-ttu-id="58fce-105">NamespaceAuthorizationRuleSet (預設) </span><span class="sxs-lookup"><span data-stu-id="58fce-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58fce-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="58fce-106">WcfRelayAuthorizationRuleSet</span></span>
```
Remove-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="58fce-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="58fce-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Remove-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-HybridConnection] <String> [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58fce-108">說明</span><span class="sxs-lookup"><span data-stu-id="58fce-108">DESCRIPTION</span></span>
<span data-ttu-id="58fce-109">**AzureRmRelayAuthorizationRule** Cmdlet 會移除指定之中繼實體的授權規則 (命名空間/WcfRelay/HybridConnection) 。</span><span class="sxs-lookup"><span data-stu-id="58fce-109">The **Remove-AzureRmRelayAuthorizationRule** cmdlet removes the authorization rule of the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="58fce-110">示例</span><span class="sxs-lookup"><span data-stu-id="58fce-110">EXAMPLES</span></span>

### <span data-ttu-id="58fce-111">範例1</span><span class="sxs-lookup"><span data-stu-id="58fce-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1
```

<span data-ttu-id="58fce-112">移除命名空間的授權規則 `AuthoRule1` `TestNameSpace-Relay1` 。</span><span class="sxs-lookup"><span data-stu-id="58fce-112">Removes the authorization rule `AuthoRule1` of the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="58fce-113">範例2</span><span class="sxs-lookup"><span data-stu-id="58fce-113">Example 2</span></span>
```
PS C:\> Remove-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWcfRelay -Name AuthoRule1
```

<span data-ttu-id="58fce-114">`AuthoRule1`從命名空間移除 WcfRelay 的授權規則 `TestWcfRelay` `TestNameSpace-Relay1` 。</span><span class="sxs-lookup"><span data-stu-id="58fce-114">Removes the authorization rule `AuthoRule1` of the WcfRelay `TestWcfRelay` from the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="58fce-115">範例3</span><span class="sxs-lookup"><span data-stu-id="58fce-115">Example 3</span></span>
```
PS C:\> Remove-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1
```

<span data-ttu-id="58fce-116">`AuthoRule1`從命名空間移除 HybridConnection 的授權規則 `TestHybridConnection` `TestNameSpace-Relay1` 。</span><span class="sxs-lookup"><span data-stu-id="58fce-116">Removes the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="58fce-117">參數</span><span class="sxs-lookup"><span data-stu-id="58fce-117">PARAMETERS</span></span>

### <span data-ttu-id="58fce-118">-確認</span><span class="sxs-lookup"><span data-stu-id="58fce-118">-Confirm</span></span>
<span data-ttu-id="58fce-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="58fce-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58fce-120">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="58fce-120">-HybridConnection</span></span>
<span data-ttu-id="58fce-121">HybridConnection [名稱]。</span><span class="sxs-lookup"><span data-stu-id="58fce-121">HybridConnection Name.</span></span>

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

### <span data-ttu-id="58fce-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="58fce-122">-Name</span></span>
<span data-ttu-id="58fce-123">AuthorizationRule [名稱]。</span><span class="sxs-lookup"><span data-stu-id="58fce-123">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="58fce-124">-命名空間</span><span class="sxs-lookup"><span data-stu-id="58fce-124">-Namespace</span></span>
<span data-ttu-id="58fce-125">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="58fce-125">Namespace Name.</span></span>

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

### <span data-ttu-id="58fce-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58fce-126">-ResourceGroupName</span></span>
<span data-ttu-id="58fce-127">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="58fce-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="58fce-128">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="58fce-128">-WcfRelay</span></span>
<span data-ttu-id="58fce-129">WcfRelay [名稱]。</span><span class="sxs-lookup"><span data-stu-id="58fce-129">WcfRelay Name.</span></span>

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

### <span data-ttu-id="58fce-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58fce-130">-WhatIf</span></span>
<span data-ttu-id="58fce-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="58fce-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58fce-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="58fce-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58fce-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58fce-133">-DefaultProfile</span></span>
<span data-ttu-id="58fce-134">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="58fce-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58fce-135">-Force</span><span class="sxs-lookup"><span data-stu-id="58fce-135">-Force</span></span>
<span data-ttu-id="58fce-136">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="58fce-136">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="58fce-137">-PassThru</span><span class="sxs-lookup"><span data-stu-id="58fce-137">-PassThru</span></span>
<span data-ttu-id="58fce-138">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="58fce-138">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="58fce-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58fce-139">CommonParameters</span></span>
<span data-ttu-id="58fce-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="58fce-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58fce-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="58fce-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58fce-142">輸入</span><span class="sxs-lookup"><span data-stu-id="58fce-142">INPUTS</span></span>

### <span data-ttu-id="58fce-143">System.object</span><span class="sxs-lookup"><span data-stu-id="58fce-143">System.String</span></span>

## <span data-ttu-id="58fce-144">輸出</span><span class="sxs-lookup"><span data-stu-id="58fce-144">OUTPUTS</span></span>

### <span data-ttu-id="58fce-145">System.object</span><span class="sxs-lookup"><span data-stu-id="58fce-145">System.Boolean</span></span>

## <span data-ttu-id="58fce-146">筆記</span><span class="sxs-lookup"><span data-stu-id="58fce-146">NOTES</span></span>

## <span data-ttu-id="58fce-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="58fce-147">RELATED LINKS</span></span>

