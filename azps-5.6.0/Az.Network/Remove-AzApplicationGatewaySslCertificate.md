---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5D788B84-0179-4A35-AC35-27C6F5FECB39
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: b8e74c8630dc7f5ba0cd3633314b416ca9a3e39e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910689"
---
# <span data-ttu-id="5e9f1-101">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5e9f1-101">Remove-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="5e9f1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5e9f1-102">SYNOPSIS</span></span>
<span data-ttu-id="5e9f1-103">從 Azure 應用程式閘道移除 SSL 憑證。</span><span class="sxs-lookup"><span data-stu-id="5e9f1-103">Removes an SSL certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="5e9f1-104">語法</span><span class="sxs-lookup"><span data-stu-id="5e9f1-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewaySslCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e9f1-105">描述</span><span class="sxs-lookup"><span data-stu-id="5e9f1-105">DESCRIPTION</span></span>
<span data-ttu-id="5e9f1-106">**Remove-AzApplicationGatewaySslCertificate** Cmdlet 會從 Azure 應用程式閘道移除安全通訊端層 (SSL) 憑證。</span><span class="sxs-lookup"><span data-stu-id="5e9f1-106">The **Remove-AzApplicationGatewaySslCertificate** cmdlet removes a Secure Sockets Layer (SSL) certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="5e9f1-107">例子</span><span class="sxs-lookup"><span data-stu-id="5e9f1-107">EXAMPLES</span></span>

### <span data-ttu-id="5e9f1-108">範例 1：從應用程式閘道移除 SSL 憑證</span><span class="sxs-lookup"><span data-stu-id="5e9f1-108">Example 1: Remove an SSL certificate from an application gateway</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert02"
```

<span data-ttu-id="5e9f1-109">第一個命令會取得名為 ApplicationGateway01 的應用程式閘道，並儲存在名為 $AppGW 的變數中。</span><span class="sxs-lookup"><span data-stu-id="5e9f1-109">The first command gets the application gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="5e9f1-110">第二個命令會從儲存在此變數的應用程式閘道移除名為 Cert02 的 SSL $AppGW憑證。</span><span class="sxs-lookup"><span data-stu-id="5e9f1-110">The second command removes the SSL certificate named Cert02 from the application gateway stored in the $AppGW variable.</span></span>

## <span data-ttu-id="5e9f1-111">參數</span><span class="sxs-lookup"><span data-stu-id="5e9f1-111">PARAMETERS</span></span>

### <span data-ttu-id="5e9f1-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5e9f1-112">-ApplicationGateway</span></span>
<span data-ttu-id="5e9f1-113">指定此 Cmdlet 會移除 SSL 憑證的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="5e9f1-113">Specifies the application gateway from which this cmdlet removes an SSL certificate.</span></span>

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

### <span data-ttu-id="5e9f1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e9f1-114">-DefaultProfile</span></span>
<span data-ttu-id="5e9f1-115">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5e9f1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e9f1-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="5e9f1-116">-Name</span></span>
<span data-ttu-id="5e9f1-117">指定此 Cmdlet 移除的 SSL 憑證名稱。</span><span class="sxs-lookup"><span data-stu-id="5e9f1-117">Specifies the name of an SSL certificate that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e9f1-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e9f1-118">CommonParameters</span></span>
<span data-ttu-id="5e9f1-119">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5e9f1-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e9f1-120">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="5e9f1-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e9f1-121">輸入</span><span class="sxs-lookup"><span data-stu-id="5e9f1-121">INPUTS</span></span>

### <span data-ttu-id="5e9f1-122">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5e9f1-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5e9f1-123">輸出</span><span class="sxs-lookup"><span data-stu-id="5e9f1-123">OUTPUTS</span></span>

### <span data-ttu-id="5e9f1-124">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5e9f1-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5e9f1-125">筆記</span><span class="sxs-lookup"><span data-stu-id="5e9f1-125">NOTES</span></span>

## <span data-ttu-id="5e9f1-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="5e9f1-126">RELATED LINKS</span></span>

[<span data-ttu-id="5e9f1-127">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5e9f1-127">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="5e9f1-128">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5e9f1-128">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="5e9f1-129">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5e9f1-129">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="5e9f1-130">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5e9f1-130">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


