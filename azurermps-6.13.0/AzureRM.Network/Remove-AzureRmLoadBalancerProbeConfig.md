---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2B15B224-E36C-454B-B6C2-F2BE032AE962
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerProbeConfig.md
ms.openlocfilehash: c52546ba0477a2911ac34533060d7a47df0b0698
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446931"
---
# <span data-ttu-id="a0daa-101">Remove-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a0daa-101">Remove-AzureRmLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="a0daa-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a0daa-102">SYNOPSIS</span></span>
<span data-ttu-id="a0daa-103">從負載平衡器移除探測器配置。</span><span class="sxs-lookup"><span data-stu-id="a0daa-103">Removes a probe configuration from a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0daa-104">句法</span><span class="sxs-lookup"><span data-stu-id="a0daa-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0daa-105">說明</span><span class="sxs-lookup"><span data-stu-id="a0daa-105">DESCRIPTION</span></span>
<span data-ttu-id="a0daa-106">**AzureRmLoadBalancerProbeConfig** Cmdlet 會從負載平衡器移除探測器配置。</span><span class="sxs-lookup"><span data-stu-id="a0daa-106">The **Remove-AzureRmLoadBalancerProbeConfig** cmdlet removes a probe configuration from a load balancer.</span></span>

## <span data-ttu-id="a0daa-107">示例</span><span class="sxs-lookup"><span data-stu-id="a0daa-107">EXAMPLES</span></span>

### <span data-ttu-id="a0daa-108">範例1：從負載平衡器移除探測器配置</span><span class="sxs-lookup"><span data-stu-id="a0daa-108">Example 1: Remove a probe configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzureRmLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $loadbalancer
```

<span data-ttu-id="a0daa-109">第一個命令會取得名為 MyLoadBalancer 的負載平衡器，然後將它儲存在 $loadbalancer 變數中。</span><span class="sxs-lookup"><span data-stu-id="a0daa-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="a0daa-110">第二個命令會從 $loadbalancer 中的負載平衡器刪除名為 MyProbe 的配置。</span><span class="sxs-lookup"><span data-stu-id="a0daa-110">The second command deletes the configuration named MyProbe from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="a0daa-111">參數</span><span class="sxs-lookup"><span data-stu-id="a0daa-111">PARAMETERS</span></span>

### <span data-ttu-id="a0daa-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0daa-112">-DefaultProfile</span></span>
<span data-ttu-id="a0daa-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a0daa-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a0daa-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a0daa-114">-LoadBalancer</span></span>
<span data-ttu-id="a0daa-115">指定包含此 Cmdlet 移除之探測配置的負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="a0daa-115">Specifies the load balancer that contains the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a0daa-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="a0daa-116">-Name</span></span>
<span data-ttu-id="a0daa-117">指定此 Cmdlet 移除之探測設定的名稱。</span><span class="sxs-lookup"><span data-stu-id="a0daa-117">Specifies the name of the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a0daa-118">-確認</span><span class="sxs-lookup"><span data-stu-id="a0daa-118">-Confirm</span></span>
<span data-ttu-id="a0daa-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a0daa-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0daa-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0daa-120">-WhatIf</span></span>
<span data-ttu-id="a0daa-121">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a0daa-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a0daa-122">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a0daa-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0daa-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0daa-123">CommonParameters</span></span>
<span data-ttu-id="a0daa-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a0daa-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0daa-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a0daa-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0daa-126">輸入</span><span class="sxs-lookup"><span data-stu-id="a0daa-126">INPUTS</span></span>

### <span data-ttu-id="a0daa-127">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a0daa-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="a0daa-128">參數： LoadBalancer (ByValue) </span><span class="sxs-lookup"><span data-stu-id="a0daa-128">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="a0daa-129">輸出</span><span class="sxs-lookup"><span data-stu-id="a0daa-129">OUTPUTS</span></span>

### <span data-ttu-id="a0daa-130">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a0daa-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="a0daa-131">筆記</span><span class="sxs-lookup"><span data-stu-id="a0daa-131">NOTES</span></span>

## <span data-ttu-id="a0daa-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="a0daa-132">RELATED LINKS</span></span>

[<span data-ttu-id="a0daa-133">附加 AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a0daa-133">Add-AzureRmLoadBalancerProbeConfig</span></span>](./Add-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="a0daa-134">AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a0daa-134">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="a0daa-135">AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a0daa-135">Get-AzureRmLoadBalancerProbeConfig</span></span>](./Get-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="a0daa-136">新-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a0daa-136">New-AzureRmLoadBalancerProbeConfig</span></span>](./New-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="a0daa-137">Set-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a0daa-137">Set-AzureRmLoadBalancerProbeConfig</span></span>](./Set-AzureRmLoadBalancerProbeConfig.md)


