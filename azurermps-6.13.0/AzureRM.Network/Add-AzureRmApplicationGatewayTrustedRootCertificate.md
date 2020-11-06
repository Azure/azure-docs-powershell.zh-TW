---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: e44136d5fa9b0a6b0b979005c13faf6041d98f61
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453691"
---
# <span data-ttu-id="82556-101">Add-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="82556-101">Add-AzureRmApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="82556-102">摘要</span><span class="sxs-lookup"><span data-stu-id="82556-102">SYNOPSIS</span></span>
<span data-ttu-id="82556-103">將信任的根憑證新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="82556-103">Adds a trusted root certificate to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="82556-104">句法</span><span class="sxs-lookup"><span data-stu-id="82556-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayTrustedRootCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82556-105">說明</span><span class="sxs-lookup"><span data-stu-id="82556-105">DESCRIPTION</span></span>
<span data-ttu-id="82556-106">**AzureRmApplicationGatewayTrustedRootCertificate** Cmdlet 會將信任的根憑證新增至 Azure 應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="82556-106">The **Add-AzureRmApplicationGatewayTrustedRootCertificate** cmdlet adds a trusted root certificate to an Azure application gateway.</span></span>

## <span data-ttu-id="82556-107">示例</span><span class="sxs-lookup"><span data-stu-id="82556-107">EXAMPLES</span></span>

### <span data-ttu-id="82556-108">範例1</span><span class="sxs-lookup"><span data-stu-id="82556-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzureRmApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Add-AzureRmApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\rootCA.cer"
PS C:\> $gw = Add-AzureRmApplicationGatewayBackendHttpSetting -Name $poolSetting01Name -Port 443 -Protocol Https -CookieBasedAffinity Enabled -PickHostNameFromBackendAddress -TrustedRootCertificate $gw.TrustedRootCertificates[0]
PS C:\> $gw = Set-AzureRmApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="82556-109">第一個命令會取得應用程式閘道，並將它儲存在 $gw 變數中。</span><span class="sxs-lookup"><span data-stu-id="82556-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="82556-110">第二個命令 addes 新的根信任憑證至應用程式閘道將根憑證的路徑做為輸入。</span><span class="sxs-lookup"><span data-stu-id="82556-110">The second command addes a new trusted root certificate to Application Gateway taking path of the root certificate as input.</span></span>
<span data-ttu-id="82556-111">第三個命令會使用信任的根憑證來建立新的後端 HTTP 設定，以驗證後端伺服器憑證。</span><span class="sxs-lookup"><span data-stu-id="82556-111">The third command creates new backend http setting using trusted root certificate for validating the backend server certificate against.</span></span>
<span data-ttu-id="82556-112">[Fouth] 命令會更新應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="82556-112">The fouth command updates the Application Gateway.</span></span>

## <span data-ttu-id="82556-113">參數</span><span class="sxs-lookup"><span data-stu-id="82556-113">PARAMETERS</span></span>

### <span data-ttu-id="82556-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="82556-114">-ApplicationGateway</span></span>
<span data-ttu-id="82556-115">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="82556-115">The applicationGateway</span></span>

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

### <span data-ttu-id="82556-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="82556-116">-CertificateFile</span></span>
<span data-ttu-id="82556-117">憑證 CER 檔案的路徑</span><span class="sxs-lookup"><span data-stu-id="82556-117">Path of certificate CER file</span></span>

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

### <span data-ttu-id="82556-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82556-118">-DefaultProfile</span></span>
<span data-ttu-id="82556-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="82556-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82556-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="82556-120">-Name</span></span>
<span data-ttu-id="82556-121">TrustedRoot 憑證的名稱</span><span class="sxs-lookup"><span data-stu-id="82556-121">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="82556-122">-確認</span><span class="sxs-lookup"><span data-stu-id="82556-122">-Confirm</span></span>
<span data-ttu-id="82556-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="82556-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82556-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82556-124">-WhatIf</span></span>
<span data-ttu-id="82556-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="82556-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82556-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="82556-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82556-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82556-127">CommonParameters</span></span>
<span data-ttu-id="82556-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="82556-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82556-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="82556-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82556-130">輸入</span><span class="sxs-lookup"><span data-stu-id="82556-130">INPUTS</span></span>

### <span data-ttu-id="82556-131">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="82556-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="82556-132">輸出</span><span class="sxs-lookup"><span data-stu-id="82556-132">OUTPUTS</span></span>

### <span data-ttu-id="82556-133">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="82556-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="82556-134">筆記</span><span class="sxs-lookup"><span data-stu-id="82556-134">NOTES</span></span>

## <span data-ttu-id="82556-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="82556-135">RELATED LINKS</span></span>
