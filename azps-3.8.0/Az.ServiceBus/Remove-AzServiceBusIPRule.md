---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusiprule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusIPRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusIPRule.md
ms.openlocfilehash: 90c832d36017aa02a05d972a7b6e26fffd93937e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957239"
---
# <span data-ttu-id="93ace-101">Remove-AzServiceBusIPRule</span><span class="sxs-lookup"><span data-stu-id="93ace-101">Remove-AzServiceBusIPRule</span></span>

## <span data-ttu-id="93ace-102">摘要</span><span class="sxs-lookup"><span data-stu-id="93ace-102">SYNOPSIS</span></span>
<span data-ttu-id="93ace-103">移除單一 IP 規則至指定命名空間的 NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="93ace-103">Remove a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="93ace-104">句法</span><span class="sxs-lookup"><span data-stu-id="93ace-104">SYNTAX</span></span>

### <span data-ttu-id="93ace-105">IPRulePropertiesParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="93ace-105">IPRulePropertiesParameterSet (Default)</span></span>
```
Remove-AzServiceBusIPRule [-ResourceGroupName] <String> [-Name] <String> [-IpMask] <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93ace-106">IPRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="93ace-106">IPRuleInputObjectParameterSet</span></span>
```
Remove-AzServiceBusIPRule [-ResourceGroupName] <String> [-Name] <String>
 [-IpRuleObject] <PSNWRuleSetIpRulesAttributes> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93ace-107">說明</span><span class="sxs-lookup"><span data-stu-id="93ace-107">DESCRIPTION</span></span>
<span data-ttu-id="93ace-108">移除單一 IP 規則至指定命名空間的 NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="93ace-108">Remove a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="93ace-109">示例</span><span class="sxs-lookup"><span data-stu-id="93ace-109">EXAMPLES</span></span>

### <span data-ttu-id="93ace-110">範例1</span><span class="sxs-lookup"><span data-stu-id="93ace-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusIPRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -IpMask "11.22.33.44"
```

<span data-ttu-id="93ace-111">移除指定命名空間之 NetworkRuleSet 的 IpMask</span><span class="sxs-lookup"><span data-stu-id="93ace-111">Removes IpMask of the NetworkRuleSet of the given namespace</span></span>

## <span data-ttu-id="93ace-112">參數</span><span class="sxs-lookup"><span data-stu-id="93ace-112">PARAMETERS</span></span>

### <span data-ttu-id="93ace-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="93ace-113">-AsJob</span></span>
<span data-ttu-id="93ace-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="93ace-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="93ace-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93ace-115">-DefaultProfile</span></span>
<span data-ttu-id="93ace-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="93ace-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93ace-117">-IpMask</span><span class="sxs-lookup"><span data-stu-id="93ace-117">-IpMask</span></span>
<span data-ttu-id="93ace-118">子網資源識別碼</span><span class="sxs-lookup"><span data-stu-id="93ace-118">Subnet Resource ID</span></span>

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

### <span data-ttu-id="93ace-119">-IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="93ace-119">-IpRuleObject</span></span>
<span data-ttu-id="93ace-120">IPRule Configuration 物件</span><span class="sxs-lookup"><span data-stu-id="93ace-120">IPRule Configuration Object</span></span>

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

### <span data-ttu-id="93ace-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="93ace-121">-Name</span></span>
<span data-ttu-id="93ace-122">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="93ace-122">Namespace Name</span></span>

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

### <span data-ttu-id="93ace-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="93ace-123">-PassThru</span></span>
<span data-ttu-id="93ace-124">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="93ace-124">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="93ace-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93ace-125">-ResourceGroupName</span></span>
<span data-ttu-id="93ace-126">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="93ace-126">Resource Group Name</span></span>

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

### <span data-ttu-id="93ace-127">-確認</span><span class="sxs-lookup"><span data-stu-id="93ace-127">-Confirm</span></span>
<span data-ttu-id="93ace-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="93ace-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93ace-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93ace-129">-WhatIf</span></span>
<span data-ttu-id="93ace-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="93ace-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93ace-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="93ace-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93ace-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93ace-132">CommonParameters</span></span>
<span data-ttu-id="93ace-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="93ace-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="93ace-134">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="93ace-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93ace-135">輸入</span><span class="sxs-lookup"><span data-stu-id="93ace-135">INPUTS</span></span>

### <span data-ttu-id="93ace-136">System.object</span><span class="sxs-lookup"><span data-stu-id="93ace-136">System.String</span></span>

### <span data-ttu-id="93ace-137">PSNWRuleSetIpRulesAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="93ace-137">Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes</span></span>

## <span data-ttu-id="93ace-138">輸出</span><span class="sxs-lookup"><span data-stu-id="93ace-138">OUTPUTS</span></span>

### <span data-ttu-id="93ace-139">PSNetworkRuleSetAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="93ace-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="93ace-140">筆記</span><span class="sxs-lookup"><span data-stu-id="93ace-140">NOTES</span></span>

## <span data-ttu-id="93ace-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="93ace-141">RELATED LINKS</span></span>
