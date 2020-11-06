---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4736FA0D-222D-4D69-BCBD-72036303A20E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 8edf8d3cee1936af263d759e512a6683af1ccde8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452167"
---
# <span data-ttu-id="eade6-101">New-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="eade6-101">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="eade6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="eade6-102">SYNOPSIS</span></span>
<span data-ttu-id="eade6-103">建立應用程式閘道的驗證憑證。</span><span class="sxs-lookup"><span data-stu-id="eade6-103">Creates an authentication certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eade6-104">句法</span><span class="sxs-lookup"><span data-stu-id="eade6-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayAuthenticationCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eade6-105">說明</span><span class="sxs-lookup"><span data-stu-id="eade6-105">DESCRIPTION</span></span>
<span data-ttu-id="eade6-106">**新的-AzureRmApplicationGatewayAuthenticationCertificate** Cmdlet 會建立 Azure 應用程式閘道的驗證憑證。</span><span class="sxs-lookup"><span data-stu-id="eade6-106">The **New-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet creates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="eade6-107">示例</span><span class="sxs-lookup"><span data-stu-id="eade6-107">EXAMPLES</span></span>

## <span data-ttu-id="eade6-108">參數</span><span class="sxs-lookup"><span data-stu-id="eade6-108">PARAMETERS</span></span>

### <span data-ttu-id="eade6-109">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="eade6-109">-CertificateFile</span></span>
<span data-ttu-id="eade6-110">指定驗證憑證的路徑。</span><span class="sxs-lookup"><span data-stu-id="eade6-110">Specifies the path of the authentication certificate.</span></span>

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

### <span data-ttu-id="eade6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eade6-111">-DefaultProfile</span></span>
<span data-ttu-id="eade6-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="eade6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eade6-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="eade6-113">-Name</span></span>
<span data-ttu-id="eade6-114">指定驗證憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="eade6-114">Specifies a name for the authentication certificate.</span></span>

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

### <span data-ttu-id="eade6-115">-確認</span><span class="sxs-lookup"><span data-stu-id="eade6-115">-Confirm</span></span>
<span data-ttu-id="eade6-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="eade6-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eade6-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eade6-117">-WhatIf</span></span>
<span data-ttu-id="eade6-118">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="eade6-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eade6-119">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="eade6-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eade6-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eade6-120">CommonParameters</span></span>
<span data-ttu-id="eade6-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="eade6-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eade6-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="eade6-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eade6-123">輸入</span><span class="sxs-lookup"><span data-stu-id="eade6-123">INPUTS</span></span>

### <span data-ttu-id="eade6-124">System.object</span><span class="sxs-lookup"><span data-stu-id="eade6-124">System.String</span></span>

## <span data-ttu-id="eade6-125">輸出</span><span class="sxs-lookup"><span data-stu-id="eade6-125">OUTPUTS</span></span>

### <span data-ttu-id="eade6-126">PSApplicationGatewayAuthenticationCertificate 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="eade6-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="eade6-127">筆記</span><span class="sxs-lookup"><span data-stu-id="eade6-127">NOTES</span></span>
* <span data-ttu-id="eade6-128">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路</span><span class="sxs-lookup"><span data-stu-id="eade6-128">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="eade6-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="eade6-129">RELATED LINKS</span></span>

[<span data-ttu-id="eade6-130">附加 AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="eade6-130">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="eade6-131">AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="eade6-131">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="eade6-132">移除-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="eade6-132">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="eade6-133">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="eade6-133">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)


