---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerbackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPool.md
ms.openlocfilehash: 5d1c561af678086671927d3782a1fafbd9de503b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94140939"
---
# <span data-ttu-id="5b064-101">Get-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="5b064-101">Get-AzLoadBalancerBackendAddressPool</span></span>

## <span data-ttu-id="5b064-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5b064-102">SYNOPSIS</span></span>
<span data-ttu-id="5b064-103">Get-AzLoadBalancerBackendAddressPool 會檢索與負載平衡器相關聯的一個或多個後端位址集區。</span><span class="sxs-lookup"><span data-stu-id="5b064-103">Get-AzLoadBalancerBackendAddressPool retrieves one or more backend address pools associated with a load balancer.</span></span> 

## <span data-ttu-id="5b064-104">句法</span><span class="sxs-lookup"><span data-stu-id="5b064-104">SYNTAX</span></span>

### <span data-ttu-id="5b064-105">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b064-105">GetByNameParameterSet</span></span>
```
Get-AzLoadBalancerBackendAddressPool -ResourceGroupName <String> -LoadBalancerName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b064-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b064-106">GetByParentObjectParameterSet</span></span>
```
Get-AzLoadBalancerBackendAddressPool [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b064-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b064-107">GetByResourceIdParameterSet</span></span>
```
Get-AzLoadBalancerBackendAddressPool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5b064-108">說明</span><span class="sxs-lookup"><span data-stu-id="5b064-108">DESCRIPTION</span></span>
<span data-ttu-id="5b064-109">Get-AzLoadBalancerBackendAddressPool 會檢索與負載平衡器相關聯的一個或多個後端位址集區。</span><span class="sxs-lookup"><span data-stu-id="5b064-109">Get-AzLoadBalancerBackendAddressPool retrieves one or more backend address pools associated with a load balancer.</span></span>

## <span data-ttu-id="5b064-110">示例</span><span class="sxs-lookup"><span data-stu-id="5b064-110">EXAMPLES</span></span>

### <span data-ttu-id="5b064-111">範例1</span><span class="sxs-lookup"><span data-stu-id="5b064-111">Example 1</span></span>
```powershell
## Get single backend under loadbalancer
PS C:\> $lb = Get-AzLoadBalancer -ResourceGroupName $resourceGroup -Name $loadBalancerName
```

```powershell
## Get all backends under loadbalancer
PS C:\> $lb | Get-AzLoadBalancerBackendAddressPool
```
### <span data-ttu-id="5b064-112">範例2</span><span class="sxs-lookup"><span data-stu-id="5b064-112">Example 2</span></span>
```powershell
#Get specific backend from loadbalancer
PS C:\> $lb | Get-AzLoadBalancerBackendAddressPool -Name $backendPool1
```

### <span data-ttu-id="5b064-113">範例3</span><span class="sxs-lookup"><span data-stu-id="5b064-113">Example 3</span></span>
```powershell
#Get a backend by resource Id
PS C:\> Get-AzLoadBalancerBackendAddressPool -ResourceId $backendPool1.Id
```

## <span data-ttu-id="5b064-114">參數</span><span class="sxs-lookup"><span data-stu-id="5b064-114">PARAMETERS</span></span>

### <span data-ttu-id="5b064-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b064-115">-DefaultProfile</span></span>
<span data-ttu-id="5b064-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5b064-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b064-117">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5b064-117">-LoadBalancer</span></span>
<span data-ttu-id="5b064-118">{{Fill [填入 LoadBalancer] 描述}}</span><span class="sxs-lookup"><span data-stu-id="5b064-118">{{ Fill LoadBalancer Description }}</span></span>

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

### <span data-ttu-id="5b064-119">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="5b064-119">-LoadBalancerName</span></span>
<span data-ttu-id="5b064-120">負載平衡器的名稱。</span><span class="sxs-lookup"><span data-stu-id="5b064-120">The name of the load balancer.</span></span>

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

### <span data-ttu-id="5b064-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="5b064-121">-Name</span></span>
<span data-ttu-id="5b064-122">後端位址集區的名稱。</span><span class="sxs-lookup"><span data-stu-id="5b064-122">The name of the backend address pool.</span></span>

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

### <span data-ttu-id="5b064-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b064-123">-ResourceGroupName</span></span>
<span data-ttu-id="5b064-124">負載平衡器的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="5b064-124">The resource group name of the load balancer.</span></span>

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

### <span data-ttu-id="5b064-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5b064-125">-ResourceId</span></span>

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

### <span data-ttu-id="5b064-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b064-126">CommonParameters</span></span>
<span data-ttu-id="5b064-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5b064-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b064-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5b064-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b064-129">輸入</span><span class="sxs-lookup"><span data-stu-id="5b064-129">INPUTS</span></span>

### <span data-ttu-id="5b064-130">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="5b064-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="5b064-131">System.object</span><span class="sxs-lookup"><span data-stu-id="5b064-131">System.String</span></span>

## <span data-ttu-id="5b064-132">輸出</span><span class="sxs-lookup"><span data-stu-id="5b064-132">OUTPUTS</span></span>

### <span data-ttu-id="5b064-133">PSBackendAddressPool 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="5b064-133">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="5b064-134">筆記</span><span class="sxs-lookup"><span data-stu-id="5b064-134">NOTES</span></span>

## <span data-ttu-id="5b064-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="5b064-135">RELATED LINKS</span></span>