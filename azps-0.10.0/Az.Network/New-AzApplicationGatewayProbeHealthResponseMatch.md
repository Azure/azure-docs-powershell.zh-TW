---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayprobehealthresponsematch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayProbeHealthResponseMatch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayProbeHealthResponseMatch.md
ms.openlocfilehash: 41693da553178bdd45d19da498a5774ef8d2fa60
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794305"
---
# <span data-ttu-id="3840e-101">New-AzApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="3840e-101">New-AzApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="3840e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3840e-102">SYNOPSIS</span></span>
<span data-ttu-id="3840e-103">建立適用于應用程式閘道的 Health 探測所使用的健康情況探測回應相符。</span><span class="sxs-lookup"><span data-stu-id="3840e-103">Creates a health probe response match used by Health Probe for an application gateway.</span></span>

## <span data-ttu-id="3840e-104">句法</span><span class="sxs-lookup"><span data-stu-id="3840e-104">SYNTAX</span></span>

```
New-AzApplicationGatewayProbeHealthResponseMatch [-Body <String>]
 [-StatusCode <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3840e-105">說明</span><span class="sxs-lookup"><span data-stu-id="3840e-105">DESCRIPTION</span></span>
<span data-ttu-id="3840e-106">**AzApplicationGatewayProbeHealthResponseMatch** Cmdlet 會建立適用于應用程式閘道的 health 探測所使用的健康情況探測回應相符。</span><span class="sxs-lookup"><span data-stu-id="3840e-106">**The Add-AzApplicationGatewayProbeHealthResponseMatch** cmdlet creates a health probe response match used by Health Probe for an application gateway.</span></span>

## <span data-ttu-id="3840e-107">示例</span><span class="sxs-lookup"><span data-stu-id="3840e-107">EXAMPLES</span></span>

### <span data-ttu-id="3840e-108">範例1</span><span class="sxs-lookup"><span data-stu-id="3840e-108">Example 1</span></span>
```
PS C:\>$responsematch = New-AzApplicationGatewayProbeHealthResponseMatch -Body "helloworld" -StatusCode "200-399","503"
```

<span data-ttu-id="3840e-109">這個命令會建立一個健康回應相符，您可以將它作為參數傳遞給 ProbeConfig。</span><span class="sxs-lookup"><span data-stu-id="3840e-109">This command creates a health response match which can be passed to ProbeConfig as a parameter.</span></span>

## <span data-ttu-id="3840e-110">參數</span><span class="sxs-lookup"><span data-stu-id="3840e-110">PARAMETERS</span></span>

### <span data-ttu-id="3840e-111">-Body</span><span class="sxs-lookup"><span data-stu-id="3840e-111">-Body</span></span>
<span data-ttu-id="3840e-112">在健康情況回應中必須包含的主體。</span><span class="sxs-lookup"><span data-stu-id="3840e-112">Body that must be contained in the health response.</span></span>
<span data-ttu-id="3840e-113">預設值為空白</span><span class="sxs-lookup"><span data-stu-id="3840e-113">Default value is empty</span></span>

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

### <span data-ttu-id="3840e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3840e-114">-DefaultProfile</span></span>
<span data-ttu-id="3840e-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3840e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3840e-116">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="3840e-116">-StatusCode</span></span>
<span data-ttu-id="3840e-117">允許的健康狀態碼範圍。健康狀態碼的預設範圍是 200-399</span><span class="sxs-lookup"><span data-stu-id="3840e-117">Allowed ranges of healthy status codes.Default range of healthy status codes is 200 - 399</span></span>

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

### <span data-ttu-id="3840e-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3840e-118">CommonParameters</span></span>
<span data-ttu-id="3840e-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3840e-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3840e-120">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3840e-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3840e-121">輸入</span><span class="sxs-lookup"><span data-stu-id="3840e-121">INPUTS</span></span>

### <span data-ttu-id="3840e-122">所有</span><span class="sxs-lookup"><span data-stu-id="3840e-122">None</span></span>

## <span data-ttu-id="3840e-123">輸出</span><span class="sxs-lookup"><span data-stu-id="3840e-123">OUTPUTS</span></span>

### <span data-ttu-id="3840e-124">PSApplicationGatewayProbeHealthResponseMatch 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="3840e-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="3840e-125">筆記</span><span class="sxs-lookup"><span data-stu-id="3840e-125">NOTES</span></span>

## <span data-ttu-id="3840e-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="3840e-126">RELATED LINKS</span></span>

