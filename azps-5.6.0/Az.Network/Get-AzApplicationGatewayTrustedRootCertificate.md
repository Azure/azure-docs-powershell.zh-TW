---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: f040110ea3e00e99b989c07e8757d3c3a0c4b976
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912750"
---
# <span data-ttu-id="a9b97-101">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="a9b97-101">Get-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="a9b97-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a9b97-102">SYNOPSIS</span></span>
<span data-ttu-id="a9b97-103">從應用程式閘道中，以特定名稱獲得信任的根憑證。</span><span class="sxs-lookup"><span data-stu-id="a9b97-103">Gets the Trusted Root Certificate with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="a9b97-104">語法</span><span class="sxs-lookup"><span data-stu-id="a9b97-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayTrustedRootCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9b97-105">描述</span><span class="sxs-lookup"><span data-stu-id="a9b97-105">DESCRIPTION</span></span>
<span data-ttu-id="a9b97-106">**Get-AzApplicationGatewayTrustedRootCertificate** Cmdlet 會從應用程式閘道取得具有特定名稱的受根信任憑證。</span><span class="sxs-lookup"><span data-stu-id="a9b97-106">The **Get-AzApplicationGatewayTrustedRootCertificate** cmdlet gets Trusted Root Certificate with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="a9b97-107">例子</span><span class="sxs-lookup"><span data-stu-id="a9b97-107">EXAMPLES</span></span>

### <span data-ttu-id="a9b97-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="a9b97-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $trustedRootCert = Get-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\rootCA.cer"
```

<span data-ttu-id="a9b97-109">第一個命令會獲得應用程式閘道，並儲存在$gw變數中。</span><span class="sxs-lookup"><span data-stu-id="a9b97-109">The first command gets the Application Gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="a9b97-110">第二個命令會從應用程式閘道獲得具有指定名稱的受根信任憑證。</span><span class="sxs-lookup"><span data-stu-id="a9b97-110">The second command gets the Trusted Root Certificate with a specified name from the Application Gateway.</span></span>

## <span data-ttu-id="a9b97-111">參數</span><span class="sxs-lookup"><span data-stu-id="a9b97-111">PARAMETERS</span></span>

### <span data-ttu-id="a9b97-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a9b97-112">-ApplicationGateway</span></span>
<span data-ttu-id="a9b97-113">應用程式Gateway</span><span class="sxs-lookup"><span data-stu-id="a9b97-113">The applicationGateway</span></span>

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

### <span data-ttu-id="a9b97-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9b97-114">-DefaultProfile</span></span>
<span data-ttu-id="a9b97-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a9b97-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9b97-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="a9b97-116">-Name</span></span>
<span data-ttu-id="a9b97-117">TrustedRoot 憑證的名稱</span><span class="sxs-lookup"><span data-stu-id="a9b97-117">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="a9b97-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9b97-118">CommonParameters</span></span>
<span data-ttu-id="a9b97-119">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a9b97-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9b97-120">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a9b97-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9b97-121">輸入</span><span class="sxs-lookup"><span data-stu-id="a9b97-121">INPUTS</span></span>

### <span data-ttu-id="a9b97-122">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a9b97-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a9b97-123">輸出</span><span class="sxs-lookup"><span data-stu-id="a9b97-123">OUTPUTS</span></span>

### <span data-ttu-id="a9b97-124">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="a9b97-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="a9b97-125">筆記</span><span class="sxs-lookup"><span data-stu-id="a9b97-125">NOTES</span></span>

## <span data-ttu-id="a9b97-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="a9b97-126">RELATED LINKS</span></span>

[<span data-ttu-id="a9b97-127">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="a9b97-127">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="a9b97-128">New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="a9b97-128">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="a9b97-129">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="a9b97-129">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="a9b97-130">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="a9b97-130">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)
