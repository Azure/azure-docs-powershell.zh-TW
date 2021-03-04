---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: 8ee58ee3f6c7a92fac0cb3c92f0a45966e4e875e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911913"
---
# <span data-ttu-id="856fb-101">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="856fb-101">Remove-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="856fb-102">簡介</span><span class="sxs-lookup"><span data-stu-id="856fb-102">SYNOPSIS</span></span>
<span data-ttu-id="856fb-103">移除現有應用程式閘道的健康狀態建議。</span><span class="sxs-lookup"><span data-stu-id="856fb-103">Removes a health probe from an existing application gateway.</span></span>

## <span data-ttu-id="856fb-104">語法</span><span class="sxs-lookup"><span data-stu-id="856fb-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayProbeConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="856fb-105">描述</span><span class="sxs-lookup"><span data-stu-id="856fb-105">DESCRIPTION</span></span>
<span data-ttu-id="856fb-106">此Remove-AzApplicationGatewayProbeConfig Cmdlet 會移除現有應用程式閘道的冷光。</span><span class="sxs-lookup"><span data-stu-id="856fb-106">The Remove-AzApplicationGatewayProbeConfig cmdlet removes a heath probe from an existing application gateway.</span></span>

## <span data-ttu-id="856fb-107">例子</span><span class="sxs-lookup"><span data-stu-id="856fb-107">EXAMPLES</span></span>

### <span data-ttu-id="856fb-108">範例 1：移除現有應用程式閘道的健康狀態</span><span class="sxs-lookup"><span data-stu-id="856fb-108">Example 1: Remove a health probe from an existing application gateway</span></span>
```
PS C:\>$Gateway = Remove-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe04"
```

<span data-ttu-id="856fb-109">此命令會從名為 Gateway 的應用程式閘道移除名為 Command04 的健康狀態建議。</span><span class="sxs-lookup"><span data-stu-id="856fb-109">This command removes the health probe named Probe04 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="856fb-110">參數</span><span class="sxs-lookup"><span data-stu-id="856fb-110">PARAMETERS</span></span>

### <span data-ttu-id="856fb-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="856fb-111">-ApplicationGateway</span></span>
<span data-ttu-id="856fb-112">指定此 Cmdlet 移除專案的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="856fb-112">Specifies the application gateway to which this cmdlet removes a probe.</span></span>

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

### <span data-ttu-id="856fb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="856fb-113">-DefaultProfile</span></span>
<span data-ttu-id="856fb-114">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="856fb-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="856fb-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="856fb-115">-Name</span></span>
<span data-ttu-id="856fb-116">指定此 Cmdlet 移除的探索名稱。</span><span class="sxs-lookup"><span data-stu-id="856fb-116">Specifies the name of the probe for which this cmdlet removes.</span></span>

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

### <span data-ttu-id="856fb-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="856fb-117">CommonParameters</span></span>
<span data-ttu-id="856fb-118">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="856fb-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="856fb-119">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="856fb-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="856fb-120">輸入</span><span class="sxs-lookup"><span data-stu-id="856fb-120">INPUTS</span></span>

### <span data-ttu-id="856fb-121">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="856fb-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="856fb-122">輸出</span><span class="sxs-lookup"><span data-stu-id="856fb-122">OUTPUTS</span></span>

### <span data-ttu-id="856fb-123">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="856fb-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="856fb-124">筆記</span><span class="sxs-lookup"><span data-stu-id="856fb-124">NOTES</span></span>

## <span data-ttu-id="856fb-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="856fb-125">RELATED LINKS</span></span>

[<span data-ttu-id="856fb-126">移除現有應用程式閘道的探索</span><span class="sxs-lookup"><span data-stu-id="856fb-126">Remove a probe from an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#remove-a-probe-from-an-existing-application-gateway)

[<span data-ttu-id="856fb-127">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="856fb-127">Add-AzApplicationGatewayProbeConfig</span></span>](./Add-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="856fb-128">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="856fb-128">Get-AzApplicationGatewayProbeConfig</span></span>](./Get-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="856fb-129">New-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="856fb-129">New-AzApplicationGatewayProbeConfig</span></span>](./New-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="856fb-130">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="856fb-130">Set-AzApplicationGatewayProbeConfig</span></span>](./Set-AzApplicationGatewayProbeConfig.md)

