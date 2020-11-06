---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6BEED413-E2E4-4557-BD31-2A655E790C1D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 070680c1dc1c9fd091b311888867cda3f844ce4a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449048"
---
# <span data-ttu-id="e642c-101">Get-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="e642c-101">Get-AzureRmLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="e642c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e642c-102">SYNOPSIS</span></span>
<span data-ttu-id="e642c-103">在負載平衡器中取得前端 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="e642c-103">Gets a front-end IP configuration in a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e642c-104">句法</span><span class="sxs-lookup"><span data-stu-id="e642c-104">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e642c-105">說明</span><span class="sxs-lookup"><span data-stu-id="e642c-105">DESCRIPTION</span></span>
<span data-ttu-id="e642c-106">**AzureRmLoadBalancerFrontendIpConfig** Cmdlet 會取得前端 ip 設定或負載平衡器中的前端 ip 配置清單。</span><span class="sxs-lookup"><span data-stu-id="e642c-106">The **Get-AzureRmLoadBalancerFrontendIpConfig** cmdlet gets a front-end IP configuration or a list of front-end IP configurations in a load balancer.</span></span>

## <span data-ttu-id="e642c-107">示例</span><span class="sxs-lookup"><span data-stu-id="e642c-107">EXAMPLES</span></span>

### <span data-ttu-id="e642c-108">範例1：在負載平衡器中取得前端 IP 配置</span><span class="sxs-lookup"><span data-stu-id="e642c-108">Example 1: Get a front-end IP configuration in a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzureRmLoadBalancerFrontendIpConfig -Name "MyFrontEnd" -LoadBalancer $slb
```

<span data-ttu-id="e642c-109">第一個命令會取得名為 MyLoadBalancer 的負載平衡器，然後將它儲存在 $slb 的變數中。</span><span class="sxs-lookup"><span data-stu-id="e642c-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="e642c-110">第二個命令會取得與該負載平衡器相關聯的前端 IP 設定。</span><span class="sxs-lookup"><span data-stu-id="e642c-110">The second command gets the front end IP configuration associated with that load balancer.</span></span>

## <span data-ttu-id="e642c-111">參數</span><span class="sxs-lookup"><span data-stu-id="e642c-111">PARAMETERS</span></span>

### <span data-ttu-id="e642c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e642c-112">-DefaultProfile</span></span>
<span data-ttu-id="e642c-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e642c-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e642c-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e642c-114">-LoadBalancer</span></span>
<span data-ttu-id="e642c-115">指定與要取得的前端 IP 配置相關聯的負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="e642c-115">Specifies the load balancer that is associated with the front-end IP configuration to get.</span></span>

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

### <span data-ttu-id="e642c-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="e642c-116">-Name</span></span>
<span data-ttu-id="e642c-117">指定包含要取得的前端 IP 配置的負載平衡器名稱。</span><span class="sxs-lookup"><span data-stu-id="e642c-117">Specifies the name of the load balancer that contains the front-end IP configuration to get.</span></span>

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

### <span data-ttu-id="e642c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e642c-118">CommonParameters</span></span>
<span data-ttu-id="e642c-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e642c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e642c-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e642c-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e642c-121">輸入</span><span class="sxs-lookup"><span data-stu-id="e642c-121">INPUTS</span></span>

### <span data-ttu-id="e642c-122">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e642c-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="e642c-123">參數： LoadBalancer (ByValue) </span><span class="sxs-lookup"><span data-stu-id="e642c-123">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="e642c-124">輸出</span><span class="sxs-lookup"><span data-stu-id="e642c-124">OUTPUTS</span></span>

### <span data-ttu-id="e642c-125">PSFrontendIPConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e642c-125">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="e642c-126">筆記</span><span class="sxs-lookup"><span data-stu-id="e642c-126">NOTES</span></span>

## <span data-ttu-id="e642c-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="e642c-127">RELATED LINKS</span></span>

[<span data-ttu-id="e642c-128">附加 AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="e642c-128">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Add-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="e642c-129">AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e642c-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="e642c-130">新-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="e642c-130">New-AzureRmLoadBalancerFrontendIpConfig</span></span>](./New-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="e642c-131">移除-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="e642c-131">Remove-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Remove-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="e642c-132">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="e642c-132">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Set-AzureRmLoadBalancerFrontendIpConfig.md)


