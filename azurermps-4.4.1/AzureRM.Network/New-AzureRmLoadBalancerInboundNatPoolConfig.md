---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 61C34433-A16A-4ACF-A318-1C7D9E49579F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 85d58154d8dd1d93e37a55b9fd0b9d306283b899
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455695"
---
# <span data-ttu-id="ca2f5-101">New-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="ca2f5-101">New-AzureRmLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="ca2f5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ca2f5-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ca2f5-103">句法</span><span class="sxs-lookup"><span data-stu-id="ca2f5-103">SYNTAX</span></span>

### <span data-ttu-id="ca2f5-104">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="ca2f5-104">SetByResourceId</span></span>
```
New-AzureRmLoadBalancerInboundNatPoolConfig -Name <String> [-FrontendIpConfigurationId <String>]
 -Protocol <String> -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ca2f5-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="ca2f5-105">SetByResource</span></span>
```
New-AzureRmLoadBalancerInboundNatPoolConfig -Name <String>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ca2f5-106">說明</span><span class="sxs-lookup"><span data-stu-id="ca2f5-106">DESCRIPTION</span></span>

## <span data-ttu-id="ca2f5-107">示例</span><span class="sxs-lookup"><span data-stu-id="ca2f5-107">EXAMPLES</span></span>

## <span data-ttu-id="ca2f5-108">參數</span><span class="sxs-lookup"><span data-stu-id="ca2f5-108">PARAMETERS</span></span>

### <span data-ttu-id="ca2f5-109">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="ca2f5-109">-BackendPort</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca2f5-110">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="ca2f5-110">-FrontendIpConfiguration</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca2f5-111">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="ca2f5-111">-FrontendIpConfigurationId</span></span>
```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca2f5-112">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="ca2f5-112">-FrontendPortRangeEnd</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca2f5-113">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="ca2f5-113">-FrontendPortRangeStart</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca2f5-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="ca2f5-114">-Name</span></span>
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

### <span data-ttu-id="ca2f5-115">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="ca2f5-115">-Protocol</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Udp

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca2f5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca2f5-116">-DefaultProfile</span></span>
<span data-ttu-id="ca2f5-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ca2f5-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ca2f5-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca2f5-118">CommonParameters</span></span>
<span data-ttu-id="ca2f5-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ca2f5-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca2f5-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ca2f5-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca2f5-121">輸入</span><span class="sxs-lookup"><span data-stu-id="ca2f5-121">INPUTS</span></span>

## <span data-ttu-id="ca2f5-122">輸出</span><span class="sxs-lookup"><span data-stu-id="ca2f5-122">OUTPUTS</span></span>

### <span data-ttu-id="ca2f5-123">PSInboundNatPool 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ca2f5-123">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="ca2f5-124">筆記</span><span class="sxs-lookup"><span data-stu-id="ca2f5-124">NOTES</span></span>

## <span data-ttu-id="ca2f5-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="ca2f5-125">RELATED LINKS</span></span>

