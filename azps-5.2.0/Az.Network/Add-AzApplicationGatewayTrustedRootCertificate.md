---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: f5e8624beeb8053cbf054526cddc24c7da6cdf3f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98281012"
---
# <span data-ttu-id="af60c-101">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="af60c-101">Add-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="af60c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="af60c-102">SYNOPSIS</span></span>
<span data-ttu-id="af60c-103">將信任的根憑證新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="af60c-103">Adds a trusted root certificate to an application gateway.</span></span>

## <span data-ttu-id="af60c-104">句法</span><span class="sxs-lookup"><span data-stu-id="af60c-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af60c-105">說明</span><span class="sxs-lookup"><span data-stu-id="af60c-105">DESCRIPTION</span></span>
<span data-ttu-id="af60c-106">**AzApplicationGatewayTrustedRootCertificate** Cmdlet 會將信任的根憑證新增至 Azure 應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="af60c-106">The **Add-AzApplicationGatewayTrustedRootCertificate** cmdlet adds a trusted root certificate to an Azure application gateway.</span></span>

## <span data-ttu-id="af60c-107">示例</span><span class="sxs-lookup"><span data-stu-id="af60c-107">EXAMPLES</span></span>

### <span data-ttu-id="af60c-108">範例1</span><span class="sxs-lookup"><span data-stu-id="af60c-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Add-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName -CertificateFile ".\rootCA.cer"
PS C:\> $gw = Add-AzApplicationGatewayBackendHttpSettings -ApplicationGateway $gw -Name $poolSetting01Name -Port 443 -Protocol Https -CookieBasedAffinity Enabled -PickHostNameFromBackendAddress -TrustedRootCertificate $gw.TrustedRootCertificates[0]
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="af60c-109">第一個命令會取得應用程式閘道，並將它儲存在 $gw 變數中。</span><span class="sxs-lookup"><span data-stu-id="af60c-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="af60c-110">第二個命令會將新的受根信任憑證新增至應用程式閘道，並將根憑證的路徑做為輸入。</span><span class="sxs-lookup"><span data-stu-id="af60c-110">The second command adds a new trusted root certificate to Application Gateway taking path of the root certificate as input.</span></span>
<span data-ttu-id="af60c-111">第三個命令會使用信任的根憑證來建立新的後端 HTTP 設定，以驗證後端伺服器憑證。</span><span class="sxs-lookup"><span data-stu-id="af60c-111">The third command creates new backend http setting using trusted root certificate for validating the backend server certificate against.</span></span>
<span data-ttu-id="af60c-112">第四個命令會更新應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="af60c-112">The fourth command updates the Application Gateway.</span></span>

## <span data-ttu-id="af60c-113">參數</span><span class="sxs-lookup"><span data-stu-id="af60c-113">PARAMETERS</span></span>

### <span data-ttu-id="af60c-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="af60c-114">-ApplicationGateway</span></span>
<span data-ttu-id="af60c-115">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="af60c-115">The applicationGateway</span></span>

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

### <span data-ttu-id="af60c-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="af60c-116">-CertificateFile</span></span>
<span data-ttu-id="af60c-117">憑證 CER 檔案的路徑</span><span class="sxs-lookup"><span data-stu-id="af60c-117">Path of certificate CER file</span></span>

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

### <span data-ttu-id="af60c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af60c-118">-DefaultProfile</span></span>
<span data-ttu-id="af60c-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="af60c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af60c-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="af60c-120">-Name</span></span>
<span data-ttu-id="af60c-121">TrustedRoot 憑證的名稱</span><span class="sxs-lookup"><span data-stu-id="af60c-121">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="af60c-122">-確認</span><span class="sxs-lookup"><span data-stu-id="af60c-122">-Confirm</span></span>
<span data-ttu-id="af60c-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="af60c-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af60c-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af60c-124">-WhatIf</span></span>
<span data-ttu-id="af60c-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="af60c-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af60c-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="af60c-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af60c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af60c-127">CommonParameters</span></span>
<span data-ttu-id="af60c-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="af60c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af60c-129">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="af60c-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af60c-130">輸入</span><span class="sxs-lookup"><span data-stu-id="af60c-130">INPUTS</span></span>

### <span data-ttu-id="af60c-131">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="af60c-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="af60c-132">輸出</span><span class="sxs-lookup"><span data-stu-id="af60c-132">OUTPUTS</span></span>

### <span data-ttu-id="af60c-133">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="af60c-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="af60c-134">筆記</span><span class="sxs-lookup"><span data-stu-id="af60c-134">NOTES</span></span>

## <span data-ttu-id="af60c-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="af60c-135">RELATED LINKS</span></span>

[<span data-ttu-id="af60c-136">AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="af60c-136">Get-AzApplicationGatewayTrustedRootCertificate</span></span>](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="af60c-137">新-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="af60c-137">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="af60c-138">移除-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="af60c-138">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="af60c-139">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="af60c-139">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)
