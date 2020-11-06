---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: 5f71f9a28eb1daae1bee070907675c87002241f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93457003"
---
# <span data-ttu-id="4079a-101">New-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="4079a-101">New-AzureRmApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="4079a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4079a-102">SYNOPSIS</span></span>
<span data-ttu-id="4079a-103">為應用程式閘道建立信任的根憑證。</span><span class="sxs-lookup"><span data-stu-id="4079a-103">Creates a Trusted Root Certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4079a-104">句法</span><span class="sxs-lookup"><span data-stu-id="4079a-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayTrustedRootCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4079a-105">說明</span><span class="sxs-lookup"><span data-stu-id="4079a-105">DESCRIPTION</span></span>
<span data-ttu-id="4079a-106">**新的-AzureRmApplicationGatewayTrustedRootCertificate** Cmdlet 會針對 Azure 應用程式閘道建立信任的根憑證。</span><span class="sxs-lookup"><span data-stu-id="4079a-106">The **New-AzureRmApplicationGatewayTrustedRootCertificate** cmdlet creates a Trusted Root Certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="4079a-107">示例</span><span class="sxs-lookup"><span data-stu-id="4079a-107">EXAMPLES</span></span>

### <span data-ttu-id="4079a-108">範例1</span><span class="sxs-lookup"><span data-stu-id="4079a-108">Example 1</span></span>
```powershell
PS C:\> $certFilePath = ".\rootCA.cer"
PS C:\> $trc = New-AzureRmApplicationGatewayTrustedRootCertificate -Name "trc1" --CertificateFile $certFilePath
```

<span data-ttu-id="4079a-109">這個命令會建立名為 List "trc1" 的根信任證書，並將結果儲存在名為 $trc 的變數中。</span><span class="sxs-lookup"><span data-stu-id="4079a-109">This command creates a Trusted Root Certificate named List "trc1" and stores the result in the variable named $trc.</span></span>

## <span data-ttu-id="4079a-110">參數</span><span class="sxs-lookup"><span data-stu-id="4079a-110">PARAMETERS</span></span>

### <span data-ttu-id="4079a-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="4079a-111">-CertificateFile</span></span>
<span data-ttu-id="4079a-112">憑證 CER 檔案的路徑</span><span class="sxs-lookup"><span data-stu-id="4079a-112">Path of certificate CER file</span></span>

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

### <span data-ttu-id="4079a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4079a-113">-DefaultProfile</span></span>
<span data-ttu-id="4079a-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4079a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4079a-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="4079a-115">-Name</span></span>
<span data-ttu-id="4079a-116">TrustedRoot 憑證的名稱</span><span class="sxs-lookup"><span data-stu-id="4079a-116">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="4079a-117">-確認</span><span class="sxs-lookup"><span data-stu-id="4079a-117">-Confirm</span></span>
<span data-ttu-id="4079a-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4079a-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4079a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4079a-119">-WhatIf</span></span>
<span data-ttu-id="4079a-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4079a-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4079a-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4079a-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4079a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4079a-122">CommonParameters</span></span>
<span data-ttu-id="4079a-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4079a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4079a-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4079a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4079a-125">輸入</span><span class="sxs-lookup"><span data-stu-id="4079a-125">INPUTS</span></span>

### <span data-ttu-id="4079a-126">所有</span><span class="sxs-lookup"><span data-stu-id="4079a-126">None</span></span>

## <span data-ttu-id="4079a-127">輸出</span><span class="sxs-lookup"><span data-stu-id="4079a-127">OUTPUTS</span></span>

### <span data-ttu-id="4079a-128">PSApplicationGatewayTrustedRootCertificate 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4079a-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="4079a-129">筆記</span><span class="sxs-lookup"><span data-stu-id="4079a-129">NOTES</span></span>

## <span data-ttu-id="4079a-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="4079a-130">RELATED LINKS</span></span>
