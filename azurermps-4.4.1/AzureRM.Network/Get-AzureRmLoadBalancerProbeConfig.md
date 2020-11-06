---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 278228EB-0126-4F27-A30F-51DC498C65FE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerProbeConfig.md
ms.openlocfilehash: 95844e21440c208db17001ca649a81e71951a128
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451631"
---
# <span data-ttu-id="5976a-101">Get-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="5976a-101">Get-AzureRmLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="5976a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5976a-102">SYNOPSIS</span></span>
<span data-ttu-id="5976a-103">取得負載平衡器的探測配置。</span><span class="sxs-lookup"><span data-stu-id="5976a-103">Gets a probe configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5976a-104">句法</span><span class="sxs-lookup"><span data-stu-id="5976a-104">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerProbeConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5976a-105">說明</span><span class="sxs-lookup"><span data-stu-id="5976a-105">DESCRIPTION</span></span>
<span data-ttu-id="5976a-106">**AzureRmLoadBalancerProbeConfig** Cmdlet 會取得一或多個負載平衡器的探測設定。</span><span class="sxs-lookup"><span data-stu-id="5976a-106">The **Get-AzureRmLoadBalancerProbeConfig** cmdlet gets one or more probe configurations for a load balancer.</span></span>

## <span data-ttu-id="5976a-107">示例</span><span class="sxs-lookup"><span data-stu-id="5976a-107">EXAMPLES</span></span>

### <span data-ttu-id="5976a-108">範例1：取得負載平衡器的探測設定</span><span class="sxs-lookup"><span data-stu-id="5976a-108">Example 1: Get the probe configuration of a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzureRmLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $slb
```

<span data-ttu-id="5976a-109">第一個命令會取得名為 MyLoadBalancer 的負載平衡器，然後將它儲存在 $slb 的變數中。</span><span class="sxs-lookup"><span data-stu-id="5976a-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>

<span data-ttu-id="5976a-110">第二個命令會從 $slb 中的負載平衡器取得名為 MyProbe 的關聯探測配置。</span><span class="sxs-lookup"><span data-stu-id="5976a-110">The second command gets the associated probe configuration named MyProbe from the load balancer in $slb.</span></span>

## <span data-ttu-id="5976a-111">參數</span><span class="sxs-lookup"><span data-stu-id="5976a-111">PARAMETERS</span></span>

### <span data-ttu-id="5976a-112">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5976a-112">-LoadBalancer</span></span>
<span data-ttu-id="5976a-113">指定與要取得之探測設定關聯的負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="5976a-113">Specifies the load balancer that is associated with the probe configuration to get.</span></span>

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

### <span data-ttu-id="5976a-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="5976a-114">-Name</span></span>
<span data-ttu-id="5976a-115">指定要取得的探測配置名稱。</span><span class="sxs-lookup"><span data-stu-id="5976a-115">Specifies the name of the probe configuration to get.</span></span>

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

### <span data-ttu-id="5976a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5976a-116">-DefaultProfile</span></span>
<span data-ttu-id="5976a-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5976a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5976a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5976a-118">CommonParameters</span></span>
<span data-ttu-id="5976a-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5976a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5976a-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5976a-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5976a-121">輸入</span><span class="sxs-lookup"><span data-stu-id="5976a-121">INPUTS</span></span>

### <span data-ttu-id="5976a-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5976a-122">PSLoadBalancer</span></span>
<span data-ttu-id="5976a-123">形參 "LoadBalancer" 接受管線中 "PSLoadBalancer" 類型的值</span><span class="sxs-lookup"><span data-stu-id="5976a-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="5976a-124">輸出</span><span class="sxs-lookup"><span data-stu-id="5976a-124">OUTPUTS</span></span>

### <span data-ttu-id="5976a-125">PSProbe 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="5976a-125">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="5976a-126">筆記</span><span class="sxs-lookup"><span data-stu-id="5976a-126">NOTES</span></span>

## <span data-ttu-id="5976a-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="5976a-127">RELATED LINKS</span></span>

[<span data-ttu-id="5976a-128">附加 AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="5976a-128">Add-AzureRmLoadBalancerProbeConfig</span></span>](./Add-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="5976a-129">AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5976a-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="5976a-130">新-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="5976a-130">New-AzureRmLoadBalancerProbeConfig</span></span>](./New-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="5976a-131">移除-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="5976a-131">Remove-AzureRmLoadBalancerProbeConfig</span></span>](./Remove-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="5976a-132">Set-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="5976a-132">Set-AzureRmLoadBalancerProbeConfig</span></span>](./Set-AzureRmLoadBalancerProbeConfig.md)

