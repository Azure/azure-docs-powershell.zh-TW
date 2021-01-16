---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: 5f52b68e538072e6ff6aecde99f59337b532130c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98277419"
---
# <span data-ttu-id="f2ecf-101">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="f2ecf-101">Set-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="f2ecf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f2ecf-102">SYNOPSIS</span></span>
<span data-ttu-id="f2ecf-103">修改應用程式閘道的信任用戶端 CA 憑證鏈。</span><span class="sxs-lookup"><span data-stu-id="f2ecf-103">Modifies the trusted client CA certificate chain of an application gateway.</span></span>

## <span data-ttu-id="f2ecf-104">句法</span><span class="sxs-lookup"><span data-stu-id="f2ecf-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2ecf-105">說明</span><span class="sxs-lookup"><span data-stu-id="f2ecf-105">DESCRIPTION</span></span>
<span data-ttu-id="f2ecf-106">**AzApplicationGatewayTrustedClientCertificate** Cmdlet 會修改應用程式閘道的信任用戶端 CA 憑證鏈。</span><span class="sxs-lookup"><span data-stu-id="f2ecf-106">The **Set-AzApplicationGatewayTrustedClientCertificate** cmdlet modifies the trusted client CA certificate chain of an application gateway.</span></span>

## <span data-ttu-id="f2ecf-107">示例</span><span class="sxs-lookup"><span data-stu-id="f2ecf-107">EXAMPLES</span></span>

### <span data-ttu-id="f2ecf-108">範例1</span><span class="sxs-lookup"><span data-stu-id="f2ecf-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Set-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\clientCAUpdated.cer"
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="f2ecf-109">上述範例案例說明如何更新現有的信任用戶端 CA 憑證鏈物件。</span><span class="sxs-lookup"><span data-stu-id="f2ecf-109">Above example scenarios shows how to update an existing trusted client CA certificate chain object.</span></span> <span data-ttu-id="f2ecf-110">第一個命令會取得應用程式閘道，並將它儲存在 $gw 變數中。</span><span class="sxs-lookup"><span data-stu-id="f2ecf-110">The first command gets an application gateway and stores it in the $gw variable.</span></span> <span data-ttu-id="f2ecf-111">第二個命令會使用新的 CA 憑證連結檔案來修改現有的信任用戶端 CA 憑證鏈物件。</span><span class="sxs-lookup"><span data-stu-id="f2ecf-111">The second command modifies the existing trusted client CA certificate chain object with a new CA certificate chain file.</span></span> <span data-ttu-id="f2ecf-112">第三個命令會更新 Azure 上的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="f2ecf-112">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="f2ecf-113">參數</span><span class="sxs-lookup"><span data-stu-id="f2ecf-113">PARAMETERS</span></span>

### <span data-ttu-id="f2ecf-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f2ecf-114">-ApplicationGateway</span></span>
<span data-ttu-id="f2ecf-115">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f2ecf-115">The applicationGateway</span></span>

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

### <span data-ttu-id="f2ecf-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="f2ecf-116">-CertificateFile</span></span>
<span data-ttu-id="f2ecf-117">受信任的用戶端 CA 憑證鏈檔案的路徑</span><span class="sxs-lookup"><span data-stu-id="f2ecf-117">Path of the trusted client CA certificate chain file</span></span>

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

### <span data-ttu-id="f2ecf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2ecf-118">-DefaultProfile</span></span>
<span data-ttu-id="f2ecf-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f2ecf-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2ecf-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="f2ecf-120">-Name</span></span>
<span data-ttu-id="f2ecf-121">受信任的用戶端 CA 憑證鏈的名稱</span><span class="sxs-lookup"><span data-stu-id="f2ecf-121">The name of the trusted client CA certificate chain</span></span>

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

### <span data-ttu-id="f2ecf-122">-確認</span><span class="sxs-lookup"><span data-stu-id="f2ecf-122">-Confirm</span></span>
<span data-ttu-id="f2ecf-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f2ecf-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2ecf-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2ecf-124">-WhatIf</span></span>
<span data-ttu-id="f2ecf-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f2ecf-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2ecf-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f2ecf-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2ecf-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2ecf-127">CommonParameters</span></span>
<span data-ttu-id="f2ecf-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f2ecf-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2ecf-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f2ecf-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2ecf-130">輸入</span><span class="sxs-lookup"><span data-stu-id="f2ecf-130">INPUTS</span></span>

### <span data-ttu-id="f2ecf-131">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f2ecf-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f2ecf-132">輸出</span><span class="sxs-lookup"><span data-stu-id="f2ecf-132">OUTPUTS</span></span>

### <span data-ttu-id="f2ecf-133">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f2ecf-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f2ecf-134">筆記</span><span class="sxs-lookup"><span data-stu-id="f2ecf-134">NOTES</span></span>

## <span data-ttu-id="f2ecf-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="f2ecf-135">RELATED LINKS</span></span>

[<span data-ttu-id="f2ecf-136">附加 AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="f2ecf-136">Add-AzApplicationGatewayTrustedClientCertificate</span></span>](./Add-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="f2ecf-137">新-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="f2ecf-137">New-AzApplicationGatewayTrustedClientCertificate</span></span>](./New-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="f2ecf-138">AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="f2ecf-138">Get-AzApplicationGatewayTrustedClientCertificate</span></span>](./Get-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="f2ecf-139">移除-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="f2ecf-139">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>](./Remove-AzApplicationGatewayTrustedClientCertificate.md)