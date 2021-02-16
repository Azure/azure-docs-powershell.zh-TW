---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azbillingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingProfile.md
ms.openlocfilehash: ec9ac0249715dc7c6d9966158b95261d0410c995
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100138762"
---
# <span data-ttu-id="c1837-101">Get-AzBillingProfile</span><span class="sxs-lookup"><span data-stu-id="c1837-101">Get-AzBillingProfile</span></span>

## <span data-ttu-id="c1837-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c1837-102">SYNOPSIS</span></span>
<span data-ttu-id="c1837-103">取得帳單設定檔。</span><span class="sxs-lookup"><span data-stu-id="c1837-103">Get billing profiles.</span></span>

## <span data-ttu-id="c1837-104">句法</span><span class="sxs-lookup"><span data-stu-id="c1837-104">SYNTAX</span></span>

### <span data-ttu-id="c1837-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="c1837-105">List (Default)</span></span>
```
Get-AzBillingProfile -BillingAccountName <String> -BillingProfileName <String> [-ExpandInvoiceSection]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1837-106">通過</span><span class="sxs-lookup"><span data-stu-id="c1837-106">Single</span></span>
```
Get-AzBillingProfile -BillingAccountName <String> -BillingProfileName <String> -Name <System.Collections.Generic.List`1[System.String]> [-ExpandInvoiceSection]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1837-107">說明</span><span class="sxs-lookup"><span data-stu-id="c1837-107">DESCRIPTION</span></span>
<span data-ttu-id="c1837-108">**AzBillingProfile** Cmdlet 會在指定的帳單帳戶下取得帳單設定檔。</span><span class="sxs-lookup"><span data-stu-id="c1837-108">The **Get-AzBillingProfile** cmdlet gets billing profiles under the specified billing account.</span></span> 

## <span data-ttu-id="c1837-109">示例</span><span class="sxs-lookup"><span data-stu-id="c1837-109">EXAMPLES</span></span>

### <span data-ttu-id="c1837-110">範例1</span><span class="sxs-lookup"><span data-stu-id="c1837-110">Example 1</span></span>
```
PS C:\> Get-AzBillingProfile -BillingAccountName 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="c1837-111">取得指定帳單帳戶下的所有帳單設定檔。</span><span class="sxs-lookup"><span data-stu-id="c1837-111">Get all billing profiles under the specified billing account.</span></span>

### <span data-ttu-id="c1837-112">範例2</span><span class="sxs-lookup"><span data-stu-id="c1837-112">Example 2</span></span>
```
PS C:\> Get-AzBillingProfile -BillingAccountName 00000000-0000-0000-0000-000000000000 -Name AAAA-0A00-AAA-ZZZ
```

<span data-ttu-id="c1837-113">取得指定名稱的帳單設定檔。</span><span class="sxs-lookup"><span data-stu-id="c1837-113">Get the billing profile with the specified name.</span></span>

### <span data-ttu-id="c1837-114">範例3</span><span class="sxs-lookup"><span data-stu-id="c1837-114">Example 3</span></span>
```
PS C:\> Get-AzBillingProfile -BillingAccountName 00000000-0000-0000-0000-000000000000 -ExpandInvoiceSection
```

<span data-ttu-id="c1837-115">取得指定帳單帳戶下的所有帳單設定檔，並在結果中包含發票區段。</span><span class="sxs-lookup"><span data-stu-id="c1837-115">Get all billing profiles under specified billing account, and include the invoice sections in the result.</span></span>

### <span data-ttu-id="c1837-116">範例4</span><span class="sxs-lookup"><span data-stu-id="c1837-116">Example 4</span></span>
```
PS C:\> Get-AzBillingProfile -BillingAccountName 00000000-0000-0000-0000-000000000000 -ExpandInvoiceSection -Name <System.Collections.Generic.List`1[System.String]>
```

<span data-ttu-id="c1837-117">取得具有指定名稱的帳單設定檔，並在結果中包含發票區段。</span><span class="sxs-lookup"><span data-stu-id="c1837-117">Get the billing profile with the specified name, and include the invoice sections in the result.</span></span>

## <span data-ttu-id="c1837-118">參數</span><span class="sxs-lookup"><span data-stu-id="c1837-118">PARAMETERS</span></span>

### <span data-ttu-id="c1837-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1837-119">-DefaultProfile</span></span>
<span data-ttu-id="c1837-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="c1837-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c1837-121">-BillingAccountName</span><span class="sxs-lookup"><span data-stu-id="c1837-121">-BillingAccountName</span></span>
<span data-ttu-id="c1837-122">特定帳單帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="c1837-122">Name of the specific billing account.</span></span>

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

### <span data-ttu-id="c1837-123">-ExpandInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="c1837-123">-ExpandInvoiceSection</span></span>
<span data-ttu-id="c1837-124">在 [帳單設定檔] 底下加入 [發票] 區段。</span><span class="sxs-lookup"><span data-stu-id="c1837-124">Include the invoices sections under billing profile.</span></span>

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

### <span data-ttu-id="c1837-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="c1837-125">-Name</span></span>
<span data-ttu-id="c1837-126">特定帳單設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="c1837-126">Name of a specific billing profile.</span></span>

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

### <span data-ttu-id="c1837-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1837-127">CommonParameters</span></span>
<span data-ttu-id="c1837-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c1837-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1837-129">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c1837-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1837-130">輸入</span><span class="sxs-lookup"><span data-stu-id="c1837-130">INPUTS</span></span>

### <span data-ttu-id="c1837-131">所有</span><span class="sxs-lookup"><span data-stu-id="c1837-131">None</span></span>

## <span data-ttu-id="c1837-132">輸出</span><span class="sxs-lookup"><span data-stu-id="c1837-132">OUTPUTS</span></span>

### <span data-ttu-id="c1837-133">PSBillingProfile 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c1837-133">Microsoft.Azure.Commands.Billing.Models.PSBillingProfile</span></span>

## <span data-ttu-id="c1837-134">筆記</span><span class="sxs-lookup"><span data-stu-id="c1837-134">NOTES</span></span>

## <span data-ttu-id="c1837-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="c1837-135">RELATED LINKS</span></span>
