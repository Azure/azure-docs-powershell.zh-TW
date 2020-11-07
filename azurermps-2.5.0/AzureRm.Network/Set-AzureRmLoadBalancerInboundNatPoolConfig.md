---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 355DF798-6233-45C6-9416-8AB0E0D7DC02
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermloadbalancerinboundnatpoolconfig
schema: 2.0.0
ms.openlocfilehash: 6f4981469bf9468de7fd05ec79b1d3d2b28daa93
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801981"
---
# <span data-ttu-id="563ad-101">Set-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="563ad-101">Set-AzureRmLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="563ad-102">摘要</span><span class="sxs-lookup"><span data-stu-id="563ad-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="563ad-103">句法</span><span class="sxs-lookup"><span data-stu-id="563ad-103">SYNTAX</span></span>

### <span data-ttu-id="563ad-104">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="563ad-104">SetByResourceId</span></span>
```
Set-AzureRmLoadBalancerInboundNatPoolConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="563ad-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="563ad-105">SetByResource</span></span>
```
Set-AzureRmLoadBalancerInboundNatPoolConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="563ad-106">說明</span><span class="sxs-lookup"><span data-stu-id="563ad-106">DESCRIPTION</span></span>

## <span data-ttu-id="563ad-107">示例</span><span class="sxs-lookup"><span data-stu-id="563ad-107">EXAMPLES</span></span>

### <span data-ttu-id="563ad-108">sr-1</span><span class="sxs-lookup"><span data-stu-id="563ad-108">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="563ad-109">參數</span><span class="sxs-lookup"><span data-stu-id="563ad-109">PARAMETERS</span></span>

### <span data-ttu-id="563ad-110">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="563ad-110">-BackendPort</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="563ad-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="563ad-111">-DefaultProfile</span></span>
<span data-ttu-id="563ad-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="563ad-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="563ad-113">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="563ad-113">-FrontendIpConfiguration</span></span>
```yaml
Type: PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="563ad-114">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="563ad-114">-FrontendIpConfigurationId</span></span>
```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="563ad-115">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="563ad-115">-FrontendPortRangeEnd</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="563ad-116">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="563ad-116">-FrontendPortRangeStart</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="563ad-117">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="563ad-117">-LoadBalancer</span></span>
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

### <span data-ttu-id="563ad-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="563ad-118">-Name</span></span>
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

### <span data-ttu-id="563ad-119">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="563ad-119">-Protocol</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Udp

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="563ad-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="563ad-120">CommonParameters</span></span>
<span data-ttu-id="563ad-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="563ad-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="563ad-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="563ad-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="563ad-123">輸入</span><span class="sxs-lookup"><span data-stu-id="563ad-123">INPUTS</span></span>

### <span data-ttu-id="563ad-124">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="563ad-124">PSLoadBalancer</span></span>
<span data-ttu-id="563ad-125">形參 "LoadBalancer" 接受管線中 "PSLoadBalancer" 類型的值</span><span class="sxs-lookup"><span data-stu-id="563ad-125">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="563ad-126">輸出</span><span class="sxs-lookup"><span data-stu-id="563ad-126">OUTPUTS</span></span>

### <span data-ttu-id="563ad-127">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="563ad-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="563ad-128">筆記</span><span class="sxs-lookup"><span data-stu-id="563ad-128">NOTES</span></span>

## <span data-ttu-id="563ad-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="563ad-129">RELATED LINKS</span></span>

[<span data-ttu-id="563ad-130">附加 AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="563ad-130">Add-AzureRmLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzureRmLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="563ad-131">AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="563ad-131">Get-AzureRmLoadBalancerInboundNatPoolConfig</span></span>](./Get-AzureRmLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="563ad-132">新-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="563ad-132">New-AzureRmLoadBalancerInboundNatPoolConfig</span></span>](./New-AzureRmLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="563ad-133">移除-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="563ad-133">Remove-AzureRmLoadBalancerInboundNatPoolConfig</span></span>](./Remove-AzureRmLoadBalancerInboundNatPoolConfig.md)


