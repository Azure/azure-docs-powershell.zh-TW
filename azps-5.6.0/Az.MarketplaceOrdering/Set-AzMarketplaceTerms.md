---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MarketplaceOrdering.dll-Help.xml
Module Name: Az.MarketplaceOrdering
online version: https://docs.microsoft.com/powershell/module/az.marketplaceordering/set-azmarketplaceterms
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Set-AzMarketplaceTerms.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Set-AzMarketplaceTerms.md
ms.openlocfilehash: b4098481db78bf045abad04aee4e2e5076f71ce1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902005"
---
# <span data-ttu-id="a01fb-101">Set-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="a01fb-101">Set-AzMarketplaceTerms</span></span>

## <span data-ttu-id="a01fb-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a01fb-102">SYNOPSIS</span></span>
<span data-ttu-id="a01fb-103">接受或拒絕 Publisher (發行者識別碼) 、提供識別碼 (產品) 以及方案 (名稱) 。</span><span class="sxs-lookup"><span data-stu-id="a01fb-103">Accept or reject terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="a01fb-104">請使用Get-AzMarketplaceTerms以取得合約條款。</span><span class="sxs-lookup"><span data-stu-id="a01fb-104">Please use Get-AzMarketplaceTerms to get the agreement terms.</span></span>

## <span data-ttu-id="a01fb-105">語法</span><span class="sxs-lookup"><span data-stu-id="a01fb-105">SYNTAX</span></span>

### <span data-ttu-id="a01fb-106">AgreementAcceptParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a01fb-106">AgreementAcceptParameterSet (Default)</span></span>
```
Set-AzMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Accept]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a01fb-107">AgreementRejectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a01fb-107">AgreementRejectParameterSet</span></span>
```
Set-AzMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Reject]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a01fb-108">InputObjectAcceptParameterSet</span><span class="sxs-lookup"><span data-stu-id="a01fb-108">InputObjectAcceptParameterSet</span></span>
```
Set-AzMarketplaceTerms [-Accept] [-InputObject] <PSAgreementTerms> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a01fb-109">InputObjectRejectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a01fb-109">InputObjectRejectParameterSet</span></span>
```
Set-AzMarketplaceTerms [-Reject] [-InputObject] <PSAgreementTerms> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a01fb-110">描述</span><span class="sxs-lookup"><span data-stu-id="a01fb-110">DESCRIPTION</span></span>
<span data-ttu-id="a01fb-111">**Set-AzMarketplaceTerms** Cmdlet 會針對指定發行者識別碼 (Publisher) ，提供識別碼 (Product) 和方案識別碼 (Name) Tuple 來) 字詞物件。</span><span class="sxs-lookup"><span data-stu-id="a01fb-111">The **Set-AzMarketplaceTerms** cmdlet saves the terms object for given publisher id(Publisher), offer id(Product) and plan id(Name) tuple.</span></span>

## <span data-ttu-id="a01fb-112">例子</span><span class="sxs-lookup"><span data-stu-id="a01fb-112">EXAMPLES</span></span>

### <span data-ttu-id="a01fb-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="a01fb-113">Example 1</span></span>
<span data-ttu-id="a01fb-114">取得服務商場發行者協定</span><span class="sxs-lookup"><span data-stu-id="a01fb-114">Get the marketplace publisher agreement</span></span>


```
PS C:\> Get-AzMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" | Set-AzMarketplaceTerms -Accept
```

### <span data-ttu-id="a01fb-115">範例 2</span><span class="sxs-lookup"><span data-stu-id="a01fb-115">Example 2</span></span>
<span data-ttu-id="a01fb-116">將發行者同意設定為 'Accept'。</span><span class="sxs-lookup"><span data-stu-id="a01fb-116">Set the publisher agreement to 'Accept'.</span></span> <span data-ttu-id="a01fb-117">從 "Get-AzMarketplaceTerms" Cmdlet 取得 'Terms' 參數的值</span><span class="sxs-lookup"><span data-stu-id="a01fb-117">Get the value for the 'Terms' parameter from the 'Get-AzMarketplaceTerms' cmdlet</span></span>


```
PS C:\> Set-AzMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" -Terms $agreementTerms -Accept
```

## <span data-ttu-id="a01fb-118">參數</span><span class="sxs-lookup"><span data-stu-id="a01fb-118">PARAMETERS</span></span>

### <span data-ttu-id="a01fb-119">-接受</span><span class="sxs-lookup"><span data-stu-id="a01fb-119">-Accept</span></span>
<span data-ttu-id="a01fb-120">請傳遞此內容以接受法律條款。</span><span class="sxs-lookup"><span data-stu-id="a01fb-120">Pass this to accept the legal terms.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AgreementAcceptParameterSet, InputObjectAcceptParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a01fb-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a01fb-121">-DefaultProfile</span></span>
<span data-ttu-id="a01fb-122">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a01fb-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a01fb-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a01fb-123">-InputObject</span></span>
<span data-ttu-id="a01fb-124">在 Cmdlet 中Get-AzMarketplaceTerms字詞物件。</span><span class="sxs-lookup"><span data-stu-id="a01fb-124">Terms object returned in Get-AzMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="a01fb-125">如果接受參數為 True，則此為強制參數。</span><span class="sxs-lookup"><span data-stu-id="a01fb-125">This is a mandatory parameter if Accepted parameter is true.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms
Parameter Sets: InputObjectAcceptParameterSet, InputObjectRejectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a01fb-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="a01fb-126">-Name</span></span>
<span data-ttu-id="a01fb-127">部署的圖像之計畫識別碼字串。</span><span class="sxs-lookup"><span data-stu-id="a01fb-127">Plan identifier string of image being deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a01fb-128">-產品</span><span class="sxs-lookup"><span data-stu-id="a01fb-128">-Product</span></span>
<span data-ttu-id="a01fb-129">提供部署之影像的識別碼字串。</span><span class="sxs-lookup"><span data-stu-id="a01fb-129">Offer identifier string of image being deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a01fb-130">-Publisher</span><span class="sxs-lookup"><span data-stu-id="a01fb-130">-Publisher</span></span>
<span data-ttu-id="a01fb-131">部署之圖像的 Publisher 識別碼字串。</span><span class="sxs-lookup"><span data-stu-id="a01fb-131">Publisher identifier string of image being deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a01fb-132">-拒絕</span><span class="sxs-lookup"><span data-stu-id="a01fb-132">-Reject</span></span>
<span data-ttu-id="a01fb-133">傳遞此選項以拒絕法律條款。</span><span class="sxs-lookup"><span data-stu-id="a01fb-133">Pass this to reject the legal terms.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AgreementRejectParameterSet, InputObjectRejectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a01fb-134">-條款</span><span class="sxs-lookup"><span data-stu-id="a01fb-134">-Terms</span></span>
<span data-ttu-id="a01fb-135">在 Cmdlet 中Get-AzMarketplaceTerms字詞物件。</span><span class="sxs-lookup"><span data-stu-id="a01fb-135">Terms object returned in Get-AzMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="a01fb-136">如果接受參數為 True，則此為強制參數。</span><span class="sxs-lookup"><span data-stu-id="a01fb-136">This is a mandatory parameter if Accepted parameter is true.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a01fb-137">-確認</span><span class="sxs-lookup"><span data-stu-id="a01fb-137">-Confirm</span></span>
<span data-ttu-id="a01fb-138">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a01fb-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a01fb-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a01fb-139">-WhatIf</span></span>
<span data-ttu-id="a01fb-140">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a01fb-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a01fb-141">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a01fb-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a01fb-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a01fb-142">CommonParameters</span></span>
<span data-ttu-id="a01fb-143">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a01fb-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a01fb-144">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="a01fb-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a01fb-145">輸入</span><span class="sxs-lookup"><span data-stu-id="a01fb-145">INPUTS</span></span>

### <span data-ttu-id="a01fb-146">Microsoft.Azure.Commands.MarketplaceOrdering.models.PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="a01fb-146">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="a01fb-147">輸出</span><span class="sxs-lookup"><span data-stu-id="a01fb-147">OUTPUTS</span></span>

### <span data-ttu-id="a01fb-148">Microsoft.Azure.Commands.MarketplaceOrdering.models.PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="a01fb-148">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="a01fb-149">筆記</span><span class="sxs-lookup"><span data-stu-id="a01fb-149">NOTES</span></span>

## <span data-ttu-id="a01fb-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="a01fb-150">RELATED LINKS</span></span>
