---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusiprule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusIPRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusIPRule.md
ms.openlocfilehash: 3fc71bb4e460cb7763fc437f0bc2ac31860dccdf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93620616"
---
# <span data-ttu-id="f8d53-101">Remove-AzServiceBusIPRule</span><span class="sxs-lookup"><span data-stu-id="f8d53-101">Remove-AzServiceBusIPRule</span></span>

## <span data-ttu-id="f8d53-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f8d53-102">SYNOPSIS</span></span>
<span data-ttu-id="f8d53-103">移除單一 IPrule 到指定命名空間的 NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="f8d53-103">Remove a single IPrule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="f8d53-104">句法</span><span class="sxs-lookup"><span data-stu-id="f8d53-104">SYNTAX</span></span>

### <span data-ttu-id="f8d53-105">IPRulePropertiesParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="f8d53-105">IPRulePropertiesParameterSet (Default)</span></span>
```
Remove-AzServiceBusIPRule [-ResourceGroupName] <String> [-Name] <String> [-IpMask] <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8d53-106">IPRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f8d53-106">IPRuleInputObjectParameterSet</span></span>
```
Remove-AzServiceBusIPRule [-ResourceGroupName] <String> [-Name] <String>
 [-IpRuleObject] <PSNWRuleSetIpRulesAttributes> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8d53-107">說明</span><span class="sxs-lookup"><span data-stu-id="f8d53-107">DESCRIPTION</span></span>
<span data-ttu-id="f8d53-108">移除單一 IPrule 到指定命名空間的 NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="f8d53-108">Remove a single IPrule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="f8d53-109">示例</span><span class="sxs-lookup"><span data-stu-id="f8d53-109">EXAMPLES</span></span>

### <span data-ttu-id="f8d53-110">範例1</span><span class="sxs-lookup"><span data-stu-id="f8d53-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusIPRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -IpMask "11.22.33.44"
```

<span data-ttu-id="f8d53-111">移除指定命名空間之 NetworkRuleSet 的 IpMask</span><span class="sxs-lookup"><span data-stu-id="f8d53-111">Removes IpMask of the NetworkRuleSet of the given namespace</span></span>

## <span data-ttu-id="f8d53-112">參數</span><span class="sxs-lookup"><span data-stu-id="f8d53-112">PARAMETERS</span></span>

### <span data-ttu-id="f8d53-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f8d53-113">-AsJob</span></span>
<span data-ttu-id="f8d53-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f8d53-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f8d53-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8d53-115">-DefaultProfile</span></span>
<span data-ttu-id="f8d53-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f8d53-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8d53-117">-IpMask</span><span class="sxs-lookup"><span data-stu-id="f8d53-117">-IpMask</span></span>
<span data-ttu-id="f8d53-118">子網資源識別碼</span><span class="sxs-lookup"><span data-stu-id="f8d53-118">Subnet Resource ID</span></span>

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

### <span data-ttu-id="f8d53-119">-IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="f8d53-119">-IpRuleObject</span></span>
<span data-ttu-id="f8d53-120">IPRule Configuration 物件</span><span class="sxs-lookup"><span data-stu-id="f8d53-120">IPRule Configuration Object</span></span>

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

### <span data-ttu-id="f8d53-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="f8d53-121">-Name</span></span>
<span data-ttu-id="f8d53-122">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="f8d53-122">Namespace Name</span></span>

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

### <span data-ttu-id="f8d53-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f8d53-123">-PassThru</span></span>
<span data-ttu-id="f8d53-124">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="f8d53-124">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="f8d53-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8d53-125">-ResourceGroupName</span></span>
<span data-ttu-id="f8d53-126">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="f8d53-126">Resource Group Name</span></span>

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

### <span data-ttu-id="f8d53-127">-確認</span><span class="sxs-lookup"><span data-stu-id="f8d53-127">-Confirm</span></span>
<span data-ttu-id="f8d53-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f8d53-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8d53-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8d53-129">-WhatIf</span></span>
<span data-ttu-id="f8d53-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f8d53-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8d53-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f8d53-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8d53-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8d53-132">CommonParameters</span></span>
<span data-ttu-id="f8d53-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f8d53-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="f8d53-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f8d53-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8d53-135">輸入</span><span class="sxs-lookup"><span data-stu-id="f8d53-135">INPUTS</span></span>

### <span data-ttu-id="f8d53-136">System.object</span><span class="sxs-lookup"><span data-stu-id="f8d53-136">System.String</span></span>

### <span data-ttu-id="f8d53-137">PSNWRuleSetIpRulesAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f8d53-137">Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes</span></span>

## <span data-ttu-id="f8d53-138">輸出</span><span class="sxs-lookup"><span data-stu-id="f8d53-138">OUTPUTS</span></span>

### <span data-ttu-id="f8d53-139">PSNetworkRuleSetAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f8d53-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="f8d53-140">筆記</span><span class="sxs-lookup"><span data-stu-id="f8d53-140">NOTES</span></span>

## <span data-ttu-id="f8d53-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="f8d53-141">RELATED LINKS</span></span>
