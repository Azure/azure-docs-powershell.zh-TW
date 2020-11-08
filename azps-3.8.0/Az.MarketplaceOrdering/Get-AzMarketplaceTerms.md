---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MarketplaceOrdering.dll-Help.xml
Module Name: Az.MarketplaceOrdering
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplaceordering/get-azmarketplaceterms
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Get-AzMarketplaceTerms.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Get-AzMarketplaceTerms.md
ms.openlocfilehash: b729eb0ca1c0cc3b051600b59f260ebfb16d6b6e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93965995"
---
# <span data-ttu-id="15fea-101">Get-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="15fea-101">Get-AzMarketplaceTerms</span></span>

## <span data-ttu-id="15fea-102">摘要</span><span class="sxs-lookup"><span data-stu-id="15fea-102">SYNOPSIS</span></span>
<span data-ttu-id="15fea-103">取得指定發行商識別碼 (Publisher) 的合約條款，提供識別碼 (產品) 與方案 id (名稱) 。</span><span class="sxs-lookup"><span data-stu-id="15fea-103">Get the agreement terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="15fea-104">此命令所傳回的 [詞彙] 物件應該傳遞給 Set-AzMarketplaceTerms，以接受法律條款。</span><span class="sxs-lookup"><span data-stu-id="15fea-104">The terms object which is returned by this command should be passed to Set-AzMarketplaceTerms to accept the legal terms.</span></span>

## <span data-ttu-id="15fea-105">句法</span><span class="sxs-lookup"><span data-stu-id="15fea-105">SYNTAX</span></span>

```
Get-AzMarketplaceTerms -Publisher <String> -Product <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="15fea-106">說明</span><span class="sxs-lookup"><span data-stu-id="15fea-106">DESCRIPTION</span></span>
<span data-ttu-id="15fea-107">**AzMarketplaceTerms** Cmdlet 會傳回指定發行商識別碼 (publisher) 中的詞彙，提供識別碼 (產品) 與計畫識別碼 (名稱) 元組。</span><span class="sxs-lookup"><span data-stu-id="15fea-107">The **Get-AzMarketplaceTerms** cmdlet returns terms for given publisher id(Publisher), offer id(Product) and plan id(Name) tuple.</span></span>

## <span data-ttu-id="15fea-108">示例</span><span class="sxs-lookup"><span data-stu-id="15fea-108">EXAMPLES</span></span>

### <span data-ttu-id="15fea-109">範例1</span><span class="sxs-lookup"><span data-stu-id="15fea-109">Example 1</span></span>
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

## <span data-ttu-id="15fea-110">參數</span><span class="sxs-lookup"><span data-stu-id="15fea-110">PARAMETERS</span></span>

### <span data-ttu-id="15fea-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15fea-111">-DefaultProfile</span></span>
<span data-ttu-id="15fea-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="15fea-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15fea-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="15fea-113">-Name</span></span>
<span data-ttu-id="15fea-114">規劃要部署之影像的識別碼字串。</span><span class="sxs-lookup"><span data-stu-id="15fea-114">Plan identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="15fea-115">-產品</span><span class="sxs-lookup"><span data-stu-id="15fea-115">-Product</span></span>
<span data-ttu-id="15fea-116">提供要部署之影像的識別碼字串。</span><span class="sxs-lookup"><span data-stu-id="15fea-116">Offer identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="15fea-117">-Publisher</span><span class="sxs-lookup"><span data-stu-id="15fea-117">-Publisher</span></span>
<span data-ttu-id="15fea-118">要部署之影像的發行者識別碼字串。</span><span class="sxs-lookup"><span data-stu-id="15fea-118">Publisher identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="15fea-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15fea-119">CommonParameters</span></span>
<span data-ttu-id="15fea-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="15fea-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15fea-121">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="15fea-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15fea-122">輸入</span><span class="sxs-lookup"><span data-stu-id="15fea-122">INPUTS</span></span>

### <span data-ttu-id="15fea-123">所有</span><span class="sxs-lookup"><span data-stu-id="15fea-123">None</span></span>

## <span data-ttu-id="15fea-124">輸出</span><span class="sxs-lookup"><span data-stu-id="15fea-124">OUTPUTS</span></span>

### <span data-ttu-id="15fea-125">PSAgreementTerms 中的 MarketplaceOrdering。</span><span class="sxs-lookup"><span data-stu-id="15fea-125">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="15fea-126">筆記</span><span class="sxs-lookup"><span data-stu-id="15fea-126">NOTES</span></span>

## <span data-ttu-id="15fea-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="15fea-127">RELATED LINKS</span></span>