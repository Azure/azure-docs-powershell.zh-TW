---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 614B0634-154A-449A-83E7-051DEF5A3BEE
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 444db99b21289f3c46c2f73a726e44dad8635d39
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435198"
---
# <span data-ttu-id="da7f6-101">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="da7f6-101">Get-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="da7f6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="da7f6-102">SYNOPSIS</span></span>
<span data-ttu-id="da7f6-103">從負載平衡器取得一或多個入站 NAT 池配置。</span><span class="sxs-lookup"><span data-stu-id="da7f6-103">Gets one or more inbound NAT pool configurations from a load balancer.</span></span>

## <span data-ttu-id="da7f6-104">句法</span><span class="sxs-lookup"><span data-stu-id="da7f6-104">SYNTAX</span></span>

```
Get-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da7f6-105">說明</span><span class="sxs-lookup"><span data-stu-id="da7f6-105">DESCRIPTION</span></span>
<span data-ttu-id="da7f6-106">**AzLoadBalancerInboundNatPoolConfig** Cmdlet 會從負載平衡器取得一或多個入站 NAT 池配置。</span><span class="sxs-lookup"><span data-stu-id="da7f6-106">The **Get-AzLoadBalancerInboundNatPoolConfig** cmdlet gets one or more inbound NAT pool configurations from a load balancer.</span></span>

## <span data-ttu-id="da7f6-107">示例</span><span class="sxs-lookup"><span data-stu-id="da7f6-107">EXAMPLES</span></span>

### <span data-ttu-id="da7f6-108">1：取得</span><span class="sxs-lookup"><span data-stu-id="da7f6-108">1: Get</span></span>
```
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Get-AzLoadBalancerInboundNatPoolConfig -Name myInboundNatPool
```

## <span data-ttu-id="da7f6-109">參數</span><span class="sxs-lookup"><span data-stu-id="da7f6-109">PARAMETERS</span></span>

### <span data-ttu-id="da7f6-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da7f6-110">-DefaultProfile</span></span>
<span data-ttu-id="da7f6-111">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="da7f6-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da7f6-112">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="da7f6-112">-LoadBalancer</span></span>
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

### <span data-ttu-id="da7f6-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="da7f6-113">-Name</span></span>
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

### <span data-ttu-id="da7f6-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da7f6-114">CommonParameters</span></span>
<span data-ttu-id="da7f6-115">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="da7f6-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da7f6-116">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="da7f6-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da7f6-117">輸入</span><span class="sxs-lookup"><span data-stu-id="da7f6-117">INPUTS</span></span>

### <span data-ttu-id="da7f6-118">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="da7f6-118">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="da7f6-119">輸出</span><span class="sxs-lookup"><span data-stu-id="da7f6-119">OUTPUTS</span></span>

### <span data-ttu-id="da7f6-120">PSInboundNatPool 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="da7f6-120">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="da7f6-121">筆記</span><span class="sxs-lookup"><span data-stu-id="da7f6-121">NOTES</span></span>

## <span data-ttu-id="da7f6-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="da7f6-122">RELATED LINKS</span></span>

[<span data-ttu-id="da7f6-123">附加 AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="da7f6-123">Add-AzLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="da7f6-124">新-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="da7f6-124">New-AzLoadBalancerInboundNatPoolConfig</span></span>](./New-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="da7f6-125">移除-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="da7f6-125">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>](./Remove-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="da7f6-126">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="da7f6-126">Set-AzLoadBalancerInboundNatPoolConfig</span></span>](./Set-AzLoadBalancerInboundNatPoolConfig.md)
