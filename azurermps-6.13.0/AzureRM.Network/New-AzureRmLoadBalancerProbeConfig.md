---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2049CB74-E3CB-4294-B97C-B41E91209A1E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerProbeConfig.md
ms.openlocfilehash: 8a4889190e58edd896d1a93222a35688dd5884c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449031"
---
# <span data-ttu-id="a2933-101">New-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a2933-101">New-AzureRmLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="a2933-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a2933-102">SYNOPSIS</span></span>
<span data-ttu-id="a2933-103">為負載平衡器建立探測配置。</span><span class="sxs-lookup"><span data-stu-id="a2933-103">Creates a probe configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a2933-104">句法</span><span class="sxs-lookup"><span data-stu-id="a2933-104">SYNTAX</span></span>

```
New-AzureRmLoadBalancerProbeConfig -Name <String> [-Protocol <String>] -Port <Int32> -IntervalInSeconds <Int32>
 -ProbeCount <Int32> [-RequestPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a2933-105">說明</span><span class="sxs-lookup"><span data-stu-id="a2933-105">DESCRIPTION</span></span>
<span data-ttu-id="a2933-106">**新的-AzureRmLoadBalancerProbeConfig** Cmdlet 會為 Azure 負載平衡器建立探測配置。</span><span class="sxs-lookup"><span data-stu-id="a2933-106">The **New-AzureRmLoadBalancerProbeConfig** cmdlet creates a probe configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="a2933-107">示例</span><span class="sxs-lookup"><span data-stu-id="a2933-107">EXAMPLES</span></span>

### <span data-ttu-id="a2933-108">範例1：建立探測器設定</span><span class="sxs-lookup"><span data-stu-id="a2933-108">Example 1: Create a probe configuration</span></span>
```
PS C:\>New-AzureRmLoadBalancerProbeConfig -Name "MyProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 15
```

<span data-ttu-id="a2933-109">這個命令會使用 HTTP 通訊協定，建立名為 MyProbe 的探測配置。</span><span class="sxs-lookup"><span data-stu-id="a2933-109">This command creates a probe configuration named MyProbe using the HTTP protocol.</span></span>
<span data-ttu-id="a2933-110">新的探測會連接到埠80上的負載平衡服務。</span><span class="sxs-lookup"><span data-stu-id="a2933-110">The new probe will connect to a load-balanced service on port 80.</span></span>

## <span data-ttu-id="a2933-111">參數</span><span class="sxs-lookup"><span data-stu-id="a2933-111">PARAMETERS</span></span>

### <span data-ttu-id="a2933-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2933-112">-DefaultProfile</span></span>
<span data-ttu-id="a2933-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a2933-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a2933-114">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="a2933-114">-IntervalInSeconds</span></span>
<span data-ttu-id="a2933-115">指定探測到負載平衡服務每個實例之間的間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="a2933-115">Specifies the interval, in seconds, between probes to each instance of a load-balanced service.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2933-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="a2933-116">-Name</span></span>
<span data-ttu-id="a2933-117">指定要建立的探針配置名稱。</span><span class="sxs-lookup"><span data-stu-id="a2933-117">Specifies the name of the probe configuration to create.</span></span>

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

### <span data-ttu-id="a2933-118">-埠</span><span class="sxs-lookup"><span data-stu-id="a2933-118">-Port</span></span>
<span data-ttu-id="a2933-119">指定新的探測器應該連線到負載平衡服務的埠。</span><span class="sxs-lookup"><span data-stu-id="a2933-119">Specifies the port on which the new probe should connect to a load-balanced service.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2933-120">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="a2933-120">-ProbeCount</span></span>
<span data-ttu-id="a2933-121">指定實例被視為不健康的每個實例連續失敗數。</span><span class="sxs-lookup"><span data-stu-id="a2933-121">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2933-122">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="a2933-122">-Protocol</span></span>
<span data-ttu-id="a2933-123">指定要用於探測設定的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="a2933-123">Specifies the protocol to use for the probe configuration.</span></span>
<span data-ttu-id="a2933-124">此參數可接受的值為： Tcp 或 Http。</span><span class="sxs-lookup"><span data-stu-id="a2933-124">The acceptable values for this parameter are: Tcp or Http.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2933-125">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="a2933-125">-RequestPath</span></span>
<span data-ttu-id="a2933-126">在負載平衡服務中指定要探測以判斷健康情況的路徑。</span><span class="sxs-lookup"><span data-stu-id="a2933-126">Specifies the path in a load-balanced service to probe to determine health.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2933-127">-確認</span><span class="sxs-lookup"><span data-stu-id="a2933-127">-Confirm</span></span>
<span data-ttu-id="a2933-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a2933-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2933-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2933-129">-WhatIf</span></span>
<span data-ttu-id="a2933-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a2933-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a2933-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a2933-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2933-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2933-132">CommonParameters</span></span>
<span data-ttu-id="a2933-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a2933-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2933-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a2933-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2933-135">輸入</span><span class="sxs-lookup"><span data-stu-id="a2933-135">INPUTS</span></span>

### <span data-ttu-id="a2933-136">所有</span><span class="sxs-lookup"><span data-stu-id="a2933-136">None</span></span>

## <span data-ttu-id="a2933-137">輸出</span><span class="sxs-lookup"><span data-stu-id="a2933-137">OUTPUTS</span></span>

### <span data-ttu-id="a2933-138">PSProbe 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a2933-138">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="a2933-139">筆記</span><span class="sxs-lookup"><span data-stu-id="a2933-139">NOTES</span></span>

## <span data-ttu-id="a2933-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="a2933-140">RELATED LINKS</span></span>

[<span data-ttu-id="a2933-141">附加 AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a2933-141">Add-AzureRmLoadBalancerProbeConfig</span></span>](./Add-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="a2933-142">AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a2933-142">Get-AzureRmLoadBalancerProbeConfig</span></span>](./Get-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="a2933-143">移除-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a2933-143">Remove-AzureRmLoadBalancerProbeConfig</span></span>](./Remove-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="a2933-144">Set-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a2933-144">Set-AzureRmLoadBalancerProbeConfig</span></span>](./Set-AzureRmLoadBalancerProbeConfig.md)


