---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: 99d56b837b67fe8b816c4f27c8658932a74452e7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98277851"
---
# <span data-ttu-id="31dc1-101">Get-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="31dc1-101">Get-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="31dc1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="31dc1-102">SYNOPSIS</span></span>
<span data-ttu-id="31dc1-103">從應用程式閘道取得具有特定名稱的可信用戶端 CA 憑證鏈。</span><span class="sxs-lookup"><span data-stu-id="31dc1-103">Gets the trusted client CA certificate chain with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="31dc1-104">句法</span><span class="sxs-lookup"><span data-stu-id="31dc1-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayTrustedClientCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31dc1-105">說明</span><span class="sxs-lookup"><span data-stu-id="31dc1-105">DESCRIPTION</span></span>
<span data-ttu-id="31dc1-106">Get-AzApplicationGatewayTrustedClientCertificate Cmdlet 會從應用程式閘道取得具有特定名稱的受信任用戶端 CA 憑證鏈。</span><span class="sxs-lookup"><span data-stu-id="31dc1-106">The Get-AzApplicationGatewayTrustedClientCertificate cmdlet gets the trusted client CA certificate chain with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="31dc1-107">示例</span><span class="sxs-lookup"><span data-stu-id="31dc1-107">EXAMPLES</span></span>

### <span data-ttu-id="31dc1-108">範例1</span><span class="sxs-lookup"><span data-stu-id="31dc1-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $trustedClientCert = Get-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway $gw -Name $certName
```

<span data-ttu-id="31dc1-109">第一個命令會取得應用程式閘道，並將它儲存在 $gw 變數中。</span><span class="sxs-lookup"><span data-stu-id="31dc1-109">The first command gets the Application Gateway and stores it in $gw variable.</span></span> <span data-ttu-id="31dc1-110">第二個命令會從應用程式閘道取得具有指定名稱的可信用戶端 CA 憑證鏈。</span><span class="sxs-lookup"><span data-stu-id="31dc1-110">The second command gets the trusted client CA certificate chain with a specified name from the Application Gateway.</span></span>

## <span data-ttu-id="31dc1-111">參數</span><span class="sxs-lookup"><span data-stu-id="31dc1-111">PARAMETERS</span></span>

### <span data-ttu-id="31dc1-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="31dc1-112">-ApplicationGateway</span></span>
<span data-ttu-id="31dc1-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="31dc1-113">The applicationGateway</span></span>

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

### <span data-ttu-id="31dc1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31dc1-114">-DefaultProfile</span></span>
<span data-ttu-id="31dc1-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="31dc1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31dc1-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="31dc1-116">-Name</span></span>
<span data-ttu-id="31dc1-117">受信任的用戶端 CA 憑證鏈的名稱</span><span class="sxs-lookup"><span data-stu-id="31dc1-117">The name of the trusted client CA certificate chain</span></span>

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

### <span data-ttu-id="31dc1-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31dc1-118">CommonParameters</span></span>
<span data-ttu-id="31dc1-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="31dc1-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31dc1-120">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="31dc1-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31dc1-121">輸入</span><span class="sxs-lookup"><span data-stu-id="31dc1-121">INPUTS</span></span>

### <span data-ttu-id="31dc1-122">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="31dc1-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="31dc1-123">輸出</span><span class="sxs-lookup"><span data-stu-id="31dc1-123">OUTPUTS</span></span>

### <span data-ttu-id="31dc1-124">PSApplicationGatewayTrustedClientCertificate 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="31dc1-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="31dc1-125">筆記</span><span class="sxs-lookup"><span data-stu-id="31dc1-125">NOTES</span></span>

## <span data-ttu-id="31dc1-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="31dc1-126">RELATED LINKS</span></span>

[<span data-ttu-id="31dc1-127">新-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="31dc1-127">New-AzApplicationGatewayTrustedClientCertificate</span></span>](./New-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="31dc1-128">附加 AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="31dc1-128">Add-AzApplicationGatewayTrustedClientCertificate</span></span>](./Add-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="31dc1-129">移除-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="31dc1-129">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>](./Remove-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="31dc1-130">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="31dc1-130">Set-AzApplicationGatewayTrustedClientCertificate</span></span>](./Set-AzApplicationGatewayTrustedClientCertificate.md)