---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D818C404-60E4-42DB-AADF-063305D9541B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: d76803df11ff3f89e20ca7d849577ca51331416c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450229"
---
# <span data-ttu-id="c3bde-101">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c3bde-101">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="c3bde-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c3bde-102">SYNOPSIS</span></span>
<span data-ttu-id="c3bde-103">從負載平衡器移除入站 NAT 規則配置。</span><span class="sxs-lookup"><span data-stu-id="c3bde-103">Removes an inbound NAT rule configuration from a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3bde-104">句法</span><span class="sxs-lookup"><span data-stu-id="c3bde-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3bde-105">說明</span><span class="sxs-lookup"><span data-stu-id="c3bde-105">DESCRIPTION</span></span>
<span data-ttu-id="c3bde-106">**AzureRmLoadBalancerInboundNatRuleConfig** Cmdlet 會從 Azure 負載平衡器移除入站網路位址轉譯 (NAT) 規則配置。</span><span class="sxs-lookup"><span data-stu-id="c3bde-106">The **Remove-AzureRmLoadBalancerInboundNatRuleConfig** cmdlet removes an inbound network address translation (NAT) rule configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="c3bde-107">示例</span><span class="sxs-lookup"><span data-stu-id="c3bde-107">EXAMPLES</span></span>

### <span data-ttu-id="c3bde-108">1：從 Azure 負載平衡器刪除入站 NAT 規則</span><span class="sxs-lookup"><span data-stu-id="c3bde-108">1: Delete an inbound NAT rule from an Azure load balancer</span></span>
```
$loadbalancer = Get-AzureRmLoadBalancer -Name mylb -ResourceGroupName myrg

 Remove-AzureRmLoadBalancerInboundNatRuleConfig -Name "myinboundnatrule" -LoadBalancer $loadbalancer
```

<span data-ttu-id="c3bde-109">第一個命令會載入一個名為 "mylb" 的現有負載等化器，並將它儲存在 $load 平衡器的變數中。</span><span class="sxs-lookup"><span data-stu-id="c3bde-109">The first command loads an already existing load balancer called "mylb" and stores it in the variable $load balancer.</span></span> <span data-ttu-id="c3bde-110">第二個命令會移除與此負載平衡器相關聯的輸入 NAT 規則。</span><span class="sxs-lookup"><span data-stu-id="c3bde-110">The second command removes the inbound NAT rule associated with this load balancer.</span></span>

## <span data-ttu-id="c3bde-111">參數</span><span class="sxs-lookup"><span data-stu-id="c3bde-111">PARAMETERS</span></span>

### <span data-ttu-id="c3bde-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3bde-112">-DefaultProfile</span></span>
<span data-ttu-id="c3bde-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c3bde-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3bde-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c3bde-114">-LoadBalancer</span></span>
<span data-ttu-id="c3bde-115">指定包含此 Cmdlet 移除之入站 NAT 規則配置的 **LoadBalancer** 物件。</span><span class="sxs-lookup"><span data-stu-id="c3bde-115">Specifies the **LoadBalancer** object that contains the inbound NAT rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c3bde-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="c3bde-116">-Name</span></span>
<span data-ttu-id="c3bde-117">指定此 Cmdlet 移除的輸入 NAT 規則配置名稱。</span><span class="sxs-lookup"><span data-stu-id="c3bde-117">Specifies the name of the inbound NAT rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c3bde-118">-確認</span><span class="sxs-lookup"><span data-stu-id="c3bde-118">-Confirm</span></span>
<span data-ttu-id="c3bde-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c3bde-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3bde-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3bde-120">-WhatIf</span></span>
<span data-ttu-id="c3bde-121">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c3bde-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c3bde-122">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c3bde-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3bde-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3bde-123">CommonParameters</span></span>
<span data-ttu-id="c3bde-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c3bde-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3bde-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c3bde-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3bde-126">輸入</span><span class="sxs-lookup"><span data-stu-id="c3bde-126">INPUTS</span></span>

### <span data-ttu-id="c3bde-127">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c3bde-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="c3bde-128">參數： LoadBalancer (ByValue) </span><span class="sxs-lookup"><span data-stu-id="c3bde-128">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="c3bde-129">輸出</span><span class="sxs-lookup"><span data-stu-id="c3bde-129">OUTPUTS</span></span>

### <span data-ttu-id="c3bde-130">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c3bde-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="c3bde-131">筆記</span><span class="sxs-lookup"><span data-stu-id="c3bde-131">NOTES</span></span>

## <span data-ttu-id="c3bde-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="c3bde-132">RELATED LINKS</span></span>

[<span data-ttu-id="c3bde-133">附加 AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c3bde-133">Add-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="c3bde-134">AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c3bde-134">Get-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="c3bde-135">新-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c3bde-135">New-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./New-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="c3bde-136">Set-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c3bde-136">Set-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzureRmLoadBalancerInboundNatRuleConfig.md)


