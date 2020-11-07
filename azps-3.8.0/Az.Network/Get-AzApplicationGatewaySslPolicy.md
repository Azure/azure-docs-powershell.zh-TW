---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AF02FFF8-F00D-4446-968F-F3C9008C39F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: 3e7e9559761bce69473511fbd6cdb94d635e13c9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957567"
---
# <span data-ttu-id="2c343-101">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="2c343-101">Get-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="2c343-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2c343-102">SYNOPSIS</span></span>
<span data-ttu-id="2c343-103">取得應用程式閘道的 SSL 原則。</span><span class="sxs-lookup"><span data-stu-id="2c343-103">Gets the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="2c343-104">句法</span><span class="sxs-lookup"><span data-stu-id="2c343-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c343-105">說明</span><span class="sxs-lookup"><span data-stu-id="2c343-105">DESCRIPTION</span></span>
<span data-ttu-id="2c343-106">**AzApplicationGatewaySslPolicy** Cmdlet 會取得應用程式閘道的 SSL 原則。</span><span class="sxs-lookup"><span data-stu-id="2c343-106">The **Get-AzApplicationGatewaySslPolicy** cmdlet gets the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="2c343-107">示例</span><span class="sxs-lookup"><span data-stu-id="2c343-107">EXAMPLES</span></span>

### <span data-ttu-id="2c343-108">sr-1</span><span class="sxs-lookup"><span data-stu-id="2c343-108">1:</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $sslpolicy = Get-AzApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="2c343-109">第一個命令會取得名為 ApplicationGateway01 的應用程式閘道，並將結果儲存在名為 $AppGW 的變數中。</span><span class="sxs-lookup"><span data-stu-id="2c343-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="2c343-110">第二個命令會從儲存在名為 $AppGW 的變數中的應用程式閘道取得 ssl 原則。</span><span class="sxs-lookup"><span data-stu-id="2c343-110">The second command gets the ssl policy from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="2c343-111">參數</span><span class="sxs-lookup"><span data-stu-id="2c343-111">PARAMETERS</span></span>

### <span data-ttu-id="2c343-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2c343-112">-ApplicationGateway</span></span>
<span data-ttu-id="2c343-113">指定此 Cmdlet 所取得之 SSL 原則的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="2c343-113">Specifies the application gateway of the SSL policy that this cmdlet gets.</span></span>

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

### <span data-ttu-id="2c343-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c343-114">-DefaultProfile</span></span>
<span data-ttu-id="2c343-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2c343-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c343-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c343-116">CommonParameters</span></span>
<span data-ttu-id="2c343-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2c343-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c343-118">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="2c343-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c343-119">輸入</span><span class="sxs-lookup"><span data-stu-id="2c343-119">INPUTS</span></span>

### <span data-ttu-id="2c343-120">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="2c343-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2c343-121">輸出</span><span class="sxs-lookup"><span data-stu-id="2c343-121">OUTPUTS</span></span>

### <span data-ttu-id="2c343-122">PSApplicationGatewaySslPolicy 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="2c343-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="2c343-123">筆記</span><span class="sxs-lookup"><span data-stu-id="2c343-123">NOTES</span></span>
* <span data-ttu-id="2c343-124">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路</span><span class="sxs-lookup"><span data-stu-id="2c343-124">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="2c343-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="2c343-125">RELATED LINKS</span></span>

[<span data-ttu-id="2c343-126">新-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="2c343-126">New-AzApplicationGatewaySslPolicy</span></span>](./New-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="2c343-127">Set-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="2c343-127">Set-AzApplicationGatewaySslPolicy</span></span>](./Set-AzApplicationGatewaySslPolicy.md)


