---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EB4DF001-AD05-4747-972B-5E4194A404C8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermloadbalancerinboundnatpoolconfig
schema: 2.0.0
ms.openlocfilehash: b53b6ed8ba5b4a79ee1913040ef58e236c22c44d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93802458"
---
# <span data-ttu-id="0bb90-101">Add-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="0bb90-101">Add-AzureRmLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="0bb90-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0bb90-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0bb90-103">句法</span><span class="sxs-lookup"><span data-stu-id="0bb90-103">SYNTAX</span></span>

### <span data-ttu-id="0bb90-104">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="0bb90-104">SetByResourceId</span></span>
```
Add-AzureRmLoadBalancerInboundNatPoolConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0bb90-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="0bb90-105">SetByResource</span></span>
```
Add-AzureRmLoadBalancerInboundNatPoolConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0bb90-106">說明</span><span class="sxs-lookup"><span data-stu-id="0bb90-106">DESCRIPTION</span></span>

## <span data-ttu-id="0bb90-107">示例</span><span class="sxs-lookup"><span data-stu-id="0bb90-107">EXAMPLES</span></span>

### <span data-ttu-id="0bb90-108">sr-1</span><span class="sxs-lookup"><span data-stu-id="0bb90-108">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="0bb90-109">參數</span><span class="sxs-lookup"><span data-stu-id="0bb90-109">PARAMETERS</span></span>

### <span data-ttu-id="0bb90-110">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="0bb90-110">-BackendPort</span></span>
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

### <span data-ttu-id="0bb90-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bb90-111">-DefaultProfile</span></span>
<span data-ttu-id="0bb90-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0bb90-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0bb90-113">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="0bb90-113">-FrontendIpConfiguration</span></span>
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

### <span data-ttu-id="0bb90-114">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="0bb90-114">-FrontendIpConfigurationId</span></span>
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

### <span data-ttu-id="0bb90-115">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="0bb90-115">-FrontendPortRangeEnd</span></span>
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

### <span data-ttu-id="0bb90-116">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="0bb90-116">-FrontendPortRangeStart</span></span>
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

### <span data-ttu-id="0bb90-117">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0bb90-117">-LoadBalancer</span></span>
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

### <span data-ttu-id="0bb90-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="0bb90-118">-Name</span></span>
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

### <span data-ttu-id="0bb90-119">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="0bb90-119">-Protocol</span></span>
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

### <span data-ttu-id="0bb90-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bb90-120">CommonParameters</span></span>
<span data-ttu-id="0bb90-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0bb90-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bb90-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0bb90-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bb90-123">輸入</span><span class="sxs-lookup"><span data-stu-id="0bb90-123">INPUTS</span></span>

### <span data-ttu-id="0bb90-124">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0bb90-124">PSLoadBalancer</span></span>
<span data-ttu-id="0bb90-125">形參 "LoadBalancer" 接受管線中 "PSLoadBalancer" 類型的值</span><span class="sxs-lookup"><span data-stu-id="0bb90-125">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="0bb90-126">輸出</span><span class="sxs-lookup"><span data-stu-id="0bb90-126">OUTPUTS</span></span>

### <span data-ttu-id="0bb90-127">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="0bb90-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="0bb90-128">筆記</span><span class="sxs-lookup"><span data-stu-id="0bb90-128">NOTES</span></span>

## <span data-ttu-id="0bb90-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="0bb90-129">RELATED LINKS</span></span>

