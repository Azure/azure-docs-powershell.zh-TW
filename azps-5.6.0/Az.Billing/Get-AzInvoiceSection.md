---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/powershell/module/az.billing/get-azinvoicesection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzInvoiceSection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzInvoiceSection.md
ms.openlocfilehash: 6bf0b5a25772d430695737d70ff68cae5c5aa0d9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917421"
---
# <span data-ttu-id="0f55d-101">Get-AzInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="0f55d-101">Get-AzInvoiceSection</span></span>

## <span data-ttu-id="0f55d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0f55d-102">SYNOPSIS</span></span>
<span data-ttu-id="0f55d-103">取得發票區段。</span><span class="sxs-lookup"><span data-stu-id="0f55d-103">Get invoice sections.</span></span>

## <span data-ttu-id="0f55d-104">語法</span><span class="sxs-lookup"><span data-stu-id="0f55d-104">SYNTAX</span></span>

### <span data-ttu-id="0f55d-105">清單 (預設) </span><span class="sxs-lookup"><span data-stu-id="0f55d-105">List (Default)</span></span>
```
Get-AzInvoiceSection -BillingAccountName <String> -BillingProfileName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0f55d-106">單</span><span class="sxs-lookup"><span data-stu-id="0f55d-106">Single</span></span>
```
Get-AzInvoiceSection -BillingAccountName <String> -BillingProfileName <String> -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f55d-107">描述</span><span class="sxs-lookup"><span data-stu-id="0f55d-107">DESCRIPTION</span></span>
<span data-ttu-id="0f55d-108">**Get-AzInvoiceSection** Cmdlet 會取得指定帳單設定檔下的發票區段。</span><span class="sxs-lookup"><span data-stu-id="0f55d-108">The **Get-AzInvoiceSection** cmdlet gets invoice sections under the specified billing profile.</span></span> 

## <span data-ttu-id="0f55d-109">例子</span><span class="sxs-lookup"><span data-stu-id="0f55d-109">EXAMPLES</span></span>

### <span data-ttu-id="0f55d-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="0f55d-110">Example 1</span></span>
```
PS C:\> Get-AzInvoiceSection -BillingAccountName 00000000-0000-0000-0000-000000000000 -BillingProfileName AAAA-0A00-AAA-ZZZ
```

<span data-ttu-id="0f55d-111">取得指定帳單設定檔下的所有發票區段。</span><span class="sxs-lookup"><span data-stu-id="0f55d-111">Get all invoice sections under the specified billing profile.</span></span>

### <span data-ttu-id="0f55d-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="0f55d-112">Example 2</span></span>
```
PS C:\> Get-AzInvoiceSection -BillingAccountName 00000000-0000-0000-0000-000000000000 -BillingProfileName AAAA-0A00-AAA-ZZZ -Name BBBB-0A00-BBB-ZZZ
```

<span data-ttu-id="0f55d-113">取得具有指定名稱的發票區段。</span><span class="sxs-lookup"><span data-stu-id="0f55d-113">Get the invoice section with the specified name.</span></span>

## <span data-ttu-id="0f55d-114">參數</span><span class="sxs-lookup"><span data-stu-id="0f55d-114">PARAMETERS</span></span>

### <span data-ttu-id="0f55d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f55d-115">-DefaultProfile</span></span>
<span data-ttu-id="0f55d-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="0f55d-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0f55d-117">-BillingAccountName</span><span class="sxs-lookup"><span data-stu-id="0f55d-117">-BillingAccountName</span></span>
<span data-ttu-id="0f55d-118">特定帳單帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="0f55d-118">Name of the specific billing account.</span></span>

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

### <span data-ttu-id="0f55d-119">-BillingProfileName</span><span class="sxs-lookup"><span data-stu-id="0f55d-119">-BillingProfileName</span></span>
<span data-ttu-id="0f55d-120">特定帳單設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="0f55d-120">Name of the specific billing profile.</span></span>

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

### <span data-ttu-id="0f55d-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="0f55d-121">-Name</span></span>
<span data-ttu-id="0f55d-122">特定發票區段的名稱。</span><span class="sxs-lookup"><span data-stu-id="0f55d-122">Name of a specific invoice section.</span></span>

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

### <span data-ttu-id="0f55d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f55d-123">CommonParameters</span></span>
<span data-ttu-id="0f55d-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0f55d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f55d-125">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="0f55d-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f55d-126">輸入</span><span class="sxs-lookup"><span data-stu-id="0f55d-126">INPUTS</span></span>

### <span data-ttu-id="0f55d-127">沒有</span><span class="sxs-lookup"><span data-stu-id="0f55d-127">None</span></span>

## <span data-ttu-id="0f55d-128">輸出</span><span class="sxs-lookup"><span data-stu-id="0f55d-128">OUTPUTS</span></span>

### <span data-ttu-id="0f55d-129">Microsoft.Azure.Commands.Billing.models.PSInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="0f55d-129">Microsoft.Azure.Commands.Billing.Models.PSInvoiceSection</span></span>

## <span data-ttu-id="0f55d-130">筆記</span><span class="sxs-lookup"><span data-stu-id="0f55d-130">NOTES</span></span>

## <span data-ttu-id="0f55d-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="0f55d-131">RELATED LINKS</span></span>
