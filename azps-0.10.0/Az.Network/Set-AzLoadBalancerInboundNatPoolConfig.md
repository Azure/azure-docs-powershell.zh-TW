---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 355DF798-6233-45C6-9416-8AB0E0D7DC02
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: cf99aba02bc4dee18ec6cfd2bdaf9fd83036e6d8
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795420"
---
# <span data-ttu-id="eb0dd-101">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="eb0dd-101">Set-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="eb0dd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="eb0dd-102">SYNOPSIS</span></span>

## <span data-ttu-id="eb0dd-103">句法</span><span class="sxs-lookup"><span data-stu-id="eb0dd-103">SYNTAX</span></span>

### <span data-ttu-id="eb0dd-104">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="eb0dd-104">SetByResourceId</span></span>
```
Set-AzLoadBalancerInboundNatPoolConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="eb0dd-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="eb0dd-105">SetByResource</span></span>
```
Set-AzLoadBalancerInboundNatPoolConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="eb0dd-106">說明</span><span class="sxs-lookup"><span data-stu-id="eb0dd-106">DESCRIPTION</span></span>

## <span data-ttu-id="eb0dd-107">示例</span><span class="sxs-lookup"><span data-stu-id="eb0dd-107">EXAMPLES</span></span>

### <span data-ttu-id="eb0dd-108">sr-1</span><span class="sxs-lookup"><span data-stu-id="eb0dd-108">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="eb0dd-109">參數</span><span class="sxs-lookup"><span data-stu-id="eb0dd-109">PARAMETERS</span></span>

### <span data-ttu-id="eb0dd-110">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="eb0dd-110">-BackendPort</span></span>
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

### <span data-ttu-id="eb0dd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb0dd-111">-DefaultProfile</span></span>
<span data-ttu-id="eb0dd-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="eb0dd-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb0dd-113">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="eb0dd-113">-FrontendIpConfiguration</span></span>
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

### <span data-ttu-id="eb0dd-114">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="eb0dd-114">-FrontendIpConfigurationId</span></span>
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

### <span data-ttu-id="eb0dd-115">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="eb0dd-115">-FrontendPortRangeEnd</span></span>
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

### <span data-ttu-id="eb0dd-116">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="eb0dd-116">-FrontendPortRangeStart</span></span>
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

### <span data-ttu-id="eb0dd-117">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="eb0dd-117">-LoadBalancer</span></span>
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

### <span data-ttu-id="eb0dd-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="eb0dd-118">-Name</span></span>
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

### <span data-ttu-id="eb0dd-119">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="eb0dd-119">-Protocol</span></span>
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

### <span data-ttu-id="eb0dd-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb0dd-120">CommonParameters</span></span>
<span data-ttu-id="eb0dd-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="eb0dd-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb0dd-122">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="eb0dd-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb0dd-123">輸入</span><span class="sxs-lookup"><span data-stu-id="eb0dd-123">INPUTS</span></span>

### <span data-ttu-id="eb0dd-124">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="eb0dd-124">PSLoadBalancer</span></span>
<span data-ttu-id="eb0dd-125">形參 "LoadBalancer" 接受管線中 "PSLoadBalancer" 類型的值</span><span class="sxs-lookup"><span data-stu-id="eb0dd-125">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="eb0dd-126">輸出</span><span class="sxs-lookup"><span data-stu-id="eb0dd-126">OUTPUTS</span></span>

### <span data-ttu-id="eb0dd-127">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="eb0dd-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="eb0dd-128">筆記</span><span class="sxs-lookup"><span data-stu-id="eb0dd-128">NOTES</span></span>

## <span data-ttu-id="eb0dd-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="eb0dd-129">RELATED LINKS</span></span>

[<span data-ttu-id="eb0dd-130">附加 AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="eb0dd-130">Add-AzLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="eb0dd-131">AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="eb0dd-131">Get-AzLoadBalancerInboundNatPoolConfig</span></span>](./Get-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="eb0dd-132">新-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="eb0dd-132">New-AzLoadBalancerInboundNatPoolConfig</span></span>](./New-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="eb0dd-133">移除-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="eb0dd-133">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>](./Remove-AzLoadBalancerInboundNatPoolConfig.md)


