---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F01CB88A-49E7-41D8-B4E7-F1A4DCDC6B84
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySku.md
ms.openlocfilehash: c8bd4a0070aa0e5635fad7cb20a627a7d23f5922
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100133927"
---
# <span data-ttu-id="22e60-101">Get-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="22e60-101">Get-AzApplicationGatewaySku</span></span>

## <span data-ttu-id="22e60-102">摘要</span><span class="sxs-lookup"><span data-stu-id="22e60-102">SYNOPSIS</span></span>
<span data-ttu-id="22e60-103">取得應用程式閘道的 SKU。</span><span class="sxs-lookup"><span data-stu-id="22e60-103">Gets the SKU of an application gateway.</span></span>

## <span data-ttu-id="22e60-104">句法</span><span class="sxs-lookup"><span data-stu-id="22e60-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySku -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22e60-105">說明</span><span class="sxs-lookup"><span data-stu-id="22e60-105">DESCRIPTION</span></span>
<span data-ttu-id="22e60-106">**AzApplicationGatewaySku** Cmdlet 會取得應用程式閘道的庫存單位 (SKU) 。</span><span class="sxs-lookup"><span data-stu-id="22e60-106">The **Get-AzApplicationGatewaySku** cmdlet gets the stock keeping unit (SKU) of an application gateway.</span></span>

## <span data-ttu-id="22e60-107">示例</span><span class="sxs-lookup"><span data-stu-id="22e60-107">EXAMPLES</span></span>

### <span data-ttu-id="22e60-108">範例1：取得應用程式閘道 SKU</span><span class="sxs-lookup"><span data-stu-id="22e60-108">Example 1: Get an application gateway SKU</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SKU = Get-AzApplicationGatewaySku -ApplicationGateway $AppGW
```

<span data-ttu-id="22e60-109">第一個命令會取得名為 ApplicationGateway01 的應用程式閘道，並將結果儲存在名為 $AppGW 的變數中。</span><span class="sxs-lookup"><span data-stu-id="22e60-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="22e60-110">第二個命令會取得名為 ApplicationGateway01 的應用程式閘道的 SKU，並將結果儲存在名為 $SKU 的變數中。</span><span class="sxs-lookup"><span data-stu-id="22e60-110">The second command gets the SKU of an application gateway named ApplicationGateway01 and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="22e60-111">參數</span><span class="sxs-lookup"><span data-stu-id="22e60-111">PARAMETERS</span></span>

### <span data-ttu-id="22e60-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="22e60-112">-ApplicationGateway</span></span>
<span data-ttu-id="22e60-113">指定應用程式閘道物件。</span><span class="sxs-lookup"><span data-stu-id="22e60-113">Specifies the application gateway object.</span></span>

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

### <span data-ttu-id="22e60-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22e60-114">-DefaultProfile</span></span>
<span data-ttu-id="22e60-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="22e60-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22e60-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22e60-116">CommonParameters</span></span>
<span data-ttu-id="22e60-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="22e60-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22e60-118">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="22e60-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22e60-119">輸入</span><span class="sxs-lookup"><span data-stu-id="22e60-119">INPUTS</span></span>

### <span data-ttu-id="22e60-120">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="22e60-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="22e60-121">輸出</span><span class="sxs-lookup"><span data-stu-id="22e60-121">OUTPUTS</span></span>

### <span data-ttu-id="22e60-122">PSApplicationGatewaySku 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="22e60-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="22e60-123">筆記</span><span class="sxs-lookup"><span data-stu-id="22e60-123">NOTES</span></span>

## <span data-ttu-id="22e60-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="22e60-124">RELATED LINKS</span></span>

[<span data-ttu-id="22e60-125">新-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="22e60-125">New-AzApplicationGatewaySku</span></span>](./New-AzApplicationGatewaySku.md)

[<span data-ttu-id="22e60-126">Set-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="22e60-126">Set-AzApplicationGatewaySku</span></span>](./Set-AzApplicationGatewaySku.md)


