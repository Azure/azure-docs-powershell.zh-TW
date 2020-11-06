---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: 0505f7452c20c0bdb3ccf3a9bc203380479083ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93443800"
---
# <span data-ttu-id="bbe56-101">Set-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="bbe56-101">Set-AzureRmApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="bbe56-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bbe56-102">SYNOPSIS</span></span>
<span data-ttu-id="bbe56-103">更新應用程式閘道的根信任證書。</span><span class="sxs-lookup"><span data-stu-id="bbe56-103">Updates a Trusted Root Certificate of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bbe56-104">句法</span><span class="sxs-lookup"><span data-stu-id="bbe56-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayTrustedRootCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bbe56-105">說明</span><span class="sxs-lookup"><span data-stu-id="bbe56-105">DESCRIPTION</span></span>
<span data-ttu-id="bbe56-106">**AzureRmApplicationGatewayTrustedRootCertificate** Cmdlet 會修改應用程式閘道的現有根信任證書。</span><span class="sxs-lookup"><span data-stu-id="bbe56-106">The **Set-AzureRmApplicationGatewayTrustedRootCertificate** cmdlet modifies the existing trusted root certificate of an Application Gateway.</span></span>

## <span data-ttu-id="bbe56-107">示例</span><span class="sxs-lookup"><span data-stu-id="bbe56-107">EXAMPLES</span></span>

### <span data-ttu-id="bbe56-108">範例1</span><span class="sxs-lookup"><span data-stu-id="bbe56-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzureRmApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Set-AzureRmApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\rootCAUpdated.cer"
PS C:\> $gw = Set-AzureRmApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="bbe56-109">上述範例案例示範如何在已匯總根憑證時更新現有的受根信任證書。</span><span class="sxs-lookup"><span data-stu-id="bbe56-109">Above example scenarios shows how to update an existing trusted root certificate when a root certificate is rolled.</span></span>
<span data-ttu-id="bbe56-110">第一個命令會取得應用程式閘道，並將它儲存在 $gw 變數中。</span><span class="sxs-lookup"><span data-stu-id="bbe56-110">The first command gets an application gateway and stores it in the $gw variable.</span></span>
<span data-ttu-id="bbe56-111">第二個命令會使用新的根憑證來修改現有的根信任憑證。</span><span class="sxs-lookup"><span data-stu-id="bbe56-111">The second command modifies the existing trusted root certificate with a new root certificate.</span></span>
<span data-ttu-id="bbe56-112">第三個命令會更新 Azure 上的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="bbe56-112">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="bbe56-113">參數</span><span class="sxs-lookup"><span data-stu-id="bbe56-113">PARAMETERS</span></span>

### <span data-ttu-id="bbe56-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bbe56-114">-ApplicationGateway</span></span>
<span data-ttu-id="bbe56-115">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bbe56-115">The applicationGateway</span></span>

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

### <span data-ttu-id="bbe56-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="bbe56-116">-CertificateFile</span></span>
<span data-ttu-id="bbe56-117">憑證 CER 檔案的路徑</span><span class="sxs-lookup"><span data-stu-id="bbe56-117">Path of certificate CER file</span></span>

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

### <span data-ttu-id="bbe56-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbe56-118">-DefaultProfile</span></span>
<span data-ttu-id="bbe56-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bbe56-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bbe56-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="bbe56-120">-Name</span></span>
<span data-ttu-id="bbe56-121">TrustedRoot 憑證的名稱</span><span class="sxs-lookup"><span data-stu-id="bbe56-121">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="bbe56-122">-確認</span><span class="sxs-lookup"><span data-stu-id="bbe56-122">-Confirm</span></span>
<span data-ttu-id="bbe56-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="bbe56-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bbe56-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbe56-124">-WhatIf</span></span>
<span data-ttu-id="bbe56-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bbe56-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bbe56-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bbe56-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bbe56-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbe56-127">CommonParameters</span></span>
<span data-ttu-id="bbe56-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bbe56-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbe56-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bbe56-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbe56-130">輸入</span><span class="sxs-lookup"><span data-stu-id="bbe56-130">INPUTS</span></span>

### <span data-ttu-id="bbe56-131">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="bbe56-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="bbe56-132">輸出</span><span class="sxs-lookup"><span data-stu-id="bbe56-132">OUTPUTS</span></span>

### <span data-ttu-id="bbe56-133">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="bbe56-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="bbe56-134">筆記</span><span class="sxs-lookup"><span data-stu-id="bbe56-134">NOTES</span></span>

## <span data-ttu-id="bbe56-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="bbe56-135">RELATED LINKS</span></span>
