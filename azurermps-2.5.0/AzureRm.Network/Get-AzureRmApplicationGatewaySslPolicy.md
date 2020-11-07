---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: AF02FFF8-F00D-4446-968F-F3C9008C39F0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaysslpolicy
schema: 2.0.0
ms.openlocfilehash: 237df37605581adeeb45fdfbb7bae6449128aa7b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93802385"
---
# <span data-ttu-id="83a06-101">Get-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="83a06-101">Get-AzureRmApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="83a06-102">摘要</span><span class="sxs-lookup"><span data-stu-id="83a06-102">SYNOPSIS</span></span>
<span data-ttu-id="83a06-103">取得應用程式閘道的 SSL 原則。</span><span class="sxs-lookup"><span data-stu-id="83a06-103">Gets the SSL policy of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="83a06-104">句法</span><span class="sxs-lookup"><span data-stu-id="83a06-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83a06-105">說明</span><span class="sxs-lookup"><span data-stu-id="83a06-105">DESCRIPTION</span></span>
<span data-ttu-id="83a06-106">**AzureRmApplicationGatewaySslPolicy** Cmdlet 會取得應用程式閘道的 SSL 原則。</span><span class="sxs-lookup"><span data-stu-id="83a06-106">The **Get-AzureRmApplicationGatewaySslPolicy** cmdlet gets the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="83a06-107">示例</span><span class="sxs-lookup"><span data-stu-id="83a06-107">EXAMPLES</span></span>

### <span data-ttu-id="83a06-108">sr-1</span><span class="sxs-lookup"><span data-stu-id="83a06-108">1:</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $sslpolicy = Get-AzureRmApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="83a06-109">第一個命令會取得名為 ApplicationGateway01 的應用程式閘道，並將結果儲存在名為 $AppGW 的變數中。</span><span class="sxs-lookup"><span data-stu-id="83a06-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="83a06-110">第二個命令會從儲存在名為 $AppGW 的變數中的應用程式閘道取得 ssl 原則。</span><span class="sxs-lookup"><span data-stu-id="83a06-110">The second command gets the ssl policy from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="83a06-111">參數</span><span class="sxs-lookup"><span data-stu-id="83a06-111">PARAMETERS</span></span>

### <span data-ttu-id="83a06-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="83a06-112">-ApplicationGateway</span></span>
<span data-ttu-id="83a06-113">指定此 Cmdlet 所取得之 SSL 原則的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="83a06-113">Specifies the application gateway of the SSL policy that this cmdlet gets.</span></span>

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

### <span data-ttu-id="83a06-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83a06-114">-DefaultProfile</span></span>
<span data-ttu-id="83a06-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="83a06-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83a06-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83a06-116">CommonParameters</span></span>
<span data-ttu-id="83a06-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="83a06-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83a06-118">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="83a06-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83a06-119">輸入</span><span class="sxs-lookup"><span data-stu-id="83a06-119">INPUTS</span></span>

### <span data-ttu-id="83a06-120">System.object</span><span class="sxs-lookup"><span data-stu-id="83a06-120">System.String</span></span>

## <span data-ttu-id="83a06-121">輸出</span><span class="sxs-lookup"><span data-stu-id="83a06-121">OUTPUTS</span></span>

### <span data-ttu-id="83a06-122">PSApplicationGatewaySslPolicy 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="83a06-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="83a06-123">筆記</span><span class="sxs-lookup"><span data-stu-id="83a06-123">NOTES</span></span>
* <span data-ttu-id="83a06-124">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路</span><span class="sxs-lookup"><span data-stu-id="83a06-124">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="83a06-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="83a06-125">RELATED LINKS</span></span>

[<span data-ttu-id="83a06-126">新-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="83a06-126">New-AzureRmApplicationGatewaySslPolicy</span></span>](./New-AzureRmApplicationGatewaySslPolicy.md)

[<span data-ttu-id="83a06-127">Set-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="83a06-127">Set-AzureRmApplicationGatewaySslPolicy</span></span>](./Set-AzureRmApplicationGatewaySslPolicy.md)


