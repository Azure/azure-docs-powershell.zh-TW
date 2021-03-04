---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: 78a9623e5e65c93d302b356b64b5c30033697fdf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915370"
---
# <span data-ttu-id="5072e-101">Get-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="5072e-101">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="5072e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5072e-102">SYNOPSIS</span></span>
<span data-ttu-id="5072e-103">獲得應用程式閘道的自動縮放組配置。</span><span class="sxs-lookup"><span data-stu-id="5072e-103">Gets the Autoscale Configuration of the Application Gateway.</span></span>

## <span data-ttu-id="5072e-104">語法</span><span class="sxs-lookup"><span data-stu-id="5072e-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5072e-105">描述</span><span class="sxs-lookup"><span data-stu-id="5072e-105">DESCRIPTION</span></span>
<span data-ttu-id="5072e-106">**Get-AzApplicationGatewayAutoscaleConfiguration** Cmdlet 會取得應用程式閘道的自動縮放組式。</span><span class="sxs-lookup"><span data-stu-id="5072e-106">The **Get-AzApplicationGatewayAutoscaleConfiguration** cmdlet gets Autoscale Configuration of the Application Gateway.</span></span>

## <span data-ttu-id="5072e-107">例子</span><span class="sxs-lookup"><span data-stu-id="5072e-107">EXAMPLES</span></span>

### <span data-ttu-id="5072e-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="5072e-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $autoscaleConfiguration = Get-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw
PS C:\> $autoscaleConfiguration.MinCapacity
```

<span data-ttu-id="5072e-109">第一個命令會獲得應用程式閘道，並儲存在$gw變數中。</span><span class="sxs-lookup"><span data-stu-id="5072e-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="5072e-110">第二個命令會從應用程式閘道解壓縮自動縮放組配置。</span><span class="sxs-lookup"><span data-stu-id="5072e-110">The second command extracts out the autoscale configuration from the application gateway.</span></span>

## <span data-ttu-id="5072e-111">參數</span><span class="sxs-lookup"><span data-stu-id="5072e-111">PARAMETERS</span></span>

### <span data-ttu-id="5072e-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5072e-112">-ApplicationGateway</span></span>
<span data-ttu-id="5072e-113">應用程式Gateway</span><span class="sxs-lookup"><span data-stu-id="5072e-113">The applicationGateway</span></span>

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

### <span data-ttu-id="5072e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5072e-114">-DefaultProfile</span></span>
<span data-ttu-id="5072e-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5072e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5072e-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5072e-116">CommonParameters</span></span>
<span data-ttu-id="5072e-117">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5072e-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5072e-118">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5072e-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5072e-119">輸入</span><span class="sxs-lookup"><span data-stu-id="5072e-119">INPUTS</span></span>

### <span data-ttu-id="5072e-120">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5072e-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5072e-121">輸出</span><span class="sxs-lookup"><span data-stu-id="5072e-121">OUTPUTS</span></span>

### <span data-ttu-id="5072e-122">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="5072e-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="5072e-123">筆記</span><span class="sxs-lookup"><span data-stu-id="5072e-123">NOTES</span></span>

## <span data-ttu-id="5072e-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="5072e-124">RELATED LINKS</span></span>

[<span data-ttu-id="5072e-125">New-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="5072e-125">New-AzApplicationGatewayAutoscaleConfiguration</span></span>](./New-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="5072e-126">Remove-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="5072e-126">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Remove-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="5072e-127">Set-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="5072e-127">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Set-AzApplicationGatewayAutoscaleConfiguration.md)
