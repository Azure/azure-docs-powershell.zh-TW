---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1FDA90C0-D01F-45E1-9149-16AD04046271
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 9304471b12f33d677f493a3ee6803a1219d9f977
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93959276"
---
# <span data-ttu-id="8d30d-101">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8d30d-101">Get-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="8d30d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8d30d-102">SYNOPSIS</span></span>
<span data-ttu-id="8d30d-103">取得負載平衡器的入站 NAT 規則配置。</span><span class="sxs-lookup"><span data-stu-id="8d30d-103">Gets an inbound NAT rule configuration for a load balancer.</span></span>

## <span data-ttu-id="8d30d-104">句法</span><span class="sxs-lookup"><span data-stu-id="8d30d-104">SYNTAX</span></span>

```
Get-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d30d-105">說明</span><span class="sxs-lookup"><span data-stu-id="8d30d-105">DESCRIPTION</span></span>
<span data-ttu-id="8d30d-106">**AzLoadBalancerInboundNatRuleConfig** Cmdlet 會在 Azure 負載平衡器中取得一或多個入站網路位址轉譯 (NAT) 規則。</span><span class="sxs-lookup"><span data-stu-id="8d30d-106">The **Get-AzLoadBalancerInboundNatRuleConfig** cmdlet gets one or more inbound network address translation (NAT) rules in an Azure load balancer.</span></span>

## <span data-ttu-id="8d30d-107">示例</span><span class="sxs-lookup"><span data-stu-id="8d30d-107">EXAMPLES</span></span>

### <span data-ttu-id="8d30d-108">範例1：取得入站 NAT 規則設定</span><span class="sxs-lookup"><span data-stu-id="8d30d-108">Example 1: Get an inbound NAT rule configuration</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerInboundNatRuleConfig -Name "MyInboundNatRule1" -LoadBalancer $slb
```

<span data-ttu-id="8d30d-109">第一個命令會取得名為 MyLoadBalancer 的負載平衡器，並將它儲存在 $slb 的變數中。</span><span class="sxs-lookup"><span data-stu-id="8d30d-109">The first command gets the load balancer named MyLoadBalancer, and stores it in the variable $slb.</span></span>
<span data-ttu-id="8d30d-110">第二個命令會從 $slb 中的負載平衡器取得關聯的 NAT 規則（名為 MyInboundNatRule1）。</span><span class="sxs-lookup"><span data-stu-id="8d30d-110">The second command gets the associated NAT rule named MyInboundNatRule1 from the load balancer in $slb.</span></span>

## <span data-ttu-id="8d30d-111">參數</span><span class="sxs-lookup"><span data-stu-id="8d30d-111">PARAMETERS</span></span>

### <span data-ttu-id="8d30d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d30d-112">-DefaultProfile</span></span>
<span data-ttu-id="8d30d-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8d30d-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d30d-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8d30d-114">-LoadBalancer</span></span>
<span data-ttu-id="8d30d-115">指定與要取得的輸入 NAT 規則配置相關聯的負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="8d30d-115">Specifies the load balancer that is associated with the inbound NAT rule configuration to get.</span></span>

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

### <span data-ttu-id="8d30d-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="8d30d-116">-Name</span></span>
<span data-ttu-id="8d30d-117">指定要取得的輸入 NAT 規則配置名稱。</span><span class="sxs-lookup"><span data-stu-id="8d30d-117">Specifies the name of the inbound NAT rule configuration to get.</span></span>

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

### <span data-ttu-id="8d30d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d30d-118">CommonParameters</span></span>
<span data-ttu-id="8d30d-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8d30d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d30d-120">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8d30d-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d30d-121">輸入</span><span class="sxs-lookup"><span data-stu-id="8d30d-121">INPUTS</span></span>

### <span data-ttu-id="8d30d-122">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="8d30d-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="8d30d-123">輸出</span><span class="sxs-lookup"><span data-stu-id="8d30d-123">OUTPUTS</span></span>

### <span data-ttu-id="8d30d-124">PSInboundNatRule 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="8d30d-124">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span></span>

## <span data-ttu-id="8d30d-125">筆記</span><span class="sxs-lookup"><span data-stu-id="8d30d-125">NOTES</span></span>

## <span data-ttu-id="8d30d-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="8d30d-126">RELATED LINKS</span></span>

[<span data-ttu-id="8d30d-127">AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8d30d-127">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="8d30d-128">新-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8d30d-128">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="8d30d-129">移除-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8d30d-129">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="8d30d-130">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8d30d-130">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


