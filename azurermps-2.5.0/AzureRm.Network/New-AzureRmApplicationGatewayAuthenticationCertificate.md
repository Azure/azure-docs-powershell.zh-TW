---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4736FA0D-222D-4D69-BCBD-72036303A20E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
ms.openlocfilehash: 3847c1026f8cea6f3c33db45215a7a3253e4c680
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800821"
---
# <span data-ttu-id="6fd66-101">New-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="6fd66-101">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="6fd66-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6fd66-102">SYNOPSIS</span></span>
<span data-ttu-id="6fd66-103">建立應用程式閘道的驗證憑證。</span><span class="sxs-lookup"><span data-stu-id="6fd66-103">Creates an authentication certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6fd66-104">句法</span><span class="sxs-lookup"><span data-stu-id="6fd66-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayAuthenticationCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6fd66-105">說明</span><span class="sxs-lookup"><span data-stu-id="6fd66-105">DESCRIPTION</span></span>
<span data-ttu-id="6fd66-106">**新的-AzureRmApplicationGatewayAuthenticationCertificate** Cmdlet 會建立 Azure 應用程式閘道的驗證憑證。</span><span class="sxs-lookup"><span data-stu-id="6fd66-106">The **New-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet creates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="6fd66-107">示例</span><span class="sxs-lookup"><span data-stu-id="6fd66-107">EXAMPLES</span></span>

### <span data-ttu-id="6fd66-108">sr-1</span><span class="sxs-lookup"><span data-stu-id="6fd66-108">1:</span></span>
```

```

## <span data-ttu-id="6fd66-109">參數</span><span class="sxs-lookup"><span data-stu-id="6fd66-109">PARAMETERS</span></span>

### <span data-ttu-id="6fd66-110">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="6fd66-110">-CertificateFile</span></span>
<span data-ttu-id="6fd66-111">指定驗證憑證的路徑。</span><span class="sxs-lookup"><span data-stu-id="6fd66-111">Specifies the path of the authentication certificate.</span></span>

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

### <span data-ttu-id="6fd66-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fd66-112">-DefaultProfile</span></span>
<span data-ttu-id="6fd66-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6fd66-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6fd66-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="6fd66-114">-Name</span></span>
<span data-ttu-id="6fd66-115">指定驗證憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="6fd66-115">Specifies a name for the authentication certificate.</span></span>

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

### <span data-ttu-id="6fd66-116">-確認</span><span class="sxs-lookup"><span data-stu-id="6fd66-116">-Confirm</span></span>
<span data-ttu-id="6fd66-117">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6fd66-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6fd66-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fd66-118">-WhatIf</span></span>
<span data-ttu-id="6fd66-119">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6fd66-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6fd66-120">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6fd66-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6fd66-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fd66-121">CommonParameters</span></span>
<span data-ttu-id="6fd66-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6fd66-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fd66-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6fd66-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fd66-124">輸入</span><span class="sxs-lookup"><span data-stu-id="6fd66-124">INPUTS</span></span>

### <span data-ttu-id="6fd66-125">System.object</span><span class="sxs-lookup"><span data-stu-id="6fd66-125">System.String</span></span>

## <span data-ttu-id="6fd66-126">輸出</span><span class="sxs-lookup"><span data-stu-id="6fd66-126">OUTPUTS</span></span>

### <span data-ttu-id="6fd66-127">PSApplicationGatewayAuthenticationCertificate 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="6fd66-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="6fd66-128">筆記</span><span class="sxs-lookup"><span data-stu-id="6fd66-128">NOTES</span></span>
* <span data-ttu-id="6fd66-129">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路</span><span class="sxs-lookup"><span data-stu-id="6fd66-129">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="6fd66-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="6fd66-130">RELATED LINKS</span></span>

[<span data-ttu-id="6fd66-131">附加 AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="6fd66-131">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="6fd66-132">AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="6fd66-132">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="6fd66-133">移除-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="6fd66-133">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="6fd66-134">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="6fd66-134">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)


