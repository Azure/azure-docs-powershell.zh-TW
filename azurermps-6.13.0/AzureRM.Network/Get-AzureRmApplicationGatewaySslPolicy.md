---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: AF02FFF8-F00D-4446-968F-F3C9008C39F0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySslPolicy.md
ms.openlocfilehash: 97851183233993400205993f091c8c57f376fcaf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624899"
---
# <span data-ttu-id="1607a-101">Get-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="1607a-101">Get-AzureRmApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="1607a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1607a-102">SYNOPSIS</span></span>
<span data-ttu-id="1607a-103">取得應用程式閘道的 SSL 原則。</span><span class="sxs-lookup"><span data-stu-id="1607a-103">Gets the SSL policy of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1607a-104">句法</span><span class="sxs-lookup"><span data-stu-id="1607a-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1607a-105">說明</span><span class="sxs-lookup"><span data-stu-id="1607a-105">DESCRIPTION</span></span>
<span data-ttu-id="1607a-106">**AzureRmApplicationGatewaySslPolicy** Cmdlet 會取得應用程式閘道的 SSL 原則。</span><span class="sxs-lookup"><span data-stu-id="1607a-106">The **Get-AzureRmApplicationGatewaySslPolicy** cmdlet gets the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="1607a-107">示例</span><span class="sxs-lookup"><span data-stu-id="1607a-107">EXAMPLES</span></span>

### <span data-ttu-id="1607a-108">sr-1</span><span class="sxs-lookup"><span data-stu-id="1607a-108">1:</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $sslpolicy = Get-AzureRmApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="1607a-109">第一個命令會取得名為 ApplicationGateway01 的應用程式閘道，並將結果儲存在名為 $AppGW 的變數中。</span><span class="sxs-lookup"><span data-stu-id="1607a-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="1607a-110">第二個命令會從儲存在名為 $AppGW 的變數中的應用程式閘道取得 ssl 原則。</span><span class="sxs-lookup"><span data-stu-id="1607a-110">The second command gets the ssl policy from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="1607a-111">參數</span><span class="sxs-lookup"><span data-stu-id="1607a-111">PARAMETERS</span></span>

### <span data-ttu-id="1607a-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1607a-112">-ApplicationGateway</span></span>
<span data-ttu-id="1607a-113">指定此 Cmdlet 所取得之 SSL 原則的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="1607a-113">Specifies the application gateway of the SSL policy that this cmdlet gets.</span></span>

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

### <span data-ttu-id="1607a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1607a-114">-DefaultProfile</span></span>
<span data-ttu-id="1607a-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1607a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1607a-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1607a-116">CommonParameters</span></span>
<span data-ttu-id="1607a-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1607a-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1607a-118">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1607a-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1607a-119">輸入</span><span class="sxs-lookup"><span data-stu-id="1607a-119">INPUTS</span></span>

### <span data-ttu-id="1607a-120">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="1607a-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="1607a-121">參數： ApplicationGateway (ByValue) </span><span class="sxs-lookup"><span data-stu-id="1607a-121">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="1607a-122">輸出</span><span class="sxs-lookup"><span data-stu-id="1607a-122">OUTPUTS</span></span>

### <span data-ttu-id="1607a-123">PSApplicationGatewaySslPolicy 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="1607a-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="1607a-124">筆記</span><span class="sxs-lookup"><span data-stu-id="1607a-124">NOTES</span></span>
* <span data-ttu-id="1607a-125">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路</span><span class="sxs-lookup"><span data-stu-id="1607a-125">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="1607a-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="1607a-126">RELATED LINKS</span></span>

[<span data-ttu-id="1607a-127">新-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="1607a-127">New-AzureRmApplicationGatewaySslPolicy</span></span>](./New-AzureRmApplicationGatewaySslPolicy.md)

[<span data-ttu-id="1607a-128">Set-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="1607a-128">Set-AzureRmApplicationGatewaySslPolicy</span></span>](./Set-AzureRmApplicationGatewaySslPolicy.md)


