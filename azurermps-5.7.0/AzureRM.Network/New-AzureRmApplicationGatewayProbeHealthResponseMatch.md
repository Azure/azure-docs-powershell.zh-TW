---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayprobehealthresponsematch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayProbeHealthResponseMatch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayProbeHealthResponseMatch.md
ms.openlocfilehash: 3306bdeb37271072b5d7e1054286f5fd9d460403
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449851"
---
# <span data-ttu-id="02a8a-101">New-AzureRmApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="02a8a-101">New-AzureRmApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="02a8a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="02a8a-102">SYNOPSIS</span></span>
<span data-ttu-id="02a8a-103">建立適用于應用程式閘道的 Health 探測所使用的健康情況探測回應相符。</span><span class="sxs-lookup"><span data-stu-id="02a8a-103">Creates a health probe response match used by Health Probe for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02a8a-104">句法</span><span class="sxs-lookup"><span data-stu-id="02a8a-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayProbeHealthResponseMatch [-Body <String>]
 [-StatusCode <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="02a8a-105">說明</span><span class="sxs-lookup"><span data-stu-id="02a8a-105">DESCRIPTION</span></span>
<span data-ttu-id="02a8a-106">**AzureRmApplicationGatewayProbeHealthResponseMatch** Cmdlet 會建立適用于應用程式閘道的 health 探測所使用的健康情況探測回應相符。</span><span class="sxs-lookup"><span data-stu-id="02a8a-106">**The Add-AzureRmApplicationGatewayProbeHealthResponseMatch** cmdlet creates a health probe response match used by Health Probe for an application gateway.</span></span>

## <span data-ttu-id="02a8a-107">示例</span><span class="sxs-lookup"><span data-stu-id="02a8a-107">EXAMPLES</span></span>

### <span data-ttu-id="02a8a-108">範例1</span><span class="sxs-lookup"><span data-stu-id="02a8a-108">Example 1</span></span>
```
PS C:\>$responsematch = New-AzureRmApplicationGatewayProbeHealthResponseMatch -Body "helloworld" -StatusCode "200-399","503"
```

<span data-ttu-id="02a8a-109">這個命令會建立一個健康回應相符，您可以將它作為參數傳遞給 ProbeConfig。</span><span class="sxs-lookup"><span data-stu-id="02a8a-109">This command creates a health response match which can be passed to ProbeConfig as a parameter.</span></span>

## <span data-ttu-id="02a8a-110">參數</span><span class="sxs-lookup"><span data-stu-id="02a8a-110">PARAMETERS</span></span>

### <span data-ttu-id="02a8a-111">-Body</span><span class="sxs-lookup"><span data-stu-id="02a8a-111">-Body</span></span>
<span data-ttu-id="02a8a-112">在健康情況回應中必須包含的主體。</span><span class="sxs-lookup"><span data-stu-id="02a8a-112">Body that must be contained in the health response.</span></span>
<span data-ttu-id="02a8a-113">預設值為空白</span><span class="sxs-lookup"><span data-stu-id="02a8a-113">Default value is empty</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02a8a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02a8a-114">-DefaultProfile</span></span>
<span data-ttu-id="02a8a-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="02a8a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02a8a-116">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="02a8a-116">-StatusCode</span></span>
<span data-ttu-id="02a8a-117">允許的健康狀態碼範圍。健康狀態碼的預設範圍是 200-399</span><span class="sxs-lookup"><span data-stu-id="02a8a-117">Allowed ranges of healthy status codes.Default range of healthy status codes is 200 - 399</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02a8a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02a8a-118">CommonParameters</span></span>
<span data-ttu-id="02a8a-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="02a8a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02a8a-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="02a8a-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02a8a-121">輸入</span><span class="sxs-lookup"><span data-stu-id="02a8a-121">INPUTS</span></span>

### <span data-ttu-id="02a8a-122">所有</span><span class="sxs-lookup"><span data-stu-id="02a8a-122">None</span></span>

## <span data-ttu-id="02a8a-123">輸出</span><span class="sxs-lookup"><span data-stu-id="02a8a-123">OUTPUTS</span></span>

### <span data-ttu-id="02a8a-124">PSApplicationGatewayProbeHealthResponseMatch 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="02a8a-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="02a8a-125">筆記</span><span class="sxs-lookup"><span data-stu-id="02a8a-125">NOTES</span></span>

## <span data-ttu-id="02a8a-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="02a8a-126">RELATED LINKS</span></span>
