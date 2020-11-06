---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azbillinginvoice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingInvoice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingInvoice.md
ms.openlocfilehash: 8c5e107de50d5e1df1f0c9da7305dbe801857410
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613618"
---
# <span data-ttu-id="07d32-101">Get-AzBillingInvoice</span><span class="sxs-lookup"><span data-stu-id="07d32-101">Get-AzBillingInvoice</span></span>

## <span data-ttu-id="07d32-102">摘要</span><span class="sxs-lookup"><span data-stu-id="07d32-102">SYNOPSIS</span></span>
<span data-ttu-id="07d32-103">取得訂閱的帳單發票。</span><span class="sxs-lookup"><span data-stu-id="07d32-103">Get billing invoices of the subscription.</span></span>

## <span data-ttu-id="07d32-104">句法</span><span class="sxs-lookup"><span data-stu-id="07d32-104">SYNTAX</span></span>

### <span data-ttu-id="07d32-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="07d32-105">List (Default)</span></span>
```
Get-AzBillingInvoice [-MaxCount <Int32>] [-GenerateDownloadUrl] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="07d32-106">最近</span><span class="sxs-lookup"><span data-stu-id="07d32-106">Latest</span></span>
```
Get-AzBillingInvoice [-Latest] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07d32-107">通過</span><span class="sxs-lookup"><span data-stu-id="07d32-107">Single</span></span>
```
Get-AzBillingInvoice -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07d32-108">說明</span><span class="sxs-lookup"><span data-stu-id="07d32-108">DESCRIPTION</span></span>
<span data-ttu-id="07d32-109">**AzBillingInvoice** Cmdlet 會取得訂閱的帳單發票。</span><span class="sxs-lookup"><span data-stu-id="07d32-109">The **Get-AzBillingInvoice** cmdlet gets billing invoices of the subscription.</span></span> 

## <span data-ttu-id="07d32-110">示例</span><span class="sxs-lookup"><span data-stu-id="07d32-110">EXAMPLES</span></span>

### <span data-ttu-id="07d32-111">範例1</span><span class="sxs-lookup"><span data-stu-id="07d32-111">Example 1</span></span>
```
PS C:\> Get-AzBillingInvoice -Latest
```

<span data-ttu-id="07d32-112">取得最新的訂閱發票。</span><span class="sxs-lookup"><span data-stu-id="07d32-112">Get the latest invoice of the subscription.</span></span>

### <span data-ttu-id="07d32-113">範例2</span><span class="sxs-lookup"><span data-stu-id="07d32-113">Example 2</span></span>
```
PS C:\> Get-AzBillingInvoice -Name 2017-02-18-432543543
```

<span data-ttu-id="07d32-114">取得具有指定名稱的訂閱發票。</span><span class="sxs-lookup"><span data-stu-id="07d32-114">Get the invoice of the subscription with the specified name.</span></span>

### <span data-ttu-id="07d32-115">範例3</span><span class="sxs-lookup"><span data-stu-id="07d32-115">Example 3</span></span>
```
PS C:\> Get-AzBillingInvoice
```

<span data-ttu-id="07d32-116">從最新發票（不含下載 Url）開始，以逆序的時間順序取得訂閱的所有可用發票。</span><span class="sxs-lookup"><span data-stu-id="07d32-116">Get all available invoices of the subscription in reverse chronological order beginning with the most recent invoice without download Url.</span></span> 

### <span data-ttu-id="07d32-117">範例4</span><span class="sxs-lookup"><span data-stu-id="07d32-117">Example 4</span></span>
```
PS C:\> Get-AzBillingInvoice -GenerateDownloadUrl -MaxCount 10
```

<span data-ttu-id="07d32-118">取得最新的訂閱10張發票，並在結果中包含下載 Url。</span><span class="sxs-lookup"><span data-stu-id="07d32-118">Get most recent 10 invoices of the subscription and include the download Url in the result.</span></span>

## <span data-ttu-id="07d32-119">參數</span><span class="sxs-lookup"><span data-stu-id="07d32-119">PARAMETERS</span></span>

### <span data-ttu-id="07d32-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07d32-120">-DefaultProfile</span></span>
<span data-ttu-id="07d32-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="07d32-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="07d32-122">-GenerateDownloadUrl</span><span class="sxs-lookup"><span data-stu-id="07d32-122">-GenerateDownloadUrl</span></span>
<span data-ttu-id="07d32-123">產生發票的下載 url。</span><span class="sxs-lookup"><span data-stu-id="07d32-123">Generate the download url of the invoices.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07d32-124">-最新</span><span class="sxs-lookup"><span data-stu-id="07d32-124">-Latest</span></span>
<span data-ttu-id="07d32-125">取得最新的發票。</span><span class="sxs-lookup"><span data-stu-id="07d32-125">Get the latest invoice.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Latest
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07d32-126">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="07d32-126">-MaxCount</span></span>
<span data-ttu-id="07d32-127">決定要傳回的記錄數目上限。</span><span class="sxs-lookup"><span data-stu-id="07d32-127">Determines the maximum number of records to return.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07d32-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="07d32-128">-Name</span></span>
<span data-ttu-id="07d32-129">要取得或最近未指定之特定發票的名稱。</span><span class="sxs-lookup"><span data-stu-id="07d32-129">Name of a specific invoice to get or the most recent if not specified.</span></span>

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

### <span data-ttu-id="07d32-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07d32-130">CommonParameters</span></span>
<span data-ttu-id="07d32-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="07d32-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07d32-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="07d32-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07d32-133">輸入</span><span class="sxs-lookup"><span data-stu-id="07d32-133">INPUTS</span></span>

### <span data-ttu-id="07d32-134">所有</span><span class="sxs-lookup"><span data-stu-id="07d32-134">None</span></span>

## <span data-ttu-id="07d32-135">輸出</span><span class="sxs-lookup"><span data-stu-id="07d32-135">OUTPUTS</span></span>

### <span data-ttu-id="07d32-136">PSInvoice 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="07d32-136">Microsoft.Azure.Commands.Billing.Models.PSInvoice</span></span>

## <span data-ttu-id="07d32-137">筆記</span><span class="sxs-lookup"><span data-stu-id="07d32-137">NOTES</span></span>

## <span data-ttu-id="07d32-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="07d32-138">RELATED LINKS</span></span>
