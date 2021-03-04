---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayprobehealthresponsematch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayProbeHealthResponseMatch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayProbeHealthResponseMatch.md
ms.openlocfilehash: 04da18bcd50fa547f1a59142682c93b4e3e5ab62
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907618"
---
# <span data-ttu-id="702b5-101">New-AzApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="702b5-101">New-AzApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="702b5-102">簡介</span><span class="sxs-lookup"><span data-stu-id="702b5-102">SYNOPSIS</span></span>
<span data-ttu-id="702b5-103">為應用程式閘道建立 Health 進位回應比對。</span><span class="sxs-lookup"><span data-stu-id="702b5-103">Creates a health probe response match used by Health Probe for an application gateway.</span></span>

## <span data-ttu-id="702b5-104">語法</span><span class="sxs-lookup"><span data-stu-id="702b5-104">SYNTAX</span></span>

```
New-AzApplicationGatewayProbeHealthResponseMatch [-Body <String>] [-StatusCode <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="702b5-105">描述</span><span class="sxs-lookup"><span data-stu-id="702b5-105">DESCRIPTION</span></span>
<span data-ttu-id="702b5-106">**Add-AzApplicationGatewayProbeHealthResponseMatch** Cmdlet 會針對應用程式閘道建立 Health 因應措施回應比對。</span><span class="sxs-lookup"><span data-stu-id="702b5-106">**The Add-AzApplicationGatewayProbeHealthResponseMatch** cmdlet creates a health probe response match used by Health Probe for an application gateway.</span></span>

## <span data-ttu-id="702b5-107">例子</span><span class="sxs-lookup"><span data-stu-id="702b5-107">EXAMPLES</span></span>

### <span data-ttu-id="702b5-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="702b5-108">Example 1</span></span>
```
PS C:\>$responsematch = New-AzApplicationGatewayProbeHealthResponseMatch -Body "helloworld" -StatusCode "200-399","503"
```

<span data-ttu-id="702b5-109">此命令會建立一個健康狀態回應比對，您可以將它以參數傳遞至ConfigConfig。</span><span class="sxs-lookup"><span data-stu-id="702b5-109">This command creates a health response match which can be passed to ProbeConfig as a parameter.</span></span>

## <span data-ttu-id="702b5-110">參數</span><span class="sxs-lookup"><span data-stu-id="702b5-110">PARAMETERS</span></span>

### <span data-ttu-id="702b5-111">-Body</span><span class="sxs-lookup"><span data-stu-id="702b5-111">-Body</span></span>
<span data-ttu-id="702b5-112">必須包含在健康回應中的內體。</span><span class="sxs-lookup"><span data-stu-id="702b5-112">Body that must be contained in the health response.</span></span>
<span data-ttu-id="702b5-113">預設值為空白</span><span class="sxs-lookup"><span data-stu-id="702b5-113">Default value is empty</span></span>

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

### <span data-ttu-id="702b5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="702b5-114">-DefaultProfile</span></span>
<span data-ttu-id="702b5-115">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="702b5-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="702b5-116">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="702b5-116">-StatusCode</span></span>
<span data-ttu-id="702b5-117">允許的健全狀態碼範圍。正常狀態碼的預設範圍為 200 - 399</span><span class="sxs-lookup"><span data-stu-id="702b5-117">Allowed ranges of healthy status codes.Default range of healthy status codes is 200 - 399</span></span>

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

### <span data-ttu-id="702b5-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="702b5-118">CommonParameters</span></span>
<span data-ttu-id="702b5-119">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="702b5-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="702b5-120">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="702b5-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="702b5-121">輸入</span><span class="sxs-lookup"><span data-stu-id="702b5-121">INPUTS</span></span>

### <span data-ttu-id="702b5-122">沒有</span><span class="sxs-lookup"><span data-stu-id="702b5-122">None</span></span>

## <span data-ttu-id="702b5-123">輸出</span><span class="sxs-lookup"><span data-stu-id="702b5-123">OUTPUTS</span></span>

### <span data-ttu-id="702b5-124">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="702b5-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="702b5-125">筆記</span><span class="sxs-lookup"><span data-stu-id="702b5-125">NOTES</span></span>

## <span data-ttu-id="702b5-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="702b5-126">RELATED LINKS</span></span>
