---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2B15B224-E36C-454B-B6C2-F2BE032AE962
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerprobeconfig
schema: 2.0.0
ms.openlocfilehash: bed9eebb8812c0bd75eb19c3e8666d6a3b418a13
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93802278"
---
# <span data-ttu-id="e2747-101">Remove-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e2747-101">Remove-AzureRmLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="e2747-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e2747-102">SYNOPSIS</span></span>
<span data-ttu-id="e2747-103">從負載平衡器移除探測器配置。</span><span class="sxs-lookup"><span data-stu-id="e2747-103">Removes a probe configuration from a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2747-104">句法</span><span class="sxs-lookup"><span data-stu-id="e2747-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerProbeConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2747-105">說明</span><span class="sxs-lookup"><span data-stu-id="e2747-105">DESCRIPTION</span></span>
<span data-ttu-id="e2747-106">**AzureRmLoadBalancerProbeConfig** Cmdlet 會從負載平衡器移除探測器配置。</span><span class="sxs-lookup"><span data-stu-id="e2747-106">The **Remove-AzureRmLoadBalancerProbeConfig** cmdlet removes a probe configuration from a load balancer.</span></span>

## <span data-ttu-id="e2747-107">示例</span><span class="sxs-lookup"><span data-stu-id="e2747-107">EXAMPLES</span></span>

### <span data-ttu-id="e2747-108">範例1：從負載平衡器移除探測器配置</span><span class="sxs-lookup"><span data-stu-id="e2747-108">Example 1: Remove a probe configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzureRmLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $loadbalancer
```

<span data-ttu-id="e2747-109">第一個命令會取得名為 MyLoadBalancer 的負載平衡器，然後將它儲存在 $loadbalancer 變數中。</span><span class="sxs-lookup"><span data-stu-id="e2747-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>

<span data-ttu-id="e2747-110">第二個命令會從 $loadbalancer 中的負載平衡器刪除名為 MyProbe 的配置。</span><span class="sxs-lookup"><span data-stu-id="e2747-110">The second command deletes the configuration named MyProbe from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="e2747-111">參數</span><span class="sxs-lookup"><span data-stu-id="e2747-111">PARAMETERS</span></span>

### <span data-ttu-id="e2747-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2747-112">-DefaultProfile</span></span>
<span data-ttu-id="e2747-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e2747-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2747-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e2747-114">-LoadBalancer</span></span>
<span data-ttu-id="e2747-115">指定包含此 Cmdlet 移除之探測配置的負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="e2747-115">Specifies the load balancer that contains the probe configuration that this cmdlet removes.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2747-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="e2747-116">-Name</span></span>
<span data-ttu-id="e2747-117">指定此 Cmdlet 移除之探測設定的名稱。</span><span class="sxs-lookup"><span data-stu-id="e2747-117">Specifies the name of the probe configuration that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2747-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2747-118">CommonParameters</span></span>
<span data-ttu-id="e2747-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e2747-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2747-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e2747-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2747-121">輸入</span><span class="sxs-lookup"><span data-stu-id="e2747-121">INPUTS</span></span>

### <span data-ttu-id="e2747-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e2747-122">PSLoadBalancer</span></span>
<span data-ttu-id="e2747-123">形參 "LoadBalancer" 接受管線中 "PSLoadBalancer" 類型的值</span><span class="sxs-lookup"><span data-stu-id="e2747-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="e2747-124">輸出</span><span class="sxs-lookup"><span data-stu-id="e2747-124">OUTPUTS</span></span>

### <span data-ttu-id="e2747-125">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e2747-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="e2747-126">筆記</span><span class="sxs-lookup"><span data-stu-id="e2747-126">NOTES</span></span>

## <span data-ttu-id="e2747-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="e2747-127">RELATED LINKS</span></span>

[<span data-ttu-id="e2747-128">附加 AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e2747-128">Add-AzureRmLoadBalancerProbeConfig</span></span>](./Add-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="e2747-129">AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e2747-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="e2747-130">AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e2747-130">Get-AzureRmLoadBalancerProbeConfig</span></span>](./Get-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="e2747-131">新-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e2747-131">New-AzureRmLoadBalancerProbeConfig</span></span>](./New-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="e2747-132">Set-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e2747-132">Set-AzureRmLoadBalancerProbeConfig</span></span>](./Set-AzureRmLoadBalancerProbeConfig.md)


