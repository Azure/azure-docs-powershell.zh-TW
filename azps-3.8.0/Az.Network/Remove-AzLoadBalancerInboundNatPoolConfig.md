---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 98D2EB70-440F-45C4-A79A-EB87BBDC6256
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: cf8afee04e8aaf1a8909988465dc4371575b4309
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93965481"
---
# <span data-ttu-id="60083-101">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="60083-101">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="60083-102">摘要</span><span class="sxs-lookup"><span data-stu-id="60083-102">SYNOPSIS</span></span>
<span data-ttu-id="60083-103">從負載平衡器移除入站 NAT 池配置。</span><span class="sxs-lookup"><span data-stu-id="60083-103">Removes an inbound NAT pool configuration from a load balancer.</span></span>

## <span data-ttu-id="60083-104">句法</span><span class="sxs-lookup"><span data-stu-id="60083-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60083-105">說明</span><span class="sxs-lookup"><span data-stu-id="60083-105">DESCRIPTION</span></span>
<span data-ttu-id="60083-106">**AzLoadBalancerInboundNatPoolConfig** Cmdlet 會從負載平衡器中移除入站 NAT 池配置。</span><span class="sxs-lookup"><span data-stu-id="60083-106">The **Remove-AzLoadBalancerInboundNatPoolConfig** cmdlet removes an inbound NAT pool configuration from a load balancer.</span></span>

## <span data-ttu-id="60083-107">示例</span><span class="sxs-lookup"><span data-stu-id="60083-107">EXAMPLES</span></span>

### <span data-ttu-id="60083-108">1：移除</span><span class="sxs-lookup"><span data-stu-id="60083-108">1: Remove</span></span>
```
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzLoadBalancerInboundNatPoolConfig -Name myinboundnatpool -LoadBalancer $slb
```

## <span data-ttu-id="60083-109">參數</span><span class="sxs-lookup"><span data-stu-id="60083-109">PARAMETERS</span></span>

### <span data-ttu-id="60083-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60083-110">-DefaultProfile</span></span>
<span data-ttu-id="60083-111">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="60083-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60083-112">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="60083-112">-LoadBalancer</span></span>
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

### <span data-ttu-id="60083-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="60083-113">-Name</span></span>
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

### <span data-ttu-id="60083-114">-確認</span><span class="sxs-lookup"><span data-stu-id="60083-114">-Confirm</span></span>
<span data-ttu-id="60083-115">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="60083-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60083-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60083-116">-WhatIf</span></span>
<span data-ttu-id="60083-117">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="60083-117">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="60083-118">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="60083-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60083-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60083-119">CommonParameters</span></span>
<span data-ttu-id="60083-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="60083-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60083-121">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="60083-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60083-122">輸入</span><span class="sxs-lookup"><span data-stu-id="60083-122">INPUTS</span></span>

### <span data-ttu-id="60083-123">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="60083-123">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="60083-124">輸出</span><span class="sxs-lookup"><span data-stu-id="60083-124">OUTPUTS</span></span>

### <span data-ttu-id="60083-125">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="60083-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="60083-126">筆記</span><span class="sxs-lookup"><span data-stu-id="60083-126">NOTES</span></span>

## <span data-ttu-id="60083-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="60083-127">RELATED LINKS</span></span>

[<span data-ttu-id="60083-128">附加 AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="60083-128">Add-AzLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="60083-129">AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="60083-129">Get-AzLoadBalancerInboundNatPoolConfig</span></span>](./Get-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="60083-130">新-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="60083-130">New-AzLoadBalancerInboundNatPoolConfig</span></span>](./New-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="60083-131">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="60083-131">Set-AzLoadBalancerInboundNatPoolConfig</span></span>](./Set-AzLoadBalancerInboundNatPoolConfig.md)
