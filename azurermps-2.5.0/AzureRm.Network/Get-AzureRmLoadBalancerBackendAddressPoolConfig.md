---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F421174A-B138-45EB-AF84-CB3CE5870F27
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancerbackendaddresspoolconfig
schema: 2.0.0
ms.openlocfilehash: 4bfae8947661f21441d67d6d82dbc8751f3128d2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800862"
---
# <span data-ttu-id="a5f01-101">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="a5f01-101">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="a5f01-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a5f01-102">SYNOPSIS</span></span>
<span data-ttu-id="a5f01-103">取得負載平衡器的後端位址集區配置。</span><span class="sxs-lookup"><span data-stu-id="a5f01-103">Gets a backend address pool configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5f01-104">句法</span><span class="sxs-lookup"><span data-stu-id="a5f01-104">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerBackendAddressPoolConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5f01-105">說明</span><span class="sxs-lookup"><span data-stu-id="a5f01-105">DESCRIPTION</span></span>
<span data-ttu-id="a5f01-106">**AzureRmLoadBalancerBackendAddressPoolConfig** Cmdlet 會取得單一後端位址集區或負載平衡器內後端位址集區清單。</span><span class="sxs-lookup"><span data-stu-id="a5f01-106">The **Get-AzureRmLoadBalancerBackendAddressPoolConfig** cmdlet gets a single backend address pool or a list of backend address pools within a load balancer.</span></span>

## <span data-ttu-id="a5f01-107">示例</span><span class="sxs-lookup"><span data-stu-id="a5f01-107">EXAMPLES</span></span>

### <span data-ttu-id="a5f01-108">範例1：取得後端位址集區</span><span class="sxs-lookup"><span data-stu-id="a5f01-108">Example 1: Get the backend address pool</span></span>
```
PS C:\>$loadbalancer = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzureRmLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" -LoadBalancer $loadbalancer
```

<span data-ttu-id="a5f01-109">第一個命令會在名為 MyResourceGroup 的資源群組中，取得名為 MyLoadBalancer 的現有負載平衡器，然後將它儲存在 $loadbalancer 變數中。</span><span class="sxs-lookup"><span data-stu-id="a5f01-109">The first command gets an existing load balancer named MyLoadBalancer in the resource group named MyResourceGroup, and then stores it in the $loadbalancer variable.</span></span>

<span data-ttu-id="a5f01-110">第二個命令會針對 $loadbalancer 中的負載平衡器，取得名為 BackendAddressPool02 的關聯後端位址集區配置。</span><span class="sxs-lookup"><span data-stu-id="a5f01-110">The second command gets the associated backend address pool configuration named BackendAddressPool02 for the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="a5f01-111">參數</span><span class="sxs-lookup"><span data-stu-id="a5f01-111">PARAMETERS</span></span>

### <span data-ttu-id="a5f01-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5f01-112">-DefaultProfile</span></span>
<span data-ttu-id="a5f01-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a5f01-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5f01-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a5f01-114">-LoadBalancer</span></span>
<span data-ttu-id="a5f01-115">指定與要取得的後端位址集區相關聯的負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="a5f01-115">Specifies the load balancer that is associated with the backend address pool to get.</span></span>

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

### <span data-ttu-id="a5f01-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="a5f01-116">-Name</span></span>
<span data-ttu-id="a5f01-117">指定包含要取得之後端位址集區的負載平衡器名稱。</span><span class="sxs-lookup"><span data-stu-id="a5f01-117">Specifies the name of the load balancer that contains the backend address pool to get.</span></span>

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

### <span data-ttu-id="a5f01-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5f01-118">CommonParameters</span></span>
<span data-ttu-id="a5f01-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a5f01-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5f01-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a5f01-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5f01-121">輸入</span><span class="sxs-lookup"><span data-stu-id="a5f01-121">INPUTS</span></span>

### <span data-ttu-id="a5f01-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a5f01-122">PSLoadBalancer</span></span>
<span data-ttu-id="a5f01-123">形參 "LoadBalancer" 接受管線中 "PSLoadBalancer" 類型的值</span><span class="sxs-lookup"><span data-stu-id="a5f01-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="a5f01-124">輸出</span><span class="sxs-lookup"><span data-stu-id="a5f01-124">OUTPUTS</span></span>

### <span data-ttu-id="a5f01-125">PSBackendAddressPool 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a5f01-125">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="a5f01-126">筆記</span><span class="sxs-lookup"><span data-stu-id="a5f01-126">NOTES</span></span>

## <span data-ttu-id="a5f01-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="a5f01-127">RELATED LINKS</span></span>

[<span data-ttu-id="a5f01-128">附加 AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="a5f01-128">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="a5f01-129">AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a5f01-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="a5f01-130">新-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="a5f01-130">New-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="a5f01-131">移除-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="a5f01-131">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzureRmLoadBalancerBackendAddressPoolConfig.md)


