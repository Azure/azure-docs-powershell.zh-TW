---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: 40f31fc2c8cc4d0cb3a9637b39d8c3fcbd18ee42
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98274500"
---
# <span data-ttu-id="4ee44-101">Remove-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="4ee44-101">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="4ee44-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4ee44-102">SYNOPSIS</span></span>
<span data-ttu-id="4ee44-103">從應用程式閘道移除受信任的用戶端 CA 憑證鏈物件。</span><span class="sxs-lookup"><span data-stu-id="4ee44-103">Removes the trusted client CA certificate chain object from an application gateway.</span></span>

## <span data-ttu-id="4ee44-104">句法</span><span class="sxs-lookup"><span data-stu-id="4ee44-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayTrustedClientCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ee44-105">說明</span><span class="sxs-lookup"><span data-stu-id="4ee44-105">DESCRIPTION</span></span>
<span data-ttu-id="4ee44-106">**AzApplicationGatewayTrustedClientCertificate** Cmdlet 會從應用程式閘道中移除受信任的用戶端 CA 憑證鏈物件。</span><span class="sxs-lookup"><span data-stu-id="4ee44-106">The **Remove-AzApplicationGatewayTrustedClientCertificate** cmdlet removes the trusted client CA certificate chain object from an application gateway.</span></span>

## <span data-ttu-id="4ee44-107">示例</span><span class="sxs-lookup"><span data-stu-id="4ee44-107">EXAMPLES</span></span>

### <span data-ttu-id="4ee44-108">範例1</span><span class="sxs-lookup"><span data-stu-id="4ee44-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Remove-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway $gw -Name "TrustedClientCertificate01"
```

<span data-ttu-id="4ee44-109">第一個命令會取得應用程式閘道，並將它儲存在 $gw 變數中。</span><span class="sxs-lookup"><span data-stu-id="4ee44-109">The first command gets an application gateway and stores it in the $gw variable.</span></span> <span data-ttu-id="4ee44-110">第二個命令會從儲存在 $gw 的應用程式閘道中，移除名為「TrustedClientCertificate01」的信任用戶端 CA 憑證鏈。</span><span class="sxs-lookup"><span data-stu-id="4ee44-110">The second command removes the trusted client CA certificate chain named "TrustedClientCertificate01" from the application gateway stored in $gw.</span></span>

## <span data-ttu-id="4ee44-111">參數</span><span class="sxs-lookup"><span data-stu-id="4ee44-111">PARAMETERS</span></span>

### <span data-ttu-id="4ee44-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4ee44-112">-ApplicationGateway</span></span>
<span data-ttu-id="4ee44-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4ee44-113">The applicationGateway</span></span>

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

### <span data-ttu-id="4ee44-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ee44-114">-DefaultProfile</span></span>
<span data-ttu-id="4ee44-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4ee44-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ee44-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="4ee44-116">-Name</span></span>
<span data-ttu-id="4ee44-117">受信任的用戶端 CA 憑證鏈的名稱</span><span class="sxs-lookup"><span data-stu-id="4ee44-117">The name of the trusted client CA certificate chain</span></span>

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

### <span data-ttu-id="4ee44-118">-確認</span><span class="sxs-lookup"><span data-stu-id="4ee44-118">-Confirm</span></span>
<span data-ttu-id="4ee44-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4ee44-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ee44-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ee44-120">-WhatIf</span></span>
<span data-ttu-id="4ee44-121">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4ee44-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ee44-122">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4ee44-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ee44-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ee44-123">CommonParameters</span></span>
<span data-ttu-id="4ee44-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4ee44-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ee44-125">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4ee44-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ee44-126">輸入</span><span class="sxs-lookup"><span data-stu-id="4ee44-126">INPUTS</span></span>

### <span data-ttu-id="4ee44-127">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4ee44-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4ee44-128">輸出</span><span class="sxs-lookup"><span data-stu-id="4ee44-128">OUTPUTS</span></span>

### <span data-ttu-id="4ee44-129">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4ee44-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4ee44-130">筆記</span><span class="sxs-lookup"><span data-stu-id="4ee44-130">NOTES</span></span>

## <span data-ttu-id="4ee44-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="4ee44-131">RELATED LINKS</span></span>

[<span data-ttu-id="4ee44-132">新-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="4ee44-132">New-AzApplicationGatewayTrustedClientCertificate</span></span>](./New-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="4ee44-133">附加 AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="4ee44-133">Add-AzApplicationGatewayTrustedClientCertificate</span></span>](./Add-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="4ee44-134">AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="4ee44-134">Get-AzApplicationGatewayTrustedClientCertificate</span></span>](./Get-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="4ee44-135">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="4ee44-135">Set-AzApplicationGatewayTrustedClientCertificate</span></span>](./Set-AzApplicationGatewayTrustedClientCertificate.md)