---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 614B0634-154A-449A-83E7-051DEF5A3BEE
online version: https://docs.microsoft.com/powershell/module/az.network/get-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 74815c263435860f9281f476babc80574b63b161
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903581"
---
# <span data-ttu-id="5bc01-101">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="5bc01-101">Get-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="5bc01-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5bc01-102">SYNOPSIS</span></span>
<span data-ttu-id="5bc01-103">從負載平衡器取得一或多個進入 NAT 區組。</span><span class="sxs-lookup"><span data-stu-id="5bc01-103">Gets one or more inbound NAT pool configurations from a load balancer.</span></span>

## <span data-ttu-id="5bc01-104">語法</span><span class="sxs-lookup"><span data-stu-id="5bc01-104">SYNTAX</span></span>

```
Get-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5bc01-105">描述</span><span class="sxs-lookup"><span data-stu-id="5bc01-105">DESCRIPTION</span></span>
<span data-ttu-id="5bc01-106">**Get-AzLoadBalancerInboundNatPoolConfig** Cmdlet 會從負載平衡器取得一或多個內建 NAT 集區組組。</span><span class="sxs-lookup"><span data-stu-id="5bc01-106">The **Get-AzLoadBalancerInboundNatPoolConfig** cmdlet gets one or more inbound NAT pool configurations from a load balancer.</span></span>

## <span data-ttu-id="5bc01-107">例子</span><span class="sxs-lookup"><span data-stu-id="5bc01-107">EXAMPLES</span></span>

### <span data-ttu-id="5bc01-108">1：取得</span><span class="sxs-lookup"><span data-stu-id="5bc01-108">1: Get</span></span>
```
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Get-AzLoadBalancerInboundNatPoolConfig -Name myInboundNatPool
```

## <span data-ttu-id="5bc01-109">參數</span><span class="sxs-lookup"><span data-stu-id="5bc01-109">PARAMETERS</span></span>

### <span data-ttu-id="5bc01-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bc01-110">-DefaultProfile</span></span>
<span data-ttu-id="5bc01-111">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5bc01-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5bc01-112">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5bc01-112">-LoadBalancer</span></span>
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

### <span data-ttu-id="5bc01-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="5bc01-113">-Name</span></span>
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

### <span data-ttu-id="5bc01-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bc01-114">CommonParameters</span></span>
<span data-ttu-id="5bc01-115">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5bc01-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bc01-116">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5bc01-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bc01-117">輸入</span><span class="sxs-lookup"><span data-stu-id="5bc01-117">INPUTS</span></span>

### <span data-ttu-id="5bc01-118">Microsoft.Azure.Commands.Network.models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5bc01-118">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="5bc01-119">輸出</span><span class="sxs-lookup"><span data-stu-id="5bc01-119">OUTPUTS</span></span>

### <span data-ttu-id="5bc01-120">Microsoft.Azure.Commands.Network.models.PSInboundNatPool</span><span class="sxs-lookup"><span data-stu-id="5bc01-120">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="5bc01-121">筆記</span><span class="sxs-lookup"><span data-stu-id="5bc01-121">NOTES</span></span>

## <span data-ttu-id="5bc01-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="5bc01-122">RELATED LINKS</span></span>

[<span data-ttu-id="5bc01-123">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="5bc01-123">Add-AzLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="5bc01-124">New-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="5bc01-124">New-AzLoadBalancerInboundNatPoolConfig</span></span>](./New-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="5bc01-125">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="5bc01-125">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>](./Remove-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="5bc01-126">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="5bc01-126">Set-AzLoadBalancerInboundNatPoolConfig</span></span>](./Set-AzLoadBalancerInboundNatPoolConfig.md)
