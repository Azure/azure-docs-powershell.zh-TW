---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: 20704f404d5fe47267f42398ef885fb2c038f84e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93956291"
---
# <span data-ttu-id="5e195-101">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="5e195-101">Remove-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="5e195-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5e195-102">SYNOPSIS</span></span>
<span data-ttu-id="5e195-103">從現有的應用程式閘道移除健康情況探測。</span><span class="sxs-lookup"><span data-stu-id="5e195-103">Removes a health probe from an existing application gateway.</span></span>

## <span data-ttu-id="5e195-104">句法</span><span class="sxs-lookup"><span data-stu-id="5e195-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayProbeConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e195-105">說明</span><span class="sxs-lookup"><span data-stu-id="5e195-105">DESCRIPTION</span></span>
<span data-ttu-id="5e195-106">Remove-AzApplicationGatewayProbeConfig Cmdlet 會從現有的應用程式閘道移除 heath 探測器。</span><span class="sxs-lookup"><span data-stu-id="5e195-106">The Remove-AzApplicationGatewayProbeConfig cmdlet removes a heath probe from an existing application gateway.</span></span>

## <span data-ttu-id="5e195-107">示例</span><span class="sxs-lookup"><span data-stu-id="5e195-107">EXAMPLES</span></span>

### <span data-ttu-id="5e195-108">範例1：從現有的應用程式閘道移除健康情況探測</span><span class="sxs-lookup"><span data-stu-id="5e195-108">Example 1: Remove a health probe from an existing application gateway</span></span>
```
PS C:\>$Gateway = Remove-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe04"
```

<span data-ttu-id="5e195-109">這個命令會從名為 [閘道] 的應用程式閘道上，移除名為 Probe04 的 health 探測</span><span class="sxs-lookup"><span data-stu-id="5e195-109">This command removes the health probe named Probe04 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="5e195-110">參數</span><span class="sxs-lookup"><span data-stu-id="5e195-110">PARAMETERS</span></span>

### <span data-ttu-id="5e195-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5e195-111">-ApplicationGateway</span></span>
<span data-ttu-id="5e195-112">指定此 Cmdlet 移除探測器的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="5e195-112">Specifies the application gateway to which this cmdlet removes a probe.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5e195-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e195-113">-DefaultProfile</span></span>
<span data-ttu-id="5e195-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5e195-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e195-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="5e195-115">-Name</span></span>
<span data-ttu-id="5e195-116">指定此 Cmdlet 移除的探測器名稱。</span><span class="sxs-lookup"><span data-stu-id="5e195-116">Specifies the name of the probe for which this cmdlet removes.</span></span>

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

### <span data-ttu-id="5e195-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e195-117">CommonParameters</span></span>
<span data-ttu-id="5e195-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5e195-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e195-119">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5e195-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e195-120">輸入</span><span class="sxs-lookup"><span data-stu-id="5e195-120">INPUTS</span></span>

### <span data-ttu-id="5e195-121">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="5e195-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5e195-122">輸出</span><span class="sxs-lookup"><span data-stu-id="5e195-122">OUTPUTS</span></span>

### <span data-ttu-id="5e195-123">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="5e195-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5e195-124">筆記</span><span class="sxs-lookup"><span data-stu-id="5e195-124">NOTES</span></span>

## <span data-ttu-id="5e195-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="5e195-125">RELATED LINKS</span></span>

[<span data-ttu-id="5e195-126">從現有的應用程式閘道移除探測器</span><span class="sxs-lookup"><span data-stu-id="5e195-126">Remove a probe from an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#remove-a-probe-from-an-existing-application-gateway)

[<span data-ttu-id="5e195-127">附加 AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="5e195-127">Add-AzApplicationGatewayProbeConfig</span></span>](./Add-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="5e195-128">AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="5e195-128">Get-AzApplicationGatewayProbeConfig</span></span>](./Get-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="5e195-129">新-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="5e195-129">New-AzApplicationGatewayProbeConfig</span></span>](./New-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="5e195-130">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="5e195-130">Set-AzApplicationGatewayProbeConfig</span></span>](./Set-AzApplicationGatewayProbeConfig.md)

