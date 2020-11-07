---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 29BB24C4-1EC9-47DE-A5B8-5EEA4525AE3A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
ms.openlocfilehash: 00ad021e86617d08f0ca30f660cac28110348885
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800418"
---
# <span data-ttu-id="fbbb4-101">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="fbbb4-101">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="fbbb4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fbbb4-102">SYNOPSIS</span></span>
<span data-ttu-id="fbbb4-103">從應用程式閘道移除驗證憑證。</span><span class="sxs-lookup"><span data-stu-id="fbbb4-103">Removes an authentication certificate from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fbbb4-104">句法</span><span class="sxs-lookup"><span data-stu-id="fbbb4-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayAuthenticationCertificate -Name <String>
 -ApplicationGateway <PSApplicationGateway> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fbbb4-105">說明</span><span class="sxs-lookup"><span data-stu-id="fbbb4-105">DESCRIPTION</span></span>
<span data-ttu-id="fbbb4-106">**AzureRmApplicationGatewayAuthenticationCertificate** Cmdlet 會從 Azure 應用程式閘道移除驗證憑證。</span><span class="sxs-lookup"><span data-stu-id="fbbb4-106">The **Remove-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet removes an authentication certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="fbbb4-107">示例</span><span class="sxs-lookup"><span data-stu-id="fbbb4-107">EXAMPLES</span></span>

### <span data-ttu-id="fbbb4-108">sr-1</span><span class="sxs-lookup"><span data-stu-id="fbbb4-108">1:</span></span>
```

```

## <span data-ttu-id="fbbb4-109">參數</span><span class="sxs-lookup"><span data-stu-id="fbbb4-109">PARAMETERS</span></span>

### <span data-ttu-id="fbbb4-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fbbb4-110">-ApplicationGateway</span></span>
<span data-ttu-id="fbbb4-111">指定此 Cmdlet 從中移除驗證憑證的應用程式閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="fbbb4-111">Specifies the name of application gateway from which this cmdlet removes an authentication certificate.</span></span>

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

### <span data-ttu-id="fbbb4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbbb4-112">-DefaultProfile</span></span>
<span data-ttu-id="fbbb4-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fbbb4-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fbbb4-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="fbbb4-114">-Name</span></span>
<span data-ttu-id="fbbb4-115">指定此 Cmdlet 移除之驗證憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="fbbb4-115">Specifies the name of the authentication certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="fbbb4-116">-確認</span><span class="sxs-lookup"><span data-stu-id="fbbb4-116">-Confirm</span></span>
<span data-ttu-id="fbbb4-117">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fbbb4-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fbbb4-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbbb4-118">-WhatIf</span></span>
<span data-ttu-id="fbbb4-119">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fbbb4-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fbbb4-120">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fbbb4-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fbbb4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbbb4-121">CommonParameters</span></span>
<span data-ttu-id="fbbb4-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fbbb4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbbb4-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fbbb4-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbbb4-124">輸入</span><span class="sxs-lookup"><span data-stu-id="fbbb4-124">INPUTS</span></span>

### <span data-ttu-id="fbbb4-125">System.object</span><span class="sxs-lookup"><span data-stu-id="fbbb4-125">System.String</span></span>

## <span data-ttu-id="fbbb4-126">輸出</span><span class="sxs-lookup"><span data-stu-id="fbbb4-126">OUTPUTS</span></span>

### <span data-ttu-id="fbbb4-127">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="fbbb4-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="fbbb4-128">筆記</span><span class="sxs-lookup"><span data-stu-id="fbbb4-128">NOTES</span></span>
* <span data-ttu-id="fbbb4-129">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路</span><span class="sxs-lookup"><span data-stu-id="fbbb4-129">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="fbbb4-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="fbbb4-130">RELATED LINKS</span></span>

[<span data-ttu-id="fbbb4-131">附加 AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="fbbb4-131">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="fbbb4-132">AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="fbbb4-132">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="fbbb4-133">新-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="fbbb4-133">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="fbbb4-134">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="fbbb4-134">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)


