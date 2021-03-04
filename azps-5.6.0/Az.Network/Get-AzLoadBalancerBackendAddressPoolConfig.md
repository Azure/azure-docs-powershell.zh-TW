---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F421174A-B138-45EB-AF84-CB3CE5870F27
online version: https://docs.microsoft.com/powershell/module/az.network/get-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: a337446238807f3a6408d0c9b68034e4a245eb48
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903125"
---
# <span data-ttu-id="12d96-101">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="12d96-101">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="12d96-102">簡介</span><span class="sxs-lookup"><span data-stu-id="12d96-102">SYNOPSIS</span></span>
<span data-ttu-id="12d96-103">取得負載平衡器後端位址資料庫組。</span><span class="sxs-lookup"><span data-stu-id="12d96-103">Gets a backend address pool configuration for a load balancer.</span></span>

## <span data-ttu-id="12d96-104">語法</span><span class="sxs-lookup"><span data-stu-id="12d96-104">SYNTAX</span></span>

```
Get-AzLoadBalancerBackendAddressPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12d96-105">描述</span><span class="sxs-lookup"><span data-stu-id="12d96-105">DESCRIPTION</span></span>
<span data-ttu-id="12d96-106">**Get-AzLoadBalancerBackendAddressPoolConfig** Cmdlet 會取得負載平衡器內的單一後端位址集區或後端位址集區清單。</span><span class="sxs-lookup"><span data-stu-id="12d96-106">The **Get-AzLoadBalancerBackendAddressPoolConfig** cmdlet gets a single backend address pool or a list of backend address pools within a load balancer.</span></span>

## <span data-ttu-id="12d96-107">例子</span><span class="sxs-lookup"><span data-stu-id="12d96-107">EXAMPLES</span></span>

### <span data-ttu-id="12d96-108">範例 1：取得後端位址資料庫</span><span class="sxs-lookup"><span data-stu-id="12d96-108">Example 1: Get the backend address pool</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" -LoadBalancer $loadbalancer
```

<span data-ttu-id="12d96-109">第一個命令會取得名為 MyResourceGroup 的資源群組中名為 MyLoadBalancer 的現有負載平衡器，然後將它儲存在 $loadbalancer 變數中。</span><span class="sxs-lookup"><span data-stu-id="12d96-109">The first command gets an existing load balancer named MyLoadBalancer in the resource group named MyResourceGroup, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="12d96-110">第二個命令會針對 $loadbalancer 中的負載平衡器，取得名為後端位址資料庫的關聯後端位址資料庫組$loadbalancer。</span><span class="sxs-lookup"><span data-stu-id="12d96-110">The second command gets the associated backend address pool configuration named BackendAddressPool02 for the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="12d96-111">參數</span><span class="sxs-lookup"><span data-stu-id="12d96-111">PARAMETERS</span></span>

### <span data-ttu-id="12d96-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12d96-112">-DefaultProfile</span></span>
<span data-ttu-id="12d96-113">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="12d96-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12d96-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="12d96-114">-LoadBalancer</span></span>
<span data-ttu-id="12d96-115">指定要取得與後端位址資料庫相關聯的負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="12d96-115">Specifies the load balancer that is associated with the backend address pool to get.</span></span>

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

### <span data-ttu-id="12d96-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="12d96-116">-Name</span></span>
<span data-ttu-id="12d96-117">指定包含要取得後端位址集區之負載平衡器的名稱。</span><span class="sxs-lookup"><span data-stu-id="12d96-117">Specifies the name of the load balancer that contains the backend address pool to get.</span></span>

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

### <span data-ttu-id="12d96-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12d96-118">CommonParameters</span></span>
<span data-ttu-id="12d96-119">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="12d96-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12d96-120">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="12d96-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12d96-121">輸入</span><span class="sxs-lookup"><span data-stu-id="12d96-121">INPUTS</span></span>

### <span data-ttu-id="12d96-122">Microsoft.Azure.Commands.Network.models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="12d96-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="12d96-123">輸出</span><span class="sxs-lookup"><span data-stu-id="12d96-123">OUTPUTS</span></span>

### <span data-ttu-id="12d96-124">Microsoft.Azure.Commands.Network.models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="12d96-124">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="12d96-125">筆記</span><span class="sxs-lookup"><span data-stu-id="12d96-125">NOTES</span></span>

## <span data-ttu-id="12d96-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="12d96-126">RELATED LINKS</span></span>

[<span data-ttu-id="12d96-127">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="12d96-127">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="12d96-128">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="12d96-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="12d96-129">New-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="12d96-129">New-AzLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="12d96-130">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="12d96-130">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzLoadBalancerBackendAddressPoolConfig.md)


