---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MarketplaceOrdering.dll-Help.xml
Module Name: Az.MarketplaceOrdering
online version: https://docs.microsoft.com/powershell/module/az.marketplaceordering/get-azmarketplaceterms
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Get-AzMarketplaceTerms.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Get-AzMarketplaceTerms.md
ms.openlocfilehash: 9878bdaa508d2cc229f494dcd53467f9c7d62ed1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905361"
---
# <span data-ttu-id="6fb65-101">Get-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="6fb65-101">Get-AzMarketplaceTerms</span></span>

## <span data-ttu-id="6fb65-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6fb65-102">SYNOPSIS</span></span>
<span data-ttu-id="6fb65-103">取得 Publisher (發行者識別碼) 、提供識別碼 (產品) 以及方案 (名稱) 。</span><span class="sxs-lookup"><span data-stu-id="6fb65-103">Get the agreement terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="6fb65-104">此命令所傳回的字詞物件應傳遞至Set-AzMarketplaceTerms接受法律條款。</span><span class="sxs-lookup"><span data-stu-id="6fb65-104">The terms object which is returned by this command should be passed to Set-AzMarketplaceTerms to accept the legal terms.</span></span>

## <span data-ttu-id="6fb65-105">語法</span><span class="sxs-lookup"><span data-stu-id="6fb65-105">SYNTAX</span></span>

```
Get-AzMarketplaceTerms -Publisher <String> -Product <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6fb65-106">描述</span><span class="sxs-lookup"><span data-stu-id="6fb65-106">DESCRIPTION</span></span>
<span data-ttu-id="6fb65-107">**Get-AzMarketplaceTerms** Cmdlet 會針對指定發行者識別碼 (Publisher) ，提供識別碼 (產品) 和方案識別碼 (Name) Tuple。</span><span class="sxs-lookup"><span data-stu-id="6fb65-107">The **Get-AzMarketplaceTerms** cmdlet returns terms for given publisher id(Publisher), offer id(Product) and plan id(Name) tuple.</span></span>

## <span data-ttu-id="6fb65-108">例子</span><span class="sxs-lookup"><span data-stu-id="6fb65-108">EXAMPLES</span></span>

### <span data-ttu-id="6fb65-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="6fb65-109">Example 1</span></span>
```
PS C:\> Get-AzMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016"
Publisher         : microsoft-ads
Product           : windows-data-science-vm
Plan              : windows2016
LicenseTextLink   : <LicenseTextLink>
PrivacyPolicyLink : <PrivacyPolicyLink>
Signature         : <Signature>
Accepted          : True
RetrieveDatetime  : <RetrieveDatetime>
```

## <span data-ttu-id="6fb65-110">參數</span><span class="sxs-lookup"><span data-stu-id="6fb65-110">PARAMETERS</span></span>

### <span data-ttu-id="6fb65-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fb65-111">-DefaultProfile</span></span>
<span data-ttu-id="6fb65-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="6fb65-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6fb65-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="6fb65-113">-Name</span></span>
<span data-ttu-id="6fb65-114">部署的圖像之計畫識別碼字串。</span><span class="sxs-lookup"><span data-stu-id="6fb65-114">Plan identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="6fb65-115">-產品</span><span class="sxs-lookup"><span data-stu-id="6fb65-115">-Product</span></span>
<span data-ttu-id="6fb65-116">提供部署之影像的識別碼字串。</span><span class="sxs-lookup"><span data-stu-id="6fb65-116">Offer identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="6fb65-117">-Publisher</span><span class="sxs-lookup"><span data-stu-id="6fb65-117">-Publisher</span></span>
<span data-ttu-id="6fb65-118">部署之圖像的 Publisher 識別碼字串。</span><span class="sxs-lookup"><span data-stu-id="6fb65-118">Publisher identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="6fb65-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fb65-119">CommonParameters</span></span>
<span data-ttu-id="6fb65-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6fb65-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fb65-121">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="6fb65-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fb65-122">輸入</span><span class="sxs-lookup"><span data-stu-id="6fb65-122">INPUTS</span></span>

### <span data-ttu-id="6fb65-123">沒有</span><span class="sxs-lookup"><span data-stu-id="6fb65-123">None</span></span>

## <span data-ttu-id="6fb65-124">輸出</span><span class="sxs-lookup"><span data-stu-id="6fb65-124">OUTPUTS</span></span>

### <span data-ttu-id="6fb65-125">Microsoft.Azure.Commands.MarketplaceOrdering.models.PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="6fb65-125">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="6fb65-126">筆記</span><span class="sxs-lookup"><span data-stu-id="6fb65-126">NOTES</span></span>

## <span data-ttu-id="6fb65-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="6fb65-127">RELATED LINKS</span></span>
