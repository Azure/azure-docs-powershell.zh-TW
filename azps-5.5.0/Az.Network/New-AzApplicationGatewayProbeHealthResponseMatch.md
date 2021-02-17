---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayprobehealthresponsematch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayProbeHealthResponseMatch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayProbeHealthResponseMatch.md
ms.openlocfilehash: edc0309b5e1a0c8b17d400e965074d38ca02bb80
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100140406"
---
# <span data-ttu-id="d2ff7-101">New-AzApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="d2ff7-101">New-AzApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="d2ff7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d2ff7-102">SYNOPSIS</span></span>
<span data-ttu-id="d2ff7-103">建立適用于應用程式閘道的 Health 探測所使用的健康情況探測回應相符。</span><span class="sxs-lookup"><span data-stu-id="d2ff7-103">Creates a health probe response match used by Health Probe for an application gateway.</span></span>

## <span data-ttu-id="d2ff7-104">句法</span><span class="sxs-lookup"><span data-stu-id="d2ff7-104">SYNTAX</span></span>

```
New-AzApplicationGatewayProbeHealthResponseMatch [-Body <String>] [-StatusCode <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2ff7-105">說明</span><span class="sxs-lookup"><span data-stu-id="d2ff7-105">DESCRIPTION</span></span>
<span data-ttu-id="d2ff7-106">**AzApplicationGatewayProbeHealthResponseMatch** Cmdlet 會建立適用于應用程式閘道的 health 探測所使用的健康情況探測回應相符。</span><span class="sxs-lookup"><span data-stu-id="d2ff7-106">**The Add-AzApplicationGatewayProbeHealthResponseMatch** cmdlet creates a health probe response match used by Health Probe for an application gateway.</span></span>

## <span data-ttu-id="d2ff7-107">示例</span><span class="sxs-lookup"><span data-stu-id="d2ff7-107">EXAMPLES</span></span>

### <span data-ttu-id="d2ff7-108">範例1</span><span class="sxs-lookup"><span data-stu-id="d2ff7-108">Example 1</span></span>
```
PS C:\>$responsematch = New-AzApplicationGatewayProbeHealthResponseMatch -Body "helloworld" -StatusCode "200-399","503"
```

<span data-ttu-id="d2ff7-109">這個命令會建立一個健康回應相符，您可以將它作為參數傳遞給 ProbeConfig。</span><span class="sxs-lookup"><span data-stu-id="d2ff7-109">This command creates a health response match which can be passed to ProbeConfig as a parameter.</span></span>

## <span data-ttu-id="d2ff7-110">參數</span><span class="sxs-lookup"><span data-stu-id="d2ff7-110">PARAMETERS</span></span>

### <span data-ttu-id="d2ff7-111">-Body</span><span class="sxs-lookup"><span data-stu-id="d2ff7-111">-Body</span></span>
<span data-ttu-id="d2ff7-112">在健康情況回應中必須包含的主體。</span><span class="sxs-lookup"><span data-stu-id="d2ff7-112">Body that must be contained in the health response.</span></span>
<span data-ttu-id="d2ff7-113">預設值為空白</span><span class="sxs-lookup"><span data-stu-id="d2ff7-113">Default value is empty</span></span>

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

### <span data-ttu-id="d2ff7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2ff7-114">-DefaultProfile</span></span>
<span data-ttu-id="d2ff7-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d2ff7-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2ff7-116">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="d2ff7-116">-StatusCode</span></span>
<span data-ttu-id="d2ff7-117">允許的健康狀態碼範圍。健康狀態碼的預設範圍是 200-399</span><span class="sxs-lookup"><span data-stu-id="d2ff7-117">Allowed ranges of healthy status codes.Default range of healthy status codes is 200 - 399</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2ff7-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2ff7-118">CommonParameters</span></span>
<span data-ttu-id="d2ff7-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d2ff7-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2ff7-120">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d2ff7-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2ff7-121">輸入</span><span class="sxs-lookup"><span data-stu-id="d2ff7-121">INPUTS</span></span>

### <span data-ttu-id="d2ff7-122">所有</span><span class="sxs-lookup"><span data-stu-id="d2ff7-122">None</span></span>

## <span data-ttu-id="d2ff7-123">輸出</span><span class="sxs-lookup"><span data-stu-id="d2ff7-123">OUTPUTS</span></span>

### <span data-ttu-id="d2ff7-124">PSApplicationGatewayProbeHealthResponseMatch 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="d2ff7-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="d2ff7-125">筆記</span><span class="sxs-lookup"><span data-stu-id="d2ff7-125">NOTES</span></span>

## <span data-ttu-id="d2ff7-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="d2ff7-126">RELATED LINKS</span></span>
