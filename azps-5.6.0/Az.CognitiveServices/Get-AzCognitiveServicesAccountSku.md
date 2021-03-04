---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 386F09F0-2EEC-4B55-825C-F2E88D3B60AA
online version: https://docs.microsoft.com/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountSku.md
ms.openlocfilehash: eb9865d69d51fffc7488379bada256a812503a24
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909229"
---
# <span data-ttu-id="77415-101">Get-AzCognitiveServicesAccountSku</span><span class="sxs-lookup"><span data-stu-id="77415-101">Get-AzCognitiveServicesAccountSku</span></span>

## <span data-ttu-id="77415-102">簡介</span><span class="sxs-lookup"><span data-stu-id="77415-102">SYNOPSIS</span></span>
<span data-ttu-id="77415-103">獲得帳戶的可用 SK。</span><span class="sxs-lookup"><span data-stu-id="77415-103">Gets the available SKUs for an account.</span></span>

## <span data-ttu-id="77415-104">語法</span><span class="sxs-lookup"><span data-stu-id="77415-104">SYNTAX</span></span>

```
Get-AzCognitiveServicesAccountSku [-Type <String>] [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77415-105">描述</span><span class="sxs-lookup"><span data-stu-id="77415-105">DESCRIPTION</span></span>
<span data-ttu-id="77415-106">**Get-AzCognitiveServicesAccountSku** Cmdlet 會取得認知服務帳戶可用的 SKU。</span><span class="sxs-lookup"><span data-stu-id="77415-106">The **Get-AzCognitiveServicesAccountSku** cmdlet gets the available SKUs for a Cognitive Services account.</span></span>
<span data-ttu-id="77415-107">SKU 是帳戶的層級方案。</span><span class="sxs-lookup"><span data-stu-id="77415-107">The SKU is the tier plan for an account.</span></span>
<span data-ttu-id="77415-108">它會定義帳戶的價格、通話限制和費率。</span><span class="sxs-lookup"><span data-stu-id="77415-108">It defines the price, call limit, and rate for the account.</span></span>
<span data-ttu-id="77415-109">F0 SKU 是免費層級。</span><span class="sxs-lookup"><span data-stu-id="77415-109">The F0 SKU is a free tier.</span></span>
<span data-ttu-id="77415-110">付費層級包括 S0、S1、S2 等。</span><span class="sxs-lookup"><span data-stu-id="77415-110">Paid tiers include S0, S1, S2, and so on.</span></span>

## <span data-ttu-id="77415-111">例子</span><span class="sxs-lookup"><span data-stu-id="77415-111">EXAMPLES</span></span>

### <span data-ttu-id="77415-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="77415-112">Example 1</span></span>
```powershell
PS C:\> (Get-AzCognitiveServicesAccountSku -Type 'TextAnalytics' -Location "westus").Value | Select-Object -E
xpandProperty Sku;

Name     Tier
----     ----
F0       Free
S0   Standard
```

## <span data-ttu-id="77415-113">參數</span><span class="sxs-lookup"><span data-stu-id="77415-113">PARAMETERS</span></span>

### <span data-ttu-id="77415-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77415-114">-DefaultProfile</span></span>
<span data-ttu-id="77415-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="77415-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="77415-116">-位置</span><span class="sxs-lookup"><span data-stu-id="77415-116">-Location</span></span>
<span data-ttu-id="77415-117">認知服務帳戶位置。</span><span class="sxs-lookup"><span data-stu-id="77415-117">Cognitive Services Account Location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77415-118">-類型</span><span class="sxs-lookup"><span data-stu-id="77415-118">-Type</span></span>
<span data-ttu-id="77415-119">認知服務帳戶類型。</span><span class="sxs-lookup"><span data-stu-id="77415-119">Cognitive Services Account Type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountType, AccountType, Kind

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77415-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77415-120">CommonParameters</span></span>
<span data-ttu-id="77415-121">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="77415-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77415-122">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="77415-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77415-123">輸入</span><span class="sxs-lookup"><span data-stu-id="77415-123">INPUTS</span></span>

### <span data-ttu-id="77415-124">System.String</span><span class="sxs-lookup"><span data-stu-id="77415-124">System.String</span></span>

## <span data-ttu-id="77415-125">輸出</span><span class="sxs-lookup"><span data-stu-id="77415-125">OUTPUTS</span></span>

### <span data-ttu-id="77415-126">Microsoft.Azure.management.CognitiveServices.models.ResourceSku</span><span class="sxs-lookup"><span data-stu-id="77415-126">Microsoft.Azure.Management.CognitiveServices.Models.ResourceSku</span></span>

## <span data-ttu-id="77415-127">筆記</span><span class="sxs-lookup"><span data-stu-id="77415-127">NOTES</span></span>

## <span data-ttu-id="77415-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="77415-128">RELATED LINKS</span></span>
