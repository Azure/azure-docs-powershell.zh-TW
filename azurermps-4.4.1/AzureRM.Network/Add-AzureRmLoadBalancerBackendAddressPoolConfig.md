---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9EB11283-0189-4333-8142-DCC3F770F91A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: ef5071ff0127c34d9ae8c41ea12e2465e83c98d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624805"
---
# <span data-ttu-id="dab90-101">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="dab90-101">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="dab90-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dab90-102">SYNOPSIS</span></span>
<span data-ttu-id="dab90-103">將後端位址集區配置新增到負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="dab90-103">Adds a backend address pool configuration to a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dab90-104">句法</span><span class="sxs-lookup"><span data-stu-id="dab90-104">SYNTAX</span></span>

```
Add-AzureRmLoadBalancerBackendAddressPoolConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dab90-105">說明</span><span class="sxs-lookup"><span data-stu-id="dab90-105">DESCRIPTION</span></span>
<span data-ttu-id="dab90-106">**AzureRmLoadBalancerBackend** Cmdlet 會將後端位址集區新增至 Azure 負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="dab90-106">The **Add-AzureRmLoadBalancerBackend** cmdlet adds a backend address pool to an Azure load balancer.</span></span>

## <span data-ttu-id="dab90-107">示例</span><span class="sxs-lookup"><span data-stu-id="dab90-107">EXAMPLES</span></span>

### <span data-ttu-id="dab90-108">範例1將後端位址集區設定新增到負載平衡器</span><span class="sxs-lookup"><span data-stu-id="dab90-108">Example 1 Add a backend address pool configuration to a load balancer</span></span>
```
PS C:\>Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "myrg" | Add-AzureRmLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzureRmLoadBalancer
```

<span data-ttu-id="dab90-109">這個命令會取得名為 MyLoadBalancer 的負載平衡器，將名為 BackendAddressPool02 的後端位址集區新增至 MyLoadBalancer，然後使用 **Set-AzureRmLoadBalancer** Cmdlet 來更新 MyLoadBalancer。</span><span class="sxs-lookup"><span data-stu-id="dab90-109">This command gets the load balancer named MyLoadBalancer, adds the backend address pool named BackendAddressPool02 to MyLoadBalancer, and then uses the **Set-AzureRmLoadBalancer** cmdlet to update MyLoadBalancer.</span></span>

## <span data-ttu-id="dab90-110">參數</span><span class="sxs-lookup"><span data-stu-id="dab90-110">PARAMETERS</span></span>

### <span data-ttu-id="dab90-111">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="dab90-111">-LoadBalancer</span></span>
<span data-ttu-id="dab90-112">指定 **LoadBalancer** 物件。</span><span class="sxs-lookup"><span data-stu-id="dab90-112">Specifies a **LoadBalancer** object.</span></span>

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

### <span data-ttu-id="dab90-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="dab90-113">-Name</span></span>
<span data-ttu-id="dab90-114">指定要新增的後端位址集區配置名稱。</span><span class="sxs-lookup"><span data-stu-id="dab90-114">Specifies the name of the backend address pool configuration to add.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dab90-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dab90-115">-DefaultProfile</span></span>
<span data-ttu-id="dab90-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dab90-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dab90-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dab90-117">CommonParameters</span></span>
<span data-ttu-id="dab90-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dab90-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dab90-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="dab90-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dab90-120">輸入</span><span class="sxs-lookup"><span data-stu-id="dab90-120">INPUTS</span></span>

### <span data-ttu-id="dab90-121">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="dab90-121">PSLoadBalancer</span></span>
<span data-ttu-id="dab90-122">形參 "LoadBalancer" 接受管線中 "PSLoadBalancer" 類型的值</span><span class="sxs-lookup"><span data-stu-id="dab90-122">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="dab90-123">輸出</span><span class="sxs-lookup"><span data-stu-id="dab90-123">OUTPUTS</span></span>

### <span data-ttu-id="dab90-124">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="dab90-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="dab90-125">筆記</span><span class="sxs-lookup"><span data-stu-id="dab90-125">NOTES</span></span>

## <span data-ttu-id="dab90-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="dab90-126">RELATED LINKS</span></span>

[<span data-ttu-id="dab90-127">AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="dab90-127">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="dab90-128">AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="dab90-128">Get-AzureRmNetworkInterface</span></span>](./Get-AzureRmNetworkInterface.md)

[<span data-ttu-id="dab90-129">AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="dab90-129">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="dab90-130">新-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="dab90-130">New-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="dab90-131">移除-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="dab90-131">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzureRmLoadBalancerBackendAddressPoolConfig.md)


