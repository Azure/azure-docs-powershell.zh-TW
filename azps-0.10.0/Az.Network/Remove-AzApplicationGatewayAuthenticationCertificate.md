---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 29BB24C4-1EC9-47DE-A5B8-5EEA4525AE3A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: bf11b2b3010a7f7683d670c3c5e95d4248b83cd6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794219"
---
# <span data-ttu-id="59967-101">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="59967-101">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="59967-102">摘要</span><span class="sxs-lookup"><span data-stu-id="59967-102">SYNOPSIS</span></span>
<span data-ttu-id="59967-103">從應用程式閘道移除驗證憑證。</span><span class="sxs-lookup"><span data-stu-id="59967-103">Removes an authentication certificate from an application gateway.</span></span>

## <span data-ttu-id="59967-104">句法</span><span class="sxs-lookup"><span data-stu-id="59967-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayAuthenticationCertificate -Name <String>
 -ApplicationGateway <PSApplicationGateway> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="59967-105">說明</span><span class="sxs-lookup"><span data-stu-id="59967-105">DESCRIPTION</span></span>
<span data-ttu-id="59967-106">**AzApplicationGatewayAuthenticationCertificate** Cmdlet 會從 Azure 應用程式閘道移除驗證憑證。</span><span class="sxs-lookup"><span data-stu-id="59967-106">The **Remove-AzApplicationGatewayAuthenticationCertificate** cmdlet removes an authentication certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="59967-107">示例</span><span class="sxs-lookup"><span data-stu-id="59967-107">EXAMPLES</span></span>

### <span data-ttu-id="59967-108">sr-1</span><span class="sxs-lookup"><span data-stu-id="59967-108">1:</span></span>
```

```

## <span data-ttu-id="59967-109">參數</span><span class="sxs-lookup"><span data-stu-id="59967-109">PARAMETERS</span></span>

### <span data-ttu-id="59967-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="59967-110">-ApplicationGateway</span></span>
<span data-ttu-id="59967-111">指定此 Cmdlet 從中移除驗證憑證的應用程式閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="59967-111">Specifies the name of application gateway from which this cmdlet removes an authentication certificate.</span></span>

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

### <span data-ttu-id="59967-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59967-112">-DefaultProfile</span></span>
<span data-ttu-id="59967-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="59967-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59967-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="59967-114">-Name</span></span>
<span data-ttu-id="59967-115">指定此 Cmdlet 移除之驗證憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="59967-115">Specifies the name of the authentication certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="59967-116">-確認</span><span class="sxs-lookup"><span data-stu-id="59967-116">-Confirm</span></span>
<span data-ttu-id="59967-117">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="59967-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59967-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59967-118">-WhatIf</span></span>
<span data-ttu-id="59967-119">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="59967-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59967-120">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="59967-120">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59967-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59967-121">CommonParameters</span></span>
<span data-ttu-id="59967-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="59967-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59967-123">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="59967-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59967-124">輸入</span><span class="sxs-lookup"><span data-stu-id="59967-124">INPUTS</span></span>

### <span data-ttu-id="59967-125">System.object</span><span class="sxs-lookup"><span data-stu-id="59967-125">System.String</span></span>

## <span data-ttu-id="59967-126">輸出</span><span class="sxs-lookup"><span data-stu-id="59967-126">OUTPUTS</span></span>

### <span data-ttu-id="59967-127">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="59967-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="59967-128">筆記</span><span class="sxs-lookup"><span data-stu-id="59967-128">NOTES</span></span>
* <span data-ttu-id="59967-129">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路</span><span class="sxs-lookup"><span data-stu-id="59967-129">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="59967-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="59967-130">RELATED LINKS</span></span>

[<span data-ttu-id="59967-131">附加 AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="59967-131">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="59967-132">AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="59967-132">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="59967-133">新-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="59967-133">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="59967-134">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="59967-134">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


