---
external help file: Microsoft.Azure.Commands.Billing.dll-Help.xml
Module Name: AzureRM.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.billing/get-azurermbillingperiod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingPeriod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingPeriod.md
ms.openlocfilehash: 7d3c09385c76fef525535384459d03b0cc65dd9c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455531"
---
# <span data-ttu-id="71ac6-101">Get-AzureRmBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="71ac6-101">Get-AzureRmBillingPeriod</span></span>

## <span data-ttu-id="71ac6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="71ac6-102">SYNOPSIS</span></span>
<span data-ttu-id="71ac6-103">取得訂閱的計費期間。</span><span class="sxs-lookup"><span data-stu-id="71ac6-103">Get billing periods of the subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71ac6-104">句法</span><span class="sxs-lookup"><span data-stu-id="71ac6-104">SYNTAX</span></span>

### <span data-ttu-id="71ac6-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="71ac6-105">List (Default)</span></span>
```
Get-AzureRmBillingPeriod [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71ac6-106">通過</span><span class="sxs-lookup"><span data-stu-id="71ac6-106">Single</span></span>
```
Get-AzureRmBillingPeriod -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71ac6-107">說明</span><span class="sxs-lookup"><span data-stu-id="71ac6-107">DESCRIPTION</span></span>
<span data-ttu-id="71ac6-108">**AzureRmBillingPeriod** Cmdlet 會取得訂閱的計費期間。</span><span class="sxs-lookup"><span data-stu-id="71ac6-108">The **Get-AzureRmBillingPeriod** cmdlet gets billing periods of the subscription.</span></span>

## <span data-ttu-id="71ac6-109">示例</span><span class="sxs-lookup"><span data-stu-id="71ac6-109">EXAMPLES</span></span>

### <span data-ttu-id="71ac6-110">範例1</span><span class="sxs-lookup"><span data-stu-id="71ac6-110">Example 1</span></span>
```
PS C:\> Get-AzureRmBillingPeriod
```

<span data-ttu-id="71ac6-111">取得訂閱的所有可用帳單週期。</span><span class="sxs-lookup"><span data-stu-id="71ac6-111">Get all available billing periods of the subscription.</span></span>

### <span data-ttu-id="71ac6-112">範例2</span><span class="sxs-lookup"><span data-stu-id="71ac6-112">Example 2</span></span>
```
PS C:\> Get-AzureRmBillingPeriod -Name 201704-1
```

<span data-ttu-id="71ac6-113">以指定名稱取得訂閱的帳單期限。</span><span class="sxs-lookup"><span data-stu-id="71ac6-113">Get the billing period of the subscription with the specified name.</span></span>

### <span data-ttu-id="71ac6-114">範例3</span><span class="sxs-lookup"><span data-stu-id="71ac6-114">Example 3</span></span>
```
PS C:\> Get-AzureRmBillingPeriod -MaxCount 2
```

<span data-ttu-id="71ac6-115">最多可以取得訂閱的2個帳單期間。</span><span class="sxs-lookup"><span data-stu-id="71ac6-115">Get at most 2 billing periods of the subscription.</span></span>

## <span data-ttu-id="71ac6-116">參數</span><span class="sxs-lookup"><span data-stu-id="71ac6-116">PARAMETERS</span></span>

### <span data-ttu-id="71ac6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71ac6-117">-DefaultProfile</span></span>
<span data-ttu-id="71ac6-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="71ac6-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="71ac6-119">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="71ac6-119">-MaxCount</span></span>
<span data-ttu-id="71ac6-120">決定要傳回的最大記錄數。</span><span class="sxs-lookup"><span data-stu-id="71ac6-120">Determine the maximum number of records to return.</span></span>

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

### <span data-ttu-id="71ac6-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="71ac6-121">-Name</span></span>
<span data-ttu-id="71ac6-122">要取得之特定帳單期間的名稱。</span><span class="sxs-lookup"><span data-stu-id="71ac6-122">Name of a specific billing period to get.</span></span>

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

### <span data-ttu-id="71ac6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71ac6-123">CommonParameters</span></span>
<span data-ttu-id="71ac6-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="71ac6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71ac6-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="71ac6-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71ac6-126">輸入</span><span class="sxs-lookup"><span data-stu-id="71ac6-126">INPUTS</span></span>

### <span data-ttu-id="71ac6-127">所有</span><span class="sxs-lookup"><span data-stu-id="71ac6-127">None</span></span>

## <span data-ttu-id="71ac6-128">輸出</span><span class="sxs-lookup"><span data-stu-id="71ac6-128">OUTPUTS</span></span>

### <span data-ttu-id="71ac6-129">[System.object]。清單 ' 1 [PSBillingPeriod，0.14.0.0，#... 帳單，版本 =，Culture = 中性，PublicKeyToken = null）]</span><span class="sxs-lookup"><span data-stu-id="71ac6-129">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod, Microsoft.Azure.Commands.Billing, Version=0.14.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="71ac6-130">PSBillingPeriod 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="71ac6-130">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span></span>

## <span data-ttu-id="71ac6-131">筆記</span><span class="sxs-lookup"><span data-stu-id="71ac6-131">NOTES</span></span>

## <span data-ttu-id="71ac6-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="71ac6-132">RELATED LINKS</span></span>

