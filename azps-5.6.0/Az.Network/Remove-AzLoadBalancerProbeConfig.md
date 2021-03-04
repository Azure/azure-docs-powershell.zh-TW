---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2B15B224-E36C-454B-B6C2-F2BE032AE962
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 3e7433c8c779c078ab1b264e6b724d06cd884bab
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912670"
---
# <span data-ttu-id="09690-101">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="09690-101">Remove-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="09690-102">簡介</span><span class="sxs-lookup"><span data-stu-id="09690-102">SYNOPSIS</span></span>
<span data-ttu-id="09690-103">移除負載平衡器上的安裝配置。</span><span class="sxs-lookup"><span data-stu-id="09690-103">Removes a probe configuration from a load balancer.</span></span>

## <span data-ttu-id="09690-104">語法</span><span class="sxs-lookup"><span data-stu-id="09690-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09690-105">描述</span><span class="sxs-lookup"><span data-stu-id="09690-105">DESCRIPTION</span></span>
<span data-ttu-id="09690-106">**Remove-AzLoadBalancerProbeConfig** Cmdlet 會從負載平衡器移除配置。</span><span class="sxs-lookup"><span data-stu-id="09690-106">The **Remove-AzLoadBalancerProbeConfig** cmdlet removes a probe configuration from a load balancer.</span></span>

## <span data-ttu-id="09690-107">例子</span><span class="sxs-lookup"><span data-stu-id="09690-107">EXAMPLES</span></span>

### <span data-ttu-id="09690-108">範例 1：從負載平衡器移除部署組式</span><span class="sxs-lookup"><span data-stu-id="09690-108">Example 1: Remove a probe configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $loadbalancer
```

<span data-ttu-id="09690-109">第一個命令會取得名為 MyLoadBalancer 的負載平衡器，然後將它儲存在$loadbalancer變數中。</span><span class="sxs-lookup"><span data-stu-id="09690-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="09690-110">第二個命令會從 $loadbalancer 中的負載平衡器中刪除名為 MyProbe 的$loadbalancer。</span><span class="sxs-lookup"><span data-stu-id="09690-110">The second command deletes the configuration named MyProbe from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="09690-111">參數</span><span class="sxs-lookup"><span data-stu-id="09690-111">PARAMETERS</span></span>

### <span data-ttu-id="09690-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09690-112">-DefaultProfile</span></span>
<span data-ttu-id="09690-113">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="09690-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09690-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="09690-114">-LoadBalancer</span></span>
<span data-ttu-id="09690-115">指定包含此 Cmdlet 移除之安裝配置的負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="09690-115">Specifies the load balancer that contains the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="09690-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="09690-116">-Name</span></span>
<span data-ttu-id="09690-117">指定此 Cmdlet 移除的群組原則組名。</span><span class="sxs-lookup"><span data-stu-id="09690-117">Specifies the name of the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="09690-118">-確認</span><span class="sxs-lookup"><span data-stu-id="09690-118">-Confirm</span></span>
<span data-ttu-id="09690-119">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="09690-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09690-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09690-120">-WhatIf</span></span>
<span data-ttu-id="09690-121">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="09690-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="09690-122">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="09690-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09690-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09690-123">CommonParameters</span></span>
<span data-ttu-id="09690-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="09690-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09690-125">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="09690-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09690-126">輸入</span><span class="sxs-lookup"><span data-stu-id="09690-126">INPUTS</span></span>

### <span data-ttu-id="09690-127">Microsoft.Azure.Commands.Network.models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="09690-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="09690-128">輸出</span><span class="sxs-lookup"><span data-stu-id="09690-128">OUTPUTS</span></span>

### <span data-ttu-id="09690-129">Microsoft.Azure.Commands.Network.models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="09690-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="09690-130">筆記</span><span class="sxs-lookup"><span data-stu-id="09690-130">NOTES</span></span>

## <span data-ttu-id="09690-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="09690-131">RELATED LINKS</span></span>

[<span data-ttu-id="09690-132">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="09690-132">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="09690-133">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="09690-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="09690-134">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="09690-134">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="09690-135">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="09690-135">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="09690-136">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="09690-136">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


