---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 29BB24C4-1EC9-47DE-A5B8-5EEA4525AE3A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 02416fdb18f01c9a2af6c091b0be109b479ce45d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957998"
---
# <span data-ttu-id="fc4da-101">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="fc4da-101">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="fc4da-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fc4da-102">SYNOPSIS</span></span>
<span data-ttu-id="fc4da-103">從應用程式閘道移除驗證憑證。</span><span class="sxs-lookup"><span data-stu-id="fc4da-103">Removes an authentication certificate from an application gateway.</span></span>

## <span data-ttu-id="fc4da-104">句法</span><span class="sxs-lookup"><span data-stu-id="fc4da-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayAuthenticationCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc4da-105">說明</span><span class="sxs-lookup"><span data-stu-id="fc4da-105">DESCRIPTION</span></span>
<span data-ttu-id="fc4da-106">**AzApplicationGatewayAuthenticationCertificate** Cmdlet 會從 Azure 應用程式閘道移除驗證憑證。</span><span class="sxs-lookup"><span data-stu-id="fc4da-106">The **Remove-AzApplicationGatewayAuthenticationCertificate** cmdlet removes an authentication certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="fc4da-107">示例</span><span class="sxs-lookup"><span data-stu-id="fc4da-107">EXAMPLES</span></span>

### <span data-ttu-id="fc4da-108">範例1：從應用程式閘道移除驗證憑證</span><span class="sxs-lookup"><span data-stu-id="fc4da-108">Example 1: Remove an authentication certificate from an application gateway</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Remove-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway $appgw -Name "cert01"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="fc4da-109">第一個命令會取得名為 appGwName 的應用程式閘道，並將結果儲存在 $appgw 變數中。</span><span class="sxs-lookup"><span data-stu-id="fc4da-109">The first command gets the application gateway named appGwName and stores the result in the $appgw variable.</span></span>
<span data-ttu-id="fc4da-110">第二個命令會從應用程式閘道移除名為 cert01 的驗證憑證。</span><span class="sxs-lookup"><span data-stu-id="fc4da-110">The second command removes the authentication certificate named cert01 from the application gateway.</span></span>
<span data-ttu-id="fc4da-111">第三個命令會更新應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="fc4da-111">The third command updates the application gateway.</span></span>

## <span data-ttu-id="fc4da-112">參數</span><span class="sxs-lookup"><span data-stu-id="fc4da-112">PARAMETERS</span></span>

### <span data-ttu-id="fc4da-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fc4da-113">-ApplicationGateway</span></span>
<span data-ttu-id="fc4da-114">指定此 Cmdlet 從中移除驗證憑證的應用程式閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="fc4da-114">Specifies the name of application gateway from which this cmdlet removes an authentication certificate.</span></span>

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

### <span data-ttu-id="fc4da-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc4da-115">-DefaultProfile</span></span>
<span data-ttu-id="fc4da-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fc4da-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc4da-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="fc4da-117">-Name</span></span>
<span data-ttu-id="fc4da-118">指定此 Cmdlet 移除之驗證憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="fc4da-118">Specifies the name of the authentication certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="fc4da-119">-確認</span><span class="sxs-lookup"><span data-stu-id="fc4da-119">-Confirm</span></span>
<span data-ttu-id="fc4da-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fc4da-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc4da-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc4da-121">-WhatIf</span></span>
<span data-ttu-id="fc4da-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fc4da-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc4da-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fc4da-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc4da-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc4da-124">CommonParameters</span></span>
<span data-ttu-id="fc4da-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fc4da-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc4da-126">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fc4da-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc4da-127">輸入</span><span class="sxs-lookup"><span data-stu-id="fc4da-127">INPUTS</span></span>

### <span data-ttu-id="fc4da-128">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="fc4da-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="fc4da-129">輸出</span><span class="sxs-lookup"><span data-stu-id="fc4da-129">OUTPUTS</span></span>

### <span data-ttu-id="fc4da-130">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="fc4da-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="fc4da-131">筆記</span><span class="sxs-lookup"><span data-stu-id="fc4da-131">NOTES</span></span>
* <span data-ttu-id="fc4da-132">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路</span><span class="sxs-lookup"><span data-stu-id="fc4da-132">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="fc4da-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="fc4da-133">RELATED LINKS</span></span>

[<span data-ttu-id="fc4da-134">附加 AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="fc4da-134">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="fc4da-135">AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="fc4da-135">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="fc4da-136">新-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="fc4da-136">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="fc4da-137">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="fc4da-137">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


