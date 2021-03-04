---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: bacdca3f26e18f3dc41ac19990e48f9e6bb63c1c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906545"
---
# <span data-ttu-id="cf42f-101">New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="cf42f-101">New-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="cf42f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="cf42f-102">SYNOPSIS</span></span>
<span data-ttu-id="cf42f-103">為應用程式閘道建立信任的根憑證。</span><span class="sxs-lookup"><span data-stu-id="cf42f-103">Creates a Trusted Root Certificate for an application gateway.</span></span>

## <span data-ttu-id="cf42f-104">語法</span><span class="sxs-lookup"><span data-stu-id="cf42f-104">SYNTAX</span></span>

```
New-AzApplicationGatewayTrustedRootCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf42f-105">描述</span><span class="sxs-lookup"><span data-stu-id="cf42f-105">DESCRIPTION</span></span>
<span data-ttu-id="cf42f-106">**New-AzApplicationGatewayTrustedRootCertificate** Cmdlet 會為 Azure 應用程式閘道建立信任的根憑證。</span><span class="sxs-lookup"><span data-stu-id="cf42f-106">The **New-AzApplicationGatewayTrustedRootCertificate** cmdlet creates a Trusted Root Certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="cf42f-107">例子</span><span class="sxs-lookup"><span data-stu-id="cf42f-107">EXAMPLES</span></span>

### <span data-ttu-id="cf42f-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="cf42f-108">Example 1</span></span>
```powershell
PS C:\> $certFilePath = ".\rootCA.cer"
PS C:\> $trc = New-AzApplicationGatewayTrustedRootCertificate -Name "trc1" -CertificateFile $certFilePath
```

<span data-ttu-id="cf42f-109">此命令會建立名為 List "trc1" 的受根信任憑證，並儲存在名為 $trc 的變數中。</span><span class="sxs-lookup"><span data-stu-id="cf42f-109">This command creates a Trusted Root Certificate named List "trc1" and stores the result in the variable named $trc.</span></span>

## <span data-ttu-id="cf42f-110">參數</span><span class="sxs-lookup"><span data-stu-id="cf42f-110">PARAMETERS</span></span>

### <span data-ttu-id="cf42f-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="cf42f-111">-CertificateFile</span></span>
<span data-ttu-id="cf42f-112">憑證憑證檔案的路徑</span><span class="sxs-lookup"><span data-stu-id="cf42f-112">Path of certificate CER file</span></span>

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

### <span data-ttu-id="cf42f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf42f-113">-DefaultProfile</span></span>
<span data-ttu-id="cf42f-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="cf42f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf42f-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="cf42f-115">-Name</span></span>
<span data-ttu-id="cf42f-116">TrustedRoot 憑證的名稱</span><span class="sxs-lookup"><span data-stu-id="cf42f-116">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="cf42f-117">-確認</span><span class="sxs-lookup"><span data-stu-id="cf42f-117">-Confirm</span></span>
<span data-ttu-id="cf42f-118">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="cf42f-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf42f-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf42f-119">-WhatIf</span></span>
<span data-ttu-id="cf42f-120">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cf42f-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf42f-121">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cf42f-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf42f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf42f-122">CommonParameters</span></span>
<span data-ttu-id="cf42f-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="cf42f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf42f-124">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="cf42f-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf42f-125">輸入</span><span class="sxs-lookup"><span data-stu-id="cf42f-125">INPUTS</span></span>

### <span data-ttu-id="cf42f-126">沒有</span><span class="sxs-lookup"><span data-stu-id="cf42f-126">None</span></span>

## <span data-ttu-id="cf42f-127">輸出</span><span class="sxs-lookup"><span data-stu-id="cf42f-127">OUTPUTS</span></span>

### <span data-ttu-id="cf42f-128">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="cf42f-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="cf42f-129">筆記</span><span class="sxs-lookup"><span data-stu-id="cf42f-129">NOTES</span></span>

## <span data-ttu-id="cf42f-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="cf42f-130">RELATED LINKS</span></span>

[<span data-ttu-id="cf42f-131">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="cf42f-131">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="cf42f-132">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="cf42f-132">Get-AzApplicationGatewayTrustedRootCertificate</span></span>](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="cf42f-133">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="cf42f-133">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="cf42f-134">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="cf42f-134">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)
