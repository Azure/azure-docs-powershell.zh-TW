---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: e8bb89f90772006ceb567ff235746a778c840bdd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911638"
---
# <span data-ttu-id="1fe76-101">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="1fe76-101">Add-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="1fe76-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1fe76-102">SYNOPSIS</span></span>
<span data-ttu-id="1fe76-103">新增信任的根憑證至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="1fe76-103">Adds a trusted root certificate to an application gateway.</span></span>

## <span data-ttu-id="1fe76-104">語法</span><span class="sxs-lookup"><span data-stu-id="1fe76-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1fe76-105">描述</span><span class="sxs-lookup"><span data-stu-id="1fe76-105">DESCRIPTION</span></span>
<span data-ttu-id="1fe76-106">**Add-AzApplicationGatewayTrustedRootCertificate** Cmdlet 會新增信任的根憑證至 Azure 應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="1fe76-106">The **Add-AzApplicationGatewayTrustedRootCertificate** cmdlet adds a trusted root certificate to an Azure application gateway.</span></span>

## <span data-ttu-id="1fe76-107">例子</span><span class="sxs-lookup"><span data-stu-id="1fe76-107">EXAMPLES</span></span>

### <span data-ttu-id="1fe76-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="1fe76-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Add-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName -CertificateFile ".\rootCA.cer"
PS C:\> $gw = Add-AzApplicationGatewayBackendHttpSettings -ApplicationGateway $gw -Name $poolSetting01Name -Port 443 -Protocol Https -CookieBasedAffinity Enabled -PickHostNameFromBackendAddress -TrustedRootCertificate $gw.TrustedRootCertificates[0]
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="1fe76-109">第一個命令會獲得應用程式閘道，並儲存在$gw變數中。</span><span class="sxs-lookup"><span data-stu-id="1fe76-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="1fe76-110">第二個命令會將新的根信任憑證新增到應用程式閘道，以根憑證的路徑做為輸入。</span><span class="sxs-lookup"><span data-stu-id="1fe76-110">The second command adds a new trusted root certificate to Application Gateway taking path of the root certificate as input.</span></span>
<span data-ttu-id="1fe76-111">第三個命令會使用信任的根憑證來驗證後端伺服器憑證，以建立新的後端 HTTP 設定。</span><span class="sxs-lookup"><span data-stu-id="1fe76-111">The third command creates new backend http setting using trusted root certificate for validating the backend server certificate against.</span></span>
<span data-ttu-id="1fe76-112">第四個命令會更新應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="1fe76-112">The fourth command updates the Application Gateway.</span></span>

## <span data-ttu-id="1fe76-113">參數</span><span class="sxs-lookup"><span data-stu-id="1fe76-113">PARAMETERS</span></span>

### <span data-ttu-id="1fe76-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1fe76-114">-ApplicationGateway</span></span>
<span data-ttu-id="1fe76-115">應用程式Gateway</span><span class="sxs-lookup"><span data-stu-id="1fe76-115">The applicationGateway</span></span>

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

### <span data-ttu-id="1fe76-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="1fe76-116">-CertificateFile</span></span>
<span data-ttu-id="1fe76-117">憑證憑證檔案的路徑</span><span class="sxs-lookup"><span data-stu-id="1fe76-117">Path of certificate CER file</span></span>

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

### <span data-ttu-id="1fe76-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fe76-118">-DefaultProfile</span></span>
<span data-ttu-id="1fe76-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="1fe76-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1fe76-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="1fe76-120">-Name</span></span>
<span data-ttu-id="1fe76-121">TrustedRoot 憑證的名稱</span><span class="sxs-lookup"><span data-stu-id="1fe76-121">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="1fe76-122">-確認</span><span class="sxs-lookup"><span data-stu-id="1fe76-122">-Confirm</span></span>
<span data-ttu-id="1fe76-123">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="1fe76-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1fe76-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fe76-124">-WhatIf</span></span>
<span data-ttu-id="1fe76-125">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1fe76-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1fe76-126">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1fe76-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1fe76-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fe76-127">CommonParameters</span></span>
<span data-ttu-id="1fe76-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1fe76-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fe76-129">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="1fe76-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fe76-130">輸入</span><span class="sxs-lookup"><span data-stu-id="1fe76-130">INPUTS</span></span>

### <span data-ttu-id="1fe76-131">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1fe76-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1fe76-132">輸出</span><span class="sxs-lookup"><span data-stu-id="1fe76-132">OUTPUTS</span></span>

### <span data-ttu-id="1fe76-133">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1fe76-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1fe76-134">筆記</span><span class="sxs-lookup"><span data-stu-id="1fe76-134">NOTES</span></span>

## <span data-ttu-id="1fe76-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="1fe76-135">RELATED LINKS</span></span>

[<span data-ttu-id="1fe76-136">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="1fe76-136">Get-AzApplicationGatewayTrustedRootCertificate</span></span>](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="1fe76-137">New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="1fe76-137">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="1fe76-138">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="1fe76-138">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="1fe76-139">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="1fe76-139">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)
