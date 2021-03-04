---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AF02FFF8-F00D-4446-968F-F3C9008C39F0
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: 4e15a4296a405a7f0f1e9ac918a5a806603203da
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912778"
---
# <span data-ttu-id="7d9b8-101">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="7d9b8-101">Get-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="7d9b8-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7d9b8-102">SYNOPSIS</span></span>
<span data-ttu-id="7d9b8-103">獲得應用程式閘道的 SSL 策略。</span><span class="sxs-lookup"><span data-stu-id="7d9b8-103">Gets the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="7d9b8-104">語法</span><span class="sxs-lookup"><span data-stu-id="7d9b8-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d9b8-105">描述</span><span class="sxs-lookup"><span data-stu-id="7d9b8-105">DESCRIPTION</span></span>
<span data-ttu-id="7d9b8-106">**Get-AzApplicationGatewaySslPolicy** Cmdlet 會取得應用程式閘道的 SSL 策略。</span><span class="sxs-lookup"><span data-stu-id="7d9b8-106">The **Get-AzApplicationGatewaySslPolicy** cmdlet gets the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="7d9b8-107">例子</span><span class="sxs-lookup"><span data-stu-id="7d9b8-107">EXAMPLES</span></span>

### <span data-ttu-id="7d9b8-108">1:</span><span class="sxs-lookup"><span data-stu-id="7d9b8-108">1:</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $sslpolicy = Get-AzApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="7d9b8-109">第一個命令會取得名為 ApplicationGateway01 的應用程式閘道，並儲存在名為 applicationGateway01 的$AppGW。</span><span class="sxs-lookup"><span data-stu-id="7d9b8-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="7d9b8-110">第二個命令會從儲存在名為 $AppGW 的變數中，從應用程式閘道獲得 ssl$AppGW。</span><span class="sxs-lookup"><span data-stu-id="7d9b8-110">The second command gets the ssl policy from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="7d9b8-111">參數</span><span class="sxs-lookup"><span data-stu-id="7d9b8-111">PARAMETERS</span></span>

### <span data-ttu-id="7d9b8-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7d9b8-112">-ApplicationGateway</span></span>
<span data-ttu-id="7d9b8-113">指定此 Cmdlet 所獲得之 SSL 策略的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="7d9b8-113">Specifies the application gateway of the SSL policy that this cmdlet gets.</span></span>

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

### <span data-ttu-id="7d9b8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d9b8-114">-DefaultProfile</span></span>
<span data-ttu-id="7d9b8-115">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="7d9b8-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d9b8-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d9b8-116">CommonParameters</span></span>
<span data-ttu-id="7d9b8-117">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7d9b8-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d9b8-118">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7d9b8-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d9b8-119">輸入</span><span class="sxs-lookup"><span data-stu-id="7d9b8-119">INPUTS</span></span>

### <span data-ttu-id="7d9b8-120">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7d9b8-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7d9b8-121">輸出</span><span class="sxs-lookup"><span data-stu-id="7d9b8-121">OUTPUTS</span></span>

### <span data-ttu-id="7d9b8-122">Microsoft.Azure.Commands.Network.models.PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="7d9b8-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="7d9b8-123">筆記</span><span class="sxs-lookup"><span data-stu-id="7d9b8-123">NOTES</span></span>
* <span data-ttu-id="7d9b8-124">關鍵字：azure、azurerm、arm、資源、管理、管理員、網路、網路</span><span class="sxs-lookup"><span data-stu-id="7d9b8-124">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="7d9b8-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="7d9b8-125">RELATED LINKS</span></span>

[<span data-ttu-id="7d9b8-126">New-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="7d9b8-126">New-AzApplicationGatewaySslPolicy</span></span>](./New-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="7d9b8-127">Set-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="7d9b8-127">Set-AzApplicationGatewaySslPolicy</span></span>](./Set-AzApplicationGatewaySslPolicy.md)


