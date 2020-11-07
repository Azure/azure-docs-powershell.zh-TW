---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 614B0634-154A-449A-83E7-051DEF5A3BEE
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: da7004c8737bf454ea8847b529f003f5b1909f9f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93789590"
---
# <span data-ttu-id="9d15a-101">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="9d15a-101">Get-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="9d15a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9d15a-102">SYNOPSIS</span></span>
<span data-ttu-id="9d15a-103">從負載平衡器取得一或多個入站 NAT 池配置。</span><span class="sxs-lookup"><span data-stu-id="9d15a-103">Gets one or more inbound NAT pool configurations from a load balancer.</span></span>

## <span data-ttu-id="9d15a-104">句法</span><span class="sxs-lookup"><span data-stu-id="9d15a-104">SYNTAX</span></span>

```
Get-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9d15a-105">說明</span><span class="sxs-lookup"><span data-stu-id="9d15a-105">DESCRIPTION</span></span>
<span data-ttu-id="9d15a-106">**AzLoadBalancerInboundNatPoolConfig** Cmdlet 會從負載平衡器取得一或多個入站 NAT 池配置。</span><span class="sxs-lookup"><span data-stu-id="9d15a-106">The **Get-AzLoadBalancerInboundNatPoolConfig** cmdlet gets one or more inbound NAT pool configurations from a load balancer.</span></span>

## <span data-ttu-id="9d15a-107">示例</span><span class="sxs-lookup"><span data-stu-id="9d15a-107">EXAMPLES</span></span>

### <span data-ttu-id="9d15a-108">1：取得</span><span class="sxs-lookup"><span data-stu-id="9d15a-108">1: Get</span></span>
```
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Get-AzLoadBalancerInboundNatPoolConfig -Name myInboundNatPool
```

## <span data-ttu-id="9d15a-109">參數</span><span class="sxs-lookup"><span data-stu-id="9d15a-109">PARAMETERS</span></span>

### <span data-ttu-id="9d15a-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d15a-110">-DefaultProfile</span></span>
<span data-ttu-id="9d15a-111">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9d15a-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d15a-112">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9d15a-112">-LoadBalancer</span></span>
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

### <span data-ttu-id="9d15a-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="9d15a-113">-Name</span></span>
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

### <span data-ttu-id="9d15a-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d15a-114">CommonParameters</span></span>
<span data-ttu-id="9d15a-115">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9d15a-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d15a-116">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9d15a-116">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d15a-117">輸入</span><span class="sxs-lookup"><span data-stu-id="9d15a-117">INPUTS</span></span>

### <span data-ttu-id="9d15a-118">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="9d15a-118">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="9d15a-119">輸出</span><span class="sxs-lookup"><span data-stu-id="9d15a-119">OUTPUTS</span></span>

### <span data-ttu-id="9d15a-120">PSInboundNatPool 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="9d15a-120">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="9d15a-121">筆記</span><span class="sxs-lookup"><span data-stu-id="9d15a-121">NOTES</span></span>

## <span data-ttu-id="9d15a-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="9d15a-122">RELATED LINKS</span></span>

[<span data-ttu-id="9d15a-123">附加 AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="9d15a-123">Add-AzLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="9d15a-124">新-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="9d15a-124">New-AzLoadBalancerInboundNatPoolConfig</span></span>](./New-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="9d15a-125">移除-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="9d15a-125">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>](./Remove-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="9d15a-126">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="9d15a-126">Set-AzLoadBalancerInboundNatPoolConfig</span></span>](./Set-AzLoadBalancerInboundNatPoolConfig.md)
