---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4736FA0D-222D-4D69-BCBD-72036303A20E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: c43fe72f8f3669b7e6e123a7f1d606771b161084
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100140442"
---
# <span data-ttu-id="b76c3-101">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="b76c3-101">New-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="b76c3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b76c3-102">SYNOPSIS</span></span>
<span data-ttu-id="b76c3-103">建立應用程式閘道的驗證憑證。</span><span class="sxs-lookup"><span data-stu-id="b76c3-103">Creates an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="b76c3-104">句法</span><span class="sxs-lookup"><span data-stu-id="b76c3-104">SYNTAX</span></span>

```
New-AzApplicationGatewayAuthenticationCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b76c3-105">說明</span><span class="sxs-lookup"><span data-stu-id="b76c3-105">DESCRIPTION</span></span>
<span data-ttu-id="b76c3-106">**新的-AzApplicationGatewayAuthenticationCertificate** Cmdlet 會建立 Azure 應用程式閘道的驗證憑證。</span><span class="sxs-lookup"><span data-stu-id="b76c3-106">The **New-AzApplicationGatewayAuthenticationCertificate** cmdlet creates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="b76c3-107">示例</span><span class="sxs-lookup"><span data-stu-id="b76c3-107">EXAMPLES</span></span>

### <span data-ttu-id="b76c3-108">範例1：建立驗證憑證</span><span class="sxs-lookup"><span data-stu-id="b76c3-108">Example 1: Create an authentication certificate</span></span>
```
PS C:\> $cert = New-AzApplicationGatewayAuthenticationCertificate -Name "cert01" -CertificateFile "C:\cert.cer"
```

<span data-ttu-id="b76c3-109">第一個命令會建立名為 cert01 的驗證憑證。</span><span class="sxs-lookup"><span data-stu-id="b76c3-109">The first command creates authentication certificate named cert01.</span></span>

## <span data-ttu-id="b76c3-110">參數</span><span class="sxs-lookup"><span data-stu-id="b76c3-110">PARAMETERS</span></span>

### <span data-ttu-id="b76c3-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="b76c3-111">-CertificateFile</span></span>
<span data-ttu-id="b76c3-112">指定驗證憑證的路徑。</span><span class="sxs-lookup"><span data-stu-id="b76c3-112">Specifies the path of the authentication certificate.</span></span>

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

### <span data-ttu-id="b76c3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b76c3-113">-DefaultProfile</span></span>
<span data-ttu-id="b76c3-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b76c3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b76c3-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="b76c3-115">-Name</span></span>
<span data-ttu-id="b76c3-116">指定驗證憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="b76c3-116">Specifies a name for the authentication certificate.</span></span>

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

### <span data-ttu-id="b76c3-117">-確認</span><span class="sxs-lookup"><span data-stu-id="b76c3-117">-Confirm</span></span>
<span data-ttu-id="b76c3-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b76c3-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b76c3-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b76c3-119">-WhatIf</span></span>
<span data-ttu-id="b76c3-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b76c3-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b76c3-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b76c3-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b76c3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b76c3-122">CommonParameters</span></span>
<span data-ttu-id="b76c3-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b76c3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b76c3-124">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b76c3-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b76c3-125">輸入</span><span class="sxs-lookup"><span data-stu-id="b76c3-125">INPUTS</span></span>

### <span data-ttu-id="b76c3-126">所有</span><span class="sxs-lookup"><span data-stu-id="b76c3-126">None</span></span>

## <span data-ttu-id="b76c3-127">輸出</span><span class="sxs-lookup"><span data-stu-id="b76c3-127">OUTPUTS</span></span>

### <span data-ttu-id="b76c3-128">PSApplicationGatewayAuthenticationCertificate 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b76c3-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="b76c3-129">筆記</span><span class="sxs-lookup"><span data-stu-id="b76c3-129">NOTES</span></span>
* <span data-ttu-id="b76c3-130">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路</span><span class="sxs-lookup"><span data-stu-id="b76c3-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="b76c3-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="b76c3-131">RELATED LINKS</span></span>

[<span data-ttu-id="b76c3-132">附加 AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="b76c3-132">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="b76c3-133">AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="b76c3-133">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="b76c3-134">移除-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="b76c3-134">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="b76c3-135">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="b76c3-135">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


