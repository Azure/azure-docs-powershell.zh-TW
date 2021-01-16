---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 278228EB-0126-4F27-A30F-51DC498C65FE
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 5b6031657438bfc28ce76519c8489e041a060965
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98280324"
---
# <span data-ttu-id="3e564-101">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="3e564-101">Get-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="3e564-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3e564-102">SYNOPSIS</span></span>
<span data-ttu-id="3e564-103">取得負載平衡器的探測配置。</span><span class="sxs-lookup"><span data-stu-id="3e564-103">Gets a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="3e564-104">句法</span><span class="sxs-lookup"><span data-stu-id="3e564-104">SYNTAX</span></span>

```
Get-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e564-105">說明</span><span class="sxs-lookup"><span data-stu-id="3e564-105">DESCRIPTION</span></span>
<span data-ttu-id="3e564-106">**AzLoadBalancerProbeConfig** Cmdlet 會取得一或多個負載平衡器的探測設定。</span><span class="sxs-lookup"><span data-stu-id="3e564-106">The **Get-AzLoadBalancerProbeConfig** cmdlet gets one or more probe configurations for a load balancer.</span></span>

## <span data-ttu-id="3e564-107">示例</span><span class="sxs-lookup"><span data-stu-id="3e564-107">EXAMPLES</span></span>

### <span data-ttu-id="3e564-108">範例1：取得負載平衡器的探測設定</span><span class="sxs-lookup"><span data-stu-id="3e564-108">Example 1: Get the probe configuration of a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $slb
```

<span data-ttu-id="3e564-109">第一個命令會取得名為 MyLoadBalancer 的負載平衡器，然後將它儲存在 $slb 的變數中。</span><span class="sxs-lookup"><span data-stu-id="3e564-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="3e564-110">第二個命令會從 $slb 中的負載平衡器取得名為 MyProbe 的關聯探測配置。</span><span class="sxs-lookup"><span data-stu-id="3e564-110">The second command gets the associated probe configuration named MyProbe from the load balancer in $slb.</span></span>

## <span data-ttu-id="3e564-111">參數</span><span class="sxs-lookup"><span data-stu-id="3e564-111">PARAMETERS</span></span>

### <span data-ttu-id="3e564-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e564-112">-DefaultProfile</span></span>
<span data-ttu-id="3e564-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3e564-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e564-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3e564-114">-LoadBalancer</span></span>
<span data-ttu-id="3e564-115">指定與要取得之探測設定關聯的負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="3e564-115">Specifies the load balancer that is associated with the probe configuration to get.</span></span>

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

### <span data-ttu-id="3e564-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="3e564-116">-Name</span></span>
<span data-ttu-id="3e564-117">指定要取得的探測配置名稱。</span><span class="sxs-lookup"><span data-stu-id="3e564-117">Specifies the name of the probe configuration to get.</span></span>

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

### <span data-ttu-id="3e564-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e564-118">CommonParameters</span></span>
<span data-ttu-id="3e564-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3e564-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e564-120">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="3e564-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e564-121">輸入</span><span class="sxs-lookup"><span data-stu-id="3e564-121">INPUTS</span></span>

### <span data-ttu-id="3e564-122">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="3e564-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="3e564-123">輸出</span><span class="sxs-lookup"><span data-stu-id="3e564-123">OUTPUTS</span></span>

### <span data-ttu-id="3e564-124">PSProbe 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="3e564-124">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="3e564-125">筆記</span><span class="sxs-lookup"><span data-stu-id="3e564-125">NOTES</span></span>

## <span data-ttu-id="3e564-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="3e564-126">RELATED LINKS</span></span>

[<span data-ttu-id="3e564-127">附加 AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="3e564-127">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="3e564-128">AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3e564-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="3e564-129">新-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="3e564-129">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="3e564-130">移除-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="3e564-130">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="3e564-131">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="3e564-131">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


