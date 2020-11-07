---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: 3e8c4f6bc25ea5ff9b8efcee989937fb688fea57
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93956280"
---
# <span data-ttu-id="77dcd-101">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="77dcd-101">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="77dcd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="77dcd-102">SYNOPSIS</span></span>
<span data-ttu-id="77dcd-103">從應用程式閘道移除受信任的根憑證。</span><span class="sxs-lookup"><span data-stu-id="77dcd-103">Removes a Trusted Root Certificate from an application gateway.</span></span>

## <span data-ttu-id="77dcd-104">句法</span><span class="sxs-lookup"><span data-stu-id="77dcd-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayTrustedRootCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77dcd-105">說明</span><span class="sxs-lookup"><span data-stu-id="77dcd-105">DESCRIPTION</span></span>
<span data-ttu-id="77dcd-106">**AzApplicationGatewayTrustedRootCertificate** Cmdlet 會從現有的應用程式閘道中移除受信任的根憑證。</span><span class="sxs-lookup"><span data-stu-id="77dcd-106">The **Remove-AzApplicationGatewayTrustedRootCertificate** cmdlet removes a Trusted Root Certificate from an existing Application Gateway.</span></span>

## <span data-ttu-id="77dcd-107">示例</span><span class="sxs-lookup"><span data-stu-id="77dcd-107">EXAMPLES</span></span>

### <span data-ttu-id="77dcd-108">範例1</span><span class="sxs-lookup"><span data-stu-id="77dcd-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Remove-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name "myRootCA"
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="77dcd-109">第一個命令會取得應用程式閘道，並將它儲存在 $gw 變數中。</span><span class="sxs-lookup"><span data-stu-id="77dcd-109">The first command gets an application gateway and stores it in the $gw variable.</span></span>
<span data-ttu-id="77dcd-110">第二個命令會從儲存在 $gw 的應用程式閘道中，移除名為 myRootCA 的根信任證書。</span><span class="sxs-lookup"><span data-stu-id="77dcd-110">The second command removes the trusted root certificate named myRootCA from the application gateway stored in $gw.</span></span>
<span data-ttu-id="77dcd-111">第三個命令會更新 Azure 上的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="77dcd-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="77dcd-112">參數</span><span class="sxs-lookup"><span data-stu-id="77dcd-112">PARAMETERS</span></span>

### <span data-ttu-id="77dcd-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="77dcd-113">-ApplicationGateway</span></span>
<span data-ttu-id="77dcd-114">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="77dcd-114">The applicationGateway</span></span>

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

### <span data-ttu-id="77dcd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77dcd-115">-DefaultProfile</span></span>
<span data-ttu-id="77dcd-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="77dcd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77dcd-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="77dcd-117">-Name</span></span>
<span data-ttu-id="77dcd-118">TrustedRoot 憑證的名稱</span><span class="sxs-lookup"><span data-stu-id="77dcd-118">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="77dcd-119">-確認</span><span class="sxs-lookup"><span data-stu-id="77dcd-119">-Confirm</span></span>
<span data-ttu-id="77dcd-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="77dcd-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77dcd-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77dcd-121">-WhatIf</span></span>
<span data-ttu-id="77dcd-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="77dcd-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77dcd-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="77dcd-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77dcd-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77dcd-124">CommonParameters</span></span>
<span data-ttu-id="77dcd-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="77dcd-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77dcd-126">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="77dcd-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77dcd-127">輸入</span><span class="sxs-lookup"><span data-stu-id="77dcd-127">INPUTS</span></span>

### <span data-ttu-id="77dcd-128">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="77dcd-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="77dcd-129">輸出</span><span class="sxs-lookup"><span data-stu-id="77dcd-129">OUTPUTS</span></span>

### <span data-ttu-id="77dcd-130">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="77dcd-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="77dcd-131">筆記</span><span class="sxs-lookup"><span data-stu-id="77dcd-131">NOTES</span></span>

## <span data-ttu-id="77dcd-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="77dcd-132">RELATED LINKS</span></span>

[<span data-ttu-id="77dcd-133">附加 AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="77dcd-133">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="77dcd-134">AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="77dcd-134">Get-AzApplicationGatewayTrustedRootCertificate</span></span>](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="77dcd-135">新-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="77dcd-135">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="77dcd-136">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="77dcd-136">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)
