---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azinvoicesection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzInvoiceSection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzInvoiceSection.md
ms.openlocfilehash: ccb686ab0aeb373a542e958aab7b90489fc36f63
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100130010"
---
# <span data-ttu-id="8b861-101">Get-AzInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="8b861-101">Get-AzInvoiceSection</span></span>

## <span data-ttu-id="8b861-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8b861-102">SYNOPSIS</span></span>
<span data-ttu-id="8b861-103">取得發票區段。</span><span class="sxs-lookup"><span data-stu-id="8b861-103">Get invoice sections.</span></span>

## <span data-ttu-id="8b861-104">句法</span><span class="sxs-lookup"><span data-stu-id="8b861-104">SYNTAX</span></span>

### <span data-ttu-id="8b861-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="8b861-105">List (Default)</span></span>
```
Get-AzInvoiceSection -BillingAccountName <String> -BillingProfileName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8b861-106">通過</span><span class="sxs-lookup"><span data-stu-id="8b861-106">Single</span></span>
```
Get-AzInvoiceSection -BillingAccountName <String> -BillingProfileName <String> -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b861-107">說明</span><span class="sxs-lookup"><span data-stu-id="8b861-107">DESCRIPTION</span></span>
<span data-ttu-id="8b861-108">**AzInvoiceSection** Cmdlet 會在指定的帳單設定檔下取得發票區段。</span><span class="sxs-lookup"><span data-stu-id="8b861-108">The **Get-AzInvoiceSection** cmdlet gets invoice sections under the specified billing profile.</span></span> 

## <span data-ttu-id="8b861-109">示例</span><span class="sxs-lookup"><span data-stu-id="8b861-109">EXAMPLES</span></span>

### <span data-ttu-id="8b861-110">範例1</span><span class="sxs-lookup"><span data-stu-id="8b861-110">Example 1</span></span>
```
PS C:\> Get-AzInvoiceSection -BillingAccountName 00000000-0000-0000-0000-000000000000 -BillingProfileName AAAA-0A00-AAA-ZZZ
```

<span data-ttu-id="8b861-111">取得指定帳單設定檔的所有發票區段。</span><span class="sxs-lookup"><span data-stu-id="8b861-111">Get all invoice sections under the specified billing profile.</span></span>

### <span data-ttu-id="8b861-112">範例2</span><span class="sxs-lookup"><span data-stu-id="8b861-112">Example 2</span></span>
```
PS C:\> Get-AzInvoiceSection -BillingAccountName 00000000-0000-0000-0000-000000000000 -BillingProfileName AAAA-0A00-AAA-ZZZ -Name BBBB-0A00-BBB-ZZZ
```

<span data-ttu-id="8b861-113">取得具有指定名稱的 [發票] 區段。</span><span class="sxs-lookup"><span data-stu-id="8b861-113">Get the invoice section with the specified name.</span></span>

## <span data-ttu-id="8b861-114">參數</span><span class="sxs-lookup"><span data-stu-id="8b861-114">PARAMETERS</span></span>

### <span data-ttu-id="8b861-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b861-115">-DefaultProfile</span></span>
<span data-ttu-id="8b861-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="8b861-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8b861-117">-BillingAccountName</span><span class="sxs-lookup"><span data-stu-id="8b861-117">-BillingAccountName</span></span>
<span data-ttu-id="8b861-118">特定帳單帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="8b861-118">Name of the specific billing account.</span></span>

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

### <span data-ttu-id="8b861-119">-BillingProfileName</span><span class="sxs-lookup"><span data-stu-id="8b861-119">-BillingProfileName</span></span>
<span data-ttu-id="8b861-120">特定帳單設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="8b861-120">Name of the specific billing profile.</span></span>

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

### <span data-ttu-id="8b861-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="8b861-121">-Name</span></span>
<span data-ttu-id="8b861-122">特定發票區段的名稱。</span><span class="sxs-lookup"><span data-stu-id="8b861-122">Name of a specific invoice section.</span></span>

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

### <span data-ttu-id="8b861-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b861-123">CommonParameters</span></span>
<span data-ttu-id="8b861-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8b861-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b861-125">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8b861-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b861-126">輸入</span><span class="sxs-lookup"><span data-stu-id="8b861-126">INPUTS</span></span>

### <span data-ttu-id="8b861-127">所有</span><span class="sxs-lookup"><span data-stu-id="8b861-127">None</span></span>

## <span data-ttu-id="8b861-128">輸出</span><span class="sxs-lookup"><span data-stu-id="8b861-128">OUTPUTS</span></span>

### <span data-ttu-id="8b861-129">PSInvoiceSection 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="8b861-129">Microsoft.Azure.Commands.Billing.Models.PSInvoiceSection</span></span>

## <span data-ttu-id="8b861-130">筆記</span><span class="sxs-lookup"><span data-stu-id="8b861-130">NOTES</span></span>

## <span data-ttu-id="8b861-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="8b861-131">RELATED LINKS</span></span>
