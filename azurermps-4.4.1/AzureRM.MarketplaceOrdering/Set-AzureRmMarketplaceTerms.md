---
external help file: Microsoft.Azure.Commands.MarketplaceOrdering.dll-Help.xml
Module Name: AzureRM.MarketplaceOrdering
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/Set-AzureRmMarketplaceTerms.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/Set-AzureRmMarketplaceTerms.md
ms.openlocfilehash: 843bb68c5aebc18af60e1cc74915b269738059f1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456539"
---
# <span data-ttu-id="623ef-101">Set-AzureRmMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="623ef-101">Set-AzureRmMarketplaceTerms</span></span>

## <span data-ttu-id="623ef-102">摘要</span><span class="sxs-lookup"><span data-stu-id="623ef-102">SYNOPSIS</span></span>
<span data-ttu-id="623ef-103">接受或拒絕指定發行者識別碼 (Publisher) 中的條款，提供識別碼 (產品) 與計畫識別碼 (名稱) 。</span><span class="sxs-lookup"><span data-stu-id="623ef-103">Accept or reject terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="623ef-104">請使用 Get-AzureRmMarketplaceTerms 取得合約條款。</span><span class="sxs-lookup"><span data-stu-id="623ef-104">Please use Get-AzureRmMarketplaceTerms to get the agreement terms.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="623ef-105">句法</span><span class="sxs-lookup"><span data-stu-id="623ef-105">SYNTAX</span></span>

### <span data-ttu-id="623ef-106">AgreementAcceptParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="623ef-106">AgreementAcceptParameterSet (Default)</span></span>
```
Set-AzureRmMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Accept]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="623ef-107">AgreementRejectParameterSet</span><span class="sxs-lookup"><span data-stu-id="623ef-107">AgreementRejectParameterSet</span></span>
```
Set-AzureRmMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Reject]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="623ef-108">InputObjectAcceptParametrSet</span><span class="sxs-lookup"><span data-stu-id="623ef-108">InputObjectAcceptParametrSet</span></span>
```
Set-AzureRmMarketplaceTerms [-Accept] [-InputObject] <PSAgreementTerms>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="623ef-109">InputObjectRejectParametrSet</span><span class="sxs-lookup"><span data-stu-id="623ef-109">InputObjectRejectParametrSet</span></span>
```
Set-AzureRmMarketplaceTerms [-Reject] [-InputObject] <PSAgreementTerms>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="623ef-110">說明</span><span class="sxs-lookup"><span data-stu-id="623ef-110">DESCRIPTION</span></span>
<span data-ttu-id="623ef-111">**AzureRmMarketplaceTerms** Cmdlet 會將指定的發行者 (id 的使用條款物件儲存在 publisher) ，提供識別碼 (產品) 與計畫識別碼 (名稱) 元組。</span><span class="sxs-lookup"><span data-stu-id="623ef-111">The **Set-AzureRmMarketplaceTerms** cmdlet saves the terms object for given publisher id(Publisher), offer id(Product) and plan id(Name) tuple.</span></span>

## <span data-ttu-id="623ef-112">示例</span><span class="sxs-lookup"><span data-stu-id="623ef-112">EXAMPLES</span></span>

### <span data-ttu-id="623ef-113">範例1</span><span class="sxs-lookup"><span data-stu-id="623ef-113">Example 1</span></span>
```
PS C:\> Set-AzureRmMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" -Terms $agreementTerms -Accept
```

### <span data-ttu-id="623ef-114">範例2</span><span class="sxs-lookup"><span data-stu-id="623ef-114">Example 2</span></span>
```
PS C:\> Get-AzureRmMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" | Set-AzureRmMarketplaceTerms -Accept
```

## <span data-ttu-id="623ef-115">參數</span><span class="sxs-lookup"><span data-stu-id="623ef-115">PARAMETERS</span></span>

### <span data-ttu-id="623ef-116">-接受</span><span class="sxs-lookup"><span data-stu-id="623ef-116">-Accept</span></span>
<span data-ttu-id="623ef-117">您可以傳送這個協定來接受法律條款。</span><span class="sxs-lookup"><span data-stu-id="623ef-117">Pass this to accept the legal terms.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AgreementAcceptParameterSet, InputObjectAcceptParametrSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="623ef-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="623ef-118">-DefaultProfile</span></span>
<span data-ttu-id="623ef-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="623ef-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="623ef-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="623ef-120">-InputObject</span></span>
<span data-ttu-id="623ef-121">在 Get-AzureRmMarketplaceTerms Cmdlet 中傳回的詞彙物件。</span><span class="sxs-lookup"><span data-stu-id="623ef-121">Terms object returned in Get-AzureRmMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="623ef-122">如果接受的參數為 true，則這是強制性參數。</span><span class="sxs-lookup"><span data-stu-id="623ef-122">This is a mandatory parameter if Accepted paramter is true.</span></span>

```yaml
Type: PSAgreementTerms
Parameter Sets: InputObjectAcceptParametrSet, InputObjectRejectParametrSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="623ef-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="623ef-123">-Name</span></span>
<span data-ttu-id="623ef-124">規劃要部署之影像的識別碼字串。</span><span class="sxs-lookup"><span data-stu-id="623ef-124">Plan identifier string of image being deployed.</span></span>

```yaml
Type: String
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="623ef-125">-產品</span><span class="sxs-lookup"><span data-stu-id="623ef-125">-Product</span></span>
<span data-ttu-id="623ef-126">提供要部署之影像的識別碼字串。</span><span class="sxs-lookup"><span data-stu-id="623ef-126">Offer identifier string of image being deployed.</span></span>

```yaml
Type: String
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="623ef-127">-Publisher</span><span class="sxs-lookup"><span data-stu-id="623ef-127">-Publisher</span></span>
<span data-ttu-id="623ef-128">要部署之影像的發行者識別碼字串。</span><span class="sxs-lookup"><span data-stu-id="623ef-128">Publisher identifier string of image being deployed.</span></span>

```yaml
Type: String
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="623ef-129">-拒絕</span><span class="sxs-lookup"><span data-stu-id="623ef-129">-Reject</span></span>
<span data-ttu-id="623ef-130">若要拒絕法律條款，請傳送。</span><span class="sxs-lookup"><span data-stu-id="623ef-130">Pass this to reject the legal terms.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AgreementRejectParameterSet, InputObjectRejectParametrSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="623ef-131">-詞彙</span><span class="sxs-lookup"><span data-stu-id="623ef-131">-Terms</span></span>
<span data-ttu-id="623ef-132">在 Get-AzureRmMarketplaceTerms Cmdlet 中傳回的詞彙物件。</span><span class="sxs-lookup"><span data-stu-id="623ef-132">Terms object returned in Get-AzureRmMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="623ef-133">如果接受的參數為 true，則這是強制性參數。</span><span class="sxs-lookup"><span data-stu-id="623ef-133">This is a mandatory parameter if Accepted paramter is true.</span></span>

```yaml
Type: PSAgreementTerms
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="623ef-134">-確認</span><span class="sxs-lookup"><span data-stu-id="623ef-134">-Confirm</span></span>
<span data-ttu-id="623ef-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="623ef-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="623ef-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="623ef-136">-WhatIf</span></span>
<span data-ttu-id="623ef-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="623ef-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="623ef-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="623ef-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="623ef-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="623ef-139">CommonParameters</span></span>
<span data-ttu-id="623ef-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="623ef-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="623ef-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="623ef-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="623ef-142">輸入</span><span class="sxs-lookup"><span data-stu-id="623ef-142">INPUTS</span></span>

### <span data-ttu-id="623ef-143">PSAgreementTerms 中的 MarketplaceOrdering。</span><span class="sxs-lookup"><span data-stu-id="623ef-143">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>
<span data-ttu-id="623ef-144">PSAgreementTerms 中的 MarketplaceOrdering。</span><span class="sxs-lookup"><span data-stu-id="623ef-144">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="623ef-145">輸出</span><span class="sxs-lookup"><span data-stu-id="623ef-145">OUTPUTS</span></span>

### <span data-ttu-id="623ef-146">PSAgreementTerms 中的 MarketplaceOrdering。</span><span class="sxs-lookup"><span data-stu-id="623ef-146">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>
<span data-ttu-id="623ef-147">PSAgreementTerms 中的 MarketplaceOrdering。</span><span class="sxs-lookup"><span data-stu-id="623ef-147">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="623ef-148">筆記</span><span class="sxs-lookup"><span data-stu-id="623ef-148">NOTES</span></span>

## <span data-ttu-id="623ef-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="623ef-149">RELATED LINKS</span></span>

