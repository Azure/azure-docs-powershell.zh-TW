---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/remove-azservicebusiprule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusIPRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusIPRule.md
ms.openlocfilehash: e14d82fbf503487ddb4e4ebac1385400305e9209
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915225"
---
# <span data-ttu-id="93dd0-101">Remove-AzServiceBusIPRule</span><span class="sxs-lookup"><span data-stu-id="93dd0-101">Remove-AzServiceBusIPRule</span></span>

## <span data-ttu-id="93dd0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="93dd0-102">SYNOPSIS</span></span>
<span data-ttu-id="93dd0-103">將單一 IP 規則移除至給定命名空間的 NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="93dd0-103">Remove a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="93dd0-104">語法</span><span class="sxs-lookup"><span data-stu-id="93dd0-104">SYNTAX</span></span>

### <span data-ttu-id="93dd0-105">IPRulePropertiesParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="93dd0-105">IPRulePropertiesParameterSet (Default)</span></span>
```
Remove-AzServiceBusIPRule [-ResourceGroupName] <String> [-Name] <String> [-IpMask] <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93dd0-106">IPRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="93dd0-106">IPRuleInputObjectParameterSet</span></span>
```
Remove-AzServiceBusIPRule [-ResourceGroupName] <String> [-Name] <String>
 [-IpRuleObject] <PSNWRuleSetIpRulesAttributes> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93dd0-107">描述</span><span class="sxs-lookup"><span data-stu-id="93dd0-107">DESCRIPTION</span></span>
<span data-ttu-id="93dd0-108">將單一 IP 規則移除至給定命名空間的 NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="93dd0-108">Remove a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="93dd0-109">例子</span><span class="sxs-lookup"><span data-stu-id="93dd0-109">EXAMPLES</span></span>

### <span data-ttu-id="93dd0-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="93dd0-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusIPRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -IpMask "11.22.33.44"
```

<span data-ttu-id="93dd0-111">移除給定命名空間 NetworkRuleSet 的 IpMask</span><span class="sxs-lookup"><span data-stu-id="93dd0-111">Removes IpMask of the NetworkRuleSet of the given namespace</span></span>

## <span data-ttu-id="93dd0-112">參數</span><span class="sxs-lookup"><span data-stu-id="93dd0-112">PARAMETERS</span></span>

### <span data-ttu-id="93dd0-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="93dd0-113">-AsJob</span></span>
<span data-ttu-id="93dd0-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="93dd0-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="93dd0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93dd0-115">-DefaultProfile</span></span>
<span data-ttu-id="93dd0-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="93dd0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93dd0-117">-IpMask</span><span class="sxs-lookup"><span data-stu-id="93dd0-117">-IpMask</span></span>
<span data-ttu-id="93dd0-118">子網資源識別碼</span><span class="sxs-lookup"><span data-stu-id="93dd0-118">Subnet Resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: IPRulePropertiesParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93dd0-119">-IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="93dd0-119">-IpRuleObject</span></span>
<span data-ttu-id="93dd0-120">IPRule Configuration 物件</span><span class="sxs-lookup"><span data-stu-id="93dd0-120">IPRule Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes
Parameter Sets: IPRuleInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="93dd0-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="93dd0-121">-Name</span></span>
<span data-ttu-id="93dd0-122">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="93dd0-122">Namespace Name</span></span>

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

### <span data-ttu-id="93dd0-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="93dd0-123">-PassThru</span></span>
<span data-ttu-id="93dd0-124">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="93dd0-124">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="93dd0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93dd0-125">-ResourceGroupName</span></span>
<span data-ttu-id="93dd0-126">資源組名</span><span class="sxs-lookup"><span data-stu-id="93dd0-126">Resource Group Name</span></span>

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

### <span data-ttu-id="93dd0-127">-確認</span><span class="sxs-lookup"><span data-stu-id="93dd0-127">-Confirm</span></span>
<span data-ttu-id="93dd0-128">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="93dd0-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93dd0-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93dd0-129">-WhatIf</span></span>
<span data-ttu-id="93dd0-130">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="93dd0-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93dd0-131">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="93dd0-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93dd0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93dd0-132">CommonParameters</span></span>
<span data-ttu-id="93dd0-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="93dd0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="93dd0-134">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="93dd0-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93dd0-135">輸入</span><span class="sxs-lookup"><span data-stu-id="93dd0-135">INPUTS</span></span>

### <span data-ttu-id="93dd0-136">System.String</span><span class="sxs-lookup"><span data-stu-id="93dd0-136">System.String</span></span>

### <span data-ttu-id="93dd0-137">Microsoft.Azure.Commands.ServiceBus.models.PSNWRuleSetipRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="93dd0-137">Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes</span></span>

## <span data-ttu-id="93dd0-138">輸出</span><span class="sxs-lookup"><span data-stu-id="93dd0-138">OUTPUTS</span></span>

### <span data-ttu-id="93dd0-139">Microsoft.Azure.Commands.ServiceBus.models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="93dd0-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="93dd0-140">筆記</span><span class="sxs-lookup"><span data-stu-id="93dd0-140">NOTES</span></span>

## <span data-ttu-id="93dd0-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="93dd0-141">RELATED LINKS</span></span>
