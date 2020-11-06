---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F421174A-B138-45EB-AF84-CB3CE5870F27
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 2a9fca5faf7ba024a5d5c891aa1c74ba002ac053
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449053"
---
# <span data-ttu-id="3aa69-101">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="3aa69-101">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="3aa69-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3aa69-102">SYNOPSIS</span></span>
<span data-ttu-id="3aa69-103">取得負載平衡器的後端位址集區配置。</span><span class="sxs-lookup"><span data-stu-id="3aa69-103">Gets a backend address pool configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3aa69-104">句法</span><span class="sxs-lookup"><span data-stu-id="3aa69-104">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerBackendAddressPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3aa69-105">說明</span><span class="sxs-lookup"><span data-stu-id="3aa69-105">DESCRIPTION</span></span>
<span data-ttu-id="3aa69-106">**AzureRmLoadBalancerBackendAddressPoolConfig** Cmdlet 會取得單一後端位址集區或負載平衡器內後端位址集區清單。</span><span class="sxs-lookup"><span data-stu-id="3aa69-106">The **Get-AzureRmLoadBalancerBackendAddressPoolConfig** cmdlet gets a single backend address pool or a list of backend address pools within a load balancer.</span></span>

## <span data-ttu-id="3aa69-107">示例</span><span class="sxs-lookup"><span data-stu-id="3aa69-107">EXAMPLES</span></span>

### <span data-ttu-id="3aa69-108">範例1：取得後端位址集區</span><span class="sxs-lookup"><span data-stu-id="3aa69-108">Example 1: Get the backend address pool</span></span>
```
PS C:\>$loadbalancer = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzureRmLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" -LoadBalancer $loadbalancer
```

<span data-ttu-id="3aa69-109">第一個命令會在名為 MyResourceGroup 的資源群組中，取得名為 MyLoadBalancer 的現有負載平衡器，然後將它儲存在 $loadbalancer 變數中。</span><span class="sxs-lookup"><span data-stu-id="3aa69-109">The first command gets an existing load balancer named MyLoadBalancer in the resource group named MyResourceGroup, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="3aa69-110">第二個命令會針對 $loadbalancer 中的負載平衡器，取得名為 BackendAddressPool02 的關聯後端位址集區配置。</span><span class="sxs-lookup"><span data-stu-id="3aa69-110">The second command gets the associated backend address pool configuration named BackendAddressPool02 for the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="3aa69-111">參數</span><span class="sxs-lookup"><span data-stu-id="3aa69-111">PARAMETERS</span></span>

### <span data-ttu-id="3aa69-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3aa69-112">-DefaultProfile</span></span>
<span data-ttu-id="3aa69-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3aa69-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3aa69-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3aa69-114">-LoadBalancer</span></span>
<span data-ttu-id="3aa69-115">指定與要取得的後端位址集區相關聯的負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="3aa69-115">Specifies the load balancer that is associated with the backend address pool to get.</span></span>

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

### <span data-ttu-id="3aa69-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="3aa69-116">-Name</span></span>
<span data-ttu-id="3aa69-117">指定包含要取得之後端位址集區的負載平衡器名稱。</span><span class="sxs-lookup"><span data-stu-id="3aa69-117">Specifies the name of the load balancer that contains the backend address pool to get.</span></span>

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

### <span data-ttu-id="3aa69-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3aa69-118">CommonParameters</span></span>
<span data-ttu-id="3aa69-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3aa69-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3aa69-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3aa69-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3aa69-121">輸入</span><span class="sxs-lookup"><span data-stu-id="3aa69-121">INPUTS</span></span>

### <span data-ttu-id="3aa69-122">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="3aa69-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="3aa69-123">參數： LoadBalancer (ByValue) </span><span class="sxs-lookup"><span data-stu-id="3aa69-123">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="3aa69-124">輸出</span><span class="sxs-lookup"><span data-stu-id="3aa69-124">OUTPUTS</span></span>

### <span data-ttu-id="3aa69-125">PSBackendAddressPool 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="3aa69-125">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="3aa69-126">筆記</span><span class="sxs-lookup"><span data-stu-id="3aa69-126">NOTES</span></span>

## <span data-ttu-id="3aa69-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="3aa69-127">RELATED LINKS</span></span>

[<span data-ttu-id="3aa69-128">附加 AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="3aa69-128">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="3aa69-129">AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3aa69-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="3aa69-130">新-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="3aa69-130">New-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="3aa69-131">移除-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="3aa69-131">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzureRmLoadBalancerBackendAddressPoolConfig.md)


