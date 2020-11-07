---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F01CB88A-49E7-41D8-B4E7-F1A4DCDC6B84
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySku.md
ms.openlocfilehash: c8bd4a0070aa0e5635fad7cb20a627a7d23f5922
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93797845"
---
# <span data-ttu-id="e1927-101">Get-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="e1927-101">Get-AzApplicationGatewaySku</span></span>

## <span data-ttu-id="e1927-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e1927-102">SYNOPSIS</span></span>
<span data-ttu-id="e1927-103">取得應用程式閘道的 SKU。</span><span class="sxs-lookup"><span data-stu-id="e1927-103">Gets the SKU of an application gateway.</span></span>

## <span data-ttu-id="e1927-104">句法</span><span class="sxs-lookup"><span data-stu-id="e1927-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySku -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1927-105">說明</span><span class="sxs-lookup"><span data-stu-id="e1927-105">DESCRIPTION</span></span>
<span data-ttu-id="e1927-106">**AzApplicationGatewaySku** Cmdlet 會取得應用程式閘道的庫存單位 (SKU) 。</span><span class="sxs-lookup"><span data-stu-id="e1927-106">The **Get-AzApplicationGatewaySku** cmdlet gets the stock keeping unit (SKU) of an application gateway.</span></span>

## <span data-ttu-id="e1927-107">示例</span><span class="sxs-lookup"><span data-stu-id="e1927-107">EXAMPLES</span></span>

### <span data-ttu-id="e1927-108">範例1：取得應用程式閘道 SKU</span><span class="sxs-lookup"><span data-stu-id="e1927-108">Example 1: Get an application gateway SKU</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SKU = Get-AzApplicationGatewaySku -ApplicationGateway $AppGW
```

<span data-ttu-id="e1927-109">第一個命令會取得名為 ApplicationGateway01 的應用程式閘道，並將結果儲存在名為 $AppGW 的變數中。</span><span class="sxs-lookup"><span data-stu-id="e1927-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="e1927-110">第二個命令會取得名為 ApplicationGateway01 的應用程式閘道的 SKU，並將結果儲存在名為 $SKU 的變數中。</span><span class="sxs-lookup"><span data-stu-id="e1927-110">The second command gets the SKU of an application gateway named ApplicationGateway01 and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="e1927-111">參數</span><span class="sxs-lookup"><span data-stu-id="e1927-111">PARAMETERS</span></span>

### <span data-ttu-id="e1927-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e1927-112">-ApplicationGateway</span></span>
<span data-ttu-id="e1927-113">指定應用程式閘道物件。</span><span class="sxs-lookup"><span data-stu-id="e1927-113">Specifies the application gateway object.</span></span>

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

### <span data-ttu-id="e1927-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1927-114">-DefaultProfile</span></span>
<span data-ttu-id="e1927-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e1927-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1927-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1927-116">CommonParameters</span></span>
<span data-ttu-id="e1927-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e1927-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1927-118">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e1927-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1927-119">輸入</span><span class="sxs-lookup"><span data-stu-id="e1927-119">INPUTS</span></span>

### <span data-ttu-id="e1927-120">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e1927-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e1927-121">輸出</span><span class="sxs-lookup"><span data-stu-id="e1927-121">OUTPUTS</span></span>

### <span data-ttu-id="e1927-122">PSApplicationGatewaySku 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e1927-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="e1927-123">筆記</span><span class="sxs-lookup"><span data-stu-id="e1927-123">NOTES</span></span>

## <span data-ttu-id="e1927-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="e1927-124">RELATED LINKS</span></span>

[<span data-ttu-id="e1927-125">新-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="e1927-125">New-AzApplicationGatewaySku</span></span>](./New-AzApplicationGatewaySku.md)

[<span data-ttu-id="e1927-126">Set-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="e1927-126">Set-AzApplicationGatewaySku</span></span>](./Set-AzApplicationGatewaySku.md)


