---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2049CB74-E3CB-4294-B97C-B41E91209A1E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerprobeconfig
schema: 2.0.0
ms.openlocfilehash: f1d5ac87cc237e5a8ec92262255e996741346613
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93802318"
---
# <span data-ttu-id="e43dc-101">New-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e43dc-101">New-AzureRmLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="e43dc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e43dc-102">SYNOPSIS</span></span>
<span data-ttu-id="e43dc-103">為負載平衡器建立探測配置。</span><span class="sxs-lookup"><span data-stu-id="e43dc-103">Creates a probe configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e43dc-104">句法</span><span class="sxs-lookup"><span data-stu-id="e43dc-104">SYNTAX</span></span>

```
New-AzureRmLoadBalancerProbeConfig -Name <String> [-RequestPath <String>] [-Protocol <String>] -Port <Int32>
 -IntervalInSeconds <Int32> -ProbeCount <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e43dc-105">說明</span><span class="sxs-lookup"><span data-stu-id="e43dc-105">DESCRIPTION</span></span>
<span data-ttu-id="e43dc-106">**新的-AzureRmLoadBalancerProbeConfig** Cmdlet 會為 Azure 負載平衡器建立探測配置。</span><span class="sxs-lookup"><span data-stu-id="e43dc-106">The **New-AzureRmLoadBalancerProbeConfig** cmdlet creates a probe configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="e43dc-107">示例</span><span class="sxs-lookup"><span data-stu-id="e43dc-107">EXAMPLES</span></span>

### <span data-ttu-id="e43dc-108">範例1：建立探測器設定</span><span class="sxs-lookup"><span data-stu-id="e43dc-108">Example 1: Create a probe configuration</span></span>
```
PS C:\>New-AzureRmLoadBalancerProbeConfig -Name "MyProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 15
```

<span data-ttu-id="e43dc-109">這個命令會使用 HTTP 通訊協定，建立名為 MyProbe 的探測配置。</span><span class="sxs-lookup"><span data-stu-id="e43dc-109">This command creates a probe configuration named MyProbe using the HTTP protocol.</span></span>
<span data-ttu-id="e43dc-110">新的探測會連接到埠80上的負載平衡服務。</span><span class="sxs-lookup"><span data-stu-id="e43dc-110">The new probe will connect to a load-balanced service on port 80.</span></span>

## <span data-ttu-id="e43dc-111">參數</span><span class="sxs-lookup"><span data-stu-id="e43dc-111">PARAMETERS</span></span>

### <span data-ttu-id="e43dc-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e43dc-112">-DefaultProfile</span></span>
<span data-ttu-id="e43dc-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e43dc-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e43dc-114">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="e43dc-114">-IntervalInSeconds</span></span>
<span data-ttu-id="e43dc-115">指定探測到負載平衡服務每個實例之間的間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="e43dc-115">Specifies the interval, in seconds, between probes to each instance of a load-balanced service.</span></span>

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

### <span data-ttu-id="e43dc-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="e43dc-116">-Name</span></span>
<span data-ttu-id="e43dc-117">指定要建立的探針配置名稱。</span><span class="sxs-lookup"><span data-stu-id="e43dc-117">Specifies the name of the probe configuration to create.</span></span>

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

### <span data-ttu-id="e43dc-118">-埠</span><span class="sxs-lookup"><span data-stu-id="e43dc-118">-Port</span></span>
<span data-ttu-id="e43dc-119">指定新的探測器應該連線到負載平衡服務的埠。</span><span class="sxs-lookup"><span data-stu-id="e43dc-119">Specifies the port on which the new probe should connect to a load-balanced service.</span></span>

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

### <span data-ttu-id="e43dc-120">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="e43dc-120">-ProbeCount</span></span>
<span data-ttu-id="e43dc-121">指定實例被視為不健康的每個實例連續失敗數。</span><span class="sxs-lookup"><span data-stu-id="e43dc-121">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

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

### <span data-ttu-id="e43dc-122">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="e43dc-122">-Protocol</span></span>
<span data-ttu-id="e43dc-123">指定要用於探測設定的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="e43dc-123">Specifies the protocol to use for the probe configuration.</span></span>
<span data-ttu-id="e43dc-124">此參數可接受的值為： Tcp 或 Http。</span><span class="sxs-lookup"><span data-stu-id="e43dc-124">The acceptable values for this parameter are: Tcp or Http.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Http

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e43dc-125">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="e43dc-125">-RequestPath</span></span>
<span data-ttu-id="e43dc-126">在負載平衡服務中指定要探測以判斷健康情況的路徑。</span><span class="sxs-lookup"><span data-stu-id="e43dc-126">Specifies the path in a load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="e43dc-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e43dc-127">CommonParameters</span></span>
<span data-ttu-id="e43dc-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e43dc-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e43dc-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e43dc-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e43dc-130">輸入</span><span class="sxs-lookup"><span data-stu-id="e43dc-130">INPUTS</span></span>

## <span data-ttu-id="e43dc-131">輸出</span><span class="sxs-lookup"><span data-stu-id="e43dc-131">OUTPUTS</span></span>

### <span data-ttu-id="e43dc-132">PSProbe 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e43dc-132">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="e43dc-133">筆記</span><span class="sxs-lookup"><span data-stu-id="e43dc-133">NOTES</span></span>

## <span data-ttu-id="e43dc-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="e43dc-134">RELATED LINKS</span></span>

[<span data-ttu-id="e43dc-135">附加 AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e43dc-135">Add-AzureRmLoadBalancerProbeConfig</span></span>](./Add-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="e43dc-136">AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e43dc-136">Get-AzureRmLoadBalancerProbeConfig</span></span>](./Get-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="e43dc-137">移除-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e43dc-137">Remove-AzureRmLoadBalancerProbeConfig</span></span>](./Remove-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="e43dc-138">Set-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e43dc-138">Set-AzureRmLoadBalancerProbeConfig</span></span>](./Set-AzureRmLoadBalancerProbeConfig.md)


