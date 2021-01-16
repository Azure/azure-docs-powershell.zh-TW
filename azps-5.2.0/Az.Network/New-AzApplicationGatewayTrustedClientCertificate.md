---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: 285e9c343ed18d4aa21c328344b7be82319f0d3b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98281914"
---
# <span data-ttu-id="39080-101">New-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="39080-101">New-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="39080-102">摘要</span><span class="sxs-lookup"><span data-stu-id="39080-102">SYNOPSIS</span></span>
<span data-ttu-id="39080-103">為應用程式閘道建立信任的用戶端 CA 憑證鏈。</span><span class="sxs-lookup"><span data-stu-id="39080-103">Creates a trusted client CA certificate chain for an application gateway.</span></span>

## <span data-ttu-id="39080-104">句法</span><span class="sxs-lookup"><span data-stu-id="39080-104">SYNTAX</span></span>

```
New-AzApplicationGatewayTrustedClientCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39080-105">說明</span><span class="sxs-lookup"><span data-stu-id="39080-105">DESCRIPTION</span></span>
<span data-ttu-id="39080-106">New-AzApplicationGatewayTrustedClientCertificate Cmdlet 會為應用程式閘道建立信任的用戶端 CA 憑證鏈。</span><span class="sxs-lookup"><span data-stu-id="39080-106">The New-AzApplicationGatewayTrustedClientCertificate cmdlet creates a trusted client CA certificate chain for an application gateway.</span></span>

## <span data-ttu-id="39080-107">示例</span><span class="sxs-lookup"><span data-stu-id="39080-107">EXAMPLES</span></span>

### <span data-ttu-id="39080-108">範例1</span><span class="sxs-lookup"><span data-stu-id="39080-108">Example 1</span></span>
```powershell
PS C:\> $trustedClient = New-AzApplicationGatewayTrustedClientCertificate -Name "ClientCert" -CertificateFile "C:\clientCAChain.cer"
```
<span data-ttu-id="39080-109">此命令會建立新的信任用戶端 CA 憑證鏈物件，並將用戶端 CA 憑證的路徑做為輸入。</span><span class="sxs-lookup"><span data-stu-id="39080-109">The command creates a new trusted client CA certificate chain object taking path of the client CA certificate as input.</span></span>

## <span data-ttu-id="39080-110">參數</span><span class="sxs-lookup"><span data-stu-id="39080-110">PARAMETERS</span></span>

### <span data-ttu-id="39080-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="39080-111">-CertificateFile</span></span>
<span data-ttu-id="39080-112">受信任的用戶端 CA 憑證鏈檔案的路徑</span><span class="sxs-lookup"><span data-stu-id="39080-112">Path of the trusted client CA certificate chain file</span></span>

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

### <span data-ttu-id="39080-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39080-113">-DefaultProfile</span></span>
<span data-ttu-id="39080-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="39080-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39080-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="39080-115">-Name</span></span>
<span data-ttu-id="39080-116">受信任的用戶端 CA 憑證鏈的名稱</span><span class="sxs-lookup"><span data-stu-id="39080-116">The name of the trusted client CA certificate chain</span></span>

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

### <span data-ttu-id="39080-117">-確認</span><span class="sxs-lookup"><span data-stu-id="39080-117">-Confirm</span></span>
<span data-ttu-id="39080-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="39080-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39080-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39080-119">-WhatIf</span></span>
<span data-ttu-id="39080-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="39080-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39080-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="39080-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39080-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39080-122">CommonParameters</span></span>
<span data-ttu-id="39080-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="39080-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39080-124">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="39080-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39080-125">輸入</span><span class="sxs-lookup"><span data-stu-id="39080-125">INPUTS</span></span>

### <span data-ttu-id="39080-126">所有</span><span class="sxs-lookup"><span data-stu-id="39080-126">None</span></span>

## <span data-ttu-id="39080-127">輸出</span><span class="sxs-lookup"><span data-stu-id="39080-127">OUTPUTS</span></span>

### <span data-ttu-id="39080-128">PSApplicationGatewayTrustedClientCertificate 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="39080-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="39080-129">筆記</span><span class="sxs-lookup"><span data-stu-id="39080-129">NOTES</span></span>

## <span data-ttu-id="39080-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="39080-130">RELATED LINKS</span></span>

[<span data-ttu-id="39080-131">附加 AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="39080-131">Add-AzApplicationGatewayTrustedClientCertificate</span></span>](./Add-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="39080-132">AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="39080-132">Get-AzApplicationGatewayTrustedClientCertificate</span></span>](./Get-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="39080-133">移除-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="39080-133">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>](./Remove-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="39080-134">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="39080-134">Set-AzApplicationGatewayTrustedClientCertificate</span></span>](./Set-AzApplicationGatewayTrustedClientCertificate.md)