---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2B15B224-E36C-454B-B6C2-F2BE032AE962
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 11de4e8966b5e57e817b6c5d829536deacf229f8
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794170"
---
# <span data-ttu-id="f2050-101">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="f2050-101">Remove-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="f2050-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f2050-102">SYNOPSIS</span></span>
<span data-ttu-id="f2050-103">從負載平衡器移除探測器配置。</span><span class="sxs-lookup"><span data-stu-id="f2050-103">Removes a probe configuration from a load balancer.</span></span>

## <span data-ttu-id="f2050-104">句法</span><span class="sxs-lookup"><span data-stu-id="f2050-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerProbeConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2050-105">說明</span><span class="sxs-lookup"><span data-stu-id="f2050-105">DESCRIPTION</span></span>
<span data-ttu-id="f2050-106">**AzLoadBalancerProbeConfig** Cmdlet 會從負載平衡器移除探測器配置。</span><span class="sxs-lookup"><span data-stu-id="f2050-106">The **Remove-AzLoadBalancerProbeConfig** cmdlet removes a probe configuration from a load balancer.</span></span>

## <span data-ttu-id="f2050-107">示例</span><span class="sxs-lookup"><span data-stu-id="f2050-107">EXAMPLES</span></span>

### <span data-ttu-id="f2050-108">範例1：從負載平衡器移除探測器配置</span><span class="sxs-lookup"><span data-stu-id="f2050-108">Example 1: Remove a probe configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $loadbalancer
```

<span data-ttu-id="f2050-109">第一個命令會取得名為 MyLoadBalancer 的負載平衡器，然後將它儲存在 $loadbalancer 變數中。</span><span class="sxs-lookup"><span data-stu-id="f2050-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>

<span data-ttu-id="f2050-110">第二個命令會從 $loadbalancer 中的負載平衡器刪除名為 MyProbe 的配置。</span><span class="sxs-lookup"><span data-stu-id="f2050-110">The second command deletes the configuration named MyProbe from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="f2050-111">參數</span><span class="sxs-lookup"><span data-stu-id="f2050-111">PARAMETERS</span></span>

### <span data-ttu-id="f2050-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2050-112">-DefaultProfile</span></span>
<span data-ttu-id="f2050-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f2050-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2050-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f2050-114">-LoadBalancer</span></span>
<span data-ttu-id="f2050-115">指定包含此 Cmdlet 移除之探測配置的負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="f2050-115">Specifies the load balancer that contains the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f2050-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="f2050-116">-Name</span></span>
<span data-ttu-id="f2050-117">指定此 Cmdlet 移除之探測設定的名稱。</span><span class="sxs-lookup"><span data-stu-id="f2050-117">Specifies the name of the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f2050-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2050-118">CommonParameters</span></span>
<span data-ttu-id="f2050-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f2050-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2050-120">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f2050-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2050-121">輸入</span><span class="sxs-lookup"><span data-stu-id="f2050-121">INPUTS</span></span>

### <span data-ttu-id="f2050-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f2050-122">PSLoadBalancer</span></span>
<span data-ttu-id="f2050-123">形參 "LoadBalancer" 接受管線中 "PSLoadBalancer" 類型的值</span><span class="sxs-lookup"><span data-stu-id="f2050-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="f2050-124">輸出</span><span class="sxs-lookup"><span data-stu-id="f2050-124">OUTPUTS</span></span>

### <span data-ttu-id="f2050-125">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f2050-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="f2050-126">筆記</span><span class="sxs-lookup"><span data-stu-id="f2050-126">NOTES</span></span>

## <span data-ttu-id="f2050-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="f2050-127">RELATED LINKS</span></span>

[<span data-ttu-id="f2050-128">附加 AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="f2050-128">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="f2050-129">AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f2050-129">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="f2050-130">AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="f2050-130">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="f2050-131">新-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="f2050-131">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="f2050-132">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="f2050-132">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


