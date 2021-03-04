---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 98D2EB70-440F-45C4-A79A-EB87BBDC6256
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 9e266ad824d5637137649c73d4e3b427af2f176b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913421"
---
# <span data-ttu-id="51631-101">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="51631-101">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="51631-102">簡介</span><span class="sxs-lookup"><span data-stu-id="51631-102">SYNOPSIS</span></span>
<span data-ttu-id="51631-103">從負載平衡器移除內入 NAT 區組組組。</span><span class="sxs-lookup"><span data-stu-id="51631-103">Removes an inbound NAT pool configuration from a load balancer.</span></span>

## <span data-ttu-id="51631-104">語法</span><span class="sxs-lookup"><span data-stu-id="51631-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51631-105">描述</span><span class="sxs-lookup"><span data-stu-id="51631-105">DESCRIPTION</span></span>
<span data-ttu-id="51631-106">**Remove-AzLoadBalancerInboundNatPoolConfig** Cmdlet 會從負載平衡器移除內建 NAT 集區組組。</span><span class="sxs-lookup"><span data-stu-id="51631-106">The **Remove-AzLoadBalancerInboundNatPoolConfig** cmdlet removes an inbound NAT pool configuration from a load balancer.</span></span>

## <span data-ttu-id="51631-107">例子</span><span class="sxs-lookup"><span data-stu-id="51631-107">EXAMPLES</span></span>

### <span data-ttu-id="51631-108">1：移除</span><span class="sxs-lookup"><span data-stu-id="51631-108">1: Remove</span></span>
```
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzLoadBalancerInboundNatPoolConfig -Name myinboundnatpool -LoadBalancer $slb
```

## <span data-ttu-id="51631-109">參數</span><span class="sxs-lookup"><span data-stu-id="51631-109">PARAMETERS</span></span>

### <span data-ttu-id="51631-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51631-110">-DefaultProfile</span></span>
<span data-ttu-id="51631-111">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="51631-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="51631-112">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="51631-112">-LoadBalancer</span></span>
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

### <span data-ttu-id="51631-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="51631-113">-Name</span></span>
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

### <span data-ttu-id="51631-114">-確認</span><span class="sxs-lookup"><span data-stu-id="51631-114">-Confirm</span></span>
<span data-ttu-id="51631-115">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="51631-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51631-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51631-116">-WhatIf</span></span>
<span data-ttu-id="51631-117">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="51631-117">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="51631-118">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="51631-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51631-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51631-119">CommonParameters</span></span>
<span data-ttu-id="51631-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="51631-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51631-121">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="51631-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51631-122">輸入</span><span class="sxs-lookup"><span data-stu-id="51631-122">INPUTS</span></span>

### <span data-ttu-id="51631-123">Microsoft.Azure.Commands.Network.models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="51631-123">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="51631-124">輸出</span><span class="sxs-lookup"><span data-stu-id="51631-124">OUTPUTS</span></span>

### <span data-ttu-id="51631-125">Microsoft.Azure.Commands.Network.models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="51631-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="51631-126">筆記</span><span class="sxs-lookup"><span data-stu-id="51631-126">NOTES</span></span>

## <span data-ttu-id="51631-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="51631-127">RELATED LINKS</span></span>

[<span data-ttu-id="51631-128">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="51631-128">Add-AzLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="51631-129">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="51631-129">Get-AzLoadBalancerInboundNatPoolConfig</span></span>](./Get-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="51631-130">New-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="51631-130">New-AzLoadBalancerInboundNatPoolConfig</span></span>](./New-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="51631-131">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="51631-131">Set-AzLoadBalancerInboundNatPoolConfig</span></span>](./Set-AzLoadBalancerInboundNatPoolConfig.md)
