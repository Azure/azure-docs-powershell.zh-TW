---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F421174A-B138-45EB-AF84-CB3CE5870F27
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: f6acd469c49df7e67e8aa9bf00faf4952a33eb79
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100133895"
---
# <span data-ttu-id="af7ea-101">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="af7ea-101">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="af7ea-102">摘要</span><span class="sxs-lookup"><span data-stu-id="af7ea-102">SYNOPSIS</span></span>
<span data-ttu-id="af7ea-103">取得負載平衡器的後端位址集區配置。</span><span class="sxs-lookup"><span data-stu-id="af7ea-103">Gets a backend address pool configuration for a load balancer.</span></span>

## <span data-ttu-id="af7ea-104">句法</span><span class="sxs-lookup"><span data-stu-id="af7ea-104">SYNTAX</span></span>

```
Get-AzLoadBalancerBackendAddressPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af7ea-105">說明</span><span class="sxs-lookup"><span data-stu-id="af7ea-105">DESCRIPTION</span></span>
<span data-ttu-id="af7ea-106">**AzLoadBalancerBackendAddressPoolConfig** Cmdlet 會取得單一後端位址集區或負載平衡器內後端位址集區清單。</span><span class="sxs-lookup"><span data-stu-id="af7ea-106">The **Get-AzLoadBalancerBackendAddressPoolConfig** cmdlet gets a single backend address pool or a list of backend address pools within a load balancer.</span></span>

## <span data-ttu-id="af7ea-107">示例</span><span class="sxs-lookup"><span data-stu-id="af7ea-107">EXAMPLES</span></span>

### <span data-ttu-id="af7ea-108">範例1：取得後端位址集區</span><span class="sxs-lookup"><span data-stu-id="af7ea-108">Example 1: Get the backend address pool</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" -LoadBalancer $loadbalancer
```

<span data-ttu-id="af7ea-109">第一個命令會在名為 MyResourceGroup 的資源群組中，取得名為 MyLoadBalancer 的現有負載平衡器，然後將它儲存在 $loadbalancer 變數中。</span><span class="sxs-lookup"><span data-stu-id="af7ea-109">The first command gets an existing load balancer named MyLoadBalancer in the resource group named MyResourceGroup, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="af7ea-110">第二個命令會針對 $loadbalancer 中的負載平衡器，取得名為 BackendAddressPool02 的關聯後端位址集區配置。</span><span class="sxs-lookup"><span data-stu-id="af7ea-110">The second command gets the associated backend address pool configuration named BackendAddressPool02 for the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="af7ea-111">參數</span><span class="sxs-lookup"><span data-stu-id="af7ea-111">PARAMETERS</span></span>

### <span data-ttu-id="af7ea-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af7ea-112">-DefaultProfile</span></span>
<span data-ttu-id="af7ea-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="af7ea-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af7ea-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="af7ea-114">-LoadBalancer</span></span>
<span data-ttu-id="af7ea-115">指定與要取得的後端位址集區相關聯的負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="af7ea-115">Specifies the load balancer that is associated with the backend address pool to get.</span></span>

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

### <span data-ttu-id="af7ea-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="af7ea-116">-Name</span></span>
<span data-ttu-id="af7ea-117">指定包含要取得之後端位址集區的負載平衡器名稱。</span><span class="sxs-lookup"><span data-stu-id="af7ea-117">Specifies the name of the load balancer that contains the backend address pool to get.</span></span>

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

### <span data-ttu-id="af7ea-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af7ea-118">CommonParameters</span></span>
<span data-ttu-id="af7ea-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="af7ea-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af7ea-120">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="af7ea-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af7ea-121">輸入</span><span class="sxs-lookup"><span data-stu-id="af7ea-121">INPUTS</span></span>

### <span data-ttu-id="af7ea-122">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="af7ea-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="af7ea-123">輸出</span><span class="sxs-lookup"><span data-stu-id="af7ea-123">OUTPUTS</span></span>

### <span data-ttu-id="af7ea-124">PSBackendAddressPool 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="af7ea-124">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="af7ea-125">筆記</span><span class="sxs-lookup"><span data-stu-id="af7ea-125">NOTES</span></span>

## <span data-ttu-id="af7ea-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="af7ea-126">RELATED LINKS</span></span>

[<span data-ttu-id="af7ea-127">附加 AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="af7ea-127">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="af7ea-128">AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="af7ea-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="af7ea-129">新-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="af7ea-129">New-AzLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="af7ea-130">移除-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="af7ea-130">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzLoadBalancerBackendAddressPoolConfig.md)


