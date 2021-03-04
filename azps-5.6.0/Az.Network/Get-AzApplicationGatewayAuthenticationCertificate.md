---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 706C918B-1D1A-476C-BB74-EBB4EE72AC0C
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 7f5dbd73158e5328ece78b1064a78ff5c4627035
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904622"
---
# <span data-ttu-id="bc738-101">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="bc738-101">Get-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="bc738-102">簡介</span><span class="sxs-lookup"><span data-stu-id="bc738-102">SYNOPSIS</span></span>
<span data-ttu-id="bc738-103">獲得應用程式閘道的驗證憑證。</span><span class="sxs-lookup"><span data-stu-id="bc738-103">Gets an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="bc738-104">語法</span><span class="sxs-lookup"><span data-stu-id="bc738-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAuthenticationCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bc738-105">描述</span><span class="sxs-lookup"><span data-stu-id="bc738-105">DESCRIPTION</span></span>
<span data-ttu-id="bc738-106">**Get-AzApplicationGatewayAuthenticationCertificate** Cmdlet 會取得 Azure 應用程式閘道的驗證憑證。</span><span class="sxs-lookup"><span data-stu-id="bc738-106">The **Get-AzApplicationGatewayAuthenticationCertificate** cmdlet gets an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="bc738-107">例子</span><span class="sxs-lookup"><span data-stu-id="bc738-107">EXAMPLES</span></span>

### <span data-ttu-id="bc738-108">範例 1：取得指定的驗證憑證</span><span class="sxs-lookup"><span data-stu-id="bc738-108">Example 1: Get a specified authentication certificate</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $cert = Get-AzApplicationGatewayAuthenticationCertificate -Name "cert01" -ApplicationGateway $appgw
```

<span data-ttu-id="bc738-109">第一個命令會獲得名為 appGwName 的應用程式閘道，並儲存在$appgw變數。</span><span class="sxs-lookup"><span data-stu-id="bc738-109">The first command gets the application gateway named appGwName and stores it in the $appgw variable.</span></span>
<span data-ttu-id="bc738-110">第二個命令會獲得名為 cert01 的驗證憑證，並儲存在 $cert 變數中。</span><span class="sxs-lookup"><span data-stu-id="bc738-110">The second command gets the authentication certificate named cert01 and stores it in the $cert variable.</span></span>

## <span data-ttu-id="bc738-111">參數</span><span class="sxs-lookup"><span data-stu-id="bc738-111">PARAMETERS</span></span>

### <span data-ttu-id="bc738-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bc738-112">-ApplicationGateway</span></span>
<span data-ttu-id="bc738-113">指定此 Cmdlet 會獲得驗證憑證的應用程式閘道名稱。</span><span class="sxs-lookup"><span data-stu-id="bc738-113">Specifies the name of application gateway for which this cmdlet gets an authentication certificate.</span></span>

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

### <span data-ttu-id="bc738-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc738-114">-DefaultProfile</span></span>
<span data-ttu-id="bc738-115">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="bc738-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc738-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="bc738-116">-Name</span></span>
<span data-ttu-id="bc738-117">指定此 Cmdlet 所獲得之驗證憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="bc738-117">Specifies the name of the authentication certificate that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc738-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc738-118">CommonParameters</span></span>
<span data-ttu-id="bc738-119">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="bc738-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc738-120">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bc738-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc738-121">輸入</span><span class="sxs-lookup"><span data-stu-id="bc738-121">INPUTS</span></span>

### <span data-ttu-id="bc738-122">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bc738-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="bc738-123">輸出</span><span class="sxs-lookup"><span data-stu-id="bc738-123">OUTPUTS</span></span>

### <span data-ttu-id="bc738-124">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="bc738-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="bc738-125">筆記</span><span class="sxs-lookup"><span data-stu-id="bc738-125">NOTES</span></span>
* <span data-ttu-id="bc738-126">關鍵字：azure、azurerm、arm、資源、管理、管理員、網路、網路</span><span class="sxs-lookup"><span data-stu-id="bc738-126">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="bc738-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="bc738-127">RELATED LINKS</span></span>

[<span data-ttu-id="bc738-128">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="bc738-128">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="bc738-129">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="bc738-129">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="bc738-130">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="bc738-130">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="bc738-131">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="bc738-131">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


