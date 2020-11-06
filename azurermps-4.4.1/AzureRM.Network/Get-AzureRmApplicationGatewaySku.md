---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F01CB88A-49E7-41D8-B4E7-F1A4DCDC6B84
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySku.md
ms.openlocfilehash: 09639badc9ac96525456b7a9556c8e2afa7ebf2d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448861"
---
# <span data-ttu-id="35de2-101">Get-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="35de2-101">Get-AzureRmApplicationGatewaySku</span></span>

## <span data-ttu-id="35de2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="35de2-102">SYNOPSIS</span></span>
<span data-ttu-id="35de2-103">取得應用程式閘道的 SKU。</span><span class="sxs-lookup"><span data-stu-id="35de2-103">Gets the SKU of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="35de2-104">句法</span><span class="sxs-lookup"><span data-stu-id="35de2-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewaySku -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="35de2-105">說明</span><span class="sxs-lookup"><span data-stu-id="35de2-105">DESCRIPTION</span></span>
<span data-ttu-id="35de2-106">**AzureRmApplicationGatewaySku** Cmdlet 會取得應用程式閘道的庫存單位 (SKU) 。</span><span class="sxs-lookup"><span data-stu-id="35de2-106">The **Get-AzureRmApplicationGatewaySku** cmdlet gets the stock keeping unit (SKU) of an application gateway.</span></span>

## <span data-ttu-id="35de2-107">示例</span><span class="sxs-lookup"><span data-stu-id="35de2-107">EXAMPLES</span></span>

### <span data-ttu-id="35de2-108">範例1：取得應用程式閘道 SKU</span><span class="sxs-lookup"><span data-stu-id="35de2-108">Example 1: Get an application gateway SKU</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SKU = Get-AzureRmApplicationGatewaySku -ApplicationGateway $AppGW
```

<span data-ttu-id="35de2-109">第一個命令會取得名為 ApplicationGateway01 的應用程式閘道，並將結果儲存在名為 $AppGW 的變數中。</span><span class="sxs-lookup"><span data-stu-id="35de2-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="35de2-110">第二個命令會取得名為 ApplicationGateway01 的應用程式閘道的 SKU，並將結果儲存在名為 $SKU 的變數中。</span><span class="sxs-lookup"><span data-stu-id="35de2-110">The second command gets the SKU of an application gateway named ApplicationGateway01 and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="35de2-111">參數</span><span class="sxs-lookup"><span data-stu-id="35de2-111">PARAMETERS</span></span>

### <span data-ttu-id="35de2-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="35de2-112">-ApplicationGateway</span></span>
<span data-ttu-id="35de2-113">指定應用程式閘道物件。</span><span class="sxs-lookup"><span data-stu-id="35de2-113">Specifies the application gateway object.</span></span>

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

### <span data-ttu-id="35de2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35de2-114">-DefaultProfile</span></span>
<span data-ttu-id="35de2-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="35de2-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="35de2-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35de2-116">CommonParameters</span></span>
<span data-ttu-id="35de2-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="35de2-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35de2-118">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="35de2-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35de2-119">輸入</span><span class="sxs-lookup"><span data-stu-id="35de2-119">INPUTS</span></span>

### <span data-ttu-id="35de2-120">System.object</span><span class="sxs-lookup"><span data-stu-id="35de2-120">System.String</span></span>

## <span data-ttu-id="35de2-121">輸出</span><span class="sxs-lookup"><span data-stu-id="35de2-121">OUTPUTS</span></span>

### <span data-ttu-id="35de2-122">PSApplicationGatewaySku 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="35de2-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="35de2-123">筆記</span><span class="sxs-lookup"><span data-stu-id="35de2-123">NOTES</span></span>

## <span data-ttu-id="35de2-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="35de2-124">RELATED LINKS</span></span>

[<span data-ttu-id="35de2-125">新-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="35de2-125">New-AzureRmApplicationGatewaySku</span></span>](./New-AzureRmApplicationGatewaySku.md)

[<span data-ttu-id="35de2-126">Set-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="35de2-126">Set-AzureRmApplicationGatewaySku</span></span>](./Set-AzureRmApplicationGatewaySku.md)


