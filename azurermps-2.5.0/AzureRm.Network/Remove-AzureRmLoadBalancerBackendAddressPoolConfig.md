---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F965A9DE-645C-471B-84E8-58D648B1CA57
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerbackendaddresspoolconfig
schema: 2.0.0
ms.openlocfilehash: 9bbfa0aec2da00ada25fc4bb8a5334f67e80e41a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93802301"
---
# <span data-ttu-id="bd8f2-101">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="bd8f2-101">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="bd8f2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bd8f2-102">SYNOPSIS</span></span>
<span data-ttu-id="bd8f2-103">從負載平衡器移除後端位址集區配置。</span><span class="sxs-lookup"><span data-stu-id="bd8f2-103">Removes a backend address pool configuration from a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bd8f2-104">句法</span><span class="sxs-lookup"><span data-stu-id="bd8f2-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerBackendAddressPoolConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd8f2-105">說明</span><span class="sxs-lookup"><span data-stu-id="bd8f2-105">DESCRIPTION</span></span>
<span data-ttu-id="bd8f2-106">**AzureRmLoadBalancerBackendAddressPoolConfig** Cmdlet 會從負載平衡器中移除後端位址集區。</span><span class="sxs-lookup"><span data-stu-id="bd8f2-106">The **Remove-AzureRmLoadBalancerBackendAddressPoolConfig** cmdlet removes a backend address pool from a load balancer.</span></span>

## <span data-ttu-id="bd8f2-107">示例</span><span class="sxs-lookup"><span data-stu-id="bd8f2-107">EXAMPLES</span></span>

### <span data-ttu-id="bd8f2-108">範例1：從負載平衡器移除後端位址集區設定</span><span class="sxs-lookup"><span data-stu-id="bd8f2-108">Example 1: Remove a backend address pool configuration from a load balancer</span></span>
```
PS C:\>Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" | Remove-AzureRmLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzureRmLoadBalancer
```

<span data-ttu-id="bd8f2-109">這個命令會取得名為 MyLoadBalancer 的負載平衡器，並將它傳遞給 **Remove-AzureRmLoadBalancerBackendAddressPoolConfig** ，這會從 MyLoadBalancer 中移除 BackendAddressPool02 設定。</span><span class="sxs-lookup"><span data-stu-id="bd8f2-109">This command gets the load balancer named MyLoadBalancer and passes it to **Remove-AzureRmLoadBalancerBackendAddressPoolConfig** , which removes the BackendAddressPool02 configuration from MyLoadBalancer.</span></span>
<span data-ttu-id="bd8f2-110">最後，Set-AzureRmLoadBalancer Cmdlet 更新 MyLoadBalancer。</span><span class="sxs-lookup"><span data-stu-id="bd8f2-110">Finally, the Set-AzureRmLoadBalancer cmdlet updates MyLoadBalancer.</span></span>
<span data-ttu-id="bd8f2-111">請注意，後端位址集區配置必須存在，才能刪除。</span><span class="sxs-lookup"><span data-stu-id="bd8f2-111">Note that a backend address pool configuration must exist before you can delete it.</span></span>

## <span data-ttu-id="bd8f2-112">參數</span><span class="sxs-lookup"><span data-stu-id="bd8f2-112">PARAMETERS</span></span>

### <span data-ttu-id="bd8f2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd8f2-113">-DefaultProfile</span></span>
<span data-ttu-id="bd8f2-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bd8f2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd8f2-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="bd8f2-115">-LoadBalancer</span></span>
<span data-ttu-id="bd8f2-116">指定包含要移除之後端位址集區的負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="bd8f2-116">Specifies the load balancer that contains the backend address pool to remove.</span></span>

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

### <span data-ttu-id="bd8f2-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="bd8f2-117">-Name</span></span>
<span data-ttu-id="bd8f2-118">指定此 Cmdlet 移除之後端位址集區的名稱。</span><span class="sxs-lookup"><span data-stu-id="bd8f2-118">Specifies the name of the backend address pool that this cmdlet removes.</span></span>

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

### <span data-ttu-id="bd8f2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd8f2-119">CommonParameters</span></span>
<span data-ttu-id="bd8f2-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bd8f2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd8f2-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bd8f2-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd8f2-122">輸入</span><span class="sxs-lookup"><span data-stu-id="bd8f2-122">INPUTS</span></span>

### <span data-ttu-id="bd8f2-123">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="bd8f2-123">PSLoadBalancer</span></span>
<span data-ttu-id="bd8f2-124">形參 "LoadBalancer" 接受管線中 "PSLoadBalancer" 類型的值</span><span class="sxs-lookup"><span data-stu-id="bd8f2-124">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="bd8f2-125">輸出</span><span class="sxs-lookup"><span data-stu-id="bd8f2-125">OUTPUTS</span></span>

### <span data-ttu-id="bd8f2-126">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="bd8f2-126">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="bd8f2-127">筆記</span><span class="sxs-lookup"><span data-stu-id="bd8f2-127">NOTES</span></span>

## <span data-ttu-id="bd8f2-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="bd8f2-128">RELATED LINKS</span></span>

[<span data-ttu-id="bd8f2-129">附加 AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="bd8f2-129">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="bd8f2-130">AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="bd8f2-130">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="bd8f2-131">AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="bd8f2-131">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="bd8f2-132">新-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="bd8f2-132">New-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzureRmLoadBalancerBackendAddressPoolConfig.md)


