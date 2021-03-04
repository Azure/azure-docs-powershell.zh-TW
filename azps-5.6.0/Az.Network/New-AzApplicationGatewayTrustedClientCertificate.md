---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: e34d170167aac09cd64ca11d0838f36fc0515423
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911633"
---
# <span data-ttu-id="87992-101">New-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="87992-101">New-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="87992-102">簡介</span><span class="sxs-lookup"><span data-stu-id="87992-102">SYNOPSIS</span></span>
<span data-ttu-id="87992-103">為應用程式閘道建立信任的用戶端 CA 憑證鏈。</span><span class="sxs-lookup"><span data-stu-id="87992-103">Creates a trusted client CA certificate chain for an application gateway.</span></span>

## <span data-ttu-id="87992-104">語法</span><span class="sxs-lookup"><span data-stu-id="87992-104">SYNTAX</span></span>

```
New-AzApplicationGatewayTrustedClientCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87992-105">描述</span><span class="sxs-lookup"><span data-stu-id="87992-105">DESCRIPTION</span></span>
<span data-ttu-id="87992-106">Cmdlet New-AzApplicationGatewayTrustedClientCertificate為應用程式閘道建立信任的用戶端 CA 憑證鏈。</span><span class="sxs-lookup"><span data-stu-id="87992-106">The New-AzApplicationGatewayTrustedClientCertificate cmdlet creates a trusted client CA certificate chain for an application gateway.</span></span>

## <span data-ttu-id="87992-107">例子</span><span class="sxs-lookup"><span data-stu-id="87992-107">EXAMPLES</span></span>

### <span data-ttu-id="87992-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="87992-108">Example 1</span></span>
```powershell
PS C:\> $trustedClient = New-AzApplicationGatewayTrustedClientCertificate -Name "ClientCert" -CertificateFile "C:\clientCAChain.cer"
```
<span data-ttu-id="87992-109">該命令會建立一個新的信任的用戶端 CA 憑證鏈物件，以用戶端 CA 憑證的路徑做為輸入。</span><span class="sxs-lookup"><span data-stu-id="87992-109">The command creates a new trusted client CA certificate chain object taking path of the client CA certificate as input.</span></span>

## <span data-ttu-id="87992-110">參數</span><span class="sxs-lookup"><span data-stu-id="87992-110">PARAMETERS</span></span>

### <span data-ttu-id="87992-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="87992-111">-CertificateFile</span></span>
<span data-ttu-id="87992-112">信任的用戶端 CA 憑證鏈檔案的路徑</span><span class="sxs-lookup"><span data-stu-id="87992-112">Path of the trusted client CA certificate chain file</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87992-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87992-113">-DefaultProfile</span></span>
<span data-ttu-id="87992-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="87992-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87992-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="87992-115">-Name</span></span>
<span data-ttu-id="87992-116">信任的用戶端 CA 憑證鏈的名稱</span><span class="sxs-lookup"><span data-stu-id="87992-116">The name of the trusted client CA certificate chain</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87992-117">-確認</span><span class="sxs-lookup"><span data-stu-id="87992-117">-Confirm</span></span>
<span data-ttu-id="87992-118">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="87992-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87992-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87992-119">-WhatIf</span></span>
<span data-ttu-id="87992-120">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="87992-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87992-121">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="87992-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87992-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87992-122">CommonParameters</span></span>
<span data-ttu-id="87992-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="87992-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87992-124">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="87992-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87992-125">輸入</span><span class="sxs-lookup"><span data-stu-id="87992-125">INPUTS</span></span>

### <span data-ttu-id="87992-126">沒有</span><span class="sxs-lookup"><span data-stu-id="87992-126">None</span></span>

## <span data-ttu-id="87992-127">輸出</span><span class="sxs-lookup"><span data-stu-id="87992-127">OUTPUTS</span></span>

### <span data-ttu-id="87992-128">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="87992-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="87992-129">筆記</span><span class="sxs-lookup"><span data-stu-id="87992-129">NOTES</span></span>

## <span data-ttu-id="87992-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="87992-130">RELATED LINKS</span></span>

[<span data-ttu-id="87992-131">Add-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="87992-131">Add-AzApplicationGatewayTrustedClientCertificate</span></span>](./Add-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="87992-132">Get-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="87992-132">Get-AzApplicationGatewayTrustedClientCertificate</span></span>](./Get-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="87992-133">Remove-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="87992-133">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>](./Remove-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="87992-134">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="87992-134">Set-AzApplicationGatewayTrustedClientCertificate</span></span>](./Set-AzApplicationGatewayTrustedClientCertificate.md)