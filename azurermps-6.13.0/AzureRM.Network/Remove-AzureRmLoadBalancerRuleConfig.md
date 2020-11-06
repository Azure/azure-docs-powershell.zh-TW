---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DEBD58A3-AFAF-485C-8708-53228625138F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerRuleConfig.md
ms.openlocfilehash: b51c7300296644ffeda75d1fb9e4cf695ff61def
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446929"
---
# <span data-ttu-id="1f85b-101">Remove-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1f85b-101">Remove-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="1f85b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1f85b-102">SYNOPSIS</span></span>
<span data-ttu-id="1f85b-103">移除負載平衡器的規則配置。</span><span class="sxs-lookup"><span data-stu-id="1f85b-103">Removes a rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f85b-104">句法</span><span class="sxs-lookup"><span data-stu-id="1f85b-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f85b-105">說明</span><span class="sxs-lookup"><span data-stu-id="1f85b-105">DESCRIPTION</span></span>
<span data-ttu-id="1f85b-106">**AzureRmLoadBalancerRuleConfig** Cmdlet 會移除 Azure 負載平衡器的規則配置。</span><span class="sxs-lookup"><span data-stu-id="1f85b-106">The **Remove-AzureRmLoadBalancerRuleConfig** cmdlet removes a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="1f85b-107">示例</span><span class="sxs-lookup"><span data-stu-id="1f85b-107">EXAMPLES</span></span>

### <span data-ttu-id="1f85b-108">範例1：從負載平衡器移除規則配置</span><span class="sxs-lookup"><span data-stu-id="1f85b-108">Example 1: Remove a rule configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzureRmLoadBalancerRuleConfig -Name "MyLBruleName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="1f85b-109">第一個命令會取得名為 MyLoadBalancer 的負載平衡器，然後將它儲存在 $loadbalancer 變數中。</span><span class="sxs-lookup"><span data-stu-id="1f85b-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="1f85b-110">第二個命令會從 $loadbalancer 中的負載平衡器移除名為 MyLBruleName 的規則配置。</span><span class="sxs-lookup"><span data-stu-id="1f85b-110">The second command removes the rule configuration named MyLBruleName from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="1f85b-111">參數</span><span class="sxs-lookup"><span data-stu-id="1f85b-111">PARAMETERS</span></span>

### <span data-ttu-id="1f85b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f85b-112">-DefaultProfile</span></span>
<span data-ttu-id="1f85b-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1f85b-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f85b-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1f85b-114">-LoadBalancer</span></span>
<span data-ttu-id="1f85b-115">指定包含此 Cmdlet 移除之規則配置的 **LoadBalancer** 物件。</span><span class="sxs-lookup"><span data-stu-id="1f85b-115">Specifies the **LoadBalancer** object that contains the rule configuration that this cmdlet removes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1f85b-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="1f85b-116">-Name</span></span>
<span data-ttu-id="1f85b-117">指定此 Cmdlet 移除的負載等化器規則配置名稱。</span><span class="sxs-lookup"><span data-stu-id="1f85b-117">Specifies the name of the load balancer rule configuration that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f85b-118">-確認</span><span class="sxs-lookup"><span data-stu-id="1f85b-118">-Confirm</span></span>
<span data-ttu-id="1f85b-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1f85b-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f85b-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f85b-120">-WhatIf</span></span>
<span data-ttu-id="1f85b-121">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1f85b-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1f85b-122">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1f85b-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f85b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f85b-123">CommonParameters</span></span>
<span data-ttu-id="1f85b-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1f85b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f85b-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1f85b-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f85b-126">輸入</span><span class="sxs-lookup"><span data-stu-id="1f85b-126">INPUTS</span></span>

### <span data-ttu-id="1f85b-127">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="1f85b-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="1f85b-128">參數： LoadBalancer (ByValue) </span><span class="sxs-lookup"><span data-stu-id="1f85b-128">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="1f85b-129">輸出</span><span class="sxs-lookup"><span data-stu-id="1f85b-129">OUTPUTS</span></span>

### <span data-ttu-id="1f85b-130">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="1f85b-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="1f85b-131">筆記</span><span class="sxs-lookup"><span data-stu-id="1f85b-131">NOTES</span></span>

## <span data-ttu-id="1f85b-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="1f85b-132">RELATED LINKS</span></span>

[<span data-ttu-id="1f85b-133">附加 AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1f85b-133">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="1f85b-134">AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1f85b-134">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="1f85b-135">AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1f85b-135">Get-AzureRmLoadBalancerRuleConfig</span></span>](./Get-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="1f85b-136">新-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1f85b-136">New-AzureRmLoadBalancerRuleConfig</span></span>](./New-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="1f85b-137">Set-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1f85b-137">Set-AzureRmLoadBalancerRuleConfig</span></span>](./Set-AzureRmLoadBalancerRuleConfig.md)


