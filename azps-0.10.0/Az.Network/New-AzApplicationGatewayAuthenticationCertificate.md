---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4736FA0D-222D-4D69-BCBD-72036303A20E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 8f3685fddf4796cd0ad500c261f157e8ac5b95f5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794326"
---
# <span data-ttu-id="18cb5-101">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="18cb5-101">New-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="18cb5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="18cb5-102">SYNOPSIS</span></span>
<span data-ttu-id="18cb5-103">建立應用程式閘道的驗證憑證。</span><span class="sxs-lookup"><span data-stu-id="18cb5-103">Creates an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="18cb5-104">句法</span><span class="sxs-lookup"><span data-stu-id="18cb5-104">SYNTAX</span></span>

```
New-AzApplicationGatewayAuthenticationCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18cb5-105">說明</span><span class="sxs-lookup"><span data-stu-id="18cb5-105">DESCRIPTION</span></span>
<span data-ttu-id="18cb5-106">**新的-AzApplicationGatewayAuthenticationCertificate** Cmdlet 會建立 Azure 應用程式閘道的驗證憑證。</span><span class="sxs-lookup"><span data-stu-id="18cb5-106">The **New-AzApplicationGatewayAuthenticationCertificate** cmdlet creates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="18cb5-107">示例</span><span class="sxs-lookup"><span data-stu-id="18cb5-107">EXAMPLES</span></span>

### <span data-ttu-id="18cb5-108">sr-1</span><span class="sxs-lookup"><span data-stu-id="18cb5-108">1:</span></span>
```

```

## <span data-ttu-id="18cb5-109">參數</span><span class="sxs-lookup"><span data-stu-id="18cb5-109">PARAMETERS</span></span>

### <span data-ttu-id="18cb5-110">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="18cb5-110">-CertificateFile</span></span>
<span data-ttu-id="18cb5-111">指定驗證憑證的路徑。</span><span class="sxs-lookup"><span data-stu-id="18cb5-111">Specifies the path of the authentication certificate.</span></span>

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

### <span data-ttu-id="18cb5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18cb5-112">-DefaultProfile</span></span>
<span data-ttu-id="18cb5-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="18cb5-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18cb5-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="18cb5-114">-Name</span></span>
<span data-ttu-id="18cb5-115">指定驗證憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="18cb5-115">Specifies a name for the authentication certificate.</span></span>

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

### <span data-ttu-id="18cb5-116">-確認</span><span class="sxs-lookup"><span data-stu-id="18cb5-116">-Confirm</span></span>
<span data-ttu-id="18cb5-117">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="18cb5-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18cb5-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18cb5-118">-WhatIf</span></span>
<span data-ttu-id="18cb5-119">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="18cb5-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18cb5-120">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="18cb5-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18cb5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18cb5-121">CommonParameters</span></span>
<span data-ttu-id="18cb5-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="18cb5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18cb5-123">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="18cb5-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18cb5-124">輸入</span><span class="sxs-lookup"><span data-stu-id="18cb5-124">INPUTS</span></span>

### <span data-ttu-id="18cb5-125">System.object</span><span class="sxs-lookup"><span data-stu-id="18cb5-125">System.String</span></span>

## <span data-ttu-id="18cb5-126">輸出</span><span class="sxs-lookup"><span data-stu-id="18cb5-126">OUTPUTS</span></span>

### <span data-ttu-id="18cb5-127">PSApplicationGatewayAuthenticationCertificate 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="18cb5-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="18cb5-128">筆記</span><span class="sxs-lookup"><span data-stu-id="18cb5-128">NOTES</span></span>
* <span data-ttu-id="18cb5-129">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路</span><span class="sxs-lookup"><span data-stu-id="18cb5-129">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="18cb5-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="18cb5-130">RELATED LINKS</span></span>

[<span data-ttu-id="18cb5-131">附加 AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="18cb5-131">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="18cb5-132">AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="18cb5-132">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="18cb5-133">移除-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="18cb5-133">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="18cb5-134">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="18cb5-134">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


