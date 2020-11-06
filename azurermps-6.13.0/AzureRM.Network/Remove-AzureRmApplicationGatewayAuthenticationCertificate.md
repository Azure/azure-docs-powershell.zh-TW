---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 29BB24C4-1EC9-47DE-A5B8-5EEA4525AE3A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 9ec4522da3c5a75a1c9e5bad977f294e0987f4fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447343"
---
# <span data-ttu-id="ee2af-101">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ee2af-101">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="ee2af-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ee2af-102">SYNOPSIS</span></span>
<span data-ttu-id="ee2af-103">從應用程式閘道移除驗證憑證。</span><span class="sxs-lookup"><span data-stu-id="ee2af-103">Removes an authentication certificate from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ee2af-104">句法</span><span class="sxs-lookup"><span data-stu-id="ee2af-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayAuthenticationCertificate -Name <String>
 -ApplicationGateway <PSApplicationGateway> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ee2af-105">說明</span><span class="sxs-lookup"><span data-stu-id="ee2af-105">DESCRIPTION</span></span>
<span data-ttu-id="ee2af-106">**AzureRmApplicationGatewayAuthenticationCertificate** Cmdlet 會從 Azure 應用程式閘道移除驗證憑證。</span><span class="sxs-lookup"><span data-stu-id="ee2af-106">The **Remove-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet removes an authentication certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="ee2af-107">示例</span><span class="sxs-lookup"><span data-stu-id="ee2af-107">EXAMPLES</span></span>

## <span data-ttu-id="ee2af-108">參數</span><span class="sxs-lookup"><span data-stu-id="ee2af-108">PARAMETERS</span></span>

### <span data-ttu-id="ee2af-109">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ee2af-109">-ApplicationGateway</span></span>
<span data-ttu-id="ee2af-110">指定此 Cmdlet 從中移除驗證憑證的應用程式閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="ee2af-110">Specifies the name of application gateway from which this cmdlet removes an authentication certificate.</span></span>

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

### <span data-ttu-id="ee2af-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee2af-111">-DefaultProfile</span></span>
<span data-ttu-id="ee2af-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ee2af-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ee2af-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="ee2af-113">-Name</span></span>
<span data-ttu-id="ee2af-114">指定此 Cmdlet 移除之驗證憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="ee2af-114">Specifies the name of the authentication certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ee2af-115">-確認</span><span class="sxs-lookup"><span data-stu-id="ee2af-115">-Confirm</span></span>
<span data-ttu-id="ee2af-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ee2af-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee2af-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee2af-117">-WhatIf</span></span>
<span data-ttu-id="ee2af-118">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ee2af-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee2af-119">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ee2af-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee2af-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee2af-120">CommonParameters</span></span>
<span data-ttu-id="ee2af-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ee2af-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee2af-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ee2af-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee2af-123">輸入</span><span class="sxs-lookup"><span data-stu-id="ee2af-123">INPUTS</span></span>

### <span data-ttu-id="ee2af-124">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ee2af-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="ee2af-125">參數： ApplicationGateway (ByValue) </span><span class="sxs-lookup"><span data-stu-id="ee2af-125">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="ee2af-126">輸出</span><span class="sxs-lookup"><span data-stu-id="ee2af-126">OUTPUTS</span></span>

### <span data-ttu-id="ee2af-127">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ee2af-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ee2af-128">筆記</span><span class="sxs-lookup"><span data-stu-id="ee2af-128">NOTES</span></span>
* <span data-ttu-id="ee2af-129">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路</span><span class="sxs-lookup"><span data-stu-id="ee2af-129">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="ee2af-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="ee2af-130">RELATED LINKS</span></span>

[<span data-ttu-id="ee2af-131">附加 AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ee2af-131">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="ee2af-132">AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ee2af-132">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="ee2af-133">新-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ee2af-133">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="ee2af-134">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ee2af-134">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)


