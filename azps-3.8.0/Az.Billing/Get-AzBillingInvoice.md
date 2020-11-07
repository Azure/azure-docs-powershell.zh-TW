---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azbillinginvoice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingInvoice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingInvoice.md
ms.openlocfilehash: 2b1906d07b3e08b1761469b4a9d6d8d565e0fd8c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958382"
---
# <span data-ttu-id="c379c-101">Get-AzBillingInvoice</span><span class="sxs-lookup"><span data-stu-id="c379c-101">Get-AzBillingInvoice</span></span>

## <span data-ttu-id="c379c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c379c-102">SYNOPSIS</span></span>
<span data-ttu-id="c379c-103">取得訂閱的帳單發票。</span><span class="sxs-lookup"><span data-stu-id="c379c-103">Get billing invoices of the subscription.</span></span>

## <span data-ttu-id="c379c-104">句法</span><span class="sxs-lookup"><span data-stu-id="c379c-104">SYNTAX</span></span>

### <span data-ttu-id="c379c-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="c379c-105">List (Default)</span></span>
```
Get-AzBillingInvoice [-MaxCount <Int32>] [-GenerateDownloadUrl] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c379c-106">最近</span><span class="sxs-lookup"><span data-stu-id="c379c-106">Latest</span></span>
```
Get-AzBillingInvoice [-Latest] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c379c-107">通過</span><span class="sxs-lookup"><span data-stu-id="c379c-107">Single</span></span>
```
Get-AzBillingInvoice -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c379c-108">說明</span><span class="sxs-lookup"><span data-stu-id="c379c-108">DESCRIPTION</span></span>
<span data-ttu-id="c379c-109">**AzBillingInvoice** Cmdlet 會取得訂閱的帳單發票。</span><span class="sxs-lookup"><span data-stu-id="c379c-109">The **Get-AzBillingInvoice** cmdlet gets billing invoices of the subscription.</span></span> 

## <span data-ttu-id="c379c-110">示例</span><span class="sxs-lookup"><span data-stu-id="c379c-110">EXAMPLES</span></span>

### <span data-ttu-id="c379c-111">範例1</span><span class="sxs-lookup"><span data-stu-id="c379c-111">Example 1</span></span>
```
PS C:\> Get-AzBillingInvoice -Latest
```

<span data-ttu-id="c379c-112">取得最新的訂閱發票。</span><span class="sxs-lookup"><span data-stu-id="c379c-112">Get the latest invoice of the subscription.</span></span>

### <span data-ttu-id="c379c-113">範例2</span><span class="sxs-lookup"><span data-stu-id="c379c-113">Example 2</span></span>
```
PS C:\> Get-AzBillingInvoice -Name 2017-02-18-432543543
```

<span data-ttu-id="c379c-114">取得具有指定名稱的訂閱發票。</span><span class="sxs-lookup"><span data-stu-id="c379c-114">Get the invoice of the subscription with the specified name.</span></span>

### <span data-ttu-id="c379c-115">範例3</span><span class="sxs-lookup"><span data-stu-id="c379c-115">Example 3</span></span>
```
PS C:\> Get-AzBillingInvoice
```

<span data-ttu-id="c379c-116">從最新發票（不含下載 Url）開始，以逆序的時間順序取得訂閱的所有可用發票。</span><span class="sxs-lookup"><span data-stu-id="c379c-116">Get all available invoices of the subscription in reverse chronological order beginning with the most recent invoice without download Url.</span></span> 

### <span data-ttu-id="c379c-117">範例4</span><span class="sxs-lookup"><span data-stu-id="c379c-117">Example 4</span></span>
```
PS C:\> Get-AzBillingInvoice -GenerateDownloadUrl -MaxCount 10
```

<span data-ttu-id="c379c-118">取得最新的訂閱10張發票，並在結果中包含下載 Url。</span><span class="sxs-lookup"><span data-stu-id="c379c-118">Get most recent 10 invoices of the subscription and include the download Url in the result.</span></span>

## <span data-ttu-id="c379c-119">參數</span><span class="sxs-lookup"><span data-stu-id="c379c-119">PARAMETERS</span></span>

### <span data-ttu-id="c379c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c379c-120">-DefaultProfile</span></span>
<span data-ttu-id="c379c-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="c379c-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c379c-122">-GenerateDownloadUrl</span><span class="sxs-lookup"><span data-stu-id="c379c-122">-GenerateDownloadUrl</span></span>
<span data-ttu-id="c379c-123">產生發票的下載 url。</span><span class="sxs-lookup"><span data-stu-id="c379c-123">Generate the download url of the invoices.</span></span>

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

### <span data-ttu-id="c379c-124">-最新</span><span class="sxs-lookup"><span data-stu-id="c379c-124">-Latest</span></span>
<span data-ttu-id="c379c-125">取得最新的發票。</span><span class="sxs-lookup"><span data-stu-id="c379c-125">Get the latest invoice.</span></span>

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

### <span data-ttu-id="c379c-126">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="c379c-126">-MaxCount</span></span>
<span data-ttu-id="c379c-127">決定要傳回的記錄數目上限。</span><span class="sxs-lookup"><span data-stu-id="c379c-127">Determines the maximum number of records to return.</span></span>

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

### <span data-ttu-id="c379c-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="c379c-128">-Name</span></span>
<span data-ttu-id="c379c-129">要取得或最近未指定之特定發票的名稱。</span><span class="sxs-lookup"><span data-stu-id="c379c-129">Name of a specific invoice to get or the most recent if not specified.</span></span>

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

### <span data-ttu-id="c379c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c379c-130">CommonParameters</span></span>
<span data-ttu-id="c379c-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c379c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c379c-132">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c379c-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c379c-133">輸入</span><span class="sxs-lookup"><span data-stu-id="c379c-133">INPUTS</span></span>

### <span data-ttu-id="c379c-134">所有</span><span class="sxs-lookup"><span data-stu-id="c379c-134">None</span></span>

## <span data-ttu-id="c379c-135">輸出</span><span class="sxs-lookup"><span data-stu-id="c379c-135">OUTPUTS</span></span>

### <span data-ttu-id="c379c-136">PSInvoice 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c379c-136">Microsoft.Azure.Commands.Billing.Models.PSInvoice</span></span>

## <span data-ttu-id="c379c-137">筆記</span><span class="sxs-lookup"><span data-stu-id="c379c-137">NOTES</span></span>

## <span data-ttu-id="c379c-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="c379c-138">RELATED LINKS</span></span>
