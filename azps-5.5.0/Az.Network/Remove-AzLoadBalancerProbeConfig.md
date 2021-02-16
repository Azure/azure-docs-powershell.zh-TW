---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2B15B224-E36C-454B-B6C2-F2BE032AE962
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 341bd8df76870de638db949fb844ac7187776509
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100135758"
---
# <span data-ttu-id="4deb1-101">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="4deb1-101">Remove-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="4deb1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4deb1-102">SYNOPSIS</span></span>
<span data-ttu-id="4deb1-103">從負載平衡器移除探測器配置。</span><span class="sxs-lookup"><span data-stu-id="4deb1-103">Removes a probe configuration from a load balancer.</span></span>

## <span data-ttu-id="4deb1-104">句法</span><span class="sxs-lookup"><span data-stu-id="4deb1-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4deb1-105">說明</span><span class="sxs-lookup"><span data-stu-id="4deb1-105">DESCRIPTION</span></span>
<span data-ttu-id="4deb1-106">**AzLoadBalancerProbeConfig** Cmdlet 會從負載平衡器移除探測器配置。</span><span class="sxs-lookup"><span data-stu-id="4deb1-106">The **Remove-AzLoadBalancerProbeConfig** cmdlet removes a probe configuration from a load balancer.</span></span>

## <span data-ttu-id="4deb1-107">示例</span><span class="sxs-lookup"><span data-stu-id="4deb1-107">EXAMPLES</span></span>

### <span data-ttu-id="4deb1-108">範例1：從負載平衡器移除探測器配置</span><span class="sxs-lookup"><span data-stu-id="4deb1-108">Example 1: Remove a probe configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $loadbalancer
```

<span data-ttu-id="4deb1-109">第一個命令會取得名為 MyLoadBalancer 的負載平衡器，然後將它儲存在 $loadbalancer 變數中。</span><span class="sxs-lookup"><span data-stu-id="4deb1-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="4deb1-110">第二個命令會從 $loadbalancer 中的負載平衡器刪除名為 MyProbe 的配置。</span><span class="sxs-lookup"><span data-stu-id="4deb1-110">The second command deletes the configuration named MyProbe from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="4deb1-111">參數</span><span class="sxs-lookup"><span data-stu-id="4deb1-111">PARAMETERS</span></span>

### <span data-ttu-id="4deb1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4deb1-112">-DefaultProfile</span></span>
<span data-ttu-id="4deb1-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4deb1-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4deb1-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4deb1-114">-LoadBalancer</span></span>
<span data-ttu-id="4deb1-115">指定包含此 Cmdlet 移除之探測配置的負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="4deb1-115">Specifies the load balancer that contains the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="4deb1-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="4deb1-116">-Name</span></span>
<span data-ttu-id="4deb1-117">指定此 Cmdlet 移除之探測設定的名稱。</span><span class="sxs-lookup"><span data-stu-id="4deb1-117">Specifies the name of the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="4deb1-118">-確認</span><span class="sxs-lookup"><span data-stu-id="4deb1-118">-Confirm</span></span>
<span data-ttu-id="4deb1-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4deb1-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4deb1-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4deb1-120">-WhatIf</span></span>
<span data-ttu-id="4deb1-121">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4deb1-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4deb1-122">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4deb1-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4deb1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4deb1-123">CommonParameters</span></span>
<span data-ttu-id="4deb1-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4deb1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4deb1-125">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4deb1-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4deb1-126">輸入</span><span class="sxs-lookup"><span data-stu-id="4deb1-126">INPUTS</span></span>

### <span data-ttu-id="4deb1-127">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4deb1-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="4deb1-128">輸出</span><span class="sxs-lookup"><span data-stu-id="4deb1-128">OUTPUTS</span></span>

### <span data-ttu-id="4deb1-129">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4deb1-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="4deb1-130">筆記</span><span class="sxs-lookup"><span data-stu-id="4deb1-130">NOTES</span></span>

## <span data-ttu-id="4deb1-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="4deb1-131">RELATED LINKS</span></span>

[<span data-ttu-id="4deb1-132">附加 AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="4deb1-132">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="4deb1-133">AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4deb1-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="4deb1-134">AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="4deb1-134">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="4deb1-135">新-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="4deb1-135">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="4deb1-136">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="4deb1-136">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


