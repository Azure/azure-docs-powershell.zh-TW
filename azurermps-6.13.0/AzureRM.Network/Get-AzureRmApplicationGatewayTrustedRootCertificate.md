---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: c37c55539f983b490c917e1fe062f14b252ee477
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624897"
---
# <span data-ttu-id="2c897-101">Get-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="2c897-101">Get-AzureRmApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="2c897-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2c897-102">SYNOPSIS</span></span>
<span data-ttu-id="2c897-103">從應用程式閘道取得具有特定名稱的受根信任證書。</span><span class="sxs-lookup"><span data-stu-id="2c897-103">Gets the Trusted Root Certificate with a specific name from the Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c897-104">句法</span><span class="sxs-lookup"><span data-stu-id="2c897-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayTrustedRootCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c897-105">說明</span><span class="sxs-lookup"><span data-stu-id="2c897-105">DESCRIPTION</span></span>
<span data-ttu-id="2c897-106">**AzureRmApplicationGatewayTrustedRootCertificate** Cmdlet 會從應用程式閘道取得具有特定名稱的根信任憑證。</span><span class="sxs-lookup"><span data-stu-id="2c897-106">The **Get-AzureRmApplicationGatewayTrustedRootCertificate** cmdlet gets Trusted Root Certificate with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="2c897-107">示例</span><span class="sxs-lookup"><span data-stu-id="2c897-107">EXAMPLES</span></span>

### <span data-ttu-id="2c897-108">範例1</span><span class="sxs-lookup"><span data-stu-id="2c897-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzureRmApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $trustedRootCert = Get-AzureRmApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\rootCA.cer"
```

<span data-ttu-id="2c897-109">第一個命令會取得應用程式閘道，並將它儲存在 $gw 變數中。</span><span class="sxs-lookup"><span data-stu-id="2c897-109">The first command gets the Application Gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="2c897-110">第二個命令會從應用程式閘道取得具有指定名稱的受根信任證書。</span><span class="sxs-lookup"><span data-stu-id="2c897-110">The second command gets the Trusted Root Certificate with a specified name from the Application Gateway.</span></span>

## <span data-ttu-id="2c897-111">參數</span><span class="sxs-lookup"><span data-stu-id="2c897-111">PARAMETERS</span></span>

### <span data-ttu-id="2c897-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2c897-112">-ApplicationGateway</span></span>
<span data-ttu-id="2c897-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2c897-113">The applicationGateway</span></span>

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

### <span data-ttu-id="2c897-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c897-114">-DefaultProfile</span></span>
<span data-ttu-id="2c897-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2c897-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c897-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="2c897-116">-Name</span></span>
<span data-ttu-id="2c897-117">TrustedRoot 憑證的名稱</span><span class="sxs-lookup"><span data-stu-id="2c897-117">The name of the TrustedRoot certificate</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c897-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c897-118">CommonParameters</span></span>
<span data-ttu-id="2c897-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2c897-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c897-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2c897-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c897-121">輸入</span><span class="sxs-lookup"><span data-stu-id="2c897-121">INPUTS</span></span>

### <span data-ttu-id="2c897-122">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="2c897-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2c897-123">輸出</span><span class="sxs-lookup"><span data-stu-id="2c897-123">OUTPUTS</span></span>

### <span data-ttu-id="2c897-124">PSApplicationGatewayTrustedRootCertificate 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="2c897-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="2c897-125">筆記</span><span class="sxs-lookup"><span data-stu-id="2c897-125">NOTES</span></span>

## <span data-ttu-id="2c897-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="2c897-126">RELATED LINKS</span></span>
