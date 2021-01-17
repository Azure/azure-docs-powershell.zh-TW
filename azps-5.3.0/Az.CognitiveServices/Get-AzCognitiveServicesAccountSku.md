---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 386F09F0-2EEC-4B55-825C-F2E88D3B60AA
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountSku.md
ms.openlocfilehash: 3c632e6ffbf26e3aaacb725e9b663ffafbc49ec2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98446571"
---
# <span data-ttu-id="ba795-101">Get-AzCognitiveServicesAccountSku</span><span class="sxs-lookup"><span data-stu-id="ba795-101">Get-AzCognitiveServicesAccountSku</span></span>

## <span data-ttu-id="ba795-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ba795-102">SYNOPSIS</span></span>
<span data-ttu-id="ba795-103">取得帳戶可用的 Sku。</span><span class="sxs-lookup"><span data-stu-id="ba795-103">Gets the available SKUs for an account.</span></span>

## <span data-ttu-id="ba795-104">句法</span><span class="sxs-lookup"><span data-stu-id="ba795-104">SYNTAX</span></span>

```
Get-AzCognitiveServicesAccountSku [-Type <String>] [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba795-105">說明</span><span class="sxs-lookup"><span data-stu-id="ba795-105">DESCRIPTION</span></span>
<span data-ttu-id="ba795-106">**AzCognitiveServicesAccountSku** Cmdlet 會針對認知服務帳戶取得可用的 sku。</span><span class="sxs-lookup"><span data-stu-id="ba795-106">The **Get-AzCognitiveServicesAccountSku** cmdlet gets the available SKUs for a Cognitive Services account.</span></span>
<span data-ttu-id="ba795-107">[SKU] 是帳戶的層級方案。</span><span class="sxs-lookup"><span data-stu-id="ba795-107">The SKU is the tier plan for an account.</span></span>
<span data-ttu-id="ba795-108">它會定義該帳戶的價格、通話限制及工資率。</span><span class="sxs-lookup"><span data-stu-id="ba795-108">It defines the price, call limit, and rate for the account.</span></span>
<span data-ttu-id="ba795-109">F0 SKU 是免費的層級。</span><span class="sxs-lookup"><span data-stu-id="ba795-109">The F0 SKU is a free tier.</span></span>
<span data-ttu-id="ba795-110">支付的層級包括 S0、S1、S2 等。</span><span class="sxs-lookup"><span data-stu-id="ba795-110">Paid tiers include S0, S1, S2, and so on.</span></span>

## <span data-ttu-id="ba795-111">示例</span><span class="sxs-lookup"><span data-stu-id="ba795-111">EXAMPLES</span></span>

### <span data-ttu-id="ba795-112">範例1</span><span class="sxs-lookup"><span data-stu-id="ba795-112">Example 1</span></span>
```powershell
PS C:\> (Get-AzCognitiveServicesAccountSku -Type 'TextAnalytics' -Location "westus").Value | Select-Object -E
xpandProperty Sku;

Name     Tier
----     ----
F0       Free
S0   Standard
```

## <span data-ttu-id="ba795-113">參數</span><span class="sxs-lookup"><span data-stu-id="ba795-113">PARAMETERS</span></span>

### <span data-ttu-id="ba795-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba795-114">-DefaultProfile</span></span>
<span data-ttu-id="ba795-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="ba795-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ba795-116">-位置</span><span class="sxs-lookup"><span data-stu-id="ba795-116">-Location</span></span>
<span data-ttu-id="ba795-117">認知服務帳戶位置。</span><span class="sxs-lookup"><span data-stu-id="ba795-117">Cognitive Services Account Location.</span></span>

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

### <span data-ttu-id="ba795-118">-類型</span><span class="sxs-lookup"><span data-stu-id="ba795-118">-Type</span></span>
<span data-ttu-id="ba795-119">認知服務帳戶類型。</span><span class="sxs-lookup"><span data-stu-id="ba795-119">Cognitive Services Account Type.</span></span>

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

### <span data-ttu-id="ba795-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba795-120">CommonParameters</span></span>
<span data-ttu-id="ba795-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ba795-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba795-122">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ba795-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba795-123">輸入</span><span class="sxs-lookup"><span data-stu-id="ba795-123">INPUTS</span></span>

### <span data-ttu-id="ba795-124">System.object</span><span class="sxs-lookup"><span data-stu-id="ba795-124">System.String</span></span>

## <span data-ttu-id="ba795-125">輸出</span><span class="sxs-lookup"><span data-stu-id="ba795-125">OUTPUTS</span></span>

### <span data-ttu-id="ba795-126">ResourceSku 中的 CognitiveServices。</span><span class="sxs-lookup"><span data-stu-id="ba795-126">Microsoft.Azure.Management.CognitiveServices.Models.ResourceSku</span></span>

## <span data-ttu-id="ba795-127">筆記</span><span class="sxs-lookup"><span data-stu-id="ba795-127">NOTES</span></span>

## <span data-ttu-id="ba795-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="ba795-128">RELATED LINKS</span></span>
