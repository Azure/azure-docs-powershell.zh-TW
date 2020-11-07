---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 706C918B-1D1A-476C-BB74-EBB4EE72AC0C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 1743ed0427fdc0dd952c9b86d51c13c3ed855620
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93789722"
---
# <span data-ttu-id="87351-101">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="87351-101">Get-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="87351-102">摘要</span><span class="sxs-lookup"><span data-stu-id="87351-102">SYNOPSIS</span></span>
<span data-ttu-id="87351-103">取得應用程式閘道的驗證憑證。</span><span class="sxs-lookup"><span data-stu-id="87351-103">Gets an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="87351-104">句法</span><span class="sxs-lookup"><span data-stu-id="87351-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAuthenticationCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87351-105">說明</span><span class="sxs-lookup"><span data-stu-id="87351-105">DESCRIPTION</span></span>
<span data-ttu-id="87351-106">**AzApplicationGatewayAuthenticationCertificate** Cmdlet 會取得 Azure 應用程式閘道的驗證憑證。</span><span class="sxs-lookup"><span data-stu-id="87351-106">The **Get-AzApplicationGatewayAuthenticationCertificate** cmdlet gets an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="87351-107">示例</span><span class="sxs-lookup"><span data-stu-id="87351-107">EXAMPLES</span></span>

### <span data-ttu-id="87351-108">範例1：取得指定的驗證憑證</span><span class="sxs-lookup"><span data-stu-id="87351-108">Example 1: Get a specified authentication certificate</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $pool = Get-AzApplicationGatewayBackendAddressPool -Name "pool01" -ApplicationGateway $appgw
```

<span data-ttu-id="87351-109">第一個命令會取得名為 appGwName 的應用程式閘道，並將它儲存在 $appgw 變數中。</span><span class="sxs-lookup"><span data-stu-id="87351-109">The first command gets the application gateway named appGwName and stores it in the $appgw variable.</span></span>
<span data-ttu-id="87351-110">第二個命令會取得名為 pool01 的驗證憑證，並將它儲存在 $pool 變數中。</span><span class="sxs-lookup"><span data-stu-id="87351-110">The second command gets the authentication certificate named pool01 and stores it in the $pool variable.</span></span>

## <span data-ttu-id="87351-111">參數</span><span class="sxs-lookup"><span data-stu-id="87351-111">PARAMETERS</span></span>

### <span data-ttu-id="87351-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="87351-112">-ApplicationGateway</span></span>
<span data-ttu-id="87351-113">指定此 Cmdlet 取得其驗證憑證之應用程式閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="87351-113">Specifies the name of application gateway for which this cmdlet gets an authentication certificate.</span></span>

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

### <span data-ttu-id="87351-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87351-114">-DefaultProfile</span></span>
<span data-ttu-id="87351-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="87351-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="87351-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="87351-116">-Name</span></span>
<span data-ttu-id="87351-117">指定此 Cmdlet 所取得之驗證憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="87351-117">Specifies the name of the authentication certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="87351-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87351-118">CommonParameters</span></span>
<span data-ttu-id="87351-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="87351-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87351-120">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="87351-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87351-121">輸入</span><span class="sxs-lookup"><span data-stu-id="87351-121">INPUTS</span></span>

### <span data-ttu-id="87351-122">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="87351-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="87351-123">輸出</span><span class="sxs-lookup"><span data-stu-id="87351-123">OUTPUTS</span></span>

### <span data-ttu-id="87351-124">PSApplicationGatewayAuthenticationCertificate 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="87351-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="87351-125">筆記</span><span class="sxs-lookup"><span data-stu-id="87351-125">NOTES</span></span>
* <span data-ttu-id="87351-126">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路</span><span class="sxs-lookup"><span data-stu-id="87351-126">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="87351-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="87351-127">RELATED LINKS</span></span>

[<span data-ttu-id="87351-128">附加 AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="87351-128">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="87351-129">新-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="87351-129">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="87351-130">移除-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="87351-130">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="87351-131">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="87351-131">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


