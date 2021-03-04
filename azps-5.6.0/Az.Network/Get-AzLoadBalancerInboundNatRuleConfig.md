---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1FDA90C0-D01F-45E1-9149-16AD04046271
online version: https://docs.microsoft.com/powershell/module/az.network/get-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 816c94281c246762dac41f2e69e080dfec70565d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902562"
---
# <span data-ttu-id="e1ec7-101">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e1ec7-101">Get-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="e1ec7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e1ec7-102">SYNOPSIS</span></span>
<span data-ttu-id="e1ec7-103">取得負載平衡器內入 NAT 規則組。</span><span class="sxs-lookup"><span data-stu-id="e1ec7-103">Gets an inbound NAT rule configuration for a load balancer.</span></span>

## <span data-ttu-id="e1ec7-104">語法</span><span class="sxs-lookup"><span data-stu-id="e1ec7-104">SYNTAX</span></span>

```
Get-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1ec7-105">描述</span><span class="sxs-lookup"><span data-stu-id="e1ec7-105">DESCRIPTION</span></span>
<span data-ttu-id="e1ec7-106">**Get-AzLoadBalancerInboundNatRuleConfig** Cmdlet 在 Azure 負載平衡器中取得一或多個輸入網路位址轉譯 (NAT) 規則。</span><span class="sxs-lookup"><span data-stu-id="e1ec7-106">The **Get-AzLoadBalancerInboundNatRuleConfig** cmdlet gets one or more inbound network address translation (NAT) rules in an Azure load balancer.</span></span>

## <span data-ttu-id="e1ec7-107">例子</span><span class="sxs-lookup"><span data-stu-id="e1ec7-107">EXAMPLES</span></span>

### <span data-ttu-id="e1ec7-108">範例 1：取得內入 NAT 規則組</span><span class="sxs-lookup"><span data-stu-id="e1ec7-108">Example 1: Get an inbound NAT rule configuration</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerInboundNatRuleConfig -Name "MyInboundNatRule1" -LoadBalancer $slb
```

<span data-ttu-id="e1ec7-109">第一個命令會取得名為 MyLoadBalancer 的負載平衡器，並儲存在變數 $slb。</span><span class="sxs-lookup"><span data-stu-id="e1ec7-109">The first command gets the load balancer named MyLoadBalancer, and stores it in the variable $slb.</span></span>
<span data-ttu-id="e1ec7-110">第二個命令會從 $slb 中的負載平衡器取得名為 MyInboundNatRule1 的關聯 NAT 規則。</span><span class="sxs-lookup"><span data-stu-id="e1ec7-110">The second command gets the associated NAT rule named MyInboundNatRule1 from the load balancer in $slb.</span></span>

## <span data-ttu-id="e1ec7-111">參數</span><span class="sxs-lookup"><span data-stu-id="e1ec7-111">PARAMETERS</span></span>

### <span data-ttu-id="e1ec7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1ec7-112">-DefaultProfile</span></span>
<span data-ttu-id="e1ec7-113">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e1ec7-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1ec7-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e1ec7-114">-LoadBalancer</span></span>
<span data-ttu-id="e1ec7-115">指定要取得與內入 NAT 規則組組關聯的負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="e1ec7-115">Specifies the load balancer that is associated with the inbound NAT rule configuration to get.</span></span>

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

### <span data-ttu-id="e1ec7-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="e1ec7-116">-Name</span></span>
<span data-ttu-id="e1ec7-117">指定要取得之輸入 NAT 規則組組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e1ec7-117">Specifies the name of the inbound NAT rule configuration to get.</span></span>

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

### <span data-ttu-id="e1ec7-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1ec7-118">CommonParameters</span></span>
<span data-ttu-id="e1ec7-119">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e1ec7-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1ec7-120">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e1ec7-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1ec7-121">輸入</span><span class="sxs-lookup"><span data-stu-id="e1ec7-121">INPUTS</span></span>

### <span data-ttu-id="e1ec7-122">Microsoft.Azure.Commands.Network.models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e1ec7-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="e1ec7-123">輸出</span><span class="sxs-lookup"><span data-stu-id="e1ec7-123">OUTPUTS</span></span>

### <span data-ttu-id="e1ec7-124">Microsoft.Azure.Commands.Network.models.PSInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="e1ec7-124">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span></span>

## <span data-ttu-id="e1ec7-125">筆記</span><span class="sxs-lookup"><span data-stu-id="e1ec7-125">NOTES</span></span>

## <span data-ttu-id="e1ec7-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="e1ec7-126">RELATED LINKS</span></span>

[<span data-ttu-id="e1ec7-127">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e1ec7-127">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="e1ec7-128">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e1ec7-128">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="e1ec7-129">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e1ec7-129">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="e1ec7-130">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e1ec7-130">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


