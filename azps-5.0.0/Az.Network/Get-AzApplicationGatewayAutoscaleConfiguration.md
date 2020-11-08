---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: b4238f5b1492afad7d09ee9c338a346d5f54a5e0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139811"
---
# <span data-ttu-id="1a735-101">Get-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="1a735-101">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="1a735-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1a735-102">SYNOPSIS</span></span>
<span data-ttu-id="1a735-103">取得應用程式閘道的自動縮放設定。</span><span class="sxs-lookup"><span data-stu-id="1a735-103">Gets the Autoscale Configuration of the Application Gateway.</span></span>

## <span data-ttu-id="1a735-104">句法</span><span class="sxs-lookup"><span data-stu-id="1a735-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a735-105">說明</span><span class="sxs-lookup"><span data-stu-id="1a735-105">DESCRIPTION</span></span>
<span data-ttu-id="1a735-106">**AzApplicationGatewayAutoscaleConfiguration** Cmdlet 會取得應用程式閘道的自動縮放設定。</span><span class="sxs-lookup"><span data-stu-id="1a735-106">The **Get-AzApplicationGatewayAutoscaleConfiguration** cmdlet gets Autoscale Configuration of the Application Gateway.</span></span>

## <span data-ttu-id="1a735-107">示例</span><span class="sxs-lookup"><span data-stu-id="1a735-107">EXAMPLES</span></span>

### <span data-ttu-id="1a735-108">範例1</span><span class="sxs-lookup"><span data-stu-id="1a735-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $autoscaleConfiguration = Get-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw
PS C:\> $autoscaleConfiguration.MinCapacity
```

<span data-ttu-id="1a735-109">第一個命令會取得應用程式閘道，並將它儲存在 $gw 變數中。</span><span class="sxs-lookup"><span data-stu-id="1a735-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="1a735-110">第二個命令會從應用程式閘道抽取自動縮放設定。</span><span class="sxs-lookup"><span data-stu-id="1a735-110">The second command extracts out the autoscale configuration from the application gateway.</span></span>

## <span data-ttu-id="1a735-111">參數</span><span class="sxs-lookup"><span data-stu-id="1a735-111">PARAMETERS</span></span>

### <span data-ttu-id="1a735-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1a735-112">-ApplicationGateway</span></span>
<span data-ttu-id="1a735-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1a735-113">The applicationGateway</span></span>

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

### <span data-ttu-id="1a735-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a735-114">-DefaultProfile</span></span>
<span data-ttu-id="1a735-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1a735-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a735-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a735-116">CommonParameters</span></span>
<span data-ttu-id="1a735-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1a735-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a735-118">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1a735-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a735-119">輸入</span><span class="sxs-lookup"><span data-stu-id="1a735-119">INPUTS</span></span>

### <span data-ttu-id="1a735-120">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="1a735-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1a735-121">輸出</span><span class="sxs-lookup"><span data-stu-id="1a735-121">OUTPUTS</span></span>

### <span data-ttu-id="1a735-122">PSApplicationGatewayAutoscaleConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="1a735-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="1a735-123">筆記</span><span class="sxs-lookup"><span data-stu-id="1a735-123">NOTES</span></span>

## <span data-ttu-id="1a735-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="1a735-124">RELATED LINKS</span></span>

[<span data-ttu-id="1a735-125">新-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="1a735-125">New-AzApplicationGatewayAutoscaleConfiguration</span></span>](./New-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="1a735-126">移除-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="1a735-126">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Remove-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="1a735-127">Set-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="1a735-127">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Set-AzApplicationGatewayAutoscaleConfiguration.md)
