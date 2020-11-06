---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9EB11283-0189-4333-8142-DCC3F770F91A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 82775229bc368f80c03a886b10a631a4482341df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449306"
---
# <span data-ttu-id="25e1a-101">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="25e1a-101">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="25e1a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="25e1a-102">SYNOPSIS</span></span>
<span data-ttu-id="25e1a-103">將後端位址集區配置新增到負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="25e1a-103">Adds a backend address pool configuration to a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25e1a-104">句法</span><span class="sxs-lookup"><span data-stu-id="25e1a-104">SYNTAX</span></span>

```
Add-AzureRmLoadBalancerBackendAddressPoolConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25e1a-105">說明</span><span class="sxs-lookup"><span data-stu-id="25e1a-105">DESCRIPTION</span></span>
<span data-ttu-id="25e1a-106">**AzureRmLoadBalancerBackend** Cmdlet 會將後端位址集區新增至 Azure 負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="25e1a-106">The **Add-AzureRmLoadBalancerBackend** cmdlet adds a backend address pool to an Azure load balancer.</span></span>

## <span data-ttu-id="25e1a-107">示例</span><span class="sxs-lookup"><span data-stu-id="25e1a-107">EXAMPLES</span></span>

### <span data-ttu-id="25e1a-108">範例1將後端位址集區設定新增到負載平衡器</span><span class="sxs-lookup"><span data-stu-id="25e1a-108">Example 1 Add a backend address pool configuration to a load balancer</span></span>
```
PS C:\>Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "myrg" | Add-AzureRmLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzureRmLoadBalancer
```

<span data-ttu-id="25e1a-109">這個命令會取得名為 MyLoadBalancer 的負載平衡器，將名為 BackendAddressPool02 的後端位址集區新增至 MyLoadBalancer，然後使用 **Set-AzureRmLoadBalancer** Cmdlet 來更新 MyLoadBalancer。</span><span class="sxs-lookup"><span data-stu-id="25e1a-109">This command gets the load balancer named MyLoadBalancer, adds the backend address pool named BackendAddressPool02 to MyLoadBalancer, and then uses the **Set-AzureRmLoadBalancer** cmdlet to update MyLoadBalancer.</span></span>

## <span data-ttu-id="25e1a-110">參數</span><span class="sxs-lookup"><span data-stu-id="25e1a-110">PARAMETERS</span></span>

### <span data-ttu-id="25e1a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25e1a-111">-DefaultProfile</span></span>
<span data-ttu-id="25e1a-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="25e1a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25e1a-113">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="25e1a-113">-LoadBalancer</span></span>
<span data-ttu-id="25e1a-114">指定 **LoadBalancer** 物件。</span><span class="sxs-lookup"><span data-stu-id="25e1a-114">Specifies a **LoadBalancer** object.</span></span>

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

### <span data-ttu-id="25e1a-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="25e1a-115">-Name</span></span>
<span data-ttu-id="25e1a-116">指定要新增的後端位址集區配置名稱。</span><span class="sxs-lookup"><span data-stu-id="25e1a-116">Specifies the name of the backend address pool configuration to add.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25e1a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25e1a-117">CommonParameters</span></span>
<span data-ttu-id="25e1a-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="25e1a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25e1a-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="25e1a-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25e1a-120">輸入</span><span class="sxs-lookup"><span data-stu-id="25e1a-120">INPUTS</span></span>

### <span data-ttu-id="25e1a-121">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="25e1a-121">PSLoadBalancer</span></span>
<span data-ttu-id="25e1a-122">形參 "LoadBalancer" 接受管線中 "PSLoadBalancer" 類型的值</span><span class="sxs-lookup"><span data-stu-id="25e1a-122">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="25e1a-123">輸出</span><span class="sxs-lookup"><span data-stu-id="25e1a-123">OUTPUTS</span></span>

### <span data-ttu-id="25e1a-124">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="25e1a-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="25e1a-125">筆記</span><span class="sxs-lookup"><span data-stu-id="25e1a-125">NOTES</span></span>

## <span data-ttu-id="25e1a-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="25e1a-126">RELATED LINKS</span></span>

[<span data-ttu-id="25e1a-127">AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="25e1a-127">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="25e1a-128">AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="25e1a-128">Get-AzureRmNetworkInterface</span></span>](./Get-AzureRmNetworkInterface.md)

[<span data-ttu-id="25e1a-129">AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="25e1a-129">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="25e1a-130">新-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="25e1a-130">New-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="25e1a-131">移除-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="25e1a-131">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzureRmLoadBalancerBackendAddressPoolConfig.md)


