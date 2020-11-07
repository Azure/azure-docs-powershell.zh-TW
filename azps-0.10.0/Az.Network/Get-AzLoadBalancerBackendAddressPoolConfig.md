---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F421174A-B138-45EB-AF84-CB3CE5870F27
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 9c2341494f1508563523a181532ce98347051ac3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794422"
---
# <span data-ttu-id="1306b-101">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="1306b-101">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="1306b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1306b-102">SYNOPSIS</span></span>
<span data-ttu-id="1306b-103">取得負載平衡器的後端位址集區配置。</span><span class="sxs-lookup"><span data-stu-id="1306b-103">Gets a backend address pool configuration for a load balancer.</span></span>

## <span data-ttu-id="1306b-104">句法</span><span class="sxs-lookup"><span data-stu-id="1306b-104">SYNTAX</span></span>

```
Get-AzLoadBalancerBackendAddressPoolConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1306b-105">說明</span><span class="sxs-lookup"><span data-stu-id="1306b-105">DESCRIPTION</span></span>
<span data-ttu-id="1306b-106">**AzLoadBalancerBackendAddressPoolConfig** Cmdlet 會取得單一後端位址集區或負載平衡器內後端位址集區清單。</span><span class="sxs-lookup"><span data-stu-id="1306b-106">The **Get-AzLoadBalancerBackendAddressPoolConfig** cmdlet gets a single backend address pool or a list of backend address pools within a load balancer.</span></span>

## <span data-ttu-id="1306b-107">示例</span><span class="sxs-lookup"><span data-stu-id="1306b-107">EXAMPLES</span></span>

### <span data-ttu-id="1306b-108">範例1：取得後端位址集區</span><span class="sxs-lookup"><span data-stu-id="1306b-108">Example 1: Get the backend address pool</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" -LoadBalancer $loadbalancer
```

<span data-ttu-id="1306b-109">第一個命令會在名為 MyResourceGroup 的資源群組中，取得名為 MyLoadBalancer 的現有負載平衡器，然後將它儲存在 $loadbalancer 變數中。</span><span class="sxs-lookup"><span data-stu-id="1306b-109">The first command gets an existing load balancer named MyLoadBalancer in the resource group named MyResourceGroup, and then stores it in the $loadbalancer variable.</span></span>

<span data-ttu-id="1306b-110">第二個命令會針對 $loadbalancer 中的負載平衡器，取得名為 BackendAddressPool02 的關聯後端位址集區配置。</span><span class="sxs-lookup"><span data-stu-id="1306b-110">The second command gets the associated backend address pool configuration named BackendAddressPool02 for the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="1306b-111">參數</span><span class="sxs-lookup"><span data-stu-id="1306b-111">PARAMETERS</span></span>

### <span data-ttu-id="1306b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1306b-112">-DefaultProfile</span></span>
<span data-ttu-id="1306b-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1306b-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1306b-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1306b-114">-LoadBalancer</span></span>
<span data-ttu-id="1306b-115">指定與要取得的後端位址集區相關聯的負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="1306b-115">Specifies the load balancer that is associated with the backend address pool to get.</span></span>

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

### <span data-ttu-id="1306b-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="1306b-116">-Name</span></span>
<span data-ttu-id="1306b-117">指定包含要取得之後端位址集區的負載平衡器名稱。</span><span class="sxs-lookup"><span data-stu-id="1306b-117">Specifies the name of the load balancer that contains the backend address pool to get.</span></span>

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

### <span data-ttu-id="1306b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1306b-118">CommonParameters</span></span>
<span data-ttu-id="1306b-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1306b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1306b-120">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1306b-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1306b-121">輸入</span><span class="sxs-lookup"><span data-stu-id="1306b-121">INPUTS</span></span>

### <span data-ttu-id="1306b-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1306b-122">PSLoadBalancer</span></span>
<span data-ttu-id="1306b-123">形參 "LoadBalancer" 接受管線中 "PSLoadBalancer" 類型的值</span><span class="sxs-lookup"><span data-stu-id="1306b-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="1306b-124">輸出</span><span class="sxs-lookup"><span data-stu-id="1306b-124">OUTPUTS</span></span>

### <span data-ttu-id="1306b-125">PSBackendAddressPool 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="1306b-125">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="1306b-126">筆記</span><span class="sxs-lookup"><span data-stu-id="1306b-126">NOTES</span></span>

## <span data-ttu-id="1306b-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="1306b-127">RELATED LINKS</span></span>

[<span data-ttu-id="1306b-128">附加 AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="1306b-128">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="1306b-129">AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1306b-129">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="1306b-130">新-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="1306b-130">New-AzLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="1306b-131">移除-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="1306b-131">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzLoadBalancerBackendAddressPoolConfig.md)


