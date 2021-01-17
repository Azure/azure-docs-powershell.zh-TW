---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: 40f31fc2c8cc4d0cb3a9637b39d8c3fcbd18ee42
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98448952"
---
# <span data-ttu-id="7ed29-101">Remove-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="7ed29-101">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="7ed29-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7ed29-102">SYNOPSIS</span></span>
<span data-ttu-id="7ed29-103">從應用程式閘道移除受信任的用戶端 CA 憑證鏈物件。</span><span class="sxs-lookup"><span data-stu-id="7ed29-103">Removes the trusted client CA certificate chain object from an application gateway.</span></span>

## <span data-ttu-id="7ed29-104">句法</span><span class="sxs-lookup"><span data-stu-id="7ed29-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayTrustedClientCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ed29-105">說明</span><span class="sxs-lookup"><span data-stu-id="7ed29-105">DESCRIPTION</span></span>
<span data-ttu-id="7ed29-106">**AzApplicationGatewayTrustedClientCertificate** Cmdlet 會從應用程式閘道中移除受信任的用戶端 CA 憑證鏈物件。</span><span class="sxs-lookup"><span data-stu-id="7ed29-106">The **Remove-AzApplicationGatewayTrustedClientCertificate** cmdlet removes the trusted client CA certificate chain object from an application gateway.</span></span>

## <span data-ttu-id="7ed29-107">示例</span><span class="sxs-lookup"><span data-stu-id="7ed29-107">EXAMPLES</span></span>

### <span data-ttu-id="7ed29-108">範例1</span><span class="sxs-lookup"><span data-stu-id="7ed29-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Remove-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway $gw -Name "TrustedClientCertificate01"
```

<span data-ttu-id="7ed29-109">第一個命令會取得應用程式閘道，並將它儲存在 $gw 變數中。</span><span class="sxs-lookup"><span data-stu-id="7ed29-109">The first command gets an application gateway and stores it in the $gw variable.</span></span> <span data-ttu-id="7ed29-110">第二個命令會從儲存在 $gw 的應用程式閘道中，移除名為「TrustedClientCertificate01」的信任用戶端 CA 憑證鏈。</span><span class="sxs-lookup"><span data-stu-id="7ed29-110">The second command removes the trusted client CA certificate chain named "TrustedClientCertificate01" from the application gateway stored in $gw.</span></span>

## <span data-ttu-id="7ed29-111">參數</span><span class="sxs-lookup"><span data-stu-id="7ed29-111">PARAMETERS</span></span>

### <span data-ttu-id="7ed29-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7ed29-112">-ApplicationGateway</span></span>
<span data-ttu-id="7ed29-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7ed29-113">The applicationGateway</span></span>

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

### <span data-ttu-id="7ed29-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ed29-114">-DefaultProfile</span></span>
<span data-ttu-id="7ed29-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7ed29-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ed29-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="7ed29-116">-Name</span></span>
<span data-ttu-id="7ed29-117">受信任的用戶端 CA 憑證鏈的名稱</span><span class="sxs-lookup"><span data-stu-id="7ed29-117">The name of the trusted client CA certificate chain</span></span>

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

### <span data-ttu-id="7ed29-118">-確認</span><span class="sxs-lookup"><span data-stu-id="7ed29-118">-Confirm</span></span>
<span data-ttu-id="7ed29-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7ed29-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ed29-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ed29-120">-WhatIf</span></span>
<span data-ttu-id="7ed29-121">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7ed29-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ed29-122">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7ed29-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ed29-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ed29-123">CommonParameters</span></span>
<span data-ttu-id="7ed29-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7ed29-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ed29-125">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="7ed29-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ed29-126">輸入</span><span class="sxs-lookup"><span data-stu-id="7ed29-126">INPUTS</span></span>

### <span data-ttu-id="7ed29-127">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="7ed29-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7ed29-128">輸出</span><span class="sxs-lookup"><span data-stu-id="7ed29-128">OUTPUTS</span></span>

### <span data-ttu-id="7ed29-129">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="7ed29-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7ed29-130">筆記</span><span class="sxs-lookup"><span data-stu-id="7ed29-130">NOTES</span></span>

## <span data-ttu-id="7ed29-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="7ed29-131">RELATED LINKS</span></span>

[<span data-ttu-id="7ed29-132">新-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="7ed29-132">New-AzApplicationGatewayTrustedClientCertificate</span></span>](./New-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="7ed29-133">附加 AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="7ed29-133">Add-AzApplicationGatewayTrustedClientCertificate</span></span>](./Add-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="7ed29-134">AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="7ed29-134">Get-AzApplicationGatewayTrustedClientCertificate</span></span>](./Get-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="7ed29-135">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="7ed29-135">Set-AzApplicationGatewayTrustedClientCertificate</span></span>](./Set-AzApplicationGatewayTrustedClientCertificate.md)