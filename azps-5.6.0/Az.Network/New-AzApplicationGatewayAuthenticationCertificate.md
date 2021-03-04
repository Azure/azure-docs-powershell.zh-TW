---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4736FA0D-222D-4D69-BCBD-72036303A20E
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: c4c2c2041c6bf21aa6bf8b13055d0dac5ffbc64a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916728"
---
# <span data-ttu-id="7c143-101">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="7c143-101">New-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="7c143-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7c143-102">SYNOPSIS</span></span>
<span data-ttu-id="7c143-103">為應用程式閘道建立驗證憑證。</span><span class="sxs-lookup"><span data-stu-id="7c143-103">Creates an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="7c143-104">語法</span><span class="sxs-lookup"><span data-stu-id="7c143-104">SYNTAX</span></span>

```
New-AzApplicationGatewayAuthenticationCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c143-105">描述</span><span class="sxs-lookup"><span data-stu-id="7c143-105">DESCRIPTION</span></span>
<span data-ttu-id="7c143-106">**New-AzApplicationGatewayAuthenticationCertificate** Cmdlet 會為 Azure 應用程式閘道建立驗證憑證。</span><span class="sxs-lookup"><span data-stu-id="7c143-106">The **New-AzApplicationGatewayAuthenticationCertificate** cmdlet creates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="7c143-107">例子</span><span class="sxs-lookup"><span data-stu-id="7c143-107">EXAMPLES</span></span>

### <span data-ttu-id="7c143-108">範例 1：建立驗證憑證</span><span class="sxs-lookup"><span data-stu-id="7c143-108">Example 1: Create an authentication certificate</span></span>
```
PS C:\> $cert = New-AzApplicationGatewayAuthenticationCertificate -Name "cert01" -CertificateFile "C:\cert.cer"
```

<span data-ttu-id="7c143-109">第一個命令會建立名為 cert01 的驗證憑證。</span><span class="sxs-lookup"><span data-stu-id="7c143-109">The first command creates authentication certificate named cert01.</span></span>

## <span data-ttu-id="7c143-110">參數</span><span class="sxs-lookup"><span data-stu-id="7c143-110">PARAMETERS</span></span>

### <span data-ttu-id="7c143-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="7c143-111">-CertificateFile</span></span>
<span data-ttu-id="7c143-112">指定驗證憑證的路徑。</span><span class="sxs-lookup"><span data-stu-id="7c143-112">Specifies the path of the authentication certificate.</span></span>

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

### <span data-ttu-id="7c143-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c143-113">-DefaultProfile</span></span>
<span data-ttu-id="7c143-114">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="7c143-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c143-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="7c143-115">-Name</span></span>
<span data-ttu-id="7c143-116">指定驗證憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="7c143-116">Specifies a name for the authentication certificate.</span></span>

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

### <span data-ttu-id="7c143-117">-確認</span><span class="sxs-lookup"><span data-stu-id="7c143-117">-Confirm</span></span>
<span data-ttu-id="7c143-118">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="7c143-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c143-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c143-119">-WhatIf</span></span>
<span data-ttu-id="7c143-120">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7c143-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c143-121">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7c143-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c143-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c143-122">CommonParameters</span></span>
<span data-ttu-id="7c143-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7c143-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c143-124">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="7c143-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c143-125">輸入</span><span class="sxs-lookup"><span data-stu-id="7c143-125">INPUTS</span></span>

### <span data-ttu-id="7c143-126">沒有</span><span class="sxs-lookup"><span data-stu-id="7c143-126">None</span></span>

## <span data-ttu-id="7c143-127">輸出</span><span class="sxs-lookup"><span data-stu-id="7c143-127">OUTPUTS</span></span>

### <span data-ttu-id="7c143-128">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="7c143-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="7c143-129">筆記</span><span class="sxs-lookup"><span data-stu-id="7c143-129">NOTES</span></span>
* <span data-ttu-id="7c143-130">關鍵字：azure、azurerm、arm、資源、管理、管理員、網路、網路</span><span class="sxs-lookup"><span data-stu-id="7c143-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="7c143-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="7c143-131">RELATED LINKS</span></span>

[<span data-ttu-id="7c143-132">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="7c143-132">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="7c143-133">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="7c143-133">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="7c143-134">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="7c143-134">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="7c143-135">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="7c143-135">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


