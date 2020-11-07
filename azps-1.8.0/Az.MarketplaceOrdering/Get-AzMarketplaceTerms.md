---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MarketplaceOrdering.dll-Help.xml
Module Name: Az.MarketplaceOrdering
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplaceordering/get-azmarketplaceterms
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Get-AzMarketplaceTerms.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Get-AzMarketplaceTerms.md
ms.openlocfilehash: 22a9c9b11063dfd9a84e8ecf292af6e9e0f7f97f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93786853"
---
# <span data-ttu-id="fe188-101">Get-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="fe188-101">Get-AzMarketplaceTerms</span></span>

## <span data-ttu-id="fe188-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fe188-102">SYNOPSIS</span></span>
<span data-ttu-id="fe188-103">取得指定發行商識別碼 (Publisher) 的合約條款，提供識別碼 (產品) 與方案 id (名稱) 。</span><span class="sxs-lookup"><span data-stu-id="fe188-103">Get the agreement terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="fe188-104">此命令所傳回的 [詞彙] 物件應該傳遞給 Set-AzMarketplaceTerms，以接受法律條款。</span><span class="sxs-lookup"><span data-stu-id="fe188-104">The terms object which is returned by this command should be passed to Set-AzMarketplaceTerms to accept the legal terms.</span></span>

## <span data-ttu-id="fe188-105">句法</span><span class="sxs-lookup"><span data-stu-id="fe188-105">SYNTAX</span></span>

```
Get-AzMarketplaceTerms -Publisher <String> -Product <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe188-106">說明</span><span class="sxs-lookup"><span data-stu-id="fe188-106">DESCRIPTION</span></span>
<span data-ttu-id="fe188-107">**AzMarketplaceTerms** Cmdlet 會傳回指定發行商識別碼 (publisher) 中的詞彙，提供識別碼 (產品) 與計畫識別碼 (名稱) 元組。</span><span class="sxs-lookup"><span data-stu-id="fe188-107">The **Get-AzMarketplaceTerms** cmdlet returns terms for given publisher id(Publisher), offer id(Product) and plan id(Name) tuple.</span></span>

## <span data-ttu-id="fe188-108">示例</span><span class="sxs-lookup"><span data-stu-id="fe188-108">EXAMPLES</span></span>

### <span data-ttu-id="fe188-109">範例1</span><span class="sxs-lookup"><span data-stu-id="fe188-109">Example 1</span></span>
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

## <span data-ttu-id="fe188-110">參數</span><span class="sxs-lookup"><span data-stu-id="fe188-110">PARAMETERS</span></span>

### <span data-ttu-id="fe188-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe188-111">-DefaultProfile</span></span>
<span data-ttu-id="fe188-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fe188-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe188-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="fe188-113">-Name</span></span>
<span data-ttu-id="fe188-114">規劃要部署之影像的識別碼字串。</span><span class="sxs-lookup"><span data-stu-id="fe188-114">Plan identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="fe188-115">-產品</span><span class="sxs-lookup"><span data-stu-id="fe188-115">-Product</span></span>
<span data-ttu-id="fe188-116">提供要部署之影像的識別碼字串。</span><span class="sxs-lookup"><span data-stu-id="fe188-116">Offer identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="fe188-117">-Publisher</span><span class="sxs-lookup"><span data-stu-id="fe188-117">-Publisher</span></span>
<span data-ttu-id="fe188-118">要部署之影像的發行者識別碼字串。</span><span class="sxs-lookup"><span data-stu-id="fe188-118">Publisher identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="fe188-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe188-119">CommonParameters</span></span>
<span data-ttu-id="fe188-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fe188-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe188-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fe188-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe188-122">輸入</span><span class="sxs-lookup"><span data-stu-id="fe188-122">INPUTS</span></span>

### <span data-ttu-id="fe188-123">所有</span><span class="sxs-lookup"><span data-stu-id="fe188-123">None</span></span>

## <span data-ttu-id="fe188-124">輸出</span><span class="sxs-lookup"><span data-stu-id="fe188-124">OUTPUTS</span></span>

### <span data-ttu-id="fe188-125">PSAgreementTerms 中的 MarketplaceOrdering。</span><span class="sxs-lookup"><span data-stu-id="fe188-125">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="fe188-126">筆記</span><span class="sxs-lookup"><span data-stu-id="fe188-126">NOTES</span></span>

## <span data-ttu-id="fe188-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="fe188-127">RELATED LINKS</span></span>
