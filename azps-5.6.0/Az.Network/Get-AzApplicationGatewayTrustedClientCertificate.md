---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: b9522cf7bc29f01215cbac7473c58643b8d63b5b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912753"
---
# <span data-ttu-id="cc989-101">Get-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="cc989-101">Get-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="cc989-102">簡介</span><span class="sxs-lookup"><span data-stu-id="cc989-102">SYNOPSIS</span></span>
<span data-ttu-id="cc989-103">從應用程式閘道中，以特定名稱獲得信任的用戶端 CA 憑證鏈。</span><span class="sxs-lookup"><span data-stu-id="cc989-103">Gets the trusted client CA certificate chain with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="cc989-104">語法</span><span class="sxs-lookup"><span data-stu-id="cc989-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayTrustedClientCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cc989-105">描述</span><span class="sxs-lookup"><span data-stu-id="cc989-105">DESCRIPTION</span></span>
<span data-ttu-id="cc989-106">此Get-AzApplicationGatewayTrustedClientCertificate Cmdlet 會從應用程式閘道獲得具有特定名稱的受信任的用戶端 CA 憑證鏈。</span><span class="sxs-lookup"><span data-stu-id="cc989-106">The Get-AzApplicationGatewayTrustedClientCertificate cmdlet gets the trusted client CA certificate chain with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="cc989-107">例子</span><span class="sxs-lookup"><span data-stu-id="cc989-107">EXAMPLES</span></span>

### <span data-ttu-id="cc989-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="cc989-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $trustedClientCert = Get-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway $gw -Name $certName
```

<span data-ttu-id="cc989-109">第一個命令會獲得應用程式閘道，並儲存在$gw變數中。</span><span class="sxs-lookup"><span data-stu-id="cc989-109">The first command gets the Application Gateway and stores it in $gw variable.</span></span> <span data-ttu-id="cc989-110">第二個命令會從應用程式閘道獲得具有指定名稱的受信任用戶端 CA 憑證鏈。</span><span class="sxs-lookup"><span data-stu-id="cc989-110">The second command gets the trusted client CA certificate chain with a specified name from the Application Gateway.</span></span>

## <span data-ttu-id="cc989-111">參數</span><span class="sxs-lookup"><span data-stu-id="cc989-111">PARAMETERS</span></span>

### <span data-ttu-id="cc989-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cc989-112">-ApplicationGateway</span></span>
<span data-ttu-id="cc989-113">應用程式Gateway</span><span class="sxs-lookup"><span data-stu-id="cc989-113">The applicationGateway</span></span>

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

### <span data-ttu-id="cc989-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc989-114">-DefaultProfile</span></span>
<span data-ttu-id="cc989-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="cc989-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc989-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="cc989-116">-Name</span></span>
<span data-ttu-id="cc989-117">信任的用戶端 CA 憑證鏈的名稱</span><span class="sxs-lookup"><span data-stu-id="cc989-117">The name of the trusted client CA certificate chain</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc989-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc989-118">CommonParameters</span></span>
<span data-ttu-id="cc989-119">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="cc989-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc989-120">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cc989-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc989-121">輸入</span><span class="sxs-lookup"><span data-stu-id="cc989-121">INPUTS</span></span>

### <span data-ttu-id="cc989-122">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cc989-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="cc989-123">輸出</span><span class="sxs-lookup"><span data-stu-id="cc989-123">OUTPUTS</span></span>

### <span data-ttu-id="cc989-124">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="cc989-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="cc989-125">筆記</span><span class="sxs-lookup"><span data-stu-id="cc989-125">NOTES</span></span>

## <span data-ttu-id="cc989-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="cc989-126">RELATED LINKS</span></span>

[<span data-ttu-id="cc989-127">New-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="cc989-127">New-AzApplicationGatewayTrustedClientCertificate</span></span>](./New-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="cc989-128">Add-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="cc989-128">Add-AzApplicationGatewayTrustedClientCertificate</span></span>](./Add-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="cc989-129">Remove-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="cc989-129">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>](./Remove-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="cc989-130">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="cc989-130">Set-AzApplicationGatewayTrustedClientCertificate</span></span>](./Set-AzApplicationGatewayTrustedClientCertificate.md)