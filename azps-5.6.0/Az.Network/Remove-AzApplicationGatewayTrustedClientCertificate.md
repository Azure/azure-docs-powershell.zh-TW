---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: c7fdf250ad7c322e47c26e023f04689a12a8eee5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908090"
---
# <span data-ttu-id="cb87d-101">Remove-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="cb87d-101">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="cb87d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="cb87d-102">SYNOPSIS</span></span>
<span data-ttu-id="cb87d-103">從應用程式閘道移除信任的用戶端 CA 憑證鏈物件。</span><span class="sxs-lookup"><span data-stu-id="cb87d-103">Removes the trusted client CA certificate chain object from an application gateway.</span></span>

## <span data-ttu-id="cb87d-104">語法</span><span class="sxs-lookup"><span data-stu-id="cb87d-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayTrustedClientCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb87d-105">描述</span><span class="sxs-lookup"><span data-stu-id="cb87d-105">DESCRIPTION</span></span>
<span data-ttu-id="cb87d-106">**Remove-AzApplicationGatewayTrustedClientCertificate** Cmdlet 會從應用程式閘道移除信任的用戶端 CA 憑證鏈物件。</span><span class="sxs-lookup"><span data-stu-id="cb87d-106">The **Remove-AzApplicationGatewayTrustedClientCertificate** cmdlet removes the trusted client CA certificate chain object from an application gateway.</span></span>

## <span data-ttu-id="cb87d-107">例子</span><span class="sxs-lookup"><span data-stu-id="cb87d-107">EXAMPLES</span></span>

### <span data-ttu-id="cb87d-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="cb87d-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Remove-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway $gw -Name "TrustedClientCertificate01"
```

<span data-ttu-id="cb87d-109">第一個命令會獲得應用程式閘道，並儲存在$gw變數。</span><span class="sxs-lookup"><span data-stu-id="cb87d-109">The first command gets an application gateway and stores it in the $gw variable.</span></span> <span data-ttu-id="cb87d-110">第二個命令會從儲存在 $gw 的應用程式閘道移除名為 "TrustedClientCertificate01" 的受信任用戶端 CA 憑證鏈。</span><span class="sxs-lookup"><span data-stu-id="cb87d-110">The second command removes the trusted client CA certificate chain named "TrustedClientCertificate01" from the application gateway stored in $gw.</span></span>

## <span data-ttu-id="cb87d-111">參數</span><span class="sxs-lookup"><span data-stu-id="cb87d-111">PARAMETERS</span></span>

### <span data-ttu-id="cb87d-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cb87d-112">-ApplicationGateway</span></span>
<span data-ttu-id="cb87d-113">應用程式Gateway</span><span class="sxs-lookup"><span data-stu-id="cb87d-113">The applicationGateway</span></span>

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

### <span data-ttu-id="cb87d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb87d-114">-DefaultProfile</span></span>
<span data-ttu-id="cb87d-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="cb87d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb87d-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="cb87d-116">-Name</span></span>
<span data-ttu-id="cb87d-117">信任的用戶端 CA 憑證鏈的名稱</span><span class="sxs-lookup"><span data-stu-id="cb87d-117">The name of the trusted client CA certificate chain</span></span>

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

### <span data-ttu-id="cb87d-118">-確認</span><span class="sxs-lookup"><span data-stu-id="cb87d-118">-Confirm</span></span>
<span data-ttu-id="cb87d-119">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="cb87d-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb87d-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb87d-120">-WhatIf</span></span>
<span data-ttu-id="cb87d-121">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cb87d-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb87d-122">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cb87d-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb87d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb87d-123">CommonParameters</span></span>
<span data-ttu-id="cb87d-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="cb87d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb87d-125">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cb87d-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb87d-126">輸入</span><span class="sxs-lookup"><span data-stu-id="cb87d-126">INPUTS</span></span>

### <span data-ttu-id="cb87d-127">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cb87d-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="cb87d-128">輸出</span><span class="sxs-lookup"><span data-stu-id="cb87d-128">OUTPUTS</span></span>

### <span data-ttu-id="cb87d-129">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cb87d-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="cb87d-130">筆記</span><span class="sxs-lookup"><span data-stu-id="cb87d-130">NOTES</span></span>

## <span data-ttu-id="cb87d-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="cb87d-131">RELATED LINKS</span></span>

[<span data-ttu-id="cb87d-132">New-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="cb87d-132">New-AzApplicationGatewayTrustedClientCertificate</span></span>](./New-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="cb87d-133">Add-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="cb87d-133">Add-AzApplicationGatewayTrustedClientCertificate</span></span>](./Add-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="cb87d-134">Get-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="cb87d-134">Get-AzApplicationGatewayTrustedClientCertificate</span></span>](./Get-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="cb87d-135">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="cb87d-135">Set-AzApplicationGatewayTrustedClientCertificate</span></span>](./Set-AzApplicationGatewayTrustedClientCertificate.md)