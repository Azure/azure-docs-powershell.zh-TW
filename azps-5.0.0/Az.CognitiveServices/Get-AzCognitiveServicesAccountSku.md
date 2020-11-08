---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 386F09F0-2EEC-4B55-825C-F2E88D3B60AA
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountSku.md
ms.openlocfilehash: 3c632e6ffbf26e3aaacb725e9b663ffafbc49ec2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139079"
---
# <span data-ttu-id="69541-101">Get-AzCognitiveServicesAccountSku</span><span class="sxs-lookup"><span data-stu-id="69541-101">Get-AzCognitiveServicesAccountSku</span></span>

## <span data-ttu-id="69541-102">摘要</span><span class="sxs-lookup"><span data-stu-id="69541-102">SYNOPSIS</span></span>
<span data-ttu-id="69541-103">取得帳戶可用的 Sku。</span><span class="sxs-lookup"><span data-stu-id="69541-103">Gets the available SKUs for an account.</span></span>

## <span data-ttu-id="69541-104">句法</span><span class="sxs-lookup"><span data-stu-id="69541-104">SYNTAX</span></span>

```
Get-AzCognitiveServicesAccountSku [-Type <String>] [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69541-105">說明</span><span class="sxs-lookup"><span data-stu-id="69541-105">DESCRIPTION</span></span>
<span data-ttu-id="69541-106">**AzCognitiveServicesAccountSku** Cmdlet 會針對認知服務帳戶取得可用的 sku。</span><span class="sxs-lookup"><span data-stu-id="69541-106">The **Get-AzCognitiveServicesAccountSku** cmdlet gets the available SKUs for a Cognitive Services account.</span></span>
<span data-ttu-id="69541-107">[SKU] 是帳戶的層級方案。</span><span class="sxs-lookup"><span data-stu-id="69541-107">The SKU is the tier plan for an account.</span></span>
<span data-ttu-id="69541-108">它會定義該帳戶的價格、通話限制及工資率。</span><span class="sxs-lookup"><span data-stu-id="69541-108">It defines the price, call limit, and rate for the account.</span></span>
<span data-ttu-id="69541-109">F0 SKU 是免費的層級。</span><span class="sxs-lookup"><span data-stu-id="69541-109">The F0 SKU is a free tier.</span></span>
<span data-ttu-id="69541-110">支付的層級包括 S0、S1、S2 等。</span><span class="sxs-lookup"><span data-stu-id="69541-110">Paid tiers include S0, S1, S2, and so on.</span></span>

## <span data-ttu-id="69541-111">示例</span><span class="sxs-lookup"><span data-stu-id="69541-111">EXAMPLES</span></span>

### <span data-ttu-id="69541-112">範例1</span><span class="sxs-lookup"><span data-stu-id="69541-112">Example 1</span></span>
```powershell
PS C:\> (Get-AzCognitiveServicesAccountSku -Type 'TextAnalytics' -Location "westus").Value | Select-Object -E
xpandProperty Sku;

Name     Tier
----     ----
F0       Free
S0   Standard
```

## <span data-ttu-id="69541-113">參數</span><span class="sxs-lookup"><span data-stu-id="69541-113">PARAMETERS</span></span>

### <span data-ttu-id="69541-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69541-114">-DefaultProfile</span></span>
<span data-ttu-id="69541-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="69541-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="69541-116">-位置</span><span class="sxs-lookup"><span data-stu-id="69541-116">-Location</span></span>
<span data-ttu-id="69541-117">認知服務帳戶位置。</span><span class="sxs-lookup"><span data-stu-id="69541-117">Cognitive Services Account Location.</span></span>

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

### <span data-ttu-id="69541-118">-類型</span><span class="sxs-lookup"><span data-stu-id="69541-118">-Type</span></span>
<span data-ttu-id="69541-119">認知服務帳戶類型。</span><span class="sxs-lookup"><span data-stu-id="69541-119">Cognitive Services Account Type.</span></span>

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

### <span data-ttu-id="69541-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69541-120">CommonParameters</span></span>
<span data-ttu-id="69541-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="69541-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69541-122">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="69541-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69541-123">輸入</span><span class="sxs-lookup"><span data-stu-id="69541-123">INPUTS</span></span>

### <span data-ttu-id="69541-124">System.object</span><span class="sxs-lookup"><span data-stu-id="69541-124">System.String</span></span>

## <span data-ttu-id="69541-125">輸出</span><span class="sxs-lookup"><span data-stu-id="69541-125">OUTPUTS</span></span>

### <span data-ttu-id="69541-126">ResourceSku 中的 CognitiveServices。</span><span class="sxs-lookup"><span data-stu-id="69541-126">Microsoft.Azure.Management.CognitiveServices.Models.ResourceSku</span></span>

## <span data-ttu-id="69541-127">筆記</span><span class="sxs-lookup"><span data-stu-id="69541-127">NOTES</span></span>

## <span data-ttu-id="69541-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="69541-128">RELATED LINKS</span></span>
