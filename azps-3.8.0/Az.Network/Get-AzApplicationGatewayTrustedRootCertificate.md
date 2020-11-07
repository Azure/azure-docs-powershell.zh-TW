---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: 5c3976ddeeaa856f956ecb785a9d35e62ba322fb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93798361"
---
# <span data-ttu-id="84dda-101">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="84dda-101">Get-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="84dda-102">摘要</span><span class="sxs-lookup"><span data-stu-id="84dda-102">SYNOPSIS</span></span>
<span data-ttu-id="84dda-103">從應用程式閘道取得具有特定名稱的受根信任證書。</span><span class="sxs-lookup"><span data-stu-id="84dda-103">Gets the Trusted Root Certificate with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="84dda-104">句法</span><span class="sxs-lookup"><span data-stu-id="84dda-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayTrustedRootCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="84dda-105">說明</span><span class="sxs-lookup"><span data-stu-id="84dda-105">DESCRIPTION</span></span>
<span data-ttu-id="84dda-106">**AzApplicationGatewayTrustedRootCertificate** Cmdlet 會從應用程式閘道取得具有特定名稱的根信任憑證。</span><span class="sxs-lookup"><span data-stu-id="84dda-106">The **Get-AzApplicationGatewayTrustedRootCertificate** cmdlet gets Trusted Root Certificate with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="84dda-107">示例</span><span class="sxs-lookup"><span data-stu-id="84dda-107">EXAMPLES</span></span>

### <span data-ttu-id="84dda-108">範例1</span><span class="sxs-lookup"><span data-stu-id="84dda-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $trustedRootCert = Get-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\rootCA.cer"
```

<span data-ttu-id="84dda-109">第一個命令會取得應用程式閘道，並將它儲存在 $gw 變數中。</span><span class="sxs-lookup"><span data-stu-id="84dda-109">The first command gets the Application Gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="84dda-110">第二個命令會從應用程式閘道取得具有指定名稱的受根信任證書。</span><span class="sxs-lookup"><span data-stu-id="84dda-110">The second command gets the Trusted Root Certificate with a specified name from the Application Gateway.</span></span>

## <span data-ttu-id="84dda-111">參數</span><span class="sxs-lookup"><span data-stu-id="84dda-111">PARAMETERS</span></span>

### <span data-ttu-id="84dda-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="84dda-112">-ApplicationGateway</span></span>
<span data-ttu-id="84dda-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="84dda-113">The applicationGateway</span></span>

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

### <span data-ttu-id="84dda-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84dda-114">-DefaultProfile</span></span>
<span data-ttu-id="84dda-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="84dda-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84dda-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="84dda-116">-Name</span></span>
<span data-ttu-id="84dda-117">TrustedRoot 憑證的名稱</span><span class="sxs-lookup"><span data-stu-id="84dda-117">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="84dda-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84dda-118">CommonParameters</span></span>
<span data-ttu-id="84dda-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="84dda-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84dda-120">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="84dda-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84dda-121">輸入</span><span class="sxs-lookup"><span data-stu-id="84dda-121">INPUTS</span></span>

### <span data-ttu-id="84dda-122">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="84dda-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="84dda-123">輸出</span><span class="sxs-lookup"><span data-stu-id="84dda-123">OUTPUTS</span></span>

### <span data-ttu-id="84dda-124">PSApplicationGatewayTrustedRootCertificate 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="84dda-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="84dda-125">筆記</span><span class="sxs-lookup"><span data-stu-id="84dda-125">NOTES</span></span>

## <span data-ttu-id="84dda-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="84dda-126">RELATED LINKS</span></span>

[<span data-ttu-id="84dda-127">附加 AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="84dda-127">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="84dda-128">新-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="84dda-128">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="84dda-129">移除-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="84dda-129">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="84dda-130">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="84dda-130">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)
