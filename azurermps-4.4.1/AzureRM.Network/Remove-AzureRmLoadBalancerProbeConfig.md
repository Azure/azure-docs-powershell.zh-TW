---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2B15B224-E36C-454B-B6C2-F2BE032AE962
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerProbeConfig.md
ms.openlocfilehash: 132ec5259a6d03591860dceaaa215f8db57c27dd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623501"
---
# <span data-ttu-id="be650-101">Remove-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="be650-101">Remove-AzureRmLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="be650-102">摘要</span><span class="sxs-lookup"><span data-stu-id="be650-102">SYNOPSIS</span></span>
<span data-ttu-id="be650-103">從負載平衡器移除探測器配置。</span><span class="sxs-lookup"><span data-stu-id="be650-103">Removes a probe configuration from a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be650-104">句法</span><span class="sxs-lookup"><span data-stu-id="be650-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerProbeConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="be650-105">說明</span><span class="sxs-lookup"><span data-stu-id="be650-105">DESCRIPTION</span></span>
<span data-ttu-id="be650-106">**AzureRmLoadBalancerProbeConfig** Cmdlet 會從負載平衡器移除探測器配置。</span><span class="sxs-lookup"><span data-stu-id="be650-106">The **Remove-AzureRmLoadBalancerProbeConfig** cmdlet removes a probe configuration from a load balancer.</span></span>

## <span data-ttu-id="be650-107">示例</span><span class="sxs-lookup"><span data-stu-id="be650-107">EXAMPLES</span></span>

### <span data-ttu-id="be650-108">範例1：從負載平衡器移除探測器配置</span><span class="sxs-lookup"><span data-stu-id="be650-108">Example 1: Remove a probe configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzureRmLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $loadbalancer
```

<span data-ttu-id="be650-109">第一個命令會取得名為 MyLoadBalancer 的負載平衡器，然後將它儲存在 $loadbalancer 變數中。</span><span class="sxs-lookup"><span data-stu-id="be650-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>

<span data-ttu-id="be650-110">第二個命令會從 $loadbalancer 中的負載平衡器刪除名為 MyProbe 的配置。</span><span class="sxs-lookup"><span data-stu-id="be650-110">The second command deletes the configuration named MyProbe from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="be650-111">參數</span><span class="sxs-lookup"><span data-stu-id="be650-111">PARAMETERS</span></span>

### <span data-ttu-id="be650-112">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="be650-112">-LoadBalancer</span></span>
<span data-ttu-id="be650-113">指定包含此 Cmdlet 移除之探測配置的負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="be650-113">Specifies the load balancer that contains the probe configuration that this cmdlet removes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="be650-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="be650-114">-Name</span></span>
<span data-ttu-id="be650-115">指定此 Cmdlet 移除之探測設定的名稱。</span><span class="sxs-lookup"><span data-stu-id="be650-115">Specifies the name of the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="be650-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be650-116">-DefaultProfile</span></span>
<span data-ttu-id="be650-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="be650-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="be650-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be650-118">CommonParameters</span></span>
<span data-ttu-id="be650-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="be650-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be650-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="be650-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be650-121">輸入</span><span class="sxs-lookup"><span data-stu-id="be650-121">INPUTS</span></span>

### <span data-ttu-id="be650-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="be650-122">PSLoadBalancer</span></span>
<span data-ttu-id="be650-123">形參 "LoadBalancer" 接受管線中 "PSLoadBalancer" 類型的值</span><span class="sxs-lookup"><span data-stu-id="be650-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="be650-124">輸出</span><span class="sxs-lookup"><span data-stu-id="be650-124">OUTPUTS</span></span>

### <span data-ttu-id="be650-125">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="be650-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="be650-126">筆記</span><span class="sxs-lookup"><span data-stu-id="be650-126">NOTES</span></span>

## <span data-ttu-id="be650-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="be650-127">RELATED LINKS</span></span>

[<span data-ttu-id="be650-128">附加 AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="be650-128">Add-AzureRmLoadBalancerProbeConfig</span></span>](./Add-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="be650-129">AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="be650-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="be650-130">AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="be650-130">Get-AzureRmLoadBalancerProbeConfig</span></span>](./Get-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="be650-131">新-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="be650-131">New-AzureRmLoadBalancerProbeConfig</span></span>](./New-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="be650-132">Set-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="be650-132">Set-AzureRmLoadBalancerProbeConfig</span></span>](./Set-AzureRmLoadBalancerProbeConfig.md)


