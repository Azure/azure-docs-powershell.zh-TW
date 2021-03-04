---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: 3c9b9b97e26738234acdf2c8f09c0e1da5eae2e3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901958"
---
# <span data-ttu-id="ed0a0-101">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="ed0a0-101">Set-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="ed0a0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ed0a0-102">SYNOPSIS</span></span>
<span data-ttu-id="ed0a0-103">修改應用程式閘道的受信任的用戶端 CA 憑證鏈。</span><span class="sxs-lookup"><span data-stu-id="ed0a0-103">Modifies the trusted client CA certificate chain of an application gateway.</span></span>

## <span data-ttu-id="ed0a0-104">語法</span><span class="sxs-lookup"><span data-stu-id="ed0a0-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed0a0-105">描述</span><span class="sxs-lookup"><span data-stu-id="ed0a0-105">DESCRIPTION</span></span>
<span data-ttu-id="ed0a0-106">**Set-AzApplicationGatewayTrustedClientCertificate** Cmdlet 會修改應用程式閘道的受信任的用戶端 CA 憑證鏈。</span><span class="sxs-lookup"><span data-stu-id="ed0a0-106">The **Set-AzApplicationGatewayTrustedClientCertificate** cmdlet modifies the trusted client CA certificate chain of an application gateway.</span></span>

## <span data-ttu-id="ed0a0-107">例子</span><span class="sxs-lookup"><span data-stu-id="ed0a0-107">EXAMPLES</span></span>

### <span data-ttu-id="ed0a0-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="ed0a0-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Set-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\clientCAUpdated.cer"
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="ed0a0-109">上述範例案例顯示如何更新現有的信任用戶端 CA 憑證鏈物件。</span><span class="sxs-lookup"><span data-stu-id="ed0a0-109">Above example scenarios shows how to update an existing trusted client CA certificate chain object.</span></span> <span data-ttu-id="ed0a0-110">第一個命令會獲得應用程式閘道，並儲存在$gw變數。</span><span class="sxs-lookup"><span data-stu-id="ed0a0-110">The first command gets an application gateway and stores it in the $gw variable.</span></span> <span data-ttu-id="ed0a0-111">第二個命令會使用新的 CA 憑證鏈檔案修改現有的信任用戶端 CA 憑證鏈物件。</span><span class="sxs-lookup"><span data-stu-id="ed0a0-111">The second command modifies the existing trusted client CA certificate chain object with a new CA certificate chain file.</span></span> <span data-ttu-id="ed0a0-112">第三個命令會更新 Azure 上的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="ed0a0-112">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="ed0a0-113">參數</span><span class="sxs-lookup"><span data-stu-id="ed0a0-113">PARAMETERS</span></span>

### <span data-ttu-id="ed0a0-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ed0a0-114">-ApplicationGateway</span></span>
<span data-ttu-id="ed0a0-115">應用程式Gateway</span><span class="sxs-lookup"><span data-stu-id="ed0a0-115">The applicationGateway</span></span>

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

### <span data-ttu-id="ed0a0-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="ed0a0-116">-CertificateFile</span></span>
<span data-ttu-id="ed0a0-117">信任的用戶端 CA 憑證鏈檔案的路徑</span><span class="sxs-lookup"><span data-stu-id="ed0a0-117">Path of the trusted client CA certificate chain file</span></span>

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

### <span data-ttu-id="ed0a0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed0a0-118">-DefaultProfile</span></span>
<span data-ttu-id="ed0a0-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ed0a0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed0a0-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="ed0a0-120">-Name</span></span>
<span data-ttu-id="ed0a0-121">信任的用戶端 CA 憑證鏈的名稱</span><span class="sxs-lookup"><span data-stu-id="ed0a0-121">The name of the trusted client CA certificate chain</span></span>

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

### <span data-ttu-id="ed0a0-122">-確認</span><span class="sxs-lookup"><span data-stu-id="ed0a0-122">-Confirm</span></span>
<span data-ttu-id="ed0a0-123">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ed0a0-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed0a0-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed0a0-124">-WhatIf</span></span>
<span data-ttu-id="ed0a0-125">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ed0a0-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed0a0-126">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ed0a0-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed0a0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed0a0-127">CommonParameters</span></span>
<span data-ttu-id="ed0a0-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ed0a0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed0a0-129">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ed0a0-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed0a0-130">輸入</span><span class="sxs-lookup"><span data-stu-id="ed0a0-130">INPUTS</span></span>

### <span data-ttu-id="ed0a0-131">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ed0a0-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ed0a0-132">輸出</span><span class="sxs-lookup"><span data-stu-id="ed0a0-132">OUTPUTS</span></span>

### <span data-ttu-id="ed0a0-133">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ed0a0-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ed0a0-134">筆記</span><span class="sxs-lookup"><span data-stu-id="ed0a0-134">NOTES</span></span>

## <span data-ttu-id="ed0a0-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="ed0a0-135">RELATED LINKS</span></span>

[<span data-ttu-id="ed0a0-136">Add-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="ed0a0-136">Add-AzApplicationGatewayTrustedClientCertificate</span></span>](./Add-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="ed0a0-137">New-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="ed0a0-137">New-AzApplicationGatewayTrustedClientCertificate</span></span>](./New-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="ed0a0-138">Get-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="ed0a0-138">Get-AzApplicationGatewayTrustedClientCertificate</span></span>](./Get-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="ed0a0-139">Remove-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="ed0a0-139">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>](./Remove-AzApplicationGatewayTrustedClientCertificate.md)