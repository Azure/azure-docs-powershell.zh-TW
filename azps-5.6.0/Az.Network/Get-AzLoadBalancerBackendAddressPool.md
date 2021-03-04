---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azloadbalancerbackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPool.md
ms.openlocfilehash: 72afb446b41143348b9feaa7e1b465a41d2b9cbe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903130"
---
# <span data-ttu-id="ee821-101">Get-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="ee821-101">Get-AzLoadBalancerBackendAddressPool</span></span>

## <span data-ttu-id="ee821-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ee821-102">SYNOPSIS</span></span>
<span data-ttu-id="ee821-103">Get-AzLoadBalancerBackendAddressPool一或多個與負載平衡器相關聯的後端位址資料庫。</span><span class="sxs-lookup"><span data-stu-id="ee821-103">Get-AzLoadBalancerBackendAddressPool retrieves one or more backend address pools associated with a load balancer.</span></span> 

## <span data-ttu-id="ee821-104">語法</span><span class="sxs-lookup"><span data-stu-id="ee821-104">SYNTAX</span></span>

### <span data-ttu-id="ee821-105">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee821-105">GetByNameParameterSet</span></span>
```
Get-AzLoadBalancerBackendAddressPool -ResourceGroupName <String> -LoadBalancerName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ee821-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee821-106">GetByParentObjectParameterSet</span></span>
```
Get-AzLoadBalancerBackendAddressPool [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ee821-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee821-107">GetByResourceIdParameterSet</span></span>
```
Get-AzLoadBalancerBackendAddressPool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ee821-108">描述</span><span class="sxs-lookup"><span data-stu-id="ee821-108">DESCRIPTION</span></span>
<span data-ttu-id="ee821-109">Get-AzLoadBalancerBackendAddressPool一或多個與負載平衡器相關聯的後端位址資料庫。</span><span class="sxs-lookup"><span data-stu-id="ee821-109">Get-AzLoadBalancerBackendAddressPool retrieves one or more backend address pools associated with a load balancer.</span></span>

## <span data-ttu-id="ee821-110">例子</span><span class="sxs-lookup"><span data-stu-id="ee821-110">EXAMPLES</span></span>

### <span data-ttu-id="ee821-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="ee821-111">Example 1</span></span>
```powershell
## Get single backend under loadbalancer
PS C:\> $lb = Get-AzLoadBalancer -ResourceGroupName $resourceGroup -Name $loadBalancerName
```

```powershell
## Get all backends under loadbalancer
PS C:\> $lb | Get-AzLoadBalancerBackendAddressPool
```
### <span data-ttu-id="ee821-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="ee821-112">Example 2</span></span>
```powershell
#Get specific backend from loadbalancer
PS C:\> $lb | Get-AzLoadBalancerBackendAddressPool -Name $backendPool1
```

### <span data-ttu-id="ee821-113">範例 3</span><span class="sxs-lookup"><span data-stu-id="ee821-113">Example 3</span></span>
```powershell
#Get a backend by resource Id
PS C:\> Get-AzLoadBalancerBackendAddressPool -ResourceId $backendPool1.Id
```

## <span data-ttu-id="ee821-114">參數</span><span class="sxs-lookup"><span data-stu-id="ee821-114">PARAMETERS</span></span>

### <span data-ttu-id="ee821-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee821-115">-DefaultProfile</span></span>
<span data-ttu-id="ee821-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ee821-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee821-117">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ee821-117">-LoadBalancer</span></span>
<span data-ttu-id="ee821-118">{{ Fill LoadBalancer Description }}</span><span class="sxs-lookup"><span data-stu-id="ee821-118">{{ Fill LoadBalancer Description }}</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ee821-119">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="ee821-119">-LoadBalancerName</span></span>
<span data-ttu-id="ee821-120">負載平衡器的名稱。</span><span class="sxs-lookup"><span data-stu-id="ee821-120">The name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee821-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="ee821-121">-Name</span></span>
<span data-ttu-id="ee821-122">後端位址資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="ee821-122">The name of the backend address pool.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee821-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee821-123">-ResourceGroupName</span></span>
<span data-ttu-id="ee821-124">負載平衡器的資源組名。</span><span class="sxs-lookup"><span data-stu-id="ee821-124">The resource group name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee821-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ee821-125">-ResourceId</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee821-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee821-126">CommonParameters</span></span>
<span data-ttu-id="ee821-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ee821-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee821-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ee821-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee821-129">輸入</span><span class="sxs-lookup"><span data-stu-id="ee821-129">INPUTS</span></span>

### <span data-ttu-id="ee821-130">Microsoft.Azure.Commands.Network.models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ee821-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="ee821-131">System.String</span><span class="sxs-lookup"><span data-stu-id="ee821-131">System.String</span></span>

## <span data-ttu-id="ee821-132">輸出</span><span class="sxs-lookup"><span data-stu-id="ee821-132">OUTPUTS</span></span>

### <span data-ttu-id="ee821-133">Microsoft.Azure.Commands.Network.models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="ee821-133">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="ee821-134">筆記</span><span class="sxs-lookup"><span data-stu-id="ee821-134">NOTES</span></span>

## <span data-ttu-id="ee821-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="ee821-135">RELATED LINKS</span></span>
