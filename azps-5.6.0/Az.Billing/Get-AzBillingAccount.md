---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/powershell/module/az.billing/get-azbillingaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingAccount.md
ms.openlocfilehash: 8c934adfd0bea950f97fbe8e8226568f9eaf57dc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903869"
---
# <span data-ttu-id="378c8-101">Get-AzBillingAccount</span><span class="sxs-lookup"><span data-stu-id="378c8-101">Get-AzBillingAccount</span></span>

## <span data-ttu-id="378c8-102">簡介</span><span class="sxs-lookup"><span data-stu-id="378c8-102">SYNOPSIS</span></span>
<span data-ttu-id="378c8-103">取得帳單帳戶。</span><span class="sxs-lookup"><span data-stu-id="378c8-103">Get billing accounts.</span></span>

## <span data-ttu-id="378c8-104">語法</span><span class="sxs-lookup"><span data-stu-id="378c8-104">SYNTAX</span></span>

### <span data-ttu-id="378c8-105">清單 (預設) </span><span class="sxs-lookup"><span data-stu-id="378c8-105">List (Default)</span></span>
```
Get-AzBillingAccount [-IncludeAddress] [-ExpandBillingProfile] [-ExpandInvoiceSection] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="378c8-106">單</span><span class="sxs-lookup"><span data-stu-id="378c8-106">Single</span></span>
```
Get-AzBillingAccount -Name <System.Collections.Generic.List`1[System.String]> [-IncludeAddress] [-ExpandBillingProfile] [-ExpandInvoiceSection] [-ListEntitiesToCreateSubscription]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="378c8-107">描述</span><span class="sxs-lookup"><span data-stu-id="378c8-107">DESCRIPTION</span></span>
<span data-ttu-id="378c8-108">**Get-AzBillingAccount** Cmdlet 會取得帳單帳戶，使用者可以存取。</span><span class="sxs-lookup"><span data-stu-id="378c8-108">The **Get-AzBillingAccount** cmdlet gets billing accounts, user has access to.</span></span> 

## <span data-ttu-id="378c8-109">例子</span><span class="sxs-lookup"><span data-stu-id="378c8-109">EXAMPLES</span></span>

### <span data-ttu-id="378c8-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="378c8-110">Example 1</span></span>
```
PS C:\> Get-AzBillingAccount
```

<span data-ttu-id="378c8-111">取得使用者能夠存取的所有帳單帳戶。</span><span class="sxs-lookup"><span data-stu-id="378c8-111">Get all billing accounts user has access to.</span></span>

### <span data-ttu-id="378c8-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="378c8-112">Example 2</span></span>
```
PS C:\> Get-AzBillingAccount -Name 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="378c8-113">取得具有指定名稱的帳單帳戶。</span><span class="sxs-lookup"><span data-stu-id="378c8-113">Get the billing account with the specified name.</span></span>

### <span data-ttu-id="378c8-114">範例 3</span><span class="sxs-lookup"><span data-stu-id="378c8-114">Example 3</span></span>
```
PS C:\> Get-AzBillingAccount -IncludeAddress
```

<span data-ttu-id="378c8-115">取得使用者能夠存取的所有帳單帳戶，並納入結果中的位址。</span><span class="sxs-lookup"><span data-stu-id="378c8-115">Get all billing accounts user has access to, and include the address in the result.</span></span>

### <span data-ttu-id="378c8-116">範例 4</span><span class="sxs-lookup"><span data-stu-id="378c8-116">Example 4</span></span>
```
PS C:\> Get-AzBillingAccount -ExpandBillingProfile
```

<span data-ttu-id="378c8-117">取得使用者能夠存取的所有帳單帳戶，並納入結果中的帳單設定檔。</span><span class="sxs-lookup"><span data-stu-id="378c8-117">Get all billing accounts user has access to, and include the billing profiles in the result.</span></span>

### <span data-ttu-id="378c8-118">範例 5</span><span class="sxs-lookup"><span data-stu-id="378c8-118">Example 5</span></span>
```
PS C:\> Get-AzBillingAccount -ExpandInvoiceSection
```

<span data-ttu-id="378c8-119">取得使用者能夠存取的所有帳單帳戶，並包含帳單設定檔及其下的發票區段。</span><span class="sxs-lookup"><span data-stu-id="378c8-119">Get all billing accounts user has access to, and include the billing profiles and invoice sections under them in the result.</span></span>

### <span data-ttu-id="378c8-120">範例 6</span><span class="sxs-lookup"><span data-stu-id="378c8-120">Example 6</span></span>
```
PS C:\> Get-AzBillingAccount -ExpandInvoiceSection -ExpandAddress -Name 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="378c8-121">取得具有指定名稱的帳單帳戶，並納入結果中的位址、帳單設定檔和發票區段。</span><span class="sxs-lookup"><span data-stu-id="378c8-121">Get the billing account with the specified name, and include the address, billing profiles and invoice sections under them in the result.</span></span>

## <span data-ttu-id="378c8-122">參數</span><span class="sxs-lookup"><span data-stu-id="378c8-122">PARAMETERS</span></span>

### <span data-ttu-id="378c8-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="378c8-123">-DefaultProfile</span></span>
<span data-ttu-id="378c8-124">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="378c8-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="378c8-125">-IncludeAddress</span><span class="sxs-lookup"><span data-stu-id="378c8-125">-IncludeAddress</span></span>
<span data-ttu-id="378c8-126">包含帳單帳戶的位址。</span><span class="sxs-lookup"><span data-stu-id="378c8-126">Include the address of the billing account.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="378c8-127">-ExpandBillingProfile</span><span class="sxs-lookup"><span data-stu-id="378c8-127">-ExpandBillingProfile</span></span>
<span data-ttu-id="378c8-128">在帳單帳戶下包含帳單設定檔。</span><span class="sxs-lookup"><span data-stu-id="378c8-128">Include the billing profiles under the billing account.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="378c8-129">-ExpandInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="378c8-129">-ExpandInvoiceSection</span></span>
<span data-ttu-id="378c8-130">在帳單帳戶下包含帳單設定檔，以及其下的發票區段。</span><span class="sxs-lookup"><span data-stu-id="378c8-130">Include the billing profiles under billing account and invoices sections under them.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="378c8-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="378c8-131">-Name</span></span>
<span data-ttu-id="378c8-132">特定帳單帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="378c8-132">Name of a specific billing account.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Single
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="378c8-133">-ListEntitiesToCreateSubscription</span><span class="sxs-lookup"><span data-stu-id="378c8-133">-ListEntitiesToCreateSubscription</span></span>
<span data-ttu-id="378c8-134">在帳單帳戶下列出帳單實體，以做為建立訂閱的輸入。</span><span class="sxs-lookup"><span data-stu-id="378c8-134">List the billing entities under billing account which can be used as input to create subscription.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="378c8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="378c8-135">CommonParameters</span></span>
<span data-ttu-id="378c8-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="378c8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="378c8-137">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="378c8-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="378c8-138">輸入</span><span class="sxs-lookup"><span data-stu-id="378c8-138">INPUTS</span></span>

### <span data-ttu-id="378c8-139">沒有</span><span class="sxs-lookup"><span data-stu-id="378c8-139">None</span></span>

## <span data-ttu-id="378c8-140">輸出</span><span class="sxs-lookup"><span data-stu-id="378c8-140">OUTPUTS</span></span>

### <span data-ttu-id="378c8-141">Microsoft.Azure.Commands.Billing.models.PSBillingAccount</span><span class="sxs-lookup"><span data-stu-id="378c8-141">Microsoft.Azure.Commands.Billing.Models.PSBillingAccount</span></span>

## <span data-ttu-id="378c8-142">筆記</span><span class="sxs-lookup"><span data-stu-id="378c8-142">NOTES</span></span>

## <span data-ttu-id="378c8-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="378c8-143">RELATED LINKS</span></span>
