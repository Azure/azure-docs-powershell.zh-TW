---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: 839f2a647c4a06ddd1bdebe9b95fac0fdbdd91dd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913141"
---
# <span data-ttu-id="f6d59-101">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f6d59-101">Set-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="f6d59-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f6d59-102">SYNOPSIS</span></span>
<span data-ttu-id="f6d59-103">更新應用程式閘道的受根信任憑證。</span><span class="sxs-lookup"><span data-stu-id="f6d59-103">Updates a Trusted Root Certificate of an application gateway.</span></span>

## <span data-ttu-id="f6d59-104">語法</span><span class="sxs-lookup"><span data-stu-id="f6d59-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6d59-105">描述</span><span class="sxs-lookup"><span data-stu-id="f6d59-105">DESCRIPTION</span></span>
<span data-ttu-id="f6d59-106">**Set-AzApplicationGatewayTrustedRootCertificate** Cmdlet 會修改應用程式閘道的現有根信任憑證。</span><span class="sxs-lookup"><span data-stu-id="f6d59-106">The **Set-AzApplicationGatewayTrustedRootCertificate** cmdlet modifies the existing trusted root certificate of an Application Gateway.</span></span>

## <span data-ttu-id="f6d59-107">例子</span><span class="sxs-lookup"><span data-stu-id="f6d59-107">EXAMPLES</span></span>

### <span data-ttu-id="f6d59-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="f6d59-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Set-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\rootCAUpdated.cer"
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="f6d59-109">上述範例案例顯示如何在卷起根憑證時更新現有的根信任憑證。</span><span class="sxs-lookup"><span data-stu-id="f6d59-109">Above example scenarios shows how to update an existing trusted root certificate when a root certificate is rolled.</span></span>
<span data-ttu-id="f6d59-110">第一個命令會獲得應用程式閘道，並儲存在$gw變數。</span><span class="sxs-lookup"><span data-stu-id="f6d59-110">The first command gets an application gateway and stores it in the $gw variable.</span></span>
<span data-ttu-id="f6d59-111">第二個命令會使用新的根憑證修改現有的根信任憑證。</span><span class="sxs-lookup"><span data-stu-id="f6d59-111">The second command modifies the existing trusted root certificate with a new root certificate.</span></span>
<span data-ttu-id="f6d59-112">第三個命令會更新 Azure 上的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="f6d59-112">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="f6d59-113">參數</span><span class="sxs-lookup"><span data-stu-id="f6d59-113">PARAMETERS</span></span>

### <span data-ttu-id="f6d59-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f6d59-114">-ApplicationGateway</span></span>
<span data-ttu-id="f6d59-115">應用程式Gateway</span><span class="sxs-lookup"><span data-stu-id="f6d59-115">The applicationGateway</span></span>

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

### <span data-ttu-id="f6d59-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="f6d59-116">-CertificateFile</span></span>
<span data-ttu-id="f6d59-117">憑證憑證檔案的路徑</span><span class="sxs-lookup"><span data-stu-id="f6d59-117">Path of certificate CER file</span></span>

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

### <span data-ttu-id="f6d59-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6d59-118">-DefaultProfile</span></span>
<span data-ttu-id="f6d59-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f6d59-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6d59-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="f6d59-120">-Name</span></span>
<span data-ttu-id="f6d59-121">TrustedRoot 憑證的名稱</span><span class="sxs-lookup"><span data-stu-id="f6d59-121">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="f6d59-122">-確認</span><span class="sxs-lookup"><span data-stu-id="f6d59-122">-Confirm</span></span>
<span data-ttu-id="f6d59-123">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f6d59-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6d59-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6d59-124">-WhatIf</span></span>
<span data-ttu-id="f6d59-125">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f6d59-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6d59-126">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f6d59-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6d59-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6d59-127">CommonParameters</span></span>
<span data-ttu-id="f6d59-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f6d59-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6d59-129">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="f6d59-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6d59-130">輸入</span><span class="sxs-lookup"><span data-stu-id="f6d59-130">INPUTS</span></span>

### <span data-ttu-id="f6d59-131">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f6d59-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f6d59-132">輸出</span><span class="sxs-lookup"><span data-stu-id="f6d59-132">OUTPUTS</span></span>

### <span data-ttu-id="f6d59-133">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f6d59-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f6d59-134">筆記</span><span class="sxs-lookup"><span data-stu-id="f6d59-134">NOTES</span></span>

## <span data-ttu-id="f6d59-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="f6d59-135">RELATED LINKS</span></span>

[<span data-ttu-id="f6d59-136">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f6d59-136">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="f6d59-137">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f6d59-137">Get-AzApplicationGatewayTrustedRootCertificate</span></span>](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="f6d59-138">New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f6d59-138">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="f6d59-139">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f6d59-139">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)
