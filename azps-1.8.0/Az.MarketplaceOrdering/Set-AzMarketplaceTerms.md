---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MarketplaceOrdering.dll-Help.xml
Module Name: Az.MarketplaceOrdering
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplaceordering/set-azmarketplaceterms
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Set-AzMarketplaceTerms.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Set-AzMarketplaceTerms.md
ms.openlocfilehash: 1cea045bd9b663e542bb435003df79f153542a75
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93786846"
---
# <span data-ttu-id="76301-101">Set-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="76301-101">Set-AzMarketplaceTerms</span></span>

## <span data-ttu-id="76301-102">摘要</span><span class="sxs-lookup"><span data-stu-id="76301-102">SYNOPSIS</span></span>
<span data-ttu-id="76301-103">接受或拒絕指定發行者識別碼 (Publisher) 中的條款，提供識別碼 (產品) 與計畫識別碼 (名稱) 。</span><span class="sxs-lookup"><span data-stu-id="76301-103">Accept or reject terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="76301-104">請使用 Get-AzMarketplaceTerms 取得合約條款。</span><span class="sxs-lookup"><span data-stu-id="76301-104">Please use Get-AzMarketplaceTerms to get the agreement terms.</span></span>

## <span data-ttu-id="76301-105">句法</span><span class="sxs-lookup"><span data-stu-id="76301-105">SYNTAX</span></span>

### <span data-ttu-id="76301-106">AgreementAcceptParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="76301-106">AgreementAcceptParameterSet (Default)</span></span>
```
Set-AzMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Accept]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="76301-107">AgreementRejectParameterSet</span><span class="sxs-lookup"><span data-stu-id="76301-107">AgreementRejectParameterSet</span></span>
```
Set-AzMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Reject]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="76301-108">InputObjectAcceptParameterSet</span><span class="sxs-lookup"><span data-stu-id="76301-108">InputObjectAcceptParameterSet</span></span>
```
Set-AzMarketplaceTerms [-Accept] [-InputObject] <PSAgreementTerms> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76301-109">InputObjectRejectParameterSet</span><span class="sxs-lookup"><span data-stu-id="76301-109">InputObjectRejectParameterSet</span></span>
```
Set-AzMarketplaceTerms [-Reject] [-InputObject] <PSAgreementTerms> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76301-110">說明</span><span class="sxs-lookup"><span data-stu-id="76301-110">DESCRIPTION</span></span>
<span data-ttu-id="76301-111">**AzMarketplaceTerms** Cmdlet 會將指定的發行者 (id 的使用條款物件儲存在 publisher) ，提供識別碼 (產品) 與計畫識別碼 (名稱) 元組。</span><span class="sxs-lookup"><span data-stu-id="76301-111">The **Set-AzMarketplaceTerms** cmdlet saves the terms object for given publisher id(Publisher), offer id(Product) and plan id(Name) tuple.</span></span>

## <span data-ttu-id="76301-112">示例</span><span class="sxs-lookup"><span data-stu-id="76301-112">EXAMPLES</span></span>

### <span data-ttu-id="76301-113">範例1</span><span class="sxs-lookup"><span data-stu-id="76301-113">Example 1</span></span>
<span data-ttu-id="76301-114">取得市場發行者合約</span><span class="sxs-lookup"><span data-stu-id="76301-114">Get the marketplace publisher agreement</span></span>


```
PS C:\> Get-AzMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" | Set-AzMarketplaceTerms -Accept
```

### <span data-ttu-id="76301-115">範例2</span><span class="sxs-lookup"><span data-stu-id="76301-115">Example 2</span></span>
<span data-ttu-id="76301-116">將發行者協定設定為 [Accept] （接受）。</span><span class="sxs-lookup"><span data-stu-id="76301-116">Set the publisher agreement to 'Accept'.</span></span> <span data-ttu-id="76301-117">從「AzMarketplaceTerms」 Cmdlet 取得「字詞」參數的值</span><span class="sxs-lookup"><span data-stu-id="76301-117">Get the value for the 'Terms' parameter from the 'Get-AzMarketplaceTerms' cmdlet</span></span>


```
PS C:\> Set-AzMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" -Terms $agreementTerms -Accept
```

## <span data-ttu-id="76301-118">參數</span><span class="sxs-lookup"><span data-stu-id="76301-118">PARAMETERS</span></span>

### <span data-ttu-id="76301-119">-接受</span><span class="sxs-lookup"><span data-stu-id="76301-119">-Accept</span></span>
<span data-ttu-id="76301-120">您可以傳送這個協定來接受法律條款。</span><span class="sxs-lookup"><span data-stu-id="76301-120">Pass this to accept the legal terms.</span></span>

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

### <span data-ttu-id="76301-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76301-121">-DefaultProfile</span></span>
<span data-ttu-id="76301-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="76301-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76301-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="76301-123">-InputObject</span></span>
<span data-ttu-id="76301-124">在 Get-AzMarketplaceTerms Cmdlet 中傳回的詞彙物件。</span><span class="sxs-lookup"><span data-stu-id="76301-124">Terms object returned in Get-AzMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="76301-125">如果接受的參數為 true，則這是強制性參數。</span><span class="sxs-lookup"><span data-stu-id="76301-125">This is a mandatory parameter if Accepted paramter is true.</span></span>

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

### <span data-ttu-id="76301-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="76301-126">-Name</span></span>
<span data-ttu-id="76301-127">規劃要部署之影像的識別碼字串。</span><span class="sxs-lookup"><span data-stu-id="76301-127">Plan identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="76301-128">-產品</span><span class="sxs-lookup"><span data-stu-id="76301-128">-Product</span></span>
<span data-ttu-id="76301-129">提供要部署之影像的識別碼字串。</span><span class="sxs-lookup"><span data-stu-id="76301-129">Offer identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="76301-130">-Publisher</span><span class="sxs-lookup"><span data-stu-id="76301-130">-Publisher</span></span>
<span data-ttu-id="76301-131">要部署之影像的發行者識別碼字串。</span><span class="sxs-lookup"><span data-stu-id="76301-131">Publisher identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="76301-132">-拒絕</span><span class="sxs-lookup"><span data-stu-id="76301-132">-Reject</span></span>
<span data-ttu-id="76301-133">若要拒絕法律條款，請傳送。</span><span class="sxs-lookup"><span data-stu-id="76301-133">Pass this to reject the legal terms.</span></span>

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

### <span data-ttu-id="76301-134">-詞彙</span><span class="sxs-lookup"><span data-stu-id="76301-134">-Terms</span></span>
<span data-ttu-id="76301-135">在 Get-AzMarketplaceTerms Cmdlet 中傳回的詞彙物件。</span><span class="sxs-lookup"><span data-stu-id="76301-135">Terms object returned in Get-AzMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="76301-136">如果接受的參數為 true，則這是強制性參數。</span><span class="sxs-lookup"><span data-stu-id="76301-136">This is a mandatory parameter if Accepted paramter is true.</span></span>

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

### <span data-ttu-id="76301-137">-確認</span><span class="sxs-lookup"><span data-stu-id="76301-137">-Confirm</span></span>
<span data-ttu-id="76301-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="76301-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76301-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76301-139">-WhatIf</span></span>
<span data-ttu-id="76301-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="76301-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="76301-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="76301-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76301-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76301-142">CommonParameters</span></span>
<span data-ttu-id="76301-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="76301-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76301-144">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="76301-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76301-145">輸入</span><span class="sxs-lookup"><span data-stu-id="76301-145">INPUTS</span></span>

### <span data-ttu-id="76301-146">PSAgreementTerms 中的 MarketplaceOrdering。</span><span class="sxs-lookup"><span data-stu-id="76301-146">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="76301-147">輸出</span><span class="sxs-lookup"><span data-stu-id="76301-147">OUTPUTS</span></span>

### <span data-ttu-id="76301-148">PSAgreementTerms 中的 MarketplaceOrdering。</span><span class="sxs-lookup"><span data-stu-id="76301-148">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="76301-149">筆記</span><span class="sxs-lookup"><span data-stu-id="76301-149">NOTES</span></span>

## <span data-ttu-id="76301-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="76301-150">RELATED LINKS</span></span>