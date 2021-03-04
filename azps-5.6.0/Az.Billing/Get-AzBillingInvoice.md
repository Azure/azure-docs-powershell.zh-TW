---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/powershell/module/az.billing/get-azbillinginvoice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingInvoice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingInvoice.md
ms.openlocfilehash: 604109a80171ff4bb294dc1643081cd8e933d728
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903861"
---
# <span data-ttu-id="eb7d0-101">Get-AzBillingInvoice</span><span class="sxs-lookup"><span data-stu-id="eb7d0-101">Get-AzBillingInvoice</span></span>

## <span data-ttu-id="eb7d0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="eb7d0-102">SYNOPSIS</span></span>
<span data-ttu-id="eb7d0-103">取得訂閱的帳單發票。</span><span class="sxs-lookup"><span data-stu-id="eb7d0-103">Get billing invoices of the subscription.</span></span>
<span data-ttu-id="eb7d0-104">取得帳單帳戶和帳單設定檔的帳單發票</span><span class="sxs-lookup"><span data-stu-id="eb7d0-104">Get billing invoices of a billing account and billing profile</span></span>

## <span data-ttu-id="eb7d0-105">語法</span><span class="sxs-lookup"><span data-stu-id="eb7d0-105">SYNTAX</span></span>

### <span data-ttu-id="eb7d0-106">清單 (預設) </span><span class="sxs-lookup"><span data-stu-id="eb7d0-106">List (Default)</span></span>
```
Get-AzBillingInvoice [-MaxCount <Int32>] [-GenerateDownloadUrl] [-DefaultProfile <IAzureContextContainer>] [-BillingAccountName] [-BillingProfileName]
 [<CommonParameters>]
```

### <span data-ttu-id="eb7d0-107">最新</span><span class="sxs-lookup"><span data-stu-id="eb7d0-107">Latest</span></span>
```
Get-AzBillingInvoice [-Latest] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>] [-BillingAccountName] [-BillingProfileName]
```

### <span data-ttu-id="eb7d0-108">單</span><span class="sxs-lookup"><span data-stu-id="eb7d0-108">Single</span></span>
```
Get-AzBillingInvoice -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb7d0-109">描述</span><span class="sxs-lookup"><span data-stu-id="eb7d0-109">DESCRIPTION</span></span>
<span data-ttu-id="eb7d0-110">**Get-AzBillingInvoice Cmdlet** 會取得訂閱的帳單發票。</span><span class="sxs-lookup"><span data-stu-id="eb7d0-110">The **Get-AzBillingInvoice** cmdlet gets billing invoices of the subscription.</span></span> 

## <span data-ttu-id="eb7d0-111">例子</span><span class="sxs-lookup"><span data-stu-id="eb7d0-111">EXAMPLES</span></span>

### <span data-ttu-id="eb7d0-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="eb7d0-112">Example 1</span></span>
```
PS C:\> Get-AzBillingInvoice -Latest
```

<span data-ttu-id="eb7d0-113">取得訂閱的最新發票。</span><span class="sxs-lookup"><span data-stu-id="eb7d0-113">Get the latest invoice of the subscription.</span></span>

### <span data-ttu-id="eb7d0-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="eb7d0-114">Example 2</span></span>
```
PS C:\> Get-AzBillingInvoice -Name 2017-02-18-432543543
```

<span data-ttu-id="eb7d0-115">取得具有指定名稱之訂閱的發票。</span><span class="sxs-lookup"><span data-stu-id="eb7d0-115">Get the invoice of the subscription with the specified name.</span></span>

### <span data-ttu-id="eb7d0-116">範例 3</span><span class="sxs-lookup"><span data-stu-id="eb7d0-116">Example 3</span></span>
```
PS C:\> Get-AzBillingInvoice
```

<span data-ttu-id="eb7d0-117">以反時間順序取得訂閱的所有可用發票，從最新的發票開始，但不下載 URL。</span><span class="sxs-lookup"><span data-stu-id="eb7d0-117">Get all available invoices of the subscription in reverse chronological order beginning with the most recent invoice without download Url.</span></span> 

### <span data-ttu-id="eb7d0-118">範例 4</span><span class="sxs-lookup"><span data-stu-id="eb7d0-118">Example 4</span></span>
```
PS C:\> Get-AzBillingInvoice -GenerateDownloadUrl -MaxCount 10
```

<span data-ttu-id="eb7d0-119">取得訂閱的最新 10 張發票，並包含結果中的下載 URL。</span><span class="sxs-lookup"><span data-stu-id="eb7d0-119">Get most recent 10 invoices of the subscription and include the download Url in the result.</span></span>

### <span data-ttu-id="eb7d0-120">範例 5</span><span class="sxs-lookup"><span data-stu-id="eb7d0-120">Example 5</span></span>
```
PS C:\> Get-AzBillingInvoice -Name 2017-02-18-432543543 -GenerateDownloadUrl
```

<span data-ttu-id="eb7d0-121">根據名稱取得特定的發票，並包含結果中的下載 URL。</span><span class="sxs-lookup"><span data-stu-id="eb7d0-121">Get the specific invoice by name and include download url in the result.</span></span>

### <span data-ttu-id="eb7d0-122">範例 6</span><span class="sxs-lookup"><span data-stu-id="eb7d0-122">Example 6</span></span>
```
PS C:\> Get-AzBillingInvoice -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -GenerateDownloadUrl
```

<span data-ttu-id="eb7d0-123">根據帳單帳戶名稱取得發票，並包含結果中每個發票的下載 URL。</span><span class="sxs-lookup"><span data-stu-id="eb7d0-123">Get invoices by billing account name and include download url for each invoice in the result.</span></span>

### <span data-ttu-id="eb7d0-124">範例 7</span><span class="sxs-lookup"><span data-stu-id="eb7d0-124">Example 7</span></span>
```
PS C:\> Get-AzBillingInvoice -Name 0000000000 -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -GenerateDownloadUrl
```

<span data-ttu-id="eb7d0-125">根據發票名稱和帳單帳戶名稱取得特定的發票，並包含結果中每個發票的下載 URL。</span><span class="sxs-lookup"><span data-stu-id="eb7d0-125">Get specific invoice by invoice name and billing account name and include download url for each invoice in the result.</span></span>

### <span data-ttu-id="eb7d0-126">範例 8</span><span class="sxs-lookup"><span data-stu-id="eb7d0-126">Example 8</span></span>
```
PS C:\> Get-AzBillingInvoice -Latest -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -GenerateDownloadUrl
```

<span data-ttu-id="eb7d0-127">根據帳單帳戶名稱取得最新的發票，並包含發票的下載 URL。</span><span class="sxs-lookup"><span data-stu-id="eb7d0-127">Get latest invoice by billing account name and include download url for invoice in the result.</span></span>

### <span data-ttu-id="eb7d0-128">範例 9</span><span class="sxs-lookup"><span data-stu-id="eb7d0-128">Example 9</span></span>
```
PS C:\> Get-AzBillingInvoice -GenerateDownloadUrl -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -BillingProfileName 0000-0000-000-000 -MaxCount 10
```

<span data-ttu-id="eb7d0-129">取得特定帳單帳戶和特定帳單設定檔的最近 10 張發票，並納入結果中的下載 URL。</span><span class="sxs-lookup"><span data-stu-id="eb7d0-129">Get most recent 10 invoices of the specific billing account and specific billing profile and include the download Url in the result.</span></span>

### <span data-ttu-id="eb7d0-130">範例 10</span><span class="sxs-lookup"><span data-stu-id="eb7d0-130">Example 10</span></span>
```
PS C:\> Get-AzBillingInvoice -Latest -GenerateDownloadUrl -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -BillingProfileName 0000-0000-000-000 
```

<span data-ttu-id="eb7d0-131">根據帳單帳戶名稱和帳單設定檔名稱取得最新的發票，並包含結果中的發票下載 URL。</span><span class="sxs-lookup"><span data-stu-id="eb7d0-131">Get latest invoice by billing account name and billing profile name and include download url for invoice in the result.</span></span>

### <span data-ttu-id="eb7d0-132">範例 10</span><span class="sxs-lookup"><span data-stu-id="eb7d0-132">Example 10</span></span>
```
PS C:\> Get-AzBillingInvoice -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -BillingProfileName 0000-0000-000-000 -PeriodStartDate 0000-00-00 -PeriodEndDate 0000-00-00
```

<span data-ttu-id="eb7d0-133">根據計費帳戶名稱和計費設定檔名稱取得由 perioStart 日期及 periodEnd 日期指定的計費期間之發票。</span><span class="sxs-lookup"><span data-stu-id="eb7d0-133">Get invoices by billing account name and billing profile name for a billing period specified by perioStart date and periodEnd date.</span></span>


## <span data-ttu-id="eb7d0-134">參數</span><span class="sxs-lookup"><span data-stu-id="eb7d0-134">PARAMETERS</span></span>

### <span data-ttu-id="eb7d0-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb7d0-135">-DefaultProfile</span></span>
<span data-ttu-id="eb7d0-136">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="eb7d0-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eb7d0-137">-GenerateDownloadUrl</span><span class="sxs-lookup"><span data-stu-id="eb7d0-137">-GenerateDownloadUrl</span></span>
<span data-ttu-id="eb7d0-138">產生發票的下載 URL。</span><span class="sxs-lookup"><span data-stu-id="eb7d0-138">Generate the download url of the invoices.</span></span>

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

### <span data-ttu-id="eb7d0-139">-最新</span><span class="sxs-lookup"><span data-stu-id="eb7d0-139">-Latest</span></span>
<span data-ttu-id="eb7d0-140">取得最新的發票。</span><span class="sxs-lookup"><span data-stu-id="eb7d0-140">Get the latest invoice.</span></span>

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

### <span data-ttu-id="eb7d0-141">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="eb7d0-141">-MaxCount</span></span>
<span data-ttu-id="eb7d0-142">決定要退回的記錄數目上限。</span><span class="sxs-lookup"><span data-stu-id="eb7d0-142">Determines the maximum number of records to return.</span></span>

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

### <span data-ttu-id="eb7d0-143">-名稱</span><span class="sxs-lookup"><span data-stu-id="eb7d0-143">-Name</span></span>
<span data-ttu-id="eb7d0-144">要取得的特定發票名稱，或最新的發票名稱 ，如果未指定。</span><span class="sxs-lookup"><span data-stu-id="eb7d0-144">Name of a specific invoice to get or the most recent if not specified.</span></span>

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

### <span data-ttu-id="eb7d0-145">-BillingAccountName</span><span class="sxs-lookup"><span data-stu-id="eb7d0-145">-BillingAccountName</span></span>
<span data-ttu-id="eb7d0-146">取得發票的特定帳單帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="eb7d0-146">Name of a specific billing account to get invoices for.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb7d0-147">-BillingProfileName</span><span class="sxs-lookup"><span data-stu-id="eb7d0-147">-BillingProfileName</span></span>
<span data-ttu-id="eb7d0-148">取得發票的特定帳單設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="eb7d0-148">Name of a specific billing profile to get invoices for.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb7d0-149">-期間啟動日期</span><span class="sxs-lookup"><span data-stu-id="eb7d0-149">-PeriodStartDate</span></span>
<span data-ttu-id="eb7d0-150">發票的開始日期。</span><span class="sxs-lookup"><span data-stu-id="eb7d0-150">Start date for invoice.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb7d0-151">-PeriodEndDate</span><span class="sxs-lookup"><span data-stu-id="eb7d0-151">-PeriodEndDate</span></span>
<span data-ttu-id="eb7d0-152">發票的結束日期。</span><span class="sxs-lookup"><span data-stu-id="eb7d0-152">End date for invoice.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```



### <span data-ttu-id="eb7d0-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb7d0-153">CommonParameters</span></span>
<span data-ttu-id="eb7d0-154">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="eb7d0-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb7d0-155">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="eb7d0-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb7d0-156">輸入</span><span class="sxs-lookup"><span data-stu-id="eb7d0-156">INPUTS</span></span>

### <span data-ttu-id="eb7d0-157">沒有</span><span class="sxs-lookup"><span data-stu-id="eb7d0-157">None</span></span>

## <span data-ttu-id="eb7d0-158">輸出</span><span class="sxs-lookup"><span data-stu-id="eb7d0-158">OUTPUTS</span></span>

### <span data-ttu-id="eb7d0-159">Microsoft.Azure.Commands.Billing.models.PSInvoice</span><span class="sxs-lookup"><span data-stu-id="eb7d0-159">Microsoft.Azure.Commands.Billing.Models.PSInvoice</span></span>

## <span data-ttu-id="eb7d0-160">筆記</span><span class="sxs-lookup"><span data-stu-id="eb7d0-160">NOTES</span></span>

## <span data-ttu-id="eb7d0-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="eb7d0-161">RELATED LINKS</span></span>
