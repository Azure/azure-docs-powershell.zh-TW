---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: 635ee4671a235506e7125d33f2f3a14917cc424a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913465"
---
# <span data-ttu-id="6addf-101">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="6addf-101">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="6addf-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6addf-102">SYNOPSIS</span></span>
<span data-ttu-id="6addf-103">從應用程式閘道移除信任的根憑證。</span><span class="sxs-lookup"><span data-stu-id="6addf-103">Removes a Trusted Root Certificate from an application gateway.</span></span>

## <span data-ttu-id="6addf-104">語法</span><span class="sxs-lookup"><span data-stu-id="6addf-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayTrustedRootCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6addf-105">描述</span><span class="sxs-lookup"><span data-stu-id="6addf-105">DESCRIPTION</span></span>
<span data-ttu-id="6addf-106">**Remove-AzApplicationGatewayTrustedRootCertificate** Cmdlet 會從現有的應用程式閘道移除信任的根憑證。</span><span class="sxs-lookup"><span data-stu-id="6addf-106">The **Remove-AzApplicationGatewayTrustedRootCertificate** cmdlet removes a Trusted Root Certificate from an existing Application Gateway.</span></span>

## <span data-ttu-id="6addf-107">例子</span><span class="sxs-lookup"><span data-stu-id="6addf-107">EXAMPLES</span></span>

### <span data-ttu-id="6addf-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="6addf-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Remove-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name "myRootCA"
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="6addf-109">第一個命令會獲得應用程式閘道，並儲存在$gw變數。</span><span class="sxs-lookup"><span data-stu-id="6addf-109">The first command gets an application gateway and stores it in the $gw variable.</span></span>
<span data-ttu-id="6addf-110">第二個命令會從儲存在 $gw 的應用程式閘道移除名為 myRootCA 的受根信任憑證。</span><span class="sxs-lookup"><span data-stu-id="6addf-110">The second command removes the trusted root certificate named myRootCA from the application gateway stored in $gw.</span></span>
<span data-ttu-id="6addf-111">第三個命令會更新 Azure 上的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="6addf-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="6addf-112">參數</span><span class="sxs-lookup"><span data-stu-id="6addf-112">PARAMETERS</span></span>

### <span data-ttu-id="6addf-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6addf-113">-ApplicationGateway</span></span>
<span data-ttu-id="6addf-114">應用程式Gateway</span><span class="sxs-lookup"><span data-stu-id="6addf-114">The applicationGateway</span></span>

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

### <span data-ttu-id="6addf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6addf-115">-DefaultProfile</span></span>
<span data-ttu-id="6addf-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="6addf-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6addf-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="6addf-117">-Name</span></span>
<span data-ttu-id="6addf-118">TrustedRoot 憑證的名稱</span><span class="sxs-lookup"><span data-stu-id="6addf-118">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="6addf-119">-確認</span><span class="sxs-lookup"><span data-stu-id="6addf-119">-Confirm</span></span>
<span data-ttu-id="6addf-120">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="6addf-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6addf-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6addf-121">-WhatIf</span></span>
<span data-ttu-id="6addf-122">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6addf-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6addf-123">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6addf-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6addf-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6addf-124">CommonParameters</span></span>
<span data-ttu-id="6addf-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6addf-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6addf-126">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="6addf-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6addf-127">輸入</span><span class="sxs-lookup"><span data-stu-id="6addf-127">INPUTS</span></span>

### <span data-ttu-id="6addf-128">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6addf-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6addf-129">輸出</span><span class="sxs-lookup"><span data-stu-id="6addf-129">OUTPUTS</span></span>

### <span data-ttu-id="6addf-130">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6addf-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6addf-131">筆記</span><span class="sxs-lookup"><span data-stu-id="6addf-131">NOTES</span></span>

## <span data-ttu-id="6addf-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="6addf-132">RELATED LINKS</span></span>

[<span data-ttu-id="6addf-133">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="6addf-133">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="6addf-134">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="6addf-134">Get-AzApplicationGatewayTrustedRootCertificate</span></span>](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="6addf-135">New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="6addf-135">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="6addf-136">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="6addf-136">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)
