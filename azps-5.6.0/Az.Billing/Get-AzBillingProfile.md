---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/powershell/module/az.billing/get-azbillingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingProfile.md
ms.openlocfilehash: c66b3a2c4c151daf0a5d3df62aaaf248a7d2e338
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910542"
---
# <span data-ttu-id="cd7ef-101">Get-AzBillingProfile</span><span class="sxs-lookup"><span data-stu-id="cd7ef-101">Get-AzBillingProfile</span></span>

## <span data-ttu-id="cd7ef-102">簡介</span><span class="sxs-lookup"><span data-stu-id="cd7ef-102">SYNOPSIS</span></span>
<span data-ttu-id="cd7ef-103">取得帳單設定檔。</span><span class="sxs-lookup"><span data-stu-id="cd7ef-103">Get billing profiles.</span></span>

## <span data-ttu-id="cd7ef-104">語法</span><span class="sxs-lookup"><span data-stu-id="cd7ef-104">SYNTAX</span></span>

### <span data-ttu-id="cd7ef-105">清單 (預設) </span><span class="sxs-lookup"><span data-stu-id="cd7ef-105">List (Default)</span></span>
```
Get-AzBillingProfile -BillingAccountName <String> -BillingProfileName <String> [-ExpandInvoiceSection]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd7ef-106">單</span><span class="sxs-lookup"><span data-stu-id="cd7ef-106">Single</span></span>
```
Get-AzBillingProfile -BillingAccountName <String> -BillingProfileName <String> -Name <System.Collections.Generic.List`1[System.String]> [-ExpandInvoiceSection]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd7ef-107">描述</span><span class="sxs-lookup"><span data-stu-id="cd7ef-107">DESCRIPTION</span></span>
<span data-ttu-id="cd7ef-108">**Get-AzBillingProfile** Cmdlet 會取得指定帳單帳戶下的帳單設定檔。</span><span class="sxs-lookup"><span data-stu-id="cd7ef-108">The **Get-AzBillingProfile** cmdlet gets billing profiles under the specified billing account.</span></span> 

## <span data-ttu-id="cd7ef-109">例子</span><span class="sxs-lookup"><span data-stu-id="cd7ef-109">EXAMPLES</span></span>

### <span data-ttu-id="cd7ef-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="cd7ef-110">Example 1</span></span>
```
PS C:\> Get-AzBillingProfile -BillingAccountName 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="cd7ef-111">取得指定帳單帳戶下的所有帳單設定檔。</span><span class="sxs-lookup"><span data-stu-id="cd7ef-111">Get all billing profiles under the specified billing account.</span></span>

### <span data-ttu-id="cd7ef-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="cd7ef-112">Example 2</span></span>
```
PS C:\> Get-AzBillingProfile -BillingAccountName 00000000-0000-0000-0000-000000000000 -Name AAAA-0A00-AAA-ZZZ
```

<span data-ttu-id="cd7ef-113">取得具有指定名稱的帳單設定檔。</span><span class="sxs-lookup"><span data-stu-id="cd7ef-113">Get the billing profile with the specified name.</span></span>

### <span data-ttu-id="cd7ef-114">範例 3</span><span class="sxs-lookup"><span data-stu-id="cd7ef-114">Example 3</span></span>
```
PS C:\> Get-AzBillingProfile -BillingAccountName 00000000-0000-0000-0000-000000000000 -ExpandInvoiceSection
```

<span data-ttu-id="cd7ef-115">取得指定帳單帳戶下的所有帳單設定檔，並包含結果中的發票區段。</span><span class="sxs-lookup"><span data-stu-id="cd7ef-115">Get all billing profiles under specified billing account, and include the invoice sections in the result.</span></span>

### <span data-ttu-id="cd7ef-116">範例 4</span><span class="sxs-lookup"><span data-stu-id="cd7ef-116">Example 4</span></span>
```
PS C:\> Get-AzBillingProfile -BillingAccountName 00000000-0000-0000-0000-000000000000 -ExpandInvoiceSection -Name <System.Collections.Generic.List`1[System.String]>
```

<span data-ttu-id="cd7ef-117">取得具有指定名稱的帳單設定檔，並包含結果中的發票區段。</span><span class="sxs-lookup"><span data-stu-id="cd7ef-117">Get the billing profile with the specified name, and include the invoice sections in the result.</span></span>

## <span data-ttu-id="cd7ef-118">參數</span><span class="sxs-lookup"><span data-stu-id="cd7ef-118">PARAMETERS</span></span>

### <span data-ttu-id="cd7ef-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd7ef-119">-DefaultProfile</span></span>
<span data-ttu-id="cd7ef-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="cd7ef-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cd7ef-121">-BillingAccountName</span><span class="sxs-lookup"><span data-stu-id="cd7ef-121">-BillingAccountName</span></span>
<span data-ttu-id="cd7ef-122">特定帳單帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="cd7ef-122">Name of the specific billing account.</span></span>

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

### <span data-ttu-id="cd7ef-123">-ExpandInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="cd7ef-123">-ExpandInvoiceSection</span></span>
<span data-ttu-id="cd7ef-124">在帳單設定檔下包含發票區段。</span><span class="sxs-lookup"><span data-stu-id="cd7ef-124">Include the invoices sections under billing profile.</span></span>

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

### <span data-ttu-id="cd7ef-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="cd7ef-125">-Name</span></span>
<span data-ttu-id="cd7ef-126">特定帳單設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="cd7ef-126">Name of a specific billing profile.</span></span>

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

### <span data-ttu-id="cd7ef-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd7ef-127">CommonParameters</span></span>
<span data-ttu-id="cd7ef-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="cd7ef-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd7ef-129">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="cd7ef-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd7ef-130">輸入</span><span class="sxs-lookup"><span data-stu-id="cd7ef-130">INPUTS</span></span>

### <span data-ttu-id="cd7ef-131">沒有</span><span class="sxs-lookup"><span data-stu-id="cd7ef-131">None</span></span>

## <span data-ttu-id="cd7ef-132">輸出</span><span class="sxs-lookup"><span data-stu-id="cd7ef-132">OUTPUTS</span></span>

### <span data-ttu-id="cd7ef-133">Microsoft.Azure.Commands.Billing.models.PSBillingProfile</span><span class="sxs-lookup"><span data-stu-id="cd7ef-133">Microsoft.Azure.Commands.Billing.Models.PSBillingProfile</span></span>

## <span data-ttu-id="cd7ef-134">筆記</span><span class="sxs-lookup"><span data-stu-id="cd7ef-134">NOTES</span></span>

## <span data-ttu-id="cd7ef-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="cd7ef-135">RELATED LINKS</span></span>
