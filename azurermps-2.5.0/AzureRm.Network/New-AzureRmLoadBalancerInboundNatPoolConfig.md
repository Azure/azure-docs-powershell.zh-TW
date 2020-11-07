---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 61C34433-A16A-4ACF-A318-1C7D9E49579F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerinboundnatpoolconfig
schema: 2.0.0
ms.openlocfilehash: 247470ee878a37968cd690d27f8e5e16047febbd
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800778"
---
# <span data-ttu-id="50f57-101">New-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="50f57-101">New-AzureRmLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="50f57-102">摘要</span><span class="sxs-lookup"><span data-stu-id="50f57-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50f57-103">句法</span><span class="sxs-lookup"><span data-stu-id="50f57-103">SYNTAX</span></span>

### <span data-ttu-id="50f57-104">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="50f57-104">SetByResourceId</span></span>
```
New-AzureRmLoadBalancerInboundNatPoolConfig -Name <String> [-FrontendIpConfigurationId <String>]
 -Protocol <String> -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="50f57-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="50f57-105">SetByResource</span></span>
```
New-AzureRmLoadBalancerInboundNatPoolConfig -Name <String>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="50f57-106">說明</span><span class="sxs-lookup"><span data-stu-id="50f57-106">DESCRIPTION</span></span>

## <span data-ttu-id="50f57-107">示例</span><span class="sxs-lookup"><span data-stu-id="50f57-107">EXAMPLES</span></span>

### <span data-ttu-id="50f57-108">sr-1</span><span class="sxs-lookup"><span data-stu-id="50f57-108">1:</span></span>
```

```

## <span data-ttu-id="50f57-109">參數</span><span class="sxs-lookup"><span data-stu-id="50f57-109">PARAMETERS</span></span>

### <span data-ttu-id="50f57-110">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="50f57-110">-BackendPort</span></span>
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

### <span data-ttu-id="50f57-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50f57-111">-DefaultProfile</span></span>
<span data-ttu-id="50f57-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="50f57-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50f57-113">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="50f57-113">-FrontendIpConfiguration</span></span>
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

### <span data-ttu-id="50f57-114">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="50f57-114">-FrontendIpConfigurationId</span></span>
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

### <span data-ttu-id="50f57-115">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="50f57-115">-FrontendPortRangeEnd</span></span>
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

### <span data-ttu-id="50f57-116">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="50f57-116">-FrontendPortRangeStart</span></span>
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

### <span data-ttu-id="50f57-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="50f57-117">-Name</span></span>
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

### <span data-ttu-id="50f57-118">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="50f57-118">-Protocol</span></span>
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

### <span data-ttu-id="50f57-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50f57-119">CommonParameters</span></span>
<span data-ttu-id="50f57-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="50f57-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50f57-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="50f57-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50f57-122">輸入</span><span class="sxs-lookup"><span data-stu-id="50f57-122">INPUTS</span></span>

## <span data-ttu-id="50f57-123">輸出</span><span class="sxs-lookup"><span data-stu-id="50f57-123">OUTPUTS</span></span>

### <span data-ttu-id="50f57-124">PSInboundNatPool 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="50f57-124">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="50f57-125">筆記</span><span class="sxs-lookup"><span data-stu-id="50f57-125">NOTES</span></span>

## <span data-ttu-id="50f57-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="50f57-126">RELATED LINKS</span></span>

