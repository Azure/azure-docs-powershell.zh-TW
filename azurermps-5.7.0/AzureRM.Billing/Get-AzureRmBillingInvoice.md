---
external help file: Microsoft.Azure.Commands.Billing.dll-Help.xml
Module Name: AzureRM.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.billing/get-azurermbillinginvoice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingInvoice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingInvoice.md
ms.openlocfilehash: 5a6ccf36f8e7aecdca4d6560614e9185a5ca26b7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446475"
---
# <span data-ttu-id="e6bee-101">Get-AzureRmBillingInvoice</span><span class="sxs-lookup"><span data-stu-id="e6bee-101">Get-AzureRmBillingInvoice</span></span>

## <span data-ttu-id="e6bee-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e6bee-102">SYNOPSIS</span></span>
<span data-ttu-id="e6bee-103">取得訂閱的帳單發票。</span><span class="sxs-lookup"><span data-stu-id="e6bee-103">Get billing invoices of the subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e6bee-104">句法</span><span class="sxs-lookup"><span data-stu-id="e6bee-104">SYNTAX</span></span>

### <span data-ttu-id="e6bee-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="e6bee-105">List (Default)</span></span>
```
Get-AzureRmBillingInvoice [-MaxCount <Int32>] [-GenerateDownloadUrl] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e6bee-106">最近</span><span class="sxs-lookup"><span data-stu-id="e6bee-106">Latest</span></span>
```
Get-AzureRmBillingInvoice [-Latest] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6bee-107">通過</span><span class="sxs-lookup"><span data-stu-id="e6bee-107">Single</span></span>
```
Get-AzureRmBillingInvoice -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6bee-108">說明</span><span class="sxs-lookup"><span data-stu-id="e6bee-108">DESCRIPTION</span></span>
<span data-ttu-id="e6bee-109">**AzureRmBillingInvoice** Cmdlet 會取得訂閱的帳單發票。</span><span class="sxs-lookup"><span data-stu-id="e6bee-109">The **Get-AzureRmBillingInvoice** cmdlet gets billing invoices of the subscription.</span></span> 

## <span data-ttu-id="e6bee-110">示例</span><span class="sxs-lookup"><span data-stu-id="e6bee-110">EXAMPLES</span></span>

### <span data-ttu-id="e6bee-111">範例1</span><span class="sxs-lookup"><span data-stu-id="e6bee-111">Example 1</span></span>
```
PS C:\> Get-AzureRmBillingInvoice -Latest
```

<span data-ttu-id="e6bee-112">取得最新的訂閱發票。</span><span class="sxs-lookup"><span data-stu-id="e6bee-112">Get the latest invoice of the subscription.</span></span>

### <span data-ttu-id="e6bee-113">範例2</span><span class="sxs-lookup"><span data-stu-id="e6bee-113">Example 2</span></span>
```
PS C:\> Get-AzureRmBillingInvoice -Name 2017-02-18-432543543
```

<span data-ttu-id="e6bee-114">取得具有指定名稱的訂閱發票。</span><span class="sxs-lookup"><span data-stu-id="e6bee-114">Get the invoice of the subscription with the specified name.</span></span>

### <span data-ttu-id="e6bee-115">範例3</span><span class="sxs-lookup"><span data-stu-id="e6bee-115">Example 3</span></span>
```
PS C:\> Get-AzureRmBillingInvoice
```

<span data-ttu-id="e6bee-116">從最新發票（不含下載 Url）開始，以逆序的時間順序取得訂閱的所有可用發票。</span><span class="sxs-lookup"><span data-stu-id="e6bee-116">Get all available invoices of the subscription in reverse chronological order beginning with the most recent invoice without download Url.</span></span> 

### <span data-ttu-id="e6bee-117">範例4</span><span class="sxs-lookup"><span data-stu-id="e6bee-117">Example 4</span></span>
```
PS C:\> Get-AzureRmBillingInvoice -GenerateDownloadUrl -MaxCount 10
```

<span data-ttu-id="e6bee-118">取得最新的訂閱10張發票，並在結果中包含下載 Url。</span><span class="sxs-lookup"><span data-stu-id="e6bee-118">Get most recent 10 invoices of the subscription and include the download Url in the result.</span></span>

## <span data-ttu-id="e6bee-119">參數</span><span class="sxs-lookup"><span data-stu-id="e6bee-119">PARAMETERS</span></span>

### <span data-ttu-id="e6bee-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6bee-120">-DefaultProfile</span></span>
<span data-ttu-id="e6bee-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="e6bee-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e6bee-122">-GenerateDownloadUrl</span><span class="sxs-lookup"><span data-stu-id="e6bee-122">-GenerateDownloadUrl</span></span>
<span data-ttu-id="e6bee-123">產生發票的下載 url。</span><span class="sxs-lookup"><span data-stu-id="e6bee-123">Generate the download url of the invoices.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6bee-124">-最新</span><span class="sxs-lookup"><span data-stu-id="e6bee-124">-Latest</span></span>
<span data-ttu-id="e6bee-125">取得最新的發票。</span><span class="sxs-lookup"><span data-stu-id="e6bee-125">Get the latest invoice.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Latest
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6bee-126">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="e6bee-126">-MaxCount</span></span>
<span data-ttu-id="e6bee-127">決定要傳回的記錄數目上限。</span><span class="sxs-lookup"><span data-stu-id="e6bee-127">Determines the maximum number of records to return.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6bee-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="e6bee-128">-Name</span></span>
<span data-ttu-id="e6bee-129">要取得或最近未指定之特定發票的名稱。</span><span class="sxs-lookup"><span data-stu-id="e6bee-129">Name of a specific invoice to get or the most recent if not specified.</span></span>

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

### <span data-ttu-id="e6bee-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6bee-130">CommonParameters</span></span>
<span data-ttu-id="e6bee-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e6bee-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6bee-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e6bee-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6bee-133">輸入</span><span class="sxs-lookup"><span data-stu-id="e6bee-133">INPUTS</span></span>

### <span data-ttu-id="e6bee-134">所有</span><span class="sxs-lookup"><span data-stu-id="e6bee-134">None</span></span>

## <span data-ttu-id="e6bee-135">輸出</span><span class="sxs-lookup"><span data-stu-id="e6bee-135">OUTPUTS</span></span>

### <span data-ttu-id="e6bee-136">[System.object]。清單 ' 1 [Microsoft..... 帳單、0.14.0.0 =、Culture = 中性、PublicKeyToken = null]」（）</span><span class="sxs-lookup"><span data-stu-id="e6bee-136">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Billing.Models.Invoice, Microsoft.Azure.Commands.Billing, Version=0.14.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="e6bee-137">[Microsoft Azure. 帳單. 發票]</span><span class="sxs-lookup"><span data-stu-id="e6bee-137">Microsoft.Azure.Management.Billing.Models.Invoice</span></span>

## <span data-ttu-id="e6bee-138">筆記</span><span class="sxs-lookup"><span data-stu-id="e6bee-138">NOTES</span></span>

## <span data-ttu-id="e6bee-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="e6bee-139">RELATED LINKS</span></span>

