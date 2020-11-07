---
external help file: Microsoft.Azure.Commands.MarketplaceOrdering.dll-Help.xml
Module Name: AzureRM.MarketplaceOrdering
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.marketplaceordering/set-azurermmarketplaceterms
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/Set-AzureRmMarketplaceTerms.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/Set-AzureRmMarketplaceTerms.md
ms.openlocfilehash: 7932a733fcd672d8ee92e6452765745281ee0a2f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623690"
---
# <span data-ttu-id="e3f5a-101">Set-AzureRmMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="e3f5a-101">Set-AzureRmMarketplaceTerms</span></span>

## <span data-ttu-id="e3f5a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e3f5a-102">SYNOPSIS</span></span>
<span data-ttu-id="e3f5a-103">接受或拒絕指定發行者識別碼 (Publisher) 中的條款，提供識別碼 (產品) 與計畫識別碼 (名稱) 。</span><span class="sxs-lookup"><span data-stu-id="e3f5a-103">Accept or reject terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="e3f5a-104">請使用 Get-AzureRmMarketplaceTerms 取得合約條款。</span><span class="sxs-lookup"><span data-stu-id="e3f5a-104">Please use Get-AzureRmMarketplaceTerms to get the agreement terms.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3f5a-105">句法</span><span class="sxs-lookup"><span data-stu-id="e3f5a-105">SYNTAX</span></span>

### <span data-ttu-id="e3f5a-106">AgreementAcceptParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e3f5a-106">AgreementAcceptParameterSet (Default)</span></span>
```
Set-AzureRmMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Accept]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e3f5a-107">AgreementRejectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3f5a-107">AgreementRejectParameterSet</span></span>
```
Set-AzureRmMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Reject]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e3f5a-108">InputObjectAcceptParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3f5a-108">InputObjectAcceptParameterSet</span></span>
```
Set-AzureRmMarketplaceTerms [-Accept] [-InputObject] <PSAgreementTerms>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3f5a-109">InputObjectRejectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3f5a-109">InputObjectRejectParameterSet</span></span>
```
Set-AzureRmMarketplaceTerms [-Reject] [-InputObject] <PSAgreementTerms>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3f5a-110">說明</span><span class="sxs-lookup"><span data-stu-id="e3f5a-110">DESCRIPTION</span></span>
<span data-ttu-id="e3f5a-111">**AzureRmMarketplaceTerms** Cmdlet 會將指定的發行者 (id 的使用條款物件儲存在 publisher) ，提供識別碼 (產品) 與計畫識別碼 (名稱) 元組。</span><span class="sxs-lookup"><span data-stu-id="e3f5a-111">The **Set-AzureRmMarketplaceTerms** cmdlet saves the terms object for given publisher id(Publisher), offer id(Product) and plan id(Name) tuple.</span></span>

## <span data-ttu-id="e3f5a-112">示例</span><span class="sxs-lookup"><span data-stu-id="e3f5a-112">EXAMPLES</span></span>

### <span data-ttu-id="e3f5a-113">範例1</span><span class="sxs-lookup"><span data-stu-id="e3f5a-113">Example 1</span></span>
<span data-ttu-id="e3f5a-114">取得市場發行者合約</span><span class="sxs-lookup"><span data-stu-id="e3f5a-114">Get the marketplace publisher agreement</span></span>
```
PS C:\> Get-AzureRmMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" | Set-AzureRmMarketplaceTerms -Accept
```

### <span data-ttu-id="e3f5a-115">範例2</span><span class="sxs-lookup"><span data-stu-id="e3f5a-115">Example 2</span></span>
<span data-ttu-id="e3f5a-116">將發行者協定設定為 [Accept] （接受）。</span><span class="sxs-lookup"><span data-stu-id="e3f5a-116">Set the publisher agreement to 'Accept'.</span></span> <span data-ttu-id="e3f5a-117">從「AzureRmMarketplaceTerms」 Cmdlet 取得「字詞」參數的值</span><span class="sxs-lookup"><span data-stu-id="e3f5a-117">Get the value for the 'Terms' parameter from the 'Get-AzureRmMarketplaceTerms' cmdlet</span></span>
```
PS C:\> Set-AzureRmMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" -Terms $agreementTerms -Accept
```


## <span data-ttu-id="e3f5a-118">參數</span><span class="sxs-lookup"><span data-stu-id="e3f5a-118">PARAMETERS</span></span>

### <span data-ttu-id="e3f5a-119">-接受</span><span class="sxs-lookup"><span data-stu-id="e3f5a-119">-Accept</span></span>
<span data-ttu-id="e3f5a-120">您可以傳送這個協定來接受法律條款。</span><span class="sxs-lookup"><span data-stu-id="e3f5a-120">Pass this to accept the legal terms.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AgreementAcceptParameterSet, InputObjectAcceptParametrSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3f5a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3f5a-121">-DefaultProfile</span></span>
<span data-ttu-id="e3f5a-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e3f5a-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3f5a-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e3f5a-123">-InputObject</span></span>
<span data-ttu-id="e3f5a-124">在 Get-AzureRmMarketplaceTerms Cmdlet 中傳回的詞彙物件。</span><span class="sxs-lookup"><span data-stu-id="e3f5a-124">Terms object returned in Get-AzureRmMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="e3f5a-125">如果接受的參數為 true，則這是強制性參數。</span><span class="sxs-lookup"><span data-stu-id="e3f5a-125">This is a mandatory parameter if Accepted paramter is true.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms
Parameter Sets: InputObjectAcceptParametrSet, InputObjectRejectParametrSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3f5a-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="e3f5a-126">-Name</span></span>
<span data-ttu-id="e3f5a-127">規劃要部署之影像的識別碼字串。</span><span class="sxs-lookup"><span data-stu-id="e3f5a-127">Plan identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="e3f5a-128">-產品</span><span class="sxs-lookup"><span data-stu-id="e3f5a-128">-Product</span></span>
<span data-ttu-id="e3f5a-129">提供要部署之影像的識別碼字串。</span><span class="sxs-lookup"><span data-stu-id="e3f5a-129">Offer identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="e3f5a-130">-Publisher</span><span class="sxs-lookup"><span data-stu-id="e3f5a-130">-Publisher</span></span>
<span data-ttu-id="e3f5a-131">要部署之影像的發行者識別碼字串。</span><span class="sxs-lookup"><span data-stu-id="e3f5a-131">Publisher identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="e3f5a-132">-拒絕</span><span class="sxs-lookup"><span data-stu-id="e3f5a-132">-Reject</span></span>
<span data-ttu-id="e3f5a-133">若要拒絕法律條款，請傳送。</span><span class="sxs-lookup"><span data-stu-id="e3f5a-133">Pass this to reject the legal terms.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AgreementRejectParameterSet, InputObjectRejectParametrSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3f5a-134">-詞彙</span><span class="sxs-lookup"><span data-stu-id="e3f5a-134">-Terms</span></span>
<span data-ttu-id="e3f5a-135">在 Get-AzureRmMarketplaceTerms Cmdlet 中傳回的詞彙物件。</span><span class="sxs-lookup"><span data-stu-id="e3f5a-135">Terms object returned in Get-AzureRmMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="e3f5a-136">如果接受的參數為 true，則這是強制性參數。</span><span class="sxs-lookup"><span data-stu-id="e3f5a-136">This is a mandatory parameter if Accepted paramter is true.</span></span>

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

### <span data-ttu-id="e3f5a-137">-確認</span><span class="sxs-lookup"><span data-stu-id="e3f5a-137">-Confirm</span></span>
<span data-ttu-id="e3f5a-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e3f5a-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3f5a-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3f5a-139">-WhatIf</span></span>
<span data-ttu-id="e3f5a-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e3f5a-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e3f5a-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e3f5a-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3f5a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3f5a-142">CommonParameters</span></span>
<span data-ttu-id="e3f5a-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e3f5a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3f5a-144">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e3f5a-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3f5a-145">輸入</span><span class="sxs-lookup"><span data-stu-id="e3f5a-145">INPUTS</span></span>

### <span data-ttu-id="e3f5a-146">PSAgreementTerms 中的 MarketplaceOrdering。</span><span class="sxs-lookup"><span data-stu-id="e3f5a-146">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>
<span data-ttu-id="e3f5a-147">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="e3f5a-147">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="e3f5a-148">輸出</span><span class="sxs-lookup"><span data-stu-id="e3f5a-148">OUTPUTS</span></span>

### <span data-ttu-id="e3f5a-149">PSAgreementTerms 中的 MarketplaceOrdering。</span><span class="sxs-lookup"><span data-stu-id="e3f5a-149">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="e3f5a-150">筆記</span><span class="sxs-lookup"><span data-stu-id="e3f5a-150">NOTES</span></span>

## <span data-ttu-id="e3f5a-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="e3f5a-151">RELATED LINKS</span></span>
