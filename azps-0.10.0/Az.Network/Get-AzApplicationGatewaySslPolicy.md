---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AF02FFF8-F00D-4446-968F-F3C9008C39F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: 98f824ec0d874f8977c6e29f51358856cb5d1ca1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794450"
---
# <span data-ttu-id="7ef7a-101">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="7ef7a-101">Get-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="7ef7a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7ef7a-102">SYNOPSIS</span></span>
<span data-ttu-id="7ef7a-103">取得應用程式閘道的 SSL 原則。</span><span class="sxs-lookup"><span data-stu-id="7ef7a-103">Gets the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="7ef7a-104">句法</span><span class="sxs-lookup"><span data-stu-id="7ef7a-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ef7a-105">說明</span><span class="sxs-lookup"><span data-stu-id="7ef7a-105">DESCRIPTION</span></span>
<span data-ttu-id="7ef7a-106">**AzApplicationGatewaySslPolicy** Cmdlet 會取得應用程式閘道的 SSL 原則。</span><span class="sxs-lookup"><span data-stu-id="7ef7a-106">The **Get-AzApplicationGatewaySslPolicy** cmdlet gets the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="7ef7a-107">示例</span><span class="sxs-lookup"><span data-stu-id="7ef7a-107">EXAMPLES</span></span>

### <span data-ttu-id="7ef7a-108">sr-1</span><span class="sxs-lookup"><span data-stu-id="7ef7a-108">1:</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $sslpolicy = Get-AzApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="7ef7a-109">第一個命令會取得名為 ApplicationGateway01 的應用程式閘道，並將結果儲存在名為 $AppGW 的變數中。</span><span class="sxs-lookup"><span data-stu-id="7ef7a-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="7ef7a-110">第二個命令會從儲存在名為 $AppGW 的變數中的應用程式閘道取得 ssl 原則。</span><span class="sxs-lookup"><span data-stu-id="7ef7a-110">The second command gets the ssl policy from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="7ef7a-111">參數</span><span class="sxs-lookup"><span data-stu-id="7ef7a-111">PARAMETERS</span></span>

### <span data-ttu-id="7ef7a-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7ef7a-112">-ApplicationGateway</span></span>
<span data-ttu-id="7ef7a-113">指定此 Cmdlet 所取得之 SSL 原則的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="7ef7a-113">Specifies the application gateway of the SSL policy that this cmdlet gets.</span></span>

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

### <span data-ttu-id="7ef7a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ef7a-114">-DefaultProfile</span></span>
<span data-ttu-id="7ef7a-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7ef7a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ef7a-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ef7a-116">CommonParameters</span></span>
<span data-ttu-id="7ef7a-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7ef7a-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ef7a-118">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7ef7a-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ef7a-119">輸入</span><span class="sxs-lookup"><span data-stu-id="7ef7a-119">INPUTS</span></span>

### <span data-ttu-id="7ef7a-120">System.object</span><span class="sxs-lookup"><span data-stu-id="7ef7a-120">System.String</span></span>

## <span data-ttu-id="7ef7a-121">輸出</span><span class="sxs-lookup"><span data-stu-id="7ef7a-121">OUTPUTS</span></span>

### <span data-ttu-id="7ef7a-122">PSApplicationGatewaySslPolicy 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="7ef7a-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="7ef7a-123">筆記</span><span class="sxs-lookup"><span data-stu-id="7ef7a-123">NOTES</span></span>
* <span data-ttu-id="7ef7a-124">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路</span><span class="sxs-lookup"><span data-stu-id="7ef7a-124">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="7ef7a-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="7ef7a-125">RELATED LINKS</span></span>

[<span data-ttu-id="7ef7a-126">新-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="7ef7a-126">New-AzApplicationGatewaySslPolicy</span></span>](./New-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="7ef7a-127">Set-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="7ef7a-127">Set-AzApplicationGatewaySslPolicy</span></span>](./Set-AzApplicationGatewaySslPolicy.md)


