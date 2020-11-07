---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2049CB74-E3CB-4294-B97C-B41E91209A1E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerProbeConfig.md
ms.openlocfilehash: 57c0d491d5e330f45550381b099e20e5d02fd8f7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625134"
---
# <span data-ttu-id="3bd3a-101">New-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="3bd3a-101">New-AzureRmLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="3bd3a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3bd3a-102">SYNOPSIS</span></span>
<span data-ttu-id="3bd3a-103">為負載平衡器建立探測配置。</span><span class="sxs-lookup"><span data-stu-id="3bd3a-103">Creates a probe configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3bd3a-104">句法</span><span class="sxs-lookup"><span data-stu-id="3bd3a-104">SYNTAX</span></span>

```
New-AzureRmLoadBalancerProbeConfig -Name <String> [-RequestPath <String>] [-Protocol <String>] -Port <Int32>
 -IntervalInSeconds <Int32> -ProbeCount <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3bd3a-105">說明</span><span class="sxs-lookup"><span data-stu-id="3bd3a-105">DESCRIPTION</span></span>
<span data-ttu-id="3bd3a-106">**新的-AzureRmLoadBalancerProbeConfig** Cmdlet 會為 Azure 負載平衡器建立探測配置。</span><span class="sxs-lookup"><span data-stu-id="3bd3a-106">The **New-AzureRmLoadBalancerProbeConfig** cmdlet creates a probe configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="3bd3a-107">示例</span><span class="sxs-lookup"><span data-stu-id="3bd3a-107">EXAMPLES</span></span>

### <span data-ttu-id="3bd3a-108">範例1：建立探測器設定</span><span class="sxs-lookup"><span data-stu-id="3bd3a-108">Example 1: Create a probe configuration</span></span>
```
PS C:\>New-AzureRmLoadBalancerProbeConfig -Name "MyProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 15
```

<span data-ttu-id="3bd3a-109">這個命令會使用 HTTP 通訊協定，建立名為 MyProbe 的探測配置。</span><span class="sxs-lookup"><span data-stu-id="3bd3a-109">This command creates a probe configuration named MyProbe using the HTTP protocol.</span></span>
<span data-ttu-id="3bd3a-110">新的探測會連接到埠80上的負載平衡服務。</span><span class="sxs-lookup"><span data-stu-id="3bd3a-110">The new probe will connect to a load-balanced service on port 80.</span></span>

## <span data-ttu-id="3bd3a-111">參數</span><span class="sxs-lookup"><span data-stu-id="3bd3a-111">PARAMETERS</span></span>

### <span data-ttu-id="3bd3a-112">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="3bd3a-112">-IntervalInSeconds</span></span>
<span data-ttu-id="3bd3a-113">指定探測到負載平衡服務每個實例之間的間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="3bd3a-113">Specifies the interval, in seconds, between probes to each instance of a load-balanced service.</span></span>

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

### <span data-ttu-id="3bd3a-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="3bd3a-114">-Name</span></span>
<span data-ttu-id="3bd3a-115">指定要建立的探針配置名稱。</span><span class="sxs-lookup"><span data-stu-id="3bd3a-115">Specifies the name of the probe configuration to create.</span></span>

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

### <span data-ttu-id="3bd3a-116">-埠</span><span class="sxs-lookup"><span data-stu-id="3bd3a-116">-Port</span></span>
<span data-ttu-id="3bd3a-117">指定新的探測器應該連線到負載平衡服務的埠。</span><span class="sxs-lookup"><span data-stu-id="3bd3a-117">Specifies the port on which the new probe should connect to a load-balanced service.</span></span>

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

### <span data-ttu-id="3bd3a-118">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="3bd3a-118">-ProbeCount</span></span>
<span data-ttu-id="3bd3a-119">指定實例被視為不健康的每個實例連續失敗數。</span><span class="sxs-lookup"><span data-stu-id="3bd3a-119">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

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

### <span data-ttu-id="3bd3a-120">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="3bd3a-120">-Protocol</span></span>
<span data-ttu-id="3bd3a-121">指定要用於探測設定的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="3bd3a-121">Specifies the protocol to use for the probe configuration.</span></span>
<span data-ttu-id="3bd3a-122">此參數可接受的值為： Tcp 或 Http。</span><span class="sxs-lookup"><span data-stu-id="3bd3a-122">The acceptable values for this parameter are: Tcp or Http.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Http

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bd3a-123">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="3bd3a-123">-RequestPath</span></span>
<span data-ttu-id="3bd3a-124">在負載平衡服務中指定要探測以判斷健康情況的路徑。</span><span class="sxs-lookup"><span data-stu-id="3bd3a-124">Specifies the path in a load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="3bd3a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bd3a-125">-DefaultProfile</span></span>
<span data-ttu-id="3bd3a-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3bd3a-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3bd3a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bd3a-127">CommonParameters</span></span>
<span data-ttu-id="3bd3a-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3bd3a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bd3a-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3bd3a-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bd3a-130">輸入</span><span class="sxs-lookup"><span data-stu-id="3bd3a-130">INPUTS</span></span>

## <span data-ttu-id="3bd3a-131">輸出</span><span class="sxs-lookup"><span data-stu-id="3bd3a-131">OUTPUTS</span></span>

### <span data-ttu-id="3bd3a-132">PSProbe 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="3bd3a-132">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="3bd3a-133">筆記</span><span class="sxs-lookup"><span data-stu-id="3bd3a-133">NOTES</span></span>

## <span data-ttu-id="3bd3a-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="3bd3a-134">RELATED LINKS</span></span>

[<span data-ttu-id="3bd3a-135">附加 AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="3bd3a-135">Add-AzureRmLoadBalancerProbeConfig</span></span>](./Add-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="3bd3a-136">AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="3bd3a-136">Get-AzureRmLoadBalancerProbeConfig</span></span>](./Get-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="3bd3a-137">移除-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="3bd3a-137">Remove-AzureRmLoadBalancerProbeConfig</span></span>](./Remove-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="3bd3a-138">Set-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="3bd3a-138">Set-AzureRmLoadBalancerProbeConfig</span></span>](./Set-AzureRmLoadBalancerProbeConfig.md)


