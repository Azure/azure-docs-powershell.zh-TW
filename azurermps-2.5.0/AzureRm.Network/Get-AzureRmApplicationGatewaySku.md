---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F01CB88A-49E7-41D8-B4E7-F1A4DCDC6B84
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaysku
schema: 2.0.0
ms.openlocfilehash: 2359459688dbae2c718e4a5d5f65bf68b2c8c5ea
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93802394"
---
# <span data-ttu-id="4ef6e-101">Get-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="4ef6e-101">Get-AzureRmApplicationGatewaySku</span></span>

## <span data-ttu-id="4ef6e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4ef6e-102">SYNOPSIS</span></span>
<span data-ttu-id="4ef6e-103">取得應用程式閘道的 SKU。</span><span class="sxs-lookup"><span data-stu-id="4ef6e-103">Gets the SKU of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ef6e-104">句法</span><span class="sxs-lookup"><span data-stu-id="4ef6e-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewaySku -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ef6e-105">說明</span><span class="sxs-lookup"><span data-stu-id="4ef6e-105">DESCRIPTION</span></span>
<span data-ttu-id="4ef6e-106">**AzureRmApplicationGatewaySku** Cmdlet 會取得應用程式閘道的庫存單位 (SKU) 。</span><span class="sxs-lookup"><span data-stu-id="4ef6e-106">The **Get-AzureRmApplicationGatewaySku** cmdlet gets the stock keeping unit (SKU) of an application gateway.</span></span>

## <span data-ttu-id="4ef6e-107">示例</span><span class="sxs-lookup"><span data-stu-id="4ef6e-107">EXAMPLES</span></span>

### <span data-ttu-id="4ef6e-108">範例1：取得應用程式閘道 SKU</span><span class="sxs-lookup"><span data-stu-id="4ef6e-108">Example 1: Get an application gateway SKU</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SKU = Get-AzureRmApplicationGatewaySku -ApplicationGateway $AppGW
```

<span data-ttu-id="4ef6e-109">第一個命令會取得名為 ApplicationGateway01 的應用程式閘道，並將結果儲存在名為 $AppGW 的變數中。</span><span class="sxs-lookup"><span data-stu-id="4ef6e-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="4ef6e-110">第二個命令會取得名為 ApplicationGateway01 的應用程式閘道的 SKU，並將結果儲存在名為 $SKU 的變數中。</span><span class="sxs-lookup"><span data-stu-id="4ef6e-110">The second command gets the SKU of an application gateway named ApplicationGateway01 and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="4ef6e-111">參數</span><span class="sxs-lookup"><span data-stu-id="4ef6e-111">PARAMETERS</span></span>

### <span data-ttu-id="4ef6e-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4ef6e-112">-ApplicationGateway</span></span>
<span data-ttu-id="4ef6e-113">指定應用程式閘道物件。</span><span class="sxs-lookup"><span data-stu-id="4ef6e-113">Specifies the application gateway object.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ef6e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ef6e-114">-DefaultProfile</span></span>
<span data-ttu-id="4ef6e-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4ef6e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ef6e-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ef6e-116">CommonParameters</span></span>
<span data-ttu-id="4ef6e-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4ef6e-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ef6e-118">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4ef6e-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ef6e-119">輸入</span><span class="sxs-lookup"><span data-stu-id="4ef6e-119">INPUTS</span></span>

### <span data-ttu-id="4ef6e-120">System.object</span><span class="sxs-lookup"><span data-stu-id="4ef6e-120">System.String</span></span>

## <span data-ttu-id="4ef6e-121">輸出</span><span class="sxs-lookup"><span data-stu-id="4ef6e-121">OUTPUTS</span></span>

### <span data-ttu-id="4ef6e-122">PSApplicationGatewaySku 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4ef6e-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="4ef6e-123">筆記</span><span class="sxs-lookup"><span data-stu-id="4ef6e-123">NOTES</span></span>

## <span data-ttu-id="4ef6e-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="4ef6e-124">RELATED LINKS</span></span>

[<span data-ttu-id="4ef6e-125">新-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="4ef6e-125">New-AzureRmApplicationGatewaySku</span></span>](./New-AzureRmApplicationGatewaySku.md)

[<span data-ttu-id="4ef6e-126">Set-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="4ef6e-126">Set-AzureRmApplicationGatewaySku</span></span>](./Set-AzureRmApplicationGatewaySku.md)


